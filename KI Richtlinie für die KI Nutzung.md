# KI-Richtlinie fuer die KI-Nutzung

Stand: 18.06.2026
Status: Vorlage fuer Unternehmen/Organisationen

> Ziel dieser Richtlinie ist eine produktive, sichere und DSGVO-konforme Nutzung von KI-Systemen wie Claude.ai, OpenAI/ChatGPT, API-Diensten, RAG-Systemen und vergleichbaren Tools. Diese Vorlage muss an Organisation, Rollen, Tools und Rechtsgrundlagen angepasst werden.

Quellen: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [DSK KI-Systeme TOM](https://datenschutzkonferenz-online.de/media/oh/DSK-OH_KI-Systeme.pdf), [DSK RAG](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf), [DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113).

## 1. Geltungsbereich

Diese Richtlinie gilt fuer alle Beschaeftigten, freien Mitarbeitenden, Dienstleister und sonstigen Personen, die im Auftrag der Organisation KI-Systeme nutzen.

Sie gilt insbesondere fuer:

- Chatbots und Assistenten, z. B. ChatGPT, Claude, Copilot oder vergleichbare Systeme
- API-basierte KI-Dienste
- KI-Funktionen in Fachanwendungen
- RAG-Systeme und interne Wissensassistenten
- Bild-, Audio-, Video- und Codegeneratoren
- agentische Funktionen wie Computer Use, Cowork, Browsersteuerung, Datei-, E-Mail-, Kalender-, Slack- oder Teams-Zugriffe

## 2. Grundsatz

KI darf nur so genutzt werden, dass Datenschutz, Informationssicherheit, Vertraulichkeit, Urheberrechte, Berufsgeheimnisse, Betriebsgeheimnisse und interne Compliance-Vorgaben eingehalten werden.

AI Act und DSGVO muessen gleichzeitig beachtet werden. Die Einhaltung einer KI-Verordnungspflicht ersetzt keine DSGVO-Pruefung.

Fuer jeden KI-Use-Case ist zusaetzlich zur DSGVO-Pruefung die KI-VO-Einstufung zu dokumentieren: verbotene KI-Praktik, Hochrisiko-KI, begrenztes Risiko mit Transparenzpflichten oder minimales Risiko. Verbotene Praktiken sind nach [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5) unzulaessig; Hochrisiko-Einstufungen sind nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) zu pruefen; Transparenzpflichten fuer bestimmte KI-Systeme ergeben sich aus [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50).

## 3. Zugelassene Tools

KI-Tools duerfen nur genutzt werden, wenn sie auf der Tool-Whitelist stehen.

| Tool | Erlaubter Plan | Erlaubte Zwecke | Personenbezogene Daten erlaubt? | Auflagen |
|---|---|---|---:|---|
| OpenAI / ChatGPT | Business / Enterprise / API |  | Ja / Nein / eingeschraenkt | DPA, Training aus, Retention geregelt |
| Claude / Anthropic | Enterprise / Team / API |  | Ja / Nein / eingeschraenkt | DPA, Retention geregelt |
| Internes RAG |  |  | Ja / Nein / eingeschraenkt | Berechtigungen, Quellen, Logging |
| Sonstige |  |  |  |  |

Private Accounts duerfen nicht fuer Unternehmensdaten verwendet werden.

Zusaetzliche Funktionen wie Chat-Suche, Memory, Projektwissen, Konnektoren oder lokale Datei-/Browserzugriffe gelten als gesondert freigabepflichtige Features.

Praxis-Hinweis: Zentrale Business-Accounts fuer Firmen-Tools, AVV/DPA, Zero Data Retention und klare Nutzungsregeln sind Kernanforderungen.

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp).

## 4. Verbotene Eingaben

In nicht freigegebene KI-Systeme duerfen nicht eingegeben werden:

- Namen, E-Mail-Adressen, Telefonnummern, Kundennummern oder sonstige Identifikatoren
- Kundendaten
- Mitarbeiterdaten
- Bewerberdaten
- Gesundheitsdaten
- biometrische Daten
- Daten von Kindern/Jugendlichen
- Mandanten-, Patienten-, Steuer-, Rechtsberatungs- oder Berufsgeheimnisse
- Passwoerter, API-Keys, Tokens, Zugangsdaten
- vertrauliche Vertrage, Strategien, Finanzdaten oder Betriebsgeheimnisse
- Daten, die einer besonderen Geheimhaltungspflicht unterliegen

Ausnahme: Die Verarbeitung wurde fuer den konkreten Use Case freigegeben, ein AVV/DPA liegt vor, Datenminimierung ist umgesetzt und die DSFA-/Rechtspruefung ist abgeschlossen, sofern erforderlich.

## 5. Erlaubte Standardnutzungen

