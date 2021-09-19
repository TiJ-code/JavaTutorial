# Java 04
### Bedingungen und Kontrollfluss


## if Statements

Ein `if` Statement führt einen Code-Block
aus, wenn eine spezielle Condition als
wahr gewertet wird.

```java
if(true)
{
	System.out.println("Diese Code wird ausgeführt");
}
// Output: Dieser Code wird ausgeführt

if(false)
{
	System.out.println("Diese Code wird nicht ausgeführt");
}
// Es gibt keinen Output für das Statement darüber
```






## else Statements

Ein `else` Statement führt einen Code-Block
aus, wenn eine Condition eines `if`-Statements
`false` ist.
Das `else` Statement wird immer die letzte Bedingung.

```java
boolean condition1 = false;

if(condition1)
{
	System.out.println("condition1 ist true");
}
else
{
	System.out.println("condition1 ist nicht true")
}
// Output: condition1 ist nicht true
```






## else if Statements

`else`-`if` Statements können zusammengehängt
werden um mehere Conditions zu checken.
Wenn eine Condition `true` ist, wird ein Code-Block
ausgeführt und Condition wird verlassen.

Es können auch mehrere `else`-`if` Statements
in einem einfachen Statement verwendet werden.

```java
int testScore = 76;
char grade;

if(testScore >= 90)
{
	grade = 'A';
}
else if(testScore >= 80)
{
	grade = 'B';
}
else if(testScore >= 70)
{
	grade = 'C';
}
else if(testScore >= 60)
{
	grade = 'D';
}
else
{
	grade = 'F';
}

System.out.println("Note ist " + grade);
// Output: C
```






## Verschachtelte Conditional Statements

Ein Verschachteltes Conditional Statement ist ein
conditional Statement verankert in einem anderen
conditional Statement. Das äußere Statement wird
zuerst ausgeführt; wenn die Condition `true` ist,
dann wird das Verschachtelte Conditional Statements
ausgeführt.

```java
boolean studied = true;
boolean wellRested = true;

if(wellRested)
{
	System.out.println("Viel Glück!");
	if(studied)
	{
		System.out.println("Du bist für die Prüfung vorbereitet!");
	}
	else
	{
		System.out.println("Lerne vor deiner Prüfung");
	}
}

// Output: Viel Glück!
// Output: Du bist für die Prüfung vorbereitet!
```






## AND Operator

Der logische Operator UND (bzw. AND) wird von
`&&` repräsentiert. Dieser Operator gibt `true`
zurück wenn die `boolean`'s auf beiden Seiten
`true` sind. Andernfalls gibt er `false` zurück.

```java
System.out.println(true && true);
// Output: true
System.out.println(true && true);
// Output: false
System.out.println(false && true);
// Output: false
System.out.println(false && false);
// Output: false
```






## NOT Operator

Der logische Operator NICHT (bzw. NOT) wird von
`!` repräsentiert. Diese Operator invertiert
den Wert eines Booleans.

```java
boolean a = true;

System.out.println(!a);
// Output: false

System.out.println(!false);
// Output: true
```






## OR Operator

Der logische Operator ODER (bzw. OR) wird von
`||` repräsentiert. Der Operator wird `true`
zurück geben wenn wenigstens einer der Booleans
`true` ist; Andernfalls gibt er `false` zurück.

```java
System.out.println(true || true); 
// Output: true
System.out.println(true || false);
// Output: true
System.out.println(false || true);
// Output: true
System.out.println(false || false); 
// Output: false
```






## Conditional Operatoren - Reihenfolge

Wenn ein Ausdruck mehrere Bedingunsoperatooren
enthält, ist die Reihenfolge wie folgt:

- Klammern
- NOT
- AND
- OR

```java
boolean foo = true && (!false || true); // true

/**
 * (!false || true)
 * wird zuerst ausgewertet,
 * da es in Klammern steht.
 * 
 * Danach wird
 * !false
 * als true ausgewertet, da es
 * den NOT Operator nutzt
 * 
 * Hiernach
 * (true || true)
 * als true.
 * 
 * Zuletzt wird
 * true && true
 * als true ausgewertet.
 * Was bedeutet foo ist true.
 **/
```
