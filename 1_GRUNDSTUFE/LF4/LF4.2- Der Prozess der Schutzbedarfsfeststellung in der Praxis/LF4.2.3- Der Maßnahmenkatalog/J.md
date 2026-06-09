# 👀 Janine

Als IT-Systemadministrator

möchte ich einen Überblick über gängige technisch-organisatorische Maßnahmen (TOMs) gewinnen,

damit ich aus einer Schutzbedarfsfeststellung konkrete und angemessene Handlungsempfehlungen ableiten kann.

# Celebration Criteria

- Wir können technische und organisatorische Maßnahmen voneinander unterscheiden.
- Wir können für die Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit jeweils mindestens zwei passende Schutzmaßnahmen nennen.
- Wir können den Zweck von Firewalls, Antivirus-Software, Backups und Passwort-Richtlinien erklären.
- Wir können begründen, warum eine Kombination aus technischen und organisatorischen Maßnahmen notwendig ist.![](files/019cee46-9f42-743c-9f14-d754e5b25860/image.png)

# Wissens-Briefing

Nachdem der Schutzbedarf bekannt ist, müssen geeignete Maßnahmen ausgewählt werden, um diesen zu erreichen. Man unterscheidet grundsätzlich zwischen technischen und organisatorischen Maßnahmen.

- **Technische Maßnahmen:** Dies sind alle Sicherheitsvorkehrungen, die direkt in der IT-Hardware und -Software implementiert sind.
  - **Beispiele:** Firewall, Virenscanner, Verschlüsselung (von Festplatten, E-Mails), regelmäßige Backups, Zwei-Faktor-Authentisierung (2FA), Intrusion Detection Systems (IDS).
- **Organisatorische Maßnahmen:** Diese umfassen alle Regelungen, Prozesse und Verhaltensweisen im Unternehmen, die die Sicherheit unterstützen.
  - **Beispiele:** Erstellung einer Passwort-Richtlinie, Durchführung von Security-Awareness-Schulungen für Mitarbeiter, ein Need-to-know-Prinzip (Benutzer erhalten nur die Rechte, die sie für ihre Arbeit benötigen), ein Notfallplan (Incident Response Plan), klare Regelungen zum Umgang mit mobilen Datenträgern.

Die größte Sicherheit wird nur durch ein Zusammenspiel beider Maßnahmenarten erreicht. Die beste Firewall ist nutzlos, wenn ein Mitarbeiter seine Zugangsdaten auf einem Zettel am Monitor befestigt.

# Aufgaben

- **Maßnahmen zuordnen:** Brainstormt in der Gruppe zu den Ergebnissen eurer Schutzbedarfsfeststellung für den Grafikdesigner. Welche konkreten TOMs (mindestens zwei technische und zwei organisatorische) würdet ihr empfehlen, um die Zielobjekte mit hohem oder sehr hohem Schutzbedarf abzusichern?
  
  - **Technische Maßnahmen**
  
  <div class="joplin-table-wrapper"><table style="width: 616px"><tbody><tr><th colspan="1" rowspan="1" colwidth="189"><p data-id="nnzjlfrxzzyo">Zielobjekt</p></th><th colspan="1" rowspan="1" colwidth="100"><p data-id="rwpmwskpsavl">Schutzbedarf</p></th><th colspan="1" rowspan="1" colwidth="327"><p data-id="icrtjxzvnxbm">Maßnahmen</p></th></tr><tr><td colspan="1" rowspan="2" colwidth="189"><p data-id="ajaaqzbrkihk">NAS</p></td><td colspan="1" rowspan="2" colwidth="100"><p data-id="rizsteixegrz">Hoch</p></td><td colspan="1" rowspan="1" colwidth="327"><ol><li><p data-id="wnemeljydfmj">Regelmäßige Back-Ups/Datenkontrolle</p></li></ol></td></tr><tr><td colspan="1" rowspan="1" colwidth="327"><ol start="2"><li><p data-id="hgdzhbmqmamw">Festplattenverschlüsselung</p></li></ol></td></tr><tr><td colspan="1" rowspan="2" colwidth="189"><p data-id="jxtzykxhqvqu">Cloud-Speicher/Zugang</p></td><td colspan="1" rowspan="2" colwidth="100"><p data-id="pupgiptdopra">Sehr hoch</p></td><td colspan="1" rowspan="1" colwidth="327"><ol><li><p data-id="rqpwbjdnhlmi">Datenverschlüsselung</p></li></ol></td></tr><tr><td colspan="1" rowspan="1" colwidth="327"><ol start="2"><li><p data-id="jfdoridrutpf"></p></li></ol></td></tr></tbody></table></div>
  
