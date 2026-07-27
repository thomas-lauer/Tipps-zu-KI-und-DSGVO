# Datenschutz-Folgenabschätzung (DSFA) - Vorlage für KI-Nutzung

Stand: 27.07.2026
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
- Werden Anthropic Managed Agents mit `scheduled deployments`, Dateien, GitHub-Zugängen, Memory Stores oder Vault-Credentials genutzt, die Sessions autonom per Cron starten können ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults))?
- Werden beim Claude-Microsoft-365-Connector `write tools` genutzt, also E-Mail-Versand/-Organisation, Kalenderänderungen oder Schreibzugriffe in OneDrive/SharePoint; Teams bleibt dabei read-only ([Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide))?
- Werden bei Anthropic `custom connectors` über remote MCP genutzt, und ist dokumentiert, dass die Verbindung zum MCP-Server von Anthropic-Servern statt vom lokalen Gerät ausgeht ([Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))?
- Ist bei Claude Cowork dokumentiert, ob für Remote-Sessions `network-access policy`, Trusted Devices, restriktives Approval-Verhalten sowie ggf. MDM-Sperren für lokale MCP-Server oder Desktop Extensions gesetzt sind ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control))?
- Ist bekannt und bewertet, dass Cowork-Aktivität derzeit nicht in Audit Logs, Compliance API oder Data Exports erscheint und hostbasierte EDR-Werkzeuge die Remote-VM nicht überwachen können ([Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview))?
- Ist bei Microsoft 365 `write tools` dokumentiert, ob der Tenant den erweiterten Microsoft-Graph-Berechtigungen erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen, Datei- und Kalender-Schreibvorgänge aber nicht ([Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector))?
- Werden private MCP-Server angebunden und bleibt deren Adresse intern, z. B. über eine outbound-only-Tunnelarchitektur statt über einen öffentlichen Endpoint?
- Werden OpenAI-Funktionen mit eigener Retention genutzt, z. B. Responses API mit `store`, Background Mode, Extended Prompt Caching, Hosted Shell, Code Interpreter, gehostete Skills, Assistants, Threads oder Vector Stores?
- Werden Anthropic-Funktionen mit eigener Retention genutzt, z. B. Claude Enterprise-Projekte, Audit Logs, Message Batches, `covered models` wie Claude Fable 5 oder API-Features ohne ZDR?
- Werden bei Anthropic Team oder Enterprise `individual usage analytics` genutzt oder nach dem Default-Wechsel ab dem 11.07.2026 bewusst deaktiviert, und ist dokumentiert, wer nutzerbezogene Nutzungsdaten nach Produkt, Modell und Skill sehen darf ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans))?
- Wird bei Anthropic Enterprise eine organisations- oder rollenbezogene Modell-Allowlist mit Effort-Caps genutzt, damit nur freigegebene Modelle auswählbar sind ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization))?
- Werden öffentlich zugängliche Webquellen oder bereits gescrapte Datensätze für Training, Fine-Tuning oder externe Wissensbestände genutzt, und ist deren Rechtsgrundlage gesondert dokumentiert ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en))?

