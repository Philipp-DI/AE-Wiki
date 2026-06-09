# Olena

Als angehender Webentwickler möchte ich die häufigsten Schwachstellen in Webanwendungen kennen, damit ich von Anfang an sichere Webanwendungen entwickeln und bestehende Anwendungen auf grundlegende Risiken prüfen kann.

# Celebration Criteria

- Wir können den Zweck der OWASP Top 10 erklären.  
  <br/>**OWASP Top 10** ist eine Liste der zehn kritischsten Sicherheitsrisiken für Webanwendungen, herausgegeben vom **Open Web Application Security Project (OWASP)**. Sie soll Entwicklern und Unternehmen helfen zu erkennen, auf welche Schwachstellen sie besonders achten müssen, um ihre Anwendungen zu schützen.
  
  ### **Zweck der OWASP Top 10**
  
  1. **Bewusstsein für Sicherheit schaffen:**  
    Zeigt häufige Sicherheitsfehler, die zu Hacks führen können.
  2. **Priorisierung von Sicherheitsmaßnahmen:**  
    Fokus auf die kritischsten Bedrohungen.
  3. **Empfehlungen zur Absicherung:**  
    Für jede Schwachstelle gibt es Best Practices.
  4. **Standardisierung:**  
    Die Liste wird häufig in Audits, Zertifizierungen und Schulungen genutzt.
  5. **Sichere Softwareentwicklung fördern:**  
    Dient als Checkliste, um Sicherheitslücken frühzeitig zu verhindern.
- Wir können mindestens drei der häufigsten Schwachstellen (z.B. Injection, Broken Authentication, Cross-Site Scripting) mit einfachen Worten beschreiben.
  
  | Risiko | Beschreibung | Beispiel |
  | --- | --- | --- |
  | **A01: Broken Access Control** | Fehlerhafte Zugriffskontrolle | Ein Benutzer kann Daten anderer sehen, indem er die URL manipuliert (ID=123 → ID=124) |
  | **A02: Cryptographic Failures** | Unsichere Verschlüsselung | Passwörter werden unverschlüsselt oder mit schwacher Hash-Funktion gespeichert |
  | **A03: Injection** | SQL-/Command-Injection | Eingabe von `'; DROP TABLE users;--` in ein Login-Formular löscht die Tabelle |
  | **A05: Security Misconfiguration** | Fehlkonfigurationen | Webserver gibt Verzeichnisse ohne Authentifizierung frei |
  | **A07: Identification & Authentication Failures** | Fehler bei Authentifizierung | Schwache Passwörter oder keine Limitierung von Login-Versuchen |
  
- Wir können das Prinzip einer SQL-Injection an einem Code-Beispiel erläutern.  
  
