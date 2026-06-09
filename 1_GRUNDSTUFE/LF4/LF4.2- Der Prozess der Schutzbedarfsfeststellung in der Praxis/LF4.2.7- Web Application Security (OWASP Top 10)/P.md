# Philipp

Als angehender Webentwickler möchte ich die häufigsten Schwachstellen in Webanwendungen kennen, damit ich von Anfang an sichere Webanwendungen entwickeln und bestehende Anwendungen auf grundlegende Risiken prüfen kann.

# Celebration Criteria

- Wir können den Zweck der OWASP Top 10 erklären.
- Wir können mindestens drei der häufigsten Schwachstellen (z.B. Injection, Broken Authentication, Cross-Site Scripting) mit einfachen Worten beschreiben.
- Wir können das Prinzip einer SQL-Injection an einem Code-Beispiel erläutern.
- Wir können grundlegende Gegenmaßnahmen wie die Validierung von Benutzereingaben als zentrales Sicherheitsprinzip begründen.

# Wissens-Briefing

Webanwendungen sind oft das "Tor zum Unternehmen" und daher ein Hauptziel für Angreifer. Die **OWASP (Open Web Application Security Project)** ist eine Non-Profit-Organisation, die das Bewusstsein für die Sicherheit von Software verbessern will. Ihr bekanntestes Projekt ist die **OWASP Top 10**, eine Liste der kritischsten Sicherheitsrisiken für Webanwendungen.

**Einige Beispiele aus der OWASP Top 10:**

- **A01: Broken Access Control (fehlerhafte Zugriffskontrolle):** Benutzer können auf Daten oder Funktionen zugreifen, für die sie keine Berechtigung haben (z.B. ein normaler User kann Admin-Funktionen aufrufen, indem er die URL manipuliert).
- **A03: Injection (Einschleusung):** Ein Angreifer sendet bösartige Daten an eine Anwendung, die diese ungeprüft weiterverarbeitet. Der bekannteste Typ ist die **SQL-Injection**. Hier werden SQL-Befehle über ein Eingabefeld (z.B. die Suche) in die Datenbank der Anwendung "injiziert", um Daten auszulesen oder zu manipulieren.
- **A07: Identification and Authentication Failures (Fehler bei der Identifizierung und Authentifizierung):** Schwachstellen im Login-Prozess, z.B. schwache Passwörter, fehlende Multi-Faktor-Authentifizierung oder unsichere Passwort-Wiederherstellungsfunktionen.

Ein Kernprinzip zur Vermeidung vieler dieser Schwachstellen lautet: **"Never trust user input!" (Vertraue niemals Benutzereingaben!)**. Alle Daten, die von außen kommen, müssen validiert und bereinigt werden, bevor sie verarbeitet werden.

# Aufgaben

