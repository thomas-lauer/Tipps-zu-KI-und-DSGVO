# Datenschutz-Folgenabschätzung (DSFA) - Vorlage für KI-Nutzung

Stand: 09.08.2026
Status: Vorlage, vor produktivem Einsatz ausfüllen und durch Datenschutzbeauftragte/Rechtsprüfung bewerten lassen.

> Hinweis: Diese Vorlage ersetzt keine Rechtsberatung. Sie orientiert sich an Art. 35 DSGVO, den DPIA-Leitlinien WP248 rev.01/EDPB, DSK-Kurzpapier Nr. 5 und den DSK-Hinweisen zu KI. Wenn Informationen fehlen, als "offen" kennzeichnen.

Quellen: [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EDPB/WP29 DPIA Guidelines WP248 rev.01](https://ec.europa.eu/newsroom/article29/items/611236/en), [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf), [BfDI DSFA-Übersicht](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Technik/Datenschutz-Folgenabschaetzungen.html), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf).

## 1. Stammdaten

| Feld | Angabe |
|---|---|
| Projekt / Verarbeitung |  |
| Verantwortlicher |  |
| Fachbereich |  |
| Datenschutzbeauftragte/r |  |
| Informationssicherheit |  |
| KI-Anbieter / Tool |  |
| Produktplan | Free / Pro / Team / Business / Enterprise / API / Sonstiges |
| Vertragspartner |  |
| AVV/DPA vorhanden | Ja / Nein / offen |
| KI-VO-Rolle | Anbieter / Betreiber / Einführer / Händler / offen |
| KI-VO-Risikoklasse | verboten / Hochrisiko / begrenztes Risiko / minimales Risiko / offen |
| Datum der Bewertung |  |
| Version der DSFA |  |
| Nächste Überprüfung |  |

## 2. Kurzbeschreibung der Verarbeitung

- Zweck der KI-Nutzung:
- Geschäftsprozess:
- Nutzergruppen:
- Eingaben/Prompts:
- Uploads/Dateien:
- Outputs:
- Automatisierungsgrad:
- Wird die KI nur assistiv genutzt?
- Gibt es eine Entscheidung über Personen?
- Werden Chat-Suche/Memory, Konnektoren, Browserzugriff, Computer Use, Cowork, Slack/Teams, E-Mail, Kalender oder lokale Dateien genutzt?
- Werden bei Claude Cowork Remote-Sessions genutzt, bei denen Sitzungen und Dateien im Claude-Account gespeichert werden und geplante Tasks serverseitig ohne online Gerät weiterlaufen ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely))?
- Werden Anthropic Managed Agents mit `scheduled deployments`, Dateien, GitHub-Zugängen, Memory Stores oder Vault-Credentials genutzt, die Sessions autonom per Cron starten können, und ist ausdrücklich bewertet, dass Gesprächsverlauf, Sandbox-Zustand und Outputs serverseitig gespeichert werden und die Funktion derzeit nicht ZDR- oder HIPAA-BAA-fähig ist ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview))?
- Werden bei Anthropic `Inference hooks` genutzt, und ist dokumentiert, welche Prompts vor der Inferenz an den AI-Security-Server gehen, ob Shadow-Mode oder Durchsetzung aktiv ist, wie Failure Handling gesetzt ist und dass die Funktion nur für Claude Enterprise, nicht aber für Bedrock oder Google Cloud verfügbar ist ([Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [Claude Platform release notes, 05.08.2026](https://platform.claude.com/docs/en/release-notes/overview))?
- Werden beim Claude-Microsoft-365-Connector `write tools` genutzt, also E-Mail-Versand/-Organisation, Kalenderänderungen oder Schreibzugriffe in OneDrive/SharePoint; Teams bleibt dabei read-only ([Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide))?
- Werden bei Anthropic `custom connectors` über remote MCP genutzt, und ist dokumentiert, dass die Verbindung zum MCP-Server von Anthropic-Servern statt vom lokalen Gerät ausgeht ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))?
- Ist bei Claude Cowork dokumentiert, ob für Remote-Sessions `network-access policy`, Trusted Devices, restriktives Approval-Verhalten sowie ggf. MDM-Sperren für lokale MCP-Server oder Desktop Extensions gesetzt sind ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control))?
- Ist bekannt und bewertet, dass Anthropic bei Claude Cowork zwischen Cloud-/Remote-Sessions und lokaler Nutzung unterscheidet, mobile/webbasierte Remote-Sessions auf die Compliance API verweist und laufende Aktivität wie Tool-Calls oder Dateizugriffe zugleich gesondert über OpenTelemetry beschreibt ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry))?
- Ist bei Claude Cowork dokumentiert, ob Cloud-Sessions planbezogen standardmäßig aktiviert oder deaktiviert sind, ob auf Enterprise eine zusätzliche Rollen- oder Gruppenfreigabe gesetzt ist, ob schreibfähige Connector-Tools nur pro Aufgabe freigegeben werden und dass Network-Egress-Regeln laut Anthropic nicht für `web fetch`, `web search` oder MCPs gelten ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans))?
- Ist bei Microsoft 365 `write tools` dokumentiert, ob der Tenant den erweiterten Microsoft-Graph-Berechtigungen erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen, Datei- und Kalender-Schreibvorgänge aber nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector))?
- Werden private MCP-Server angebunden und bleibt deren Adresse intern, z. B. über eine outbound-only-Tunnelarchitektur statt über einen öffentlichen Endpoint?
- Werden OpenAI-Funktionen mit eigener Retention genutzt, z. B. Responses API mit `store`, Background Mode, Extended Prompt Caching, Hosted Shell, Code Interpreter, gehostete Skills, Assistants, Threads oder Vector Stores?
- Wird bei OpenAI-API-Nutzung `Fast mode` eingesetzt, und ist dokumentiert, dass dieser Modus laut OpenAI zwar mit Data Residency, Zero Data Retention und BAA kompatibel ist, die Prüfung der konkret genutzten Endpunkte, Tools und der regionalen Verfügbarkeit aber unberührt lässt ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq))?
- Werden ChatGPT Work oder Scheduled Tasks genutzt, und ist dokumentiert, welche lokalen Ordner, Apps oder Dateien freigegeben sind, ob Monitoring- oder Wiederholungsläufe stattfinden, dass Tasks in Projekten nicht auf Projektdateien zugreifen, dass Task-Konversationen in der Compliance API erscheinen und ob `Voice` in Work/Codex dieselben Tool- und Rechtepfade nutzen darf ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex))?
- Ist für berechtigte Enterprise-/Edu-Workspaces mit EKM dokumentiert, ob `Work Cloud`, `Work Local` und die Default-Aktivierung für Mitglieder der Default-Rolle zugelassen sind und wie Cloud-synchronisierte Work-Chats von lokalen Chats auf dem Gerät abgegrenzt werden ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex))?
- Wird bei ChatGPT Desktop dokumentiert, ob In-App-Updates zentral deaktiviert oder zugelassen sind und wer neue Versionen sowie Sicherheitsfixes vor dem Rollout prüft und verteilt ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes))?
- Werden Anthropic-Funktionen mit eigener Retention genutzt, z. B. Claude Enterprise-Projekte, Audit Logs, Message Batches, `covered models` wie Claude Fable 5 oder API-Features ohne ZDR?
- Werden bei Anthropic Team oder Enterprise `individual usage analytics` genutzt oder nach dem Default-Wechsel ab dem 11.07.2026 bewusst deaktiviert, und ist dokumentiert, wer nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill sehen darf ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans))?
- Wird bei Anthropic Enterprise eine organisations- oder rollenbezogene Modell-Allowlist mit Effort-Caps genutzt, damit nur freigegebene Modelle auswählbar sind ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization))?
- Werden bei Anthropic Skills oder Plugins genutzt, und ist dokumentiert, ob `Skill and plugin security scanning` aktiviert ist, dass diese Enterprise-Funktion standardmäßig deaktiviert ist, nur neue Uploads oder Änderungen scannt und wie Warnhinweise für riskante Inhalte behandelt werden ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization))?
- Wird `ChatGPT Voice` in Work oder Codex genutzt, und ist dokumentiert, dass Voice seit den Enterprise-/Edu-Release-Notes vom 07.08.2026 auch Datei-Uploads und Projects unterstützt, dabei auf aktuelle Projekt-Chats, Quellen und Projektanweisungen zugreifen kann und `Live` bei aktivierter Voice-Funktion zum Standard werden kann ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes))?
- Werden öffentlich zugängliche Webquellen oder bereits gescrapte Datensätze für Training, Fine-Tuning oder externe Wissensbestände genutzt, und ist deren Rechtsgrundlage gesondert dokumentiert ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en))?

