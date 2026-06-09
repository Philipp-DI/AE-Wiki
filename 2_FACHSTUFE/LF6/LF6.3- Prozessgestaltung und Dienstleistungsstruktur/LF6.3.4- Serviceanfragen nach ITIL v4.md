# LF6.3.4- Serviceanfragen nach ITIL v4

:::warning
➕ Du hast alle Pflicht- und Zusatzaufgaben bearbeitet und dir sichtlich Gedanken zum Thema gemacht. Dein Ansatz bei P5 bringt die Vorteile eines Portals gut auf den Punkt.

➖ Bei Aufgabe P1 hast du leider ein wichtiges Kernkonzept von ITIL missverstanden: Die Fälle "Der PC geht nicht mehr an" und "Wifi schwächelt" sind keine Serviceanfragen (Requests), sondern handfeste **Störungen (Incidents)**, da hier ein bestehender Dienst unterbrochen ist.

➖ Auch deine Beschreibung des Genehmigungsverfahrens (P4) mit "Hardware-Tokens wie beim Banktransfer" geht völlig an der betrieblichen Realität vorbei. In der Praxis geht es hier um Budgetfreigaben und Workflows im ITSM-Tool, nicht um kryptografische Schlüsseltransfers.

💡 Bitte lies dir die Abgrenzung zwischen Incident (Etwas ist kaputt und muss repariert werden) und Service Request (Ein Standard-Service wird beantragt, z.B. eine neue Maus) noch einmal genau durch. Standard-Changes (P3) sind zudem vorab genehmigte, risikoarme Änderungen durch die IT, nicht zwingend Aufgaben, die der Nutzer selbst durchführt.
:::

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

**Als Service-Desk-Mitarbeiter_in möchte ich Serviceanfragen (Service Requests) nach ITIL-Standard bearbeiten, damit Routineaufgaben effizient und zur Kundenzufriedenheit erledigt werden.**

## ✅ Celebration Criteria (Lernziele)

- Ich kann den Begriff "Service Request" nach ITIL v4 definieren. (K2)
- Ich kann den Standard-Workflow für eine Serviceanfrage beschreiben. (K2)
- Ich kann Serviceanfragen von Störungen abgrenzen. (K3)

## ⚠️ Typische Fallstricke & Impulsfragen

- **Incident-Request-Mix:** Eine Störung wird als Serviceanfrage erfasst, weil der User "einen funktionierenden PC will". -> _Impuls:_ Warum ist die korrekte Unterscheidung für die Statistik und die SLAs so wichtig?
- **Genehmigungs-Dschungel:** Der Prozess für eine neue Maus erfordert 5 Manager-Unterschriften. -> _Impuls:_ Ab wann schadet zu viel Kontrolle der Effizienz?

## 🛠️ Pflichtaufgaben (Training)

1. Erstelle eine Liste mit 5 typischen Serviceanfragen in deinem Szenario. (K3)
2. Zeichne den Weg einer Passwort-Zurücksetzung als Prozess. (K3)
3. Erkläre die Bedeutung von "Standard-Änderungen" (Standard Changes) im Support. (K2)
4. Entwirf ein Genehmigungs-Verfahren für eine Hardware-Bestellung. (K3)
5. Beschreibe, wie ein Serviceanfrage-Portal die Effizienz steigert. (K2)

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

1. Gestalte einen Self-Service-Katalog für häufige Anfragen. (K5)
2. Analysiere das Potenzial von Chatbots bei der Annahme von Anfragen. (K4)
3. Entwickle Kriterien für die automatische Genehmigung von Kleinst-Anfragen. (K5)

## 🔗 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann LF6:** Lernsituation 3 "Serviceanfragen entgegennehmen".
- **ITIL v4 Foundation:** Handbuch (Kapitel "Service Request Management").

### 🔍 Web (Suchwortliste)

- **Methodik:** `ITIL 4 Service Request Management Practice`
- **Abgrenzung:** `Unterschied Incident Service Request ITIL`

</details>

# Lösungen

## Pflichtaufgaben

