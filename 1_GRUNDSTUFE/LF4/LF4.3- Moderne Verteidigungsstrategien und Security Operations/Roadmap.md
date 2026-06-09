# Roadmap

# Strategische IT-Security Roadmap: KreativKopf GmbH

## 1\. Zero Trust & Cloud Security: „Vertrauen ist gut, Kontrolle ist besser“

Der Wechsel von lokalen Servern zu Anbietern wie Microsoft Azure oder AWS bedeutet, dass der klassische „Burggraben“ (die Firewall im Büro) nicht mehr ausreicht. Wir führen das **Zero-Trust-Prinzip** ein.

### Das Konzept: „Der VIP-Club-Check“

Stell dir vor, das Unternehmen ist ein exklusiver Club. Früher reichte es, einmal am Eingang den Ausweis zu zeigen. Bei **Zero Trust** steht vor _jeder_ Bar, _jeder_ Lounge und _jedem_ VIP-Bereich ein Türsteher, der dich erneut fragt: „Wer bist du und darfst du das wirklich?“

- **Always Verify (MFA):** Ohne Multi-Faktor-Authentifizierung kommt niemand rein. Ein Passwort allein ist heute so sicher wie ein Haustürschlüssel, der unter der Fußmatte liegt.
- **Assume Breach:** Wir arbeiten so, als wäre bereits ein Angreifer im System. Sensible Daten werden einzeln verschlüsselt und das Netzwerk in kleine, isolierte Räume unterteilt (Segmentierung).
- **Least Privilege:** Jeder Mitarbeiter erhält nur so viele Rechte, wie er für seine aktuelle Aufgabe unbedingt benötigt. Wer nur Texte schreibt, braucht keinen Zugriff auf die Buchhaltung.
- **Shared Responsibility Model:**
  - **Der Anbieter (AWS/Azure):** Ist verantwortlich für die „Sicherheit **der** Cloud“ (Hardware, Rechenzentren, Strom).
  - **KreativKopf GmbH:** Wir sind verantwortlich für die „Sicherheit **in** der Cloud“ (unsere Daten, die Rechteverwaltung und die Konfiguration).¹

---

## 2\. Moderne Bedrohungen: Supply-Chain & KI-Angriffe

Die Professionalität der Angreifer steigt. Wir müssen verstehen, dass Gefahren oft „durch die Hintertür“ kommen.

### Supply-Chain-Angriffe: „Die vergiftete Zutat“

Stell dir vor, du backst einen Kuchen und kaufst dafür Mehl von einem vertrauenswürdigen Bio-Händler. Wenn dieser Händler jedoch (ohne es zu wissen) giftiges Mehl liefert, ist dein ganzer Kuchen ruiniert.

- **Lösung:** Wir führen eine **SBOM (Software Bill of Materials)**. Das ist wie eine Zutatenliste für unsere Software. Wir prüfen regelmäßig über Datenbanken wie [CVE Details](https://www.cvedetails.com/) oder [OSV.dev](https://osv.dev/list), ob unsere „Zutaten“ (Open-Source-Bibliotheken) noch sicher sind.

### KI-gestütztes Social Engineering

Angreifer nutzen KI, um täuschend echte E-Mails oder sogar Stimmen (Deepfakes) zu imitieren.

- **Lösung:** Wir etablieren ein internes **„Codewort-System“** für ungewöhnliche Anfragen (z. B. schnelle Überweisungen durch den Chef – „CEO Fraud“).

---

## 3\. Security Culture: „Security als KreativKopf“

Sicherheit ist kein reines IT-Thema, sondern Teil unserer Unternehmenskultur. Wir wollen weg von trockenen Pflichtschulungen hin zu echter Begeisterung.

|     |     |     |
| --- | --- | --- |
| **Maßnahme** | **Beschreibung** | **Ziel** |
| **Gamification** | Monatliche, harmlose Phishing-Simulationen. Wer sie erkennt, sammelt Punkte für sein Team. | Spielerisches Lernen & Aufmerksamkeit |
| **Sicherheitshelden** | Wer einen echten Betrugsversuch meldet, wird im internen Newsletter als „Held der Woche“ gefeiert. | Positive Verstärkung statt Angst |
| **Micro-Learnings** | 5-Minuten-Häppchen in der Kaffeepause via App statt 4-Stunden-Vortrag. | Nachhaltige Wissensvermittlung |