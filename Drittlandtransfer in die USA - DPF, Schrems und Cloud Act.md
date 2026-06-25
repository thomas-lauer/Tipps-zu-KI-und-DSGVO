# Drittlandtransfer in die USA - DPF, Schrems-Urteile und US Cloud Act

Stand: 25.06.2026

Dieses Dokument vertieft die Drittlandproblematik beim KI-Einsatz, insbesondere die Übermittlung personenbezogener Daten in die USA. Es erklärt die rechtlichen Hintergründe (Data Privacy Framework, Schrems-Urteile, US-Überwachungsrecht) und leitet daraus datenschutzorientierte LLM-Setups ab. Es dient der Orientierung und ersetzt keine Rechtsberatung.

Grundlagen zur Drittlandübermittlung finden sich in `DSGVO-Grundlagen.md`, die praktische Anbieter- und Transferprüfung in `Tipps zur DSGVO.md`.

## 1. Warum die USA ein Sonderfall sind

Viele KI- und SaaS-Anbieter wie Microsoft, Amazon, Google, Meta und OpenAI unterliegen US-Recht, selbst wenn ihre Rechenzentren in Europa stehen. Eine EU-Data-Residency-Zusage allein löst das Problem deshalb nicht automatisch, weil US-Behörden auch auf in Europa gespeicherte Daten zugreifen können.

Diese Konstellation steht im Spannungsverhältnis zu den DSGVO-Grundsätzen der Rechtmäßigkeit, Transparenz und Vertraulichkeit und erschwert die Nachvollziehbarkeit, die Kontrolle sowie die Ausübung der Betroffenenrechte.

## 2. Problematisches US-Recht

- **CLOUD Act (2018)** - Verpflichtet US-IT-Unternehmen zur Zusammenarbeit mit US-Behörden und sichert den Zugriff auf gespeicherte Daten, auch wenn diese außerhalb der USA gespeichert sind.
- **FISA Section 702 (Foreign Intelligence Surveillance Act)** - Ermöglicht US-Geheimdiensten den Zugriff auf Kommunikationsdaten nicht-US-amerikanischer Personen ohne richterliche Anordnung.
- **USA PATRIOT Act (2001) und USA Freedom Act (2015)** - Weitreichende Überwachungsbefugnisse, die auch gegenüber ausländischen Tochterunternehmen greifen können.
- **Executive Order 12333 (seit 1981)** - Grundlage für weltweite, anlasslose Überwachung durch US-Geheimdienste.

