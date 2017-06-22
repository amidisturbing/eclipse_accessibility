---
ID: 28
post_title: Eclipse Tutorial
author: amidisturbing
post_date: 2017-03-24 16:05:54
post_excerpt: ""
layout: page
permalink: >
  http://www.amidisturbing.com/tutorial/eclipse-tutorial/
published: true
---

##Einleitung
Dieses Tutorial richtet sich an blinde Softwareentwickler/innen, die in der Hochsprache Java innerhalb der Eclipse IDE Programme schreiben möchten und bis jetzt kein geeignetes Tutorial für sehbehinderte Menschen finden konnten. Das gewählte Betriebssystem ist Windows. Als unterstützende Technologie wird der Screenreader JAWS genutzt. Sollten Sie mit NVDA oder einem anderen Screenreader vertraut sein, spricht nichts dagegen, dieses Tutorial mit dem Screenreader Ihrer Wahl zu bearbeiten.

Die Grundlage für dieses Tutorial bietet ein [Eclipse Tutorial](https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml) der *University of Washington*, welches unter der URL <https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml> abrufbar ist.

## Was ist die Eclipse IDE?
Die Eclipse IDE (Integrated Development Environment) ist eine generische, quelloffene Software-Entwicklungsumgebung. Diese basiert auf einem *Plugin*-Modell, das es ermöglicht die IDE betriebssystemübergreifend für verschiedenste Entwicklungen zu nutzen, sofern Java auf dem System installiert ist.

## Installation

### Anforderungen 
Vor der Installation der Eclipse IDE muss entweder das JDK (Java Development Kit) oder die JRE (Java Runtime Environment) auf ihrem Computer installiert sein. Sie können diese unter <http://java.sun.com/javase/downloads/index.jsp> downloaden.
Die Installation des JDK wird angeraten, da dieses Ihnen den Zugriff auf die Dokumentation und den Quellcode der Standard-Java-Klassen ermöglicht.

### Download
Die offizielle Seite für den Download der Eclipse IDE ist <https://www.eclipse.org/downloads>. Um die Navigation so einfach wie möglich zu halten, startet dieses Tutorial eine Ebene tiefer auf der Eclipse-Website, als es der offizielle Download-Link tut.

1. Rufen Sie die Seite <https://www.eclipse.org/downloads/packages> in Ihrem Browser auf.
2. Laden Sie die **Eclipse IDE für Java Developers** herunter. 

*Anmerkung: Sie haben hier die Wahl zwischen **Eclipse IDE für Java Developers**, **Eclipse IDE für Java EE Developers** und weiteren Versionen für Java-Entwickler. Alle sind für dieses Tutorial geeignet.*

Zur Auswahl der jeweiligen Eclipse-Version gelangen Sie im Hauptbereich der Seite. Nutzen Sie hierfür den Link *Skip to main content* am Anfang der Seite. In diesem stehen pro Eclipse-Variante fünf Download-Links zur Verfügung. Die Links im Hauptbereich der Seite teilen sich der Reihe nach wie folgt auf:

1. Link zur Übersichtsseite des Pakets
2. Link zur Downloadseite der Version für Windows 64-bit
3. Link zur Downloadseite der Version für Mac 64-bit
4. Link zur Downloadseite der Version für Linux 32-bit
5. Link zur Downloadseite der Version für Linux 64-bit

Falls Sie also Linux oder Mac nutzen, finden Sie auch hierfür die entsprechenden Downloadlinks im Hauptfenster der Downloadseite.

## Eclipse auf dem PC installieren 

1. Verschieben oder kopieren Sie das heruntergeladene .zip- oder .tar.gz-Archiv in Ihr Root-Verzeichnis (unter Windows **C:\\**).
2. Entpacken Sie das Archiv. Daraufhin wird Ihnen ein Ordner namens **eclipse** im aktuellen Verzeichnis erstellt.

## Grundlagen

Sowohl Eclipse als auch Screenreader wie JAWS haben viele Shortcuts, die die Arbeit mit diesen Programmen enorm beschleunigen bzw. vereinfachen. So kann es vorkommen, dass zwei Tastenkombinationen sowohl von JAWS (oder einem anderen Screenreader) als auch von Eclipse für eine bestimmte Funktionalität reserviert sind. Da der Screenreader in der Regel zunächst alle Tastenkombinationen abfängt, besitzt bei einer Shortcutüberlappung der Screenreader Vorrang. Um die gewünschte Tastenkombination an die Anwendung durchreichen zu können, müssen Sie bei JAWS `JAWSTASTE`+`F3` drücken und dann die Tastenkombination ausführen. Wenn also in diesem Tutorial manche Shortcuts aufgeführt werden, die nicht auf Anhieb bei Ihnen funktionieren, könnte es sein, dass der Screenreader diese Tastenkombination belegt.

### Starten und der Startbildschirm

1. Führen Sie die Datei **eclipse.exe** aus.

2. Legen Sie Ihren Arbeitsbereich, den sogenannten *Workspace*, fest. Für dieses Tutorial ist der vorausgewählte *Workspace* im Ordner **C:\eclipse** am besten geeignet.  

*Anmerkung: Der Workspace kann für jede Sitzung neu definiert werden. Falls Sie nur einen Workspace für all Ihre Projekte benötigen, aktivieren Sie die Checkbox "Use this as default and do not ask again". Unter Windows: Halten Sie die `ALT`-Taste gedrückt und drücken Sie zusätzlich`U`.*

3. Starten Sie die Eclipse IDE.
 
4. Bei erstmaligem Starten sehen Sie den *Welcome*-Bildschirm. Dieser stellt eine gewisse Barriere dar. In dem Fenster befindet sich (ab Eclipse Neon) ein Markierungsfeld mit der Beschriftung "Always show Welcome at start up". Dieses ist per default aktiviert. Deaktivieren Sie es. Der *Welcome*-Bildschirm stellt so beim nächsten Start keine Hürde mehr dar.

5. Tabben Sie zu *Workspace* und bestätigen Sie. Nun befinden Sie sich in Ihrem Arbeitsbereich. Die für dieses Tutorial wichtigsten Ansichten sind der *Package Explorer*, der *Editor* und die *Console*.

#### Aufbau der Standardansicht

Nachdem der *Welcome-Bildschirm* geschlossen wurde, befinden Sie sich in der Standard-Entwickleransicht der Eclipse IDE, in welcher Ihnen die wichtigsten Ansichten sofort zur Verfügung stehen. Der *Package Explorer* beinhaltet alle geöffneten Projekte, welche sich in Ihrem *Workspace* befinden. Einzelne Dateien können Sie im *Editor* öffnen, bearbeiten und speichern. Dieser steht Ihnen ebenfalls in der Standardansicht zur Verfügung, ebenso wie das *Console*-Fenster, welches die Ausgaben Ihres Programmes darstellt.

Der Fokus liegt beim erstmaligen Starten auf dem *Package Explorer*. Wenn Sie allerdings bereits ein Projekt mit einer Klasse erstellt haben und diese im *Editor* beim letzten Beenden des Programms geöffnet ließen, liegt der Fokus im *Editor*, an der Stelle, an der er auch beim Beenden des Programmes lag.

### Wie Dateien organisiert werden

#### Workspaces und Projekte

Eclipse nutzt zwei grundlegende Abstraktionen zum Strukturieren von Quellcode.

##### Workspace

Der *Workspace* ist das Arbeitsverzeichnis für all Ihre Projekte. Sie können mit Eclipse auch mehrere *Workspaces* verwalten, falls Sie dies wünschen.

##### Project

Ein *Project* ist eine Sammlung zusammengehörigen Quellcodes, welcher meist ein unabhängiges Programm formt.
Kurz gesagt ist Ihr *Workspace* der Ordner, der all Ihre Projekte beinhaltet.
Einem *Project* ist auch ein *Classpath* zugeordnet. Der *Classpath*  ist der Ort, an welchem Bibliotheken und andere Projekte eingebunden werden. Das Tutorial widmet sich dem  *Classpath* später in einem eigenen Abschnitt.

##### Strukturierung des Workspace und der Projekte

Immer, wenn Sie in Eclipse ein Projekt anlegen, wird von Eclipse automatisch ein neuer, gleichnamiger Ordner im aktuellen *Workspace* angelegt. In diesem Ordner werden zwei weitere Ordner, nämlich *bin* und *src* (source) angelegt. Sie können den Ordner *bin* ignorieren. In diesem werden automatisch alle Kompilate, also die *.class*-Dateien, gespeichert. 

All Ihre *.java*-Dateien befinden sich im *src*-Ordner.

