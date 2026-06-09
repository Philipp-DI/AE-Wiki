# Jay

# LF4.3.2- Zero Trust- Vertraue niemandem

Als Junior Network Security Engineer

möchte ich die Prinzipien von Zero Trust verstehen,

damit ich moderne Sicherheitsarchitekturen entwerfen kann, die nicht mehr auf veralteten Perimetermodellen basieren.

# Celebration Criteria

- Wir können das traditionelle "Castle-and-Moat"-Sicherheitsmodell dem Zero-Trust-Ansatz gegenüberstellen.
- Wir können die drei Kernprinzipien von Zero Trust ("Verify explicitly", "Use least privilege access", "Assume breach") erklären.
- Wir können die zentrale Rolle von Identität und Multi-Faktor-Authentifizierung (MFA) in einer Zero-Trust-Architektur begründen.

# Wissens-Briefing

Das traditionelle Sicherheitsmodell **("Castle-and-Moat" / Burg und Graben)** geht davon aus, dass alles innerhalb des Unternehmensnetzwerks vertrauenswürdig ("innen") und alles außerhalb bösartig ("außen") ist. Eine starke Firewall schützt die Grenze. Dieses Modell versagt, sobald ein Angreifer einmal "drin" ist (z.B. durch eine Phishing-Mail) oder wenn es keine klare Grenze mehr gibt (Remote-Arbeit, Cloud-Dienste).

**Zero Trust** ist eine moderne Sicherheitsstrategie, die auf dem Grundsatz **"Never trust, always verify" (Vertraue niemals, überprüfe immer)** basiert. Es gibt kein "innen" oder "außen" mehr. Jeder Zugriff, egal von wo, wird als potenziell feindlich betrachtet und muss authentifiziert und autorisiert werden.

**Kernprinzipien:**

1. **Verify explicitly (Explizit überprüfen):** Jeder Zugriffsversuch wird basierend auf allen verfügbaren Datenpunkten (Identität, Standort, Geräte-Sicherheit, Dienst) authentifiziert und autorisiert.
2. **Use least privilege access (Zugriff mit geringsten Rechten):** Benutzer erhalten nur die minimalen Berechtigungen, die sie für ihre Arbeit benötigen (Just-in-Time und Just-Enough-Access).
3. **Assume breach (Von einer Kompromittierung ausgehen):** Man geht davon aus, dass der Angreifer bereits im Netzwerk ist. Daher wird der Netzwerkverkehr segmentiert, um die Ausbreitung zu minimieren, und alles wird protokolliert und analysiert.

# Aufgaben

1. **Modelle vergleichen:** Zeichnet ein einfaches Diagramm, das den "Castle-and-Moat"-Ansatz darstellt, und ein weiteres, das die Zero-Trust-Prinzipien visualisiert. Stellt sie gegenüber.  
  <br/><br/>![](files/019cee46-b990-7118-bf51-bfeba4c997a0/Gemini_Generated_Image_ib9zbvib9zbvib9z.png)

**Szenario anwenden:** Wie würde sich der Zugriff eines Designers der "KreativKopf GmbH" aus dem Homeoffice auf den Cloud-Speicher in einem Zero-Trust-Modell vom traditionellen VPN-Zugriff unterscheiden? Welche Faktoren würden bei der Zugriffsentscheidung geprüft?  
<br/>**Antwort nach zusammenarbeit mit meinem Gemini Gem. (Bitte nicht überprüfen fall nicht notwendig/Ich habe alles verstanden. Falls nötig fasse ich die Antwort mit eigenen Worten zusammen.)**  
<br/>**Lerninhalt vom Gem:** Moin! Hier ist wieder **BruddaJay**. Das ist ein richtig gutes Szenario, das die "KreativKopf GmbH" da vorhat. Der Schritt in die Cloud und hin zu Zero Trust ist modern, aber für Quereinsteiger oft erstmal abstrakt.

Lass uns das **Zugriffsszenario** für den Designer im Homeoffice mal genau unter die Lupe nehmen. Ich erkläre dir den Unterschied zwischen dem "alten" VPN und dem modernen Zero Trust so, dass du es sofort verstehst – mit einem einfachen Vergleich und dann den technischen Fakten.

