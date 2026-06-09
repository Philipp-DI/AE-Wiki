# LF4.1- Grundlagen der Schutzbedarfsanalyse

Als Umschüler zum Fachinformatiker

möchte ich die Grundlagen und die Notwendigkeit der Schutzbedarfsanalyse verstehen,

damit ich die IT-Sicherheitsmaßnahmen in einem Unternehmen kontextbezogen einordnen und begründen kann.

# Celebration Criteria

- Wir können die drei Grundwerte der Informationssicherheit (Vertraulichkeit, Integrität, Verfügbarkeit) erklären und anhand von Praxisbeispielen voneinander abgrenzen.  
  **Vertraulichkeit (Confidentiality)**
  - Bedeutung: Nur autorisierte Personen dürfen auf die Informationen zugreifen.
  - Beispiel: Nur die Buchhaltung darf Gehaltsdaten der Mitarbeiter einsehen, externe Partner nicht.
  - Verstoß: Ein unbefugter Zugriff auf geheime Dokumente – Datenleck.
- **Integrität (Integrity)**
  - Bedeutung: Informationen dürfen nicht unberechtigt verändert, beschädigt oder manipuliert werden.
  - Beispiel: Eine Banküberweisung darf auf dem Weg vom Kunden zur Bank nicht geändert werden.
  - Verstoß: Ein Hacker verändert den Betrag der Überweisung – Integrität verletzt.
- **Verfügbarkeit (Availability)**
  - Bedeutung: Informationen und Systeme müssen für berechtigte Benutzer verfügbar sein, wenn sie benötigt werden.
  - Beispiel: Die Bankwebsite muss rund um die Uhr verfügbar sein, damit Kunden Transaktionen durchführen können.
  - Verstoß: Ein Server ist durch einen DDoS-Angriff nicht erreichbar – Mitarbeiter und Kunden können nicht arbeiten.

**Wichtig:** Die drei Grundwerte stehen in Verbindung, können sich aber unterscheiden:

- Man kann Vertraulichkeit und Integrität schützen, aber die Verfügbarkeit verlieren.
- Man kann Verfügbarkeit gewährleisten, aber die Vertraulichkeit verletzen, wenn Daten öffentlich werden.

Ziel der Informationssicherheit ist es, **ein ausgewogenes Verhältnis zwischen diesen drei Aspekten herzustellen**.

- Wir können den Zweck und die Phasen eines Sicherheitsprozesses nach der Methodik des BSI-IT-Grundschutzes erläutern.  
  <br/>**Zweck des Sicherheitsprozesses:**
  - Systematischen Schutz der Informationswerte sicherstellen.
  - Risiken von Datenverlust, Manipulation oder Nichtverfügbarkeit minimieren.
  - Transparente Zuständigkeiten und Kontrollmechanismen schaffen.
- **Hauptphasen nach BSI-IT-Grundschutz:**
  1. **Initiierung**
    - Ziele der Informationssicherheit definieren.
    - Verantwortliche Personen und Ressourcen benennen.
    - Beispiel: Die Geschäftsführung entscheidet, einen Schutzprozess einzuführen.
  2. **Strukturanalyse**
    - Alle IT-Systeme, Daten und Prozesse erfassen.
    - „Kronjuwelen“ identifizieren – besonders schützenswerte Informationen.
  3. **Schutzbedarfsfeststellung**
    - Bestimmen, welche Objekte hohen Schutzbedarf haben und welche nur Basis-Schutz.
  4. **Umsetzung von Sicherheitsmaßnahmen**
    - Technische, organisatorische und personelle Maßnahmen einführen.
    - Beispiele: Datenverschlüsselung, Multi-Faktor-Authentifizierung, Schulungen.
  5. **Überprüfung / Audit**
    - Wirksamkeit der Maßnahmen kontrollieren.
    - Gefundene Lücken beheben.
  6. **Fortlaufende Verbesserung**
    - Maßnahmen kontinuierlich an neue Bedrohungen anpassen.
    - Prozesse und Dokumentation aktualisieren.