Zusammengefasst ist also ihr *Workspace* der Ordner, welcher alle Projekte beinhaltet, welche wiederum Ordner, benannt nach den zugehörigen Projekten, sind.

### Einen Workspace anlegen
Sie können sich Ihren *Workspace* auch wie den Root-Folder, von welchem Eclipse ausgeht, vorstellen. Sie können zwar mehrere *Workspaces* mit Eclipse verwalten, allerdings können Sie nur einen *Workspace* gleichzeitig in Eclipse öffnen. Der *Welcome*-Bildschirm und wie Sie diese Hürde meistern wurde bereits im Kapitel Grundlagen unter 3.1 Starten und der Startbildschirm erklärt. Tabben Sie also zu *Workspace* und bestätigen Sie. Sollten Sie während des Arbeitens mit Eclipse einen neuen *Workspace* anlegen oder einen bereits bestehenden *Workspace* auswählen wollen, gehen Sie über die Menüleiste zu *File* und dort zu *Switch Workspace*. Es öffnet sich ein weiteres Untermenü, in welchem Sie einen Eclipse bereits bekannten *Workspace* auswählen können. Sie können stattdessen auch die Option *Other* in diesem Untermenü nutzen, um das Fenster *Workspace Launcher* zu öffnen. Im *Workspace Launcher* liegt der Fokus zuerst auf einem Auswahlmenü, in welchem Sie wiederum die bekannten *Workspaces* auswählen können. Alternativ steht Ihnen die Möglichkeit zur Verfügung, zu einem *Workspace* im Dateisystem zu navigieren und einen bestehenden oder neuen Ordner als *Workspace* auszuwählen. Von der Verwendung eines Ordners, der bereits Dateien enthält, die keine Eclipse-Projekte sind, wird abgeraten. Bei der Erstauswahl eines Ordners als *Workspace* wird in diesem ein versteckter Ordner namens *.metadata* erstellt.

### Ein Projekt anlegen
Nachdem Sie einen *Workspace* angelegt oder ausgewählt haben, können Sie auch Projekte anlegen. Projekte sind die nächstkleinere Organisationseinheit nach dem *Workspace*. Ein *Workspace* beinhaltet in der Regel mehrere Projekte. Um ein neues Projekt anzulegen, nutzen Sie die Tastenkombination `ALT` + `SHIFT` + `N` . Anhand dieses Shortcuts öffnet sich eine Liste, welche Sie durch das Drücken der `Pfeiltaste nach oben`- bzw. `Pfeiltaste nach unten` durchlaufen können. Wählen Sie mit Pfeiltaste nach unten *Java Project* aus. Benennen Sie Ihr Projekt und bestätigen Sie das Formular. Das Projekt ist nun durch Eclipse angelegt worden und im *Package Explorer* verfügbar, zu welchem Sie mit `ALT` + `SHIFT` + `Q` , `P` navigieren können. Der aktuelle Fokus des Programm-Cursors ändert sich beim Anlegen eines Projekts nur, sollte dieser im *Package Explorer* gelegen haben. In diesem Fall ändert er sich vom vorher ausgewählten Projekt zum neu erstellten. Anderenfalls bleibt der Fokus an der Stelle, an welcher er sich befand, bevor Sie ein neues Projekt angelegt haben.

### 3.5 Ein Paket erstellen	
Ein Paket (englisch *package*) dient dazu bestimmte Programmbereiche zu gliedern. Hierzu wird in vielen Programmiersprachen mit dem Konzept der Namensräume (englisch *namespaces*) gearbeitet. Anhand von Namensräume wird die Verwendung von gleichen Bezeichnungen ermöglicht, ähnlich wie eine Verzeichnisstruktur es ermöglicht den selben Dateinamen in verschiedenen Verzeichnissen zu nutzen. Sie können zum Beispiel im selben Projekt zwei Mal die Klasse random.java anlegen. Sofern diese in zwei verschiedenen *Packages* liegen, können diese anhand ihres Pakets unterschieden werden.

Es wird empfohlen Dateien innerhalb Ihres Projekts mittels Paketen zu strukturieren. Wenn Sie kein *Package* anlegen, werden Ihre Dateien im *Default Package* angelegt. Um nun ein weiteres Paket anzulegen, führen Sie den Shortcut zum Anlegen einer neuen Ressource aus (`ALT` + `SHIFT` + `N`) und navigieren Sie mit der `Pfeiltaste nach unten` solange bis der Fokus auf *Package* liegt. Wenn Sie diese Auswahl bestätigen öffnet sich ein *Wizard*, der Sie nach dem gewünschten Namen des *Packages* fragt. Geben Sie den Namen ein und bestätigen Sie mit `ENTER`.

Im Paketmanager erscheint jetzt ein neuer Eintrag mit dem vergebenen Namen. Auf der Festplatte werden *Packages* als Verzeichnisse realisiert.

### Eine Klasse erstellen
Nun haben Sie schon Ihr erstes Projekt angelegt und möchten sicherlich auch eine eigene Klasse erstellen.

Durch das Kommando *Neue Ressource anlegen*, also `ALT`+`SHIFT`+`N`, öffnet sich edie Ihnen bereits bekannte Liste, welche Sie mit den Pfeiltasten fokussieren können. Wählen Sie mit `Pfeiltaste nach unten` *Class* aus.

Es öffnet sich der *Wizard* der Sie durch die Erstellung einer Klasse führt. Pflicht ist die Vergabe eines Namens. Mittels der `TAB`-Taste können Sie durch die einzelnen Funktionen navigieren.

Die Klasse wird in dem *Project* und dem *Package* angelegt, das gerade selektiert ist. Im Formular haben Sie die Möglichkeit beides zu ändern. Sie können auch direkt beim Anlegen der Klasse das *Package* angeben, sollte dieses nicht mit dem aktuellen übereinstimmen. Geben Sie Ihrer Ressource einen Namen.

Wenn Sie eine Klasse anlegen möchten, die den Startpunkt für Ihre Anwendung darstellt, steht Ihnen im nächsten Schritt ein Kontrollkästchen zur Verfügung, welches, wenn es aktiviert ist, für die Generierung der sogenannten main-Methode sorgt. Aktivieren Sie hierfür das Kontrollfeld *public static void main (String[] args)*  mit der Tastenkombination für *Bestätigen* `ALT`+`V`. Bestätigen Sie das ausgefüllte Formular.

Sie können Ihre Klasse direkt beim Erstellen mit den dazugehörigen *Modifiers* ausstatten, indem Sie deren Kontrollfelder  unter der Option *Modifiers* aktivieren.

Wenn Sie eine andere Klasse erweitern wollen, können Sie die Superklasse über den Namen spezifizieren. Tun Sie dies, indem Sie Paket und Namen über die Punktnotation angeben. Ist die Superklasse beispielsweise die Klasse *Object*, so lautet der Name *java.lang.Object*, da es sich um die Klasse *Object* im Paket *java.lang.* handelt.

Sie können die Superklasse, das Interface und die vorzugenerierenden Methoden auch in diesem Formular über die *Browse*-Funktion auswählen.

Der Fokus liegt nach dem Anlegen im *Editor* auf Ihrer neu erstellten Klasse in Zeile 1.

Alternativ zu dem Shortcut `ALT`+`SHIFT`+`N` gelangen Sie auch mit der Tastenkombination `CTRL`+`N` in den *Wizard* zum Anlegen neuer Ressourcen. Wenn Sie sich bereits in einem Java-Projekt befinden, stehen Ihnen direkt nach dem Drücken des Shortcuts die Optionen zum Anlegen aller möglichen Java-Ressourcen zur Verfügung.

Diese Tastenkombination hat bei manchen Screenreadern den Vorteil, dass sie nicht von selbigem belegt wird. 

### Der Classpath
Wird eine Java-Klasse instanziiert, muss die Java Virtual Machine (JVM) wissen, wo die kompilierte Klasse, also die zugehörige *.class*-Datei, liegt. Im *Classpath* stehen die Pfade zu den obersten *Packages* eines Java-Programms und zu eingebundenen *.jar*-Dateien. Die kompilierten *.class*-Dateien eines Java-Projekts sind in einer Ordnerstruktur abgelegt, die der Paketstruktur des Projekts gleicht. In *.jar*-Dateien sind die *.class*-Dateien ebenfalls in dieser Ordnerstruktur abgelegt. Dadurch weiß die JVM jederzeit, wo der kompilierte Code zu einer bestimmten Klasse liegt und kann diesen nutzen.

### Kompilieren und Fehlerbehebung
Dieser Abschnitt beschäftigt sich nicht mit *Debugging*. Stattdessen soll hier auf das Beheben von kleineren Kompilierfehlern eingegangen werden.

