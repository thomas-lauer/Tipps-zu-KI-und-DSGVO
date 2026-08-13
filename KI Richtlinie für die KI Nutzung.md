# KI-Richtlinie für die KI-Nutzung

Stand: 13.08.2026
Status: Vorlage für Unternehmen/Organisationen

> Ziel dieser Richtlinie ist eine produktive, sichere und DSGVO-konforme Nutzung von KI-Systemen wie Claude.ai, OpenAI/ChatGPT, API-Diensten, RAG-Systemen und vergleichbaren Tools. Diese Vorlage muss an Organisation, Rollen, Tools und Rechtsgrundlagen angepasst werden.

Quellen: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [DSK KI-Systeme TOM](https://datenschutzkonferenz-online.de/media/oh/DSK-OH_KI-Systeme.pdf), [DSK RAG](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf), [DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113).

## 1. Geltungsbereich

Diese Richtlinie gilt für alle Beschäftigten, freien Mitarbeitenden, Dienstleister und sonstigen Personen, die im Auftrag der Organisation KI-Systeme nutzen.

Sie gilt insbesondere für:

- Chatbots und Assistenten, z. B. ChatGPT, Claude, Copilot oder vergleichbare Systeme
- API-basierte KI-Dienste
- KI-Funktionen in Fachanwendungen
- RAG-Systeme und interne Wissensassistenten
- Bild-, Audio-, Video- und Codegeneratoren
- agentische Funktionen wie Computer Use, Cowork, Browsersteuerung, Datei-, E-Mail-, Kalender-, Slack- oder Teams-Zugriffe

## 2. Grundsatz

KI darf nur so genutzt werden, dass Datenschutz, Informationssicherheit, Vertraulichkeit, Urheberrechte, Berufsgeheimnisse, Betriebsgeheimnisse und interne Compliance-Vorgaben eingehalten werden.

AI Act und DSGVO müssen gleichzeitig beachtet werden. Die Einhaltung einer KI-Verordnungspflicht ersetzt keine DSGVO-Prüfung.

Für jeden KI-Use-Case ist zusätzlich zur DSGVO-Prüfung die KI-VO-Einstufung zu dokumentieren: verbotene KI-Praktik, Hochrisiko-KI, begrenztes Risiko mit Transparenzpflichten oder minimales Risiko. Verbotene Praktiken sind nach [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5) unzulässig; Hochrisiko-Einstufungen sind nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) zu prüfen; Transparenzpflichten für bestimmte KI-Systeme ergeben sich aus [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50).

Bei Hochrisiko-KI sind nach der aktuellen Kommissions-FAQ insbesondere `instructions of use`, laufendes Monitoring, menschliche Aufsicht, relevante und hinreichend repräsentative Eingabedaten sowie gegebenenfalls eine Grundrechte-Folgenabschätzung vor Erstnutzung zu organisieren; für entscheidungsrelevante Outputs ist außerdem ein Prozess für das Recht auf Erklärung vorzusehen ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

## 3. Zugelassene Tools

KI-Tools dürfen nur genutzt werden, wenn sie auf der Tool-Whitelist stehen.

| Tool | Erlaubter Plan | Erlaubte Zwecke | Personenbezogene Daten erlaubt? | Auflagen |
|---|---|---|---:|---|
| OpenAI / ChatGPT | Business / Enterprise / API |  | Ja / Nein / eingeschränkt | DPA, Training aus, Retention geregelt |
| Claude / Anthropic | Enterprise / Team / API |  | Ja / Nein / eingeschränkt | DPA, Retention geregelt |
| Internes RAG |  |  | Ja / Nein / eingeschränkt | Berechtigungen, Quellen, Logging |
| Sonstige |  |  |  |  |

Private Accounts dürfen nicht für Unternehmensdaten verwendet werden.

Neu zu berücksichtigen ist außerdem, dass Anthropic laut einer am 12.08.2026 aktualisierten Help-Center-Seite für einzelne Use Cases, Integritätsprüfungen oder andere Safety-/Compliance-Maßnahmen eine Identitäts- oder Business-Verifikation verlangen kann. Die konkrete Reichweite betroffener Fähigkeiten nennt Anthropic dort nicht. Wenn solche Prompts im Unternehmen sichtbar werden, darf die Verifikation nur über vorab benannte und freigegebene Personen erfolgen; Ausweisbild, Live-Selfie und gegebenenfalls Registrierungsdaten der Organisation sind als eigener Datenfluss zu dokumentieren. Laut Anthropic ist Anthropic für diese Verifikationsdaten verantwortlich; ID- und Selfie-Bilder werden bei Persona gehalten und laut Anthropic weder auf Anthropics Systemen kopiert noch für Modelltraining genutzt ([Identity verification on Claude](https://support.claude.com/en/articles/14328960-identity-verification-on-claude)).

Zusätzliche Funktionen wie Chat-Suche, Memory, Projektwissen, Konnektoren oder lokale Datei-/Browserzugriffe gelten als gesondert freigabepflichtige Features.

Öffentlich zugängliche Webquellen oder bereits gescrapte Datensätze für Training, Fine-Tuning oder externe Wissensbestände gelten ebenfalls als gesondert freigabepflichtig. Der Umstand, dass Daten öffentlich erreichbar sind, ersetzt weder Rechtsgrundlage noch Transparenz- und Art.-9-Prüfung ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Für Claude Cowork ist zusätzlich zu beachten, dass Anthropic seit dem 07.07.2026 Remote-Sessions auf Web und Mobile dokumentiert: Die Arbeit läuft serverseitig auf Anthropic-Servern, Sitzungen und Dateien liegen im Claude-Account und lokale Dateien oder Browserfunktionen werden nur über die geöffnete Claude-Desktop-App und freigegebene Ordner erreicht ([Anthropic Release notes, 07.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely)).

Für Anthropic Managed Agents ist zusätzlich zu beachten, dass Anthropic seit dem 10.07.2026 geplante `scheduled deployments` dokumentiert, die Sessions autonom per Cron starten können. Dabei können Dateien, GitHub-Zugänge, Memory Stores und Vaults eingebunden werden; für `environment_variable`-Vault-Credentials wird der Secret-Wert laut Anthropic dem Agenten nicht offengelegt, sondern erst beim ausgehenden Request eingesetzt. Solche Funktionen gelten als gesondert freigabepflichtig ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview)).

Neu zu berücksichtigen ist außerdem, dass Anthropic Managed Agents laut aktueller Produktdokumentation zustandsbehaftet sind: Gesprächsverlauf, Sandbox-Zustand und Outputs werden serverseitig gespeichert; deshalb sind Managed Agents derzeit nicht für Zero Data Retention oder eine HIPAA-BAA-Abdeckung geeignet. Anthropic verweist zugleich darauf, dass Sessions und hochgeladene Dateien separat per API gelöscht werden können. Solche Funktionen dürfen deshalb nur freigegeben werden, wenn der serverseitige State mit dem Daten- und Löschkonzept der Organisation vereinbar ist ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)).

