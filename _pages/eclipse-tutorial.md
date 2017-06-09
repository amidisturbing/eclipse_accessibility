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
<style>

li p.first {
  display: inline-block; }
li {
  margin: 0; }
span.frame {
  display: block;
  overflow: hidden; }
  span.frame > span {
    border: 1px solid #dddddd;
    display: block;
    float: left;
    overflow: hidden;
    margin: 13px 0 0;
    padding: 7px;
    width: auto; }
  span.frame span img {
    display: block;
    float: left; }
  span.frame span span {
    clear: both;
    color: #333333;
    display: block;
    padding: 5px 0 0; }
span.align-center {
  display: block;
  overflow: hidden;
  clear: both; }
  span.align-center > span {
    display: block;
    overflow: hidden;
    margin: 13px auto 0;
    text-align: center; }
  span.align-center span img {
    margin: 0 auto;
    text-align: center; }
span.align-right {
  display: block;
  overflow: hidden;
  clear: both; }
  span.align-right > span {
    display: block;
    overflow: hidden;
    margin: 13px 0 0;
    text-align: right; }
  span.align-right span img {
    margin: 0;
    text-align: right; }
span.float-left {
  display: block;
  margin-right: 13px;
  overflow: hidden;
  float: left; }
  span.float-left span {
    margin: 13px 0 0; }
span.float-right {
  display: block;
  margin-left: 13px;
  overflow: hidden;
  float: right; }
  span.float-right > span {
    display: block;
    overflow: hidden;
    margin: 13px auto 0;
    text-align: right; }
code, tt {
  margin: 0 2px;
  padding: 0 5px;
  white-space: nowrap;
  border: 1px solid #eaeaea;
  background-color: #f8f8f8;
  border-radius: 3px; }
pre code {
  margin: 0;
  padding: 0;
  white-space: pre;
  border: none;
  background: transparent; }

.highlight pre {
  background-color: #f8f8f8;
  border: 1px solid #cccccc;
  font-size: 13px;
  line-height: 19px;
  overflow: auto;
  padding: 6px 10px;
  border-radius: 3px; }

pre {
  background-color: #f8f8f8;
  border: 1px solid #cccccc;
  font-size: 13px;
  line-height: 19px;
  overflow: auto;
  padding: 6px 10px;
  border-radius: 3px; }
  pre code, pre tt {
    background-color: transparent;
    border: none; }
sup {
    font-size: 0.83em;
    vertical-align: super;
    line-height: 0;
}
</style>

<!-- START TOC -->
  <h1>Inhaltsverzeichnis</h1>
<ul id="toc">
<li><a href="#top">Eclipse Tutorial</a>

<ul>
<li><a href="#eclipse">1. Was ist die Eclipse IDE?</a></li>
<li><a href="#installation">2. Installation</a>

<ul>
<li><a href="#anforderungen">2.1 Anforderungen</a></li>
<li><a href="#download">2.2 Download</a></li>
<li><a href="#win-installation">2.3 Eclipse auf dem PC installieren</a></li>
</ul>
</li>
<li><a href="#grundlagen">3. Grundlagen</a>

<ul>
<li><a href="#first-start">3.1 Starten und der Startbildschirm</a></li>
<li><a href="#32dateien-organisation">3.2 Wie Dateien organisiert werden</a>

<ul>
<li><a href="#workspaces-und-projekte">3.2.1 Workspaces und Projekte</a>

<ul>
<li><a href="#workspace">3.2.1.1 Workspace</a></li>
<li><a href="#projekte">3.2.1.2 Project</a></li>
<li><a href="#struktur">3.2.1.3 Strukturierung des Workspace und der Projekte</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#workspace-anlegen">3.3 Einen Workspace anlegen</a></li>
<li><a href="#projekt-anlegen">3.4 Ein Projekt anlegen</a></li>
<li><a href="#klasse-anlegen">3.5 Eine Klassen erstellen</a></li>
<li><a href="#classpath">3.6 Der Classpath</a></li>
<li><a href="#kompilieren-und-fehler">3.7 Kompilieren und Fehlerbehebung</a></li>
<li><a href="#programm-ausfuehren">3.8 Ein Programm ausführen</a></li>
<li><a href="#auto-complete">3.9 Autovervollständigung mit <em>Code Assist</em> nutzen</a></li>
</ul>
</li>
<li><a href="#tipps-und-tricks">4. Tipps und Tricks</a></li>
<li><a href="#shortcuts">4.1 Gedächtnisstütze für Keyboard-Shortcuts</a></li>
<li><a href="#code-assist">4.2 Code Assist</a>

<ul>
<li><a href="#vorschlag-fehler">4.2.1 Vorschläge zur Fehlerbehandlung</a></li>
<li><a href="#definition">4.2.2 Definitionen einsehen</a></li>
<li><a href="#attribute-und-methoden">4.2.3 Alle Attribute und Methoden im aktuellen Editorfenster anzeigen</a></li>
<li><a href="#formatierung">4.2.4 Perfekte Code-Formatierung</a></li>
<li><a href="#clean-up">4.2.5 Clean Up</a></li>
<li><a href="#to-dos">4.2.6 To-Dos verfolgen</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#fortgeschrittenes">5. Fortgeschrittene Themen</a>

<ul>
<li><a href="#interface-anlegen">5.1 Ein neues Interface erstellen</a></li>
<li><a href="#arbeiten-mit-packages">5.2 Arbeiten mit Packages</a>

<ul>
<li><a href="#package-explorer">5.2.1 In den Package Explorer springen</a></li>
</ul>
</li>
<li><a href="#dateien-importieren">5.3 Dateien importieren</a></li>
<li><a href="#archiv-importieren">5.4 Archive importieren</a></li>
<li><a href="#refactoring">5.5 Code-Refactoring</a></li>
<li><a href="#plugins">5.6 Plugins installieren</a>

<ul>
<li><a href="#marketplace">5.6.1 Eclipse Marketplace</a></li>
<li><a href="#update-manager">5.6.2 Update Manager</a></li>
<li><a href="#manuell">5.6.3 Manuelle Installation</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="suchen-und-navigieren">6. Suche und Navigation</a>

<ul>
<li><a href="#suchen-und-ersetzen">6.1 Suche/Ersetze Funktionalität im Editor</a></li>
<li><a href="#zurueck">6.2 Die Zurück Funktion</a></li>
<li><a href="#editor-navigation">6.3 Navigation im Editor</a>

<ul>
<li><a href="#in-editor-springen">6.3.1 Von überall in den Editor springen</a></li>
<li><a href="#zwischen-fenstern-navigieren">6.3.2 Zwischen den offenen <em>Editor</em>-Fenstern navigieren</a></li>
<li><a href="#springe-in-zeile">6.3.3 Zu einer bestimmten Zeile im Editor springen</a></li>
</ul>
</li>
<li><a href="#console-navigation">6.4 Navigation in der Console</a>

<ul>
<li><a href="#aufbau-console">6.4.1 Aufbau der <em>Console</em>-Ansicht</a></li>
<li><a href="#console-oeffnen">6.4.2 Weitere <em>Console</em>-Fenster öffnen</a></li>
<li><a href="#console-exceptions">6.4.3 Exceptions in der <em>Console</em></a></li>
</ul>
</li>
<li><a href="#65problems-navigation">6.5 Navigation in der <em>Problems</em>-View</a>

<ul>
<li><a href="#problems-view">6.5.1 Wie ist die die <em>Problems</em>-View aufgebaut?</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="#hello-world">7. Erstellen einer Hello World Applikation</a>

<ul>
<li><a href="#java-dateien">7.1 Anlegen von Java Dateien</a></li>
<li><a href="#zeile">7.2 Zeilenweise navigieren</a></li>
<li><a href="#codevervollstaendigung">7.3 Codevervollständigung</a></li>
<li><a href="#fehlerpruefung">7.4 Fehlerprüfung</a></li>
<li><a href="#programmausfuehrung">7.5 Programmausführung</a></li>
<li><a href="#ansict-wechseln">7.6 Ansicht wechseln</a></li>
<li><a href="#exeptions">7.7 Exeptions</a></li>
<li><a href="#terminate">7.8 Der Terminate-Schalter</a></li>
</ul>
</li>
</ul>
</li>
</ul>


