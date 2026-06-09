# Janine

Als angehender IT-Sicherheitsbeauftragter möchte ich die Struktur und die Komponenten des BSI IT-Grundschutzes verstehen, damit ich systematisch Sicherheitsanforderungen für mein Unternehmen finden und anwenden kann.

# Celebration Criteria

- Wir können den Zweck des BSI IT-Grundschutzes und seine Beziehung zur internationalen Norm ISO 27001 erklären.
- Wir können die Hauptkomponenten des IT-Grundschutzes (BSI-Standards, IT-Grundschutz-Kompendium) benennen.
- Wir können die Struktur eines "Bausteins" aus dem Kompendium (Gefährdungen, Anforderungen) beschreiben.
- Wir können in den Bausteinen gezielt nach Sicherheitsanforderungen für ein konkretes Zielobjekt (z.B. einen Webserver) suchen.

# Wissens-Briefing

Der **BSI IT-Grundschutz** ist eine vom Bundesamt für Sicherheit in der Informationstechnik (BSI) entwickelte, praxiserprobte Methodik zum Aufbau eines Informationssicherheits-Managementsystems (ISMS). Er bietet eine konkrete Anleitung, um ein angemessenes Sicherheitsniveau zu erreichen und ist kompatibel zur internationalen Norm **ISO 27001**.

Die zentralen Bestandteile sind:

- **BSI-Standards:** Sie beschreiben die Vorgehensweise.
  - **BSI 200-1:** Allgemeine Anforderungen an ein ISMS.
  - **BSI 200-2:** Die IT-Grundschutz-Vorgehensweise (Strukturanalyse, Schutzbedarf, Modellierung - die wir in diesem Epic praktisch anwenden).
  - **BSI 200-3:** Risikomanagement.
- **IT-Grundschutz-Kompendium:** Dies ist das Herzstück und quasi ein riesiger Katalog von Best Practices. Es ist in **Bausteine** gegliedert, die typische Komponenten einer IT-Landschaft repräsentieren (z.B. `SYS.1.2 Windows Server`, `APP.3.2 Webbrowser`, `ORP.4 Patch- und Änderungsmanagement`).

Jeder **Baustein** enthält:

1. Eine Beschreibung des Themas.
2. Eine Liste typischer **elementarer Gefährdungen**.
3. Eine Liste konkreter **Sicherheitsanforderungen**, die umgesetzt werden müssen. Diese sind unterteilt in:
  - **Basis-Anforderungen (B):** Absolut grundlegend, müssen immer erfüllt sein.
  - **Standard-Anforderungen (S):** Sollten bei normalem Schutzbedarf umgesetzt werden.
  - **Anforderungen für hohen Schutzbedarf (H):** Notwendig bei hohem oder sehr hohem Schutzbedarf.

# Aufgaben

