# DSGVO-Grundlagen für den KI-Einsatz

Stand: 25.06.2026

Dieses Dokument fasst die wichtigsten Grundlagen der Datenschutz-Grundverordnung (DSGVO) zusammen, die für die Entwicklung und Nutzung von KI-Systemen relevant sind. Es dient der Orientierung und ersetzt keine Rechtsberatung. Im Zweifelsfall ist eine spezialisierte Datenschutzfachkraft oder eine Rechtsanwältin bzw. ein Rechtsanwalt hinzuzuziehen.

Die praktischen Checklisten und Vorlagen finden sich in den übrigen Projektdateien. Dieses Dokument liefert das rechtliche Fundament dazu.

## 1. Kontext

Die DSGVO (englisch GDPR, General Data Protection Regulation) ist eine EU-Verordnung (2016/679) zum Schutz personenbezogener Daten. Sie wurde 2016 beschlossen und gilt seit dem 25.05.2018. Sie umfasst 11 Kapitel mit 99 Artikeln.

Geregelt werden insbesondere:

- Voraussetzungen und Regeln für die Verarbeitung personenbezogener Daten
- Rechte der betroffenen Personen
- Pflichten für Verantwortliche und Auftragsverarbeiter
- Haftung und Sanktionen bei Verstößen

In Deutschland wird die DSGVO durch das Bundesdatenschutzgesetz (BDSG) ergänzt.