<!-- END TOC -->
<h1 id="top">Eclipse Tutorial</h1>

  <p>Dieses Tutorial richtet sich an blinde Softwareentwickler/innen,
    die in der Hochsprache Java innerhalb der Eclipse IDE Programme
    schreiben möchten und bis jetzt kein geeignetes Tutorial für
    sehbehinderte Menschen finden konnten. Das gewählte Betriebssystem ist
    Windows. Als unterstützende Technologie wird der Screenreader JAWS
    genutzt. Sollten Sie mit NVDA oder einem anderen Screenreader vertraut
    sein, spricht nichts dagegen, dieses Tutorial mit dem Screenreader
    Ihrer Wahl zu bearbeiten.</p>

  <p>
    Die Grundlage für dieses Tutorial bietet ein <a
      href="https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml">Eclipse
      Tutorial</a> der <em>University of Washington</em>, welches unter der URL
    <a
      href="https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml">https://courses.cs.washington.edu/courses/cse143/11wi/eclipse-tutorial/index.shtml</a>
    abrufbar ist.
  </p>

 <h2 id="eclipse">1. Was ist die Eclipse IDE?</h2>

  <p>Die Eclipse IDE (Integrated Development Environment) ist eine
    generische, quelloffene Software-Entwicklungsumgebung. Diese basiert
    auf einem Plugin-Modell, das es ermöglicht die IDE
    betriebssystemübergreifend für verschiedenste Entwicklungen zu nutzen,
    sofern Java auf dem System installiert ist.</p>

  <h2 id="installation">2. Installation</h2>

  <h3 id="anforderungen">2.1 Anforderungen</h3>

  <p>
    Vor der Installation der Eclipse IDE muss entweder das JDK (Java
    Development Kit) oder die JRE (Java Runtime Environment) auf ihrem
    Computer installiert sein. Sie können diese unter <a
      href="http://java.sun.com/javase/downloads/index.jsp">http://java.sun.com/javase/downloads/index.jsp</a>
    downloaden. Die Installation des JDK wird angeraten, da dieses Ihnen
    den Zugriff auf die Dokumentation und den Quellcode der Standard-Java-Klassen ermöglicht.
  </p>

  <h3 id="download">2.2 Download</h3>

  <p>
    Die offizielle Seite für den Download der Eclipse IDE ist <a
      href="https://www.eclipse.org/downloads">https://www.eclipse.org/downloads</a>.
    Um die Navigation so einfach wie möglich zu halten, startet dieses
    Tutorial eine Ebene tiefer auf der Eclipse-Website, als es der
    offizielle Download-Link tut.
  </p>

  <ol id="steps-download">
    <li>Rufen Sie die Seite <a
      href="https://www.eclipse.org/downloads/packages">https://www.eclipse.org/downloads/packages</a>
      in Ihrem Browser auf.
    </li>
    <li>Laden Sie die <strong>Eclipse IDE für Java
        Developers</strong> herunter.
    </li>
  </ol>


  <p>
    <em>Anmerkung: Sie haben hier die Wahl zwischen <strong>Eclipse
        IDE für Java Developers</strong>, <strong>Eclipse IDE für Java EE
        Developers</strong> und weiteren Versionen für Java-Entwickler. Alle sind für
      dieses Tutorial geeignet.
    </em>
  </p>

  <p>
    Zur Auswahl der jeweiligen Eclipse-Version gelangen Sie im
    Hauptbereich der Seite. Nutzen Sie hierfür den Link <em>Skip to main content</em> am Anfang der Seite.
        In diesem stehen pro Eclipse Variante fünf
    Download-Links zur Verfügung. Die Links im Hauptbereich der Seite teilen sich der Reihe nach
         wie folgt auf:</p>

  <ol id="versionen">
    <li>Link zur Übersichtsseite des Pakets</li>
    <li>Link zur Downloadseite der Version für Windows 64-bit</li>
    <li>Link zur Downloadseite der Link zur Version für Mac 64-bit</li>
    <li>Link zur Downloadseite der Version für Linux 32-bit</li>
    <li>Link zur Downloadseite der Version für Linux 64-bit</li>
  </ol>
  <p>Falls Sie also Linux oder Mac nutzen, finden Sie auch hierfür
    die dementsprechenden Downloadlinks im Hauptfenster der
    Downloadseite.</p>

  <h3 id="win-installation">2.3 Eclipse auf dem PC installieren</h3>

  <ol id="steps-installation">
    <li>Verschieben oder Kopieren Sie das heruntergeladene .zip oder
      .tar.gz Archiv in Ihr Root-Verzeichnis (unter Windows <strong>C:\</strong>).
    </li>
    <li>Entpacken Sie das Archiv. Somit wird Ihnen ein Ordner namens
      <strong>eclipse</strong> im aktuellen Verzeichnis erstellt.
    </li>
  </ol>


  <h2 id="grundlagen">3. Grundlagen</h2>

  <h3 id="starten-und-der-startbildschirm">3.1 Starten und der
    Startbildschirm</h3>

  <ol id="steps-start">
    <li><p>
        Führen Sie die Datei <strong>eclipse.exe</strong> aus.
      </p></li>
    <li><p>
        Legen Sie Ihren Arbeitsbereich, den sogenannten <strong>Workspace</strong>
        fest. Für dieses Tutorial ist der vorausgewählte Workspace im Ordner
        <strong>C:\eclipse</strong> am besten geeignet.
      </p>
      <p>
        <em>Anmerkung: Der Workspace kann für jede Sitzung neu definiert
          werden. Falls Sie nur einen Workspace für all Ihre Projekte
          benötigen, aktivieren Sie die Checkbox "Use this as default and do
          not ask again". Unter Windows: Halten Sie die <code>ALT</code>-Taste
          gedrückt und drücken Sie zusätzlich<code>U</code>.
        </em>
      </p>
    </li>
    <li><p>Starten Sie die Eclipse IDE.</p></li>
    <li><p>
        Bei erstmaligem Starten sehen Sie den <em>Welcome Bildschirm</em>.
        Dieser stellt eine gewisse Barriere dar. In dem Fenster befindet
        sich (ab Eclipse Neon) ein Markierungsfeld mit der Beschriftung "Always
          show Welcome at start up". Dieses ist per default aktiviert.
        Deaktivieren Sie es. Der <em>Welcome Bildschirm</em> stellt
        so beim nächsten Start keine Hürde mehr dar.
      </p></li>
    <li><p>
        Tabben Sie zu <em>Workspace</em> und bestätigen Sie. Nun befinden
        Sie sich in Ihrem Arbeitsbereich. Die für dieses Tutorial
        wichtigsten Ansichten sind der <em>Package Explorer</em>, der <em>Editor</em>
        und die <em>Console</em>.
      </p></li>
  </ol>

  <h4 id="standard-ansicht">3.1.1 Aufbau der Standardansicht</h4>
  <p>
    Nachdem der <em>Welcome-Bildschirm</em> geschlossen wurde, befinden Sie sich in der
    Standard-Entwickler-Ansicht der Eclipse IDE, in welcher Ihnen die
    wichtigsten Ansichten sofort zur Verfügung stehen. Der <em>Package
      Explorer</em> beinhaltet alle geöffneten <em>Projekte</em>, welche sich in
    Ihrem <em>Workspace</em> befinden. Einzelne Dateien können Sie im <em>Editor</em>
    öffnen, bearbeiten und speichern. Dieser steht Ihnen ebenfalls in der
    Standardansicht zur Verfügung, ebenso wie das <em>Console</em>-Fenster,
    welches die Ausgaben Ihres Programmes darstellt.
  </p>

  <p>
    Der Fokus liegt beim erstmaligen Starten auf dem <em>Package
      Explorer</em>. Wenn Sie allerdings bereits ein Projekt mit einer Klasse
    erstellt haben und diese im <em>Editor</em>, beim letzten Beenden des Programms
    geöffnet ließen, liegt der Fokus im <em>Editor</em>, an der Stelle, an
    der er auch beim Beenden des Programmes lag.
  </p>

  <h3 id="datei-organisation">3.2 Wie Dateien organisiert werden</h3>

  <h4 id="workspaces-und-projekte">3.2.1 Workspaces und Projekte</h4>

  <p>Eclipse nutzt zwei grundlegende Abstraktionen zum Strukturieren
    von Quellcode.</p>

  <h5 id="workspaces">3.2.1.1 Workspace</h5>

  <p>
    Der <em>Workspace</em> ist das Arbeitsverzeichnis für all Ihre
    Projekte. Sie können mit Eclipse auch mehrere Workspaces verwalten,
    falls Sie dies wünschen.
  </p>
  <h5 id="projekte">3.2.1.2 Project</h5>

  <p>
    Ein <em>Project</em> ist eine Sammlung zusammengehörigen Quellcodes,
    welcher meist ein unabhängiges Programm formt. Kurz gesagt ist Ihr
    Workspace der Ordner, welcher all Ihre Projekte beinhaltet. Einem <em>Project</em>
    ist auch ein <em>Classpath</em> zugeordnet. Der <em>Classpath</em> ist
    der Ort, an welchem Bibliotheken und andere Projekte eingebunden
    werden. Dieses Tutorial widmet sich dem <em>Classpath</em> später in
    einem eigenen Abschnitt.
  </p>

  <h5 id="struktur">3.2.1.3 Strukturierung des Workspace und der
    Projekte</h5>

  <p>
    Immer, wenn Sie in Eclipse ein Projekt anlegen, wird von Eclipse
    automatisch ein neuer, gleichnamiger Ordner im aktuellen Workspace
    angelegt. In diesem Ordner werden zwei weitere Ordner, nämlich <em>bin</em>
    und <em>src</em> (source) angelegt. Sie können den Ordner <em>bin</em>
    ignorieren. In diesem werden automatisch alle Kompilate, also die <em>.class</em>-Dateien,
    gespeichert.
  </p>

  <p>
    All Ihre <em>.java</em>-Dateien befinden sich im <em>src</em>-Ordner.
  </p>

  <p>Zusammengefasst ist also ihr Workspace der Ordner, welcher alle
    Projekte beinhaltet, welche wiederum Ordner, benannt nach den
    zugehörigen Projekten, sind.</p>

  <h3 id="workspace-anlegen">3.3 Einen Workspace anlegen</h3>

  <p>
    Sie können sich Ihren <em>Workspace</em> auch wie den Root-Folder, von welchem
    Eclipse ausgeht, vorstellen. Sie können zwar mehrere Workspaces mit
    Eclipse verwalten, allerdings können Sie nur einen Workspace
    gleichzeitig in Eclipse öffnen. Der <em>Welcome Bildschirm</em> und
    wie Sie diese Hürde meistern wurde bereits im Kapitel Grundlagen unter <a href="#starten-und-der-startbildschirm">
    3.1 Starten und der Startbildschirm</a>
    erklärt. Tabben Sie also zu <em>Workspace</em> und bestätigen Sie.
    Sollten Sie während des Arbeitens mit Eclipse einen neuen Workspace
    anlegen oder einen bereits bestehenden Workspace auswählen wollen,
    gehen Sie über die Menüleiste zu <em>File</em> und dort zu <em>Switch
      Workspace</em>. Es öffnet sich ein weiteres Untermenü, in welchem Sie
    einen Eclipse bereits bekannten <em>Workspace</em> auswählen können.
    Sie können stattdessen auch die Option <em>Other</em> in diesem
    Untermenü nutzen, um das Fenster <em>Workspace Launcher</em> zu öffnen.
    Im <em>Workspace Launcher</em> liegt der Fokus zuerst auf einem
    Auswahlmenü, in welchem Sie wiederum die bekannten <em>Workspaces</em>
    auswählen können. Alternativ steht Ihnen die Möglichkeit zur
    Verfügung, zu einem <em>Workspace</em> im Dateisystem zu navigieren
    und einen bestehenden oder neuen Ordner als <em>Workspace</em>
    auszuwählen. Von der Verwendung eines Ordners, der bereits Dateien
    enthält, die keine Eclipse-Projekte sind, wird abgeraten. Bei der
    Erstauswahl eines Ordners als <em>Workspace</em> wird in diesem ein
    versteckter Ordner namens <em>.metadata</em> erstellt.
  </p>

  <h3 id="projekt-anlegen">3.4 Ein Projekt anlegen</h3>

  <p>
    Nachdem Sie einen <em>Workspace</em> angelegt oder ausgewählt haben, können Sie
    auch Projekte anlegen. Projekte sind die nächstkleinere
    Organisationseinheit nach dem Workspace. Ein Workspace beinhaltet in
    der Regel mehrere Projekte. Um ein neues Projekt anzulegen, nutzen Sie
    die Tastenkombination <em>neues Projekt</em>, nämlich
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>N</code>
    . Es öffnet sich eine Liste, welche Sie durch das Drücken der
    Pfeiltasten fokussieren können. Wählen Sie mit
    <code>↓</code>
    <em>Java Project</em> aus. Benennen Sie Ihr Projekt und bestätigen Sie
    das Formular. Das Projekt ist nun durch Eclipse angelegt worden und im
    <em>Package Explorer</em> verfügbar, zu welchem Sie mit
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>P</code>
    navigieren können. Der aktuelle Fokus des Programm-Cursors
    ändert sich beim Anlegen eines Projektes nur, sollte dieser im <em>Package
      Explorer</em> gelegen haben. In diesem Fall ändert er sich vom vorher
    ausgewählten Projekt zum neu erstellten. Anderenfalls bleibt der Fokus
    an der Stelle, an welcher er sich befand, bevor Sie ein neues Projekt
    angelegt haben.
  </p>

  <h3 id="klasse-anlegen">3.5 Eine Klassen erstellen</h3>

  <p>Nun haben Sie schon Ihr erstes Projekt angelegt und möchten
    sicherlich auch eine eigene Klasse erstellen.</p>

  <p>
    Durch das Kommando <em>Neue Ressource anlegen</em>, also
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>N</code>
    öffnet sich eine Liste, welche Sie dmit den
    Pfeiltasten fokussieren können. Wählen Sie mit
    <code>↓</code>
    <em>Package</em> aus. Wählen Sie dann die gewünschte Java-Resource aus
    der Liste aus. Sie haben die Wahl zwischen den Optionen <em>Class</em>,
    <em>Interface</em>, <em>Enum</em> und <em>Annotation</em>.
  </p>

  <p>
    Alternativ gelangen Sie auch mit der Tastenkombination <em>Neue
      Ressource über das Wizard anlegen</em>
    <code>CTRL</code>
    +
    <code>N</code>
    zum Ziel. Die Klasse wird in dem <em>Project</em> und dem <em>Package</em>
    angelegt, das gerade selektiert ist. Sie können aber im Formular noch
    beides ändern.
  </p>

  <p>Wenn Sie sich bereits in einem Java-Projekt befinden stehen
    Ihnen direkt nach dem Drücken des Shortcuts die Optionen zum Anlegen
    aller möglichen Java Ressourcen zur Verfügung.</p>

  <p>Sie können auch direkt beim Anlegen der Klasse das <em>Package</em>
    angeben, sollte dieses nicht mit dem aktuellen übereinstimmen. Geben
    Sie Ihrer Ressource einen Namen.</p>

  <p>
    Wenn Sie eine Klasse anlegen möchten, die den Startpunkt für Ihre
    Anwendung darstellt, steht Ihnen im nächsten Schritt ein
    Kontrollkästchen zur Verfügung, welches, wenn es aktiviert ist, für
    die Generierung der sogenannten <em>main</em>-Methode sorgt. Aktivieren Sie
    hierfür das Kontrollfeld <em>public static void main (String[]
      args)</em> mit der Tastenkombination für <em>Bestätigen</em>
    <code>ALT</code>
    +
    <code>V</code>
    . Bestätigen Sie das ausgefüllte Formular.
  </p>

  <p>
    Sie können Ihre Klasse direkt beim Erstellen mit den dazugehörigen <em>Modifiers</em>
    ausstatten, indem Sie deren Kontrollfelder unter der Option <em>Modifiers</em>
    aktivieren.
  </p>

  <p>
    Wenn Sie eine andere Klasse erweitern wollen können Sie die
    Superklasse über den Namen spezifizieren. Tun Sie dies, indem Sie
    Paket und Namen über die Punktnotation angeben. Ist die Superklasse
    beispielsweise die Klasse <em>Object</em>, so lautet der Name <em>java.lang.Object</em>,
    da es sich um die Klasse <em>Object</em> im Paket <em>java.lang.</em>
    handelt.
  </p>

  <p>
    Sie können die Superklasse, das Interface und die vorzugenerierenden Methoden
    auch in diesem Formular über die <em>Browse</em>-Funktion auswählen.
  </p>

  <p>Der Fokus liegt nach dem Anlegen im <em>Editor</em> auf Ihrer neu
    erstellten Klasse in Zeile 1.</p>

  <h3 id="classpath">3.6 Der Classpath</h3>

  <p>
    Wird eine Java-Klasse instanziiert, muss die Java Virtual Machine (JVM) wissen,
    wo die kompilierte Klasse, also die zugehörige
    .class-Datei, liegt. Im <em>Classpath</em> stehen die Pfade zu den
    obersten <em>Packages</em> eines Java-Programms und zu eingebundenen
    .jar-Dateien. Die kompilierten .class-Dateien eines Java-Projekts sind
    in einer Ordnerstruktur abgelegt, die der Paketstruktur des Projekts
    gleicht. In .jar-Dateien sind die .class-Dateien ebenfalls in dieser
    Ordnerstruktur abgelegt. Dadurch weiß die JVM jederzeit, wo der
    kompilierte Code zu einer bestimmten Klasse liegt und kann diesen
    nutzen.
  </p>

  <h3 id="kompilieren-und-fehler">3.7 Kompilieren und Fehlerbehebung</h3>

  <p>Dieser Abschnitt beschäftigt sich nicht mit Debugging. Stattdessen soll hier auf das
    Beheben von kleineren Kompilierfehlern eingegangen werden.</p>

  <p>Markierungen in Form von roten Unterringelungen für <em>Errors</em>
    (Fehler) und gelben Unterringelungen für <em>Warnings</em> (Warnungen)
    weisen sehende Menschen frühzeitig auf Kompilierfehler hin. Dies ist nur möglich, da
    Ihr Code fortlaufend durch Eclipse in Zwischencode für die JVM (Jave Virtual Machine) übersetzt wird.
  </p>

  <p>
    Da diese Markierungen in erster Linie visuell sind wird Blinden oder sehbehinderten Programmierern empfohlen,
    regelmäßig von dem Shortcut
    <code>CTRL</code>
    +
    <code>.</code>
    gebrauch zu machen, um <em>zur nächsten Warnung oder zum nächsten
      Fehler springen</em>. Der Fokus Ihres Screenreader springt damit sofort
    zum nächsten Fehler oder zur nächsten Warnung in der aktuellen
    Java-Datei und liest Ihnen die unterringelte Stelle vor. Sollten Sie
    den Fehler hieraus noch nicht deduzieren können, haben Sie zwei
    Möglichkeiten, um ihm auf einem simplen Weg auf die Spur zu kommen.
    Allerdings wird der Fehler von JAWS nicht sofort vorgelesen.
    Drücken Sie einmal Pfeil nach links und dann erneut <code>CTRL</code>
    +
    <code>.</code>. Nun wird der Fehler vorgelesen. Wird Ihnen nichts vorgelesen, sollte kein <em>Errors</em>
    und keine <em>Warnings</em> vorhanden sein.
  </p>

  <ol id="fehler-finden">
    <li><p>Aktivieren Sie den JAWS-Cursor, um damit ein
        Mouse-Hover zu simulieren.</p>

      <p>
        Der Maus-Cursor steht nach der Nutzung des Befehls <em>zur
          nächsten Warnung oder zum nächsten Fehler springen</em> genau am Ende
        der Zeichenfolge die das Problem verursacht. Es reicht also aus,
        die Pfeiltaste ein- oder zweimal anzuschlagen, um so den JAWS-Cursor
        etwas nach links zu bewegen. Es öffnet sich ein Systemdialog mit der
        Fehlerbeschreibung und möglichen <em>Quick-Fixes</em>, welche
        Eclipse Ihnen vorschlägt. Die Error-Message des Systemdialogs ist
        sofort fokussiert und wird Ihnen vom Screenreader vorgelesen.
        Darunter befinden sich die Quick-Fixes, die Sie direkt auswählen
        können. Eclipse setzt diese unmittelbar für Sie um.
      </p></li>
    <li><p>
        Nutzen Sie an dieser Stelle <em>View</em>-Menü anzeigen, also
        <code>CTRL</code>+<code>Leertaste</code>.
      </p>

      <p>
        Dieser Shortcut zeigt Ihnen das Menü für die aktuelle
        Cursor-Position an. Da Sie mittels
        <code>CTRL</code>
        +
        <code>.</code>
        , also <em>zur nächsten Warnung oder zum nächsten Fehler
          springen</em>, direkt hinter die markierte Stelle gelangen, werden Ihnen
        die möglichen Problembehandlungen direkt angezeigt. Allerdings
        müssen Sie bei dieser Möglichkeit auf die Error-Message verzichten,
        denn diese ist kein Teil des <em>View</em>-Menüs.
      </p></li>
  </ol>


  <p>Sie sollten sich trotz dieser Möglichkeiten nicht allein auf
    die Intelligenz Ihrer IDE verlassen, denn auch Eclipse hat nicht immer
    recht!</p>

  <h3 id="programm-ausfuehren">3.8 Ein Programm ausführen</h3>
  <p>Nun ist es an der Zeit, Ihr Programm auszuführen. Wenn Sie Ihr
    Programm zum ersten Mal starten, müssen Sie Eclipse erst mitteilen,
    als welche Art von Java-Programm das Ihre gestartet werden soll.</p>

  <p>
    Eclipse kennt grundsätzlich zwei gängige Varianten, um Java-Code
    auszuführen. Einmal das <em>Java-Applet</em>, welches im Browser läuft
    und die <em>Java-Application</em>, ein eigenständiges Programm. Für
    dieses Tutorial ist nur die <em>Java-Application</em> relevant.
  </p>

  <p>
    Um lästige Systemdialoge zu vermeiden, nutzen Sie den Hotkey <em>Run
      as Java Application</em>,
    <code>SHIFT</code>
    +
    <code>ALT</code>
    +
    <code>X</code>
    , dann
    <code>J</code>
    .
    Falls dieser Shortcut nicht wie beschrieben funktioniert können Sie Ihr Programm auch 
    mit dem Befehl <em>Run</em>,
    also
    <code>CTRL</code>
    +
    <code>F11</code>, starten
    .
    Wenn Sie Ihr Programm zum ersten Mal auf diese Weise starten, öffnet sich
    ein Systemdialog, welcher Sie fragt, als welche Art von Anwendung Ihr Programm ausgeführt
    werden soll. Wählen Sie <em>Java Application</em> aus und bestätigen
    Sie Ihre Eingabe.

    Ihr Programm wird beim Ausführen dieses Befehls, wie auch beim <em>Speichern</em>
    mittels
    <code>CTRL</code>
    +
    <code>S</code>
    , als Java-Datei in Ihrem Workspace gespeichert. Darauf weist Sie der
    zu bestätigende Systemdialog <em>Save and Launch</em> hin.
  </p>

  <p>
    Außerdem verfügt Eclipse über einen <em>Run</em>-Schalter, welcher der 9.
    Schalter von links, oben in der Toolbar von Eclipse ist. Direkt neben
    diesem Schalter befindet sich ein kleiner schwarzer Pfeil, welcher
    unter anderem dazu dient, die <em>Run Configurations</em> zu setzen.
    Die <em>Run Configurations</em> werden in einem Dialogfeld
    dargestellt, in welchem Sie auch die <em>Main Class</em>, also den
    Startpunkt Ihres Programms, setzen können. Dies können Sie im Reiter <em>Main</em>
    tun. Direkt daneben befindet sich die Registerkarte <em>Arguments</em>,
    wo Sie die Argumente setzen können, mit denen Ihr Programm
    standardmäßig starten soll. Dies ist empfehlenswert, falls Ihre
    Software Startparameter erwarten sollte.
  </p>

  <p>Keine Angst, Sie müssen nicht mit der Maus auf den kleinen
    schwarzen Pfeil neben dem <em>Run</em>-Schalter klicken, um die Parameter für
    den Start Ihres Programmes festzulegen. Stattdessen gehen sie wie
    folgt vor:</p>

  <p>
    Navigieren Sie in der Symbolleiste zu dem Schalter, welcher mit <em>Run
      Main</em>-Aufteilung-Schalter beschriftet ist und drücken Sie
    <code>↓</code>
    . Es öffnet sich eine Liste, in welcher Sie die Option <em>Run
      Configuration</em> auswählen dürfen. In dem sich nun öffnenden Dialogfeld
    navigieren Sie zur Registerkarte <em>Arguments</em>. Im Freifeld
    der Registerkarte, die den Titel <em>Program Arguments</em> trägt,
    können Sie die Argumente für den Programmstart mit Leerzeichen
    getrennt eingeben. Eine Eingabe von "spam and eggs" käme dem Starten
    Ihres Programms über die Kommandozeile, mittels "java [Name des
    Programms] spam and eggs", gleich.
  </p>

  <h3 id="auto-complete">
    3.9 Autovervollständigung mit <em>Code Assist</em> nutzen
  </h3>

  <p>
    Die meisten Menschen schätzen an Entwicklungsumgebungen die
    programmiersprachensprachenbezogenen Unterstützungen, die die
    jeweilige Umgebung mitbringt. Was bei Microsoft Visual Studio <em>IntelliSense</em>
    heißt, ist bei Eclipse das Feature <em>Code Assist</em>.
  </p>

  <p>
    <em>Code Assist</em> wird in einigen Situationen automatisch von der
    Eclipse IDE ausgelöst, beispielsweise bei der Eingabe eines Punktes
    (also <code>.</code>), nach Variablen oder Klassennamen. Wenn Sie <em>Code Assist</em>
    selbst auslösen möchten, nutzen Sie
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    . Zur Veranschaulichung folgt ein kleines Beispiels aus dem <em>Hello World Tutorial</em>:
  </p>

  <p>Schreiben Sie im Quellcode-Editor von Eclipse</p>
  <pre>
    <code>syso