---

### Der Vergleich: Die "Burg" vs. der "VIP-Club"

Um das Prinzip zu verstehen, stell dir Folgendes vor:

- Traditionelles VPN (Castle & Moat):Das Firmennetzwerk ist wie eine Burg. Der Designer hat den Schlüssel für das Haupttor (VPN-Passwort). Sobald er durch das Tor ist (VPN-Verbindung steht), ist er "drinnen". Er kann sich im Innenhof relativ frei bewegen. Wenn er jetzt "krank" ist (sein Laptop hat einen Virus), kann er alle anderen in der Burg anstecken, weil die Mauern nur außen sind.
- Zero Trust (Never Trust, Always Verify):Es gibt keine Burg mehr. Die Daten liegen in einem Hochsicherheits-VIP-Club (Cloud). Es gibt keinen Schlüssel für die Eingangstür. Stattdessen steht vor jeder einzelnen Tür (jeder Datei, jeder App) ein Türsteher. Der Türsteher prüft nicht nur den Ausweis, sondern auch, ob der Designer gesund aussieht, ob er nüchtern ist und ob er überhaupt auf der Gästeliste für genau diesen Raum steht.

---

### Szenario: Der Designer greift auf den Cloud-Speicher zu

Hier ist der direkte Vergleich der Abläufe, wenn der Designer eine Grafikdatei öffnen will.

#### A) Der traditionelle Weg (VPN)

1. **Verbindung:** Der Designer startet seinen Laptop und aktiviert den **VPN-Client**.
2. **Authentifizierung:** Er gibt Benutzername und Passwort ein (vielleicht noch einen 2. Faktor).
3. **Der Tunnel:** Ein verschlüsselter Tunnel ins Firmennetzwerk wird aufgebaut. Der Laptop ist nun logisch Teil des Firmennetzwerks.
4. **Zugriff:** Der Designer öffnet den Dateiserver. Da er "im Netz" ist, vertraut das System ihm weitestgehend.
5. **Risiko:** Wenn der Designer auf eine Phishing-Mail geklickt hat und Malware auf dem Laptop ist, kann diese Malware nun durch den Tunnel ins Firmennetz kriechen und andere Server scannen (Sicherheitsrisiko!).

#### B) Der Zero Trust Weg (Modern)

1. **Anfrage:** Der Designer öffnet direkt den Browser oder die Cloud-App (z. B. OneDrive/SharePoint/AWS S3). Er baut _keinen_ generellen Tunnel auf.
2. **Die Prüfung (Policy Engine):** Bevor er die Datei sieht, prüft das System im Hintergrund massive viele Faktoren (siehe Punkt 3).
3. **Entscheidung:** Das System sagt: "Okay, das ist wirklich der Designer, sein Laptop ist sicher, er darf _nur_ diese Design-Dateien sehen."
4. **Zugriff:** Der Zugriff wird **nur für diese Sitzung und diese Datei** gewährt.
5. **Vorteil:** Selbst wenn der Laptop Malware hat, würde das Zero-Trust-System merken: "Halt, der Laptop verhält sich komisch" oder "Der Virenscanner ist aus" und den Zugriff sofort blockieren. Die Malware kommt nicht an andere Systeme.

---

### Welche Faktoren werden bei Zero Trust geprüft?

In deinem Szenario (KreativKopf GmbH) würde die "Policy Engine" (der Entscheider) folgende Signale prüfen, bevor der Designer Zugriff erhält. Das geht weit über ein einfaches Passwort hinaus.

Hier ist eine Checkliste, wie sie in der Praxis (und teils im BSI-Grundschutz angedeutet) aussieht:

#### 👤 1. Identität (Wer bist du?)

- **Benutzer-Credentials:** Stimmen Name und Passwort?
- **MFA (Multi-Faktor-Authentifizierung):** Wurde der zweite Faktor bestätigt (z. B. App oder Token)? _Das BSI empfiehlt dies dringend, um Identitätsdiebstahl zu erschweren_.
- **Verhalten (User Behavior):** Meldet sich der Designer wie gewohnt um 9:00 Uhr aus Berlin an, oder plötzlich um 3:00 Uhr nachts aus Nordkorea? (Anomalie-Erkennung).

