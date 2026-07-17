# Anforderungskatalog B aus User-Test 2 (Beraterin, Change-/Governance-Kontext, 2026-07-17)

> 21-Min.-Test per Screensharing, lautes Denken. Bewertung: ✅ übernehmen · 🟡 modifiziert · 🔴 zurückstellen.
> Abgleich mit Katalog A (User-Test 1, docs/anforderungen-usertest-2026-07.md) am Ende.

## Bestätigte Stärken

- **Checkbox→Bewertung-Automatik:** „irgendwas Neues – dass aus dem, was man anklickt, direkt eine Bewertung generiert wird, finde ich gut"
- **Fokus-Funktion des Reports:** erkennt sofort Defizit-Dimensionen („kann schnell den Fokus drauflegen, wo Defizite vorhanden sind"), lobt Strukturierung
- **Reifegrad-Visualisierung:** „hilft sofort, sich einen Überblick zu verschaffen"
- **Übergangs-Hinweise** („Richtung Stufe 3"): „sehr anschaulich"
- **Datenbasis:** erkennt Kotter/Lewin wieder, „sehr interessant, was er da rauszieht"; EU AI Act + DSGVO positiv registriert
- **Nutzen als Doku-/Checklisten-Grundlage** für den Projektfortschritt

---

## B1 · Einstiegstext zu lang — ✅ übernehmen
Erste Reaktion auf die Kurzanleitung: „sehr viel Text … die Leute lesen das dann nicht."
**Bewertung:** Deckt sich mit bekannter Lektion (Guiding statt Textwand). Kurzanleitung straffen: 3 Schritte auf je 1 Zeile kürzen, Meta-Block (Wozu/Für wen/USP) einklappbar machen. *Aufwand: 30 Min.*

## B2 · Skala „Warum nicht bei 0?" — 🟡 Wirkung des A3-Fixes prüfen
Identische Irritation wie in Test 1 (A3) — **obwohl der A3-Fix beim Test bereits live war**. Nach mündlicher Erklärung sofort akzeptiert („Ja, OK, alles in Ordnung").
**Bewertung:** Der Hinweis in der Score-Zeile wird offenbar erst nach der Irritation gelesen. Option: Skalen-Erklärung prominenter an die erste Frage (einmaliger Hinweis-Banner in der Erhebung) statt nur im Kleingedruckten. *Aufwand: 20 Min.*

## B3 · Beobachtung vs. Bewertung inkonsistent — ✅ übernehmen (Erklärlücke)
Erwartung: Freitext-Beobachtungen fließen in die Bewertung ein („dann wäre es einheitlicher: Beobachtung → Bewertung auch bei individueller Angabe").
**Bewertung:** Genau das TUT der Agent (Feature „Notizen analysieren") — aber ohne Agent-Verbindung ist der Zusammenhang unsichtbar. Lösung: Hinweis am Notizfeld („Mit Agent-Verbindung werden Beobachtungen automatisch gegen die Kriterien geprüft"), Button auch ohne Verbindung sichtbar (deaktiviert mit Tooltip). *Aufwand: 20 Min.*

## B4 · Erhebung textlastig / Voice als Alternative — 🟡 Backlog (validiert Option 4)
„Viel zum Lesen, kostet Zeit" + zur Voice-Idee: „kann man auf jeden Fall als Alternative mit anbieten und schauen, wie sehr das genutzt wird."
**Bewertung:** Zweite unabhängige Bestätigung für den Voice-/Interview-Copiloten (Agentik-Option 4, auch FK-Wunsch bei adnetwork). Bleibt Backlog — Aufwand hoch. Kurzfristig hilft B1/B10 gegen Textlast.

## B5 · Speichern/Laden-Verortung unklar — ✅ Priorität hoch (= A2!)
„Der Button war auch vorher … das wäre für mich noch unklar" — exakt dieselbe Verwirrung wie in Test 1.
**Bewertung:** Zwei von zwei Testerinnen → nicht diskutabel, umsetzen. Lösung wie in A2 geplant: Leiste als eigene Gruppe beschriften („Assessment-Stand: 💾 …") + Tooltip „gilt für das gesamte Assessment, nicht nur diesen Schritt". *Aufwand: 15 Min.*

## B6 · Top-3 zu exklusiv — Empfehlungen aller Dimensionen sichtbar — ✅ übernehmen
„Top 3 weiß ich nicht, ob das so super ist … ich würde direkt gerne das Gleiche mit den anderen sehen können."
**Bewertung:** Berechtigt — aktuell springt man von Top-3 in die (anders aussehende) Bibliothek. Lösung: In jeder Dimensions-Karte die Empfehlungen der aktuellen Stufe direkt anzeigen (aufklappbar), gleiche Darstellung wie Top-3. Top-3 bleibt als Priorisierung erhalten. *Aufwand: 45 Min.*

## B7 · Drilldown je Dimension — 🟡 Backlog
Wunsch: in eine Dimension „reinklicken" und die Verteilung der Einzelfragen sehen („vielseitigeres Dashboard").
**Bewertung:** Sinnvoll, aber die Daten stehen bereits als Frage-Aufschlüsselung in der Karte (qbreak) — das Problem ist eher Darstellung (siehe B10). Erst B10 umsetzen, dann prüfen, ob der Wunsch bleibt. Voller Drilldown (Balken je Frage) = Backlog.

## B8 · Verlaufs-Vergleich („Was hat sich getan?") — ✅ Backlog-Aufwertung
„Ich möchte so eine Entwicklung sehen … wo stehe ich in ein paar Wochen oder Monaten … Das fände ich ganz gut." Plus: gute Transparenz-Basis gegenüber Auftraggebenden.
**Bewertung:** Zweite unabhängige Bestätigung des Delta-Vergleichs aus unserem Backlog — von „Idee" auf „validierter Bedarf" hochstufen. Technisch vorbereitet (JSON-Snapshots existieren). *Nächster größerer Inhalts-Sprint.*

## B9 · Empfehlungen als abhakbare Checkliste — ✅ in Maßnahmenplan integrieren
„Daraus eine Checkliste generieren: Punkt 1 erledigt, Punkt 2 noch nicht."
**Bewertung:** Deckt sich mit dem gerade gebauten Maßnahmenplan-Agenten — dort Checkboxen je Maßnahme ergänzen (Status: offen/erledigt, wird mitgespeichert). *Aufwand: 30 Min., auf Branch massnahmenplan-agent aufsetzen.*

## B10 · „Auswertungsgrundlage" braucht Überschrift + Blockbildung — ✅ übernehmen
Die Frage-Aufschlüsselung in den Dimensions-Karten „geht unter … hier fehlt einfach eine Überschrift"; Wunsch: als abgesetzter Block mit Label (z. B. „Auswertungsgrundlage") und Rahmen.
**Bewertung:** Klein, klar, sofort machbar. Auch Empfehlungs-Label ergänzen („Empfehlung für Stufe X"). *Aufwand: 20 Min.*

## B11 · Dimensionsname „Widerstände" irritiert bei hohem Score — 🟡 beobachten
„Wenn ich höre Widerstände, ist das ja … muss ich weiterlesen" (hoher Reifegrad bei „Widerstände" klingt zunächst negativ).
**Bewertung:** Einmal-Irritation, nach Lesen ok. Option: Untertitel schärfen („Umgang mit Widerständen" statt „Widerstände"). Mit Testerin A5-Rückkopplung bündeln (betrifft dieselbe Begriffsschärfung in Dim. 5/6). *Kein Sofort-Fix.*

## B12 · DORA vermisst — ✅ klein ergänzen
„Mir fehlt zwar jetzt die DORA-Sache, aber er hat den EU AI Act drin."
**Bewertung:** DORA steht bereits im Branchenprofil Banken — war unsichtbar, weil keine Bank-Branche gewählt. Lösung: DORA als Quelle ins Register + Erwähnung im Rechtsstand-Hinweis („sektorspezifisch z. B. DORA über Branchenprofil"). *Aufwand: 15 Min.*

## B13 · Quellen-Chips anfangs irritierend — ✅ mit B10 erledigt
„Warum zieht der hier? … ein bisschen irritierend am Anfang" — nach Erklärung: „dann ignoriert man die Referenzen erstmal und liest die Texte."
**Bewertung:** Kein Entfernen (Testerin A lobte die Quellen ausdrücklich!), sondern Kontext: kleines Label „Quellen:" vor den Chips bzw. Hinweis in der Bibliothek. *Aufwand: 10 Min.*

---

## Abgleich Katalog A (Test 1) × Katalog B (Test 2)

| Thema | A | B | Konsequenz |
|---|---|---|---|
| **Speichern/Laden-Verortung** | A2 | B5 | ⭐ 2/2 Testerinnen → höchste Priorität im nächsten UI-Fix |
| **Skala 1–5 statt 0** | A3 | B2 | 2/2 — A3-Fix reicht nicht, prominenter platzieren |
| **Quellen/Methodik-Transparenz** | A9/A10 (gewünscht) | B13 (anfangs irritierend, dann geschätzt) | Transparenz behalten, aber mit Kontext-Label einführen |
| **Datenbasis-Lob** | ✔ „immens, fundiert" | ✔ „sehr interessant, was er rauszieht" | USP bestätigt — für PPTX |
| **Radar/Visualisierung-Lob** | ✔ „entspricht Praxis beim Kunden" | ✔ „hilft sofort beim Überblick" | Kern-Feature bestätigt — für PPTX |
| **Rechtlicher Rahmen** | A8 (Datum prüfen) | B12 (DORA ergänzen) | Rechts-Layer wird aktiv genutzt/geprüft → Pflege-Agent-Story! |
| **Verlaufs-Vergleich** | – | B8 | Delta-Vergleich von Backlog-Idee zu validiertem Bedarf |
| **Checkliste/Maßnahmen nachhalten** | – | B9 | Bestätigt Maßnahmenplan-Agent, Checkbox-Ausbau |
| Nur A: Begriffe (A5), KI-Freigabe (A4), pos./neg. Erfahrung (A6) | A4–A6 | – | wie geplant Sprint 3 |
| Nur B: Top-3-Exklusivität (B6), Blockbildung (B10), Intro-Länge (B1) | – | B1/B6/B10 | in Sprint 3 aufnehmen |

## Aktualisierte Umsetzungsreihenfolge (Sprint 3)

1. **B5/A2** Persist-Leiste beschriften · **B10** Auswertungsgrundlage-Block · **B13** Quellen-Label · **B12** DORA *(zusammen ~1 h)*
2. **B2/A3** Skalen-Hinweis prominent · **B1** Intro straffen · **B3** Beobachtung→Bewertung erklären
3. **B6** Empfehlungen je Dimensions-Karte · **B9** Checkboxen im Maßnahmenplan · **A6** pos./neg. Erfahrungen · **A4** Freigabe-Meta-Feld · **A7** Fragenkatalog-Referenz
4. Nach Rückkopplung: **A5/B11** Begriffsschärfung · dann **B8** Delta-Vergleich als eigener Sprint
