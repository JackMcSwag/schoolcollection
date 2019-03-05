# Netzwerke

## OSI-Referenzmodell

|Layer | Englisch | Deutsch
|:---:|:---:|:---:
|7|Application Layer| Anwedungsschicht
|6|Presentation Layer| Darstellungschicht
|5|Session Layer| Sitzungsschicht
|4|Transport Layer| Transportschicht
|3|Network Layer| Vermittlungsschicht
|2|Data Link Layer| Sicherungsschicht
|1|Physical Layer| Bitübertragungsschicht

## MAC - Adresse

* Media Access Control - Adressen sind eindeutig
* Werden von Herstellern in netzwerkfähige Geräte eingebaut
* Vergabe der Adressbereiche ist daher herstellerspezifisch
* Darstellung hexadezimal mit einer Länge von 96 Bit

## IP - Adresse

* Die Internet Protocol - Adresse MUSS in __einem__ Netzwerk eindeutig sein.

## Protokolle
Legen Regeln für Sprache und Form(Format) fest. Durch die Einigung ist die Kommunikation unter Teilnehmern gegeben und zusätzlich bietet diese Art der Standardisierung Sicherheit und Effizienz.

Die Protokolle, die bei der Netzwerkkommunikation verwendet werden, weisen viele grundlegende Funktionen auf. Zusätzlich zur Identifizierung von der Quelle und dem Ziel der Nachricht enthalten Netzwerkprotokolle Details, wie die Nachricht über dein Netzwerk übertragen wird. Dafür müssen vorgegebene Regeln eingehalten werden.

Nicht ordnungsgemäß formatierte Nachrichten können weder erfolgreich übertragen noch vom Empfänger verarbeitet werden.

### Formatierungsregeln:

    +--------------------------------------+
    |Frame Adressierung:                   |
    |   Ziel    (physische Hardwareadresse)|
    |   Quelle  (physische Hardwareadresse)|
    +--------------------------------------+
    |Gekapselte Nachricht:                 |
    |   Start-Kennung                      |
    |   Empfänger   (Ziel-ID)              |
    |   Absender    (Quell-ID)             |
    |   Gekapselte Daten (Bits)            | 
    +--------------------------------------+
    |Ende des Frames                       |
    |   (Anzeige für Ende der Nachricht)   |
    +--------------------------------------+

### Unicast

* Von __einem Sender__ zu __einem Empfänger__

### Broadcast

* Von __einem Sender__ and __alle__

### Multicast

* Von __einem Sender__ an __definierte Empfängergruppe__

### Carrier Sense Multiple Access / Collison Detection

Um Kollisionen von Datenpakten auf Netzwerkleitungen zu vermeiden, gibt es folgendes Verfahren:

__CSMA/CD__

* Carrier Sense (Träger-Zustandserkennung): Jede Station prüft, ob das Übertragungsmedium frei ist.

* Multiple Access (Mehrfachzugriff): Mehrere Stationen teilen sich das Übertragungsmedium.

* Collision Detection (Kollisionserkennung): Wenn mehrere Stationen gleichzeitig senden, erkennen sie die Kollision.

#### Ablauf

 * "Listen-before-Talk": Alle Stationen hören permanent das Übertragunsmedium ab, bei freiem Übertragungsmedium darf gesendet werden

 * Der Sender überprüft das Signal auf dem Bus mit dem gesendeten Signal. Ist dieses nicht gleich, hat ein anderer Sender auch gesendet und es kommt zu einer Kollision (Überlagerung)

 * Bei einer Kollision wird die Übertragung abgebrochen und ein Störsignal wird von dem Sender gesendet, der die Überlagerung zuerst bemerkt hat

 * Alle anderen Stationen wissen nun, dass das Übertragungsmedium besetzt ist und überprüfen dieses nach zufälliger Wartezeit erneut

* Konnte die Übertragung ohne Kollisionserkennung beendet werden, dann gilt die Übertragung als erfolgreich

