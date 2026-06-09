# LF4.3- Moderne Verteidigungsstrategien und Security Operations

Als Junior SecOps Engineer

möchte ich moderne Sicherheitskonzepte wie Zero Trust und Cloud Security verstehen und die Bedeutung des Faktors Mensch erkennen,

damit ich Unternehmen nicht nur nach etablierten Standards, sondern auch gegen aktuelle und zukünftige Bedrohungen schützen kann.

# Celebration Criteria

- Wir können das Zero-Trust-Sicherheitsmodell erklären und es vom traditionellen Perimeterschutz abgrenzen.
- Wir können das Shared-Responsibility-Modell für Cloud-Dienste (IaaS, PaaS, SaaS) erläutern und typische Cloud-Sicherheitsrisiken benennen.
- Wir können eine praxisnahe Maßnahme zur Förderung der Security Awareness in einem Unternehmen konzipieren.
- Wir können die Funktionsweise von Supply-Chain-Angriffen und KI-gestützten Bedrohungen erklären und erste Abwehrstrategien skizzieren.

# Fiktives Szenario

Die "KreativKopf GmbH" hat die grundlegenden Maßnahmen aus eurer Analyse umgesetzt. Nun plant das Unternehmen den nächsten Schritt: Die restlichen lokalen Dienste sollen zu einem Public-Cloud-Anbieter (z.B. Microsoft Azure oder AWS) migriert und die Remote-Arbeit weiter ausgebaut werden. Gleichzeitig stellt die Geschäftsführung fest, dass trotz erster Schulungen immer noch Mitarbeiter auf einfache Phishing-Mails hereinfallen. Zudem sorgt sich die IT-Leitung um die Sicherheit der vielen eingesetzten Open-Source-Bibliotheken und die zunehmende Professionalität von Phishing-Angriffen.

# Gesamtaufgabe

Erstellt als Lerngruppe eine strategische Roadmap für die Geschäftsführung der "KreativKopf GmbH". Diese Präsentation soll die nächsten Schritte zur Modernisierung der IT-Sicherheit skizzieren.

1. **Zero Trust & Cloud Security:** Erklärt, wie die Prinzipien von Zero Trust auf die neue Cloud- und Remote-Arbeits-Struktur der Agentur angewendet werden können und welche Verantwortlichkeiten die Agentur in der Cloud hat.  
  \- **Always verify** → Also für jeden Schritt/Zugriff authentifizieren → MFA unabdingbar  
  \- Ausgehend davon, dass die **Systeme bereits kompromittiert** sind → sensible **Dateien einzeln verschlüsseln**; Systeme weitgehend **segmentieren**;  
  \- Gemäß des Prinzips des “**Least Privilege**” werden entsprechend Rollen und Zugriffsrechte verteilt (**minimal benötigte Rechte**)  
  \- **Auditlogs**  
  \- Grundlegend sind **WIR** für die Sicherheit **IN** der Cloud verantwortlich und der Cloud-Anbieter für die (**physische**) Sicherheit **DER** Cloud+++ columnContainer +++  
  +++ column xs:12 md:6 lg:6 +++  
  MS![Diagramm zeigt Zuständigkeitszonen.](https://learn.microsoft.com/de-de/azure/security/fundamentals/media/shared-responsibility/shared-responsibility.svg)  
  +++ end:column ++++++ column xs:12 md:6 lg:6 +++  
  AWS![](files/019cee3c-14c9-710a-bf05-0ab329689eb2/image.png)  
  +++ end:column +++  
  +++ end:columnContainer +++
2. **Moderne Bedrohungen:** Klärt die Geschäftsführung über die Risiken von Supply-Chain-Angriffen und KI-gestütztem Social Engineering auf und zeigt erste Lösungsansätze auf.  
  \- Supply-Chain Angriffe sind gefährlich, da sie einerseits ihren Ursprung dort haben, wo wir kein direktes Handlungs- und Verantwortungsvermögen haben und andererseits, da sie aus vertrauenswürdigen Quellen stammen können  
  \- **SBOM-Liste führen** → regelmäßig zu Vorfällen informieren und ggf. genutzte und betroffene Software verifizieren, updaten und/oder löschen (nicht mehr nutzen) → nützliche Links: https://www.cvedetails.com/ oder https://www.cve.org/ oder https://osv.dev/  
  \- Social Engineering: internes “Codewort" oder Verhalten für Verdachtsfälle etablieren  
  **Risiken**
  - Kontoübernahmen
  - Finanzbetrug (CEO-Fraud)
  - Einspeisung von Ransomware  
    
3. **Security Culture:** Stellt ein kreatives Konzept für eine nachhaltige Security-Awareness-Kampagne vor, die über eine einmalige Schulung hinausgeht.  
  <br/>**Konzept: „Security als KreativKopf“**
  1. **Gamification & Wettbewerb**
    - Interaktive Challenges, z. B. monatliche Phishing-Simulationen mit Punktesystem.
    - Prämien für Teams mit den besten Sicherheitsentscheidungen.
  2. **Storytelling & interne Kampagnen**
    - Kurze Videos oder Comic-Strips, die reale Angriffe anonymisiert darstellen.
    - „Sicherheitsheld der Woche“ – Anerkennung für vorbildliches Verhalten.
  3. **Kontinuierliche Micro-Learnings**
    - 5–10-minütige Mini-Trainings via App oder Intranet.
    - Fokus auf aktuelle Bedrohungen (Phishing, Social Engineering, sichere Nutzung der Cloud).
  4. **Feedback-Mechanismen & Reporting**
    - Einfache Meldung verdächtiger Mails/Links.
    - Auswertung und Rückmeldung an Mitarbeiter über reale Sicherheitsvorfälle.
  5. **Management-Engagement**
    - Führungskräfte beteiligen sich aktiv an Awareness-Maßnahmen.
    - Kommunikation der Bedeutung von Sicherheit als Teil der Unternehmensstrategie.