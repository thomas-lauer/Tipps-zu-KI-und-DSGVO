# Tipps zur DSGVO bei der Nutzung von Claude.ai und OpenAI

Stand: 29.07.2026

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

Wenn Daten angeblich anonymisiert sind, reicht das bloße Entfernen direkter Identifikatoren nicht automatisch aus. Nach den am 07.07.2026 angenommenen EDPB-Entwurfsleitlinien ist Anonymität aus Sicht der jeweils relevanten Stellen zu beurteilen; das EDPB nennt dafür die Prüfkriterien `No Record Isolation`, `No Linkage` und `No Inference`. Bis zu einer dokumentierten Prüfung sollten pseudonymisierte oder nur geschwärzte Datensätze weiter als personenbezogen behandelt werden ([Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

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

Zusätzlich ist bei ChatGPT/OpenAI-Apps zu prüfen, ob eine Funktion nur lesend arbeitet oder Inhalte per `sync` vorab indexiert. Laut aktueller OpenAI-Dokumentation werden Chat- und Deep-Research-Daten bei Apps transient verarbeitet und nicht indexiert, `apps with sync` dagegen zur schnelleren Suche vorab indexiert; Unterhaltungen mit Apps sind über die Compliance API nachvollziehbar und App-Calls werden in Compliance Logs protokolliert. Für nicht in der eigenen Residency-Region unterstützte Sync-Apps wird der Suchindex laut OpenAI in US-Azure-Rechenzentren gespeichert. Für sensible Daten sollte deshalb getrennt dokumentiert werden, ob nur nicht-synchronisierte Nutzung zulässig ist oder ob die Indexierung in einer fremden Region akzeptiert werden kann ([Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)).

Bei Anthropic sind Enterprise-Retention-Kontrollen plan- und rollenabhängig. Für Claude Enterprise beginnen Retention-Fristen nach Anthropic-Angaben bei Chats mit der letzten Nachricht und bei Projekten mit der letzten Projektaktualisierung; Projekt-Retention kann Chat-Retention übersteuern. Bei der Claude API muss ZDR pro Feature geprüft werden; Message Batches sind nach Anthropic-Dokumentation nicht ZDR-fähig.

Zusätzlich ist bei Anthropic laut aktueller Modelldokumentation und aktualisierter Help-Center-Dokumentation modellbezogen zu prüfen, ob ein Modell als `covered model` nur mit 30-Tage-Retention nutzbar ist. Anthropic dokumentiert für Mythos-class-Modelle eine 30-Tage-Retention von Prompts und Outputs; Claude Fable 5 ist laut Migration Guide nicht unter Zero Data Retention verfügbar. Für ZDR-Setups können deshalb getrennte Workspaces, Cloud-Subscriptions oder Sandbox-Umgebungen mit aktivierter Retention erforderlich sein. Bei Claude Chat oder Cowork in Claude Enterprise besteht insoweit laut Anthropic keine zusätzliche Umstellung, weil diese Oberflächen bereits mit Standard-Retention arbeiten.

Neu zu berücksichtigen ist außerdem, dass Anthropic laut Release Notes seit dem 01.07.2026 für Enterprise-Pläne eine Beta zur organisations- und rollenbezogenen Modellfreigabe dokumentiert. Admins können damit festlegen, welche Modelle organisationsweit oder je Custom Role verfügbar sind und welches maximale Effort-Level pro Rolle zulässig ist; Haiku-Modelle bleiben laut Anthropic dabei immer verfügbar. Das ist für Datenschutz und Informationssicherheit relevant, weil sich `covered models` oder andere nicht freigegebene Modelle technisch begrenzen lassen, statt nur per Richtlinie verboten zu sein ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization)).

Neu zu berücksichtigen ist außerdem, dass Claude Cowork laut Anthropic seit dem 07.07.2026 auf Web und Mobile als Remote-Session auf Anthropic-Servern läuft; Sitzungen und Dateien werden im Claude-Account gespeichert und geplante Tasks laufen auch ohne online Gerät weiter. Wenn Cowork dabei über die geöffnete Desktop-App auf lokale Ordner oder Browserfunktionen zugreift, sollte dokumentiert werden, welche verbundenen Ordner erreichbar sind und dass die Verarbeitung trotzdem serverseitig bei Anthropic erfolgt ([Anthropic Release notes, 07.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely)).