### P1: Erstelle eine Liste mit 5 typischen Serviceanfragen in deinem Szenario. (K3)

1. Hilfe - ich kann mich nicht einloggen!
2. ~~Der PC geht nicht mehr an.~~ ← Incident, keine traditionelle Service-Anfrage (besser: Bestellung neues Toners für Office-Drucker)
3. Auftrag - Hardware-Einrichtung
4. ~~Wifi schwächelt~~ ← Incident, keine traditionelle Service-Anfrage (besser: Anfrage Erweiterung des Wifi Signals)
5. Software-Lizenz ungültig/abgelaufen.

---

### P2: Zeichne den Weg einer Passwort-Zurücksetzung als Prozess. (K3)

Link “Passwort vergessen oder zurücksetzen” klicken → E-Mail-Adresse eingeben → neues Passwort oder Link zum Zurücksetzen wird an die Adresse gesendet

Falls E-Mail betroffen ist, so muss man sich entweder mit einer alternativen E-Mail-Adresse verifizieren oder direkt an den Admin wenden.

---

### P3: Erkläre die Bedeutung von "Standard-Änderungen" (Standard Changes) im Support. (K2)

~~Standard-Änderungen sind vermutlich solche, die immer wieder aufkommen und der Nutzer im besten Fall alleine vornehmen kann.~~

Solche Änderungen sind vorab genehmigt und als risikoarm eingestuft, sodass sie automatisch und/oder zeitnah durchgeführt werden können.

---

### P4: Entwirf ein Genehmigungs-Verfahren für eine Hardware-Bestellung. (K3)

~~Ähnlich, wie bei einem Banktransfer werden “Hardware-Tokens” generiert, die die Bestellung berechtigen. Die Tokens werden dann auch ähnlich wie eine übliche Transaktion validiert, indem per geheimen Schlüssel die Tokens aufgelöst und bei Übereinstimmung erfolgreich eingelöst werden können.~~

Zunächst muss eine Budgetfreigabe erfolgen, die aufgrund einer entsprechenden Analyse angefertigt wird. Bei erfolgreicher Freigabe wird das Ganze dann durch die ITSM Workflows geleitet und im besten Falle am Ende der Kette bereitgestellt/genehmigt. Falls dem ITSM Probleme bspw. im Bereich der Machbarkeit o.ä. auffallen, kann das Verfahren dynamisch angepasst bzw. erweitert werden.

---

### P5: Beschreibe, wie ein Serviceanfrage-Portal die Effizienz steigert. (K2)

Feste Muster ermöglichen die Automatisierung und erleichtern die Einordnung der Priorisierung.

---

## Freiwillige Aufgaben

### Z1: Gestalte einen Self-Service-Katalog für häufige Anfragen. (K5)

FAQ bei einen Mitbewerber oder in ähnlichen Bereichen tätiger Unternehmen anschauen und diese zunächst als Basis für den eigenen Katalog nehmen. Falls es schon ausreichend Daten gibt, so kann und sollte man natürlich mit rein internen Daten arbeiten.

---

### Z2: Analysiere das Potenzial von Chatbots bei der Annahme von Anfragen. (K4)

Aus ethischer Sicht empfinde ich Chatbots als fragwürdig. Es kommt natürlich darauf an, wie man diese einsetzt. Wenn ich sie als eine reine, zusätzliche Option anbiete, dann bin ich der Meinung, dass man hier ein nützliches zusätzliches Tool hat. Sollte der Chatbot jedoch Anlaufstelle Nummer 1 sein, so gehen Arbeitsplätze flöten und Kunden müssen sich u.U. frustriert mit automatisch generierten Nachrichten rumschlagen.  
Aus rein wirtschaftlicher Sicht natürlich ein super Ding.

---

### Z3: Entwickle Kriterien für die automatische Genehmigung von Kleinst-Anfragen. (K5)

Sicherheitsstufenschwellenwerte akribisch festlegen und vordefinieren und anhand dessen, könnte man unter einer gewissen Schwelle die Automatisierung freischalten.