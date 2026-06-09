# LF6.2.3- Identitäts- und Zugriffsberechtigung

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

> _Als Identitäts-Administrator\*in_  
> _möchte ich Benutzerkonten lokal und in Verzeichnisdiensten verwalten,_  
> _damit der Zugriff auf Ressourcen sicher und nachvollziehbar gesteuert wird._

## 🎉 Celebration Criteria (Lernziele)

- Ich kann lokale Benutzer und Gruppen unter Linux und Windows (VM) konfigurieren. (K3)
- Ich kann die Funktion und den Aufbau von Verzeichnisdiensten wie OpenLDAP beschreiben. (K2)
- Ich kann lokale Benutzerverwaltung mit zentralen Lösungen (AD / Entra ID) vergleichen. (K4)

## 🧠 Wissens-Briefing

| Konzept | Erklärung & Relevanz |
| --- | --- |
| **Lokal vs. Zentral** | Lokal: Benutzer existiert nur auf einem Gerät. Zentral: Benutzer existiert im Netzwerk (Verzeichnisdienst) und kann sich an jedem Gerät anmelden. |
| **OpenLDAP** | Ein quelloffener Verzeichnisdienst (Lightweight Directory Access Protocol). Standard in der Linux-Welt. |
| **Active Directory (AD)** | Microsofts klassischer Verzeichnisdienst für lokale Netzwerke (Domänen). |
| **RBAC** | _Role-Based Access Control_. Berechtigungen werden nicht Personen, sondern Rollen (Gruppen) zugewiesen. |

## ⚠️ Typische Fallstricke & Impulsfragen

- **Verwaiste Konten:** Mitarbeiter verlässt die Firma, das Konto bleibt aktiv. -> _Impuls:_ Wie stellen wir sicher, dass beim Ausscheiden alle Zugänge (Lokal & SaaS) gesperrt werden?
- **Passwort-Sharing:** Nutzer geben Passwörter weiter. -> _Impuls:_ Welche technischen Maßnahmen (außer Verboten) helfen dagegen?

## 🛠️ Pflichtaufgaben (Bloom K2 & K3)

1. **Lokale Gruppenverwaltung:** Erstellt unter Linux zwei Gruppen (`vertrieb`, `technik`) und fügt Testnutzer hinzu. Testet den Zugriff auf einen gemeinsamen Ordner. (K3)
2. **OpenLDAP Struktur:** Zeichnet einen Verzeichnisbaum (DIT) für euer Szenario mit Organisationseinheiten (OUs) für Benutzer und Gruppen. (K3)
3. **Rechtevergabe (Windows):** Erstellt in eurer Windows-VM zwei Ordner und konfiguriert die NTFS-Rechte so, dass Gruppe A nur lesen und Gruppe B schreiben darf. (K3)
4. **Vergleichstabelle:** Erstellt eine Tabelle, die lokale Benutzerverwaltung, OpenLDAP und Entra ID gegenüberstellt (Vorteile/Nachteile). (K4)
5. **Sudo-Berechtigungen:** Erlaubt einer speziellen lokalen Gruppe unter Linux das Ausführen von `apt update` mittels der `/etc/sudoers`\-Konfiguration. (K3)

## 🔥 Freiwillige Zusatzaufgaben (Bloom K4 & K5)

1. **AD-Ausblick:** Recherchiert, warum Firmen trotz Cloud-Trend oft noch ein "Hybrid-AD" (Lokal + Cloud) einsetzen. (K4)
2. **Passwort-Sicherheit:** Vergleicht verschiedene Hash-Algorithmen in der `/etc/shadow`. Welcher gilt heute als sicher? (K4)
3. **SaaS-Rechte-Audit:** Simuliert ein Audit: Wer hat Zugriff auf die Firmen-Cloud (z.B. Dateiaustausch)? Erstellt eine Liste aller aktiven Logins. (K5)

## 📚 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Rheinwerk:** Kapitel "Benutzerverwaltung und Verzeichnisdienste".

### 🔍 Web

- https://de.wikipedia.org/wiki/Identit%C3%A4tsmanagement
- https://de.wikipedia.org/wiki/OpenLDAP
- https://de.wikipedia.org/wiki/Active_Directory

</details>

### P1: Lokale Gruppenverwaltung: Erstellt unter Linux zwei Gruppen (vertrieb, technik) und fügt Testnutzer hinzu. Testet den Zugriff auf einen gemeinsamen Ordner. (K3)

---

### P2: OpenLDAP Struktur: Zeichnet einen Verzeichnisbaum (DIT) für euer Szenario mit Organisationseinheiten (OUs) für Benutzer und Gruppen. (K3)

---

### P3: Rechtevergabe (Windows): Erstellt in eurer Windows-VM zwei Ordner und konfiguriert die NTFS-Rechte so, dass Gruppe A nur lesen und Gruppe B schreiben darf. (K3)

---

### P4: Vergleichstabelle: Erstellt eine Tabelle, die lokale Benutzerverwaltung, OpenLDAP und Entra ID gegenüberstellt (Vorteile/Nachteile). (K4)

---

### P5: Sudo-Berechtigungen: Erlaubt einer speziellen lokalen Gruppe unter Linux das Ausführen von apt update mittels der /etc/sudoers-Konfiguration. (K3)

---

### Z1: AD-Ausblick: Recherchiert, warum Firmen trotz Cloud-Trend oft noch ein "Hybrid-AD" (Lokal + Cloud) einsetzen. (K4)

---

### Z2: Passwort-Sicherheit: Vergleicht verschiedene Hash-Algorithmen in der /etc/shadow. Welcher gilt heute als sicher? (K4)

---

### Z3: SaaS-Rechte-Audit: Simuliert ein Audit: Wer hat Zugriff auf die Firmen-Cloud (z.B. Dateiaustausch)? Erstellt eine Liste aller aktiven Logins. (K5)