Neu zu berücksichtigen ist außerdem, dass Anthropic seit dem 05.08.2026 `Inference hooks` als Beta für Claude Enterprise dokumentiert. Dabei werden gesteuerte Prompts vor der Inferenz an einen organisationsseitigen AI-Security-Server übermittelt und erst nach dessen Allow-/Deny-Verdikt verarbeitet; laut technischer Dokumentation sind Shadow-Mode, Rollout-Prozentsätze, Ausschlüsse nach Rollen und konfigurierbares Failure Handling vorgesehen. Die Funktion gilt organisationsweit für `claude.ai`, Cowork und Claude Code, ist aber nicht für Amazon Bedrock oder Google Cloud verfügbar ([Claude Platform release notes, 05.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)).

Für Anthropic Enterprise ist zusätzlich zu beachten, dass laut Release Notes seit dem 01.07.2026 organisations- und rollenbezogene Modellfreigaben mit Effort-Caps als Beta dokumentiert sind. Diese Funktion sollte genutzt werden, um nur freigegebene Modelle technisch bereitzustellen; bei `covered models` oder anderen Modellen mit abweichender Retention reicht ein bloßes Richtlinienverbot nicht aus ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization)).

Zusätzlich ist zu beachten, dass Anthropic laut aktueller Herstellerdokumentation `individual usage analytics` für Team- und Enterprise-Organisationen ab dem 11.07.2026 standardmäßig aktiviert. Nutzerbezogene Auswertungen nach Produkt, Modell und Skill dürfen nur mit dokumentiertem Zweck, klaren Sichtrechten und interner Transparenz genutzt werden; falls das nicht gewollt ist, muss die Option organisatorisch geprüft und gegebenenfalls deaktiviert werden ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans)).

Neu zu berücksichtigen ist außerdem, dass Anthropic `custom connectors` über remote MCP inzwischen auf Claude, Cowork und Claude Desktop anbietet. Laut Help Center verbindet sich Claude dabei aus der Anthropic-Cloud mit dem MCP-Server und nicht vom lokalen Gerät aus. Solche Connectoren gelten deshalb als gesondert freigabepflichtig; dokumentiert werden sollten Ziel-URL, Authentisierung, Datenfluss und Drittlandbezug ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)).

Für Claude Cowork ist außerdem zu beachten, dass Anthropic die Nachweis- und Monitoringlage inzwischen enger differenziert. Nach dem am 12.08.2026 aktualisierten Help-Center-Stand deckt die Compliance API für Enterprise nun Cowork über Claude, Claude Desktop und Claude Mobile sowie Claude Code über CLI und Claude Desktop betaweise ab. Für lokale Cowork-Sessions beschreibt Anthropic zugleich, dass die Gesprächsinhalte zwar in der Beta abrufbar sein können, lokale Sessions aber weiterhin lokal gespeichert bleiben, nicht den üblichen Anthropic-Retention-Regeln unterliegen und für sie derzeit keine Lösch-Endpunkte dokumentiert sind. Für laufende Cowork-Aktivität wie Tool-Calls, Dateizugriffe und Approval-Entscheidungen verweist Anthropic daneben weiterhin auf OpenTelemetry und stellt klar, dass dies die Compliance API nicht ersetzt. Die Organisation sollte deshalb ausdrücklich zwischen abrufbaren Transkripten, sonstigen lokal verbleibenden Daten und separater Aktivitätstelemetrie unterscheiden; die genaue Grenzziehung ist in den Herstellerunterlagen nicht vollständig ausbuchstabiert und muss intern sauber dokumentiert werden ([Access the Compliance API](https://support.claude.com/en/articles/13015708-access-the-compliance-api), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Claude Code on Console to Enterprise migration](https://support.claude.com/en/articles/14128775-claude-code-on-console-to-enterprise-migration), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview)).

Mit der am 07.08.2026 aktualisierten Team-/Enterprise-Dokumentation präzisiert Anthropic außerdem die Admin-Steuerung für Claude Cowork. Auf Team-Plänen sind Sessions in der Cloud standardmäßig aktiviert, auf Enterprise-Plänen standardmäßig deaktiviert und erst nach zusätzlicher Rollen- oder Gruppenfreigabe nutzbar. Für schreibfähige Connector-Tools ist `Allow for all tasks` standardmäßig ausgeschaltet; viele Custom Connectoren annotieren ihre Tools nicht als read-only, sodass sie pro Aufgabe freigegeben werden müssen. Zusätzlich gibt es derzeit keine separate Admin-Abschaltung für Cowork-Projekte; bei Cloud-Sessions werden Projektdaten im Claude-Account gespeichert ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).

Ebenso wichtig ist, dass Anthropic Network-Egress-Regeln nicht auf `web fetch`, `web search` oder MCPs einschließlich Claude in Chrome erstreckt. Diese Wege müssen deshalb gesondert deaktiviert, beschränkt oder überwacht werden; normale Code-Ausführungs-Allowlists reichen dafür nicht aus ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).

Für den Claude-Microsoft-365-Connector ist zusätzlich zu beachten, dass `write tools` laut aktueller Herstellerdokumentation erneute Tenant-Einwilligungen zu erweiterten Microsoft-Graph-Berechtigungen voraussetzen können. Außerdem tragen derzeit nur gesendete E-Mails einen `agent-initiated`-Header; Datei- und Kalender-Schreibvorgänge werden nach derzeitigem Dokumentationsstand nicht entsprechend gekennzeichnet ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector)).

Für ChatGPT/OpenAI ist zusätzlich zu beachten, dass Plugins, Apps und Skills inzwischen getrennt administriert werden. Seit dem 09.07.2026 verweist OpenAI auf das Plugin Directory als zentrale Oberfläche; in Enterprise und Edu sind Plugins und die zugrunde liegenden Apps standardmäßig deaktiviert und rollenbezogen getrennt freizugeben. OpenAI plant außerdem, Skills in Enterprise-Workspaces ohne Opt-out seit dem 23.07.2026 standardmäßig zu aktivieren. Skill-Uploads oder Custom Apps dürfen deshalb nur aus vertrauenswürdigen Quellen und mit klaren Rollenrechten, Installationsrechten und Freigabeprozessen genutzt werden ([Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Neu zu berücksichtigen ist außerdem, dass Anthropic seit dem 06.08.2026 für Enterprise-Pläne `Skill and plugin security scanning` als Beta dokumentiert. Wenn die Funktion aktiviert wird, prüft Claude neue Uploads oder Änderungen an Dritt-Skills und -Plugins vor der Ausführung auf schädliche Inhalte; sie ist standardmäßig deaktiviert, bestehende Skills/Plugins bleiben unberührt, und der Geltungsbereich kann über Custom Roles weiter eingegrenzt werden. Solche Skills oder Plugins sollten deshalb nur mit dokumentierter Owner-Freigabe, definierter Behandlung von Warnhinweisen und klaren Regeln für Neu-Uploads oder Änderungen zugelassen werden ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)).

Neu zu berücksichtigen ist außerdem, dass Anthropic laut Claude-Platform-Release-Notes vom 07.08.2026 bei Managed Agents `inference_geo` auf Agenten- oder Session-Ebene sowie das automatische Laden von Skills aus gemounteten GitHub-Repositories dokumentiert. Laut Data-Residency- und Self-hosted-Sandbox-Dokumentation steuert `inference_geo` den Ort der Modellinferenz; das Workspace-Geo steuert Speicherung und weitere Endpoint-Verarbeitung. `Self-hosted sandboxes` halten Tool-Ausführung, Dateisystem und Network Egress zwar im eigenen Umfeld, Tool-Ein- und -Ausgaben fließen laut Anthropic aber weiter an die Control Plane. Solche Setups gelten deshalb ebenfalls als gesondert freigabepflichtig; dokumentiert werden sollten Geo-Einstellungen, Sandbox-Modell, Datenflussgrenzen sowie Herkunft und Freigabe von GitHub-Repositories mit `.claude/skills` ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github)).

