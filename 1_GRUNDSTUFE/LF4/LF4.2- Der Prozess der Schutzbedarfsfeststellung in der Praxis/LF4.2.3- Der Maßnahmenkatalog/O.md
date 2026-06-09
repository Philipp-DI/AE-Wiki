# 🐝 Olena

Als IT-Systemadministrator

möchte ich einen Überblick über gängige technisch-organisatorische Maßnahmen (TOMs) gewinnen,

damit ich aus einer Schutzbedarfsfeststellung konkrete und angemessene Handlungsempfehlungen ableiten kann.

# Celebration Criteria

- Wir können technische und organisatorische Maßnahmen voneinander unterscheiden.  
  **Technische Maßnahmen:**  
  Schutz durch Technik, z. B. Firewalls, Virenschutz, Verschlüsselung, Backups, Zugangskontrollen.**Organisatorische Maßnahmen:**  
  Schutz durch Regeln und Prozesse, z. B. Sicherheitsrichtlinien, Schulungen, klare Zuständigkeiten, Vier-Augen-Prinzip.📘 **Unterschied:**  
  Technische Maßnahmen schützen Systeme direkt.  
  Organisatorische Maßnahmen sorgen dafür, dass Menschen und Prozesse sicher handeln.
- Wir können für die Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit jeweils mindestens zwei passende Schutzmaßnahmen nennen.  
  **Vertraulichkeit:**
  - Verschlüsselung von Daten.
  - Zugriffsbeschränkungen durch Passwörter und Rollenrechte.
- **Integrität:**
  - Einsatz von Prüfsummen oder digitalen Signaturen.
  - Protokollierung und Kontrolle von Änderungen.
- **Verfügbarkeit:**
  - Regelmäßige Datensicherungen (Backups).
  - Redundante Systeme und unterbrechungsfreie Stromversorgung (USV).
- Wir können den Zweck von Firewalls, Antivirus-Software, Backups und Passwort-Richtlinien erklären.  
  **Firewall:** Überwacht und filtert den Datenverkehr, schützt vor unbefugtem Zugriff.
- **Antivirus-Software:** Erkennt, blockiert und entfernt Schadsoftware.
- **Backups:** Sichern Daten, damit sie nach Verlust oder Angriff wiederhergestellt werden können.
- **Passwort-Richtlinien:** Legen fest, wie Passwörter sicher gestaltet und regelmäßig geändert werden sollen.
- Wir können begründen, warum eine Kombination aus technischen und organisatorischen Maßnahmen notwendig ist.  
  <br/>Technische Maßnahmen allein reichen nicht aus, weil viele Sicherheitsvorfälle durch menschliche Fehler entstehen.  
  Organisatorische Maßnahmen allein sind ebenfalls zu schwach, wenn keine technischen Schutzmechanismen vorhanden sind.✅ **Kombination:**
  
  - Technische Maßnahmen schützen Systeme.
  - Organisatorische Maßnahmen sorgen für korrektes Verhalten der Mitarbeitenden.  
    Gemeinsam bilden sie ein ganzheitliches Sicherheitskonzept.
  
  ![](files/019cee46-9118-749b-9cdc-3a9943ab1709/image.png)

# Wissens-Briefing

Nachdem der Schutzbedarf bekannt ist, müssen geeignete Maßnahmen ausgewählt werden, um diesen zu erreichen. Man unterscheidet grundsätzlich zwischen technischen und organisatorischen Maßnahmen.

- **Technische Maßnahmen:** Dies sind alle Sicherheitsvorkehrungen, die direkt in der IT-Hardware und -Software implementiert sind.
  - **Beispiele:** Firewall, Virenscanner, Verschlüsselung (von Festplatten, E-Mails), regelmäßige Backups, Zwei-Faktor-Authentisierung (2FA), Intrusion Detection Systems (IDS).
