# Datensicherheitskonzept – KI-Reifegrad-Assessment

> Zielszenario (Entscheidung 2026-07-10): **Öffentliche URL mit Passwort-Gate**.
> Status: Entwurf zur Abstimmung mit dem Kollegen / ggf. adesso-interner Freigabe.

## 1. Architektur & Datenflüsse (Ist-Analyse)

Das Tool ist eine rein clientseitige Single-File-Webanwendung: **kein Backend,
keine Datenbank, keine serverseitige Speicherung oder Übertragung**. Eingaben
(Kundenname, Fachbereich, Bewertungen, Interview-Notizen) existieren nur im
Arbeitsspeicher des Browser-Tabs und sind beim Schließen/Reload verloren.

Reale Datenabflüsse:

| # | Pfad | Daten | Bewertung |
|---|------|-------|-----------|
| 1 | **LLM-Agent (optional)** – „Notizen analysieren", „Frage vorschlagen", „Zusammenfassung" | Kundenname, Branche, Scores, **vollständige Freitext-Notizen** an Anthropic-API oder konfigurierten Endpunkt | ⚠️ Kritischster Pfad. Notizen können personenbezogene Daten von Mitarbeitenden des Kunden enthalten → DSGVO-relevant |
| 2 | **Exporte** – „Text kopieren", Druck/PDF | Vollständiger Report | Zwischenablage/Dateisystem des Consultant-Geräts; übliche Dokumenten-Policies gelten |
| 3 | **Chart.js via cdnjs (Cloudflare)** | Nur IP/User-Agent des Nutzers (kein Inhalt) | Gering; Option: Self-Hosting der Library (Tool hat bereits Fallback ohne CDN) |
| 4 | *(geplant)* Persistenz | Assessment-Daten auf Consultant-Gerät | Siehe Abschnitt 4 – Konzept VOR Implementierung |

## 2. Schutzbedarf

- **Kundenname + Assessment-Ergebnisse:** vertraulich (Geschäftsgeheimnis des Kunden, Beratungsverhältnis).
- **Interview-Notizen:** potenziell personenbezogene Daten Dritter (Beschäftigte des Kunden) → höchster Schutzbedarf im Tool.
- Das Tool selbst (Fragen, Empfehlungen, Quellen) ist **nicht schutzbedürftig** — es enthält keine Daten.

## 3. Maßnahmen für das Zielszenario „Öffentliche URL + Passwort-Gate"

### 3.1 Zugangsschutz
- Passwort-Gate vor der Anwendung (clientseitig, analog adnetwork-Ansatz).
- **Ehrliche Einordnung:** Ein clientseitiges Gate schützt den *Zugang zum Tool*
  (Marke, unbefugte Nutzung), nicht die *Kundendaten* — die liegen ohnehin nie
  auf dem Server. Der eigentliche Datenschutz kommt aus der No-Backend-Architektur.
- Auslieferung ausschließlich über HTTPS (bei GitHub Pages Standard).

### 3.2 LLM-Pfad (wichtigste Regeln)
1. **Für Assessments mit echten Kundendaten nur freigegebene Endpunkte** nutzen
   (interner/adesso-GPT-Endpunkt statt persönlichem Anthropic-Key). Der direkte
   Anthropic-Modus bleibt für Demos/Tests ohne Realdaten.
2. **Notiz-Hygiene:** Keine Klarnamen oder identifizierende Angaben zu
   Mitarbeitenden des Kunden in Freitextnotizen (Rollen statt Namen:
   „Teamleiter Vertrieb" statt „Herr Müller"). Hinweis dazu direkt im Tool (umgesetzt).
3. **AVV/Auftragsverarbeitung klären**, bevor der LLM-Pfad mit Realdaten
   freigegeben wird (adesso-interner Prozess; bei Anthropic: DPA + EU-Datenregion prüfen).
4. Keys bleiben wie bisher nur im RAM (kein localStorage) — beibehalten.

### 3.3 Repo-/Deployment-Hygiene
- **Niemals echte Kundendaten ins Repo** (auch nicht in Screenshots, Beispiel-JSONs, Commits).
- Demo-/Beispieldaten klar fiktiv benennen („Mustermann GmbH").
- Docs (Recherche, Konzepte) sind unkritisch und können im Repo bleiben.

### 3.4 Exporte
- Bestehende Praxis beibehalten; Reports unterliegen der üblichen
  Dokumentenklassifizierung (vertraulich, Kundenkontext).

## 4. Geplante Persistenz — Vorgaben (vor Implementierung)

- **JSON-Export/-Import als Datei** statt stillem `localStorage`:
  Speichern ist ein bewusster Akt, der Speicherort ist sichtbar und liegt auf
  dem (firmenverschlüsselten) Gerät des Consultants.
- Falls zusätzlich localStorage als Komfort-Zwischenspeicher: nur mit sichtbarem
  Indikator + „Lokale Daten löschen"-Button; keine API-Keys, niemals.
- Export-Dateiname ohne Kundennamen als Default anbieten (z. B. Datum + Kürzel).

## 5. Offene Punkte

- [ ] Abstimmung mit Kollege (sebastiangei) über Zielszenario & Gate-Mechanik
- [ ] adesso-interne Freigabe für LLM-Endpunkt mit Kundendaten (AVV)
- [ ] Entscheidung Chart.js: CDN belassen vs. einbetten (Offline-Fähigkeit + ein Datenabfluss weniger)
- [ ] Passwort-Gate implementieren (bei Deployment, nicht vorher nötig)