Quelle: [Überblick US-Geheimdienstrecht](https://www.kuketz-blog.de/jenseits-der-grenzen-ueberblick-ueber-das-us-geheimdienstrecht/).

## 3. Die Schrems-Urteile

Die Rechtsgrundlage für den EU-US-Datentransfer wurde mehrfach durch den Europäischen Gerichtshof gekippt:

- **Schrems I (Oktober 2015)** - Das Safe-Harbor-Abkommen wurde für ungültig erklärt.
- **Schrems II (Juli 2020)** - Auch das Nachfolgeabkommen Privacy Shield wurde gekippt.
- **EU-US Data Privacy Framework (seit Juli 2023)** - Aktueller Nachfolger, der den eingeschränkten Angemessenheitsbeschluss für die USA umsetzt.

Quelle: [America First - ist das Data Privacy Framework in Gefahr?](https://www.dr-datenschutz.de/america-first-ist-das-data-privacy-framework-in-gefahr/).

## 4. EU-US Data Privacy Framework (DPF)

Das EU-US Data Privacy Framework ist seit Juli 2023 in Kraft und ermöglicht die DSGVO-konforme Übermittlung personenbezogener Daten aus der EU an zertifizierte US-Unternehmen.

Wichtige Punkte:

- Die Zertifizierung ist freiwillig und erfolgt jährlich über das US-Handelsministerium.
- Ob ein Anbieter für einen konkreten Dienst zertifiziert ist, muss in der öffentlichen DPF-Liste geprüft werden.
- Nicht zertifizierte Unternehmen sind wie ein Drittlandtransfer ohne Angemessenheitsbeschluss zu behandeln. Dann sind erforderlich: Standardvertragsklauseln (SCC), ein Transfer Impact Assessment (TIA) zur Bewertung der US-Zugriffsrisiken sowie zusätzliche technische und organisatorische Maßnahmen (z. B. Verschlüsselung, Anonymisierung, Pseudonymisierung).

**Risikobewertung:** Die Stabilität des DPF gilt als unsicher. Verbesserungen des US-Datenschutzes sind derzeit eher unwahrscheinlich, relevante Aufsichtsgremien werden geschwächt, und weitere Klagen europäischer Datenschutzorganisationen sind anhängig. Empfehlung: Angemessenheitsbeschlüsse regelmäßig kontrollieren, frühzeitig Alternativen prüfen und betroffene Dienste bei Bedarf vermeiden.

Quellen: [Data Privacy Framework List](https://www.dataprivacyframework.gov/list), [Heise zum DPF und politischen Risiken](https://www.heise.de/hintergrund/Nach-Trump-Entscheidung-Kippt-das-Abkommen-fuer-Datenuebermittlungen-in-die-USA-10260045.html).

## 5. Länder mit Angemessenheitsbeschluss

Für eine Reihe von Ländern hat die EU-Kommission ein angemessenes Schutzniveau festgestellt. Zum Stand 6. Juli 2025 zählen dazu: Andorra, Argentinien, Färöer-Inseln, Guernsey, Isle of Man, Israel (eingeschränkt), Japan, Jersey, Kanada (eingeschränkt), Neuseeland, Schweiz, Südkorea, Uruguay, Vereinigtes Königreich (eingeschränkt) und USA (eingeschränkt, über das DPF).

Auch bei einem Angemessenheitsbeschluss bleibt ein AVV/DPA Pflicht. Die Liste wird regelmäßig überprüft und sollte vor einer Anbieterentscheidung aktuell kontrolliert werden.

Quellen: [EU-Kommission Angemessenheitsbeschlüsse](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en), [LDI NRW zum Angemessenheitsbeschluss](https://www.ldi.nrw.de/datenschutz/internationaler-datenverkehr/angemessenheitsbeschluss), [Datenschutz Hessen zu Angemessenheitsbeschlüssen](https://datenschutz.hessen.de/datenschutz/internationaler-datentransfer/angemessenheitsbeschluesse-der-europaeischen-kommission).

## 6. Transfer Impact Assessment (TIA)

Wenn ein Transfer auf Standardvertragsklauseln gestützt wird, ist ein Transfer Impact Assessment erforderlich. Es bewertet, ob die vertraglichen Garantien im Zielland tatsächlich durchsetzbar sind und welche staatlichen Zugriffsrisiken bestehen, und legt zusätzliche Maßnahmen fest.

Quellen: [TIA-Leitfaden](https://www.dr-datenschutz.de/drittlanduebermittlung-leitfaden-zu-transfer-impact-assessments/), [TIA-Vorlagen (IAPP)](https://iapp.org/resources/article/transfer-impact-assessment-templates/).

## 7. DSGVO-orientierte LLM-Setups

Eine praktische Daumenregel: Je weiter personenbezogene Daten geografisch wandern, desto größer wird der regulatorische Aufwand. Bei einem Transfer in die USA oder andere Drittländer müssen Angemessenheitsbeschlüsse, Standardvertragsklauseln, ein TIA und gegebenenfalls zusätzliche technische Maßnahmen wie Verschlüsselung oder Pseudonymisierung geprüft werden.

Zur Risikominimierung sprechen daher viele Argumente für lokale oder EU-basierte Lösungen:

- **Lokale Modelle** - Verarbeitung im eigenen Haus, kein Drittlandtransfer; allerdings höherer initialer Aufwand und meist geringere Leistungsfähigkeit als führende Cloud-Modelle.
- **EU-gehostete Modelle** - Cloud-Modelle, die in EU-Rechenzentren betrieben werden. Beispielsweise lassen sich über Azure OpenAI Services GPT-Modelle in einer EU-Region bereitstellen und in Automatisierungs-Plattformen einbinden; dabei sind die Anbieter-Credentials sorgfältig zu konfigurieren.

Wichtig: Auch bei EU-Hosting bleibt zu prüfen, ob der Anbieter US-Recht unterliegt (siehe Abschnitt 1 und 2). EU-Region und Zertifizierung verringern das Risiko, beseitigen aber nicht automatisch jeden Zugriff durch Drittstaaten. Die Bewertung muss anbieter-, plan- und funktionsbezogen erfolgen und im Transfer Impact Assessment dokumentiert werden.

## Quellen

- [Art. 44 ff. DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [Data Privacy Framework List](https://www.dataprivacyframework.gov/list)
- [EU-Kommission Angemessenheitsbeschlüsse](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en)
- [LDI NRW zum Angemessenheitsbeschluss](https://www.ldi.nrw.de/datenschutz/internationaler-datenverkehr/angemessenheitsbeschluss)
- [Datenschutz Hessen zu Angemessenheitsbeschlüssen](https://datenschutz.hessen.de/datenschutz/internationaler-datentransfer/angemessenheitsbeschluesse-der-europaeischen-kommission)
- [TIA-Leitfaden](https://www.dr-datenschutz.de/drittlanduebermittlung-leitfaden-zu-transfer-impact-assessments/)
- [TIA-Vorlagen (IAPP)](https://iapp.org/resources/article/transfer-impact-assessment-templates/)
- [America First - ist das Data Privacy Framework in Gefahr?](https://www.dr-datenschutz.de/america-first-ist-das-data-privacy-framework-in-gefahr/)
- [Heise zum DPF und politischen Risiken](https://www.heise.de/hintergrund/Nach-Trump-Entscheidung-Kippt-das-Abkommen-fuer-Datenuebermittlungen-in-die-USA-10260045.html)
- [Überblick US-Geheimdienstrecht](https://www.kuketz-blog.de/jenseits-der-grenzen-ueberblick-ueber-das-us-geheimdienstrecht/)
