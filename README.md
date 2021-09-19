# Java 03
### Objektorientiertes Java


## Zustand und Verhalten von Java Objekten

In Java, sind Instanzen einer Klasse
bekannt als Objekte.
Jedes Objekt hat Zustand und Verhalten in
Form von Instanzfeldern bzw. Methoden.

```java
public class Person
{
	// Zustand eines Objekts
	int age;
	String name;

	// Verhalten eines Objekts
	public void set_value()
	{
		age = 20;
		name = "Robin";
	}
	public void get_value()
	{
		System.out.println("Alter ist " + age);
		System.out.println("Name ist "+ name);
	}

	// Main Methode
	public static void main(String[] args)
	{
		// erstellet ein neues Person Objekt
		Person p = new Person();

		// ändert den Zustand durch Verhalten
		p.set_value()
	}
}
```






## Java Instanz

Java Instanzen sind Objekte welche auf Klassen 
basieren.
Als Beispiel, `Bob` könnte eine Instanz der Klasse
`Person` sein.

Jede Instanz hat Zugriff auf seine eigenen Variablen
welche als Instanzfelder bekannt sind. Das sind
Variablen, die im Arbeitsbereich der Instanz
deklariert sind.

```java
public class Person
{
	int age;
	String name;

	// Constrctor Methode
	public Person(int age, String name)
	{
		this.age = age;
		this.name = name;
	}

	// Main Methode
	public static void main(String[] args)
	{
		Person Bob = new Person(31, "Bob");
		Person Alice = new Person(27, "Alice");
	}
}
```






## Java Dot Notation

In der Java Programmiersprache, benutzt man einen
`.` um Zugriff auf die Variablen und Methoden
eines Objektes oder einer Klasse zu haben.

Das ist bekannt als Dot Notation und die Struktur
sind folgendermasen aus:

`instanzOderKlassenname.fieldOderMethodenName`

```java
public class Person
{
	int age;

	public static void main(String[] args)
	{
		Person p = ner Person();

		// Hier nutzen wir die Dot Notation
		// um das Alter zu verändern
		p.age = 20;

		System.out.println("Alter ist " + p.age);
		// Output: Alter ist 20
	}
}
```






## Constructor Methode in Java

Java Klassen beinhalten eine
Construktor Methode welche benutzt
wird um Instanzen der Klasse zu erstellen.

Der Constructer heißt genauso wie die klasse.
Wenn kein Constructor definiert ist, wird
ein leerer Constructor verwendet.

```java
public class Maths
{
	public Maths()
	{
		System.out.println("Ich bin ein Constructor")
	}

	public static void main(String[] args)
	{
		System.out.println("Ich bin die Main Methode")
		Maths obj = new Maths();
	}
}
```






## Erstellen einer neuen Klasseninstanz in Java

In Java verwenden wir das `new` Keyword gefolgt
von einem Aufruf des Klassenconstructor, um
eine Instanz der Klasse zu erstellen.

Der Constructor kann genutzt werden, um
Anfangswerte für Instanzfields bereit-
zustellen.

```java
public class Person
{
	int age;

	// Constructor:
	public Person(int a)
	{
		age = a;
	}

	public static void main(String[] args)
	{
		// Hier erstellen wir eine Instanz
		// Person Klasse
		Person p = new Person(20);
		System.out.println("Alter ist " + p.age);
		// Output: Alter ist 20
	}
}
```






## Referenzdatentypen

Eine Variable mit einem Referenzdatentyp
hat einen Wert, der auf die Speicheradresse
einer Instanz verweist.
Bei der Variablendeklaration wird der Klassenname
als Typ der Variablen verwendet.

```java
public class Cat
{
	public Cat()
	{

	}

	public static void main(String[] args)
	{
		// garfield ist mit dem Referenzdatentyp
		// `Cat` deklariert
		Cat garfield = new Cat();
		System.out.println(garfield);
		// Output: Cat@76ed5528
	}
}

```






## Constructor Signaturen

