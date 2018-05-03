# Zusammenfassung Wirtschaft

## Ablauforganisation

Die Ablauforganisation ordnet die Arbeitsprozesse in sachlicher, personeller, zeitlicher
und räumlicher Reihenfolge.
Sie stellt den Betrieb in Aktionb dar.

### Arten der Ablauforganisation

#### funktionsorientiert

Welche Arbeiten müssen in welcher Reihenfolge ausgeführt werden. (Flussdiagramm oder Ablaufdiagramm)

#### zeitorientiert

Optimierung von zeitlich aufeinanderfolgenden Arbeiten.(Balkendiagramm oder Netzplan)

#### raumorientiert

Minimale Wege bei räumlicher Ordnung der Aufgabenträger(Kommunikationsmatrix)

#### Ergonomie

estaltung des Arbeitsablaufs, um den Bedürfnissen des Menschen gerecht zu werden.

### Ziel

* Minimierung der Durchlaufzeiten
* optimale Ausnutzung vorhandener Kapazitäten
* menschengerechte Gestalung der Arbeitsprozesse

### Reorganisation von Arbeitabläufen

Arbeitsabläufe werden normalerweise für längeren Zeitraum bestimmt. Doch es gibt Ausnahmen:

* häufige Sörungen im Arbeitsablauf festgestellt
* Einführung neuer moderner Arbeitsmittel
* Veränderung des Produktionsprogramms
* notwendige Rationalisierungsmaßnahmen

Vorgehensweise für die Reorganisation:

1.  **Ist-Aufnahme**: Erfassung der besherigen Arbeitsabläufe
2.  **Ist-Analyse**: Analyse des Ist-Zustands
3.  **Soll-Konzept**: Aus der Ist-Analyse Vorschlag erarbeiten
4.  **Tests**: Soll-Konzept testen und ggf. überarbeiten
5.  **Einführung**: Nach erfolgreichen Tests Abläufe in den Alltag einführen
6.  **Kontrolle**: Einhaltung der Regelungen überwachen und Bewährung der Methoden prüfen

#### Methoden Ist-Aufnahme

* Interview
* Fragebogen
* Beobachtung
* Selbstaufschreibung
* Dokumentenauswertung

#### Methoden Ist-Analyse & Soll-Konzept

* Flussdiagramm (funktionsorientiert):

  * Rund: Anfangs und Endzeitpunkt
  * Rechteck: Tätigkeiteit
  * Raute: Entscheidungssymbol (nur ja und nein)
  * Kreis: Sprungstelle zur Ziffer oder Buchstaben

* Ablaufdiagramm (funktionsorientiert):

  * Kreis: Bearbeitung
  * Rechteck: Kontrolle
  * Dreieck: Lagerung
  * Pfeil: Transport
  * Halbkreis: Verzögerung