- Wir können grundlegende Gegenmaßnahmen wie die Validierung von Benutzereingaben als zentrales Sicherheitsprinzip begründen.  
  <br/>**Kernaussage:** Eingabevalidierung trennt _Daten_ von _Code/Logik_. Wenn Eingaben geprüft und auf erwartete Formate begrenzt werden, sinkt das Risiko für Injektionen (z. B. SQL‑Injection), Umgehung von Zugriffsregeln, Abstürze und andere Sicherheitsvorfälle deutlich.
  
  # Wichtige Gründe
  
  - **Verhindert Injektionen** (SQL, OS‑Befehle, LDAP, XPath usw.).
  - **Schützt Geschäftslogik und Berechtigungen** vor Manipulation durch unerwartete Werte.
  - **Reduziert Angriffsfläche** — weniger unerwartete Daten = weniger mögliche Exploits.
  - **Verbessert Stabilität** (keine Abstürze durch falsche Typen oder zu große Eingaben).
  - **Erleichtert Monitoring & Forensik** (normalisierte, geprüfte Daten sind leichter analysierbar).
  
  # Grundprinzipien der Validierung
  
  1. **Whitelist vor Blacklist:** nur erwartete Werte und Formate erlauben.
  2. **Fail‑fast / Reject‑unknown:** ungültige Eingaben sofort ablehnen.
  3. **Serverseitig validieren:** Client‑Validierung ist nützlich für UX, ersetzt aber nicht die serverseitige Prüfung.
  4. **Normalisieren vor Validierung:** (z. B. URL‑Decoding) bevor geprüft wird.
  5. **Kontext‑bewusst prüfen:** Regeln hängen vom Zielkontext ab (SQL, HTML, Dateisystem, Shell).
  6. **Defense‑in‑depth:** Validierung ist eine Schicht — ergänzen mit Parameterisierung, Output‑Encoding, Rechtemanagement.
  
  # Konkrete Maßnahmen (kurz)
  
  - **Typprüfung:** IDs als Integer, Datum im ISO‑Format, etc.
  - **Längenbegrenzungen:** Maximalwerte für Textfelder (z. B. Name ≤ 256).
  - **Regex‑Whitelist:** nur erlaubte Zeichen/Pattern (z. B. für E‑Mail, UUID).
  - **Parameterisierte Queries / Prepared Statements:** niemals SQL‑Strings per String‑Konkatenation bauen.
  - **File‑Uploads:** MIME‑Type prüfen, Größe limitieren, Dateien außerhalb des Webroots speichern, zufällige Dateinamen verwenden.
  - **Rate‑Limits / Quotas:** Begrenzung von Anfragen zur Vermeidung von Brute‑Force/DoS.
  - **Least Privilege:** DB‑Benutzer mit minimalen Rechten.
  - **Logging & Monitoring:** fehlgeschlagene Validierungen protokollieren und Alarme setzen.
  - **Tests:** Unit‑Tests, Fuzzing, SAST/DAST und regelmäßige Pen‑Tests.
  
  # Beispiele (sehr kurz, konzeptionell)
  
  - Feld `user_id` → prüfen: ist Integer und im erlaubten Bereich?
  - Feld `email` → prüfen: Regex (Whitelist) + Länge ≤ 254 + Domain‑Normalisierung.
  - Upload `avatar` → prüfen: Content‑Type in {image/png,image/jpeg}, Größe ≤ 5 MB, speichern außerhalb von /var/www/html mit neuem Dateinamen.
  
  # Checkliste (für Entwickler / Code‑Reviews)
  
  - Serverseitige Validierung für alle Eingaben implementiert?
  - Whitelist‑Regeln für jedes Feld definiert und dokumentiert?
  - Maximale Längen gesetzt und durchgesetzt?
  - Parameterisierte Datenbankabfragen verwendet (keine String‑Konkatenation)?
  - Uploads validiert und sicher gespeichert?
  - DB‑Zugang mit Least‑Privilege konfiguriert?
  - Fehlgeschlagene Validierungen werden geloggt und überwacht?
  - Unit‑Tests und Security‑Tests (Fuzzing/SAST/DAST) vorhanden?
  
  # Kurze Empfehlung für die Praxis
  
  1. Definiere für jedes Eingabefeld eine **erlaubte Form** (Typ, Länge, Pattern).
  2. Implementiere **serverseitige** Validierung als erste Verteidigungslinie.
  3. Nutze **parameterisierte Abfragen** für DB‑Zugriffe.
  4. Ergänze durch **Monitoring**, **Logging** und regelmäßige Security‑Tests.
  5. Behandle Validierung als Teil der Code‑Qualität: dokumentieren, testen, in CI integrieren

# Wissens-Briefing

Webanwendungen sind oft das "Tor zum Unternehmen" und daher ein Hauptziel für Angreifer. Die **OWASP (Open Web Application Security Project)** ist eine Non-Profit-Organisation, die das Bewusstsein für die Sicherheit von Software verbessern will. Ihr bekanntestes Projekt ist die **OWASP Top 10**, eine Liste der kritischsten Sicherheitsrisiken für Webanwendungen.

**Einige Beispiele aus der OWASP Top 10:**

- **A01: Broken Access Control (fehlerhafte Zugriffskontrolle):** Benutzer können auf Daten oder Funktionen zugreifen, für die sie keine Berechtigung haben (z.B. ein normaler User kann Admin-Funktionen aufrufen, indem er die URL manipuliert).
- **A03: Injection (Einschleusung):** Ein Angreifer sendet bösartige Daten an eine Anwendung, die diese ungeprüft weiterverarbeitet. Der bekannteste Typ ist die **SQL-Injection**. Hier werden SQL-Befehle über ein Eingabefeld (z.B. die Suche) in die Datenbank der Anwendung "injiziert", um Daten auszulesen oder zu manipulieren.
- **A07: Identification and Authentication Failures (Fehler bei der Identifizierung und Authentifizierung):** Schwachstellen im Login-Prozess, z.B. schwache Passwörter, fehlende Multi-Faktor-Authentifizierung oder unsichere Passwort-Wiederherstellungsfunktionen.

Ein Kernprinzip zur Vermeidung vieler dieser Schwachstellen lautet: **"Never trust user input!" (Vertraue niemals Benutzereingaben!)**. Alle Daten, die von außen kommen, müssen validiert und bereinigt werden, bevor sie verarbeitet werden.