Markierungen in Form von roten Unterringelungen für *Errors* (Fehler) und gelben Unterringelungen für *Warnings*  (Warnungen) weisen sehende Menschen frühzeitig auf Kompilierfehler hin. Dies ist nur möglich, da Ihr Code fortlaufend durch Eclipse in Zwischencode für die JVM (Jave Virtual Machine) übersetzt wird.

Da diese Markierungen in erster Linie visuell sind, wird blinden oder sehbehinderten Programmierern empfohlen, regelmäßig, vorallem am Ende einer Programmierperiode, von dem Shortcut `CTRL`+`.` gebrauch zu machen, um zur nächsten Warnung oder zum nächsten Fehler zu springen. Der Fokus Ihres Screenreaders springt damit sofort zum nächsten Fehler oder zur nächsten Warnung in der aktuellen Java-Datei und liest Ihnen die unterringelte Stelle vor. Wenn JAWS die Fehlerzeile nicht sofort vorließt, so drücken Sie einmal `Pfeiltaste nach oben` und dann wieder `Pfeiltaste nach unten`. Allerdings ist es zu Empfehlen direkt nach dem Drücken von `CTRL` + `.` für JAWS-Nutzer `INSERT` + `PageDown` zu drücken, um die Fehlerhinweise auslesen zu können. Die Schnellhilfe wird nur mit dem Anspringen via `CTRL` + `.` vorgelesen und nicht mehr, wenn die Pfeiltasten zum Einsatz kommen.

Sollten Sie den Fehler hieraus noch nicht deduzieren können, gibt es die Möglichkeit eine Schnellhilfe von Eclipse zu erhalten. Hierzu drücken Sie die Tasten `CTRL`+`1` und im Anschluss `F2`. Die Tastenkombination `CTRL`+`1` öffnet das Schnellhilfe-Fenster. Mit `F2` wird der Fokus in diesem Fenster verlagert, so dass der Screenreader den Inhalt ausließt.

Sie sollten sich trotz dieser Möglichkeiten nicht allein auf die Intelligenz Ihrer IDE verlassen, denn auch Eclipse hat nicht immer recht!

### Ein Programm ausführen
Nun ist es an der Zeit, Ihr Programm auszuführen. Wenn Sie Ihr Programm zum ersten Mal starten, müssen Sie Eclipse erst mitteilen, als welche Art von Java-Programm das Ihre gestartet werden soll.

Eclipse kennt grundsätzlich zwei gängige Varianten, um Java-Code auszuführen. Einmal das *Java-Applet*, welches im Browser läuft, und die *Java-Application*, ein eigenständiges Programm. Für dieses Tutorial ist nur die *Java-Application* relevant.

Um lästige Systemdialoge zu vermeiden, nutzen Sie den Hotkey *Run as Java Application*, `⇧`+`ALT`+`X`, dann `J`. Falls dieser Shortcut nicht wie beschrieben funktioniert, können Sie Ihr Programm auch mit dem Befehl *Run*, also `CTRL`+`F11`, starten. Wenn Sie Ihr Programm zum ersten Mal auf diese Weise starten, öffnet sich ein Systemdialog, welcher Sie fragt, als welche Art von Anwendung Ihr Programm ausgeführt werden soll. Wählen Sie *Java Application* aus und bestätigen Sie Ihre Eingabe. Ihr Programm wird beim Ausführen dieses Befehls, wie auch beim Speichern mittels `CTRL`+`S`, als Java-Datei in Ihrem *Workspace* gespeichert. Darauf weist Sie der zu bestätigende Systemdialog *Save and Launch* hin.

Um die *Main-Class*, welche den Startpunkt Ihres Programms darstellt, festzulegen, oder, um Parameter an Ihr Programm übergeben zu können, müssen Sie diese Einstellungen im Dialogfeld *Run Configurations* vornehmen. Dieses Dialog erreichen Sie indem Sie `ALT`+`R`, `N` drücken.

Um Ihrem Programm beispielsweise die Argumente *arg1*, *arg2* und *arg3* zu übergeben, drücken Sie nach der Tastenkombination `CTRL`+`R`, `N` solange `TAB`, bis Sie in die Registerleiste gekommen sind. Im Anschluss drücken Sie `CTRL`+`PageDown` um zum Reiter *Arguments* zu gelangen. Dort springen Sie mit `TAB` dann ins Eingabefeld *Program arguments*, wo Sie die gewünschten Argumente durch Leertasten getrennt eingeben können.

Achtung, um aus diesen Textfeld wieder rauszukommen müssen Sie `SHIFT`+`TAB` drücken. Im Anschluss drücken Sie `ENTER`. Diese Eingabe von "arg1 arg2 arg3" käme dem Starten Ihres Programms über die Kommandozeile, mittels "java [Name des Programms] Arg1 Arg2 Arg3", gleich.

### Autovervollständigung mit Code Assist nutzen
Die meisten Menschen schätzen an Entwicklungsumgebungen die programmiersprachenbezogenen Unterstützungen, die die jeweilige Umgebung mitbringt. Was bei Microsoft Visual Studio *IntelliSense* heißt, ist bei Eclipse das Feature namens *Code Assist*.

*Code Assist* wird in einigen Situationen automatisch von der Eclipse IDE ausgelöst, beispielsweise bei der Eingabe eines Punktes (also`.`), nach Variablen oder Klassennamen. Wenn Sie *Code Assist* selbst auslösen möchten, nutzen Sie `CTRL`+`Leertaste`. Zur Veranschaulichung folgt hier ein kleines Beispiel aus dem *Hello World Tutorial*:

Schreiben Sie im Quellcode-*Editor* von Eclipse

	syso

dann `CTRL`+`Leertaste`. Wenn Sie diese Kombination zum ersten Mal ausführen, steht Ihnen bis zur Eclipse-Version Luna die Auswahl *Enable Smart Code Completion* zur Verfügung. Wählen Sie diese aus. Da wird Ihnen zukünftig die Eingabe des Strings 

	syso

gefolgt von dem Shortcut zur Codevervollständigung  `CTRL`+`Leertaste` 

sofort zu 


	System.out.println(); 

komplettiert.

*Code Assist* bietet viele weitere Hilfestellungen.

Stellen Sie sich vor, Sie programmieren seit einigen Stunden und haben gerade eine längere Pause beendet. Eigentlich wollten Sie eine Fallunterscheidung aufstellen, nur von welcher Variable sollte sie abhängen? Statt Ihren Code erneut durchzugehen, drücken Sie einfach "*View*-Menü anzeigen", also `CTRL`+`Leertaste` und drücken Sie im Anschluss `F2`. Das sich nun öffnende *View*-Menü enthält alle möglichen Funktionalitäten, die Sie an dieser Stelle nutzen können, wie zum Beispiel lokale oder globale Variablen, Methoden der jeweiligen Klasse oder statische *Imports*. Damit diese Ihnen vorgelesen werden, müssen Sie mit `F2` den Fokus in diesem Fenster verlagern. Achtung, zwar wird das erste Element der Liste direkt fokussiert, aber von JAWS nicht sofort vorgelesen. Drücken Sie `Pfeiltaste nach unten` und dann wieder `Pfeiltaste nach oben`, um auch das erste Elemente der Liste vorgelesen zu bekommen.

Wenn Sie ein Java-Objekt benutzen möchten, geben Sie mindestens den Anfangsbuchstaben als Großbuchstaben an. Drücken Sie nun den Hotkey für *Code Assist*, also `CTRL`+`Leertaste`. Eclipse öffnet eine Liste von Vorschlägen für Sie, die direkt fokussiert wird. Durch die Liste kann wie gewohnt mit den Pfeiltasten navigiert werden. Für das aktuell fokussierte Objekt wird direkt das zugehörige *JavaDoc* geöffnet. Durch das Drücken der Taste `TAB` springen Sie ins den *JavaDoc*-Bereich und durch das Drücken von `ESC` springen Sie wieder in die Auswahlliste. Mit `ENTER` wählen Sie eine Auswahl aus. Das Ergebnis wird direkt im Quellcode platziert.

*Code Assist* auch sehr gut für Neugierige geeignet, die einfach nur mehr über ein Objekt, das sie verwenden, wissen möchten. Dies bedeutet einfach, dass alle Informationen in der *Online-Java-API*, die aus *JavaDoc-Kommentaren* generiert werden, für Sie verfügbar sind, ohne das Programm zu wechseln.

Sie sollten nun eine gute Vorstellung davon haben, was man mit *Code Assist* alles machen kann. Probieren Sie es aus!

