# Jay

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

1. **Modell erklären:** Findet online die Grafiken zum Shared Responsibility Modell von Microsoft Azure und AWS. Vergleicht sie und erklärt in eigenen Worten die wesentlichen Unterschiede und Gemeinsamkeiten.  
  <br/>![Diagramm zeigt Zuständigkeitszonen.](https://learn.microsoft.com/de-de/azure/security/fundamentals/media/shared-responsibility/shared-responsibility.svg)![](files/019cee46-b43f-74ef-a0c1-6fabe65f4339/image.png)
2. **Szenario-Analyse:** Die "KreativKopf GmbH" will einen Webserver in der Cloud (IaaS) betreiben. Welche Sicherheitsaufgaben muss die Agentur selbst übernehmen? Listet mindestens fünf konkrete Punkte auf.  
  \- Least Privilege für Users  
  \- Keine Root-Accounts im Alltag  
  \- MFA (Multi-Faktor-Authentifizierung)  
  \- Virtuelle Firewalls  
  \- Backup  
  \- Patchen und Absichern des Betriebssystems

**Fehlkonfiguration finden:** Recherchiert den Begriff "Offener S3 Bucket". Beschreibt, was das Problem ist und welches Schutzziel (V, I, V) hier hauptsächlich verletzt wird.  
<br/>Ein **offener S3-Bucket** ist ein ==Amazon Simple Storage Service (S3)-Container, der so konfiguriert ist, dass er== **\==öffentlich zugänglich==** ==ist==, was bedeutet, dass jedermann über eine URL darauf zugreifen, Dateien herunterladen und sogar den Inhalt auflisten kann, ohne sich authentifizieren zu müssen  
<br/>**Schutzziel:** Vertraulichkeit kann hierbei verletzt werden, wenn es sich um Kundendaten handelt oder personenbezogne daten handelt da jeder zugriff auf die Daten hat ohne sich vorher zu authentifizieren. Integrität wird hier dann auch nur verletzt wenn jeder mit zugriff auch die Daten bearbeiten kann. ( Dies bietet die Möglichkeit die Daten zu manipulieren)

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 19 "Cloud Computing", Abschnitt 19.7 "Sicherheit und Datenschutz" (S. 840-844).
- **Online-Ressource:** [Microsoft - Geteilte Verantwortung in der Cloud](https://docs.microsoft.com/de-de/azure/security/fundamentals/shared-responsibility)
- **Online-Ressource:** [AWS - Modell der geteilten Verantwortung](https://aws.amazon.com/de/compliance/shared-responsibility-model/)