- Wir können die wichtigsten rechtlichen und normativen Rahmenbedingungen (DSGVO, IT-SiG 2.0, BSI, ISO 27001) für die Informationssicherheit in Deutschland benennen und ihren Zweck erklären.
  
  | **Rahmen / Norm** | **Beschreibung** | **Zweck / Ziel** |
  | --- | --- | --- |
  | **DSGVO (Datenschutz-Grundverordnung)** | EU-Verordnung zum Schutz personenbezogener Daten. Gilt für alle Unternehmen, die Daten von EU-Bürgern verarbeiten. | Schutz personenbezogener Daten, Transparenz der Datenverarbeitung, Stärkung der Rechte der Betroffenen. |
  | **IT-SiG 2.0 (IT-Sicherheitsgesetz 2.0)** | Deutsches Gesetz zur Stärkung der IT-Sicherheit, besonders in kritischen Infrastrukturen. | Erhöhung der IT-Sicherheit, Meldepflicht bei Sicherheitsvorfällen, Verpflichtung zu technischen und organisatorischen Schutzmaßnahmen. |
  | **BSI (Bundesamt für Sicherheit in der Informationstechnik)** | Nationale Behörde für IT-Sicherheit, erstellt Standards, Richtlinien und den **BSI-IT-Grundschutz**. | Förderung der IT-Sicherheit in Deutschland, Beratung und Unterstützung von Behörden und Unternehmen. |
  | **ISO/IEC 27001** | International anerkannte Norm für Informationssicherheits-Managementsysteme (ISMS). | Etablierung eines strukturierten Managementsystems zur kontinuierlichen Verbesserung der Informationssicherheit. |
  
- Wir können die Begriffe "Gefährdung", "Schwachstelle" und "Risiko" im Kontext der IT-Sicherheit definieren und an konkreten Beispielen erläutern.  
  **Risiko = Gefährdung × Schwachstelle**  
  <br/>in Mitarbeiter klickt auf einen Phishing-Link →  
  Gefährdung: Phishing-Mail  
  Schwachstelle: Unachtsamkeit / fehlendes Sicherheitsbewusstsein  
  Risiko: Kompromittierte Zugangsdaten
  
  | **Begriff** | **Definition** | **Beispiel** |
  | --- | --- | --- |
  | **Gefährdung** | Ein potenzielles Ereignis, das Schaden an Informationswerten oder Systemen verursachen kann. | Hackerangriff, Feuer, Stromausfall, Phishing-Mail. |
  | **Schwachstelle** | Eine Schwäche oder Lücke im System, die eine Gefährdung ausnutzen kann. | Unsichere Passwörter, fehlende Updates, keine Datensicherung. |
  | **Risiko** | Die Wahrscheinlichkeit, dass eine Gefährdung eine Schwachstelle ausnutzt und Schaden verursacht. | Wenn Mitarbeiter schwache Passwörter nutzen, besteht hohes Risiko eines Datendiebstahls. |
  

# Fiktives Szenario

Die "KreativKopf GmbH", eine kleine Werbeagentur mit 15 Mitarbeitenden, arbeitet hauptsächlich in der Cloud und nutzt diverse SaaS-Dienste für Grafikdesign, Projektmanagement und Kundenkommunikation. Kürzlich gab es einen Vorfall, bei dem ein Mitarbeiter auf eine Phishing-E-Mail hereinfiel und seine Zugangsdaten für das Projektmanagement-Tool preisgab. Es entstand zwar kein direkter finanzieller Schaden, aber die Geschäftsführung ist alarmiert und befürchtet Reputationsschäden und den Verlust von Kundendaten. Ein IT-Sicherheitskonzept existiert bisher nicht.

# Gesamtaufgabe

Erstellt als Lerngruppe eine Präsentation für die Geschäftsführung der "KreativKopf GmbH". Klärt darin über die fundamentalen Schutzziele der Informationssicherheit auf und verdeutlicht, welche dieser Ziele im geschilderten Szenario verletzt wurden oder gefährdet sind. Stellt die grundlegenden Phasen eines Sicherheitsprozesses vor und begründet, warum eine systematische Schutzbedarfsanalyse für die Agentur unerlässlich ist, um zukünftige Vorfälle zu vermeiden und Kundenvertrauen zu sichern. **Nutzt für die Präsentation eine Kreativtechnik eurer Wahl aus eurem Methodenkoffer.**

**→ Technisches Storytelling - Wie geht das?**