* Balkendiagramm (zeitorientiert):
  * ![Gantt-Diagramm](http://aha-wissen-praxis.de/sites/default/files/pictures/diagramme/gantt-diagramm.png "Gantt-Diagramm")
* Netzplan (zeitorientiert):
  * ![Beispiel](https://inlooxcdn.azureedge.net/var/corporate_site/storage/images/media/images/glossar/beispiel-netzplan/832394-1-ger-DE/beispiel-netzplan.png "Netzplan")
  * Erstellung durch 1. Strukturanalyse dann 2. Zeitanalyse
* Kommunikationsdiagramm (raumorientiert):
  * ![Beispiel Dreiecksform](https://www.bwl-betriebswirtschaft.de/gfx/raumdiagramm-komunikationsmatrix.jpg "Kommunigram Dreiecksform")
    * z.B. Verteilung der Räume im Büro
  * Kreisform
    * viel Kommunikation durch dicke Striche makiert

#### Netzplan

* Knoten:

| FAZ |      |               |      | FEZ |
| :-: | :--- | :------------ | :--- | :-- |
|     | \|Nr | \|BEZEICHNUNG |      | \|  |
|     | \|D  | \|GP          | \|FP | \|  |
| SAZ |      |               |      | SEZ |

* FAZ : Frühster Anfangszeitpunkt
* D: Dauer
* FEZ: Frühster Endzeitpunkt
* SAZ: Spätester Angfangszeitpunkt
* SEZ: Spätester Endzeitpunkt
* GP: Gesamtpuffer
* FP: Freier Puffer

1.  Vorwärtsrechnung
    * Startknoten FAZ = 0
    * FEZ = FAZ + Dauer
2.  Rückwärtsrechnung
    * FEZ Zielknoten = SEZ Zielknoten
    * SAZ = SEZ - Dauer
    * SAZ = SEZ aller Vorgänger
3.  Berechnung der Gesamtpufferzeiten
    * GP = SAZ - FAZ
4.  Berechnung der freien Pufferzeiten
    * FP = FAZ des Nachfolgers - FEZ
5.  Darstellung kritischer Weg
    * Vorgänge die FP und GP = 0 haben

#

## Lagerverwaltung

Definition: Unter Lager versteht man den Ort, an dem Ware auf Vorrat aufbewahrt wird. Ein Lager ist dann nötig, wenn zwischen den Materialabgängen und -zugängen ein zeitlicher Unterschied besteht.

### Funktionen:

* Koordinationsfuncktion zwischen Materialzugang und -abgang
* Sicherungsfunktion (z.B. Reserven)
* Spekulationsfunktion, wenn Waren z.B. im Preis schwanken
* Veredelungsfunktion, wenn Waren mit Zeit wertvoller werden (z.B. Wein)

**Just-in-time-Beschaffung** wenn die Materialzugänge und -abgänge exakt aufeinander abgestimmt sind

Bei Einführung oder Modifizierung von Produkten muss eine **Materialbedarfsplanung** durchgeführt werden. Zwei Verfahren sind üblich:

* programmgebundene Bedarfsplanung:
  * Bedarf wird anhand Stücklisten errechnet
  * bei teuren Bauteilen
* verbauchsorientierte Materialbedarfsplanung:
  * Menge wird aus bisherigem Materialverbauch _abgeleitet_
  * Mithilfe von _Materialentnahmescheinen_ wird versucht eine Aussage über den zukünftigen Verbrauch zu machen
  * bei weniger wertvollen Gütern (Roh- & Hilfsstoffe)

### ABC-Analyse

Hilft zur Bestimmung des Verfahrens für die Materialbedarfsplanung. Die Güter werden in A (wichtig) über B (mittel) bis hin zu C (unwichtig) Güter getrennt.

Folgende Grundsätze gelten (gemessen am Lagerbestan):

* **A-Güter**:
  * geringer Mengenanteil
  * hoher Wertanteil
  * Verfahren: programmgebundene Materialbedarfsplanung
* **B-Güter**:
  * geringerer Wertanteil als A-Güter
  * geringerer Mengenanteil als C-Güter
  * Vorgabe für Verfahren durch Unternehmensleitung
* **C-Güter**:
  * sehr geringer Wertanteil
  * hoher Mengenanteil
  * Verfahren: verbrauchsorientierte Materialbedarfsplanung

#### Vorgehensweise zur Bestimmung:

Vorraussetzung: Materialliste (Artikel|Menge|Preis)

1.  Materialliste wertmäßig erweitern
    * [Artikel | Menge | Preis | Verbauch | %-Anteil]
    * Verbrauch = Menge \* Preis
    * Anteil = (Verbauch des Arikels) / (Summe Verbauch aller Artikel)
2.  Liste nach Verbrauch sortieren:
    * teuerster Artikel zuerst
3.  %-Anteil kumulieren
4.  Anhand des Kum. %-Anteils klassifizieren
    * Vorgaben vom Unternehmen beachten

_Achtung_: Wenn Grenze für A 75% ist, wird ab 75,5% aufgerundet, d.h. bis einschließlich 75,4% ist es noch Klasse A sonst B.

_INFO_: ABC-Analyse wird auch bei der Bildung von Kundengruppen angewandt, die dann unterschiedlich stark betreut werden. Oder auch Lieferanten, die mit einem Unternehmen zusammenarbeiten.

### Ergebnis einer Materialbedarfsplanung

Ergebnis ist die Berrechnung des _Bruttobedarfs_. Um die tatsächliche Bestellmenge (= _Nettobedarf_) zu erhalten, muss man vom Bruttoberf den Lager-, Bestell- und Werkstattbestand abzeihen. Zusatzbedarf (für die Forschung z.B.) muss dementsprechen ergänzt werden.

### Optimaler Bestellzeitpunkt

Faktoren:

* Kapazität des Lagers
* Kosten durch Lagerung
* Rabatte durch große Bestellmengen
* Kosten für die Bearbeitung von Bestellungen sinken bei großen Bestellmengen

Verfahren:

* **Bestellpunktverfahren**
  * Sicherheitsbestand festlegen
  * Meldebestand errechnen:
    * **Meldebestand** = Täglicher Verbauch \* Lieferzeit in Tagen + Sicherheitsbestand
  * Bestellung aufgeben, wenn Materialbestand = Meldebestand ist.
* **Bestellrythmusverfahren**
  * Material wird zu bestimmten Terminen geordert
  * Lager wird bis zu bestimmten Bestand gefüllt

**Kommissionierung** ist die Zusammenstellung von Artikeln zu einem Auftrag.

### Lagerkennziffern

#### durchschnittlicher Lagerbestand:

* monatlich:
  * (Anfangsbestand + 12 Monatsbestände) / 13
* jährlich:

  * (Anfangsbestand + Endbestand) / 2

* Wert:
  * durschnitt. Lagerbestand \* Einstandspreis

#### Wareneinsatz

* Anfangsbestand + Lagerzugänge - Endbestand

#### Umschlagshäufigkeit

Wie oft ist der Lagerbestand verkauft worden.

* Wareneinsatz / durschnittlicher Lagerbestand

#### durschnittliche Lagerdauer

Wie lange liegt Ware durschnittlich im Lager

* 360 / Umschlagshäufigkeit

#### Lagerzinssatz und Lagerzinskosten

Zinsverlust durch das in den Lagervorräten gebundene Kapital

* Lagerzinssatz = (Jahreszinssatz \* durschnittliche Lagerdauer) / 360
* Lagerzinskosten = Lagerzinssatz \* Wert des durchschnittlichen Lagerbestands

#

## Geschäftsprozesse

Definition: Ein Geschäftsprozess ist eine Folge von Tätigkeiten, die ein bestimmtes Ergebnis anstreben. Die Summe der Geschäftsprozesse spiegelt die Aufgaben des Unternehmens wider.
Geschäftsprozesse werden durch den Auftrag eines internen oder externen Kundens ausgelöst.

Ziel der Modellierung:

* Optimierung der Arbeitsabläufe

**Kernprozesse** dienen der Wertschöpfung des Unternehmens.
Beispiele:

* Innovationsprozesse
* Beschaffungsprozesse
* Fertigungsprozesse
* Absatzprozess

**Unterstützungsprozesse** dienen dem Management und Support des Unternehmens. Beispiele:

* Personalwesen
* Lagerhaltung
* Buchhaltung
* Führung des Unternehmens

Visualisiert werden Geschäftsprozesse durch **ereignisgesteuerte Prozessketten** (EPK).