1. **Recherche:** Wählt in eurer Gruppe drei Risiken aus der aktuellen OWASP Top 10 aus. Erstellt für jedes Risiko einen kurzen Steckbrief, der die Schwachstelle und ein einfaches Beispiel beschreibt.
  
  <div class="joplin-table-wrapper"><table style="min-width: 486px"><tbody><tr><th colspan="1" rowspan="1" colwidth="436"><p data-id="tugxtdlaosrj">Risiko &amp; Beschreibung</p></th><th colspan="1" rowspan="1"><p data-id="ppxmvrlqxnaz">Common Weakness Enumerations (CWEs)</p></th><th colspan="1" rowspan="1"><p data-id="dmngthbqdbeo">Beispiel / Szenario</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="ikpjatpwpkqc"><strong>A01:2021 — Broken Access Control:</strong> Wenn ein Nutzer auf Inhalte und Funktionen zugreifen kann, zu denen er eigentlich keine Berechtigung hat.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="vaglwmwelljv">CWE-200: Exposure of Sensitive Information to an Unauthorized Actor</p></li><li><p data-id="dowzrnnxveps">CWE-201: Insertion of Sensitive Information Into Sent Data</p></li><li><p data-id="mstyehcvaleu">CWE-352: Cross-Site Request Forgery.</p></li></ul></td><td colspan="1" rowspan="1"><p data-id="izozoeffknnh">Durch Manipulation der URL gelangt ein Nutzer auf eine Seite, auf die eigentlich nur ein Admin Zugang hat. (z.B. test.de/berichte → test.de/admin_berichte)</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="ljqscbcciauy"><strong>A04:2021 — Insecure Design:</strong> “Unsicheres Design” beschreibt, dass bereits in der Konzeptionierung Sicherheitsmängel entstanden sind. Die Implementierung ist hier NICHT enthalten.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="zklbpshwdwzw">CWE-209: Generation of Error Message Containing Sensitive Information</p></li><li><p data-id="geqpzonnnwqa">CWE-256: Unprotected Storage of Credentials</p></li><li><p data-id="mvelamqqmuro">CWE-501: Trust Boundary Violation</p></li><li><p data-id="bfyrskezctwn">CWE-522: Insufficiently Protected Credentials</p></li></ul></td><td colspan="1" rowspan="1"><p data-id="eeuehqtvopps">Ein Online-Shop hat einen unzureichenden Schutz gegen Bots, die Einkäufe tätigen. Somit wird es Scalpern leicht gemacht.</p></td></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="ojebrvyppxpa"><strong>A03:2021 — Injection:</strong> Das Einschleusen von Befehlen, Skripts, o.ä.. Laut OWASP gibt typischerweise folgende Arten der Injection: SQL, NoSQL, OS command, Object Relational Mapping (ORM), LDAP, und Expression Language (EL) oder Object Graph Navigation Library (OGNL) injection.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="mhrerutyrump">CWE-79: Cross-site Scripting</p></li><li><p data-id="ovkbnklyslts">CWE-89: SQL Injection</p></li><li><p data-id="cccqokthverw">CWE-73: External Control of File Name or Path</p></li></ul></td><td colspan="1" rowspan="1"><p data-id="itqvfqbmozhn">Per SQL-Query können sensible Daten abgefragt und ausgelesen werden. Diese können dann missbraucht, modifiziert oder gelöscht werden.</p></td></tr></tbody></table></div>
  
2. **SQL-Injection verstehen:** Analysiert den folgenden (unsicheren) PHP-Code-Schnipsel: `$sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";`. Diskutiert, was ein Angreifer in das `username`\-Feld eingeben könnte, um die Abfrage zu manipulieren (z.B. um sich ohne Passwort einzuloggen).Aufgrund starken Mangels an Wissen in diesem Bereich und des starken Zeitdrucks, habe ich mir das Ganze von Gemini erklären lassen:
  
  ### Analyse der SQL-Injection-Schwachstelle
  
  Das Kernproblem in diesem PHP-Code-Schnipsel ist die **direkte Verkettung** von Benutzereingaben in eine SQL-Abfrage.PHP
  
  ```
  // Unsicherer Code
  $sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";
  ```
  
  Hier wird alles, was im Formularfeld `username` gesendet wird (`$_POST['username']`), direkt zwischen die einfachen Anführungszeichen (`'`) im SQL-String eingefügt. Ein Angreifer kann dies ausnutzen, indem er nicht nur einen Benutzernamen, sondern auch eigene SQL-Befehle eingibt.
  
  ---
  
  ### Was ein Angreifer eingeben könnte
  
  Ein klassisches Beispiel, um die Authentifizierung zu umgehen (wie Sie erwähnten, "ohne Passwort einloggen", obwohl diese Abfrage nur Benutzer auswählt), wäre die Eingabe von:`' OR '1'='1`
  
  #### Was passiert im Hintergrund?
  
  Wenn der Angreifer diesen String eingibt, setzt PHP ihn in die `$sql`\-Variable ein:
  
  - **Original-Template:** `SELECT * FROM users WHERE username = '` ... `';`
  - **Eingabe des Angreifers:** `' OR '1'='1`
  - **Resultierende SQL-Abfrage:** `SELECT * FROM users WHERE username = '' OR '1'='1';`
  
  #### Warum ist das gefährlich?
  
  Schauen wir uns die resultierende `WHERE`\-Klausel an: `WHERE username = '' OR '1'='1`
  
  - Der Server prüft zuerst `username = ''`. Das ist wahrscheinlich `false` (es sei denn, es gibt einen Benutzer mit leerem Namen).
  - Dann prüft er das `OR`.
  - Danach prüft er `'1'='1'`. Dies ist **immer** `true`.
  
  Da die Bedingung `false OR true` zu `true` ausgewertet wird, wird die `WHERE`\-Klausel für **jede einzelne Zeile** in der `users`\-Tabelle wahr. Die Abfrage `SELECT * FROM users WHERE true;` gibt also einfach **alle Benutzer** aus der Datenbank zurück, anstatt nur den einen, der angefragt wurde.Wenn dies ein Login-Skript wäre (das auch ein Passwort prüft), könnte ein Angreifer eine ähnliche Technik verwenden (z. B. durch Hinzufügen von `--` oder `#` am Ende, um den Rest der Abfrage auszukommentieren), um die Passwortprüfung komplett zu umgehen.
  
  ---
  
  ### 🔒 Wie man es richtig macht (Prävention)
  
  Um diese Art von Angriff zu verhindern, sollte man **niemals** Benutzereingaben direkt in Abfragen einbauen. Die Standardlösung sind **Prepared Statements** (Vorbereitete Anweisungen) mit Parameterbindung.Hier ist ein sicheres Beispiel (unter Verwendung von PDO, einer modernen PHP-Datenbankerweiterung):
  
  ```
  // Sicherer Code mit Prepared Statements
  $username = $_POST['username'];
  
  // 1. Die Abfrage vorbereiten (mit einem Platzhalter '?')
  $stmt = $pdo->prepare("SELECT * FROM users WHERE username = ?");
  
  // 2. Die Abfrage sicher ausführen (die Datenbank fügt den Wert selbst ein)
  $stmt->execute([$username]);
  
  // 3. Ergebnisse abrufen
  $user = $stmt->fetch();
  ```
  
  Bei dieser Methode wird die Benutzereingabe (`$username`) getrennt von der SQL-Anweisung an die Datenbank gesendet. Die Datenbank "weiß", dass der Wert im Platzhalter `?` nur ein Datenwert und **niemals** ein SQL-Befehl sein darf. Selbst wenn ein Angreifer `' OR '1'='1` eingibt, sucht die Datenbank einfach nach einem Benutzer mit dem exakten (und unsinnigen) Namen `' OR '1'='1` und wird (höchstwahrscheinlich) nichts finden.
