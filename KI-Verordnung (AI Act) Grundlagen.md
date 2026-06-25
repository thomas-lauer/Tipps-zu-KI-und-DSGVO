# KI-Verordnung (EU AI Act) - Grundlagen

Stand: 25.06.2026

Dieses Dokument fasst die Grundlagen der EU-KI-Verordnung (AI Act) zusammen: Begriffe, Risikoklassen, Rollen, Pflichten, Transparenz, Sanktionen und Fristen. Es dient der Orientierung und ersetzt keine Rechtsberatung. Für rechtssichere Einzelfallaussagen sind spezialisierte Rechtsanwältinnen und Rechtsanwälte oder die zuständigen Aufsichtsbehörden heranzuziehen.

Die KI-VO ersetzt die DSGVO nicht. Beide müssen gleichzeitig beachtet werden. Den praktischen KI-VO-Kurzcheck enthält `Tipps zur DSGVO.md`, die Pflichten in der internen Richtlinie `KI Richtlinie für die KI Nutzung.md`.

## 1. Kontext

Die KI-Verordnung (AI Act) ist die EU-Verordnung 2024/1689 und seit August 2024 in Kraft. Sie reguliert KI nach ihrem Risikopotenzial und ist in 13 Kapiteln aufgebaut. Schwerpunkte sind:

- Einstufung von KI-Systemen in Risikoklassen
- Pflichten für Anbieter, Betreiber und weitere Rollen
- Anforderungen an KI-Modelle
- Haftung und Sanktionen bei Verstößen

Die KI-VO gilt als hochkomplex und bedeutet besonders für Selbstständige und KMU einen erheblichen Mehraufwand. Die praktische Umsetzung ist teilweise noch im Fluss.

