# LF6.3.6- Metriken und Vereinbarungen (SLA, SLR, SLI, OLA)

:::warning
➕ Deine Berechnung der Ausfallzeit (P4) ist absolut korrekt und du hast die Einschränkung bezüglich der variierenden Monatslängen und Geschäftszeiten sehr gut erkannt und beschrieben.  
➕ Deine Küchen-Analogie für den OLA (P5) ist sehr anschaulich.

➖ In der Tabelle bei P1 fehlt der "Underpinning Contract" (UC) komplett. Ist drin. Hier hat irgendwas in der Analyse nicht geklappt. (evtl. “Volle Breite” aktivieren)

➖ Dein SLR für die Buchhaltung (P2) ist mit nur einem einzigen, kurzen Satz viel zu oberflächlich für die geforderte Taxonomiestufe (K3).
:::

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

**Als Service-Level-Manager_in möchte ich Dienstgüte-Metriken definieren und vereinbaren, damit die Leistung der IT messbar und vergleichbar wird.**

## ✅ Celebration Criteria (Lernziele)

- Ich kann die Begriffe **SLA**, **SLR**, **SLI** und **OLA** voneinander unterscheiden. (K2)
- Ich kann messbare Service-Level-Indikatoren (SLI) für einen Dienst festlegen. (K3)
- Ich kann die Struktur eines Service-Level-Agreements (SLA) beschreiben. (K2)

## 🧠 Wissens-Briefing

- **SLR (Requirement):** Was der Kunde braucht.
- **SLA (Agreement):** Was vertraglich zugesichert wird.
- **SLI (Indicator):** Was tatsächlich gemessen wird (z. B. Uptime in %).
- **OLA (Operational):** Interne Vereinbarung zwischen IT-Teams.

## ⚠️ Typische Fallstricke & Impulsfragen

- **Wassermelonen-Effekt:** Das Dashboard ist grün (SLA eingehalten), aber der Kunde ist tiefrot (unzufrieden). -> _Impuls:_ Wie können wir "weiche" Faktoren wie Zufriedenheit messbar machen?
- **Unerreichbare Ziele:** Ein SLA von 99,99% Verfügbarkeit versprechen, ohne dass redundante Hardware vorhanden ist. -> _Impuls:_ Wer trägt die Kosten für jedes zusätzliche Prozent Verfügbarkeit?

## 🛠️ Pflichtaufgaben (Training)

1. Erstelle eine Tabelle, die SLA, OLA und UC (Underpinning Contract) vergleicht. (K3)
2. Formuliere ein SLR für eine fiktive Abteilung "Buchhaltung". (K3)
3. Definiere 3 SLIs für den Dienst "Internet-Zugang". (K3)
4. Berechne die erlaubte Ausfallzeit bei einer Verfügbarkeit von 99,5 % pro Monat. (K3)
5. Erkläre, warum ein OLA notwendig ist, um ein SLA einzuhalten. (K2)

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

1. Entwirf ein Dashboard zur Visualisierung von SLIs in Echtzeit. (K5)
2. Analysiere die Konsequenzen von SLA-Verletzungen (Pönalen). (K4)
3. Diskutiere den Begriff "Watermelon Effect" im Service Reporting. (K5)

## 🔗 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann LF6:** Lernsituation 2 "Standards und Vorgaben".
- **Rheinwerk:** Kapitel "Service-Level-Management".

### 🔍 Web (Suchwortliste)

- **Metriken:** `SLA OLA UC Unterschied Beispiele`
- **Berechnung:** `Hochverfügbarkeit Rechner Ausfallzeit`

</details>

# Lösungen

## Pflichtaufgaben

### P1: Erstelle eine Tabelle, die ==SLA==, ==OLA== und ==UC== (Underpinning Contract) vergleicht. (K3)

|     |     |     |     |
| --- | --- | --- | --- |
| **Merkmal** | **SLA (Service Level Agreement)** | **OLA (Operational Level Agreement)** | **UC (Underpinning Contract)** |
| Vertragspartner | IT-Dienstleister ←→ **Externer Kunde** | IT-Abteilung ←→ **Interne Teams** (bspw. Server-Team) | IT-Dienstleister ←→ **Externer Zulieferer** (bspw. ISP) |
| Fokus | Was bekommt der Kunde am Ende? | Wie arbeiten die internen Teams zusammen, um das SLA zu stützen? | Welche Leistungen kaufen wir von Dritten ein? |
| Beispiel | "Das ERP-System ist zu 99,75% der Geschäftszeiten verfügbar." | "Das Server-Team stellt sicher, dass der Server in 1 Std. wieder läuft." | "Der Internetanbieter (ISP) garantiert 99,9 % Leitungsverfügbarkeit." |

---

### P2: Formuliere ein SLR für eine fiktive Abteilung "Buchhaltung". (K3)

~~“Innerhalb der Abrechnungsphase zum Übergang eines jeden Monats muss die Verfügbarkeit des Buchhaltungssystems zu 99,7% gewährleistet sein und ein Störungsfall erhält eine höhere Priorisierung und wird innerhalb von 30 Minuten gelöst.”~~

