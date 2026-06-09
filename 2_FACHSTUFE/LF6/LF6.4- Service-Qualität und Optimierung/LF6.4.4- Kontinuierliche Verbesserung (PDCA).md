# LF6.4.4: Kontinuierliche Verbesserung (PDCA)

<details>
<summary>Briefing</summary>

## 👤 User Story

> Als Qualitätsverantwortliche\*r  
> möchte ich den PDCA-Zyklus anwenden,  
> um Schwachstellen im Service-Prozess systematisch zu beheben und die Qualität dauerhaft zu steigern.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann die vier Phasen des PDCA-Zyklus (Plan-Do-Check-Act) **erläutern**. (K2)
- Ich kann ein Ishikawa-Diagramm (Ursache-Wirkung) zur Fehleranalyse **erstellen**. (K3)
- Ich kann aus einer Fehleranalyse konkrete Verbesserungsmaßnahmen **ableiten**. (K3)

## 🧠 Wissens-Briefing

- **Plan:** Problem identifizieren, Ziel definieren, Maßnahmen planen.
- **Do:** Maßnahmen im kleinen Rahmen testen (Pilotierung).
- **Check:** Ergebnisse messen und mit den Zielen vergleichen.
- **Act:** Wenn erfolgreich: Standardisieren. Wenn nicht: Neuer Zyklus.
- **Ishikawa (Fischgräte):** Systematische Suche nach Ursachen in den Kategorien Mensch, Maschine, Methode, Material, Mitwelt.

## ⚠️ Typische Fallstricke & Impulsfragen

- **Symptombekämpfung:** Man behebt nur die Wirkung, nicht die Ursache. -> _Impuls:_ Wie tief muss man graben (5-Why-Methode)?
- **Fehlendes "Check":** Maßnahmen werden eingeführt, aber nie auf Erfolg geprüft. -> _Impuls:_ Warum scheitern KVP-Initiativen oft nach der "Do"-Phase?

## 🛠️ Pflichtaufgaben (K1-K3)

1. Wende den PDCA-Zyklus auf das Problem "Zu viele Rückfragen bei Hardware-Bestellungen" an. (K3)
2. Zeichne ein Ishikawa-Diagramm für das Problem "Deployment der Linux-Rechner bricht oft ab". (K3)
3. Erstelle einen Maßnahmenplan (Wer, Was, Bis wann?) für eine der gefundenen Ursachen. (K3)
4. Erkläre den Unterschied zwischen einer Korrektur (kurzfristig) und einer Korrekturmaßnahme (nachhaltig). (K2)
5. Definiere, wie man im Schritt "Check" den Erfolg einer Kommunikationsschulung messen könnte. (K3)

## ⭐ Freiwillige Zusatzaufgaben (K4-K6)

1. Recherchiere den **DMAIC-Zyklus** (Six Sigma) und vergleiche ihn mit PDCA. (K4)
2. Beurteile: Warum scheitern viele KVP-Initiativen in der Praxis? (Fehlerkultur). (K6)

### 🔍 Web (Suchwortliste)

- **Prozess:** `PDCA Zyklus ITIL einfach erklärt`
- **Analyse:** `Ishikawa Diagramm Anleitung Fischgräte`

</details>

# Lösungen

## Pflichtaufgaben

### P1: Wende den PDCA-Zyklus auf das Problem "Zu viele Rückfragen bei Hardware-Bestellungen" an. (K3)

**Analogie:** PDCA ist wie das Perfektionieren eines Rezepts. Erst planen, dann kochen im Kleinen, dann probieren, dann entscheiden, ob man es so behältst oder (nochmal) anpasst.

| Phase | Inhalt |
| --- | --- |
| **P.lan** | **Problem:** Besteller stellen nach Hardware-Bestellungen im Schnitt 3-4 Rückfragen. **Ursache (vermutet):** Bestellformular ist unklar, keine Pflichtfelder, keine Hinweise auf Lieferzeiten. **Ziel:** Rückfragen um 60 % reduzieren in 8 Wochen. **Maßnahme:** Überarbeitung des Bestellformulars mit Pflichtfeldern, Tooltips und automatischer Bestätigungs-Mail. |
| **D.o** | **Pilottest:** Neues Formular wird in einer Abteilung (z. B. Vertrieb, 10 Personen) für 4 Wochen eingesetzt. Ticketvolumen und Rückfragen werden gezählt. |
| **C.heck** | **Vergleich:** Rückfragen vor Pilottest (Ø 3,5 / Bestellung) vs. nach Pilottest (Ø 1,1 / Bestellung). Ziel fast erreicht (68 % Reduktion). Negatives Feedback: Tooltip zur Lieferzeit war unverständlich. |
| **A.ct** | Formular/Tooltip wird angepasst und unternehmensweit **ausgerollt**. Neue Baseline für Rückfragenquote wird ins Dashboard aufgenommen. |

---

### P2: Zeichne ein Ishikawa-Diagramm (Ursache-Wirkungs-Diagramm) für das Problem "Deployment der Linux-Rechner bricht oft ab". (K3)

![diagram.drawio.svg](files/019da9c9-b924-76b7-af43-1018556da48c/diagram.drawio.svg?t=1776670063084)

---

### P3: Erstelle einen Maßnahmenplan (Wer, Was, Bis wann?) für eine der gefundenen Ursachen. (K3)

**Ursache:** Veraltetes Preseed-Image

