---
ID: 13
post_title: Usability
author: amidisturbing
post_date: 2017-03-24 16:00:12
post_excerpt: ""
layout: page
permalink: >
  http://www.amidisturbing.com/tutorial/usability/
published: true
---
[github_readme repo=“github.com/amidisturbing/eclipse_accessibility“]

<h1>Eclipse Tutorial</h1>

Dieses Tutorial richtet sich an blinde Softwareentwickler/innen, die in der Hochsprache Java innerhalb der Eclipse IDE Programme schreiben möchten und bis jetzt kein geeignetes Tutorial für sehbehinderte Menschen finden konnten. Das gewählte Betriebssystem ist Windows. Als unterstützende Technologie wird der Screenreader JAWS genutzt. Sollten Sie mit NVDA oder einem anderen Screenreader vertraut sein, spricht nichts dagegen, dieses Tutorial mit dem Screenreader Ihrer Wahl zu bearbeiten.

Die Grundlage für dieses Tutorial bietet ein <a href="https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml">Eclipse Tutorial</a> der <em>University of Washington</em>, welches unter der URL <a href="https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml">https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml</a> abrufbar ist.

<h2>1. Was ist die Eclipse IDE?</h2>

Die Eclipse IDE (Integrated Development Environment) ist eine generische, quelloffene Software-Entwicklungsumgebung. Diese basiert auf einem <em>Plugin</em>-Modell, das es ermöglicht die IDE betriebssystemübergreifend für verschiedenste Entwicklungen zu nutzen, sofern Java auf dem System installiert ist.

<h2>2. Installation</h2>

<h3>2.1 Anforderungen</h3>

Vor der Installation der Eclipse IDE muss entweder das JDK (Java Development Kit) oder die JRE (Java Runtime Environment) auf ihrem Computer installiert sein. Sie können diese unter <a href="http://java.sun.com/javase/downloads/index.jsp">http://java.sun.com/javase/downloads/index.jsp</a> downloaden.
Die Installation des JDK wird angeraten, da dieses Ihnen den Zugriff auf die Dokumentation und den Quellcode der Standard-Java-Klassen ermöglicht.

<h3>2.2 Download</h3>

Die offizielle Seite für den Download der Eclipse IDE ist <a href="https://www.eclipse.org/downloads">https://www.eclipse.org/downloads</a>. Um die Navigation so einfach wie möglich zu halten, startet dieses Tutorial eine Ebene tiefer auf der Eclipse-Website, als es der offizielle Download-Link tut.

<ol>
<li>Rufen Sie die Seite <a href="https://www.eclipse.org/downloads/packages">https://www.eclipse.org/downloads/packages</a> in Ihrem Browser auf.</li>
<li>Laden Sie die <strong>Eclipse IDE für Java Developers</strong> herunter. </li>
</ol>

<em>Anmerkung: Sie haben hier die Wahl zwischen <strong>Eclipse IDE für Java Developers</strong>, <strong>Eclipse IDE für Java EE Developers</strong> und weiteren Versionen für Java-Entwickler. Alle sind für dieses Tutorial geeignet.</em>

Zur Auswahl der jeweiligen Eclipse-Version gelangen Sie im Hauptbereich der Seite. Nutzen Sie hierfür den Link <em>Skip to main content</em> am Anfang der Seite. In diesem stehen pro Eclipse-Variante fünf Download-Links zur Verfügung. Die Links im Hauptbereich der Seite teilen sich der Reihe nach wie folgt auf:

<ol>
<li>Link zur Übersichtsseite des Pakets</li>
<li>Link zur Downloadseite der Version für Windows 64-bit</li>
<li>Link zur Downloadseite der Version für Mac 64-bit</li>
<li>Link zur Downloadseite der Version für Linux 32-bit</li>
<li>Link zur Downloadseite der Version für Linux 64-bit</li>
</ol>

Falls Sie also Linux oder Mac nutzen, finden Sie auch hierfür die entsprechenden Downloadlinks im Hauptfenster der Downloadseite.

<h2>2.3 Eclipse auf dem PC installieren</h2>

