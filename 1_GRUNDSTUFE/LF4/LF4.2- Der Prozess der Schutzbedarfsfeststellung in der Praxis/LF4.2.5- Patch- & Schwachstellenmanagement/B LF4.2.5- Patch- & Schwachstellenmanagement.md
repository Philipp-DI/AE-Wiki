# BruddaJay LF4.2.5- Patch- & Schwachstellenmanagement

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
3. 
4. **Testen:** Wird der Patch in einer Testumgebung eingespielt, um sicherzustellen, dass er keine anderen wichtigen Programme stört.
5. **Ausrollen (Deployment):** Der Patch wird auf den produktiven Systemen installiert.
6. **Verifizieren:** Es wird überprüft, ob die Installation erfolgreich war und die Lücke geschlossen ist.

**Beispiel WannaCry (2017):** Diese Ransomware nutzte die "EternalBlue"-Schwachstelle in Windows aus. Microsoft hatte bereits zwei Monate zuvor einen Patch veröffentlicht. Hunderttausende Systeme weltweit, die nicht gepatcht waren, wurden innerhalb kürzester Zeit infiziert.

# Aufgaben

1. **CVE-Recherche:** Recherchiert die CVE-Datenbank (z.B. bei MITRE oder NIST). Sucht nach einer kürzlich veröffentlichten, kritischen Schwachstelle für eine bekannte Software (z.B. Windows, Chrome oder ein Adobe-Produkt). Fasst zusammen, was die Lücke ermöglicht und wie hoch ihr Schweregrad (CVSS-Score) ist.
  - **_Schwachstelle_**: **CVE-2025-59287** kritische Remote-Code-Execution (RCE) in **Windows Server Update Services (WSUS)**.
  - **_Lücke_**: Es gibt in WSUS (dem Windows-Update-Server) einen Fehler, durch den jemand von außen manipulierte Daten an den Server schicken kann. Das bedeutet im Prinzip: Er kann alles machen, was das System selbst darf.
  - **_Schweregrad:_** Der CVSS-Score wurde mit **9.8** (kritisch) bewertet.
2. **Prozess-Visualisierung:** Erstellt eine einfache Grafik oder ein Flussdiagramm, das die fünf Phasen des Patch-Management-Prozesses darstellt.![diagram.drawio.svg](files/019cee46-a96e-7682-9201-1e9a5075c1cb/diagram.drawio.svg)
  1. **Szenario-Diskussion:** Die "KreativKopf GmbH" hat Windows-PCs, macOS-Laptops, Android- und iOS-Smartphones sowie Linux-Server in der Cloud. Diskutiert die unterschiedlichen Herausforderungen beim Patch-Management für diese vier Systemwelten.
    
    | OS  | Vorteile | Nachteile |
    | --- | --- | --- |
    | Windows | PCs sind gut verwaltbar | Gefährdung durch lücken im System |
    | macOS | Zentrale Verwaltung | Asynchrone Updates zwischen geräte und softwares |
    | Linux (Server) | Automatisches Updaten | Diversität in Linux versionen |
    | Android | gute Frage | Zu viele Hersteller und zu viele Update zyklen |
    | iOS | Schnelle uns zentrale Update System | Nicht jede Mitarbeiter updatet sofort. Asynchronität. |
    
    \==MH==
    
    <div class="joplin-table-wrapper"><table style="width: 925px"><tbody><tr><th colspan="1" rowspan="1" colwidth="192"><p data-id="kymyyynprbdh">“Welt”</p></th><th colspan="1" rowspan="1" colwidth="733"><p data-id="mcxtdezghfcm">Herausforderungen</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="192"><p data-id="oqptmnvhrkaj">Windows Clients</p></td><td colspan="1" rowspan="1" colwidth="733"><ul><li><p data-id="kkdzfdogempq">Vielfalt (HW &amp; SW)</p></li><li><p data-id="nitpmspqznqj">Benutzer-Interaktionen</p></li><li><p data-id="stidtzpctipi">Legacy-Software</p></li><li><p data-id="jwjipxulgrhi">Deployment-Werkzeuge</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="192"><p data-id="qukyqthokxvx">MacOS Clients</p></td><td colspan="1" rowspan="1" colwidth="733"><ul><li><p data-id="whjeefngsazo">geschlossenes Ökosystem</p></li><li><p data-id="szpiimklvygc">Mobile Device Management (MDM) Abhängigkeit, sonst keine Kontrolle über Geräte</p></li><li><p data-id="jqfdzbhwcmmz">Firmware-Updates</p></li><li><p data-id="uhzjzhssszag">SW-Kompatibilittät</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="192"><p data-id="zguggdmzitic">Mobile Clients (iOS / Android)</p></td><td colspan="1" rowspan="1" colwidth="733"><ul><li><p data-id="osyxschrwyat">Android-Fragmentierung —&gt; herstellerabhängige Aktualisierungen</p></li><li><p data-id="ojriffhqrbdw">iOS Homogenität —&gt; fehlerhaftes Update bekommen alle Geräte</p></li><li><p data-id="konrqdfxdofo">Trennung von OS und APP —&gt; getrenntes Patchen</p></li><li><p data-id="gxighmygtbjd">BYOD —&gt; kein Patchmgmt. bei Privatgeräten möglich</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="192"><p data-id="gokyvihtrtwo">Linux Server</p></td><td colspan="1" rowspan="1" colwidth="733"><ul><li><p data-id="irehrvnrnwia">Hochverfügbarkeit —&gt; Neustart = Ausfall —&gt; akribische Planung erforderlich</p></li><li><p data-id="remfuiiiuecp">Distributionsvielfalt —&gt; eigene Zyklen und Tools</p></li><li><p data-id="mhvtvagrmufv">Kernel Live Patching</p></li><li><p data-id="othmsyxxigub">Abhängigkeiten zu Bibliotheken</p></li></ul></td></tr></tbody></table></div>
    
3. **Argumentation:** Bereitet eine kurze Argumentation (3-4 Sätze) für die Geschäftsführung der "KreativKopf GmbH" vor, die erklärt, warum das Testen von Patches vor dem Ausrollen trotz des Zeitverlusts absolut notwendig ist.  
  <br/>“Wenn man Updates einfach blind installiert, kann schnell mal etwas kaputtgehen und das kostet im Zweifel mehr Zeit und Geld, als vorher kurz zu testen. Ein Testlauf hilft, böse Überraschungen zu vermeiden, und sorgt dafür, dass wichtige Programme weiter stabil laufen. Auch bei dringenden Sicherheitslücken sollte man zumindest einen kurzen Schnelltest machen, bevor man die Updates auf alle Systeme verteilt.”

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Sicherheitsmaßnahmen umsetzen" (implizit, S. 1004 ff.).
- **Online-Ressource:** [BSI - Baustein ORP.4 Patch- und Änderungsmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Grundschutz/DE/IT-GS-Kompendium/bausteine/ORP/ORP_4_Patch_und_Aenderungsmanagement.html)
- **Datenbank:** [CVE Details](https://www.cvedetails.com/)