Neu zu berücksichtigen ist außerdem, dass Anthropic seit dem 10.07.2026 für Managed Agents geplante `scheduled deployments` dokumentiert, die Sessions autonom per Cron starten können. Dabei können Dateien, GitHub-Zugänge, Memory Stores und Vaults eingebunden werden; Run-Historie und Lifecycle-Änderungen lassen sich über Deployment-Runs und Webhooks nachvollziehen. Für Vault-Credentials des Typs `environment_variable` stellt Anthropic klar, dass der Secret-Wert dem Agenten nicht offengelegt wird, sondern erst beim ausgehenden Request eingesetzt wird. Für Datenschutz und Informationssicherheit sollte deshalb dokumentiert werden, welche Zeitpläne, Datenquellen, Vaults und Secrets freigegeben sind, wer Deployments pausieren oder archivieren darf und wie Rotation/Audit erfolgen ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview)).

Neu zu berücksichtigen ist außerdem, dass Anthropic die Nachweis- und Monitoringlage für Claude Cowork inzwischen enger ausdifferenziert. Die aktuelle Team-/Enterprise-Dokumentation verweist darauf, dass Cowork via Mobile und Web in der Compliance API erfasst ist, während lokale Sessions lokal auf dem Rechner bleiben und nicht zentral exportierbar sind. Zugleich beschreibt Anthropic für laufende Cowork-Aktivität wie Tool-Calls, Dateizugriffe und Approval-Entscheidungen OpenTelemetry als Monitoring-Weg und stellt klar, dass dies die Compliance API nicht ersetzt. Für Datenschutz- und Kontrollkonzepte sollte daher ausdrücklich zwischen Session-Inhalten/Artefakten in Cloud-Remote-Sessions und separater Aktivitätstelemetrie unterschieden werden; die genaue Grenzziehung ist in den Herstellerunterlagen nicht vollständig ausbuchstabiert und sollte intern dokumentiert werden ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview)).