Quellen: [AI Act Volltext](https://artificialintelligenceact.eu/), [AI Act Explorer](https://artificialintelligenceact.eu/ai-act-explorer/), [Small Businesses Guide to the AI Act](https://artificialintelligenceact.eu/small-businesses-guide-to-the-ai-act/), [IHK München AI-Act-Ratgeber](https://www.ihk-muenchen.de/ratgeber/digitalisierung/kuenstliche-intelligenz/ai-act/).

## 2. Abgrenzung zur DSGVO

Verarbeitet ein KI-System personenbezogene Daten (z. B. ein Bewerber-Tool), sind DSGVO und KI-VO parallel zu prüfen. Beide verfolgen unterschiedliche Schutzrichtungen: Eine Verarbeitung kann datenschutzrechtlich rechtmäßig sein und dennoch durch Bias diskriminierend wirken und damit gegen die KI-VO verstoßen. Die Einhaltung einer KI-VO-Pflicht ersetzt deshalb keine DSGVO-Prüfung und umgekehrt.

## 3. Risikomodell

Die KI-VO folgt einem risikobasierten Ansatz nach der Logik des Produktsicherheitsrechts: Je höher das Schadenspotenzial für Menschen, desto strenger die Anforderungen. Es gibt vier Stufen:

1. **Verbotene Praktiken** - unzulässige KI-Anwendungen nach Art. 5.
2. **Hochrisiko-KI** - zulässig, aber mit umfangreichen Pflichten; die Anwendungsfälle sind in Annex III aufgelistet.
3. **Begrenztes Risiko mit Transparenzpflichten** - nach Art. 50.
4. **Minimales Risiko** - keine besonderen Pflichten.

Quellen: [Art. 5 AI Act (verbotene Praktiken)](https://artificialintelligenceact.eu/de/article/5/), [Annex III (Hochrisiko)](https://artificialintelligenceact.eu/de/annex/3/), [Art. 50 AI Act (Transparenz)](https://artificialintelligenceact.eu/de/article/50/).

## 4. Definition: KI-System und Allzweck-KI

**KI-System** ist ein maschinengestütztes System, das für vom Menschen definierte Ziele autonom agiert und mittels maschinellen Lernens oder logikbasierter Ansätze Ausgaben wie Inhalte, Vorhersagen, Empfehlungen oder Entscheidungen erzeugt, die physische oder virtuelle Umgebungen beeinflussen können.

Beispiele:

- Chatbots und virtuelle Assistenten im Kundenservice
- Empfehlungssysteme für Produktvorschläge
- Bilderkennungssysteme in der Qualitätskontrolle
- Predictive Analytics für Umsatzprognosen

**Allzweck-KI-Modell (General Purpose AI Model, GPAI)** ist ein KI-Modell, das eine Vielzahl von Aufgaben erfüllen kann, in verschiedene Systeme und Anwendungen integrierbar ist und nicht auf einen eng definierten Anwendungsbereich beschränkt ist. Beispiele sind GPT, Claude, Gemini und Llama, die etwa für Texterstellung, Übersetzung, Programmierung und Analyse genutzt werden.

Quelle: [Art. 3 AI Act (Definitionen)](https://artificialintelligenceact.eu/de/article/3/).

## 5. Rolle: Anbieter

Anbieter ist, wer ein KI-System entwickelt oder entwickeln lässt und es unter eigenem Namen oder eigener Marke in der EU in Verkehr bringt, entgeltlich oder kostenlos.

Kernpflichten für Hochrisiko-KI-Systeme:

- **Risikomanagementsystem (Art. 9)** - einrichten, anwenden, dokumentieren und aufrechterhalten.
- **Datenqualität (Art. 10)** - Trainings-, Validierungs- und Testdatensätze müssen den Qualitätskriterien entsprechen.
- **Technische Dokumentation (Art. 11)** - muss vor dem Inverkehrbringen oder der Inbetriebnahme vorliegen.
- **Logging (Art. 12)** - automatische Protokollierung von Vorgängen und Ereignissen während des Betriebs.
- **Menschliche Aufsicht (Art. 14)** - wirksame Beaufsichtigung durch natürliche Personen.
- **Genauigkeit, Robustheit und Cybersicherheit (Art. 15)** - in angemessenem Maß über den gesamten Lebenszyklus.

Für Solo-Selbstständige und kleine KMU sind diese Anbieterpflichten kaum vollständig zu stemmen.

## 6. Rolle: Betreiber

Betreiber ist, wer ein KI-System unter eigener Verantwortung im Rahmen seiner beruflichen Tätigkeit einsetzt, etwa einen KI-Chatbot zur Vorsortierung von Kundenanfragen oder KI-Tools zur E-Mail-Klassifizierung und Dokumentzusammenfassung. Auch ohne Eigenentwicklung tragen Betreiber Verantwortung für den Einsatz.

Pflichten:

- **Anweisungen befolgen** - Nutzung gemäß Gebrauchsanweisung des Anbieters; Zweckentfremdung kann Haftungsprobleme auslösen.
- **Menschliche Aufsicht** - eine qualifizierte Person überwacht die KI-Ausgaben, besonders bei kritischen Entscheidungen.
- **Datenqualität sicherstellen** - Eingabedaten müssen zweckrelevant und ausreichend genau sein.
- **Überwachung im Betrieb** - bei Fehlern oder gefährlichen Ergebnissen den Betrieb unterbrechen und den Anbieter informieren.
- **Transparenz** - Nutzer informieren, wenn sie mit einer KI interagieren.

**Achtung Rollenwechsel:** Wer ein bestehendes System stark verändert oder es unter eigenem Namen bzw. Branding weitergibt, kann rechtlich vom Betreiber zum Anbieter hochgestuft werden, mit der vollen Last von technischer Dokumentation und Konformitätsbewertung.

## 7. Weitere Rollen

- **Bevollmächtigter** - in der EU ansässiger Vertreter, der im Auftrag eines Nicht-EU-Anbieters dessen KI-VO-Pflichten sicherstellt.
- **Importeur** - Person oder Firma, die ein KI-System aus einem Drittland in den EU-Markt einführt.
- **Produkthersteller / nachgeschalteter Anbieter** - integriert ein KI-System eines Drittanbieters (z. B. ein LLM) in ein eigenes Produkt oder passt es an und bringt es unter eigenem Namen in Verkehr. Dies ist eine häufige Rolle bei der Automatisierung mit bestehenden Modellen.

## 8. Transparenzverpflichtungen

Die allgemeinen Transparenzpflichten betreffen nahezu jeden Einsatz von KI-Tools und gelten ab dem 2. August 2026.

- **Interaktion mit KI** - Nutzer müssen wissen, dass sie mit einer KI interagieren; der Hinweis muss spätestens bei der ersten Interaktion klar erkennbar sein. Ausnahme: Es ist offensichtlich erkennbar, oder das System dient der Strafverfolgung.
- **Kennzeichnung synthetischer Inhalte** - Anbieter von KI, die Audio-, Bild-, Video- oder Textinhalte erzeugen, müssen sicherstellen, dass diese als künstlich erzeugt oder manipuliert erkennbar sind; dies gilt auch für GPAI-Modelle.
- **KI-generierte Texte zu Themen von öffentlichem Interesse** - Bei Texten zur Information der Öffentlichkeit über wichtige gesellschaftliche Themen besteht eine Offenlegungspflicht. Sie entfällt, wenn ein Mensch die Inhalte geprüft und die redaktionelle Verantwortung übernommen hat.

Quelle: [Art. 50 AI Act](https://artificialintelligenceact.eu/de/article/50/).

## 9. KI-Kompetenz und Schulung

Die KI-VO verlangt KI-Kompetenz bei den Personen, die KI-Systeme betreiben oder nutzen. Schulungen sollten sich an den technischen Kenntnissen, der Erfahrung, der Ausbildung, dem Nutzungskontext und den betroffenen Personengruppen orientieren und dokumentiert werden. Inhalte einer KI-Kompetenzschulung umfassen typischerweise erlaubte Tools, verbotene Daten, Output-Prüfung, Risiken von RAG und agentischer KI sowie Quellenkritik.

## 10. Sanktionen

Bei Verstößen drohen gestaffelte Bußgelder:

- **Verbotene KI-Praktiken (Art. 5)** - bis zu 35 Mio. Euro oder 7 % des weltweiten Jahresumsatzes.
- **Verletzung weiterer Vorschriften (z. B. Hochrisiko-KI)** - bis zu 15 Mio. Euro oder 3 %.
- **Nichteinhalten der GPAI-Vorschriften** - bis zu 15 Mio. Euro oder 3 %.
- **Falsche oder irreführende Angaben** - bis zu 7,5 Mio. Euro oder 1,5 %.

Für KMU und Startups gilt jeweils die niedrigere der beiden Grenzen.

Quelle: [AI Act Kapitel 5 (Sanktionen)](https://artificialintelligenceact.eu/de/chapter/5/).

## 11. Innovationsförderung

Die KI-VO enthält Maßnahmen zum Schutz der Wettbewerbsfähigkeit von KMU. Sie betreffen vor allem Kosten und Erprobung, ändern aber nichts an den Kernanforderungen zu Sicherheit und Robustheit:

- **Regulatorische Reallabore (Sandboxes)** - priorisierter, in der Regel kostenloser Zugang zur Erprobung in kontrollierter Umgebung, mit der Chance auf Rechtssicherheit vor Markteinführung.
- **Reduzierte Kosten und Gebühren** - ermäßigte Gebühren für Konformitätsbewertungen und Marktüberwachung sowie niedrigere Bußgeldschwellen.
- **Vereinfachte Dokumentation** - vereinfachte Formulare und Leitfäden für kleine Teams sind in Arbeit.

Praxis-Hinweis (Stand Januar 2026): Die Umsetzung ist bislang unvollständig. Sandboxes für Deutschland existieren noch nicht, und Leitfäden bzw. Dokumentationshilfen fehlen teilweise, obwohl einzelne Sanktionsregeln bereits greifen.

## 12. Zeitplan

Die KI-VO ist seit August 2024 in Kraft. Nach Art. 113 KI-VO gilt sie grundsätzlich ab dem 2. August 2026. Wichtige Zwischenschritte:

- Kapitel I und II (u. a. verbotene Praktiken, KI-Kompetenz) gelten seit dem 2. Februar 2025.
- Bestimmte GPAI-, Governance- und Sanktionsregeln gelten seit dem 2. August 2025.
- Die allgemeinen Transparenzpflichten nach Art. 50 gelten ab dem 2. August 2026.
- Pflichten für bestimmte Hochrisiko-Systeme nach Art. 6 Abs. 1 gelten ab dem 2. August 2027.

Quelle: [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113).

## 13. Erste Compliance-To-Dos

- KI-VO-Rolle bestimmen: Anbieter, Betreiber, Importeur, Bevollmächtigter oder Produkthersteller.
- Risikoklasse einstufen: verboten, Hochrisiko, begrenztes Risiko oder minimales Risiko.
- Verbotene Praktiken nach Art. 5 ausschließen.
- Transparenzpflichten nach Art. 50 für den eigenen Einsatzfall prüfen und umsetzen.
- KI-Kompetenz und Schulung sicherstellen und dokumentieren.
- Bei personenbezogenen Daten parallel die DSGVO prüfen (DSFA, Rechtsgrundlage, Betroffenenrechte).
- Bei Hochrisiko-Einsatz die Anbieterpflichten (Art. 9 bis 15) und eine mögliche Grundrechte-Folgenabschätzung nach Art. 27 KI-VO berücksichtigen.

## Quellen

- [AI Act Volltext](https://artificialintelligenceact.eu/)
- [AI Act Explorer](https://artificialintelligenceact.eu/ai-act-explorer/)
- [Small Businesses Guide to the AI Act](https://artificialintelligenceact.eu/small-businesses-guide-to-the-ai-act/)
- [IHK München AI-Act-Ratgeber](https://www.ihk-muenchen.de/ratgeber/digitalisierung/kuenstliche-intelligenz/ai-act/)
- [Art. 3 AI Act (Definitionen)](https://artificialintelligenceact.eu/de/article/3/)
- [Art. 5 AI Act (verbotene Praktiken)](https://artificialintelligenceact.eu/de/article/5/)
- [Annex III (Hochrisiko)](https://artificialintelligenceact.eu/de/annex/3/)
- [Art. 50 AI Act (Transparenz)](https://artificialintelligenceact.eu/de/article/50/)
- [AI Act Kapitel 5 (Sanktionen)](https://artificialintelligenceact.eu/de/chapter/5/)
- [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113)
