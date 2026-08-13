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

Aktuelle Version: 1.17.0
Stand: 13.08.2026

## Versionsinfo

### Version 1.17.0 - 13.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zur Compliance-API-Abdeckung lokaler Cowork- und Claude-Code-Sitzungen ergänzt: Anthropic dokumentiert seit dem am 12.08.2026 aktualisierten Help-Center-Stand die Beta-Abdeckung von Cowork über Claude, Claude Desktop und Claude Mobile sowie von Claude Code über CLI und Claude Desktop in der Compliance API für Enterprise. Für lokale Cowork-Sitzungen nennt Anthropic zusätzlich, dass Session-Inhalte zwar in der Beta abrufbar sind, Lösch-Endpunkte dafür aber noch nicht bereitstehen ([Access the Compliance API](https://support.claude.com/en/articles/13015708-access-the-compliance-api), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Claude Code on Console to Enterprise migration](https://support.claude.com/en/articles/14128775-claude-code-on-console-to-enterprise-migration)).

Geändert:

- Frühere Cowork-Hinweise präzisiert: Für lokale Anthropic-Sitzungen reicht die Formulierung "nicht zentral exportierbar" nach dem aktuellen Herstellerstand nicht mehr aus. Zu dokumentieren ist jetzt getrennt, welche lokalen Cowork- und Claude-Code-Transkripte in der Enterprise-Beta über die Compliance API abrufbar sind, welche lokalen Daten weiterhin nicht zentral administrierbar bleiben und dass für lokale Sessions noch keine Lösch-Endpunkte dokumentiert sind ([Access the Compliance API](https://support.claude.com/en/articles/13015708-access-the-compliance-api), [Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.16.0 - 12.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zur Abschaltung individuell autorisierter App-Synchronisierung in Enterprise/Edu ergänzt: Seit dem 10.08.2026 sind neue solche Sync-Verbindungen nicht mehr verfügbar; ab dem 14.08.2026 werden bestehende deaktiviert und die Löschung der zugehörigen Sync-Daten beginnt. Wenn synchronisiertes Wissen weiter benötigt wird, verweist OpenAI auf admin-gemanagte Google-Drive-/SharePoint-Syncs oder auf nicht-synchronisierte Plugins/Apps ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zur Identitäts- und Business-Verifikation ergänzt: Anthropic beschreibt seit dem 12.08.2026 offiziell, dass für einzelne Use Cases, Integritätsprüfungen oder andere Safety-/Compliance-Maßnahmen eine Verifikation mit Ausweis, Live-Selfie und ggf. Organisationsdaten verlangt werden kann. Laut Hersteller ist Anthropic für diese Verifikationsdaten verantwortlich, die ID-/Selfie-Bilder werden aber bei Persona gehalten und laut Anthropic nicht auf Anthropics Systemen kopiert oder für Modelltraining genutzt ([Identity verification on Claude](https://support.claude.com/en/articles/14328960-identity-verification-on-claude)).

Geändert:

- Account-, Freigabe- und Connector-Hinweise präzisiert: Bei Anthropic sollte vorab festgelegt werden, wer eine etwaige Verifikation überhaupt durchführen darf und ob Business-Verifikation statt ad hoc privater Individualverifikation zu nutzen ist; bei OpenAI sind Altbestände individuell autorisierter Sync-Verbindungen jetzt als konkreter Migrations- und Löschpunkt zu dokumentieren ([Identity verification on Claude](https://support.claude.com/en/articles/14328960-identity-verification-on-claude), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.15.0 - 11.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu Art.-50-Markierungen ergänzt: Anthropic dokumentiert jetzt ausdrücklich maschinenlesbare Markierungen für unterstützte Claude-Outputs. Für in der EU am oder nach dem 02.08.2026 gestartete Modelle nennt Anthropic eingebettete Wasserzeichen für Text und digital signierte Provenance-Metadaten für unterstützte Dateien; ältere Modelle sind laut Hersteller noch in der Nachrüstung ([How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zur EU-AI-Act- und Provenance-Guidance ergänzt: OpenAI ordnet seine Trainingsdatensummaries nun ausdrücklich Art. 53 Abs. 1 Buchst. d KI-VO zu und verweist für Herkunftsnachweise auf C2PA/SynthID, `openai.com/verify` und eine Content Provenance API. Laut separater Help-Center-Doku decken diese Provenance-Signale derzeit unterstützte Bilder und Audiodateien ab; für Text beschreibt OpenAI bislang nur das Ziel eines späteren Ausbaus ([EU AI Act: OpenAI Resources and Customer Guidance](https://help.openai.com/en/articles/12141645-eu-ai-act-openai-resources-and-customer-guidance), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content)).

Geändert:

- Art.-50- und Freigabehinweise präzisiert: Für Anbieter-Markierungen genügt kein pauschales Vertrauen; pro Modalität, Exportpfad und Plattform sollte dokumentiert werden, ob Markierungen technisch verfügbar, erhaltbar und intern prüfbar sind ([How Claude marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), [Provenance signals (Content Credentials, SynthID) in OpenAI-generated content](https://help.openai.com/en/articles/8912793-provenance-signals-content-credentials-synthid-in-openai-generated-content), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.14.0 - 10.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Managed-Agents-Hinweise zu `inference_geo` und `self-hosted sandboxes` ergänzt: Laut Claude-Platform-Release-Notes vom 07.08.2026 kann Anthropic den Ort der Modellinferenz nun pro Agent oder Session steuern; die aktuelle Data-Residency-Dokumentation trennt dabei zwischen Inference-Geo und Workspace-Geo. Für `self-hosted sandboxes` dokumentiert Anthropic, dass Tool-Ausführung, Dateisystem und Network Egress in eigener Infrastruktur bleiben können, Tool-Ein- und -Ausgaben aber weiter an die Control Plane fließen ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu gemounteten GitHub-Repositories ergänzt: Ebenfalls seit dem 07.08.2026 können Claude Managed Agents Skills aus dem Wurzelpfad `.claude/skills` eines gemounteten GitHub-Repositories automatisch erkennen und laden; dafür sind Repo-Herkunft, Zugriffsrechte sowie Branch-/PR-Kontrollen als eigener Governance-Punkt zu dokumentieren ([Claude Platform release notes, 07.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github)).

Geändert:

- Freigabehinweise für Anthropic-Agentik präzisiert: Für Managed Agents sollten jetzt zusätzlich Geo-Einstellungen, Cloud-vs.-`self-hosted`-Betrieb und automatisch geladene GitHub-Skills getrennt dokumentiert und freigegeben werden ([Data residency](https://platform.claude.com/docs/en/manage-claude/data-residency), [Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Accessing GitHub](https://platform.claude.com/docs/en/managed-agents/github)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.13.0 - 09.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu Skill-/Plugin-Scanning ergänzt: Seit dem 06.08.2026 dokumentiert Anthropic für Enterprise-Pläne eine Beta, mit der neue Uploads oder Änderungen an Dritt-Skills und -Plugins vor der Ausführung auf schädliche Inhalte geprüft werden können; die Funktion ist standardmäßig aus, bestehende Skills/Plugins bleiben unberührt, und Rollen können den Geltungsbereich weiter eingrenzen ([Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu ChatGPT Voice ergänzt: Laut Enterprise-/Edu-Release-Notes vom 07.08.2026 unterstützt `ChatGPT Voice` jetzt Datei-Uploads und Projects; Voice kann damit in Projekten auf aktuelle Projekt-Chats, Quellen und Projektanweisungen zugreifen. Ebenfalls seit dem 07.08.2026 ist `Live` in Enterprise-, Edu- und Healthcare-Workspaces die Standard-Voice-Erfahrung, sobald Workspace-Owner Voice aktivieren ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Geändert:

- Freigabehinweise für Anthropic-Skills/-Plugins präzisiert: Wenn Skills oder Plugins zugelassen werden, sollte jetzt dokumentiert werden, ob das optionale Scanning aktiviert ist, dass es nur für neue Uploads/Änderungen gilt und wie mit Warnhinweisen für riskante Inhalte umgegangen wird ([Provision and manage skills for your organization](https://support.claude.com/en/articles/13119606-provision-and-manage-skills-for-your-organization)).
- Freigabehinweise für OpenAI-Voice/Workloads präzisiert: Bei `ChatGPT Voice` in Work oder Codex sind jetzt nicht nur identische Tool-/Rechtepfade, sondern auch Datei-Uploads, Project-Kontext und die Default-Umstellung auf `Live` als eigener Governance-Punkt zu dokumentieren ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.12.0 - 08.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu Managed Agents ergänzt: Laut aktueller Anthropic-Produktdokumentation sind Claude Managed Agents zustandsbehaftet, speichern Gesprächsverlauf, Sandbox-Zustand und Outputs serverseitig und sind deshalb derzeit weder für Zero Data Retention noch für HIPAA-BAA-Abdeckung geeignet; Sessions und hochgeladene Dateien lassen sich aber separat per API löschen ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu `Inference hooks` ergänzt: Seit dem 05.08.2026 dokumentiert Anthropic die Beta für Claude Enterprise als vorgelagerten Allow-/Deny-Kontrollpunkt über `claude.ai`, Cowork und Claude Code; die technische Doku nennt zusätzlich Shadow-Mode, konfigurierbares Failure Handling und den Ausschluss von Bedrock/Google Cloud ([Claude Platform release notes, 05.08.2026](https://platform.claude.com/docs/en/release-notes/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks), [Configure Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks-configuration)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu ChatGPT Work/Voice ergänzt: OpenAI dokumentiert für die Desktop-App jetzt ausdrücklich, dass Voice in Work und Codex dieselben Tools und Berechtigungen wie die gewählte Experience nutzt und zur Koordination laufender Aufgaben dienen kann; für berechtigte Enterprise-/Edu-Workspaces mit EKM ist Work standardmäßig für Mitglieder der Default-Rolle aktiviert, Cloud-Work-Chats synchronisieren zwischen Web, Mobile und Desktop, lokale Chats bleiben dagegen auf dem jeweiligen Rechner ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)).

Geändert:

- Freigabehinweise für Anthropic-Agentik präzisiert: Für Managed Agents sollten neben Zeitplänen, Vaults und Deployment-Rechten jetzt ausdrücklich Server-State, fehlende ZDR-/BAA-Eignung und eine eventuelle vorgeschaltete Inline-Policy-Prüfung per `Inference hooks` dokumentiert werden ([Claude Managed Agents overview](https://platform.claude.com/docs/en/managed-agents/overview), [Inference hooks](https://platform.claude.com/docs/en/manage-claude/inference-hooks)).
- Freigabehinweise für OpenAI-Workloads präzisiert: Bei Work/Codex sind jetzt Default-Aktivierung, Cloud-vs.-Lokal-Trennung und Voice-Nutzung mit identischen Tool-/Rechtepfaden als eigener Governance-Punkt zu dokumentieren ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice-in-work-and-codex)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.11.0 - 07.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue operative Steuerungshinweise zu Claude Cowork ergänzt: Anthropic präzisiert in der am 07.08.2026 aktualisierten Team-/Enterprise-Dokumentation die Default-Einstellungen für Cloud-Sessions, die Freigabelogik für schreibfähige Connector-Tools, die fehlende separate Admin-Abschaltung für Cowork-Projekte und die getrennte Behandlung von `web fetch`, `web search` und MCPs außerhalb der normalen Network-Egress-Regeln ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen kleinen OpenAI-Governance-Hinweis ergänzt: Seit dem 06.08.2026 können Enterprise-, Edu- und Healthcare-Admins In-App-Updates der ChatGPT-Desktop-App abschalten. Wenn diese Steuerung genutzt wird, braucht es einen eigenen zeitnahen Freigabe- und Patchprozess, weil OpenAI laut Release Notes weder Version-Pinning noch einen separaten Stable Channel oder erweiterten Support für ältere Versionen anbietet ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).
- KI-VO-Hinweise um den Vollzugsstart zu Art. 50 ergänzt: Die EU-Kommission dokumentiert seit dem 31.07./02.08.2026 den Beginn der Durchsetzung, fasst die vier Transparenzfallgruppen nochmals kompakt zusammen und nennt den Bußgeldrahmen sowie die fortgeltende Übergangslogik für vor dem 02.08.2026 in Verkehr gebrachte generative Systeme ([Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems)).

Geändert:

- Cowork- und Agentik-Freigabehinweise präzisiert: Für Claude Cowork sollten Session-Ort, Rollenfreigaben, Per-Task-Approval, Projekt-/Dateispeicher sowie separate Kontrollen für Websuche, Web-Fetch und MCPs jetzt ausdrücklich getrennt dokumentiert werden ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).
- Art.-50-KI-VO-Hinweise auf laufenden Vollzug umgestellt: Seit dem 02.08.2026 sind Transparenzpflichten nicht mehr nur ein Vorbereitungsprojekt, sondern ein aktiv durchgesetzter Compliance-Baustein mit dokumentierbaren Sanktionen ([Commission starts enforcing AI Act rules and new transparency requirements on 2 August](https://digital-strategy.ec.europa.eu/en/news/commission-starts-enforcing-ai-act-rules-and-new-transparency-requirements-2-august), [Quick Facts: Transparency rules for AI systems](https://digital-strategy.ec.europa.eu/en/factpages/quick-facts-transparency-rules-ai-systems)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.10.1 - 31.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen kleinen OpenAI-API-Hinweis ergänzt: OpenAI dokumentiert `Fast mode` seit dem 30./31.07.2026 ausdrücklich als mit Data Residency, Zero Data Retention und BAA kompatibel. Für Freigaben bedeutet das, dass ein bloßer Wechsel des Verarbeitungsmodus die Datenschutz-Grundvoraussetzungen nicht automatisch ändert, die Prüfung der konkret genutzten Endpunkte, Tools und der regionalen Verfügbarkeit aber bestehen bleibt ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq)).

Geändert:

- OpenAI-Freigabehinweise für API-Projekte präzisiert: `Fast mode` sollte nicht pauschal als unzulässig behandelt werden, wenn Data Residency, ZDR oder BAA genutzt werden; maßgeblich bleiben die Dokumentation der konkret aktivierten Features und die regionale Verfügbarkeit laut OpenAI ([Fast mode](https://developers.openai.com/api/docs/guides/fast-mode), [Fast mode FAQ](https://help.openai.com/en/articles/11647665-fast-mode-faq), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.10.0 - 30.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu Work/Agent/Library ergänzt: Das aktuelle Work-Admin-FAQ grenzt die Nachweislage enger ein. Für Work/Codex decken Compliance API und Compliance Logs zwar Unterhaltungen und Responses ab, nicht aber Dateien, Aktionen oder Tool-Calls; die Compliance Logs Platform hält diese Daten laut OpenAI 30 Tage vor, längere Aufbewahrung erfordert einen laufenden Export. Für ChatGPT-Agent stellt OpenAI außerdem klar, dass individuelle Agent-Aktionen nicht in der Compliance API erscheinen und `apps with sync` nicht direkt als Agent-Datenquelle dienen. Zusätzlich werden ChatGPT-Library-Dateien getrennt von Chats verwaltet; das Löschen eines Chats löscht gespeicherte Library-Dateien nicht automatisch, und Compliance-Admins können sie über eigene Endpunkte exportieren oder löschen ([ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [File storage and Library in ChatGPT](https://help.openai.com/en/articles/20001052-file-storage-and-library-in-chatgpt), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt)).
- KI-VO-Hinweise um den neuen Kommissionsstand vom 30.07.2026 ergänzt: Die veröffentlichte Art.-50-Leitlinienseite stellt nun ausdrücklich klar, dass Unterzeichner des Transparency Code sich unionsweit auf dessen Maßnahmen stützen können; außerdem nennt sie nationale Marktüberwachungsbehörden, das AI Office für seine Zuständigkeiten und den EDPS für EU-Organe als Vollzugsstellen. Für die Anbieterprüfung kommt hinzu, dass die aktuelle EU-Liste zum GPAI Code of Practice `Anthropic` und `OpenAI` als Signatories führt; das ist ein freiwilliger Governance-Hinweis, ersetzt aber keine DSGVO-, Transfer- oder Featureprüfung ([Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai)).

Geändert:

- OpenAI-Freigabe-, Lösch- und Logging-Hinweise präzisiert: Für ChatGPT Work, Agent, Codex und Library sollten Nachweislücken bei Dateien/Aktionen/Tool-Calls, getrennte Retention von Chats und Library-Dateien sowie ein nötiger Export aus den 30-Tage-Compliance-Logs ausdrücklich dokumentiert werden ([ChatGPT Work admin FAQ](https://learn.chatgpt.com/docs/enterprise/work-admin-faq), [ChatGPT agent](https://help.openai.com/en/articles/11752874-chatgpt-agent), [Chat and File Retention Policies in ChatGPT](https://help.openai.com/en/articles/8983778-chat-and-file-retention-policies-in-chatgpt)).
- Art.-50-KI-VO-Umsetzung präzisiert: Neben den bisherigen FAQ- und Leitlinienhinweisen sollte jetzt auch dokumentiert werden, ob die Organisation den Transparency Code als Nachweisbaustein nutzt oder gleichwertige Alternativmaßnahmen vorhält; bei Modellanbietern kann der aktuelle GPAI-Code-Signaturstatus als ergänzender, aber nicht abschließender Governance-Baustein erfasst werden ([Guidelines on transparency obligations for providers and deployers of certain AI systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [The General-Purpose AI Code of Practice](https://digital-strategy.ec.europa.eu/en/policies/contents-code-gpai)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.9.1 - 29.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um eine neue Anthropic-Klarstellung ergänzt: Die aktuelle Team-/Enterprise-Dokumentation trennt bei Claude Cowork zwischen Cloud-/Remote-Sessions und lokaler Nutzung. Für mobile/webbasierte bzw. cloudgespeicherte Remote-Sessions verweist Anthropic nun auf Erfassbarkeit über die Compliance API; lokale Sessions bleiben dagegen lokal gespeichert und nicht zentral exportierbar ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans)).

Geändert:

- Bisher zu pauschale Cowork-Hinweise präzisiert: Für Claude Cowork sollte nach aktueller Anthropic-Dokumentation zwischen Session-Inhalten/Artefakten einerseits und laufender Aktivitätstelemetrie andererseits unterschieden werden. Anthropic beschreibt für Tool-Calls, Dateizugriffe und Approval-Entscheidungen OpenTelemetry als Monitoring-Weg und stellt zugleich klar, dass dies die Compliance API nicht ersetzt; die genaue Grenzziehung sollte deshalb intern ausdrücklich dokumentiert werden ([Use Claude Cowork on Team and Enterprise plans](https://support.claude.com/en/articles/13455879-use-claude-cowork-on-team-and-enterprise-plans), [Monitor Claude Cowork activity with OpenTelemetry](https://support.claude.com/en/articles/14477985-monitor-claude-cowork-activity-with-opentelemetry)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.9.0 - 28.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen neuen Art.-4-KI-VO-Prüfpunkt ergänzt: Die aktuelle Kommissions-Q&A konkretisiert AI Literacy als risikobasiertes, rollen- und kontextbezogenes Pflichtprogramm; interne Nachweise zu Trainings oder anderen Leitmaßnahmen genügen, ein Zertifikat oder eine bestimmte AI-Officer-Struktur werden nicht verlangt. Die Überwachung und Durchsetzung zu Art. 4 startet ab dem 03.08.2026 ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Agentik-Hinweise ergänzt: ChatGPT Work kann auf dem Desktop freigegebene lokale Ordner öffnen; lokale Dateien und Outputs bleiben dort, bis sie ausdrücklich bewegt oder geteilt werden. Work kann außerdem über Scheduled Tasks einmalig, wiederkehrend oder monitoringbasiert laufen; solche Tasks sind laut OpenAI in der Compliance API enthalten und sollten deshalb als gesondert freigabepflichtige Agentik-Funktion dokumentiert werden ([ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt)).

Geändert:

- Schulungs-, Freigabe- und DSFA-Hinweise präzisiert: Art.-4-KI-VO-Compliance sollte nicht nur als allgemeine Schulung, sondern nach Zielgruppe, Risiko und Use Case dokumentiert werden. Für ChatGPT Work und Scheduled Tasks sollten freigegebene lokale Ordner, zulässige App-/Dateizugriffe, Monitoring-Läufe, Benachrichtigungen und der fehlende Zugriff von Tasks auf Projektdateien getrennt bewertet werden ([AI Literacy - Questions & Answers](https://digital-strategy.ec.europa.eu/en/faqs/ai-literacy-questions-answers), [ChatGPT Work and Codex](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex), [Scheduled Tasks in ChatGPT](https://help.openai.com/en/articles/10291617-tasks-in-chatgpt)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.8.2 - 27.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Governance-Hinweise ergänzt: Seit dem 09.07.2026 laufen ChatGPT-Apps über das Plugin Directory; in Enterprise/Edu werden Plugin-Installation, zugrunde liegende Apps und Rollen getrennt verwaltet, und für Enterprise-Workspaces ohne Opt-out plant OpenAI seit dem 23.07.2026 eine Standardaktivierung von Skills. Skill-Uploads und pluginbasierte Zusatzfunktionen sollten deshalb getrennt freigegeben und dokumentiert werden ([Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).

Geändert:

- OpenAI-Connector-/App-Hinweise präzisiert: Bei `apps with sync` werden Inhalte vorab indexiert; für nicht in der eigenen Residency-Region unterstützte Sync-Apps liegt dieser Suchindex laut OpenAI in US-Azure-Rechenzentren. Außerdem sind App-Unterhaltungen in der Compliance API und App-Calls in den Compliance Logs nachvollziehbar, während nicht synchronisierte Apps zwar residency-kompatibel sein können, Daten an den angebundenen Drittservice aber dessen eigenen Residency-Regeln unterwerfen ([Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.8.1 - 26.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um den neuen FAQ-Stand der EU-Kommission vom 26.07.2026 zu Art. 50 KI-VO ergänzt: Die Kommission präzisiert u. a. eng auszulegende Ausnahmen von der Markierungs- und Erkennungspflicht für generative Outputs, etwa für Quellcode, reine Maschine-zu-Maschine-Outputs, geschlossene Entwicklungsumgebungen und Standard-Editing; außerdem nennt sie für vor dem 02.08.2026 in Verkehr gebrachte Systeme nun ausdrücklich den 02.12.2026 als Ende der begrenzten Übergangsfrist für Art. 50 Abs. 2 und verweist im Regelfall auf nationale Marktüberwachungsbehörden als Vollzugsstellen ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).

Geändert:

- KI-VO-Zeitplan zu Hochrisiko-KI präzisiert: Die bisher nur über Leitlinien dargestellte Verschiebung bestimmter Hochrisiko-Pflichten steht nun im Zusammenhang mit dem im Amtsblatt vom 24.07.2026 veröffentlichten `Digital Omnibus on AI` (Regulation (EU) 2026/1744); die Kommissionsübersicht nennt dafür nun einen endgültigen Anwendungsbeginn ab 02.12.2027 bzw. 02.08.2028 ([AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.8.0 - 25.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Prüfpunkte ergänzt: `custom connectors` über remote MCP können laut aktueller Herstellerdokumentation auf Claude, Cowork und Claude Desktop aus der Anthropic-Cloud statt vom lokalen Gerät verbinden; außerdem beschreibt Anthropic für Cowork zusätzliche Organisationskontrollen für Remote-Sessions, weist aber zugleich darauf hin, dass Cowork-Aktivität derzeit nicht in Audit Logs, Compliance API oder Data Exports erscheint ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview)).
- KI-VO-Hinweise um die neue Kommissions-FAQ vom 22.07.2026 ergänzt: Bei Hochrisiko-KI müssen Betreiber laut FAQ u. a. Nutzungsanweisungen umsetzen, den Betrieb überwachen, menschliche Aufsicht zuweisen und bei eigenen Eingabedaten auf Relevanz und hinreichende Repräsentativität achten; öffentliche Stellen bzw. Anbieter öffentlicher Dienste brauchen grundsätzlich vor der ersten Nutzung eine Grundrechte-Folgenabschätzung, und bei entscheidungsrelevanten Hochrisiko-Outputs ist ein Recht auf Erklärung zu berücksichtigen ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

Geändert:

- Hinweise zu Claude-Microsoft-365-`write tools` präzisiert: Für die aktivierten Schreibwerkzeuge ist laut aktueller Herstellerdokumentation eine erneute Tenant-Einwilligung zu erweiterten Microsoft-Graph-Berechtigungen erforderlich; E-Mails tragen einen `agent-initiated`-Header, Datei- und Kalender-Schreibvorgänge derzeit nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.7.4 - 23.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um den neuen Leitlinienstand der EU-Kommission vom 20.07.2026 zu Art. 50 KI-VO ergänzt: direkte Interaktion mit Chatbots, Agenten oder Avataren soll grundsätzlich ab der ersten Interaktion klar kenntlich gemacht werden; für veröffentlichte KI-Texte zu Fragen von öffentlichem Interesse reicht eine bloß formale Endredaktion nicht als `human review` oder `editorial control` aus ([Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act)).
- KI-VO-Hinweise um den neuen Kommissionsstand zu Übergangslogik und Labels ergänzt: Laut FAQ vom 20.07.2026 ist nur für vor dem 02.08.2026 in Verkehr gebrachte Systeme eine begrenzte Übergangslogik bei Art. 50 Abs. 2 KI-VO vorgesehen; Inhalte von vor dem 02.08.2026 müssen nicht rückwirkend gekennzeichnet werden. Die neuen EU-Icons sind nur ein optionales Hilfsmittel und begründen für sich keinen Compliance-Nachweis ([Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content)).

Geändert:

- Den operativen FAQ-Hinweis zum Art.-50-Transparenzcode aktualisiert: Für die erste Signatory-Liste nennt die aktuelle AI-Office-FAQ den 27.07.2026, 18:00 CEST; spätere Unterzeichnungen bleiben möglich ([Signing the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.7.3 - 12.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen Governance-Prüfpunkt ergänzt: Anthropic dokumentiert seit dem 01.07.2026 für Enterprise-Pläne eine Beta zur organisations- und rollenbezogenen Modellfreigabe einschließlich Effort-Caps; damit lassen sich nicht freigegebene Modelle technisch begrenzen, statt nur organisatorisch zu verbieten ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen Transparenz-/Beschäftigtendatenschutz-Prüfpunkt ergänzt: Bei Anthropic Team und Enterprise ist `individual usage analytics` laut aktueller Herstellerdokumentation ab dem 11.07.2026 standardmäßig aktiviert, sofern die Organisation es nicht wieder abschaltet; damit werden nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill sichtbar ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans)).

Geändert:

- Anbieter- und DSFA-Prüfung präzisiert: Für Claude Code, Cowork und andere Anthropic-Organisationen reichen allgemeine Freigabehinweise nicht mehr aus; Modell-Allowlist, Effort-Grenzen und der Umgang mit nutzerbezogenen Usage-Analytics sollten getrennt dokumentiert werden ([Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.7.2 - 11.07.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen neuen Agentik-Prüfpunkt ergänzt: Anthropic dokumentiert seit dem 10.07.2026 für Managed Agents geplante `scheduled deployments`, die Sessions autonom per Cron starten können; dabei können u. a. Dateien, GitHub-Zugänge, Memory Stores und Vaults eingebunden werden. Für `environment_variable`-Vault-Credentials stellt Anthropic klar, dass Secret-Werte dem Agenten nicht offengelegt, sondern erst beim ausgehenden Request eingesetzt werden ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview)).
- KI-VO-Hinweise um den neuen AI-Office-FAQ-Stand ergänzt: Für die erste Signatory-Liste zum Art.-50-Transparenzcode müssen Signaturformulare bis zum 27.07.2026, 18:00 CEST eingereicht werden; eine spätere Unterzeichnung bleibt möglich, Nicht-Unterzeichner müssen die Einhaltung von Art. 50 KI-VO aber auf anderem Weg darlegen ([Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Geändert:

- Freigabe- und DSFA-Prüfung präzisiert: Für Anthropic-Managed-Agents reichen allgemeine Hinweise zu Agentik oder Secrets nicht mehr aus; Zeitpläne, autonome Sessionstarts, Run-Historie/Webhooks, eingebundene Vaults und Secret-Scopes sollten getrennt freigegeben und dokumentiert werden ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults)).

Entfernt:

- Keine Inhalte entfernt.

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
