# LF6.2.2- Software-Verteilung und SaaS-Management

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

> _Als IT-Bereitsteller\*in_  
> _möchte ich Software abhängig von Benutzergruppen ausrollen und den Zugriff auf SaaS-Anwendungen verwalten,_  
> _damit jeder Mitarbeiter die richtigen Werkzeuge zur Verfügung hat._

## 🎉 Celebration Criteria (Lernziele)

- Ich kann einen **Staged Rollout** (stufenweise Einführung) für eine neue Softwareanwendung planen. (K3)
- Ich kann zwischen lokaler Software-Paketierung und der Verwaltung von SaaS-Berechtigungen unterscheiden. (K2)
- Ich kann Softwarelizenzen basierend auf Funktionsrollen (Gruppen) zuweisen. (K3)

## 🧠 Wissens-Briefing

| Konzept | Erklärung & Relevanz |
| --- | --- |
| **Staged Rollout** | Software wird erst an eine Testgruppe ("Canary"), dann an eine Abteilung und erst dann an alle verteilt. Minimiert das Risiko von Totalausfällen. |
| **SaaS-Provisionierung** | Der Prozess, einem Benutzer Zugang zu einer Web-Anwendung (z. B. M365, Slack) zu geben. Oft verknüpft mit Lizenzkosten. |
| **Software-Repository** | Eine zentrale Quelle für Software-Pakete. Lokal (Eigener Server) oder Global (Internet). |
| **M365 / Entra ID Ausblick** | Microsofts Identitätslösung. Ermöglicht "Single Sign-On" (SSO): Ein Login für Windows und alle SaaS-Apps. |

## ⚠️ Typische Fallstricke & Impulsfragen

- **Lizenz-Wildwuchs:** Jeder Nutzer abonniert selbst SaaS-Dienste. -> _Impuls:_ Wie können wir die Kosten zentral kontrollieren?
- **Rollback-Plan:** Eine neue Version einer Software funktioniert nicht. -> _Impuls:_ Wie kommen wir schnell zur alten Version zurück?

## 🛠️ Pflichtaufgaben (Bloom K2 & K3)

1. **Rollout-Planung:** Erstellt eine Tabelle für einen Staged Rollout einer neuen Browserversion (Phase 1: IT-Abteilung, Phase 2: Verwaltung etc.). (K3)
2. **Software-Zuweisung:** Erstellt eine Matrix: Welche Benutzergruppe (Marketing, Technik, HR) erhält welche Softwarepakete? (K3)
3. **SaaS-Analyse:** Wählt eine SaaS-Lösung (z. B. ein Online-Tool). Dokumentiert, welche Berechtigungsstufen (Admin, User, Gast) dort möglich sind. (K2)
4. **M365/Entra Recherche:** Erstellt eine Infografik (Skizze), die zeigt, wie sich ein Benutzer bei Entra ID anmeldet und dadurch Zugriff auf verschiedene Apps erhält. (K3)
5. **Paket-Installation:** Installiert ein Softwarepaket auf eurem Linux-System über die Kommandozeile und dokumentiert die Abhängigkeiten. (K3)

## 🔥 Freiwillige Zusatzaufgaben (Bloom K4 & K5)

1. **SaaS-Sicherheit:** Recherchiert das Konzept von MFA (Multi-Faktor-Authentifizierung) für Cloud-Dienste und erklärt dessen Notwendigkeit. (K4)
2. **Shadow IT:** Diskutiert im Team, warum Nutzer "Schatten-IT" (eigene Tools) einführen und wie man dies durch guten Service verhindern kann. (K5)
3. **Silent Install:** Recherchiert die Parameter für eine "stille" Installation eines Windows-Programms (z.B. `/quiet` oder `/s`). (K4)

## 📚 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann:** Kapitel "Softwaremanagement".

### 🔍 Web

- https://developerexperience.io/articles/staged-rollout
- https://de.wikipedia.org/wiki/Microsoft_Entra_ID

</details>

### P1: Rollout-Planung: Erstellt eine Tabelle für einen Staged Rollout einer neuen Browserversion (Phase 1: IT-Abteilung, Phase 2: Verwaltung etc.). (K3)

---

### P2: Software-Zuweisung: Erstellt eine Matrix: Welche Benutzergruppe (Marketing, Technik, HR) erhält welche Softwarepakete? (K3)

---

### P3: SaaS-Analyse: Wählt eine SaaS-Lösung (z. B. ein Online-Tool). Dokumentiert, welche Berechtigungsstufen (Admin, User, Gast) dort möglich sind. (K2)

---

### P4: M365/Entra Recherche: Erstellt eine Infografik (Skizze), die zeigt, wie sich ein Benutzer bei Entra ID anmeldet und dadurch Zugriff auf verschiedene Apps erhält. (K3)

---

### P5: Paket-Installation: Installiert ein Softwarepaket auf eurem Linux-System über die Kommandozeile und dokumentiert die Abhängigkeiten. (K3)

---

### Z1: SaaS-Sicherheit: Recherchiert das Konzept von MFA (Multi-Faktor-Authentifizierung) für Cloud-Dienste und erklärt dessen Notwendigkeit. (K4)

---

### Z2: Shadow IT: Diskutiert im Team, warum Nutzer "Schatten-IT" (eigene Tools) einführen und wie man dies durch guten Service verhindern kann. (K5)

---

### Z3: Silent Install: Recherchiert die Parameter für eine "stille" Installation eines Windows-Programms (z.B. /quiet oder /s). (K4)