Praxis-Hinweis: Zentrale Business-Accounts, AVV/DPA, Zero Data Retention, DSFA, dokumentierte Feature-Freigaben für Memory/Chat-Suche, Konnektoren und private MCP-Tunnelarchitekturen sowie eine interne Richtlinie sind Mindestbausteine vor produktiver Nutzung. Bei Claude Cowork sollten Remote-Sessions, gespeicherte Dateien/Sitzungen und erreichbare lokale Ordner getrennt freigegeben werden; bei Microsoft-365-Connectoren gilt das zusätzlich für aktivierte Schreibwerkzeuge. Werden Anthropic Managed Agents genutzt, sollten zusätzlich Zeitpläne, Deployment-Runs/Webhooks, eingebundene Vaults und Secret-Scopes freigegeben und dokumentiert werden; neu ausdrücklich zu bewerten ist dabei auch der serverseitige State ohne ZDR-/HIPAA-BAA-Eignung ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)). Für Anthropic Team und Enterprise sollte außerdem festgehalten werden, ob nutzerbezogene Usage-Analytics aktiv sind oder bewusst deaktiviert wurden. Für Anthropic Enterprise kann die Modellfreigabe inzwischen organisations- und rollenbezogen technisch erzwungen werden; das sollte für retention-pflichtige oder sonst nicht freigegebene Modelle genutzt und dokumentiert werden. Werden Anthropic-Skills oder -Plugins zugelassen, sollte zusätzlich festgehalten werden, ob das optionale Enterprise-Scanning aktiviert ist, dass es nur neue Uploads oder Änderungen erfasst und wie Warnhinweise für riskante Inhalte behandelt werden ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)). Bei Anthropic-`custom connectors` über remote MCP ist zusätzlich zu dokumentieren, dass die Verbindung aus Anthropic-Cloud-Infrastruktur statt vom lokalen Gerät erfolgt. Für Claude Cowork sollte außerdem festgehalten werden, ob Cloud-Sessions planbezogen standardmäßig aktiv sind, ob auf Enterprise zusätzliche Rollen- oder Gruppenfreigaben gesetzt wurden, ob schreibfähige Connector-Tools nur pro Aufgabe freigegeben bleiben und dass `web fetch`, `web search` sowie MCPs gesonderte Kontrollen brauchen. Werden `Inference hooks` genutzt, sollte zusätzlich dokumentiert werden, ob Shadow-Mode oder Durchsetzung aktiv ist, welcher AI-Security-Server eingebunden ist und wie Failure Handling bewertet wurde ([Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)). Bei OpenAI-API-Projekten sollte außerdem getrennt festgehalten werden, ob `Fast mode` genutzt wird; laut OpenAI ist dieser Modus zwar mit Data Residency, ZDR und BAA kompatibel, die Prüfung von Endpunkten, Tools und regionaler Verfügbarkeit entfällt dadurch aber nicht. Bei ChatGPT Work oder Scheduled Tasks sollte getrennt festgehalten werden, welche lokalen Ordner, Apps oder Dateien freigegeben sind, ob monitoringbasierte Wiederholungsläufe stattfinden, wie Benachrichtigungen gesteuert werden und dass Tasks in Projekten nicht auf Projektdateien zugreifen, aber in der Compliance API erscheinen. Neu zu dokumentieren ist auch, ob `Voice` in Work/Codex erlaubt ist, ob Voice Datei-Uploads und Project-Kontext nutzen darf und ob `Work Cloud`, `Work Local` sowie die Default-Aktivierung für Mitglieder der Default-Rolle in berechtigten Enterprise-/Edu-Workspaces mit EKM zugelassen sind ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)). Für ChatGPT Desktop sollte zusätzlich festgehalten werden, ob In-App-Updates zugelassen oder bewusst durch einen eigenen IT-Freigabe- und Patchprozess ersetzt werden. Bei Cowork sollte festgehalten werden, welche Cloud-/Remote-Session-Inhalte laut Anthropic über die Compliance API erreichbar sind, was bei lokalen Sessions nicht zentral exportierbar bleibt und wie laufende Aktivität wie Tool-Calls oder Dateizugriffe zusätzlich über OpenTelemetry überwacht oder organisatorisch kompensiert wird. Die genaue Grenzziehung ist in den Herstellerunterlagen nicht vollständig ausbuchstabiert und sollte deshalb ausdrücklich intern dokumentiert werden. Beim Microsoft-365-Connector sollte außerdem dokumentiert werden, ob der Tenant den erweiterten Graph-Scopes erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen. Als "anonymisiert" deklarierte Daten sollten erst nach dokumentierter Re-Identifikationsprüfung freigegeben werden; nach den neuen EDPB-Entwurfsleitlinien sind dafür insbesondere `No Record Isolation`, `No Linkage` und `No Inference` zu prüfen ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

