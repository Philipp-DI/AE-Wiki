# LF6.2.1- Automatisierte Systembereitstellung und Wartung

<details>
<summary>Briefing</summary>

**Schätzung:** 5 SP

## 👤 User Story

> _Als System-Administrator\*in_  
> _möchte ich die Installation und Aktualisierung von Betriebssystemen automatisieren,_  
> _damit Sicherheitslücken zeitnah geschlossen werden und neue Rechner ohne Zeitverzug einsatzbereit sind._

## 🎉 Celebration Criteria (Lernziele)

- Ich kann eine funktionale `autoinstall.yaml` für eine "Zero-Touch"-Installation von Ubuntu 24.04 erstellen. (K3)
- Ich kann automatisierte Sicherheitsupdates (Unattended-Upgrades) unter Linux konfigurieren. (K3)
- Ich kann den Prozess der Betriebssystem-Aktualisierung und die Bedeutung von Release-Zyklen (LTS) erläutern. (K2)

## 🧠 Wissens-Briefing

| Konzept | Erklärung & Relevanz |
| --- | --- |
| **Autoinstall (YAML)** | Konfigurationsdatei für den Ubuntu-Installer (Subiquity). Steuert Partitionierung, Sprache und erste Pakete. |
| **LTS (Long Term Support)** | Betriebssystem-Versionen mit langjähriger Garantie für Sicherheitsupdates. Wichtig für die Stabilität im Unternehmen. |
| **Unattended-Upgrades** | Ein Dienst unter Linux, der im Hintergrund kritische Sicherheits-Patches installiert, ohne den Betrieb zu stören. |
| **Kernel-Livepatching** | Technik, um kritische Kernel-Updates ohne einen Neustart des Systems einzuspielen. |

## ⚠️ Typische Fallstricke & Impulsfragen

- **Update-Fehler:** Ein automatisches Update zerschießt die Grafiktreiber. -> _Impuls:_ Wie können wir Updates erst testen, bevor sie alle Rechner erreichen?
- **Stromausfall beim Deployment:** Das System bricht während der Automatisierung ab. -> _Impuls:_ Wie können wir den Status der Installation überwachen?

## 🛠️ Pflichtaufgaben (Bloom K2 & K3)

1. **YAML-Konfiguration:** Erstellt eine `autoinstall.yaml`, die neben der Benutzeranlage auch den SSH-Dienst und das Paket `curl` automatisch installiert. (K3)
2. **Sicherheitsupdates aktivieren:** Installiert und konfiguriert das Paket `unattended-upgrades` in eurer Linux-Umgebung. (K3)
3. **Wartungsplan erstellen:** Entwerft einen tabellarischen Plan: Wann werden Betriebssystem-Updates eingespielt (Tage/Uhrzeiten) und wer wird informiert? (K3)
4. **Versionen prüfen:** Ermittelt via Terminal den aktuellen Kernel-Stand und das nächste verfügbare Betriebssystem-Upgrade. (K2)
5. **Automatisierung testen:** Führt eine Installation mit eurem Medium auf dem Experimentier-PC durch und prüft die Logs nach dem ersten Bootvorgang. (K3)

## 🔥 Freiwillige Zusatzaufgaben (Bloom K4 & K5)

1. **Windows-Exkurs (Theorie):** Recherchiert, wie Windows-Updates in großen Firmen gesteuert werden (WSUS/Intune) und vergleicht dies mit Linux-Repository-Servern. (K4)
2. **Skript-Check:** Schreibt ein kurzes Skript, das prüft, ob ein Neustart nach Updates erforderlich ist (Existenz der Datei `/var/run/reboot-required`). (K4)
3. **Cleanup-Automation:** Erstellt einen Cronjob, der einmal pro Woche alte, nicht mehr benötigte Pakete (`apt autoremove`) entfernt. (K4)

## 📚 Quellen & Referenzen

### 📖 Literatur (Westermann, Rheinwerk)

