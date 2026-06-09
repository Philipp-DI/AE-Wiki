# LF4.2.2- Die eigentliche Schutzbedarfsfeststellung

Als angehender IT-Sicherheitsberater

möchte ich lernen, den Schutzbedarf für Zielobjekte zu bestimmen,

damit ich eine fundierte Grundlage für die Risikoanalyse und die Auswahl angemessener Schutzmaßnahmen schaffen kann.

# Celebration Criteria

- Wir können die drei Schutzbedarfskategorien des BSI ("normal", "hoch", "sehr hoch") den möglichen Schadensauswirkungen zuordnen.
- Wir können für ein Zielobjekt den Schutzbedarf für Vertraulichkeit, Integrität und Verfügbarkeit bestimmen und unsere Entscheidung anhand von Schadensszenarien begründen.
- Wir können das Maximumprinzip anwenden, um den Schutzbedarf von einem Zielobjekt auf ein abhängiges Zielobjekt zu "vererben".
- Wir können die Ergebnisse in einer Tabelle nach BSI-Vorbild dokumentieren.

# Wissens-Briefing

Nachdem wir wissen, **was** wir schützen müssen, legen wir fest, **wie stark** wir es schützen müssen.

## Schutzbedarfskategorien

Der Schutzbedarf wird für jeden der drei Grundwerte (Vertraulichkeit, Integrität, Verfügbarkeit) separat festgelegt. Das BSI schlägt drei Kategorien vor, die sich an den maximal tolerierbaren Schäden orientieren:

- **Normal:** Ein Schaden wäre ärgerlich und mit begrenztem Aufwand verbunden, ist aber für das Unternehmen nicht existenzbedrohend. Die Auswirkungen sind überschaubar.
- **Hoch:** Ein Schaden hätte beträchtliche Auswirkungen. Er könnte zu erheblichen finanziellen Verlusten, Image-Schäden oder zur Verletzung gesetzlicher Vorschriften führen.
- **Sehr Hoch:** Ein Schaden hätte katastrophale, existenzbedrohende Auswirkungen für das Unternehmen, könnte die persönliche Unversehrtheit von Menschen gefährden oder gegen Gesetze in schwerwiegender Weise verstoßen.

**Der Prozess:** Für jedes Zielobjekt aus der Strukturanalyse stellt man sich die Frage: "Was ist der maximale denkbare Schaden, wenn die **Vertraulichkeit / Integrität / Verfügbarkeit** dieses Objekts verletzt wird?" Anhand der Antwort ordnet man die entsprechende Kategorie zu.

## Das Maximumprinzip (Vererbung)

Der Schutzbedarf vererbt sich in der Regel von oben nach unten. Eine Anwendung kann nur so sicher sein wie das IT-System, auf dem sie läuft.

- **Beispiel:** Die Anwendung "Kundendatenbank" hat einen **hohen** Schutzbedarf bezüglich Vertraulichkeit. Der Server, auf dem diese Anwendung läuft, muss daher ebenfalls mindestens einen **hohen** Schutzbedarf bezüglich Vertraulichkeit haben. Hat der Server noch eine andere Anwendung mit **sehr hohem** Schutzbedarf, erbt er diesen **sehr hohen** Schutzbedarf (Maximumprinzip).

# Aufgaben

1. **Schutzbedarf bestimmen:** Nehmt eure Liste der Zielobjekte aus der vorherigen Lern-Story. Bestimmt nun für jedes Zielobjekt den Schutzbedarf für V, I und V. Nutzt eine Tabelle mit den Spalten: `Zielobjekt`, `Schutzbedarf Vertraulichkeit`, `Begründung`, `Schutzbedarf Integrität`, `Begründung`, `Schutzbedarf Verfügbarkeit`, `Begründung`.
2. **Maximumprinzip anwenden:** Identifiziert in eurer Liste mindestens zwei Beispiele, bei denen das Maximumprinzip zur Anwendung kommt. Markiert diese und erklärt kurz, warum der Schutzbedarf "vererbt" wird.
3. **Diskussion von Grenzfällen:** Diskutiert in der Gruppe folgende Fälle für die "KreativKopf GmbH":
  - Welchen Schutzbedarf hat die Verfügbarkeit der internen Chat-Anwendung? (Normal? Hoch?)
  - Welchen Schutzbedarf hat die Vertraulichkeit von Entwürfen, die für einen Pitch bei einem Neukunden erstellt wurden? (Hoch? Sehr hoch?) Begründet eure unterschiedlichen Meinungen.
