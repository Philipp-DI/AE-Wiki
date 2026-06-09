# 🐝 Janine

Als Mitglied eines Incident-Response-Teams

möchte ich die grundlegenden Schritte im Umgang mit Schutzverletzungen kennen,

damit ich im Ernstfall schnell, strukturiert und korrekt handeln kann, um den Schaden zu minimieren.

# Celebration Criteria

- Wir können die Phasen eines typischen Incident-Response-Prozesses (z.B. Vorbereitung, Identifikation, Eindämmung, Beseitigung, Wiederherstellung, Lessons Learned) benennen.
- Wir können erklären, warum eine umgehende Meldung eines Sicherheitsvorfalls entscheidend ist.
- Wir können mindestens drei Sofortmaßnahmen nennen, die bei einer akuten Ransomware-Infektion an einem Arbeitsplatz ergriffen werden sollten.
- Wir können die Bedeutung der "Lessons Learned"-Phase für die zukünftige Verbesserung der IT-Sicherheit erklären.

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

1. 

![](files/019cee46-a41d-73bd-81b3-f4d8ed7bbf1e/ChatGPT_Image_6._Nov._2025,_14_50_03.png)

**Prozess visualisieren:** Erstellt einen einfachen Flowchart (Ablaufdiagramm) mit den 6 Phasen des Incident-Response-Prozesses. Nutzt dazu ein Online-Tool eurer Wahl.**Vorbereitung (Preparation)**  
↓**Identifikation (Identification)**  
↓**Eindämmung (Containment)**  
↓**Beseitigung (Eradication)**  
↓**Wiederherstellung (Recovery)**  
↓**Lessons Learned (Post-Incident Activity)**

- **Rollenspiel "Ransomware-Alarm":** Simuliert folgende Situation als Rollenspiel: Ein Mitarbeiter der "KreativKopf GmbH" ruft panisch im IT-Helpdesk an, weil auf seinem Bildschirm eine Lösegeldforderung erschienen ist. Ein Teammitglied ist der Mitarbeiter, ein anderes der Helpdesk-Agent. Spielt das Gespräch durch. Welche drei Anweisungen muss der Helpdesk-Agent dem Mitarbeiter _sofort_ geben, um die Eindämmung (Containment) zu starten?**Trennen Sie den Computer sofort vom Netzwerk.**  
  (Ziehen Sie das Netzwerkkabel oder schalten Sie WLAN aus, um die Ausbreitung zu stoppen)**Schalten Sie den Computer nicht aus und verändern Sie nichts**  
  (Das System muss für die forensische Analyse unverändert bleiben)**Informieren Sie keine weiteren Personen über private Kanäle**, sondern  
  **melden Sie den Vorfall nur an die IT-Sicherheitsabteilung**
- **Lessons Learned:** Bezieht euch auf das ursprüngliche Phishing-Szenario der "KreativKopf GmbH". Was wären die wichtigsten "Lessons Learned" aus diesem Vorfall? Listet mindestens drei konkrete Punkte auf, die in den Notfallplan oder die Sicherheitsrichtlinien des Unternehmens aufgenommen werden sollten.**Verstärkte Schulung der Mitarbeitenden:**
  
  - Regelmäßige Awareness-Trainings zu Phishing, Social Engineering und verdächtigen E-Mails
  - Simulierte Phishing-Kampagnen zur Übung
  
  **Klare Melde- und Eskalationswege:**
  
  - Jeder Mitarbeiter muss wissen, **wie und an wen** er einen Vorfall sofort meldet
  - Einrichtung einer zentralen E-Mail-Adresse oder Notfallhotline
  
  **Technische Prävention und Monitoring:**
  - Einführung oder Verbesserung von **E-Mail-Filtern, Endpoint Detection & Response (EDR)** und **Backup-Strategien**
  - Regelmäßige Überprüfung, ob Backups offline und sicher aufbewahrt werden
  - **Logische/Netzwerk-Verbindung.** Das "Offline"-Backup ist fälschlicherweise noch über das Netzwerk erreichbar oder mit denselben Anmeldeinformationen wie das Produktivsystem verbunden. **Ransomware** greift gezielt diese Sicherungen an, um die Wiederherstellung zu verhindern. **Mangelnde Prüfroutinen.** Es wird nicht regelmäßig oder vollständig getestet, ob die Daten aus dem Offline-Backup tatsächlich **Wiederherstellbar** und **fehlerfrei** sind. Das Backup ist vorhanden, aber unbrauchbar (_"Backup-Lüge"_).**Unzureichende physische Sicherheit.** Das Offline-Speichermedium (Band, externe Festplatte) wird nicht sicher (z. B. feuerfest, zugangskontrolliert) gelagert, was zu **physischem Verlust**, Diebstahl oder Beschädigung führen kann. **Ungeprüfte Immutability**Die Daten werden als "unveränderbar" (immutable) markiert, aber die **technische Umsetzung** ist fehlerhaft oder die Aufbewahrungsfrist der Immutability ist zu kurz. **Unzureichende Segregation of Duties** Administratoren, die das Produktivsystem verwalten, haben auch **volle Zugriffsrechte** auf die Backup-Systeme, was das Risiko bei einer Kompromittierung des Admin-Kontos erhöht
- **Recherche Meldepflicht:** Recherchiert, innerhalb welcher Frist ein relevanter Datenschutzvorfall nach DSGVO an die zuständige Aufsichtsbehörde gemeldet werden muss.Nach **Artikel 33 der Datenschutz-Grundverordnung (DSGVO)** gilt:
  
  > **Ein relevanter Datenschutzvorfall muss innerhalb von 72 Stunden**  
  > **nach Bekanntwerden** des Vorfalls  
  > **an die zuständige Aufsichtsbehörde gemeldet werden**
  

| Thema | Kernaussage |
| --- | --- |

|     |     |
| --- | --- |
| **Incident-Response-Prozess** | Vorbereitung → Identifikation → Eindämmung → Beseitigung → Wiederherstellung → Lessons Learned |

|     |     |
| --- | --- |
| **Sofortmaßnahmen bei Ransomware** | 1\. Netzwerk trennen 2. System unverändert lassen 3. IT-Sicherheit informieren |

|     |     |
| --- | --- |
| **Lessons Learned (Phishing)** | Schulungen, klare Meldewege, technische Sicherheitsmaßnahmen |

|     |     |
| --- | --- |
| **DSGVO-Meldepflicht** | Innerhalb von **72 Stunden** an die Aufsichtsbehörde |

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.7 "Incident Response – Reaktion auf Sicherheitsvorfälle"
- **Online-Ressource:** [BSI-Standard 200-4: Notfallmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-4.pdf%3F__blob%3DpublicationFile).