Ohne personenbezogene oder vertrauliche Daten sind in der Regel erlaubt:

- Formulierung allgemeiner Texte
- Ideenfindung
- Strukturierung nicht vertraulicher Inhalte
- Erstellen allgemeiner Checklisten
- Uebersetzen oder Vereinfachen anonymisierter Texte
- Codebeispiele ohne Geheimnisse, Zugangsdaten oder produktive Daten
- Zusammenfassung oeffentlicher Informationen mit Quellenpruefung

## 6. Eingaberegeln

Vor jeder Eingabe pruefen:

1. Ist die Information personenbezogen?
2. Ist sie vertraulich?
3. Ist sie fuer den Zweck wirklich erforderlich?
4. Kann sie anonymisiert oder pseudonymisiert werden?
5. Ist das Tool fuer diese Datenart freigegeben?
6. Ist Training/Model Improvement deaktiviert oder ausgeschlossen?
7. Gilt eine passende Retention?

Beispiele:

- Statt "Max Mueller, Kunde 12345, mahnt Rechnung an" schreiben: "Kunde A mahnt eine Rechnung an".
- Statt vollstaendiger Vertragsdatei nur die relevante anonymisierte Klausel eingeben.
- Statt Mitarbeiterbewertung keine KI-Einschaetzung ueber Leistung, Verhalten oder Zukunftsentscheidungen erzeugen lassen.

## 7. Output-Regeln

KI-Ausgaben muessen geprueft werden, bevor sie verwendet werden.

Pflichten:

- fachliche Pruefung
- Quellenpruefung bei Tatsachenbehauptungen
- Pruefung auf personenbezogene Falschinformationen
- Pruefung auf Diskriminierung
- Pruefung auf Halluzinationen
- keine ungepruefte Uebernahme in Kunden-, HR-, Rechts- oder Finanzprozesse

## 8. Keine automatisierte Letztentscheidung

KI darf nicht allein ueber Personen entscheiden. Verboten ohne gesonderte Rechts- und Datenschutzfreigabe sind insbesondere:

- Bewerberauswahl
- Mitarbeiterbewertung
- Kuendigungsempfehlungen
- Bonitaetsentscheidungen
- Versicherungsentscheidungen
- Gesundheits- oder Risikobewertungen
- Sperrung, Sanktionierung oder Ablehnung von Leistungen

Quelle: [Art. 22 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en).

## 9. Agentische KI und Cowork/Computer Use

Agentische Funktionen haben ein hoeheres Risiko als reine Chat-Nutzung, weil sie auf lokale Daten, Browser, Dienste, Dateien oder Kommunikationskanaele zugreifen koennen.

Nur mit separater Freigabe erlaubt:

- Computer Use
- Cowork
- Browsersteuerung
- Zugriff auf lokale Dateien
- Zugriff auf Slack, Teams, E-Mail, Kalender, CRM, ERP, Ticketsysteme
- automatische Aktionen wie Senden, Speichern, Loeschen, Kaufen, Buchen oder Veraendern von Daten
- Computer Use oder vergleichbare UI-Steuerung, bei der Screenshots, Browserinhalte oder Desktop-Oberflaechen verarbeitet werden

Mindestanforderungen:

- Least-Privilege-Zugriff
- Testumgebung vor Produktivzugriff
- keine autonomen Aktionen ohne Freigabe
- Protokollierung
- Prompt-Injection-Schutz
- fuer Konnektoren und MCP-Server Retention/Residency jedes Drittservers separat pruefen
- Chat-Suche/Memory nur nach dokumentierter Freigabe; Retention, Export und Admin-Kontrollen pruefen
- klare Abbruch- und Kontrollmechanismen
- DSFA-Pruefung bei personenbezogenen Daten

Praxis-Hinweis: Cowork-, Computer-Use- und Browserzugriffe auf lokale Daten, Screenshots, Webseiten und Dienste wie Slack koennen zu ungewollter Datenuebertragung fuehren und muessen separat freigegeben werden. OpenAI beschreibt Computer Use als UI-operierende Modellfunktion; Anthropic kennzeichnet Computer Use als Beta-Funktion mit besonderen Sicherheitsrisiken, insbesondere bei Internetzugriff.

Quellen: [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use), [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context).

## 10. RAG und interne Wissenssysteme

RAG-Systeme duerfen nur freigegebene Quellen verwenden.

Pflichten:

- Berechtigungen aus Quellsystemen uebernehmen
- keine Indexierung ohne Rechtsgrundlage
- Loeschung aus Quelle muss auch im Index beruecksichtigt werden
- Quellen in Antworten anzeigen, soweit moeglich
- Prompt-Injection pruefen
- vertrauliche Dokumente getrennt indexieren
- Zugriffe protokollieren

