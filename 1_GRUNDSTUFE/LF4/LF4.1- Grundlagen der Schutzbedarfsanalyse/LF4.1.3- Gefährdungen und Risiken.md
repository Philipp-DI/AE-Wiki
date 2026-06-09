# LF4.1.3- Gefährdungen und Risiken

Als Mitarbeiter im IT-Helpdesk

möchte ich typische Gefährdungen wie Phishing und Malware sicher erkennen,

damit ich auf Anfragen von Usern korrekt reagieren und erste Schutzmaßnahmen einleiten kann.

# Celebration Criteria

- Wir können die Begriffe "Gefährdung", "Schwachstelle" und "Risiko" voneinander abgrenzen.  
  **Kurz erklärt:**
  
  - **Gefährdung** = was potenziell schaden kann
  - **Schwachstelle** = wo das System anfällig ist
  - **Risiko** = die Kombination aus Gefahr + Anfälligkeit + Schadenspotenzial
  
  | Begriff | Bedeutung | Beispiel |
  | --- | --- | --- |
  | **Gefährdung (Threat)** | Potenzielle Bedrohung oder Ereignis, das Schaden verursachen könnte | Ein Hackerangriff, Feuer im Serverraum, Stromausfall |
  | **Schwachstelle (Vulnerability)** | Eine Lücke oder Schwäche in Systemen, Prozessen oder Anwendungen, die eine Gefährdung ausnutzen kann | Nicht gepatchte Software, unsichere Passwörter, unverschlüsselte Daten |
  | **Risiko (Risk)** | Wahrscheinlichkeit, dass eine Gefährdung eine Schwachstelle ausnutzt, multipliziert mit dem möglichen Schaden | Risiko eines Datenverlusts durch Hackerangriff auf ungesicherte Datenbanken |
  
- Wir können mindestens drei verschiedene Arten von Malware (z.B. Viren, Trojaner, Ransomware) und ihre Funktionsweise erklären.  
  <br/>**Kurz erklärt:**
  
  - **Viren** brauchen Dateien oder Programme, um sich zu verbreiten.
  - **Trojaner** tarnen sich und ermöglichen Angreifern Zugriff.
  - **Ransomware** erpresst Geld durch Verschlüsselung von Daten.
  - **Würmer** verbreiten sich automatisch über Netzwerke.
  - **Spyware** spioniert aus, **Adware** nervt mit Werbung.  
    <br/>**Fazit:**  
    Malware kann **die Vertraulichkeit, Integrität und Verfügbarkeit** von IT-Systemen bedrohen. Jede Art hat **einen spezifischen Angriffszweck**, weshalb Prävention und Sicherheitsmaßnahmen angepasst werden müssen.
  
  | Malware-Art | Funktionsweise / Wirkung | Beispiel / Hinweis |
  | --- | --- | --- |
  | **Virus** | Selbstverbreitend, hängt sich an Dateien oder Programme; kann Dateien löschen, Systeme verlangsamen oder beschädigen | Macro-Viren in Office-Dokumenten |
  | **Trojaner** | Tarnen sich als harmlose Programme, öffnen jedoch Hintertüren für Angreifer; selbst verbreiten sie sich meist nicht | Remote-Access-Trojaner (RAT) ermöglicht Kontrolle über PC |
  | **Ransomware** | Verschlüsselt Dateien oder ganze Systeme und verlangt Lösegeld (meist in Kryptowährung) | WannaCry, Locky |
  | **Wurm** | Selbstverbreitend über Netzwerke, kann ganze Systeme infizieren | Conficker, Stuxnet |
  | **Spyware / Keylogger** | Zeichnet Benutzeraktivitäten auf, stiehlt Passwörter oder andere vertrauliche Daten | Software zur Passwortausspähung |
  | **Adware** | Zeigt unerwünschte Werbung an, oft mit Tracking des Nutzerverhaltens | Pop-up-Werbung, Browser-Toolbars |
  
