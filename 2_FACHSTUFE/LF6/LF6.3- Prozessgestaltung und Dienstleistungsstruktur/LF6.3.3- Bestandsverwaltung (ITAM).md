# LF6.3.3- Bestandsverwaltung (ITAM)

:::success
➕ Du hast eine sehr solide und sauber strukturierte Arbeit abgeliefert. Die logische Trennung der Monitor-Attribute in kaufmännische und technische Sicht (P1) hast du hervorragend dargestellt. Deine Probe-Inventur (P3) ist übersichtlich und absolut praxisnah. Auch deine Zusatzaufgaben (Z1–Z3) zeigen ein sehr gutes Verständnis für den gesamten Asset-Lebenszyklus, insbesondere deine prägnante Analyse zum QR-Code-Tracking.

💡 Kleiner Tipp für die Fachsprache: Du hast bei P1 den Begriff "TOC-Prognose" verwendet – üblicher und fachlich korrekt ist hier die Abkürzung **TCO** (Total Cost of Ownership).

_Diese Rückmeldung wurde automatisiert erstellt._
:::

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

**Als Bestandsverwalter_in möchte ich das IT-Asset-Management (ITAM) Modell nutzen, um eine lückenlose Übersicht aller IT-Werte zu gewährleisten.**

## ✅ Celebration Criteria (Lernziele)

- Ich kann den Zweck von ITAM innerhalb der IT-Organisation beschreiben. (K2)
- Ich kann ein Inventarisierungsschema für verschiedene Asset-Typen entwickeln. (K3)
- Ich kann den Zusammenhang zwischen ITAM und Finanzbuchhaltung erläutern. (K2)

## 🧠 Wissens-Briefing

- **ITAM:** IT Asset Management konzentriert sich auf den geschäftlichen Wert und die kaufmännische Verwaltung von Hardware und Software.
- **Ziele:** Kostenkontrolle, Compliance (Lizenzen), Risikomanagement.

## ⚠️ Typische Fallstricke & Impulsfragen

- **Schatten-IT:** Geräte werden am ITAM vorbei beschafft. -> _Impuls:_ Wie können wir sicherstellen, dass jedes neue Gerät erfasst wird?
- **Asset vs. CI Verwechslung:** Kaufmännische Daten (Preis, Garantie) werden mit technischen Details (IP-Adresse, CPU) vermischt. -> _Impuls:_ Warum sollten diese Daten logisch getrennt, aber verknüpft sein?

## 🛠️ Pflichtaufgaben (Training)

1. Erstelle eine Liste von Attributen, die für ein Asset (z. B. Monitor) in der CMDB gespeichert werden müssen. (K3)
2. Erkläre den Unterschied zwischen einem Asset (kaufmännisch) und einem Configuration Item (technisch). (K2)
3. Führe eine Probe-Inventur von 5 Gegenständen im Raum durch. (K3)
4. Beschreibe den Prozess eines "Asset-Audits". (K2)
5. Erläutere, warum Lizenzmanagement ein Teil von ITAM ist. (K2)

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

1. Entwirf einen Prozess für den Umgang mit "verlorenen" Assets. (K5)
2. Analysiere Tools für automatisiertes Asset-Discovery im Netzwerk. (K4)
3. Evaluiere die Vorteile von QR-Code-basiertem Asset-Tracking. (K6)

## 🔗 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann LF6:** LS 3 "Serviceanfragen entgegennehmen und bearbeiten".
- **Rheinwerk:** Kapitel "Lizenzmanagement und Compliance".

### 🔍 Web (Suchwortliste)

- **Best Practices:** `IT Asset Management Framework`
- **Inventur:** `Hardware Inventarisierung Best Practices`

</details>

# Lösungen

## Pflichtaufgaben (Training)

### P1: Erstelle eine Liste von Attributen, die für ein Asset (z. B. Monitor) in der CMDB gespeichert werden müssen. (K3)

| Asset/Item | Kaufmännisches Attribut | Technisches Attribut (CI) |
| --- | --- | --- |
| Monitor | Kaufdatum | CMDB-ID (u.U. auch Aufkleber mit QR- oder BarCode) |
| Datum d. Inbetriebnahme | Technischer Zustand |
| Garantiezeit | Datum d. letzten techn. Prüfung |
| TOC-Prognose | Standort, Verwendungszweck |

---

### P2: Erkläre den Unterschied zwischen einem Asset (kaufmännisch) und einem Configuration Item (technisch). (K2)

Ein kaufmännisches Asset fokussiert sich eher auf den monetären Wert eines Objektes oder Prozesses, während ein Configuration Item die technischen Daten hinterlegt. Natürlich gibt es auch hier bereichsübergreifende Schnittstellen, die eine eindeutige Zuordnung nicht garantieren. Bspw. der Verwendungszweck ist für beide Seiten relevant.

---

### P3: Führe eine Probe-Inventur von 5 Gegenständen im Raum durch. (K3)