## Tips und Tricks
Eclipse bietet ihnen viele kleine Features, die dafür gemacht wurden, Ihren Programmieralltag zu vereinfachen. Die meisten sind trivial, werden aber häufig genutzt und sorgen für eine enorme Produktivitätssteigerung.

### Gedächtnisstütze für Keyboard-Shortcuts
In Eclipse müssen Sie sich wirklich nur an eine Tastenkombination erinnern, nämlich  `CTRL`+`SHIFT`+`L`. Diese zeigt Ihnen eine alphabetisch sortierte Liste aller Tastaturbefehle in der Eclipse IDE an, welche auch sofort fokussiert ist.

### Code Assist
Dieses Tutorial enthält einen ganzen Abschnitt über die *Code Assist*-Funktion. Diesen finden Sie im Kapitel 3.9 Autovervollständigung mit *Code Assist* nutzen.

#### Vorschläge zur Fehlerbehandlung
Diese Funktion wird im Abschnitt 3.7 Kompilieren und Fehlerbehebung kurz angeschnitten. Eclipse bietet Ihnen eine Funktion, die Ihnen Lösungsmöglichkeiten aufzeigt, um Kompilierfehler und Warnungen zu beheben. Sollte irgendeine Art von Fehler oder Warnung auftreten, springen Sie in die entsprechende Zeile und drücken Sie `CTRL`+`1` und im Anschluss `F2`, um den Fokus in das Schnellhilfe-Fenster zu verlagern. Eine Liste der möglichen Optionen erscheint. Sie enthält nicht immer die besten Lösungsvorschläge, aber oftmals funktionieren sie gut. Dies gilt vor allem bei Fehlern wie vergessenen *Imports*. Dennoch sollten Sie die Vorschläge gut prüfen, bevor Sie diese anwenden.

#### Definitionen einsehen
Im Folgenden werden Shortcuts behandelt, welche dienlich sind, falls Sie Code nutzen, den Sie nicht selbst geschrieben haben. Wenn Sie nämlich direkt zu der Definition einer Methode, Klasse, eines Interfaces oder Ähnlichem springen möchten, nutzen Sie einfach die Taste `F3`.

Um diese Funktion nutzen zu können, müssen Sie allerdings Zugang zu den Quelldateien, also *.java*-Files, haben. Mit vorkompilierten Bibliotheken können Sie diese Funktion nicht verwenden.

#### Alle Attribute und Methoden im aktuellen Editorfenster anzeigen
Eclipse tut wirklich alles, damit Sie sich nicht auf Ihr Gedächtnis verlassen müssen. Sollten Sie sich nicht mehr genau erinnern, wie die Attribute oder Methoden der Klasse heißen, die Sie aktuell bearbeiten, drücken Sie einfach `CTRL`+`O`. Diese Funktion ist aber nicht nur eine Gedächtnisstütze, sondern auch eine perfekte Navigationshilfe. Wählen Sie einfach mit Hilfe der Pfeiltasten das gesuchte Element aus und drücken Sie `ENTER`. Damit springen Sie im *Editor* direkt hinter den Namen in der Variablen- oder Methoden-Deklaration.

#### Perfekte Code-Formatierung
Sie können Ihren Quellcode mit Eclipse auf zwei Arten auto-formatieren.

