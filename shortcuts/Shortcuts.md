<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Hotkeys](#hotkeys)
  - [Datei und Projekt Management](#datei-und-projekt-management)
  - [Editor Fenster](#editor-fenster)
  - [Im Editor navigieren](#im-editor-navigieren)
  - [Text auswählen](#text-ausw%C3%A4hlen)
  - [Text editieren](#text-editieren)
  - [Suchen und Ersetzen](#suchen-und-ersetzen)
  - [Einrückungen und Kommentare](#einr%C3%BCckungen-und-kommentare)
  - [Quellcode editieren](#quellcode-editieren)
  - [Code-Informationen](#code-informationen)
  - [Refactoring](#refactoring)
  - [Run und Debug](#run-und-debug)
  - [Weitere Shortcuts](#weitere-shortcuts)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Hotkeys
Eclipse bietet mehr als 200 Hotkeys und Shortcuts an.
Mit der Tastenkombination

**`CTRL`+`SHIFT`+`L`**

wird eine Liste der Hotkeys fokussiert, durch welche mit Hilfe der Pfeiltasten, in Kombination mit dem Anfangsbuchstaben der gesuchten Aktion, navigiert werden kann.


## Datei und Projekt Management
|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`N`        | Neues Projekt, Datei, Klasse über das Wizard anlegen |
| `CTRL`+`ALT`+`N`      | Neues Projekt, Datei, Klasse etc. anlegen       |
| `ALT`+`F`, dann `.` | Öffne Projekt, Datei. etc.      |
| `CTRL`+`SHIFT`+`R` | Öffne Projekt, Datei. etc.      |
| `ALT`+`Enter` | Öffne Eigenschaften der Datei |
| `CTRL`+`S` | Speichern der aktuellen Datei |
| `CTRL`+`SHIFT`+`S` | Speichern aller Dateien |
| `CTRL`+`W` | Schließen der aktuellen Datei |
| `CTRL`+`SHIFT`+`W` | Schließen aller Dateien |
| `F5` | Aktualisieren des ausgewählten Elements mit Dateisystem  |

## Editor Fenster

Hierfür muss das Editor-Fenster fokussiert sein.

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `F12` | In den Editor springen | 
| `CTRL`+`M` | Fenster maximieren/minimieren |
| `CTRL`+`E` | Offene Editoren anzeigen |
| `CTRL`+`F6`/`CTRL`+`SHIFT`+`F6` | Offene Editoren anzeigen, Wechsel erfolgt sofort nach loslassen der Ctrl-Taste |
| `ALT`+`Pfeiltaste nach links`/`Pfeiltaste nach rechts` | Zum vorherigen/ nächsten Editorfenster wechseln |
| `ALT`+`-` | Öffne die Optionen des Editor-Fensters |
| `CTRL`+`F10` | View-Menü anzeigen (*Breakpoints*, *Bookmarks* etc.) |
| `CTRL`+`F10`, dann `N` | Zeilennummerierung anzeigen/ausblenden |
| `CTRL`+`SHIFT`+`Q` | Diff anzeigen/verbergen (Änderungen seit dem letzten Speichern) |
| `CTRL`+`SHIFT`+`+`/`-` | Rein-/Raus-Zoomen |

## Im Editor navigieren
 
|Shortcut       | Aktion        |
|:------------- |:-------------|
| `Home`/`End` | Springe zum Anfang/Ende einer Einrückung. Zweimal Home drücken um zum Zeilenanfang zu springen  |
| `CTRL`+`Home`/`End` | Springe zum Anfang/Ende der Quelle |
| `CTRL`+`Pfeiltaste nach links`/`Pfeiltaste nach rechts` | Ein Wort nach links/rechts springen |
| `CTRL`+`SHIFT`+`Pfeiltaste nach oben`/`Pfeiltaste nach unten`| Springe zur vorigen/nächsten Methode |
| `CTRL`+`L` | Springe zu Zeilennummer. Hier öffnet sich ein Formular |
| `CTRL`+`Q` | Springe zur zuletzt editierten Stelle. |
| `CTRL`+`.`/`CTRL`+`,` | Springe zur nächsten/vorigen Stelle mit Compilerfehler oder Warnung |
| `CTRL`+`SHIFT`+`P` | Springe zur dazugehörigen öffnenden/ schließenden Klammer, bei selektierter Klammer. |
| `CTRL`+`[`+`]`/`CTRL`+`*`auf Nummernpad | Ein- oder ausklappen aller Methoden/Klassen |
| `CTRL`+`[`/`]`/`CTRL`+`-`| Ein- oder ausklappen der ausgewählten Methode/Klasse |
| `CTRL`+`Pfeiltaste nach oben`/`Pfeiltaste nach unten` | Scrollen im Editor, ohne die Cursorposition zu verändern NTM: für Braille mit Cursor? |
| `ALT`+`BildPfeiltaste nach oben`/`BildPfeiltaste nach unten` | Nächster/Voriger Subtab |

## Text auswählen

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `SHIFT`+`Pfeiltaste nach links`/`Pfeiltaste nach rechts` | Erweitere Auswahl um einen Buchstaben nach links/rechts |
| `CTRL`+`SHIFT`+`Pfeiltaste nach links`/`Pfeiltaste nach rechts`  | Erweitere Auswahl um das vorige/nächste Wort |
| `SHIFT`+`End`/`Home` | Erweitere Auswahl um eine Zeile darunter/darüber |
| `CTRL`+`A` | Alles auswählen |
| `ALT`+`SHIFT`+`Pfeiltaste nach oben` | Erweitere Auswahl um das aktuelle Element (also einzeiliger Ausdruck oder gesamter Klammerinhalt) |
| `ALT`+`SHIFT`+`Pfeiltaste nach links`/`Pfeiltaste nach rechts` |  Erweitere Auswahl um das vorige/nächste Element |
| `ALT`+`SHIFT`+`Pfeiltaste nach unten` | Reduziere vorher ausgeklappte Auswahl um eine Stufe |


## Text editieren

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`C`/`X`/`V` | Kopieren, Ausschneiden, Einfügen |
| `CTRL`+`Z` | Ungeschehen machen der letzten Editierung |
| `CTRL`+`Y`| Ungeschehen machen aufheben |
| `CTRL`+`D` | Zeile löschen |
| `ALT`+`Pfeiltaste nach oben`/`Pfeiltaste nach unten` | Auswahl kopieren und nach oben oder unten verschieben |
| `CTRL`+`delete` | Lösche nächstes Wort |
| `CTRL`+`backspace` | Lösche voriges Wort |
| `insert` | Wechsel zwischen Überschreiben und Einfügen |
| `SHIFT`+`CTRL`+`Y`| Konvertiere Auswahl in Kleinbuchstaben |
| `SHIFT`+`CTRL`+`X` | Konvertiere Auswahl in Großbuchstaben |

## Suchen und Ersetzen

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`F` | Finden und Ersetzen (*Find/Replace*) |
| `CTRL`+`K`/`CTRL`+`SHIFT`+`K`| Finde vorige/ nächste Vorkommnis des Suchbegriffs. Schließen Sie vorher das *Find/Replace*-Fenster |
| `CTRL`+`H` | Durchsucht den *Workspace*. |
| `CTRL`+`J`/`CTRL`+`SHIFT`+`J` | Durchsucht den Teil der aktuellen Klasse vor/ nach der Cursorposition |

## Einrückungen und Kommentare

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `TAB` /`SHIFT`+`TAB` | Auswahl einrücken |
| `CTRL`+`I`| Einrückung der Auswahl korrigieren |
| `CTRL`+`SHIFT`+`F` | Auto-Formatierung |
| `CTRL`+`/` | Ein- oder Auskommentieren der Auswahl (fügt // am Zeilenanfang ein)|
| `CTRL`+`SHIFT`+`/` | Block-Kommentar einfügen (fügt /...*/ ein) |
| `CTRL`+`SHIFT`+`\` | Block-Kommentar entfernen |
| `ALT`+`SHIFT`+`J` | Element-Kommentar hinzufügen |

## Quellcode editieren

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`LEERTASTE` | Öffnet den Content-Assistenten, d.h. zeigt alle enthaltenen Methoden etc. an. |
| `CTRL`+ |  |
| `ALT`+`/` | Vorschläge zur Wortvervollständigung, nachdem mindestens ein Buchstabe eingegeben wurde. Solange Tastenkombination drücken, bis der korrekte Name erreicht wurde. |
| `CTRL`+`SHIFT`+`INSERT` | Aktiviert/Deaktiviert den *Smart Insert Mode* für automatische Einrückungen, Klammern etc. |

## Code-Informationen

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`O` | Outline/Struktur anzeigen |
| `F2` | Tooltip |
| `F3` | Springe zu Deklaration (Klasse, Methode oder Parameter) |
| `F4` | Typ-Hierarchie für ausgewähltes Element öffnen. |
| `CTRL`+`T` | Quick-Type-Hierarchie für Auswahl öffnen. |
| `CTRL`+`SHIFT`+`T` | Typ-Hierarchie öffnen. |
| `CTRL`+`ALT`+`H` | Aufruf-Hierarchie öffnen |
| `CTRL`+`SHIFT`+`U` | Finde Vorkommnisse des Ausdrucks in der aktuellen Datei. |
|  `CTRL`+ Maus-hover (JAWS Cursor) über Methode | Öffne Deklaration oder Implementierung der Methode |

## Refactoring

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `ALT`+`SHIFT`+`R` | Umbenennen des ausgewählten Elements mit all seinen Referenzen |
| `ALT`+`SHIFT`+`V`| Verschiebe ausgewähltes Element in eine andere Klasse oder eine andere Datei, selektieren Sie hierfür die komplette Methode oder Klasse |
| `ALT`+`SHIFT`+`C` | Methodensignatur ändern, selektieren Sie hierfür den Methodennamen |
| `ALT`+`SHIFT`+`M` | Auswahl in der Methode einfügen |
| `ALT`+`SHIFT`+`L` | Lokale Variable extrahieren, Variable von einem ausgewählten Ausdruck erstellen und zuweisen |
| `ALT`+`SHIFT`+`I` | 	Inline Auswahl der möglichen lokalen Variablen, Methodenoder Konstanten (Variablen mit ihrer Deklarations/ Zuweisung ersetzen und in den Ausdruck einfügen) |

## Run und Debug

|Shortcut       | Aktion        |
|:------------- |:-------------|
|`CTRL`+`F11`  | Programm speichern und ausführen. |
| `F11` | Programm im Debug-Modus starten, falls vorher ein *Breakpoint* gesetzt wurde.  |
| `F5` | *Step Into*, in Funktion gehen |
| `F6` | Nächste Zeile/ nächster Schritt |
| `F7` | *Step Out*, auf der Funktion gehen |
| `F8` | Springe zum nächsten *Breakpoint* |

## Weitere Shortcuts

|Shortcut       | Aktion        |
|:------------- |:-------------|
| `CTRL`+`F7`/`CTRL`+`SHIFT`+`F7`| Zwischen den Ansichten wechseln. Nützlich um zwischen *Package Explorer* und *Editor* zu wechseln.  |
|`ALT`+`SHIFT`+`Q`, `X` | In *Problems* springen |
|`ALT`+`SHIFT`+`Q`, `C` | In die *Console* springen |
|`ALT`+`SHIFT`+`Q`, `P` | In den *Package Explorer* springen |
|`Pfeiltaste nach rechts` | Ordner öffnen |
| `CTRL`+`F8`/`CTRL`+`SHIFT`+`F8` | Vorwärts/ Rückwärts durch *Perspectives* wechseln |
| `CTRL`+`P` | Drucken |
| `F1` | Öffnen der Hilfe |
| `SHIFT`+`F10` | Kontext-Menü anzeigen (`rechter Mausklick`)|
| `SHIFT`+`ALT`+`X`, `J` | Run as Java Application |


Quelle: [https://shortcutworld.com/en/Eclipse/win/all](https://shortcutworld.com/en/Eclipse/win/all)
Veröffentlicht unter der Creative Common Attribute License