3. **Gegenmaßnahmen finden:** Brainstormt, welche Maßnahmen die "KreativKopf GmbH" ergreifen muss, um ihr neues Kundenportal (eine Webanwendung) gegen die von euch recherchierten OWASP Top 10 Risiken abzusichern.
  
  <div class="joplin-table-wrapper"><table style="min-width: 461px"><tbody><tr><th colspan="1" rowspan="1" colwidth="436"><p data-id="ukxlawzjthvi">Risiko &amp; Beschreibung aus Aufg. 1</p></th><th colspan="1" rowspan="1"><p data-id="xgpeoucsdlrm">Präventivmaßnahmen für KreativKopf</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="xbtxfrgboxcs"><strong>A01:2021 — Broken Access Control:</strong> Wenn ein Nutzer auf Inhalte und Funktionen zugreifen kann, zu denen er eigentlich keine Berechtigung hat.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="pruaofqgqmwq">Zugangskontrollen einrichten</p></li><li><p data-id="htwkbeymglxq">Eben diese auch überprüfen (Backlog)</p></li><li><p data-id="cuimddyvizsv">Zugriffsintervalle und -anfragen limitieren</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="igitoqfckali"><strong>A04:2021 — Insecure Design:</strong> “Unsicheres Design” beschreibt, dass bereits in der Konzeptionierung Sicherheitsmängel entstanden sind. Die Implementierung ist hier NICHT enthalten.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="bdgeiudfwmfm">Bei und besonders VOR der Einrichtung des Portals explizit auf alle Sicherheitsstandards und Risiken achten</p></li><li><p data-id="ovqfkpgpbddn">Moderne Infrastruktur und Systeme nutzen</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="436"><p data-id="ozcaxvkdsuir"><strong>A03:2021 — Injection:</strong> Das Einschleusen von Befehlen, Skripts, o.ä.. Laut OWASP gibt typischerweise folgende Arten der Injection: SQL, NoSQL, OS command, Object Relational Mapping (ORM), LDAP, und Expression Language (EL) oder Object Graph Navigation Library (OGNL) injection.</p></td><td colspan="1" rowspan="1"><ul><li><p data-id="uiiasnvejwvb">Daten von Befehlen und Anfragen trennen</p></li><li><p data-id="tfkaabovgiai">Platzhalter für sensible Daten einbauen</p></li></ul></td></tr></tbody></table></div>
  

# Quellen und Vertiefung

- **Online-Ressource:** [OWASP Top 10 - 2021 (Offizielle Seite)](https://owasp.org/Top10/)
- **Online-Ressource:** [Heise.de - Serie zur OWASP Top 10](https://www.google.com/search?q=https://www.heise.de/thema/OWASP-Top-10)