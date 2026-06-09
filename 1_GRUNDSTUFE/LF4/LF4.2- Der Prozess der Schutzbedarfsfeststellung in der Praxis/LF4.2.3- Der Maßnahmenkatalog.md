# LF4.2.3- Der Maßnahmenkatalog

Als IT-Systemadministrator

möchte ich einen Überblick über gängige technisch-organisatorische Maßnahmen (TOMs) gewinnen,

damit ich aus einer Schutzbedarfsfeststellung konkrete und angemessene Handlungsempfehlungen ableiten kann.

# Celebration Criteria

- Wir können technische und organisatorische Maßnahmen voneinander unterscheiden.
- Wir können für die Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit jeweils mindestens zwei passende Schutzmaßnahmen nennen.
- Wir können den Zweck von Firewalls, Antivirus-Software, Backups und Passwort-Richtlinien erklären.
- Wir können begründen, warum eine Kombination aus technischen und organisatorischen Maßnahmen notwendig ist.![](files/019cee42-e5b1-7349-a9e4-fe093283c21a/image.png)

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
  
  <div class="joplin-table-wrapper"><table style="width: 616px"><tbody><tr><th colspan="1" rowspan="1" colwidth="189"><p data-id="qsmeygrwjxjr">Zielobjekt</p></th><th colspan="1" rowspan="1" colwidth="100"><p data-id="kilaybpxtzfj">Schutzbedarf</p></th><th colspan="1" rowspan="1" colwidth="327"><p data-id="bpulhikbuqvy">Maßnahmen</p></th></tr><tr><td colspan="1" rowspan="2" colwidth="189"><p data-id="nhhyjltygkaw">NAS</p></td><td colspan="1" rowspan="2" colwidth="100"><p data-id="liugggxdajqj">Hoch</p></td><td colspan="1" rowspan="1" colwidth="327"><ol><li><p data-id="ecrfnpzuddeq">Regelmäßige Back-Ups/Datenkontrolle</p></li></ol></td></tr><tr><td colspan="1" rowspan="1" colwidth="327"><ol start="2"><li><p data-id="yxpkxqwofjba">Festplattenverschlüsselung</p></li></ol></td></tr><tr><td colspan="1" rowspan="2" colwidth="189"><p data-id="iiugpfxpmcei">Cloud-Speicher/Zugang</p></td><td colspan="1" rowspan="2" colwidth="100"><p data-id="vjdqximguulp">Sehr hoch</p></td><td colspan="1" rowspan="1" colwidth="327"><ol><li><p data-id="wzobfibffkzz">Datenverschlüsselung</p></li></ol></td></tr><tr><td colspan="1" rowspan="1" colwidth="327"><ol start="2"><li><p data-id="ggxbxfnlkdkg"></p></li></ol></td></tr></tbody></table></div>
  
2. **Recherche "Next-Gen-Firewall":** Recherchiert online, was eine "Next-Generation-Firewall" (NGFW) von einer klassischen Firewall unterscheidet. Stellt die Zusatzfunktionen in 3-4 Stichpunkten vor.
3. **Passwort-Policy entwerfen:** Erstellt in einem geteilten Dokument den Entwurf für eine einfache Passwort-Richtlinie für die "KreativKopf GmbH". Legt darin die Mindestlänge, die Komplexitätsanforderungen (Groß-/Kleinbuchstaben, Zahlen, Sonderzeichen) und das Wechselintervall fest.
4. **Diskussion:** Diskutiert die Aussage: "Der Mensch ist das schwächste Glied in der Sicherheitskette. Deshalb sind organisatorische Maßnahmen wie Schulungen wichtiger als technische Maßnahmen." Findet Pro- und Contra-Argumente.

# Quellen und Vertiefung

1. **Authentisierung**  
  Der Fokus ist auf den Benutzer gerichtet, der sich am System anmeldet. Dazu weist er seine Identität nach, indem er z.B. seinen Benutzernamen und das dazugehörige Passwort eingibt. Die Authentisierung kann auch in anderer Form erfolgen, z.B. durch eine Magnetkarte oder biometrische Merkmale.
2. **Authentifizierung**  
  In diesem Schritt ist das System am Zug. Im Rahmen der Authentifizierung überprüft das System die vom Benutzer gemachten Angaben. Dazu werden die eingegebenen Daten mit den Einträgen in der zugehörigen Datenbank, wie z.B. dem hinterlegten Benutzernamen und dem Hashwert des Passworts, verglichen.
3. **Autorisierung**  
  Erst nach erfolgreicher Authentifizierung kann die Autorisierung, d.h. die Festlegung der Zugriffsberechtigung erfolgen. Dabei werden dem Benutzer seine Rechte zugewiesen. Die Zugriffsrechte entscheiden darüber, in welchem Umfang das System genutzt werden kann und ob z.B. personenbezogene Daten eingesehen oder verändert werden können.

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.6 "Maßnahmen" (S. 1000-1018).
- **Online-Ressource:** [BSI IT-Grundschutz-Kompendium](https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/IT-Grundschutz-Kompendium/it-grundschutz-kompendium_node.html) (bietet zu allen Bausteinen konkrete Maßnahmen).