Neu zu berücksichtigen ist außerdem, dass OpenAI Plugins, Apps und Skills inzwischen als getrennte Governance-Ebenen dokumentiert. Seit dem 09.07.2026 verweist OpenAI auf das Plugin Directory als zentrale Oberfläche; in Enterprise und Edu sind Plugins und zugrunde liegende Apps standardmäßig deaktiviert und rollenbezogen getrennt freizugeben. Für Skills plant OpenAI in Enterprise-Workspaces ohne Opt-out seit dem 23.07.2026 eine Standardaktivierung; hochgeladene Skills werden zwar gescannt, der Scan ersetzt aber laut OpenAI keine eigene Freigabeprüfung. Für Datenschutz und Informationssicherheit sollte deshalb nicht nur der Plugin-Name, sondern auch die enthaltenen Apps, Rollenrechte, Skill-Uploads und Installationsrechte dokumentiert werden ([Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Quellen: [OpenAI Business Data](https://openai.com/business-data/), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Anthropic Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Anthropic Zero Data Retention](https://privacy.anthropic.com/en/articles/8956058-i-have-a-zero-retention-agreement-with-anthropic-what-products-does-it-apply-to), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Anthropic Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

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

Bei OpenAI-`apps with sync` ist zusätzlich zu beachten, dass eine Residency-Zusage nicht automatisch für jede Sync-App in jeder Region gilt. Laut aktueller OpenAI-Dokumentation wird der Sync-Index für Apps, die in der eigenen Residency-Region nicht unterstützt werden, in US-Azure-Rechenzentren gespeichert; bei nicht synchronisierten Apps endet die OpenAI-Residency-Zusage zudem dort, wo Eingaben an den angebundenen Drittservice weitergegeben werden. Für Transferprüfungen sollten deshalb Sync- und Non-Sync-Nutzung getrennt bewertet werden ([Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps)).

Bei Anthropic ist zusätzlich zwischen lokal konfigurierten MCP-Servern in Claude Desktop und `custom connectors` über remote MCP zu unterscheiden. Laut aktueller Help-Center-Dokumentation sind solche remote MCP-Connectoren inzwischen auf Claude, Cowork und Claude Desktop verfügbar; die Verbindung zum MCP-Server geht dabei aus der Anthropic-Cloud und nicht vom lokalen Gerät aus. Für Transfer-, Netzwerk- und TOM-Prüfungen muss deshalb der konkrete Verbindungsweg dokumentiert werden; auf Team- und Enterprise-Plänen können nur Owners solche Connectoren organisationsweit hinzufügen ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)).

Quellen: [Art. 44 ff. DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Data Privacy Framework List](https://www.dataprivacyframework.gov/list), [OpenAI Data Residency Europe](https://openai.com/index/introducing-data-residency-in-europe/), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [EU-Kommission DPF Q&A](https://ec.europa.eu/commission/presscorner/detail/en/qanda_23_3752), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

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

Für Hochrisiko-KI konkretisiert die Kommission seit dem 22.07.2026 zusätzlich die Betreiberpflichten: Nutzungsanweisungen müssen technisch und organisatorisch umgesetzt, der Betrieb überwacht und menschliche Aufsicht klar zugewiesen werden. Wenn der Betreiber selbst Eingabedaten bereitstellt, müssen diese für den vorgesehenen Zweck relevant und hinreichend repräsentativ sein. Öffentliche Stellen und private Anbieter öffentlicher Dienste müssen vor der ersten Nutzung grundsätzlich eine Grundrechte-Folgenabschätzung durchführen; wenn der Output eines Hochrisiko-Systems für eine Entscheidung über eine natürliche Person mit Rechtswirkung genutzt wurde, ist ein Prozess für das Recht auf Erklärung vorzusehen ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

Quellen: [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf), [BfDI Konsultation KI-Modelle und personenbezogene Daten](https://www.bfdi.bund.de/DE/BfDI/Konsultationsverfahren/KI-Modelle-pbD/KI-Modelle-pbD_node.html), [Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act).

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

Wenn für ein eigenes Modell, Fine-Tuning oder externe Wissensbestände öffentlich zugängliche Webdaten oder bereits gescrapte Datensätze genutzt werden, ist das keine folgenlose "Öffentlichkeitsnutzung". Das EDPB stellt in neuen Entwurfsleitlinien klar, dass Web Scraping für generative KI der DSGVO unterfällt, sobald personenbezogene Daten erhoben, gespeichert, strukturiert oder wiederverwendet werden. Besondere Aufmerksamkeit verlangt das EDPB für Zweckbindung, Transparenz, Datenminimierung, verlässliche Quellen, Zeitstempel/Validierung sowie den Ausschluss bestimmter Quellen oder Websites, die Scraping klar entgegenstehen; bei Art.-9-Daten braucht es zusätzlich zu Art. 6 eine Ausnahme nach Art. 9 Abs. 2 DSGVO. Die Leitlinien sind seit 08.07.2026 bis 30.10.2026 in Konsultation ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Quellen: [DSK RAG Orientierungshilfe, Oktober 2025](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en).

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

Nach der aktuellen Kommissions-Q&A zu Art. 4 KI-VO sollte die Richtlinie oder ein Begleitkonzept außerdem dokumentieren, welche Zielgruppen geschult werden, wie sich Inhalte nach Rolle, Risiko und Use Case unterscheiden und wie Trainings oder andere Leitmaßnahmen intern nachgewiesen werden. Ein Zertifikat oder eine bestimmte AI-Officer-Struktur verlangt die Kommission dafür nicht; bloßes Verteilen von Nutzungsanweisungen reicht aber regelmäßig nicht aus. Die Überwachung und Durchsetzung zu Art. 4 startet ab dem 03.08.2026 ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)).

Quellen: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers).

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
- Gibt es modellbezogene Retention-Ausnahmen, z. B. Anthropic-`covered models` oder Claude Fable 5 mit 30-Tage-Retention statt ZDR?
- Gibt es Audit-Logs, wer darf sie exportieren, wie lange reichen sie zurück und enthalten sie Chat-/Projektinhalte oder nur Identifier/Metadaten?
- Werden Konnektoren, MCP-Server, Chat-Suche, Memory oder Projektwissen genutzt, und welche eigenen Speicher-/Transferregeln gelten dort?
- Werden bei Anthropic `custom connectors` oder remote MCP genutzt, und ist dokumentiert, dass die Verbindung zum MCP-Server von Anthropic-Servern statt vom lokalen Gerät ausgeht ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))?
- Werden öffentliche Webdaten, gescrapte Datensätze oder fremde Trainingskorpora genutzt, und sind dafür Rechtsgrundlage, Transparenz, Quellen-/Widerspruchsmanagement, Datenminimierung, Validierung und eine etwaige Art.-9-Ausnahme dokumentiert?
- Sind angeblich anonymisierte Datensätze anhand eines dokumentierten Re-Identifikationschecks bewertet, statt nur direkte Identifikatoren zu entfernen?
- Falls Claude Cowork als Remote-Session genutzt wird: Ist dokumentiert, dass Sitzungen und Dateien im Claude-Account liegen, geplante Tasks serverseitig weiterlaufen und lokale Ordner nur über die geöffnete Desktop-App erreichbar sind ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely))?
- Falls Claude Cowork genutzt wird: Ist für Cloud-/Remote-Sessions getrennt von lokaler Nutzung dokumentiert, welche Inhalte laut Anthropic über die Compliance API erreichbar sind, was lokal verbleibt und dass laufende Aktivitätstelemetrie wie Tool-Calls oder Dateizugriffe weiterhin gesondert über OpenTelemetry zu bewerten ist ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry))?
- Falls Claude Cowork oder Remote Control in Team/Enterprise genutzt wird: Sind `network-access policy`, restriktives Approval-Verhalten und Trusted Devices soweit verfügbar aktiv gesetzt, statt auf offene Default-Freigaben zu vertrauen ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control))?
- Falls Anthropic Managed Agents genutzt werden: Sind autonome `scheduled deployments`, eingebundene Dateien/GitHub-Zugänge/Memory Stores/Vaults, Deployment-Run-Logs/Webhooks sowie Rechte zum Pausieren oder Archivieren dokumentiert ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview))?
- Falls Anthropic Vault-Credentials genutzt werden: Ist der Scope von MCP- und `environment_variable`-Credentials eng begrenzt, rotierbar und auditierbar, obwohl der Secret-Wert laut Anthropic erst beim ausgehenden Request eingesetzt und dem Agenten nicht offengelegt wird ([Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults))?
- Falls der Claude-Microsoft-365-Connector genutzt wird: Sind aktivierte `write tools` für E-Mail, Kalender sowie OneDrive/SharePoint separat freigegeben, administrativ aktiviert und auf notwendige Anwendungsfälle begrenzt, obwohl Teams read-only bleibt ([Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide))?
- Falls der Claude-Microsoft-365-Connector genutzt wird: Ist dokumentiert, dass der Tenant den erweiterten Microsoft-Graph-Berechtigungen erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen, Datei- und Kalender-Schreibvorgänge aber nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector))?
- Falls Claude Code, Cowork oder Cloud-Zugänge mit ZDR genutzt werden: Ist für Modelle mit Retention-Pflicht ein getrenntes Workspace-, Subscription- oder Sandbox-Setup dokumentiert?
- Falls Anthropic Enterprise genutzt wird: Sind organisations- oder rollenbezogene Modell-Allowlist und Effort-Caps so gesetzt, dass nur freigegebene Modelle verfügbar sind, statt sich allein auf Richtlinien oder Schulungen zu verlassen ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization))?
- Falls Anthropic Team oder Enterprise genutzt wird: Ist dokumentiert, ob `individual usage analytics` genutzt oder bewusst deaktiviert werden, wer nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill sehen darf und ob interne Transparenzanforderungen geprüft wurden ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans))?
- Falls ChatGPT Work oder Scheduled Tasks genutzt werden: Sind freigegebene lokale Ordner, zulässige App-/Dateizugriffe, wiederkehrende oder monitoringbasierte Läufe, Benachrichtigungen und der Umstand dokumentiert, dass Tasks in Projekten nicht auf Projektdateien zugreifen, aber in der Compliance API erscheinen ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt))?
- Wenn private MCP-Server angebunden werden: Bleibt der Server hinter der eigenen Umgebung, erfolgt die Anbindung über eine enge outbound-only-Tunnelarchitektur statt über einen öffentlichen Endpoint oder breite Netzfreigaben, und sind Zielsystem, Rollen und Audit-Logs dokumentiert?
- Ist eine DSFA erforderlich?

