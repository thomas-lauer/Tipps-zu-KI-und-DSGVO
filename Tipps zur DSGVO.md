# Tipps zur DSGVO bei der Nutzung von Claude.ai und OpenAI

Stand: 16.06.2026

Dieses Dokument ist eine praktische Checkliste fuer den Einsatz generativer KI. Es ersetzt keine Rechtsberatung. Wenn ein Punkt nicht sicher bewertet werden kann, muss er als offen dokumentiert und vor produktiver Nutzung geklaert werden.

## 1. Erst klaeren: Welcher Account wird genutzt?

Nutze fuer Unternehmensdaten keine privaten Free/Pro/Max-Accounts. Verwende nur Business-, Enterprise- oder API-Angebote, bei denen ein AVV/DPA, Admin-Kontrollen, Retention-Einstellungen und Nachweise zu Subprozessoren verfuegbar sind.

Quellen: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [Anthropic Claude for Work Rollen](https://support.anthropic.com/en/articles/9267385-what-is-the-data-relationship-between-anthropic-the-customer-and-the-user).

## 2. Keine sensiblen Daten in Consumer-KI

Nicht eingeben:

- Gesundheitsdaten
- Bewerber- und HR-Bewertungen
- Kundendaten mit Identifikatoren
- Vertrags-, Steuer-, Rechts- oder Mandantendaten
- Passwoerter, API-Keys, Tokens
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

## 4. Training/Model Improvement deaktivieren

Bei OpenAI und Anthropic muss fuer den konkreten Dienst geprueft werden, ob Eingaben/Dateien/Outputs fuer Training oder Serviceverbesserung verwendet werden. Fuer personenbezogene Unternehmensdaten sollte Training vertraglich ausgeschlossen oder technisch deaktiviert sein.

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

Nutze moeglichst kurze Retention. Zero Data Retention ist nur dann relevant, wenn sie fuer den konkreten Vertrag/Plan/Endpunkt tatsaechlich gilt.

Quellen: [OpenAI Business Data](https://openai.com/business-data/), [Anthropic Enterprise Retention](https://support.anthropic.com/en/articles/10440198-custom-data-retention-controls-for-claude-enterprise), [Anthropic Zero Data Retention](https://privacy.anthropic.com/en/articles/8956058-i-have-a-zero-retention-agreement-with-anthropic-what-products-does-it-apply-to).

## 6. AVV/DPA abschliessen

Wenn die KI personenbezogene Daten im Auftrag verarbeitet, ist ein AVV/DPA nach Art. 28 DSGVO erforderlich. Pruefe:

- Vertragspartner
- Rolle des Anbieters
- Subprozessoren
- Weisungsbindung
- technische und organisatorische Massnahmen
- Loeschung/Rueckgabe
- Audit-/Nachweisrechte
- Drittlandtransfers

Quellen: [Art. 28 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [OpenAI DPA](https://openai.com/policies/data-processing-addendum/), [Anthropic Claude for Work Rollen](https://support.anthropic.com/en/articles/9267385-what-is-the-data-relationship-between-anthropic-the-customer-and-the-user).

## 7. Drittlandtransfer nicht vergessen

OpenAI und Anthropic sind US-nahe Anbieter bzw. nutzen internationale Infrastruktur/Subprozessoren. Vor Einsatz mit personenbezogenen Daten muss der Drittlandtransfer nach Art. 44 ff. DSGVO geprueft werden. Moegliche Bausteine sind EU-Data-Residency, Standardvertragsklauseln, Transfer Impact Assessment, EU-U.S. Data Privacy Framework und zusaetzliche technische Massnahmen. Ob ein Anbieter aktuell fuer einen konkreten Dienst zertifiziert ist, muss in der offiziellen DPF-Liste geprueft werden.

Quellen: [Art. 44 ff. DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [Data Privacy Framework List](https://www.dataprivacyframework.gov/list), [OpenAI Data Residency Europe](https://openai.com/index/introducing-data-residency-in-europe/), [EU-Kommission DPF Q&A](https://ec.europa.eu/commission/presscorner/detail/en/qanda_23_3752).

## 8. DSFA pruefen

Eine Datenschutz-Folgenabschaetzung ist besonders naheliegend bei:

- neuen Technologien mit hohem Risiko
- umfangreicher Verarbeitung personenbezogener Daten
- Profiling oder Scoring
- Beschaeftigtendaten
- Gesundheitsdaten oder anderen Art.-9-Daten
- automatisierten Entscheidungen
- systematischer Ueberwachung
- RAG-Systemen mit grossen internen Wissensbestaenden

Quellen: [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 9. Keine automatisierte Letztentscheidung

KI-Ausgaben duerfen nicht ungeprueft ueber Menschen entscheiden. Besonders kritisch sind Bewerbungen, Mitarbeiterbewertungen, Bonitaet, Versicherungen, Gesundheit, Vertragszugang, Sanktionen und Leistungsentscheidungen. Eine menschliche Pruefung muss echt, kompetent und dokumentiert sein.

Quellen: [Art. 22 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 10. Ergebnisse immer pruefen

LLMs koennen falsche Tatsachen, erfundene Quellen, diskriminierende Muster oder personenbezogene Falschinformationen erzeugen. Ergebnisse duerfen deshalb nicht blind uebernommen werden. Bei personenbezogenen Aussagen ist das Richtigkeitsgebot besonders wichtig.

Quellen: [Art. 5 DSGVO Richtigkeit, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [EDPB ChatGPT Taskforce](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-chatgpt-taskforce_en).

## 11. RAG ist hilfreich, aber kein Freifahrtschein

Ein internes RAG-System kann Datenschutz verbessern, wenn es nur freigegebene Quellen nutzt und Berechtigungen sauber abbildet. Es kann aber auch neue Risiken schaffen:

- falsche Indexierung
- Zugriff auf Dokumente ohne Berechtigung
- Prompt-Injection
- veraltete Quellen
- unklare Loeschung aus Indexen
- Offenlegung vertraulicher Passagen in Antworten

Quelle: [DSK RAG Orientierungshilfe, Oktober 2025](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf).

## 12. Interne KI-Richtlinie erstellen

Eine gute KI-Richtlinie enthaelt:

- erlaubte Tools und verbotene Tools
- erlaubte Datenarten
- verbotene Datenarten
- Prompt-Regeln
- Freigabeprozess fuer neue Use Cases
- Umgang mit Dateien und Konnektoren
- Pruefpflicht fuer Outputs
- Kennzeichnung von KI-Unterstuetzung, wenn erforderlich
- Meldeweg fuer Datenschutzvorfaelle
- Schulungspflicht

Quelle: [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

## 13. Anbieterpruefung als Kurzcheck

Vor Freigabe eines KI-Tools beantworten:

- Welcher Anbieter und welcher konkrete Plan?
- Gibt es AVV/DPA?
- Werden Eingaben fuer Training genutzt?
- Welche Retention gilt?
- Wo werden Daten verarbeitet?
- Welche Subprozessoren gibt es?
- Gibt es Admin-Konsole, SSO, MFA, Rollenrechte?
- Koennen Chats/Dateien geloescht/exportiert werden?
- Gibt es Logs fuer Missbrauch und Security?
- Wie werden Betroffenenrechte erfuellt?
- Gibt es eine Moeglichkeit fuer EU Data Residency oder ZDR?
- Ist eine DSFA erforderlich?

Quellen: [OpenAI Security and Privacy](https://openai.com/security-and-privacy/), [OpenAI Enterprise Privacy](https://openai.com/enterprise-privacy/), [Anthropic Trust Center](https://trust.anthropic.com/), [Anthropic Commercial Customers](https://privacy.anthropic.com/en/collections/10663361-commercial-customers).

## 14. Was aus Entscheidungen gelernt werden kann

- ChatGPT/OpenAI: Aufsichtsbehoerden pruefen Transparenz, Rechtsgrundlage, Richtigkeit, Betroffenenrechte und Kinderschutz. Die italienische Sanktion aus 2024 darf wegen des 2026 veroeffentlichten gerichtlichen Hinweises auf der Garante-Seite nicht als final bestaetigt dargestellt werden.
- Clearview AI: Oeffentlich zugaengliche Daten sind nicht automatisch frei nutzbar. Scraping und biometrische Verarbeitung sind sehr risikoreich.
- SCHUFA: Automatisierte Scores koennen Art. 22 DSGVO ausloesen, wenn sie fuer Entscheidungen faktisch massgeblich sind.

Quellen: [EDPB ChatGPT Taskforce](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-chatgpt-taskforce_en), [Garante ChatGPT Hinweis](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10085432), [EDPB Clearview Niederlande](https://www.edpb.europa.eu/news/national-news/2024/dutch-supervisory-authority-imposes-fine-clearview-because-illegal-data_en), [EDPB Clearview Frankreich](https://www.edpb.europa.eu/news/national-news/2022/french-sa-fines-clearview-ai-eur-20-million_en), [EuGH SCHUFA C-634/21](https://infocuria.curia.europa.eu/tabs/redirect/juris/document/document.jsf?docid=280426&doclang=en).

## 15. Sofort umsetzbare Praxisregeln

1. Private KI-Accounts fuer Unternehmensdaten sperren.
2. Offizielle KI-Tools mit DPA/AVV freigeben.
3. Training/Model Improvement deaktivieren.
4. Kurze Retention einstellen.
5. MFA/SSO aktivieren.
6. Rollen und Projekte trennen.
7. Keine Art.-9-Daten ohne DSFA und Rechtsfreigabe.
8. Keine KI-Letztentscheidungen ueber Personen.
9. Prompts pseudonymisieren.
10. Outputs fachlich pruefen.
11. Quellen fuer KI-Aussagen verlangen.
12. Neue Features wie Konnektoren, Computer Use, Datei-Uploads oder RAG vor Aktivierung separat pruefen.
13. Zentrale Business-Accounts fuer Firmen-Tools nutzen, nicht verstreute Einzelaccounts.
14. Tool-Whitelist, Nutzungsregeln und Input-Grenzen schriftlich festlegen.
15. Agentische Funktionen wie Cowork, Computer Use, Browserzugriff oder Slack-/Dienstzugriffe nur separat freigeben.

## Mini-Entscheidungsbaum

1. Enthalten Eingabe oder Upload personenbezogene Daten?
   - Nein: Nutzung mit allgemeinen Sicherheitsregeln moeglich.
   - Ja: weiter zu 2.
2. Handelt es sich um besondere Kategorien, HR, Kinder, Scoring, Gesundheit, Mandanten oder Geheimnisse?
   - Ja: nicht ohne DSFA/Rechtspruefung/Freigabe.
   - Nein: weiter zu 3.
3. Wird ein Business/API/Enterprise-Angebot mit DPA genutzt?
   - Nein: nicht verwenden.
   - Ja: weiter zu 4.
4. Sind Training aus, Retention kurz, Drittlandtransfer geprueft und Betroffenenrechte umsetzbar?
   - Nein: erst konfigurieren/dokumentieren.
   - Ja: kontrollierte Nutzung moeglich.
