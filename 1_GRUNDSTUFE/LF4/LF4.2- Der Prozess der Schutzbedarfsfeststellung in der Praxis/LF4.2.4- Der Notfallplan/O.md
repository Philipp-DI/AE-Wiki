# 🐝 Olena

Als Mitglied eines Incident-Response-Teams

möchte ich die grundlegenden Schritte im Umgang mit Schutzverletzungen kennen,

damit ich im Ernstfall schnell, strukturiert und korrekt handeln kann, um den Schaden zu minimieren.

# Celebration Criteria

- Wir können die Phasen eines typischen Incident-Response-Prozesses (z.B. Vorbereitung, Identifikation, Eindämmung, Beseitigung, Wiederherstellung, Lessons Learned) benennen.  
  Der Incident-Response-Prozess beschreibt die Schritte, mit denen ein Unternehmen auf IT-Sicherheitsvorfälle reagiert. Typischerweise umfasst er sechs Phasen:
  1. **Vorbereitung:** Erstellung von Plänen, Schulung der Mitarbeitenden, Einrichtung von Monitoring-Systemen.
  2. **Identifikation:** Erkennung und Bestätigung des Sicherheitsvorfalls.
  3. **Eindämmung:** Begrenzung der Ausbreitung (z. B. durch Isolierung des betroffenen Geräts).
  4. **Beseitigung:** Entfernung von Schadsoftware und Behebung der Schwachstellen.
  5. **Wiederherstellung:** Rückkehr zum Normalbetrieb und Wiederherstellung der Daten.
  6. **Lessons Learned:** Analyse des Vorfalls und Verbesserung zukünftiger Sicherheitsmaßnahmen.
- Wir können erklären, warum eine umgehende Meldung eines Sicherheitsvorfalls entscheidend ist.  
  <br/>Eine **sofortige Meldung eines Sicherheitsvorfalls** ist entscheidend, weil:
  
  1. **Schnelle Eindämmung der Bedrohung:**  
    Das IT-Team kann betroffene Geräte sofort isolieren und die Ausbreitung verhindern.
  2. **Minimierung des Schadens:**  
    Je früher reagiert wird, desto geringer sind Datenverlust und Systemausfall.
  3. **Beweissicherung:**  
    Protokolle und Spuren des Angriffs werden rechtzeitig gesichert, wichtig für Analyse und Prävention.
  4. **Einhaltung von Vorschriften:**  
    In vielen Organisationen und gesetzlich (z. B. DSGVO) gibt es Meldepflichten für Sicherheitsvorfälle.
  
  **Fazit:**  
  Eine umgehende Meldung ermöglicht schnelles Handeln, reduziert Schäden und stärkt die IT-Sicherheit insgesamt.  
  <br/>
  
  | Gesetz / Regelung | Wer betroffen ist | Was gemeldet werden muss | An wen melden | Frist / Zeitpunkt |
  | --- | --- | --- | --- | --- |
  | **DSGVO** | Alle Unternehmen, die personenbezogene Daten verarbeiten | Datenschutzverletzungen / Datenpannen | Bundesbeauftragter für Datenschutz; ggf. betroffene Personen | **Innerhalb von 72 Stunden** nach Kenntnis |
  | **IT-Sicherheitsgesetz / BSI-Gesetz** | Kritische Infrastruktur (KRITIS) | IT-Sicherheitsvorfälle, die kritische Prozesse beeinträchtigen | BSI (Bundesamt für Sicherheit in der Informationstechnik) | **Sofort / ohne unnötige Verzögerung** |
  | **Telekommunikationsgesetz (TKG)** | Telekommunikationsanbieter, Internetprovider | Sicherheitsvorfälle in Netzwerken oder Diensten | BSI | **Unverzüglich nach Entdeckung** |
  | **Allgemeine Unternehmenspflicht** | Alle Unternehmen, IT-Dienste | Schwerwiegende IT-Sicherheitsvorfälle | Interne IT-Sicherheitsverantwortliche; ggf. Behörden | Sofort nach Entdeckung |
  
- Wir können mindestens drei Sofortmaßnahmen nennen, die bei einer akuten Ransomware-Infektion an einem Arbeitsplatz ergriffen werden sollten.  
  **Isolierung infizierter Geräte**
  - PCs/Server sofort vom Netzwerk trennen (LAN, WLAN, VPN).
  - Falls nötig, ganze Netzwerksegmente isolieren.
  - Keine USB-Sticks oder externen Laufwerke anschließen.
- **Bewertung des Vorfalls**
  - Prüfen, welche Systeme und Daten betroffen sind.
  - Logdateien und Monitoring-Systeme auswerten.
  - Infektionsweg und Schadensumfang feststellen.
