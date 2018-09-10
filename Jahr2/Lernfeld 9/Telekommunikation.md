# Telekommunikation

## Aufbau des klassischen Telefonnetzes

Das klassische analoge Telefonetz wird auch __POTS__ genannt, was von "plain old telephone service" abzuleiten ist.

![Aufbau POTS](./AufbauPOTS.png "Aufbau POTS")

### TAE = Telekommunikations-Anschluss-Einheit

Anschlussdose für analoge Telefonanschlüsse (a/b - Schnittstelle) und ISDN-Anschlüsse zum Anschlißene des NTBA an die Anschlussleitung.

### PPA = Passiver Prüfabschluss

Dient zu Messzwecken im Telefonnetz. Sie makiert den Abschlusspunkt der Verantwortlichkeit des Netzbetreibers. 

### APL = Abschlusspunkt des Liniennetzes

Ist das Ende ders Verzweigungskables der Teilnehmeranschlussleitung im Telefonnetz.

### TAL = Teilnehmeranschlussleitung (letzte Meile)

Stellt die Verbindung zwischen der Ortsvermittlungsstelle des Netzbetreibers und dem Telefonanschluss des Dienstnutzers dar.
Besteht aus einer Kupfer-Doppelader.

### KVZ = Kabelverzweiger

Der Kabelverzweiger ist ein passiver Schaltschrank zur Kabelverteilung der Leitungen innerhalb eines Fernsprech-Ortsnetzes,der Hauptkabel mit Verzweigungskabel verbindet.

### OASL = Ortsanschlussleitung

Stellt die Verbindung zwischen dem Kabelverzweiger und der Ortsvermittlungsstelle dar.

### OVSt = Ortsvermittlungsstelle

Ortsvermittlungsstellen bieten je nach Ausbauzustand zwischen 100 und 10.000 Teilnehmernummern. Sie sind die Verbindung von Teilnehmerendgeräten an KVSt oder HVSt. Letze Ziffer der Ortskennzahl

#### HVT = Hauptverteiler

Stehen im __Kollokationsraum__ einer jeden OVSt und verlegen Hauptkabel zu den KVZ.

#### EWSD = Elektronisches Wählsystem Digital

Produktbezeichnung der digitalen Vermittlungsstelle von Siemens, die auch in der OVSt untergebracht war.

#### S12

Digitale Vermittlungsanlage von Alcatel, die früher in der OVSt benutzt wurde.

### KVSt = Knotenvermittlungsstelle



### HVSt = Hauptvermittlungsstelle



## Aufbau einer Telefonnummer

Eine Telefonnummer ist maximal 15 Ziffern lang. 

         VAZ          ONKZ       Teilnehmer
        00|49       5 4 2 1      12345678   

### VAZ = Verkehrsausscheidungsziffer

Unterscheidet zwischen Innland- uns Auslandanrufen.

### ONKz = Ortsnetzkennzahl

Wird aus der HVSt (1. Ziffer), der KVSt (2. & 3. Ziffer ) und der OVSt (letzte Ziffer) gebildet. In dicht besiedelten Bereichen ist die OVSt 2-stellig.

# ISDN

## Intergrated Services Network

* Verschieden Dienste
* Digital
* Bildschirmtext (BTX)

### ISDN Basisanschluss

Beim Basisanschluss hat man die Wahl, ob man eine Telefonanlage einsetzt oder nicht, also man einen Mehrgeräte- oder Anlagenanschluss nutzt

![Aufbau ISDN-Basisanschluss](./ISDN-Basisanschluss.png "ISDN-Basisanschluss")

* Analoge Schnittstelle = Uk0
* Digitale Schnittstelle = S0
* 2x B-Kanal mit je 64 kbit/s (Nutzkanal)
* 1x D-Kanal mit je 12 kbit/s (Steuerkanal)
 
 = 144 kbit/s Netto-Datenübertragungsrate

 Da auf Bussystemen oft sehr hochfrequente elektrische Signale übertragen werden, können an Verzweigungen und Enden des Übertragungsmediums auftretende Reflexionen nicht vernachlässigt werden; sie können zur Auslöschung der Signale durch Interferenz an bestimmten Stellen und damit zur Fehlfunktion des gesamten Systems führen. __Daher muss an beiden Enden im BUS terminiert werden__ (meist mit 100 Ohm).

#### NTBA = Network Termination Basic Access
Der NTBA ermöglich den Anschluss unterschiedlicher ISDN-fähiger Endgeräte an eine ISDN-Vermittlungsstelle des öffentlichen Telefonnetzes.

#### IAE = ISDN-Anschluss-Einheit

Eine ISDN-Anschluss-Einheit (IAE) ist eine Anschlussdose für Endgeräte am S0-Bus in ISDN-Installationen. 

#### EAZ = Endgeräteauswahlziffer

Bezeichnet die unter dem ISDN-Anschluss verwendete Rufnummer. Die EAZ ist die Erweiterung
der Hauptrufnummer und dient zur direkten Verbindung zu einem Endgerät. Die EAZ 0 ist dabei für das Ansprechen aller Endgeräte.

#### MSN = Multiple Subscriber Number

Mit MSN kann ein ISDN-Basisanschluss unter mehreren Rufnummern erreichbar sein. Die MSNs können flexibel auf die Endgeräte aufgeteilt werden. In Deutschland ist die Anzahl der MSNs pro ISDN-Mehrgeräteanschluss von der Bundesnetzagentur auf maximal zehn begrenzt. Die MSN ist der Teil der Telefonnummer, der auf die Ortsnetzkennzahl, auch Vorwahl genannt, folgt.

#### S0-Bus

