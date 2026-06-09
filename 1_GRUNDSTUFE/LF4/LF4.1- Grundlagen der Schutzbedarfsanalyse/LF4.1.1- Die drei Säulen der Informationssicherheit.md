# LF4.1.1- Die drei Säulen der Informationssicherheit

Als IT-Support-Mitarbeiter im 1st-Level-Support

möchte ich die Schutzziele der Informationssicherheit kennenlernen,

damit ich Anwendern die Bedeutung von Sicherheitsregeln (z.B. Passwort-Policy) praxisnah erklären kann.

# Celebration Criteria

- Wir können die Schutzziele Vertraulichkeit, Integrität und Verfügbarkeit definieren.  
  Die **Schutzziele** der IT-Sicherheit sind **Vertraulichkeit**, **Integrität** und **Verfügbarkeit**.  
  Sie werden oft als das **CIA-Triad** bezeichnet (engl. _Confidentiality, Integrity, Availability_).
  
  1. **Vertraulichkeit (Confidentiality):**  
    Nur **autorisierte Personen** dürfen auf Daten zugreifen.  
    → Beispiel: Passwörter, Verschlüsselung und Zugriffsrechte schützen sensible Daten vor Unbefugten.
  2. **Integrität (Integrity):**  
    Daten dürfen **nicht unbemerkt verändert** werden – sie müssen **echt und unverfälscht** bleiben.  
    → Beispiel: Prüfsummen (Hashes), digitale Signaturen oder Versionskontrolle (z. B. Git) stellen sicher, dass Daten nicht manipuliert wurden.
  3. **Verfügbarkeit (Availability):**  
    Systeme und Daten müssen **immer erreichbar** sein, wenn sie gebraucht werden.  
    → Beispiel: Backups, redundante Server, stabile Netzwerke und DDoS-Schutz sichern die ständige Erreichbarkeit.
  
  Diese drei Ziele stehen manchmal im **Spannungsverhältnis**:  
  Wenn man zum Beispiel die Vertraulichkeit durch starke Verschlüsselung erhöht, kann die Verfügbarkeit oder Geschwindigkeit leiden.  
  <br/>
- Wir können zu jedem Schutzziel mindestens zwei Beispiele aus dem Unternehmensalltag nennen.
- Wir können erläutern, wie die Verletzung eines Schutzziels die anderen Schutzziele beeinträchtigen kann (z.B. Verletzung der Integrität von Zugangsdaten gefährdet die Vertraulichkeit).  
  <br/>Wenn **Zugangsdaten manipuliert** oder verändert werden,  
  kann jemand **unbefugt auf vertrauliche Daten zugreifen**.  
  Das heißt: **Integritätsverlust** führt auch zu **Verlust der Vertraulichkeit**.**Beispiel:** Ein Angreifer ändert Passwörter in der Datenbank → andere Mitarbeiter können sich nicht mehr anmelden, und er erhält Zugriff auf geheime Informationen.