Quellen: [OpenAI Security and Privacy](https://openai.com/security-and-privacy/), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Anthropic Trust Center](https://trust.anthropic.com/), [Anthropic Commercial Customers](https://privacy.anthropic.com/en/collections/10663361-commercial-customers), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

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
19. Bei Anthropic ZDR nicht pauschal auf neue Frontier-Modelle übertragen; `covered models` wie Claude Fable 5 gegebenenfalls nur in getrennten Workspaces, Subscriptions oder Sandbox-Umgebungen mit aktivierter 30-Tage-Retention freigeben.
20. Claude Cowork-Remote-Sessions nur freigeben, wenn serverseitige Verarbeitung, gespeicherte Sitzungen/Dateien, geplante Hintergrundaufgaben und die über die Desktop-App erreichbaren lokalen Ordner ausdrücklich dokumentiert und akzeptiert sind ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely)).
21. Claude-Microsoft-365-`write tools` nur separat freigeben; E-Mail-Versand, Kalenderänderungen und Schreibzugriffe in OneDrive/SharePoint erhöhen das Fehlversand- und Fehländerungsrisiko, auch wenn Teams read-only bleibt ([Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide)).
22. Öffentlich zugängliche Webdaten nicht ohne separate Rechtsgrundlagen-, Transparenz- und Art.-9-Prüfung in Trainings-, Fine-Tuning- oder Fremddatensätze für KI übernehmen ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).
23. "Anonymisiert" erst dann als Freigabegrund akzeptieren, wenn die Re-Identifizierbarkeit dokumentiert geprüft wurde; bloßes Entfernen von Namen oder IDs reicht nicht automatisch ([Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).
24. Anthropic Managed Agents nur mit dokumentierten Cron-Zeitplänen, freigegebenen Dateien/GitHub-Zugängen/Memory Stores, enger Vault- und Secret-Begrenzung sowie nachvollziehbarer Run-Historie und klaren Pause-/Archivierungsrechten einsetzen ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults)).
25. Bei Anthropic Enterprise organisations- oder rollenbezogene Modell-Allowlist und Effort-Caps aktiv setzen, damit nicht freigegebene oder retention-pflichtige Modelle technisch begrenzt und nicht nur organisatorisch untersagt werden ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization)).
26. Bei Anthropic Team oder Enterprise prüfen, ob `individual usage analytics` ab dem 11.07.2026 aktiv sind; wenn ja, Zweck, Sichtberechtigungen und interne Transparenzanforderungen für nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill dokumentieren ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans)).
27. Bei interaktiven KI-Systemen wie Chatbots, Agenten oder Avataren den KI-Hinweis grundsätzlich ab der ersten direkten Interaktion klar und unterscheidbar anzeigen; die Ausnahme "ohnehin offensichtlich" eng auslegen ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).
28. Bei veröffentlichten KI-Texten zu Fragen von öffentlichem Interesse eine echte inhaltliche Human Review oder redaktionelle Verantwortung dokumentieren; reine Rechtschreib-, Stil- oder Grammatikkorrektur genügt nach der Kommission nicht ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).
29. EU-Icons für KI-Kennzeichnungen höchstens als Hilfsmittel nutzen; sie ersetzen weder die materielle Art.-50-Prüfung noch die passende Platzierung und Formulierung des Hinweises ([EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content)).
30. Anthropic-`custom connectors` über remote MCP nur freigeben, wenn Ziel-URL, Authentisierung, Zweck und der cloudseitige Verbindungsweg über Anthropic-Server statt über das lokale Gerät dokumentiert und transferrechtlich bewertet sind ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)).
31. Claude Cowork-Remote-Sessions nur dort freigeben, wo getrennt dokumentiert ist, welche Cloud-/Remote-Session-Inhalte laut Anthropic über die Compliance API erreichbar sind, was bei lokalen Sessions nicht zentral exportierbar bleibt und wie laufende Cowork-Aktivität wie Tool-Calls oder Dateizugriffe zusätzlich über OpenTelemetry überwacht oder organisatorisch kompensiert wird ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry)).
32. Für Claude Cowork oder Remote Control auf Team-/Enterprise-Ebene nach Möglichkeit Trusted Devices, restriktive `network-access policy` und kein dauerhaftes `always allow` für freigabepflichtige Tool-Aufrufe erzwingen ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control)).
33. Claude-Microsoft-365-`write tools` nur nach erneuter Tenant-Einwilligung zu den erweiterten Graph-Berechtigungen aktivieren; dabei berücksichtigen, dass derzeit nur E-Mails einen `agent-initiated`-Header tragen, Datei- und Kalender-Schreibvorgänge aber nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector)).
34. Art.-4-KI-VO nicht auf eine allgemeine Einweisung reduzieren: Zielgruppen, Risiko, Nutzungskontext und interne Nachweise zu Schulungen oder anderen Leitmaßnahmen dokumentieren; bloßes Verteilen von Nutzungsanweisungen genügt regelmäßig nicht ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)).
35. ChatGPT Work und Scheduled Tasks nur separat freigeben: lokale Ordnerzugriffe, zulässige Apps/Dateien, Monitoring-Läufe, Benachrichtigungen und Compliance-API-Nachweise dokumentieren; berücksichtigen, dass Tasks in Projekten nicht auf Projektdateien zugreifen ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt)).

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content).