- **Organisatorische Maßnahmen:** Diese umfassen alle Regelungen, Prozesse und Verhaltensweisen im Unternehmen, die die Sicherheit unterstützen.
  - **Beispiele:** Erstellung einer Passwort-Richtlinie, Durchführung von Security-Awareness-Schulungen für Mitarbeiter, ein Need-to-know-Prinzip (Benutzer erhalten nur die Rechte, die sie für ihre Arbeit benötigen), ein Notfallplan (Incident Response Plan), klare Regelungen zum Umgang mit mobilen Datenträgern.

Die größte Sicherheit wird nur durch ein Zusammenspiel beider Maßnahmenarten erreicht. Die beste Firewall ist nutzlos, wenn ein Mitarbeiter seine Zugangsdaten auf einem Zettel am Monitor befestigt.

# Aufgaben

1. **Maßnahmen zuordnen:** Brainstormt in der Gruppe zu den Ergebnissen eurer Schutzbedarfsfeststellung für den Grafikdesigner. Welche konkreten TOMs (mindestens zwei technische und zwei organisatorische) würdet ihr empfehlen, um die Zielobjekte mit hohem oder sehr hohem Schutzbedarf abzusichern?
  - **Technische Maßnahmen**  
    
    | **Zielobjekt** | **Maßnahme** | **Beschreibung / Umsetzung & Begründung** |
    | --- | --- | --- |
    | **Windows 11 PC** | **Festplattenverschlüsselung (BitLocker)** | Aktivieren der Laufwerksverschlüsselung mit BitLocker, um Daten bei Geräteverlust oder Diebstahl zu schützen. |
    |     | **Benutzerkonten & starke Passwörter** | Für jede Person eigene Benutzerkonten mit eingeschränkten Rechten einrichten; Passwörter mit mindestens 12 Zeichen, Zahlen und Sonderzeichen verwenden. |
    |     | **Schulung zu Datensicherheit und Phishing** | Mitarbeitende regelmäßig zum sicheren Umgang mit E-Mails, Anhängen und Datenträgern schulen, um Schadsoftware zu vermeiden. |
    |     | **Passwort- und Gerätepolitik** | Interne Richtlinie: Passwortwechsel alle 90 Tage, Nutzung privater USB-Geräte verboten. |
    | **NAS-Server** | **RAID konfigurieren** | Redundante Datenspeicherung einrichten, damit Daten auch bei Ausfall einer Festplatte erhalten bleiben. |
    |     | **Zugriffsbeschränkung per Benutzerrechten** | Zugriff nur für autorisierte Benutzer einrichten; Rechte nach dem Prinzip der minimalen Berechtigung vergeben. |
    |     | **Backup-Protokoll und regelmäßige Prüfungen** | Protokoll über durchgeführte Backups führen; monatlich Wiederherstellung testen, um Funktionsfähigkeit sicherzustellen. |
    |     | **Freigaberegeln definieren** | Festlegen, wer Daten auf dem NAS erstellen, ändern oder löschen darf; Änderungen müssen freigegeben werden. |
    | **Kundendaten & vertrauliche Entwürfe** | **Verschlüsselung** | Daten verschlüsselt speichern (AES-256) und nur über gesicherte Verbindungen (HTTPS/VPN) übertragen. |
    |     | **Audit-Logs aktivieren** | Aufzeichnen, wer wann auf Daten zugreift oder Änderungen vornimmt, um Missbrauch zu erkennen. |
    |     | **Datenschutzrichtlinie nach DSGVO** | Dokumentieren, wie personenbezogene Daten gespeichert, verarbeitet und gesichert werden. |
    |     | **Mitarbeiterschulung zum Datenschutz** | Mitarbeitende sensibilisieren: Keine Kundendaten auf private Geräte oder per unverschlüsselter E-Mail versenden. |
    | **Cloud-Zugang / Cloud-Speicher** | **TLS/SSL & VPN verwenden** | Zugriff auf Cloud-Dienste nur über verschlüsselte VPN-Verbindung zulassen, um Datenabfluss zu verhindern. |
    |     | **Zwei-Faktor-Authentifizierung (2FA)** | Anmeldung in der Cloud durch zusätzlichen Sicherheitsfaktor absichern (z. B. App-Code oder SMS). |
    |     | **Rollenbasierte Rechteverwaltung (RBAC)** | Nur notwendige Rechte vergeben; Administratorrechte auf wenige Personen beschränken. |
    |     | **Cloud-Nutzungsrichtlinie** | Interne Richtlinie, dass ausschließlich der Unternehmens-Cloud-Dienst genutzt werden darf (keine privaten Konten). |
    | **WLAN & LAN** | **WPA3-Verschlüsselung aktivieren** | Sicheres WLAN-Protokoll WPA3 verwenden, WPS deaktivieren und starkes Passwort setzen. |
    |     | **Netzwerk-Segmentierung (VLAN)** | Gäste-WLAN strikt vom internen Netz trennen, um Zugriff auf Firmendaten zu verhindern. |
    |     | **WLAN-Nutzungsrichtlinie** | Regeln für Passwortvergabe, Verantwortlichkeiten und Wartung definieren. |
    |     | **Überwachung & Log-Kontrolle** | Monatliche Kontrolle der Router-Logs und der Firmware-Versionen durchführen. |
    | **Büroraum** | **Zutrittskontrolle (Karte/Code)** | Zugang nur für autorisierte Mitarbeitende mittels Schlüsselkarten oder Codesystem. |
    |     | **Videoüberwachung / Bewegungsmelder** | Installation von Kameras oder Sensoren zur Diebstahlprävention. |
    |     | **Besucherregelung** | Externe Besucher dürfen nur in Begleitung eines Mitarbeitenden in Büroräume. |
    |     | **Schlüsselmanagement** | Ausgabe und Rückgabe von Schlüsseln oder Zugangskarten dokumentieren. |
    
