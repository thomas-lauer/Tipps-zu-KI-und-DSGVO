# Datenschutz-Folgenabschätzung (DSFA) - Vorlage für KI-Nutzung

Stand: 23.08.2026
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
- Kann bei Anthropic für den konkreten Use Case eine Identitäts- oder Business-Verifikation ausgelöst werden, und ist dokumentiert, wer diese durchführen darf, ob Business-Verifikation statt ad hoc privater Individualverifikation zu nutzen ist und dass Anthropic laut Help Center für die Verifikationsdaten verantwortlich ist, während ID-/Selfie-Bilder laut Anthropic bei Persona liegen und nicht auf Anthropics Systemen kopiert werden; der genaue Scope betroffener Fähigkeiten bleibt dort offen ([Identity verification on Claude](https://support.claude.com/en/articles/14328960-identity-verification-on-claude))?
- Werden bei Claude Cowork Remote-Sessions genutzt, bei denen Sitzungen und Dateien im Claude-Account gespeichert werden und geplante Tasks serverseitig ohne online Gerät weiterlaufen ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely))?
- Werden Anthropic Managed Agents mit `scheduled deployments`, Dateien, GitHub-Zugängen, Memory Stores oder Vault-Credentials genutzt, die Sessions autonom per Cron starten können, und ist ausdrücklich bewertet, dass Gesprächsverlauf, Sandbox-Zustand und Outputs serverseitig gespeichert werden und die Funktion derzeit nicht ZDR- oder HIPAA-BAA-fähig ist ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview))?
- Werden bei Anthropic Managed Agents `inference_geo`, Workspace-Geo, Cloud-Sandbox oder `self-hosted sandboxes` genutzt, und ist dokumentiert, welche Datenpfade in eigener Infrastruktur bleiben und welche Tool-Ein-/Ausgaben weiter an Anthropics Control Plane fließen ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes))?
- Werden bei Anthropic-`self-hosted sandboxes` zusätzlich `memory stores` angebunden, und ist dokumentiert, dass diese laut Anthropic einschließlich Versionshistorie weiter bei Anthropic gehostet bleiben, lokal nur als Arbeitskopie unter `/mnt/memory/` gespiegelt werden und bei fehlgeschlagenem Worker-Teardown zurückbleiben können; sind Bereinigung, Rechte auf diesem Pfad und Isolation zwischen Sessions geregelt ([Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Security model](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes-security))?
- Werden bei Anthropic Managed Agents GitHub-Repositories gemountet, aus denen Skills im Wurzelpfad `.claude/skills` automatisch geladen werden können, und sind Herkunft, Repo-Zugriffsrechte, Branch-/PR-Kontrollen und Skill-Freigaben dokumentiert ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github))?
- Werden bei Anthropic `Inference hooks` genutzt, und ist dokumentiert, welche Prompts vor der Inferenz an den AI-Security-Server gehen, ob Shadow-Mode oder Durchsetzung aktiv ist, wie Failure Handling gesetzt ist und dass die Funktion nur für Claude Enterprise, nicht aber für Bedrock oder Google Cloud verfügbar ist ([Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [Claude Platform release notes, 05.08.2026](https://platform.claude.com/docs/en/release-notes/overview))?
- Werden beim Claude-Microsoft-365-Connector `write tools` genutzt, also E-Mail-Versand/-Organisation, Kalenderänderungen oder Schreibzugriffe in OneDrive/SharePoint; Teams bleibt dabei read-only ([Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide))?
- Werden bei Anthropic `custom connectors` über remote MCP genutzt, und ist dokumentiert, dass die Verbindung zum MCP-Server von Anthropic-Servern statt vom lokalen Gerät ausgeht ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))?
- Werden bei Anthropic Enterprise Connectoren per `Enterprise-managed auth` oder `Restrict verified-domain connectors to your Enterprise` zentral gesteuert, und ist dokumentiert, welche Rollen oder Gruppen Connectoren automatisch erhalten, welche Scopes je Rolle erlaubt sind, dass persönliche Zusatz-Connectoren daneben weiter möglich sein können und ob Unternehmensdomains technisch gegen persönliche Claude-Konten abgegrenzt werden ([Authorize MCP connectors for your entire organization](https://support.claude.com/en/articles/15537633-authorize-mcp-connectors-for-your-entire-organization), [Restrict verified-domain connectors to your Enterprise](https://support.claude.com/en/articles/15402193-restrict-verified-domain-connectors-to-your-enterprise), [Set up role-based permissions on Enterprise plans](https://support.claude.com/en/articles/13930458-set-up-role-based-permissions-on-enterprise-plans), [Manage custom roles on Enterprise plans](https://support.claude.com/en/articles/13930452-manage-custom-roles-on-enterprise-plans))?
- Ist bei Claude Cowork dokumentiert, ob für Remote-Sessions `network-access policy`, Trusted Devices, restriktives Approval-Verhalten sowie ggf. MDM-Sperren für lokale MCP-Server oder Desktop Extensions gesetzt sind ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control))?
- Ist bekannt und bewertet, dass Anthropic bei Claude Cowork zwischen Cloud-/Remote-Sessions und lokaler Nutzung unterscheidet, Cloud-Sessions über Claude, Claude Desktop und Claude Mobile auf die Compliance API verweist und lokale Cowork-Sitzungsinhalte für Enterprise betaweise ebenfalls abrufbar sein können, während für lokale Sessions laut Anthropic derzeit keine Lösch-Endpunkte dokumentiert sind; zugleich beschreibt Anthropic laufende Aktivität wie Tool-Calls oder Dateizugriffe gesondert über OpenTelemetry ([Access the Compliance API](https://support.claude.com/en/articles/13015708-access-the-compliance-api), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry))?
- Ist bei Claude Cowork dokumentiert, ob Cloud-Sessions planbezogen standardmäßig aktiviert oder deaktiviert sind, ob auf Enterprise eine zusätzliche Rollen- oder Gruppenfreigabe gesetzt ist, ob schreibfähige Connector-Tools nur pro Aufgabe freigegeben werden und dass Network-Egress-Regeln laut Anthropic nicht für `web fetch`, `web search` oder MCPs gelten ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans))?
- Ist bei Microsoft 365 `write tools` dokumentiert, ob der Tenant den erweiterten Microsoft-Graph-Berechtigungen erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen, Datei- und Kalender-Schreibvorgänge aber nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector))?
- Werden private MCP-Server angebunden und bleibt deren Adresse intern, z. B. über eine outbound-only-Tunnelarchitektur statt über einen öffentlichen Endpoint?
- Werden OpenAI-Funktionen mit eigener Retention genutzt, z. B. Responses API mit `store`, Background Mode, Extended Prompt Caching, Hosted Shell, Code Interpreter, gehostete Skills, Assistants, Threads oder Vector Stores?
- Wird die OpenAI-`Compliance Platform` genutzt, und ist dokumentiert, dass sie laut OpenAI aus einer `Compliance Logs Platform` für unveränderliche, nur anhängbare Audit-Events und einer `Stateful Compliance API` für zustandsbezogene Abfragen besteht, dass Logs 30 Tage vorgehalten werden, längere Aufbewahrung einen laufenden Export erfordert, Löschungen intern protokollierte Audit-/Security-Daten nicht beseitigen und alle authentifizierten Zugriffe auf diese API selbst protokolliert werden ([OpenAI Compliance Platform for Enterprise and Edu Customers](https://help.openai.com/en/articles/9261474-openai-compliance-platform-for-enterprise-and-edu-customers))?
- Wird bei OpenAI-API-Nutzung `Fast mode` eingesetzt, und ist dokumentiert, dass dieser Modus laut OpenAI zwar mit Data Residency, Zero Data Retention und BAA kompatibel ist, die Prüfung der konkret genutzten Endpunkte, Tools und der regionalen Verfügbarkeit aber unberührt lässt ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq))?
- Wird `ChatGPT search` genutzt, und ist dokumentiert, dass OpenAI dafür disassoziierte Suchanfragen sowie gegebenenfalls strukturierte Prompt-Daten an Bing oder spezialisierte Datenanbieter sendet, dass die IP-Adresse selbst laut OpenAI nicht geteilt wird, ein ungefährer Standort aus der IP aber geteilt werden kann, und wie Workspace- bzw. Rollenfreigaben dafür gesetzt sind ([ChatGPT search for Enterprise and Edu](https://help.openai.com/en/articles/10093903-chatgpt-search-for-enterprise-and-edu))?
- Werden ChatGPT Work oder Scheduled Tasks genutzt, und ist dokumentiert, welche lokalen Ordner, Apps oder Dateien freigegeben sind, ob Monitoring- oder Wiederholungsläufe stattfinden, dass Tasks in Projekten nicht auf Projektdateien zugreifen, dass Task-Konversationen in der Compliance API erscheinen und ob `Voice` in Work/Codex dieselben Tool- und Rechtepfade nutzen darf ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex))?
- Ist für berechtigte Enterprise-/Edu-Workspaces mit EKM dokumentiert, ob `Work Cloud`, `Work Local` und die Default-Aktivierung für Mitglieder der Default-Rolle zugelassen sind und wie Cloud-synchronisierte Work-Chats von lokalen Chats auf dem Gerät abgegrenzt werden ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex))?
- Wird bei ChatGPT Desktop dokumentiert, ob In-App-Updates zentral deaktiviert oder zugelassen sind und wer neue Versionen sowie Sicherheitsfixes vor dem Rollout prüft und verteilt ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes))?
- Sind in ChatGPT Enterprise/Edu noch Altfälle mit individuell autorisierter App-Synchronisierung betroffen, obwohl OpenAI seit dem 10.08.2026 keine neuen solchen Verbindungen mehr zulässt und ab dem 14.08.2026 bestehende deaktiviert sowie mit der Löschung zugehöriger Sync-Daten beginnt; falls synchronisiertes Wissen weiter nötig ist, sind admin-gemanagte Syncs oder rein nicht-synchronisierte Plugins/Apps freigegeben und dokumentiert ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt))?
- Wird in ChatGPT Business oder Enterprise `Computer History` genutzt, obwohl OpenAI die Funktion laut Release Notes vom 20.08.2026 nun auch im EEA, im Vereinigten Königreich und in der Schweiz verfügbar macht, sie standardmäßig deaktiviert bleibt, `Memories` voraussetzt, im Workspace eine Admin-Freigabe braucht und nur nach individuellem Opt-in Interaktionsereignisse aus ausgewählten Apps und Websites einbezieht ([ChatGPT Business - Release Notes](https://help.openai.com/en/articles/11391654-chatgpt-business-release-notes), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Computer History](https://developers.openai.com/codex/customization/computer-history))?
- Wird in ChatGPT Work oder Codex auf Apple-Silicon-Macs das `Apple Messages`-Plugin genutzt, und ist dokumentiert, dass es iMessage-, SMS- und RCS-Konversationen lesen und durchsuchen sowie Nachrichten vorbereiten oder senden kann, dass standardmäßig die Freigabe von Nachricht und Empfängern erforderlich ist und dass dauerhafte Sendefreigaben pro Chat gesondert bewertet sind ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Plugins - ChatGPT Learn](https://developers.openai.com/codex/plugins))?
- Werden schreibgeschützte Codex-Snapshots oder Workspace-Share-Links genutzt, und ist dokumentiert, dass Snapshots laut OpenAI u. a. Nachrichten, Reasoning-Zusammenfassungen, Bilder, Dateipfade und Diffs enthalten können, während nur bekannte Secret-Muster automatisch redigiert werden und sensible Inhalte dennoch verbleiben können ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Use ChatGPT](https://developers.openai.com/codex/use-chatgpt))?
- Werden für Codex-Automatisierungen dedizierte `service accounts` oder persönliche `access tokens` genutzt, und ist dokumentiert, welche Rollen, Gruppen, Plugins, Token-Laufzeiten und vertrauenswürdigen Runner dafür freigegeben sind ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Service accounts](https://learn.chatgpt.com/docs/enterprise/service-accounts), [Access tokens](https://learn.chatgpt.com/docs/enterprise/access-tokens))?
- Werden OpenAI-`Admin APIs` oder `Admin keys` genutzt, und ist dokumentiert, welche Endpoint-Kategorien, Laufzeiten und Rollenfreigaben sie haben, dass sie keinen Modellzugriff gewähren, von `service-account access tokens` zu trennen sind und sensitive Compliance-Scopes nur Workspace-Ownern offenstehen ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Managing Admin keys in the Credentials tab](https://help.openai.com/en/articles/20001407-managing-admin-keys-in-the-credentials-tab))?
- Werden OpenAI-`workspace agents` oder aus `app templates` veröffentlichte Workspace-Apps genutzt, und ist dokumentiert, welche Rollen Agents in das gemeinsame Directory veröffentlichen dürfen, welche App-Aktionen pro Agent erlaubt sind, wann Endnutzer Freigaben erteilen müssen und ob providerbezogene Konfigurationen wie OAuth-Credentials, Webhooks oder `managed MCP server URLs` für GitHub Enterprise, Snowflake oder Databricks tatsächlich freigegeben sind ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps))?
- Wird statt normaler ChatGPT-/Codex-Agentik `OpenAI Presence` genutzt, und ist deployment-spezifisch dokumentiert, welche Daten der Agent sehen darf, welche Guardrails, Freigaben, Session-Aufzeichnungen oder Action-Historien aktiviert sind, wie Maskierung und Retention geregelt sind und wer auf diese Daten zugreifen darf ([OpenAI Presence](https://help.openai.com/en/articles/20001405), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes))?
- Sind bei OpenAI `Workspace analytics`, `Task insights`, Audit-Ansichten im `Global Admin Console` oder das `Personal Analytics plugin` aktiviert, und ist dokumentiert, wer Audit-Ereignisse, per-user usage metrics, CSV-Exporte oder aggregierte Workspace-Trends sehen darf, dass Workspace Analytics laut OpenAI kein Rohlog-Interface ist und dass in EU-Residency-Workspaces `Task insights` standardmäßig aus ist, bereits erzeugte aggregierte Daten laut OpenAI bei späterem Abschalten aber derzeit nicht gelöscht werden ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Workspace analytics for ChatGPT Enterprise and Edu](https://help.openai.com/en/articles/10875114-workspace-analytics-for-chatgpt-enterprise-and-edu), [Global Admin Console](https://help.openai.com/en/articles/12289294-global-admin-console))?
- Ist die OpenAI-Rollenlogik mit additiver RBAC dokumentiert, also `Default`/`On`/`Off`, Mehrfachrollen, explizites `Off` als Sperre trotz anderer Freigaben und ein möglicher zusätzlicher Eingriff von `Lockdown Mode`, bevor Funktionen wie Websuche, Apps, Work oder Agentik freigegeben werden ([Role Based Access Controls for ChatGPT Enterprise](https://help.openai.com/en/articles/11750701))?
- Werden Anthropic-Funktionen mit eigener Retention genutzt, z. B. Claude Enterprise-Projekte, Audit Logs, Message Batches, `covered models` wie Claude Fable 5 oder API-Features ohne ZDR?
- Werden in der Anthropic Console noch `Workbench (legacy)`-Altbestände genutzt, und ist dokumentiert, dass der neue `Playground` laut Anthropic keine Prompt-Historie oder Gespräche serverseitig speichert, während gespeicherte Legacy-Workbench-Daten nur bis zum 01.09.2026 exportiert werden können und danach nicht mehr wiederherstellbar sind ([How do I use the playground?](https://support.claude.com/en/articles/8606378-how-do-i-use-the-playground))?
- Werden bei Anthropic Team oder Enterprise `individual usage analytics` genutzt oder nach dem Default-Wechsel ab dem 11.07.2026 bewusst deaktiviert, und ist dokumentiert, wer nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill sehen darf ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans))?
- Wird bei Anthropic Enterprise eine organisations- oder rollenbezogene Modell-Allowlist mit Effort-Caps genutzt, damit nur freigegebene Modelle auswählbar sind ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization))?
- Werden bei Anthropic Skills oder Plugins genutzt, und ist dokumentiert, ob `Skill and plugin security scanning` aktiviert ist, dass diese Enterprise-Funktion standardmäßig deaktiviert ist, nur neue Uploads oder Änderungen scannt und wie Warnhinweise für riskante Inhalte behandelt werden ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization))?
- Wird `Claude Tag` in Slack genutzt, und ist dokumentiert, in welchen Kanälen oder Rollen es unter der Organisationsidentität arbeiten darf, welche Direct-Message-Nutzung stattdessen über persönliche Claude-Konten läuft, wie kanal- bzw. workspacebezogene Memory überprüft oder gelöscht wird und wie sich die 30-Tage-Löschung in Claude nach Trennung oder Deinstallation von den Slack-Retention-Regeln abgrenzt ([What is Claude Tag?](https://support.claude.com/en/articles/15594475-what-is-claude-tag))?
- Ist für Anthropic-Enterprise-Domain-Claiming dokumentiert, ob SSO erzwungen, JIT oder SCIM aktiviert, alle betroffenen Nutzer im IdP vorhanden und die betroffenen persönlichen Claude-Konten vorab inventarisiert sind, dass nach Aktivierung von `Migrate accounts using your domain` ein organisationsweites 30-Tage-Fenster gilt und dass bei HIPAA-readiness oder CMEK laut Anthropic nur `join fresh` ohne Datenübernahme möglich ist ([Claim and migrate accounts on your domain](https://support.claude.com/en/articles/14625619-claim-and-migrate-accounts-on-your-domain))?
- Ist bei Anthropic zusätzlich dokumentiert, ob persönliche Claude-Konten freiwillig in Team oder Enterprise migriert werden dürfen, welche Inhalte laut Anthropic mitwandern können (z. B. Chats, Projekte, Tasks, Memory, Projekt-Sync-Konfigurationen) und welche ausdrücklich nicht mitwandern (z. B. Custom Skills, App-Logins, eigene Connectoren, öffentliche Share-Links, Cowork-Task-/Session-Historien, lokale Cowork-Daten, Claude-Code-Cloud-Sessions) ([Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization))?
- Wird `ChatGPT Voice` in Work oder Codex genutzt, und ist dokumentiert, dass Voice seit den Enterprise-/Edu-Release-Notes vom 07.08.2026 auch Datei-Uploads und Projects unterstützt, dabei auf aktuelle Projekt-Chats, Quellen und Projektanweisungen zugreifen kann und `Live` bei aktivierter Voice-Funktion zum Standard werden kann ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes))?
- Werden Outputs von OpenAI oder Anthropic veröffentlicht, geteilt oder in DMS-, RAG- oder Kommunikationsprozesse übernommen, und ist dokumentiert, welche maschinenlesbaren Herkunftssignale der konkrete Anbieter-, Modalitäts- und Exportpfad tatsächlich unterstützt, wie `openai.com/verify` oder andere Prüfwege eingebunden sind und wo Signale bei Copy/Paste, Konvertierung oder nicht unterstützten Pfaden entfallen können ([EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content), [How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content))?
- Werden öffentlich zugängliche Webquellen oder bereits gescrapte Datensätze für Training, Fine-Tuning oder externe Wissensbestände genutzt, und ist deren Rechtsgrundlage gesondert dokumentiert ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en))?