Die __Kollisionsdomäne__ umfasst ein Netzwerk oder auch nur ein Teilnetzwerk aus Leitungen, Stationen und Kopplungselementen der Schicht 1 (OSI-Referenzmodell). In der Kollisionsdomäne müssen die Kollisionen innerhalb einer bestimmten Zeit jede Station erreichen. Das ist die Bedingung, damit das CSMA/CD-Verfahren funktionieren kann.

## Adressierung im Internet Protocol

* Ein Teilnehmer ist im Internet weltweit eindeutig durch eine Adressen zu erkennen, damit die Kommunikation zwischen Teilnehmern gesichert ist

* Die IP-Adresse wird den zu versendenden Datenpaketen auf der Vermittlungsschicht (Network Layer) vorangestellt.

### Aufbau IPv4

* Länge 32 Bit
* 8 Bit zu einem Byte zusammegefast 
* Der Bytewert wird Dezimal dargestellt
* Die 4 Werte werden durch Punkte getrennt (Dotted Decimal Notation DDN)
* Bereich jeweils 0 - 255

        Beispiel:
        11000000|10110010|00000000|00010100
        192     .178     .0       .20

Eine IP-Adresse setzt sich aus 2 Bestandteilen zusammen: Dem __Host-Anteil__ und dem __Netz-Anteil__

* Der Netz-Anteil begint beim höchstwertigen Bit ganz links
* Der Host-Anteil folgt bis zum niederwertigsten Bit ganz rechts
* Der Netz-Anteil bestimmt die Nummer eines Netzes
* Der Host-Anteil bestimmt die Nummer des Teilnehmers in diesem Netz
* Kein Netz darf mehr als einmal vorkommen
* Zwei Hosts in einem Netz dürfen keine identische Host-Adresse haben
* Somit muss jede __öffentliche__ IP-Adresse weltweit eindeutig sein

Bits des Host-Anteils = 0 => __Netzadresse__

Bits des Hots-Anteils = 1 => __Breoadcast-Adresse__

### Subnetzmaske

* Bestimmt Netz-Anteil in einer IP-Adresse

Vorgang:

* Logische UND-Verknüpfung der Bits aus der IP-Adresse und der Netzmaske

Beispiel:

||Dezimale Darstellung|1. Oktett|2. Oktett|3. Oktett|4. Oktett
|:---:|:---:|:---:|:---:|:---:|:---:|
IP-Adresse|192.168.111.100|11000000|10101000|01101111|01100100
Subnetzmaske|255.255.255.0|11111111|11111111|1111111|00000000
UND-Verknüpfung|192.168.111.0|11000000|10101000|01101111|00000000
||||Netzadresse||Hostadresse

Netzadresse: 192.168.111.0

#### Suffix

Der Suffix gibt die Anzahl der aufeinander folgenden 1er Bits in der Subnetzmaske an:

192.168.111.100/24

#### Maximale Teilnehmerzahl

* Die Anzahl der Teilnehmer in einem Netz ist immer 2^N - 2, wobei N die Anzahl der Bits vom Hostanteil bezeichnet.
* Zwei Adressen entfallen in jedem Netz (Netzadresse, Broadcast-Adresse)

#### Netzwerkklassen

* Unterteilung der Adressbereiche in 5 Netzklassen: Klasse A - E

Klasse| 1.Byte Binär |Von: | Bis:| Subnetzmaske| Bemerkung
|:---:|:---:|:---:|:---:|:---:|:---:|
Class A|0XXXXXXX|0.X.X.X|127.255.255.255|255.0.0.0|2^7 Netze/2^24-2 Hosts
Class B|10XXXXXX|128.0.X.X|191.255.X.X|255.255.0.0|2^14 Netze/2^16-2 Hosts
Class C|110XXXXX|192.0.0.X|223.255.255.X|255.255.255.0| 2^21 Netze/2^8-2 Hosts
Class D|1110XXXX|224.0.0.0|239.255.255.255|Multicasting
Class E|1111XXXX|240.0.0.0|255.255.255.255|Experimental

