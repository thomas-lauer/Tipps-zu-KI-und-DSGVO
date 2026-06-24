# Datenschutz-Folgenabschaetzung (DSFA) - Vorlage fuer KI-Nutzung

Stand: 18.06.2026
Status: Vorlage, vor produktivem Einsatz ausfuellen und durch Datenschutzbeauftragte/Rechtspruefung bewerten lassen.

> Hinweis: Diese Vorlage ersetzt keine Rechtsberatung. Sie orientiert sich an Art. 35 DSGVO, den DPIA-Leitlinien WP248 rev.01/EDPB, DSK-Kurzpapier Nr. 5 und den DSK-Hinweisen zu KI. Wenn Informationen fehlen, als "offen" kennzeichnen.

Quellen: [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EDPB/WP29 DPIA Guidelines WP248 rev.01](https://ec.europa.eu/newsroom/article29/items/611236/en), [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf), [BfDI DSFA-Uebersicht](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Technik/Datenschutz-Folgenabschaetzungen.html), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf), [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf).

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
| KI-VO-Rolle | Anbieter / Betreiber / Einfuehrer / Haendler / offen |
| KI-VO-Risikoklasse | verboten / Hochrisiko / begrenztes Risiko / minimales Risiko / offen |
| Datum der Bewertung |  |
| Version der DSFA |  |
| Naechste Ueberpruefung |  |

## 2. Kurzbeschreibung der Verarbeitung

- Zweck der KI-Nutzung:
- Geschaeftsprozess:
- Nutzergruppen:
- Eingaben/Prompts:
- Uploads/Dateien:
- Outputs:
- Automatisierungsgrad:
- Wird die KI nur assistiv genutzt?
- Gibt es eine Entscheidung ueber Personen?
- Werden Chat-Suche/Memory, Konnektoren, Browserzugriff, Computer Use, Cowork, Slack/Teams, E-Mail, Kalender oder lokale Dateien genutzt?
- Werden OpenAI-Funktionen mit eigener Retention genutzt, z. B. Responses API mit `store`, Background Mode, Extended Prompt Caching, Hosted Shell, Code Interpreter, gehostete Skills, Assistants, Threads oder Vector Stores?
- Werden Anthropic-Funktionen mit eigener Retention genutzt, z. B. Claude Enterprise-Projekte, Audit Logs, Message Batches oder API-Features ohne ZDR?

Praxis-Hinweis: Zentrale Business-Accounts, AVV/DPA, Zero Data Retention, DSFA, dokumentierte Feature-Freigaben fuer Memory/Chat-Suche und Konnektoren sowie eine interne Richtlinie sind Mindestbausteine vor produktiver Nutzung.

Quellen: [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp).

## 3. Schwellwertanalyse: Ist eine DSFA erforderlich?

| Kriterium | Ja/Nein/offen | Begruendung |
|---|---:|---|
| Neue Technologie oder neuartiger KI-Einsatz |  |  |
| Umfangreiche Verarbeitung personenbezogener Daten |  |  |
| Besondere Kategorien nach Art. 9 DSGVO |  |  |
| Daten von Kindern/Jugendlichen |  |  |
| Beschaeftigtendaten |  |  |
| Profiling, Scoring oder Bewertung von Personen |  |  |
| Automatisierte Entscheidung mit erheblicher Wirkung |  |  |
| Systematische Ueberwachung |  |  |
| Zusammenfuehrung mehrerer Datenquellen |  |  |
| Einsatz von RAG/Wissensdatenbank mit internen Dokumenten |  |  |
| Drittlandtransfer in die USA oder andere Drittlaender |  |  |
| Agentische Funktionen mit Zugriff auf lokale Daten/Dienste |  |  |
| Hochrisiko-KI oder Profiling nach KI-VO |  |  |
| Grundrechte-Folgenabschaetzung nach KI-VO erforderlich |  |  |

Ergebnis: DSFA erforderlich: Ja / Nein / offen  
Begruendung:

KI-VO-Hinweis: Die Grundrechte-Folgenabschaetzung nach [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27) ersetzt die DSFA nicht; wenn Pflichten aus einer DSFA nach [Art. 35 DSGVO](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng) bereits erfuellt sind, ergaenzt die KI-VO-Abschaetzung diese DSFA. Hochrisiko-Einstufungen sind nach [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6) zu dokumentieren.

## 4. Datenkategorien

| Datenkategorie | Beispiele | Erforderlich? | Schutzbedarf |
|---|---|---:|---|
| Kontaktdaten | Name, E-Mail, Telefon |  | niedrig / mittel / hoch |
| Kundendaten | Kundenhistorie, Anfragen, Vertragsdaten |  | niedrig / mittel / hoch |
| Beschaeftigtendaten | Rolle, Leistung, Abwesenheit, Kommunikation |  | niedrig / mittel / hoch |
| Art.-9-Daten | Gesundheit, Religion, biometrische Daten |  | hoch |
| Kommunikationsdaten | Chat, E-Mail, Tickets |  | niedrig / mittel / hoch |
| Inhaltsdaten | Dokumente, Code, Dateien, Wissensdatenbank |  | niedrig / mittel / hoch |
| Metadaten/Logs | Nutzer, Zeitpunkt, IP, Token, Fehlerlogs |  | niedrig / mittel / hoch |
| Sonstige |  |  |  |

## 5. Betroffene Personen

- Kunden / Interessenten:
- Beschaeftigte:
- Bewerber:
- Lieferanten / Partner:
- Website-Nutzer:
- Kinder/Jugendliche:
- Sonstige:

## 6. Rechtsgrundlagen

| Verarbeitungsschritt | Rechtsgrundlage | Begruendung |
|---|---|---|
| Eingabe in KI-System | Art. 6 Abs. 1 ... DSGVO |  |
| Upload von Dokumenten | Art. 6 Abs. 1 ... DSGVO |  |
| Verarbeitung durch Anbieter | Art. 28 DSGVO / eigene Verantwortlichkeit / offen |  |
| Speicherung von Logs | Art. 6 Abs. 1 ... DSGVO |  |
| Art.-9-Daten, falls vorhanden | Art. 9 Abs. 2 ... DSGVO |  |
| Drittlandtransfer | Art. 44 ff. DSGVO, Mechanismus:  |  |

Offene Rechtsfragen:

## 7. Anbieter- und Vertragspruefung

| Pruefpunkt | Ergebnis |
|---|---|
| AVV/DPA abgeschlossen |  |
| Rolle des Anbieters geklaert | Verantwortlicher / Auftragsverarbeiter / gemeinsam / offen |
| Subprozessoren geprueft |  |
| TOMs erhalten/geprueft |  |
| Chat-Suche/Memory/Projektwissen aktiviert |  |
| Admin-Kontrollen fuer Zusatzfunktionen geprueft |  |
| MCP/Konnektoren/Drittserver separat geprueft |  |
| Datenresidenz | EU / USA / global / offen |
| SCC/DPF/TIA geprueft |  |
| Training/Model Improvement deaktiviert |  |
| Zero Data Retention verfuegbar und aktiv |  |
| API-spezifische Speicherlogik (z. B. Responses API / Background Mode) geprueft |  |
| Extended Prompt Caching / Hosted Containers / gehostete Skills geprueft |  |
| Assistants / Threads / Vector Stores geloescht oder Retention dokumentiert |  |
| Anthropic Message Batches oder sonstige nicht-ZDR-faehige Features ausgeschlossen oder bewertet |  |
| Audit Logs und Datenexporte dokumentiert |  |
| Retention fuer Chats/Dateien/Logs dokumentiert |  |
| Loeschkonzept vorhanden |  |
| Betroffenenrechte umsetzbar |  |

Quellen: [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp), [Claude Chat Search and Memory](https://support.claude.com/en/articles/11817273-use-claude-s-chat-search-and-memory-to-build-on-previous-context), [Claude Enterprise Retention](https://support.claude.com/en/articles/10440198-configure-custom-data-retention-controls-for-enterprise-plans), [Claude Audit Logs](https://support.claude.com/en/articles/9970975-access-audit-logs), [Anthropic Message Batches](https://platform.claude.com/docs/en/build-with-claude/batch-processing).

## 8. Notwendigkeit und Verhaeltnismaessigkeit

- Warum ist der KI-Einsatz erforderlich?
- Welche weniger eingriffsintensiven Alternativen wurden geprueft?
- Warum reichen lokale Tools, klassische Suche, manuelle Bearbeitung oder anonymisierte Daten nicht aus?
- Welche Daten werden bewusst nicht verarbeitet?
- Wie wird verhindert, dass Nutzer mehr Daten eingeben als erforderlich?
- Gibt es eine Tool-Whitelist und Input-Grenzen?
- Wie wird die Qualitaet der Ergebnisse geprueft?

## 9. Datenschutzgrundsaetze

| Grundsatz | Umsetzung | Bewertung |
|---|---|---|
| Rechtmaessigkeit |  | ausreichend / offen / unzureichend |
| Transparenz | Datenschutzhinweis, interne Richtlinie, Kennzeichnung |  |
| Zweckbindung | klarer Use Case, keine Zweckausweitung |  |
| Datenminimierung | Pseudonymisierung, Prompt-Regeln, Input-Grenzen |  |
| Richtigkeit | Output-Pruefung, Quellenkontrolle |  |
| Speicherbegrenzung | Retention, Loeschkonzept |  |
| Integritaet/Vertraulichkeit | MFA, SSO, Rollen, Verschluesselung |  |
| Rechenschaftspflicht | Dokumentation, Freigabe, Review |  |

## 10. Risikoanalyse

Bewertungsskala:

- Eintrittswahrscheinlichkeit: 1 niedrig, 2 mittel, 3 hoch
- Schwere des Schadens: 1 niedrig, 2 mittel, 3 hoch
- Risiko: Wahrscheinlichkeit x Schwere

| Risiko fuer Betroffene | W | S | Risiko | Massnahmen | Restrisiko |
|---|---:|---:|---:|---|---:|
| Unbefugte Offenlegung personenbezogener Daten an KI-Anbieter |  |  |  | DPA, Retention, ZDR, Minimierung |  |
| Training/Weiterverwendung von Eingaben |  |  |  | Opt-out/vertraglicher Ausschluss |  |
| Drittlandtransfer ohne ausreichende Grundlage |  |  |  | SCC/DPF/TIA, EU-Residenz |  |
| Falsche personenbezogene KI-Ausgabe |  |  |  | Human Review, Quellenpruefung |  |
| Diskriminierende Ausgabe |  |  |  | Testfaelle, Review, keine Letztentscheidung |  |
| Automatisierte Entscheidung nach Art. 22 DSGVO |  |  |  | nur assistiv, menschliche Entscheidung |  |
| Unberechtigter Zugriff durch falsche RAG-Berechtigungen |  |  |  | RBAC, Index-Trennung, Tests |  |
| Prompt-Injection / Datenabfluss bei RAG oder Agenten |  |  |  | Isolation, Allowlist, Logging, Freigabe |  |
| Ungewollte Wiederverwendung frueherer Chats/Projektinhalte durch Memory oder Chat-Suche |  |  |  | Feature-Freigabe, Retention, Admin-Kontrollen |  |
| Missbrauch von Konnektoren, Browser oder lokalen Dateien |  |  |  | separate Freigabe, Least Privilege |  |
| Memorisation oder Rekonstruktion personenbezogener Daten aus LLM-Kontexten |  |  |  | Minimierung, Pseudonymisierung, kurze Retention, Tests |  |
| Feature-Retention weicht von ZDR-Annahme ab |  |  |  | endpointbezogene Pruefung, technische Konfiguration, Vertragsnachweis |  |
| Unvollstaendige KI-VO-Einstufung oder fehlende Transparenz |  |  |  | KI-VO-Kurzcheck, Schulung, Kennzeichnung, Dokumentation |  |
| Unklare Loeschung aus Logs/Backups/Indexen |  |  |  | Loeschkonzept, Anbieterpruefung |  |
| Fehlende Transparenz gegenueber Betroffenen |  |  |  | Datenschutzhinweise, interne Hinweise |  |

Quellen: [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf), [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data), [Anthropic API and Data Retention](https://platform.claude.com/docs/en/manage-claude/api-and-data-retention), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50).

## 11. Technische und organisatorische Massnahmen

Mindestmassnahmen:

- zentraler Business-/Enterprise-/API-Account
- AVV/DPA
- Training/Model Improvement deaktiviert oder ausgeschlossen
- kurze Retention bzw. Zero Data Retention, falls verfuegbar
- SSO/MFA
- Rollen- und Berechtigungskonzept
- Tool-Whitelist
- Verbot privater Accounts fuer Unternehmensdaten
- Prompt-Regeln und Pseudonymisierung
- Upload-Beschraenkungen
- Output-Pruefung
- Logging mit Datenschutzbegrenzung
- Incident-Prozess
- Schulung der Nutzer
- regelmaessige Re-Evaluation

Zusatzmassnahmen fuer hohe Risiken:

- DSFA-Freigabe durch Datenschutzbeauftragte
- Rechtsfreigabe
- Informationssicherheitsfreigabe
- TIA/Drittlandtransferbewertung
- RAG-Berechtigungstest
- Prompt-Injection-Test
- separate Freigabe fuer agentische Funktionen
- Pilotphase mit anonymisierten Daten

## 12. KI-VO-Zusatzpruefung

| Pruefpunkt | Ergebnis |
|---|---|
| Verbotene KI-Praktik nach Art. 5 KI-VO ausgeschlossen |  |
| Hochrisiko-Einstufung nach Art. 6 KI-VO geprueft |  |
| Transparenzpflichten nach Art. 50 KI-VO geprueft |  |
| Nutzerhinweis bei Interaktion mit Chatbots oder anderen interaktiven KI-Systemen dokumentiert |  |
| Kennzeichnung von Deepfakes sowie KI-generierten/manipulierten Texten zu oeffentlichem Interesse geprueft |  |
| KI-Kompetenz und Schulung nach Art. 4 KI-VO umgesetzt |  |
| Grundrechte-Folgenabschaetzung nach Art. 27 KI-VO erforderlich | Ja / Nein / offen |
| Technische Dokumentation / Protokollierung / menschliche Aufsicht relevant |  |

Praxis-Hinweis: Der finale [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content) wurde am 10.06.2026 veroeffentlicht. Er ist freiwillig; die gesetzlichen Transparenzpflichten nach Art. 50 KI-VO gelten ab dem 02.08.2026. In der DSFA sollte deshalb festgehalten werden, wie Interaktionshinweise, Labels, Zustaendigkeiten und Ausnahmen fuer den konkreten Use Case umgesetzt und nachgewiesen werden.

Quellen: [Art. 4 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-4), [Art. 5 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-5), [Art. 6 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-6), [Art. 27 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-27), [Art. 50 KI-VO](https://ai-act-service-desk.ec.europa.eu/de/ai-act/article-50), [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content), [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content).

## 13. Betroffenenrechte

| Recht | Umsetzung |
|---|---|
| Auskunft |  |
| Berichtigung |  |
| Loeschung |  |
| Einschraenkung |  |
| Widerspruch |  |
| Datenuebertragbarkeit |  |
| Art. 22 DSGVO |  |

Offene Punkte:

## 14. Ergebnis und Freigabeentscheidung

Gesamtrisiko vor Massnahmen: niedrig / mittel / hoch  
Restrisiko nach Massnahmen: niedrig / mittel / hoch  
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
| Geschaeftsfuehrung / Leitung |  |  |  |

## 15. Review

Erneute Pruefung bei:

- Anbieterwechsel
- Modellwechsel
- Aktivierung oder Aenderung von Chat-Suche/Memory/Projektwissen
- neuer Funktion wie Konnektoren, Computer Use, Cowork oder RAG
- neuer Konnektor oder MCP-Server
- Aenderung der Datenkategorien
- Aenderung der Retention
- neuer Drittlandtransfer
- neue KI-VO-Einstufung, Transparenzpflicht oder Grundrechte-Folgenabschaetzung
- Datenschutzvorfall
- neue aufsichtsbehoerdliche Entscheidung
- spaetestens nach 12 Monaten

## Quellen

- [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng)
- [EDPB/WP29 DPIA Guidelines WP248 rev.01](https://ec.europa.eu/newsroom/article29/items/611236/en)
- [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf)
- [BfDI DSFA-Uebersicht](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Technik/Datenschutz-Folgenabschaetzungen.html)
- [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf)
- [DSK RAG Orientierungshilfe](https://www.datenschutzkonferenz-online.de/media/oh/DSK_OH_RAG.pdf)
- [EDPB AI Privacy Risks and Mitigations in LLMs](https://www.edpb.europa.eu/system/files/2025-04/ai-privacy-risks-and-mitigations-in-llms.pdf)
- [OpenAI Data controls](https://developers.openai.com/api/docs/guides/your-data)
- [OpenAI MCP and Connectors](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)
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
- [Code of Practice on Transparency of AI-Generated Content](https://digital-strategy.ec.europa.eu/en/policies/code-practice-ai-generated-content)
- [EU-Kommission zum finalen Code of Practice vom 10.06.2026](https://digital-strategy.ec.europa.eu/en/news/commission-publishes-code-practice-marking-and-labelling-ai-generated-content)