1. **Definieren Sie das "Warum":** Was ist die Kernbotschaft Ihrer Präsentation? Warum sollte sich das Publikum dafür interessieren? → **_IT-Sicherheit sollte höchste Priorität haben! Jay_**
2. **Finden Sie Ihren Helden:** Der Held ist nicht die Technologie, sondern der Mensch, der davon profitiert. Das kann ein:e Endbenutzer:in, ein:e Kolleg:in aus einer anderen Abteilung oder das Unternehmen als Ganzes sein. → **_Mitarbeitern (Cornelia), die geschult ist, weist ihren Kollegen auf eine verdächtige Phishing Mail hin; und verhindert so Schlimmeres! Olena_**
3. **Beschreiben Sie den Konflikt:** Welches Problem hat Ihr Held? Welche Herausforderung muss er meistern? Beschreiben Sie den Schmerzpunkt so konkret und nachvollziehbar wie möglich. → **_Aufgrund des Szenarios (s.o.) bleibt der Zugriff auf das Arbeitsprojekt verwehrt. Somit entsteht ein Rücklauf an Arbeit und ein großer, finanzieller Schaden. Olena_**
4. **Präsentieren Sie die Lösung:** Zeigen Sie, wie Ihre technische Lösung (das neue Feature, der optimierte Prozess) dem Helden hilft, den Konflikt zu überwinden und sein Ziel zu erreichen. → **_BSI-IT-Grundschutz Maßnahmen durchführen_**  
  Erzählt als „Held\*innenreise“:
  1. **Initiierung: Mohammed**  
    Geschäftsführung erkennt, dass IT-Sicherheit Chefsache ist.  
    → _„Wir müssen handeln!“_
  2. **Strukturanalyse: Jay**  
    Alle Systeme, Anwendungen und Daten werden erfasst.  
    → _„Wo liegen unsere Kronjuwelen?“_
  3. **Schutzbedarfsanalyse: Philipp**  
    Bestimmung, welche Daten **kritisch** für die Agentur sind.  
    → Kundendaten = sehr hoher Schutzbedarf!
  4. **Modellierung und Umsetzung: Janine**  
    Passende Sicherheitsmaßnahmen (z. B. Backup, Firewall, MFA) werden eingeführt.
  5. **Kontrolle und Verbesserung: Janine**  
    Regelmäßige Tests, Awareness-Schulungen, Notfallübungen.  
    → _„Sicherheit ist kein Projekt, sondern ein Prozess.“_  
    **Der Weg zur Sicherheit**
5. **Nutzen Sie Details und Emotionen:** Eine gute Geschichte lebt von Details. Beschreiben Sie die Situation des Helden lebhaft und wecken Sie Emotionen wie Mitgefühl für das Problem und Freude über die Lösung.

https://www.canva.com/design/DAG2ZhrqAd0/5Eej2NUIghBgIH-ropzJwg/edit?utm_content=DAG2ZhrqAd0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton  
<br/>Als PDF:

Notizen: - Risikomatrix erstellen!

[IT-Sicherheit_-\_KreativKopf_GmbH.pdf](files/019cee3c-0b53-75c8-81bd-4fd9a322ce75/IT-Sicherheit_-_KreativKopf_GmbH.pdf)

  
**_Story Beispiel K.I:_** Chatgpt  
🛡️ **Cornelia und die unsichtbare Bedrohung – Eine Heldinnengeschichte über IT-Sicherheit**

### **1\. Initiierung – „Wir müssen handeln!“**

Montagmorgen, 9:00 Uhr. Die Sonne scheint durch die Glasfassade der Agentur KreationPlus. Alles läuft wie gewohnt – bis plötzlich die Geschäftsführung eine dringende E-Mail erhält:  
Ein Kunde meldet, dass vertrauliche Projektdaten im Umlauf sind. Ein Albtraum.

In der Krisensitzung wird klar: IT-Sicherheit war bisher _ein Thema für die IT-Abteilung_. Jetzt erkennt die Geschäftsführung:

> „Das betrifft uns alle – IT-Sicherheit ist Chefsache! Wir müssen handeln.“

So beginnt die Reise.

---

### **2\. Strukturanalyse – „Wo liegen unsere Kronjuwelen?“**

Ein interdisziplinäres Team wird zusammengestellt: IT, Verwaltung, Projektmanagement. Gemeinsam kartieren sie alle Systeme, Anwendungen und Datenflüsse.  
Cornelia, Projektmanagerin, hilft, die Abläufe ihrer Abteilung zu dokumentieren. Dabei wird ihr bewusst, wie viele sensible Daten tagtäglich durch ungeschützte Kanäle gehen.

> „Wir wussten gar nicht, _wo überall_ Kundendaten liegen“, sagt sie später.  
> „Erst durch die Analyse wurde uns klar, wie verletzlich wir wirklich sind.“

---

### **3\. Schutzbedarfsanalyse – „Was ist kritisch?“**

Das Team bewertet den Schutzbedarf der Daten. Besonders Kundendaten und Projektskizzen erweisen sich als _hochkritisch_. Ein Verlust oder Leak könnte nicht nur finanziellen Schaden verursachen, sondern auch den Ruf der Agentur ruinieren.

