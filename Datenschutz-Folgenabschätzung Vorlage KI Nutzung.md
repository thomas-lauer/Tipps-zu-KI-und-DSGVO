# Datenschutz-Folgenabschaetzung (DSFA) - Vorlage fuer KI-Nutzung

Stand: 16.06.2026  
Status: Vorlage, vor produktivem Einsatz ausfuellen und durch Datenschutzbeauftragte/Rechtspruefung bewerten lassen.

> Hinweis: Diese Vorlage ersetzt keine Rechtsberatung. Sie orientiert sich an Art. 35 DSGVO, den DPIA-Leitlinien WP248 rev.01/EDPB, DSK-Kurzpapier Nr. 5 und den DSK-Hinweisen zu KI. Wenn Informationen fehlen, als "offen" kennzeichnen.

Quellen: [Art. 35 DSGVO, EUR-Lex](https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng), [EDPB/WP29 DPIA Guidelines WP248 rev.01](https://ec.europa.eu/newsroom/article29/items/611236/en), [DSK Kurzpapier Nr. 5 DSFA](https://www.datenschutzkonferenz-online.de/media/kp/dsk_kpnr_5.pdf), [BfDI DSFA-Uebersicht](https://www.bfdi.bund.de/DE/Fachthemen/Inhalte/Technik/Datenschutz-Folgenabschaetzungen.html), [DSK KI und Datenschutz](https://www.datenschutzkonferenz-online.de/media/oh/20240506_DSK_Orientierungshilfe_KI_und_Datenschutz.pdf).

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
- Werden Konnektoren, Browserzugriff, Computer Use, Cowork, Slack/Teams, E-Mail, Kalender oder lokale Dateien genutzt?

Praxis-Hinweis: Zentrale Business-Accounts, AVV/DPA, Zero Data Retention, DSFA und interne Richtlinie sind Mindestbausteine vor produktiver Nutzung.

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

Ergebnis: DSFA erforderlich: Ja / Nein / offen  
Begruendung:

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
| Datenresidenz | EU / USA / global / offen |
| SCC/DPF/TIA geprueft |  |
| Training/Model Improvement deaktiviert |  |
| Zero Data Retention verfuegbar und aktiv |  |
| Retention fuer Chats/Dateien/Logs dokumentiert |  |
| Loeschkonzept vorhanden |  |
| Betroffenenrechte umsetzbar |  |

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
| Missbrauch von Konnektoren, Browser oder lokalen Dateien |  |  |  | separate Freigabe, Least Privilege |  |
| Unklare Loeschung aus Logs/Backups/Indexen |  |  |  | Loeschkonzept, Anbieterpruefung |  |
| Fehlende Transparenz gegenueber Betroffenen |  |  |  | Datenschutzhinweise, interne Hinweise |  |

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

## 12. Betroffenenrechte

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

## 13. Ergebnis und Freigabeentscheidung

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

## 14. Review

Erneute Pruefung bei:

- Anbieterwechsel
- Modellwechsel
- neuer Funktion wie Konnektoren, Computer Use, Cowork oder RAG
- Aenderung der Datenkategorien
- Aenderung der Retention
- neuer Drittlandtransfer
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