- Wir können das Prinzip von "Social Engineering" und "Phishing" erklären und typische Merkmale einer Phishing-Mail benennen.  
  **Social Engineering**
  
  - **Definition:** Methoden, bei denen Angreifer **Menschen manipulieren**, um **geheime Informationen** (Passwörter, Zugangsdaten) oder **direkten Zugriff** auf Systeme zu erhalten.
  - **Prinzip:** Psychologische Tricks, Vertrauen ausnutzen, z. B. durch Dringlichkeit, Autorität oder Neugier.
  - **Beispiel:** Jemand gibt sich am Telefon als IT-Mitarbeiter aus und fordert dein Passwort.
  
  ---
  
  ### **Phishing**
  
  - **Definition:** Eine **Form von Social Engineering**, meist per **E-Mail oder Messenger**, um vertrauliche Daten zu stehlen.
  - **Ziel:** Zugang zu Konten, Bankdaten, Firmennetzwerken oder persönliche Daten erlangen.
  - **Beispiel:** Eine E-Mail von „Bank XY“ fordert, ein Login über einen Link zu bestätigen.
  
  ---
  
  ### **Typische Merkmale einer Phishing-Mail**
  
  1. **Dringlichkeit / Bedrohung:** „Ihr Konto wird gesperrt, wenn Sie nicht sofort handeln!“
  2. **Unbekannter Absender oder gefälschte E-Mail-Adresse**
  3. **Rechtschreib- und Grammatikfehler**
  4. **Verdächtige Links oder Anhänge** (URLs führen auf gefälschte Webseiten)
  5. **Ungewöhnliche Anrede oder generische Begrüßung:** „Sehr geehrter Kunde“
  6. **Anfragen nach sensiblen Daten:** Passwörter, Kreditkarten, TANs
  
  **Kurz gesagt:**  
  Social Engineering **nutzt menschliches Vertrauen**, Phishing ist eine häufige Methode, um über **E-Mail oder Messenger** an Daten zu gelangen.
- Wir können den Unterschied zwischen technischen und organisatorischen Schwachstellen erläutern.  
  <br/>**Kurz erklärt:**
  
  - **Technische Schwachstellen** betreffen die Systeme selbst.
  - **Organisatorische Schwachstellen** betreffen **Mensch, Prozesse und Regeln**.
  - Beide zusammen erhöhen das **Sicherheitsrisiko** für das Unternehmen.
  
  | Merkmal | Technische Schwachstelle | Organisatorische Schwachstelle |
  | --- | --- | --- |
  | **Definition** | Schwächen oder Fehler in **Hardware, Software oder IT-Systemen**, die von Angreifern ausgenutzt werden können | Schwächen in **Prozessen, Richtlinien, Abläufen oder menschlichem Verhalten**, die Sicherheitsrisiken erhöhen |
  | **Beispiele** | \- Nicht gepatchte Software- Unsichere Netzwerkkonfiguration- Fehlende Firewall oder Antivirensoftware | \- Fehlende Sicherheitsrichtlinien- Unzureichende Schulung der Mitarbeiter- Keine Zugriffsberechtigungen oder Kontrollen |
  | **Ursache** | Technische Mängel, Programmierfehler, veraltete Systeme | Menschliches Fehlverhalten, unklare Prozesse, organisatorische Lücken |
  | **Maßnahmen zur Behebung** | Updates, Patches, Firewalls, Sicherheitssoftware | Richtlinien einführen, Schulungen, Rollen- und Rechtekonzept, Notfallpläne |
  

# Wissens-Briefing

Um den Schutzbedarf zu ermitteln, muss man wissen, wovor man sich schützen will.

- **Gefährdung:** Ein Ereignis oder eine Handlung, die potenziell einen Schaden verursachen kann. Gefährdungen können höhere Gewalt (Brand, Hochwasser), technisches Versagen (Festplattencrash) oder vorsätzliche Handlungen (Hackerangriff) sein. Das BSI listet 47 elementare Gefährdungen auf.
- **Schwachstelle:** Eine Eigenschaft eines Systems, die von einer Gefährdung ausgenutzt werden kann.
  - **Technische Schwachstelle:** Ein fehlendes Sicherheitsupdate in einem Betriebssystem.
  - **Organisatorische Schwachstelle:** Ein fehlendes Passwort-Reglement im Unternehmen.