> „Wenn unsere Kunden uns nicht mehr vertrauen, verlieren wir alles“, denkt Cornelia.

---

### **4\. Modellierung und Umsetzung – „Wir bauen unsere Schutzmauer.“**

Auf Basis des **BSI-IT-Grundschutzes** werden Maßnahmen eingeführt:

- Multi-Faktor-Authentifizierung (MFA) für alle Zugänge
- Regelmäßige Backups und ein neues Firewall-System
- Awareness-Schulungen für alle Mitarbeitenden

Cornelia nimmt an einer dieser Schulungen teil. Anfangs ist sie skeptisch – Phishing, Passwörter, Updates – klingt nach IT-Sh\*t.  
Doch dann passiert es.

Ein paar Wochen später erhält sie eine E-Mail mit dem Betreff: _„Projektänderung dringend – bitte prüfen“_. Der Absender sieht vertraut aus.  
Doch Cornelia erinnert sich an die Schulung: Tippfehler in der Adresse, ungewöhnlicher Link.  
Sie stoppt, informiert die IT – und verhindert so, dass Schadsoftware das gesamte Firmennetzwerk lahmlegt.

> „Ein Klick – und alles wäre verloren gewesen“, sagt sie erleichtert.

---

### **5\. Kontrolle und Verbesserung – „Sicherheit ist kein Projekt, sondern ein Prozess.“**

Seitdem hat sich viel verändert. IT-Sicherheit ist kein lästiges Thema mehr, sondern Teil des Alltags:  
Regelmäßige Tests, Notfallübungen, Feedbackrunden.

Cornelia wird intern zur „Security-Botschafterin“.  
Ihre Kolleginnen hören auf sie, wenn sie sagt:

> „Ich hab da was Verdächtiges entdeckt lasst uns lieber prüfen.“

Die Agentur ist heute sicherer, stärker und bewusster.  
Nicht, weil sie Technik gekauft hat –  
sondern, weil ihre Menschen gelernt haben, Verantwortung zu übernehmen.

---

### 💬 **Schlussbotschaft**

IT-Sicherheit ist keine Frage der Technik allein.  
Sie beginnt mit Menschen wie Cornelia –  
die hinschauen, verstehen und handeln.  
<br/>**_Prompt für Vidnoz_**:

_Es ist Montagmorgen in der Agentur KreationPlus._  
_Alles läuft wie immer – bis plötzlich eine alarmierende Nachricht eingeht: Vertrauliche Projektdaten sind im Umlauf._  
_Die Geschäftsführung reagiert sofort. „IT-Sicherheit ist Chefsache. Wir müssen handeln!“_

_Von diesem Moment an ändert sich alles._  
_Cornelia, Projektmanagerin, wird Teil des neuen Sicherheitsteams. Gemeinsam mit Kolleginnen und Kollegen analysiert sie alle Systeme und Datenflüsse._  
_Dabei wird schnell klar: Viele vertrauliche Informationen sind ungeschützt._  
_„Unsere Kronjuwelen – die Kundendaten – liegen offen da“, denkt sie besorgt._

_Es folgen Schulungen. Themen wie Phishing, sichere Passwörter, Backups und Mehrfaktor-Authentifizierung._  
_Cornelia nimmt aufmerksam teil, auch wenn sie anfangs denkt: „So schlimm wird’s schon nicht sein.“_

_Doch einige Wochen später erhält sie eine E-Mail mit dem Betreff: „Projektänderung dringend – bitte prüfen.“_  
_Der Absender sieht vertraut aus. Ein kurzer Moment des Zweifelns – dann erinnert sie sich an die Schulung._  
_Der Absender ist gefälscht. Der Link verdächtig._  
_Cornelia klickt nicht. Stattdessen informiert sie die IT._

_Wenig später steht fest: Sie hat einen Angriff verhindert, der das gesamte Netzwerk lahmgelegt hätte._

_Heute gilt Cornelia als Vorbild in ihrer Firma._  
_Sie weiß: IT-Sicherheit ist kein Projekt, das irgendwann abgeschlossen ist –_  
_sondern ein Prozess, der jeden betrifft._

_Denn echte Sicherheit beginnt bei den Menschen,_  
_die mutig genug sind, hinzusehen und zu handeln._

[Video_ohne_Titel_(1).mp4](files/019cee3c-0b53-75c8-81bd-51a381ad01de/Video_ohne_Titel_(1).mp4)[Video_ohne_Titel.mp4](files/019cee3c-0b53-75c8-81bd-55d21b0d0124/Video_ohne_Titel.mp4)