Für OpenAI-Apps mit `sync` ist zusätzlich zu beachten, dass OpenAI Inhalte je nach App vorab indexieren kann. Laut aktueller Herstellerdokumentation werden Chat- und Deep-Research-Daten mit Apps transient verarbeitet, `sync`-Daten dagegen indexiert; App-Unterhaltungen erscheinen in der Compliance API und App-Calls in den Compliance Logs. Für Sync-Apps, die nicht in der eigenen Residency-Region unterstützt werden, liegt der Suchindex laut OpenAI in US-Azure-Rechenzentren. Solche Apps dürfen deshalb nur mit dokumentierter Residency-Prüfung, klaren App-Berechtigungen und passendem Logging-Konzept freigegeben werden ([Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)).

Neu zu berücksichtigen ist außerdem, dass OpenAI laut Enterprise-&-Edu-Release-Notes seit dem 10.08.2026 keine neuen individuell autorisierten Sync-Verbindungen mehr zulässt. Am 14.08.2026 werden bestehende solche Verbindungen deaktiviert, und die Löschung der zugehörigen Sync-Daten beginnt; admin-gemanagte Syncs bleiben unberührt. Wenn synchronisiertes Wissen weiter benötigt wird, darf es deshalb nur über ausdrücklich freigegebene admin-gemanagte Syncs oder andernfalls über nicht-synchronisierte Plugins/Apps bereitgestellt werden. Betroffene Altverbindungen und Workflows sind bis zum 14.08.2026 zu identifizieren und zu bereinigen ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)).

Neu zu berücksichtigen ist außerdem, dass OpenAI ChatGPT Work als längerlaufenden Agenten für Web, Mobile und Desktop dokumentiert. Auf dem Desktop kann Work freigegebene lokale Ordner öffnen; lokale Dateien und Outputs bleiben dort, bis sie ausdrücklich bewegt oder geteilt werden. Work kann außerdem über Scheduled Tasks einmalig, wiederkehrend oder monitoringbasiert laufen. Solche Funktionen gelten als gesondert freigabepflichtig; dokumentiert werden sollten freigegebene lokale Ordner, zulässige App-/Dateizugriffe, Monitoring-Zwecke, Benachrichtigungen und Review-Pflichten. Zu beachten ist auch, dass Tasks in Projekten nicht auf Projektdateien zugreifen, Task-Konversationen laut OpenAI aber in der Compliance API erscheinen ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt)).