1. Markieren Sie den gewünschten Abschnitt mit `SHIFT`+`Pfeiltaste nach links`/`Pfeiltaste nach links` und nutzen Sie anschließend `CTRL`+I`. Der markierte Bereich wird perfekt eingerückt.

Um das vorherige Auswählen zu umgehen, nutzen Sie die zweite Option.

2. Der komplette Code der aktuellen .java-Datei wird mittels `CTRL`+`SHIFT`+`F` nach der Java-Standardspezifikation formatiert. Diese Variante beinhaltet auch Abstände und Zeilenumbrüche.

#### Clean Up
Diese Funktion von Eclipse soll nur am Rande erwähnt werden. Wenn Sie in der Menüleiste Source auswählen und hier *Clean Up*, beginnt Eclipse, Ihren Code auf Redundanzen zu untersuchen, um im Anschluss ungenutzte oder bedeutungslose Codefragmente zu eliminieren. Dieses Feature ist dazu entworfen, Ihren Code eleganter zu machen. Wenn Sie diese Funktion auf den von Ihnen geschriebenen Code anwenden, ist es erstrebenswert, dass dieser unverändert bleibt. Falls Sie die Grundprinzipien der Java-Programmierung beherrschen, liegt dies sicher im Bereich Ihrer Fähigkeiten.

#### To-Dos verfolgen
Während des Schreibens von Programmen kommen Ihnen sicherlich immer wieder Dinge in den Kopf, die Sie zu einem späteren Zeitpunkt noch umsetzen möchten. In der Industrie herrscht der Standard, dass solche unerledigten Dinge mittels

	// TODO: Aufgabenbeschreibung
	
gekennzeichnet werden. Eclipse macht Ihnen Ihren Programmieralltag an dieser Stelle leichter, indem es Ihren Quellcode nach solchen Kommentaren durchsucht und diese in einem eigenen Fenster namens *Tasks* bündelt. Dieses erreichen Sie in erster Instanz nur über die Menüleiste, via *Window* bei *Show View* finden Sie *Task*. Wenn Sie das Fenster einmal geöffnet haben, können Sie es über den Shortcut, der zwischen den Ansichten wechselt, also `CTRL`+`F7`, ansteuern. Mit den Pfeiltasten kommen Sie zur gewünschten Ansicht. Die *Tasks*-Ansicht erscheint unter dem *Editor*-Fenster als einer der Reiter auf der Höhe der *Console*, wo auch das *Problems*-Fenster angesiedelt ist. Die einzelnen *Tasks* können mit den Pfeiltasten ausgewählt werden. Drücken Sie `ENTER`, springt Ihr Cursor direkt in die Zeile des jeweiligen *Tasks*.

Die *Tasks-View* wird erst nach dem Kompilieren des Programms aktualisiert und die *Tasks* erschienen in der Liste.

Alle *Tasks* werden projektübergreifend, das heißt für alle in Ihrem *Workspace* geöffneten Projekte angezeigt.

Achtung, verwechseln Sie die *Tasks* nicht mit der *TaskList*!

## Fortgeschrittene Themen
### Ein neues Interface erstellen
Sollten Sie den Abschnitt 3.5 Eine Klasse erstellen bereits gelesen haben, wird Ihnen das hier beschriebene Vorgehen bekannt erscheinen. Drücken Sie nun die Tastenkombination, um eine neue Ressource anzulegen `ALT`+`SHIFT`+`N`. Oder nutzen Sie die Tastenkombination, um eine neue Ressource über das Wizard anzulegen, also `CTRL`+`N`.

Wählen Sie *Interface* aus und spezifizieren Sie das *Package*, falls notwendig. Benennen Sie die neue Ressource. Alle *Interfaces*, die durch das, was Sie neu anlegen, erweitert werden sollen, können Sie durch Bestätigen das *Add*-Schalters im Formular hinzufügen.

Nach Bestätigen des ausgefüllten Formulars wird Ihr neues *Interface* angelegt.

### Arbeiten mit Packages
Ein *Package*, zu deutsch Paket, ist mehr oder weniger das Äquivalent zu *Namespaces* in Sprachen wie Javascript oder C++. Durch das Strukturieren von Klassen in Paketen können Sie sicherstellen, dass keine Namenskonflikte entstehen. In vielen Javaprojekten kommen beispielsweise zwei verschiedene Date-Klassen zum Einsatz, nämlich java.util.Date und java.sql.Date. Jede der beiden Klassen befindet sich innerhalb eines Pakets, einmal des Pakets java.util und einmal des Paket java.sql, so dass keine Konflikte zwischen den beiden Klassen entstehen.

Wäre keine der beiden Klassen innerhalb eines Pakets angesiedelt, würden die Bibliotheken nicht kompilieren. Der Compiler würde eine der beiden Klassen als eine Re-Definition der anderen Klasse ansehen. Dies würde zu Verwirrung führen.

Pakete erlauben auch eine logische organisatorische Abstraktion für verwandte Gruppen von Java-Klassen und Interfaces. Um ein Paket für Ihre Klasse oder Schnittstelle anzugeben, muss die erste Zeile Ihrer Java-Datei wie folgt lauten:

	package [package.name];
	
	
Dieses Tutorial wird hier nicht weiter auf Pakete als Sprachmerkmale eingehen. Es gibt viele Ressourcen, online und anderswo, die Ihnen helfen können, diesen Aspekt der Programmiersprache Java zu verstehen. Sollten Sie absoluter Neuling auf diesem Gebiet sein, kann eine Lösung sein, Ihre Lieblings-Suchmaschine einmal mit dieser Frage zu bemühen. Sollten Sie gezielt mit Paketen arbeiten, wird empfohlen, sich vorher mit den Einschränkungen, die dieses Sprachmerkmal mit sich bringt, vertraut zu machen.

Vielmehr sollen die paketbezogenen Funktionalitäten von Eclipse besprochen werden. Die erste ist der *Package Explorer*. Der *Package Explorer* präsentiert Ihnen Ihre Projekte mit dem Fokus auf deren Java-Paketstruktur. Sollten Sie Eclipse schon einmal genutzt haben, ist Ihnen vielleicht aufgefallen, dass neu angelegte Klassen in Eclipse nicht einfach irgendwo, sondern im sogenannten *default package* auftauchen, welches einen Knotenpunkt in der Hierarchie des *Package Explorers* darstellt. Geben Sie nämlich kein Paket für Ihre neue Java-Klasse an, wird es mit allen anderen nicht verpackten Klassen in diesem Standardpaket gruppiert.

#### In den Package Explorer springen
Um in den *Package Explorer* zu springen, dient Ihnen der Shortcut `ALT`+`SHIFT`+`Q`, `P`.

Um ein neues Paket anzulegen, gehen Sie wie folgt vor: Drücken Sie nun die Tastenkombination für *neue Ressource anlegen*, `ALT`+`SHIFT`+`N`. Es öffnet sich eine Liste, welche Sie durch das Anschlagen der Pfeiltasten fokussieren können. Wählen Sie mit `Pfeiltaste nach unten` das Wort *Package* aus.

Ihr Paket existiert erst dann wirklich, wenn es mit Inhalten, also Ressourcen im Sinne von Klassen oder *Interfaces*, gefüllt wurde. Logischer ist es allerdings, das Paket beim Anlegen einer Klasse zu definieren, wodurch es direkt mit angelegt wird (siehe Kapitel 3.6 Eine Klasse erstellen).

### Dateien importieren
Angenommen, Sie haben Ihr Projekt in Eclipse angelegt, aber wollen die einzelnen Komponenten nicht von Grund auf neu in Eclipse erstellen, sondern einige vorgefertigte Dateien, beispielsweise aus Ihrem lokalen Dateisystem, nutzen. Hierfür gibt es drei Wege für Sehbehinderte, welche Sie nachfolgend aufgelistet finden.

1. Der Weg über die Menüleiste

	Springen Sie in die Menüleiste der Eclipse IDE zu *File* und wählen Sie *Import* aus der Liste aus. Nun öffnet sich das *Import*-Fenster. Der Fokus liegt auf einem Textfeld mit dem Text "*type filter text*". Dieses dient der Eingabe des Suchtextes zur Filterung der möglichen zu importierenden Typen von Quellen. Tippen Sie *File* ein, um die Ergebnisliste zu minimieren. Drücken Sie `Pfeiltaste nach unten`, um in die Auswahlliste zu springen und wählen Sie *File System*. Bestätigen Sie Ihre Auswahl. Es öffnet sich nun ein Fenster, in welchem Sie, unter *From directory*, die gewünschte Datei auswählen und zu Ihrem Eclipse-Projekt hinzufügen können. Statt einer Datei können Sie auch ein ganzes Verzeichnis auswählen. Sobald Sie einen Ordner ausgewählt haben, haben Sie die Wahl, ganze Verzeichnisse oder nur deren Unterkomponenten zu importieren. Es öffnet sich eine Tabelle mit den Inhalten des selektierten Ordners. Um ganze Ordner zu importieren, aktivieren Sie dessen Markierungsfeld. Möchten Sie an dieser Stelle bestimmte Dateien anstelle von ganzen Verzeichnissen auswählen, wählen Sie statt der übergeordneten Komponente dessen gewünschten Inhalt. Jede dieser Dateien kann einzeln ausgewählt werden, genau wie vorher die Verzeichnisse. Des Weiteren haben Sie in diesem Fenster die Möglichkeit unter *Into folder:* das jeweilige *Project*, sowie das *Package* oder, anders formuliert, das Verzeichnis zu spezifizieren, in welches die Datei importiert werden soll. Stellen Sie sicher, dass Sie in den richtigen Ordner importieren und dass die Optionen so eingestellt sind, wie Sie sie wünschen, und bestätigen Sie mit der *Finish*-Taste.


2. Der Weg über das Kontextmenü im *Package Explorer*

	Springen Sie zuerst mit `ALT`+`SHIFT`+`Q`, `P` in den *Package Explorer*. Wählen Sie das richtige Projekt und drücken Sie dann die Kontextmenü-Taste. Sie können das Projekt auch später, wie bereits vorher erwähnt, im *Import*-Dialog noch ändern. Wählen Sie aus der sich öffnenden Liste *Import*. Das *Import*-Fenster wird geöffnet. Ihnen stehen die selben Eingabemöglichkeiten wie auch bei der Auswahl über die Menüleiste zur Verfügung. Gehen Sie ab jetzt genau wie auch dort beschrieben vor.


3. Copy und Paste aus dem Dateisystem

	Kopieren Sie die gewünschte Datei in Ihrem Dateisystem, ganz einfach mit `CTRL`+`C` oder über das Kontextmenü. Gehen Sie in die Eclipse IDE und wählen Sie das Projekt sowie das Paket aus, in welches Sie diese Datei importieren wollen und drücken Sie Einfügen, also `CTRL`+`V`. Die Datei wird nun in das Projekt importiert.

### Archive importieren
Das Importieren eines Archivs ist dem Importieren einer Datei sehr ähnlich. Öffnen Sie das Kontextmenü Ihres Projekts im Paket-Explorer und klicken Sie auf *Import*. Dieses Mal verwenden Sie *Archive File* als Ihren Filtertext und wählen die Option *Archive File*. Bestätigen Sie Ihre Auswahl.

Gehen Sie so vor wie auch beim Importieren von Dateien, aber dieses Mal, anstatt ein Verzeichnis auszuwählen, wählen Sie die benötigte Archivdatei. Dies wird dazu führen, dass Sie das Dateisystem im Archiv so gut wie möglich durchsuchen können, wenn Sie ein Verzeichnis importieren. Wählen Sie Unterordner zum Importieren oder wählen Sie einfach Dateien aus. Nachdem Sie alle Optionen ausgewählt haben, bestätigen Sie mit *Finish*. Ihr Archiv wird nun entpackt und in das Projekt importiert.

Wenn Sie Ihr Archiv stattdessen per Copy und Paste aus dem Dateisystem importieren möchten, wird dieses, falls es nicht bereits entpackt ist, als komprimierter Ordner zum Projekt hinzugefügt. Öffnen Sie diesen Ordner im *Editor*. Da das *Editor*-Fenster nun fokussiert ist, können Sie direkt mit `SHIFT`+`TAB` in die Funktionsleiste des *Editors* navigieren. Diese befindet sich im Falle eines geöffneten Archivs direkt über dem eigentlichen *Editor*-Bereich. Dort steht Ihnen neben einigen anderen auch die Funktion *Extract files from the archive* zur Verfügung. Wählen Sie diese aus. Dadurch öffnet sich das *Select Target to extract to*-Fenster, in welchem Sie den Ort angeben können, an welchem das Archiv entpackt werden soll.

### Code-Refactoring
*Refactoring* bezieht sich auf die Umformung von Code, um seinen Stil, sein Design, oder dergleichen zu verbessern. Das Ergebnis der Ausführung des Codes im Bezug auf den Benutzer ändert sich hierbei nicht. In der Strukturierung, unbemerkt durch den Anwender oder die Anwenderin, fallen die Änderungen jedoch ins Gewicht.

Schon das Umbenennen von Klassen oder Methoden würde in größeren Projekten einen riesigen Aufwand bedeuten. Stellen Sie sich vor, Sie müssten jedesmal einen regulären Ausdruck schreiben, der das für Sie tut, oder gar alles manuell ändern. Natürlich lässt Eclipse Sie hier nicht alleine. Die IDE bietet Ihnen einen einfachen Weg, Ihren kompletten Code mit allen Referenzen auf die umzuformende Code-Passage zu aktualisieren.

Der Hotkey für das *Refactoring* an sich ist `ALT`+`T`,wodurch eine Ansicht geöffnet wird, unter welcher Sie die Art des *Refactoring* wählen können. Die simpelste Umformung ist die *Rename*-Funktion, welche Sie auch über den Shortcut `ALT`+`SHIFT`+`R` erreichen. Die sich öffnende Ansicht beinhaltet außer dem Textfelde für den neuen Namen des umzubenennenden Elementes das Markierungsfeld *Update References*. Stellen Sie sicher, dass dieses ausgewählt ist und bestätigen Sie Ihre Eingabe. Ihre Methode oder Klasse ist nun für alle im *Package Explorer* geöffneten Projekte umbenannt.

### Plugins installieren
#### Eclipse Marketplace
Sie können *Plugins* in Eclipse auf unterschiedliche Weise installieren. Es gibt den *Eclipse Marketplace*, welcher eine Art *Appstore* für Eclipse-*Plugins* ist. Um ein *Plugin* hierüber installieren zu können, muss es im *Marketplace* gehostet werden.

#### Update Manager
Sollte das gesuchte *Plugin* lokal zur Verfügung stehen und nicht im *Eclipse Marketplace* vorhanden sein, können Sie den *Update Manager* nutzen. Die *Eclipse Foundation* empfiehlt eine Installation über den Update-Manager, welchen Sie im Menü unter *Help* bei *Install New Software...* finden. Nach Auslösen des Schalters *Add* können Sie entweder eine URL eingeben, oder durch auslösen der Schaltfläche *Local* ein *Plugin* aus Ihrem Dateisystem wählen. Diese Option prüft zum Beispiel, ob Kompatibilitätsprobleme zu Ihrer Eclipse-Version oder Abhängigkeiten zu anderen *Plugins* bestehen.

#### Manuelle Installation
Ein Plugin in Eclipse manuell zu installieren bedeutet ganz einfach, das *Plugin* in den sich im Installationsordner von Eclipse befindenden Ordner namens *Plugins* zu legen. Starten Sie danach die IDE neu.

## Suche und Navigation
### Suchen/Ersetzen-Funktionalität im Editor
Mit Hilfe des Shortcuts `CTRL`+`F` öffnen Sie das *Suchen und Ersetzen*-Fenster. Geben Sie den gesuchten Wert ein und gegebenenfalls den, mit welchem dieser ersetzt werden soll, und bestätigen Sie Ihre Eingaben mit dem gewünschten Schalter. Ihnen stehen hierfür in erster Instanz *Find* und *Replace All* zur verfügung.

Wurde bereits *Find* angewendet, haben Sie die zusätzlichen Optionen *Replace/Find*, die einen Wert nach dem anderen ersetzt, sowie *Replace*, welches nur einen einzelnen Wert mit dem zu ersetzenden auswechselt.

### Die Zurück-Funktion
In jedem *Wizard*-Formular, welches Sie in Eclipse ausfüllen, befindet sich ein Zurück-Schalter. Falls Sie also versehentlich die falsche Art von Java-Datei, z.B. *Class* statt *Interface*, gewählt haben, können Sie über diesen Schalter im Formular zurücknavigieren und Ihre Eingabe korrigieren.

### Navigation im Editor
Der *Editor* ist das Fenster, in welchem Sie Ihren Quellcode schreiben. Dieser ähnelt den gängigen Text-Editoren, die Sie auch für das reine Editieren von Fließtexten kennen. Der *Editor*, welcher in Eclipse integriert ist, bietet zusätzlich noch einige visuelle Hilfen zum Erstellen von Software, auf welche in diesem Tutorial bewusst nicht eingegangen wird.

Die nächsten Unterüberschriften beschäftigen sich mit den Möglichkeiten, den *Editor* als blinder Programmierer effizient zu nutzen.

#### Von überall in den Editor springen
Der Fokus des Cursors wechselt, je nachdem in welchem Bereich der Eclipse IDE Sie sich gerade befinden. Es ist ineffizient, die einzelnen Bereiche der Eclipse IDE der Reihenfolge nach anzusteuern, um in den gewünschten Bereich zu gelangen.

Wie Sie bereits im Laufe dieses Tutorials erfahren konnten, bietet Eclipse die Möglichkeit, mittels Shortcuts oder Hotkeys direkt in bestimmte Bereiche zu springen.

Um von einer beliebigen Stelle in der Eclipse IDE in den *Editor* zu springen, nutzen Sie die Taste `F12`. In Einzelfällen funktioniert diese Schnellnavigation nicht, dann muss man explizit in die *Editor*-Ansicht navigieren.


#### Zwischen den offenen Editor-Fenstern navigieren
Während der Entwicklung eines Programmes öffnen wir für gewöhnlich viele *Editor*-Fenster. Jedesmal, wenn wir eine Klasse aus dem *Package Explorer* auswählen, öffnet Eclipse diese automatisch in einem neuen Fenster. Somit können all diese geöffneten *Editor*-Fenster bis sie aktiv geschlossen werden, auch erreicht werden. Die Eclipse IDE bietet Ihnen im Großen und Ganzen drei Möglichkeiten, um komfortabel zwischen den offenen *Editor*-Fenstern zu navigieren.

Wenn Sie einen bestimmten Pfad beschreiten wollen, ist es hilfreich, wenn Sie sich erst einmal die Möglichkeiten anzeigen lassen, wo Sie hingehen können. So verhält es sich auch im Fall von mehreren geöffneten *Editor*-Fenstern.

Der Shortcut, um offene Editoren anzeigen zu lassen, ist in der Standardeinstellung `CTRL`+`E` belegt.

Wenn Sie stattdessen die Tastenkombination `CTRL`+`F6` oder `CTRL`+`SHIFT`+`F6` nutzen, zeigt dies auch offene Editoren an, wobei der Wechsel zwischen den Fenstern sofort nach loslassen der `CTRL`-Taste erfolgt.

#### Zu einer bestimmten Zeile im Editor springen
Um in eine bestimmte Zeile im *Editor*-Fenster zu springen, muss dieses fokussiert sein. Nutzen Sie den Shortcut `CTRL`+`L`, der das Fenster *go to line*  öffnet, geben Sie die gewünschte Zeilennummer ein und bestätigen Sie Ihre Eingabe.

### Navigation in der Console
#### Aufbau der *Console*-Ansicht
Die drei Konsolen, die standardmäßig in Eclipse zur Verfügung stehen, sind die *Process Console*, die *Stacktrace Console* und die *CVS Console*.

Die in der *Console* verfügbaren Befehle werden im Folgenden behandelt und können mit aktiviertem JAWS-Cursor angesteuert werden. Sie sind durch beschriftete *Icons* abgebildet. Diese befinden sich rechts auf der Höhe des *Console*-Reiters. Sollte die Breite Ihres Bildschirms nicht ausreichen, um die *Icons* neben den Reitern darzustellen, verschieben sich diese leicht nach unten.

Es handelt sich um *Clear Console*, *Display Selected Console*, *Open Console*, *Pin* und *Scroll Lock*. In diesem Tutorial soll nur *Open Console* näher besprochen werden.

Sollten Sie Ihre *Console* aus irgendeinem Grund einmal geschlossen haben, können Sie diese mittels des Shortcuts um in die Konsole zu springen, `ALT`+`SHIFT`+`Q`,`C`, erneut öffnen. Egal ob eine *Console* geöffnet ist oder nicht, mit diesem Shortcut springen Sie direkt hinein.

#### Weitere Console-Fenster öffnen
In manchen Fällen kann es nötig sein, eine zweite *Console* zu öffnen. Hier kommt der  JAWS-Cursor ins Spiel.
Springen Sie zuerst in die *Console*, um schon in der Nähe des Bereichs zu sein.
Aktivieren Sie den JAWS-Cursor, in dem Sie `Insert`+`-` auf dem Nummernpad drücken. Sie hören nun "ziehe JAWS zu PC". Nun können Sie mit den Pfeiltasten den Cursor bedienen. 

Nutzen Sie jetzt die Pfeiltasten, um etwas nach oben und rechts zu navigieren. Leider sind die einzelnen *Icons* in der Leiste der *Console* standardmäßig nicht beschriftet. Bleiben Sie an dieser Stelle probierfreudig. Mit der Taste `/` können Sie einen Linksklick auf ein Element ausführen. Wenn Ihnen JAWS das Wort "Kontextmenü" mitteilt, befinden Sie sich in dem Drop-Down, in welchem Sie eine neue *Console* öffnen können. Navigieren Sie mit den Pfeiltasten zu *New Console View* und drücken Sie `ENTER`. Sie haben nun eine zweite *Console* geöffnet.

Drücken Sie `F12`, um wieder zurück in den *Editor* zu springen.

#### Exceptions in der Console
Beim Ausführen eines Programmes werden oft, je nach Parameter, Fehler oder Ausnahmen provoziert. Gerade in den Randfällen kann es schnell einmal zu einer *NullPointerException* kommen, wenn Sie als Programmierer diesen Fall im Vorfeld nicht bedenken. Auch hier bietet Eclipse Ihnen eine Hilfestellung, um schnell an die Stelle, an welcher die *Exception* geworfen wird, zu gelangen.

Sollte Ihr Programm eine *Exception* ausgelöst haben, stellt Eclipse diese Ausgabe in der *Console* mit einem Link dar.

Sollte beispielsweise eine *IndexOutOfBoundsException* geworfen werden, würde Ihr Screenreader in etwa verlauten lassen:

	Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
	at hello.world.Main.foo(Main.java:23)
	at hello.world.Main.main(Main.java:18)
	
Diese Ausgabe möchte ich Ihnen nun Zeile für Zeile erläutern.

In Zeile 1:

	Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
	
teilt Ihnen Eclipse mit, dass im Haupt-Thread Ihrer Anwendung, im Thread *main*, eine *ArrayIndexOutOfBoundsException* an der Stelle 2 geworfen wurde.

In Zeile 2:

	at hello.world.Main.foo(Main.java:23)

informiert Sie Ihre IDE, dass diese Exception in der Klasse mit dem Namen Main, des Paketes namens hello.world, in der mit foo benannten Methode, in Zeile 23 geworfen wurde. Der letzte Teil, nämlich

	(Main.java:23)
	
ist der Link in Zeile 23.

Zeile 3:

		at hello.world.Main.main(Main.java:18)

erläutert, dass die Ausnahme in der Zeile 18, der Klasse mit dem Namen Main, welche sich in einem Paket namens hello.world befindet, in der mit main benannten Methode, in Zeile 18 ausgelöst wurde.

Der hintere Teil ist wiederum der Link zur Zeile, also

	(Main.java:23)


Mit diesem Wissen stehen Ihnen folgende Möglichkeiten zur Verfügung, um an die angegebenen Stellen zu gelangen.

1. Nutzung des Shortcut *go to line*

	Verwenden Sie den Shortcut *go to line*, also `CTRL`+`L` und geben Sie die Zeilennummer ein, in welcher die *Exception* entstand oder ausgelöst wurde. Sie springen nun direkt zurück in den *Editor* in die angegebene Zeile. Der Fokus liegt am Anfang der Zeile.
	
2. Nutzung des JAWS-Cursor 

	Aktivieren Sie den JAWS-Cursor, navigieren Sie mit den Pfeiltasten an die verlinkte Stelle und lösen Sie einen Linksklick aus. Sie springen nun direkt zurück in den *Editor* in die angegebene Zeile. Der Fokus liegt im Gegensatz zur Möglichkeit 1 am Ende des Ausdrucks, der die Ausnahme auslöste.


### Navigation in der Problems-View
Ein Weg zu *Problems* ist der Shortcut zum Öffnen der Listenansicht aller *Views*, also `CTRL`+`SHIFT`+`F7`. Wählen Sie in der Ansicht mit den Pfeiltasten *Problems* aus.

Alternativ steht Ihnen der Shortcut, um in *Problems* zu springen, nämlich `ALT`+`SHIFT`+`Q`,`X` zur Verfügung.

#### Wie ist die Problems-View aufgebaut?
Die Ansicht der *Problems* ist eine schlichte Baumansicht mit allen Fehlern und allen Warnungen aus allen geöffneten Projekten. Die Probleme sind nach Typ strukturiert. Hieraus resultiert ein Baum pro Typ, also je nach Vorkommnis in all den in der IDE geöffneten Projekten maximal zwei Bäume. Hierfür ist einer für *Warnings* und der andere für *Error* reserviert.

Die Navigation in dieser Ansicht gestaltet sich intuitiv. Mit der Taste `Pfeiltaste nach rechts` klappen Sie die jeweilige Baumansicht auf. Mit `Pfeiltaste nach oben` oder `Pfeiltaste nach unten` navigieren Sie durch die Warnungen beziehungsweise durch die Fehler. Mit `ENTER` gelangen Sie direkt in die Zeile, hinter das Auftreten des jeweiligen Fehlers beziehungsweise der jeweiligen Warnung. 

## Erstellen einer Hello-World-Applikation
### Anlegen von Java-Dateien
Erstellen Sie ein neues Projekt  und geben Sie dieser den Namen eclipseTutorial, für eine Hilfestellung siehe Kapitel 3.4 Ein Projekt anlegen. Legen Sie im neu angelegten Projekt eine neue Java-Klasse an und geben Sie ihr den Namen *Main*, wie im Kapitel 3.6 Eine Klasse erstellen* beschrieben. Sorgen Sie dafür, dass die Klasse, die Ihnen erstellt wird, bereits eine *main*-Methode enthält. In Ihrem *Workspace* wurde nun eine Datei mit dem Namen *Main.java* erstellt.

### Zeilenweise navigieren
Navigieren Sie nun zu Zeile 6. Dafür haben Sie zwei Möglichkeiten. Entweder Sie nutzen die Pfeiltasten oder Sie wählen den Shortcut *go to line*, `CTRL`+`L` und geben in dem sich nun öffnenden Formular die Zeilennummer 6 an.

In Zeile 6 befindet sich ein Kommentar, der automatisch beim Anlegen der Java-Datei mit der *main*-Methode generiert wurde. Der Kommentar lautet

	//TODO Auto-generated method stub

### Codevervollständigung
Ersetzen Sie den Kommentar durch einen *print*-Befehl. Markieren Sie hierfür den Kommentar und tippen Sie


	syso

dann `CTRL`+`Leertaste`. Wenn Sie diese Kombination zum ersten Mal ausführen, steht Ihnen bis zur Version Luna von Eclipse die Auswahl *Enable Smart Code Completion* zur Verfügung. Wählen Sie diese aus. Damit wird Ihnen zukünftig die Eingabe des Strings

	syso

gefolgt von dem Shortcut zur *Codevervollständigung*  `CTRL`+`Leertaste`, 

sofort zu 


	System.out.println(); 

komplettiert.

Sollten Sie Eclipse Neon nutzen, steht Ihnen diese Option in der Liste nicht zur Verfügung.

Der Fokus liegt nun in den Klammern, also bei den Parametern des Aufrufens der *print*-Funktion.

Ergänzen Sie den Methodenaufruf mit dem String

	"Hello World!"

Ihr Programm ist jetzt fertig.

### Fehlerprüfung
Der Shortcut um *zur nächsten Warnung oder zum nächsten Fehler springen*, `CTRL`+`.` , hilft Ihnen, Ihr Projekt auf Fehler oder Warnungen zu überprüfen. Der Screenreader springt damit zum nächsten Fehler oder zur nächsten Warnung. Wie bereits in Kapitel 3.7 erwähnt, wird der Fehler von JAWS nicht sofort vorgelesen. Nutzen Sie `Pfeil nach links` und dann erneut `CTRL`+`.`. Nun wird der Fehler vorgelesen. Schweigt der Screenreader, ist kein Fehler vorhanden.

### Programmausführung
Nun können Sie Ihr Programm ausführen. Nutzen Sie hierfür den Shortcut *Run* `CTRL`+`F11`. Ihr Programm wird beim Ausführen dieses Befehls, genau wie beim Speichern mit `CTRL`+`S`, als Java-Datei in Ihrem *Workspace* gespeichert. Darauf weist Sie der zu bestätigende Systemdialog *Save and Launch* hin.

### Ansicht wechseln  
Wechseln Sie zwischen den Ansichten, mit `CTRL`+`F7`, um zur Ausgabe Ihres Programms in der Console zu gelangen. Halten Sie `CTRL` gedrückt. Es wird eine Liste aller *Views* geöffnet, durch welche Sie mit `Pfeiltaste nach unten`/`Pfeiltaste nach oben` navigieren können. Wählen Sie *Console* aus.

Alternativ gelangen Sie auch mit dem Shortcut zum in die *Console* springen, also `CTRL`+`SHIFT`+`Q`, dann `C`, direkt in die *Console*.

Ihr Screenreader sollte nun verlauten lassen: Hello World!

Herzlichen Glückwunsch zu Ihrer ersten Hello-World-Applikation, erstellt in der Eclipse IDE mit dem Screenreader JAWS.


### Fehlerbehebung
Lassen Sie uns nun einen Fehler provozieren. Springen Sie hierfür zurück in den *Editor* mittels `F12` oder drücken Sie den Hotkey um zwischen den Ansichten zu wechseln, also `CTRL`+`F7` und halten Sie `CTRL` gedrückt. Es ist eine Liste aller *Views* geöffnet, durch welche Sie mit `Pfeiltaste nach unten`/`Pfeiltaste nach oben` navigieren können. Wählen Sie *Editor* aus.

Springen Sie mittels *go to line*, also `CTRL`+`L`, in Zeile 6 und löschen Sie das Semikolon hinter dem *print*-Befehl, sodass folgende Syntax übrig bleibt
	
	System.out.println("Hello World!")
	
und führen Sie das Programm erneut mit *Run* aus. Eclipse warnt Sie zwar schon, dass es Fehler im existierenden Projekt gibt, führen Sie es dennoch aus und springen Sie zurück in die *Console*, mit dem Shortcut `CTRL`+`⇧`+`Q`,`C`. Dort sollte nun folgende Ausgabe stehen:

	Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
	Syntax error, insert ";" to complete Statement

	at hello.world.Main.main(Main.java:7)
	
Um den Fehler zu finden, haben Sie jetzt mehrere Möglichkeiten, davon sind zwei aufgrund der schnellen Anwendung für Screenreadernutzer zu empfehlen:

1. Fehlersuche im *Editor* 

	Drücken Sie `CTRL`+`.`, um zum nächsten Fehler zu springen  und direkt im Anschluss `INSERT`+`PageDown`, um sich den Fehler vorlesen zu lassen. `INSERT` + `PageDown` ist ein Shortcut für JAWS, um die Statusleiste auszulesen.
	
2. Fehlersuche in der *Problems*-Ansicht

	Sobald Sie ihr Programm gespeichert haben aktualisiert sich in der Regel die *Problems*-Ansicht. Springen Sie in diese mittels ``ALT`+`SHIFT`+`Q`, `X`. Dort finden Sie das aufklappbare Listenelement *Errors*. Wenn Sie mit `Pfeiltaste nach rechts` dieses Listenelement ausklappen, erhalten Sie die Fehlermeldung: 

	'Syntax error, insert ";" to complete Statement'
	
	und weitere Zusatzinformationen wie Dateinamen und Zeilennummer. Betätigen Sie die `ENTER`-Taste, während die Fehlermeldung fokussiert ist, um  direkt in den *Editor* in die Fehlerzeile zu springen.

