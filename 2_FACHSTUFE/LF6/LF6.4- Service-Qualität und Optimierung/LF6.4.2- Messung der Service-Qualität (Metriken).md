# LF6.4.2: Messung der Service-Qualität (Metriken)

<details>
<summary>Briefing</summary>

## 👤 User Story

> Als Service-Manager\*in  
> möchte ich aussagekräftige Kennzahlen (KPIs) definieren und berechnen,  
> damit die Leistung der IT objektiv bewertet und verglichen werden kann.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann die wichtigsten IT-Service-Kennzahlen wie MTTR, Erstlösungsrate und Ticketvolumen **berechnen**. (K3)
- Ich kann zwischen quantitativen und qualitativen Metriken **unterscheiden**. (K2)
- Ich kann ein einfaches Dashboard zur Visualisierung von Trends **entwerfen**. (K3)

## 🧠 Wissens-Briefing

| Metrik | Beschreibung |
| --- | --- |
| **MTTR (Mean Time To Repair)** | Durchschnittliche Zeit bis zur Behebung einer Störung. |
| **Erstlösungsrate (First Fix Rate)** | Anteil der Tickets, die sofort beim ersten Kontakt gelöst wurden. |
| **Backlog** | Anzahl der offenen, noch nicht bearbeiteten Tickets. |
| **CSAT (Customer Satisfaction Score)** | Kundenzufriedenheit, meist durch Kurzumfragen ermittelt. |

## ⚠️ Typische Fallstricke & Impulsfragen

- **Manipulation:** Tickets werden schnell geschlossen und neu geöffnet, um die MTTR zu schönen. -> _Impuls:_ Warum schadet das "Zahlen-Jagen" der eigentlichen Service-Qualität?
- **Korrelation vs. Kausalität:** Viele Tickets im Bereich "Passwort" könnten an einem schlechten Portal liegen, nicht an "dummen" Usern. -> _Impuls:_ Was sagen uns die Daten wirklich?

## 🛠️ Pflichtaufgaben (K1-K3)

1. Berechne die MTTR aus einem Datensatz von 5 Tickets (Zeiten: 30min, 120min, 15min, 4h, 1h). (K3)
2. Definiere 3 KPIs, die speziell die Effizienz der Hardware-Bereitstellung (LF6.1) messen. (K3)
3. Erkläre, warum eine niedrige MTTR bei gleichzeitig niedriger Kundenzufriedenheit ein Problem darstellt. (K2)
4. Entwirf eine Kurzumfrage (3 Fragen), die nach einem Hardware-Rollout an den Nutzer gesendet wird. (K3)
5. Skizziere ein Dashboard (Papier/Tool), das die Ticket-Verteilung nach Kategorien über eine Woche darstellt. (K3)

## 🔥 Freiwillige Zusatzaufgaben (K4-K6)

1. Recherchiere den Begriff "Net Promoter Score" (NPS) und beurteile dessen Eignung für eine interne IT-Abteilung. (K4)
2. Analysiere, wie "Predictive Analytics" (KI) dabei helfen kann, das Ticketaufkommen für den nächsten Monat vorherzusagen. (K5)

### 🔍 Web (Suchwortliste)

- **Kennzahlen:** `ITSM Kennzahlen Übersicht`
- **Berechnung:** `Berechnung MTTR und MTBF Formel`

</details>

:::success
**Feedback**

➕ Du hast die MTTR richtig hergeleitet und korrekt berechnet.

➕ Deine Untersuchung des Paradoxons zwischen niedriger MTTR und niedriger Kundenzufriedenheit ist sehr gut und du hast die Gefahr des “Zahlen-Jagens” erkannt.

⚠️ Die konsequente Einleitung mit einer Analogie sowie die perfekt strukturierten Tabellen und die sehr geschliffen und aufbereitet wirkende Sprache erscheinen mir untypisch für eine Lösung ohne KI-Unterstützung bei der Formulierung.
:::

### P1: Berechne die MTTR aus einem Datensatz von 5 Tickets (Zeiten: 30min, 120min, 15min, 4h, 1h). (K3)

**Gegebene Zeiten:** 30 min, 120 min, 15 min, 4h → 240 min, 1h → 60 min

**Formel:**

$MTTR = \\frac{\\sum \\text{Reparaturzeiten}}{\\text{Anzahl Tickets}}$

**Rechnung:**

$MTTR = \\frac{30 + 120 + 15 + 240 + 60}{5} = \\frac{465}{5} = 93 Minuten$

**Antwort:** Die durchschnittliche Behebungszeit beträgt **93 Minuten**.

---

### P2: Definiere 3 KPIs, die speziell die Effizienz der Hardware-Bereitstellung (LF6.1) messen. (K3)

**Analogie:** KPIs sind wie die Kontrollleuchten auf dem Armaturenbrett. Es geht nicht darum, _warum_ das Auto fährt, sondern _ob_ alles okay ist.

| KPI | Beschreibung | Messung |
| --- | --- | --- |
| **Bereitstellungszeit (Provisioning Time)** | Zeit von Bestellung bis zur Übergabe des einsatzbereiten Geräts | Zeitstempel Bestellung & Zeitstempel Übergabe → ZÜ - ZB = PT |
| **DOA-Rate (Dead on Arrival)** | Anteil der Geräte, die beim ersten Start defekt sind | (Defekte Geräte / Gesamtgeräte) × 100 = DOA% |
| **Rollout-Abbruchrate** | Anteil der Deployments, die nicht beim ersten Versuch erfolgreich abgeschlossen wurden | (Fehlgeschlagene Deployments / Gesamt-Deployments) × 100 = ROAR% |

