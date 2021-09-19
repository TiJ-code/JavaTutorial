# Java 05
### Arrays und ArrayLists

## Index

Ein Index bezieht sich auf die Position
eines Elements innerhalb eines Arrays.

Der Index eines Arrays beginnt bei 0
und reicht bis eins weniger als die
Gesamtlänge des Arrays.

```java
int[] marks = {50, 55, 60, 65, 70, 75, 80};

System.out.println(marks[0]);
// Output: 50

System.out.println(marks[4]);
// Output: 70
```






## Arrays

In Java wird ein Array verwendet, um eine
Liste von Elementen desselben Datentyps
zu speichern.

Arrays haben eine feste Größe und ihre
Elemente sind geordnet.

```java
// Erstellen eines Arrays mit 5 int Elementen.
int[] marks = {10, 20, 30, 40, 50};
```






## Erstellen eines Arrays in Java

In Java kann ein Array auf folgende Weise
erstellt werden:

- Verwende die Notation `{}`, indem
  man jedes Element auf einmal
  hinzufügt.
- Verwende das Keyword `new` und
  weise jede Position des Arrays
  einzeln zu.

 ```java
 int[] age = {20, 21, 30};

 int[] marks = new int[3];
 marks[0] = 50;
 marks[1] = 70;
 marks[2] = 93;
 ```






## Ändern eines Elementen Wertes

Um ein Elementen Wert zu ändern, wähle das
Element über den Index und verwende den
Zuweisungsoperator um den neuen Wert zu
setzen.

```java
int[] nums = {1, 2, 0, 4};

// Ändern des Werts am Index auf 2
nums[2] = 3;
```






## Java Arraylist

In Java wird eine ArrayList verwendet,
um eine dynamische Liste darzustellen.

Während Java-Arrays eine feste Größe
haben (die Größe kann nicht geändert
werden), bietet eine ArrayList
Flexibilität, indem sie Elemente sowohl
hinzufügen als auch entfernen kann.