Eine Klasse can mehrere Constructors beinhalten,
solange diese verschiedene Parameter Werte haben.
Eine Signatur hilft dem Compile zwischen
den Constructors zu unterscheiden.

```java
// Die Signature ist 'Cat(String furLength, boolean hasClaws)'
public class Cat
{
	String furType;
	boolean containsClaws;

	public Cat(String furLength, boolean hasClaws)
	{
		furType = furLength;
		containsClaws = hasClaws;
	}

	public static void main(String[] args)
	{
		Cat garfield = new Cat("Langhaar", true);
	}
}
```






## `null` Werte

`null` ist ein spezieller Wert welcher
beschreibt dass ein Objekt keine bzw.
eine `void` Referenz hat.

```java
public class Bear
{
	String species;

	public Bear(String speciesOfBear)
	{
		species = speciesOfBear;
	}

	public static void main(String[] args)
	{
		Bear baloo = new Bear("Sloth Bär");
		System.out.println(baloo);
		// Output: Bear@4517d9a3

		baloo = null; // setzte Objekt zu `null`
		System.out.println(baloo);
		// Output: null
	}
}
```






# Extras

## Deklarieren einer Methode

Methodendeklarationen sollten die
folgenden Methodeninformationen
definieren:

scope (`private` oder `public`),
return typ,
Methodenname,
Parameter

```java
// Hier ist eine `public` Methode
// mit dem Namen `sum` deren return
// type ein      `int` und zwei Paramter 
// namens        `a` & `b` besitzt.
public int sum(int a, int b)
{
	return (a + b);
}
```






## Der Body einer Java Methode

In Java benutzt man geschweifte Klammern `{}` um
den Body einer Methode einzuschließen.

Die Statements welche in den `{}` sind, werden
dann ausgeführt, wenn die Methode ausgerufen wird.

```java
public class Maths
{
	public static void sum(int a, int b)
	{ // Beginn von `sum`
		int result = a + b;
		System.out.println("Summe ist " + result);
	} // Ende von `sum`

	public static void main(String[] args)
	{
		// Hier rufen wir die Methode `sum` auf
		sum(10, 20);
		// Output: Summe ist 30
	}
}
```






## Java Variablen in einer Methode

Java Variablen die in einer Methode definiert
werden, können nicht außerhalb dieser Methode
verwenden.

```java
public class Maths
{
	public static void main(String[] args)
	{
		int i, j;
		System.out.println("Diese zwei Variablen sind nur in der Main Methode");
	}
}
```






## Rückgabe von Informationen von einer Java Methode

Eine Java Methode kann jeden Wert zurückgeben,
welcher auch in einer Variable gespeichert werden
kann.
Der Wert der zurückgegeben wird, muss aber dem
Return Type der Methode entsprechen.

Der Wert wird mit dem Keyword `return` zurückgegeben.

```java
public class Maths
{
	// return type ist int
	public int sum(int a, int b)
	{
		int k;
		k = a + b;
		// Die Methode `sum` gibt durch das Keyword
		// `return` etwas zurück
		return k;
	}

	public static void main(String[] args)
	{
		Maths m = new Maths();
		int result;
		result = m.sum(10, 20);
		System.out.println("Summe ist " + result);
		// Output: Summe ist 30
	}
}
```






## Methodenparameter in Java

In Java sind Parameter in der Methodendefinition
deklariert. Die Parameter agieren als Variablen
in der Methode und halten den Wert der eingetragen
wurde. Diese können in einer Methode für das
Ausgeben oder Rechnen verwendet werden.

Im Beispiel sind 'a' und 'b' zwei Parameter,
die beim Aufruf Methode den Wert 10 bzw. 20 enthalten.

```java
public class Maths
{
	public int sum(int a, int b)
	{
		int k = a + b;
		return k;
	}

	public static void main(String[] args)
	{
		Maths m = new Maths();
		int result = m.sum(10, 20);
		System.out.println("Summe ist " + result);
		// Output: Summe ist 30
	}
}
```