Die Baumansicht in der *Problems-View* wird erst nach dem Kompilieren des Programms aktualisiert und durch JAWS vorgelesen.

Die *Problems*-Ansicht beinhaltet allerdings nur Probleme die zur Kompilierzeit bekannt sind, Fehler die während der Ausführung entstehen, sogennante *RunTimeErrors*, werden nur in der *Console* angezeigt. Somit können die beiden hier vorgestellten Fehlerbehebungsmaßnahmen für solche Fehlertypen nicht angewendet werden. Um solch einen Laufzeitfehler zu provozieren, erzeugen wir abschließend eine *ArrayIndexOutOfBoundsException*.

Hierfür legen Sie ein *Array* an. Springen Sie mit *go to line*, also `CTRL`+`L` zu Zeile 6. Verschieben Sie Ihre Ausgabe von "Hello World!" mit Hilfe der `ENTER`-Taste und legen Sie in der Zeile ein *Array* an. Lösen Sie eine *ArrayIndexOutOfBoundsException* in der darauffolgenden Zeile aus. Versuchen Sie z.B auf den Index 2 zuzugreifen, wobei Ihr *Array* nur 2 Stellen, also die Indizes 0 und 1, besitzt. Nutzen Sie hierfür folgende Syntax

	int []a = new int [2];
	System.out.println(a[2]);
	