## 3. Schwellwertanalyse: Ist eine DSFA erforderlich?

| Kriterium | Ja/Nein/offen | Begründung |
|---|---:|---|
| Neue Technologie oder neuartiger KI-Einsatz |  |  |
| Umfangreiche Verarbeitung personenbezogener Daten |  |  |
| Besondere Kategorien nach Art. 9 DSGVO |  |  |
| Daten von Kindern/Jugendlichen |  |  |
| Beschäftigtendaten |  |  |
| Profiling, Scoring oder Bewertung von Personen |  |  |
| Automatisierte Entscheidung mit erheblicher Wirkung |  |  |
| Systematische Überwachung |  |  |
| Zusammenführung mehrerer Datenquellen |  |  |
| Einsatz von RAG/Wissensdatenbank mit internen Dokumenten |  |  |
| Drittlandtransfer in die USA oder andere Drittländer |  |  |
| Agentische Funktionen mit Zugriff auf lokale Daten/Dienste |  |  |
| Hochrisiko-KI oder Profiling nach KI-VO |  |  |
| Grundrechte-Folgenabschätzung nach KI-VO erforderlich |  |  |

Ergebnis: DSFA erforderlich: Ja / Nein / offen  
Begründung:

KI-VO-Hinweis: Die Grundrechte-Folgenabschätzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) ersetzt die DSFA nicht; wenn Pflichten aus einer DSFA nach [Art. 35 DSGVO](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng) bereits erfüllt sind, ergänzt die KI-VO-Abschätzung diese DSFA. Hochrisiko-Einstufungen sind nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) zu dokumentieren.

## 4. Datenkategorien

| Datenkategorie | Beispiele | Erforderlich? | Schutzbedarf |
|---|---|---:|---|
| Kontaktdaten | Name, E-Mail, Telefon |  | niedrig / mittel / hoch |
| Kundendaten | Kundenhistorie, Anfragen, Vertragsdaten |  | niedrig / mittel / hoch |
| Beschäftigtendaten | Rolle, Leistung, Abwesenheit, Kommunikation |  | niedrig / mittel / hoch |
| Art.-9-Daten | Gesundheit, Religion, biometrische Daten |  | hoch |
| Kommunikationsdaten | Chat, E-Mail, Tickets |  | niedrig / mittel / hoch |
| Inhaltsdaten | Dokumente, Code, Dateien, Wissensdatenbank |  | niedrig / mittel / hoch |
| Metadaten/Logs | Nutzer, Zeitpunkt, IP, Token, Fehlerlogs |  | niedrig / mittel / hoch |
| Sonstige |  |  |  |