#### Klassenlose Netze

* Wird auch CIDR (Classless Inter Domain Routing) genannt
* Wird zur effizienteren Ausnutzung von IP-Adressräumen angewandt
* Die Konvention der Netzklassenzuordnung wird aufgehoben
* Die Aufteilung eines Netzes in Subnetze wird __Subnetting__ bezeichnet

#### Reservierte IP-Adressen in lokalen Netzwerk
* 0.0.0.0: Wird für das Routing benötigt. Bei unbekannten Empfängeradressen
* 127.0.0.0 & 127.0.0.1: Diese IP-Adressen dienen dem Rückopplungstest  

#### Adressbereiche (lokales Netzwerk)

Netzklasse| Anzahl der Netze |Netzadressen| Subnetzmaske| IP-Adressbereich
|:---:|:---:|:---:|:---:|:---:|
Klasse A|1|10.0.0.0|255.0.0.0|10.0.0.0-10.255.255.254
Klasse B|16|172.16.0.0-172.31.0.0|255.255.0.0|172.16.0.1-172.16.255.254
Klasse C|256|192.168.0.0-192.168.255.0|255.255.255.0| 192.168.0.1-192.168.0.254

#### DHCP Dynamical Host Configuration Protocol

* Durch das Verfahren DHCP werden druch den Router automatisch IP-Adressen an Teilnehmer eines Netzwerkes vergeben

### DNS Domain Name System

* Verantwortlich für die Namensauflösung (Url zu Ip)

#### Standard Gateway

* Router als Verbindung zu anderen Netzwerken
* Router als Ansprechstation für unbekannte IP-Adressen


### How to Subnetting

#### 1. Anforderungen definieren

* Anzahl der Netze
* Zur Verfügung stehende Hosts

        Anzahl von Subnetzen    2 |4 |8 |16|32|64|128   
        Anzahl geliehener Bits  1 |2 |3 |4 |5 |6 |7


#### 2. IP-Klasse, IP-Netzadresse

        Beispiel:
        192.168.1  .00000000
        Netzadresse|Hostanteil

#### 3. Netzanteil verlängern

* Die Anzahl der Bits ab dem MSB(Most Significat Bit) der Hostadresse ersetzen

        192.168.1.00|000000
                 .01|
                 .10|       Hosts: 2^6 - 2
                 .11|              = 62

#### 4. Bereiche festlegen

Achtung: 
* Erste Adresse = Netzadresse
* Letzte Adresse = Broadcast-Adresse 

1. Subnetz:
Netzadresse: 192.168.1.0 
Hosts:                .1-62
Broadcast:            .63


2. Subnetz:
Netzadresse: 192.168.1.64
Hosts:                .65-126
Broadcast:            .127

usw.

## Aktive Geräte in einem Netzwerk

### Router

* Verbinden mehrere Netzwerke mit unterschiedlichen Protokollen und Architekturen
* Network-Layer (3)

### Switch

* Trifft Weiterleitungsentscheidungen anhand der der selbständig erlernten Hardware-Adressen der angeschlossenen Geräte.
* Multi-Layer (2 & 3) (Eigentlich nur 2. Die, die auch Teile aus Layer 3 übernehmen sind spezielle Switches die halt auch Router-Funktionalitäten übernehmen)

### Hubs und Accesspoints

* Leiten Daten ohne weitere Verarbeitung auf allen anderen ihnen zur Verfügung stehenden Kanälen weiter

### Firewall

* Netzwerksicherheitseinrichtung, die ein- und ausgehenden Netzwerkverkehr anhand von Regeln kontrolliert


## Konvergenz

Kleine Netze werden aufgelöst und zu größeren
Netzen zusammengefasst die ihre Aufgaben übernehmen.
