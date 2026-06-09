# Mohammed

Als angehender Cloud Administrator möchte ich die spezifischen Sicherheitsherausforderungen und Verantwortlichkeiten in der Cloud verstehen, damit ich Cloud-Umgebungen sicher konfigurieren und betreiben kann.

# Celebration Criteria

- Wir können das Shared-Responsibility-Modell für IaaS, PaaS und SaaS grafisch darstellen und erklären.
- Wir können mindestens drei häufige Sicherheitsrisiken in der Cloud benennen
- Wir können den Zweck von fundamentalen Cloud-Sicherheits-Tools wie IAM (Identity and Access Management) und Security Groups/NSGs erklären.

# Wissens-Briefing

Sicherheit in der Cloud funktioniert anders als im eigenen Rechenzentrum. Das wichtigste Konzept ist das **Shared Responsibility Modell (Modell der geteilten Verantwortung)**. Es definiert, wofür der Cloud-Anbieter (z.B. Amazon, Microsoft) und wofür der Kunde verantwortlich ist.

- **IaaS (Infrastructure as a Service):** Der Anbieter ist für die physische Sicherheit (Rechenzentrum, Server-Hardware) verantwortlich. Der Kunde ist für fast alles andere verantwortlich (Betriebssystem, Netzwerk-Konfiguration, Anwendungen, Daten).
- **PaaS (Platform as a Service):** Der Anbieter kümmert sich zusätzlich um das Betriebssystem und die Laufzeitumgebung. Der Kunde ist für die Sicherheit seiner Anwendung und Daten verantwortlich.
- **SaaS (Software as a Service):** Der Anbieter ist für fast alles verantwortlich. Der Kunde ist hauptsächlich für die Verwaltung der Benutzer und die sichere Nutzung der Software verantwortlich. **Fazit:** Der Kunde ist IMMER für seine Daten, Identitäten und Zugriffsrechte verantwortlich. Die häufigsten Sicherheitsprobleme in der Cloud sind nicht Hacker, die den Anbieter knacken, sondern **Fehlkonfigurationen durch den Kunden**.

# Aufgaben

> 1. **Modell erklären:** Findet online die Grafiken zum Shared Responsibility Modell von Microsoft Azure und AWS. Vergleicht sie und erklärt in eigenen Worten die wesentlichen Unterschiede und Gemeinsamkeiten.

:::success
### **AWS vs. Microsoft Azure:**

Beide Anbieter verfolgen dasselbe Ziel: Klarheit darüber zu schaffen, wer den "Schlüssel" für welchen Raum besitzt.

### **\==Gemeinsamkeiten:==**

- **Die goldene Regel:** Die Verantwortung für die **Daten** liegt immer beim Kunden. Weder Amazon noch Microsoft schauen in die Dateien oder Datenbanken, um dort Sicherheitslücken zu suchen.
- **Physische Sicherheit:** Beide übernehmen zu 100 % den Schutz der Rechenzentren **(Zutrittskontrollen, Stromversorgung, Hardware-Wartung).**
- **Trennung:** Beide unterscheiden strikt zwischen der Sicherheit **der** Cloud (Infrastruktur) und der Sicherheit **in** der Cloud (Ihre Konfiguration).

### **\==Unterschiede:==**

**Vereinfachtes Beispiel**