Wenn Sie Ihr Programm nun mit *Run*, also `CTRL`+`F11`, starten, wird eine *ArrayIndexOutOfBoundsException* geworfen.

Springen Sie zurück in die *Console* mittels `ALT`+`SHIFT`+`Q`, `C`. Ihnen wird nun die *Exception* vorgelesen. Nun können Sie, wie bereits zuvor beschrieben, über die *Console* zur genannten Zeile springen und Ihren Fehler beheben.

### Der Terminate-Schalter
Es kann vorkommen, dass Ihr Programm auf einmal nicht mehr läuft und in einer Endlosschleife gefangen ist, je nachdem mit welchen Werten Sie beispielsweise eine Schleife betreten.

Was tun?

Als durchschnittlicher Nutzer wäre die Frage ganz einfach zu beantworten: Man klickt auf den roten *Terminate*-Schalter, der das Programm sofort beendet. Es ist zwar ein Shortcut zum Auslösen der *Terminate*-Funktion voreingestellt, allerdings ist dieser dem *Debug*-Modus vorbehalten.

Statt Eclipse jedesmal zu schließen, wenn sich Ihr Programm nicht wie vorgesehen beenden lässt, lernen Sie nun einen Weg kennen, wie Sie Ihr Programm in der IDE terminieren können.