- **Beweissicherung**
  - Forensische Kopien (Disk-Images, Logs) erstellen.  
    (Disk-Images sind im Falle eines Sicherheitsvorfalls wie einer Ransomware-Infektion besonders wichtig, weil sie eine exakte Kopie des gesamten Laufwerks erstellen, einschließlich gelöschter oder versteckter Dateien. Dadurch kann ein IT-Forensiker die Infektion später analysieren, ohne das Originalsystem zu verändern, was auch einen rechtlichen Vorteil hat, da die Originaldaten „forensisch sauber“ bleiben. Außerdem ermöglicht das Disk-Image eine sichere Untersuchung in einer Testumgebung, sodass die Schadsoftware analysiert werden kann, ohne andere Systeme zu gefährden. Sollte während der Wiederherstellung etwas schiefgehen, bleibt das unveränderte Original erhalten, ähnlich wie ein Sicherheits-Backup. Zusätzlich dient das Image der Dokumentation des Vorfalls und zeigt genau, wann und wie er passiert ist, was für interne Audits oder Meldungen an Behörden sehr hilfreich sein kann.)
  - Keine verdächtigen Dateien löschen oder Programme starten.
  - Dokumentation aller Schritte (Zeit, Maßnahmen, beteiligte Personen).
- **Analyse und Behebung der Schwachstellen (Ursachenanalyse)**
  - Ermitteln, **wie** die Schadsoftware eingedrungen ist (z. B. Phishing-Mail, ungepatchte Software, unsichere RDP-Verbindung).
  - Alle Sicherheitslücken schließen (Updates, Patches, Passwortänderungen).
  - Systeme nur nach gründlicher Prüfung wieder ans Netz anschließen.
- **Wiederherstellung aus Backups**
  - Sicherstellen, dass Backups **sauber und nicht infiziert** sind.
  - Daten **auf isolierten, neu aufgesetzten Systemen** wiederherstellen.
  - Funktionsprüfung nach Wiederherstellung durchführen.
- **Kommunikation und Meldung**
  - Management, IT-Sicherheitsbeauftragte und ggf. Datenschutzbeauftragte informieren.
  - Bei personenbezogenen Daten: Meldung an Datenschutzbehörde (gemäß DSGVO Art. 33).
  - Ggf. Unterstützung durch das **BSI** oder externe Forensik-Experten.
- **Sicherheitsrichtlinien aktualisieren („Lessons Learned“)**
  - Erkenntnisse aus dem Vorfall dokumentieren.
  - Sicherheitsrichtlinien und Notfallpläne anpassen.
  - Mitarbeitende gezielt schulen (z. B. Phishing-Simulation, sichere Dateiverwaltung).
- Wir können die Bedeutung der "Lessons Learned"-Phase für die zukünftige Verbesserung der IT-Sicherheit erklären.  
  <br/>**Was ist die „Lessons Learned“-Phase?**  
  Dies ist die Phase nach einem Sicherheitsvorfall, in der die Organisation **analysiert, was passiert ist**, um zu verstehen, was funktioniert hat und was verbessert werden muss.**Warum ist sie wichtig für IT-Sicherheit:**
  
  1. **Ursachenanalyse des Vorfalls**
    - Herausfinden, wie Angreifer eingedrungen sind und welche Schwachstellen genutzt wurden.
  2. **Verbesserung von Prozessen und Technik**
    - Software aktualisieren, Firewalls optimieren, Backups verbessern.
  3. **Steigerung des Sicherheitsbewusstseins der Mitarbeitenden**
    - Mitarbeiterschulungen basierend auf dem Vorfall durchführen, neue Regeln erklären.
  4. **Verhinderung zukünftiger Vorfälle**
    - Organisation wird widerstandsfähiger gegen Angriffe und das Risiko von Wiederholungen sinkt.
  
  **Fazit:**  
  Die „Lessons Learned“-Phase verwandelt **Fehler und Sicherheitsvorfälle in Wissen**, das IT-Systeme und Mitarbeitende stärker und sicherer macht.

# Wissens-Briefing

Trotz bester Vorsorge kann es zu einem Sicherheitsvorfall (Incident) kommen. Dann ist ein schnelles und planvolles Vorgehen entscheidend. Der Prozess der Reaktion wird als **Incident Response** bezeichnet.

## Typische Phasen nach einem Sicherheitsvorfall

1. **Vorbereitung (Preparation):** Diese Phase findet vor dem Vorfall statt. Hier werden Notfallpläne erstellt, Verantwortlichkeiten festgelegt und Mitarbeiter geschult.
2. **Identifikation (Identification):** Ein Vorfall wird erkannt und gemeldet. Es wird analysiert, um was für einen Vorfall es sich handelt (z.B. Malware, unautorisierter Zugriff).
3. **Eindämmung (Containment):** Die Ausbreitung des Schadens wird verhindert. Das betroffene System wird z.B. sofort vom Netzwerk getrennt.
4. **Beseitigung (Eradication):** Die Ursache des Vorfalls wird entfernt, z.B. wird die Schadsoftware vom System gelöscht.
5. **Wiederherstellung (Recovery):** Die betroffenen Systeme werden wieder in den Normalbetrieb überführt, z.B. durch das Einspielen eines sauberen Backups.
6. **Lessons Learned (Post-Incident Activity):** Nach dem Vorfall wird analysiert, was passiert ist, was gut und was schlecht gelaufen ist. Die Erkenntnisse fließen in die Verbesserung der Sicherheitsmaßnahmen und des Notfallplans ein.