## 16. KI-VO-Kurzcheck zusätzlich zur DSGVO

Die KI-Verordnung ersetzt die DSGVO nicht. Für jeden KI-Einsatz sollte separat dokumentiert werden:

- Fällt der Use Case unter [verbotene KI-Praktiken nach Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5)?
- Liegt ein Hochrisiko-KI-System nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) vor?
- Geht es nur um begrenztes Risiko mit Transparenzpflichten, insbesondere nach [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50)?
- Sind KI-Kompetenz, Schulung und Kontextkenntnis nach [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4) umgesetzt?
- Muss bei Hochrisiko-Einsatz eine Grundrechte-Folgenabschätzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) die DSFA ergänzen?
- Muss bei interaktiven KI-Systemen klar kenntlich gemacht werden, dass Personen mit KI interagieren?
- Werden Deepfakes oder KI-generierte/manipulierte Texte zu Fragen von öffentlichem Interesse veröffentlicht und müssen klar gekennzeichnet werden?

Nach [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113) gilt die Verordnung grundsätzlich ab dem 2. August 2026; Kapitel I und II gelten seit dem 2. Februar 2025, bestimmte GPAI-, Governance- und Sanktionsregeln seit dem 2. August 2025. Für Hochrisiko-KI verweist die Kommission inzwischen auf das im Amtsblatt vom 24.07.2026 veröffentlichte `Digital Omnibus on AI` (Regulation (EU) 2026/1744): Bestimmte Hochrisikobereiche gelten danach ab dem 02.12.2027, in Produkte integrierte Systeme z. B. Robotik oder Industriemaschinen ab dem 02.08.2028 ([AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744)).

