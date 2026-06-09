# 🐝 Mohammed

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

1. **Prozess visualisieren:** Erstellt einen einfachen Flowchart (Ablaufdiagramm) mit den 6 Phasen des Incident-Response-Prozesses. Nutzt dazu ein Online-Tool eurer Wahl.[https://www.canva.com/design/DAG3n71f8TQ/0hFrGcH4JLgGHaTxBYjgIA/edit?utm_content=DAG3n71f8TQ&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton!\[\](files/019a48ef-3570-71bd-b7dd-885160eea7d5/image.png)](https://www.canva.com/design/DAG3n71f8TQ/0hFrGcH4JLgGHaTxBYjgIA/edit?utm_content=DAG3n71f8TQ&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton!%5B%5D%28files/019a48ef-3570-71bd-b7dd-885160eea7d5/image.png%29)
2. **Rollenspiel "Ransomware-Alarm":** Simuliert folgende Situation als Rollenspiel: Ein Mitarbeiter der "KreativKopf GmbH" ruft panisch im IT-Helpdesk an, weil auf seinem Bildschirm eine Lösegeldforderung erschienen ist. Ein Teammitglied ist der Mitarbeiter, ein anderes der Helpdesk-Agent. Spielt das Gespräch durch. Welche drei Anweisungen muss der Helpdesk-Agent dem Mitarbeiter _sofort_ geben, um die Eindämmung (Containment) zu starten?

**_Dialogbeispiel:_**

**👨‍💼 Mitarbeiter:**  
„Hilfe! Auf meinem Bildschirm steht, dass meine Dateien verschlüsselt wurden und ich ein Lösegeld zahlen soll! Was soll ich tun?!“

**👩‍💻 Helpdesk-Agent:**  
„Bleiben Sie ruhig, wir kümmern uns darum. Befolgen Sie bitte sofort diese drei Schritte:“

1. **Trennen Sie den Computer sofort vom Netzwerk!**  
  → Ziehen Sie das Netzwerkkabel oder deaktivieren Sie WLAN.  
  _(Ziel: Eindämmung der Verbreitung)_
2. \*\*Wenn der PC / Laptop sich nicht anders trennen lässt, ist auch Ausschalten / Zerstören möglich  
  _(Ziel: Beweise sichern, Verschlüsselungsprozess beobachten)_
3. **Informieren Sie Ihre Teamleitung und das IT-Sicherheits-Team sofort!**  
  → Offizielle Incident-Meldung wird gestartet.  
  _(Ziel: Eskalation und forensische Analyse starten)_

**👩‍💻 Helpdesk-Agent (weiter):**  
„Ich leite den Vorfall jetzt an unser Incident-Response-Team weiter. Bitte lassen Sie das Gerät so stehen und warten Sie auf weitere Anweisungen.“

3. **Lessons Learned:** Bezieht euch auf das ursprüngliche Phishing-Szenario der "KreativKopf GmbH". Was wären die wichtigsten "Lessons Learned" aus diesem Vorfall? Listet mindestens drei konkrete Punkte auf, die in den Notfallplan oder die Sicherheitsrichtlinien des Unternehmens aufgenommen werden sollten.

Nach der Analyse sollten folgende Punkte **in den Notfallplan** und die **Sicherheitsrichtlinien** aufgenommen werden:

| Nr. | Lesson Learned | Begründung / Maßnahme |
| --- | --- | --- |
| 1   | **Sensibilisierung der Mitarbeiter** | Regelmäßige Schulungen zu Phishing, Social Engineering und sicheren E-Mail-Praktiken. |
| 2   | **Schnelle Meldekette etablieren** | Jeder Vorfall muss sofort an das IT-Security-Team gemeldet werden – klare Verantwortlichkeiten. |
| 3   | **Technische Schutzmaßnahmen verstärken** | E-Mail-Filter, Endpoint-Schutz, Netzwerksegmentierung, regelmäßige Backups. |
| 4   | **Notfallhandbuch und Checklisten aktualisieren** | Enthält Vorgehen bei Ransomware, Kontaktlisten und Kommunikationsplan. |
| 5   | **Regelmäßige Incident-Response-Übungen** | Simulationen verbessern Reaktionsgeschwindigkeit und Koordination. |

3. **Recherche Meldepflicht:** Recherchiert, innerhalb welcher Frist ein relevanter Datenschutzvorfall nach DSGVO an die zuständige Aufsichtsbehörde gemeldet werden muss.

**_Meldepflicht nach DSGVO (Art. 33 DSGVO)_**

Ein Datenschutzvorfall muss innerhalb von 72 Stunden nach Bekanntwerden  
an die zuständige Aufsichtsbehörde gemeldet werden.

**Ausnahme:**  
Wenn „kein Risiko für die Rechte und Freiheiten betroffener Personen“ besteht, ist keine Meldung erforderlich.

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 22.7 "Incident Response – Reaktion auf Sicherheitsvorfälle"
- **Online-Ressource:** [BSI-Standard 200-4: Notfallmanagement](https://www.google.com/search?q=https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Grundschutz/BSI-Standards/BSI-Standard_200-4.pdf%3F__blob%3DpublicationFile).