Quellen: [DSGVO Volltext](https://dsgvo-gesetz.de/), [DSGVO Bußgeld-Datenbank](https://www.dsgvo-portal.de/dsgvo-bussgeld-datenbank/).

## 2. Personenbezogene Daten

Personenbezogene Daten sind nach Art. 4 Abs. 1 DSGVO alle Informationen, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen. Identifizierbar bedeutet direkt oder indirekt erkennbar, z. B. über Namen, Kennnummern, Standortdaten oder besondere Merkmale.

Beispiele:

- Name, Adresse, Telefonnummer, E-Mail-Adresse
- IP-Adressen, Standortdaten
- Kunden- und Kontonummern

### Besondere Kategorien (Art. 9 DSGVO)

Für besonders schützenswerte Daten gelten strengere Regeln. Dazu gehören:

- Gesundheitsdaten
- Daten zur sexuellen Orientierung oder zum Sexualleben
- biometrische und genetische Daten
- politische Meinungen
- religiöse oder weltanschauliche Überzeugungen
- Gewerkschaftszugehörigkeit
- ethnische oder rassische Herkunft

Die Verarbeitung dieser Daten ist grundsätzlich verboten, es sei denn, eine Ausnahme nach Art. 9 Abs. 2 DSGVO greift. Für den KI-Einsatz bedeutet das: Art.-9-Daten gehören nicht ohne ausdrückliche Rechtsgrundlage, DSFA und Freigabe in ein KI-System.

Quellen: [Art. 4 DSGVO](https://dsgvo-gesetz.de/art-4-dsgvo/), [Art. 9 DSGVO](https://dsgvo-gesetz.de/art-9-dsgvo/).

## 3. Was ist eine Datenverarbeitung?

Verarbeitung ist nach Art. 4 Abs. 2 DSGVO jeder Vorgang im Zusammenhang mit personenbezogenen Daten, mit oder ohne automatisierte Verfahren. Dazu zählen unter anderem:

- Erheben, Erfassen, Organisieren, Ordnen
- Speichern, Anpassen, Verändern
- Auslesen, Abfragen, Verwenden
- Offenlegen durch Übermittlung, Verbreitung oder andere Bereitstellung
- Abgleichen, Verknüpfen
- Einschränken, Löschen, Vernichten

Praktisch bedeutet das: Sobald personenbezogene Daten überhaupt in ein System gelangen, liegt eine Verarbeitung vor. Auch die Eingabe in ein KI-Tool oder das Hochladen einer Datei ist eine Verarbeitung im Sinne der DSGVO.

## 4. Grundsätze für die Verarbeitung

Art. 5 Abs. 1 DSGVO nennt sieben Grundsätze, die für jede Verarbeitung gelten:

1. **Rechtmäßigkeit, Verarbeitung nach Treu und Glauben, Transparenz** - Es braucht eine gesetzliche Grundlage; das Verhalten muss redlich sein; betroffene Personen müssen verstehen, was zu welchem Zweck mit ihren Daten geschieht.
2. **Zweckbindung** - Verarbeitung nur für den bei der Erhebung angegebenen konkreten Zweck.
3. **Datenminimierung** - Nur die tatsächlich notwendigen Daten verwenden.
4. **Richtigkeit** - Daten müssen inhaltlich richtig und aktuell sein; falsche Daten sind zu korrigieren oder zu löschen.
5. **Speicherbegrenzung** - Speicherung nur so lange, wie es für den Zweck erforderlich ist.
6. **Integrität und Vertraulichkeit** - Schutz vor unbefugtem Zugriff, Verlust und Manipulation durch technische und organisatorische Maßnahmen.
7. **Rechenschaftspflicht** - Der Verantwortliche muss die Einhaltung nachweisen können; Dokumentation ist zentral.

Diese Grundsätze sind der Maßstab, an dem auch jeder KI-Use-Case gemessen wird.

Quelle: [Art. 5 DSGVO](https://dsgvo-gesetz.de/).

## 5. Rechtmäßigkeit der Verarbeitung

Jede Verarbeitung braucht eine gültige Rechtsgrundlage nach Art. 6 Abs. 1 DSGVO. Ohne sie ist die Verarbeitung unzulässig, auch bei scheinbar harmlosen oder öffentlich zugänglichen Daten.

Mögliche Rechtsgrundlagen:

- **Einwilligung** - freiwillig, informiert und eindeutig; dokumentationspflichtig (z. B. Checkbox, Tastendruck, Unterschrift); jederzeit widerrufbar. Beispiel: Newsletter-Anmeldung.
- **Vertragserfüllung oder vorvertragliche Maßnahmen** - Beispiel: Online-Bestellung mit Versand an die Lieferadresse.
- **Erfüllung einer rechtlichen Verpflichtung** - z. B. Aufbewahrungspflichten nach Handels- und Steuerrecht.
- **Schutz lebenswichtiger Interessen** - nur in Ausnahmefällen, z. B. medizinische Notfälle; für IT- und Geschäftsprozesse meist irrelevant.
- **Wahrnehmung einer Aufgabe im öffentlichen Interesse** - vor allem für Behörden und hoheitliche Aufgaben. Beispiel: Ausstellung eines Personalausweises.
- **Berechtigtes Interesse** des Verantwortlichen oder eines Dritten - z. B. Betrugsprävention, IT-Sicherheit, Videoüberwachung; erfordert eine Interessenabwägung mit den Rechten der betroffenen Personen.

Die Auswahl und Begründung der Rechtsgrundlage ist zu dokumentieren. Im Zweifel mit einer Datenschutzfachkraft abstimmen.

Quelle: [Musterformulierung Interessenabwägung](https://dsgvo-vorlagen.de/interessenabwaegung-dsgvo-durchfuehren-musterformulierung).

## 6. Betroffenenrechte

Die DSGVO räumt betroffenen Personen umfassende Rechte ein (Art. 12 bis 23). Sie sollen erfahren können, welche Daten verarbeitet werden, woher diese stammen, wofür sie verwendet werden und wer Zugriff hat.

- **Informationspflichten (Art. 13, 14)** - Information bei der Erhebung sowie Benachrichtigung bei Speicherung; in der Praxis über die Datenschutzerklärung umgesetzt.
- **Auskunft (Art. 15)** - Bestätigung der Verarbeitung und Auskunft über Zweck, Datenkategorien, Empfänger und Herkunft.
- **Berichtigung (Art. 16)** - unverzügliche Korrektur falscher oder unvollständiger Daten.
- **Löschung / Recht auf Vergessenwerden (Art. 17)** - bei Wegfall der Erforderlichkeit, Widerruf der Einwilligung oder unrechtmäßiger Verarbeitung. Ausnahme: gesetzliche Aufbewahrungspflichten.
- **Einschränkung (Art. 18)** - bei zweifelhafter Richtigkeit oder unrechtmäßiger Verarbeitung.
- **Datenübertragbarkeit (Art. 20)** - Erhalt der Daten in einem maschinenlesbaren Format oder Übertragung an einen anderen Verantwortlichen.
- **Widerspruch (Art. 21)** - vor allem bei Verarbeitung im öffentlichen Interesse oder aufgrund berechtigten Interesses; nach erfolgreichem Widerspruch folgt Einstellung und ggf. Löschung.

### Datenschutzerklärung

Die Datenschutzerklärung steht nicht ausdrücklich in der DSGVO, hat sich aber zur Erfüllung der Informationspflichten (Art. 13, 14) und des Transparenzgebots durchgesetzt. Typische Inhalte:

- Verantwortlicher (inklusive Datenschutzbeauftragter, falls vorhanden)
- Datenkategorien
- Zweck und Rechtsgrundlage
- Weitergabe an Dritte inklusive Begründung
- Drittstaatenübermittlung
- Speicherdauer
- Betroffenenrechte
- Hinweis auf das Beschwerderecht bei der Aufsichtsbehörde

Generatoren können als Ausgangspunkt dienen, die finale Version sollte aber stets selbst geprüft und angepasst werden, bei Bedarf mit fachkundiger Unterstützung.

### Konsequenzen bei Verstößen

Verstöße können zu Abmahnungen durch Mitbewerber, Unterlassungsansprüchen, Bußgeldern (Art. 83 DSGVO) und Imageschäden führen.

Quellen: [Art. 13 DSGVO](https://dsgvo-gesetz.de/art-13-dsgvo/), [Art. 15 DSGVO](https://dsgvo-gesetz.de/art-15-dsgvo/), [Art. 16 DSGVO](https://dsgvo-gesetz.de/art-16-dsgvo/), [Art. 17 DSGVO](https://dsgvo-gesetz.de/art-17-dsgvo/), [Art. 18 DSGVO](https://dsgvo-gesetz.de/art-18-dsgvo/), [Art. 20 DSGVO](https://dsgvo-gesetz.de/art-20-dsgvo/), [Art. 21 DSGVO](https://dsgvo-gesetz.de/art-21-dsgvo/), [BfDI zum Widerspruchsrecht](https://www.bfdi.bund.de/DE/Buerger/Inhalte/Allgemein/Betroffenenrechte/Betroffenenrechte_Widerspruch.html).

## 7. Verzeichnis von Verarbeitungstätigkeiten (VVT)

Das Verzeichnis von Verarbeitungstätigkeiten nach Art. 30 DSGVO ist eines der wichtigsten Datenschutzdokumente. Es schafft Transparenz und Nachvollziehbarkeit, intern und gegenüber der Aufsichtsbehörde, und gibt einen strukturierten Überblick darüber, welche Daten wo, wie und zu welchem Zweck verarbeitet werden.

Das VVT ist nicht öffentlich, muss aber auf Anfrage der Datenschutzaufsicht vorgelegt werden.

Pflicht ist es grundsätzlich für jedes Unternehmen mit regelmäßiger Verarbeitung. Eine Ausnahme gilt nur für Kleinstunternehmen mit weniger als 250 Mitarbeitenden und ohne risikobehaftete Verarbeitung, was in der Praxis selten zutrifft.

Mindestinhalte nach Art. 30 DSGVO:

- Angaben zum Verantwortlichen (ggf. Datenschutzbeauftragter)
- Zweck der Verarbeitung
- Kategorien betroffener Personen
- Art der Daten
- Empfänger
- Drittlandübermittlungen
- Löschfristen
- technische und organisatorische Maßnahmen

Für KI-Verarbeitungen sollte das VVT entsprechend erweitert werden, etwa um genutzte KI-Tools, Anbieter, Datenkategorien und Drittlandtransfers.

Quellen: [VVT-Pflicht und Ausnahmen](https://www.dr-datenschutz.de/verzeichnis-von-verarbeitungstaetigkeiten-pflicht-mit-ausnahmen/), [BfDI-Vorlage VVT](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Allgemein/Verzeichnis-Verarbeitungstaetigkeiten.html).

## 8. Technische und organisatorische Maßnahmen (TOM)

Verantwortliche und Auftragsverarbeiter müssen nach Art. 24 und Art. 32 DSGVO geeignete technische und organisatorische Maßnahmen treffen, um ein angemessenes Schutzniveau sicherzustellen. Schutzziele sind Vertraulichkeit, Integrität, Verfügbarkeit und Belastbarkeit der Systeme und Dienste.

Konkrete Maßnahmen sind nicht vorgeschrieben (Technikoffenheit); die Auswahl liegt beim Verantwortlichen und kann für mehrere Verarbeitungszwecke wiederverwendet werden. Bei besonderem Risiko für die Rechte und Freiheiten der Betroffenen sind weiterreichende Maßnahmen erforderlich, was zur Frage einer Datenschutz-Folgenabschätzung führt.

Für KI-Systeme sind typische TOM unter anderem zentrale Business-Accounts, SSO/MFA, Rollen- und Berechtigungskonzepte, kurze Retention, Verschlüsselung sowie Prompt- und Upload-Regeln.

Quellen: [TOM-Checkliste LDA Bayern](https://www.lda.bayern.de/media/checkliste/baylda_checkliste_tom.pdf), [IHK TOM-Checkliste](https://www.ihk.de/blueprint/servlet/resource/blob/5310324/23f13456b5bf192eafe0f1de2847b42d/tom-massnahmen-datenschutz-data.pdf).

## 9. Auftragsverarbeitung (AVV / DPA)

Eine Auftragsverarbeitung nach Art. 28 DSGVO liegt vor, wenn ein externer Dienst (z. B. Hosting, Terminbuchung, Newsletter-Versand oder ein KI-Anbieter) personenbezogene Daten im Auftrag des Verantwortlichen verarbeitet.

In diesem Fall muss ein Auftragsverarbeitungsvertrag (AVV) abgeschlossen werden. Er regelt unter anderem:

- Gegenstand und Zweck der Verarbeitung
- Pflichten und Rechte beider Parteien
- technische und organisatorische Maßnahmen
- Löschung oder Rückgabe der Daten nach Ende der Zusammenarbeit
- mögliche Unterauftragsverhältnisse (Subprozessoren)

Ohne AVV ist die Zusammenarbeit nicht DSGVO-konform, auch bei einem seriösen Dienstleister. Die englische Bezeichnung lautet DPA (Data Processing Addendum oder Agreement). AVV bzw. DPA sind oft in die AGB eingebunden; sie sollten selbst geprüft werden, bei Bedarf ist ein eigener AVV anzufragen.

Quelle: [LfD Niedersachsen FAQ Auftragsverarbeitung](https://www.lfd.niedersachsen.de/faq/faq-auftragsverarbeitung-nach-artikel-28-dsgvo-189637.html).

## 10. Drittlandübermittlung

Drittländer sind Staaten außerhalb des Europäischen Wirtschaftsraums (EWR). Da viele KI-Anbieter US-nah sind oder internationale Infrastruktur nutzen, ist die Drittlandübermittlung nach Art. 44 bis 50 DSGVO ein zentrales Thema beim KI-Einsatz.

Zulässigkeitswege:

- **Angemessenheitsbeschluss** - Die EU-Kommission stellt ein ausreichendes Schutzniveau fest. Ein AVV/DPA bleibt trotzdem Pflicht.
- **Standardvertragsklauseln (SCC)** - bei fehlendem Angemessenheitsbeschluss als geeignete Garantie; verpflichten Datenexporteur und Datenimporteur zu einem angemessenen Schutzniveau. Die Garantien müssen durchsetzbar sein, weshalb ein Transfer Impact Assessment (TIA) erforderlich ist.
- **Ausnahmen nach Art. 49** - nur begründet und dokumentiert, nicht für regelmäßige Verarbeitung; z. B. ausdrückliche Einwilligung oder Vertragserfüllung.

Eine ausführliche Darstellung der USA-Problematik (Data Privacy Framework, Schrems-Urteile, US Cloud Act) sowie datenschutzorientierte LLM-Setups finden sich in der Datei `Drittlandtransfer in die USA - DPF, Schrems und Cloud Act.md`.

Quellen: [Art. 44 ff. DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [TIA-Leitfaden](https://www.dr-datenschutz.de/drittlanduebermittlung-leitfaden-zu-transfer-impact-assessments/), [EU-Kommission Angemessenheitsbeschlüsse](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en).

## Quellen

- [DSGVO Volltext](https://dsgvo-gesetz.de/)
- [DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [DSGVO Bußgeld-Datenbank](https://www.dsgvo-portal.de/dsgvo-bussgeld-datenbank/)
- [Art. 4 DSGVO](https://dsgvo-gesetz.de/art-4-dsgvo/)
- [Art. 9 DSGVO](https://dsgvo-gesetz.de/art-9-dsgvo/)
- [Musterformulierung Interessenabwägung](https://dsgvo-vorlagen.de/interessenabwaegung-dsgvo-durchfuehren-musterformulierung)
- [BfDI zum Widerspruchsrecht](https://www.bfdi.bund.de/DE/Buerger/Inhalte/Allgemein/Betroffenenrechte/Betroffenenrechte_Widerspruch.html)
- [VVT-Pflicht und Ausnahmen](https://www.dr-datenschutz.de/verzeichnis-von-verarbeitungstaetigkeiten-pflicht-mit-ausnahmen/)
- [BfDI-Vorlage VVT](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Allgemein/Verzeichnis-Verarbeitungstaetigkeiten.html)
- [TOM-Checkliste LDA Bayern](https://www.lda.bayern.de/media/checkliste/baylda_checkliste_tom.pdf)
- [IHK TOM-Checkliste](https://www.ihk.de/blueprint/servlet/resource/blob/5310324/23f13456b5bf192eafe0f1de2847b42d/tom-massnahmen-datenschutz-data.pdf)
- [LfD Niedersachsen FAQ Auftragsverarbeitung](https://www.lfd.niedersachsen.de/faq/faq-auftragsverarbeitung-nach-artikel-28-dsgvo-189637.html)
- [EU-Kommission Angemessenheitsbeschlüsse](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/adequacy-decisions_en)
