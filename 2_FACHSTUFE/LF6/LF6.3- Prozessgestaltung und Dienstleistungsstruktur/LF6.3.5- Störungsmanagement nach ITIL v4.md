# LF6.3.5- Störungsmanagement nach ITIL v4

:::warning
➕ Lobenswert ist, dass du dich an alle Aufgaben inklusive der Zusatzaufgaben herangewagt hast.

➕ Deine Kriterien für die Störungsmeldung (P5) sind vollständig.

➖ Bei P2 beschreibst du Eskalation fehlerhaft: Eine hierarchische Eskalation beschleunigt die Bearbeitung nicht funktional, sondern holt Management-Entscheidungsträger (z.B. für Budget oder rechtliche Freigaben) ins Boot.  
➖ Bei P4 hast du das Kernkonzept komplett verdreht: Incident- und Problem-Management unterscheiden sich nicht durch "Verwaltung vs. Technik" (beide sind hochgradig technisch!), sondern durch "Schnelle Symptombehebung (Incident)" vs. "Nachhaltige Ursachenforschung (Problem)".
:::

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

**Als Support-Spezialist_in möchte ich Störungen (Incidents) systematisch bearbeiten, um den normalen Betriebszustand so schnell wie möglich wiederherzustellen.**

## ✅ Celebration Criteria (Lernziele)

- Ich kann den Begriff "Incident" nach ITIL v4 definieren. (K2)
- Ich kann Störungen nach Auswirkung und Dringlichkeit priorisieren. (K3)
- Ich kann den Unterschied zwischen einer Problem-Analyse und einer Störungsbehebung erläutern. (K2)

## ⚠️ Typische Fallstricke & Impulsfragen

- **Workaround-Falle:** Ein Provisorium wird zur Dauerlösung. -> _Impuls:_ Wann muss aus einer wiederkehrenden Störung ein "Problem" werden?
- **Mangelnde Kommunikation:** Der Techniker repariert, aber der User weiß nicht, wie lange es noch dauert. -> _Impuls:_ Was ist wichtiger: Die Reparaturzeit oder die Information über die Dauer?

## 🛠️ Pflichtaufgaben (Training)

1. Erstelle eine Priorisierungsmatrix für 5 Beispielfälle. (K3)
2. Beschreibe den Prozess der "Eskalation" (funktional vs. hierarchisch). (K2)
3. Dokumentiere einen simulierten Incident inklusive Workaround. (K3)
4. Erkläre das Ziel des Incident Managements im Vergleich zum Problem Management. (K2)
5. Liste die notwendigen Informationen für eine Störungsmeldung auf. (K3)

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

1. Untersuche die Rolle von Major Incidents und deren Krisenmanagement. (K4)
2. Entwickle ein Schema zur automatischen Zuweisung von Incidents an Fachgruppen. (K5)
3. Beurteile die Wichtigkeit einer Post-Incident-Review (PIR). (K6)

## 🔗 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann LF6:** Kapitel "Störungsmanagement".
- **Rheinwerk:** Kapitel "IT-Betrieb und Support".

### 🔍 Web (Suchwortliste)

- **Prozess:** `ITIL 4 Incident Management Workflow`
- **Analyse:** `Root Cause Analysis Methoden IT`

Dringlichkeit nach ITIL v4:

<div class="joplin-table-wrapper"><table style="min-width: 149px"><tbody><tr><th colspan="1" rowspan="1" colwidth="124" style="background-color: rgb(1, 59, 94)" data-background-color="rgb(1, 59, 94)"><p data-id="rlyxrfjhiadg">Kategorie</p></th><th colspan="1" rowspan="1" style="background-color: rgb(250, 204, 106)" data-background-color="rgb(250, 204, 106)"><p data-id="nisgrlqeokex">Beschreibung</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="ulkmivvecdtu"><strong>Hoch (H)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="kqbmiqcrwhih">Der von dem Incident verursachte Schaden nimmt im schnell zu.</p></li><li><p data-id="nuuhlluacaex">Die Aufgaben, die von den Mitarbeitern nicht erfüllt werden können, sind sehr zeitkritisch.</p></li><li><p data-id="hfwxzbrwgikx">Durch schnelles Handeln kann verhindert werden, dass aus einem Minor Incident ein Major Incident wird.</p></li><li><p data-id="povbrlogmmbi">Mehrere Benutzer mit VIP-Status sind betroffen.</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="hoxgxkvnlyuc"><strong>Mittel (M)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="idcphxxfguvx">Der von dem Incident verursachte Schaden nimmt im Verlauf der Zeit substantiell zu.</p></li><li><p data-id="xtobygancybl">Die Aufgaben, die von den Mitarbeitern nicht erfüllt werden können, sind nur mäßig zeitkritisch.</p></li><li><p data-id="felztgsvzjex">Ein einzelner Benutzer mit VIP-Status ist betroffen.</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="hawvpqwzhqcs"><strong>Niedrig (N)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="pavsiekghjec">Der von dem Incident verursachte Schaden nimmt im Verlauf der Zeit nur unwesentlich zu.</p></li><li><p data-id="guquzmrfhirz">Die Aufgaben, die von den Mitarbeitern nicht erfüllt werden können, sind nicht zeitkritisch.</p></li></ul></td></tr></tbody></table></div>

Auswirkung nach ITIL v4:

<div class="joplin-table-wrapper"><table style="min-width: 149px"><tbody><tr><th colspan="1" rowspan="1" colwidth="124" style="background-color: rgb(1, 59, 94)" data-background-color="rgb(1, 59, 94)"><p data-id="aclotssyrmsw">Kategorie</p></th><th colspan="1" rowspan="1" style="background-color: rgb(250, 204, 106)" data-background-color="rgb(250, 204, 106)"><p data-id="bulxhxytssvw">Beschreibung</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="loxixpxwjwjm"><strong>Hoch (H)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="botchnggotkk">Eine große Anzahl von Mitarbeitern ist betroffen und/oder kann ihre Aufgaben nicht erfüllen.</p></li><li><p data-id="qftmbdcktbvh">Eine große Anzahl von Kunden ist betroffen und/oder ist in irgendeiner Weise akuten Nachteilen ausgesetzt.</p></li><li><p data-id="bbrfoygqsqgc">Der finanzielle Schaden durch den Incident ist voraussichtlich höher als (zum Beispiel) 10.000 EUR.</p></li><li><p data-id="yjkjvavhgkdc">Eine Beschädigung der Reputation des Unternehmens in großem Umfang ist wahrscheinlich.</p></li><li><p data-id="jnsrtbtxsavj">Es besteht Gefahr für Leib und Leben.</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="qdtkrkpoineq"><strong>Mittel (M)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="mdedemrtmlvn">Eine mäßige Anzahl von Mitarbeitern ist betroffen und/oder kann ihre Aufgaben nicht wie vorgesehen erfüllen.</p></li><li><p data-id="abhrribwfirz">Eine mäßige Anzahl von Kunden ist betroffen und/oder erfährt Einschränkungen beim Komfort.</p></li><li><p data-id="balwcrlecvta">Der finanzielle Schaden durch den Incident liegt voraussichtlich zwischen (zum Beispiel) 1.000 EUR und 10.000 EUR.</p></li><li><p data-id="jaqhgbcuekmy">Eine Beschädigung der Reputation des Unternehmens in mäßigem Umfang ist wahrscheinlich.</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="124"><p data-id="nmwkhnxumkcy"><strong>Niedrig (N)</strong></p></td><td colspan="1" rowspan="1"><ul><li><p data-id="oixqfxtvysiw">Eine minimale Anzahl von Mitarbeitern ist betroffen und/oder kann ihre Aufgaben erfüllen, jedoch nur mit zusätzlichem Aufwand.</p></li><li><p data-id="tkazojjhxvmz">Eine minimale Anzahl von Kunden ist betroffen und/oder erfährt Einschränkungen beim Komfort, jedoch nur in geringem Umfang.</p></li><li><p data-id="eiarmudiohby">Der finanzielle Schaden durch den Incident ist voraussichtlich weniger als (zum Beispiel) 1.000 EUR.</p></li><li><p data-id="ezeunysdlksj">Eine Beschädigung der Reputation des Unternehmens ist nur in minimalem Umfang zu erwarten.</p></li></ul></td></tr></tbody></table></div>

</details>

## Lösungen

### P1: Erstelle eine Priorisierungsmatrix für 5 Beispielfälle. (K3)