Lassen Sie uns zuerst dafür sorgen, dass unser kleines Hello-World-Programm endlos durchläuft.

Springen Sie in die letzte Zeile Ihrer *main*-Methode der Klasse Main. Nutzen Sie hierfür den Weg über die Ansicht der *Outline*.  Die *Outline-View* zeigt Ihnen das Gerüst der aktuellen Klasse an, mit all ihren Variablen und Methoden. Der Shortcut, um in die *Outline* zu gelangen, ist `ALT`+`SHIFT`+`Q`, `O`. Wir nutzen nun allerdings nicht die *Outline-View*, sondern die *Quick Outline*, welche Sie mit `CTRL`+`O` öffnen. Dadurch erscheint ein Fenster mit der *Outline* der aktuellen Klasse als Listenansicht. Diese liegt als neue Ebene über dem *Editor*-Fenster und schließt sich nach Ausführen der gewünschten Aktion von selbst. Suchen Sie die *main*-Methode aus dieser Liste heraus und bestätigen Sie Ihre Auswahl. Der Fokus liegt nun auf Ihrer *main*-Methode, hinter deren Namen. Um schnell an das Ende der Methode zu gelangen, kann es nützlich sein, erst eine Zeile nach unten zu gehen und dann *Go to matching bracket* mit `SHIFT`+`CTRL`+`P` direkt hinter die schließende Klammer der Methode zu springen. Mit `ALT`+`Pfeiltaste nach unten` verschieben Sie einfach die schließende Klammer der Methode eine Zeile nach unten und haben darüber Platz für Ihre Endlosschleife. Sie können auch einfach eine Zeile höher gehen und `ENTER` drücken. Wie Sie die benötigte Zeile einfügen, bleibt ganz Ihrer Vorliebe überlassen. Erweitern Sie nun die *main*-Methode um eine Endlosschleife.

Eine mögliche Syntax ist:
	while (true) {
		System.out.		println("La la la!");
	}

Wenn Sie nun mit `CTRL`+`F11` Ihr Programm starten, wird dieses sich nicht von alleine beenden. Im Normalfall wundern Sie sich vielleicht, warum Ihr Programm nicht die gewünschte Ausgabe erzeugt, Sie werden sich aber nicht sofort bewusst sein, dass Sie sich in einer Endlosschleife befinden. Springen Sie in die *Console* (`ALT`+`SHIFT`+`Q`, `C`), um die Ausgabe Ihrer Applikation zu überprüfen. Ihr Screenreader sollte nun ununterbrochen "La la la!" verlauten lassen. Eine Navigation durch die Ausgaben der *Console* ist nur schwer möglich, da diese fortlaufend aktualisiert wird.

Da Sie sich bereits mit dem Fokus in der *Console* befinden, reicht es aus, die Kontextmenü-Taste zu betätigen, um eine Strukturansicht aufzurufen. Wählen Sie aus der Liste *Terminate/Disconnect All*.

Sie haben Ihr Programm beendet, ohne dabei die Eclipse IDE beenden zu müssen.

Leider können Sie den Erfolg dieser Aktion nur schwer verifizieren. Eine Möglichkeit, dies zu tun, wäre zum Beispiel zu versuchen, an das Ende der Ausgabe in der *Console* zu navigieren. Hat die Ausgabe ein Ende, ist auch Ihr Programm erfolgreich beendet worden, es sei denn Sie befinden sich in einer Endlosschleife ohne Ausgabe.

Überzeugender ist der erneute Weg über das Kontext-Menü der *Console*. Wenn die Option *Remove All Terminated* akustisch als nicht verfügbar gekennzeichnet ist, gibt es keine terminierte Ausführung. Somit können Sie davon ausgehen, dass kein Programm beendet wurde. Sollte Ihr Programm noch laufen, steht Ihnen die Option *Terminate/Disconnect All* zur Verfügung. Wählen Sie diese aus und versuchen Sie danach erneut *Remove All Terminated* auszuwählen, um sicherzustellen, dass das Programm beendet wurde und die Ausgaben in der *Console* gelöscht sind.