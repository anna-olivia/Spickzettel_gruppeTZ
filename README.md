# HTML und CSS Spickzettel 💻🤓💡

## Allgemein

[HTML](#1-html-die-websprache-für-das-gerüst-einer-website) und [CSS](#2-css-die-websprache-für-die-gestaltung-einer-website) sind Websprachen. Sie werden von Webentwickler*innen genutzt, um über den Webbrowser Webauftritte überhaupt erstmal anzeigen zu lassen.  Sobald wir HTML und CSS verwenden, kommunizieren wir mit dem Webbrowser. Wir kommunizieren über Code mit dem Webbrowser, der wiederum den Code den Nutzern unserer Website "übersetzt". Nutzer können sich über eine statische Website über bestimmte Themen informieren. Sobald Nutzer mit der Website (auch oft dann WebApp) interagieren, kommt die Skriptsprache [JavaScript](#3-js-die-websprache-für-die-dynamik-einer-website) hinzu. Alle drei Websprachen zusammen werden im **Frontend** – der Aufgabenbereich, der sich auf die Benutzeroberfläche konzentriert – genutzt. 

<br>

![Websprachen und ihre Aufgaben](./assets/HTML_CSS_JS.png) *Abb.: Websprachen und ihre Aufgaben*


<br><br>
1. [HTML-Elemente](#html-elemente)
  - [Grundstruktur](#grundstruktur-einer-html-seite)
    - [Head-Elemente](#head-elemente-erscheinen-nicht-auf-der-seite-sondern-nur-infos-für-den-browser-und-google)
    - [Body-Elemente](#body-elemente-der-sichtbare-bereich-eurer-webseite)
        - [Block Elemente](#block-elemente-nehmen-die-gesamte-breite-des-elternelements-ein)
        - [Inline Elemente](#inline-elemente-nehmen-nur-die-breite-ihres-inhalts)

2. [CSS-Eigenschaften](#css-eigenschaften)
    - [Textformatierung](#textformatierung)
    - [Größen](#größen)
    - [Hintergrund](#hintergrund)
3. [JavaScript](#3-js-die-websprache-für-die-dynamik-einer-website)

4. [nützliche Tastenkombinationen](#4-nützliche-tastenkombinationen)


<br><br><br>


## 1. HTML die Websprache für das Gerüst einer Website

## HTML-Elemente
**HTML** steht für ***Hypertext Markup Language*** und ist eine Auszeichnungssprache, die verwendet wird, um den Inhalt einer Webseite zu strukturieren und zu kennzeichnen. HTML ist zuständig für die Markierung verschiedener Elemente wie Überschriften, Fließtexte, Bilder und Links, damit der Webbrowser die Elemente den Nutzern anzeigen und für weitere Zwecke nutzen kann. In der Regel sind HTML Elemente valide – also gültig – wenn sie ein sogenanntes **Start - und Endtag** aufweisen.

```
<p>Ich bin ein Text, der für den Webbrowser als Textabsatz (abgekürzt p) markiert wurde.</p>
```
``` 
<!-- Ich bin ein HTML Kommentar -->
 ```
---

> [!TIP]
> Start- und Endtag bestimmen den Anfang und das Ende der Markierung.

---
---

> [!TIP]
> nur wenn Texte, Bilder etc. richtig markiert wurden, können wir sie später färben, ausrichten, gestalten ohne Verfahrensfehler zu riskieren! 

---

> [!TIP]  
> Kommentare sind für uns Menschen wichtig damit wir Code in der Entwicklungsumgebung nachvollziehen können und Kolleg*innen und uns Hinweise zum Code zu geben. Kommentare werden im Browser nicht für die Nutzer angezeigt. 

<br><br><br>


### Grundstruktur einer HTML-Seite

| HTML-Element    | Beschreibung                                    | Beispiel                              |
|:---------------:|:-----------------------------------------------:|:-------------------------------------:|
| `<!DOCTYPE html>`| Definiert den Dokumenttyp und die HTML-Version  | `<!DOCTYPE html>`                     |
| `<html>`        | Wurzelelement einer HTML-Seite                  | `<html>...</html>`                    |
| `<head>`        | Enthält Metadaten und Links zu Stylesheets etc. | `<head>...</head>`                    |
| `<body>`        | Enthält den für Nutzer sichtbaren Inhalt der Webseite      | `<body>...</body>`                    |
<br>

**Beispiel**

```
<!DOCTYPE html>
<html>
    <head>...</head>
    <body>...</body>
</html>
```
<br>

> [!TIP]
> `<head>`und `<body>` befinden sich innerhalb des `<html>` Wurzel Elements - diese Elemente sind also in Wurzelelement verschachtelt oder anders gesagt, liegen zwischen **Start- und Endtag** des `<html>`Elements.

<br><br><br>

### Head-Elemente (erscheinen nicht auf der Seite, sondern nur Infos für den Browser und Google)

| HTML-Element | Beschreibung                                           | Beispiel                                 |
|:------------:|:------------------------------------------------------:|:----------------------------------------:|
| `<title>`    | Titel der Webseite, erscheint in der Browser-Tab-Leiste | `<title>Meine Webseite</title>`          |
| `<meta>`     | Metainformationen, z.B. Zeichensatz oder Keywords       | `<meta charset="UTF-8">`                 |
| `<link>`     | Verknüpfung mit externen Dateien, z.B. CSS-Stylesheets  | `<link rel="stylesheet" href="style.css">`|

<br><br><br>

### Body-Elemente (der sichtbare Bereich eurer Webseite)
    
| HTML-Element  | Beschreibung                               | Beispiel                             |
|:-------------:|:------------------------------------------:|:------------------------------------:|
| `<h1>`...`<h6>` | Überschriften                            | `<h1>Überschrift</h1>`               |
| `<p>`          | Textabsatz                                | `<p>Textabsatz</p>`                  |
| `<a>`        | Hyperlink (intern, extern)      | `<a href="./unterseite.html"> Dies ist der klickbare Linktext </a>`<br>`<a href="url"> Die ist der klickbare Linktext</a>`|
| `<img>`      | Bild einfügen                                 | `<img src="./bilder/meinBild.jpg" alt="Bildbeschreibung">`  |
| `<ul>`         | Ungeordnete Liste                         | `<ul><li>Element</li></ul>`          |
| `<ol>`         | Geordnete Liste                           | `<ol><li>Erstes Element</li></ol>`   |
| `<li>`         | Listenelement                             | `<li>Listeneintrag</li>`             |

#### HTML Attribute

Einige HTML Elemente brauchen notwendigerweise Zusatzinformationen, um zu funktionieren. Diese Zusatzinformationen müssen wir mit einem sogenannten Schlüssel-Wert Paar im Starttag des jeweiligen HTML Elements angeben. 

| HTML-Attribut  | Beschreibung                               | Beispiel                             |
|:-------------:|:------------------------------------------:|:------------------------------------:|
| `href` | Schlüssel des Attributs                            | `<a href="./kontakt.html">Zur Kontaktseite</a>`|
| `"./kontakt.html"` | Wert des Attributs(hier Strukturpfad/Wegbeschreibung zum gewünschten Zieldokument)|`<a href="./kontakt.html">Zur Kontaktseite</a>`|



#### Block-Elemente (nehmen die gesamte Breite des Elternelements ein)

| HTML-Element  | Beschreibung                               | Beispiel                             |
|:-------------:|:------------------------------------------:|:------------------------------------:|
| `<h1>`...`<h6>` | Überschriften                            | `<h1>Überschrift</h1>`               |
| `<p>`          | Textabsatz                                | `<p>Textabsatz</p>`                  |
| `<ul>`         | Ungeordnete Liste                         | `<ul><li>Element</li></ul>`          |
| `<ol>`         | Geordnete Liste                           | `<ol><li>Erstes Element</li></ol>`   |
| `<li>`         | Listenelement                             | `<li>Listeneintrag</li>`             |
| `<div>`        | generisches Containerelement                          | `<div>Inhalt</div>`                  |
<br>

##### semantische Containerelemente:

| HTML-Element  | Beschreibung                               | Beispiel                             |
|:-------------:|:------------------------------------------:|:------------------------------------:|
| `<header>`    | Definiert den Kopfbereich eines Dokuments oder einer Sektion. | `<header>Kopfbereich</header>`       |
| `<main>`      | Hauptinhalt des Dokuments, sollte einzigartig sein. | `<main>Hauptinhalt</main>`           |
| `<footer>`    | Definiert den Fußbereich eines Dokuments oder einer Sektion. | `<footer>Fußbereich</footer>`        |
| `<section>`   | Thematisch zusammenhängender Bereich eines Dokuments. | `<section>Abschnitt</section>`       |
| `<nav>`       | Definiert eine Gruppe von Navigationslinks. | `<nav>Navigation</nav>`              |
| `<article>`   | Unabhängiger Artikel, der in sich geschlossen ist. | `<article>Artikel</article>`         |

<br><br>

> [!TIP]
> Ein generisches HTML Element kann als Inhalt alle möglichen anderen Elemente verschachteln ohne spezifisch zu werden. Semantische HTML Elemente definieren ihren Inhalt sehr konkret, so sollte man nicht einen Fließtext mit einem `nav` Element markieren. 

> [!important]
> Je sorgfältiger man von Anfang arbeiten, desto weniger Vorgangsfehler entstehen in der weiteren Entwicklung einer Website.


<br><br><br>
   
#### Inline Elemente (nehmen nur die Breite ihres Inhalts)

| HTML-Element | Beschreibung                    | Beispiel                              |
|:------------:|:-------------------------------:|:-------------------------------------:|
| `<a>`        | Hyperlink (intern, extern)      | `<a href="./unterseite.html"> Dies ist der klickbare Linktext </a>` <br>  `<a href="url"> Die ist der klickbare Linktext. </a>`           |
| `<span>`       | Element, das ausgewählten Bereich makiert  | `<p> Dies ist ein Textabsatz und innerhalb dieses Fließtextes kann ich bestimmte <span>Bereiche</span> zusätlich makieren.</p>`         |
| `<img>`      | Bild einfügen                                 | `<img src="./bilder/meinBild.jpg" alt="Bildbeschreibung">`  |

  
<!--
## 2. CSS die Websprache für die Gestaltung einer Website
<br><br><br>
## CSS-Eigenschaften
**CSS** steht für ***Cascading Style Sheets*** und wird verwendet, um das Aussehen von HTML-Elementen auf einer Webseite zu definieren. Mit CSS können verschiedene Eigenschaften wie Farbe, Schriftart und Positionierung definiert werden. Durch die Trennung von Inhalt und Design wird das Ändern des Aussehens der Webseite einfacher, da nur das CSS geändert werden muss, ohne den HTML-Code zu bearbeiten.

## Selektoren
| Selektor              | Beschreibung                                          | Beispiel                            |
|-----------------------|-------------------------------------------------------|-------------------------------------|
| Elementselektor       | Wählt alle Elemente eines bestimmten Typs aus.        | `p { color: blue; }`                |
| Klassen-Selektor      | Wählt alle Elemente mit einer bestimmten Klasse aus.  | `.classname { color: red; }`        |
| Nachfahren-Selektor   | Wählt alle Elemente innerhalb eines bestimmten Elternteils aus. | `div p { color: green; }`          |
| `:hover`              | Pseudoklasse für den Hover-Zustand eines Elements.    | `a:hover { color: red; }`           |



### Textformatierung
| Eigenschaft       | Beschreibung                                   | Beispiel                        |
|-------------------|------------------------------------------------|---------------------------------|
| `color`           | Setzt die Textfarbe.                           | `color: blue;`                  |
| `font-size`       | Bestimmt die Schriftgröße.                     | `font-size: 16px;`              |
| `text-decoration` | Fügt Dekorationen wie Unterstreichungen hinzu. | `text-decoration: underline;`   |
| `font-weight`     | Definiert die Dicke der Schrift.               | `font-weight: bold;`            |
| `font-family`     | Bestimmt die Schriftart.                       | `font-family: Arial, sans-serif;`|
| `font-style`      | Legt den Stil der Schrift fest (z.B. kursiv).  | `font-style: italic;`           |


### Größen, Abstände und Rahmen (Boxmodel)
| Eigenschaft | Beschreibung                            | Beispiel              |
|-------------|-----------------------------------------|-----------------------|
| `width`     | Setzt die Breite eines Elements.        | `width: 100px;`       |
| `height`    | Bestimmt die Höhe eines Elements.       | `height: 200px;`      |
| `margin`    | Bestimmt den Außenabstand eines Elements. | `margin: 20px;`       |
| `padding`   | Setzt den Innenabstand eines Elements.  | `padding: 15px;`      |
| `border`    | Definiert die Rahmenlinie eines Elements. | `border: 1px solid black;` |

## Hintergrund
| Eigenschaft           | Beschreibung                                          | Beispiel                            |
|-----------------------|-------------------------------------------------------|-------------------------------------|
| `background-color`    | Legt die Hintergrundfarbe fest.                       | `background-color: yellow;`         |
| `background-size`     | Bestimmt die Größe des Hintergrundbildes.             | `background-size: cover;`           |
| `background-repeat`   | Legt fest, ob und wie das Hintergrundbild wiederholt wird. | `background-repeat: no-repeat;`     |
| `background-position` | Definiert die Position des Hintergrundbildes.         | `background-position: center;`      |
| `background-attachment` | Legt fest, ob das Hintergrundbild scrollt oder fixiert ist. | `background-attachment: fixed;` |


## Flex (erste Schritte)
| Eigenschaft      | Beschreibung                                            | Beispiel                        |
|------------------|---------------------------------------------------------|---------------------------------|
| `display`        | Legt den flexiblen Container fest und stellt so Kinder nebeneinander.    (Achtung: display wird nicht nur für flex verwendet!)                   | `display: flex;`                |
| `justify-content`| Bestimmt die Ausrichtung der flexiblen Elemente entlang der Hauptachse. (hier horizontal) | `justify-content: center;`      |
| `align-items`    | Bestimmt die Ausrichtung der flexiblen Elemente entlang der Querachse. (hier: vertikal) | `align-items: center;`          |
| `gap`            | Legt den Abstand zwischen den flexiblen Elementen fest. | `gap: 10px;`                    |
| `flex-wrap`      | Bestimmt, ob die flexiblen Elemente in einer einzigen Zeile oder in mehreren Zeilen angezeigt werden. | `flex-wrap: wrap;`              |


## Erweiterte CSS-Effekte
| Eigenschaft           | Beschreibung                                          | Beispiel                            |
|-----------------------|-------------------------------------------------------|-------------------------------------|
| `transition`          | Definiert Übergangseffekte zwischen zwei Zuständen eines Elements. | `transition: all 0.3s ease;`       |
| `box-shadow`          | Fügt einem Element einen Schatten hinzu.              | `box-shadow: 0px 4px 8px rgba(0,0,0,0.3);` |




<br><br><br>



## 3. JS die Websprache für die Dynamik einer Website


-->

## 4. Nützliche Tastenkombinationen

Tastenkombinationen, die in **VS Code** und anderen Programmen funktionieren:

- Fenster wechseln = `Alt` + `Tab`
- Kopieren         = `STRG` + `c`
- Ausschneiden     = `STRG` + `x`
- Einfügen         = `STRG` + `v`
- rückgängig       = `Strg` + `z`
- Suchen           = `STRG` + `f`
- Speichern        = `STRG` + `s`
- alles markieren  = `STRG` + `a`

### VS-Code

Diese praktischen Kombinationen funktionieren nur in VS Code:
- `STRG`+ `#`          = erzeugt einen Kommentar 
- `!`+ `tab`          = erzeugt das HTML Grundgerüst (auch boilerplate genannt) 
- `p` + `tab`          = erzeugt ein HTML Textabsatz (wenn ihr h1 wählt erzeugt es eine h1 Überschrift etc.)


<!--

- `Alt` + `Pfeiltaste` = Zeilen verschieben, hoch/runter
- `Alt` + `z`          = Zeilenumbruch anschalten/ausschalten
- `STRG`+ `l`          = Zeile markieren


#### Emmet Abkürzungen in VS Code

Emmet sind Kurzformen, die VS Code zu Code umschreibt, hier einige kurze Beispiele für ***HTML***:
- `!`               = erzeugt in einen Boilerplate-Code (Grundstruktur)
- `lorem50`         = erzeugt einen Lorem-Text mit 50 Worten
- `div.box`         = erzeugt eine `<div class="box">`
- `ul>li*3`         = erzeugt eine `<ul>` mit 3 `<li>`Elementen
- `a{weiterlesen}`  = erzeugt ein `<a href="">weiterlesen</a>`
- `section>img+p+a` = erzeugt eine Sektion und darin ein `<img>`, `<p>`und ein `<a>`

> [!TIP]
> Ihr könnt diese Elemente miteinander kombinieren und damit sehr umfangreiche Codeblöcke bauen. Benutzt diese aber erst, wenn ihr euch mit eurem html sicher seid. Je länger eure Kombinationen sind, desto leichter könnt ihr Fehler produzieren und den Überblick verlieren. Es gibt diese Emmet Abkürzungen auch für CSS. Einen (sehr) umfangreichen Überblick über die verschiedenen Möglichkeiten findet ihr hier:
***[Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)***