# Aufgaben

1. **Recherche:** Wählt in eurer Gruppe drei Risiken aus der aktuellen OWASP Top 10 aus. Erstellt für jedes Risiko einen kurzen Steckbrief, der die Schwachstelle und ein einfaches Beispiel beschreibt.  
  
2. **SQL-Injection verstehen:** Analysiert den folgenden (unsicheren) PHP-Code-Schnipsel: `$sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";`. Diskutiert, was ein Angreifer in das `username`\-Feld eingeben könnte, um die Abfrage zu manipulieren (z.B. um sich ohne Passwort einzuloggen).  
  <br/>Ursprünglicher unsicherer Code
  
  ```
  $sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";
  ```
  
  Hier wird der rohe Benutzer‑Input **direkt** in die SQL‑Zeichenkette eingefügt. Damit kann ein Angreifer die Struktur der Abfrage verändern.
  
  ---
  
  ## Was kann ein Angreifer in `username` eingeben — Beispiele und was sie bewirken
  
  1. **Login‑Bypass (WHERE immer wahr machen)**  
    Payload:
  
  ```
  ' OR '1'='1
  ```
  
  Eingesetzt ergibt das (nach Einfügen):
  
  ```
  SELECT * FROM users WHERE username = '' OR '1'='1';
  ```
  
  Da `'1'='1'` immer wahr ist, liefert die Abfrage (je nach Anwendung) womöglich eine Benutzerzeile — in Verbindung mit fehlerhafter Auth‑Logik kann das eine Anmeldung ohne Passwort ermöglichen.
  
  2. **Kommentar anhängen, um Rest der Query zu ignorieren**  
    Payload:
  
  ```
  ' OR '1'='1' --
  ```
  
  Ergebnis (bei SQL‑Kommentar `--`):
  
  ```
  SELECT * FROM users WHERE username = '' OR '1'='1' -- ';
  ```
  
  Alles nach `--` wird als Kommentar behandelt. Sehr nützlich, wenn hinter dem username noch andere Bedingungen stünden (z. B. `AND password = '...'`), dann werden diese ausgeblendet.
  
  3. **Union‑Attack — zusätzliche Daten auslesen**  
    Payload (vereinfachtes Beispiel):
  
  ```
  ' UNION SELECT credit_card,1,1 FROM payments --
  ```
  
  Ergebnis:
  
  ```
  SELECT * FROM users WHERE username = '' UNION SELECT credit_card,1,1 FROM payments -- ';
  ```
  
  Damit kann der Angreifer versuchen, Daten aus anderen Tabellen zu kombinieren (funktioniert nur wenn Spaltenanzahl/Typen passen).
  
  4. **Zerstörerischer Befehl (wenn DB stacked queries erlaubt)**  
    Payload:
  
  ```
  '; DROP TABLE users; --
  ```
  
  Ergebnis:
  
  ```
  SELECT * FROM users WHERE username = ''; DROP TABLE users; -- ';
  ```
  
  Achtung: Viele DB‑Treiber verbieten mehrere Statements pro Query; trotzdem ist dieser Angriff möglich in manchen Konfigurationen.
  
  5. **Fehlermeldungs‑Based Injection**  
    Payloads, die Fehler erzwingen, um Informationen (Schema, Spaltennamen) aus Fehlermeldungen zu ziehen — nützlich beim Recon.
  
  ---
  
  ## Warum das gefährlich ist
  
  - Manipulation von WHERE‑Bedingungen → Authentifizierungsumgehung, Datenabzug.
  - UNION/SELECT → vertrauliche Daten aus anderen Tabellen auslesen.
  - DROP/ALTER → Datenverlust.
  - Erhöhte Angriffsfläche bei ausführbaren Statements oder unsauberer Konfiguration.
  
  ---
  
  ## Wichtige Details (DB‑abhängig)
  
  - Kommentar‑Syntax: `--` (häufig), `#` (MySQL), `/* ... */` (mehrzeilig).
  - Manche DBs/Treiber erlauben **keine** mehreren Statements pro `execute()` — dann klappt `DROP TABLE;` nicht direkt.
  - Typ‑ und Spaltenanzahl beim `UNION` müssen passen.
  - Fehlermeldungen sollten nicht an Nutzer geleakt werden (Information Disclosure).
  
  ---
  
  ## Sofortmaßnahmen — wie man das sicher macht
  
  ### 1) Parameterisierte Queries / Prepared Statements (empfohlen)
  
  Beispiel mit PDO:
  
  ```
  $stmt = $pdo->prepare("SELECT * FROM users WHERE username = ?");
  $stmt->execute([$_POST['username']]);
  $user = $stmt->fetch();
  ```
  
  Oder benannte Parameter:
  
  ```
  $stmt = $pdo->prepare("SELECT * FROM users WHERE username = :username");
  $stmt->execute([':username' => $_POST['username']]);
  ```
  
  Parameter werden als **Daten** behandelt — Angreifer können die SQL‑Struktur nicht verändern.
  
  ### 2) Zusätzliche Schutzschichten
  
  - **Whitelist‑Validierung** (z. B. erlaubte Zeichen/Max‑Länge).
  - **Least privilege:** DB‑User nur mit notwendigen Rechten.
  - **Output‑und Error‑Handling:** Keine detaillierten DB‑Fehlermeldungen an Endnutzer.
  - **WAF / Monitoring / Logging:** Erkennen und blockieren verdächtiger Patterns.
  - **Prepared Statements + ORM** nutzen — viele Frameworks binden das automatisch ein.
  
  ---
  
  ## Kurzes Fazit
  
  Der gezeigte Einzeiler ist anfällig, weil er Code und Daten vermischt. Ein Angreifer kann durch gezielte Eingaben (z. B. `' OR '1'='1' --`) die Abfrage so manipulieren, dass sie unerwünschte Ergebnisse liefert (Login‑Bypass, Datenleck, Zerstörung). **Die zuverlässige Lösung** ist Parameterisierung (prepared statements) kombiniert mit Validierung, least privilege und gutem Fehler‑/Logging‑Management.  
  <br/>
