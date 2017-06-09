<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [1. Einleitung](#1-einleitung)
  - [1.2 Download und Installation](#12-download-und-installation)
    - [1.2.1 Anforderungen](#121-anforderungen)
    - [1.2.3 Installation](#123-installation)
  - [1.3 Starten und der Startbildschirm](#13-starten-und-der-startbildschirm)
- [2. Erste Schritte in Eclipse](#2-erste-schritte-in-eclipse)
  - [2.1 Beschreibung der Benutzeroberfläche](#21-beschreibung-der-benutzeroberfl%C3%A4che)
    - [2.1.1 Erstanwendung](#211-erstanwendung)
    - [2.1.2 Workspace](#212-workspace)
    - [2.1.2 Package-Explorer](#212-package-explorer)
  - [2.2 Anlegen eines Projektes](#22-anlegen-eines-projektes)
  - [2.3 Strukturierung von Eclipse Projekten](#23-strukturierung-von-eclipse-projekten)
  - [2.4 Anlegen von Java Dateien](#24-anlegen-von-java-dateien)
    - [2.4.1 Zeilenweise navigieren](#241-zeilenweise-navigieren)
    - [2.4.2 Codevervollständigung](#242-codevervollst%C3%A4ndigung)
    - [2.4.3 Fehlerprüfung](#243-fehlerpr%C3%BCfung)
    - [2.4.4 Programmausführung](#244-programmausf%C3%BChrung)
    - [2.4.2 Ansicht wechseln](#242-ansicht-wechseln)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



#Hello World Tutorial für blinde Programmierer mittels Java, Eclipse und Voice Over unter Mac Os X

## 1. Einleitung
Dieses Tutorial soll blinden Programmierern zeigen, wie man ein simples Java *Hello World*-Programm, als Eclipse Projekte, erstellen und ausführen kann. 

Das hier verwendete Betriebssystem ist Mac OS X.

Die Tastenkombinationen gleichen Windows, allerdings wird statt der `CMD`-Taste die `CTRL`-Taste verwendet.

Statt `TAB` oder `CMD`+`↓`/`↑`, kommt Windows lediglich mit den jeweiligen Pfeiltastenaus.

### 1.2 Download und Installation

#### 1.2.1 Anforderungen 
Vor der Installation der Eclipse IDE muss entweder das JDK (Java Development Kit) oderdie JRE (Java Runtime Environment) auf Ihrem Computer installiert sein. Diese können Sie ggf.unter <http://java.sun.com/javase/downloads/index.jsp> downloaden. Die Installation des JDK istindes zu empfehlen, da dieses den Zugriff auf die Dokumentation und den Quellcode der StandardJava-Klassen ermöglicht.

####1.2.2 Download
Laden Sie sich die Eclipse IDE for Java Developers für Mac Os unter <https://www.eclipse.org/downloads/packages> herunter.

Zur Auswahl der jeweiligen Eclipse Version gelangen Sie im Hauptbereich der Seite. Das Element der Klasse *package-teaser-title* beschreibt, um welche Variante der Eclipse IDE es sich genau handelt. Lässt Ihr Screenreader den gesuchten Titel, in unserem Fall **Eclipse IDE für Java Developers**, verlauten, stehen Ihnen 5 weitere Bereiche zur Verfügung, bevor Sie beim nächsten *package-teaser-title*  angekommen sind. 
Leider werden Ihnen hier, im Bereich mit dem Klassentitel *package-teaser-download-link*  nur die Bit-Angaben der Betriebssystemversion vorgelesen, also jeweils 32-bit oder 64-bit. Die Ansicht im Hauptfenster, im Element *package-teaser-title* , gliedert sich wie folgt:

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

#### 1.2.3 Installation
Eclipse muss nicht installiert, nur entpackt werden.
Entpacken Sie das Archiv in einem beliebigen Ordner.

### 1.3 Starten und der Startbildschirm

Eclipse bittet Sie nach dem Starten einen Workspace anzulegen. Dies ist ein Ordner, ein Arbeitsbereich, in welchem Eclipse Ihre Projekte speichert. Der Default-Workspace ist für dieses Tutorial bestens geeignet. Bestätigen Sie die Eingabe.

## 2. Erste Schritte in Eclipse
### 2.1 Beschreibung der Benutzeroberfläche
#### 2.1.1 Erstanwendung
Bei erstmaligem Starten erscheint der *Welcome-Bildschirm*. Dieser stellt eine gewisse Barriere dar. In dem Fenster befindet sich (ab Eclipse Neon) ein Markierungsfeld mit der Beschriftung *Always show Welcome at start up*. Per default ist dieses aktiviert. Bitte deaktivieren Sie es jetzt. Der *Welcome Bildschrim* stellt somit beim nächsten Start keine Hürde mehr dar.
#### 2.1.2 Workspace
Tabben Sie zu *Workspace* und bestätigen Sie. Nun befinden Sie sich in Ihrem Arbeitsbereich. Die für dieses Tutorial wichtigsten Ansichten sind der *Package Explorer*, der *Editor* und die *Console*.
#### 2.1.2 Package-Explorer
Der Fokus liegt nun auf dem *Package Explorer*. 

In jedem Formular, welches Sie in Eclipse ausfüllen, befindet sich ein Zurück-Button.
Falls Sie also versehentlich die falsche Art von Java-Datei, z.B. *Class* statt *Interface*, gewählt haben, können Sie über diesen Button im Formular zurück navigieren und Ihre Eingabe korrigieren.

### 2.2 Anlegen eines Projektes
Drücken Sie nun die Tastenkombination *Neue Ressource anlegen*, nämlich `alt` + `cmd` + `N`. Es öffnet sich eine Liste, in welche Sie mit `cmd` + `↑` springen können. Mit `cmd` + `↓` wählen Sie *Java Project* aus. NTM: Alle anderen Optionen habe ich bis jetzt nicht geschafft, aus dieser Liste auszuwählen.

### 2.3 Strukturierung von Eclipse Projekten
Es öffnet sich ein Formular, geben Sie den Projektnamen ein und bestätigen Sie. Die Struktur bleibt Ihnen überlassen. NTM: Namenskonvention für Java Projekte? Vorlesungsfolien FPA? SUN?

### 2.4 Anlegen von Java Dateien
Drücken Sie nun die Tastenkombination *Neue Ressource über das Wizard anlegen*, also `cmd` + `N`. Sie befinden sich in einem Java Projekt und somit  nach Drücken des Shortcuts bereits in den Optionen zum Anlegen aller möglichen Java Ressourcen. Wählen Sie *Class* aus.

Geben Sie Ihrer Klasse einen Namen. Klassennamen beginnen laut der Java Namenskonvention immer mit einem Großbuchstaben. Aktivieren Sie zusätzlich das Markierungsfeld *public static void main (String[] args)*. Damit wird Ihnen direkt von Eclipse eine sogenannte Main-Methode, der Startpunkt eines jeden Java-Programms, generiert.

Falls Sie versehentlich statt *Class* eine andere Option gewählt haben, steht Ihnen im Formular die Zurück-Funktion zur Verfügung, welche wenn sie fokussiert ist, mit `ctrl`+`alt`+`Leertaste` zu bestätigen ist.

Der Fokus liegt nun im Editor, auf Ihrer neu erstellten Klasse in Zeile 1.
#### 2.4.1 Zeilenweise navigieren
Navigieren Sie nun mittels `alt`+`↓` oder mit dem Shortcut *go to line*, `cmd`+`L`, zu Zeile 6. Hier befindet sich der von Eclipse automatisch generierte Kommentar

	//TODO Auto-generated method stub

#### 2.4.2 Codevervollständigung
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

#### 2.4.3 Fehlerprüfung
Der Shortcut *zur nächsten Warnung oder zum nächsten Fehler springen* ,`cmd`+`.` hilft Ihnen, Ihr Projekt auf Fehler oder Warnungen zu überprüfen. Der Screenreader springt damit zum nächsten Fehler oder zur nächsten Warnung. Schweigt der Screenreader, ist kein Fehler vorhanden.

#### 2.4.4 Programmausführung
Nun können Sie Ihr Programm ausführen. Nutzen Sie hierfür den Shortcut für *Run*, 
`⇧`+`cmd`+`F11`. Ihr Programm wird beim Ausführen dieses Befehls, genau wie beim Shortcut zum *Speichern*, `cmd`+`S`, als Java-Datei in Ihrem Workspace gespeichert. Darauf weist Sie der zu  bestätigende Systemdialog *Save and Lauch* hin.

#### 2.4.2 Ansicht wechseln 
Drücken Sie nun *zwischen den Ansichten wechseln*, also `cmd`+`F7`, um zur Ausgabe Ihres Programms in der *Console* zu gelangen. Halten Sie `cmd` gedrückt. Es ist eine Liste aller *Views* geöffnet, durch welche Sie mit `↓`/`↑` navigieren können. Wählen Sie *Console* aus. 

Ihr Screenreader sollte nun verlauten lassen: Hello World!


Herzlichen Glückwunsch zu Ihrer ersten Hello-World-Applikation, erstellt in der Eclipse IDE.