- **Risiko:** Die Wahrscheinlichkeit, dass eine Gefährdung eine Schwachstelle ausnutzt, und die Höhe des daraus resultierenden Schadens. **Risiko = Eintrittswahrscheinlichkeit x Schadenshöhe**.

## Typische Gefährdungen durch vorsätzliche Handlungen

- **Malware (Schadsoftware):**
  - **Viren:** Programme, die sich in andere Dateien einnisten und sich so verbreiten.
  - **Würmer:** Verbreiten sich selbstständig über Netzwerke.
  - **Trojaner:** Tarnen sich als nützliche Programme, führen aber im Hintergrund schädliche Funktionen aus (z.B. Ausspähen von Passwörtern).
  - **Ransomware (Erpressungstrojaner):** Verschlüsselt die Daten auf einem Computer und fordert Lösegeld für die Entschlüsselung. Dies ist eine der größten aktuellen Bedrohungen.
- **Social Engineering:** Die Manipulation von Personen, um an vertrauliche Informationen zu gelangen. Der Angreifer nutzt menschliche Eigenschaften wie Hilfsbereitschaft, Neugier oder Angst aus.
  - **Phishing:** Eine Form des Social Engineering, bei der gefälschte E-Mails, SMS oder Webseiten genutzt werden, um an Zugangsdaten, Kreditkarteninformationen oder andere sensible Daten zu gelangen. Phishing-Mails enthalten oft dringende Handlungsaufforderungen, Drohungen und Links zu gefälschten Webseiten.

# Aufgaben

1. **Risikomatrix erstellen:** Zeichnet eine einfache Risikomatrix mit den Achsen "Eintrittswahrscheinlichkeit" und "Schadenshöhe". Ordnet die folgenden Ereignisse für die "KreativKopf GmbH" ein:
  1. Totalausfall des Internets für 24h
  2. Ransomware-Angriff
  3. Defekt der Kaffeemaschine.
    
    | Ereignis | Eintrittswahrscheinlichkeit | Schadenshöhe | Einordnung |
    | --- | --- | --- | --- |
    | **Totalausfall des Internets (24h)** | mittel | hoch | mittleres bis hohes Risiko |
    | **Ransomware-Angriff** | mittel | sehr hoch | hohes Risiko |
    | **Defekt der Kaffeemaschine** | hoch | gering | niedriges Risiko |
    