Praxis-Hinweis: Zentrale Business-Accounts, AVV/DPA, Zero Data Retention, DSFA, dokumentierte Feature-Freigaben für Memory/Chat-Suche, Konnektoren und private MCP-Tunnelarchitekturen sowie eine interne Richtlinie sind Mindestbausteine vor produktiver Nutzung. Bei Claude Cowork sollten Remote-Sessions, gespeicherte Dateien/Sitzungen und erreichbare lokale Ordner getrennt freigegeben werden; bei Microsoft-365-Connectoren gilt das zusätzlich für aktivierte Schreibwerkzeuge. Werden Anthropic Managed Agents genutzt, sollten zusätzlich Zeitpläne, Deployment-Runs/Webhooks, eingebundene Vaults und Secret-Scopes freigegeben und dokumentiert werden. Für Anthropic Team und Enterprise sollte außerdem festgehalten werden, ob nutzerbezogene Usage-Analytics aktiv sind oder bewusst deaktiviert wurden. Für Anthropic Enterprise kann die Modellfreigabe inzwischen organisations- und rollenbezogen technisch erzwungen werden; das sollte für retention-pflichtige oder sonst nicht freigegebene Modelle genutzt und dokumentiert werden. Bei Anthropic-`custom connectors` über remote MCP ist zusätzlich zu dokumentieren, dass die Verbindung aus Anthropic-Cloud-Infrastruktur statt vom lokalen Gerät erfolgt. Bei Cowork sollte festgehalten werden, ob verfügbare Organisationskontrollen wie `network-access policy`, Trusted Devices und restriktives Approval-Verhalten aktiv sind und wie die fehlende Sichtbarkeit in Audit Logs, Compliance API und Data Exports kompensiert wird. Beim Microsoft-365-Connector sollte außerdem dokumentiert werden, ob der Tenant den erweiterten Graph-Scopes erneut zugestimmt hat und dass derzeit nur E-Mails einen `agent-initiated`-Header tragen. Als "anonymisiert" deklarierte Daten sollten erst nach dokumentierter Re-Identifikationsprüfung freigegeben werden; nach den neuen EDPB-Entwurfsleitlinien sind dafür insbesondere `No Record Isolation`, `No Linkage` und `No Inference` zu prüfen ([Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Guidelines on anonymisation](https://www.edpb.europa.eu/public-consultations/guidelines-on-anonymisation_en), [Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

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
| Fehlende Cowork-Sichtbarkeit in Audit Logs / Compliance API / Data Exports bewertet |  |
| Anthropic-Managed-Agents mit `scheduled deployments`, Deployment-Runs/Webhooks und Lifecycle-Rechten bewertet |  |
| Anthropic-Vaults und Secret-Scopes für MCP- oder `environment_variable`-Credentials dokumentiert |  |
| Microsoft-365-Connector-`write tools` separat freigegeben und begrenzt |  |
| Microsoft-365-`write tools`: Tenant-Re-Consent und fehlende Tagging-Abdeckung für Datei-/Kalenderwrites dokumentiert |  |
| Private MCP-Server/Tunnelarchitektur mit Ziel- und Rollenbegrenzung dokumentiert |  |
| OpenAI-Sync-Apps: Indexierung, Residency-Region und US-Azure-Fallback bewertet |  |
| OpenAI-App-Unterhaltungen/App-Calls in Compliance API bzw. Compliance Logs berücksichtigt |  |
| Datenresidenz | EU / USA / global / offen |
| SCC/DPF/TIA geprüft |  |
| Training/Model Improvement deaktiviert |  |
| Zero Data Retention verfügbar und aktiv |  |
| API-spezifische Speicherlogik (z. B. Responses API / Background Mode) geprüft |  |
| Default-Retention ohne ZDR, insbesondere Extended Prompt Caching bei unterstützten OpenAI-Modellen, dokumentiert |  |
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

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Apps in ChatGPT](https://help.openai.com/en/articles/11487775-connectors-in-chatgpt), [Admin controls, security, and compliance for plugins and apps](https://help.openai.com/en/articles/11509118-admin-controls-security-and-compliance-for-plugins-and-apps), [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt), [ChatGPT Enterprise & Edu - Release Notes](https://help.openai.com/en/articles/10128477-chatgpt-enterprise-edu-release-notes), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Claude Cowork architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-architecture-overview), [Continue local sessions from any device with Remote Control](https://code.claude.com/docs/en/remote-control), [Get started with custom connectors using remote MCP](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Set up the Microsoft 365 connector](https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide).

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
| Direkte Interaktion mit Chatbots/Agenten/Avataren ab erster Interaktion kenntlich gemacht, sofern nicht ausnahmsweise offensichtlich |  |
| Für Art. 50 Abs. 2 ist dokumentiert, ob eine enge Ausnahme greift z. B. Quellcode, reine Maschine-zu-Maschine-Outputs, geschlossene Entwicklungsumgebung oder Standard-Editing |  |
| Für veröffentlichte KI-Texte zu Fragen von öffentlichem Interesse ist dokumentiert, ob echte Human Review oder redaktionelle Verantwortung vorliegt; bloße Rechtschreib-/Grammatikkorrektur reicht nicht |  |
| Gewählte Labels oder EU-Icons nur als Hilfsmittel bewertet; materielle Art.-50-Anforderungen und Platzierung separat geprüft |  |
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

Neu zu berücksichtigen ist außerdem die allgemeine Kommissions-FAQ vom 22.07.2026 zum AI Act: Für Hochrisiko-KI muss die DSFA bzw. die damit verknüpfte KI-VO-Dokumentation festhalten, wie `instructions of use`, laufendes Monitoring, menschliche Aufsicht und die Prüfung der Relevanz bzw. hinreichenden Repräsentativität selbst bereitgestellter Eingabedaten umgesetzt werden. Öffentliche Stellen und private Anbieter öffentlicher Dienste müssen vor der ersten Nutzung grundsätzlich eine Grundrechte-Folgenabschätzung dokumentieren. Wenn der Output eines Hochrisiko-Systems für eine Entscheidung über eine natürliche Person mit Rechtswirkung genutzt wird, sollte die DSFA außerdem festhalten, wie das Recht auf Erklärung operativ erfüllt werden kann ([Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act)).

Quellen: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4), [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [Regulation (EU) 2026/1744](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ%3AL_202601744), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Guidelines on transparency obligations for providers and deployers of AI systems](https://digital-strategy.ec.europa.eu/en/library/guidelines-transparency-obligations-providers-and-deployers-ai-systems), [Transparency obligations under Article 50 of the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/transparency-obligations-under-article-50-ai-act), [EU Icons for labelling AI-generated content](https://digital-strategy.ec.europa.eu/en/policies/eu-icons-labelling-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content), [Navigating the AI Act](https://digital-strategy.ec.europa.eu/en/faqs/navigating-ai-act).

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