3. **Gegenmaßnahmen finden:** Brainstormt, welche Maßnahmen die "KreativKopf GmbH" ergreifen muss, um ihr neues Kundenportal (eine Webanwendung) gegen die von euch recherchierten OWASP Top 10  
  Risiken abzusichern.  
  
  | Risiko | Beschreibung | Einfaches Beispiel | Kurzmaßnahmen |
  | --- | --- | --- | --- |
  | **Broken Access Control (A01)** | Fehlerhafte Zugriffskontrolle erlaubt Benutzern, auf Daten/Funktionen ohne Berechtigung zuzugreifen. | Benutzer ändert URL von `/orders?id=101` → `/orders?id=102` und sieht Bestellungen anderer. | Serverseitige Zugriffskontrolle, _deny by default_, rollenbasierte Berechtigungen. |
  | **Cryptographic Failures (A02)** | Fehlerhafte/fehlende Kryptografie führt zu Offenlegung sensibler Daten (unsichere Algorithmen, fehlendes TLS, unsicher gespeicherte Passwörter). | Passwörter in DB als Klartext oder MD5 ohne Salt gespeichert → bei DB-Diebstahl sofort nutzbar. | Starke Algorithmen (bcrypt/argon2), TLS, sichere Schlüsselverwaltung, Rotation von Geheimnissen. |
  | **Injection (A03)** | Ungeprüfte Eingaben werden in SQL/OS/LDAP-Interpreter eingebracht, Angreifer können Befehle einschleusen. | SQL-Login: `SELECT * FROM users WHERE username = 'EINGABE' AND password = 'EINGABE';` → Eingabe `' OR '1'='1` erlaubt Login ohne Passwort. | Prepared Statements/Parameterbindung, Whitelist-Validierung, least-privilege DB-Zugänge. |
  | **Security Misconfiguration (A05)** | Unsichere Standardkonfigurationen oder falsche Einstellungen öffnen Angriffsflächen. | Ein Webserver zeigt das Verzeichnis `/uploads` ohne Authentifizierung, jeder kann Dateien ansehen oder hochladen. | Minimale Standardrechte, geschützte Konfigurationen, regelmäßige Überprüfung, sichere Defaults. |
  | **Identification & Authentication Failures (A07)** | Fehlerhafte Authentifizierung oder Session-Management erlaubt Kontenübernahme. | Keine Limitierung von Login-Versuchen → Brute-Force-Angriff möglich. | Starke Passwörter erzwingen, Multi-Faktor-Authentifizierung, Session-Timeouts, Login-Limits. |
  

# Quellen und Vertiefung

- **Online-Ressource:** [OWASP Top 10 - 2021 (Offizielle Seite)](https://owasp.org/Top10/)
- **Online-Ressource:** [Heise.de - Serie zur OWASP Top 10](https://www.google.com/search?q=https://www.heise.de/thema/OWASP-Top-10)