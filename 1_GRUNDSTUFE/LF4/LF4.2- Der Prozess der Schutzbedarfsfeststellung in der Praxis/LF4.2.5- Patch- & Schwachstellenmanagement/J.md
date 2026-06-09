# Janine

Als IT-Administrator möchte ich einen systematischen Prozess für das Patch-Management verstehen, damit ich die IT-Systeme des Unternehmens (mobil, desktop, server) zeitnah gegen bekannte Schwachstellen absichern kann.

# Celebration Criteria

- Wir können den Lebenszyklus einer Sicherheitslücke von der Entdeckung über die CVE-Nummer bis zum Patch erklären.
- Wir können die Wichtigkeit eines etablierten und schnellen Patch-Management-Prozesses für die IT-Sicherheit begründen.
- Wir können den Unterschied zwischen einem sicherheitskritischen Patch und einem reinen Funktionsupdate erläutern.
- Wir können anhand eines realen Beispiels (z.B. WannaCry/EternalBlue) die katastrophalen Folgen fehlender Updates erläutern.

# Wissens-Briefing

Eine der häufigsten Ursachen für erfolgreiche Cyberangriffe sind **nicht gepatchte Schwachstellen** in Software und Betriebssystemen. Patch-Management ist daher keine lästige Pflicht, sondern ein fundamentaler Sicherheitsprozess.

- **Schwachstelle (Vulnerability):** Ein Fehler in einer Software, der von einem Angreifer ausgenutzt werden kann.
- **CVE (Common Vulnerabilities and Exposures):** Sobald eine Schwachstelle bekannt und bestätigt ist, erhält sie eine eindeutige CVE-Nummer (z.B. `CVE-2017-0144` für die "EternalBlue"-Lücke), was die weltweite Kommunikation darüber erleichtert.
- **Patch:** Ein vom Hersteller bereitgestelltes Software-Update, das eine oder mehrere Sicherheitslücken schließt.
- **Zero-Day-Lücke:** Eine Schwachstelle, die Angreifern bereits bekannt ist und aktiv ausgenutzt wird, für die es aber vom Hersteller noch keinen Patch gibt. Hier zählt jede Sekunde.

Ein **Patch-Management-Prozess** sorgt dafür, dass Patches kontrolliert und zeitnah ausgerollt werden:

1. **Identifizieren:** Überwachen, welche neuen Patches für die im Unternehmen eingesetzte Software verfügbar sind.
2. **Bewerten:** Wie kritisch ist der Patch? Muss er sofort oder beim nächsten regulären Wartungsfenster installiert werden?
3. **Testen:** Wird der Patch in einer Testumgebung eingespielt, um sicherzustellen, dass er keine anderen wichtigen Programme stört.
4. **Ausrollen (Deployment):** Der Patch wird auf den produktiven Systemen installiert.
5. **Verifizieren:** Es wird überprüft, ob die Installation erfolgreich war und die Lücke geschlossen ist.

**Beispiel WannaCry (2017):** Diese Ransomware nutzte die "EternalBlue"-Schwachstelle in Windows aus. Microsoft hatte bereits zwei Monate zuvor einen Patch veröffentlicht. Hunderttausende Systeme weltweit, die nicht gepatcht waren, wurden innerhalb kürzester Zeit infiziert.

# Aufgaben

