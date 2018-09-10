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

![Aufbau ISDN-Basisanschluss](./ISDN-Basisanschluss.png "ISDN-Basisanschluss")

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