- **Westermann:** Kapitel "Systempflege und Wartung".

### 🔍 Web

- https://canonical-subiquity.readthedocs-hosted.com/en/latest/reference/autoinstall-reference.html
- https://derlinuxwikinger.de/automatische-ubuntu-installation-mit-autoinstall/
- https://www.starline.de/magazin/technische-artikel/automatische-sicherheitsupdates-unter-linux-aktivieren

</details>

### P1: YAML-Konfiguration: Erstellt eine autoinstall.yaml, die neben der Benutzeranlage auch den SSH-Dienst und das Paket curl automatisch installiert. (K3)

```yaml
identity:
  hostname: dualis-laptop
  username: user
  password: "2e2b6533a81bc15430cf65de46dc097eeb5ba70c" # Hash (SHA-1) von "passwort"

ssh:
  install-server: true

packages:
  - curl
```

---

### P2: Sicherheitsupdates aktivieren: Installiert und konfiguriert das Paket unattended-upgrades in eurer Linux-Umgebung. (K3)

```yaml
packages:
  - curl
  - unattended-upgrades

late-commands: # mit curtin in-target IM Zielsystem ausführen
  - curtin in-target -- wait-for-grid; dpkg-reconfigure -f noninteractive unattended-upgrades
  - |
    curtin in-target -- bash -c 'cat <<EOF > /etc/apt/apt.conf.d/50unattended-upgrades
    Unattended-Upgrade::Allowed-Origins {
      "\${distro_id}:\${distro_codename}-security";
      // "${distro_id}:${distro_codename}-updates";
    };
    Unattended-Upgrade::Package-Blacklist {
    };
    EOF'
```

---

### P3: Wartungsplan erstellen: Entwerft einen tabellarischen Plan: Wann werden Betriebssystem-Updates eingespielt (Tage/Uhrzeiten) und wer wird informiert? (K3)

Updates solcher Art sollten außerhalb der Nutzungs- bzw. Betriebszeiten geschehen. Im Allgemeinen ist es auch ratsam zunächst ein Test-PC oder Test-Server zu nutzen, um sicherstellen zu können, dass das Update den Betrieb nicht stört und funktioniert. Dieser Test findet dann natürlich während den Arbeitszeiten des IT-Teams statt.

| Welches System? | Was? | Wann? | Wer wird informiert? |
| --- | --- | --- | --- |
| Test-PC/Server | OS  | Montag, 9:00 Uhr | IT-Team |
| Office-PCs | OS  | Donnerstag, 22:00 Uhr | Alle betroffenen Mitarbeitenden |

---

### P4: Versionen prüfen: Ermittelt via Terminal den aktuellen Kernel-Stand und das nächste verfügbare Betriebssystem-Upgrade. (K2)

Vor einem großen Upgrade zunächst das aktuelle System updaten:  
`sudo apt update`  
`sudo apt dist-upgrade -o APT::Get::Always-Include-Phased-Updates=true`

Für das große Upgrade bieten sich zwei Möglichkeiten in Ubuntu:

- per GUI mit dem Befehl `update-manager`
- direkt mittels `do-release-upgrade` (Option `-c` führt lediglich einen “Check” aus)

---

### P5: Automatisierung testen: Führt eine Installation mit eurem Medium auf dem Experimentier-PC durch und prüft die Logs nach dem ersten Bootvorgang. (K3)

---

### Z1: Windows-Exkurs (Theorie): Recherchiert, wie Windows-Updates in großen Firmen gesteuert werden (WSUS/Intune) und vergleicht dies mit Linux-Repository-Servern. (K4)

---

### Z2: Skript-Check: Schreibt ein kurzes Skript, das prüft, ob ein Neustart nach Updates erforderlich ist (Existenz der Datei /var/run/reboot-required). (K4)

---

### Z3: Cleanup-Automation: Erstellt einen Cronjob, der einmal pro Woche alte, nicht mehr benötigte Pakete (apt autoremove) entfernt. (K4)

---