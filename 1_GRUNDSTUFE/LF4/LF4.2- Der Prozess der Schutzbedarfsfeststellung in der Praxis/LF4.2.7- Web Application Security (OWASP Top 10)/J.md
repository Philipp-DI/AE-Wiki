# Janine

Als angehender Webentwickler möchte ich die häufigsten Schwachstellen in Webanwendungen kennen, damit ich von Anfang an sichere Webanwendungen entwickeln und bestehende Anwendungen auf grundlegende Risiken prüfen kann.

# Celebration Criteria

- Wir können den Zweck der OWASP Top 10 erklären.
- Wir können mindestens drei der häufigsten Schwachstellen (z.B. Injection, Broken Authentication, Cross-Site Scripting) mit einfachen Worten beschreiben.
- Wir können das Prinzip einer SQL-Injection an einem Code-Beispiel erläutern.
- Wir können grundlegende Gegenmaßnahmen wie die Validierung von Benutzereingaben als zentrales Sicherheitsprinzip begründen.

# Wissens-Briefing

Webanwendungen sind oft das "Tor zum Unternehmen" und daher ein Hauptziel für Angreifer. Die **OWASP (Open Web Application Security Project)** ist eine Non-Profit-Organisation, die das Bewusstsein für die Sicherheit von Software verbessern will. Ihr bekanntestes Projekt ist die **OWASP Top 10**, eine Liste der kritischsten Sicherheitsrisiken für Webanwendungen.

**Einige Beispiele aus der OWASP Top 10:**

- **A01: Broken Access Control (fehlerhafte Zugriffskontrolle):** Benutzer können auf Daten oder Funktionen zugreifen, für die sie keine Berechtigung haben (z.B. ein normaler User kann Admin-Funktionen aufrufen, indem er die URL manipuliert)
- **A03: Injection (Einschleusung):** Ein Angreifer sendet bösartige Daten an eine Anwendung, die diese ungeprüft weiterverarbeitet. Der bekannteste Typ ist die **SQL-Injection**. Hier werden SQL-Befehle über ein Eingabefeld (z.B. die Suche) in die Datenbank der Anwendung "injiziert", um Daten auszulesen oder zu manipulieren
- **A07: Identification and Authentication Failures (Fehler bei der Identifizierung und Authentifizierung):** Schwachstellen im Login-Prozess, z.B. schwache Passwörter, fehlende Multi-Faktor-Authentifizierung oder unsichere Passwort-Wiederherstellungsfunktionen

Ein Kernprinzip zur Vermeidung vieler dieser Schwachstellen lautet: **"Never trust user input!" (Vertraue niemals Benutzereingaben!)**. Alle Daten, die von außen kommen, müssen validiert und bereinigt werden, bevor sie verarbeitet werden.

# Aufgaben

1. **Recherche:** Wählt in eurer Gruppe drei Risiken aus der aktuellen OWASP Top 10 aus. Erstellt für jedes Risiko einen kurzen Steckbrief, der die Schwachstelle und ein einfaches Beispiel beschreibt.
  
  | Risiko | Beschreibung | Beispiel |
  | --- | --- | --- |
  
  |     |     |     |
  | --- | --- | --- |
  | **A01 – Broken Access Control** | Benutzer können auf Ressourcen oder Funktionen zugreifen, für die sie keine Berechtigung haben | Ein normaler User kann durch Manipulation der URL `https://firma.de/admin` auf Admin-Funktionen zugreifen |
  
  |     |     |     |
  | --- | --- | --- |
  | **A03 – Injection (z. B. SQL-Injection)** | Bösartige Eingaben werden ungeprüft an die Datenbank oder andere Systeme weitergegeben | Ein Angreifer gibt in ein Login-Feld ein: `' OR '1'='1` → kann sich ohne korrektes Passwort einloggen |
  
  |     |     |     |
  | --- | --- | --- |
  | **A07 – Identification and Authentication Failures** | Schwächen im Authentifizierungsprozess, z. B. einfache Passwörter, fehlende Multi-Faktor-Authentifizierung oder unsichere Passwort-Wiederherstellung | Ein Benutzer kann das Passwort eines anderen zurücksetzen, indem er die Passwort-Reset-URL manipuliert oder einfache Sicherheitsfragen errät |
  
2. **SQL-Injection verstehen:** Analysiert den folgenden (unsicheren) PHP-Code-Schnipsel: `$sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";`. Diskutiert, was ein Angreifer in das `username`\-Feld eingeben könnte, um die Abfrage zu manipulieren (z.B. um sich ohne Passwort einzuloggen).
  
  | Feld | Inhalt |
  | --- | --- |
  
  |     |     |
  | --- | --- |
  | **Unsicherer Code** | `php\n$sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";\n` |
  
  |     |     |
  | --- | --- |
  | **Problem** | Die Eingabe `$_POST['username']` wird **direkt** in die SQL-Abfrage eingefügt — ohne Validierung, Escaping oder Parameterisierung |
  
  |     |     |
  | --- | --- |
  | **Beispiel Eingabe (Angreifer)** | `' OR '1'='1` |
  
  |     |     |
  | --- | --- |
  | **Resultierende Abfrage** | `SELECT * FROM users WHERE username = '' OR '1'='1';` |
  
  |     |     |
  | --- | --- |
  | **Folge / Impact** | `1=1` ist immer wahr → die Abfrage liefert (je nach Implementierung) alle Benutzerzeilen; Angreifer kann sich ggf. ohne Passwort einloggen oder Daten auslesen |
  
  |     |     |
  | --- | --- |
  | **Weitere Angriffsvarianten (Beispiele)** | `'; DROP TABLE users; --` (löscht Tabelle), `admin' --` (umgeht Passwortabfrage), zeitbasierte/boolean-basierte Blind‑SQLi für Datenexfiltration |
  
  |     |     |
  | --- | --- |
  | **Kurzempfehlung zur Vermeidung** | Prepared Statements / parameterisierte Queries verwenden; Eingaben validieren und minimal nötige Berechtigungen verwenden; ORM/whitelisting; Prinzip der geringsten Rechte |
  
3. **Gegenmaßnahmen finden:** Brainstormt, welche Maßnahmen die "KreativKopf GmbH" ergreifen muss, um ihr neues Kundenportal (eine Webanwendung) gegen die von euch recherchierten OWASP Top 10 Risiken abzusichern.
  
  | Risiko | Maßnahmen |
  | --- | --- |
  
  |     |     |
  | --- | --- |
  | **Broken Access Control** | \- Rollenbasierte Zugriffskontrolle implementieren - Serverseitige Checks für alle Aktionen - Keine sicherheitsrelevanten Daten nur durch „versteckte“ Links schützen |
  
  |     |     |
  | --- | --- |
  | **Injection (SQL, Command, etc.)** | \- Prepared Statements / Parameterized Queries verwenden - Eingaben validieren und escapen - ORM-Frameworks nutzen, die SQL-Injections verhindern |
  
  |     |     |
  | --- | --- |
  | **Identification & Authentication Failures** | \- Starke Passwortregeln und Multi-Faktor-Authentifizierung einführen - Passwort-Reset-Prozesse absichern (Token, Ablaufzeit) - Session-Management härtet (z. B. Session-Timeout, sichere Cookies) |
  

# Quellen und Vertiefung

- **Online-Ressource:** [OWASP Top 10 - 2021 (Offizielle Seite)](https://owasp.org/Top10/)
- **Online-Ressource:** [Heise.de - Serie zur OWASP Top 10](https://www.google.com/search?q=https://www.heise.de/thema/OWASP-Top-10)