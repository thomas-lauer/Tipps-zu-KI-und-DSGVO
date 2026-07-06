# Tipps zur DSGVO bei der Nutzung von Claude.ai und OpenAI

Stand: 06.07.2026

Dieses Dokument ist eine praktische Checkliste für den Einsatz generativer KI. Es ersetzt keine Rechtsberatung. Wenn ein Punkt nicht sicher bewertet werden kann, muss er als offen dokumentiert und vor produktiver Nutzung geklärt werden.

## 1. Erst klären: Welcher Account wird genutzt?

Nutze für Unternehmensdaten keine privaten Free/Pro/Max-Accounts. Verwende nur Business-, Enterprise- oder API-Angebote, bei denen ein AVV/DPA, Admin-Kontrollen, Retention-Einstellungen und Nachweise zu Subprozessoren verfügbar sind.

Quellen: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [Anthropic Claude for Work Rollen](https://support.anthropic.com/en/articles/9267385-what-is-the-data-relationship-between-anthropic-the-customer-and-the-user).

## 2. Keine sensiblen Daten in Consumer-KI

Nicht eingeben:

- Gesundheitsdaten
- Bewerber- und HR-Bewertungen
- Kundendaten mit Identifikatoren
- Vertrags-, Steuer-, Rechts- oder Mandantendaten
- Passwörter, API-Keys, Tokens
- interne Geheimnisse
- Daten von Kindern
- biometrische Daten oder Fotos zur Identifizierung

Quellen: [Art. 9 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Anthropic Consumer Sensitive Data](https://support.anthropic.com/en/articles/8325621-i-would-like-to-input-sensitive-data-into-free-claude-ai-or-claude-pro-who-can-view-my-conversations), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 3. Prompts minimieren

Vor jeder Eingabe fragen:

- Braucht die KI den Namen wirklich?
- Reicht eine Rolle wie "Kunde A" oder "Mitarbeiter B"?
- Kann ich IDs, E-Mail-Adressen, Telefonnummern und Aktenzeichen entfernen?
- Kann ich den Sachverhalt abstrakt beschreiben?
- Kann ich lokale Verarbeitung oder ein internes RAG-System nutzen?

Quelle: [Art. 5 DSGVO Datenminimierung, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng).

## 4. Training/Model Improvement deaktivieren

Bei OpenAI und Anthropic muss für den konkreten Dienst geprüft werden, ob Eingaben/Dateien/Outputs für Training oder Serviceverbesserung verwendet werden. Für personenbezogene Unternehmensdaten sollte Training vertraglich ausgeschlossen oder technisch deaktiviert sein.

Quellen: [OpenAI API Data Controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [Anthropic Consumer Terms/Privacy Update](https://www.anthropic.com/news/updates-to-our-consumer-terms), [Anthropic Commercial Customers](https://privacy.anthropic.com/en/collections/10663361-commercial-customers).

## 5. Speicherfristen festlegen

Dokumentiere, wie lange gespeichert werden:

- Chats
- Dateien
- Projektwissen
- API-Requests
- Outputs
- Logs
- Abuse-/Security-Daten
- Support-Tickets
- Backups

Nutze möglichst kurze Retention. Zero Data Retention ist nur dann relevant, wenn sie für den konkreten Vertrag/Plan/Endpunkt tatsächlich gilt.

Bei API-Nutzung die konkrete Speicherlogik pro Funktion prüfen. Laut OpenAI werden im Responses API "Application State" standardmäßig für mindestens 30 Tage gespeichert; bei aktivierter Zero Data Retention wird `store` zwar auf `false` erzwungen, Background Mode speichert Daten aber für ungefähr 10 Minuten auf Disk. Remote-MCP-Server sind Drittservices mit eigenen Retention-Regeln; Hosted Shell, Code Interpreter und gehostete Skills können temporäre Daten im Container-Dateisystem verarbeiten, bis der Container abläuft oder gelöscht wird. Laut aktueller OpenAI-Datendokumentation nutzen Organisationen ohne ZDR bei allen unterstützten Modellen standardmäßig Extended Prompt Caching; die dafür nötigen verschlüsselten Key/Value-Tensoren werden als Application State auf GPU-lokalem Speicher bis zum 24-Stunden-Ablauf gehalten. Für `gpt-5.5`, `gpt-5.5-pro` und künftige Modelle ist `prompt_cache_retention=in_memory` dabei nicht zulässig.

Bei Anthropic sind Enterprise-Retention-Kontrollen plan- und rollenabhängig. Für Claude Enterprise beginnen Retention-Fristen nach Anthropic-Angaben bei Chats mit der letzten Nachricht und bei Projekten mit der letzten Projektaktualisierung; Projekt-Retention kann Chat-Retention übersteuern. Bei der Claude API muss ZDR pro Feature geprüft werden; Message Batches sind nach Anthropic-Dokumentation nicht ZDR-fähig.

Quellen: [OpenAI Business Data](https://openai.com/business-data/), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Anthropic Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Anthropic Zero Data Retention](https://privacy.anthropic.com/en/articles/8956058-i-have-a-zero-retention-agreement-with-anthropic-what-products-does-it-apply-to).

## 6. AVV/DPA abschließen

Wenn die KI personenbezogene Daten im Auftrag verarbeitet, ist ein AVV/DPA nach Art. 28 DSGVO erforderlich. Prüfe:

- Vertragspartner
- Rolle des Anbieters
- Subprozessoren
- Weisungsbindung
- technische und organisatorische Maßnahmen
- Löschung/Rückgabe
- Audit-/Nachweisrechte
- Drittlandtransfers

Quellen: [Art. 28 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [OpenAI DPA](https://openai.com/policies/data-processing-addendum/), [Anthropic Claude for Work Rollen](https://support.anthropic.com/en/articles/9267385-what-is-the-data-relationship-between-anthropic-the-customer-and-the-user).

## 7. Drittlandtransfer nicht vergessen

OpenAI und Anthropic sind US-nahe Anbieter bzw. nutzen internationale Infrastruktur/Subprozessoren. Vor Einsatz mit personenbezogenen Daten muss der Drittlandtransfer nach Art. 44 ff. DSGVO geprüft werden. Mögliche Bausteine sind EU-Data-Residency, Standardvertragsklauseln, Transfer Impact Assessment, EU-U.S. Data Privacy Framework und zusätzliche technische Maßnahmen. Ob ein Anbieter aktuell für einen konkreten Dienst zertifiziert ist, muss in der offiziellen DPF-Liste geprüft werden.

Bei Konnektoren oder MCP-Servern reicht die Data-Residency-/ZDR-Zusage des Hauptanbieters nicht automatisch aus. Für angebundene Drittserver müssen eigene Retention-, Residency- und Transferregeln geprüft werden.

Quellen: [Art. 44 ff. DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Data Privacy Framework List](https://www.dataprivacyframework.gov/list), [OpenAI Data Residency Europe](https://openai.com/index/introducing-data-residency-in-europe/), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [EU-Kommission DPF Q&A](https://ec.europa.eu/commission/presscorner/detail/en/qanda_23_3752).

## 8. DSFA prüfen

Eine Datenschutz-Folgenabschätzung ist besonders naheliegend bei:

- neuen Technologien mit hohem Risiko
- umfangreicher Verarbeitung personenbezogener Daten
- Profiling oder Scoring
- Beschäftigtendaten
- Gesundheitsdaten oder anderen Art.-9-Daten
- automatisierten Entscheidungen
- systematischer Überwachung
- RAG-Systemen mit großen internen Wissensbeständen

Quellen: [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

Das EDPB-Dokument zu LLM-Risiken ersetzt keine DSFA, kann aber als technische Risikoprüfung für LLM-Systeme herangezogen werden. Relevante Prüffelder sind insbesondere Datenminimierung, Schutz vor Datenabfluss, Prompt-Injection, Memorisation, unberechtigte Offenlegung aus Trainings-/Kontextdaten, Richtigkeit personenbezogener Outputs und technische/organisatorische Maßnahmen nach Art. 25 und Art. 32 DSGVO.

Quellen: [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf), [BfDI Konsultation KI-Modelle und personenbezogene Daten](https://www.bfdi.bund.de/DE/BfDI/Konsultationsverfahren/KI-Modelle-pbD/KI-Modelle-pbD_node.html).

## 9. Keine automatisierte Letztentscheidung

KI-Ausgaben dürfen nicht ungeprüft über Menschen entscheiden. Besonders kritisch sind Bewerbungen, Mitarbeiterbewertungen, Bonität, Versicherungen, Gesundheit, Vertragszugang, Sanktionen und Leistungsentscheidungen. Eine menschliche Prüfung muss echt, kompetent und dokumentiert sein.

Quellen: [Art. 22 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 10. Ergebnisse immer prüfen

LLMs können falsche Tatsachen, erfundene Quellen, diskriminierende Muster oder personenbezogene Falschinformationen erzeugen. Ergebnisse dürfen deshalb nicht blind übernommen werden. Bei personenbezogenen Aussagen ist das Richtigkeitsgebot besonders wichtig.

Quellen: [Art. 5 DSGVO Richtigkeit, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [EDPB ChatGPT Taskforce](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-chatgpt-taskforce_en).

## 11. RAG ist hilfreich, aber kein Freifahrtschein

Ein internes RAG-System kann Datenschutz verbessern, wenn es nur freigegebene Quellen nutzt und Berechtigungen sauber abbildet. Es kann aber auch neue Risiken schaffen:

- falsche Indexierung
- Zugriff auf Dokumente ohne Berechtigung
- Prompt-Injection
- veraltete Quellen
- unklare Löschung aus Indexen
- Offenlegung vertraulicher Passagen in Antworten

Funktionen wie Chat-Suche, Projektwissen oder Memory können ebenfalls frühere Inhalte für neue Antworten heranziehen. Bei Claude sollte deshalb separat geprüft werden, ob Chat-Suche/Memory aktiviert sein dürfen, wie Admin-Kontrollen aussehen und wie Retention, Export und Löschung geregelt sind.

Quellen: [DSK RAG Orientierungshilfe, Oktober 2025](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context).

## 12. Interne KI-Richtlinie erstellen

Eine gute KI-Richtlinie enthält:

- erlaubte Tools und verbotene Tools
- erlaubte Datenarten
- verbotene Datenarten
- Prompt-Regeln
- Freigabeprozess für neue Use Cases
- Umgang mit Dateien und Konnektoren
- Prüfpflicht für Outputs
- Kennzeichnung von KI-Unterstützung, wenn erforderlich
- Meldeweg für Datenschutzvorfälle
- Schulungspflicht

Quelle: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 13. Anbieterprüfung als Kurzcheck

Vor Freigabe eines KI-Tools beantworten:

- Welcher Anbieter und welcher konkrete Plan?
- Gibt es AVV/DPA?
- Werden Eingaben für Training genutzt?
- Welche Retention gilt?
- Wo werden Daten verarbeitet?
- Welche Subprozessoren gibt es?
- Gibt es Admin-Konsole, SSO, MFA, Rollenrechte?
- Können Chats/Dateien gelöscht/exportiert werden?
- Gibt es Logs für Missbrauch und Security?
- Wie werden Betroffenenrechte erfüllt?
- Gibt es eine Möglichkeit für EU Data Residency oder ZDR?
- Gibt es featurebezogene Abweichungen von ZDR oder Retention, z. B. Background Mode, standardmäßiges Extended Prompt Caching ohne ZDR, Hosted Containers, Message Batches oder nicht gelöschte Assistants-/Vector-Store-Objekte?
- Gibt es Audit-Logs, wer darf sie exportieren, wie lange reichen sie zurück und enthalten sie Chat-/Projektinhalte oder nur Identifier/Metadaten?
- Werden Konnektoren, MCP-Server, Chat-Suche, Memory oder Projektwissen genutzt, und welche eigenen Speicher-/Transferregeln gelten dort?
- Wenn private MCP-Server angebunden werden: Bleibt der Server hinter der eigenen Umgebung, erfolgt die Anbindung über eine enge outbound-only-Tunnelarchitektur statt über einen öffentlichen Endpoint oder breite Netzfreigaben, und sind Zielsystem, Rollen und Audit-Logs dokumentiert?
- Ist eine DSFA erforderlich?

Quellen: [OpenAI Security and Privacy](https://openai.com/security-and-privacy/), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic Trust Center](https://trust.anthropic.com/), [Anthropic Commercial Customers](https://privacy.anthropic.com/en/collections/10663361-commercial-customers), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs).

## 14. Was aus Entscheidungen gelernt werden kann

- ChatGPT/OpenAI: Aufsichtsbehörden prüfen Transparenz, Rechtsgrundlage, Richtigkeit, Betroffenenrechte und Kinderschutz. Die italienische Sanktion aus 2024 darf wegen des 2026 veröffentlichten gerichtlichen Hinweises auf der Garante-Seite nicht als final bestätigt dargestellt werden.
- Clearview AI: Öffentlich zugängliche Daten sind nicht automatisch frei nutzbar. Scraping und biometrische Verarbeitung sind sehr risikoreich.
- SCHUFA: Automatisierte Scores können Art. 22 DSGVO auslösen, wenn sie für Entscheidungen faktisch maßgeblich sind.

Quellen: [EDPB ChatGPT Taskforce](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-chatgpt-taskforce_en), [Garante ChatGPT Hinweis](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432), [EDPB Clearview Niederlande](https://www.edpb.europa.eu/news/national-news/2024/dutch-supervisory-authority-imposes-fine-clearview-because-illegal-data_en), [EDPB Clearview Frankreich](https://www.edpb.europa.eu/news/national-news/2022/french-sa-fines-clearview-ai-eur-20-million_en), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en).

## 15. Sofort umsetzbare Praxisregeln

1. Private KI-Accounts für Unternehmensdaten sperren.
2. Offizielle KI-Tools mit DPA/AVV freigeben.
3. Training/Model Improvement deaktivieren.
4. Kurze Retention einstellen.
5. MFA/SSO aktivieren.
6. Rollen und Projekte trennen.
7. Keine Art.-9-Daten ohne DSFA und Rechtsfreigabe.
8. Keine KI-Letztentscheidungen über Personen.
9. Prompts pseudonymisieren.
10. Outputs fachlich prüfen.
11. Quellen für KI-Aussagen verlangen.
12. Neue Features wie Konnektoren, Computer Use, Datei-Uploads oder RAG vor Aktivierung separat prüfen.
13. Zentrale Business-Accounts für Firmen-Tools nutzen, nicht verstreute Einzelaccounts.
14. Tool-Whitelist, Nutzungsregeln und Input-Grenzen schriftlich festlegen.
15. Agentische Funktionen wie Cowork, Computer Use, Browserzugriff oder Slack-/Dienstzugriffe nur separat freigeben.
16. Memory-, Chat-Suche-, Connector- und MCP-Funktionen nur separat freigeben und dokumentieren.
17. Bei OpenAI-API-Integrationen ZDR/Data Residency nicht nur pauschal, sondern pro genutzter Funktion prüfen.
18. Private MCP-Server nach Möglichkeit über eng begrenzte outbound-only-Tunnel statt über öffentliche Endpunkte oder unnötig breite Netzfreigaben anbinden; Ziele, Rollen und Audit-Logs dokumentieren.

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context).

## 16. KI-VO-Kurzcheck zusätzlich zur DSGVO

Die KI-Verordnung ersetzt die DSGVO nicht. Für jeden KI-Einsatz sollte separat dokumentiert werden:

- Fällt der Use Case unter [verbotene KI-Praktiken nach Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5)?
- Liegt ein Hochrisiko-KI-System nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) vor?
- Geht es nur um begrenztes Risiko mit Transparenzpflichten, insbesondere nach [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50)?
- Sind KI-Kompetenz, Schulung und Kontextkenntnis nach [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4) umgesetzt?
- Muss bei Hochrisiko-Einsatz eine Grundrechte-Folgenabschätzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) die DSFA ergänzen?
- Muss bei interaktiven KI-Systemen klar kenntlich gemacht werden, dass Personen mit KI interagieren?
- Werden Deepfakes oder KI-generierte/manipulierte Texte zu Fragen von öffentlichem Interesse veröffentlicht und müssen klar gekennzeichnet werden?

Nach [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113) gilt die Verordnung grundsätzlich ab dem 2. August 2026; Kapitel I und II gelten seit dem 2. Februar 2025, bestimmte GPAI-, Governance- und Sanktionsregeln seit dem 2. August 2025. Für Hochrisiko-KI verweist die aktuelle Kommissionsdarstellung vom 01.07.2026 auf einen differenzierten Zeitplan: bestimmte Hochrisikobereiche sollen ab dem 02.12.2027, in Produkte integrierte Systeme z. B. Robotik oder Industriemaschinen ab dem 02.08.2028 greifen. Die zugrunde liegenden Leitlinien sind nicht rechtsverbindlich, spiegeln aber die Auslegung der Kommission wider und sollen die Durchsetzung leiten.

Praxis-Hinweis zu Art. 50 KI-VO: Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde laut EU-Kommission am 10.06.2026 veröffentlicht. Der Code ist freiwillig, die Transparenzpflichten selbst gelten aber ab dem 02.08.2026. Nach der Kommissionsmitteilung müssen Nutzer informiert werden, wenn sie mit einem interaktiven KI-System wie einem Chatbot interagieren; außerdem müssen Deepfakes sowie KI-generierte oder KI-manipulierte Texte, die auf Fragen von öffentlichem Interesse abzielen, klar gekennzeichnet werden.

Quellen: [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content).

## Mini-Entscheidungsbaum

1. Enthalten Eingabe oder Upload personenbezogene Daten?
   - Nein: Nutzung mit allgemeinen Sicherheitsregeln möglich.
   - Ja: weiter zu 2.
2. Handelt es sich um besondere Kategorien, HR, Kinder, Scoring, Gesundheit, Mandanten oder Geheimnisse?
   - Ja: nicht ohne DSFA/Rechtsprüfung/Freigabe.
   - Nein: weiter zu 3.
3. Wird ein Business/API/Enterprise-Angebot mit DPA genutzt?
   - Nein: nicht verwenden.
   - Ja: weiter zu 4.
4. Sind Training aus, Retention kurz, Drittlandtransfer geprüft und Betroffenenrechte umsetzbar?
   - Nein: erst konfigurieren/dokumentieren.
   - Ja: kontrollierte Nutzung möglich.
