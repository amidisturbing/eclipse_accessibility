---
ID: 124
post_title: Eclipse OsX Hello World Beispiel
author: amidisturbing
post_date: 2017-06-22 19:37:36
post_excerpt: ""
layout: page
permalink: >
  http://www.amidisturbing.com/barrierefreies/eclipse-osx-hello-world/
published: true
---
## Einleitung
Dieses Tutorial soll blinden Programmierern zeigen, wie man ein simples Java *Hello World*-Programm, als Eclipse Projekte, erstellen und ausführen kann.

Das hier verwendete Betriebssystem ist Mac OS X.

Die Tastenkombinationen gleichen Windows, allerdings wird statt der `CMD`-Taste die `CTRL`-
Taste verwendet.

Statt `TAB` oder `CMD`+`↓`/`↑`, kommt Windows lediglich mit den jeweiligen Pfeiltasten
aus.

### Download und Installation

#### Anforderungen
Vor der Installation der Eclipse IDE muss entweder das JDK (Java Development Kit) oder
die JRE (Java Runtime Environment) auf Ihrem Computer installiert sein. Diese können Sie ggf.
unter &lt;http://java.sun.com/javase/downloads/index.jsp&gt; downloaden. Die Installation des JDK ist
indes zu empfehlen, da dieses den Zugriff auf die Dokumentation und den Quellcode der Standard
Java-Klassen ermöglicht.

#### Download
Laden Sie sich die Eclipse IDE for Java Developers für Mac Os unter &lt;https://www.eclipse.org/downloads/packages&gt; herunter.

Zur Auswahl der jeweiligen Eclipse Version gelangen Sie im Hauptbereich der Seite. Das Element der Klasse *package-teaser-title* beschreibt, um welche Variante der Eclipse IDE es sich genau handelt. Lässt Ihr Screenreader den gesuchten Titel, in unserem Fall **Eclipse IDE für Java Developers**, verlauten, stehen Ihnen 5 weitere Bereiche zur Verfügung, bevor Sie beim nächsten *package-teaser-title* angekommen sind.
Leider werden Ihnen hier, im Bereich mit dem Klassentitel *package-teaser-download-link* nur die Bit-Angaben der Betriebssystemversion vorgelesen, also jeweils 32-bit oder 64-bit. Die Ansicht im Hauptfenster, im Element *package-teaser-title* , gliedert sich wie folgt:

Die Versionen für Windows 32-bit und 64-bit
Die Version für Mac 64-bit
Die Versionen für Linux 32-bit und 64-bit

Ihnen stehen also insgesamt, pro Eclipse Variante 5 Download-Links zur Verfügung. Hier nochmal eine Auflistung, der Reihe nach:

1. Version für Windows 32-bit
2. Version für Windows 64-bit
3. Version für Mac 64-bit
4. Version für Linux 32-bit
5. Version für Linux 64-bit

Nutzen Sie für dieses Tutorial die 3. Option zum Download.

#### Installation
Eclipse muss nicht installiert, nur entpackt werden.
Entpacken Sie das Archiv in einem beliebigen Ordner.

### Starten und der Startbildschirm

Eclipse bittet Sie nach dem Starten einen Workspace anzulegen. Dies ist ein Ordner, ein Arbeitsbereich, in welchem Eclipse Ihre Projekte speichert. Der Default-Workspace ist für dieses Tutorial bestens geeignet. Bestätigen Sie die Eingabe.

## Erste Schritte in Eclipse
### Beschreibung der Benutzeroberfläche
#### Erstanwendung
Bei erstmaligem Starten erscheint der *Welcome-Bildschirm*. Dieser stellt eine gewisse Barriere dar. In dem Fenster befindet sich (ab Eclipse Neon) ein Markierungsfeld mit der Beschriftung *Always show Welcome at start up*. Per default ist dieses aktiviert. Bitte deaktivieren Sie es jetzt. Der *Welcome Bildschrim* stellt somit beim nächsten Start keine Hürde mehr dar.
#### Workspace
Tabben Sie zu *Workspace* und bestätigen Sie. Nun befinden Sie sich in Ihrem Arbeitsbereich. Die für dieses Tutorial wichtigsten Ansichten sind der *Package Explorer*, der *Editor* und die *Console*.
#### Package-Explorer
Der Fokus liegt nun auf dem *Package Explorer*.

In jedem Formular, welches Sie in Eclipse ausfüllen, befindet sich ein Zurück-Button.
Falls Sie also versehentlich die falsche Art von Java-Datei, z.B. *Class* statt *Interface*, gewählt haben, können Sie über diesen Button im Formular zurück navigieren und Ihre Eingabe korrigieren.