</code>
  </pre>

  <p>
    dann
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    . Wenn Sie diese Kombination zum ersten Mal ausführen, steht Ihnen bis
    zur Eclipse-Version Luna die Auswahl <em>Enable Smart Code
      Completion</em> zur Verfügung. Wählen Sie diese aus. Da wird Ihnen
    zukünftig die Eingabe des Strings
  </p>
  <pre>
    <code>syso
</code>
  </pre>

  <p>
    gefolgt von dem Shortcut zur <em>Codevervollständigung</em>
    <code>CTRL</code>
    +
    <code>Leertaste</code>
  </p>

  <p>sofort zu</p>
  <pre>
    <code>System.out.println(); 
</code>
  </pre>

  <p>komplettiert.</p>

  <p>
    <em>Code Assist</em>
    bietet viele weitere Hilfestellungen.
  </p>

  <p>
    Stellen Sie sich vor, Sie programmieren seit einigen Stunden
    und haben gerade eine längere Pause beendet. Eigentlich wollten Sie
    eine Fallunterscheidung aufstellen, nur von welcher Variable
    sollte sie abhängen? Statt Ihren Code erneut
    durchzugehen, drücken Sie einfach <em>View</em>-Menü anzeigen, also
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    . Das sich nun öffnende <em>View</em>-Menü enthält alle möglichen
    Funktionalitäten, die Sie an dieser Stelle nutzen können, wie zum
    Beispiel lokale oder globale Variablen, Methoden der jeweiligen Klasse
    oder statische Imports.
  </p>

  <p>
    Wenn Sie ein Java-Objekt benutzen möchten, geben Sie mindestens den Anfangsbuchstaben als
    Großbuchstaben an. Drücken Sie nun den Hotkey für <em>Code Assist</em>,
    also
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    . Eclipse öffnet eine Liste von Vorschlägen für Sie, die direkt
    fokussiert wird. Durch die Liste kann wie gewohnt mit den Pfeiltasten
    navigiert werden. Für das aktuell fokussierte Objekt wird
    direkt das zugehörigen <em>JavaDoc</em> geöffnet. Durch das Drücken
    der Taste
    <code>F2</code>
    wird die Vorlesefunktion aktiviert. Dies kann sehr nützlich sein, um
    zu entscheiden, welche Methode Sie am geschicktesten verwenden oder
    welche Objekt-Implementierung Sie in Ihrem Projekt nutzen möchten.
  </p>

  <p>
    Diese Funktion ist auch sehr gut für Neugierige geeignet, die einfach
    nur mehr über ein Objekt, das Sie verwenden, wissen möchten. Dies
    bedeutet schlichtweg, dass alle Informationen in der Online-Java-API,
    die aus <em>JavaDoc</em>-Kommentaren generiert werden, für Sie
    verfügbar sind, ohne das Programm zu wechseln.
  </p>

  <p>
    Sie sollten nun eine gute Vorstellung davon haben, was man mit <em>Code
      Assist</em> alles machen kannst. Probieren Sie es aus!
  </p>

  <h2 id="tipps-und-tricks">4. Tipps und Tricks</h2>

  <p>Eclipse bietet ihnen viele kleine Features, die dafür gemacht
    wurden, um Ihren Programmieralltag zu vereinfachen. Die meisten sind
    trivial, werden aber häufig genutzt und sorgen somit für eine enorme
    Produktivitätssteigerung.</p>

  <h3 id="shortcuts">4.1 Gedächtnisstütze für Keyboard-Shortcuts</h3>

  <p>
    In Eclipse müssen Sie sich wirklich nur an eine Tastenkombination
    erinnern, nämlich
    <code>CTRL</code>
    +
    <code>SHIFT</code>
    +
    <code>L</code>
    . Diese zeigt Ihnen eine alphabetisch sortierte Liste aller
    Tastaturbefehle in der Eclipse IDE an, welche auch sofort fokussiert
    ist.
  </p>

  <h3 id="code-assist">4.2 Code Assist</h3>

  <p>
    Dieses Tutorial enthält einen ganzen Abschnitt über
    die <em>Code Assist</em>-Funktion. Diesen finden Sie im Kapitel 
    <a href="#auto-complete">3.9 Autovervollständigung mit <em>Code Assist</em> nutzen</a></li>
  </p>

  <h4 id="vorschlag-fehler">4.2.1 Vorschläge zur Fehlerbehandlung</h4>

  <p>
    Diese Funktion wird im Abschnitt <a href="#kompilieren-und-fehler">3.7 Kompilieren und Fehlerbehebung</a>
    kurz angeschnitten. Eclipse bietet Ihnen eine Funktion, die Ihnen
    Lösungsmöglichkeiten aufzeigt, um Kompilierfehler und Warnungen zu
    beheben. Sollte irgendeine Art von Fehler oder Warnung auftreten, springen Sie in die entsprechende Zeile und drücken Sie
    <code>CTRL</code>
    +
    <code>1</code>
    . Eine Liste der möglichen Optionen erscheint. Sie enthält nicht immer
    die besten Lösungsvorschläge, aber oftmals funktionieren sie gut. Dies
    gilt vor allem bei Fehlern wie vergessenen Imports. Dennoch sollten
    Sie die Vorschläge gut prüfen, bevor Sie diese anwenden.
  </p>

  <h4 id="definition">4.2.2 Definitionen einsehen</h4>

  <p>
    Im Folgenden werden Shortcut behandelt, welche dienlich sind, falls Sie Code nutzen, welchen Sie nicht selbst geschrieben haben. Wenn Sie
    nämlich direkt zu der Definition einer Methode, Klasse, eines
    Interfaces oder Ähnlichem springen möchten, nutzen Sie einfach die
    Taste
    <code>F3</code>
    .
  </p>

  <p>Um diese Funktion nutzen zu können, müssen Sie allerdings Zugang
    zu den Quelldateien, also .java-Files, haben. Mit vorkompilierten
    Bibliotheken können Sie diese Funktion nicht nutzen.</p>

  <h4 id="attribute-und-methoden">4.2.3 Alle Attribute und Methoden
    im aktuellen Editorfenster anzeigen</h4>

  <p>
    Eclipse tut wirklich alles, damit Sie sich nicht auf Ihr Gedächtnis
    verlassen müssen. Sollten Sie sich nicht mehr genau erinnern, wie die
    Attribute oder Methoden der Klasse heißen, die Sie aktuell bearbeiten,
    drücken Sie einfach
    <code>CTRL</code>
    +
    <code>O</code>
    . Diese Funktion ist aber nicht nur eine Gedächtnisstütze, sondern
    auch eine perfekte Navigationshilfe. Wählen Sie einfach mit Hilfe der
    Pfeiltasten das gesuchte Element aus und drücken Sie <code>ENTER</code>. Damit
    springen Sie im Editor direkt hinter den Namen in der Variablen- oder
    Methoden-Deklaration.
  </p>

  <h4 id="formatierung">4.2.4 Perfekte Code-Formatierung</h4>

  <p>Sie können Ihren Quellcode mit Eclipse auf zwei Arten
    autoformatieren.</p>

  <ol id="bereichformatierung">
    <li>Markieren Sie den gewünschten Abschnitt mit <code>SHIFT</code>+<code>←</code>/<code>→</code> und
      nutzen Sie anschließend <code>CTRL</code>+<code>I</code>. Der markierte Bereich wird
      perfekt eingerückt.</li>
  </ol>


  <p>Um das vorherige Auswählen zu umgehen, nutzen Sie die zweite
    Option.</p>

  <ol id="komplettformatierung">
    <li>Der komplette Code der aktuellen .java-Datei wird mittels <code>CTRL</code>+<code>SHIFT</code>+<code>F</code>
      nach der Java-Standardspezifikation formatiert. Diese Variante
      beinhaltet auch Abstände und Zeilenumbrüche.
    </li>
  </ol>


  <h4 id="clean-up">4.2.5 Clean Up</h4>

  <p>Diese Funktion von Eclipse soll nur am Rande erwähnt werden.
    Wenn Sie in der Menüleiste <em>Source</em> auswählen und hier <em>Clean Up</em>, beginnt
    Eclipse, Ihren Code auf Redundanzen zu untersuchen, um im Anschluss
    ungenutzte oder bedeutungslose Codefragmente zu eliminieren. Dieses
    Feature ist dazu entworfen, Ihren Code eleganter zu machen. Wenn Sie
    diese Funktion auf den von Ihnen geschriebenen Code anwenden, ist es
    erstrebenswert, dass dieser unverändert bleibt. Falls Sie die
    Grundprinzipien der Java-Programmierung beherrschen, liegt dies sicher im Bereich
    Ihrer Fähigkeiten.</p>

  <h4 id="to-dos">4.2.6 To-Dos verfolgen</h4>

  <p>Während des Schreibens von Programmen kommen Ihnen sicherlich
    immer wieder Dinge in den Kopf, die Sie zu einem späteren Zeitpunkt
    noch umsetzen möchten. In der Industrie herrscht der Standard, dass
    solche unerledigten Dinge mittels</p>
  <pre>
    <code>// TODO: Aufgabenbeschreibung
