# LF6.4.3: Wissensmanagement (KCS)

<details>
<summary>Briefing</summary>

## 👤 User Story

> Als Knowledge-Manager\*in  
> möchte ich eine Wissensbasis aufbauen und pflegen,  
> damit bekannte Lösungen schnell geteilt werden und das Team nicht jedes Problem neu lösen muss.

## 🎉 Celebration Criteria (Lernziele)

- Ich kann das Prinzip von KCS (Knowledge Centered Service) **erläutern**. (K2)
- Ich kann strukturierte Knowledge-Base-Artikel (FAQ) nach dem Problem-Lösung-Schema **erstellen**. (K3)
- Ich kann Informationen durch Metadaten (Tags) für eine bessere Suche **klassifizieren**. (K3)

## 🧠 Wissens-Briefing

KCS ist eine Methode, bei der die Dokumentation direkt während der Ticketbearbeitung entsteht.

- **UFFA-Prinzip:** Use it, Flag it, Fix it, Add it.
- **Struktur:** Ein guter Artikel braucht: 1. Klaren Titel, 2. Symptombeschreibung, 3. Ursache, 4. Lösungsschritte.

## ⚠️ Typische Fallstricke & Impulsfragen

- **Informationsfriedhof:** Es gibt 1000 Artikel, aber keiner findet etwas. -> _Impuls:_ Wie wichtig ist eine gute Suchfunktion und Verschlagwortung?
- **Veraltetes Wissen:** Die Anleitung gilt für Ubuntu 18.04, wir nutzen aber 24.04. -> _Impuls:_ Wer ist für die Aktualisierung der Artikel verantwortlich?

## 🛠️ Pflichtaufgaben (K1-K3)

1. Erstelle einen FAQ-Artikel für den "Unattended Linux Install" (aus LF6.2). (K3)
2. Definiere ein Tagging-System (Schlagworte) für Hardware-Probleme in deinem Szenario. (K3)
3. Überführe eine informelle E-Mail-Anleitung eines Kollegen in einen strukturierten Wiki-Eintrag. (K3)
4. Erkläre den Unterschied zwischen internem Wissen (für Techniker) und externem Wissen (für Endanwender). (K2)
5. Beschreibe den "Review-Prozess": Wann muss ein Artikel gelöscht oder überarbeitet werden? (K2)

## ⭐ Freiwillige Zusatzaufgaben (K4-K6)

1. Recherchiere, wie KI (z.B. LLMs) dabei helfen kann, aus alten Ticket-Lösungstexten automatisch Wiki-Artikel zu generieren. (K4)
2. Evaluiere verschiedene Wiki-Tools (DokuWiki, BookStack, Confluence) für ein kleines Startup. (K6)

### 🔍 Web (Suchwortliste)

- **Methodik:** `KCS Methodology Introduction Guide`
- **Struktur:** `Struktur von Knowledge Base Artikeln Vorlage`

</details>

## Lösungen

### Pflichtaufgaben

### P1: Erstelle einen FAQ-Artikel für den "Unattended Linux Install" (aus LF6.2). (K3)

**_To-Do_**

---

### P2: Definiere ein Tagging-System (Schlagworte) für Hardware-Probleme in deinem Szenario. (K3)

**Analogie:** Tags sind wie Etiketten in einer gut sortierten Werkzeugkiste.

| Kategorie | Tags |
| --- | --- |
| **Geräteart** | `laptop`, `desktop`, `drucker`, `monitor`, `server`, `switch` |
| **Hersteller** | `lenovo`, `hp`, `dell`, `canon`, `logitech` |
| **Problem-Typ** | `kein_strom`, `kein_display`, `überhitzung`, `kein_boot`, `doa` |
| **Status** | `in_reparatur`, `garantiefall`, `austausch_nötig`, `gelöst` |
| **Priorität** | `kritisch`, `hoch`, `normal`, `niedrig` |
| **Zielgruppe** | `end_user`, `admin`, `management` |

**Empfehlung:** Maximal 8 Tags pro Artikel. Tags immer in Kleinbuchstaben, mit Underscore “\_” (→ Snake-Case) statt Leerzeichen.

---

### P3: Überführe eine informelle E-Mail-Anleitung eines Kollegen in einen strukturierten Wiki-Eintrag. (K3)

**E-Mail:** _"Hey, wenn der Drucker mal wieder spinnt und nichts druckt, einfach den Spooler-Dienst neu starten: Services öffnen, Print Spooler suchen, rechtsklick, Neustarten. Dann löppt’s wieder. LG, Klaus"_

---

**Wiki-Artikel:**

**Titel:** Druckerwarteschlange hängt - Print Spooler neu starten (Windows)

**Symptom:** Der Drucker nimmt Druckaufträge an, druckt aber nicht. Die Warteschlange ist blockiert, Aufträge lassen sich nicht löschen.

**Ursache:** Der Windows-Dienst "Druckwarteschlange" (Print Spooler) ist eingefroren oder in einem Fehlerzustand.

**Lösung:**

_Methode 1 – Über die Dienste-Verwaltung (empfohlen):_

1. `Win + R` → `services.msc` → Enter
2. Dienst **"Druckwarteschlange"** suchen
3. Rechtsklick → **"Neu starten"**
4. Druckauftrag erneut senden

