# Philipp

Als angehender Cloud Administrator möchte ich die spezifischen Sicherheitsherausforderungen und Verantwortlichkeiten in der Cloud verstehen, damit ich Cloud-Umgebungen sicher konfigurieren und betreiben kann.

# Celebration Criteria

- Wir können das Shared-Responsibility-Modell für IaaS, PaaS und SaaS grafisch darstellen und erklären.
- Wir können mindestens drei häufige Sicherheitsrisiken in der Cloud benennen
- Wir können den Zweck von fundamentalen Cloud-Sicherheits-Tools wie IAM (Identity and Access Management) und Security Groups/NSGs erklären.

# Wissens-Briefing

Sicherheit in der Cloud funktioniert anders als im eigenen Rechenzentrum. Das wichtigste Konzept ist das **Shared Responsibility Modell (Modell der geteilten Verantwortung)**. Es definiert, wofür der Cloud-Anbieter (z.B. Amazon, Microsoft) und wofür der Kunde verantwortlich ist.

- **IaaS (Infrastructure as a Service):** Der Anbieter ist für die physische Sicherheit (Rechenzentrum, Server-Hardware) verantwortlich. Der Kunde ist für fast alles andere verantwortlich (Betriebssystem, Netzwerk-Konfiguration, Anwendungen, Daten).
- **PaaS (Platform as a Service):** Der Anbieter kümmert sich zusätzlich um das Betriebssystem und die Laufzeitumgebung. Der Kunde ist für die Sicherheit seiner Anwendung und Daten verantwortlich.
- **SaaS (Software as a Service):** Der Anbieter ist für fast alles verantwortlich. Der Kunde ist hauptsächlich für die Verwaltung der Benutzer und die sichere Nutzung der Software verantwortlich. **Fazit:** Der Kunde ist IMMER für seine Daten, Identitäten und Zugriffsrechte verantwortlich. Die häufigsten Sicherheitsprobleme in der Cloud sind nicht Hacker, die den Anbieter knacken, sondern **Fehlkonfigurationen durch den Kunden**.

# Aufgaben

1. **Modell erklären:** Findet online die Grafiken zum Shared Responsibility Modell von Microsoft Azure und AWS. Vergleicht sie und erklärt in eigenen Worten die wesentlichen Unterschiede und Gemeinsamkeiten.+++ columnContainer +++  
  +++ column xs:12 md:6 lg:6 +++  
  Microsoft![Diagramm zeigt Zuständigkeitszonen.](https://learn.microsoft.com/de-de/azure/security/fundamentals/media/shared-responsibility/shared-responsibility.svg)  
  +++ end:column ++++++ column xs:12 md:6 lg:6 +++  
  AWS![](files/019cee46-b790-75e5-a1b9-41216863c794/image.png)  
  +++ end:column +++  
  +++ end:columnContainer +++Im Gegensatz zu Microsoft teilt AWS die Verantwortung konkret und klar auf. Bei Amazon ist der Kunde komplett und eigenständig für die Sicherheit IN der Cloud zuständig, während AWS die Sicherheit DER Cloud gewährleistet. Microsoft hingegen unterscheidet je nach Anwendungsfall: Die Verantwortungsbereiche des Kunden vergrößern sich mit zunehmender Inanspruchnahme angebotener Infrastruktur und Services. Beim SaaS ist der Kunde lediglich für die Daten- und Endgerätesicherheit verantwortlich, während bei einer On-Premise (vor Ort) Lösung sämtliche Verantwortung beim Kunden liegt.
2. **Szenario-Analyse:** Die "KreativKopf GmbH" will einen Webserver in der Cloud (IaaS) betreiben. Welche Sicherheitsaufgaben muss die Agentur selbst übernehmen? Listet mindestens fünf konkrete Punkte auf.  
  Wenn die KreativKopf einen Server über IaaS anmietet und nutzt, ist sie für nahezu alle Sicherheiten verantwortlich. Lediglich die physikalische Komponente bleibt beim Anbieter.  
  \- Datensicherheit eigenständig gewährleisten  
  \- Einrichtung sicherheitsrelevanter Mechanismen (z.B. Firewall)  
  \- Aktualisierungen der Software  
  \- Passwort- und Zugriffsrichtlinien erstellen & wahren  
  \- Netzwerk- und Betriebssystemkonfigurationen anpassen
3. **Fehlkonfiguration finden:** Recherchiert den Begriff "Offener S3 Bucket". Beschreibt, was das Problem ist und welches Schutzziel (V, I, V) hier hauptsächlich verletzt wird.  
  S3 bedeutet Simple Storage Service und ist eine simple Form der Datenspeicherung. Bei einem “offenen S3 Bucket” handelt es sich um eine frei zugängliche Datenablage (Bucket). Sofern man den Namen des Buckets kennt, kann man auf die hier hinterlegten Daten zugreifen, somit wird vornehmlich das Schutzziel der Vertraulichkeit verletzt. In einigen Fällen gibt es zudem auch “schreibbare” Buckets; hier können auch die anderen beiden Schutzziele - Integrität und Verfügbarkeit - bedroht werden (aufgrund Serverseitiger Back-Ups, aber eher lediglich Integrität). Schreibbare Buckets können aber auch ein Risiko darstellen, indem sie Malware verbreiten.

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 19 "Cloud Computing", Abschnitt 19.7 "Sicherheit und Datenschutz" (S. 840-844).
- **Online-Ressource:** [Microsoft - Geteilte Verantwortung in der Cloud](https://docs.microsoft.com/de-de/azure/security/fundamentals/shared-responsibility)
- **Online-Ressource:** [AWS - Modell der geteilten Verantwortung](https://aws.amazon.com/de/compliance/shared-responsibility-model/)