### Anlegen eines Projektes
Drücken Sie nun die Tastenkombination *Neue Ressource anlegen*, nämlich `alt` + `cmd` + `N`. Es öffnet sich eine Liste, in welche Sie mit `cmd` + `↑` springen können. Mit `cmd` + `↓` wählen Sie *Java Project* aus. NTM: Alle anderen Optionen habe ich bis jetzt nicht geschafft, aus dieser Liste auszuwählen.

### Strukturierung von Eclipse Projekten
Es öffnet sich ein Formular, geben Sie den Projektnamen ein und bestätigen Sie. Die Struktur bleibt Ihnen überlassen. NTM: Namenskonvention für Java Projekte? Vorlesungsfolien FPA? SUN?

### Anlegen von Java Dateien
Drücken Sie nun die Tastenkombination *Neue Ressource über das Wizard anlegen*, also `cmd` + `N`. Sie befinden sich in einem Java Projekt und somit nach Drücken des Shortcuts bereits in den Optionen zum Anlegen aller möglichen Java Ressourcen. Wählen Sie *Class* aus.

Geben Sie Ihrer Klasse einen Namen. Klassennamen beginnen laut der Java Namenskonvention immer mit einem Großbuchstaben. Aktivieren Sie zusätzlich das Markierungsfeld *public static void main (String[] args)*. Damit wird Ihnen direkt von Eclipse eine sogenannte Main-Methode, der Startpunkt eines jeden Java-Programms, generiert.

Falls Sie versehentlich statt *Class* eine andere Option gewählt haben, steht Ihnen im Formular die Zurück-Funktion zur Verfügung, welche wenn sie fokussiert ist, mit `ctrl`+`alt`+`Leertaste` zu bestätigen ist.

Der Fokus liegt nun im Editor, auf Ihrer neu erstellten Klasse in Zeile 1.
#### Zeilenweise navigieren
Navigieren Sie nun mittels `alt`+`↓` oder mit dem Shortcut *go to line*, `cmd`+`L`, zu Zeile 6. Hier befindet sich der von Eclipse automatisch generierte Kommentar

//TODO Auto-generated method stub

#### Codevervollständigung
Ersetzen Sie den Kommentar durch einen print-Befehl. Markieren Sie dafür mit `shift`+`alt`+`→` den Kommentar und tippen Sie
syso, dann den Shortcut zur *Codevervollständigung* `ctrl`+`Leertaste`. Wenn Sie diese Kombination zum ersten mal ausführen, steht Ihnen bis zur Version Luna von Eclipse die Auswahl *Enable Smart Code Complition* zur Verfügung. Wählen Sie diese aus, wird Ihnen zukünftig die Eingabe des Strings

syso

gefolgt von dem Shortcut `ctrl`+`Leertaste`,

sofort zu

System.out.println();

komplettiert.

Sollten Sie Eclipse Neon nutzen, steht Ihnen diese Option in der Liste nicht zur Verfügung.

Der Fokus liegt nun in den Klammern, also bei den Parametern des Aufrufes der print-Funktion.

Ergänzen Sie den Methodenaufruf mit dem String

"Hello World!"

Ihr Programm ist jetzt fertig.

#### Fehlerprüfung
Der Shortcut *zur nächsten Warnung oder zum nächsten Fehler springen* ,`cmd`+`.` hilft Ihnen, Ihr Projekt auf Fehler oder Warnungen zu überprüfen. Der Screenreader springt damit zum nächsten Fehler oder zur nächsten Warnung. Schweigt der Screenreader, ist kein Fehler vorhanden.

#### Programmausführung
Nun können Sie Ihr Programm ausführen. Nutzen Sie hierfür den Shortcut für *Run*,
`⇧`+`cmd`+`F11`. Ihr Programm wird beim Ausführen dieses Befehls, genau wie beim Shortcut zum *Speichern*, `cmd`+`S`, als Java-Datei in Ihrem Workspace gespeichert. Darauf weist Sie der zu bestätigende Systemdialog *Save and Lauch* hin.

#### Ansicht wechseln
Drücken Sie nun *zwischen den Ansichten wechseln*, also `cmd`+`F7`, um zur Ausgabe Ihres Programms in der *Console* zu gelangen. Halten Sie `cmd` gedrückt. Es ist eine Liste aller *Views* geöffnet, durch welche Sie mit `↓`/`↑` navigieren können. Wählen Sie *Console* aus.

Ihr Screenreader sollte nun verlauten lassen: Hello World!

Herzlichen Glückwunsch zu Ihrer ersten Hello-World-Applikation, erstellt in der Eclipse IDE.