[**1.AWS**](http://1.AWS) : ist der **Vermieter eines Hochhauses**.

- **Security OF the Cloud (AWS):** Der Vermieter garantiert, dass das Haus stabil steht, die Wände feuerfest sind, der Fahrstuhl gewartet ist und niemand ohne Erlaubnis durch den Haupteingang spaziert. Das ist das Fundament – die Infrastruktur.
- **Security IN the Cloud (Kunde):** Sobald man als mieter in die Wohnung ziehen, ist man der Chef. Wenn man die Tür nicht abschließt oder sein WLAN-Passwort nennt, kann der Vermieter nichts dafür. AWS sagt ganz klar: "Ich baue dir ein sicheres Haus, aber was du _drinnen_ machst, ist deine Sache."

2. **Microsoft Azure:** denkt eher wie ein **Full-Service-Dienstleister**. Das Modell ist wie eine Tabelle, in der man sieht: "Je mehr ich bezahle, desto mehr nimmt mir Microsoft ab."

- **Der Fokus auf Endpunkte:** Das ist der Clou bei Azure. Microsoft sagt: "Selbst wenn du bei uns ein Rundum-Sorglos-Paket (SaaS) buchst, ist dein **Laptop** (der Endpunkt), mit dem du dich einloggst, immer noch deine Baustelle." Wenn dein Mitarbeiter sein Handy im Café liegen lässt und dort kein PIN-Code drauf ist, ist das deine Verantwortung.
- **Der Stufenplan:** Azure zeigt sehr schön grafisch, wie sich der Balken der Verantwortung verschiebt. Bei IaaS (Leere Wohnung) hat man viel Arbeit. Bei SaaS (Hotelzimmer) übernimmt Microsoft fast alles – außer eben Identität (wer man ist) und sein Gerät.

![](files/019cee46-b57c-74e2-b10f-4a5191e45728/image.png)
:::

> 2. **Szenario-Analyse:** Die "KreativKopf GmbH" will einen Webserver in der Cloud (IaaS) betreiben. Welche Sicherheitsaufgaben muss die Agentur selbst übernehmen? Listet mindestens fünf konkrete Punkte auf.

:::success
### **Hier sind fünf konkrete Aufgaben, die die KreativKopf GmbH selbst erledigen muss:**

1. **Betriebssystem-Härtung & Patching:** Die Agentur muss Sicherheitsupdates für Windows oder Linux installieren.
2. **Firewall-Konfiguration (Tür Steher):** Die Agentur muss festlegen, welche Ports für Web-Traffic offen sein oder darf .
3. **Identity & Access Management (IAM):** Wer darf sich am Server anmelden? Die Agentur muss starke Passwörter und Zwei-Faktor-Authentifizierung (2FA) für ihre Administratoren erzwingen.
4. **Webserver-Absicherung:** Die Konfiguration der Software und die Installation von SSL-Zertifikaten (HTTPS) liegt voll in der Hand der Agentur.
5. **Datensicherung (Backup):** Der Anbieter garantiert meist nur, dass die Festplatte nicht physisch kaputtgeht. Wenn die Agentur versehentlich Daten löscht, hilft nur ein selbst eingerichtetes Backup.
:::

> 3. **Fehlkonfiguration finden:** Recherchiert den Begriff "Offener S3 Bucket". Beschreibt, was das Problem ist und welches Schutzziel (V, I, V) hier hauptsächlich verletzt wird.

:::success
Ein **"S3 Bucket"** ist ein einfacher Speicherort für Dateien in der Cloud (Cloud-Speicher). **"Offen"** bedeutet in diesem Zusammenhang, dass die Zugriffsberechtigungen so falsch eingestellt wurden, dass **jeder Mensch auf der Welt mit der URL** die Daten lesen **(und manchmal sogar löschen)** kann.

### Welches Schutzziel wird verletzt?

Im klassischen IT-Sicherheitsmodell der **VIV** **(Vertraulichkeit, Integrität, Verfügbarkeit)** wird hier primär die **Vertraulichkeit** verletzt.

- **Vertraulichkeit (V):** Dies ist der Hauptschaden. Daten, die eigentlich nur intern zugänglich sein sollten **(z. B. Kundendaten, Kopien von Ausweisen oder interne Rechnungen)**, gelangen an die Öffentlichkeit.
- **Integrität (I):** Falls der Bucket auch Schreibrechte für Fremde hat, könnten Angreifer Dateien manipulieren **(z. B. Schadsoftware in die Downloads der Website einschleusen).**
- **Verfügbarkeit (V):** Wenn Fremde die Daten löschen dürfen, ist auch die Verfügbarkeit dahin.
:::

# Quellen und Vertiefung

- **Primärquelle:** Rheinwerk IT-Handbuch, Kapitel 19 "Cloud Computing", Abschnitt 19.7 "Sicherheit und Datenschutz" (S. 840-844).
- **Online-Ressource:** [Microsoft - Geteilte Verantwortung in der Cloud](https://docs.microsoft.com/de-de/azure/security/fundamentals/shared-responsibility)
- **Online-Ressource:** [AWS - Modell der geteilten Verantwortung](https://aws.amazon.com/de/compliance/shared-responsibility-model/)