Neu zu berücksichtigen ist außerdem, dass OpenAI die Governance-, Logging- und Löschlogik für Work, Codex, Agent und Library seit Ende Juli 2026 enger ausbuchstabiert. Nach dem aktuellen Work-Admin-FAQ decken Compliance API und Compliance Logs bei Work/Codex zwar Unterhaltungen und Responses ab, nicht aber Dateien, Aktionen oder Tool-Calls; die Compliance Logs Platform hält diese Daten laut OpenAI 30 Tage vor, sodass für längere Aufbewahrung ein laufender Export nötig ist. Für ChatGPT-Agent stellt OpenAI zusätzlich klar, dass individuelle Agent-Aktionen wie Virtual Computer Usage oder App-Requests nicht in der Compliance API erscheinen und `apps with sync` nicht direkt als Agent-Datenquelle dienen. Gespeicherte ChatGPT-Library-Dateien werden getrennt von Chats verwaltet; das Löschen eines Chats löscht diese Dateien nicht automatisch, und Compliance-Admins können sie über eigene Endpunkte exportieren oder löschen. Solche Funktionen gelten deshalb ebenfalls als gesondert freigabepflichtig ([ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [File storage and Library in ChatGPT](https://help.openai.com/en/articles/20001052-file-storage-and-library-in-chatgpt), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt)).

Neu zu berücksichtigen ist außerdem, dass OpenAI seit dem 06.08.2026 für Enterprise-, Edu- und Healthcare-Workspaces eine Admin-Steuerung für In-App-Updates der ChatGPT-Desktop-App dokumentiert. Wird sie genutzt, um Updates nicht automatisch auszurollen, muss die Organisation neue Versionen und Sicherheitsfixes selbst zeitnah verteilen; OpenAI bietet dafür laut Release Notes weder Version-Pinning noch einen separaten Stable Channel oder erweiterten Support für ältere Versionen. Für lokal zugreifende Work-/Codex-/Agentik-Funktionen sollte deshalb ein eigener Freigabe- und Patchprozess dokumentiert sein ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Neu zu berücksichtigen ist außerdem, dass OpenAI `ChatGPT Voice` nun ausdrücklich als Live-Schnittstelle für Work und Codex in der Desktop-App dokumentiert. Voice nutzt dabei dieselben Tools und Berechtigungen wie die gewählte Experience; laut Voice-Dokumentation kann es Aufgaben starten, Fortschritte abfragen und mehrere Agenten über eine Unterhaltung koordinieren. Zugleich dokumentiert OpenAI für berechtigte Enterprise- und Edu-Workspaces mit EKM, dass Work für Mitglieder der Default-Rolle standardmäßig aktiviert ist, Cloud-Work-Chats zwischen Web, Mobile und Desktop synchronisieren und lokale Chats auf dem jeweiligen Rechner verbleiben. Für Freigaben ist deshalb getrennt festzulegen, ob Voice, Cloud Work und Local Work erlaubt sind und welche lokalen Dateien oder Desktop-Apps dabei erreichbar sein dürfen ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)).

Laut Enterprise-/Edu-Release-Notes vom 07.08.2026 unterstützt `ChatGPT Voice` jetzt außerdem Datei-Uploads und Projects. Voice kann damit in Projekten auf aktuelle Projekt-Chats, Quellen und Projektanweisungen zugreifen; zugleich wird `Live` bei Enterprise-, Edu- und Healthcare-Workspaces zur Standard-Voice-Erfahrung, sobald Workspace-Owner Voice aktivieren. Für Freigaben sollte deshalb ausdrücklich dokumentiert werden, ob Voice nur für allgemeine Koordination oder auch für Datei- und Project-Kontext genutzt werden darf ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Neu zu berücksichtigen ist außerdem, dass OpenAI und Anthropic ihre Herkunfts- und Markierungsdokumentation für KI-generierte Inhalte deutlich ausgebaut haben. Anthropic dokumentiert nun für unterstützte Claude-Modelle maschinenlesbare Markierungen mit eingebetteten Wasserzeichen für Text und signierten Provenance-Metadaten für unterstützte Dateien; die Verfügbarkeit bei älteren Modellen ist laut Anthropic noch im Ausbau. OpenAI verweist in seiner am 11.08.2026 aktualisierten EU-AI-Act-Guidance auf Trainingsdatensummaries sowie auf C2PA/SynthID, `openai.com/verify` und eine Content Provenance API; laut separater Provenance-Doku sind diese Signale derzeit nur für unterstützte Bilder und Audiodateien konkret beschrieben, nicht allgemein für Text. Wenn Outputs extern veröffentlicht, an Kunden versandt oder in RAG-, DMS- oder Kommunikationsprozesse übernommen werden, ist deshalb pro Anbieter, Modalität und Exportpfad festzulegen, ob Herkunftssignale erhalten bleiben, wer sie prüfen darf und dass fehlende oder nicht nachweisbare Signale kein Ersatz für eigenständige Kennzeichnungs- oder Review-Pflichten sind ([How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content)).

Praxis-Hinweis: Zentrale Business-Accounts für Firmen-Tools, AVV/DPA, Zero Data Retention und klare Nutzungsregeln sind Kernanforderungen. Bei privaten MCP-Servern ist eine enge Tunnel-/Allowlist-Architektur statt öffentlicher Freigaben oder unnötig breiter Netzverbindungen zu bevorzugen. Für Anthropic Managed Agents ist neu ausdrücklich zu bewerten, dass sie serverseitig zustandsbehaftet sind und derzeit nicht unter ZDR oder HIPAA-BAA laufen; werden `Inference hooks` genutzt, sollten AI-Security-Server, Shadow-Mode bzw. Durchsetzung und Failure Handling dokumentiert sein ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)). Zusätzlich sollte festgehalten werden, ob `inference_geo`, Workspace-Geo, Cloud-Sandbox oder `self-hosted sandboxes` genutzt werden; `self-hosted` hält Tool-Ausführung, Dateisystem und Network Egress zwar im eigenen Umfeld, Tool-Ein- und -Ausgaben fließen laut Anthropic aber weiter an die Control Plane. Werden GitHub-Repositories gemountet, ist außerdem zu dokumentieren, ob daraus Skills aus `.claude/skills` automatisch geladen werden dürfen und welche Repo- und Freigabekontrollen dafür gelten ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github)). Für OpenAI Work ist zusätzlich festzuhalten, ob `Voice`, `Work Cloud`, `Work Local` und die Default-Aktivierung für Mitglieder der Default-Rolle in berechtigten Enterprise-/Edu-Workspaces mit EKM freigegeben sind; Cloud-Work-Chats synchronisieren zwischen Web, Mobile und Desktop, lokale Chats verbleiben auf dem jeweiligen Rechner ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)).

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [File storage and Library in ChatGPT](https://help.openai.com/en/articles/20001052-file-storage-and-library-in-chatgpt), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt), [Anthropic Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

## 4. Verbotene Eingaben

In nicht freigegebene KI-Systeme dürfen nicht eingegeben werden:

- Namen, E-Mail-Adressen, Telefonnummern, Kundennummern oder sonstige Identifikatoren
- Kundendaten
- Mitarbeiterdaten
- Bewerberdaten
- Gesundheitsdaten
- biometrische Daten
- Daten von Kindern/Jugendlichen
- Mandanten-, Patienten-, Steuer-, Rechtsberatungs- oder Berufsgeheimnisse
- Passwörter, API-Keys, Tokens, Zugangsdaten
- vertrauliche Verträge, Strategien, Finanzdaten oder Betriebsgeheimnisse
- Daten, die einer besonderen Geheimhaltungspflicht unterliegen

Ausnahme: Die Verarbeitung wurde für den konkreten Use Case freigegeben, ein AVV/DPA liegt vor, Datenminimierung ist umgesetzt und die DSFA-/Rechtsprüfung ist abgeschlossen, sofern erforderlich.

## 5. Erlaubte Standardnutzungen

Ohne personenbezogene oder vertrauliche Daten sind in der Regel erlaubt:

- Formulierung allgemeiner Texte
- Ideenfindung
- Strukturierung nicht vertraulicher Inhalte
- Erstellen allgemeiner Checklisten
- Übersetzen oder Vereinfachen anonymisierter Texte
- Codebeispiele ohne Geheimnisse, Zugangsdaten oder produktive Daten
- Zusammenfassung öffentlicher Informationen mit Quellenprüfung

## 6. Eingaberegeln

Vor jeder Eingabe prüfen:

1. Ist die Information personenbezogen?
2. Ist sie vertraulich?
3. Ist sie für den Zweck wirklich erforderlich?
4. Kann sie anonymisiert oder pseudonymisiert werden?
5. Ist das Tool für diese Datenart freigegeben?
6. Ist Training/Model Improvement deaktiviert oder ausgeschlossen?
7. Gilt eine passende Retention?

Beispiele:

- Statt "Max Mueller, Kunde 12345, mahnt Rechnung an" schreiben: "Kunde A mahnt eine Rechnung an".
- Statt vollständiger Vertragsdatei nur die relevante anonymisierte Klausel eingeben.
- Statt Mitarbeiterbewertung keine KI-Einschätzung über Leistung, Verhalten oder Zukunftsentscheidungen erzeugen lassen.

Als "anonymisiert" deklarierte Daten dürfen nicht allein deshalb freigegeben werden. Nach den EDPB-Entwurfsleitlinien ist Anonymität perspektivbezogen zu prüfen; bis zu einer dokumentierten Prüfung sollten nur pseudonymisierte oder geschwärzte Daten weiter als personenbezogen behandelt werden ([Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

## 7. Output-Regeln

KI-Ausgaben müssen geprüft werden, bevor sie verwendet werden.

Pflichten:

- fachliche Prüfung
- Quellenprüfung bei Tatsachenbehauptungen
- Prüfung auf personenbezogene Falschinformationen
- Prüfung auf Diskriminierung
- Prüfung auf Halluzinationen
- keine ungeprüfte Übernahme in Kunden-, HR-, Rechts- oder Finanzprozesse

## 8. Keine automatisierte Letztentscheidung

KI darf nicht allein über Personen entscheiden. Verboten ohne gesonderte Rechts- und Datenschutzfreigabe sind insbesondere:

- Bewerberauswahl
- Mitarbeiterbewertung
- Kündigungsempfehlungen
- Bonitätsentscheidungen
- Versicherungsentscheidungen
- Gesundheits- oder Risikobewertungen
- Sperrung, Sanktionierung oder Ablehnung von Leistungen

Quelle: [Art. 22 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en).

## 9. Agentische KI und Cowork/Computer Use

Agentische Funktionen haben ein höheres Risiko als reine Chat-Nutzung, weil sie auf lokale Daten, Browser, Dienste, Dateien oder Kommunikationskanäle zugreifen können.

Nur mit separater Freigabe erlaubt:

- Computer Use
- Cowork
- Browsersteuerung
- Zugriff auf lokale Dateien
- Zugriff auf Slack, Teams, E-Mail, Kalender, CRM, ERP, Ticketsysteme
- Connector-Schreibzugriffe, z. B. E-Mail-Versand, Kalenderänderungen sowie Schreiben in OneDrive oder SharePoint
- automatische Aktionen wie Senden, Speichern, Löschen, Kaufen, Buchen oder Verändern von Daten
- Computer Use oder vergleichbare UI-Steuerung, bei der Screenshots, Browserinhalte oder Desktop-Oberflächen verarbeitet werden

Mindestanforderungen:

- Least-Privilege-Zugriff
- Testumgebung vor Produktivzugriff
- keine autonomen Aktionen ohne Freigabe
- Protokollierung
- Prompt-Injection-Schutz
- für Konnektoren und MCP-Server Retention/Residency jedes Drittservers separat prüfen
- Anthropic-`custom connectors`/remote MCP nur mit dokumentiertem cloudseitigem Verbindungsweg, Zielsystem und Owner-Freigabe einsetzen
- OpenAI-Plugins nur freigeben, wenn Plugin, zugrunde liegende App und Rollenrechte getrennt geprüft wurden; Workspace-Default nicht mit Einzel-Freigabe verwechseln
- OpenAI-Skills oder Skill-Uploads nur aus vertrauenswürdigen Quellen zulassen; für Enterprise-Workspaces ist eine mögliche Default-Aktivierung ausdrücklich zu prüfen
- Anthropic-Skills oder -Plugins nur zulassen, wenn dokumentiert ist, ob das optionale Enterprise-Scanning aktiviert wurde, dass es standardmäßig aus ist, nur neue Uploads oder Änderungen prüft und wie Warnhinweise für riskante Inhalte behandelt werden
- bei Claude Cowork Remote-Sessions, gespeicherte Sitzungen/Dateien, geplante Tasks und erreichbare lokale Ordner separat freigeben und dokumentieren
- bei Claude Cowork oder Remote Control soweit verfügbar `network-access policy`, restriktives Approval-Verhalten und Trusted Devices erzwingen
- bei Claude Cowork und Claude Code getrennt bewerten, welche Cloud-/Remote-Session-Inhalte über die Compliance API erreichbar sind, dass lokale Cowork-Sitzungsinhalte und lokale Claude-Code-Transkripte für Enterprise betaweise abrufbar sein können, welche lokalen Daten dennoch außerhalb zentraler Administration verbleiben und wie laufende Aktivität wie Tool-Calls oder Dateizugriffe zusätzlich über OpenTelemetry überwacht oder kompensiert wird
- bei Claude Cowork berücksichtigen, dass `web fetch`, `web search` und MCPs nicht von den normalen Network-Egress-Regeln erfasst werden; dafür separate Schalter oder Kontrollen setzen
- bei Anthropic Managed Agents getrennt dokumentieren, ob `inference_geo`, Workspace-Geo, Cloud-Sandbox oder `self-hosted sandbox` genutzt werden; `self-hosted` hält Tool-Ausführung, Dateisystem und Network Egress zwar im eigenen Umfeld, Tool-Ein- und -Ausgaben fließen laut Anthropic aber weiter an die Control Plane
- gemountete GitHub-Repositories mit automatischer `.claude/skills`-Erkennung nur aus vertrauenswürdigen Quellen zulassen; Repo-Zugriffe, Branch-/PR-Kontrollen und Skill-Freigaben gesondert dokumentieren
- Microsoft-365-Connector-`write tools` nur nach Admin-Freigabe und enger Zweckbegrenzung aktivieren
- Microsoft-365-Connector-`write tools` nur nach erneuter Tenant-Einwilligung zu erweiterten Graph-Berechtigungen aktivieren; berücksichtigen, dass derzeit nur E-Mails einen `agent-initiated`-Header tragen
- OpenAI-`apps with sync` nur nach Prüfung von Indexierung, Residency-Region, Compliance-API/Compliance-Logs und erforderlichen App-Berechtigungen einsetzen
- ChatGPT Work, `Work Cloud`, `Work Local` und Scheduled Tasks nur nach separater Freigabe einsetzen; lokale Ordnerzugriffe, zulässige Apps/Dateien, Monitoring-Läufe, Benachrichtigungen, die Default-Aktivierung für Mitglieder der Default-Rolle in berechtigten Enterprise-/Edu-Workspaces mit EKM sowie der fehlende Projektdateizugriff von Tasks sind gesondert zu dokumentieren
- `ChatGPT Voice` in Work oder Codex nur nach separater Freigabe einsetzen, weil Voice dieselben Tools und Berechtigungen wie die gewählte Experience nutzt
- bei `ChatGPT Voice` zusätzlich festlegen, ob Datei-Uploads und Project-Kontext erlaubt sind; seit dem 07.08.2026 kann Voice in Projects auf aktuelle Chats, Quellen und Projektanweisungen zugreifen
- bei ChatGPT Work, Codex oder Agent getrennt dokumentieren, dass Compliance API/Compliance Logs zwar Unterhaltungen und Responses, nicht aber Dateien, Aktionen oder Tool-Calls abdecken; für Aufbewahrung über 30 Tage ist ein laufender Export vorzusehen
- ChatGPT-Library-Dateien und Chat-Löschung getrennt steuern; das Löschen eines Chats entfernt gespeicherte Library-Dateien nicht automatisch
- wenn In-App-Updates der ChatGPT-Desktop-App organisatorisch deaktiviert werden, Releases und Sicherheitsfixes über einen eigenen Freigabe- und Patchprozess zeitnah verteilen
- Anthropic-Managed-Agents mit `scheduled deployments`, Vaults oder GitHub-/Dateianbindung nur nach separater Freigabe, enger Zeitplan- und Secret-Begrenzung sowie dokumentierter Run-Historie einsetzen
- Anthropic-Managed-Agents nur freigeben, wenn der serverseitige State ausdrücklich bewertet ist; nach aktueller Anthropic-Dokumentation sind Managed Agents derzeit nicht ZDR- oder HIPAA-BAA-fähig
- Anthropic-`Inference hooks` nur als Kontrollmaßnahme einplanen, wenn Scope, AI-Security-Server, Shadow-Mode bzw. Durchsetzung, Failure Handling und der Ausschluss von Bedrock/Google Cloud dokumentiert sind
- bei Anthropic Enterprise Modell-Allowlist und Effort-Caps so setzen, dass nicht freigegebene oder retention-pflichtige Modelle technisch begrenzt sind
- nutzerbezogene KI-Analytics nur mit dokumentiertem Zweck, enger Sichtberechtigung und interner Transparenz aktiv lassen
- für private MCP-Server nach Möglichkeit outbound-only-Tunnel oder gleichwertig enge Anbindung; keine unnötigen öffentlichen Endpunkte oder breiten VPN-/Peering-Freigaben
- Chat-Suche/Memory nur nach dokumentierter Freigabe; Retention, Export und Admin-Kontrollen prüfen
- klare Abbruch- und Kontrollmechanismen
- DSFA-Prüfung bei personenbezogenen Daten

Praxis-Hinweis: Cowork-, Computer-Use- und Browserzugriffe auf lokale Daten, Screenshots, Webseiten und Dienste wie Slack können zu ungewollter Datenübertragung führen und müssen separat freigegeben werden. OpenAI beschreibt Computer Use als UI-operierende Modellfunktion; Anthropic kennzeichnet Computer Use als Beta-Funktion mit besonderen Sicherheitsrisiken, insbesondere bei Internetzugriff. Neu dokumentiert ist zudem, dass Cowork auf Web und Mobile als Remote-Session auf Anthropic-Servern läuft und Aufgaben ohne online Gerät weiterlaufen können. Für den Claude-Microsoft-365-Connector gilt zusätzlich: Wenn `write tools` aktiviert sind, kann Claude E-Mails senden und organisieren, Kalenderereignisse erstellen, aktualisieren oder löschen sowie Dateien in OneDrive und SharePoint erstellen oder aktualisieren; Teams bleibt read-only, und gesendete E-Mails tragen laut Anthropic einen agent-initiated-Header ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide)). Für Anthropic Managed Agents kommt hinzu, dass `scheduled deployments` Sessions autonom starten können und Vault-Credentials in ausgehende Requests eingebracht werden können; neu ausdrücklich zu bewerten ist außerdem, dass Managed Agents serverseitig zustandsbehaftet sind und derzeit nicht für ZDR oder HIPAA-BAA geeignet sind ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)). Werden in Anthropic Enterprise Skills oder Plugins freigegeben, sollte zusätzlich klar dokumentiert werden, ob das optionale Scanning für neue Uploads oder Änderungen aktiv ist und wie mit Warnhinweisen umgegangen wird ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)). Werden Anthropic-`Inference hooks` genutzt, sollten AI-Security-Server, Shadow-Mode bzw. Durchsetzung und Failure Handling dokumentiert sein ([Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)). Für OpenAI Work ist zusätzlich zu berücksichtigen, dass `Voice` dieselben Tools und Berechtigungen wie Work oder Codex nutzt und dass berechtigte Enterprise-/Edu-Workspaces mit EKM Work für Mitglieder der Default-Rolle standardmäßig aktivieren können; seit dem 07.08.2026 kann Voice außerdem Dateien hochladen und in Projects auf aktuelle Chats, Quellen und Projektanweisungen zugreifen ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)). Für private MCP-Server beschreibt OpenAI seit Juni 2026 mit dem Secure MCP Tunnel eine kundenseitig betriebene outbound-only-Anbindung, bei der die private Serveradresse intern bleibt; das ersetzt aber nicht die Prüfung von Drittservern, Rollen, Zielbegrenzungen und Logging.

