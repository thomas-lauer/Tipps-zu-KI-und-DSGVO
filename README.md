# Tipps zu KI und DSGVO

Dieses Repository sammelt praktische Vorlagen und Hinweise zur datenschutzkonformen Nutzung von KI-Systemen wie Claude, ChatGPT/OpenAI, API-Diensten, RAG-Systemen und vergleichbaren Tools.

## Inhalt

### Tipps zur DSGVO.md

Datei: [Tipps zur DSGVO.md](./Tipps%20zur%20DSGVO.md)

Enthält eine praktische Checkliste für den Einsatz generativer KI. Behandelt werden unter anderem erlaubte und riskante Datenarten, Account-Auswahl, AVV/DPA, Training/Model Improvement, Speicherfristen, Drittlandtransfer, DSFA-Prüfung, automatisierte Entscheidungen, RAG-Systeme, Anbieterprüfung und sofort umsetzbare Praxisregeln.

### Datenschutz-Folgenabschätzung Vorlage KI Nutzung.md

Datei: [Datenschutz-Folgenabschätzung Vorlage KI Nutzung.md](./Datenschutz-Folgenabsch%C3%A4tzung%20Vorlage%20KI%20Nutzung.md)

Enthält eine ausfüllbare Vorlage für eine Datenschutz-Folgenabschätzung nach Art. 35 DSGVO bei KI-Nutzung. Die Vorlage führt durch Stammdaten, Schwellwertanalyse, Datenkategorien, Rechtsgrundlagen, Anbieter- und Vertragsprüfung, Notwendigkeit und Verhältnismäßigkeit, Datenschutzgrundsätze, Risikoanalyse, technische und organisatorische Maßnahmen, Betroffenenrechte, Freigabeentscheidung und Review.

### KI Richtlinie für die KI Nutzung.md

Datei: [KI Richtlinie für die KI Nutzung.md](./KI%20Richtlinie%20f%C3%BCr%20die%20KI%20Nutzung.md)

Enthält eine Vorlage für eine interne KI-Nutzungsrichtlinie. Sie beschreibt Geltungsbereich, zugelassene Tools, verbotene Eingaben, Standardnutzungen, Eingabe- und Output-Regeln, Regeln zu automatisierten Entscheidungen, agentischer KI, RAG-Systemen, Beschaffung/Freigabe, DSFA, Transparenz, Sicherheitsvorfällen, Schulung, Kontrolle und Review.

### DSGVO-Grundlagen.md

Datei: [DSGVO-Grundlagen.md](./DSGVO-Grundlagen.md)

Enthält das rechtliche Fundament zu den praktischen Checklisten: Kontext und Aufbau der DSGVO, personenbezogene und besondere Daten (Art. 4, 9), Definition der Verarbeitung, die sieben Verarbeitungsgrundsätze (Art. 5), Rechtsgrundlagen (Art. 6), Betroffenenrechte und Datenschutzerklärung (Art. 12 bis 23), Verzeichnis von Verarbeitungstätigkeiten (Art. 30), technische und organisatorische Maßnahmen (Art. 24, 32), Auftragsverarbeitung/AVV/DPA (Art. 28) und die Grundlagen der Drittlandübermittlung (Art. 44 ff.).

### Drittlandtransfer in die USA - DPF, Schrems und Cloud Act.md

Datei: [Drittlandtransfer in die USA - DPF, Schrems und Cloud Act.md](./Drittlandtransfer%20in%20die%20USA%20-%20DPF%2C%20Schrems%20und%20Cloud%20Act.md)

Vertieft die USA-Drittlandproblematik: problematisches US-Recht (CLOUD Act, FISA 702, PATRIOT/Freedom Act, Executive Order 12333), die Schrems-Urteile, das EU-US Data Privacy Framework, die Länderliste mit Angemessenheitsbeschluss, das Transfer Impact Assessment sowie datenschutzorientierte LLM-Setups mit lokalen und EU-gehosteten Modellen.

### KI-Verordnung (AI Act) Grundlagen.md

Datei: [KI-Verordnung (AI Act) Grundlagen.md](./KI-Verordnung%20%28AI%20Act%29%20Grundlagen.md)

Enthält die Grundlagen der EU-KI-Verordnung: Kontext und Aufbau, Abgrenzung zur DSGVO, das vierstufige Risikomodell, Definition von KI-System und Allzweck-KI (Art. 3), die Rollen Anbieter, Betreiber, Importeur, Bevollmächtigter und Produkthersteller inklusive Rollenwechsel, Anbieterpflichten (Art. 9 bis 15), Transparenzverpflichtungen (Art. 50), KI-Kompetenz, Sanktionen, Innovationsförderung, Zeitplan und erste Compliance-To-Dos.

## Version

Aktuelle Version: 1.7.1
Stand: 10.07.2026

## Versionsinfo