**Service Level Requirement - Abteilung Buchhaltung**

| Kategorie | Anforderung |
| --- | --- |
| Service | Buchhaltungssystem |
| Auftraggeber | Abteilung Buchhaltung |
| Auftragnehmer | IT-Abteilung / interner IT-Dienstleister |
| Gültigkeitsbereich | Alle Arbeitsplätze der Buchhaltungsabteilung |

**Serviceverfügbarkeit**

| Zeitraum | Anforderung |
| --- | --- |
| Standard (regulärer Betrieb) | 08:00 - 18:00 Uhr, Mo-Fr (5x10) |
| Kritischer Zeitraum (Monatsabschluss) | 06:00 - 22:00 Uhr, inkl. Wochenende, letzter und erster Arbeitstag je Monat |
| Verfügbarkeit gesamt | \>= 99,0 % (Jahresdurchschnitt) |
| Verfügbarkeit kritischer Zeitraum | \>= 99,7 % |

_Zur Einordnung:_ 99,7 % Verfügbarkeit entspricht einer maximalen Ausfallzeit von **ca. 26 Minuten pro Monat in diesem Zeitraum**.

**Störungspriorisierung und Reaktionszeiten**

| Priorität | Auslöser | Reaktionszeit | Lösungszeit |
| --- | --- | --- | --- |
| Hoch (kritisch) | Systemausfall während Monatsabschluss | <= 10 Min. | <= 30 Min. |
| Mittel | Eingeschränkte Funktion, kein Totalausfall | <= 30 Min. | <= 4 Std. |
| Niedrig | Allgemeine Anfrage, kein Betriebsausfall | <= 4 Std. | <= 1 Werktag |

Störungen, die während der Abrechnungsphase (Übergang Monatsende/-anfang) auftreten, werden automatisch als "hoch (kritisch)" eingestuft und erhalten Vorrang gegenüber allen anderen offenen Tickets.

**Eskalation**

Kann ein Incident der Priorität "hoch" nicht innerhalb von 30 Minuten durch den First-Level-Support (SL1) behoben werden, erfolgt unmittelbar die funktionale Eskalation an den Second-Level-Support (SL2). Bei weiter ausbleibendem Erfolg innerhalb von 60 Minuten wird hierarchisch die IT-Leitung einbezogen.

**Weitere Anforderungen**

- _Datensicherung:_ tägliches Backup, Wiederherstellung innerhalb von 4 Stunden möglich
- _Datenschutz:_ Zugriff nur für autorisierte Mitarbeiter der Buchhaltung (DSGVO-konform)
- _Wartungsfenster:_ ausschließlich außerhalb der kritischen Abrechnungsphasen, nach Absprache mit der Abteilungsleitung Buchhaltung
- _Kommunikationskanal:_ Störungsmeldungen per Ticketsystem und Telefon-Hotline

**Messgrößen / KPI**

- Einhaltung der Verfügbarkeitsquote (monatlicher Report)
- Anteil gelöster Tickets innerhalb der vereinbarten Lösungszeiten
- Anzahl der Eskalationen pro Monat

---

### P3: Definiere 3 SLIs für den Dienst "Internet-Zugang". (K3)

Prüfung durch:

- regelmäßige Pings, bspw. an DNS-Server
- reibungslosen Zugriff auf einen Browser
- metering, um die Stabilität und gleichbleibende Geschwindigkeit zu bestimmen

---

### P4: Berechne die erlaubte Ausfallzeit bei einer Verfügbarkeit von 99,5 % pro Monat. (K3)

Dies ist ohne weitere Rahmenbedingungen nicht einfach zu beantworten, da zunächst Monate nicht immer die gleichen Anzahl an Tagen haben und darüber hinaus nicht definiert ist, ob es hier lediglich um Geschäftszeiten geht oder doch der gesamte Zeitraum betrachtet werden soll.

Ich fahre also fort, indem ich vom gesamten Zeitraum ausgehe und ein Monat im Schnitt 30 Tage lang ist:

$30×0,005=0,15 Tage$ dies beschreibt den maximal erlaubten Ausfallzeitraum.

$0,15×24×60=216Minuten$ hier in einer etwas verständlicheren EInheit.

---

### P5: Erkläre, warum ein OLA notwendig ist, um ein SLA einzuhalten. (K2)

Wenn ich kein funktionierendes Küchenteam habe, so wird auch aus den besten Zutaten keine ordentliche Mahlzeit. Und erst recht keine, die vom Kunden angefragt wurde.

---

## Freiwillige Aufgaben

### Z1: Entwirf ein Dashboard zur Visualisierung von SLIs in Echtzeit. (K5)

---

### Z2: Analysiere die Konsequenzen von SLA-Verletzungen (Pönalen). (K4)

---

### Z3: Diskutiere den Begriff "Watermelon Effect" im Service Reporting. (K5)

---