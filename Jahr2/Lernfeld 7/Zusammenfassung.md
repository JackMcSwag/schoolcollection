# Zusammfassung Lernfeld 7

## IPv6-Adressierung

* Durch eine IPv6-Adresse werden Hosts innerhalb eines Netzwerkes eindeutig erkannt
* Ein Host kann dabei mehrere IPv6-Adressen haben
* Gültigkeitsbereich einer IPv6-Adresse wird grob in verbindungslokal und global unterschieden
    * __verbindungslokal__: Nur im lokalen Netzwerk Gültig
    * __global__: Ist über das lokale Netzwerk auch im Internet gültig

### Segmentierung

* Adressen werden hierarchisch strukturiert vergeben
* Eine IPv6-Adresse besteht aus 128-Bit
* 128 Bit werden in 8 x 16 Bit aufgeteilt
* Von den 16 Bit werden jeweils 4 Bit hexadezimal dargestellt
* 4 Hexzahlen werden gruppiert und durch ':' getrennt
* Führende Nullen können weggelassen werden
* Eine Folge von 8 Nullen wird durch '::' abgekürzt

        Beispiel
         __________Network Prefix(64Bit)_____   _____Interface Identifier(64Bit)____    
        /                                    \ /                                    \
        2 0 0 1 : 0 d b 8 : 0 0 0 0 : 0 0 0 1 : 0 0 0 0 : 0 0 0 0 : 0 0 0 0 : 0 0 0 1 
        \                               / \_/
         \_____________________________/    \
            Network Prefix (64Bit)           Subnet Prefix(8 Bit)


* Eine IPv6-Adresse besteht aus zwei Teilen
    * Network Prefix (Präfix oder Netz-ID)
        * kennzeichnet Netz, Subnetz oder Adressbereich
    * Netz-ID (Suffix, IID oder EUI)
        * kennezeichnet Host im Netzwerk
        * wird aus der 48-Bit-MAC-Adresse gebildet und in 64-Bit unmgewandelt
        * Format: Modified-EUI-64-Format
        * unabhängig vom Network Prefix identifizierbar

### Präfix und Präfixlänge

* Die von IPv4 bekannte Netz bzw. Subnetzmaske fällt weg
* Segmentierung von Adressbereichn und Subnetzen durch Präfix
* Präfixlänge in Bits wird mit "/" and die Adresse angehängt
* Standardmäßig ist die Präfixlänge 64 Bit ("/64")

#### Typische Adressbereiche

* /64 oder /56 für Privatanwender oder kleinere Unternehmen
* /48 für Enterprise-Kunden die eigene Netze betreiben
* /32 für große Netzbetreiber oder Provider

### IPv6-Scopes (Gültigkeitsbereiche)

Im Gegensatz zu IPv4-Adressen, die nur in private und öffentliche Adressen unterschieden werden, sind IPv6-Adressen vielschichtiger.

* Host-Scope: localhost, Loopback
* Link-Local-Scope(LLA): Präfix immer "fe80::/64", reicht bis zum nächsten Router
* Unique-Local-Scope: Reservierte Adressbereiche im privaten lokalen Netz
* Site-Local-Scope(veraltet): Ähnlich wie Unique-Local-Scope
* Global-Scope: Global routbarer Adressbereich
* Multicast-Scope: Zusammenfassung von Routern, Zeit-Servern und anderen Diensten.

## Routingverfahren

### statisches Routing

* feste Vergabe der Wege zwischen Endpunkten
* Vergabe wird bei der Installation getroffen -> Routingtabelle
* Bei der Festlegung muss bekannt sein:
    * Konfiguration des Netzes
    * Anzahl der Leitungen und Router
    * Lage und Übertragungskapazität
* Änderungen müssen manuell konfiguriert werden

### dynamisches Routing

* Routen werden während des Netzbetriebes dynamisch vergeben
* Wege werden durch Metriken bestimmt
* Metriken als zentrale Funktion dieses Netzwerks
* Metriken beachten:
    * kürzesten Weg
    * schnellsten Weg
    * sichersten Weg
    * kostengünstigsten Weg
    * Knoten/Leitungsausfälle
    * Warteschlangenbildung
* Protokolle:
    * RIP
        * Legt Routingtabellen an, die sich während des Betriebs ändern
    * OSPF
        * Erfasst die Verfügbarkeit der Verbindungswege


## Adress Resolution Protocol (ARP)

* Arbeitet auf Schicht 2
* Sendet einen Broadcast an alle MAC-Adressen um Host zu identifiezieren
* Speichert tabellarisch, welche MAC-Adresse sich als Host der per Broadcast mitgeschickten IP-Adresse angesprochen fühlt

## Network Translation Protocol (NAT)

* Verfahren um lokale Netzwerke mit dem Internet zu verbinden
* Die IPv4-Adresse des Hosts wird durch die IP-Adresse des Routers ersetzt, da diese im Internet öffentlich ist.
* Der Router speichert sich über eine Port-Tabelle den zugehörigen Clienten ab
* Durch IPv6 wird das Verfahren überflüssig


## Virtual Private Network (VPN)

* Logisches privates Netzwerk auf öffentlicher zugägnlichen Infrastruktur
* Nur Teilnehmer des privaten Netzwerks können miteinander kommunizieren
* Ein VPN muss Vertraulichkeit, Integrität und Authentizität sicherstellen
* Tunneling der Datenpakete als verschlüsselte Verbindung zwischen den Endpunkten
    * Schicht 2 und 3
    * IPsec oder SSL

### VPN-Typen 