| ID  | Maßnahme | Verantwortlich | Frist | Erfolgskontrolle |
| --- | --- | --- | --- | --- |
| 1   | Aktuelles Ubuntu-ISO herunterladen und Preseed-Datei aktualisieren | Max | 25.04.2026 | Neue Datei in Versionskontrolle eingecheckt |
| 2   | Testlauf auf 3 Referenz-Geräten | Max & Moritz | 30.04.2026 | Alle 3 Deployments erfolgreich |
| 3   | Dokumentation in Knowledge Base aktualisieren | Luisa | 02.05.2026 | Wiki-Artikel "Unattended Install" aktualisiert |
| 4   | Altes Image aus PXE-Server entfernen | Max | 02.05.2026 | PXE-Menü zeigt nur neue Version |
| 5   | Ergebnis im Weekly vorstellen | Team-Lead | 05.05.2026 | Abbruchrate der Woche ≤ 5 % |

---

### P4: Erkläre den Unterschied zwischen einer Korrektur (kurzfristig) und einer Korrekturmaßnahme (nachhaltig). (K2)

**Analogie:** Eine Korrektur ist wie ein Pflaster auf einer Wunde. Die Korrekturmaßnahme ist die Operation, die das Problem _dauerhaft_ heilt.

|     | Korrektur | Korrekturmaßnahme |
| --- | --- | --- |
| **Definition** | Sofortige Behebung der Auswirkung | Nachhaltige Beseitigung der Ursache |
| **Zeitraum** | Kurzfristig (Sofortmaßnahme) | Mittel- bis langfristig |
| **Beispiel Deployment** | Deployment manuell neu starten | Retry-Mechanismus ins Skript einbauen |
| **Beispiel Drucker** | Print Spooler neu starten | Treiber-Update ausrollen, das Einfrieren verhindert |
| **Wirkung** | Symptom verschwindet vorübergehend | Problem tritt nicht mehr auf |

**Fazit:** Korrektur = _Feuerlöschen_. Korrekturmaßnahme = _Brandschutzanlage installieren_.

---

### P5: Definiere, wie man im Schritt "Check" den Erfolg einer Kommunikationsschulung messen könnte. (K3)

**Analogie:** Messen bedeutet hier: Wirkung prüfen, nicht Aktivität.

| Messung | Methode | Zielwert |
| --- | --- | --- |
| **CSAT vor/nach Schulung** | Kundenzufriedenheitsumfragen vergleichen | Anstieg um >= 0,5 Punkte |
| **Eskalationsrate** | Eskalierte Tickets vor/nach Schulung zählen | Reduktion um >= 20% |
| **Erstlösungsrate** | First Fix Rate vor/nach Schulung | Anstieg um >= 10% |
| **Teilnehmer-Feedback** | Umfrage direkt nach Schulung | \>= 80% Zufriedenheit |
| **Mystery Call** | Supervisor bewertet echte Gespräche nach Kriterien | \>= 80% erfüllen Standard |

**Zeitplan:** Messung direkt nach Schulung (_Feedback_) → nach 4 Wochen (_Verhalten_) → nach 8 Wochen (_Ergebnis_).

---

## Freiwillige Aufgaben

### Z1: Recherchiere den **DMAIC-Zyklus** (Six Sigma) und vergleiche ihn mit PDCA. (K4)

| Kriterium | PDCA | DMAIC (Six Sigma) |
| --- | --- | --- |
| **Phasen** | Plan - Do - Check - Act | Define - Measure - Analyze - Improve - Control |
| **Fokus** | Kontinuierliche Verbesserung, iterativ | Fehlereliminierung, datengetrieben |
| **Datenbedarf** | Gering bis mittel | Hoch (statistische Analyse nötig) |
| **Aufwand** | Niedrig, schnell einsetzbar | Hoch, Experten nötig |
| **Eignung IT-Alltag** | Gut geeignet | Overkill für kleine Prozesse |

**Fazit:** **PDCA** = pragmatischer Einstieg | **DMAIC** = datengetriebener Tiefgang. Für den IT-Alltag scheint PDCA ausreichend; DMAIC lohnt sich wohl eher bei hartnäckigen, messbaren Qualitätsproblemen, die einen analytischen Tiefgang bedürfen.

---

### Z2: Beurteile: Warum scheitern viele KVP-Initiativen ([Kontinuierlicher Verbesserungsprozess](https://de.wikipedia.org/wiki/Kontinuierlicher_Verbesserungsprozess)) in der Praxis? (Fehlerkultur). (K6)

**Analogie:** Ein Fitnessprogramm scheitert selten am Plan, sondern am Umsetzen - fehlende Zeit, keine Motivation, kein Feedback.

| Ursache | Erklärung |
| --- | --- |
| **Fehlende Führungsunterstützung** | KVP wird als "Projekt der Qualitätsabteilung" gesehen, nicht als Chefsache |
| **Angst vor Fehlern** | In Kulturen, wo Fehler bestraft werden, werden Probleme oftmals versteckt statt gemeldet |
| **Fehlende Zeit** | Mitarbeiter sollen KVP betreiben, haben aber keine Kapazität neben dem Tagesgeschäft |
| **Keine Rückmeldung** | Verbesserungsvorschläge verschwinden in Schubladen → Demotivation |
| **Fehlender "Check"** | Maßnahmen werden eingeführt, aber nicht auf Wirkung geprüft |

**Mögliche Lösung:** Teams, die Fehler offen besprechen können, verbessern sich schneller. KVP braucht **Fehlerkultur, keine Schuldkultur**.