</code>
  </pre>

  <p>
    gekennzeichnet werden. Eclipse macht Ihnen Ihren Programmieralltag an
    dieser Stelle leichter, indem es Ihren Quellcode nach solchen
    Kommentaren durchsucht und diese in einem eigenen Fenster namens <em>Tasks</em>
    bündelt. Dieses erreichen Sie in erster Instanz nur
    über die Menüleiste, via <em>Window</em> bei <em>Show View</em> finden Sie <em>Task</em>. Wenn Sie das
    Fenster einmal geöffnet haben, können Sie es über den Shortcut um zwischen
      den Ansichten wechseln, also <code>CTRL</code>+<code>F7</code>, ansteuern. Mit den
    Pfeiltasten kommen Sie zur gewünschten Ansicht. Die <em>Tasks</em>-Ansicht
    erscheint unter dem <em>Editor</em>-Fenster als einer der Reiter auf der Höhe
    der Konsole, wo auch das <em>Problems</em>-Fenster angesiedelt ist. Die
    einzelnen <em>Tasks</em> können mit den Pfeiltasten ausgewählt werden.
    Drücken Sie <code>ENTER</code>, springt Ihr Cursor direkt in die Zeile des
    jeweiligen <em>Tasks</em>.
  </p>

  <p>
    Alle <em>Tasks</em> werden projektübergreifend, das heißt dür alle in Ihrem <em>Workspace</em> geöffneten Projekte, angezeigt.
  </p>

  <h2 id="forgeschrittenes">5. Fortgeschrittene Themen</h2>

  <h3 id="interface-anlegen">5.1 Ein neues Interface erstellen</h3>

  <p>
    Sollten Sie den Abschnitt <a href="#klasse-anlegen">3.5 Eine Klassen erstellen</a> bereits gelesen
    haben, wird Ihnen das hier beschriebene Vorgehen bekannt erscheinen.
    Drücken Sie nun die Tastenkombination <em>Neue Ressource anlegen</em>
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>N</code>
    . Oder nutzen Sie die Tastenkombination <em>Neue Ressource über
      das Wizard anlegen</em>
    <code>CTRL</code>
    +
    <code>N</code>
    .
  </p>

  <p>
    Wählen Sie <em>Interface</em> aus und spezifizieren Sie das <em>Package</em>,
    falls notwendig. Benennen Sie die neue Ressource. Alle Interfaces, die
    durch das, welches Sie neu anlegen erweitert werden sollen, können Sie durch Bestätigen das <em>Add</em>-Schalters
    im Formular hinzufügen.
  </p>

  <p>
    Nach Bestätigen des ausgefüllte Formulars wird Ihr neues <em>Interface</em> angelegt.
  </p>

  <h3 id="arbeiten-mit-packages">5.2 Arbeiten mit Packages</h3>

  <p>
    Ein <em>Package</em>, zu deutsch Paket, ist mehr oder weniger das
    Äquivalent zu Namespaces in Sprachen wie Javascript oder
    C++. Durch das Strukturieren von Klassen in Paketen können Sie
    sicherstellen, dass keine Namenskonflikte entstehen. In vielen
    Javaprojekten kommen beispielsweise zwei verschiedene Date-Klassen zum
    Einsatz, nämlich java.util.Date und java.sql.Date. Jede der beiden
    Klassen befindet sich innerhalb eines Paketes, einmal dem
    Paket java.util und einmal in dem Paket java.sql, sodass keine
    Konflikte zwischen den beiden Klassen entstehen.
  </p>

  <p>Wäre keine der beiden Klassen innerhalb eines Paketes
    angesiedelt, würden die Bibliotheken nicht kompilieren. Der Compiler
    würde eine der beiden Klassen als eine Re-Definition der anderen
    Klasse ansehen. Dies würde zu Verwirrung führen.</p>

  <p>Pakete erlauben auch eine logische organisatorische Abstraktion
    für verwandte Gruppen von Java-Klassen und Interfaces. Um ein Paket
    für Ihre Klasse oder Schnittstelle anzugeben, muss die erste Zeile Ihrer
    Java-Datei wie folgt lauten:</p>
  <pre>
    <code>package [package.name];