### Version 1.7.1 - 10.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um den neuen Art.-50-KI-VO-Nachweisstand ergänzt: Die EU-Kommission bewertet den Transparency Code seit dem 09.07.2026 als angemessenes freiwilliges Instrument; der AI Board hat die Angemessenheitsbewertung am Folgetag übernommen. Das kann als belastbarer Compliance-Baustein dokumentiert werden, ersetzt aber keine Einzelfallprüfung ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Geändert:

- KI-VO-Transparenzhinweise präzisiert: Eine Unterzeichnung des freiwilligen Codes ist nun als EU-weit anerkanntes Hilfsmittel darstellbar, begründet laut Kommission aber keinen abschließenden Compliance-Nachweis und ersetzt keine konkrete Pflichtenumsetzung nach Art. 50 KI-VO ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.7.0 - 09.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um EDPB-Entwurfsleitlinien vom 07./08.07.2026 zu Web Scraping für generative KI ergänzt: Öffentlich zugängliche Webdaten sind nicht frei für KI-Training oder Fine-Tuning nutzbar; Rechtsgrundlage, Zweckbindung, Transparenz, Datenminimierung, Quellenauswahl und eine etwaige Art.-9-Ausnahme müssen gesondert geprüft werden ([EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en)).
- Hinweise zur Anonymisierung ergänzt: Nach den neuen EDPB-Entwurfsleitlinien ist Anonymität perspektivbezogen zu bewerten; das EDPB nennt dafür die Prüfkriterien `No Record Isolation`, `No Linkage` und `No Inference` ([Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Geändert:

- Freigabe- und DSFA-Prüfung präzisiert: Bloßes Entfernen direkter Identifikatoren reicht nicht automatisch als Anonymisierung, und gescrapte öffentliche Daten oder fremde Trainingskorpora müssen getrennt dokumentiert und freigegeben werden ([Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.6.0 - 08.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen operativen Cowork-Prüfpunkt ergänzt: Anthropic dokumentiert seit dem 07.07.2026 für Claude Cowork auf Web und Mobile serverseitige Remote-Sessions; Sitzungen und Dateien liegen im Claude-Account, geplante Tasks laufen ohne online Gerät weiter ([Anthropic Release notes, 07.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely)).
- Hinweise zu Connector-Schreibrechten konkretisiert: Der Claude-Microsoft-365-Connector kann bei aktivierten `write tools` nun E-Mails senden/organisieren, Kalendereinträge ändern sowie Dateien in OneDrive und SharePoint erstellen oder aktualisieren; Teams bleibt dabei read-only ([Anthropic Release notes, 07.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide)).

Geändert:

- Anbieter- und Freigabeprüfung präzisiert: Für Cowork-Remote-Sessions und Connector-Schreibwerkzeuge reichen allgemeine Agentik-Hinweise nicht mehr aus; es sollte getrennt dokumentiert werden, welche Ordner, Konten, Schreibaktionen und laufenden Hintergrundaufgaben tatsächlich freigegeben sind ([Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.5.2 - 07.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen modellbezogenen Anthropic-Prüfpunkt ergänzt: Für `covered models` bzw. Mythos-class-Modelle dokumentiert Anthropic inzwischen eine 30-Tage-Retention; Claude Fable 5 ist laut offizieller Modelldokumentation nicht unter Zero Data Retention nutzbar ([Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide)).

Geändert:

- Anbieterprüfung präzisiert: Bei Anthropic reichen pauschale ZDR-Annahmen nicht aus; für Claude Code, Cowork und Cloud-Zugänge mit ZDR muss modellbezogen dokumentiert werden, ob ein separates Workspace-, Subscription- oder Sandbox-Setup mit aktivierter Retention erforderlich ist ([Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.5.1 - 06.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen Prüfaspekt zur aktuellen OpenAI-Retention ergänzt: Ohne Zero Data Retention nutzen unterstützte Modelle laut aktueller Datendokumentation standardmäßig Extended Prompt Caching; bei `gpt-5.5`, `gpt-5.5-pro` und künftigen Modellen ist `prompt_cache_retention=in_memory` nicht zulässig ([OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)).

Geändert:

- OpenAI-Hinweise zu API-Retention und Freigabeprozessen präzisiert, damit Default-Speicherlogiken nicht fälschlich als rein optionale Zusatzfunktion bewertet werden ([OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.5.0 - 05.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um Prüfpunkte für private MCP-Server ergänzt, insbesondere zu outbound-only-Tunnelarchitektur, Zielbegrenzung, Rollen und Audit-Logs auf Basis offizieller OpenAI-Dokumentation.
- KI-VO-Hinweise um die aktuellen Entwurfsleitlinien der EU-Kommission zur Hochrisiko-Einstufung erweitert.

Geändert:

- Zeitplanhinweise zu Hochrisiko-KI präzisiert: Die aktuelle Kommissionsdarstellung vom 01.07.2026 beschreibt einen differenzierten Zeitplan mit bestimmten Hochrisikobereichen ab 02.12.2027 und in Produkte integrierten Systemen ab 02.08.2028; die Leitlinien sind nicht rechtsverbindlich, sollen aber die Durchsetzung leiten.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.4.0 - 25.06.2026

Ergänzt:

- Datei `DSGVO-Grundlagen.md` mit dem rechtlichen Fundament (personenbezogene Daten, Verarbeitung, Grundsätze, Rechtsgrundlagen, Betroffenenrechte, VVT, TOM, Auftragsverarbeitung, Drittlandübermittlung) inklusive offizieller Quellen.
- Datei `Drittlandtransfer in die USA - DPF, Schrems und Cloud Act.md` mit Vertiefung zu US-Recht (CLOUD Act, FISA 702, PATRIOT/Freedom Act, Executive Order 12333), Schrems-Urteilen, Data Privacy Framework, Angemessenheitsbeschluss-Länderliste, TIA und datenschutzorientierten LLM-Setups (lokal und EU-gehostet).
- Datei `KI-Verordnung (AI Act) Grundlagen.md` mit Risikomodell, Definitionen (KI-System, GPAI), Rollen inklusive Rollenwechsel, Anbieterpflichten, Transparenzverpflichtungen, KI-Kompetenz, Sanktionen, Innovationsförderung und Zeitplan.

Geändert:

- README um die drei neuen Grundlagendokumente und deren Inhaltsbeschreibung erweitert.
- Alle Texte auf korrekte deutsche Umlaute (ä, ö, ü, ß) umgestellt.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.3.0 - 24.06.2026

Ergänzt:

- Praktische Art.-50-KI-VO-Transparenzpflichten auf Basis des finalen EU Code of Practice vom 10.06.2026 in Checkliste, DSFA-Vorlage und KI-Richtlinie konkretisiert.
- Prüfpunkte zu Nutzerhinweisen bei interaktiven KI-Systemen sowie zur Kennzeichnung von Deepfakes und KI-generierten/manipulierten Texten von öffentlichem Interesse aufgenommen.

Geändert:

- KI-VO-Hinweise präzisiert: Der Code of Practice ist freiwillig, die gesetzlichen Transparenzpflichten gelten dennoch ab dem 02.08.2026.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.2.0 - 18.06.2026

Ergänzt:

- KI-VO-Kurzcheck mit Risikoklassen, KI-Kompetenz, Transparenzpflichten und Grundrechte-Folgenabschätzung auf Basis des EU AI Act Service Desk.
- DSFA-Vorlage um LLM-spezifische Risiken, AI-Act-Prüfpunkte, OpenAI-Feature-Retention und Anthropic-Enterprise-/API-Kontrollen erweitert.
- Hinweise zu agentischer KI, Computer Use, Hosted Containers, MCP-Drittservern, Claude Audit Logs und Anthropic Message Batches aufgenommen.

Geändert:

- OpenAI-/Anthropic-Anbieterprüfung präzisiert: ZDR, Retention, Datenresidenz und Logs müssen funktions- bzw. endpointbezogen bewertet werden.
- Quellenbasis um offizielle EDPB-, BfDI-, EU-AI-Act-Service-Desk-, OpenAI- und Anthropic-Dokumentation erweitert.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.1.0 - 17.06.2026

Ergänzt:

- AI-Act-Transparenzpflichten ab 02.08.2026 für generative KI in der KI-Richtlinie konkretisiert.
- Hinweise zu Claude Chat-Suche/Memory und deren Retention-/Admin-Kontrollen in die Checkliste und Richtlinie aufgenommen.

Geändert:

- Anbieter- und Transferprüfung um OpenAI-MCP/Konnektoren ergänzt: Drittserver müssen separat auf Retention, Residency und Datenschutz geprüft werden.
- DSFA-Vorlage um Prüfpunkte zu Chat-Suche/Memory, MCP/Konnektoren und API-spezifischer Speicherlogik erweitert.
- OpenAI-API-Hinweise zu Responses-API-Retention und Background-Mode/ZDR in die Checkliste aufgenommen.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.0.0 - 16.06.2026

Ergänzt:

- Erstveröffentlichung des Repositorys.
- Datei `Tipps zur DSGVO.md` hinzugefügt.
- Datei `Datenschutz-Folgenabschätzung Vorlage KI Nutzung.md` hinzugefügt.
- Datei `KI Richtlinie für die KI Nutzung.md` hinzugefügt.
- README mit Inhaltsbeschreibung, Versionsinfo und Hinweisen hinzugefügt.

Entfernt:

- Keine Inhalte entfernt.

## Hinweise

Diese Inhalte stellen keine rechtliche Beratung dar. Sie dienen nur als allgemeine Orientierung und müssen für den jeweiligen Einzelfall rechtlich und organisatorisch geprüft werden.

Der Ersteller übernimmt keine Haftung für die Richtigkeit, Vollständigkeit, Aktualität oder Nutzbarkeit der Inhalte.

Diese Dateien werden regelmäßig automatisch ergänzt.