* End-to-Site-VPN (Host-to-Gateway-VPN / Remote-Access-VPN)
* Site-to-Site-VPN (LAN-to-LAN-VPN / Gateway-to-Gateway-VPN / Branch-Office-VPN)
* End-to-End-VPN (Host-to-Host-VPN / Remote-Desktop-VPN)


## Verschlüsselung

### Symmetrische Verschlüsselung

* Ein Schlüssel für Ver- und Entschlüsselung
* Hohe Geschwindigkeit
* Leichte Implementiereung
* Verschlüsselung unsicher, wenn ein Schlüssel bekannt
* Beispiel: ROT13, DES

### Asymmetrische Verschlüsselung

* Verschlüsselung durch Schlüsselpaar
* öffentlicher Schlüsse wird den Kommunikationspartnern zugägnlich gemacht
* privater Schlüssel bleibt verborgen
* Daten werden mit öffentlichem Schlüssel verschlüsselt und dem Empfänger übergeben
* Daten werden vom Empfänger durch den privaten Schlüssel entschlüsselt
* Falltür-Funktion: Werden die Daten mit dem öffentlichen Schlüssel durch mathematische Verfahren leicht verschlüsselt, die Umkehrung ist meist sehr aufwendig
* Beispiele: Diffie-Hellmann, RSA


## Datensicherheit

### Cloud-Computing

* Verügbarkeit, Skalierbarkeit, Effizienz, Kostenvorteile
* Software as a Service (SaaS): Anwedungen sind auf dem Server des Anbieters installiert
* Platform as a Service (PaaS): Betriebssystem, technisches Framework oder Entwicklungsumgebung
* Infrastructure as a Service (IaaS): Virtuelle Ressourcesn wie Server, Rechenleistung oder Festplattenspeicher
* Public Cloud: Dienste werden vom Provider öffentlich über das Internet zur Verfügung gestellt
* Private Cloud: Dienste werden vom Unternehmen nur den Mitarbeitern zur Verfüfung gestellt

### Speichermedien

* Optisch (CD, Bluray)
* Magnetisch (Magnetband)
* Elektronisch (Festplatte, USB-Stick, Speicherkarte)
* Cloud

### Backup-Arten

* Vollbackup: Hoher Speicherbedarf, Sicher alles
* Differentielles Backup: Sichert Änderungen zum Vollbackup, mittleres Speicherbedarf
* Inkrementelles Backup: Sichert Änderungen seit letztem Backup, geringer Speicherbedarf

### RAID

* RAID 0: Min. 2 Festplatten, keine Redundanz
* RAID 1: Min. 2 Festplatten, Spiegelung der Daten
* RAID 5: Min. 3 Festplatten, Verteilte Parität, 1 Platte darf ausfallen
* RAID 6: Min. 4 Festplatten, Verteilte Parität, 2 Platten können ausfallen
* Mischform: RAID 10, RAID 51

# Strukturierte Verkabelung

* auch unviverselle Gebäuderverkabelung (UGV) genannt
* einheitlicher Aufbauplan
* zukunftsorientiert und anwedungsunabhängig
* Standards sind für 3km, 1 Mio. qm und 50 - 50.000 Anwender ausgelegt

## Primärverkabelung
* Campus- oder Geländerverkabelung
* Verkabelung der Gebäude, wenige Stationen
* Hohe Datenübertragungsraten und große Entfernungen
* Meist durch Glasfaserkabel mit max. 1500 m 

## Sekundärverkabelung
* Gebäudeverkabelung über die Etagen
* Einzelne Stockwerke oder Etagen werden miteinander verkabelt
* Glasfaser oder Kupfer mit max. 500 m Länge

## Tertiärverkabelung
* Etagenverkabelung
* Verkabelung zwischen Etagen- und Stockwerksverteilern zur Anschlussdose am Arbeitsplatz
* Twisted-Pair-Kabel mit max 90m zzgl. 2 mal 5 m Anschlusskabel
* Teilweise auch Glasfaser

## Elemente der strukturierten Verkabelung

* Patchfeld, Patchkabel, Anschlussdosen, Netzwerkkabel, Verteilerschränke, Switches, Hubs, Router

Zu beachten:
* Anwendungsfall, Reichweite, Stabilität, Verfügbarkeit, Erweiterbarkeit, Dienstneutral, Wartbarkeit, Dokumentation

* Permanent-Link: Ende bis zur Dose
* Channel-Link: Ende bis zum Endgerät

### Spanning Tree Verfahren

* Verhindert parallele Verbindungen in Netzen mit vielen Switches
* Es werden keine Schleifen erzeugt
* Wird in beliebig vermaschten Netzstrukturen angewendet
* Erzeugt eine Baumtopologie mit eindeutigen Verbindungspfaden

## Leistungsmerkmale der Datenübertragung

### Klasse

Die Klasse bezieht sich auf die installierte und angeschlossene Verkabelung

| Verkabelungsklasse | Übertragungsfrequenzen MHz         | Datenübertragungsraten Gbit/s                                                   |
|:------------------:|:----------------------------------:|:-------------------------------------------------------------------------------:|
|          E         | 250                                | 1                                                                               |
|         EA         | 500                                | 10                                                                              |
|          F         | 600                                | >10                                                                             |
|         FA         | 1000                               | >10                                                                             
### Kategorie

Die Kategorie bezieht sich auf die einzelnen Komponenten (Kabel oder Anschlussdose)

| Komponentenkategorie | Übertragungsfrequenzen MHz | Datenübertragungsraten Gbit/s |
|:--------------------:|:--------------------------:|:-----------------------------:|
|           6          |             250            |               1               |
|          6A          |             500            |               10              |
|           7          |             600            |               10              |
|          7A          |            1000            |               10              |
|           8          |            2000            |               40              |