Wenn Claude Code, Cowork oder Cloud-Zugänge mit ZDR betrieben werden, ist zusätzlich modellbezogen zu prüfen, ob Anthropic für das gewünschte Modell eine Retention-Pflicht vorgibt. Anthropic dokumentiert für `covered models` bzw. Mythos-class-Modelle eine 30-Tage-Retention; Claude Fable 5 ist laut Migration Guide nicht unter Zero Data Retention verfügbar. Für solche Modelle kann ein getrenntes Workspace-, Subscription- oder Sandbox-Setup mit aktivierter Retention erforderlich sein.

Quellen: [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex), [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

## 10. RAG und interne Wissenssysteme

RAG-Systeme dürfen nur freigegebene Quellen verwenden.

Pflichten:

- Berechtigungen aus Quellsystemen übernehmen
- keine Indexierung ohne Rechtsgrundlage
- Löschung aus Quelle muss auch im Index berücksichtigt werden
- Quellen in Antworten anzeigen, soweit möglich
- Prompt-Injection prüfen
- vertrauliche Dokumente getrennt indexieren
- Zugriffe protokollieren

Quelle: [DSK RAG Orientierungshilfe](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf).

## 11. Beschaffung und Freigabe neuer KI-Tools

Vor Freigabe eines KI-Tools müssen geprüft werden:

- Zweck
- Datenarten
- Rechtsgrundlage
- Anbieterrolle
- AVV/DPA
- Subprozessoren
- Drittlandtransfer
- Retention
- Training/Model Improvement
- TOMs
- Betroffenenrechte
- DSFA-Pflicht
- Informationssicherheit
- AI-Act-Relevanz
- KI-VO-Risikoklasse: verboten / Hochrisiko / begrenztes Risiko / minimales Risiko
- Nachweislage für ChatGPT Work/Codex/Agent: welche Unterhaltungen, Dateien, Aktionen und Tool-Calls tatsächlich protokolliert werden, wie lange diese Daten vorliegen und ob ein Export nötig ist
- getrennte Lösch- und Retention-Logik für ChatGPT-Library-Dateien statt bloßer Chat-Löschung
- Anbindungsarchitektur für private MCP-Server oder REST-Ziele: öffentliche Freigabe, VPN/Peering oder enge Tunnel-Lösung; Begründung und Freigabe dokumentieren
- featurebezogene Retention, z. B. Background Mode, standardmäßiges Extended Prompt Caching ohne ZDR, Hosted Containers, Message Batches, Audit Logs oder Vector Stores
- cloudseitiger Verbindungsweg bei Anthropic-`custom connectors`/remote MCP statt bloßer Annahme eines lokalen Desktop-Datenpfads
- autonome Agentik-Orchestrierung, z. B. Anthropic-`scheduled deployments`, Deployment-Run-Historie/Webhooks sowie Dateien-, GitHub-, Memory- und Vault-Einbindung
- verfügbare Remote-Session-Kontrollen für Claude Cowork wie `network-access policy`, Trusted Devices, Approval-Vorgaben sowie MDM-Sperren für lokale MCP-Server/Desktop Extensions
- fehlende Nachweisquellen für Claude Cowork, insbesondere keine Audit-Logs/Compliance-API/Data-Exports und keine hostseitige EDR-Sicht auf die Remote-VM
- modellbezogene Retention-Ausnahmen, z. B. Anthropic-`covered models` oder Claude Fable 5 mit 30-Tage-Retention statt ZDR, sowie ein ggf. erforderliches separates Workspace-, Subscription- oder Sandbox-Setup
- organisations- oder rollenbezogene Modell-Allowlist und Effort-Caps, soweit der Anbieter dies unterstützt
- nutzerbezogene Usage-Analytics, Reports oder ähnliche Admin-Auswertungen: Zweck, Sichtberechtigungen und interne Transparenz prüfen
- aktueller GPAI-Code-Signaturstatus wesentlicher Modellanbieter als freiwilliger Governance-Hinweis, ohne Ersatz der DSGVO-, Transfer- oder Featureprüfung
- Microsoft-365-Connector-`write tools`: Tenant-Re-Consent zu erweiterten Graph-Scopes und fehlende Kennzeichnung von Datei-/Kalenderwrites
- Nutzung öffentlich zugänglicher Webquellen, gescrapter Datensätze oder Datenbroker-Datensätze: getrennte Prüfung von Rechtsgrundlage, Transparenz, Quellenauswahl, Widerspruchs-/robots.txt-Behandlung, Datenminimierung, Validierung und Art.-9-Ausnahmen
- dokumentierte Anonymisierungsbewertung statt bloßer Annahme, dass entfernte Identifikatoren genügen

Praxis-Hinweis: Bei OpenAI-API-Integrationen ist nicht nur zu prüfen, ob Extended Prompt Caching theoretisch genutzt werden könnte. Laut aktueller OpenAI-Datendokumentation verwenden Organisationen ohne Zero Data Retention bei allen unterstützten Modellen standardmäßig Extended Prompt Caching; bei `gpt-5.5`, `gpt-5.5-pro` und künftigen Modellen ist `prompt_cache_retention=in_memory` nicht zulässig. Diese Default-Logik ist im Freigabe- und Löschkonzept ausdrücklich zu dokumentieren. Seit dem 30./31.07.2026 dokumentiert OpenAI außerdem `Fast mode` ausdrücklich als mit Data Residency, ZDR und BAA kompatibel. Für die interne Freigabe heißt das: `Fast mode` ist nicht schon wegen des Verarbeitungsmodus auszuschließen, die konkrete Prüfung genutzter Endpunkte, Tools und der regionalen Verfügbarkeit bleibt aber erforderlich ([OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq)).

Praxis-Hinweis: Bei Anthropic ist ZDR ebenfalls nicht pauschal auf jedes Modell übertragbar. Für `covered models` verlangt Anthropic laut aktueller Help-Center-Dokumentation 30 Tage Retention; Claude Fable 5 ist laut Migration Guide nicht unter ZDR verfügbar. Freigaben sollten deshalb dokumentieren, welches Modell verwendet wird und ob dafür eine getrennte Retention-Konfiguration nötig ist.

Praxis-Hinweis: Die neuen EDPB-Entwurfsleitlinien vom 07./08.07.2026 behandeln Web Scraping für generative KI und Anonymisierung ausdrücklich noch als Konsultationsfassungen. Inhaltlich sind sie dennoch belastbar genug, um Freigabeprozesse bereits jetzt zu schärfen: Das EDPB empfiehlt für Web-Scraping-Setups u. a. verlässliche Quellen, Zeitstempel und Validierung, Filter zur Datensparsamkeit sowie den Ausschluss von Quellen, die Scraping klar entgegenstehen. Für Anonymisierung nennt das EDPB die Prüfkriterien `No Record Isolation`, `No Linkage` und `No Inference` ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Freigabe erfolgt durch:

| Rolle | Freigabe erforderlich? |
|---|---:|
| Fachbereich | Ja |
| Datenschutz | Ja |
| Informationssicherheit | Ja |
| Rechtsabteilung / externe Beratung | bei hohem Risiko |
| Geschäftsführung / Leitung | bei hohem Risiko |

Quellen: [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

## 12. Datenschutz-Folgenabschätzung

Eine DSFA ist zu prüfen bei:

- Verarbeitung personenbezogener Daten mit neuen KI-Technologien
- Profiling, Scoring oder Bewertung
- Beschäftigtendaten
- Gesundheitsdaten oder Art.-9-Daten
- umfangreicher Verarbeitung
- RAG mit internen personenbezogenen Wissensbeständen
- agentischer KI mit Dienst-/Dateizugriff
- automatisierten Entscheidungen

Vorlage: `Datenschutz-Folgenabschätzung Vorlage KI Nutzung.md`

Eine Grundrechte-Folgenabschätzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) kann für bestimmte Hochrisiko-KI-Systeme zusätzlich relevant sein und ergänzt eine DSFA, soweit deren Pflichten bereits einschlägige Punkte abdecken.

Quellen: [Art. 35 DSGVO](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27).

## 13. Transparenz

Betroffene Personen müssen informiert werden, wenn ihre personenbezogenen Daten mit KI verarbeitet werden und eine Informationspflicht besteht.

Interne Transparenz:

- Mitarbeitende erhalten diese Richtlinie.
- Freigegebene Tools werden zentral dokumentiert.
- Schulungen sind zu dokumentieren.

Externe Transparenz:

- Datenschutzhinweise prüfen und anpassen.
- Bei Kundenprozessen klarstellen, ob KI assistiv genutzt wird, soweit rechtlich erforderlich.
- Bei interaktiven KI-Systemen wie Chatbots dokumentieren, wie Nutzer vor oder spätestens bei der Interaktion darauf hingewiesen werden, dass sie mit KI interagieren.
- Deepfakes sowie KI-generierte oder KI-manipulierte Texte zu Fragen von öffentlichem Interesse vor Veröffentlichung auf Kennzeichnungspflichten, Position des Labels und Verantwortlichkeit prüfen.

Zusatzhinweis zum AI Act: Die KI-VO ist seit 1. August 2024 in Kraft. Nach [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113) gilt sie grundsätzlich ab dem 2. August 2026; Kapitel I und II gelten seit dem 2. Februar 2025, bestimmte GPAI-, Governance- und Sanktionsregeln seit dem 2. August 2025. Für Hochrisiko-KI verweist die Kommission inzwischen auf das im Amtsblatt vom 24.07.2026 veröffentlichte `Digital Omnibus on AI` (Regulation (EU) 2026/1744): Bestimmte Hochrisikobereiche gelten danach ab dem 02.12.2027, in Produkte integrierte Systeme z. B. Robotik oder Industriemaschinen ab dem 02.08.2028 ([AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744)). Nach [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50) müssen u. a. direkte Interaktion mit KI-Systemen, bestimmte KI-generierte oder manipulierte Inhalte, Deepfakes sowie Emotionserkennungs- oder biometrische Kategorisierungssysteme transparent gemacht werden; Ausnahmen und Detailpflichten sind einzelfallbezogen zu prüfen. Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde am 10.06.2026 veröffentlicht. Er ist freiwillig, die gesetzlichen Transparenzpflichten gelten dennoch ab dem 02.08.2026.

Neu zu berücksichtigen ist, dass die EU-Kommission den Code am 09.07.2026 als angemessenes freiwilliges Instrument zur Erleichterung der Umsetzung von Art. 50 Abs. 2, 4 und 5 KI-VO bewertet hat und der AI Board die Angemessenheitsbewertung am Folgetag übernommen hat. Wenn die Organisation den Code als Nachweisbaustein nutzen will, sollte der Signaturstatus dokumentiert und den konkreten Transparenzmaßnahmen zugeordnet werden. Laut Kommission ersetzt die Zeichnung des Codes weder die konkrete Pflichtenumsetzung noch einen abschließenden Compliance-Nachweis ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der aktualisierte FAQ-Stand des AI Office: Für die erste Signatory-Liste vor dem 02.08.2026 müssen Signaturformulare bis zum 27.07.2026, 18:00 CEST eingereicht werden. Eine spätere Unterzeichnung bleibt möglich; wenn die Organisation nicht unterzeichnet, sollte sie ihre alternativen Maßnahmen zur Markierung, Erkennung und Kennzeichnung nach Art. 50 KI-VO besonders belastbar dokumentieren ([Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Neu zu berücksichtigen sind außerdem die Kommissionsleitlinien und FAQ vom 20.07.2026 zu Art. 50 KI-VO: Bei Chatbots, Agenten und Avataren soll der KI-Hinweis grundsätzlich ab der ersten direkten Interaktion klar und unterscheidbar erfolgen, sofern die KI-Nutzung nicht ausnahmsweise ohnehin offensichtlich ist. Für veröffentlichte KI-generierte oder KI-manipulierte Texte zu Fragen von öffentlichem Interesse reicht eine bloß formale Prüfung wie Rechtschreib- oder Grammatikkorrektur nicht als `human review` oder `editorial control`; erforderlich ist eine inhaltliche Prüfung mit fachlichem Urteil oder redaktioneller Verantwortung. Laut FAQ ist nur für vor dem 02.08.2026 in Verkehr gebrachte Systeme eine begrenzte Übergangslogik bei Art. 50 Abs. 2 KI-VO vorgesehen; Inhalte von vor dem 02.08.2026 müssen nicht rückwirkend gekennzeichnet werden. Die neuen EU-Icons können als Hilfsmittel genutzt werden, ersetzen aber weder die materielle Art.-50-Prüfung noch die richtige Ausgestaltung des Labels ([Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der FAQ-Stand der Kommission vom 26.07.2026 zu Art. 50 KI-VO: Für markierungspflichtige generative Outputs nennt die Kommission nun ausdrücklich enge Ausnahmen etwa für Quellcode, reine Maschine-zu-Maschine-Outputs, geschlossene Entwicklungs- oder Produktumgebungen und Standard-Editing; eine B2B- oder Industrie-Ausnahme ist nur eng zu verstehen. Für vor dem 02.08.2026 in Verkehr gebrachte Systeme läuft die begrenzte Übergangsfrist für Art. 50 Abs. 2 bis zum 02.12.2026. Wenn die Organisation den freiwilligen Transparency Code nicht zeichnet, sollte sie alternative Nachweise für Art. 50 Abs. 2, 4 und 5 dokumentieren; vollzogen wird Art. 50 im Regelfall durch nationale Marktüberwachungsbehörden, während das AI Office nur begrenzt zuständig ist ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Neu zu berücksichtigen ist außerdem der veröffentlichte Leitlinienstand der Kommission vom 30.07.2026: Die Leitlinien stellen nun ausdrücklich klar, dass Unterzeichner des Transparency Code sich unionsweit auf dessen Maßnahmen stützen können. Als Vollzugsstellen nennen sie nationale Marktüberwachungsbehörden, das AI Office für seine Zuständigkeiten und den EDPS für EU-Organe. Die Organisation sollte deshalb dokumentieren, ob sie den Code als Nachweisbaustein nutzt oder welche gleichwertigen Alternativmaßnahmen sie stattdessen vorhält ([Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Seit dem 02.08.2026 ist Art. 50 KI-VO außerdem im laufenden Vollzug. Laut Kommission beginnen seit diesem Datum AI Office und nationale Behörden mit der Durchsetzung. Die neue Kommissions-Kompaktübersicht fasst die vier Transparenzfallgruppen zusammen und nennt für Unternehmen als Bußgeldrahmen bis zu 15 Mio. EUR oder 3 % des weltweiten Jahresumsatzes; für vor dem 02.08.2026 in Verkehr gebrachte generative Systeme bleibt die Übergangsfrist für Art. 50 Abs. 2 bis Dezember 2026 relevant. Die Organisation sollte deshalb nicht nur künftige, sondern bereits live geltende Transparenzpflichten, Ausnahmen und Kontrollzuständigkeiten dokumentieren ([Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems)).

Für die praktische Umsetzung von Art. 50 sollte die Organisation zusätzlich dokumentieren, auf welche anbieterseitigen Markierungsmechanismen sie sich überhaupt stützen darf. Nach aktueller Herstellerdokumentation nennt Anthropic maschinenlesbare Markierungen für unterstützte Claude-Modelle; OpenAI beschreibt gegenwärtig überprüfbare Provenance-Signale für unterstützte Bilder und Audiodateien sowie Prüfwerkzeuge über `openai.com/verify` und eine API. Daraus folgt nicht automatisch, dass jeder Text- oder Dateiausgang in jedem Workflow erkennbar markiert bleibt; bei Copy/Paste, Konvertierung, Bearbeitung oder nicht unterstützten Exportpfaden sind eigene Kennzeichnungs- und Kontrollschritte weiter zu prüfen ([How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Für die Anbieterprüfung kann ergänzend festgehalten werden, ob ein Modellanbieter in der aktuellen EU-Liste als Signatory des GPAI Code of Practice geführt wird. `Anthropic` und `OpenAI` erscheinen dort derzeit; das ist ein freiwilliger Governance-Hinweis zu Provider-Pflichten, ersetzt aber weder AVV/DPA-, Transfer-, Retention- noch Featureprüfungen ([The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai)).

Quellen: [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content), [The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai), [How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content).

## 14. Sicherheitsvorfälle

Sofort melden:

- versehentliche Eingabe personenbezogener Daten in nicht freigegebene KI
- Upload vertraulicher Dateien
- falsche Freigabe von RAG-Quellen
- Datenabfluss durch Agenten/Cowork/Computer Use
- unberechtigter Zugriff
- KI-Ausgabe mit personenbezogenen Falschinformationen, die verwendet wurde

Meldeweg:

1. Vorgesetzte/r
2. Datenschutzbeauftragte/r
3. Informationssicherheit
4. Incident-Team

## 15. Schulung

Alle Nutzer freigegebener KI-Tools müssen geschult werden zu:

- erlaubten Tools
- verbotenen Daten
- Prompt-Minimierung
- Output-Prüfung
- Datenschutzvorfällen
- Risiken von RAG und agentischer KI
- Quellenkritik
- KI-Kompetenz nach Art. 4 KI-VO, bezogen auf technische Kenntnisse, Erfahrung, Ausbildung, Nutzungskontext und betroffene Personengruppen

Die aktuelle Kommissions-Q&A zu Art. 4 KI-VO konkretisiert, dass Schulung und andere Leitmaßnahmen risikobasiert, zielgruppengerecht und am konkreten Nutzungskontext auszurichten sind. Ein Zertifikat oder eine bestimmte AI-Officer-Struktur ist nicht vorgeschrieben; die Organisation sollte aber interne Nachweise zu Trainings oder anderen Leitmaßnahmen führen. Bloßes Verteilen von Nutzungsanweisungen reicht regelmäßig nicht aus. Die Überwachung und Durchsetzung zu Art. 4 startet ab dem 03.08.2026 ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)).

Quellen: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4), [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers).

## 16. Kontrolle und Sanktionen

Die Einhaltung dieser Richtlinie kann stichprobenartig kontrolliert werden, soweit arbeits- und datenschutzrechtlich zulässig. Verstöße können arbeitsrechtliche, vertragliche oder organisatorische Folgen haben.

## 17. Review

Diese Richtlinie wird mindestens jährlich und bei wesentlichen Änderungen aktualisiert:

- neues KI-Tool
- neues Modell
- neues Anthropic-`covered model` oder geänderte modellbezogene Retention-Pflicht
- Aktivierung von Chat-Suche/Memory, Projektwissen, Konnektoren oder MCP
- Aktivierung von Claude-Cowork-Remote-Sessions oder Microsoft-365-Connector-`write tools`
- Nutzung neuer Web-Scraping-Quellen oder fremder Trainingsdatensätze
- neue Anonymisierungsmethode oder geänderte Re-Identifikationsbewertung
- neue Anbieterbedingungen
- neue Retention-/Trainingseinstellung
- neue AI-Act-Transparenzpflicht für den eigenen Einsatzfall
- neue KI-VO-Einstufung, Grundrechte-Folgenabschätzung oder Hochrisiko-Leitlinie
- neue Rechtslage
- neue aufsichtsbehördliche Entscheidung
- Datenschutzvorfall

## Quellen

- [DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf)
- [DSK KI-Systeme TOM](https://datenschutzkonferenz-online.de/media/oh/DSK-OH_KI-Systeme.pdf)
- [DSK RAG Orientierungshilfe](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf)
- [EDPB Opinion 28/2024 KI-Modelle](https://www.edpb.europa.eu/our-work-tools/our-documents/opinion-board-art-64/opinion-282024-certain-data-protection-aspects_en)
- [EDPB ChatGPT Taskforce](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-chatgpt-taskforce_en)
- [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf)
- [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4)
- [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5)
- [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6)
- [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27)
- [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50)
- [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113)
- [AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)
- [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems)
- [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)
- [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content)
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels)
- [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex)
- [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt)
- [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en)
- [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en)
- [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)
- [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use)
- [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)
- [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context)
- [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans)
- [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs)
- [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing)
- [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en)
