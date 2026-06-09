# LF6.3.7- Der Dienstleistungskatalog

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

**Als Service-Designer_in möchte ich einen IT-Dienstleistungskatalog erstellen, damit das Serviceangebot für Kunden und IT-Mitarbeiter transparent dargestellt wird.**

## ✅ Celebration Criteria (Lernziele)

- Ich kann den Zweck eines Dienstleistungskatalogs erläutern. (K2)
- Ich kann zwischen der Business-Sicht und der technischen Sicht eines Katalogs unterscheiden. (K2)
- Ich kann eine Dienstleistung katalogfähig beschreiben. (K3)

## ⚠️ Typische Fallstricke & Impulsfragen

- **Techniker-Jargon:** Der Katalog beschreibt "Provisionierung von VM-Instanzen" statt "Beantragung eines virtuellen PCs". -> _Impuls:_ Wer ist die Hauptzielgruppe des Katalogs?
- **Veraltete Inhalte:** Services werden angeboten, die technisch gar nicht mehr unterstützt werden. -> _Impuls:_ Wer ist im Team für die Pflege des Katalogs verantwortlich?

## 🛠️ Pflichtaufgaben (Training)

1. Skizziere die Struktur eines modernen, webbasierten Service-Katalogs. (K3)
2. Erstelle eine Business-Beschreibung für den Dienst "Home-Office Paket". (K3)
3. Erstelle die zugehörige technische Sicht (Benötigte Ressourcen/Server) für den gleichen Dienst. (K3)
4. Liste 4 Kategorien auf, in die ein Katalog unterteilt werden sollte. (K2)
5. Beschreibe den Prozess, wie ein neuer Dienst in den Katalog aufgenommen wird. (K2)

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

1. Gestalte einen interaktiven Prototyp eines Katalogs (z. B. mit Draw.io oder Markdown-Links). (K5)
2. Evaluiere den Einsatz von Verrechnungspreisen im Dienstleistungskatalog. (K6)
3. Untersuche die Verknüpfung zwischen Dienstleistungskatalog und Request Fulfillment. (K4)

## 🔗 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann LF6:** Lernsituation 1 "Services im IT-Bereich beschreiben".
- **Rheinwerk:** Sektion "Service Catalogue Management".

### 🔍 Web (Suchwortliste)

- **Design:** `Service Catalog Business vs Technical View`
- **Struktur:** `ITIL 4 Service Catalogue Practice`

</details>

# Lösungen

## Pflichtaufgaben

### P1: Skizziere die Struktur eines modernen, webbasierten Service-Katalogs. (K3)

Die Inhalte sollten so strukturiert sein, dass der Kunde schon auf den ersten Blick alles Wichtige sieht:

- Exakte, kurze, On-Point Beschreibung (Name) des Services
- Vollständige oder “aufklappbare” Liste der Inhalte des Pakets oder Services
- Die SLA-Details (Wann ist alles bereitgestellt? Wie schnell wird geholfen?)
- Die Kosten
- Optional: Berechtigungsbezug/Level (Wer darf bestellen?)

Eine ausgearbeitet UX-Struktur für einen solchen Katalog könnte wie folgt aussehen:

| Ebene | Element | Funktion |
| --- | --- | --- |
| Header | Globale Suche | Echtzeit-Suche (Filterung "live") |
| Navigation | Service-Baum | Kategorisierung wie "Arbeitsplatz", "Software", "Netzzugang" oder "Cloud-Services"  In der Ansichtsliste sind die oben beschriebenen Daten für jedes Item zu sehen |
| Zusätzliche Ansicht | Service-Karten | Liste der Treffer mit "Quickview"-Button für einen schnellen Überblick |
| Detailseite | Service-Profil | Vollständige Beschreibung, technische Voraussetzungen und "In den Warenkorb" |

---

### P2: Erstelle eine Business-Beschreibung für den Dienst "Home-Office Paket". (K3)

