# KI-Richtlinie für die KI-Nutzung

Stand: 05.07.2026
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

Praxis-Hinweis: Zentrale Business-Accounts für Firmen-Tools, AVV/DPA, Zero Data Retention und klare Nutzungsregeln sind Kernanforderungen. Bei privaten MCP-Servern ist eine enge Tunnel-/Allowlist-Architektur statt öffentlicher Freigaben oder unnötig breiter Netzverbindungen zu bevorzugen.

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels).

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
- automatische Aktionen wie Senden, Speichern, Löschen, Kaufen, Buchen oder Verändern von Daten
- Computer Use oder vergleichbare UI-Steuerung, bei der Screenshots, Browserinhalte oder Desktop-Oberflächen verarbeitet werden

Mindestanforderungen:

- Least-Privilege-Zugriff
- Testumgebung vor Produktivzugriff
- keine autonomen Aktionen ohne Freigabe
- Protokollierung
- Prompt-Injection-Schutz
- für Konnektoren und MCP-Server Retention/Residency jedes Drittservers separat prüfen
- für private MCP-Server nach Möglichkeit outbound-only-Tunnel oder gleichwertig enge Anbindung; keine unnötigen öffentlichen Endpunkte oder breiten VPN-/Peering-Freigaben
- Chat-Suche/Memory nur nach dokumentierter Freigabe; Retention, Export und Admin-Kontrollen prüfen
- klare Abbruch- und Kontrollmechanismen
- DSFA-Prüfung bei personenbezogenen Daten

Praxis-Hinweis: Cowork-, Computer-Use- und Browserzugriffe auf lokale Daten, Screenshots, Webseiten und Dienste wie Slack können zu ungewollter Datenübertragung führen und müssen separat freigegeben werden. OpenAI beschreibt Computer Use als UI-operierende Modellfunktion; Anthropic kennzeichnet Computer Use als Beta-Funktion mit besonderen Sicherheitsrisiken, insbesondere bei Internetzugriff. Für private MCP-Server beschreibt OpenAI seit Juni 2026 mit dem Secure MCP Tunnel eine kundenseitig betriebene outbound-only-Anbindung, bei der die private Serveradresse intern bleibt; das ersetzt aber nicht die Prüfung von Drittservern, Rollen, Zielbegrenzungen und Logging.

Quellen: [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use), [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context).

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
- featurebezogene Retention, z. B. Background Mode, Extended Prompt Caching, Hosted Containers, Message Batches, Audit Logs oder Vector Stores

Freigabe erfolgt durch:

| Rolle | Freigabe erforderlich? |
|---|---:|
| Fachbereich | Ja |
| Datenschutz | Ja |
| Informationssicherheit | Ja |
| Rechtsabteilung / externe Beratung | bei hohem Risiko |
| Geschäftsführung / Leitung | bei hohem Risiko |

Quellen: [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs).

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

Quellen: [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [Guidelines for providers and deployers of AI high-risk systems](https://digital-strategy.ec.europa.eu/en/policies/guidelines-ai-high-risk-systems), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content).

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
- Aktivierung von Chat-Suche/Memory, Projektwissen, Konnektoren oder MCP
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
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Secure MCP Tunnel](https://developers.openai.com/api/docs/guides/secure-mcp-tunnels)
- [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use)
- [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)
- [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context)
- [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans)
- [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs)
- [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing)
- [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en)