2. **Phishing-Mail analysieren:** Sucht online nach einem aktuellen Beispiel für eine Phishing-Mail. Analysiert sie und erstellt eine Checkliste "So erkenne ich eine Phishing-Mail".Betreff etwa: „Ihr Konto wurde wegen unautorisierter Aktivität gesperrt – bitte sofort bestätigen“  
  <br/>**Absender:** support@secure‑[mail.de](http://mail.de)  
  **Empfänger:** [max.mustermann@kreativkopf.de](mailto:max.mustermann@kreativkopf.de)  
  **Betreff:** Dringende Bestätigung Ihres Kontozugangs erforderlich**Text:**  
  Sehr geehrte/r Max Mustermann,aus Sicherheitsgründen wurde ein unautorisierter Anmeldeversuch auf Ihrem Projektmanagement‑Account festgestellt. Wir benötigen Ihre Hilfe, um Ihr Konto zu verifizieren und eine Sperrung zu verhindern.Bitte bestätigen Sie Ihre Zugangsdaten jetzt innerhalb von 24 Stunden, sonst wird Ihr Konto automatisch deaktiviert:  
  → **Klicken Sie hier:** [http://secure‑verify.example‑login.com](http://secure%E2%80%91verify.example%E2%80%91login.com) (ACHTUNG: nicht echt)Zur Bestätigung benötigen wir: Benutzername, Passwort und evtl. Ihre Sicherheitsfrage.Mit freundlichen Grüßen,  
  Ihr IT‑Support  
  KreativKopf GmbH
  
  #### Checkliste “So erkenne ich eine Phishing-Mail”:
  
  - [ ] Handelt es sich beim Absender der Mail um eine offizielle Adresse?
  - [ ] Grammatik & Rechtschreibung auffällig?
  - [ ] Dringlichkeit hoch? Handlungsaufruf?
  - [ ] Verdächtige Links? Bspw. zu gefälschten Webseiten
  - [ ] Im Junk-Postfach/Spam-Ordner gelandet?
  - [ ] In der Regel sehr allgemeine Anrede?
  - [ ] Handelt es sich um sensible Daten, die gefordert werden?
  - [ ] verdächtige Datei-Anhänge? → unbedingt ignorieren!
3. **Malware-Steckbriefe:** Erstellt kurze Steckbriefe für Virus, Wurm, Trojaner und Ransomware.
  
  | **Typ** | **Kurzbeschreibung** | **Beispiel / Wirkung** |
  | --- | --- | --- |
  | **Virus** | Programm, das sich an andere Dateien anhängt und sich verbreitet | Zerstört Dateien, verbreitet sich über USB-Sticks |
  | **Wurm** | Selbstständig verbreitende Malware über Netzwerk | Schnelle Ausbreitung, z. B. WannaCry |
  | **Trojaner** | Täuscht nützliche Software vor, enthält aber Schadcode | Keylogger, Remote-Access-Trojaner |
  | **Ransomware** | Verschlüsselt Daten und fordert Lösegeld | CryptoLocker, Daten sind ohne Schlüssel unzugänglich |
  
4. **Rollenspiel "Social Engineering":** Führt ein kurzes Rollenspiel durch, in dem ein Angreifer versucht, am Telefon ein Passwort zu erfragen.  
  **_Story:_** “Guten Tag, hier ist Herr Mustermann aus der IT-Abteilung. Wir führen gerade ein Sicherheitsupdate durch. Können Sie mir bitte kurz Ihr Passwort nennen, damit ich Sie aus dem System ausloggen kann?”  
  <br/>**_Was nun? Was tun?_**
  - _Keiner darf ohne weiteres Passwörter weitergeben!_
  - Mitarbeiter sollen möglichst schnell und höflich ablehnen und die IT-Abteilung kontaktieren.
  - _PS: Das Vertrauen eines Menschen ist meist eine große Sicherheitslücke._
5. **STRIDE-Klassifizierung:** Ordnet die folgenden Angriffe den STRIDE-Kategorien zu (Mehrfachnennungen sind möglich):
  1. Der Phishing-Angriff auf die "KreativKopf GmbH". → _Spoofing, Ziel - Vertraulichkeitsverletzung_
  2. Ein Ransomware-Angriff, der alle Daten verschlüsselt. → _Manipulation > Dienstunterbrechung_
  3. Ein Angreifer knackt einen User-Account und nutzt eine Systemschwachstelle, um Admin zu werden. → _Spoofing > Manipulation > Erhöhung von Rechten_  
    <br/>**S** = Spoofing (Identitätsfälschung)  
    **T** = Tampering (Manipulation von Daten/Programmen)**R** = Repudiation (Abstreiten von Handlungen / Nicht-Zuordenbarkeit)**I** = Information Disclosure (Vertraulichkeitsverletzung)**D** = Denial of Service (Dienstunterbrechung)**E** = Elevation of Privilege (Erhöhung von Rechten)

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.4 "Gefahren und Risiken" (S. 979-994)
- **Online-Ressource:** [Microsoft - STRIDE Threat Model](https://learn.microsoft.com/de-de/azure/security/develop/threat-modeling-tool-threats)
- **Online-Ressource:** [Verbraucherzentrale - Aktuelle Phishing-Warnungen](https://www.google.com/search?q=https://www.verbraucherzentrale.de/wissen/digitale-welt/phishingradar/phishingradar-aktuelle-warnungen-6072)  
  <br/><br/>