- **Recherche "Next-Gen-Firewall":** Recherchiert online, was eine "Next-Generation-Firewall" (NGFW) von einer klassischen Firewall unterscheidet. Stellt die Zusatzfunktionen in 3-4 Stichpunkten vor.
  
  | **Merkmal / Funktion** | **Klassische Firewall** | **Next-Generation Firewall (NGFW)** |
  | --- | --- | --- |
  
  |     |     |     |
  | --- | --- | --- |
  | **Grundprinzip** | Filterung von IP-Adressen, Ports, Protokollen | Zusätzlich Anwendungserkennung und Layer-7-Kontrolle |
  
  |     |     |     |
  | --- | --- | --- |
  | **Paketprüfung** | Nur Paketkopf (Header) | Deep Packet Inspection (DPI), auch Payload und verschlüsselter Traffic |
  
  |     |     |     |
  | --- | --- | --- |
  | **Bedrohungserkennung** | Basis-Schutz vor bekannten Angriffen | Eingebautes Intrusion Prevention System (IPS) + Threat Intelligence |
  
  |     |     |     |
  | --- | --- | --- |
  | **Richtliniensteuerung** | IP- und Port-basiert | Kontext-/Identitätsbasiert: Benutzer, Gruppen, Geräte, Standort |
  
  |     |     |     |
  | --- | --- | --- |
  | **Zusatzfunktionen** | Eingeschränkt | SSL/TLS-Inspektion, Anwendungssteuerung, granulare Policies |
  