Gemäß ITIL v4 sieht sie grundlegende Matrix wie folgt aus. Anhand ihr lassen sich dann die Priorisierungscodes (1-5) zuweisen.

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
|     |     | Auswirkung |     |     |
| Hoch | Mittel | Niedrig |
| Dringlichkeit | Hoch | 1   | 2   | 3   |
| Mittel | 2   | 3   | 4   |
| Niedrig | 3   | 4   | 5   |

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| Beispielfälle |     | Auswirkung |     |     |
| Hoch | Mittel | Niedrig |
| Dringlichkeit | Hoch | Ausfall einer kritischen Infrastruktur (bspw. Strom, Internetzugang) | Die Geschäftsleitung kann nicht auf die Präsentationsdaten zugreifen | 3   |
| Mittel | 2   | Es besteht kein Zugriff mehr auf den Netzwerkdrucker | 4   |
| Niedrig | 3   | Aus ungeklärten Gründen ist in einer Abteilung die Internetgeschwindigkeit extrem langsam | Wifi-Signal in der Cafeteria ist schwach/gestört |

---

### P2: Beschreibe den Prozess der "Eskalation" (funktional vs. hierarchisch). (K2)

Wenn ein Incident bzw. Vorfall “eskaliert” wird, so verschiebt sich seine Priorität schrittweise nach oben. ~~(hierarchisch) und wird somit (hoffentlich) schneller bearbeitet (funktional).~~

**Funktionale Eskalation** - horizontal nach oben, fachlich tiefer; hierbei geht es direkt um die funktionale Lösung des Incidents, indem fachspezifisch an eine qualifiziertere Stelle weitergegeben wird.

**Hierarchische Eskalation** - vertikal nach oben, managementseitig; hier wird der Vorfall nach oben im Bereich des Managements weitergeleitet, welches den Vorfall nicht direkt löst, sondern ggf. mehr Ressourcen freigeben kann, die zur Lösung beitragen.

---

### P3: Dokumentiere einen simulierten Incident inklusive Workaround. (K3)

1. Incident wird reported (via Mail oder Ticket-System):

“Das Internet in der Marketing-Abteilung ist extrem langsam.”

2. Incident wird entsprechend dokumentiert und anhand der Priority-Matrix eingestuft.
3. Bearbeitung des Incidents und Fehlersuche (Weiterleitung an Problem Management).
4. Workaround - mittels Switches werden essenzielle Systeme zunächst per Kabel angeschlossen.
5. Lösung des “lahmenden Wifis” gefunden und Problem behoben.
6. Ticket wird geschlossen und im Log abgelegt.

---

### P4: Erkläre das Ziel des Incident Managements im Vergleich zum Problem Management. (K2)

~~Das IM kümmert sich vorrangig um die Einstufung, Kategorisierung, Eskalation und Katalogisierung der Incidents/Anfragen, während das PM damit beauftragt ist die Probleme aus technischer Sicht zu lösen. Im Grunde also Verwaltung vs Technik.~~

Das IM bekämpft akute Symptome, während es beim PM um langfristige, ursächliche Lösungen geht.

---

### P5: Liste die notwendigen Informationen für eine Störungsmeldung auf. (K3)

- Datum: Beginn der Störung
- Ort
- Wer meldet? Wer ist betroffen?
- (geschätzte Dringlichkeit - Deadline?)
- Was ist gestört/funktioniert nicht? (CIs)
- Wurde zuvor schon mal gemeldet? Wiederholungsfall?

---

### Z1: Untersuche die Rolle von Major Incidents und deren Krisenmanagement. (K4)

**Kritisch** - hohe Priorität und/oder Aufwand. Spürbarer verursachter Schaden.

---

### Z2: Entwickle ein Schema zur automatischen Zuweisung von Incidents an Fachgruppen. (K5)

Dazu bedarf es zunächst einer umfangreichen Kategorisierung. Anschließend können Tickets dann automatisch zugewiesen werden.

---

### Z3: Beurteile die Wichtigkeit einer Post-Incident-Review (PIR). (K6)

Ist essenziell, um nachvollziehen zu können, ob die Stellen adäquat bzw. ausreichend besetzt sind; ob die SLAs eingehalten wurden; ob und wo es Verbesserungspotenziale gibt.