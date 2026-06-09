# Mohammed

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

> 1. **Modelle vergleichen:** Zeichnet ein einfaches Diagramm, das den **"Castle-and-Moat"**\-Ansatz darstellt, und ein weiteres, das die Zero-Trust-Prinzipien visualisiert. Stellt sie gegenüber.

:::success
![](files/019cee46-ba34-76a6-89b3-9465abe22bae/PDF_3_(1).png)![](files/019cee46-ba39-70d9-83cc-bd2c12b7e50d/image.png)
:::

:::success
### Der "Castle-and-Moat"-Ansatz (Die Burg)

Man könnte sich dies wie eine mittelalterliche Burg vorstellen. Es gibt eine dicke Mauer und einen tiefen Wassergraben **(die Firewall)**. Wer über die Zugbrücke (das **VPN**) kommt, ist "drinnen" und gilt als Freund.

- **Das Problem:** Wenn ein Spion (Hacker) es einmal über die Brücke geschafft hat, kann er sich in der ganzen Burg frei bewegen und alle Schätze plündern, weil ihm drinnen niemand mehr Fragen stellt.

### Der Zero-Trust-Ansatz (Der moderne Hochsicherheits-Check)

Hier gibt es keine schützende Außenmauer mehr. Man könnte sich das eher als einen modernen Flughafen vorstellen.

- **Das Prinzip:** Egal ob man von draußen kommt oder schon am Gate stehet: man muss an jedem Durchgang sein Ticket und sein Pass zeigen.
- **Die Grafik:** Ein Zero-Trust-Diagramm zeigt keinen „Schutzwall“ um eine Firma, sondern einen **kontrollierten Kanal**, der jedes Mal neu aufgebaut wird, wenn jemand auf ein Programm zugreift.
:::

> 2. **Szenario anwenden:** Wie würde sich der Zugriff eines Designers der "KreativKopf GmbH" aus dem Homeoffice auf den Cloud-Speicher in einem Zero-Trust-Modell vom traditionellen VPN-Zugriff unterscheiden? Welche Faktoren würden bei der Zugriffsentscheidung geprüft?

:::success
### Der traditionelle Weg (VPN)

1. Der Designer startet sein **VPN**.
2. Er gibt sein Passwort ein.
3. **Die Folge:** Er ist nun **"im Firmennetz"**. Er kann oft nicht nur auf den Cloud-Speicher zugreifen, sondern sieht im Netzwerk auch den Drucker, den Buchhaltungs-Server und andere Computer. Wenn sein Laptop infiziert ist, verbreitet sich der Virus ungehindert im ganzen **"Burghof".**

### Der moderne Weg (Zero Trust)

Es gibt keinen **"Generalschlüssel" (VPN)** mehr. Bei jedem Klick auf den Cloud-Speicher entscheidet ein System im Hintergrund neu.

**Folgende Faktoren werden bei jeder Zugriffsentscheidung geprüft:**

- **Identität:** Ist es wirklich der Designer? (Bestätigt durch MFA).
- **Gerätezustand:** Ist der Laptop virenfrei und auf dem neuesten Stand? (Managed Device).
- **Standort/Netzwerk:** Kommt die Anfrage aus einem bekannten Land oder plötzlich aus einer ganz anderen Weltregion?
- **Anwendung:** Will er wirklich nur auf den Speicher zugreifen oder versucht er, auf Datenbanken zuzugreifen, die ihn nichts angehen? (**Least Privilege**).
:::

> 3. **Diskussion:** Warum ist Multi-Faktor-Authentifizierung (MFA) eine absolut unverzichtbare Grundlage für jede Zero-Trust-Strategie?

:::success
In der alten Welt war das Passwort der König. In der Zero-Trust-Welt ist die **Identität das neue Perimeter** (die neue Grenze).

**Multi-Faktor-Authentifizierung (MFA)** ist deshalb unverzichtbar, weil:

1. **Passwörter schwach sind:** Sie werden erraten, gestohlen oder per Phishing erschlichen. Ein Passwort allein ist in einer Cloud-Welt kein Schutz mehr.
2. **Identität alles entscheidet:** Da wir bei Zero Trust keine **"sichere Burgmauer"** mehr haben, müssen wir uns zu 100 % sicher sein, dass die Person, die klopft, auch die ist, für die sie sich ausgibt.
3. **Hürden für Angreifer:** Selbst wenn ein Hacker das Passwort des Designers stiehlt, scheitert er am zweiten Faktor (z. B. einer App-Bestätigung auf dem Handy). Ohne MFA bricht das gesamte **"Never trust, always verify"**\-Kartenhaus sofort zusammen.
:::

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Zero Trust - Ein Überblick](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/CS/Konzeptstudien/Zero-Trust_Ueberblick.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Microsoft - Was ist Zero Trust?](https://docs.microsoft.com/de-de/security/zero-trust/zero-trust-overview)