- **Passwort-Policy entwerfen:** Erstellt in einem geteilten Dokument den Entwurf für eine einfache Passwort-Richtlinie für die "KreativKopf GmbH". Legt darin die Mindestlänge, die Komplexitätsanforderungen (Groß-/Kleinbuchstaben, Zahlen, Sonderzeichen) und das Wechselintervall fest.
  
  ## 1\. Geltungsbereich
  
  Diese Richtlinie gilt für alle Mitarbeiter:innen, externen Mitarbeitenden und Dienstleister, die Zugang zu IT-Systemen, Anwendungen oder Daten der KreativKopf GmbH haben.
  
  ## 2\. Mindestanforderungen an Passwörter
  
  Alle Passwörter müssen folgende Kriterien erfüllen:
  
  - **Mindestlänge:** 12 Zeichen
  - **Komplexität:**
    - Mindestens ein Großbuchstabe (A–Z)
    - Mindestens ein Kleinbuchstabe (a–z)
    - Mindestens eine Zahl (0–9)
    - Mindestens ein Sonderzeichen (z. B. !, @, #, \$, %, &, \*)
  
  ## 3\. Passwortwechsel
  
  - Passwörter müssen **alle 90 Tage** geändert werden.
  - Vorherige **5 Passwörter dürfen nicht erneut verwendet** werden.
  
  ## 4\. Zusätzliche Empfehlungen
  
  - Nutzung von **Passwort-Managern** wird empfohlen, um sichere und einzigartige Passwörter zu erstellen und zu verwalten.
  - Zwei-Faktor-Authentifizierung (2FA) sollte immer aktiviert werden, wenn verfügbar.
  
  ## 5\. Verantwortung
  
  - Jede:r Nutzer:in ist verantwortlich für die Sicherheit ihres/seines Passworts.
  - Verdacht auf Missbrauch oder Passwortverlust ist **sofort an die IT-Abteilung zu melden**

**Diskussion:** Diskutiert die Aussage: "Der Mensch ist das schwächste Glied in der Sicherheitskette. Deshalb sind organisatorische Maßnahmen wie Schulungen wichtiger als technische Maßnahmen." Findet Pro- und Contra-Argumente.

## **Pro-Argumente (für die Aussage)**

- **Menschliche Fehler sind häufige Ursache von Sicherheitsvorfällen**
- Phishing, unsichere Passwörter oder versehentliches Weitergeben von sensiblen Daten sind Beispiele, bei denen Menschen trotz technischer Schutzmaßnahmen Sicherheitslücken verursachen
- **Technische Maßnahmen allein reichen nicht aus**
- Firewalls, Virenscanner oder Verschlüsselung schützen nur innerhalb der vorgesehenen Parameter. Wird der Mensch überlistet, kann das System trotzdem kompromittiert werden
- **Schulungen erhöhen das Sicherheitsbewusstsein**
- Mitarbeiter:innen, die regelmäßig geschult werden, erkennen Sicherheitsrisiken eher und handeln vorsichtiger, wodurch viele Angriffe bereits im Vorfeld abgewehrt werden
- **Organisatorische Maßnahmen sind oft kosteneffizient**
- Präventive Schulungen oder Richtlinien sind häufig günstiger als aufwendige technische Systeme und reduzieren die Wahrscheinlichkeit von Zwischenfällen langfristig

## **Contra-Argumente (gegen die Aussage)**

- **Technische Maßnahmen sind zwingend notwendig**
- Auch geschulte Mitarbeiter:innen können Fehler machen. Starke Firewalls, Multi-Faktor-Authentifizierung und automatische Updates verhindern Schäden, selbst wenn ein Mensch versehentlich eine falsche Aktion ausführt
- **Nicht jeder Mensch verhält sich immer korrekt**
- Schulungen erhöhen das Bewusstsein, garantieren aber kein fehlerfreies Verhalten. Manche Angriffe wie Social Engineering können selbst geschulte Personen täuschen
- **Menschliche Faktoren sind schwer zu kontrollieren**
- Motivation, Stress oder Ablenkung beeinflussen Verhalten, während technische Systeme konsistent arbeiten
- **Synergieeffekt ist entscheiden**
- Sicherheitsmaßnahmen wirken am besten in Kombination: Technik schützt, Menschen erkennen und reagieren auf ungewöhnliche Situationen. Eine einseitige Fokussierung auf Schulungen kann falsche Sicherheit suggerieren

# Quellen und Vertiefung

1. **Authentisierung**  
  Der Fokus ist auf den Benutzer gerichtet, der sich am System anmeldet. Dazu weist er seine Identität nach, indem er z.B. seinen Benutzernamen und das dazugehörige Passwort eingibt. Die Authentisierung kann auch in anderer Form erfolgen, z.B. durch eine Magnetkarte oder biometrische Merkmale.
2. **Authentifizierung**  
  In diesem Schritt ist das System am Zug. Im Rahmen der Authentifizierung überprüft das System die vom Benutzer gemachten Angaben. Dazu werden die eingegebenen Daten mit den Einträgen in der zugehörigen Datenbank, wie z.B. dem hinterlegten Benutzernamen und dem Hashwert des Passworts, verglichen.
3. **Autorisierung**  
  Erst nach erfolgreicher Authentifizierung kann die Autorisierung, d.h. die Festlegung der Zugriffsberechtigung erfolgen. Dabei werden dem Benutzer seine Rechte zugewiesen. Die Zugriffsrechte entscheiden darüber, in welchem Umfang das System genutzt werden kann und ob z.B. personenbezogene Daten eingesehen oder verändert werden können.

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.6 "Maßnahmen" (S. 1000-1018).
- **Online-Ressource:** [BSI IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html) (bietet zu allen Bausteinen konkrete Maßnahmen).