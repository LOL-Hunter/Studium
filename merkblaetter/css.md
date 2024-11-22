# CSS
## Inhalt

Trennung von Struktur/Inhalt und Design

zuordnung über class Attribut in HTML

VuiewPort -> AnzeigeBereich

````css
Selektor {Eigenschaft:Wert1; ...}
````
Selektor indentifizerit ein oder mehrere Elemente in der HTML-Datei denen die Eigenschaft zugeordnet werden soll.
Keine Strings: Entweder Schlüssenwörter oder Zahlen mit Einheit: 20px (ohne leerzeichen 10 px!)
Mehrere Werte werden duch leerzeichen getrennt.
Mehrere Deklarationen werden durch ; getrennt.
Hersteller spez beginnen mit "-"


Es werden alle Regeln mit h1 berücksichtigt.
Es gilt der letzte wert. (color: red; color: blue;)

---
````css
@import "sub.css"
@import url "http...<url>.css"
````
Importieren anderer css Dateien. \
Dies muss IMMER zu Beginn passieren.

---
````css
@charset
@viewport 
@media
@page
````
Weitere @-Regeln.

---
````css
<link rel="stylesheet" href="<path>">
````
Einbinden einer css in ein HTML im Head.

---
````html
<h1>Heading1</h1>
<h2>Heading1</h2>
````

## Block / Inline - Elemente

## Positioning
static (default)
relative
absolute
fixed
z-index
(top, left, right, bottom)


## Selektoren

````css
01.  * { color: red; } // Universalselector 
02.  h1, h2 { color: red; }  // Typselector
03.  .testclass { color: red;} // class Selector
04.  #absatz { width: 100%;} // ID Selector
05.  [lang] {width: 100%;} // Attribut Selector
06.  [lang="de"] {width: 100%;} // Attribut Selector mit wert gleich x.
07.  :hover {color: red;} // Pseudoklasse (hover, visited, link, active, ...)
08.  div p {color: red;} // Nachfahrenselector 
09.  div > p {color: red;} // Kindselector
11.  div ~ p {color: red;} // Geschwisterselector
12.  div + p {color: red;} // Nachbarselector

:: Pseudoelement

h1.rot {color: red;} // Kombination von class und Typ
h1#rot {color: red;} // Kombination von id und Typ
````
* Gültig für alle Elemente im Dokument.
* Gültig für alle Elemente mit folgendem HTML-Tag.
* Gültig für alle Elemente die folgende class haben.
* Gültig für das Element mit foldenger id.
* Gültig für alle Elemente mit folgendem Attribut haben.
* Gültig für alle angegebenen Elemente auf einem Event x.
* Gültig für alle Elemente a die in b enthalten sind.
---
````html
<div class="testclass">Heading1</div>
````
````css

````
Ansprechen der Elemente über class. \
Klassenzugehörigkeit oder Gruppenselektor.

---
````html
<p id="absatz">Paragraph1</p>
````
````css
#absatz {
    width: 100%;
    height: 80px;
}
````
Ansprechen der Elemente über die id. \
Einmalig.


## Spezifität
und oder
## Kaskadierung

## Besondere Eigenschaften

#### Farben

````css
color: red;
color: #8080000;
color: rgb(12, 23, 255);
````
#### Pixel
````html
margin-left: 20px; // WICHTIG zwischen einheit und zahl KEIN Leerzeichen.
margin-left: 50%; // Angabe in Prozent
margin-left: 1em; // 1em // 100% vom elternelement
margin-left: 1vw; // viewport Width 1vw = 1% des anzeigebereichs
margin-left: 1vh; // viewport Height
````


---
## Elemente

````html
<div class="container"></div>
````
````css
.container {
    display: flex;
    flex-direcion: row;
}
````
Flexboxen

---