## 5. Betroffene Personen

- Kunden / Interessenten:
- Beschäftigte:
- Bewerber:
- Lieferanten / Partner:
- Website-Nutzer:
- Kinder/Jugendliche:
- Sonstige:

## 6. Rechtsgrundlagen

| Verarbeitungsschritt | Rechtsgrundlage | Begründung |
|---|---|---|
| Eingabe in KI-System | Art. 6 Abs. 1 ... DSGVO |  |
| Upload von Dokumenten | Art. 6 Abs. 1 ... DSGVO |  |
| Verarbeitung durch Anbieter | Art. 28 DSGVO / eigene Verantwortlichkeit / offen |  |
| Speicherung von Logs | Art. 6 Abs. 1 ... DSGVO |  |
| Art.-9-Daten, falls vorhanden | Art. 9 Abs. 2 ... DSGVO |  |
| Drittlandtransfer | Art. 44 ff. DSGVO, Mechanismus:  |  |

Offene Rechtsfragen:

## 7. Anbieter- und Vertragsprüfung

| Prüfpunkt | Ergebnis |
|---|---|
| AVV/DPA abgeschlossen |  |
| Rolle des Anbieters geklärt | Verantwortlicher / Auftragsverarbeiter / gemeinsam / offen |
| Subprozessoren geprüft |  |
| TOMs erhalten/geprüft |  |
| Chat-Suche/Memory/Projektwissen aktiviert |  |
| Admin-Kontrollen für Zusatzfunktionen geprüft |  |
| OpenAI-Plugins und zugrunde liegende Apps/Rollen getrennt freigegeben |  |
| OpenAI-Skills, Skill-Uploads und etwaige Enterprise-Default-Aktivierung bewertet |  |
| MCP/Konnektoren/Drittserver separat geprüft |  |
| Claude-Cowork-Remote-Sessions, gespeicherte Sitzungen/Dateien und erreichbare lokale Ordner bewertet |  |
| Anthropic-remote-MCP-/Custom-Connectoren mit cloudseitigem Verbindungsweg dokumentiert |  |
| Cowork-Remote-Session-Kontrollen wie `network-access policy`, Trusted Devices und Approval-Verhalten gesetzt |  |
| Unterschied zwischen Cloud-/Remote-Sessions in der Compliance API, lokaler Cowork-Nutzung und separater OpenTelemetry-Aktivität bewertet |  |
| Anthropic-Managed-Agents mit `scheduled deployments`, Deployment-Runs/Webhooks und Lifecycle-Rechten bewertet |  |
| Anthropic-Vaults und Secret-Scopes für MCP- oder `environment_variable`-Credentials dokumentiert |  |
| Microsoft-365-Connector-`write tools` separat freigegeben und begrenzt |  |
| Microsoft-365-`write tools`: Tenant-Re-Consent und fehlende Tagging-Abdeckung für Datei-/Kalenderwrites dokumentiert |  |
| Private MCP-Server/Tunnelarchitektur mit Ziel- und Rollenbegrenzung dokumentiert |  |
| OpenAI-Sync-Apps: Indexierung, Residency-Region und US-Azure-Fallback bewertet |  |
| OpenAI-App-Unterhaltungen/App-Calls in Compliance API bzw. Compliance Logs berücksichtigt |  |
| OpenAI Work/Codex/Agent: dokumentiert, dass Compliance API bzw. Compliance Logs Unterhaltungen und Responses, nicht aber Dateien, Aktionen oder Tool-Calls abdecken |  |
| Für OpenAI-Compliance-Logs mit 30-Tage-Retention ist bei Bedarf ein laufender Export in SIEM/eDiscovery/Data Lake festgelegt |  |
| ChatGPT-Library-Dateien und Chat-Dateien getrennt bewertet; Chat-Löschung löscht gespeicherte Library-Dateien nicht automatisch |  |
| Datenresidenz | EU / USA / global / offen |
| SCC/DPF/TIA geprüft |  |
| Training/Model Improvement deaktiviert |  |
| Zero Data Retention verfügbar und aktiv |  |
| API-spezifische Speicherlogik (z. B. Responses API / Background Mode) geprüft |  |
| Default-Retention ohne ZDR, insbesondere Extended Prompt Caching bei unterstützten OpenAI-Modellen, dokumentiert |  |
| Bei GPAI-Anbietern ist dokumentiert, ob ein aktueller EU-Signaturstatus zum GPAI Code of Practice vorliegt, ohne dies mit DSGVO- oder Feature-Compliance gleichzusetzen |  |
| Modellbezogene Anthropic-Ausnahmen, insbesondere `covered models` bzw. Claude Fable 5 mit 30-Tage-Retention statt ZDR, geprüft |  |
| Getrennte Workspace-, Subscription- oder Sandbox-Konfiguration für solche Anthropic-Modelle dokumentiert |  |
| Anthropic-Modellfreigaben / Effort-Caps organisations- oder rollenbezogen gesetzt |  |
| Anthropic-`individual usage analytics` geprüft, begrenzt und intern transparent dokumentiert |  |
| Nutzung öffentlich zugänglicher Webdaten oder gescrapter Datensätze für Training/Fine-Tuning gesondert geprüft |  |
| Anonymisierungsmethode dokumentiert; Re-Identifikationscheck statt bloßer Pseudonymisierung durchgeführt |  |
| Extended Prompt Caching / Hosted Containers / gehostete Skills geprüft |  |
| Assistants / Threads / Vector Stores gelöscht oder Retention dokumentiert |  |
| Anthropic Message Batches oder sonstige nicht-ZDR-fähige Features ausgeschlossen oder bewertet |  |
| Audit Logs und Datenexporte dokumentiert |  |
| Retention für Chats/Dateien/Logs dokumentiert |  |
| Löschkonzept vorhanden |  |
| Betroffenenrechte umsetzbar |  |

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [File storage and Library in ChatGPT](https://help.openai.com/en/articles/20001052-file-storage-and-library-in-chatgpt), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt), [The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

## 8. Notwendigkeit und Verhältnismäßigkeit

- Warum ist der KI-Einsatz erforderlich?
- Welche weniger eingriffsintensiven Alternativen wurden geprüft?
- Warum reichen lokale Tools, klassische Suche, manuelle Bearbeitung oder anonymisierte Daten nicht aus?
- Welche Daten werden bewusst nicht verarbeitet?
- Wie wird verhindert, dass Nutzer mehr Daten eingeben als erforderlich?
- Gibt es eine Tool-Whitelist und Input-Grenzen?
- Wie wird die Qualität der Ergebnisse geprüft?

## 9. Datenschutzgrundsätze

| Grundsatz | Umsetzung | Bewertung |
|---|---|---|
| Rechtmäßigkeit |  | ausreichend / offen / unzureichend |
| Transparenz | Datenschutzhinweis, interne Richtlinie, Kennzeichnung |  |
| Zweckbindung | klarer Use Case, keine Zweckausweitung |  |
| Datenminimierung | Pseudonymisierung, Prompt-Regeln, Input-Grenzen |  |
| Richtigkeit | Output-Prüfung, Quellenkontrolle |  |
| Speicherbegrenzung | Retention, Löschkonzept |  |
| Integrität/Vertraulichkeit | MFA, SSO, Rollen, Verschlüsselung |  |
| Rechenschaftspflicht | Dokumentation, Freigabe, Review |  |

## 10. Risikoanalyse

Bewertungsskala:

- Eintrittswahrscheinlichkeit: 1 niedrig, 2 mittel, 3 hoch
- Schwere des Schadens: 1 niedrig, 2 mittel, 3 hoch
- Risiko: Wahrscheinlichkeit x Schwere

| Risiko für Betroffene | W | S | Risiko | Maßnahmen | Restrisiko |
|---|---:|---:|---:|---|---:|
| Unbefugte Offenlegung personenbezogener Daten an KI-Anbieter |  |  |  | DPA, Retention, ZDR, Minimierung |  |
| Training/Weiterverwendung von Eingaben |  |  |  | Opt-out/vertraglicher Ausschluss |  |
| Drittlandtransfer ohne ausreichende Grundlage |  |  |  | SCC/DPF/TIA, EU-Residenz |  |
| Falsche personenbezogene KI-Ausgabe |  |  |  | Human Review, Quellenprüfung |  |
| Diskriminierende Ausgabe |  |  |  | Testfälle, Review, keine Letztentscheidung |  |
| Automatisierte Entscheidung nach Art. 22 DSGVO |  |  |  | nur assistiv, menschliche Entscheidung |  |
| Unberechtigter Zugriff durch falsche RAG-Berechtigungen |  |  |  | RBAC, Index-Trennung, Tests |  |
| Prompt-Injection / Datenabfluss bei RAG oder Agenten |  |  |  | Isolation, Allowlist, Logging, Freigabe |  |
| Unvollständige Nachvollziehbarkeit von OpenAI-Agent-Aktionen, Dateien oder Tool-Calls |  |  |  | Export-/SIEM-Konzept, Freigabebegrenzung, Vier-Augen-Prüfung |  |
| Ungewollte Wiederverwendung früherer Chats/Projektinhalte durch Memory oder Chat-Suche |  |  |  | Feature-Freigabe, Retention, Admin-Kontrollen |  |
| Missbrauch von Konnektoren, Browser oder lokalen Dateien |  |  |  | separate Freigabe, Least Privilege |  |
| Cloudseitige remote-MCP-Connectoren oder Cowork-Remote-Sessions führen zu unvollständiger Nachvollziehbarkeit des tatsächlichen Verbindungswegs |  |  |  | Verbindungsweg dokumentieren, Zielsysteme begrenzen, Monitoring-Ersatz festlegen |  |
| Fehlversand oder Fehländerung durch Connector-Schreibwerkzeuge oder Cowork-Write-Aktionen |  |  |  | Ask-before-acting, Vier-Augen-Prüfung, begrenzte Schreibrechte |  |
| Autonome Fehlstarts oder unerwartete Datenverarbeitung durch `scheduled deployments` |  |  |  | enge Cron-Zeitpläne, Run-Historie, Webhooks, Pause-/Archivierungsrechte |  |
| Zu weit gefasste Vault- oder Secret-Freigaben für Managed Agents |  |  |  | Secret-Minimierung, Rotation, Scope-Begrenzung, Audit |  |
| Zu breite Netzfreigabe für private MCP-Server oder REST-Ziele |  |  |  | outbound-only Tunnel, Ziel-Allowlist, Rollen, Audit-Logs |  |
| Rechtswidriges Web-Scraping oder unklare Wiederverwendung fremder Trainingsdatensätze |  |  |  | separate Rechtsgrundlage, Transparenz, Quellenauswahl, Filter, Art.-9-Prüfung |  |
| Pseudonymisierte oder geschwärzte Daten werden irrtümlich als anonym behandelt |  |  |  | Re-Identifikationscheck, Freigabeprozess, Datenminimierung |  |
| Memorisation oder Rekonstruktion personenbezogener Daten aus LLM-Kontexten |  |  |  | Minimierung, Pseudonymisierung, kurze Retention, Tests |  |
| Feature-Retention weicht von ZDR-Annahme ab |  |  |  | endpointbezogene Prüfung, technische Konfiguration, Vertragsnachweis |  |
| Unverhältnismäßige Mitarbeitertransparenz oder faktische Leistungsüberwachung durch nutzerbezogene KI-Analytics |  |  |  | Zweckbegrenzung, Rollenbeschränkung, interne Transparenz, ggf. Mitbestimmung |  |
| Unvollständige KI-VO-Einstufung oder fehlende Transparenz |  |  |  | KI-VO-Kurzcheck, Schulung, Kennzeichnung, Dokumentation |  |
| Unklare Löschung aus Logs/Backups/Indexen |  |  |  | Löschkonzept, Anbieterprüfung |  |
| Fehlende Transparenz gegenüber Betroffenen |  |  |  | Datenschutzhinweise, interne Hinweise |  |

Quellen: [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50).

## 11. Technische und organisatorische Maßnahmen

Mindestmaßnahmen:

- zentraler Business-/Enterprise-/API-Account
- AVV/DPA
- Training/Model Improvement deaktiviert oder ausgeschlossen
- kurze Retention bzw. Zero Data Retention, falls verfügbar
- SSO/MFA
- Rollen- und Berechtigungskonzept
- Tool-Whitelist
- Verbot privater Accounts für Unternehmensdaten
- Prompt-Regeln und Pseudonymisierung
- Upload-Beschränkungen
- Output-Prüfung
- Logging mit Datenschutzbegrenzung
- Incident-Prozess
- Schulung der Nutzer
- regelmäßige Re-Evaluation

Zusatzmaßnahmen für hohe Risiken:

- DSFA-Freigabe durch Datenschutzbeauftragte
- Rechtsfreigabe
- Informationssicherheitsfreigabe
- TIA/Drittlandtransferbewertung
- RAG-Berechtigungstest
- Prompt-Injection-Test
- separate Freigabe für agentische Funktionen
- Pilotphase mit anonymisierten Daten

## 12. KI-VO-Zusatzprüfung

| Prüfpunkt | Ergebnis |
|---|---|
| Verbotene KI-Praktik nach Art. 5 KI-VO ausgeschlossen |  |
| Hochrisiko-Einstufung nach Art. 6 KI-VO geprüft |  |
| Transparenzpflichten nach Art. 50 KI-VO geprüft |  |
| Bei Hochrisiko-KI sind `instructions of use`, laufendes Monitoring und menschliche Aufsicht organisatorisch zugewiesen |  |
| Bei Hochrisiko-KI sind selbst bereitgestellte Eingabedaten auf Relevanz und hinreichende Repräsentativität geprüft |  |
| Bei Einsatz durch öffentliche Stelle oder privaten Anbieter öffentlicher Dienste ist eine Grundrechte-Folgenabschätzung vor Erstnutzung dokumentiert |  |
| Prozess für das Recht auf Erklärung bei entscheidungsrelevanten Hochrisiko-Outputs vorgesehen |  |
| Art.-4-KI-Kompetenz-/Schulungskonzept risikobasiert dokumentiert; interne Nachweise zu Trainings oder anderen Leitmaßnahmen vorhanden |  |
| Direkte Interaktion mit Chatbots/Agenten/Avataren ab erster Interaktion kenntlich gemacht, sofern nicht ausnahmsweise offensichtlich |  |
| Für Art. 50 Abs. 2 ist dokumentiert, ob eine enge Ausnahme greift z. B. Quellcode, reine Maschine-zu-Maschine-Outputs, geschlossene Entwicklungsumgebung oder Standard-Editing |  |
| Für veröffentlichte KI-Texte zu Fragen von öffentlichem Interesse ist dokumentiert, ob echte Human Review oder redaktionelle Verantwortung vorliegt; bloße Rechtschreib-/Grammatikkorrektur reicht nicht |  |
| Gewählte Labels oder EU-Icons nur als Hilfsmittel bewertet; materielle Art.-50-Anforderungen und Platzierung separat geprüft |  |
| Wenn der Transparency Code gezeichnet wird: Signaturstatus, Geltungsbereich und Zuordnung zu konkreten Maßnahmen dokumentiert |  |
| Wenn der Transparency Code nicht gezeichnet wird: alternative Nachweismaßnahmen für Art. 50 Abs. 2, 4 und 5 dokumentiert |  |
| Nutzerhinweis bei Interaktion mit Chatbots oder anderen interaktiven KI-Systemen dokumentiert |  |
| Kennzeichnung von Deepfakes sowie KI-generierten/manipulierten Texten zu öffentlichem Interesse geprüft |  |
| KI-Kompetenz und Schulung nach Art. 4 KI-VO umgesetzt |  |
| Grundrechte-Folgenabschätzung nach Art. 27 KI-VO erforderlich | Ja / Nein / offen |
| Technische Dokumentation / Protokollierung / menschliche Aufsicht relevant |  |

Praxis-Hinweis: Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde am 10.06.2026 veröffentlicht. Er ist freiwillig; die gesetzlichen Transparenzpflichten nach Art. 50 KI-VO gelten ab dem 02.08.2026. In der DSFA sollte deshalb festgehalten werden, wie Interaktionshinweise, Labels, Zuständigkeiten und Ausnahmen für den konkreten Use Case umgesetzt und nachgewiesen werden. Für die Hochrisiko-Einstufung verweist die Kommission inzwischen auf das im Amtsblatt vom 24.07.2026 veröffentlichte `Digital Omnibus on AI` (Regulation (EU) 2026/1744); danach gelten bestimmte Hochrisikobereiche ab dem 02.12.2027 und in Produkte integrierte Systeme ab dem 02.08.2028 ([AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744)).

Seit der Commission Opinion vom 09.07.2026 und der AI-Board-Bewertung vom Folgetag kann in der DSFA zusätzlich dokumentiert werden, ob der freiwillige Transparency Code als Nachweisbaustein genutzt wird. Das ist nur ein Hilfsmittel: Laut Kommission ersetzt die Zeichnung des Codes weder die konkrete Pflichtenumsetzung noch einen abschließenden Compliance-Nachweis ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Der aktualisierte FAQ-Stand des AI Office ergänzt die operative Nachweisfrage: Für die erste Signatory-Liste vor dem 02.08.2026 müssen Signaturformulare bis zum 27.07.2026, 18:00 CEST eingehen. Eine spätere Unterzeichnung bleibt möglich; Nicht-Unterzeichner sollten in der DSFA aber umso klarer dokumentieren, mit welchen alternativen Markierungs-, Erkennungs- und Label-Maßnahmen sie Art. 50 KI-VO erfüllen ([Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der Leitlinienstand der Kommission vom 20.07.2026: Für Chatbots, Agenten und Avatare ist zu dokumentieren, ob der KI-Hinweis ab der ersten direkten Interaktion klar und unterscheidbar erfolgt und ob eine Berufung auf die enge Ausnahme "ohnehin offensichtlich" tragfähig begründet werden kann. Für veröffentlichte KI-generierte oder KI-manipulierte Texte zu Fragen von öffentlichem Interesse reicht eine bloß formale Schlussredaktion wie Rechtschreib- oder Grammatikkorrektur nicht als `human review` oder `editorial control`; die DSFA sollte deshalb festhalten, wer die inhaltliche Prüfung übernimmt, welche fachliche Kompetenz vorliegt und wer die rechtliche Veröffentlichungsverantwortung trägt. Laut FAQ ist nur für vor dem 02.08.2026 in Verkehr gebrachte Systeme eine begrenzte Übergangslogik bei Art. 50 Abs. 2 KI-VO vorgesehen; Inhalte von vor dem 02.08.2026 müssen nicht rückwirkend gekennzeichnet werden. Die neuen EU-Icons können ergänzend genutzt werden, genügen für sich aber nicht als Compliance-Nachweis ([Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der FAQ-Stand der Kommission vom 26.07.2026 zu Art. 50 KI-VO: In der DSFA sollte nun ausdrücklich dokumentiert werden, ob der konkrete Output unter eine enge Ausnahme von Art. 50 Abs. 2 fällt, etwa bei Quellcode, reiner Maschine-zu-Maschine-Kommunikation, geschlossenen Entwicklungs- oder Produktumgebungen oder bloßem Standard-Editing. Für vor dem 02.08.2026 in Verkehr gebrachte Systeme nennt die Kommission nun ausdrücklich den 02.12.2026 als Ende der begrenzten Übergangsfrist für Art. 50 Abs. 2. Wird der freiwillige Transparency Code nicht gezeichnet, sollten alternative Nachweise für Art. 50 Abs. 2, 4 und 5 besonders belastbar dokumentiert werden; vollzogen wird Art. 50 im Regelfall durch nationale Marktüberwachungsbehörden, während das AI Office nur begrenzt zuständig ist ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Neu zu berücksichtigen ist außerdem der veröffentlichte Leitlinienstand der Kommission vom 30.07.2026: Die Leitlinien stellen nun ausdrücklich klar, dass Unterzeichner des Transparency Code sich unionsweit auf dessen Maßnahmen stützen können. Als Vollzugsstellen nennen sie nationale Marktüberwachungsbehörden, das AI Office für seine Zuständigkeiten und den EDPS für EU-Organe. Die DSFA sollte deshalb festhalten, ob ein Code-Beitritt genutzt wird oder welche gleichwertigen Alternativmaßnahmen den Nachweis tragen ([Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Seit dem 02.08.2026 ist Art. 50 KI-VO außerdem im laufenden Vollzug. Laut Kommission beginnen seit diesem Datum AI Office und nationale Behörden mit der Durchsetzung. Die neue Kommissions-Kompaktübersicht fasst die vier Transparenzfallgruppen zusammen und nennt als Bußgeldrahmen für Unternehmen bis zu 15 Mio. EUR oder 3 % des weltweiten Jahresumsatzes; für vor dem 02.08.2026 in Verkehr gebrachte generative Systeme bleibt die Übergangsfrist für Art. 50 Abs. 2 bis Dezember 2026 relevant. Die DSFA sollte deshalb ausdrücklich festhalten, welche Transparenzpflichten live gelten, welche Übergangslogik beansprucht wird und wer laufend deren Umsetzung kontrolliert ([Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems)).

Neu zu berücksichtigen ist außerdem die allgemeine Kommissions-FAQ vom 22.07.2026 zum AI Act: Für Hochrisiko-KI muss die DSFA bzw. die damit verknüpfte KI-VO-Dokumentation festhalten, wie `instructions of use`, laufendes Monitoring, menschliche Aufsicht und die Prüfung der Relevanz bzw. hinreichenden Repräsentativität selbst bereitgestellter Eingabedaten umgesetzt werden. Öffentliche Stellen und private Anbieter öffentlicher Dienste müssen vor der ersten Nutzung grundsätzlich eine Grundrechte-Folgenabschätzung dokumentieren. Wenn der Output eines Hochrisiko-Systems für eine Entscheidung über eine natürliche Person mit Rechtswirkung genutzt wird, sollte die DSFA außerdem festhalten, wie das Recht auf Erklärung operativ erfüllt werden kann ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

Neu zu berücksichtigen ist außerdem die aktuelle Kommissions-Q&A zu Art. 4 KI-VO: Die DSFA oder das begleitende Governance-Konzept sollte dokumentieren, welche Zielgruppen mit dem System arbeiten, wie Schulung und Leitmaßnahmen nach Rolle, Risiko und Nutzungskontext differenziert werden und wie diese Maßnahmen intern nachgewiesen werden. Ein Zertifikat oder eine bestimmte AI-Officer-Struktur verlangt die Kommission nicht; bloßes Verteilen von Nutzungsanweisungen genügt regelmäßig nicht. Die Überwachung und Durchsetzung zu Art. 4 startet ab dem 03.08.2026 ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)).

Quellen: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4), [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content), [Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act).

## 13. Betroffenenrechte

| Recht | Umsetzung |
|---|---|
| Auskunft |  |
| Berichtigung |  |
| Löschung |  |
| Einschränkung |  |
| Widerspruch |  |
| Datenübertragbarkeit |  |
| Art. 22 DSGVO |  |

Offene Punkte:

## 14. Ergebnis und Freigabeentscheidung

Gesamtrisiko vor Maßnahmen: niedrig / mittel / hoch  
Restrisiko nach Maßnahmen: niedrig / mittel / hoch  
Produktive Nutzung erlaubt: Ja / Nein / nur Pilot / nur mit Auflagen

Auflagen:

1. 
2. 
3. 

Unterschriften/Freigaben:

| Rolle | Name | Datum | Freigabe |
|---|---|---:|---|
| Fachbereich |  |  |  |
| Datenschutz |  |  |  |
| Informationssicherheit |  |  |  |
| Geschäftsführung / Leitung |  |  |  |

## 15. Review

Erneute Prüfung bei:

- Anbieterwechsel
- Modellwechsel
- Aktivierung oder Änderung von Chat-Suche/Memory/Projektwissen
- neuer Funktion wie Konnektoren, Computer Use, Cowork oder RAG
- neuem Anthropic-Modell mit `covered model`-Status oder geänderter Retention-Pflicht
- Nutzung neuer Web-Scraping-Quellen oder fremder Trainingsdatensätze
- neue Anonymisierungsmethode oder geänderte Re-Identifikationsbewertung
- neuer Konnektor oder MCP-Server
- Änderung der Datenkategorien
- Änderung der Retention
- neuer Drittlandtransfer
- neue KI-VO-Einstufung, Transparenzpflicht oder Grundrechte-Folgenabschätzung
- Datenschutzvorfall
- neue aufsichtsbehördliche Entscheidung
- spätestens nach 12 Monaten

## Quellen

- [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [EDPB/WP29 DPIA Guidelines WP248 rev.01](https://ec.europa.eu/newsroom/article29/items/611236/en)
- [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf)
- [BfDI DSFA-Übersicht](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Technik/Datenschutz-Folgenabschaetzungen.html)
- [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf)
- [DSK RAG Orientierungshilfe](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf)
- [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf)
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels)
- [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en)
- [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en)
- [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)
- [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context)
- [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans)
- [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs)
- [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention)
- [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing)
- [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4)
- [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5)
- [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6)
- [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27)
- [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50)
- [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems)
- [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)
- [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content)