</code>
  </pre>

  <p>Dieses Tutorial wird hier nicht weiter auf Pakete als
    Sprachmerkmale eingehen. Es gibt viele Ressourcen, online und
    anderswo, die Ihnen helfen können, diesen Aspekt der
    Programmiersprache Java zu verstehen. Sollten Sie absoluter Neuling
    auf diesem Gebiet sein, kann eine Lösung sein, Ihre
    Lieblings-Suchmaschine einmal mit dieser Frage zu bemühen. Sollten Sie
    gezielt mit Paketen arbeiten, wird empfohlen, sich vorher mit den
    Einschränkungen, die dieses Sprachmerkmal mit sich bringt, vertraut zu
    machen.</p>

  <p>
    Des Weiteren sollen die paketbezogenen Funktionalitäten von Eclipse
    besprochen werden. Die erste ist der <em>Package Explorer</em>. Der <em>Package
      Explorer</em> präsentiert Ihnen Ihre Projekte mit dem Fokus auf deren Java
    Paket Struktur. Sollten Sie Eclipse schon einmal genutzt haben, ist Ihnen
    vielleicht aufgefallen, dass neu angelegte Klassen in Eclipse nicht
    einfach irgendwo, sondern im sogenannten <em>Default Package</em>
    auftauchen, welches einen Knotenpunkt in der Hierarchie des <em>Package
      Explorers</em> darstellt. Geben Sie nämlich kein Paket für Ihre neue
    Java-Klasse an, wird es mit allen anderen nicht verpackten Klassen in
    diesem Standardpaket gruppiert.
  </p>

  <h4 id="package-explorer">5.2.1 In den Package Explorer springen</h4>

  <p>
    Hierfür dient Ihnen der Hotkey
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>P</code>
    .
  </p>

  <p>
    Um ein neues Paket anzulegen, gehen Sie wie folgt vor: Drücken Sie nun
    die Tastenkombination für <em>Neue Ressource anlegen</em>,
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>N</code>
    . Es öffnet sich eine Liste, welche Sie durch das Anschlagen der
    Pfeiltasten fokussieren können. Wählen Sie mit
    <code>↓</code>
    <em>Package</em> aus.
  </p>

  <p>Ihr Paket existiert erst dann wirklich, wenn es mit
    Inhalten, also Ressourcen im Sinne von Klassen oder Interfaces, gefüllt
    wurde. Logischer ist es allerdings, das Paket beim Anlegen einer
    Klasse zu definieren, wodurch es direkt mit angelegt wird 
    (siehe Kapitel <a href="#klasse-anlegen">3.5 Eine Klassen erstellen</a>).</p>

  <h3 id="dateien-importieren">5.3 Dateien importieren</h3>

  <p>Angenommen, Sie haben Ihr Projekt in Eclipse erstellt, aber
    wollen die einzelnen Komponenten nicht von Grund auf neu in Eclipse
    erstellen, sondern einige vorgefertigte Dateien, beispielsweise aus
    Ihrem lokalen Dateisystem, nutzen. Hierfür gibt es drei Wege für
    Sehbehinderte, welche Sie nachfolgend aufgelistet finden.</p>

  <ol id="import-varianten">
    <li><p>Der Weg über die Menüleiste</p>

      <p>
        Springen Sie in die Menüleiste der Eclipse IDE zu <em>File</em> und wählen
        Sie <em>Import</em> aus der Liste aus. Nun öffnet sich das <em>Import</em>-Fenster.
        Der Fokus liegt auf einem Textfeld mit dem Text "type filter text".
        Dieses dient der Eingabe des Suchtextes zur Filterung der möglichen
        zu importierenden Typen von Quellen. Tippen Sie <em>File</em> ein, um die
        Ergebnisliste zu minimieren. Drücken Sie <code>↓</code> um in die Auswahlliste zu
        springen und wählen Sie <em>File System</em>. Bestätigen Sie Ihre Auswahl. Es
        öffnet sich nun ein Fenster in welchem Sie, unter <em>From
          directory</em>, die gewünschte Datei auswählen und zu Ihrem
        Eclipse-Projekt hinzufügen können. Statt einer Datei können Sie auch
        ein ganzes Verzeichnis auswählen. Sobald Sie einen Ordner ausgewählt
        haben, haben Sie die Wahl, ganze Verzeichnisse oder nur deren
        Unterkomponenten zu importieren. Es öffnet sich eine Tabelle mit den
        Inhalten des selektierten Ordners. Um ganze Ordner zu importieren,
        aktivieren Sie dessen Markierungsfeld. Möchten Sie an dieser Stelle
        bestimmte Dateien anstelle von ganzen Verzeichnissen auswählen,
        wählen Sie statt der übergeordneten Komponente dessen gewünschten
        Inhalt. Jede dieser Dateien kann einzeln ausgewählt werden, genau
        wie vorher die Verzeichnisse. Des Weiteren haben Sie in diesem
        Fenster die Möglichkeit unter <em>Into folder:</em> das jeweilige <em>Project</em>,
        sowie das <em>Package</em>, oder, anders formuliert, das Verzeichnis
        zu spezifizieren, in welches die Datei importiert werden soll.
        Stellen Sie sicher, dass Sie in den richtigen Ordner importieren und
        dass die Optionen so eingestellt sind, wie Sie sie wünschen, und
        bestätigen Sie mit der <em>Finish</em>-Taste.
      </p></li>
    <li><p>
        Der Weg über das Kontextmenü im <em>Package Explorer</em>
      </p>

      <p>
        Springen Sie zuerst mit
        <code>ALT</code>
        +
        <code>SHIFT</code>
        +
        <code>Q</code>
        ,
        <code>P</code>
        in den <em>Package Explorer</em>. Wählen Sie das richtige Projekt
        und drücken Sie dann die Kontextmenü-Taste. Sie können das Projekt
        auch später, wie bereits vorher erwähnt, im <em>Import</em>-Dialog
        noch ändern. Wählen Sie aus der sich öffnenden Liste <em>Import</em>.
        Das <em>Import</em>-Fenster wird geöffnet. Ihnen stehen die selben
        Eingabemöglichkeiten wie auch bei der Auswahl über die Menüleiste
        zur Verfügung. Gehen Sie ab jetzt genau wie dort beschrieben
        vor.
      </p></li>
    <li><p>Copy und Paste aus dem Dateisystem</p>

      <p>
        Kopieren Sie die gewünschte Datei in Ihrem Dateisystem, ganz einfach
        mit
        <code>CTRL</code>
        +
        <code>C</code>
        oder über das Kontextmenü. Gehen Sie in die Eclipse IDE und wählen
        Sie das Projekt sowie das Paket aus, in welches Sie diese Datei
        importieren wollen und drücken Sie "Einfügen", also
        <code>CTRL</code>
        +
        <code>V</code>
        . Die Datei wird nun in das Projekt importiert.
      </p></li>
  </ol>


  <h3 id="archiv-importieren">5.4 Archive importieren</h3>

  <p>
    Das Importieren eines Archivs ist dem Importieren einer Datei sehr
    ähnlich. Öffnen Sie das Kontextmenü Ihres Projekts im Paket-Explorer
    und klicken Sie auf Import. Dieses Mal verwenden Sie <em>Archive</em> als
    Ihren Filtertext und wählen die Option <em>Archive File</em>.
    Bestätigen Sie Ihre Auswahl.
  </p>

  <p>
    Gehen Sie so vor wie auch beim Importieren von Dateien, aber dieses Mal,
    anstatt ein Verzeichnis auszuwählen, wählen Sie die benötigte
    Archivdatei. Dies wird dazu führen, dass Sie das Dateisystem im Archiv
    so gut wie möglich durchsuchen können, wenn Sie ein Verzeichnis
    importieren. Wählen Sie Unterordner zum Importieren oder wählen
    Sie einfach Dateien aus. Nachdem Sie alle Optionen ausgewählt haben,
    bestätigen Sie mit <em>Finish</em>. Ihr Archiv wird nun entpackt und
    in das Projekt importiert.
  </p>

  <p>
    Wenn Sie Ihr Archiv stattdessen per <em>Copy & Paste</em> aus dem Dateisystem
    importieren möchten, wird dieses, falls es nicht bereits entpackt ist,
    als komprimierter Ordner zum Projekt hinzugefügt. Öffnen Sie diesen
    Ordner im Editor. Da das Editorfenster nun fokussiert ist, können Sie
    direkt mit
    <code>SHIFT</code>
    +
    <code>tab</code>
    in die Funktionsleiste des Editors navigieren. Diese befindet sich im
    Falle eines geöffneten Archives direkt über dem eigentlichen
    Editorbereich. Dort steht ihnen neben einigen anderen auch die
    Funktion <em>Extract files from the archive</em> zur Verfügung. Wählen
    Sie diese aus. Dadurch öffnet sich das <em>Select Target to
      extract to</em>-Fenster, in welchem Sie den Ort angeben können, an welchem
    das Archiv entpackt werden soll.
  </p>

  <h3 id="refactoring">5.5 Code-Refactoring</h3>

  <p>
    <em>Refactoring</em> bezieht sich auf die Umformung von Code, um
    seinen Stil, sein Design, oder etwas dergleichen zu verbessern. Das Ergebnis der Ausführung
    des Codes im Bezug auf den Benutzer ändert sich hierbei nicht. In der Strukturierung, unbemerkt durch den Anwender oder die Anwenderin, fallen die Änderungen jedoch ins Gewicht.
  </p>

  <p>Schon das Umbenennen von Klassen oder Methoden würde in
    größeren Projekten einen riesigen Aufwand bedeuten. Stellen Sie sich
    vor, Sie müssten jedesmal einen regulären Ausdruck schreiben, der das
    für Sie tut, oder gar alles manuell ändern. Natürlich lässt Eclipse
    Sie hier nicht alleine. Die IDE bietet Ihnen einen einfachen Weg,
    Ihren kompletten Code mit allen Referenzen auf die umzuformende
    Code-Passage zu aktualisieren.</p>

  <p>
    Der Hotkey für das <em>Refactoring</em> an sich ist
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>T</code>
    , wodruch eine Ansicht geöffnet wird, unter welcher Sie die Art des <em>Refactoring</em>
    wählen können. Die simpelste Umformung ist die <em>Rename</em>-Funktion,
    welche Sie auch über den Shortcut
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>R</code>
    erreichen. Die sich öffnende Ansicht beinhaltet außer des Textfeldes
    für den neuen Namen der Auswahl das Markierungsfeld <em>Update
      References</em>. Stellen Sie sicher, dass dieses ausgewählt ist und
    bestätigen Sie Ihre Eingabe. Ihre Methode oder Klasse ist nun für alle
    im <em>Package Explorer</em> geöffneten Projekte umbenannt.
  </p>

  <h3 id="plugins">5.6 Plugins installieren</h3>

  <h4 id="marketplace">5.6.1 Eclipse Marketplace</h4>

  <p>
    Sie können Plugins in Eclipse auf unterschiedliche Weise installieren.
    Es gibt den <em>Eclipse Marketplace</em>, welcher eine Art Appstore
    für Eclipse-PlugIns ist. Um ein Plugin hierüber installieren zu können,
    muss es im <em>Marketplace</em> gehostet werden.
  </p>

  <h4 id="update-manager">5.6.2 Update Manager</h4>

  <p>
    Ist dem nicht der Fall, empfiehlt die <em>Eclipse Foundation</em> eine
    Installation über den Update-Manager, welchen Sie im Menü unter <em>Help bei Install New Software...</em> finden. Nach Auslösen des Schalters <em>Add</em>
    können Sie entweder eine URL eingeben, oder durch auslösen der
    Schaltfläche <em>Local</em> ein Plugin aus Ihrem Dateisystem wählen.
    Diese Option prüft zum Beispiel, ob Kompatibilitätsprobleme zu Ihrer
    Eclipse-Version bestehen oder ob Abhängigkeiten zu anderen Plugins
    bestehen.
  </p>

  <h4 id="manuell">5.6.3 Manuelle Installation</h4>

  <p>
    Ein Plugin in Eclipse manuell zu installieren bedeutet schlichtweg,
    das Plugin in den sich im Installationsordner von Eclipse befindenden
    Ordner namens <em>plugins</em> zu legen. Starten Sie danach die IDE
    neu.
  </p>

  <h2 id="suchen-und-navigieren">6. Suche und Navigation</h2>

  <h3 id="suchen-und-ersetzen">6.1 Suche/Ersetze Funktionalität im
    Editor</h3>

  <p>
    Mittels dem Shortcut
    <code>CTRL</code>
    +
    <code>F</code>
    öffnen Sie das <em>Suchen und Ersetzen</em> Fenster. Geben Sie den
    gesuchten Wert ein und gegebenenfalls den, mit welchem dieser ersetzt
    werden soll und bestätigen Sie Ihre Eingaben mit dem gewünschten
    Schalter. Ihnen stehen hierfür in erster Instanz <em>Find</em> und <em>Replace
      All</em> zur verfügung, wobei <em>Find</em> die zusätzliche Möglichkeit
    bietet, mittels der Taste
    <code>N</code>
    und <em>Replace All</em> mit der Taste
    <code>A</code>
    eine Möglichkeit zum Betätigen bietet. Außerdem sind die Schalters
    mittels
    <code>TAB</code>
    ansteuerbar. Wurde bereits <em>Find</em> angewendet haben Sie die
    zusätzlichen Optionen <em>Replace/Find</em>, welches einen Wert nach
    dem Anderen ersetzt, sowie <em>Replace</em>, welches nur einen
    einzigen Wert mit dem zu Ersetzenden auswechselt.
  </p>

  <h3 id="zurueck">6.2 Die Zurück Funktion</h3>

  <p>
    In jedem Formular, welches Sie in Eclipse ausfüllen, befindet sich ein
    Zurück-Schalter. Falls Sie also versehentlich die falsche Art von
    Java-Datei, z.B. <em>Class</em> statt <em>Interface</em>, gewählt
    haben, können Sie über diesen Schalter im Formular zurücknavigieren
    und Ihre Eingabe korrigieren.
  </p>

  <h3 id="editor-navigation">6.3 Navigation im Editor</h3>

  <p>
    Der <em>Editor</em> ist das Fenster, in welchem Sie Ihren Quellcode
    schreiben. Dieser ähnelt den gängigen Text-Editoren, die Sie auch für
    das reine Editieren von Fließtexten kennen. Der Editor, welcher in
    Eclipse integriert ist, bietet zusätzlich noch einige visuelle Hilfen
    zum Erstellen von Software, auf welche in diesem Tutorial bewusst
    nicht eingegangen wird.
  </p>

  <p>
    Die nächsten Unterüberschriften beschäftigen sich mit den
    Möglichkeiten, den <em>Editor</em> als blinder Programmierer effizient
    zu nutzen.
  </p>

  <h4 id="in-editor-springen">6.3.1 Von überall in den Editor
    springen</h4>

  <p>Der Fokus des Cursors wechselt, je nachdem in welchem Bereich
    der Eclipse IDE Sie sich gerade befinden. Es ist ineffizient die einzelnen Bereiche der Eclipse IDE der Reihenfolge nach
    anzusteuern, um in den gewünschten Bereich zu gelangen.</p>

  <p>Wie Sie bereits im Laufe dieses Tutorials erfahren konnte,
    bietet Eclipse die Möglichkeit, mittels Shortcuts oder Hotkeys direkt
    in bestimmte Bereiche zu springen.</p>

  <p>
    Um von einer beliebigen Stelle in der Eclipse IDE in den <em>Editor</em>
    zu springen, nutzen Sie die Taste
    <code>F12</code>
    .
  </p>

  <h4 id="zwischen-fenstern-navigieren">
    6.3.2 Zwischen den offenen <em>Editor</em>-Fenstern navigieren
  </h4>

  <p>
    Während der Entwicklung eines Programmes öffnen wir für gewöhnlich
    viele <em>Editor</em>-Fenster. Jedesmal, wenn wir eine Klasse aus dem
    <em>Package Explorer</em> auswählen, öffnet Eclipse diese automatisch
    in einem neuen Fenster. Somit können all diese geöffneten <em>Editor</em>-Fenster
    bis sie aktiv geschlossen werden, auch erreicht werden. Die Eclipse
    IDE bietet Ihnen im Großen und Ganzen drei Möglichkeiten, um
    komfortabel zwischen den offenen <em>Editor</em>-Fenstern zu
    navigieren.
  </p>

  <p>
    Wen wir irgendwo hin wollen ist es hilfreich, wenn wir uns erst einmal
    die Möglichkeiten anzeigen lassen, wo wir hingehen können. So verhält
    es sich auch im Fall von mehreren geöffneten <em>Editor</em>-Fenstern.
  </p>

  <p>
    Der Shortcut für <em>offene Editoren anzeigen</em> ist in der
    Standardeinstellung mit
    <code>CTRL</code>
    +
    <code>E</code>
    belegt.
  </p>

  <p>
    Wenn Sie stattdessen die Tastenkombination
    <code>CTRL</code>
    +
    <code>F6</code>
    oder
    <code>CTRL</code>
    +
    <code>SHIFT</code>
    +
    <code>F6</code>
    nutzen steht dies auch für <em>offene Editoren anzeigen</em>, wobei
    der Wechsel zwischen den Fenstern sofort nach loslassen der ctrl-Taste
    erfolgt.
  </p>

  <p>
    Ein einfaches Navigieren zum jeweils nächsten, bzw. vorhergehenden <em>Editor</em>-Fenster
    ist mittels
    <code>ALT</code>
    +
    <code>←</code>
    /
    <code>→</code>
    möglich.
  </p>

  <h4 id="springe-in-zeile">6.3.3 Zu einer bestimmten Zeile im
    Editor springen</h4>

  <p>
    Um in eine bestimmte Zeile im Editorfenster zu springen, muss dieses
    fokussiert sein. Nutzen Sie den Hotkey
    <code>CTRL</code>
    +
    <code>L</code>
    der das Fenster <em>go to line</em> öffnet, geben Sie die gewünschte
    Zeilennummer ein und bestätigen Sie Ihre Eingabe.
  </p>

  <h3 id="console-navigation">6.4 Navigation in der Console</h3>

  <h4 id="aufbau-console">
    6.4.1 Aufbau der <em>Console</em>-Ansicht
  </h4>

  <p>
    Die drei Konsolen, die standardmäßig in Eclipse zur Verfügung
    stehen sind die <em>Process Console</em>, die <em>Stacktrace
      Console</em> und die <em>CVS Console</em>
  </p>

  <p>
    Die in der Console verfügbaren Befehle werden im Folgenden
    behandelt und können mit aktiviertem JAWS-Cursor angesteuert werden.
    Sie sind durch beschriftete Icons abgebildet. Diese befinden sich rechts auf der Höhe
    des <em>Console</em>-Reiters. Sollte die Breite
    Ihres Bildschirms nicht ausreichen, um die Icons neben den Reitern
    darzustellen, verschieben sich diese leicht nach unten.
  </p>

  <p>
    Es handelt sich um <em>Clear Console</em>, <em>Display Selected
      Console</em>, <em>Open Console</em>, <em>Pin</em> und <em>Scroll Lock</em>.
    In diesem Tutorial soll nur <em>Open Console</em> näher besprochen
    werden.
  </p>

  <p>
    Sollten Sie Ihre <em>Console</em> aus irgend einem Grund einmal
    geschlossen haben, können Sie diese mittels des Shortcuts <em>In
      die Konsole springen</em>,
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>C</code>
    , erneut öffnen. Egal ob eine <em>Console</em> geöffnet ist oder
    nicht, mit diesem Shortcut springen Sie direkt hinein.
  </p>

  <h4 id="console-oeffnen">
    6.4.2 Weitere <em>Console</em>-Fenster öffnen
  </h4>

  <p>
    In manchen Fällen kann es nötig sein, eine zweite <em>Console</em> zu
    öffnen. Hier kommt der JAWS-Cursor ins Spiel. Springen Sie zuerst in
    die <em>Console</em>, um schon in der Nähe des Bereichs zu sein.
    Aktivieren Sie den JAWS-Cursor, in dem Sie
    <code>Insert</code>
    +
    <code>-</code>
    auf dem Nummernpad drücken. Sie hören nun "ziehe JAWS zu PC". Nun
    können Sie mit den Pfeiltasten den Cursor bedienen.
  </p>

  <p>
    Nutzen Sie jetzt die Pfeiltasten um etwas nach oben und rechts zu
    navigieren. Leider sind die einzelnen Icons in der Leiste der <em>Console</em> standardmäßig nicht beschriftet. Bleiben Sie an dieser Stelle probierfreudig. Mit der Taste
    <code>/</code>
    können Sie einen Linksklick auf ein Element ausführen. Wenn Ihnen JAWS
    das Wort "Kontextmenü" mitteilt, befinden Sie sich in dem Drop-Down,
    in welchem Sie eine neue <em>Console</em> öffnen können.Navigieren Sie mit den Pfeiltasten zu <em>New Console View</em> und drücken Sie
    <code>ENTER</code>
    . Sie haben nun eine zweite <em>Console</em> geöffnet.
  </p>

  <p>
    Drücken Sie
    <code>F12</code>,
    um wiederum zurück in den Editor zu springen.
  </p>

  <h4 id="console-exceptions">
    6.4.3 <em>Exceptions</em> in der <em>Console</em>
  </h4>

  <p>
    Beim Ausführen eines Programmes werden oft, je nach Parameter, Fehler
    oder Ausnahmen provoziert. Gerade in den Randfällen kann es schnell einmal
    zu einer <em>NullPointerException</em> kommen, wenn Sie als
    Programmierer diesen Fall im Vorfeld nicht bedenken. Auch hier bietet
    Eclipse Ihnen eine Hilfestellung, um schnell an die Stelle, an welcher
    die <em>Exception</em> geworfen wird, zu gelangen.
  </p>

  <p>
    Sollte Ihr Programm eine <em>Exception</em> ausgelöst haben, stellt
    Eclipse diese Ausgabe in der <em>Console</em> mit einem Link dar.
  </p>

  <p>
    Sollte beispielsweise eine <em>IndexOutOfBoundsException</em> geworfen
    werden, würde Ihr Screenreader in etwa verlauten lassen:
  </p>
  <pre>
    <code>Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 3