2. **Recherche "Next-Gen-Firewall":** Recherchiert online, was eine "Next-Generation-Firewall" (NGFW) von einer klassischen Firewall unterscheidet. Stellt die Zusatzfunktionen in 3-4 Stichpunkten vor.
  
  | Funktion / Eigenschaft | Klassische Firewall | NGFW (Next-Generation Firewall) |
  | --- | --- | --- |
  | **Traffic-Kontrolle** | Nur IP, Port, Protokoll | IP, Port, Protokoll + Kontrolle von Anwendungen |
  | **Packet Inspection** | Nur Kopfzeilen der Pakete | Deep Packet Inspection (DPI), prüft auch Inhalte, kann SSL/TLS entschlüsseln |
  | **Bedrohungsschutz** | Keine eingebaute Schutzfunktion | Integriertes IPS, Antivirus, Malware-Schutz |
  | **Benutzer- und Rollenbewusstsein** | Nein | Regeln nach User, Rolle oder Gerät (AD/LDAP) |
  | **Konsolidierung von Funktionen** | Nur Filterung des Traffics | Kombination von Anwendungskontrolle, IPS, Antivirus, Verschlüsselung |
  | **Netzwerk-Transparenz** | Eingeschränkt | Vollständige Sicht auf Netzwerkverkehr und Anwendungen |
  
  | Abkürzung | Ausgeschrieben | Einfache Erklärung für Kinder |
  | --- | --- | --- |
  | **NGFW** | Next-Generation Firewall | Firewall der neuen Generation, „Super-Wachhund“ |
  | **DPI** | Deep Packet Inspection | „Tiefes Lesen“ von Datenpaketen, prüft Inhalte |
  | **IPS** | Intrusion Prevention System | System, das Angriffe erkennt und stoppt |
  | **AD** | Active Directory | „Benutzerliste“, wer ist wer in der Firma |
  | **LDAP** | Lightweight Directory Access Protocol | Technik, um Benutzer in der Liste zu prüfen |
  | **NDA** | Non-Disclosure Agreement | Geheimhaltungsvertrag, damit niemand Daten weitergibt |
  
