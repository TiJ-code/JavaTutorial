# Java 01
### Hello World


## Klassen

Eine Klasse repräsentiert ein "single concept".
Ein Java Programm muss eine Klasse mit dem Selben
Namen des Programms besitzten.

Beispiel:

```java
public class Person()
{
	public static void main(String[] args)
	{
		System.out.println("Ich bin eine Person!");
	}
}
```

Die Klasse Person muss auch in der Programmdatei
namens Person.java sein.






## main() Methode

Jedes Java Programm muss die 'main()' Methode be-
inhalten, denn die ist der Eingangspunkt für das
Programm. Alle anderen Methoden werden dann von
hier aus aufgerufen.

Zum erstellen einer Main-Methode schreibt man

```java
public static void main(String[] args) {}
```

Außerdem akzeptiert diese Methode ein
einziges Argument, ein Array aus Elementen
des Typen 'String'.






## PrintLn

Mit dem Befehl:

```java
System.out.println("");
```

kann man einen Text in die Konsole ausgeben.
Hierbei besteht der Befehl aus drei bereichen:

*System*  : Ist die Core Bibliothek von Java
*out*     : Ist ein Object, welches den Output
		    kontrolliert.
*pintln()*: Ist die Methode, welche als einziges
			Argument in die Konsole ausgibt.






## Kommentare

Kommentare sind Zeichenfolgen welche vom Compiler
ignoriert werden.
Diese werden benutzt um die verständlichkeit
des Programms beizuhelfen.

`//    `: Singleline Comment
`/* */ `: Multiline Comment






## Whitespace

Der Abstand zwischen zwei Ausgaben wird ignoriert.

Bsp:
```java
System.out.println("Example 1")



System.out.println("Example 2")

// Output
// Example1
// Example2
```






## Compiling Java

Wenn man in Java ein Programm compiled
wird jede einzelne Klasse (.java) in
einen .class Datei konvertiert.
Welche auch bekannt als Bytecode ist.

Die Java Virtual Machine kann diesen
dann auf jedem Betriebssystem ausführen.






## Statements

In Java ist ein Statement eine Zeile
des Codes, welches einen Task
ausführt und mit einem ';' abgeschlossen
wird.
