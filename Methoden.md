## Java Methoden

In diesem Kurs lernst du die Verwendung von Methoden in Java.

Lies dich in das Thema ein:
https://www.w3schools.com/java/java_methods.asp

Was sind Methoden? Erklähre in eigenen Worten.
Wie werden Methoden verwendet?
Was sind die Bestandteile einer Methode?

Informiere dich als nächstes darüber wie man Dateien in Java einliest.
https://www.w3schools.com/java/java_files_read.asp

Erstelle eine Datei mit dem Namen "mitarbeiter.csv" und dem Inhalt

```csv
Vorname,Nachname,Geschlecht,Alter,Wohnort
Max,Mustermann,m,30,Berlin
Anna,Musterfrau,w,25,München
Julia,Schmidt,w,35,Hamburg
Michael,Klein,m,28,Köln
Lena,Groß,w,40,Frankfurt
Markus,Meier,m,33,Düsseldorf
Sophie,Wolf,w,27,Stuttgart
Felix,Bauer,m,29,Leipzig
Laura,Becker,w,31,Dresden
Simon,Hoffmann,m,26,Nürnberg
Sarah,Schulz,w,38,Bremen
Andreas,Krüger,m,32,Hannover
Hannah,Lehmann,w,34,Dortmund
David,Wagner,m,36,Essen
Carolin,Fuchs,w,29,Duisburg
Jan,Möller,m,37,Bochum
Maria,Huber,w,24,Wuppertal
Thomas,Schneider,m,39,Bielefeld
Nina,Bergmann,w,28,Bonn
Marcel,Koch,m,26,Mannheim
```

Verwende bei den nachfolgenden Aufgaben Methoden. 

### 1. Datei Einlesen 
Schreibe ein Program das den Benutzer begrüßt und ihn darum bittet ein Dateipfad anzugeben um eine CSV Datei einzulesen.
Gib danach eine Erfolgsmeldung aus.

### 2. Datei Verarbeiten
Erweitere das Program so das es nach dem Einlesen der Datei den Benutzer um die Eingabe von einem der folgenden Befehle bittet.
```
- info                            | gibt die Anzahl der Zeilen und Spalten aus
- getRow n                        | gibt die Zeile n aus
- removeRow n                     | löscht die Zeile n
- save \<Pfad der neuen Datei\>   | speichert die Datei an dem Pfad ab
- find \<string\>                 | sucht nach dem ersten Vorkommen des in <string> enthaltenen wertes und gibt die Zeile aus
- quit                            | beendet das Program
```
Implementiere für jeden der Befehle eine eigene Methode.