4. **Dokumentation:** Füllt die finale Schutzbedarfstabelle für den Grafikdesigner-Arbeitsplatz sauber und vollständig aus. Achtet auf eine klare und nachvollziehbare Formulierung der Begründungen.

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Schutzbedarfsfeststellung" (S. 997-999).
- **Online-Ressource:** [BSI-Standard 200-2: IT-Grundschutz-Vorgehensweise (PDF)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-2.pdf%3F__blob%3DpublicationFile), Kapitel 4.3 "Schutzbedarfsfeststellung".
- **Tool:** [Digital-Social-Chart der Fachhochschule Münster](https://www.google.com/search?q=https://digital-social-chart.de/schutzbedarfsfeststellung/) - Ein Online-Tool zur Unterstützung bei der Schutzbedarfsfeststellung.

Als angehender IT-Sicherheitsberater

möchte ich lernen, den Schutzbedarf für Zielobjekte zu bestimmen,

damit ich eine fundierte Grundlage für die Risikoanalyse und die Auswahl angemessener Schutzmaßnahmen schaffen kann.

# Celebration Criteria

- Wir können die drei **Schutzbedarfskategorien des BSI ("normal", "hoch", "sehr hoch")** den **möglichen Schadensauswirkungen** zuordnen.
- Wir können für ein Zielobjekt den Schutzbedarf für **Vertraulichkeit, Integrität und Verfügbarkeit** bestimmen und unsere Entscheidung anhand von **Schadensszenarien** begründen.
- Wir können das **Maximumprinzip** anwenden, um den Schutzbedarf von einem Zielobjekt auf ein abhängiges Zielobjekt zu "vererben".
- Wir können die Ergebnisse in einer **Tabelle nach BSI-Vorbild** dokumentieren.

# Wissens-Briefing

Nachdem wir wissen, **was** wir schützen müssen, legen wir fest, **wie stark** wir es schützen müssen.

## Schutzbedarfskategorien

Der Schutzbedarf wird für jeden der drei Grundwerte (Vertraulichkeit, Integrität, Verfügbarkeit) separat festgelegt. Das BSI schlägt drei Kategorien vor, die sich an den maximal tolerierbaren Schäden orientieren:

- **Normal:** Ein Schaden wäre ärgerlich und mit begrenztem Aufwand verbunden, ist aber für das Unternehmen nicht existenzbedrohend. Die Auswirkungen sind überschaubar.
- **Hoch:** Ein Schaden hätte beträchtliche Auswirkungen. Er könnte zu erheblichen finanziellen Verlusten, Image-Schäden oder zur Verletzung gesetzlicher Vorschriften führen.
- **Sehr Hoch:** Ein Schaden hätte katastrophale, existenzbedrohende Auswirkungen für das Unternehmen, könnte die persönliche Unversehrtheit von Menschen gefährden oder gegen Gesetze in schwerwiegender Weise verstoßen.

**Der Prozess:** Für jedes Zielobjekt aus der Strukturanalyse stellt man sich die Frage: "Was ist der maximale denkbare Schaden, wenn die **Vertraulichkeit / Integrität / Verfügbarkeit** dieses Objekts verletzt wird?" Anhand der Antwort ordnet man die entsprechende Kategorie zu.

## Das Maximumprinzip (Vererbung)

Der Schutzbedarf vererbt sich in der Regel von oben nach unten. Eine Anwendung kann nur so sicher sein wie das IT-System, auf dem sie läuft.

- **Beispiel:** Die Anwendung "Kundendatenbank" hat einen **hohen** Schutzbedarf bezüglich Vertraulichkeit. Der Server, auf dem diese Anwendung läuft, muss daher ebenfalls mindestens einen **hohen** Schutzbedarf bezüglich Vertraulichkeit haben. Hat der Server noch eine andere Anwendung mit **sehr hohem** Schutzbedarf, erbt er diesen **sehr hohen** Schutzbedarf (Maximumprinzip).

# Aufgaben

1. **Schutzbedarf bestimmen:** Nehmt eure Liste der Zielobjekte aus der vorherigen Lern-Story. Bestimmt nun für jedes Zielobjekt den Schutzbedarf für V, I und V. Nutzt eine Tabelle mit den Spalten: `Zielobjekt`, `Schutzbedarf Vertraulichkeit`, `Begründung`, `Schutzbedarf Integrität`, `Begründung`, `Schutzbedarf Verfügbarkeit`, `Begründung`.
  
  | Zielobjekt | Schutzbedarf Vertraulichkeit | Begründung | Schutzbedarf Integrität | Begründung | Schutzbedarf Verfügbarkeit | Begründung |
  | --- | --- | --- | --- | --- | --- | --- |
  | **Desktop-PC** | Hoch | Enthält sensible Projektdateien und Zugang zu Anwendungen. | Sehr hoch | Alle Daten und Software müssen korrekt sein und funktionieren. | Sehr hoch | Ausfall blockiert sämtliche Arbeit. |
  | **Bildbearbeitung (Adobe CC)** | Hoch | Verarbeitung vertraulicher Kundendaten in Bildbearbeitung und Entwürfe. | Hoch | Bearbeitung von Bildern mit fehlerhaften Kundendaten, kann zu fehlerhafte Projektausführung kommen. | Hoch | Verzögerung der Arbeitsprozesse bei Projekten wenn es zu einem Ausfall kommt. |
  | **NAS-Server** | Hoch | Zwischengespeicherte Dateien können vertraulich sein. | Hoch | Daten müssen fehlerfrei gespeichert werden | Hoch | Daten müssen für Arbeitsfluss verfügbar sein. |
  | **Büroraum** | Hoch | Unbefugte sollten keinen Zugang haben, da sonst sensible Daten mitgelesen oder gestohlen werden könnten. | Normal | Die Integrität des Raumes ist absolut zweitrangig und hat keine Priorität. Nur durch abstrakte Fälle kann hierdurch ein Schaden entstehen. | Normal | Verzögerung der Arbeitsprozesse **_vor Ort_** bei Projekten wenn es zu einem Ausfall kommt. |
  | **WAN, LAN, WLAN** | Hoch | Zugang zur Cloud-Anwendung benötigt sichere Internet-Verbindung. | Hoch | Datenübertragung muss fehlerfrei sein. | Hoch | Netzverbindung notwendig für Zugriff auf Cloud und NAS. |
  | **Cloudzugang/ Cloud-Speicher** | Sehr hoch | Zugangsdaten müssen vertraulich behandelt werden! Enthält finale Kundendaten und vertrauliche Projekte. | Sehr hoch | Zugangsdaten und Kundendaten müssen unverändert und korrekt sein. | Sehr hoch | Ausfall verhindert Zugriff auf zentrale Daten/Kundendaten/Entwürfe. |
  
    
  
2. **Maximumprinzip anwenden:** Identifiziert in eurer Liste mindestens zwei Beispiele, bei denen das Maximumprinzip zur Anwendung kommt. Markiert diese und erklärt kurz, warum der Schutzbedarf "vererbt" wird. → https://www.bsi.bund.de/DE/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/IT-Grundschutz/Zertifizierte-Informationssicherheit/IT-Grundschutzschulung/Online-Kurs-IT-Grundschutz/Lektion_4_Schutzbedarfsfeststellung/Lektion_4_03/Lektion_4_03_node.html**Desktop-PC des Designers\*\*  
  → Erbt „**_sehr hoch_**“ bei Vertraulichkeit, weil dort **Entwürfe (sehr hoch)** und **Kundendaten (sehr hoch)** verarbeitet und (zwischen)gespeichert sind.  
  → Das System muss daher insgesamt als **sehr** **hoch** bewertet werden, auch wenn einzelne Komponenten geringeren Bedarf hätten.**Büroraum**  
  → Erbt „**_sehr hoch_**“ bei Verfügbarkeit, weil der Desktop-PC hier steht (_angenommen remote work ist nicht möglich_).  
  → Wenn der Raum nicht verfügbar ist, kann nicht am PC, der hier steht, gearbeitet werden.
3. **Diskussion von Grenzfällen:** Diskutiert in der Gruppe folgende Fälle für die "KreativKopf GmbH":
  - Welchen Schutzbedarf hat die Verfügbarkeit der internen Chat-Anwendung? (Normal? Hoch?)
  - Welchen Schutzbedarf hat die Vertraulichkeit von Entwürfen, die für einen Pitch bei einem Neukunden erstellt wurden? (Hoch? Sehr hoch?) Begründet eure unterschiedlichen Meinungen.**Meinung A (Normal):** Ein kurzer Ausfall ist verkraftbar, da Kommunikation auch über Telefon oder E-Mail möglich ist.**Meinung B (Hoch):** Während eines Kundenprojekts kann fehlende Abstimmung zu Verzögerungen, Missverständnissen oder Projektfehlern führen.
4. **Dokumentation:** Füllt die finale Schutzbedarfstabelle für den Grafikdesigner-Arbeitsplatz sauber und vollständig aus. Achtet auf eine klare und nachvollziehbare Formulierung der Begründungen. → _siehe oben_

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.5 "Der Weg zum Sicherheitskonzept", Abschnitt "Schutzbedarfsfeststellung"
- **Online-Ressource:** [BSI-Standard 200-2: IT-Grundschutz-Vorgehensweise (PDF)](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-2.pdf%3F__blob%3DpublicationFile), Kapitel 4.3 "Schutzbedarfsfeststellung".
- **Tool:** [Digital-Social-Chart der Fachhochschule Münster](https://www.google.com/search?q=https://digital-social-chart.de/schutzbedarfsfeststellung/) - Ein Online-Tool zur Unterstützung bei der Schutzbedarfsfeststellung.