at hello.world.Main.foo(Main.java:23)
at hello.world.Main.main(Main.java:18)
</code>
  </pre>

  <p>Diese Ausgabe möchte ich Ihnen nun Zeile für Zeile erläutern.</p>

  <p>In Zeile 1:</p>
  <pre>
    <code>Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 3
</code>
  </pre>

  <p>teilt Ihnen Eclipse mit, dass im Haupt-Thread Ihrer Anwendung,
    im Thread "main", eine ArrayIndexOutOfBoundsException an der Stelle 3
    geworfen wurde.</p>

  <p>In Zeile 2:</p>
  <pre>
    <code>at hello.world.Main.foo(Main.java:23)
</code>
  </pre>

  <p>informiert Sie Ihre IDE, dass diese Exception in der Klasse mit
    dem Namen Main, des Paketes namens hello.world, in der mit foo
    benannten Methode, in Zeile 23 geworfen wurde. Der letzte Teil,
    nämlich</p>
  <pre>
    <code>(Main.java:23)
</code>
  </pre>

  <p>ist der Link in Zeile 23.</p>

  <p>Zeile 3:</p>
  <pre>
    <code>    at hello.world.Main.main(Main.java:18)
</code>
  </pre>

  <p>erläutert, dass die Ausnahme in der Zeile 18, der Klasse mit dem Namen Main, welche
    sich in einem Paket namens hello.world befindet, in der mit main
    benannten Methode, in Zeile 18 ausgelöst wurde.</p>

  <p>Der hintere Teil ist wiederum der Link zur Zeile, also</p>
  <pre>
    <code>(Main.java:23)
