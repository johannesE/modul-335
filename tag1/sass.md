# SASS
[Link zur offiziellen SASS-Website](http://sass-lang.com/guide)

## Preprocessors

CSS alleine kann Spass machen. Stylesheets werden aber immer grösser, komplexer und schwieriger zu Warten. Hier können dir Preprocessoren helfen. SASS bietet dir Funktionen die es so in CSS nicht gibt:

* Variablen \(variables\)
* Verschachtelung \(nesting\)
* Operatoren
* Mixins, Extend, usw.

Ein Preprocessor nimmt deine SASS-Datei und wandelt Sie in eine herkömliche CSS-Datei um. Denn dein Browser versteht nur CSS, kein SASS.  
Es gibt diverse Programme die dir diese Umwandlung abnehmen, egal ob Terminal, Programm oder in Ionic direkt - die Idee bleibt die gleiche. Im Beispiel unten ist zu sehen, dass SASS Tabulatoren verwendet, SCSS jedoch Klammern. In der Fachliteratur wird daher oft SASS synonym mit SCSS beschrieben. 

_Codebeispiel:_
![](https://futurestud.io/blog/content/images/2014/Jun/sass-vs-scss.png)


## Variablen

Du kannst ganz einfach Variablen in Sass definieren. Oft werden Variablen für Grössen oder Farben verwendet.

```html
<div class="wrapper">
  <h1>Variablen</h1>
  <h2>Ich liebe diese verschiedene Farben!</h2>
</div>
```
```css
// SCSS: Variablen
// ----
$farbe-blau: #34495E;
$farbe-rot: #E74C3C;
$farbe-gruen: #2ECC71;
$groesse: 20px;

$hintergrund: $farbe-blau;

.wrapper {
  background: $hintergrund;
}
h1 { 
  font-style: italic;
  color: $farbe-rot;
}
h2 {
  font-size: $groesse;
  color: $farbe-gruen;
}
```
wird zu CSS
```css
.wrapper {
  background: #34495E;
}

h1 {
  font-style: italic;
  color: #E74C3C;
}

h2 {
  font-size: 20px;
  color: #2ECC71;
}

```
[Auf Sassmeister ansehen](http://www.sassmeister.com/gist/e4a777cd959c035502658c0bded5f66b)




## Nesting
Bei der Verschachtelung kann man sich einiges an Platz sparen und wie im HTML DOM die effektive Struktur der Seite stylen.
```html
<h1>Ausserhalb eines DIV</h1>
<div class="wrapper">
  <h1>In einem DIV</h1>
</div>
```

```css
// SCSS: Nesting
// ----
h1 { 
  color: red; 
}

.wrapper {
  h1 { 
  font-style: italic;
  color: black;
  }
}
```

Wird zu folgendem CSS:
```css
h1 {
  color: red;
}

.wrapper h1 {
  font-style: italic;
  color: black;
}

```

[Auf Sassmeister ansehen](http://www.sassmeister.com/gist/2fdb11998adcf5b390d053c006d56e11)


## Operatoren
Operatoren sind eine ziemlich nützliche Sache.

```html
<h1>Dies ist eine Box die durch Operatoren 15x grösser ist:</h1>
<div class="box">
</div>
```

Die SCSS-Datei
```sass
// SCSS: Operatoren
// ----
$faktor:15;
h1 { 
  color: black; 
}

.box {
  background: red;
  height: 20px;
  width: 10px * $faktor;
}
```

wird zur CSS-Datei:

```css
h1 {
  color: black;
}

.box {
  background: red;
  height: 20px;
  width: 150px;
}
```

[Auf Sassmeister ansehen](http://www.sassmeister.com/gist/855910db908128842a9eb6936d7516be)

## SCSS in Ionic
Ionic setzt voll und ganz auf SCSS. Du kannst so deine App bis ins letzte Detail stylen. Dazu wurde in der Doku ein eigenes Kapitel gewidmet:
https://ionicframework.com/docs/theming/theming-your-app/

Etwas für die Lachmuskeln:
{% youtube %}https://www.youtube.com/watch?v=1cgr0z9TXnQ {% endyoutube %}
















