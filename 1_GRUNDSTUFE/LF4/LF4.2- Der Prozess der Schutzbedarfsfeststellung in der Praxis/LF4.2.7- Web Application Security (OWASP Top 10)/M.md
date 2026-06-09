# Mohammed

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

### **Beispiel:**

| Risiko | Beschreibung | Beispiel |
| --- | --- | --- |
| **A01 – Injection** | Angreifer kann unkontrollierte Daten an SQL, OS oder LDAP senden | Eingabe in ein Loginfeld: `' OR '1'='1` um sich ohne Passwort einzuloggen |
| **A03 – Sensitive Data Exposure** | Unverschlüsselte oder unsichere Speicherung sensibler Daten | Kreditkartennummer wird als Klartext in der Datenbank gespeichert |
| **A05 – Security Misconfiguration** | Fehlkonfigurierte Server oder Anwendungen können ausgenutzt werden | Standardpasswörter auf Admin-Konten werden nicht geändert |

2. **SQL-Injection verstehen:** Analysiert den folgenden (unsicheren) PHP-Code-Schnipsel: `$sql = "SELECT * FROM users WHERE username = '" . $_POST['username'] . "';";`. Diskutiert, was ein Angreifer in das `username`\-Feld eingeben könnte, um die Abfrage zu manipulieren (z.B. um sich ohne Passwort einzuloggen)

' OR '1'='1 → **_Dadurch wird die Bedingung immer wahr und der Angreifer kann sich ohne Passwort einloggen._**

3. **Gegenmaßnahmen finden:** Brainstormt, welche Maßnahmen die "KreativKopf GmbH" ergreifen muss, um ihr neues Kundenportal (eine Webanwendung) gegen die von euch recherchierten OWASP Top 10 Risiken abzusichern.

### **Beispiele für Maßnahmen:**

- **Input-Validierung & Prepared Statements** → verhindert SQL-Injection.
- **Sichere Authentifizierung** → z. B. Passwortregeln, Zwei-Faktor-Authentifizierung (MFA).
- **HTTPS & Verschlüsselung sensibler Daten** → schützt sensible Datenübertragung und Speicherung.
- **Regelmäßige Updates & Patches** → verhindert Exploits durch bekannte Sicherheitslücken.
- **Rollen- und Zugriffskontrolle** → nur berechtigte Nutzer dürfen bestimmte Daten oder Funktionen nutzen.

# Quellen und Vertiefung

- **Online-Ressource:** [OWASP Top 10 - 2021 (Offizielle Seite)](https://owasp.org/Top10/)
- **Online-Ressource:** [Heise.de - Serie zur OWASP Top 10](https://www.google.com/search?q=https://www.heise.de/thema/OWASP-Top-10)