</code>
  </pre>

  <p>Mit diesem Wissen stehen Ihnen folgende Möglichkeiten zur
    Verfügung, um an die angegebenen Stellen zu gelangen.</p>

  <ol id="jaws-cursor-exception">
    <li>Möglichkeit: Nutzung des Shortcut <em>go to line</em>
      Nutzen Sie den Hotkey <em>go to line</em>, also <code>CTRL</code>+<code>L</code>
      und geben Sie die Zeilennummer ein, in welcher Die Exception entstand
      oder ausgelöst wurde. Sie springen nun direkt zurück in den <em>Editor</em>
      in die angegebene Zeile. Der Fokus liegt am Anfang der Zeile.
    </li>
    <li>Möglichkeit: Nutzung des JAWS-Cursor Aktivieren Sie den
      JAWS-Cursor, navigieren Sie mit den Pfeiltasten an die verlinkte
      Stelle und lösen Sie einen Linksklick aus. Sie springen nun
      direkt zurück in den <em>Editor</em> in die angegebene Zeile. Der
      Fokus liegt im Gegensatz zur 1. Möglichkeit am Ende des
      Ausdrucks, der die Ausnahme auslöste.
    </li>
  </ol>


  <h3 id="problems-navigation">6.5 Navigation in der Problems-View</h3>

  <p>
    Ein Weg zu <em>Problems</em>, ist der Shortcut zum öffnen der Listenansicht alle <em>Views</em>, also
    <code>CTRL</code>
    +
    <code>SHIFT</code>
    +
    <code>F7</code>
    . Wählen Sie in der Ansicht mit den Pfeiltasten <em>Problems</em> aus.
  </p>

  <p>
    Alternativ steht Ihnen der Hotkey <em>in Problems springen</em>,
    nämlich
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>X</code>
    zur Verfügung.
  </p>

  <h4 id="problems-view">
    6.5.1 Wie ist die die <em>Problems</em>-Ansicht aufgebaut?
  </h4>

  <p>
    Die Ansicht der <em>Problems</em> ist eine schlichte Baumansicht mit
    allen Fehlern und allen Warnungen aus allen geöffneten Projekten. Die
    Probleme sind nach Typ strukturiert. Hieraus resultiert ein Baum pro
    Typ, also je nach Vorkommnis in all den in der IDE geöffneten
    Projekten maximal zwei Bäume. Hierfür ist einer für <em>Warnings</em> und
    der andere für <em>Error</em> reserviert.
  </p>

  <p>
    Die Navigation in dieser Ansicht gestaltet sich intuitiv. Mit der
    Taste
    <code>→</code>
    klappen Sie die jeweilige Baumansicht auf. Mit
    <code>↑</code>
    oder
    <code>↓</code>
    navigieren Sie durch die Warnungen, beziehungsweise durch die Fehler.
    Mit
    <code>Enter</code>
    gelangen Sie direkt in die Zeile, hinter das Auftreten des jeweiligen
    Fehlers beziehungsweise der jeweiligen Warnung.
  </p>

  <h2 id="hello-world">7. Erstellen einer Hello World Applikation</h2>

  <h3 id="java-dateien">7.1 Anlegen von Java-Dateien</h3>

  <p>
    Erstellen Sie ein neues Projekt , siehe Kapitel <a href="#projekt-anlegen">3.4 Ein Projekt anlegen</a></li>. Legen Sie darin eine neue
    Java-Klasse an und benennen Sie diese, wie im Kapitel <a href="#klasse-anlegen">3.5 Eine Klassen erstellen</a></li>. Geben Sie ihr den Namen <em>Main</em>.
    Sorgen Sie dafür, dass die Klasse, die Ihnen erstellt wird, bereits
    eine <em>main-Methode</em> enthält. In Ihrem <em>Workspace</em> wurde
    nun eine Datei mit dem Namen <em>Main.java</em> erstellt.
  </p>

  <h3 id="zeile">7.2 Zeilenweise navigieren</h3>

  <p>
    Navigieren Sie nun in Zeile 6. Dafür haben Sie zwei Möglichkeiten.
    Entweder Sie nutzen die Pfeiltasten oder Sie wählen den Shortcut <em>go
      to line</em>,
    <code>CTRL</code>
    +
    <code>L</code>
    und geben in dem sich nun öffnenden Formular die Zeilennummer 6 an.
  </p>

  <p>
    In Zeile 6 befindet sich ein Kommentar, der automatisch beim Anlegen
    der Java-Datei mit der <em>main-Methode</em> generiert wurde. Der
    Kommentar lautet
  </p>
  <pre>
    <code>//TODO Auto-generated method stub
</code>
  </pre>

  <h3 id="codevervollstaendigung">7.3 Codevervollständigung</h3>

  <p>Ersetzen Sie den Kommentar durch einen print-Befehl. Markieren
    Sie hierfür den Kommentar und tippen Sie</p>
  <pre>
    <code>syso
</code>
  </pre>

  <p>
    dann
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    . Wenn Sie diese Kombination zum ersten Mal ausführen steht Ihnen bis
    zur Version Luna von Eclipse die Auswahl <em>Enable Smart Code
      Complition</em> zur Verfügung. Wählen Sie diese aus. Somit wird Ihnen
    zukünftig die Eingabe des Strings
  </p>
  <pre>
    <code>syso
</code>
  </pre>

  <p>
    gefolgt von dem Shortcut zur <em>Codevervollständigung</em>
    <code>CTRL</code>
    +
    <code>Leertaste</code>
    ,
  </p>

  <p>sofort zu</p>
  <pre>
    <code>System.out.println(); 
</code>
  </pre>

  <p>komplettiert.</p>

  <p>Sollten Sie Eclipse Neon nutzen, steht Ihnen diese Option in der
    Liste nicht zur Verfügung.</p>

  <p>Der Fokus liegt nun in den Klammern, also bei den Parametern des
    Aufrufes der print-Funktion.</p>

  <p>Ergänzen Sie den Methodenaufruf mit dem String</p>
  <pre>
    <code>"Hello World!"