1. **CVE-Recherche:** Recherchiert die CVE-Datenbank (z.B. bei MITRE oder NIST). Sucht nach einer kürzlich veröffentlichten, kritischen Schwachstelle für eine bekannte Software (z.B. Windows, Chrome oder ein Adobe-Produkt). Fasst zusammen, was die Lücke ermöglicht und wie hoch ihr Schweregrad (CVSS-Score) ist.**CVE-2025-55234** – eine Elevation-of-Privilege (EoP) Schwachstelle im Windows SMB Server-Dienst von Microsoft. [Tenable®+2The Hacker News+2](https://www.tenable.com/blog/microsofts-september-2025-patch-tuesday-addresses-80-cves-cve-2025-55234?utm_source=chatgpt.com)Der offizielle CVSSv3-Score lautet **8,8** – damit als „hoch“ einzustufen. [crowdstrike.com](http://crowdstrike.com)[+1](https://www.crowdstrike.com/en-us/blog/patch-tuesday-analysis-september-2025/?utm_source=chatgpt.com)Beschreibung: Ein Angreifer ohne Authentifizierung kann durch unsachgemäße Authentifizierungsmechanismen im SMB-Dienst (Server Message Block) erhöhte Rechte erlangen. Erfolgreiche Ausnutzung würde dem Angreifer ermöglichen, Aktionen auf dem System mit höheren Privilegien auszuführen. [The Hacker News+1](https://thehackernews.com/2025/09/microsoft-fixes-80-flaws-including-smb.html?utm_source=chatgpt.com)Besonderheit: Die Schwachstelle war **öffentlich bekannt**, bevor der Patch bereitgestellt wurde. [The Hacker News+1](https://thehackernews.com/2025/09/microsoft-fixes-80-flaws-including-smb.html?utm_source=chatgpt.com)Bedeutung: Da SMB-Dienste oft in Unternehmensnetzwerken zentral sind, kann eine solche Lücke eine weitreichende Kompromittierung ermöglichen (z. B. lateral movement, Privilege Escalation).Fazit: Diese Schwachstelle passt exakt in das von Ihnen beschriebene Szenario – nicht gepatcht = grosses Risiko
2. **Prozess-Visualisierung:** Erstellt eine einfache Grafik oder ein Flussdiagramm, das die fünf Phasen des Patch-Management-Prozesses darstellt.Entdeckung von Schwachstellen  
  ↓  
  Bewertung / Priorisierung  
  ↓  
  Patch-Entwicklung / -Bereitstellung  
  ↓  
  Installation / Anwendung des Patches  
  ↓  
  Überprüfung & Monitoring
3. **Szenario-Diskussion:** Die "KreativKopf GmbH" hat Windows-PCs, macOS-Laptops, Android- und iOS-Smartphones sowie Linux-Server in der Cloud. Diskutiert die unterschiedlichen Herausforderungen beim Patch-Management für diese vier Systemwelten.**Windows-PCs**: Große Anzahl unterschiedlicher Versionen, hohe Verbreitung, häufig Ziel von Exploits (z. B. SMB-Lücken). Patch-Zyklen sind vergleichsweise klar (z. B. Patch Tuesday bei Microsoft). Herausforderung: möglichst schnell im Unternehmen ausrollen, ohne Geschäftsprozesse zu stören.**macOS-Laptops**: Weniger häufig als Ziel im Vergleich zu Windows, aber trotzdem relevant. Apple veröffentlicht Updates unregelmässiger, diverse Versionen im Umlauf; Besonderheit: oft am Arbeitsplatz durch Endnutzer (Home/Office) eingesetzt → Kontrolle schwieriger.**Android- & iOS-Smartphones**: Mobilgeräte bringen zusätzliche Komplexität: Herstellerabhängigkeit, Mobilfunk-Updates, BYOD (Bring Your Own Device) im Unternehmen, viele Geräte ausserhalb direkt steuerbarer Infrastruktur. Zudem viele Apps mit eigenen Updatezyklen. Herausforderung: Sicherstellen, dass Gerätebestände aktuell sind und mobile Sicherheitsrichtlinien gelten.**Linux-Server in der Cloud**: Diese Systeme haben oft andere Mechanismen (z. B. Repository-Updates, Paketmanager, eventuell Container). Herausforderung: zahlreiche Distributionen, teils kundenspezifische Builds, Cloud-Provider-Schnittstellen, System-Downtimes, eventuell automatisiertes Roll-out vs. manueller Eingriff. Dazu: Skalierung, Remote-Infrastruktur, evtl. hybride Umgebungen.**Zusätzliche übergreifende Herausforderungen**: Unterschiedliche Update-Mechanismen, Abhängigkeiten (z. B. Anwendungen, Datenbanken), unterschiedliche Wartungsfenster, Risiko von Ausfall durch fehlerhafte Patches, Priorisierung – nicht alle Systeme können sofort gepatcht werden
4. **Argumentation:** Bereitet eine kurze Argumentation (3-4 Sätze) für die Geschäftsführung der "KreativKopf GmbH" vor, die erklärt, warum das Testen von Patches vor dem Ausrollen trotz des Zeitverlusts absolut notwendig ist.Es stellt sicher, dass kritische Geschäftsapplikationen durch das Update nicht beeinträchtigt werden. Ohne Test besteht das Risiko, dass ein Patch zwar eine Sicherheitslücke schließt — aber gleichzeitig Geschäftsprozesse stört oder gar ausfallen lässt. Wir müssen Sicherheit und Betriebssicherheit gemeinsam gewährleisten, damit das Unternehmen nicht durch einen ungeplanten Ausfall stärker geschädigt wird als durch die ursprüngliche Schwachstelle

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Sicherheitsmaßnahmen umsetzen" (implizit, S. 1004 ff.).
- **Online-Ressource:** [BSI - Baustein ORP.4 Patch- und Änderungsmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Grundschutz/DE/IT-GS-Kompendium/bausteine/ORP/ORP_4_Patch_und_Aenderungsmanagement.html)
- **Datenbank:** [CVE Details](https://www.cvedetails.com/)