#### 💻 2. Geräte-Gesundheit (Device Health)

- **Ist das Gerät bekannt?** Handelt es sich um den verwalteten Firmen-Laptop oder das private iPad der Tochter? (Stichwort: "Bring Your Own Device" Risiken).
- **Sicherheitsstatus:**
  - Ist der Virenscanner aktuell und aktiv?
  - Ist die Firewall auf dem Laptop an?
  - Sind die neuesten Sicherheitsupdates (Patches) für das Betriebssystem installiert? _Veraltete Software ist ein riesiges Einfallstor_.
- **Verschlüsselung:** Ist die Festplatte verschlüsselt?.

#### 🌐 3. Netzwerk & Kontext

- **Standort:** Kommt die Anfrage aus einem unsicheren öffentlichen WLAN (Café) ohne Verschlüsselung? _Hier warnt der Grundschutz vor dem Abhören_.
- **IP-Adresse:** Ist die IP-Adresse vertrauenswürdig oder auf einer Blacklist?

#### 📦 4. Daten-Sensibilität (Data Classification)

- **Was wird angefragt?** Will er nur das Kantinen-Menü sehen (Niedriges Risiko) oder die geheimen neuen Produktentwürfe (Hohes Risiko / "Vertraulichkeit sehr hoch")?
- _Zero Trust entscheidet dynamisch:_ Für das Menü reicht das Passwort. Für die Entwürfe muss das Gerät 100% sicher sein und MFA bestätigt werden.

---

### 4\. Zusammenfassung für die KreativKopf GmbH

Warum ist das für dein Szenario wichtig?

1. **Gegen Phishing:** Da Mitarbeiter immer noch auf Mails hereinfallen, hilft Zero Trust. Selbst wenn ein Hacker das Passwort klaut (Identitätsdiebstahl), kommt er nicht rein, weil ihm der "Gesunde Firmen-Laptop" (Geräte-Faktor) fehlt.
2. **Gegen Open-Source-Risiken:** Wenn eine Software-Bibliothek kompromittiert ist und eine Anwendung "kapert", verhindert Zero Trust (durch Segmentierung), dass diese Anwendung auf alles andere zugreifen darf.
3. **Remote Work:** Der Designer kann sicher arbeiten, egal wo er ist, weil die Sicherheit nicht mehr am "Standort Büro", sondern an "Identität und Gerät" hängt.

---

### Eine Risiko-Tabelle erstellen, welche konkreten Gefahren (aus dem Text) durch Zero Trust gemindert werden