<ol>
<li>Verschieben oder kopieren Sie das heruntergeladene .zip- oder .tar.gz-Archiv in Ihr Root-Verzeichnis (unter Windows **C:&#42;*).</li>
<li>Entpacken Sie das Archiv. Daraufhin wird Ihnen ein Ordner namens <strong>eclipse</strong> im aktuellen Verzeichnis erstellt.</li>
</ol>

<h2>3. Grundlagen</h2>

Sowohl Eclipse als auch Screenreader wie JAWS haben viele Shortcuts, die die Arbeit mit diesen Programmen enorm beschleunigen bzw. vereinfachen. So kann es vorkommen, dass zwei Tastenkombinationen sowohl von JAWS (oder einem anderen Screenreader) als auch von Eclipse für eine bestimmte Funktionalität reserviert sind. Da der Screenreader in der Regel zunächst alle Tastenkombinationen abfängt, besitzt bei einer Shortcutüberlappung der Screenreader Vorrang. Um die gewünschte Tastenkombination an die Anwendung durchreichen zu können, müssen Sie bei JAWS <code>JAWSTASTE</code>+<code>F3</code> drücken und dann die Tastenkombination ausführen. Wenn also in diesem Tutorial manche Shortcuts aufgeführt werden, die nicht auf Anhieb bei Ihnen funktionieren, könnte es sein, dass der Screenreader diese Tastenkombination belegt.

<h3>3.1 Starten und der Startbildschirm</h3>

<ol>
<li>Führen Sie die Datei <strong>eclipse.exe</strong> aus.</p></li>
<li>Legen Sie Ihren Arbeitsbereich, den sogenannten <em>Workspace</em>, fest. Für dieses Tutorial ist der vorausgewählte <em>Workspace</em> im Ordner <strong>C:eclipse</strong> am besten geeignet.</p></li>
</ol>

<p><em>Anmerkung: Der Workspace kann für jede Sitzung neu definiert werden. Falls Sie nur einen Workspace für all Ihre Projekte benötigen, aktivieren Sie die Checkbox "Use this as default and do not ask again". Unter Windows: Halten Sie die <code>ALT</code>-Taste gedrückt und drücken Sie zusätzlich<code>U</code>.</em>

<ol>
<li>Starten Sie die Eclipse IDE.

</li>
<li>

Bei erstmaligem Starten sehen Sie den <em>Welcome</em>-Bildschirm. Dieser stellt eine gewisse Barriere dar. In dem Fenster befindet sich (ab Eclipse Neon) ein Markierungsfeld mit der Beschriftung "Always show Welcome at start up". Dieses ist per default aktiviert. Deaktivieren Sie es. Der <em>Welcome</em>-Bildschirm stellt so beim nächsten Start keine Hürde mehr dar.

</li>
<li>

Tabben Sie zu <em>Workspace</em> und bestätigen Sie. Nun befinden Sie sich in Ihrem Arbeitsbereich. Die für dieses Tutorial wichtigsten Ansichten sind der <em>Package Explorer</em>, der <em>Editor</em> und die <em>Console</em>.

</li>
</ol>

<h4>3.1.1 Aufbau der Standardansicht</h4>

Nachdem der <em>Welcome-Bildschirm</em> geschlossen wurde, befinden Sie sich in der Standard-Entwickleransicht der Eclipse IDE, in welcher Ihnen die wichtigsten Ansichten sofort zur Verfügung stehen. Der <em>Package Explorer</em> beinhaltet alle geöffneten Projekte, welche sich in Ihrem <em>Workspace</em> befinden. Einzelne Dateien können Sie im <em>Editor</em> öffnen, bearbeiten und speichern. Dieser steht Ihnen ebenfalls in der Standardansicht zur Verfügung, ebenso wie das <em>Console</em>-Fenster, welches die Ausgaben Ihres Programmes darstellt.

Der Fokus liegt beim erstmaligen Starten auf dem <em>Package Explorer</em>. Wenn Sie allerdings bereits ein Projekt mit einer Klasse erstellt haben und diese im <em>Editor</em> beim letzten Beenden des Programms geöffnet ließen, liegt der Fokus im <em>Editor</em>, an der Stelle, an der er auch beim Beenden des Programmes lag.

<h3>3.2 Wie Dateien organisiert werden</h3>

<h4>3.2.1 Workspaces und Projekte</h4>

Eclipse nutzt zwei grundlegende Abstraktionen zum Strukturieren von Quellcode.

<h5>3.2.1.1 Workspace</h5>

Der <em>Workspace</em> ist das Arbeitsverzeichnis für all Ihre Projekte. Sie können mit Eclipse auch mehrere <em>Workspaces</em> verwalten, falls Sie dies wünschen.

<h5>3.2.1.2 Project</h5>

Ein <em>Project</em> ist eine Sammlung zusammengehörigen Quellcodes, welcher meist ein unabhängiges Programm formt.
Kurz gesagt ist Ihr <em>Workspace</em> der Ordner, der all Ihre Projekte beinhaltet.
Einem <em>Project</em> ist auch ein <em>Classpath</em> zugeordnet. Der <em>Classpath</em>  ist der Ort, an welchem Bibliotheken und andere Projekte eingebunden werden. Das Tutorial widmet sich dem  <em>Classpath</em> später in einem eigenen Abschnitt.

<h5>3.2.1.3 Strukturierung des Workspace und der Projekte</h5>

Immer, wenn Sie in Eclipse ein Projekt anlegen, wird von Eclipse automatisch ein neuer, gleichnamiger Ordner im aktuellen <em>Workspace</em> angelegt. In diesem Ordner werden zwei weitere Ordner, nämlich <em>bin</em> und <em>src</em> (source) angelegt. Sie können den Ordner <em>bin</em> ignorieren. In diesem werden automatisch alle Kompilate, also die <em>.class</em>-Dateien, gespeichert.

All Ihre <em>.java</em>-Dateien befinden sich im <em>src</em>-Ordner.

Zusammengefasst ist also ihr <em>Workspace</em> der Ordner, welcher alle Projekte beinhaltet, welche wiederum Ordner, benannt nach den zugehörigen Projekten, sind.

<h3>3.3 Einen Workspace anlegen</h3>

Sie können sich Ihren <em>Workspace</em> auch wie den Root-Folder, von welchem Eclipse ausgeht, vorstellen. Sie können zwar mehrere <em>Workspaces</em> mit Eclipse verwalten, allerdings können Sie nur einen <em>Workspace</em> gleichzeitig in Eclipse öffnen. Der <em>Welcome</em>-Bildschirm und wie Sie diese Hürde meistern wurde bereits im Kapitel Grundlagen unter 3.1 Starten und der Startbildschirm erklärt. Tabben Sie also zu <em>Workspace</em> und bestätigen Sie. Sollten Sie während des Arbeitens mit Eclipse einen neuen <em>Workspace</em> anlegen oder einen bereits bestehenden <em>Workspace</em> auswählen wollen, gehen Sie über die Menüleiste zu <em>File</em> und dort zu <em>Switch Workspace</em>. Es öffnet sich ein weiteres Untermenü, in welchem Sie einen Eclipse bereits bekannten <em>Workspace</em> auswählen können. Sie können stattdessen auch die Option <em>Other</em> in diesem Untermenü nutzen, um das Fenster <em>Workspace Launcher</em> zu öffnen. Im <em>Workspace Launcher</em> liegt der Fokus zuerst auf einem Auswahlmenü, in welchem Sie wiederum die bekannten <em>Workspaces</em> auswählen können. Alternativ steht Ihnen die Möglichkeit zur Verfügung, zu einem <em>Workspace</em> im Dateisystem zu navigieren und einen bestehenden oder neuen Ordner als <em>Workspace</em> auszuwählen. Von der Verwendung eines Ordners, der bereits Dateien enthält, die keine Eclipse-Projekte sind, wird abgeraten. Bei der Erstauswahl eines Ordners als <em>Workspace</em> wird in diesem ein versteckter Ordner namens <em>.metadata</em> erstellt.

<h3>3.4 Ein Projekt anlegen</h3>

Nachdem Sie einen <em>Workspace</em> angelegt oder ausgewählt haben, können Sie auch Projekte anlegen. Projekte sind die nächstkleinere Organisationseinheit nach dem <em>Workspace</em>. Ein <em>Workspace</em> beinhaltet in der Regel mehrere Projekte. Um ein neues Projekt anzulegen, nutzen Sie die Tastenkombination <code>ALT</code> + <code>SHIFT</code> + <code>N</code> . Anhand dieses Shortcuts öffnet sich eine Liste, welche Sie durch das Drücken der <code>Pfeiltaste nach oben</code>- bzw. <code>Pfeiltaste nach unten</code> durchlaufen können. Wählen Sie mit Pfeiltaste nach unten <em>Java Project</em> aus. Benennen Sie Ihr Projekt und bestätigen Sie das Formular. Das Projekt ist nun durch Eclipse angelegt worden und im <em>Package Explorer</em> verfügbar, zu welchem Sie mit <code>ALT</code> + <code>SHIFT</code> + <code>Q</code> , <code>P</code> navigieren können. Der aktuelle Fokus des Programm-Cursors ändert sich beim Anlegen eines Projekts nur, sollte dieser im <em>Package Explorer</em> gelegen haben. In diesem Fall ändert er sich vom vorher ausgewählten Projekt zum neu erstellten. Anderenfalls bleibt der Fokus an der Stelle, an welcher er sich befand, bevor Sie ein neues Projekt angelegt haben.

<h3>3.5 Ein Paket erstellen</h3>

Ein Paket (englisch <em>package</em>) dient dazu bestimmte Programmbereiche zu gliedern. Hierzu wird in vielen Programmiersprachen mit dem Konzept der Namensräume (englisch <em>namespaces</em>) gearbeitet. Anhand von Namensräume wird die Verwendung von gleichen Bezeichnungen ermöglicht, ähnlich wie eine Verzeichnisstruktur es ermöglicht den selben Dateinamen in verschiedenen Verzeichnissen zu nutzen. Sie können zum Beispiel im selben Projekt zwei Mal die Klasse random.java anlegen. Sofern diese in zwei verschiedenen <em>Packages</em> liegen, können diese anhand ihres Pakets unterschieden werden.

Es wird empfohlen Dateien innerhalb Ihres Projekts mittels Paketen zu strukturieren. Wenn Sie kein <em>Package</em> anlegen, werden Ihre Dateien im <em>Default Package</em> angelegt. Um nun ein weiteres Paket anzulegen, führen Sie den Shortcut zum Anlegen einer neuen Ressource aus (<code>ALT</code> + <code>SHIFT</code> + <code>N</code>) und navigieren Sie mit der <code>Pfeiltaste nach unten</code> solange bis der Fokus auf <em>Package</em> liegt. Wenn Sie diese Auswahl bestätigen öffnet sich ein <em>Wizard</em>, der Sie nach dem gewünschten Namen des <em>Packages</em> fragt. Geben Sie den Namen ein und bestätigen Sie mit <code>ENTER</code>.

Im Paketmanager erscheint jetzt ein neuer Eintrag mit dem vergebenen Namen. Auf der Festplatte werden <em>Packages</em> als Verzeichnisse realisiert.

<h3>3.6 Eine Klasse erstellen</h3>

Nun haben Sie schon Ihr erstes Projekt angelegt und möchten sicherlich auch eine eigene Klasse erstellen.

Durch das Kommando <em>Neue Ressource anlegen</em>, also <code>ALT</code>+<code>SHIFT</code>+<code>N</code>, öffnet sich edie Ihnen bereits bekannte Liste, welche Sie mit den Pfeiltasten fokussieren können. Wählen Sie mit <code>Pfeiltaste nach unten</code> <em>Class</em> aus.

Es öffnet sich der <em>Wizard</em> der Sie durch die Erstellung einer Klasse führt. Pflicht ist die Vergabe eines Namens. Mittels der <code>TAB</code>-Taste können Sie durch die einzelnen Funktionen navigieren.

Die Klasse wird in dem <em>Project</em> und dem <em>Package</em> angelegt, das gerade selektiert ist. Im Formular haben Sie die Möglichkeit beides zu ändern. Sie können auch direkt beim Anlegen der Klasse das <em>Package</em> angeben, sollte dieses nicht mit dem aktuellen übereinstimmen. Geben Sie Ihrer Ressource einen Namen.

Wenn Sie eine Klasse anlegen möchten, die den Startpunkt für Ihre Anwendung darstellt, steht Ihnen im nächsten Schritt ein Kontrollkästchen zur Verfügung, welches, wenn es aktiviert ist, für die Generierung der sogenannten main-Methode sorgt. Aktivieren Sie hierfür das Kontrollfeld <em>public static void main (String[] args)</em>  mit der Tastenkombination für <em>Bestätigen</em> <code>ALT</code>+<code>V</code>. Bestätigen Sie das ausgefüllte Formular.

Sie können Ihre Klasse direkt beim Erstellen mit den dazugehörigen <em>Modifiers</em> ausstatten, indem Sie deren Kontrollfelder  unter der Option <em>Modifiers</em> aktivieren.

Wenn Sie eine andere Klasse erweitern wollen, können Sie die Superklasse über den Namen spezifizieren. Tun Sie dies, indem Sie Paket und Namen über die Punktnotation angeben. Ist die Superklasse beispielsweise die Klasse <em>Object</em>, so lautet der Name <em>java.lang.Object</em>, da es sich um die Klasse <em>Object</em> im Paket <em>java.lang.</em> handelt.

Sie können die Superklasse, das Interface und die vorzugenerierenden Methoden auch in diesem Formular über die <em>Browse</em>-Funktion auswählen.

Der Fokus liegt nach dem Anlegen im <em>Editor</em> auf Ihrer neu erstellten Klasse in Zeile 1.

Alternativ zu dem Shortcut <code>ALT</code>+<code>SHIFT</code>+<code>N</code> gelangen Sie auch mit der Tastenkombination <code>CTRL</code>+<code>N</code> in den <em>Wizard</em> zum Anlegen neuer Ressourcen. Wenn Sie sich bereits in einem Java-Projekt befinden, stehen Ihnen direkt nach dem Drücken des Shortcuts die Optionen zum Anlegen aller möglichen Java-Ressourcen zur Verfügung.

Diese Tastenkombination hat bei manchen Screenreadern den Vorteil, dass sie nicht von selbigem belegt wird.

<h3>3.7 Der Classpath</h3>

Wird eine Java-Klasse instanziiert, muss die Java Virtual Machine (JVM) wissen, wo die kompilierte Klasse, also die zugehörige <em>.class</em>-Datei, liegt. Im <em>Classpath</em> stehen die Pfade zu den obersten <em>Packages</em> eines Java-Programms und zu eingebundenen <em>.jar</em>-Dateien. Die kompilierten <em>.class</em>-Dateien eines Java-Projekts sind in einer Ordnerstruktur abgelegt, die der Paketstruktur des Projekts gleicht. In <em>.jar</em>-Dateien sind die <em>.class</em>-Dateien ebenfalls in dieser Ordnerstruktur abgelegt. Dadurch weiß die JVM jederzeit, wo der kompilierte Code zu einer bestimmten Klasse liegt und kann diesen nutzen.

<h3>3.8 Kompilieren und Fehlerbehebung</h3>

Dieser Abschnitt beschäftigt sich nicht mit <em>Debugging</em>. Stattdessen soll hier auf das Beheben von kleineren Kompilierfehlern eingegangen werden.

Markierungen in Form von roten Unterringelungen für <em>Errors</em> (Fehler) und gelben Unterringelungen für <em>Warnings</em>  (Warnungen) weisen sehende Menschen frühzeitig auf Kompilierfehler hin. Dies ist nur möglich, da Ihr Code fortlaufend durch Eclipse in Zwischencode für die JVM (Jave Virtual Machine) übersetzt wird.

Da diese Markierungen in erster Linie visuell sind, wird blinden oder sehbehinderten Programmierern empfohlen, regelmäßig, vorallem am Ende einer Programmierperiode, von dem Shortcut <code>CTRL</code>+<code>.</code> gebrauch zu machen, um zur nächsten Warnung oder zum nächsten Fehler zu springen. Der Fokus Ihres Screenreaders springt damit sofort zum nächsten Fehler oder zur nächsten Warnung in der aktuellen Java-Datei und liest Ihnen die unterringelte Stelle vor. Wenn JAWS die Fehlerzeile nicht sofort vorließt, so drücken Sie einmal <code>Pfeiltaste nach oben</code> und dann wieder <code>Pfeiltaste nach unten</code>. Allerdings ist es zu Empfehlen direkt nach dem Drücken von <code>CTRL</code> + <code>.</code> für JAWS-Nutzer <code>INSERT</code> + <code>PageDown</code> zu drücken, um die Fehlerhinweise auslesen zu können. Die Schnellhilfe wird nur mit dem Anspringen via <code>CTRL</code> + <code>.</code> vorgelesen und nicht mehr, wenn die Pfeiltasten zum Einsatz kommen.

Sollten Sie den Fehler hieraus noch nicht deduzieren können, gibt es die Möglichkeit eine Schnellhilfe von Eclipse zu erhalten. Hierzu drücken Sie die Tasten <code>CTRL</code>+<code>1</code> und im Anschluss <code>F2</code>. Die Tastenkombination <code>CTRL</code>+<code>1</code> öffnet das Schnellhilfe-Fenster. Mit <code>F2</code> wird der Fokus in diesem Fenster verlagert, so dass der Screenreader den Inhalt ausließt.

Sie sollten sich trotz dieser Möglichkeiten nicht allein auf die Intelligenz Ihrer IDE verlassen, denn auch Eclipse hat nicht immer recht!

<h3>3.9 Ein Programm ausführen</h3>

Nun ist es an der Zeit, Ihr Programm auszuführen. Wenn Sie Ihr Programm zum ersten Mal starten, müssen Sie Eclipse erst mitteilen, als welche Art von Java-Programm das Ihre gestartet werden soll.

Eclipse kennt grundsätzlich zwei gängige Varianten, um Java-Code auszuführen. Einmal das <em>Java-Applet</em>, welches im Browser läuft, und die <em>Java-Application</em>, ein eigenständiges Programm. Für dieses Tutorial ist nur die <em>Java-Application</em> relevant.

Um lästige Systemdialoge zu vermeiden, nutzen Sie den Hotkey <em>Run as Java Application</em>, <code>⇧</code>+<code>ALT</code>+<code>X</code>, dann <code>J</code>. Falls dieser Shortcut nicht wie beschrieben funktioniert, können Sie Ihr Programm auch mit dem Befehl <em>Run</em>, also <code>CTRL</code>+<code>F11</code>, starten. Wenn Sie Ihr Programm zum ersten Mal auf diese Weise starten, öffnet sich ein Systemdialog, welcher Sie fragt, als welche Art von Anwendung Ihr Programm ausgeführt werden soll. Wählen Sie <em>Java Application</em> aus und bestätigen Sie Ihre Eingabe. Ihr Programm wird beim Ausführen dieses Befehls, wie auch beim Speichern mittels <code>CTRL</code>+<code>S</code>, als Java-Datei in Ihrem <em>Workspace</em> gespeichert. Darauf weist Sie der zu bestätigende Systemdialog <em>Save and Launch</em> hin.

Um die <em>Main-Class</em>, welche den Startpunkt Ihres Programms darstellt, festzulegen, oder, um Parameter an Ihr Programm übergeben zu können, müssen Sie diese Einstellungen im Dialogfeld <em>Run Configurations</em> vornehmen. Dieses Dialog erreichen Sie indem Sie <code>ALT</code>+<code>R</code>, <code>N</code> drücken.

Um Ihrem Programm beispielsweise die Argumente <em>arg1</em>, <em>arg2</em> und <em>arg3</em> zu übergeben, drücken Sie nach der Tastenkombination <code>CTRL</code>+<code>R</code>, <code>N</code> solange <code>TAB</code>, bis Sie in die Registerleiste gekommen sind. Im Anschluss drücken Sie <code>CTRL</code>+<code>PageDown</code> um zum Reiter <em>Arguments</em> zu gelangen. Dort springen Sie mit <code>TAB</code> dann ins Eingabefeld <em>Program arguments</em>, wo Sie die gewünschten Argumente durch Leertasten getrennt eingeben können.

Achtung, um aus diesen Textfeld wieder rauszukommen müssen Sie <code>SHIFT</code>+<code>TAB</code> drücken. Im Anschluss drücken Sie <code>ENTER</code>. Diese Eingabe von "arg1 arg2 arg3" käme dem Starten Ihres Programms über die Kommandozeile, mittels "java [Name des Programms] Arg1 Arg2 Arg3", gleich.

<h3>3.10 Autovervollständigung mit Code Assist nutzen</h3>

Die meisten Menschen schätzen an Entwicklungsumgebungen die programmiersprachenbezogenen Unterstützungen, die die jeweilige Umgebung mitbringt. Was bei Microsoft Visual Studio <em>IntelliSense</em> heißt, ist bei Eclipse das Feature namens <em>Code Assist</em>.

<em>Code Assist</em> wird in einigen Situationen automatisch von der Eclipse IDE ausgelöst, beispielsweise bei der Eingabe eines Punktes (also<code>.</code>), nach Variablen oder Klassennamen. Wenn Sie <em>Code Assist</em> selbst auslösen möchten, nutzen Sie <code>CTRL</code>+<code>Leertaste</code>. Zur Veranschaulichung folgt hier ein kleines Beispiel aus dem <em>Hello World Tutorial</em>:

Schreiben Sie im Quellcode-<em>Editor</em> von Eclipse

<pre><code>syso
</code></pre>

dann <code>CTRL</code>+<code>Leertaste</code>. Wenn Sie diese Kombination zum ersten Mal ausführen, steht Ihnen bis zur Eclipse-Version Luna die Auswahl <em>Enable Smart Code Completion</em> zur Verfügung. Wählen Sie diese aus. Da wird Ihnen zukünftig die Eingabe des Strings

<pre><code>syso
</code></pre>

gefolgt von dem Shortcut zur Codevervollständigung  <code>CTRL</code>+<code>Leertaste</code>

sofort zu

<pre><code>System.out.println(); 
</code></pre>

komplettiert.

<em>Code Assist</em> bietet viele weitere Hilfestellungen.

Stellen Sie sich vor, Sie programmieren seit einigen Stunden und haben gerade eine längere Pause beendet. Eigentlich wollten Sie eine Fallunterscheidung aufstellen, nur von welcher Variable sollte sie abhängen? Statt Ihren Code erneut durchzugehen, drücken Sie einfach "<em>View</em>-Menü anzeigen", also <code>CTRL</code>+<code>Leertaste</code> und drücken Sie im Anschluss <code>F2</code>. Das sich nun öffnende <em>View</em>-Menü enthält alle möglichen Funktionalitäten, die Sie an dieser Stelle nutzen können, wie zum Beispiel lokale oder globale Variablen, Methoden der jeweiligen Klasse oder statische <em>Imports</em>. Damit diese Ihnen vorgelesen werden, müssen Sie mit <code>F2</code> den Fokus in diesem Fenster verlagern. Achtung, zwar wird das erste Element der Liste direkt fokussiert, aber von JAWS nicht sofort vorgelesen. Drücken Sie <code>Pfeiltaste nach unten</code> und dann wieder <code>Pfeiltaste nach oben</code>, um auch das erste Elemente der Liste vorgelesen zu bekommen.

Wenn Sie ein Java-Objekt benutzen möchten, geben Sie mindestens den Anfangsbuchstaben als Großbuchstaben an. Drücken Sie nun den Hotkey für <em>Code Assist</em>, also <code>CTRL</code>+<code>Leertaste</code>. Eclipse öffnet eine Liste von Vorschlägen für Sie, die direkt fokussiert wird. Durch die Liste kann wie gewohnt mit den Pfeiltasten navigiert werden. Für das aktuell fokussierte Objekt wird direkt das zugehörige <em>JavaDoc</em> geöffnet. Durch das Drücken der Taste <code>TAB</code> springen Sie ins den <em>JavaDoc</em>-Bereich und durch das Drücken von <code>ESC</code> springen Sie wieder in die Auswahlliste. Mit <code>ENTER</code> wählen Sie eine Auswahl aus. Das Ergebnis wird direkt im Quellcode platziert.

<em>Code Assist</em> auch sehr gut für Neugierige geeignet, die einfach nur mehr über ein Objekt, das sie verwenden, wissen möchten. Dies bedeutet einfach, dass alle Informationen in der <em>Online-Java-API</em>, die aus <em>JavaDoc-Kommentaren</em> generiert werden, für Sie verfügbar sind, ohne das Programm zu wechseln.

Sie sollten nun eine gute Vorstellung davon haben, was man mit <em>Code Assist</em> alles machen kann. Probieren Sie es aus!

<h2>4. Tips und Tricks</h2>

Eclipse bietet ihnen viele kleine Features, die dafür gemacht wurden, Ihren Programmieralltag zu vereinfachen. Die meisten sind trivial, werden aber häufig genutzt und sorgen für eine enorme Produktivitätssteigerung.

<h3>4.1 Gedächtnisstütze für Keyboard-Shortcuts</h3>

In Eclipse müssen Sie sich wirklich nur an eine Tastenkombination erinnern, nämlich  <code>CTRL</code>+<code>SHIFT</code>+<code>L</code>. Diese zeigt Ihnen eine alphabetisch sortierte Liste aller Tastaturbefehle in der Eclipse IDE an, welche auch sofort fokussiert ist.

<h3>4.2 Code Assist</h3>

Dieses Tutorial enthält einen ganzen Abschnitt über die <em>Code Assist</em>-Funktion. Diesen finden Sie im Kapitel 3.9 Autovervollständigung mit <em>Code Assist</em> nutzen.

<h4>4.2.1 Vorschläge zur Fehlerbehandlung</h4>

Diese Funktion wird im Abschnitt 3.7 Kompilieren und Fehlerbehebung kurz angeschnitten. Eclipse bietet Ihnen eine Funktion, die Ihnen Lösungsmöglichkeiten aufzeigt, um Kompilierfehler und Warnungen zu beheben. Sollte irgendeine Art von Fehler oder Warnung auftreten, springen Sie in die entsprechende Zeile und drücken Sie <code>CTRL</code>+<code>1</code> und im Anschluss <code>F2</code>, um den Fokus in das Schnellhilfe-Fenster zu verlagern. Eine Liste der möglichen Optionen erscheint. Sie enthält nicht immer die besten Lösungsvorschläge, aber oftmals funktionieren sie gut. Dies gilt vor allem bei Fehlern wie vergessenen <em>Imports</em>. Dennoch sollten Sie die Vorschläge gut prüfen, bevor Sie diese anwenden.

<h4>4.2.2 Definitionen einsehen</h4>

Im Folgenden werden Shortcuts behandelt, welche dienlich sind, falls Sie Code nutzen, den Sie nicht selbst geschrieben haben. Wenn Sie nämlich direkt zu der Definition einer Methode, Klasse, eines Interfaces oder Ähnlichem springen möchten, nutzen Sie einfach die Taste <code>F3</code>.

Um diese Funktion nutzen zu können, müssen Sie allerdings Zugang zu den Quelldateien, also <em>.java</em>-Files, haben. Mit vorkompilierten Bibliotheken können Sie diese Funktion nicht verwenden.

<h4>4.2.3 Alle Attribute und Methoden im aktuellen Editorfenster anzeigen</h4>

Eclipse tut wirklich alles, damit Sie sich nicht auf Ihr Gedächtnis verlassen müssen. Sollten Sie sich nicht mehr genau erinnern, wie die Attribute oder Methoden der Klasse heißen, die Sie aktuell bearbeiten, drücken Sie einfach <code>CTRL</code>+<code>O</code>. Diese Funktion ist aber nicht nur eine Gedächtnisstütze, sondern auch eine perfekte Navigationshilfe. Wählen Sie einfach mit Hilfe der Pfeiltasten das gesuchte Element aus und drücken Sie <code>ENTER</code>. Damit springen Sie im <em>Editor</em> direkt hinter den Namen in der Variablen- oder Methoden-Deklaration.

<h4>4.2.4 Perfekte Code-Formatierung</h4>

Sie können Ihren Quellcode mit Eclipse auf zwei Arten auto-formatieren.

<ol>
<li>Markieren Sie den gewünschten Abschnitt mit <code>SHIFT</code>+<code>Pfeiltaste nach links</code>/<code>Pfeiltaste nach links</code> und nutzen Sie anschließend <code>CTRL</code>+I`. Der markierte Bereich wird perfekt eingerückt.</li>
</ol>

Um das vorherige Auswählen zu umgehen, nutzen Sie die zweite Option.

<ol>
<li>Der komplette Code der aktuellen .java-Datei wird mittels <code>CTRL</code>+<code>SHIFT</code>+<code>F</code> nach der Java-Standardspezifikation formatiert. Diese Variante beinhaltet auch Abstände und Zeilenumbrüche.</li>
</ol>

<h4>4.2.5 Clean Up</h4>

Diese Funktion von Eclipse soll nur am Rande erwähnt werden. Wenn Sie in der Menüleiste Source auswählen und hier <em>Clean Up</em>, beginnt Eclipse, Ihren Code auf Redundanzen zu untersuchen, um im Anschluss ungenutzte oder bedeutungslose Codefragmente zu eliminieren. Dieses Feature ist dazu entworfen, Ihren Code eleganter zu machen. Wenn Sie diese Funktion auf den von Ihnen geschriebenen Code anwenden, ist es erstrebenswert, dass dieser unverändert bleibt. Falls Sie die Grundprinzipien der Java-Programmierung beherrschen, liegt dies sicher im Bereich Ihrer Fähigkeiten.

<h4>4.2.6 To-Dos verfolgen</h4>

Während des Schreibens von Programmen kommen Ihnen sicherlich immer wieder Dinge in den Kopf, die Sie zu einem späteren Zeitpunkt noch umsetzen möchten. In der Industrie herrscht der Standard, dass solche unerledigten Dinge mittels

<pre><code>// TODO: Aufgabenbeschreibung
</code></pre>

gekennzeichnet werden. Eclipse macht Ihnen Ihren Programmieralltag an dieser Stelle leichter, indem es Ihren Quellcode nach solchen Kommentaren durchsucht und diese in einem eigenen Fenster namens <em>Tasks</em> bündelt. Dieses erreichen Sie in erster Instanz nur über die Menüleiste, via <em>Window</em> bei <em>Show View</em> finden Sie <em>Task</em>. Wenn Sie das Fenster einmal geöffnet haben, können Sie es über den Shortcut, der zwischen den Ansichten wechselt, also <code>CTRL</code>+<code>F7</code>, ansteuern. Mit den Pfeiltasten kommen Sie zur gewünschten Ansicht. Die <em>Tasks</em>-Ansicht erscheint unter dem <em>Editor</em>-Fenster als einer der Reiter auf der Höhe der <em>Console</em>, wo auch das <em>Problems</em>-Fenster angesiedelt ist. Die einzelnen <em>Tasks</em> können mit den Pfeiltasten ausgewählt werden. Drücken Sie <code>ENTER</code>, springt Ihr Cursor direkt in die Zeile des jeweiligen <em>Tasks</em>.

Die <em>Tasks-View</em> wird erst nach dem Kompilieren des Programms aktualisiert und die <em>Tasks</em> erschienen in der Liste.

Alle <em>Tasks</em> werden projektübergreifend, das heißt für alle in Ihrem <em>Workspace</em> geöffneten Projekte angezeigt.

Achtung, verwechseln Sie die <em>Tasks</em> nicht mit der <em>TaskList</em>!

<h2>5. Fortgeschrittene Themen</h2>

<h3>5.1 Ein neues Interface erstellen</h3>

Sollten Sie den Abschnitt 3.5 Eine Klasse erstellen bereits gelesen haben, wird Ihnen das hier beschriebene Vorgehen bekannt erscheinen. Drücken Sie nun die Tastenkombination, um eine neue Ressource anzulegen <code>ALT</code>+<code>SHIFT</code>+<code>N</code>. Oder nutzen Sie die Tastenkombination, um eine neue Ressource über das Wizard anzulegen, also <code>CTRL</code>+<code>N</code>.

Wählen Sie <em>Interface</em> aus und spezifizieren Sie das <em>Package</em>, falls notwendig. Benennen Sie die neue Ressource. Alle <em>Interfaces</em>, die durch das, was Sie neu anlegen, erweitert werden sollen, können Sie durch Bestätigen das <em>Add</em>-Schalters im Formular hinzufügen.

Nach Bestätigen des ausgefüllten Formulars wird Ihr neues <em>Interface</em> angelegt.

<h3>5.2 Arbeiten mit Packages</h3>

Ein <em>Package</em>, zu deutsch Paket, ist mehr oder weniger das Äquivalent zu <em>Namespaces</em> in Sprachen wie Javascript oder C++. Durch das Strukturieren von Klassen in Paketen können Sie sicherstellen, dass keine Namenskonflikte entstehen. In vielen Javaprojekten kommen beispielsweise zwei verschiedene Date-Klassen zum Einsatz, nämlich java.util.Date und java.sql.Date. Jede der beiden Klassen befindet sich innerhalb eines Pakets, einmal des Pakets java.util und einmal des Paket java.sql, so dass keine Konflikte zwischen den beiden Klassen entstehen.

Wäre keine der beiden Klassen innerhalb eines Pakets angesiedelt, würden die Bibliotheken nicht kompilieren. Der Compiler würde eine der beiden Klassen als eine Re-Definition der anderen Klasse ansehen. Dies würde zu Verwirrung führen.

Pakete erlauben auch eine logische organisatorische Abstraktion für verwandte Gruppen von Java-Klassen und Interfaces. Um ein Paket für Ihre Klasse oder Schnittstelle anzugeben, muss die erste Zeile Ihrer Java-Datei wie folgt lauten:

<pre><code>package [package.name];
</code></pre>

Dieses Tutorial wird hier nicht weiter auf Pakete als Sprachmerkmale eingehen. Es gibt viele Ressourcen, online und anderswo, die Ihnen helfen können, diesen Aspekt der Programmiersprache Java zu verstehen. Sollten Sie absoluter Neuling auf diesem Gebiet sein, kann eine Lösung sein, Ihre Lieblings-Suchmaschine einmal mit dieser Frage zu bemühen. Sollten Sie gezielt mit Paketen arbeiten, wird empfohlen, sich vorher mit den Einschränkungen, die dieses Sprachmerkmal mit sich bringt, vertraut zu machen.

Vielmehr sollen die paketbezogenen Funktionalitäten von Eclipse besprochen werden. Die erste ist der <em>Package Explorer</em>. Der <em>Package Explorer</em> präsentiert Ihnen Ihre Projekte mit dem Fokus auf deren Java-Paketstruktur. Sollten Sie Eclipse schon einmal genutzt haben, ist Ihnen vielleicht aufgefallen, dass neu angelegte Klassen in Eclipse nicht einfach irgendwo, sondern im sogenannten <em>default package</em> auftauchen, welches einen Knotenpunkt in der Hierarchie des <em>Package Explorers</em> darstellt. Geben Sie nämlich kein Paket für Ihre neue Java-Klasse an, wird es mit allen anderen nicht verpackten Klassen in diesem Standardpaket gruppiert.

<h4>5.2.1 In den Package Explorer springen</h4>

Um in den <em>Package Explorer</em> zu springen, dient Ihnen der Shortcut <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>, <code>P</code>.

Um ein neues Paket anzulegen, gehen Sie wie folgt vor: Drücken Sie nun die Tastenkombination für <em>neue Ressource anlegen</em>, <code>ALT</code>+<code>SHIFT</code>+<code>N</code>. Es öffnet sich eine Liste, welche Sie durch das Anschlagen der Pfeiltasten fokussieren können. Wählen Sie mit <code>Pfeiltaste nach unten</code> das Wort <em>Package</em> aus.

Ihr Paket existiert erst dann wirklich, wenn es mit Inhalten, also Ressourcen im Sinne von Klassen oder <em>Interfaces</em>, gefüllt wurde. Logischer ist es allerdings, das Paket beim Anlegen einer Klasse zu definieren, wodurch es direkt mit angelegt wird (siehe Kapitel 3.6 Eine Klasse erstellen).

<h3>5.3 Dateien importieren</h3>

Angenommen, Sie haben Ihr Projekt in Eclipse angelegt, aber wollen die einzelnen Komponenten nicht von Grund auf neu in Eclipse erstellen, sondern einige vorgefertigte Dateien, beispielsweise aus Ihrem lokalen Dateisystem, nutzen. Hierfür gibt es drei Wege für Sehbehinderte, welche Sie nachfolgend aufgelistet finden.

<ol>
<li>Der Weg über die Menüleiste

Springen Sie in die Menüleiste der Eclipse IDE zu <em>File</em> und wählen Sie <em>Import</em> aus der Liste aus. Nun öffnet sich das <em>Import</em>-Fenster. Der Fokus liegt auf einem Textfeld mit dem Text "<em>type filter text</em>". Dieses dient der Eingabe des Suchtextes zur Filterung der möglichen zu importierenden Typen von Quellen. Tippen Sie <em>File</em> ein, um die Ergebnisliste zu minimieren. Drücken Sie <code>Pfeiltaste nach unten</code>, um in die Auswahlliste zu springen und wählen Sie <em>File System</em>. Bestätigen Sie Ihre Auswahl. Es öffnet sich nun ein Fenster, in welchem Sie, unter <em>From directory</em>, die gewünschte Datei auswählen und zu Ihrem Eclipse-Projekt hinzufügen können. Statt einer Datei können Sie auch ein ganzes Verzeichnis auswählen. Sobald Sie einen Ordner ausgewählt haben, haben Sie die Wahl, ganze Verzeichnisse oder nur deren Unterkomponenten zu importieren. Es öffnet sich eine Tabelle mit den Inhalten des selektierten Ordners. Um ganze Ordner zu importieren, aktivieren Sie dessen Markierungsfeld. Möchten Sie an dieser Stelle bestimmte Dateien anstelle von ganzen Verzeichnissen auswählen, wählen Sie statt der übergeordneten Komponente dessen gewünschten Inhalt. Jede dieser Dateien kann einzeln ausgewählt werden, genau wie vorher die Verzeichnisse. Des Weiteren haben Sie in diesem Fenster die Möglichkeit unter <em>Into folder:</em> das jeweilige <em>Project</em>, sowie das <em>Package</em> oder, anders formuliert, das Verzeichnis zu spezifizieren, in welches die Datei importiert werden soll. Stellen Sie sicher, dass Sie in den richtigen Ordner importieren und dass die Optionen so eingestellt sind, wie Sie sie wünschen, und bestätigen Sie mit der <em>Finish</em>-Taste.

</li>
<li>

Der Weg über das Kontextmenü im <em>Package Explorer</em>

Springen Sie zuerst mit <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>, <code>P</code> in den <em>Package Explorer</em>. Wählen Sie das richtige Projekt und drücken Sie dann die Kontextmenü-Taste. Sie können das Projekt auch später, wie bereits vorher erwähnt, im <em>Import</em>-Dialog noch ändern. Wählen Sie aus der sich öffnenden Liste <em>Import</em>. Das <em>Import</em>-Fenster wird geöffnet. Ihnen stehen die selben Eingabemöglichkeiten wie auch bei der Auswahl über die Menüleiste zur Verfügung. Gehen Sie ab jetzt genau wie auch dort beschrieben vor.

</li>
<li>

Copy und Paste aus dem Dateisystem

Kopieren Sie die gewünschte Datei in Ihrem Dateisystem, ganz einfach mit <code>CTRL</code>+<code>C</code> oder über das Kontextmenü. Gehen Sie in die Eclipse IDE und wählen Sie das Projekt sowie das Paket aus, in welches Sie diese Datei importieren wollen und drücken Sie Einfügen, also <code>CTRL</code>+<code>V</code>. Die Datei wird nun in das Projekt importiert.

</li>
</ol>

<h3>5.4 Archive importieren</h3>

Das Importieren eines Archivs ist dem Importieren einer Datei sehr ähnlich. Öffnen Sie das Kontextmenü Ihres Projekts im Paket-Explorer und klicken Sie auf <em>Import</em>. Dieses Mal verwenden Sie <em>Archive File</em> als Ihren Filtertext und wählen die Option <em>Archive File</em>. Bestätigen Sie Ihre Auswahl.

Gehen Sie so vor wie auch beim Importieren von Dateien, aber dieses Mal, anstatt ein Verzeichnis auszuwählen, wählen Sie die benötigte Archivdatei. Dies wird dazu führen, dass Sie das Dateisystem im Archiv so gut wie möglich durchsuchen können, wenn Sie ein Verzeichnis importieren. Wählen Sie Unterordner zum Importieren oder wählen Sie einfach Dateien aus. Nachdem Sie alle Optionen ausgewählt haben, bestätigen Sie mit <em>Finish</em>. Ihr Archiv wird nun entpackt und in das Projekt importiert.

Wenn Sie Ihr Archiv stattdessen per Copy und Paste aus dem Dateisystem importieren möchten, wird dieses, falls es nicht bereits entpackt ist, als komprimierter Ordner zum Projekt hinzugefügt. Öffnen Sie diesen Ordner im <em>Editor</em>. Da das <em>Editor</em>-Fenster nun fokussiert ist, können Sie direkt mit <code>SHIFT</code>+<code>TAB</code> in die Funktionsleiste des <em>Editors</em> navigieren. Diese befindet sich im Falle eines geöffneten Archivs direkt über dem eigentlichen <em>Editor</em>-Bereich. Dort steht Ihnen neben einigen anderen auch die Funktion <em>Extract files from the archive</em> zur Verfügung. Wählen Sie diese aus. Dadurch öffnet sich das <em>Select Target to extract to</em>-Fenster, in welchem Sie den Ort angeben können, an welchem das Archiv entpackt werden soll.

<h3>5.5 Code-Refactoring</h3>

<em>Refactoring</em> bezieht sich auf die Umformung von Code, um seinen Stil, sein Design, oder dergleichen zu verbessern. Das Ergebnis der Ausführung des Codes im Bezug auf den Benutzer ändert sich hierbei nicht. In der Strukturierung, unbemerkt durch den Anwender oder die Anwenderin, fallen die Änderungen jedoch ins Gewicht.

Schon das Umbenennen von Klassen oder Methoden würde in größeren Projekten einen riesigen Aufwand bedeuten. Stellen Sie sich vor, Sie müssten jedesmal einen regulären Ausdruck schreiben, der das für Sie tut, oder gar alles manuell ändern. Natürlich lässt Eclipse Sie hier nicht alleine. Die IDE bietet Ihnen einen einfachen Weg, Ihren kompletten Code mit allen Referenzen auf die umzuformende Code-Passage zu aktualisieren.

Der Hotkey für das <em>Refactoring</em> an sich ist <code>ALT</code>+<code>T</code>,wodurch eine Ansicht geöffnet wird, unter welcher Sie die Art des <em>Refactoring</em> wählen können. Die simpelste Umformung ist die <em>Rename</em>-Funktion, welche Sie auch über den Shortcut <code>ALT</code>+<code>SHIFT</code>+<code>R</code> erreichen. Die sich öffnende Ansicht beinhaltet außer dem Textfelde für den neuen Namen des umzubenennenden Elementes das Markierungsfeld <em>Update References</em>. Stellen Sie sicher, dass dieses ausgewählt ist und bestätigen Sie Ihre Eingabe. Ihre Methode oder Klasse ist nun für alle im <em>Package Explorer</em> geöffneten Projekte umbenannt.

<h3>5.6 Plugins installieren</h3>

<h4>5.6.1 Eclipse Marketplace</h4>

Sie können <em>Plugins</em> in Eclipse auf unterschiedliche Weise installieren. Es gibt den <em>Eclipse Marketplace</em>, welcher eine Art <em>Appstore</em> für Eclipse-<em>Plugins</em> ist. Um ein <em>Plugin</em> hierüber installieren zu können, muss es im <em>Marketplace</em> gehostet werden.

<h4>5.6.2 Update Manager</h4>

Sollte das gesuchte <em>Plugin</em> lokal zur Verfügung stehen und nicht im <em>Eclipse Marketplace</em> vorhanden sein, können Sie den <em>Update Manager</em> nutzen. Die <em>Eclipse Foundation</em> empfiehlt eine Installation über den Update-Manager, welchen Sie im Menü unter <em>Help</em> bei <em>Install New Software...</em> finden. Nach Auslösen des Schalters <em>Add</em> können Sie entweder eine URL eingeben, oder durch auslösen der Schaltfläche <em>Local</em> ein <em>Plugin</em> aus Ihrem Dateisystem wählen. Diese Option prüft zum Beispiel, ob Kompatibilitätsprobleme zu Ihrer Eclipse-Version oder Abhängigkeiten zu anderen <em>Plugins</em> bestehen.

<h4>5.6.3 Manuelle Installation</h4>

Ein Plugin in Eclipse manuell zu installieren bedeutet ganz einfach, das <em>Plugin</em> in den sich im Installationsordner von Eclipse befindenden Ordner namens <em>Plugins</em> zu legen. Starten Sie danach die IDE neu.

<h2>6. Suche und Navigation</h2>

<h3>6.1 Suchen/Ersetzen-Funktionalität im Editor</h3>

Mit Hilfe des Shortcuts <code>CTRL</code>+<code>F</code> öffnen Sie das <em>Suchen und Ersetzen</em>-Fenster. Geben Sie den gesuchten Wert ein und gegebenenfalls den, mit welchem dieser ersetzt werden soll, und bestätigen Sie Ihre Eingaben mit dem gewünschten Schalter. Ihnen stehen hierfür in erster Instanz <em>Find</em> und <em>Replace All</em> zur verfügung.

Wurde bereits <em>Find</em> angewendet, haben Sie die zusätzlichen Optionen <em>Replace/Find</em>, die einen Wert nach dem anderen ersetzt, sowie <em>Replace</em>, welches nur einen einzelnen Wert mit dem zu ersetzenden auswechselt.

<h3>6.2 Die Zurück-Funktion</h3>

In jedem <em>Wizard</em>-Formular, welches Sie in Eclipse ausfüllen, befindet sich ein Zurück-Schalter. Falls Sie also versehentlich die falsche Art von Java-Datei, z.B. <em>Class</em> statt <em>Interface</em>, gewählt haben, können Sie über diesen Schalter im Formular zurücknavigieren und Ihre Eingabe korrigieren.

<h3>6.3 Navigation im Editor</h3>

Der <em>Editor</em> ist das Fenster, in welchem Sie Ihren Quellcode schreiben. Dieser ähnelt den gängigen Text-Editoren, die Sie auch für das reine Editieren von Fließtexten kennen. Der <em>Editor</em>, welcher in Eclipse integriert ist, bietet zusätzlich noch einige visuelle Hilfen zum Erstellen von Software, auf welche in diesem Tutorial bewusst nicht eingegangen wird.

Die nächsten Unterüberschriften beschäftigen sich mit den Möglichkeiten, den <em>Editor</em> als blinder Programmierer effizient zu nutzen.

<h4>6.3.1 Von überall in den Editor springen</h4>

Der Fokus des Cursors wechselt, je nachdem in welchem Bereich der Eclipse IDE Sie sich gerade befinden. Es ist ineffizient, die einzelnen Bereiche der Eclipse IDE der Reihenfolge nach anzusteuern, um in den gewünschten Bereich zu gelangen.

Wie Sie bereits im Laufe dieses Tutorials erfahren konnten, bietet Eclipse die Möglichkeit, mittels Shortcuts oder Hotkeys direkt in bestimmte Bereiche zu springen.

Um von einer beliebigen Stelle in der Eclipse IDE in den <em>Editor</em> zu springen, nutzen Sie die Taste <code>F12</code>. In Einzelfällen funktioniert diese Schnellnavigation nicht, dann muss man explizit in die <em>Editor</em>-Ansicht navigieren.

<h4>6.3.2 Zwischen den offenen Editor-Fenstern navigieren</h4>

Während der Entwicklung eines Programmes öffnen wir für gewöhnlich viele <em>Editor</em>-Fenster. Jedesmal, wenn wir eine Klasse aus dem <em>Package Explorer</em> auswählen, öffnet Eclipse diese automatisch in einem neuen Fenster. Somit können all diese geöffneten <em>Editor</em>-Fenster bis sie aktiv geschlossen werden, auch erreicht werden. Die Eclipse IDE bietet Ihnen im Großen und Ganzen drei Möglichkeiten, um komfortabel zwischen den offenen <em>Editor</em>-Fenstern zu navigieren.

Wenn Sie einen bestimmten Pfad beschreiten wollen, ist es hilfreich, wenn Sie sich erst einmal die Möglichkeiten anzeigen lassen, wo Sie hingehen können. So verhält es sich auch im Fall von mehreren geöffneten <em>Editor</em>-Fenstern.

Der Shortcut, um offene Editoren anzeigen zu lassen, ist in der Standardeinstellung <code>CTRL</code>+<code>E</code> belegt.

Wenn Sie stattdessen die Tastenkombination <code>CTRL</code>+<code>F6</code> oder <code>CTRL</code>+<code>SHIFT</code>+<code>F6</code> nutzen, zeigt dies auch offene Editoren an, wobei der Wechsel zwischen den Fenstern sofort nach loslassen der <code>CTRL</code>-Taste erfolgt.

<h4>6.3.3 Zu einer bestimmten Zeile im Editor springen</h4>

Um in eine bestimmte Zeile im <em>Editor</em>-Fenster zu springen, muss dieses fokussiert sein. Nutzen Sie den Shortcut <code>CTRL</code>+<code>L</code>, der das Fenster <em>go to line</em>  öffnet, geben Sie die gewünschte Zeilennummer ein und bestätigen Sie Ihre Eingabe.

<h3>6.4 Navigation in der Console</h3>

<h4>6.4.1 Aufbau der <em>Console</em>-Ansicht</h4>

Die drei Konsolen, die standardmäßig in Eclipse zur Verfügung stehen, sind die <em>Process Console</em>, die <em>Stacktrace Console</em> und die <em>CVS Console</em>.

Die in der <em>Console</em> verfügbaren Befehle werden im Folgenden behandelt und können mit aktiviertem JAWS-Cursor angesteuert werden. Sie sind durch beschriftete <em>Icons</em> abgebildet. Diese befinden sich rechts auf der Höhe des <em>Console</em>-Reiters. Sollte die Breite Ihres Bildschirms nicht ausreichen, um die <em>Icons</em> neben den Reitern darzustellen, verschieben sich diese leicht nach unten.

Es handelt sich um <em>Clear Console</em>, <em>Display Selected Console</em>, <em>Open Console</em>, <em>Pin</em> und <em>Scroll Lock</em>. In diesem Tutorial soll nur <em>Open Console</em> näher besprochen werden.

Sollten Sie Ihre <em>Console</em> aus irgendeinem Grund einmal geschlossen haben, können Sie diese mittels des Shortcuts um in die Konsole zu springen, <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>,<code>C</code>, erneut öffnen. Egal ob eine <em>Console</em> geöffnet ist oder nicht, mit diesem Shortcut springen Sie direkt hinein.

<h4>6.4.2 Weitere Console-Fenster öffnen</h4>

In manchen Fällen kann es nötig sein, eine zweite <em>Console</em> zu öffnen. Hier kommt der  JAWS-Cursor ins Spiel.
Springen Sie zuerst in die <em>Console</em>, um schon in der Nähe des Bereichs zu sein.
Aktivieren Sie den JAWS-Cursor, in dem Sie <code>Insert</code>+<code>-</code> auf dem Nummernpad drücken. Sie hören nun "ziehe JAWS zu PC". Nun können Sie mit den Pfeiltasten den Cursor bedienen.

Nutzen Sie jetzt die Pfeiltasten, um etwas nach oben und rechts zu navigieren. Leider sind die einzelnen <em>Icons</em> in der Leiste der <em>Console</em> standardmäßig nicht beschriftet. Bleiben Sie an dieser Stelle probierfreudig. Mit der Taste <code>/</code> können Sie einen Linksklick auf ein Element ausführen. Wenn Ihnen JAWS das Wort "Kontextmenü" mitteilt, befinden Sie sich in dem Drop-Down, in welchem Sie eine neue <em>Console</em> öffnen können. Navigieren Sie mit den Pfeiltasten zu <em>New Console View</em> und drücken Sie <code>ENTER</code>. Sie haben nun eine zweite <em>Console</em> geöffnet.

Drücken Sie <code>F12</code>, um wieder zurück in den <em>Editor</em> zu springen.

<h4>6.4.3 Exceptions in der Console</h4>

Beim Ausführen eines Programmes werden oft, je nach Parameter, Fehler oder Ausnahmen provoziert. Gerade in den Randfällen kann es schnell einmal zu einer <em>NullPointerException</em> kommen, wenn Sie als Programmierer diesen Fall im Vorfeld nicht bedenken. Auch hier bietet Eclipse Ihnen eine Hilfestellung, um schnell an die Stelle, an welcher die <em>Exception</em> geworfen wird, zu gelangen.

Sollte Ihr Programm eine <em>Exception</em> ausgelöst haben, stellt Eclipse diese Ausgabe in der <em>Console</em> mit einem Link dar.

Sollte beispielsweise eine <em>IndexOutOfBoundsException</em> geworfen werden, würde Ihr Screenreader in etwa verlauten lassen:

<pre><code>Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
at hello.world.Main.foo(Main.java:23)
at hello.world.Main.main(Main.java:18)
</code></pre>

Diese Ausgabe möchte ich Ihnen nun Zeile für Zeile erläutern.

In Zeile 1:

<pre><code>Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
</code></pre>

teilt Ihnen Eclipse mit, dass im Haupt-Thread Ihrer Anwendung, im Thread <em>main</em>, eine <em>ArrayIndexOutOfBoundsException</em> an der Stelle 2 geworfen wurde.

In Zeile 2:

<pre><code>at hello.world.Main.foo(Main.java:23)
</code></pre>

informiert Sie Ihre IDE, dass diese Exception in der Klasse mit dem Namen Main, des Paketes namens hello.world, in der mit foo benannten Methode, in Zeile 23 geworfen wurde. Der letzte Teil, nämlich

<pre><code>(Main.java:23)
</code></pre>

ist der Link in Zeile 23.

Zeile 3:

<pre><code>    at hello.world.Main.main(Main.java:18)
</code></pre>

erläutert, dass die Ausnahme in der Zeile 18, der Klasse mit dem Namen Main, welche sich in einem Paket namens hello.world befindet, in der mit main benannten Methode, in Zeile 18 ausgelöst wurde.

Der hintere Teil ist wiederum der Link zur Zeile, also

<pre><code>(Main.java:23)
</code></pre>

Mit diesem Wissen stehen Ihnen folgende Möglichkeiten zur Verfügung, um an die angegebenen Stellen zu gelangen.

<ol>
<li>Nutzung des Shortcut <em>go to line</em>

Verwenden Sie den Shortcut <em>go to line</em>, also <code>CTRL</code>+<code>L</code> und geben Sie die Zeilennummer ein, in welcher die <em>Exception</em> entstand oder ausgelöst wurde. Sie springen nun direkt zurück in den <em>Editor</em> in die angegebene Zeile. Der Fokus liegt am Anfang der Zeile.

</li>
<li>

Nutzung des JAWS-Cursor

Aktivieren Sie den JAWS-Cursor, navigieren Sie mit den Pfeiltasten an die verlinkte Stelle und lösen Sie einen Linksklick aus. Sie springen nun direkt zurück in den <em>Editor</em> in die angegebene Zeile. Der Fokus liegt im Gegensatz zur Möglichkeit 1 am Ende des Ausdrucks, der die Ausnahme auslöste.

</li>
</ol>

<h3>6.5 Navigation in der Problems-View</h3>

Ein Weg zu <em>Problems</em> ist der Shortcut zum Öffnen der Listenansicht aller <em>Views</em>, also <code>CTRL</code>+<code>SHIFT</code>+<code>F7</code>. Wählen Sie in der Ansicht mit den Pfeiltasten <em>Problems</em> aus.

Alternativ steht Ihnen der Shortcut, um in <em>Problems</em> zu springen, nämlich <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>,<code>X</code> zur Verfügung.

<h4>6.5.1 Wie ist die Problems-View aufgebaut?</h4>

Die Ansicht der <em>Problems</em> ist eine schlichte Baumansicht mit allen Fehlern und allen Warnungen aus allen geöffneten Projekten. Die Probleme sind nach Typ strukturiert. Hieraus resultiert ein Baum pro Typ, also je nach Vorkommnis in all den in der IDE geöffneten Projekten maximal zwei Bäume. Hierfür ist einer für <em>Warnings</em> und der andere für <em>Error</em> reserviert.

Die Navigation in dieser Ansicht gestaltet sich intuitiv. Mit der Taste <code>Pfeiltaste nach rechts</code> klappen Sie die jeweilige Baumansicht auf. Mit <code>Pfeiltaste nach oben</code> oder <code>Pfeiltaste nach unten</code> navigieren Sie durch die Warnungen beziehungsweise durch die Fehler. Mit <code>ENTER</code> gelangen Sie direkt in die Zeile, hinter das Auftreten des jeweiligen Fehlers beziehungsweise der jeweiligen Warnung.

<h2>7. Erstellen einer Hello-World-Applikation</h2>

<h3>7.1 Anlegen von Java-Dateien</h3>

Erstellen Sie ein neues Projekt  und geben Sie dieser den Namen eclipseTutorial, für eine Hilfestellung siehe Kapitel 3.4 Ein Projekt anlegen. Legen Sie im neu angelegten Projekt eine neue Java-Klasse an und geben Sie ihr den Namen <em>Main</em>, wie im Kapitel 3.6 Eine Klasse erstellen* beschrieben. Sorgen Sie dafür, dass die Klasse, die Ihnen erstellt wird, bereits eine <em>main</em>-Methode enthält. In Ihrem <em>Workspace</em> wurde nun eine Datei mit dem Namen <em>Main.java</em> erstellt.

<h3>7.2 Zeilenweise navigieren</h3>

Navigieren Sie nun zu Zeile 6. Dafür haben Sie zwei Möglichkeiten. Entweder Sie nutzen die Pfeiltasten oder Sie wählen den Shortcut <em>go to line</em>, <code>CTRL</code>+<code>L</code> und geben in dem sich nun öffnenden Formular die Zeilennummer 6 an.

In Zeile 6 befindet sich ein Kommentar, der automatisch beim Anlegen der Java-Datei mit der <em>main</em>-Methode generiert wurde. Der Kommentar lautet

<pre><code>//TODO Auto-generated method stub
</code></pre>

<h3>7.3 Codevervollständigung</h3>

Ersetzen Sie den Kommentar durch einen <em>print</em>-Befehl. Markieren Sie hierfür den Kommentar und tippen Sie

<pre><code>syso
</code></pre>

dann <code>CTRL</code>+<code>Leertaste</code>. Wenn Sie diese Kombination zum ersten Mal ausführen, steht Ihnen bis zur Version Luna von Eclipse die Auswahl <em>Enable Smart Code Completion</em> zur Verfügung. Wählen Sie diese aus. Damit wird Ihnen zukünftig die Eingabe des Strings

<pre><code>syso
</code></pre>

gefolgt von dem Shortcut zur <em>Codevervollständigung</em>  <code>CTRL</code>+<code>Leertaste</code>,

sofort zu

<pre><code>System.out.println(); 
</code></pre>

komplettiert.

Sollten Sie Eclipse Neon nutzen, steht Ihnen diese Option in der Liste nicht zur Verfügung.

Der Fokus liegt nun in den Klammern, also bei den Parametern des Aufrufens der <em>print</em>-Funktion.

Ergänzen Sie den Methodenaufruf mit dem String

<pre><code>"Hello World!"
</code></pre>

Ihr Programm ist jetzt fertig.

<h3>7.4 Fehlerprüfung</h3>

Der Shortcut um <em>zur nächsten Warnung oder zum nächsten Fehler springen</em>, <code>CTRL</code>+<code>.</code> , hilft Ihnen, Ihr Projekt auf Fehler oder Warnungen zu überprüfen. Der Screenreader springt damit zum nächsten Fehler oder zur nächsten Warnung. Wie bereits in Kapitel 3.7 erwähnt, wird der Fehler von JAWS nicht sofort vorgelesen. Nutzen Sie <code>Pfeil nach links</code> und dann erneut <code>CTRL</code>+<code>.</code>. Nun wird der Fehler vorgelesen. Schweigt der Screenreader, ist kein Fehler vorhanden.

<h3>7.5 Programmausführung</h3>

Nun können Sie Ihr Programm ausführen. Nutzen Sie hierfür den Shortcut <em>Run</em> <code>CTRL</code>+<code>F11</code>. Ihr Programm wird beim Ausführen dieses Befehls, genau wie beim Speichern mit <code>CTRL</code>+<code>S</code>, als Java-Datei in Ihrem <em>Workspace</em> gespeichert. Darauf weist Sie der zu bestätigende Systemdialog <em>Save and Launch</em> hin.

<h3>7.6 Ansicht wechseln</h3>

Wechseln Sie zwischen den Ansichten, mit <code>CTRL</code>+<code>F7</code>, um zur Ausgabe Ihres Programms in der Console zu gelangen. Halten Sie <code>CTRL</code> gedrückt. Es wird eine Liste aller <em>Views</em> geöffnet, durch welche Sie mit <code>Pfeiltaste nach unten</code>/<code>Pfeiltaste nach oben</code> navigieren können. Wählen Sie <em>Console</em> aus.

Alternativ gelangen Sie auch mit dem Shortcut zum in die <em>Console</em> springen, also <code>CTRL</code>+<code>SHIFT</code>+<code>Q</code>, dann <code>C</code>, direkt in die <em>Console</em>.

Ihr Screenreader sollte nun verlauten lassen: Hello World!

Herzlichen Glückwunsch zu Ihrer ersten Hello-World-Applikation, erstellt in der Eclipse IDE mit dem Screenreader JAWS.

<h3>7.7 Fehlerbehebung</h3>

Lassen Sie uns nun einen Fehler provozieren. Springen Sie hierfür zurück in den <em>Editor</em> mittels <code>F12</code> oder drücken Sie den Hotkey um zwischen den Ansichten zu wechseln, also <code>CTRL</code>+<code>F7</code> und halten Sie <code>CTRL</code> gedrückt. Es ist eine Liste aller <em>Views</em> geöffnet, durch welche Sie mit <code>Pfeiltaste nach unten</code>/<code>Pfeiltaste nach oben</code> navigieren können. Wählen Sie <em>Editor</em> aus.

Springen Sie mittels <em>go to line</em>, also <code>CTRL</code>+<code>L</code>, in Zeile 6 und löschen Sie das Semikolon hinter dem <em>print</em>-Befehl, sodass folgende Syntax übrig bleibt

<pre><code>System.out.println("Hello World!")
</code></pre>

und führen Sie das Programm erneut mit <em>Run</em> aus. Eclipse warnt Sie zwar schon, dass es Fehler im existierenden Projekt gibt, führen Sie es dennoch aus und springen Sie zurück in die <em>Console</em>, mit dem Shortcut <code>CTRL</code>+<code>⇧</code>+<code>Q</code>,<code>C</code>. Dort sollte nun folgende Ausgabe stehen:

<pre><code>Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
Syntax error, insert ";" to complete Statement

at hello.world.Main.main(Main.java:7)
</code></pre>

Um den Fehler zu finden, haben Sie jetzt mehrere Möglichkeiten, davon sind zwei aufgrund der schnellen Anwendung für Screenreadernutzer zu empfehlen:

<ol>
<li>Fehlersuche im <em>Editor</em>

Drücken Sie <code>CTRL</code>+<code>.</code>, um zum nächsten Fehler zu springen  und direkt im Anschluss <code>INSERT</code>+<code>PageDown</code>, um sich den Fehler vorlesen zu lassen. <code>INSERT</code> + <code>PageDown</code> ist ein Shortcut für JAWS, um die Statusleiste auszulesen.

</li>
<li>

Fehlersuche in der <em>Problems</em>-Ansicht

Sobald Sie ihr Programm gespeichert haben aktualisiert sich in der Regel die <em>Problems</em>-Ansicht. Springen Sie in diese mittels ``ALT<code>+</code>SHIFT<code>+</code>Q<code>,</code>X<code>. Dort finden Sie das aufklappbare Listenelement *Errors*. Wenn Sie mit</code>Pfeiltaste nach rechts` dieses Listenelement ausklappen, erhalten Sie die Fehlermeldung:

'Syntax error, insert ";" to complete Statement'

und weitere Zusatzinformationen wie Dateinamen und Zeilennummer. Betätigen Sie die <code>ENTER</code>-Taste, während die Fehlermeldung fokussiert ist, um  direkt in den <em>Editor</em> in die Fehlerzeile zu springen.

</li>
</ol>

Die Baumansicht in der <em>Problems-View</em> wird erst nach dem Kompilieren des Programms aktualisiert und durch JAWS vorgelesen.

Die <em>Problems</em>-Ansicht beinhaltet allerdings nur Probleme die zur Kompilierzeit bekannt sind, Fehler die während der Ausführung entstehen, sogennante <em>RunTimeErrors</em>, werden nur in der <em>Console</em> angezeigt. Somit können die beiden hier vorgestellten Fehlerbehebungsmaßnahmen für solche Fehlertypen nicht angewendet werden. Um solch einen Laufzeitfehler zu provozieren, erzeugen wir abschließend eine <em>ArrayIndexOutOfBoundsException</em>.

Hierfür legen Sie ein <em>Array</em> an. Springen Sie mit <em>go to line</em>, also <code>CTRL</code>+<code>L</code> zu Zeile 6. Verschieben Sie Ihre Ausgabe von "Hello World!" mit Hilfe der <code>ENTER</code>-Taste und legen Sie in der Zeile ein <em>Array</em> an. Lösen Sie eine <em>ArrayIndexOutOfBoundsException</em> in der darauffolgenden Zeile aus. Versuchen Sie z.B auf den Index 2 zuzugreifen, wobei Ihr <em>Array</em> nur 2 Stellen, also die Indizes 0 und 1, besitzt. Nutzen Sie hierfür folgende Syntax

<pre><code>int []a = new int [2];
System.out.println(a[2]);
</code></pre>

Wenn Sie Ihr Programm nun mit <em>Run</em>, also <code>CTRL</code>+<code>F11</code>, starten, wird eine <em>ArrayIndexOutOfBoundsException</em> geworfen.

Springen Sie zurück in die <em>Console</em> mittels <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>, <code>C</code>. Ihnen wird nun die <em>Exception</em> vorgelesen. Nun können Sie, wie bereits zuvor beschrieben, über die <em>Console</em> zur genannten Zeile springen und Ihren Fehler beheben.

<h3>7.8 Der Terminate-Schalter</h3>

Es kann vorkommen, dass Ihr Programm auf einmal nicht mehr läuft und in einer Endlosschleife gefangen ist, je nachdem mit welchen Werten Sie beispielsweise eine Schleife betreten.

Was tun?

Als durchschnittlicher Nutzer wäre die Frage ganz einfach zu beantworten: Man klickt auf den roten <em>Terminate</em>-Schalter, der das Programm sofort beendet. Es ist zwar ein Shortcut zum Auslösen der <em>Terminate</em>-Funktion voreingestellt, allerdings ist dieser dem <em>Debug</em>-Modus vorbehalten.

Statt Eclipse jedesmal zu schließen, wenn sich Ihr Programm nicht wie vorgesehen beenden lässt, lernen Sie nun einen Weg kennen, wie Sie Ihr Programm in der IDE terminieren können.

Lassen Sie uns zuerst dafür sorgen, dass unser kleines Hello-World-Programm endlos durchläuft.

Springen Sie in die letzte Zeile Ihrer <em>main</em>-Methode der Klasse Main. Nutzen Sie hierfür den Weg über die Ansicht der <em>Outline</em>.  Die <em>Outline-View</em> zeigt Ihnen das Gerüst der aktuellen Klasse an, mit all ihren Variablen und Methoden. Der Shortcut, um in die <em>Outline</em> zu gelangen, ist <code>ALT</code>+<code>SHIFT</code>+<code>Q</code>, <code>O</code>. Wir nutzen nun allerdings nicht die <em>Outline-View</em>, sondern die <em>Quick Outline</em>, welche Sie mit <code>CTRL</code>+<code>O</code> öffnen. Dadurch erscheint ein Fenster mit der <em>Outline</em> der aktuellen Klasse als Listenansicht. Diese liegt als neue Ebene über dem <em>Editor</em>-Fenster und schließt sich nach Ausführen der gewünschten Aktion von selbst. Suchen Sie die <em>main</em>-Methode aus dieser Liste heraus und bestätigen Sie Ihre Auswahl. Der Fokus liegt nun auf Ihrer <em>main</em>-Methode, hinter deren Namen. Um schnell an das Ende der Methode zu gelangen, kann es nützlich sein, erst eine Zeile nach unten zu gehen und dann <em>Go to matching bracket</em> mit <code>SHIFT</code>+<code>CTRL</code>+<code>P</code> direkt hinter die schließende Klammer der Methode zu springen. Mit <code>ALT</code>+<code>Pfeiltaste nach unten</code> verschieben Sie einfach die schließende Klammer der Methode eine Zeile nach unten und haben darüber Platz für Ihre Endlosschleife. Sie können auch einfach eine Zeile höher gehen und <code>ENTER</code> drücken. Wie Sie die benötigte Zeile einfügen, bleibt ganz Ihrer Vorliebe überlassen. Erweitern Sie nun die <em>main</em>-Methode um eine Endlosschleife.

Eine mögliche Syntax ist:
    while (true) {
        System.out.     println("La la la!");
    }

Wenn Sie nun mit <code>CTRL</code>+<code>F11</code> Ihr Programm starten, wird dieses sich nicht von alleine beenden. Im Normalfall wundern Sie sich vielleicht, warum Ihr Programm nicht die gewünschte Ausgabe erzeugt, Sie werden sich aber nicht sofort bewusst sein, dass Sie sich in einer Endlosschleife befinden. Springen Sie in die <em>Console</em> (<code>ALT</code>+<code>SHIFT</code>+<code>Q</code>, <code>C</code>), um die Ausgabe Ihrer Applikation zu überprüfen. Ihr Screenreader sollte nun ununterbrochen "La la la!" verlauten lassen. Eine Navigation durch die Ausgaben der <em>Console</em> ist nur schwer möglich, da diese fortlaufend aktualisiert wird.

Da Sie sich bereits mit dem Fokus in der <em>Console</em> befinden, reicht es aus, die Kontextmenü-Taste zu betätigen, um eine Strukturansicht aufzurufen. Wählen Sie aus der Liste <em>Terminate/Disconnect All</em>.

Sie haben Ihr Programm beendet, ohne dabei die Eclipse IDE beenden zu müssen.

Leider können Sie den Erfolg dieser Aktion nur schwer verifizieren. Eine Möglichkeit, dies zu tun, wäre zum Beispiel zu versuchen, an das Ende der Ausgabe in der <em>Console</em> zu navigieren. Hat die Ausgabe ein Ende, ist auch Ihr Programm erfolgreich beendet worden, es sei denn Sie befinden sich in einer Endlosschleife ohne Ausgabe.

Überzeugender ist der erneute Weg über das Kontext-Menü der <em>Console</em>. Wenn die Option <em>Remove All Terminated</em> akustisch als nicht verfügbar gekennzeichnet ist, gibt es keine terminierte Ausführung. Somit können Sie davon ausgehen, dass kein Programm beendet wurde. Sollte Ihr Programm noch laufen, steht Ihnen die Option <em>Terminate/Disconnect All</em> zur Verfügung. Wählen Sie diese aus und versuchen Sie danach erneut <em>Remove All Terminated</em> auszuwählen, um sicherzustellen, dass das Programm beendet wurde und die Ausgaben in der <em>Console</em> gelöscht sind.