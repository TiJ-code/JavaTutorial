# Java 02
### Variablen


## `int` Datentyp

In Java, wird der primitive Datentyp `int`
benutzt um Ganzzahlen zu speichern.
Was bedeutet du kannst alle positiven,
negativen und 0 speichern.

```java
int negative = -999;
int zero     = 0;
int positive = 1230;
```






## `boolean` Datentyp

In Java, wird der primitive Datentyp `boolean`
benutzt um die Werte `true` oder `false`
zu speichern.

```java
boolean yes = true;
boolean no  = false;
```






## `char` Datentyp

In Java, wird der Datentyp `char` verwendet,
einen einzigen Character zu speichern.
Der Character muss in single Quotes (')
gespeichert werden.

```java
char character = 'y'
```






## Primitive Datentypen

In Java sind die Basic Datentypen als Primitive
Datentypen bekannt und sind dort auch normalerweise
verwendet.

Bsp:
- int
- char
- boolean
- byte
- long
- short
- double
- float

`null` ist ebenfalls einer, aber dieser kann nur
den Wert `null` speichern.






## Strings

Ein String in Java ist ein Object, welcher
mehrere Character behinhalten kann.
Es ist kein primitiver Datentyp.

Ein String kann erstellt werden, indem man
Character zwischen double quotes (") schreibt.

Um Strings zu vergleichen, wird die `equals()` 
Methode verwendet, anstatt der Primitive
Gleichheitsoperator `==`.

```java
// Erstellen einer String variable
String name = "Bob"

// Die folgende Zeile wird "false" ausgeben, da
// Strings auf die Schreibweise achten.
// (Case Sensitive)
System.out.println(name.equals("bob"))
```






## Static Typing

In Java, der Typ der Variable wird beim
compilen gecheckt. Dies ist auch als
`static typing` bekannt. Es hat den
Vorteil, dass Fehler bereits schon
beim compilen erkannt werden, und nicht
auftreten wenn das Programm schon läuft.

Variablen müssten mit dem passenden
Datentyp deklariert werden, oder das
Programm wird nicht ausführen.

```java
int i   = 10;  // typ ist int
char ch = 'a'; // typ ist char

j = 20; // wird nicht compilen, da kein typ
char name = 'Paul' // wird nicht compilen, da
                   // kein Typ
```






## Schlüsselwort `final`

Der Wert einer Variable kann nicht nicht
geändert werden, wenn diese als mit dem
`final` Keyword deklariert wurde.

Vergiss nicht, dass Variablen einen Wert
haben müssen, wenn sie mit `final`
deklariert werden.
`final` Variablen können nicht geändert
werden. Jeder versucht dies zu erreichen
wird in einer Fehlermeldung enden.

```java
// Wert kann nicht verändert werden.
final double Pi = 3.14
```






## double Datentyp

Der primitive Datentyp `double` wird
verwendet um dezimal Zahlen zu speichern.

```java
double PI = 3.14
double price = 5.75;
```






# Extras

## Mathematische Operatoren

Einfache Mathematik kann mit den
Datentypen `int`, `double` und
`float` angewandt werden:

- `+` Addition
- `-` Subtrahierung
- `*` Multiplikation
- `/` Division
- `%` Modulo (gibt den Rest wieder)

Diese Operatoren funktionen nicht auf
anderen Datentypen.

```java
int a = 20;
int b = 10;

int result;

result = a + b; // 30
result = a - b; // 10
result = a * b; // 200
result = a / b; // 2
result = a % b; // 0
```






## Vergleichsoperatoren

Vergleichsoperatoren können genutzt werden,
um zwei Werte zu vergleichen

- `>` größer als
- `<` kleiner als
- `>=` größer gleich
- `<=` kleiner gleich
- `== ` gleich
- `!=` nicht gleich

Diese werden von Primitiven Datentypen
unterstützt und das Ergebnis dieser
Vergleiche ist ein Boolean der den
Wert `true` oder `false` hat.


```java
int a = 5;
int b = 3;

boolean result = a > b;
// result hat nun den Wert `true`
```






## Zusammengesetzte Zuweißungsoperatoren

Zusammengesetzte Zuweißungsoperatoren können
verwendet werden um den Wert einer Variable
zu ändern oder neuzuzuweißen in einer Zeile
Code.

Zusammengesetzte Zuweißungsoperatoren sind:
- `+=` vergrößern um
- `-=` verkleinern um
- `*=` mal
- `/=` durch
- `%=` überig

```java
int number = 5;

// 5 + 3 = 8
number += 3; // Wert ist nun 8
// 8 - 4 = 4
number -= 4; // Wert ist nun 4
// 4 * 6 = 24
number *= 6; // Wert ist nun 24
// 24 / 2 = 12
number /= 2; // Wert ist nun 12
// 12 % 5 = 7
number %= 7; // Wert ist nun 5
```






## Vergrößerungs und Verkleinerungsoperatoren

Der Vergrößerungsoperator, (`++`), kann
den Wert einer Zahlen-basierten variable
um `1` erhöhen, während der
Verkleinerungsoperator, (`--`), eine
Variable um den Wert von `1` verkleinern
kann.

```java
int numApples = 5;
numApples++;  // Wert ist nun 6

int numOranges = 5;
numOranges--; // Wert ist nun 4
```






## Reihenfolge der Operatoren

Die Reihenfolge in welcher, in einer
Rechnung mit mehreren Operatoren,
berechnet werden ist festgelegt:

- `Klammern`
- `Multiplikation`
- `Division`
- `Modulo`
- `Addition`
- `Subtrahierung`
