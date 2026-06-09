# Olena

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

1. **Deepfake-Recherche:** Recherchiert einen realen Fall von CEO-Betrug, bei dem eine geklonte Stimme zum Einsatz kam. Fasst den Fall kurz zusammen und beschreibt den entstandenen Schaden.  
  Fall: Deepfake-Voice-Betrug (2019)
  
  ```
  Was passierte: Betrüger imitierten per KI die Stimme eines deutschen CEOs und riefen den Chef einer britischen Tochtergesellschaft an.
  
  Die Täuschung: Die Stimme war so perfekt (Akzent, Klang), dass der Mitarbeiter glaubte, einen direkten Befehl seines Vorgesetzten zu erhalten.
  
  Die Tat: Er überwies sofort 220.000 € auf ein Konto in Ungarn, im Glauben, es sei eine dringende Zahlung an einen Lieferanten.
  
  Der Schaden: Das Geld wurde nach Mexiko weitergeleitet und ist verloren.
  ```
  
2. **Analyse:** Vergleicht eine "klassische" Phishing-Mail mit einer hypothetischen, KI-generierten Spear-Phishing-Mail. Erstellt eine Tabelle mit den Unterschieden in Bezug auf Anrede, Sprache, Inhalt und Glaubwürdigkeit.
  
  |     |     |     |
  | --- | --- | --- |
  | **Merkmal** | **Klassische Phishing-Mail** | **KI-generierte Spear-Phishing-Mail** |
  | **Anrede** | Generisch (z. B. "Sehr geehrter Kunde" oder "Liebe Nutzer"). | Hochgradig personalisiert (Name, Vorname, oft mit Bezug auf die Position). |
  | **Sprache** | Oft fehlerhaft, hölzerner Satzbau oder erkennbare Übersetzungsfehler. | Perfektes Deutsch, Berücksichtigung von Firmenjargon und individuellem Schreibstil. |
  | **Inhalt** | Standard-Szenarien (z. B. Kontosperrung), die massenhaft versendet werden. | Kontextbezogen: Nimmt Bezug auf reale Projekte, Termine oder LinkedIn-Aktivitäten. |
  | **Glaubwürdigkeit** | Gering. Bei genauerem Hinsehen meist leicht als Betrug erkennbar. | Sehr hoch. Wirkt wie eine legitime Fortsetzung eines echten Arbeitsprozesses. |
  
3. **Verhaltensregeln entwerfen:** Erstellt in der Gruppe einen kurzen Leitfaden (5 Verhaltensregeln) für Mitarbeiter der "KreativKopf GmbH" zum Thema "Umgang mit unerwarteten Anrufen oder E-Mails von der Geschäftsführung mit Zahlungsaufforderungen". Was sollte man tun, um einen Deepfake-Betrug zu verhindern?  
  
  |     |     |     |
  | --- | --- | --- |
  | **№** | **Regel** | **Beschreibung** |
  | **1** | **Kanalwechsel (Verify & Call-Back)** | Bei unerwarteten Anrufen/Mails: Legen Sie auf und rufen Sie die Führungskraft über die **bekannte interne Nummer** zurück. Nutzen Sie niemals die Nummer, die Ihnen im verdächtigen Gespräch mitgeteilt wurde. |
  | **2** | **Vier-Augen-Prinzip strikt einhalten** | Keine Zahlung ohne Freigabe durch eine zweite Person. Deepfake-Betrüger versuchen oft, Zeitdruck aufzubauen, um diesen Kontrollschritt zu umgehen. **Dringlichkeit ist ein Warnsignal!** |
  | **3** | **Sicherheitsfragen stellen (Shared Secrets)** | Stellen Sie dem Anrufer Fragen, die eine KI oder ein Fremder nicht wissen kann (z. B. „Was haben wir gestern beim Team-Lunch besprochen?“). Ein Betrüger wird hier ausweichen. |
  | **4** | **Keine vertraulichen Daten am Telefon** | Die Geschäftsführung wird Sie niemals bitten, Passwörter, TANs oder Kontodaten am Telefon preiszugeben. Solche Anfragen sind immer als Betrugsversuch zu werten. |
  | **5** | **Sofortige Meldepflicht (Incident Reporting)** | Melden Sie jeden verdächtigen Kontakt sofort der IT-Sicherheit oder Ihrem Vorgesetzten – auch wenn Sie (noch) nicht auf den Betrug reingefallen sind. So schützen Sie Ihre Kollegen. |
  

# Quellen und Vertiefung

- **Online-Ressource:** [BSI - Deepfakes: Potenziale, Risiken und Handlungsbedarf](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/Studien/Deepfakes/Deepfakes.pdf%3F__blob%3DpublicationFile)
- **Online-Ressource:** [Tagesschau.de - Wie KI-Betrüger mit Stimmen-Klonen Geld erbeuten](https://www.google.com/search?q=https://www.tagesschau.de/investigativ/br-recherche/ki-stimmen-klonen-betrug-100.html)