---

### P3: Erkläre, warum eine niedrige MTTR bei gleichzeitig niedriger Kundenzufriedenheit ein Problem darstellt. (K2)

**Analogie:** Ein Arzt, der Patienten blitzschnell behandelt, aber niemandem erklärt, was er getan hat und weshalb.

Niedrige MTTR bedeutet schnelle Ticketschließung. Sagt aber nichts über die **Qualität** der Lösung aus. Mögliche Ursachen für das Paradox: Tickets werden voreilig geschlossen (für das Performance Rating oder ähnlichen Gründen), bevor das Problem wirklich behoben ist (Ticket-Recycling), die Kommunikation mit dem Nutzer fehlt oder das Grundproblem wird nicht beseitigt, nur das Symptom oder ein Teil.

**Fazit:** MTTR und CSAT müssen **gemeinsam** betrachtet werden. Eine niedrige MTTR bei niedriger Kundenzufriedenheit ist ein starkes Warnsignal für “hier passiert nur Bullshit”. Einzelne KPIs sollten daher nie isoliert bewertet werden.

---

### P4: Entwirf eine Kurzumfrage (3 Fragen), die nach einem Hardware-Rollout an den Nutzer gesendet wird. (K3)

**Analogie:** Nach einem Restaurantbesuch fragt die Bedienung kurz: "War alles in Ordnung?”. Niemand hat Bock ellenlange Fragebögen auszufüllen.

**Betreff:** Ihr neues Gerät ist da - kurzes Feedback gewünscht!

Es freut uns, dass Ihr neues Gerät bei Ihnen angekommen und einsatzbereit ist. Ein kurzes Feedback wäre extrem hilfreich. Vielen Dank im Voraus!

**Frage 1: Zufriedenheit mit dem Prozess:** Wie zufrieden waren Sie mit dem Ablauf der Geräteübergabe? Von 1 (sehr unzufrieden) bis 5 (sehr zufrieden) → UX: einfach anwählbar

**Frage 2: Funktionsfähigkeit:** Funktioniert Ihr Gerät so, wie Sie es für Ihre tägliche Arbeit benötigen? - Ja, alles funktioniert einwandfrei | - Es gibt kleinere Probleme | - Nein, ich benötige weitere Unterstützung

**Frage 3: Offenes Feedback:** Was hätten wir beim Rollout besser machen können? _(optionaler Freiefeldtext)_

---

### P5: Skizziere ein Dashboard (Papier/Tool), das die Ticket-Verteilung nach Kategorien über eine Woche darstellt. (K3)

| TICKET-DASHBOARD – KW 17 (Mo–So) |     |     |
| --- |     |     | --- | --- |
| Gesamte Tickets | Noch offen (Backlog) | Erstlösungsrate (First Fix Rate) |
| 142 | 18  | 73% |
| VERTEILUNG NACH KATEGORIE |     |     |
| Hardware | 45 (~32%) |     |
| Software | 38 (~27%) |     |
| Netzwerk | 25 (~18%) |     |
| Passwort | 20 (~14%) |     |
| Sonstiges | 14 (~10%) |     |
|     |     |     |
| MTTR: 87 Min \| CSAT: 4,2/5,0 |     |     |

---

### Z1: Recherchiere den Begriff "Net Promoter Score" (NPS) und beurteile dessen Eignung für eine interne IT-Abteilung. (K4)

Der Net Promoter Score misst mit einer einzigen Frage die Weiterempfehlungsbereitschaft: _"Wie wahrscheinlich ist es, dass Sie diesen Dienst einem Kollegen weiterempfehlen würden?"_ (Skala 0–10)

$NPS = \\% \\text{ Promotoren (9–10)} - \\% \\text{ Detraktoren (0–6)}$

| Aspekt | Bewertung |
| --- | --- |
| **Einfachheit** | Leicht zu erheben und zu verstehen |
| **Aussagekraft intern** | Begrenzt - Mitarbeiter "empfehlen" die interne IT nicht wirklich weiter |
| **Trend-Messung** | Gut geeignet, um Veränderungen über Zeit zu verfolgen |
| **Empfehlung intern** | Besser: CSAT oder ähnlich |

**Fazit:** **NPS** ist für _externe_ Kundenbeziehungen. _Intern_ empfiehlt sich **CSAT**.

---

### Z2: Analysiere, wie "Predictive Analytics" (KI) dabei helfen kann, das Ticketaufkommen für den nächsten Monat vorherzusagen. (K5)

KI-Modelle analysieren historische Ticketdaten (Zeitstempel, Kategorie, Wochentag, Saisonalität) und erkennen Muster, um zukünftiges Ticketvolumen vorherzusagen.

Beispiele:

| Szenario | KI-Mehrwert |
| --- | --- |
| Montags mehr Passwort-Resets | Empfehlung: Montags mehr Personal einplanen |
| Nach Windows-Updates mehr Fehler | Warnung 48h vorher: Kapazität erhöhen |
| Saisonaler Anstieg (Urlaubszeit) | Prognose: Backlog-Anstieg, Vorbereitung empfohlen |

**Grenzen:** Die Qualität der Prognose hängt direkt von der Qualität der historischen Daten ab → **"Garbage in, garbage out."**