Praxis-Hinweis zu Art. 50 KI-VO: Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde laut EU-Kommission am 10.06.2026 veröffentlicht. Der Code ist freiwillig, die Transparenzpflichten selbst gelten aber ab dem 02.08.2026. Nach der Kommissionsmitteilung müssen Nutzer informiert werden, wenn sie mit einem interaktiven KI-System wie einem Chatbot interagieren; außerdem müssen Deepfakes sowie KI-generierte oder KI-manipulierte Texte, die auf Fragen von öffentlichem Interesse abzielen, klar gekennzeichnet werden.

Neu zu berücksichtigen ist, dass die EU-Kommission den Code am 09.07.2026 als angemessenes freiwilliges Instrument zur Erleichterung der Umsetzung von Art. 50 Abs. 2, 4 und 5 KI-VO bewertet hat und der AI Board die Angemessenheitsbewertung am Folgetag übernommen hat. Für Anbieter und Betreiber kann eine Unterzeichnung deshalb als belastbarer Compliance-Baustein dokumentiert werden; sie ersetzt aber keine Einzelfallprüfung und begründet laut Kommission keinen abschließenden Compliance-Nachweis ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der aktualisierte FAQ-Stand des AI Office: Wer vor dem 02.08.2026 in der ersten Signatory-Liste erscheinen will, muss das Signaturformular bis zum 27.07.2026, 18:00 CEST einreichen. Eine spätere Unterzeichnung bleibt möglich; Nicht-Unterzeichner müssen die Einhaltung von Art. 50 KI-VO aber durch andere angemessene Maßnahmen belegen und sollten deshalb ihre Markierungs-, Erkennungs- und Label-Prozesse besonders nachvollziehbar dokumentieren ([Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Neu zu berücksichtigen sind außerdem die Kommissionsleitlinien und FAQ vom 20.07.2026 zu Art. 50 KI-VO: Bei direkter Interaktion mit Chatbots, Agenten oder Avataren soll der KI-Hinweis grundsätzlich ab der ersten Interaktion klar und unterscheidbar erfolgen, sofern die KI-Nutzung nicht ausnahmsweise offensichtlich ist. Für veröffentlichte KI-generierte oder KI-manipulierte Texte zu Fragen von öffentlichem Interesse reicht eine bloß formale Prüfung wie Rechtschreib- oder Grammatikkorrektur nicht als `human review` oder `editorial control`; erforderlich ist eine inhaltliche Prüfung mit fachlichem Urteil oder redaktioneller Verantwortung. Laut derselben FAQ ist nur für vor dem 02.08.2026 in Verkehr gebrachte Systeme eine begrenzte Übergangslogik bei Art. 50 Abs. 2 KI-VO vorgesehen; Inhalte von vor dem 02.08.2026 müssen nicht rückwirkend gekennzeichnet werden. Die von der EU veröffentlichten Icons können als Label-Hilfe genutzt werden, begründen für sich aber keinen Compliance-Nachweis ([Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der FAQ-Stand der Kommission vom 26.07.2026 zu Art. 50 KI-VO: Die Markierungs- und Erkennungspflicht nach Art. 50 Abs. 2 wird dort enger operationalisiert und u. a. für Quellcode, reine Maschine-zu-Maschine-Outputs, rein geschlossene Entwicklungs- oder Produktumgebungen sowie bloßes Standard-Editing verneint; für bestimmte B2B- oder industrielle Kontexte wird nur eine enge Ausnahme beschrieben. Für vor dem 02.08.2026 in Verkehr gebrachte Systeme nennt die Kommission nun ausdrücklich den 02.12.2026 als Ende der begrenzten Übergangsfrist für Art. 50 Abs. 2. Wer den freiwilligen Transparency Code nicht zeichnet, muss alternative angemessene Nachweise vorhalten und kann mit mehr Informationsanfragen rechnen; vollzogen wird Art. 50 im Regelfall durch nationale Marktüberwachungsbehörden, während das AI Office nur begrenzt zuständig ist ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Neu zu berücksichtigen ist außerdem die allgemeine Kommissions-FAQ vom 22.07.2026 zum AI Act: Für Hochrisiko-KI müssen Betreiber die `instructions of use` umsetzen, den Betrieb überwachen, menschliche Aufsicht organisatorisch zuweisen und bei selbst bereitgestellten Eingabedaten auf Relevanz und hinreichende Repräsentativität achten. Öffentliche Stellen und private Anbieter öffentlicher Dienste müssen vor der ersten Nutzung eine Grundrechte-Folgenabschätzung durchführen. Wird der Output eines Hochrisiko-Systems für eine Entscheidung über eine natürliche Person mit Rechtswirkung genutzt, muss eine klare und sinnvolle Erklärung gegenüber der betroffenen Person ermöglicht werden ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

Quellen: [AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content), [Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act).

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
