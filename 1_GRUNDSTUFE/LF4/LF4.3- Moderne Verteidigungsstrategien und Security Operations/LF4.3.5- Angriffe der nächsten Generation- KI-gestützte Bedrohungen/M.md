# Mohammed

Als Security Analyst

möchte ich die Möglichkeiten von KI-gestützten Angriffen kennen,

damit ich unsere Verteidigungsstrategien anpassen und Mitarbeiter für neue, raffinierte Arten von Social Engineering sensibilisieren kann.

# Celebration Criteria

- Wir können erklären, wie Künstliche Intelligenz (KI) genutzt wird, um Phishing- und Social-Engineering-Angriffe zu verbessern.
- Wir können das Konzept von "Deepfakes" (Audio und Video) und die daraus resultierende Gefahr für Unternehmen beschreiben.
- Wir können den Unterschied zwischen "Offensive AI" (Angriff) und "Defensive AI" (Verteidigung) skizzieren.
- Wir können Merkmale identifizieren, die auf eine potenziell KI-generierte Phishing-Mail oder einen Deepfake-Anruf hindeuten könnten.

# Wissens-Briefing

Künstliche Intelligenz wird nicht nur für legitime Zwecke, sondern auch von Angreifern eingesetzt, um ihre Methoden zu verfeinern (**Offensive AI**).

**Verbesserte Angriffe durch KI:**

- **Hyper-personalisiertes Phishing (Spear Phishing):** KI-Systeme können riesige Mengen an öffentlich verfügbaren Informationen (z.B. aus sozialen Netzwerken) analysieren, um extrem überzeugende und individuell zugeschnittene Phishing-Mails zu erstellen, die kaum noch von echten E-Mails zu unterscheiden sind. Die klassischen Fehler (schlechte Grammatik etc.) entfallen.
- **Deepfakes (Audio & Video):** KI kann die Stimme einer Person klonen (oft reichen wenige Sekunden Audiomaterial) oder ihr Gesicht in einem Video realistisch animieren. Dies wird für Betrugsmaschen wie den **CEO Fraud** eingesetzt: Ein Angreifer ruft als vermeintlicher Geschäftsführer in der Buchhaltung an und weist eine dringende Überweisung an. Die Stimme klingt täuschend echt.
- **Automatisierte Schwachstellensuche:** KI kann Code analysieren und neue, bisher unbekannte Sicherheitslücken (Zero-Day-Exploits) wesentlich schneller finden als menschliche Forscher.

Gleichzeitig wird KI aber auch zur Verteidigung eingesetzt (**Defensive AI**), z.B. um in riesigen Datenmengen (Logs) anomales Verhalten zu erkennen, das auf einen Angriff hindeuten könnte.

# Aufgaben

> 1. **Deepfake-Recherche:** Recherchiert einen realen Fall von CEO-Betrug, bei dem eine geklonte Stimme zum Einsatz kam. Fasst den Fall kurz zusammen und beschreibt den entstandenen Schaden.

:::success
Ein sehr bekannter und erschreckender Fall von **CEO Fraud** (Geschäftsführer-Betrug) ereignete sich 2019 bei einem britischen Energieunternehmen.

- **Der Vorfall:** Ein Angreifer nutzte KI-Software, um die Stimme des deutschen Mutterkonzern-Chefs perfekt zu imitieren. Er rief den Geschäftsführer der britischen Tochtergesellschaft an und wies ihn an, dringend **220.000 Euro** an einen ungarischen Lieferanten zu überweisen.
- **Der Clou:** Die Stimme klang so täuschend echt (inklusive des deutschen Akzents und der typischen Sprechweise), dass das Opfer keinen Verdacht schöpfte.
- **Der Schaden:** Das Geld wurde überwiesen und war sofort weg. Es ist ein Paradebeispiel für die Gefahr von Audio-Deepfakes.
:::

> 2. **Analyse:** Vergleicht eine "klassische" Phishing-Mail mit einer hypothetischen, KI-generierten Spear-Phishing-Mail. Erstellt eine Tabelle mit den Unterschieden in Bezug auf Anrede, Sprache, Inhalt und Glaubwürdigkeit.

:::success
### Analyse: Klassisches Phishing vs. KI-Spear-Phishing

Der gewaltige Unterschied zwischen den "alten" Methoden und den neuen, KI-gestützten Angriffen:

|     |     |     |
| --- | --- | --- |
| **Merkmal** | **Klassische Phishing-Mail** | **KI-generiertes Spear Phishing** |
| **Anrede** | Allgemein **("Sehr geehrter Kunde")** | Hochgradig persönlich **("Hallo Vorname")** |
| **Sprache** | Oft fehlerhaft (Grammatik, Rechtschreibung) | Perfektes Deutsch, fehlerfrei und professionell |
| **Inhalt** | Standard-Text (z. B. "Konto gesperrt") | Bezieht sich auf reale Projekte oder LinkedIn-Posts |
| **Glaubwürdigkeit** | Gering (wirkt oft "billig") | Extrem hoch, wirkt wie vom Kollegen |
:::

> 3. **Verhaltensregeln entwerfen:** Erstellt in der Gruppe einen kurzen Leitfaden (5 Verhaltensregeln) für Mitarbeiter der "KreativKopf GmbH" zum Thema "Umgang mit unerwarteten Anrufen oder E-Mails von der Geschäftsführung mit Zahlungsaufforderungen". Was sollte man tun, um einen Deepfake-Betrug zu verhindern?

:::success
**Um sich gegen Deepfakes und KI-Betrug zu schützen, brauchen wir klare Verhaltensregeln.**

- **Explizite Überprüfung (Verify explicitly):** Bei jeder dringenden Zahlungsaufforderung muss ein **zweiter Kanal** zur Bestätigung genutzt werden. **\==(den Chef unter seiner bekannten Nummer zurück).==**
- **Codewort vereinbaren:** In der Geschäftsführung und Buchhaltung wird ein internes, geheimes **Codewort** eingeführt, das bei außerordentlichen Überweisungen genannt werden muss.
- **Gesunde Skepsis bei "Dringlichkeit":** KI-Angriffe nutzen oft künstlichen Zeitdruck aus. Ruhig bleiben, wenn es heißt: **\=="Das Geld muss in 10 Minuten raus sein!"==**
- **Achten auf Deepfake-Merkmale:** Bei Videoanrufen auf unnatürliche Augenbewegungen, seltsame Schatten oder metallisch wirkende Stimmen achten. Bittet man die Person im Zweifel, sich einmal zur Seite zu drehen (das bricht oft die KI-Animation ab).
- **Keine sensiblen Daten am Telefon:** Man gibt niemals Zugangsdaten oder interne Details preis, nur weil der Anrufer "wichtig" klingt.
:::

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Deepfakes: Potenziale, Risiken und Handlungsbedarf](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/Studien/Deepfakes/Deepfakes.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Tagesschau.de - Wie KI-Betrüger mit Stimmen-Klonen Geld erbeuten](https://www.google.com/search?q=https://www.tagesschau.de/investigativ/br-recherche/ki-stimmen-klonen-betrug-100.html)