</code>
  </pre>

  <p>Ihr Programm ist jetzt fertig.</p>

  <h3 id="fehlerpruefung">7.4 Fehlerprüfung</h3>

  <p>
    Der Shortcut <em>zur nächsten Warnung oder zum nächsten Fehler
      springen</em>,
    <code>CTRL</code>
    +
    <code>.</code>
    , hilft Ihnen, Ihr Projekt auf Fehler oder Warnungen zu überprüfen.
    Der Screenreader springt damit zum nächsten Fehler oder zur nächsten
    Warnung. Schweigt der Screenreader, ist kein Fehler vorhanden.
  </p>

  <h3 id="programmausfuehrung">7.5 Programmausführung</h3>

  <p>
    Nun können Sie Ihr Programm ausführen. Nutzen Sie hierfür den Shortcut
    <em>Run</em>
    <code>SHIFT</code>
    +
    <code>F11</code>
    . Ihr Programm wird beim Ausführen dieses Befehls, genau wie beim <em>Speichern</em>
    mit
    <code>CMD</code>
    +
    <code>S</code>
    , als Java-Datei in Ihrem Workspace gespeichert. Darauf weist Sie der
    zu bestätigende Systemdialog <em>Save and Lauch</em> hin.
  </p>

  <h3>7.6 Ansicht wechseln</h3>

  <p>
    Drücken Sie nun <em>zwischen den Ansichten Wechseln</em>, also
    <code>CTRL</code>
    +
    <code>F7</code>,
    um zur Ausgabe Ihres Programms in der <em>Console</em> zu gelangen.
    Halten Sie
    <code>CTRL</code>
    gedrückt. Es wird eine Liste aller <em>Views</em> geöffnet, durch
    welche Sie mit
    <code>↓</code>
    /
    <code>↑</code>
    navigieren können. Wählen Sie <em>Console</em> aus.
  </p>

  <p>
    Alternativ gelangen Sie auch mit <em>in die Console springen</em>,
    also
    <code>CTRL</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    , dann
    <code>C</code>
    direkt in die <em>Console</em>.
  </p>

  <p>Ihr Screenreader sollte nun verlauten lassen: Hello World!</p>

  <p>Herzlichen Glückwunsch zu Ihrer ersten Hello-World-Applikation,
    erstellt in der Eclipse IDE mit dem Screenreader JAWS.</p>

  <h3>7.7 Exeptions</h3>

  <p>
    Lassen Sie uns nun einen Fehler provozieren. Springen Sie hierfür
    zurück in den Editor. Drücken Sie den Hotkey <em>zwischen den
      Ansichten Wechseln</em>, also
    <code>CTRL</code>
    +
    <code>F7</code>,
    um zurück in den Editor zu gelangen. Halten Sie
    <code>CTRL</code>
    gedrückt. Es ist eine Liste aller <em>Views</em> geöffnet, durch
    welche Sie mit
    <code>↓</code>
    /
    <code>↑</code>
    navigieren können. Wählen Sie <em>Editor</em> aus.
  </p>

  <p>
    Springen Sie mittels <em>go to line</em>, also
    <code>CTRL</code>
    +
    <code>L</code>
    , in Zeile 6 und löschen Sie das Semikolon hinter dem print-Befehl,
    sodass folgende Syntax übrig bleibt
  </p>
  <pre>
    <code>System.out.println("Hello World!")
</code>
  </pre>

  <p>
    und führen Sie das Programm erneut mit <em>Run</em> aus. Eclipse warnt
    Sie zwar schon, dass es Fehler im existierenden Projekt gibt, führen
    Sie es dennoch aus und springen Sie zurück in die Console, mit dem
    Shortcut
    <code>CTRL</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>C</code>
    . Dort sollte nun folgende Ausgabe stehen:
  </p>
  <pre>
    <code>Exception in thread "main" java.lang.Error: Unresolved compilation problem: 
Syntax error, insert ";" to complete Statement

at hello.world.Main.main(Main.java:7)
</code>
  </pre>

  <p>
    Nun müssen Sie den JAWS-Cursor aktivieren. Tun Sie dies, indem Sie
    <code>Insert</code>
    +
    <code>-</code>
    auf dem Nummernpad drücken. Sie hören nun "ziehe JAWS zu PC". Nun
    können Sie mit den Pfeiltasten den Cursor bedienen. Wenn Sie nun mit
    <code>/</code>
    auf die Angabe der Zeile, in welcher der Fehler auftritt, klicken,
    nämlich auf (Main.java:7), springen Sie direkt in die Zeile.
  </p>

  <p>
    Zum Deaktivieren des JAWS-Cursor drücken Sie nun
    <code>Insert</code>
    +
    <code>-</code>
    auf dem Nummernpad. Da die gesamte Zeile, in welcher der Fehler
    auftritt, markiert ist, drücken Sie
    <code>→</code>,
    um ans Ende dieser Zeile zu gelangen. Fügen Sie nun das Semikolon
    wieder ein.
  </p>

  <p>Abschließend provozieren wir noch eine
    ArrayIndexOutOfBoundsException.</p>

  <p>
    Legen Sie ein Array an. Springen Sie mit <em>go to line</em>, also
    <code>CTRL</code>
    +
    <code>L</code>
    zu Zeile 6. Verschieben Sie Ihre Ausgabe von "Hello World!" mit Hilfe
    der Enter-Taste und legen Sie in der Zeile ein Array an. Lösen Sie
    eine ArrayIndexOutOfBoundsException in der darauffolgenden Zeile aus.
    Versuchen Sie z.B auf den Index 3 zuzugreifen, wobei Ihr Array nur 2
    besitzt. Nutzen Sie hierfür folgende Syntax
  </p>
  <pre>
    <code>int []a = new int [2];
System.out.println(a[3]);
</code>
  </pre>

  <p>
    Wenn Sie Ihr Programm nun mit <em>Run</em>, also
    <code>F11</code>
    , starten, wird eine ArrayIndexOutOfBoundsException geworfen.
  </p>

  <p>
    Springen Sie zurück in die <em>Console</em> mittels
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>C</code>
    . Ihnen wird nun die Exception vorgelesen. Nun können Sie, wie bereits
    zuvor beschrieben, über die Console zur genannten Zeile springen und
    Ihren Fehler beheben.
  </p>

  <h3 id="terminate">7.8 Der Terminate-Schalter</h3>

  <p>Es kann vorkommen, dass unser Programm auf einmal nicht mehr
    läuft und in einer Endlosschleife gefangen ist, je nachdem mit welchen
    Werten wir beispielsweise eine Schleife betreten.</p>

  <p>Was tun?</p>

  <p>
    Als durchschnittlicher Nutzer wäre die Frage ganz einfach zu
    beantworten: ich klicke auf den roten <em>Terminate</em>-Schalter, der
    das Programm sofort beendet. Es ist zwar ein Shortcut zum Auslösen der
    <em>Terminate</em>-Funktion voreingestellt, allerdings ist dieser dem
    Debug-Modus vorbehalten.
  </p>

  <p>Statt Eclipse jedesmal zu schließen, wenn sich Ihr Programm
    nicht wie vorgesehen beenden lässt, lernen Sie nun einen Weg kennen,
    wie Sie Ihr Programm in der IDE terminieren können.</p>

  <p>Lassen Sie uns zuerst dafür sorgen, dass unser kleines
    Hello-World-Programm endlos durchläuft.</p>

  <p>
    Springen Sie in die letzte Zeile Ihrer main-Methode der Klasse Main.
    Nutzen Sie hierfür den Weg über die Ansicht der <em>Outline</em>. Die
    <em>Outline</em>-View zeigt Ihnen das Gerüst der aktuellen Klasse an,
    mit all ihren Variablen und Methoden. Der Shortcut, um in die <em>Outline</em>
    zu gelangen, ist
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>O</code>
    . Wir nutzen nun allerdings nicht die <em>Outline</em>-View, sondern
    die <em>Quick Outline</em>, welche Sie mit
    <code>CTRL</code>
    +
    <code>O</code>
    öffnen. Dadurch erscheint ein Fenster mit der <em>Outline</em> der
    aktuellen Klasse als Listenansicht. Diese liegt als neue Ebene über
    dem Editor-Fenster und schließt sich nach Ausführen der gewünschten
    Aktion von selbst. Suchen Sie die main-Methode aus dieser Liste heraus
    und bestätigen Sie Ihre Auswahl. Der Fokus liegt nun auf Ihrer
    main-Methode, hinter deren Namen. Um schnell an das Ende der Methode
    zu gelangen, kann es nützlich sein, erst eine Zeile nach unten zu gehen
    und dann <em>Go to matching bracket</em> mit
    <code>SHIFT</code>
    +
    <code>CTRL</code>
    +
    <code>P</code>
    direkt hinter die schließende Klammer der Methode zu springen. Mit
    <code>ALT</code>
    +
    <code>↓</code>
    verschieben Sie einfach die schließende Klammer der Methode eine Zeile
    nach unten und haben darüber Platz für Ihre Endlosschleife. Sie können
    auch einfach eine Zeile höher gehen und
    <code>ENTER</code>
    drücken. Wie Sie die benötigte Zeile einfügen, bleibt ganz Ihrer
    Vorliebe überlassen. Erweitern Sie nun die main-Methode um eine
    Endlosschleife.
  </p>

  <p>Eine mögliche Syntax ist:</p>
  <pre>
  <code>while (true) {
    System.out.println("La la la!");
}
</code>
  </pre>

  <p>
    Wenn Sie nun mit
    <code>F11</code>
    ihr Programm starten, wird dieses sich nicht von alleine beenden. Im
    Normalfall wundern Sie sich vielleicht, warum Ihr Programm nicht die
    gewünschte Ausgabe erzeugt, Sie werden sich aber nicht sofort bewusst
    sein, dass Sie sich in einer Endlosschleife befinden. Springen Sie in
    die <em>Console</em> (
    <code>ALT</code>
    +
    <code>SHIFT</code>
    +
    <code>Q</code>
    ,
    <code>C</code>
    ), um die Ausgabe Ihrer Applikation zu überprüfen. Ihr Screenreader
    sollte nun ununterbrochen "La la la!", verlauten lassen. Eine
    Navigation durch die Ausgaben der Console ist nur schwer möglich, da
    diese fortlaufend aktualisiert wird.
  </p>

  <p>
    Da Sie sich bereits mit dem Fokus in der <em>Console</em> befinden,
    reicht es aus, die Kontextmenü-Taste zu betätigen, um eine
    Strukturansicht aufzurufen. Wählen Sie aus der Liste <em>Terminate/Disconnect
      All</em>.
  </p>

  <p>Sie haben Ihr Programm beendet, ohne
    dabei die Eclipse IDE beenden zu müssen.</p>

  <p>
    Leider können Sie den Erfolg dieser Aktion nur schwer verifizieren.
    Eine Möglichkeit, dies zu tun, wäre zum Beispiel zu versuchen, an das
    Ende der Ausgabe in der <em>Console</em> zu navigieren. Hat die
    Ausgabe ein Ende, ist auch Ihr Programm erfolgreich beendet worden, es
    sei denn Sie befinden sich in einer Endlosschleife ohne Ausgabe.
  </p>

  <p>
    Überzeugender ist der erneute Weg über das Kontext-Menü der <em>Console</em>.
    Wenn die Option <em>Remove All Terminated</em> akustisch als nicht
    verfügbar gekennzeichnet ist, gibt es keine terminierte Session. Somit
    können Sie davon ausgehen, dass kein Programm beendet wurde. Sollte
    Ihr Programm noch laufen, steht Ihnen die Option <em>Terminate/Disconnect
      All</em> zur Verfügung. Wählen Sie diese aus und versuchen Sie danach
    erneut <em>Remove All Terminated</em> auszuwählen, um sicherzustellen, dass das
    Programm beendet wurde und die Ausgaben in der <em>Console</em>
    gelöscht sind.
  </p>