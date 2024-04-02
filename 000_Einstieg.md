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
```

## Arrays
Oft müssen wir mit einer beliebige Anzahl an Variablen des gleichen Types arbeiten. Dies wird oft mit sogenannten 'Arrays' gemacht.

### Deklaration eines Arrays
Arrays werden durch ein '[]' nach dem Datentyp gekennzeichnet
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Deklaration eines Arrays vom Datentyp Ganzzahl
      int[] unserZahllenArray;
  }
}
```

### Initialisierung eines Arrays
Ein Array muss immer mit einer Länge initialisiert werden. Diese Länge zeichnet die Anzahl an werten die in das Array abgelegt werden können.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Deklaration eines Arrays vom Datentyp Ganzzahl
      int[] unserZahllenArray;
      //Initialisierung des Arrays unserZahllenArray mit der Länge 10.
      //Im Speicher sehen wir dann 10 leere Bereich mit der Größe eines INT [ ][ ][ ][ ][ ][ ][ ][ ][ ][ ][ ]
      unserZahllenArray = new int[10];
  }
}
```

### Belegung eines Arrays
Dies reserviert 10 Speicherbereiche für den Datentyp Ganzzahl in dem Arbeitsspeicher. Wir können diese mit einem 'Index' ansprechen.
Dabei beginnt der Index immer bei '0' und geht bis zu der initialisierten Länge - 1! Bei einer Reservierung von 10 Speicherbereichen ist der erste bereich 0 der letzte 9.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Deklaration eines Arrays vom Datentyp Ganzzahl
      int[] unserZahllenArray;

      //Initialisierung des Arrays unserZahllenArray mit der Länge 10.
      //Im Speicher sehen wir dann 10 leere Bereich mit der Größe eines
      //INT-Array:  [ ][ ][ ][ ][ ][ ][ ][ ][ ][ ][ ]
      unserZahllenArray = new int[10];

      // INT-Array:  [1][ ][ ][ ][ ][ ][ ][ ][ ][ ][ ]
      //Das Array an der Position 0 erhällt den Wert 1
      unserZahllenArray[0] = 1;

      // INT-Array:  [1][ ][2][ ][ ][ ][ ][ ][ ][ ][ ]
      //Das Array an der Position 2 erhällt den Wert 4. Wir zählen von 0 somit ist Position 2 das dritte Element
      unserZahllenArray[2] = 4;

      // INT-Array:  [1][ ][2][7][ ][ ][ ][ ][ ][ ][ ]
      //Das Array an der Position 3 erhällt den Wert 7
      unserZahllenArray[3] = 7;

      // INT-Array: [1][ ][2][7][ ][ ][ ][ ][ ][ ][56]
      //Das Array an der Position 9 erhällt den Wert 56
      unserZahllenArray[9] = 56;

      
      //INVALID!! Position 10 gibt es nicht da unser array mit 'unserZahllenArray = new int[10];' initialisiert wurde.
      //Das heißt 0 bis 9 sind 10 Stellen
      unserZahllenArray[10] = 56;
      //INVALID!! Position 100000 gibt es nicht da unser array mit 'unserZahllenArray = new int[10];' initialisiert wurde.
      //Das heißt 0 bis 9 sind 10 Stellen
      unserZahllenArray[100000] = 56;
      //INVALID!! Negative Arraypositionen existieren nicht!
      unserZahllenArray[-1] = 56;

      
  }
}
```

### Zugriff auf Bereiche eines Arrays
Wir können die Daten die wir in ein Array geschrieben haben jederzeit wieder hervorholen in dem wir auf den entsprechenden Index des Arrays zugreifen. 
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Deklaration eines Arrays vom Datentyp Ganzzahl
      int[] unserZahllenArray;
      //Initialisierung des Arrays unserZahllenArray mit der Länge 10.
      unserZahllenArray = new int[10];
      //Das Array an der Position 0 erhällt den Wert 1
      unserZahllenArray[0] = 1;
      //Das Array an der Position 2 erhällt den Wert 4
      unserZahllenArray[2] = 4;
      //Das Array an der Position 3 erhällt den Wert 7
      unserZahllenArray[3] = 7;
      //Das Array an der Position 9 erhällt den Wert 56
      unserZahllenArray[9] = 56;

      //Wir gleifen auf Position 3 also den 4. Element des Arrays zu.
      System.out.println("Array an Position 3 ist gleich: " + unserZahllenArray[3]);
  }
}
```
Ausgabe:
```
>Array an Position 3 ist gleich: 7
```

## Entscheidungen

In unserem Program müssen wir oft Entscheidungen treffen. Dies wird oft mit dem 'if - else' Ausdruck gemacht.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int a = 5;
      if(a > 5) {
        System.out.println("Die Variable a ist größer als der Wert 5");
      } else {
        System.out.println("Die Variable a ist kleiner als der Wert 5");
      }
  }
}
```

Es ist möglich die Ausdrücke beliebig lang zu verketten
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      int a = 5;
      if(a > 5) {
        System.out.println("Die Variable a ist größer als der Wert 5");
      } else if(a == 5) {
        System.out.println("Die Variable a ist gleich dem Wert 5");
      }
      else {
        System.out.println("Die Variable a ist kleiner als der Wert 5");
      }
  }
}
```


## Schleifen
Schleifen benötigen wir um ein Ausdruck mehrfach zu wiederholen.
Der Kopf einer Schleife besteht aus den bereits erlernten Elementen 'for(int i = 0; i < 10; i++)'.
Wir schlüsseln diese auf in.
- for: der Schleifen Typ
- int i = 0; Deklaration der Variable i und Zuweisung des Wertes 0 zu der Variable
- i < 10; Abfrage der Variable i. Ist diese Variable kleiner 10?
- i++; Increment der Variable um 1.
Das heißt es wird zuerst eine Variable mit dem Wert 0 initialisiert und danach bei jedem Durchlauf der Schleife mit dem Wert 10 verglichen.
Wenn i kleiner als 10 ist, dann wird die Schleife ausgeführt und die Variable i wird für den nächsten Durchlauf der Schleife um 1 erhöht.

Dadurch können wir auf einfach Weiße ein Array der Länge 10 mit 10 Werten initialisieren.
```java
//Main- Klasse
public class Main {
  //Main Methode
  public static void main(String[] args) {
      //Programmeinstieg hier
      //Deklaration eines Arrays vom Datentyp Ganzzahl
      int[] unserZahllenArray;
      //Initialisierung des Arrays unserZahllenArray mit der Länge 10.
      unserZahllenArray = new int[10];

      for(int i = 0; i < 10; i++) {
        System.out.println("Schreibe den Wert: " + i + " an die Position " + unserZahllenArray[i] + "des Arrays.");
        unserZahllenArray[i] = i;
      }
      
      for(int i = 0; i < 10; i++) {
        System.out.println("Die Position des Arrays: " + i + " enthällt den Wert: " + unserZahllenArray[i]);
        unserZahllenArray[i] = i;
      }
      
  }
}
```