* max. 12 UAE-Anschlussdosen
* max. 8 Endgeräte
* max. 4 passive Geräte
* max. Buslänge von NTBA->UAE: 180m
* bei Anlagenanschluss (da passiver Bus): 1000m
* empfohlene Länge von UAE zum Endgerät: 10m
* Muss mit zwei 100 Ohm Widerständen terminiert werden


### Mehrgeräteanschluss

Für private Haushalte eignet sich am besten ein Mehrgeräteanschluss. Hier werden die ISDN-Geräte direkt an das NTBA angeschlossen, woraus sich auch die Bezeichnung Point-to-Multipoint ergibt. Da an einem Mehreräteanschluss maximal nur 8 Geräte angeschlossen werden können, sind diesem Anschluss schnell die Grenzen gesetzt. Dem Basisanschluss im Mehrgerätebetrieb sind in Deutschland bis zu zehn eigenständige Rufnummern (MSN) fest zugeordnet, üblicherweise drei.


### Anlagenanschluss

![Aufbau ISDN-Anlagenanschluss](./ISDN-Anlagenanschluss.png "ISDN-Anlagenanschluss")

An den Anlagenanschluss (point to point) kann lediglich ein Gerät (üblicherweise eine Telefonanlage) angeschlossen werden. Das Endgerät wird an den S0-Bus angeschlossen und erhält den festgelegten TEI-Wert 0. Wegen der unterschiedlichen Terminal Endpoint Identifier (TEIs) können in der Betriebsart Anlagenanschluss keine Geräte betrieben werden, die für die Betriebsart Mehrgeräteanschluss bestimmt sind. Beim Anlagenanschluss wird eine „Rumpfnummer“ vergeben, die der Teilnehmer um Durchwahlen aus einem vorgegebenen Bereich ergänzen kann. Hierbei können auch mehrere Basisanschlüsse mit einer gemeinsamen Rumpfnummer betrieben werden. Dadurch steigt die Kapazität des gemeinsamen Anschlusses und zugleich ist eine effektivere Nutzung möglich, da jeder Basisanschluss jedes Gespräch übertragen kann.Die Nummern eines Anlagenanschlusses befinden sich meistens in einem zusammenhängenden Nummernblock, z. B. 100 Nummern von 00 - 99.

### Primärmultiplexanschluss (PMxAs)

Der Primämultiplexanschluss ist für größerer Unternehmen geeignet, denn er bietet 16 bis 30 Nutzkanäle (B-Kanäle) an, was eine deutliche Steigerung im Vergleich zum Basisanschluss ist. Dies lassen sich die ISDN-Anbieter selbstverständlich gut bezahlen, so dass sich ein PMX-Anschluss für den Privatanwender nicht lohnt.

Der PMX-Anschluss ist nur als Anlagenanschluss verfügbar. Technisch gesehen wäre ein PMX-Anschluss als Mehrgeräteanschluss möglich, was aber wenig Sinn machen würde, da maximal 8 Endgeräte angeschlossen werden würden und die restlichen Nutzkanäle brach liegen würden. Aus diesem Grund wird eine Telefonanlage benötigt.

![Aufbau ISDN-Primärmultiplex](./ISDN-PMxAs.png "ISDN-Primärmultiplex")

* Verfügbar als Anlagenanschluss
* B-Kanäle: 16 - 30 (64 KBit/s)
* D-Kanäle: 1 (64 KBit/s)
* Synchronisationskanal: 1 (64 KBit/s) (Datensicherung)
* Analoge Schnittstelle: UK2
* Digitale Schnittstelle: S2M
* Maximale Bruttobandbreite: 2048 KBit/s (32x64 KBit/s)

#### NTPM = Network Termination Primary Multiplex

Der NTPM ermöglicht den Anschluss unterschiedlicher ISDN-fähiger Endgeräte an eine ISDN-Vermittlungsstelle des öffentlichen Telefonnetzes.

Die Begriffe Mehrgeräteanschluss, Anlagenanschluss, Basisanschluss und Primärmultiplexanschluss sind auf den ersten Blick etwas verwirrend und man sollte diese nicht miteinander vermischen. Ein Mehrgeräteanschluss oder Anlagenanschluss sagt erst einmal aus, auf welche Weise die ISDN-Geräte die Verbindung zur örtlichen Vermittlungstelle bekommen, nämlich direkt über das NTBA (Mehrgeräteanschluss) oder auf einen Umweg über eine Telefonanlage (Anlagenanschluss). Basisanschluss und Primärmultiplexanschluss sind Leistungsmerkmale des ISDN-Anbieters (Anzahl der Kanäle, Bandbreite, etc).


## Breitband ISDN (B-ISDN)

![Aufbau Breitband-ISDN](./Breitband-ISDN.png "Breitband-ISDN")


Übertragen per COAX- (155 Mbit/s) oder Glasfaserkabel (622 Mbit/s). Großer Nachteil, da die Bandbreite nicht geshared werden konnte.

Die Planung für B-ISDN sah als Übertragungstechniken den Asynchronous Transfer Mode (ATM) und
die Synchrone Digitale Hierarchie (SDH) vor.

Dieses universelle Netzwerk sollte in der Lage sein, zum einen die Funktionen der damals existierenden Sprachnetze, Datennetze und Fernsehnetzwerke zu übernehmen und zum anderen genügend Spielraum für die Umsetzung zukünftiger Kommunikationstechnologien zur Verfügung stellen. Dabei wurde an eine Vielzahl von Breitbanddiensten gedacht, u.a. an Bildfernsprechen, Arbeitsplatz- und Videokonferenzen, Multimediatechnik, Fernsehprogrammverteilung und Breitband-Kabeltext. Das Breitband-ISDN sollte konzeptionell mit Übertragungsgeschwindigkeiten bis 140 Mbit/s ausgestattet werden und setzte in der Übertragungshierarchie auf ISDN auf.