- Wir können in einem gegebenen Szenario erkennen, welche Schutzziele verletzt wurden.  
  Analyse der Schutzziele:
  
  1. **Vertraulichkeit (Confidentiality) – verletzt**  
    → Unbefugte Personen könnten durch die gestohlenen Zugangsdaten **Einblick in vertrauliche Kunden- oder Projektdaten** erhalten.  
    **Beispiel:** Kundennamen, Aufträge oder interne Dokumente könnten eingesehen werden.
  2. **Integrität (Integrity) – potenziell verletzt**  
    → Wenn die Angreifer Zugang zum Tool hatten, könnten sie **Daten verändern oder löschen**.  
    **Beispiel:** Projektdaten könnten manipuliert oder Aufgaben unbemerkt geändert worden sein.
  3. **Verfügbarkeit (Availability) – nicht direkt betroffen**, aber gefährdet  
    → Falls das Konto gesperrt oder Systeme zur Schadensbegrenzung vorübergehend deaktiviert werden,  
    könnte die **Nutzung der Cloud-Dienste eingeschränkt** sein.
  
  ### **Fazit:**
  
  In diesem Szenario wurde vor allem die **Vertraulichkeit** verletzt,  
  möglicherweise auch die **Integrität**,  
  und indirekt ist die **Verfügbarkeit** gefährdet.Das zeigt: Ohne IT-Sicherheitskonzept (z. B. Schulungen, Passwortmanagement, 2FA) ist das Unternehmen anfällig für menschliche Fehler und Angriffe.
  
  ---
  
  ### Szenario:
  
  Bei der **KreativKopf GmbH** hat ein Mitarbeiter auf eine **Phishing-Mail** reagiert und seine **Zugangsdaten** zu einem **SaaS-Projektmanagement-Tool** weitergegeben.  
  Dadurch konnten Unbefugte möglicherweise auf Kundendaten zugreifen.
  
  ---
  
  ### Analyse der Schutzziele:
  
  1. **Vertraulichkeit (Confidentiality) – verletzt**  
    → Unbefugte Personen könnten durch die gestohlenen Zugangsdaten **Einblick in vertrauliche Kunden- oder Projektdaten** erhalten.  
    **Beispiel:** Kundennamen, Aufträge oder interne Dokumente könnten eingesehen werden.
  2. **Integrität (Integrity) – potenziell verletzt**  
    → Wenn die Angreifer Zugang zum Tool hatten, könnten sie **Daten verändern oder löschen**.  
    **Beispiel:** Projektdaten könnten manipuliert oder Aufgaben unbemerkt geändert worden sein.
  3. **Verfügbarkeit (Availability) – nicht direkt betroffen**, aber gefährdet  
    → Falls das Konto gesperrt oder Systeme zur Schadensbegrenzung vorübergehend deaktiviert werden,  
    könnte die **Nutzung der Cloud-Dienste eingeschränkt** sein.
  
  ---
  
  ### **Fazit:**
  
  In diesem Szenario wurde vor allem die **Vertraulichkeit** verletzt,  
  möglicherweise auch die **Integrität**,  
  und indirekt ist die **Verfügbarkeit** gefährdet.Das zeigt: Ohne IT-Sicherheitskonzept (z. B. Schulungen, Passwortmanagement, 2FA) ist das Unternehmen anfällig für menschliche Fehler und Angriffe.

# Wissens-Briefing

Die Informationssicherheit stützt sich auf drei fundamentale Grundwerte oder Schutzziele. Jede Sicherheitsmaßnahme zielt darauf ab, eines oder mehrere dieser Ziele zu gewährleisten.

## Vertraulichkeit (Confidentiality)

Stellt sicher, dass Daten und Informationen nur von autorisierten Personen eingesehen oder offengelegt werden dürfen. Es geht um den Schutz vor unbefugtem Informationsgewinn.

- **Beispiel:** Eine Personalakte darf nur von Mitarbeitern der Personalabteilung und der Geschäftsführung eingesehen werden, nicht aber von Kollegen aus der Entwicklung.
- **Verletzung:** Ein Hacker verschafft sich Zugriff auf eine Kundendatenbank und veröffentlicht die Daten im Darknet.

## Integrität (Integrity)

Bezeichnet die Korrektheit und Unverfälschtheit von Daten und Systemen. Es muss sichergestellt sein, dass Informationen nicht unbemerkt und unautorisiert verändert werden können.

- **Beispiel:** Der Betrag auf einer Online-Rechnung muss exakt dem Betrag entsprechen, der vom System ursprünglich generiert wurde.
- **Verletzung:** Ein Virus manipuliert die Kontodaten in einer Überweisungsvorlage, sodass Geld auf ein falsches Konto transferiert wird.

## Verfügbarkeit (Availability)

Gewährleistet, dass IT-Systeme, Dienste und die darin gespeicherten Informationen den autorisierten Benutzern zur Verfügung stehen, wenn sie benötigt werden.

