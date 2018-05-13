# Funktionen

* Funktionen sind Unterprogramme die Daten verarbeiten und Werte zurückgeben können
* Aus der Hauptfunktion __main()__ können Unterfunktionen aufgerufen werden
* Ruft ein Programm eine Funktion auf, springt die Ausführung zur Funktion und fährt nach Abschluss der Funktion auf der Zeile des Aufrufs fort

## Gründe für Funktionen

* Übersichtlichkeit des Quellcodes
* Wartbarkeit des Quellcodes wird verbessert
* Effizienz des Quellcodes durch mehrfache Verwendbarkeit
* Compiler kann Programm genauer auf Fehler überprüfen

## Definition

Eine Funktionsdefinition besteht aus Rückgabetyp, Funktionsname, Parameterliste und Anweisungsblock.

Funktionsprototyp:
```c
Rückgabetyp Funktionsname(Parametertyp1, Parametertyp2, ...);
```
* Prototypen werden vor der __main()__ gesetzt
* Teilt dem Compiler den Rückgabetyp und die Parametertypen mit
* Compiler kennt nun die Funktion
* Bessere Fehlerbehandlung

Definition der Funktion mit Anweisungsblock:
```c
Rückabetyp Funktionsname(Paramtertyp1 Parameter1, Parametertyp2 Parameter2, ...)
{
    lokale Vereinbarung;
    Anweiungen;
    return (Ergebnis);
}
```
* Rückgabetyp kann jeder gültige Typ sein, wird keiner angegeben ist es _int_
* Bei Funktionen die keinen Wert liefern, benutzt man den Rückgabetyp _void_
* Paramterliste besteht aus Typ und Name der übergebenen Werte
* _return_ dient zur Rückgabe eines Wertes und beendet die Funktion
* _return_ ohne Ausdruck beendet Funktion ohne Rückgabewert
* Variablen die im Anweisungsblock erstellt werden, sind auch nur in der Funktion verfügbar

Funktionsaufruf:

```c
Funktionsname(Parameter1, Parameter2, ...);
```

## Beispiele aus dem Unterricht:

* Währungsrechner III
* Volumen und Oberfläche einer Kugel in gesonderten Funktionen
* Mathematische Funktionen
* Kreditberechnung
* Fläschenrechner
* Süßigkeitenautomat


# Felder (engl. Array)

Ein Array ist eine gruppierten Anzahl von Speicherstellen des gleichen  Datentyps, die durch den Index unterschieden werden.

## Defintion

```c
Datentyp Name[Anzahl Elemente]; 

double temperatur[30];

oder

double temperatur[30] = {Wert1, Wert2, ..., Wert30};
```
* Definition durch eckige Klammern ([]) mit Anzahl der Elementen
* Alle Felder beginnen mit Index __0__
* Feldelemente werden über den Index angesprochen (z.B. temperatur[__3__])
* Feldgrenzen werden von C nicht überprüft. Programmierer ist dafür verantwortlich, dass die Felder groß genug für alle Elemente sind
* Das Überschreiten von Feldgrenzen kann andere Variablen zerstören

### Beispiele aus dem Unterricht:

* Tag des Jahres
* Zahlenraten
* Sortieren von Zahlenreihen
* Rechnungsposten
* Additionsprogramm mit Arrays
* Lottozahlengenerator
* Schiffe versenken

# String

Ein String ist nichts anderes als ein Feld aus __char__-Werten, da es in C keinen Datentyp speziell für Strings gibt. Zeichenketten sind das weitaus häufigste Einsatzgebiet für Felder.

## Definition

```c
char text[10] = {'H','a', 'l', 'l', 'o', '!', '\0'};

oder 

char text[10] = "Hallo!" //Endemarkierung durch Compiler
```
* Endemarkierung eines Strings: ``` '\0' ```
* Endemarkierung siganlisiert dem Programm das Ende eines Strings, auch wenn nicht alle vorhandenen Speicherplätze der Zeichenkette benutzt wurden
* _%s_ zur Ausgabe von Zeichenketten durch _printf()_

Opertionen mit Strings werden über die Feldelemente durchgeführt.
Durch das Einbinden der Bibliothek _string.h_ werden viele Funktionen zum bearbeiten von Strings bereitgestellt.

Beispiele aus dem Unterricht:

* Eingabezeichen
* Textauswertung
* Palindrom
* Brotmonate 
* Schleifenprogrammierung