Praxis-Hinweis: Zentrale Business-Accounts, AVV/DPA, Zero Data Retention, DSFA, dokumentierte Feature-Freigaben für Memory/Chat-Suche, Konnektoren und private MCP-Tunnelarchitekturen sowie eine interne Richtlinie sind Mindestbausteine vor produktiver Nutzung. Bei Claude Cowork sollten Remote-Sessions, gespeicherte Dateien/Sitzungen und erreichbare lokale Ordner getrennt freigegeben werden; bei Microsoft-365-Connectoren gilt das zusätzlich für aktivierte Schreibwerkzeuge. Wird bei Anthropic eine Identitäts- oder Business-Verifikation ausgelöst, sollte vorab festgelegt sein, welche benannten Personen sie durchführen dürfen und wie der zusätzliche Datenfluss zu Anthropic und Persona dokumentiert wird ([Identity verification on Claude](https://support.claude.com/en/articles/14328960-identity-verification-on-claude)). Werden Anthropic Managed Agents genutzt, sollten zusätzlich Zeitpläne, Deployment-Runs/Webhooks, eingebundene Vaults und Secret-Scopes freigegeben und dokumentiert werden; neu ausdrücklich zu bewerten ist dabei auch der serverseitige State ohne ZDR-/HIPAA-BAA-Eignung ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)). Zusätzlich sollte festgehalten werden, ob `inference_geo`, Workspace-Geo, Cloud-Sandbox oder `self-hosted sandboxes` genutzt werden; `self-hosted` hält Tool-Ausführung, Dateisystem und Network Egress zwar in eigener Infrastruktur, Tool-Ein- und -Ausgaben fließen laut Anthropic aber weiter an die Control Plane. Werden dabei `memory stores` genutzt, ist zusätzlich zu dokumentieren, dass deren Inhalte samt Versionshistorie bei Anthropic verbleiben, lokal nur als Arbeitskopie unter `/mnt/memory/` liegen und bei fehlgeschlagenem Teardown bereinigt werden müssen ([Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Security model](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes-security)). Werden GitHub-Repositories gemountet, ist zudem zu dokumentieren, ob daraus Skills aus `.claude/skills` automatisch geladen werden dürfen und welche Repo-, Branch- und Freigabekontrollen dafür gelten ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github)). Für Anthropic Team und Enterprise sollte außerdem festgehalten werden, ob nutzerbezogene Usage-Analytics aktiv sind oder bewusst deaktiviert wurden. Für Anthropic Enterprise kann die Modellfreigabe inzwischen organisations- und rollenbezogen technisch erzwungen werden; das sollte für retention-pflichtige oder sonst nicht freigegebene Modelle genutzt und dokumentiert werden. Werden Anthropic-Skills oder -Plugins zugelassen, sollte zusätzlich festgehalten werden, ob das optionale Enterprise-Scanning aktiviert ist, dass es nur neue Uploads oder Änderungen erfasst und wie Warnhinweise für riskante Inhalte behandelt werden ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)). Bei Anthropic-`custom connectors` über remote MCP ist zusätzlich zu dokumentieren, dass die Verbindung aus Anthropic-Cloud-Infrastruktur statt vom lokalen Gerät erfolgt. Für Claude Cowork sollte außerdem festgehalten werden, ob Cloud-Sessions planbezogen standardmäßig aktiv sind, ob auf Enterprise zusätzliche Rollen- oder Gruppenfreigaben gesetzt wurden, ob schreibfähige Connector-Tools nur pro Aufgabe freigegeben bleiben und dass `web fetch`, `web search` sowie MCPs gesonderte Kontrollen brauchen. Werden `Inference hooks` genutzt, sollte zusätzlich dokumentiert werden, ob Shadow-Mode oder Durchsetzung aktiv ist, welcher AI-Security-Server eingebunden ist und wie Failure Handling bewertet wurde ([Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)). Bei OpenAI-API-Projekten sollte außerdem getrennt festgehalten werden, ob `Fast mode` genutzt wird; laut OpenAI ist dieser Modus zwar mit Data Residency, ZDR und BAA kompatibel, die Prüfung von Endpunkten, Tools und regionaler Verfügbarkeit entfällt dadurch aber nicht. Bei ChatGPT Work oder Scheduled Tasks sollte getrennt festgehalten werden, welche lokalen Ordner, Apps oder Dateien freigegeben sind, ob monitoringbasierte Wiederholungsläufe stattfinden, wie Benachrichtigungen gesteuert werden und dass Tasks in Projekten nicht auf Projektdateien zugreifen, aber in der Compliance API erscheinen. Neu zu dokumentieren ist auch, ob `Voice` in Work/Codex erlaubt ist, ob Voice Datei-Uploads und Project-Kontext nutzen darf und ob `Work Cloud`, `Work Local` sowie die Default-Aktivierung für Mitglieder der Default-Rolle in berechtigten Enterprise-/Edu-Workspaces mit EKM zugelassen sind ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)). Für OpenAI-Apps ist ab dem 14.08.2026 zusätzlich festzuhalten, ob noch Altbestände individuell autorisierter Sync-Verbindungen betroffen sind, welche Sync-Daten gelöscht werden sollen und ob ein Wechsel auf admin-gemanagte oder rein nicht-synchronisierte Nutzung umgesetzt wurde ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)). Für ChatGPT-Administrationsschnittstellen ist zusätzlich festzuhalten, ob `Admin keys` überhaupt genutzt werden, wie ihre Scopes, Laufzeiten und Owner-/Admin-Zuordnungen begrenzt sind und dass sie von `service-account access tokens` getrennt verwaltet werden ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Managing Admin keys in the Credentials tab](https://help.openai.com/en/articles/20001407-managing-admin-keys-in-the-credentials-tab)). Für ChatGPT Desktop sollte zusätzlich festgehalten werden, ob In-App-Updates zugelassen oder bewusst durch einen eigenen IT-Freigabe- und Patchprozess ersetzt werden. Bei Cowork sollte festgehalten werden, welche Cloud-/Remote-Session-Inhalte laut Anthropic über die Compliance API erreichbar sind, was bei lokalen Sessions nicht zentral exportierbar bleibt und wie laufende Aktivität wie Tool-Calls oder Dateizugriffe zusätzlich über OpenTelemetry überwacht oder organisatorisch kompensiert wird. Die genaue Grenzziehung ist in den Herstellerunterlagen nicht vollständig ausbuchstabiert und sollte deshalb ausdrücklich intern dokumentiert werden. Beim Microsoft-365-Connector sollte außerdem dokumentiert werden, ob der Tenant den erweiterten Graph-Scopes erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen. Als "anonymisiert" deklarierte Daten sollten erst nach dokumentierter Re-Identifikationsprüfung freigegeben werden; nach den neuen EDPB-Entwurfsleitlinien sind dafür insbesondere `No Record Isolation`, `No Linkage` und `No Inference` zu prüfen ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Security model](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes-security), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Managing Admin keys in the Credentials tab](https://help.openai.com/en/articles/20001407-managing-admin-keys-in-the-credentials-tab), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

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
| Anthropic-Managed-Agents: `inference_geo`, Workspace-Geo und Cloud-vs.-`self-hosted` dokumentiert |  |
| Anthropic-Managed-Agents: gemountete GitHub-Repositories und `.claude/skills` gesondert freigegeben |  |
| Microsoft-365-Connector-`write tools` separat freigegeben und begrenzt |  |
| Microsoft-365-`write tools`: Tenant-Re-Consent und fehlende Tagging-Abdeckung für Datei-/Kalenderwrites dokumentiert |  |
| Private MCP-Server/Tunnelarchitektur mit Ziel- und Rollenbegrenzung dokumentiert |  |
| OpenAI-Sync-Apps: Indexierung, Residency-Region und US-Azure-Fallback bewertet |  |
| OpenAI-`ChatGPT search`: Web-search-Freigabe, externe Datenanbieter, ungefährer Standort aus IP und RBAC bewertet |  |
| OpenAI-App-Unterhaltungen/App-Calls in Compliance API bzw. Compliance Logs berücksichtigt |  |
| OpenAI Work/Codex/Agent: dokumentiert, dass Compliance API bzw. Compliance Logs Unterhaltungen und Responses, nicht aber Dateien, Aktionen oder Tool-Calls abdecken |  |
| Für OpenAI-Compliance-Logs mit 30-Tage-Retention ist bei Bedarf ein laufender Export in SIEM/eDiscovery/Data Lake festgelegt |  |
| ChatGPT-Library-Dateien und Chat-Dateien getrennt bewertet; Chat-Löschung löscht gespeicherte Library-Dateien nicht automatisch |  |
| ChatGPT-Enterprise-`Computer History` und einbezogene Apps/Websites bewertet |  |
| OpenAI-Codex-Automatisierung: `service accounts`, Plugins, Token-Laufzeiten und Trusted Runner dokumentiert |  |
| OpenAI-`workspace agents`/`app templates`: Publishing-Rechte, App-Aktionen, Freigabe- und `managed MCP`-Konfiguration dokumentiert |  |
| OpenAI-`Workspace analytics`/`Task insights`/`Personal Analytics plugin`: Zweck, Rollen, Exporte, EU-Residency-Default und Nicht-Löschung bereits erzeugter aggregierter `Task insights`-Daten bewertet |  |
| OpenAI-RBAC-Logik mit `Default`/`On`/`Off`, Mehrfachrollen und `Lockdown Mode` dokumentiert |  |
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
| Anthropic-`Claude Tag`: Kanal-/Workspace-Memory, Slack-vs.-Claude-Historie, DM-vs.-Organisationsidentität und 30-Tage-Löschung bewertet |  |
| Anthropic-Connector-Governance: `verified-domain`-Sperre, `Enterprise-managed auth`, Rollen-/Scope-Zuweisung und serverseitige Durchsetzung bewertet |  |
| Anthropic-Domain-Claiming/Migration: SSO/JIT/SCIM, IdP-Abgleich, 30-Tage-Frist, Deaktivierung nicht migrierter Privatkonten, HIPAA-/CMEK-Ausnahme und produktbezogene Migrationsgrenzen wie `Claude Design` ab/nicht vor 14.08.2026 bewertet ([Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization)) |  |
| Nutzung öffentlich zugänglicher Webdaten oder gescrapter Datensätze für Training/Fine-Tuning gesondert geprüft |  |
| Anonymisierungsmethode dokumentiert; Re-Identifikationscheck statt bloßer Pseudonymisierung durchgeführt |  |
| Extended Prompt Caching / Hosted Containers / gehostete Skills geprüft |  |
| Assistants / Threads / Vector Stores gelöscht oder Retention dokumentiert |  |
| Anthropic Message Batches oder sonstige nicht-ZDR-fähige Features ausgeschlossen oder bewertet |  |
| Audit Logs und Datenexporte dokumentiert |  |
| Retention für Chats/Dateien/Logs dokumentiert |  |
| Löschkonzept vorhanden |  |
| Betroffenenrechte umsetzbar |  |

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Service accounts](https://learn.chatgpt.com/docs/enterprise/service-accounts), [Access tokens](https://learn.chatgpt.com/docs/enterprise/access-tokens), [ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [File storage and Library in ChatGPT](https://help.openai.com/en/articles/20001052-file-storage-and-library-in-chatgpt), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt), [The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

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
| Zusätzliche Nutzungs- oder Beschäftigtentransparenz durch `Computer History` |  |  |  | Rollenfreigabe, Opt-in, App-/Site-Begrenzung, Transparenz, ggf. Mitbestimmung |  |
| Persönliche Tokens oder überprivilegierte `service accounts` in Codex-Automatisierungen |  |  |  | Service-Account-Trennung, Least Privilege, Token-Rotation, Trusted Runner |  |
| Unverhältnismäßige Mitarbeitertransparenz oder faktische Leistungsüberwachung durch nutzerbezogene KI-Analytics |  |  |  | Zweckbegrenzung, Rollenbeschränkung, interne Transparenz, ggf. Mitbestimmung |  |
| Kontosperre, ungeplante Datenübernahme oder Datenverlust bei Anthropic-Domain-Claiming |  |  |  | IdP-Abgleich, SSO/JIT/SCIM vor Aktivierung, Nutzerkommunikation, Fristmanagement, dokumentierte `join fresh`-/Merge-Entscheidung |  |
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
| Für genutzte Anbieter ist dokumentiert, welche maschinenlesbaren Markierungen oder Herkunftssignale im konkreten Workflow tatsächlich verfügbar und prüfbar sind und wo sie entfallen können ([EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content), [How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content)) |  |
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

Neu zu berücksichtigen ist außerdem der am 11.08.2026 verifizierte Herstellerstand zu Art.-50-bezogenen Herkunftssignalen: Anthropic beschreibt nun maschinenlesbare Markierungen für unterstützte Claude-Modelle mit eingebetteten Wasserzeichen für Text und digital signierten Provenance-Metadaten für unterstützte Dateien; OpenAI verweist in seiner aktualisierten EU-AI-Act-Guidance auf Trainingsdatensummaries, C2PA/SynthID, `openai.com/verify` und eine Content Provenance API, beschreibt in der separaten Provenance-Dokumentation derzeit aber nur unterstützte Bilder und Audiodateien als konkret abgedeckte Modalitäten. Die DSFA sollte deshalb ausdrücklich festhalten, ob der konkrete Workflow solche Signale überhaupt erzeugt, erhält und prüfbar macht oder ob eigene Kennzeichnungs- und Nachweismaßnahmen erforderlich bleiben ([How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Quellen: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4), [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content), [Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act), [How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content).

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
- [ChatGPT Business - Release Notes](https://help.openai.com/en/articles/11391654-chatgpt-business-release-notes)
- [ChatGPT search for Enterprise and Edu](https://help.openai.com/en/articles/10093903-chatgpt-search-for-enterprise-and-edu)
- [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)
- [Computer History](https://developers.openai.com/codex/customization/computer-history)
- [OpenAI Presence](https://help.openai.com/en/articles/20001405)
- [Workspace analytics for ChatGPT Enterprise and Edu](https://help.openai.com/en/articles/10875114-workspace-analytics-for-chatgpt-enterprise-and-edu)
- [Global Admin Console](https://help.openai.com/en/articles/12289294-global-admin-console)
- [Role Based Access Controls for ChatGPT Enterprise](https://help.openai.com/en/articles/11750701)
- [Plugins - ChatGPT Learn](https://developers.openai.com/codex/plugins)
- [Use ChatGPT](https://developers.openai.com/codex/use-chatgpt)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels)
- [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en)
- [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en)
- [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)
- [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context)
- [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans)
- [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs)
- [What is Claude Tag?](https://support.claude.com/en/articles/15594475-what-is-claude-tag)
- [Claim and migrate accounts on your domain](https://support.claude.com/en/articles/14625619-claim-and-migrate-accounts-on-your-domain)
- [Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization)
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
