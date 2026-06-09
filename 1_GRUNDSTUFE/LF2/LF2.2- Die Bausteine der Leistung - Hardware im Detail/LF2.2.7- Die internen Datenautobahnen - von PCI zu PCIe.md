# LF2.2.7- Die internen Datenautobahnen - von PCI zu PCIe

Als **PC-Bauer**  
möchte ich **die verschiedenen internen Steckplätze und Busse auf einem Mainboard identifizieren können**,  
um **Erweiterungskarten korrekt auszuwählen und die Systemleistung optimal zu nutzen**.

# Celebration Criteria

- Wir können die Entwicklung der internen Erweiterungsbusse von **ISA** über **PCI** und **AGP** zu **PCIe** nachzeichnen.
- Wir können die Bedeutung der verschiedenen **PCIe-Lanes** (x1, x4, x8, x16) für die Leistungsfähigkeit einer Komponente erläutern.
- Wir können die Funktion von CPU-internen Bussen wie dem **FSB** (historisch) und modernen Verbindungen wie **DMI** oder **HyperTransport** beschreiben.

# Wissens-Briefing

## Was ist ein Bussystem?

Ein **Bussystem** ist die zentrale Datenautobahn in einem Computer.

- **Elektrisch** besteht es aus einer Gruppe von parallelen Leiterbahnen auf dem Mainboard, die verschiedene Komponenten miteinander verbinden.
- **Mechanisch** wird es durch standardisierte Steckplätze (Slots) und Anschlüsse (Ports) sichtbar, in die man Erweiterungskarten oder externe Geräte steckt. Der Zweck ist es, die Kommunikation zwischen CPU, Arbeitsspeicher, Festspeichern und Erweiterungskarten zu ermöglichen.

## Entwicklung der internen Bussysteme (Erweiterungsslots)

<table style="min-width: 364px"><tbody><tr><th colspan="1" rowspan="1" colwidth="101"><p>Bus</p></th><th colspan="1" rowspan="1" colwidth="90"><p>Typ</p></th><th colspan="1" rowspan="1" colwidth="148"><p>Max. Bandbreite</p></th><th colspan="1" rowspan="1"><p>Merkmale</p></th></tr><tr><td colspan="1" rowspan="1" colwidth="101"><p>ISA (hist.)</p></td><td colspan="1" rowspan="1" colwidth="90"><p>parallel</p></td><td colspan="1" rowspan="1" colwidth="148"><p>8 MB/s</p></td><td colspan="1" rowspan="1"><ul><li><p>sehr langsam</p></li><li><p>manuelle Konfiguration (Jumper)</p></li><li><p>abgelöst durch PCI</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="101"><p>PCI (hist.)</p></td><td colspan="1" rowspan="1" colwidth="90"><p>parallel</p></td><td colspan="1" rowspan="1" colwidth="148"><p>133 MB/s</p></td><td colspan="1" rowspan="1"><ul><li><p>“plug &amp; play”</p></li><li><p>shared bus —&gt; Flaschenhals</p></li><li><p>abgelöst durch PCIe</p></li></ul></td></tr><tr><td colspan="1" rowspan="1" colwidth="101"><p>PCIe (aktuell)</p></td><td colspan="1" rowspan="1" colwidth="90"><p>seriell</p></td><td colspan="1" rowspan="1" colwidth="148"><p>63.000 MB/s</p></td><td colspan="1" rowspan="1"><ul><li><p>Point2Point Verbindung</p></li><li><p>skalierbar (x1, x4, x8, x16)</p></li></ul></td></tr></tbody></table>

## CPU-, Speicher- und Chipsatz-Busse

- **FSB (Front Side Bus, historisch):** Früher die zentrale Verbindung zwischen CPU, Northbridge (Chipsatz) und RAM. War oft der Flaschenhals des gesamten Systems.
- **Northbridge/Southbridge (historisch):** Der Chipsatz war früher in zwei Teile geteilt. Die Northbridge war die schnelle Anbindung für CPU, RAM und Grafik. Die Southbridge war für die langsameren I/O-Geräte zuständig. Heute sind diese Funktionen in der CPU und einem einzigen "Platform Controller Hub" (PCH) integriert.
- **DMI/HyperTransport:** Moderne, schnelle Point-to-Point-Verbindungen, die die CPU direkt mit dem Chipsatz (für Peripherie) verbinden. Der Speichercontroller ist heute direkt in der CPU integriert.

# Aufgaben

1.  Sucht Bilder von einem alten Mainboard mit ISA- und PCI-Slots und vergleicht sie mit einem modernen Mainboard mit PCIe-Slots. Beschreibt die sichtbaren Unterschiede.
2.  Eine Grafikkarte benötigt einen PCIe-x16-Slot. Erklärt, warum man sie nicht in einen x1-Slot stecken sollte (und warum es oft mechanisch gar nicht passt).
3.  Findet ein Schaubild einer alten Mainboard-Architektur mit North- und Southbridge und vergleicht es mit einer aktuellen Architektur. Beschreibt, welche Komponenten heute direkt in der CPU integriert sind.

# Quellen & Vertiefung

- **Rheinwerk IT-Handbuch:** Kapitel 4.1.4 "Bussysteme und Schnittstellen", Seiten 214 ff.
- **Wikipedia:** [PCI Express](https://de.wikipedia.org/wiki/PCI_Express), [Front Side Bus](https://www.google.com/search?q=https://de.wikipedia.org/wiki/Front_Side_Bus), [Chipsatz](https://de.wikipedia.org/wiki/Chipsatz)