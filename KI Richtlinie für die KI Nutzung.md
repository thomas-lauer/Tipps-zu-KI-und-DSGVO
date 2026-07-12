# KI-Richtlinie für die KI-Nutzung

Stand: 12.07.2026
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

## 3. Zugelassene Tools

KI-Tools dürfen nur genutzt werden, wenn sie auf der Tool-Whitelist stehen.

| Tool | Erlaubter Plan | Erlaubte Zwecke | Personenbezogene Daten erlaubt? | Auflagen |
|---|---|---|---:|---|
| OpenAI / ChatGPT | Business / Enterprise / API |  | Ja / Nein / eingeschränkt | DPA, Training aus, Retention geregelt |
| Claude / Anthropic | Enterprise / Team / API |  | Ja / Nein / eingeschränkt | DPA, Retention geregelt |
| Internes RAG |  |  | Ja / Nein / eingeschränkt | Berechtigungen, Quellen, Logging |
| Sonstige |  |  |  |  |

Private Accounts dürfen nicht für Unternehmensdaten verwendet werden.

Zusätzliche Funktionen wie Chat-Suche, Memory, Projektwissen, Konnektoren oder lokale Datei-/Browserzugriffe gelten als gesondert freigabepflichtige Features.

Öffentlich zugängliche Webquellen oder bereits gescrapte Datensätze für Training, Fine-Tuning oder externe Wissensbestände gelten ebenfalls als gesondert freigabepflichtig. Der Umstand, dass Daten öffentlich erreichbar sind, ersetzt weder Rechtsgrundlage noch Transparenz- und Art.-9-Prüfung ([Guidelines on web scraping](https://www.edpb.europa.eu/public-consultations/guidelines-on-web-scraping_en), [EDPB News, 08.07.2026](https://www.edpb.europa.eu/news/edpb-sheds-light-on-anonymisation-and-web-scraping-for-generative-ai-and-adopts-final-version_en)).

Für Claude Cowork ist zusätzlich zu beachten, dass Anthropic seit dem 07.07.2026 Remote-Sessions auf Web und Mobile dokumentiert: Die Arbeit läuft serverseitig auf Anthropic-Servern, Sitzungen und Dateien liegen im Claude-Account und lokale Dateien oder Browserfunktionen werden nur über die geöffnete Claude-Desktop-App und freigegebene Ordner erreicht ([Anthropic Release notes, 07.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely)).

Für Anthropic Managed Agents ist zusätzlich zu beachten, dass Anthropic seit dem 10.07.2026 geplante `scheduled deployments` dokumentiert, die Sessions autonom per Cron starten können. Dabei können Dateien, GitHub-Zugänge, Memory Stores und Vaults eingebunden werden; für `environment_variable`-Vault-Credentials wird der Secret-Wert laut Anthropic dem Agenten nicht offengelegt, sondern erst beim ausgehenden Request eingesetzt. Solche Funktionen gelten als gesondert freigabepflichtig ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview)).

Für Anthropic Enterprise ist zusätzlich zu beachten, dass laut Release Notes seit dem 01.07.2026 organisations- und rollenbezogene Modellfreigaben mit Effort-Caps als Beta dokumentiert sind. Diese Funktion sollte genutzt werden, um nur freigegebene Modelle technisch bereitzustellen; bei `covered models` oder anderen Modellen mit abweichender Retention reicht ein bloßes Richtlinienverbot nicht aus ([Release notes, 01.07.2026](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization)).

Zusätzlich ist zu beachten, dass Anthropic laut aktueller Herstellerdokumentation `individual usage analytics` für Team- und Enterprise-Organisationen ab dem 11.07.2026 standardmäßig aktiviert. Nutzerbezogene Auswertungen nach Produkt, Modell und Skill dürfen nur mit dokumentiertem Zweck, klaren Sichtrechten und interner Transparenz genutzt werden; falls das nicht gewollt ist, muss die Option organisatorisch geprüft und gegebenenfalls deaktiviert werden ([View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans)).