- **Beispiel:** Der Online-Shop eines Unternehmens muss für Kunden rund um die Uhr erreichbar sein.
- **Verletzung:** Ein DDoS-Angriff (Distributed Denial of Service) überlastet einen Webserver, sodass die Unternehmenswebsite nicht mehr erreichbar ist.

Diese drei Ziele stehen oft in einer Wechselbeziehung. Sehr hohe Vertraulichkeit (z.B. durch komplexe Verschlüsselung und mehrstufige Logins) kann die Verfügbarkeit (schneller Zugriff) leicht einschränken.

# Aufgaben

1. **Diskussion im Team:** Brainstormt in eurer Gruppe (z.B. auf einem Online-Whiteboard), welche alltäglichen digitalen Aktivitäten ihr durchführt (Online-Banking, Social Media, E-Mail). Ordnet jeder Aktivität zu, welches der drei Schutzziele (V, I, V) für euch persönlich am wichtigsten ist und begründet eure Entscheidung. → **ALLE!**
2. **Szenario-Analyse:** Analysiert das Szenario der "KreativKopf GmbH" aus dem Lern-Epic. Welche Schutzziele wurden durch den Phishing-Vorfall konkret verletzt oder sind akut gefährdet? Haltet eure Ergebnisse in einem geteilten Dokument fest.  
  → **_Vertraulichkeit_** _wurde verletzt,_ **_Integrität und Verfügbarkeit_** _unterstehen einem implizitem Risiko._
3. **Gegenmaßnahmen zuordnen:** Recherchiert die folgenden drei Sicherheitsmaßnahmen:
  
  1. Festplattenverschlüsselung (z.B. BitLocker für Windows oder LUKS für Ubuntu),
  2. Tägliches Backup auf ein externes System,
  3. Zwei-Faktor-Authentisierung (2FA).
    
    | Maßnahme | Primäres Schutzziel | Funktionsweise / Erklärung |
    | --- | --- | --- |
    
    |     |     |     |
    | --- | --- | --- |
    | **Festplattenverschlüsselung** (z. B. BitLocker, LUKS) | **Vertraulichkeit** | Daten werden auf dem Speichermedium verschlüsselt. Ohne Schlüssel kann niemand die Dateien lesen – auch nicht bei Geräteverlust. Daten zum Booten dürfen nicht verschlüsselt sein, es sei denn man verwendet einen Boot-Manager |
    
    |     |     |     |
    | --- | --- | --- |
    | **Tägliches Backup** auf ein externes System | **Verfügbarkeit & ggf. Integrität** | Bei Datenverlust (z. B. durch Ransomware oder Hardwaredefekt) können Daten aus der Sicherung wiederhergestellt werden. |
    
    |     |     |     |
    | --- | --- | --- |
    | **Zwei-Faktor-Authentisierung (2FA)** | **Integrität & Vertraulichkeit** | Neben Passwort ist ein zweiter Faktor (z. B. Code auf Smartphone) nötig. Dadurch sind Konten besser geschützt – selbst wenn Passwörter bekannt werden. |
    
  
  Ordnet jede Maßnahme dem primären Schutzziel zu, das sie stärkt, und erklärt kurz die Funktionsweise.
4. **Präsentation:** Erstellt eine kurze Präsentation (3-5 Folien oder ein kurzes Erklärvideo) für einen "Tag der IT-Sicherheit" in einem fiktiven Unternehmen. Erklärt darin die drei Schutzziele mit einfachen Worten und plakativen Beispielen für Nicht-IT-Mitarbeiter.

[Die_drei_Schutzziele_der_IT-Sicherheit_–\_einfach_erklärt_1.odp](files/019cee42-e3b3-723a-ae41-ea96880682e1/Die_drei_Schutzziele_der_IT-Sicherheit_–_einfach_erklärt_1.odp)

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22 "IT-Sicherheit", Abschnitt 22.1 "Was ist IT-Sicherheit?" (S. 969-972)
- **Online-Ressource:** [BSI für Bürger - Informationssicherheit](https://www.google.com/search?q=https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Informationen-und-Empfehlungen/Themenuebersicht/Informationssicherheit/informationssicherheit_node.html)