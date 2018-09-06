# Zahlensysteme

### Dezimalsystem

    1984 = 1 x 1000 + 9 x 100 + 8 x 10 + 4 x 1

Basis: 10

Ziffern: 0,1,2,3,4,5,6,7,8,9

### Dual/Binärsystem

    10011 = 1 x 2^4 + 0 x 2^3 + 0 x 2^2 + 1 x 2^1 + 1 x 2^0
          = 16 + 2 + 1 = 19(10)

Basis: 2

Ziffern: 0,1

### Hexadezimalsystem

    2AC = 2 x 16^2 + 10 x 16^1 + 12 x 16^0
        = 2 x 265 + 10 x 16 + 12 x 1 = 684(10)

Basis: 16

Ziffern: 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F

### Oktalsystem

    456 = 4 x 8^2 +  5 x 8^1 + 6 x 8^0
        = 4 x 64 + 5 x 8 + 6 x 1 = 302(10)

Basis: 8

Ziffern: 0,1,2,3,4,5,6,7

## Umwandlung einer Zahl Dezimal - Dual

### Subtraktionsverfahren

Man subtrahiert mit der größten 2er-Potenz die passt.

     2er Potenzen:  64  32  16  8   4   2   1
                    1   0   1   1   0   0   1
        89          |       |   |           |
    -   64 ---------+       |   |           |
                            |   |           |
        25                  |   |           |
    -   16------------------+   |           |
                                |           |
        9                       |           |
    -   8-----------------------+           |
                                            |
        1                                   |
    -   1-----------------------------------+

    89(10)=1011001(2)

### Divisionsmethode

Man teilt durch 2 und schaut auf den Rest, bis das Ergebnis 0 ist.

    89 : 2 = 44     Rest 1  ^
    44 : 2 = 22     Rest 0  |       Von unten nach oben
    22 : 2 = 11     Rest 0  |       lesen!
    11 : 2 = 5      Rest 1  |
    5  : 2 = 2      Rest 1  |
    2  : 2 = 1      Rest 0  |
    1  : 2 = 0      Rest 1  |

## Zusammenhang zwischen Hex - Binär/Dual - Oktal

    Idee:
    16 = 2x2x2x2 => 4 Stellen
    8  = 2x2x2   => 3 Stellen

    0 1 0 1 | 1 0 1 1 | 1 1 0 1 => 5BD(16)
    8 4 2 1   8 4 2 1   8 4 2 1

Man bildet von rechts kommend 4er-Gruppen und wandelt jede Gruppe für sich mit 8-4-2-1 um.
In Oktal dann entsprechend in 3er-Gruppen mit 4-2-1.

    0 1 0 | 1 1 0 | 1 1 1 | 1 0 1 => 2675(8)
    4 2 1   4 2 1   4 2 1   4 2 1

| OKT  |     BIN      | HEX |
| :--: | :----------: | :-: |
| 456  |  100101110   | 12E |
| 1273 |  1010111011  | 2BB |
| 664  | 000110110100 | 1B4 |

## Dartellung von Zahlen < 1

Achtung: Nachkommastellen sind nicht zu 100% darstellbar, der Computer rundet.

    Dezimal zum Vergleich:
    3,275
    => 3 x 10^0 + 2 x 10^-1 + 7 x 10^-2 + 5 x 10^-3

    Binär:
    1,1011
    => 1 x 2^0 + 1 x 2^-1 + 0 x 2^-2 + 1 x 2^-3 + 1 x 2^-4

    => 1       + 0,5      + 0        + 0,125    + 0,0625
    => 1,6875(10)

### Umwandlung einer Dezimal < 1 nach Dual

#### Subtraktionsverfahren

    0,5     0,25    0,125   0,0625  0,03125
    0       1       1       0       1

        0,40625 = 0,01101(2)
    -   0,25000

        0,15625
    -   0,12500

        0,03125
    -   0,03125

        0

#### Multiplikationsverfahren

    0,40625 x 2 =| 0 |,8125

    0,8125  x 2 =| 1 |,625         von oben

    0,625   x 2 =| 1 |,25          Dualzahl ablesen

    0,25    x 2 =| 0 |,5

    0,5     x 2 =| 1 |,0 <-- ENDE

## Rechnen im Dualsystem

### Addition

        1101110             Merke:
    +   1011100                     1+1 = 10(2)
        1 11   <--Übertrag        1+1+1 = 11(2)
       11001010

### Subtraktion

        1001010
    -   0110100
        11 1   <--Übertrag
        0010110
         |  |
         |  +--> von 1 bis 10 = 1
         |                          Merke!
         +-----> von 2 bis 10 = 0

## Darstellung negativer Zahlen

- Negative Zahlen werden im Zweierkomplement dargestellt. Vorteil: Nur eine Null, Rechenregeln funktionieren

- Bildung des Zweierkomplements:

  1. Alles invertieren 0 -> 1 & 1 -> 0
  2. Eine 1 addieren

Beispiel:

                    0001 = +1        0111 = +7
    Invertieren     1110             1000
    1 addieren     +0001            +0001
                    1111 -1          1001 = -7

Wichtig! Datentypen vereinbaren (Bitstellen und Vorzeichen)

Betragszahlen: 'unsigned' damit nur positiv dargestellt wird

Zweierkomplement: 'signed' (Defaultwert) damit positiv/negativ dargestellt wird

## Dezimalpräfixe/Binärprefixe

Achtung! Prüfungsrelevant!

8 Bit = 1 Byte

2^8 = 256 Kombinationen (Anzahl möglicher Zeichen/Stellen)

|                       |     |
| :-------------------: | :-: |
| 2^10 = 1024 Ki (KiBi) |     |