Praxis-Hinweis: Zentrale Business-Accounts für Firmen-Tools, AVV/DPA, Zero Data Retention und klare Nutzungsregeln sind Kernanforderungen. Bei privaten MCP-Servern ist eine enge Tunnel-/Allowlist-Architektur statt öffentlicher Freigaben oder unnötig breiter Netzverbindungen zu bevorzugen.

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic Release notes](https://support.claude.com/en/articles/12138966-release-notes), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

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
- bei Claude Cowork Remote-Sessions, gespeicherte Sitzungen/Dateien, geplante Tasks und erreichbare lokale Ordner separat freigeben und dokumentieren
- Microsoft-365-Connector-`write tools` nur nach Admin-Freigabe und enger Zweckbegrenzung aktivieren
- Anthropic-Managed-Agents mit `scheduled deployments`, Vaults oder GitHub-/Dateianbindung nur nach separater Freigabe, enger Zeitplan- und Secret-Begrenzung sowie dokumentierter Run-Historie einsetzen
- bei Anthropic Enterprise Modell-Allowlist und Effort-Caps so setzen, dass nicht freigegebene oder retention-pflichtige Modelle technisch begrenzt sind
- nutzerbezogene KI-Analytics nur mit dokumentiertem Zweck, enger Sichtberechtigung und interner Transparenz aktiv lassen
- für private MCP-Server nach Möglichkeit outbound-only-Tunnel oder gleichwertig enge Anbindung; keine unnötigen öffentlichen Endpunkte oder breiten VPN-/Peering-Freigaben
- Chat-Suche/Memory nur nach dokumentierter Freigabe; Retention, Export und Admin-Kontrollen prüfen
- klare Abbruch- und Kontrollmechanismen
- DSFA-Prüfung bei personenbezogenen Daten

Praxis-Hinweis: Cowork-, Computer-Use- und Browserzugriffe auf lokale Daten, Screenshots, Webseiten und Dienste wie Slack können zu ungewollter Datenübertragung führen und müssen separat freigegeben werden. OpenAI beschreibt Computer Use als UI-operierende Modellfunktion; Anthropic kennzeichnet Computer Use als Beta-Funktion mit besonderen Sicherheitsrisiken, insbesondere bei Internetzugriff. Neu dokumentiert ist zudem, dass Cowork auf Web und Mobile als Remote-Session auf Anthropic-Servern läuft und Aufgaben ohne online Gerät weiterlaufen können. Für den Claude-Microsoft-365-Connector gilt zusätzlich: Wenn `write tools` aktiviert sind, kann Claude E-Mails senden und organisieren, Kalenderereignisse erstellen, aktualisieren oder löschen sowie Dateien in OneDrive und SharePoint erstellen oder aktualisieren; Teams bleibt read-only, und gesendete E-Mails tragen laut Anthropic einen agent-initiated-Header ([Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide)). Für Anthropic Managed Agents kommt hinzu, dass `scheduled deployments` Sessions autonom starten können und Vault-Credentials in ausgehende Requests eingebracht werden können; deshalb sind Zeitpläne, Deployment-Runs/Webhooks, Pause-/Archivierungsrechte und Secret-Scopes getrennt freizugeben und zu dokumentieren ([Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview)). Für private MCP-Server beschreibt OpenAI seit Juni 2026 mit dem Secure MCP Tunnel eine kundenseitig betriebene outbound-only-Anbindung, bei der die private Serveradresse intern bleibt; das ersetzt aber nicht die Prüfung von Drittservern, Rollen, Zielbegrenzungen und Logging.

Wenn Claude Code, Cowork oder Cloud-Zugänge mit ZDR betrieben werden, ist zusätzlich modellbezogen zu prüfen, ob Anthropic für das gewünschte Modell eine Retention-Pflicht vorgibt. Anthropic dokumentiert für `covered models` bzw. Mythos-class-Modelle eine 30-Tage-Retention; Claude Fable 5 ist laut Migration Guide nicht unter Zero Data Retention verfügbar. Für solche Modelle kann ein getrenntes Workspace-, Subscription- oder Sandbox-Setup mit aktivierter Retention erforderlich sein.

Quellen: [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use), [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile), [Use Claude Cowork safely](https://support.claude.com/en/articles/13364135-use-claude-cowork-safely), [Connect to Microsoft 365](https://support.claude.com/en/articles/15183774-connect-to-microsoft-365), [Microsoft 365 connector security guide](https://support.claude.com/en/articles/12684923-microsoft-365-connector-security-guide), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

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
- Anbindungsarchitektur für private MCP-Server oder REST-Ziele: öffentliche Freigabe, VPN/Peering oder enge Tunnel-Lösung; Begründung und Freigabe dokumentieren
- featurebezogene Retention, z. B. Background Mode, standardmäßiges Extended Prompt Caching ohne ZDR, Hosted Containers, Message Batches, Audit Logs oder Vector Stores
- autonome Agentik-Orchestrierung, z. B. Anthropic-`scheduled deployments`, Deployment-Run-Historie/Webhooks sowie Dateien-, GitHub-, Memory- und Vault-Einbindung
- modellbezogene Retention-Ausnahmen, z. B. Anthropic-`covered models` oder Claude Fable 5 mit 30-Tage-Retention statt ZDR, sowie ein ggf. erforderliches separates Workspace-, Subscription- oder Sandbox-Setup
- organisations- oder rollenbezogene Modell-Allowlist und Effort-Caps, soweit der Anbieter dies unterstützt
- nutzerbezogene Usage-Analytics, Reports oder ähnliche Admin-Auswertungen: Zweck, Sichtberechtigungen und interne Transparenz prüfen
- Nutzung öffentlich zugänglicher Webquellen, gescrapter Datensätze oder Datenbroker-Datensätze: getrennte Prüfung von Rechtsgrundlage, Transparenz, Quellenauswahl, Widerspruchs-/robots.txt-Behandlung, Datenminimierung, Validierung und Art.-9-Ausnahmen
- dokumentierte Anonymisierungsbewertung statt bloßer Annahme, dass entfernte Identifikatoren genügen

Praxis-Hinweis: Bei OpenAI-API-Integrationen ist nicht nur zu prüfen, ob Extended Prompt Caching theoretisch genutzt werden könnte. Laut aktueller OpenAI-Datendokumentation verwenden Organisationen ohne Zero Data Retention bei allen unterstützten Modellen standardmäßig Extended Prompt Caching; bei `gpt-5.5`, `gpt-5.5-pro` und künftigen Modellen ist `prompt_cache_retention=in_memory` nicht zulässig. Diese Default-Logik ist im Freigabe- und Löschkonzept ausdrücklich zu dokumentieren.

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

Quellen: [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Help Center: Data retention practices for Mythos-class models](https://support.claude.com/en/articles/15425996-data-retention-practices-for-mythos-class-models), [Anthropic Migration Guide](https://platform.claude.com/docs/en/about-claude/models/migration-guide), [Manage model access for your organization](https://support.claude.com/en/articles/15694740-manage-model-access-for-your-organization), [View usage analytics for Team and Enterprise plans](https://support.claude.com/en/articles/12883420-view-usage-analytics-for-team-and-enterprise-plans), [Scheduled deployments](https://platform.claude.com/docs/en/managed-agents/scheduled-deployments), [Authenticate with vaults](https://platform.claude.com/docs/en/managed-agents/vaults), [Claude Platform Release Notes, 10.07.2026](https://platform.claude.com/docs/en/release-notes/overview).

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

Zusatzhinweis zum AI Act: Die KI-VO ist seit 1. August 2024 in Kraft. Nach [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113) gilt sie grundsätzlich ab dem 2. August 2026; Kapitel I und II gelten seit dem 2. Februar 2025, bestimmte GPAI-, Governance- und Sanktionsregeln seit dem 2. August 2025. Für Hochrisiko-KI verweist die aktuelle Kommissionsdarstellung vom 01.07.2026 auf einen differenzierten Zeitplan: bestimmte Hochrisikobereiche sollen ab dem 02.12.2027, in Produkte integrierte Systeme z. B. Robotik oder Industriemaschinen ab dem 02.08.2028 greifen. Die zugrunde liegenden Leitlinien sind nicht rechtsverbindlich, spiegeln aber die Auslegung der Kommission wider und sollen die Durchsetzung leiten. Nach [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50) müssen u. a. direkte Interaktion mit KI-Systemen, bestimmte KI-generierte oder manipulierte Inhalte, Deepfakes sowie Emotionserkennungs- oder biometrische Kategorisierungssysteme transparent gemacht werden; Ausnahmen und Detailpflichten sind einzelfallbezogen zu prüfen. Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde am 10.06.2026 veröffentlicht. Er ist freiwillig, die gesetzlichen Transparenzpflichten gelten dennoch ab dem 02.08.2026.

Neu zu berücksichtigen ist, dass die EU-Kommission den Code am 09.07.2026 als angemessenes freiwilliges Instrument zur Erleichterung der Umsetzung von Art. 50 Abs. 2, 4 und 5 KI-VO bewertet hat und der AI Board die Angemessenheitsbewertung am Folgetag übernommen hat. Wenn die Organisation den Code als Nachweisbaustein nutzen will, sollte der Signaturstatus dokumentiert und den konkreten Transparenzmaßnahmen zugeordnet werden. Laut Kommission ersetzt die Zeichnung des Codes weder die konkrete Pflichtenumsetzung noch einen abschließenden Compliance-Nachweis ([Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)).

Neu zu berücksichtigen ist außerdem der FAQ-Stand des AI Office vom 09.07.2026: Für die erste Signatory-Liste vor dem 02.08.2026 müssen Signaturformulare bis zum 22.07.2026, 18:00 CEST eingereicht werden. Eine spätere Unterzeichnung bleibt möglich; wenn die Organisation nicht unterzeichnet, sollte sie ihre alternativen Maßnahmen zur Markierung, Erkennung und Kennzeichnung nach Art. 50 KI-VO besonders belastbar dokumentieren ([Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content)).

Quellen: [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content), [Signing the Code of Practice on transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/faqs/signing-code-practice-transparency-ai-generated-content).

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

Quelle: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4).

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
- [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems)
- [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)
- [Commission Opinion on the assessment of the Code of Practice on Transparency of AI-generated content](https://digital-strategy.ec.europa.eu/en/library/commission-opinion-assessment-code-practice-transparency-ai-generated-content)
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels)
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