3. **Passwort-Policy entwerfen:** Erstellt in einem geteilten Dokument den Entwurf für eine einfache Passwort-Richtlinie für die "KreativKopf GmbH". Legt darin die Mindestlänge, die Komplexitätsanforderungen (Groß-/Kleinbuchstaben, Zahlen, Sonderzeichen) und das Wechselintervall fest.  
  [BSI - Sichere Passwörter erstellen](https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Cyber-Sicherheitsempfehlungen/Accountschutz/Sichere-Passwoerter-erstellen/sichere-passwoerter-erstellen_node.html)
  
  | Regel | Vorgabe / Erklärung |
  | --- | --- |
  | **Mindestlänge** | 16 Zeichen |
  | **Großbuchstaben** | Mindestens 1 (A–Z) |
  | **Kleinbuchstaben** | Mindestens 1 (a–z) |
  | **Zahlen** | Mindestens 1 (0–9) |
  | **Sonderzeichen** | Mindestens 1 (!, @, #, \$, %, &, \*) |
  | **Wechselintervall** | Alle 90 Tage |
  | **Passwort-Wiederverwendung** | Die letzten 5 Passwörter dürfen nicht erneut verwendet werden |
  | **Sicherer Umgang** | Passwörter nicht weitergeben oder ungeschützt speichern |
  | **Bei Verdacht** | Passwort sofort ändern |
  
4. **Diskussion:** Diskutiert die Aussage: "Der Mensch ist das schwächste Glied in der Sicherheitskette. Deshalb sind organisatorische Maßnahmen wie Schulungen wichtiger als technische Maßnahmen." Findet Pro- und Contra-Argumente.  
  <br/>**Fazit / Schlussfolgerung**
  
  - Menschliche Fehler sind häufig, daher sind Schulungen und organisatorische Maßnahmen wichtig.
  - Technische Maßnahmen schützen zuverlässig, auch bei Fehlern.
  - **Die beste Sicherheitsstrategie** ist eine Kombination aus organisatorischen und technischen Maßnahmen.
  
  | Argumenttyp | Argument | Erklärung / Beispiel |
  | --- | --- | --- |
  | **Pro** | Menschliche Fehler passieren am häufigsten | Phishing, schwache Passwörter, versehentliches Löschen von Daten |
  | **Pro** | Schulungen erhöhen das Sicherheitsbewusstsein | Mitarbeiter lernen Risiken zu erkennen und korrekt zu reagieren |
  | **Pro** | Technische Maßnahmen allein sind nicht perfekt | Technik kann umgangen oder durch Social Engineering überlistet werden |
  | **Contra** | Technische Maßnahmen sind objektiv und zuverlässig | Firewalls, Antivirus, Verschlüsselung schützen auch bei menschlichen Fehlern |
  | **Contra** | Organisatorische Maßnahmen reichen nicht aus | Schulungen helfen nur, wenn Mitarbeiter die Regeln konsequent umsetzen |
  | **Contra** | Kombination ist effektiver | Beste Sicherheit entsteht, wenn technische und organisatorische Maßnahmen zusammenwirken |
  

# Quellen und Vertiefung

1. **Authentisierung**  
  Der Fokus ist auf den Benutzer gerichtet, der sich am System anmeldet. Dazu weist er seine Identität nach, indem er z.B. seinen Benutzernamen und das dazugehörige Passwort eingibt. Die Authentisierung kann auch in anderer Form erfolgen, z.B. durch eine Magnetkarte oder biometrische Merkmale.
2. **Authentifizierung**  
  In diesem Schritt ist das System am Zug. Im Rahmen der Authentifizierung überprüft das System die vom Benutzer gemachten Angaben. Dazu werden die eingegebenen Daten mit den Einträgen in der zugehörigen Datenbank, wie z.B. dem hinterlegten Benutzernamen und dem Hashwert des Passworts, verglichen.
3. **Autorisierung**  
  Erst nach erfolgreicher Authentifizierung kann die Autorisierung, d.h. die Festlegung der Zugriffsberechtigung erfolgen. Dabei werden dem Benutzer seine Rechte zugewiesen. Die Zugriffsrechte entscheiden darüber, in welchem Umfang das System genutzt werden kann und ob z.B. personenbezogene Daten eingesehen oder verändert werden können.

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.6 "Maßnahmen" (S. 1000-1018).
- **Online-Ressource:** [BSI IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html) (bietet zu allen Bausteinen konkrete Maßnahmen).