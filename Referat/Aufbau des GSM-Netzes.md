# GSM - Netzarchitektur

* Netzarchitektur ist zur Übertragung der Sprache ausgelegt
* Man gliedert diese in 3 Teile

## Radio Sub-System


* Die Mobile Station (MS) ermöglicht dem Nutzer den Zugang zum Mobilfunknetz. Hauptaufgabe ist das Empfangen und Senden von Nutz- und Steuerdaten. Beispiele für die Mobile Station sind Mobiletelefone oder ein GSM-Modem zur Datenübertragung.

* In dem Telefon befindet sich die SIM-Karte zur Identifikation des Teilnehmers. Kann auch als Speicherplatz für Telefonbuch oder Kurzmitteilungen sein.

* Die Basisstation heißt Base Transciever Station. Sie übernimmt die Versorgung der Funkzelle. Das passiert über die Um-Schnittstelle (Luft- oder Funkschnittstelle).

* Der maximal zulässig Funkzellen Radius liegt bei 34.88 km. Aber wird aufgrund der eingeschränkten Sendeleistung durch geländebedingter Begebenheiten oder kleinern Zellen in Ballungsgebieten, dieser Wert nie erreicht.

* Die Basisstationen (10 bis 100) sind an einem Base Station Controller angeschlossen. Teilweise aber auch indirekt, da sie über andere Basisstationen mitgeschleift werden (Leitungen oder Richtfunk).

* Der BSC wählt den passenden Funkkanal und kümmert sich über die Leistungsregelung und den Handover zu einer anderen Funkzelle. (Handover oder Leistungsregelungen finden aber ja nach Hersteller zum Teil schon in der Basisstation statt)

* Durch den BSC wird der Mobilfunk in der Systemarchitektur zusammengefasst, so spart man auch Leistung auf dem Weg zur Vermittlungsstelle

* Bevor das GSM-Sprachsignal (13kbit/s) in die  Mobilfunkvermittlungsstelle (MSC) übergeht wird die Sprachübertragung von der Transcoding und Rate Adaption Unit (TRAU) 
in ein PCM-Signal (64kbit/s) umgewandelt. (Pulse-Code-Modulation, Umwandlung eines analogen Signals in ein digitales Signal)

* TRAU übernimmt auch die Datenratenanpassungen für die Datendienste. 

__Achtung!__ TRAU befindet sich häufig im MSC, obwohl es dem Radio Sub-System zugeordnet ist.


## Switching Sub-System

* Mobile Switiching Center (MSC) verwalte die Verbindungen und Nutzerdaten.

* HLR - Home Location Register enthält die Daten jedes Kunden (u.A. Rufumleitungen und Gesprächsdaten für Gebührenabrechnungen)

* VLR - Visitor Location Register enthalt dann die Heimatdateiadresse und die Rufnummer in der MSC. Bei Verlassen des Einzugsgebietes der MSC wird die Besucherdatei gelöscht und in der neuen Vermittlungsstelle gespeichert.


    Handy anschalten -> Daten der SIM an BTS -> Vergleich der Daten mit HLR und speichern des Handystandortes -> Anlegen einer VLR-Datei im MSC


* Die Beglaubigungszentrale (AuC - Authenticaiton Center) ist eine Datenbank, die die Funkschnittstelle gegen unberechtigtes Abhören schützt. (Geheimschlüssel, der auch auf der SIM ist)

* EIR - Equipment Identity Register speichert die IMEI-Nummer (International Mobile Equipment Identity) eines Handy (MS) ab, falls dieses defekt oder gestohlen wurde.

* Gateway - MSC (GSMC) erstellt Übergänge in andere Netze. Beispiel: Mobilfunkteilnehmer wird aus dem Festnetz angerufen -> GSMC ermittelt in der Heimatdatei (HLR) die zuständige MSC und vermittelt den Ruf weiter.


## Operation and Maintenance Sub-System

* Betriebs und Wartungszentrale eines GSM-Netzes ist das Operation and Maintenance Center (OMC). Unterschieden wird zwischen den Basisstationen (OMC-B) und den Vermittlungsstellen (OMC-S).

* Überwacht einen Teil des Gesamtmobilfunknetzes zum Lokalisieren und Beheben von Fehlern oder Netzelemente konfiguriert und neue Software aufgespielt.

* Einrichtung und Gebührenabrechnung von Teilnehmern

* Organisatorisch werden die Datenbanken EIR und AuC den OMCs zugeordnet, da sie dort gepflegt werden. Funktionell sind sie aber an die Vermittlungsstellen (MSC) gebunden.

## Wichtige Abkürzungen

| Abk. | Name                               | Beschreibung                                                                    |
|:----:|------------------------------------|---------------------------------------------------------------------------------|
|  AuC | Authentication Center              | Zugangsberechtigungszentrale                                                    |
|  BSC | Base Station Controller            | Steuerung mehrer Basisstationen                                                 |
|  BTS | Base Transceiver Station           | Basisstation                                                                    |
| EIR  | Equipment Identity Register        | Datenbank für die Geräte-Kennung IMEI                                           |
| GMSC | Gateway-MSC                        | Vermittlungsstelle mit Schnittstelle in andere Netze                            |
| HLR  | Home Location Register             | Heimatdatei                                                                     |
| MS   | Mobile Station                     | Mobilfunktelefon, Handy                                                         |
| MSC  | Mobile Switching Center            | Mobilfunkvermittlungsstelle                                                     |
| OMC  | Operation and Maintenance Center   | Betriebs- und Wartungszentrale                                                  |
| SIM  | Subscriber Identify Module         | Karte mit Chip zum Speichern benutzerdefinierter Daten und Zugriffsberechtigung |
| TRAU | Transcoding und Rate Adaption Unit | Umsetzung von Datenraten                                                        |
| VLR  | Visitor Location Register          | Besucherdatei                                                                   |