- **Titel:** Home-Office Paket - für sicheres und effizientes Arbeiten von Zuhause
- **Beschreibung:** Durch den Erhalt und die Nutzung dieses Pakets, können Sie ohne Weiteres Ihre Arbeit von Zuhause oder sogar einem anderen Ort erledigen. Alles wird entsprechend vor konfiguriert, damit Sie sich direkt auf das Wesentliche konzentrieren können und nicht erst wichtige Zeit mit der Einrichtung verlieren. Sie erhalten ein System (Laptop), das direkt in ihr gewohntes Arbeitsnetzwerk integriert ist. So können Sie auch von Zuhause aus fast genauso arbeiten, als wären Sie im Büro.  
  Sollten während der Einrichtung oder des Betriebs widererwartend Störungen auftreten, garantieren wird Ihnen Unterstützung innerhalb der vereinbarten Service-Zeiten.
- **Inhalt (Soft- & Hardware, Services, etc.):** Liste aller beinhalteten Komponenten, wie etwa Laptop, dessen Software und welche Services dazugehören.
- **(technische) Voraussetzungen:** “Anforderungen” an den Kunden, also “was muss vorhanden sein?” oder “was sollte man wissen?” oder “welche Position notwendig ist?”
- **SLAs:** Hier wird der grundsätzliche Rahmen der Services und Service-Zeiten festgelegt.
- **Kosten:** Am Ende natürlich der Preis.

---

### P3: Erstelle die zugehörige technische Sicht (Benötigte Ressourcen/Server) für den gleichen Dienst. (K3)

| Kategorie | Konkrete Komponenten |
| --- | --- |
| Hardware | Laptop (Office-Modell), ggf. Headset, Webcam, Dockingstation |
| Betriebssystem (OS) | bspw. Windows 11 Image |
| Software-Pakete | Alle benötigten Office-Programme: bspw. Microsoft 365 Suite, Browser (Chrome/Edge), Adobe Acrobat |
| Netzwerk & Security | VPN-Client, Antivirus-Software, Zertifikate |
| Identität & Zugriff | Benutzerkonto im Active Directory, Berechtigung für Remote-Zugriff |

---

### P4: Liste 4 Kategorien auf, in die ein Katalog unterteilt werden sollte. (K2)

- Arbeitsplatz & Hardware
- Applikationen & Software
- Kommunikation & Netzwerk
- Support & Infrastruktur

---

### P5: Beschreibe den Prozess, wie ein neuer Dienst in den Katalog aufgenommen wird. (K2)

1. **Definition & Business Case:** Hier findet u.a. die Bedarfs- und Ressourcenprüfung statt.
2. **Design:** Wie oben beispielhaft geschehen, erstellt man nun die technische und Business-Sicht.
3. **Transition:** Der Service wird zunächst “versteckt” eingebunden und getestet. Wie eine Demo.
4. **Aktivierung:** Der Dienst wird nach erfolgreichem Testen nun auch aktiv geschaltet und ist für Kunden zugriffsbereit.

---

## Freiwillige Aufgaben

### Z1: Gestalte einen interaktiven Prototyp eines Katalogs (z. B. mit [Draw.io](http://Draw.io) oder Markdown-Links). (K5)

## Unsere Services

### Arbeitsplatz & Hardware

<details>
<summary>Mehr dazu…</summary>

Einen oder mehrere Laptops anfordern

Einen oder mehrere Desktop-PCs anfordern

Andere Geräte anfordern

</details>

### Applikationen & Software

<details>
<summary>Mehr dazu…</summary>

Eine oder mehrere Software-Lizenzen anfordern

Software-Lizenzverträge verlängern

Software-Lizenzverträge kündigen

Wunsch für eine bestimmte Applikation

</details>

### Kommunikation & Netzwerk

<details>
<summary>Mehr dazu…</summary>

Netzwerk einrichten

Virtuelles (simuliertes) Netzwerk einrichten (bspw. für “Home-Office”)

Internes Sprachnetz einrichten

Rund um das WLAN (kabelloses Netzwerk)

</details>

### Support & Infrastruktur

<details>
<summary>Mehr dazu…</summary>

Störung melden

Datensicherheit (Redundanz)

Datenschutz (Sicherheit)

Eskalationsgesuch

</details>

---

### Z2: Evaluiere den Einsatz von Verrechnungspreisen im Dienstleistungskatalog. (K6)

---

### Z3: Untersuche die Verknüpfung zwischen Dienstleistungskatalog und Request Fulfillment. (K4)