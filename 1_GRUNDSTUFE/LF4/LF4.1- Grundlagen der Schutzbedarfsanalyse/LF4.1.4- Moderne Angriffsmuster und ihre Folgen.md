# LF4.1.4- Moderne Angriffsmuster und ihre Folgen

Als verantwortungsbewusster IT-Nutzer

möchte ich moderne Angriffsmuster wie Doxing und Identitätsdiebstahl verstehen,

damit ich meine persönlichen und die Unternehmensdaten effektiver schützen kann.

# Celebration Criteria

- Wir können die Begriffe Datenleak, Doxing, Identitätsdiebstahl, SEO-Poisoning und Botnetz definieren.
- Wir können den Zusammenhang zwischen einem Datenleak und einem nachfolgenden Identitätsdiebstahl erklären.
- Wir können beschreiben, wie Botnetze für kriminelle Aktivitäten missbraucht werden.
- Wir können grundlegende Schutzmaßnahmen gegen diese Angriffsarten für Privatpersonen und Unternehmen nennen.

# Wissens-Briefing

Neben klassischen Angriffen gibt es eine Reihe moderner Muster, die oft aufeinander aufbauen und immense Schäden verursachen können.

- **Datenleak (Data Leak):** Die unbeabsichtigte oder unrechtmäßige Veröffentlichung von vertraulichen, geschützten oder sensiblen Daten. Ein Leak kann durch einen Hackerangriff, aber auch durch menschliches Versagen (z.B. eine falsch konfigurierte Datenbank) entstehen.
- **Identitätsdiebstahl:** Die missbräuchliche Verwendung personenbezogener Daten einer anderen Person (Name, Geburtsdatum, Adresse, Kreditkartennummer) durch Dritte, um sich zu bereichern oder dem Opfer zu schaden. Gestohlene Daten aus Leaks sind die Hauptquelle für Identitätsdiebstahl.
- **Doxing:** Das Zusammentragen und anschließende Veröffentlichen von privaten Informationen über eine Person im Internet, oft mit dem Ziel, diese Person einzuschüchtern, zu belästigen oder an den Pranger zu stellen.
- **Botnetz:** Ein Netzwerk aus mit Schadsoftware infizierten Computern ("Bots" oder "Zombies"), die von einem Angreifer (dem "Bot-Herder") ferngesteuert werden. Botnetze werden oft vermietet und für großangelegte Angriffe wie DDoS-Attacken, den Versand von Spam/Phishing-Mails oder das Schürfen von Kryptowährungen genutzt.
- **SEO-Poisoning (Suchmaschinenoptimierungs-Vergiftung):** Angreifer manipulieren Suchmaschinen-Ergebnisse, um ihre bösartigen Webseiten auf den vorderen Plätzen für populäre Suchanfragen zu platzieren. Nutzer, die nach legitimen Inhalten suchen, werden so auf Seiten mit Malware oder Phishing-Inhalten gelockt.

# Aufgaben

1. **Recherche "Have I Been Pwned":** Besucht die Webseite "Have I Been Pwned?" von Troy Hunt. Diskutiert in der Gruppe den Zweck dieser Seite. Welche Rolle spielt sie im Kontext von Datenleaks und Identitätsdiebstahl?
  - **Webseite:** https://haveibeenpwned.com
  - **Erstellt von:** Troy Hunt (Sicherheitsforscher aus Australien)
    - **Zweck der Seite**\- Nutzer können ihre **E-Mail-Adresse** eingeben, um zu prüfen, ob diese in einem **Datenleck** (z. B. bei LinkedIn, Adobe, Dropbox) aufgetaucht ist.- Die Seite listet auf, **wann und wo** die Daten kompromittiert wurden.- Ziel: **Früherkennung von Datenlecks** → Nutzer können Passwörter ändern, bevor Schaden entsteht.
    - **Rolle im Kontext von Datenleaks & Identitätsdiebstahl**\- Hilft, **Kompro­mittierungen** frühzeitig zu erkennen.- Unterstützt Nutzer dabei, **Passwort-Wiederverwendung** zu vermeiden.- Dient als **Sensibilisierungstool**: zeigt, wie verbreitet Datenlecks sind.- Wichtiges Instrument für **Identitätsschutz und Cyberhygiene**.
2. **Szenario-Kette:** Erstellt ein kleines Schaubild (z.B. auf einem Whiteboard), das die Kette eines Angriffs darstellt: Ein Datenleak bei einem Onlineshop führt zum Identitätsdiebstahl bei einem Kunden, dessen Daten anschließend für Doxing missbraucht werden.  
  _Leak → Daten werden (im “Darknet”) veröffentlicht → Daten werden missbraucht → Doxing mithilfe persönlicher, sensibler Daten_
3. **Botnetz-Analyse:** Recherchiert einen bekannten Fall eines Botnetzes (z.B. "Emotet" oder "Mirai"). Beschreibt kurz, wofür das Botnetz verwendet wurde und wie es unschädlich gemacht wurde.https://www.cloudflare.com/de-de/learning/ddos/glossary/mirai-botnet/
  
  | **Botnetz** | **Beschreibung** |
  | --- | --- |
  | **Name:** | Emotet |
  | **Art:** | Schadsoftware (ursprünglich Banking-Trojaner) |
  | **Funktion:** | Infiziert Computer über Phishing-Mails und nutzt sie als Teil eines weltweiten Botnetzes. Wird zur Verbreitung anderer Schadsoftware (z. B. Ransomware) genutzt. |
  | **Verwendung:** | Spam-Kampagnen, Datendiebstahl, Verbreitung von Malware |
  | **Bekämpfung:** | 2021 internationale Aktion von Europol, BKA und FBI → Server-Infrastruktur wurde übernommen und abgeschaltet. |
  
4. **Prävention:** Brainstormt und listet 3 konkrete Tipps für Mitarbeiter der "KreativKopf GmbH" auf, wie sie sich vor SEO-Poisoning schützen können.
  - Immer misstrauisch gegenüber unbekannten Website oder Links sein. (Bei Suchergebnissen)
  - Adressen/URLs PRÜFEN (offiziell?) Bsp.: [Google.com](http://Google.com) (o), [Guugle.com](http://Guugle.com) (f)
  - IT-Sicherheitsschulung besuchen und ernst nehmen
  - Technische Schutzmaßnahmen: Browser-Schutz / Antivirus mit URL-Prüfung einsetzen
  - Firewall (Whitelisting/Blacklisting)

# Quellen und Vertiefung

- **Online-Ressource:** [BSI für Bürger - Identitätsdiebstahl](https://www.google.com/search?q=https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Cyber-Straftaten/Identitaetsdiebstahl/identitaetsdiebstahl_node.html)
- **Online-Ressource:** [BSI für Bürger - Botnetze](https://www.google.com/search?q=https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Cyber-Straftaten/Botnetze/botnetze_node.html)
- **Tool:** [Have I Been Pwned?](https://haveibeenpwned.com/)