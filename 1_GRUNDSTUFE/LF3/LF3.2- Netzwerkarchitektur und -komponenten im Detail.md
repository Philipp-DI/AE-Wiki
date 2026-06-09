# 3️⃣LF3.2- Netzwerkarchitektur und -komponenten im Detail

Als Junior-Systemplaner

möchte ich die physischen und logischen Strukturen von Netzwerken sowie die Funktionsweise zentraler Netzwerkkomponenten verstehen,

damit ich für die "Innovate GmbH" eine detaillierte und standardkonforme Netzwerkplanung durchführen kann.

# Celebration Criteria

- Wir können die physische Infrastruktur eines LANs auf Basis von Topologien und strukturierter Verkabelung planen und dokumentieren.
- Wir können die logische Netzwerkkommunikation anhand von Schichtenmodellen (OSI/TCP-IP) analysieren und die Rolle der verschiedenen Adresstypen (MAC/IPv4) zuordnen.
- Wir können IPv4-Adressräume für kleine Netzwerke konzipieren und grundlegendes Subnetting anwenden.
- Wir können verschiedene Breitband-Anschlusstechnologien bewerten und eine fundierte Empfehlung für einen Unternehmensstandort abgeben.

# Szenario

Nachdem die Geschäftsführung der "Innovate GmbH" von eurem Grundlagenkonzept überzeugt ist, erhaltet ihr den Folgeauftrag: die detaillierte technische Planung des Netzwerks. Ihr habt einen Grundriss des Büros mit den 5 Arbeitsplätzen und einem kleinen Abstellraum, der als Technikzentrale dienen soll. Nun müsst ihr entscheiden, wie das Netzwerk physisch aufgebaut, logisch strukturiert, welche Komponenten benötigt werden und wie der Anschluss an das Internet realisiert wird.

# Abschlussaufgabe

## Technisches Anforderungsdokument für das Netzwerk der "Innovate GmbH"

Nachdem die Geschäftsführung grünes Licht gegeben hat, sollt ihr nun ein detailliertes technisches Anforderungsdokument (Lastenheft) erstellen. Dieses Dokument dient als formale Grundlage für die Ausschreibung und die Beauftragung eines externen Installationsbetriebs. Es muss so präzise sein, dass der Installateur genau weiß, was zu tun ist.

## Anforderungen an den Inhalt

### Physischer Netzwerkplan (Anhang A):

- Erstellt einen sauberen, maßstabsgetreuen Grundriss des Büros.
- Zeichnet exakt die Positionen der Netzwerkdosen (doppelt, RJ45), die genauen Kabelwege in Kabelkanälen und den Standort des Netzwerkschranks ein.
- Spezifiziert den zu verwendenden Kabeltyp (z.B. "Cat 7 S/FTP Verlegekabel") und begründet die Wahl mit Blick auf Zukunftssicherheit und mögliche Störquellen.

### Logischer Netzwerkplan (Anhang B):

- Definiert den exakten privaten IPv4-Adressbereich für das Unternehmen (z.B. `192.168.50.0 /24`).
- Erstellt eine detaillierte Adresstabelle, die IP-Adresse, Subnetzmaske, Gateway und DNS-Server für alle 5 PCs, einen Netzwerkdrucker, den Router und optional einen Server festlegt. Begründet, warum ihr diesen Adressbereich gewählt habt.
- Berechnet die maximale Anzahl an Hosts in diesem Subnetz und erklärt kurz, warum dieser Adressraum für zukünftiges Wachstum ausreicht.

### Stückliste der Komponenten (Bill of Materials):

- Listet alle benötigten passiven Komponenten (z.B. 1x 19" Wandschrank, 1x 24-Port Patchpanel Cat 6a, 5x Datendosen, 150m Verlegekabel) und aktiven Komponenten (1x Gigabit-Switch mit mind. 8 Ports, 1x Router) auf. Gebt für die aktiven Komponenten die wichtigsten Leistungsmerkmale an.

### Anforderung an die Internetanbindung:

- Formuliert eine klare Anforderung an den Internetanschluss. Spezifiziert die empfohlene Technologie (z.B. "Glasfaser FTTH"), die Mindestbandbreite (symmetrisch, z.B. 100/100 MBit/s) und begründet dies mit den Bedürfnissen eines kreativen Startups (Umgang mit großen Dateien, Cloud-Nutzung).

## Abgabe

Das Dokument soll als professionelle PDF-Datei abgegeben werden, die an einen echten Dienstleister weitergeleitet werden könnte.