_Methode 2 – Per Kommandozeile (Admin):_

In cmd: `net stop spooler` → `net start spooler`  

**Hinweis:** Falls das Problem regelmäßig auftritt, Ticket mit Tag `drucker`, `spooler`, `wiederkehrend` erstellen.

**Tags:** `drucker`, `spooler`, `windows`, `warteschlange`, `end_user`

**Schwierigkeitsgrad:** Einfach

**Autor:** Klaus M. (überführt durch: Philipp S.)

---

### P4: Erkläre den Unterschied zwischen internem Wissen (für Techniker) und externem Wissen (für Endanwender). (K2)

**Analogie:** Interne Dokumente sind wie die Notizen eines Arztes in der Akte. Externe Dokumente sind wie der Beipackzettel: Für den Patienten geschrieben, klar und möglichst ohne Fachbegriffe.

Beispielhaft:

| Kriterium | Internes Wissen (für Techniker) | Externes Wissen (für Endanwender) |
| --- | --- | --- |
| **Zielgruppe** | IT-Fachpersonal | Mitarbeiter ohne IT-Kenntnisse |
| **Sprache** | Fachbegriffe erlaubt | Einfache, klare Sprache |
| **Detailtiefe** | Hoch (Befehle, Logs, Konfigurationen) | Niedrig (Schritt-für-Schritt, Screenshots) |
| **Beispiel** | `sudo systemctl restart networking` | "Klicken Sie auf das WLAN-Symbol unten rechts" |
| **Zugang** | Nur intern / VPN | Intranet / Self-Service-Portal |

**Fazit:** Eine gute Knowledge Base trennt diese Wissenstypen klar durch eigene Bereiche oder Rollen-Filterung.

---

### P5: Beschreibe den "Review-Prozess": Wann muss ein Artikel gelöscht oder überarbeitet werden? (K2)

**Analogie:** Durch neue wissenschaftliche Erkenntnisse ändern sich zuvor angenommene/etablierte “Wahrheiten”. Genauso veralten/verdummen Wiki-Artikel, ohne Review sind sie Fehlerquellen.

| Auslöser | Maßnahme |
| --- | --- |
| **Zeitbasiert** | Jeder Artikel wird alle 6 Monate automatisch zur Überprüfung markiert |
| **Ereignisbasiert** | Nach System-Updates oder Versionswechseln sofort prüfen |
| **Nutzerfeedback** | "War dieser Artikel hilfreich?" → Nein löst Review-Flag aus |
| **Ticket-basiert** | Wenn ein Fall nicht durch bestehende Artikel abgedeckt ist → neuer Artikel |

**Wann löschen?** Das beschriebene System wird nicht mehr genutzt, der Artikel ist seit 12 Monaten ungenutzt, oder ein aktuellerer Artikel deckt denselben Inhalt ab.

**Wann überarbeiten?** Software-Version hat sich geändert, Screenshots sind veraltet, oder Nutzerfeedback zeigt Verwirrung.

**Verantwortlichkeit:** Jeder Artikel hat einen benannten **Owner**. Der Knowledge Manager überwacht den Gesamtbestand quartalsweise.

---

### Zusatzaufgaben

### Z1: Recherchiere, wie KI (z.B. LLMs) dabei helfen kann, aus alten Ticket-Lösungstexten automatisch Wiki-Artikel zu generieren. (K4)

LLMs können, mit den richtigen Prompts, aus dem Freitext eines Ticket-Abschlussberichts automatisch einen strukturierten Wiki-Artikel generieren.

**Workflow:**

:::note
Ticket abgeschlossen → Lösungstext aus Ticket extrahieren → LLM-Prompt: "Erstelle Artikel nach Schema x: Titel / Symptom / Ursache / Lösung / Tags” → Entwurf wird Techniker zur Freigabe vorgelegt → Freigabe → Artikel in Wissensbasis veröffentlicht
:::

**Vorteile:** Reduziert manuellen Aufwand, kein Wissen geht verloren, skalierbar.

**Risiken:** KI kann Lösungsschritte falsch zusammenfassen → daher menschliche Freigabe = Pflicht.

---

### Z2: Evaluiere verschiedene Wiki-Tools (DokuWiki, BookStack, Confluence) für ein kleines Startup. (K6)

| Kriterium | DokuWiki | BookStack | Confluence |
| --- | --- | --- | --- |
| **Kosten** | Kostenlos, Open Source | Kostenlos, Open Source | Kostenpflichtig |
| **Installation** | Einfach (PHP, keine DB) | Mittel (Laravel/PHP) | Komplex (Cloud oder Server) |
| **Struktur** | Dateibasiert | Buch → Kapitel → Seiten | Spaces → Pages |
| **Suche** | Gut | Sehr gut | Sehr gut |
| **Eignung Startup** | Ideal (leichtgewichtig) | Sehr gut | Overkill und teuer |
| **LDAP/SSO** | Plugin nötig | Eingebaut | Eingebaut |

**Empfehlung für kleines Startup:** **_BookStack_** → modernes UI, einfache Struktur, kostenlos und ausreichend skalierbar.