Eine Inventur dient zur schnellen Übersicht der aktuellen Lage bzw. des “Inventars”. Daher in der folgenden Tabelle nur die wichtigsten Daten zur Identifizierung. In einem geschlossenen Software-System könnte man Details zu den einzelnen Posten bspw. in deren Beschreibung (Modell) per Hyperlink einfügen/verlinken.

| Inventur-Nummer | Bezeichnung (Modell) | Typ/Art | Asset-ID | Seriennummer | Standort | Zustand |
| --- | --- | --- | --- | --- | --- | --- |
| 1   | SOLAKAKA E9Pro | Ergonomische Maus | 2026-003 | Derzeit nicht einsehbar | Schönefeld | einwandfrei / neu |
| 2   | Corsair K55 | Tastatur | 2022-002 | 018921179143 | Schönefeld | gebraucht (i.O.) |
| 3   | Sennheiser G ONE | Stereo-Headset | 2018-001 | Derzeit nicht einsehbar | Schönefeld | gebraucht (mangelhaft) |
| 4   | LG Ultragear | Monitor | 2024-001 | 813218746247 | Schönefeld | gebraucht (gut) |
| 5   | IT-Handbuch | Literatur | 2025-004 | 10672 | Schönefeld | gebraucht (nahezu unbenutzt) |

---

### P4: Beschreibe den Prozess eines "Asset-Audits". (K2)

Hierbei geht es um die Überprüfung und Verifikation zwischen Systemen (Soll-Zustand) und der tatsächlichen Lage (Ist-Zustand). Dieser Prozess hilft dabei Lücken und Probleme zu identifizieren, sowie möglichen Diebstahl oder die Nutzung sog. “Schatten-IT”-Items (undokumentierte Systeme) aufzudecken.  
Ein “Asset-Audit” muss man natürlich zunächst **planen**, dann **durchführen** und zuletzt **nachbereiten**.

---

### P5: Erläutere, warum Lizenzmanagement ein Teil von ITAM ist. (K2)

Lizenzmanagement ist ein essenzieller Teil von ITAM, damit das Risiko von Lizenzverletzungen minimiert werden kann. Sind Lizenzen nicht Bestandteil des ITAMs, so läuft man Gefahr einerseits den Überblick zu verlieren und andererseits “aus Versehen” mehr Lizenzen nutzen (zu wollen) als vertraglich festgelegt sind. Oder auch andersherum sinnhaft und auf einen Blick deutlich machen kann, wie viele Lizenzen überhaupt notwendig sind. Also anhand der Anzahl der verfügbaren Hardware und Arbeitsplätze.

---

## ⭐ Freiwillige Zusatzaufgaben (Expertise)

### Z1: Entwirf einen Prozess für den Umgang mit "verlorenen" Assets. (K5)

Wenn wir anhand eines Asset-Audits “verlorene” Assets festgestellt haben, bedarf es einer Aufklärung in der Nachbereitungsphase. Ausgangspunkt und wichtigstes Hilfsmittel sind entsprechende Audit-Logs in unserem ITAM-System. Im besten Fall können wir hier die letzte Aktualisierung als Startpunkt der Investigation nehmen. Anhand der letzten Aktion, bzw. des zuletzt bekannten Ortes und der zugewiesenen Person, können wir zumindest einen Anhaltspunkt gewinnen, wo das Verlorengehen seinen Lauf genommen hat.  
Ungeachtet des Ergebnisses unserer Investigation muss anschließend unbedingt der Status des Assets entsprechend aktualisiert werden.

---

### Z2: Analysiere Tools für automatisiertes Asset-Discovery im Netzwerk. (K4)

Grundlegend gibt es hierfür wohl 2 Varianten: Agentenbasiertes Suchsystem und agenten-loses Suchsystem per Netzwerk-Scan. Pauschal würde ich ein agenten-loses System zunächst vorziehen, da hierzu nicht auf jedem System der Agent installiert sein muss und er auch funktioniert. Daher scheint ein Netzwerk-Scan geringere Anforderungen an die Sub-Systeme zu haben und bietet somit einen Vorteil. Für welches System oder welche Software man sich letztlich entscheidet ist am jeweiligen Anwendungszweck auszumachen (Was brauche ich und wofür?). Aus meiner Laiensicht scheint ein “smartes” System, bei dem ich lediglich zunächst nur die Seriennummer eingeben oder scannen muss, um das Produkt aufzunehmen und anschließend per Netzwerk-Scan dessen Status angepasst werden als sinnvoll.

---

### Z3: Evaluiere die Vorteile von QR-Code-basiertem Asset-Tracking. (K6)

Kleiner Mehraufwand beim erstmaligen Loggen, aber erhebliche Ersparnis im Bezug auf Arbeitsaufwand und Zeit während des Betriebs und Audits, sowie eine erhöhte Präzision durch das Vermeiden von eventuellen Tipp- oder Kategorisierungsfehlern, o.ä.. Natürlich muss bei der erstmaligen Einrichtung alles stimmen, damit besagt Fehler im Anschluss vermieden werden können.