Eine schnelle und ehrliche Kommunikation (intern an Mitarbeiter, extern an Kunden oder Behörden wie bei DSGVO-Verstößen) ist in allen Phasen kritisch für den Erfolg.

# Aufgaben

1. **Prozess visualisieren:** Erstellt einen einfachen Flowchart (Ablaufdiagramm) mit den 6 Phasen des Incident-Response-Prozesses. Nutzt dazu ein Online-Tool eurer Wahl.  
  https://affine.ideenschmiede.hamburg/workspace/4def35ef-4587-45fc-bfd4-73b2ac3b4e32/4oM-PS4u5MxOmcFbjIbmV
2. **Rollenspiel "Ransomware-Alarm":** Simuliert folgende Situation als Rollenspiel: Ein Mitarbeiter der "KreativKopf GmbH" ruft panisch im IT-Helpdesk an, weil auf seinem Bildschirm eine Lösegeldforderung erschienen ist. Ein Teammitglied ist der Mitarbeiter, ein anderes der Helpdesk-Agent. Spielt das Gespräch durch. Welche drei Anweisungen muss der Helpdesk-Agent dem Mitarbeiter _sofort_ geben, um die Eindämmung (Containment) zu starten?  
  „Trennen Sie **sofort Ihr Gerät vom Netzwerk** (LAN/WLAN).“„**Starten Sie den Computer nicht neu** und öffnen Sie keine Dateien.“„**Bleiben Sie am Telefon** und geben Sie das Gerät nicht aus der Hand – wir kümmern uns um die Wiederherstellung.“
3. **Lessons Learned:** Bezieht euch auf das ursprüngliche Phishing-Szenario der "KreativKopf GmbH". Was wären die wichtigsten "Lessons Learned" aus diesem Vorfall? Listet mindestens drei konkrete Punkte auf, die in den Notfallplan oder die Sicherheitsrichtlinien des Unternehmens aufgenommen werden sollten.  
  <br/>**Was könnte die Ursache (Schwachstelle) sein und welche Maßnahme wäre geeignet?**  
  <br/>**Ursache / Schwachstelle**
  
  - **Menschlicher Faktor / Social Engineering:**  
    Der Mitarbeiter fiel auf eine Phishing-E-Mail herein und gab seine Zugangsdaten preis. Dies zeigt, dass **Sensibilisierung und Schulung der Mitarbeitenden** unzureichend waren.
  - **Fehlende technische Absicherung:**  
    Es gab keine **Mehrfaktor-Authentifizierung (MFA)** für die SaaS-Dienste, wodurch ein kompromittiertes Passwort sofort Zugriff auf das Projektmanagement-Tool ermöglichte.
  - **Unzureichende E-Mail-Sicherheitskontrollen:**  
    Spam- oder Phishing-Filter waren entweder nicht vorhanden oder unzureichend konfiguriert, sodass die Phishing-Mail den Posteingang erreichte.
  
  **Technische Maßnahmen:**  
  <br/>**Geeignete Maßnahmen**
  1. **Awareness & Schulungen:**  
    Regelmäßige Mitarbeiterschulungen zum Erkennen von Phishing und unsicheren Links. Simulierte Phishing-Tests zur Übung.
  2. **Technische Sicherheitsmaßnahmen:**
    - Einführung von **MFA** für alle wichtigen Cloud- und SaaS-Konten.
    - Starke Passwort-Richtlinien (z. B. Passwortmanager, keine Wiederverwendung von Passwörtern).
    - Verbesserte E-Mail-Sicherheitslösungen: Anti-Phishing, Spamfilter, DMARC/SPF/DKIM-Konfigurationen.
  3. **Prozesse & Richtlinien:**
    - Klare **Meldewege** bei verdächtigen E-Mails.
    - Regelmäßige Überprüfung von Benutzerrechten und Zugängen.
    - Implementierung eines Notfallplans für kompromittierte Konten (Passwortänderung, Zugriff sperren, Log-Überprüfung).
4. **Recherche Meldepflicht:** Recherchiert, innerhalb welcher Frist ein relevanter Datenschutzvorfall nach DSGVO an die zuständige Aufsichtsbehörde gemeldet werden muss.  
  <br/>**Frist:** Ein relevanter Datenschutzvorfall muss **innerhalb von 72 Stunden** nach Bekanntwerden **der zuständigen Aufsichtsbehörde** gemeldet werden.**Quelle:** Art. 33 DSGVO („Meldung von Verletzungen des Schutzes personenbezogener Daten an die Aufsichtsbehörde“).**Hinweis:**
  - Wenn die Meldung nicht innerhalb von 72 Stunden erfolgen kann, **muss eine Begründung für die Verzögerung** angegeben werden.
  - Zusätzlich müssen ggf. **betroffene Personen informiert** werden (Art. 34 DSGVO), wenn ein hohes Risiko für ihre Rechte und Freiheiten besteht.

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.7 "Incident Response – Reaktion auf Sicherheitsvorfälle"
- **Online-Ressource:** [BSI-Standard 200-4: Notfallmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-4.pdf%3F__blob%3DpublicationFile).