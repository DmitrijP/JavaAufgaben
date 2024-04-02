# Einstieg in die Java Entwicklung
Hier werden die Basics der Java Entwicklung beschrieben. 

## Kommentare

Kommentare in Java werden mit einem `//`gestartet. Diese Teile des Programcodes werden nicht ausgeführt und dienen dazu das Program zu beschreiben.
Beispiel:
```java
// dies ist ein Kommentar
// dies auch
```

## Programmeinstieg

Ein Java Programm beginnt mit der folgenden Datei.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int i = 0;
  }
}
```
Dies ist die **Main-Klasse**, sie enthällt die **main**-Methode nach der die JRE (Java Runtime Environment) beim Programmstart sucht.
Der Ausdruck `public static void main(String[] args)` ist der Start unseres Programes. Innerhalb der geschweiften Klammern schreiben wir unser Program. 

## Variablen
Jede Programmiersprache verwendet Variablen. Variablen sind Speicherbereiche für unsere Daten mit denen unser Program arbeitet.

### Variablendeklaration
Eine Variablendeklaration besteht aus dem *Datentyp*, dem *Variablennamen*.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Datentyp: int
      //Variablenname: meineVar
      int meineVar;
  }
}
```
Durch diesen Ausdruck `int meineVar;` sagen wir unserem Computer das dieser ein Bereich im Arbeitsspeicher mit der Größe einer Ganzzahl reservieren soll.
Es gibt unterschiedliche Datentypen die unterscheidlich große Bereiche in unserem Arbeitsspeicher reservieren.

- int: Ganzzahl
- double: Kommazahl
- String: Textzeichenkette
- boolean: Ja / Nein
- char: Textzeichen
- usw

### Variablenzuweisung
Nach der Delkaration einer Variable können wir dieser ein Wert zuweisen

```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Datentyp: int
      //Variablenname: meineVar
      int meineVar;

      //Zuweisung
      meineVar = 5;
  }
}
```
Eine zuweisung erfolgt immer mit dem `=` Zeichen. Dieses Zeichen entspricht NICHT dem Mathematischen 'istgleich'! Es ist ein Befehlt an den Computer den Wert der auf der rechten Seite des '=' steht in die Variable/Speicherbereich die auf der linken Seite des '=' steht zu schreiben.
Einer Variable können wir beliebig oft Daten zuweisen:
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Datentyp: int
      //Variablenname: meineVar
      int meineVar;

      //Zuweisung
      meineVar = 5;
      meineVar = 6;
      meineVar = 566;
      meineVar = 35;
      meineVar = -56777;
  }
}
```
In dem Fall würde am Ende des Programmes die Variable 'meineVar' den Wert -56777 enthalten.
Variablen können nur Daten des in der Deklaration definierten Datentypen enthalten. Daten eines anderen Datentypen führen zum Absturz unseres Programmes oder dazu das es gar nicht ers Kompiliert werden kann.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Datentyp: int
      //Variablenname: meineVar
      int meineVar;

      //Valide
      meineVar = 5;

      //!!NICHT Valide!! - Compilefehler da wir eine Zeichenkette in eine Ganzzahl speichern wollen.
      meineVar = "Hallo";
  }
}
```

## Kommandozeilenausgabe

Java sowie viele andere Programmiersprachen bringen Bibliotheken mit die Grundfunktionalitäten bereitstellen. 
Wie zum Beispiel die Möglichkeit auf der Konsole Werte auszugeben.
Dies geschieht mit der Funktion 'System.out.println("Dieser Text wird auf der Konsole ausgegeben.");' 

```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Datentyp: String
      //Variablenname: begruessung
      String begruessung;
      begruessung = "Hallo, Wie geht es dir?";

      //Ausgabe auf der Konsole des Inhaltes der Variable begruessung
      System.out.println(begruessung);
      
  }
}
```
Wie man oben sieht kann man an die Funktion auch vorher deklarierte und mit Werten belegte Variablen übergeben.
In dem Fall würde folgende Ausgabe auf der Konsole erscheinen:
```
>Hallo, Wie geht es dir?
```

## Arbeiten mit Variablen

Wir können unterschiedliche Mathematische Funktionen auf die Variablen ausführen.

### Addition, Subtraktion, Division, Multiplikation

Nachfolgend sehen wir die Deklaration von drei Variablen, deren Zuweisung und die Addition von den Variablen 'zahl1' mit 'zahl2'.
Das Ergebnis dieser Addition wird dann in die Variable 'ergebnis' geschrieben. Am Ende wird das Ergebnis auf der Konsole ausgegeben.
Die anderen drei Rechenarten können analog durchgeführt werden.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int zahl1;
      int zahl2;
      int ergebnis
      zahl1 = 4;
      zahl2 = 3;
      ergebnis = 0;
      ergebnis = zahl1 + zahl2;
      System.out.println(ergebnis);
  }
}
```
### Inkrement oder Dekrement um 1

Viele unserer Programmieraufgaben erforder den Inkrement oder Dekrement einer Variable um einen festen Wert.
In dem Nachfolgenden Beispiel wird eine Variable 'zahl1' deklariert, mit dem Wert '0' belegt und dann um '1' erhöht.
Das Ergebnis davon wird dann wiederrum in der Variable 'zahl1' abgelegt.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int zahl1;
      zahl1 = 0;
      //Variable zahl1 enthällt den Wert 1
      zahl1 = zahl1 + 1;
      //Variable zahl1 enthällt den Wert 2
      zahl1 = zahl1 + 1;
      //Variable zahl1 enthällt den Wert 3
      zahl1 = zahl1 + 1;
      //Variable zahl1 enthällt den Wert 4
      zahl1 = zahl1 + 1;
      //Variable zahl1 enthällt den Wert 5
      zahl1 = zahl1 + 1;
      System.out.println(zahl1);
  }
}
```
Für diese Aufgabe gibt es eine Kurzform das '++':
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int zahl1;
      zahl1 = 0;
      //Variable zahl1 enthällt den Wert 0
      zahl1 = zahl1++;
      //Variable zahl1 enthällt den Wert 1
      zahl1 = zahl1++;
      //Variable zahl1 enthällt den Wert 2
      zahl1 = zahl1++;
      //Variable zahl1 enthällt den Wert 3
      zahl1 = zahl1++;
      //Variable zahl1 enthällt den Wert 4
      zahl1 = zahl1++;
      //Variable zahl1 enthällt den Wert 5
      System.out.println(zahl1);
  }
}
```
Gleiches gilt für die dekrementierung:
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int zahl1;
      zahl1 = 0;
      //Variable zahl1 enthällt den Wert 0
      zahl1 = zahl1--;
      //Variable zahl1 enthällt den Wert -1
      zahl1 = zahl1--;
      //Variable zahl1 enthällt den Wert -2
      zahl1 = zahl1--;
      //Variable zahl1 enthällt den Wert -3
      zahl1 = zahl1--;
      //Variable zahl1 enthällt den Wert -4
      zahl1 = zahl1--;
      //Variable zahl1 enthällt den Wert -5
      System.out.println(zahl1);
  }
}
