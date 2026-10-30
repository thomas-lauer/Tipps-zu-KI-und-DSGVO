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

Aktuelle Version: 1.32.1
Stand: 30.10.2026

## Versionsinfo

### Version 1.32.1 - 30.10.2026

Ergänzt:

- Anthropic-`Inference hooks` als zusätzlichen Datenfluss präzisiert: Die Funktion ist laut Anthropic für Enterprise allgemein verfügbar; jeder Prompt, jede Tool-Antwort und Text aus Uploads wird vor der Claude-Verarbeitung an einen kundenseitig betriebenen Policy-Server übermittelt. Der Endpoint, die dortige Verarbeitung sowie Freigabe- und Fehlerverhalten sind daher in Checkliste, DSFA und Richtlinie zu dokumentieren ([Inference hooks overview](https://support.claude.com/en/articles/16059458-inference-hooks-overview)).

Geändert:

- Die bisherige Beta-Einordnung von `Inference hooks` durch den aktuelleren offiziellen Herstellerstand ersetzt; die technische Ausgestaltung und tatsächliche Nutzung bleiben organisationsspezifisch zu prüfen.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.32.0 - 29.10.2026

Ergänzt:

- Hinweise zur Prüfung persönlicher Inhalte vor Workspace-Migration in Checkliste, DSFA und Richtlinie. OpenAI dokumentiert seit dem 23.10.2026 eine feste Siebentagesfrist für verpflichtende Enterprise-/Edu-Migrationen mit verifizierter Domain; Beginn ist die Aufnahme in den Workspace ([Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-and-edu-release-notes)).

Geändert:

- Migrationsprüfung um Datenumfang, Export und Zielzugriff präzisiert; einzelne Chats sind nicht zur Übertragung auswählbar ([OpenAI: Workspace-Migration](https://help.openai.com/en/articles/8801890-migrating-your-personal-workspace-to-chatgpt-business-or-enterprise), abgerufen am 29.10.2026; ein absolutes Aktualisierungsdatum nennt die Seite nicht).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.31.0 - 23.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen Aufbewahrungs- und Transparenzhinweis zu `Locked chats` ergänzt: OpenAI dokumentiert für ChatGPT Enterprise und Edu seit dem 20.10.2026, dass gesperrte Unterhaltungen aus regulärem Verlauf, angehefteten Chats und der Suche ausgeblendet werden; sie werden dadurch nicht gelöscht. Die Aufbewahrungsrichtlinien der Organisation und die Compliance-Anforderungen gelten weiter, und die Nachrichten bleiben in den über die Compliance Platform verfügbaren Conversation Message Logs enthalten. Die Sperrfunktion darf daher nicht als Lösch- oder Retention-Kontrolle eingeordnet werden ([ChatGPT Enterprise and Edu release notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-and-edu-release-notes)).

Geändert:

- Freigabe-, DSFA- und Richtlinienprüfung für geschützte Chatansichten präzisiert: Zweck, zulässige Nutzerkreise, Aufbewahrung, Compliance-Export und Betroffenenrechte sind unabhängig von der lokalen Sperransicht festzulegen ([ChatGPT Enterprise and Edu release notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-and-edu-release-notes)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.30.0 - 22.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen eng abgegrenzten QMS-Prüfpunkt für Anbieter von Hochrisiko-KI ergänzt: Die Kommission berichtete am 19.10.2026 über die mit Durchführungsbeschluss (EU) 2026/2274 am 14.10.2026 im Amtsblatt veröffentlichte Referenz auf EN 18286:2026. Der harmonisierte Standard kann für die von ihm abgedeckten Anforderungen des Qualitätsmanagementsystems nach Art. 17 KI-VO eine Konformitätsvermutung begründen; er gilt nicht als pauschaler Compliance-Nachweis für Betreiber oder andere KI-Systeme. Anbieter müssen daher Rolle, Hochrisiko-Einstufung, abgedeckte Art.-17-Anforderungen und die tatsächliche Umsetzung getrennt dokumentieren ([European Commission: First harmonised standard supporting the AI Act](https://digital-strategy.ec.europa.eu/en/library/first-harmonised-standard-supporting-ai-act-published-official-journal), [Commission Implementing Decision (EU) 2026/2274](https://eur-lex.europa.eu/eli/dec_impl/2026/2274/oj/eng)).

Geändert:

- KI-VO-Prüfung um die Abgrenzung zwischen einer Konformitätsvermutung für abgedeckte Art.-17-QMS-Anforderungen und der weiterhin erforderlichen Einzelfallprüfung ergänzt.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.29.0 - 21.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um Freigabehinweise für `ChatGPT Sites`, Enterprise-Workspace-Blocking und `Claude Design` ergänzt: ChatGPT Sites kann Prompts, Gesprächskontext, Dateien, Site-Code, Zugriffs- und Speichereinstellungen sowie Betriebsdaten verarbeiten; in Enterprise ist öffentliche Veröffentlichung standardmäßig deaktiviert, in Business sind Sites standardmäßig aktiviert. Das Enterprise-Workspace-Blocking kann über einen Netzwerk-Header nicht zugelassene, auch persönliche Workspaces ausfiltern. `Claude Design` ist auf Enterprise-Plänen seit dem 15.10.2026 standardmäßig aktiv und kann Design-Assets wie Codebasen oder Präsentationen verarbeiten. Freigaben müssen daher Datenkategorien, Rollen, Veröffentlichungsziel, verbundene Apps sowie die jeweiligen Admin- und Netzwerkkontrollen getrennt festlegen ([ChatGPT Sites](https://help.openai.com/en/articles/20001339-creating-and-using-chatgpt-sites), [Corporate Network Controls](https://help.openai.com/en/articles/20001323-corporate-network-controls-in-chatgpt-enterprise), [Claude Design admin guide](https://support.claude.com/en/articles/14604406-claude-design-admin-guide-for-team-and-enterprise-plans)).

Geändert:

- Freigabe- und DSFA-Prüfpunkte für veröffentlichbare KI-Artefakte, externe Site-Zugriffe und die organisatorische Trennung zugelassener Enterprise- von persönlichen ChatGPT-Workspaces präzisiert.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.28.0 - 20.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um Freigabehinweise für `ChatGPT for Word` ergänzt: Die offizielle OpenAI-Dokumentation beschreibt die Funktion als Seitenleiste im geöffneten Word-Dokument. Seit dem 01.10.2026 ist sie standardmäßig aktiviert; Workspace-Admins und Microsoft-365-Admins können sie jeweils steuern. Unterhaltungen des Add-ins sind von der ChatGPT-Historie getrennt, Memory und Skills werden nicht übernommen. Die Freigabe muss daher Dokumentzugriff, beide Administrationsschalter, das getrennte Gesprächs- und Löschkonzept sowie die Datenkontrollen des verwendeten ChatGPT-Plans abdecken ([ChatGPT for Word](https://help.openai.com/en/articles/20001526-chatgpt-for-word)).

Geändert:

- Freigabe- und DSFA-Prüfpunkte für ChatGPT-Add-ins in Microsoft 365 präzisiert.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.27.0 - 18.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um Governance-Hinweise für `@ChatGPT` in Slack und Microsoft Teams ergänzt: OpenAI dokumentiert für Business, Edu und Enterprise einen eigenen Service-Account mit den für ihn konfigurierten Unternehmensverbindungen. Die Rechte dieses Kontos bestimmen lesbare Daten und zulässige Aktionen; persönliche Autorisierungen einzelner Mitglieder sind davon getrennt. Antworten in geteilten Gesprächen sind für deren Teilnehmende sichtbar. Die Freigabe muss daher Service-Account, Verbindungsrechte, persönliche Autorisierungen, zulässige Kanäle/Chats und Empfängerkreis getrennt dokumentieren ([Setting up and managing @ChatGPT in Slack and Microsoft Teams](https://help.openai.com/en/articles/20001538-setting-up-and-managing-chatgpt-in-slack-and-microsoft-teams)).

Geändert:

- Freigabe- und DSFA-Prüfpunkte für Slack-/Teams-Integrationen von ChatGPT präzisiert.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.26.0 - 17.10.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Hinweise zur Anthropic-Cowork-Umstellung ergänzt: Seit dem 06.10.2026 laufen neue Cowork-Aufgaben für Pro- und Max-Pläne laut Anthropic in der Cloud; die Option „Only on your computer“ wurde entfernt. Bereits lokal begonnene Aufgaben verbleiben lokal, neue geplante Aufgaben laufen in der Cloud. Lokale Ordner bleiben laut Anthropic auf dem Gerät; bei Cloud-Aufgaben werden nur Dateien aus verbundenen Ordnern bei Bedarf kopiert. Für Team und Enterprise nennt Anthropic Cloud-Cowork weiterhin Beta-Status und eine Admin-Freigabe für Enterprise ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Admin-Kontrollen ergänzt: OpenAI dokumentiert für Enterprise und Edu seit dem 16.10.2026 neue Inhaltskontrollen für den Echtzeit-Zugriff der Apps Google Drive, Microsoft Teams und Outlook Email, soweit diese im Workspace aktiviert sind. Owners und Admins können sie unter „Safety & Security Controls“ je App prüfen; individuelle Google-/Microsoft-Berechtigungen gelten weiter. Seit dem 08.10.2026 können Enterprise-/Edu-Admins mit RBAC außerdem Pluginzugriff rollenbezogen auf „Available“, „Install“ oder „Disabled“ setzen ([ChatGPT Enterprise and Edu release notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-and-edu-release-notes)).

Geändert:

- Freigabe- und DSFA-Hinweise zu agentischen Cloud-Aufgaben und OpenAI-Plugins präzisiert: Für die jeweiligen Workspaces sind Ausführungsort, Datenkopien, lokale Ordnerzugriffe, Zeitpläne sowie App-Inhaltskontrollen und rollenbezogene Pluginrechte nachvollziehbar zu dokumentieren.

Entfernt:

- Keine Inhalte entfernt.

### Version 1.25.0 - 24.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um einen neuen Anthropic-Hinweis zu Google-Workspace-Connectoren ergänzt: Beim am 24.08.2026 verifizierten Help-Center-Stand speichert Anthropic über Gmail-, Drive- und Calendar-Connectoren abgerufene Daten auf Anthropic-Servern zusammen mit dem zugehörigen Chat; laut Anthropic können diese Daten grundsätzlich über die Löschung des Chats entfernt werden. Für Team- und Enterprise-Pläne werden die Connectoren erst nach Owner-/Primary-Owner-Freigabe nutzbar. Anthropic erklärt außerdem, die Connector-Daten selbst nicht für Modelltraining zu verwenden; bei Consumer-Nutzung mit aktiviertem Trainings-Opt-in können aber kopierte Inhalte oder Antworten mit solchen Daten weiterhin in die Modellverbesserung einfließen ([Use Google Workspace connectors](https://support.claude.com/en/articles/10166901-use-google-workspace-connectors)).

Geändert:

- Freigabe-, Lösch- und Trainingshinweise zu Anthropic-Connectoren präzisiert: Für Google-Workspace-Connectoren ist nun gesondert zu dokumentieren, ob nur Team-/Enterprise-Nutzung zulässig ist, wie Chat-Löschung als Löschpfad organisatorisch umgesetzt wird und dass Consumer-Konten mit Trainings-Opt-in trotz fehlendem Connector-Training über kopierte Inhalte oder Antworten weiterhin ein Trainingsrisiko auslösen können ([Use Google Workspace connectors](https://support.claude.com/en/articles/10166901-use-google-workspace-connectors)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.24.0 - 23.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zur `Compliance Platform` ergänzt: Beim am 23.08.2026 verifizierten Help-Center-Stand beschreibt OpenAI die Enterprise-/Edu-Compliance jetzt ausdrücklich als Kombination aus `Compliance Logs Platform` für unveränderliche, nur anhängbare Audit-Events und `Stateful Compliance API` für zustandsbezogene Abfragen. Die Logs werden laut OpenAI 30 Tage vorgehalten; für längere Aufbewahrung ist ein laufender Export nötig. Löschungen über die API machen Daten nicht wiederherstellbar, beseitigen aber laut OpenAI keine intern zu Audit- oder Sicherheitszwecken protokollierten Daten; außerdem werden alle authentifizierten Zugriffe auf diese API selbst protokolliert ([OpenAI Compliance Platform for Enterprise and Edu Customers](https://help.openai.com/en/articles/9261474-openai-compliance-platform-for-enterprise-and-edu-customers)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu `Playground`/`Workbench (legacy)` ergänzt: Beim am 23.08.2026 verifizierten Help-Center-Stand speichert der neue Playground laut Anthropic weder Prompt-Historie noch Gespräche serverseitig; der aktuelle Entwurf bleibt im Browser. Gespeicherte Legacy-Workbench-Daten können nur noch bis zum 01.09.2026 aus der Claude Console exportiert werden und sind danach laut Anthropic nicht mehr wiederherstellbar ([How do I use the playground?](https://support.claude.com/en/articles/8606378-how-do-i-use-the-playground)).

Geändert:

- Hinweise zu Anthropic-Konto-Migrationen präzisiert: Laut der am 23.08.2026 verifizierten Migrationsdokumentation wandern `Claude Design`-Systeme und -Projekte nur dann mit, wenn sie seit dem 14.08.2026 migriert wurden; vor dem 14.08.2026 migrierte Design-Inhalte werden ausdrücklich nicht übernommen ([Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.23.1 - 22.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `workspace-scoped Admin APIs` und `Admin keys` ergänzt: Seit dem Release-Stand vom 20.08.2026 können Workspace-Owner und -Admins Einladungen sowie Mitglieder automatisiert verwalten; laut der am 22.08.2026 verifizierten Admin-Key-Dokumentation können Admin Keys u. a. Analytics, Gruppen-/Mitgliedschaftslisten, Service-Accounts oder Compliance-Endpunkte steuern, gewähren aber keinen Modellzugriff und sind von `service-account access tokens` zu trennen ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Managing Admin keys in the Credentials tab](https://help.openai.com/en/articles/20001407-managing-admin-keys-in-the-credentials-tab)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um präzisierte Anthropic-Hinweise zu `memory stores` in `self-hosted sandboxes` ergänzt: Laut aktueller Sandbox- und Sicherheitsdokumentation bleiben `memory stores` einschließlich Versionshistorie bei Anthropic gehostet; lokal liegt nur eine synchronisierte Arbeitskopie unter `/mnt/memory/`, die bei fehlgeschlagenem Worker-Teardown zurückbleiben kann und dann in eigener Verantwortung zu bereinigen ist ([Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Security model](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes-security)).

Geändert:

- Die bisherigen Hinweise zu Anthropic-`self-hosted sandboxes` präzisiert: `read_only` schützt laut aktueller Dokumentation nur vor Rückschreiben in den zentralen Store, nicht zwingend vor lokalen Änderungen etwa über `bash`, Custom Tools oder eigene MCP-Server; Synchronisationskonflikte werden zugunsten des zentralen Stores aufgelöst ([Self-hosted sandboxes](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes), [Security model](https://platform.claude.com/docs/en/managed-agents/self-hosted-sandboxes-security)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.23.0 - 21.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `Apple Messages` in ChatGPT Work und Codex ergänzt: Auf Apple-Silicon-Macs kann das Plugin iMessage-, SMS- und RCS-Unterhaltungen lesen und durchsuchen sowie Nachrichten vorbereiten oder senden; standardmäßig ist vor dem Senden die Freigabe von Nachricht und Empfängern erforderlich, dauerhafte Sendefreigaben pro Chat sind aber möglich ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Plugins - ChatGPT Learn](https://developers.openai.com/codex/plugins)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu schreibgeschützten Codex-Snapshots ergänzt: Workspace-Links sind auf Mitglieder des Ursprungs-Workspaces begrenzt, Snapshots können laut OpenAI aber u. a. Nachrichten, Reasoning-Zusammenfassungen, Bilder, Dateipfade und Diffs enthalten; bekannte Secret-Muster werden redigiert, sensible Inhalte können dennoch verbleiben ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Use ChatGPT](https://developers.openai.com/codex/use-chatgpt)).

Geändert:

- Die bisherigen Hinweise zu `Computer History` korrigiert: Seit den Release Notes vom 20.08.2026 ist die Funktion für Business- bzw. Enterprise-Nutzer in der ChatGPT-macOS-App auch im EEA, im Vereinigten Königreich und in der Schweiz verfügbar; sie bleibt standardmäßig deaktiviert, erfordert `Memories`, eine Admin-Freigabe im Workspace und zusätzlich ein individuelles Opt-in ([ChatGPT Business - Release Notes](https://help.openai.com/en/articles/11391654-chatgpt-business-release-notes), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Computer History](https://developers.openai.com/codex/customization/computer-history)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.22.0 - 20.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `OpenAI Presence` ergänzt: OpenAI dokumentiert `Presence` als separates, gemanagtes Enterprise-Produkt für stark kontrollierte agentische Workflows mit Testing-, Guardrail-, Monitoring- und Human-Handoff-Funktionen; welche Daten zugänglich sind, geloggt, maskiert, gespeichert oder wie lange aufbewahrt werden, ist laut OpenAI deployment-spezifisch in Architektur, Security-Dokumentation und Vertrag zu prüfen ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [OpenAI Presence](https://help.openai.com/en/articles/20001405)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zur freiwilligen Migration persönlicher Claude-Konten in Team-/Enterprise-Organisationen ergänzt: Laut dem am 20.08.2026 verifizierten Help-Center-Stand können dabei u. a. Chats, Projekte, Dateien, Tasks, Projekt-Sync-Konfigurationen, Memory und Claude-Code-Einstellungen mitwandern, während z. B. Custom Skills, App-Logins, eigene Connectoren, öffentliche Share-Links, Cowork-Task-/Session-Historien, lokale Cowork-Daten und Claude-Code-Cloud-Sessions nicht migriert werden ([Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization)).

Geändert:

- Freigabe- und Governance-Hinweise präzisiert: Für OpenAI-Agentik ist jetzt ausdrücklich zwischen `Workspace Agents` innerhalb von ChatGPT und `OpenAI Presence` als separatem Deployment mit eigener Daten- und Logging-Architektur zu unterscheiden. Für Anthropic-Konto-Migrationen ist zusätzlich zum Domain-Claiming nun getrennt zu dokumentieren, welche Inhalte bei freiwilliger Migration in den Unternehmens-Workspace übergehen dürfen und welche vorher separat gesichert oder neu verbunden werden müssen ([OpenAI Presence](https://help.openai.com/en/articles/20001405), [Move your personal Claude account to a Team or Enterprise organization](https://support.claude.com/en/articles/9267400-move-your-personal-claude-account-to-a-team-or-enterprise-organization)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.21.0 - 18.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `Workspace analytics`, `Task insights`, `Personal Analytics plugin`, Audit-Logs im `Global Admin Console` und additiver RBAC-Logik ergänzt: Beim am 18.08.2026 verifizierten Stand dokumentiert OpenAI per-user usage metrics, CSV-Exporte, optionale Aufgabenkategorisierung, neue Audit-Log-Einsicht für Workspace-Owner/-Admins sowie Rollenlogik mit `Default`/`On`/`Off`, bei der ein explizites `Off` eine Berechtigung trotz anderer Rollen sperrt ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Workspace analytics for ChatGPT Enterprise and Edu](https://help.openai.com/en/articles/10875114-workspace-analytics-for-chatgpt-enterprise-and-edu), [Global Admin Console](https://help.openai.com/en/articles/12289294-global-admin-console), [Role Based Access Controls for ChatGPT Enterprise](https://help.openai.com/en/articles/11750701)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu `Claim and migrate accounts on your domain` ergänzt: Anthropic dokumentiert seit dem am 18.08.2026 verifizierten Help-Center-Stand ein Enterprise-Verfahren zum organisationsweiten Claiming und Migrieren privater Claude-Konten auf verifizierten Unternehmensdomains mit SSO-/JIT-/SCIM-Voraussetzungen, einmaligem 30-Tage-Migrationsfenster und Ausschluss einer Datenübernahme bei aktivierter HIPAA-readiness oder CMEK ([Claim and migrate accounts on your domain](https://support.claude.com/en/articles/14625619-claim-and-migrate-accounts-on-your-domain)).

Geändert:

- Freigabe- und Governance-Hinweise präzisiert: Für OpenAI-Analytics ist jetzt getrennt zu dokumentieren, wer Audit- oder Nutzungsdaten sehen darf, ob `Task insights` oder das `Personal Analytics plugin` aktiviert sind und dass bereits erzeugte aggregierte `Task insights`-Daten laut OpenAI bei späterem Abschalten derzeit nicht gelöscht werden. Für Anthropic-Domain-Claiming ist zusätzlich zu dokumentieren, ob alle betroffenen Nutzer vor Aktivierung im IdP sind, wie das 30-Tage-Fenster begleitet wird und ob nur `join fresh` statt Datenmigration zulässig ist ([Workspace analytics for ChatGPT Enterprise and Edu](https://help.openai.com/en/articles/10875114-workspace-analytics-for-chatgpt-enterprise-and-edu), [Claim and migrate accounts on your domain](https://support.claude.com/en/articles/14625619-claim-and-migrate-accounts-on-your-domain)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.20.0 - 17.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `ChatGPT workspace agents` und `app templates` ergänzt: Beim am 17.08.2026 verifizierten Stand der Enterprise-&-Edu-Release-Notes vom 28.05.2026 dokumentiert OpenAI rollenbezogene Veröffentlichungsrechte für Agents im gemeinsamen Workspace-Verzeichnis sowie templatebasierte Workspace-Apps für GitHub Enterprise, Snowflake und Databricks mit Konfigurationspunkten wie OAuth-Credentials, Webhooks, `managed MCP server URLs`, Rollenfreigaben und Action-Controls ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu Connector- und MCP-Governance ergänzt: Beim am 17.08.2026 verifizierten Help-Center-Stand beschreibt Anthropic technische Enterprise-Kontrollen, mit denen verifizierte Unternehmensdomains für bestimmte Connectoren auf Enterprise-Konten beschränkt, Connectoren per Identity-Provider zentral und rollenbezogen ausgerollt und Connector-Berechtigungen serverseitig über Claude-Web, Mobile, Cowork und Claude Code durchgesetzt werden können ([Restrict verified-domain connectors to your Enterprise](https://support.claude.com/en/articles/15402193-restrict-verified-domain-connectors-to-your-enterprise), [Authorize MCP connectors for your entire organization](https://support.claude.com/en/articles/15537633-authorize-mcp-connectors-for-your-entire-organization), [Set up role-based permissions on Enterprise plans](https://support.claude.com/en/articles/13930458-set-up-role-based-permissions-on-enterprise-plans), [Manage custom roles on Enterprise plans](https://support.claude.com/en/articles/13930452-manage-custom-roles-on-enterprise-plans)).

Geändert:

- Freigabe- und Governance-Hinweise präzisiert: Für OpenAI-Agentik ist jetzt getrennt zu dokumentieren, wer Agents veröffentlichen darf, welche App-Aktionen pro Agent zulässig sind und ob templatebasierte Apps mit Webhook-, Connector- oder `managed MCP`-Anbindung in die Workspace-Whitelist aufgenommen werden. Für Anthropic-Connectoren ist zusätzlich zu dokumentieren, ob persönliche Claude-Konten technisch von Unternehmens-Connectoren ausgeschlossen werden, welche Rollen Connectoren automatisch erhalten und wo lokale oder Drittplattform-Wege außerhalb der serverseitigen Connector-Steuerung verbleiben ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Restrict verified-domain connectors to your Enterprise](https://support.claude.com/en/articles/15402193-restrict-verified-domain-connectors-to-your-enterprise), [Authorize MCP connectors for your entire organization](https://support.claude.com/en/articles/15537633-authorize-mcp-connectors-for-your-entire-organization), [Manage custom roles on Enterprise plans](https://support.claude.com/en/articles/13930452-manage-custom-roles-on-enterprise-plans)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.19.0 - 15.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `ChatGPT search` ergänzt: Beim am 15.08.2026 verifizierten Help-Center-Stand beschreibt OpenAI `ChatGPT search` für Enterprise und Edu als gesondert steuerbare Web-Funktion, bei der disassoziierte Suchanfragen und gegebenenfalls strukturierte Prompt-Daten an Bing oder spezialisierte Datenanbieter gehen können; die IP-Adresse selbst wird laut OpenAI nicht geteilt, ein ungefährer Standort aus der IP kann aber weitergegeben werden ([ChatGPT search for Enterprise and Edu](https://help.openai.com/en/articles/10093903-chatgpt-search-for-enterprise-and-edu)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue Anthropic-Hinweise zu `Claude Tag` ergänzt: Beim am 15.08.2026 verifizierten Help-Center-Stand dokumentiert Anthropic die Slack-Integration als organisationsgebundene Identität mit kanal- und workspacebezogener Memory, Admin-Rechten zum Anzeigen/Bearbeiten/Löschen dieser Memory, getrennten Slack-/Claude-Historien und automatischer Löschung aus Claude innerhalb von 30 Tagen nach Trennung oder Deinstallation ([What is Claude Tag?](https://support.claude.com/en/articles/15594475-what-is-claude-tag)).

Geändert:

- Freigabe- und Governance-Hinweise präzisiert: Für `ChatGPT search` sind nun Workspace-/Rollenfreigaben, Bing-/Datenanbieter-Nutzung und die Weitergabe eines ungefähren Standorts aus der IP gesondert zu dokumentieren; für `Claude Tag` sind Kanal-/Rollenfreigaben, Organisationsidentität im Kanal, Direct-Message-Nutzung über persönliche Konten sowie die Abgrenzung zwischen Slack-Retention und Claude-Löschung getrennt festzuhalten ([ChatGPT search for Enterprise and Edu](https://help.openai.com/en/articles/10093903-chatgpt-search-for-enterprise-and-edu), [What is Claude Tag?](https://support.claude.com/en/articles/15594475-what-is-claude-tag)).

Entfernt:

- Keine Inhalte entfernt.

### Version 1.18.0 - 14.08.2026

Ergänzt:

- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `Computer History` ergänzt: OpenAI dokumentiert in den Enterprise-&-Edu-Release-Notes vom 13.08.2026 eine optionale macOS-Funktion für ChatGPT Enterprise, die Kontext aus ausgewählten Apps und Websites in ChatGPT und Codex einbringt und dabei laut OpenAI Interaktionsereignisse, aber keine Screenshots, Bildschirmaufnahmen, Mikrofoneingaben oder Systemaudio erfasst. Die Funktion ist standardmäßig deaktiviert, rollenbasiert freizugeben, erfordert zusätzlich ein Nutzer-Opt-in und ist derzeit laut OpenAI nicht im EEA, im Vereinigten Königreich oder in der Schweiz verfügbar ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes)).
- Checkliste, DSFA-Vorlage und KI-Richtlinie um neue OpenAI-Hinweise zu `Codex service accounts` und lokalen `access tokens` ergänzt: OpenAI beschreibt seit den Enterprise-&-Edu-Release-Notes vom 13.08.2026 dedizierte nicht-menschliche Workspace-Identitäten für CI-Runner und Scheduled Jobs. Die verifizierte OpenAI-Dokumentation trennt diese ausdrücklich von persönlichen Access Tokens und verweist auf getrennte Rollen-, Gruppen-, Plugin- und Token-Steuerung für vertrauenswürdige lokale Automatisierung ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Service accounts](https://learn.chatgpt.com/docs/enterprise/service-accounts), [Access tokens](https://learn.chatgpt.com/docs/enterprise/access-tokens)).

Geändert:

- Freigabe- und Governance-Hinweise präzisiert: Für OpenAI-Automatisierung ist jetzt getrennt zu dokumentieren, ob private Benutzerkonten, persönliche Access Tokens oder dedizierte Service Accounts genutzt werden; für `Computer History` sind Rollenfreigabe, App-/Site-Auswahl, Nutzer-Opt-in und interne Transparenz gesondert festzuhalten ([ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Service accounts](https://learn.chatgpt.com/docs/enterprise/service-accounts), [Access tokens](https://learn.chatgpt.com/docs/enterprise/access-tokens)).

Entfernt:

- Keine Inhalte entfernt.

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