1. **Struktur verstehen:** Navigiert auf der Webseite des BSI zum IT-Grundschutz-Kompendium. Wählt den Baustein `APP.1.2 Webbrowser` aus. Identifiziert die Anzahl der Basis-, Standard- und Hoch-Anforderungen.**Basis-Anforderungen:** **13** [bsi.bund.de](http://bsi.bund.de)[+](https://verinicexp.org/fileadmin/user_upload/veriniceXP2021_Slides/verinice.XP2021_Desti_Neuerungen_im_IT-Grundschutz_Kompendium_2021.pdf?utm_source=chatgpt.com)[3verinicexp.org](http://3verinicexp.org)[+](https://verinicexp.org/fileadmin/user_upload/veriniceXP2021_Slides/verinice.XP2021_Desti_Neuerungen_im_IT-Grundschutz_Kompendium_2021.pdf?utm_source=chatgpt.com)[3bsi.bund.de](http://3bsi.bund.de)[+3](https://verinicexp.org/fileadmin/user_upload/veriniceXP2021_Slides/verinice.XP2021_Desti_Neuerungen_im_IT-Grundschutz_Kompendium_2021.pdf?utm_source=chatgpt.com)**Standard-Anforderungen:** **10** [verinicexp.org](http://verinicexp.org)[+](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium/IT_Grundschutz_Kompendium_Edition2021.pdf?__blob=publicationFile&v=6&utm_source=chatgpt.com)[3bsi.bund.de](http://3bsi.bund.de)[+3Die Familienunternehmer+3](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium/IT_Grundschutz_Kompendium_Edition2021.pdf?__blob=publicationFile&v=6&utm_source=chatgpt.com)**Anforderungen für erhöhten Schutzbedarf** (Hoch): **2** [bsi.bund.de](http://bsi.bund.de)[+1](https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/IT-GS-Kompendium/Archiv/Kompendium_Einzel_PDFs_2020/06_APP_Anwendungen/APP_1_2_Webbrowser_Edition_2020.pdf?__blob=publicationFile&v=1&utm_source=chatgpt.com)
2. **Anforderung analysieren:** Lest euch im selben Baustein die Standard-Anforderung `APP.3.2.S5: Zeitnahe Aktualisierung eines Webbrowsers` durch. Fasst in eigenen Worten zusammen, was diese Anforderung verlangt und warum sie wichtig ist.Wenn Sicherheits‑ oder Funktionsupdates verfügbar sind, müssen diese installiert oder zumindest eingespielt werden, damit der Browser nicht mit bekannten Schwachstellen betrieben wird. Damit verbunden ist, dass veraltete Browser‑Versionen nicht mehr genutzt werden, solange ihre Sicherheit nicht gewährleistet ist**Warum ist das wichtig?**
  - Ein Webbrowser ist häufig Angriffsziel: Da viele Anwendungen und Webseiten über den Browser laufen, ist er ein beliebtes Einfallstor für Angriffe (z. B. durch Exploits, Cross‑Site‑Scripting, Drive‑by‑Downloads).
  - Sicherheitslücken entstehen laufend: Hersteller finden Schwachstellen oder Hacker nutzen neue Angriffsformen. Wenn Browser‑Updates nicht zeitnah installiert werden, bleibt das System angreifbar.
  - Risiko für Vertraulichkeit, Integrität und Verfügbarkeit: Ein kompromittierter Browser kann z. B. Zugang zu geschützten Informationen ermöglichen, Manipulationen erlauben oder Dienste lahmlegen.
  - Schutzbedarf: Gerade bei Anwendungen mit höherem Schutzbedarf ist eine lückenlose aktuelle Sicherheit essenziell – andernfalls kann ein „Schwachstellenfenster“ entstehen, das ein reales Risiko darstellt
3. **Anwendung im Szenario:** Welche Bausteine aus dem Kompendium wären für die Analyse des Grafikdesigner-Arbeitsplatzes der "KreativKopf GmbH" (Desktop-PC mit Windows 11, Adobe CC, NAS, Cloud-Anbindung) relevant? Listet mindestens fünf passende Bausteine auf.:
  1. **Hardware-Sicherheit**
    - Schutz des Desktop-PCs, der Peripherie (Monitor, Tastatur, externe Speicher), physischer Zugriffsschutz.
    - Relevanz: Verhindert unbefugten Zugriff oder Diebstahl der Arbeitsgeräte.
  2. **Betriebssystem- und Software-Management**
    - Verwaltung und Absicherung von Windows 11, Patch-Management, Rechteverwaltung.
    - Relevanz: Schützt vor Sicherheitslücken und sorgt für stabile Arbeitsumgebung.
  3. **Anwendungs- und Lizenzmanagement**
    - Adobe Creative Cloud-Installation, Lizenzkontrolle, Update-Management.
    - Relevanz: Sichert legale Nutzung und verhindert Kompatibilitäts- oder Sicherheitsprobleme.
  4. **Datenmanagement und Speicherlösungen**
    - NAS-Anbindung, Cloud-Speicher, Backup-Strategien, Datenverschlüsselung.
    - Relevanz: Schützt vor Datenverlust und gewährleistet sichere Ablage sensibler Designprojekte.
  5. **Netzwerk- und Kommunikationssicherheit**
    - Absicherung der LAN/WLAN-Verbindung, VPN-Zugriffe auf NAS oder Cloud, Firewall.
    - Relevanz: Schützt Datenverkehr und verhindert unbefugten Zugriff auf das Firmennetzwerk.
  6. _(optional, aber empfehlenswert)_ **Endpoint Security / Virenschutz**
    - Antivirus, Antimalware, Monitoring des Arbeitsplatzes.
    - Relevanz: Schützt vor Schadsoftware, die insbesondere beim Austausch von Dateien über Cloud oder Internet auftreten kann
      
      | Baustein | Konkrete Maßnahmen für Grafikdesigner | Nutzen / Relevanz |
      | --- | --- | --- |
      
      |     |     |     |
      | --- | --- | --- |
      | **Hardware-Sicherheit** | \- PCs an festen Arbeitsplätzen sichern (Kensington-Lock) - Monitore so platzieren, dass Bildschirminhalte nicht einsehbar sind - Externe Festplatten verschlüsseln | Schutz vor Diebstahl und unbefugtem Zugriff auf Geräte und Daten |
      
      |     |     |     |
      | --- | --- | --- |
      | **Betriebssystem- und Software-Management** | \- Regelmäßige Windows-Updates einspielen - Benutzerkonten mit eingeschränkten Rechten für Designer - Sicherheitsrichtlinien (z. B. BitLocker, Firewall) konfigurieren | Minimiert Sicherheitslücken und erhöht Systemstabilität |
      
      |     |     |     |
      | --- | --- | --- |
      | **Anwendungs- und Lizenzmanagement** | \- Adobe CC aktuell halten - Lizenzverwaltung zentral prüfen - Plugins und Erweiterungen nur aus vertrauenswürdigen Quellen installieren | Vermeidung von Lizenzproblemen und Schadsoftware, sicheres Arbeiten mit professioneller Software |
      
      |     |     |     |
      | --- | --- | --- |
      | **Datenmanagement und Speicherlösungen** | \- NAS-Zugriff nur über gesicherte Benutzerkonten - Cloud-Daten verschlüsselt synchronisieren - Regelmäßige Backups (lokal + extern/Cloud) | Schutz vor Datenverlust, sichere Zusammenarbeit, schnelle Wiederherstellung bei Problemen |
      
      |     |     |     |
      | --- | --- | --- |
      | **Netzwerk- und Kommunikationssicherheit** | \- LAN/WLAN absichern (WPA3, starke Passwörter) - VPN-Zugriffe auf NAS oder Cloud für externe Designer - Firewall-Regeln konfigurieren | Schutz vor unbefugtem Netzwerkzugriff, sichere Übertragung sensibler Designprojekte |
      
      |     |     |     |
      | --- | --- | --- |
      | **Endpoint Security / Virenschutz** | \- Antivirus-Software aktuell halten - E-Mail-Anhänge und Downloads prüfen - Malware-Scanner regelmäßig laufen lassen | Schutz vor Schadsoftware, insbesondere bei Austausch von Dateien über Internet oder Cloud |
      

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.2 "Standards und Normen", Abschnitt "IT-Grundschutz des BSI" (S. 973-976).
- **Online-Ressource:** [BSI - IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html)