Quelle: [DSK RAG Orientierungshilfe](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf).

## 11. Beschaffung und Freigabe neuer KI-Tools

Vor Freigabe eines KI-Tools muessen geprueft werden:

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
- featurebezogene Retention, z. B. Background Mode, Extended Prompt Caching, Hosted Containers, Message Batches, Audit Logs oder Vector Stores

Freigabe erfolgt durch:

| Rolle | Freigabe erforderlich? |
|---|---:|
| Fachbereich | Ja |
| Datenschutz | Ja |
| Informationssicherheit | Ja |
| Rechtsabteilung / externe Beratung | bei hohem Risiko |
| Geschaeftsfuehrung / Leitung | bei hohem Risiko |

Quellen: [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs).

## 12. Datenschutz-Folgenabschaetzung

Eine DSFA ist zu pruefen bei:

- Verarbeitung personenbezogener Daten mit neuen KI-Technologien
- Profiling, Scoring oder Bewertung
- Beschaeftigtendaten
- Gesundheitsdaten oder Art.-9-Daten
- umfangreicher Verarbeitung
- RAG mit internen personenbezogenen Wissensbestaenden
- agentischer KI mit Dienst-/Dateizugriff
- automatisierten Entscheidungen

Vorlage: `Datenschutz-Folgenabschätzung Vorlage KI Nutzung.md`

Eine Grundrechte-Folgenabschaetzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) kann fuer bestimmte Hochrisiko-KI-Systeme zusaetzlich relevant sein und ergaenzt eine DSFA, soweit deren Pflichten bereits einschlaegige Punkte abdecken.

Quellen: [Art. 35 DSGVO](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27).

## 13. Transparenz

Betroffene Personen muessen informiert werden, wenn ihre personenbezogenen Daten mit KI verarbeitet werden und eine Informationspflicht besteht.

Interne Transparenz:

- Mitarbeitende erhalten diese Richtlinie.
- Freigegebene Tools werden zentral dokumentiert.
- Schulungen sind zu dokumentieren.

Externe Transparenz:

- Datenschutzhinweise pruefen und anpassen.
- Bei Kundenprozessen klarstellen, ob KI assistiv genutzt wird, soweit rechtlich erforderlich.

Zusatzhinweis zum AI Act: Die KI-VO ist seit 1. August 2024 in Kraft. Nach [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113) gilt sie grundsaetzlich ab dem 2. August 2026; Kapitel I und II gelten seit dem 2. Februar 2025, bestimmte GPAI-, Governance- und Sanktionsregeln seit dem 2. August 2025, und Art. 6 Abs. 1 mit entsprechenden Pflichten ab dem 2. August 2027. Nach [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50) muessen u. a. direkte Interaktion mit KI-Systemen, bestimmte KI-generierte oder manipulierte Inhalte, Deepfakes sowie Emotionserkennungs- oder biometrische Kategorisierungssysteme transparent gemacht werden; Ausnahmen und Detailpflichten sind einzelfallbezogen zu pruefen.

Quellen: [Art. 113 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-113), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content).

## 14. Sicherheitsvorfaelle

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

Alle Nutzer freigegebener KI-Tools muessen geschult werden zu:

- erlaubten Tools
- verbotenen Daten
- Prompt-Minimierung
- Output-Pruefung
- Datenschutzvorfaellen
- Risiken von RAG und agentischer KI
- Quellenkritik
- KI-Kompetenz nach Art. 4 KI-VO, bezogen auf technische Kenntnisse, Erfahrung, Ausbildung, Nutzungskontext und betroffene Personengruppen

Quelle: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4).

## 16. Kontrolle und Sanktionen

Die Einhaltung dieser Richtlinie kann stichprobenartig kontrolliert werden, soweit arbeits- und datenschutzrechtlich zulaessig. Verstoesse koennen arbeitsrechtliche, vertragliche oder organisatorische Folgen haben.

## 17. Review

Diese Richtlinie wird mindestens jaehrlich und bei wesentlichen Aenderungen aktualisiert:

- neues KI-Tool
- neues Modell
- Aktivierung von Chat-Suche/Memory, Projektwissen, Konnektoren oder MCP
- neue Anbieterbedingungen
- neue Retention-/Trainingseinstellung
- neue AI-Act-Transparenzpflicht fuer den eigenen Einsatzfall
- neue KI-VO-Einstufung, Grundrechte-Folgenabschaetzung oder Hochrisiko-Leitlinie
- neue Rechtslage
- neue aufsichtsbehoerdliche Entscheidung
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
- [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
- [OpenAI Computer Use](https://developers.openai.com/api/docs/guides/tools-computer-use)
- [Anthropic Computer Use](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use)
- [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context)
- [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans)
- [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs)
- [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing)
- [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en)