|     |     |     |
| --- | --- | --- |
| Gefahr / Szenario | BSI-Hintergrund & Fakten (aus dem Text) | Lösung durch Zero Trust (Die "Policy Engine") |
| **1\. Phishing & Identitätsdiebstahl** _(Mitarbeiter klicken auf Phishing-Mails)_ | "84% aller betrügerischen E-Mails waren Phishing-E-Mails". Cyberkriminelle wollen Zugangsdaten "abfischen" (Phishing), um Identitätsdiebstahl zu begehen. | **Faktor: Starke Authentifizierung (MFA)** Selbst wenn der Angreifer das Passwort durch Phishing erbeutet hat, kommt er nicht rein. Zero Trust verlangt zwingend einen **zweiten Faktor** (z. B. Handy-App) und prüft oft auch den Standort. Ohne den zweiten Faktor ist das Passwort nutzlos. |
| **2\. Malware auf Endgeräten** _(Designer-Laptop infiziert)_ | "Etwa 70% aller Malware-Ausbrüche hatten ihren Ursprung in den Geräten". Malware kann sich über vernetzte Computer schnell im ganzen Netz verbreiten. | **Faktor: Device Health (Gerätegesundheit)** Bevor der Zugriff auf die Cloud erlaubt wird, prüft das System den Laptop. Meldet der Virenscanner ein Problem oder fehlen Updates, wird der **Zugriff verweigert**. Die Malware bleibt auf dem Laptop isoliert und kommt nicht in die Cloud. |
| **3\. Unsichere Software-Bibliotheken** _(Sorge um Open-Source-Sicherheit)_ | Dies fällt unter "Software-Schwachstellen oder -Fehler" (G 0.28). Angreifer nutzen Schwachstellen aus, um Systeme zu übernehmen (Exploits). | **Prinzip: Least Privilege (Wenigste Rechte)** Zero Trust segmentiert (trennt) Anwendungen. Wenn eine Grafik-Software durch eine Bibliothek kompromittiert wird, darf sie trotzdem **nur** auf Grafik-Dateien zugreifen und nicht plötzlich auf die Buchhaltung oder Kundendatenbank. Der Schaden wird begrenzt. |
| **4\. Unsicheres Homeoffice-Netz** _(Designer arbeitet von zuhause/Café)_ | Gefahr durch "Abhören" (G 0.15) oder "Man-in-the-Middle-Angriffe", bei denen sich jemand in die Kommunikation einschleicht. | **Faktor: Verschlüsselung & Kein Netz-Vertrauen** Zero Trust vertraut _keinem_ Netzwerk, egal ob Büro oder Café. Jede Verbindung ist **Ende-zu-Ende verschlüsselt** (z. B. via TLS). Ein Angreifer im gleichen WLAN kann die Daten nicht mitlesen. |
| **5\. Ransomware** _(Verschlüsselungstrojaner)_ | "Ransomware ist weiterhin die größte Bedrohung". Sie schränkt den Zugriff auf Daten ein (Verfügbarkeit) und erpresst Lösegeld. | **Prinzip: Ständige Verifikation** Ransomware versucht oft, sich "seitwärts" durchs Netz zu bewegen, um alles zu verschlüsseln. Zero Trust prüft bei _jedem_ neuen Dateizugriff erneut. Das ungewöhnlich schnelle Öffnen tausender Dateien (typisch für Ransomware) würde als Anomalie erkannt und blockiert werden. |

1. **Diskussion:** Warum ist Multi-Faktor-Authentifizierung (MFA) eine absolut unverzichtbare Grundlage für jede Zero-Trust-Strategie?  
  <br/>Angenommen, ein Passwort ist wie ein Hausschlüssel. Das Problem: Schlüssel können nachgemacht, geklaut oder einfach irgendwo liegen gelassen werden (genau wie Passwörter durch Phishing).**MFA** ist aus drei Gründen der "Türsteher" bei Zero Trust:
  
  1. **Ein Passwort allein ist nichts mehr wert:** Bei Zero Trust gilt das Prinzip "Vertraue niemandem". Nur weil jemand das richtige Passwort eintippt, glaubt das System noch lange nicht, dass es auch wirklich der Designer ist. Die MFA ist der Beweis (z. B. ein Code auf dem Handy), den ein Hacker im Ausland trotz Phishing-Passwort meistens nicht hat.
  2. **Schutz vor "menschlichen Fehlern":** Da die Mitarbeiter der KreativKopf GmbH ja leider immer noch auf Phishing-Mails klicken, ist MFA der Rettungsanker. Selbst wenn der Mitarbeiter sein Passwort auf einer Fake-Seite eingibt, kommt der Angreifer ohne den zweiten Faktor nicht ins System.
  3. **Identität ist die neue Grenze:** Früher war die Firewall (das Bürogebäude) der Schutz. Heute arbeiten alle im Homeoffice oder in der Cloud. Die Identität ist das Einzige, was wir noch kontrollieren können – und MFA macht diese Identität erst halbwegs sicher.
  
  **Kurz gesagt:** Ohne MFA ist Zero Trust wie eine Hochsicherheitstür, bei der man den Schlüssel unter die Fußmatte legt. Es bringt einfach nichts.

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Zero Trust - Ein Überblick](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/CS/Konzeptstudien/Zero-Trust_Ueberblick.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Microsoft - Was ist Zero Trust?](https://docs.microsoft.com/de-de/security/zero-trust/zero-trust-overview)