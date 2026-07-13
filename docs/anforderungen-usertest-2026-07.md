# Anforderungskatalog aus User-Test (Kollegin, 2026-07)

> Status: bewertet, noch NICHT umgesetzt. Bewertungslegende:
> ✅ übernehmen · 🟡 modifiziert übernehmen · 🔴 zurückstellen/ablehnen (mit Begründung)

## Bestätigte Stärken (beibehalten, nicht anfassen)

- Umfang & Fundierung der Datenbasis
- Radar-Chart („Spinnennetz") — entspricht Praxisanforderung beim Kunden
- Top-3-Empfehlungen + Quellenverweise
- Idee: Fragenkatalog transparent als Referenz → siehe A7

---

## A1 · Theme-Umschalter: „System" unverständlich — ✅ übernehmen (klein)

**Anforderung:** Begriff „System" ist nicht intuitiv.
**Bewertung:** Berechtigt — „System" ist Entwickler-Jargon. Lösung: Label „Auto"
mit Tooltip „folgt der Systemeinstellung (Windows/macOS)". Reihenfolge
Hell → Dunkel → Auto beibehalten (Konvention). Der Alternativvorschlag
„System hell-dunkel" wäre eher verwirrender.
**Aufwand:** 5 Min.

## A2 · Speichern/Laden wirkt wie Teil von „Angaben" — 🟡 modifiziert

**Anforderung:** Bereich in „Daten"/„Ausgabe" umbenennen.
**Bewertung:** Das Problem ist real (Leiste klebt optisch am Schritt 1), aber die
Diagnose führt in die Irre: Speichern/Laden gehört zu KEINEM Schritt — es wirkt
auf das gesamte Assessment. Den Schritt „Angaben" umzubenennen wäre falsch
(dort stehen ja wirklich Angaben). **Bessere Lösung:** Persist-Leiste visuell
als eigene Gruppe kennzeichnen, z. B. Beschriftung „Assessment-Stand:" vor den
Buttons + dezente Abgrenzung; alternativ in den Header verschieben.
**Aufwand:** 15 Min.

## A3 · Scoring-Skala erklären (4 Checkboxen → Score 5) — ✅ übernehmen

**Anforderung:** Irritation, dass 4 Kriterien zu Stufe 5 führen.
**Bewertung:** Voll berechtigt — der bestehende Hinweis „(Anzahl erfüllter
Kriterien + 1)" reicht offensichtlich nicht. Lösung: (a) Formulierung schärfen:
„0 Kriterien = Stufe 1 (Basis) … 4 Kriterien = Stufe 5", (b) in Schritt-Hilfe
und Kurzanleitung die Skala 1–5 explizit erklären (1 ist der Startwert, nicht 0
— es gibt kein „gar nichts", jede Organisation steht mindestens auf Stufe 1).
**Aufwand:** 15 Min.

## A4 · Frage „KI-Einsatz für Projekt freigegeben?" — 🟡 modifiziert

**Anforderung:** Explizite (potenziell redundante) Freigabe-Frage aufnehmen.
**Bewertung:** Als 25. Reifegrad-Frage falsch platziert — die Projektfreigabe
ist kein Reifemerkmal der Organisation, sondern **Kontext des konkreten
Assessments** (die Kollegin nennt die Redundanz selbst). Teilweise deckt
prozesse_4 (Freigabeprozess) das strukturelle Thema bereits ab.
**Bessere Lösung:** Checkbox/Feld in Schritt 1 „Angaben": „KI-Einsatz für
diesen Projektkontext freigegeben? (ja/nein/offen)" — erscheint als Meta-Info
im Report-Kopf. So ist es dokumentiert, ohne das Scoring zu verwässern.
**Aufwand:** 20 Min.

## A5 · Begriffstrennung Stakeholder vs. Mitarbeitende — 🟡 modifiziert, diskutieren!

**Anforderung:** Stakeholder (= Treiber wie GF/Vorstand) nicht synonym mit
Mitarbeitenden (= Betroffene) verwenden.
**Bewertung:** Das Präzisions-Anliegen ist berechtigt — Dimension 5 mischt
tatsächlich beide Gruppen. **Aber fachlicher Widerspruch zur vorgeschlagenen
Definition:** In der Change-/PM-Literatur (Freeman, PMI) umfasst „Stakeholder"
ALLE Anspruchsgruppen — Mitarbeitende sind Stakeholder. Die enge Lesart
„Stakeholder = nur Entscheider" ist verbreitet, aber nicht lehrbuchkonform;
sie in unser quellenbasiertes Tool zu übernehmen wäre inkonsistent.
**Bessere Lösung:** Nicht die Definition übernehmen, sondern die Fragen
präzisieren: je Frage benennen, WER gemeint ist („Führungsebene/Entscheider"
vs. „betroffene Mitarbeitende"). Ggf. Dimensionsuntertitel ergänzen:
„Entscheider und Betroffene". → Mit Kollegin rückkoppeln.
**Aufwand:** 30 Min. (Formulierungsarbeit)

## A6 · Positive vs. negative KI-Erfahrungen — ✅ übernehmen

**Anforderung:** Bei „Nutzen erlebbar" (stakeholder_4) differenzieren, ob
Erfahrungen positiv oder negativ sind.
**Bewertung:** Fachlich stark — negative Ersterfahrungen sind ein belegter
Adoptionskiller (Einstellung r=.72, TAM-Meta). Aktuell fragen die Kriterien
nur nach Erfolgsgeschichten; eine Organisation mit vielen schlechten
KI-Erfahrungen sähe fälschlich aus wie eine ohne Erfahrungen.
**Lösung:** Kriterium ergänzen/ersetzen: „Negative KI-Erfahrungen werden
systematisch erfasst und aufgearbeitet (nicht nur Erfolge kommuniziert)" +
Anker-Texte anpassen. Passt auch zur Fehlerkultur (Dimension 4) — Querverweis.
**Aufwand:** 20 Min.

## A7 · Fragenkatalog als Referenz — ✅ übernehmen (war schon positiv vermerkt)

**Lösung:** Aufklappbare Gesamtübersicht (analog Empfehlungs-Bibliothek) oder
Export des Fragenkatalogs (Druckansicht/CSV). Schlank: eigenes
Akkordeon „Fragenkatalog & Kriterien (Referenz)" in der Auswertung.
**Aufwand:** 30 Min.

## A8 · Fakten-Check EU-AI-Act-Datum — ✅ prüfen (nicht blind ändern!)

**Anforderung:** Datum zum AI Act wirkt fehlerhaft.
**Bewertung:** Ernst nehmen, aber NICHT ungeprüft ändern. Die Daten im Tool
(Art. 4 gilt seit 02.02.2025; VO (EU) 2024/1689 in Kraft seit 01.08.2024)
stammen aus der verifizierten Recherche und sind nach aktuellem Stand korrekt.
Möglicher Auslöser der Irritation: Die Digital-Omnibus-Verschiebung
(Hochrisiko-Fristen → Dez. 2027) ist politisch geeint, aber noch nicht
Amtsblatt-final — Fristen kursieren daher unterschiedlich.
**Lösung:** (a) Konkret bei Kollegin nachfragen, WELCHES Datum gemeint war;
(b) allen Rechtsangaben im Tool ein sichtbares „Rechtsstand: MM/JJJJ"-Label
geben — das beugt jeder künftigen Irritation vor und ist ohnehin Best Practice.
**Aufwand:** Prüfung 10 Min., Label 15 Min.

## A9 · Methoden-Transparenz (wie entstand die Datenbasis) — ✅ übernehmen

**Anforderung:** Nachvollziehbar machen, wie die Datenbasis entstand.
**Bewertung:** Sinnvoll und stärkt den USP (validierte statt behaupteter
Inhalte). Präzisierung fürs Protokoll: Der Workflow war Multi-Agenten-Recherche
mit adversarischer Verifikation (3 unabhängige Prüfinstanzen je Aussage,
25/25 bestätigt) plus separate Recherche zu Recht/Branchen — die Beschreibung
„Claude-Recherche + Gegenprüfung via Gemini" aus dem Transkript ist zu
vereinfacht/nicht ganz korrekt; vor Veröffentlichung sauber formulieren.
**Lösung:** Abschnitt „Über die Datenbasis" in der Kurzanleitung (Consultant)
+ Verweis auf docs/methodik-fundament.md.
**Aufwand:** 20 Min.

## A10 · Begründung der Modellwahl (warum Kotter, Errida & Lotfi, Pinto …) — ✅ übernehmen

*(Transkript-Korrektur: „Irida, Lottvieh" = Errida & Lotfi 2021.)*
**Bewertung:** Passt exakt zur Consultant-Zielgruppe; die Begründungen liegen
aus Paket 1 fertig vor (meistgenutzte Modelle lt. systematischem Review,
meta-analytisch validierte Adoptionstheorien, offizielle Standards).
**Lösung:** Kompakter Block „Warum diese Frameworks?" — 4–5 Sätze in der
Methoden-Transparenz-Sektion (zusammen mit A9 umsetzen).
**Aufwand:** in A9 enthalten.

---

## Priorisierte Umsetzungsreihenfolge (Vorschlag)

| Prio | Items | Charakter |
|---|---|---|
| 1 | A3, A1, A8 (Prüfung + Rechtsstand-Label) | Verständnis & Vertrauen, je < 20 Min. |
| 2 | A9 + A10, A2 | Transparenz, UI-Klarheit |
| 3 | A6, A4, A7 | Inhaltliche Schärfung |
| 4 | A5 (nach Rückkopplung mit Kollegin) | Begriffsarbeit, Abstimmung nötig |

**Rückfragen an die Kollegin vor Umsetzung:**
1. A8: Welches Datum genau wirkte falsch?
2. A5: Einverstanden mit „präzisieren statt umdefinieren" (Stakeholder-Begriff)?
