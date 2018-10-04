# JavaScript specific exercises

> Exercises for JavaScript, may be duplicates from `exercises/general.md`. This document is not cleaned up and can sometimes be hard to read. This is not complete and will be filled with more exercises.

## Reading Comprehension

### Övning 1
> Vilka datatyper är följande uttryck? Varje ny rad är kommer visa en ny datatyp. Tips: använd typeof för att kontrollera ditt svar 

Exempelvis kan man svara att första uppgiften är datatypen `Number` och har värdet `1,01`. Se till att du förstår varför resultatet blir som det blir.

```js
1.01
true + true + false
'false'
5 && 8
5 || 8
!5
1 / 0
!!5
false || true
true && false || false && true
"123" - 0
typeof (typeof true)
"1000" / 10
123.4 - ''
2 < 3
'5' + "0" / '2'
'två' < 'tre'
'5' + "0" / '5' + 0
17 === 17.0
'1' + '5' - '4' * '2' - '3'
17 === '17'
'kalle' - 5
17.000000000000000000001 == 17
undefined || null || 0 || false || "foo"
```

### Övning 2

Vilket värde kommer variabeln `z` att ha efter att respektive kodrad har körts? Skriv ut vad `z` är på varje rad utan att köra koden.
```js
let z = 5;
z++;
--z;
z += 15;
let x = 8;
let y = 16;
z = y - x;
x = 10;
z = x++;
x = 2;
y = 5; 
x = x + y; 
y = x + y;
z = y;
```

### Övning 3
> Förklara i text hur funktionen nedan körs när vi kallar på den(dvs. i vilken ordning allt händer) i dessa scenarion:
 
* a) Vi kallar på funktionen med: `multiply(2, 2, 2);`
* b) Vi kallar på funktionen med: `multiply(2, 2);`
* c) Vi kallar på funktionen med: `multiply(2, 2, "2");`
* d) Vi kallar på funktionen med: `multiply(2, 2, function(){ return 2;});`

```javascript
function multiply(a, b, c){
    return a * b * c;
}
```

### Övning 4 

I koden ovan, vilka värden är parametrar och vilka värden är argument? Hur skiljer de sig åt och i vilket scope är parametrarna tillgängliga?

### Övning 5

Förklara i text hur denna funktion kommer att köras och vad som kommer att hända på varje rad: 

```js
const text = "Do not call me!";
function callMe(){
    const text = "Call me!";
    return text;
    console.log(text);
}

callMe();
```

### Övning 6
> Vad skriver följande kodrader ut?

__a)__
```js
function foo() {
  console.log("test");
}
foo("hej");
```

---

__b)__
```js
let a = foo(3);
console.log(a);
function foo(i) {
  return i * i;
}
```

---

__c)__
```js
console.log(foo(3, 5));
function foo(x, y) {
  return x * y;
}
```

---

__d)__
```js
console.log(foo(3, 5));
const foo = function(x, y) {
  return x * y;
}
```

---

__e)__
```js
let x = 2;
let y = 3
let a = foo(foo(x) + foo(y));
console.log(a);
function foo(i) {
  return 5 * i;
}
```
 
---

__f)__
```js
const person = {
    name: "Steffe",
    sayName(){
        console.log(this.name);
    }
}
person.sayName();
```

---

__g)__
```js
const person = {
    name: "Steffe",
}

function sayName(){
    console.log(this.name);
}
person.sayName = sayName;
person.sayName();
```

---

__h)__
```js
const animals = ["dog", "cat", "zebra", "horse", "cow"];
animals.shift();
console.log(`My favourite animal is ${animals[0]}`);
```

---

__i)__

```js
let a = 5;
function foo(a) {
  a++;
}
a += 2;
console.log(a);
```

---

__j)__
```js
function foo(a) {
  return a + 2;
};
function goo(x, y) {
  return x(y);
};
let a = goo(foo, 3);
console.log(a);
```

---

__k)__

```js
var text = "";
var a = {
    value: "c"
};
var b = {
    value: "a"
};
var c = {
    value: "b"
};
text = a.value + b.value + c.value;
console.log(text);
```

---

__l)__
```js
const a = 0;
const objekt = {
    a: 100,
    b: 200,
    c: 300
};
for(const value in objekt){
    a += value;
}

console.log(a);
```

---

__m)__
```js
function foo () {
  //Här returneras bar() innan funktionen har deklarerats
  return bar();
  //Dock så hoistas bar() upp ovanför return vilket gör att funktionen ändå 
  //kallas på eftersom här blir funktionen deklarerad innan return p.g.a hoist
  function bar() {
    return "FOOBAR!!";
  }
}
console.log(foo());
```


## DOM & Events
### Skapa element med JavaScript

Utgå från denna HTML och följ sedan instruktionerna nedan.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JavaScript</title>
</head>
<body>
   
<script src="main.js"></script> 
</body>
</html>
```

1. Skapa ett nytt element av typen `<div>` på sidan med hjälp av `document.createElement()` och spara det elementet i en ny variabel.
2. Skapa ett nytt element av typen `<p>` med hjälp av `document.createTextNode()` och spara det elementet i en ny variabel.
3. Skapa en ny textnod med `document.createTextNode()` med innehållet *"Satan va kul JavaScript är!"*. 
4. Lägg till textnoden som ett child av ditt `<p>`-elementet med `element.appendChild(TextNode)`. 
5. Lägg sedan till `<p>`-elementet som ett child av `<div>`-elementet som du skapade tidigare med `appendChild`.
6. Lägg sedan till `<div>`-elementet i `<body>` med `appendChild`. 

Du borde nu ha en liknande struktur i din HTML när du laddar om sidan:
```html
<body>
    <div>
        <p>Satan va kul JavaScript är!</p>
    </div>
</body>
```

7. Lägg till ett `id` av `text` på `<p>`-elementet.
8. Hämta ut `<p>`-elementet från sidan genom att använda `document.getElementById()`. Alltså hämta elementet via dess id.
10. Ändra färgen på `<p>`-taggen genom att använda `p.style.color`. Ändra t.ex. till en röd färg. 

### `innerHTML`

Ett mer risky men snabbare sätt att lägga till samma information är med funktionen `.innerHTML`. Med `.innerHTML` byter du ut hela innehållet i elementet istället för att lägga till nya barn som tidigare. Du lägger helt enkelt in en sträng som innehåller all HTML du vill lägga till.

```js
const output = document.getElementById('output');
output.innerHTML = "<p>Adding text node and element node at the same time</p>";
```

1. Skriv om koden som du gjorde tidigare så att den istället använder `.innerHTML` och lägger till samma information.

### Om mig!

```html
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8" />
  <title>This is me!</title>
  <style type="text/css">
      .list-item {
        background-color: #666;
        color: white;;
      }
  </style>
</head>
<body>
  <h1>Facts about me</h1>
  <ul>
    <li>Nickname: <span id="nickname"></span>
    <li>Favorite food:  <span id="favoriteFood"></span>
    <li>Hometown: <span id="hometown"></span>
    <li></li>
   </ul>
  <!-- script goes here -->
 </body>
</html>
```

1. Lägg till ett script längst ner så att du kan skriva JavaScript.
2. Med JavaScript, ändra så att sidan har `font-family`: "Comic Sans";
3. Med JavaScript, ersätt varje `<span>` med din egen information
4. Loopa igenom alla `<li>`-element och lägg till klassen `.list-item` på varje `<li>`.
5. Ändra så att bara varannat list item har en annan klass.
5. Skapa en `<img>`-tagg med en bild på dig själv och lägg till den på sidan.

### Boklistan

Du ska skapa en lista helt med JavaScript som listar upp en samling böcker. I listan ska man även kunna se vilka böcker som du har läst eller inte.

1. Skapa en `index.html` med en header i där det står "Min boklista",
2. Länka in ett script i botten av `body` där din kod ska ligga.
3. Använd denna array av objekt och loopa igenom den. Det kan vara en bra idé att bara använda `console.log` till en början för att se hur du får ut innehållet. Tänk på att värden och egenskaper som ligger inuti kommer vi åt genom att skriva `objectToAccess.propertyToAcces`.
```js
const books = [
  {
    title: 'The Design of EveryDay Things',
    author: 'Don Norman',
    isRead: true
  },
  {
    title: 'Darling River',
    author: 'Sara Stridsberg',
    isRead: true
  },
  {
    title: 'A book',
    author: 'Unknown',
    isRead: false
  }
];
```

4. Loopa igenom varje objekt i arrayen. För varje bok, skapa ett `<p>`-element med bokens title och författare och lägg till `<p>`-taggen på sidan (`appendChild`)
5. Gör om listan så att den använder `<ul>` och `<li>` istället för bara `<p>`-taggar.
6. Lägg till en egenskap till varje bok (efter `isRead`) som heter `url` där du lägger till en länk i form av en `string`. Gör så att denna bild visas på sidan under varje bok genom att skapa en `<img>`-tagg och sätta `src`.
7. Ändra textfärgen/bakgrundsfärgen baserat på om boken är läst eller inte när du skriver ut alla böcker.

### Get the element!

Du har följande HTML & JavaScript att arbeta med. Du får inte ändra i HTMLen och du får inte hämta flera element. Du ska bara använda `childElement`, `childNodes`, `parentElement`, `parentNode`, `nextSibling`, `previousSibling` etc. för att lösa uppgifterna. Du får alltså **bara** jobba utifrån variabeln `article` och sedan ändra innehållet utifrån den.

```html
<!-- Put this inside index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>MF DOM</title>
</head>
<body>
    <h1>Welcome to my DOM!</h1>
    <main>
        <article id="first">
            <h2>I am a second heading</h2>
            <p>So semantic lorum ipsi tipsi</p>     
            <img src="" alt=""/>      
        </article>
        <article>
            <h2>New blog post!</h2>
            <p>My DOM!</p>
        </article>
    </main>
</body>
</html>
```

```js
//Put this in your main.js then work from there
const article = document.getElementsById('first');
//to change h2 for example
article.firstElementChild.innerText = "I've changed!";

```

1. Ändra titeln på `<h2>` inuti `article`.
2. Lägg till en `alt`-beskrivning på `<img>`-elementet inuti `article`.
3. Ta bort `<p>`-taggen inuti `article`.
4. Ändra texten inuti `<h1>`.
5. Ändra titeln på den andra artikeln
6. Lägg till en bild med `src` samt `alt` på den andra artikeln
7. Lägg till ett `<span>` med texten `"I'm special"` i båda `<p>`-elementen på sidan.
8. Lägg till styling på båda `<span>`-elementen så att de har en annan färg än `<p>`-elementen.

### Add and remove element

```html
<!--Create a button that will be bound to the event listener -->
<button id="myButton">Min knapp</button>
```

```js
//Get the button from the DOM
const button = document.getElementById("myButton");

//You can use the onlick on the element directly, onclick takes
//an anonymous function as argument, the code that you want to run
//should be inside the brackets {}
button.onclick(function(){
    alert('Hej');
})

//I ususally use `addEventListener` instead. I think it looks better 
//and you can also easily change the event that is being triggered,
//there is no differens between this one and the one above tho.
button.addEventListener('click', function(){
    alert('Hej!');
})
```

1. Använd `appendChild` för att lägga till en ny `<p>`-tagg på sidan med innehållet `"JavaScript is great"` varje gång du klickar på en knapp, knappen kan ha `id="addButton"`.
2. Skapa en till knapp med `id="sparkle"`, denna knapp ska göra så att alla paragrafer ändra färg till `lightcoral` när du trycker på knappen.
3. Skapa en tredje knapp med `id="removeButton"` som tar bort dina tidigare skapade `<p>`-taggar som innehåller `"JavaScript is great!"`. Ena knappen ska alltså lägga till texten och den andra knappen ska ta bort texten.

### Pizza calculator

1. Använd HTML-koden nedan för att bygga din `PizzaCalculator`. Du ska skriva in antalet personer som ni är i gruppen som ska beställa pizza. Sedan när du trycker på **Calculate Pizzas** så ska resultatet visas upp i `<div>`-en nedanför knappen. Din javascript ska alltså läsa in värdet som är i input-fältet, beräkna det nya värdet samt skriva ut det på sidan igen när du trycker på knappen.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Pizza Calculator</title>
</head>
<body>
    <main>
        <label for="numberOfPeople">Number of people</label>
        <input type="text" id="numberOfPeople" placeholder="Number of people"/>
        <button id="calculatePizzas">Calculate Pizzas</button>
        <div id="output"></div>
    </main>
</body>
</html>
```

2. Gör istället så att antalet pizzor beräknas utan att du trycker på knappen, direkt när en användare har skrivit in ett värde i rutan så uppdateras `<div>`-en med `output`. För detta kan man använda: 
```js
element.addEventListener('keyup', function(){
    //Listens to when a key is being released
});
```

### Toggle class

Det lättaste och effektivaste sättet att ändra stylingen på ett element är genom att lägga till och ta bort en klass. Detta gör man med funktionen `classList`.

```html
<html>
<head>
    <meta charset="UTF-8">
    <title>classList</title>
    <style type="text/css">
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <button id="toggle">Toggle visibility</button>
    <div id="output">Hide me please</div>
</body>
</html>
```

```js
const output = document.getElementById('output');
//If we want to hide the div we add the 'hidden class'
output.classList.add('hidden');
//If we want normal behavior, remove the class, default is `display: block`
output.classList.remove('hidden');

// get the button-element
const button = document.getElementById('toggle');
//Add an onclick event listener that toggles the class.
//.toggle is a built in function bound to the classList
button.addEventListener('click', function(){
    output.classList.toggle('hidden');
})
```

1. Skapa en navigation med 3 stycken länkar. Ge navigationen ett id av `#nav`.Dessa länkar ska inte leda någonstans och ska ha `href="#"` för att förhindra att vi byter sida.
2. Gör så att den länken du klickar på får klassen `active` och att klassen `active` har någon unik styling som indikerar att vi har tryckt på den länken. Det kluriga här är att du måste dels lägga till klassen `active` på det element som du har klickat på, samtidigt så måste klassen `active` tas bort från alla andra länkar.

### Discofredag

1. Gör så att varje gång du trycker på bakgrunden på sidan så ändras bakgrunden till en slumpmässig färg. Detta sker med eventet `click`.
2. Gör så att varje gång du trycker på någon knapp på tangentbordet så ändras bakgrundsfärgen. Detta sker med eventet `keydown`eller `keyup`.

### Remove me!

Du har följande HTML, du ska göra så att varje gång du klickar på ett `<li>`-element ska det tas bort från sidan.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>List</title>
</head>
<body>
    <ul id="todo">
        <li>Köpa mjölk</li>
        <li>Lära mig JavaScript</li>
        <li>Leka med DOMen</li>
        <li>DOOMSDAY</li>
    </ul> 
    <ul id="done">
        
    </ul>
</body>
</html>
```

### Do not remove me, transfer me

Använd samma HTML som i förra övningen. Du ska istället för att ta bort elementet när du klickar på det, flytta det till listan med `id="done"`. Så vid klick så tas det bort från första listan och läggs i den andra listan.


### Validate

Gör ett textfält som validerar tal. När textfältet tappar fokus ska du kontrollera om texten i textfältet är ett giltigt tal. Du ska skriva ut resultatet i ett annat element som ligger i anslutning till textfältet. Om texten är ett tal ska talet skrivas ut, om texten inte är ett gitligt tal så ska det skrivas ut _Not a number silly!"_. _Kom ihåg att du hämtar värdet med `.value` från ett inputfält samt att det finns en inbyggd hjälpfunktion för att kolla om något är ett nummer eller inte_

### Validate 2
Liknande som föregående övning. Ha ett `<input>`-fält som du läser in text ifrån. När du skriver något i inputfältet ska det skrivas ut i ett element bredvid inputfältet (eller någonstans på sidan). Texten ska vara röd så länge längden på texten är under 8 tecken. När texten går över 8 tecken så sak texten bli grön. _Extra: gör så att texten blir gul om texten är mellan 5 och 8 tecken_.

### Print keycode

Gör en sida med ett textfält. När användaren håller nere en tangent ska du skriva ut i en div vilka knappar som hålls nere. Vilka events ska man använda? Tips: googla på `keyevent` eller `keycode`

### Add a button

Skapa en knapp. När du trycker på den knappen ska en ny knapp läggas till på sidan. Vilken knapp du än trycker på så ska en ny knapp läggas till på sidan. _Tips, när du skapar en ny knapp så måste du samtidigt binda ett nytt event till den._

### Random add a button
Fortsättning på föregående uppgift. Varje gång du lägger till en knapp så ska den knappen läggas till på ett slumpmässigt ställe på sidan. _Tips, tänk på hur du skulle göra i CSS_. 

### Start stop

Gör en sida med två knappar. På den ena ska det stå "Start" och på den andra "Stopp". Stopp-knappen ska vara inaktiverad, använd `element.disabled=true`. När man klickar på Start ska start-knappen inaktiveras och stopp-knappen aktiveras. När man klickar på Stopp ska det bli tvärtom.

### Hamburger
Skapa eller kopiera en hamburgermeny. När du klickar på hamburgaren så ska en meny glida fram från höger eller vänster. Detta gör du med en event listener, men majoriteten av implementationen handlar om CSS. _Tips, använd `classList.toggle`_


### Övningar utan facit
> Exempel på vad ni kan fortsätta med att försöka implementera på egen hand

* Gör en sida med "flikar". Ett system med flikar är när man har två eller flera element (använd `<div>`) som finns på samma plats på sidan, men bara ett är synligt åt gången. Det ska finnas knappar eller andra element (ett per div) som man klickar på för att göra motsvarande element synligt. Detta skulle sen kunna göras som ett galleri. D.v.s. Du har en stor bild i mitten, sedan när du klickar på en av 3-5 olika mindre thumbnails under den stora bilden så växlas den stora bilden. _Tips, hämta ut `img.src` och sätt det på ett annat element_
* Gör om övningen som mätte längden på inputvärdet och visade grönt, gult eller rött. Gör istället för att texten blir färglagd så att det finns en **progress bar** som visar upp färgerna.
* Skapa tre stycken checkboxes, Varje gång man trycker i en av checkboxarna så ska texten på dess `<label>` läggas till i en lista vid sidan om. När du trycker bort checkboxen så att den blir okryssad så ska elementet tas bort från lista.

## Strings


### Övning 1

__a)__
Gör om följande kod så att den använder template literals:

```js
const numberOfPeople = 10;
const pizzasPerPerson = 3;

console.log("You are " + numberOfPeople + " people and there is one pizza for every " + pizzasPerPerson + " person. This means that you have to buy " + Math.ceil(numberOfPeople / pizzasPerPerson) + " pizzas!");

```

__b)__

Gör om följande kod så att den använder `innerHTML` samt _template literals_ för att skapa HTMLen. _Tips: du behöver bara `document.body.innerHTML =`_

```js
const container = document.createElement('div');
div.classList.add('img-container');
const img = document.createElement('img');
img.src = "images/img.png";
img.alt = "Wtf is this image, ugh!";
img.height = "200px";
img.width ="200px";
div.appendChild(img);
document.body.appendChild(div);
```

__c)__

Du ska återskapa en HTML-struktur med hjälp av JavaScript och `insertAdjacentHTML`. Du ska alltså inte lägga den nedre HTMLen i din `index.html`. Det enda du ska ha i `<body>` är detta:

```html
<p id="content">A nice picture<p>
```

Men du ska skapa detta:

```html
<div class="img-container">
    <img src="http://www.exoticanimalsforsale.net/img/Quokka-for-sale.jpg" alt="Wtf is this image, ugh!" height="200" width="200" />
    <p id="content">A nice <span>picture<span><p>
</div>`
```

Men du har enbart denna JavaScript:

```js
const content = document.getElementById('content');
```

Utgå från denna variabel `content` och bygg sedan upp HTML-strukturen utifrån den med `insertAdjacentHTML`.

### Övning 2

Skriv en funktion som gör om en sträng, en mening, till en array av strängar som exemplet nedan. _Tips: använd `split()`_

_exempel_
```
'Hello my name is Jesper' ->
[ 
    'Hello',
    'my',
    'name',
    'is',
    'Jesper'
];
```

Funktionen borde se ut något som såhär:

```js
const result = splitIntoArray('Hello my name is Jesper');
```

### Övning 3

Skriv en funktion som gör om första tecknet i en mening till stor bokstav. _Tips: använd `charAt()` och `slice()`_
_exempel_
```
'hello my name is jesper' ->
'Hello my name is jesper'
```

### Övning 4

Skriv en funktion som gör om alla första tecken i samtliga ord till stor bokstav. _Tips: använd `split()`_ 
_exempel_
```
'hello my name is jesper' ->
'Hello My Name Is Jesper'
```

### Övning 5

Skriv en funktion som gör om en större text till ett **excerpt** och där du kan bestämma hur långt utdraget ska vara. _Tips: använd `substr()/substring()`_

```
'This is a long text that describes the content of my blogpost, on some sites I wish to shorten this text' ->
'This is a long text that describes the content of my blogpost...'
```

### Övning 6

Skriv en funktion som gör om **snake_case** till **camelCase**. _Tips: använd `split()` och `join()`_

```
'my_snake_function' ->
'mySnakeFunction'
```

### Övning 7 

Gör om övning 6 så att du kan skicka med ett andra argument till funktionen som bestämmer vilket casing som ska användas. _Tips: använd `split()` och `join()`_

```js
changeCase('my_snake_function', 'camel');
changeCase('my_snake_function', 'hyphen');
```

### Övning 8

Skriv en funktion som tar en sträng som argument och sedan returnerar den strängen baklänges

_exempel_
```js
'jesper' ->
'repsej'
```

### Övning 9

Skriv två funktioner med namn `getMonth` och `getDay` som plockar ut månad respektive dag ur en datumsträng (`'2018-02-20'`). Skriv med hjälp av dessa fuktioner en till funktion med namnet `daysBetween` som räknar ut hur många dagar det är mellan två datum. Du kan utgå från till en början att du ska räkna ut dagarna mellan två datum på samma månad. Om du vill kan du sedan gå vidare med att försöka få fram hur det blir om två datum är på olika månader. _Tips: använd `substr/substring`_
_exempel_
```
getDay('2018-02-20')    // === 20
getMonth('2018-02-20')  // === 2

daysBetween('2018-02-20', '2017-02-24') === 4 

```

### Övning 10

Skriv en funktion som översätter argumentet som skickas in till rövarspråk.

_exempel_
```
"Hej mitt namn är Waboo" ->
"Hohejoj momitottot nonamomnon äror Wawaboboo"
```

### Övning 11

Du har följande array och du ska skriva ut arrayen och samtliga `reviews` i arrayen med hjälp av `innerHTML` eller `insertAdjacentHTML` så att den får strukturen som du ser nedanför arrayen. D.v.s. att varje objekt i arrayen ska bli en egen artikel. Hur du stylar artikeln är upp till dig.
    
```js
const reviews = [
    { 
        name: 'Golden Gate Bridge',
        location: 'San Fransisco',
        grade: 8,
        author: 'Petronella',
        message: 'Visit the bridge at sunset for an absolute magnificent experience!',
        date: '2017-08-12'
    },
    { 
        name: 'Colors',
        location: 'Berlin',
        grade: 9,
        author: 'Sofia',
        message: 'Wow, awesome second hand store! Pay by the kilo.',
        date: '2015-09-23'
    },
    { 
        name: 'Pizzeria En Till',
        location: 'Köping',
        grade: 6,
        author: 'Jonne',
        message: 'Pizza is pizza.',
        date: '2018-01-01'
    }
];

```

```html
<article class="review-container">
    <h2>San Fransisco: Golden Gate Bridge<h2>
    <p class="content">'Visit the bridge at sunset for an absolute magnificent experience!'</p>
    <footer>
        <p class="grade">Grade: 8/10</p>
        <p class="metadata">By Petronella @ 2017-08-12</p>
    </footer>
</article>
```

#### Övning 12

Jag har inga fler övningar men ta en titt på W3Resources hemsida för att få tips på vad du kan göra för olika grejer. Väldigt många funktioner med lösningsförslag. En del kan ha lite utdaterad syntax men de funkar fortfarande bra.

* [https://www.w3resource.com/javascript-exercises/javascript-string-exercises.php](https://www.w3resource.com/javascript-exercises/javascript-string-exercises.php)
* [https://www.w3resource.com/javascript-exercises/javascript-dom-exercises.php](https://www.w3resource.com/javascript-exercises/javascript-dom-exercises.php)

## Objects & Context

### Övning 1 - Lägg till en funktion i ett objekt

Ett objekt är en variabel som är en samling av andra variabler, dessa variabler i samlingen är alltid ett `key/value`-par. En funktion är också en variabel, nästan allt i JavaScript kan sparas i variabler. Om vi lägger ihop det vi nu vet betyder det att en funktion kan lagras i ett objekt. Så här ser det ut:

```javascript
const album = {
    albumName: "Trouble Will Find Me",
    artist: "The National",
    year: 2013,
    printAlbum: function(){
        console.log(`The album ${this.albumName} by ${this.artist} was released in ${this.year}`);
    }
};
```

Namnet på funktionen blir `getContent` och är vår **property(egenskap)** i objektet, värdet på denna **property** blir en **anonym funktion**. När vi sedan vill använda oss av denna funktion kan vi kalla på den med `album.getContent()`. D.v.s. funktionen ligger inuti objektet och tillhör objektet, vi måste alltid kalla på den med punktnotation.

Den mest förvirrande delen av detta är att vi inte kan referera till variablerna i objektet genom deras namn enbart. Vi måste referera till dem med hjälp av `this.`. `this` syftar på just **det här** objektets variabler. `this` är ett nyckelord. Vi har alltid ett `this`. Om vi refererar till `this` **utanför** ett objekt så kommer vi att komma åt det globala objektet `window`.

__a)__
Använd koden ovan men skapa ytterligare en funktion i objektet. Denna funktion ska använda sig utav `year` och beräkna hur länge sen det var albumet släpptes. Funktionen ska returnera följande:
`This album was release 3 years ago`. Där årtalet ska ändras beroende på vilket år ditt album släpptes.
__b)__
Finns det något annat sätt att komma åt `year`, `artist` och `albumName` utan att använda `this`? Skriv hur det skulle se ut.

### Övning 2 - Object constructor

Vi vill oftast göra många olika album med olika innehåll. Vi vill kunna skriva ut albumet och när det släpptes men vi vill inte alltid hårdkoda in de värden som sak skrivas ut. Då kan det vara bra att använda en __constructor__. Det är också här `this.` kommer in tydligare i bilden. En __constructor__ kan skapa flera olika objekt utifrån samma **"mall"**. Vi defininerar hur objektet ska se ut, skapar en mall som objektet ska förhålla sig till. Sedan kan vi skapa flera olika objekt genom att använda samma kod. Se detta exempel:

```javascript

// A constructor is simply a function. As best practice we usually
// write them with first letter capitalized to distinguish them
// "ordinary" functions. But they are just an ordinary function.
function Album(albumName, artist, year){
    // Each time we call this function we are saving the arguments
    // each time to a new `this`, a new object. They have the samlingen
    // structure but are not the same object. Kinda like when we are creating
    // elements in the DOM. Each new <button> is unique but they are still of
    // the type 'button' and have properties that are 'buttony'
    this.albumName = albumName;
    this.artist = artist;
    this.year = year;
}

// The difference is when we call the function. If we call the function with
// the keyword  `new` we will create a new `this`. Otherwise we wont create
// a new object. The `new` keyword is important in this case
const album1 = new album("Blue", "Joni Mitchell", 1971);
const album2 = new album("Panic Prevention", "Jamie T", 2007);
```

```javascript
console.log(typeof Album);
console.log(typeof album1);
console.log(album1 instanceof Album);
console.log(album1 instanceof Object);
console.log(typeof album1.artist);
```

### Övning 3 - Create your weapon

1. Använd strukturen ovan (`Album()`) och skapa en egen **object constructor**. 
2. Objektet ska ha namnet `Weapon`;
3. Objektet ska ta två parametrar: `type` och `damage`
4. Värdena ska lagras med hjälp av `this.`
6. Du ska sedan med hjälp av objektet kunna skapa olika sorters vapen genom att kalla på detta constructor-objekt via nyckelordet `new` och sedan lagra vapnet i en ny variabel.

### Övning 4 - Slay the monster

Whaaha, ett monster! Ouf babouf!

```javascript
function Monster(name, health){
    this.name = name;
    this.health = health;
    this.speak = function(){
        console.log(`${this.name} hungry! ${this.name} kill!`);
    }
}

var Grublak = new Monster("Grublak", 500);

Grublak.speak();
```

1. Du har redan ett vapen som kan skada monstret från förra övningen.
2. Vi måste bygga en funktion som kan ta ner **Grublak**. Funktionen ska ta två argument, det ena argumentet ska vara ditt vapen och det andra argumentet ska vara monstret: `function slayMonster(weapon, monster){}`.
3. Funktionen ska sedan jämföra skadan från ditt vapen med livet på monstret.
4. Om `damage` är högre eller lika med monstrets `health` ska funktionen skriva ut `"Ouchy, me dead."`
5. Om skadan inte är högre än hälsan på monstret ska skadan subtraheras (-) från monstrets `health`.
6. Funktionen ska fortsätta köras tills monstret är dräpt. D.v.s när `damage` är högre än `health`.

### Övning 5 - Critta monstret!

1. Du kan nu döda monstret. Men det kanske tar lite tid beroende på hur mycket skada ditt vapen gör. Grublak är dock svag mot vapen av typen `Tenta`
2. Ändra i din funktion `slayTheMonster` så att om vapnet är av typen `Tenta` så tar Grublak dubbel skada.
3. Du har också turen på din sida. Ibland kan du få in en lyckosam crit så att du gör dubbel skada oberoende av vilket vapen du har. Det är 20% chans att du crittar.
4. Lägg till i din funktion så att du gör __dubbel__ skada på monstret om du går en critical hit.


### Övning 6 - Slay all the monsters

1. Skapa en array av olika monster, en array av objekt alltså.
2. Loopa sedan igenom alla monster med din funktion. Antingen genom att ha en loop inuti funktionen eller genom att kalla på funktionen `slayTheMonster` i en loop.


## Prototypes

1.  Det ska finnas ett "huvuddjur" som minst 2 djur ärver av. Tänk på att "Huvuddjuret" ska ha egenskaper som är gemensamma för de tre andra djuren så att de ej behöver repeteras.

2. Dina tre djurobjekt ska vara unika från varandra men ärva gemensamma egenskaper från huvuddjuret. Ett attribut du ska ha med är om djuret anses
farligt för människan eller inte.

3. Skapa en instans av vardera av de 2 djuren, inte av huvuddjuret. Lagra sedan dessa 2 djur i en array.

4. Skapa en for-loop som stegar igenom arrayen och skapar tre divar i body på ditt dokument. Divarna ska i sin tur innehålla information om djuren som kommer direkt från objekten. Om djuret är farligt ska bakgrundfärgen på div-en vara röd, om inte, grön.

1. Du ska skapa en `Constructor`-funktion som ska skapa ett nytt `Country`-objekt. Ett `Country` består av `name`, `continent`, `population`, ``
2. Kalla sedan på `Country`-funktionen och skapa två `Country`-objekt.
3. Lägg till två funktioner på prototypen till denna `constructor`-funktion. Funktionerna kommer alltså att vara kopplade till `Country`s prototyp. Den ena funktionen ska skriva ut befolkningen i landet i en snygg sträng och den andra ska göra samma sak fast med kontinenten, typ _"This country is in Africa"_. Testa kalla på de funktioner du skapat på varje enskilt `Country`-objekt för att se att de fungerar.
4. Skapa en ny `City`-constructor. `City`-constructorn ska ha samma egenskaper som `Country` förutom att den ska ha en ny egenskap: `country` (landet staden ligger i) och `name` ska nu istället vara namnet på staden.
5. Ändra på din `City`-constructor fast använd den här gången `call` för att kalla på `Country`-functionen för att återanvända dess parametrar. Kom ihåg att `City` nu har en ny egenskap: `country` som måste lagras och som inte finns i `Country`-funktionen.

```javascript
function City(){
    Country.call(obj, parameters);
}

```


6. Återskapa ovanstående funktionalitet med `Object.create`. För att skapa en prototyp åt ett objekt så måste du kalla på `Object.create` med ett objekt som innehar dina prototyp-funktioner.

## Solutions 

### Reading Comprehension


#### Övning 1
```js
1.01                 // Float number, still 'Number'
// true === 1 and false which means that this is 1 + 1 + 0
true + true + false
// Just a string, you can convert it with Boolean('false')
'false'
//5 is true, so we negate that and get false
!5
// Can't divide 0, we get 'Infinity'
1 / 0
// 5 is true, negate that and get false, negate that and get true
!!5
// one must be true, the second is true
false || true
// Neither is true so we get false
true && false || false && true
// 123 as a Number, the 0 converts it to a number
"123" - 0
// Implicit conversion of "1000" to 1000 === 100
"1000" / 10
// empty string is false === 0, so nothing happens
123.4 - ''
// 2 is not bigger than 3 so we get false
2 < 3
// "5" + "0" is concatenation so "50". We can't divide a string so "2" is ignored
'5' + "0" / '2'
// comparing strings, false
'två' < 'tre'
// The '5' is ignored but the 0 is converted to a string === "500"
'5' + "0" / '5' + 0
// the decimal doesn't add anything so === true
17 === 17.0
// Only numbers are being implicit converted
'1' + '5' - '4' * '2' - '3'
// The are no strictly the same === false
17 === '17'
// But these are kinda the same === true
17 == '17'
// NaN, you can't subtract 5 from a string
'kalle' - 5
//every value before is false, which will reach 'foo' and return 'foo'
undefined || null || 0 || false || "foo"
```


#### Övning 2 

```js
let z = 5;
// z = z + 1;
z++;
// z = z - 1;
--z;
// z = z + 15;
z += 15;
let x = 8;
let y = 16;
// z = 16 - 8
z = y - x;
// x = 10
x = 10;
// z = 10
z = x++;
x = 2;
y = 5; 
// x = 7
x = x + y; 
// y = 7 + 5
y = x + y;
// z = 12
z = y;
```

#### Övning 3 
> Denna får ni beskriva med egna ord men här är ett ungefärlig förklaring

__a)__
Funktionen tar 3 argument för att vi har 3 parametrar, alla parametrar multipliceras med varandra inuti funktionen. Vilket gör att vi får `2 * 2 * 2` vilket för att funktionen returnerar `8`
__b)__
Vi kallar på funktionen med enbart 2 argument. Detta skulle möjligtvis kunna gå men vi har sagt att vi ska lägga ihop **alla 3 värden**, om ett av dessa värden saknas så kommer parametern (`c` i det här fallet) att bli `undefined` vilket betyder att vi gör följande `return 2 * 2 * undefined`. Detta kommer att resultera att vi får tillbaka `NaN` (Not A Number). Alternativet är att vi kollar så att alla värden finns med en if-sats och sedan lägger ihop värdena.
__c)__
JavaScript konverterar i smyg alla strängar som kan konverteras till nummer, i detta fall så kan `"2"` bli `2` och inget konstigt händer. Funktionen fungerar som den ska.
__d)__
Nej, vi kan inte skicka med en funktion heller. Funktionen förväntar sig ett värde, en funktion är en variabel men den kan inte multipliceras. Vi skulle kunna lösa detta med följande:
```js
function multiply(a, b, c){
    return a * b * c();
}
```
Men samtidigt så skulle vi då inte kunna kalla på funktionen med ett sista värde som är ett nummber, sista värdet måste här alltid vara en funktion i så fall. Dum idé!


> Förklara i text hur funktionen nedan körs när vi kallar på den(dvs. i vilken ordning allt händer) i dessa scenarion:
 
* a) Vi kallar på funktionen med: `multiply(2, 2, 2);`
* b) Vi kallar på funktionen med: `multiply(2, 2);`
* c) Vi kallar på funktionen med: `multiply(2, 2, "2");`
* d) Vi kallar på funktionen med: `multiply(2, 2, function(){ return 2;});`

```javascript
function multiply(a, b, c){
    return a * b * c;
}
```

#### Övning 4

Argumenten är de värden som skickas med när vi kallar på funktionen. Dessa kan vara ensamstående värden eller variabler. Det spelar ingen roll vad variablerna heter när vi skickar med de som argument, de kommer ändå att få namnen `a,b,c` **inuti** funktionen.
```js
let blabb = 4;
let slabb = 2;
let klabb = 2;
multiply(2,2,2);
multiply(blabb, slabb, klabb);
```

Parametrarna är de variabler som är innanför paranteserna på en funktion. I det här fallet så är det `a`, `b` och `c`. I princip är det som att vi skapar nya variabler i scopet men vi behöver aldrig skriva `var` eller `let`. `a`, `b` och `c` existerar bara i funktionens scope.
```js
function multiply(a, b, c){
    let a;
    let b;
    let c;
    return a * b * c;
}
```


#### Övning 5

Vi deklarerar och initierar en global variabel som är av typen `String` och som heter `text`. Vi skapar en funktion som heter `callMe`. Funktionen `callMe` deklarerar en ny variabel som också heter `text`. `text` finns i två olika scope och kan därför ha olika värden utan att störa varandra. Vi returnerar direkt detta inre värde `text` som när vi returnerar det är `"Call me!"`. Eftersom `console.log` ligger efter `return` så kommer de raderna aldrig att nås eftersom vi redan har "gått ur" funktionen, när vi skriver `return` så lämnar vi funktionen. `callMe()` kommer att returnera texten, men den kommer aldrig sparas eller skrivas ut någonstans eftersom vi varken loggar ut den eller sparar den i en variabel. 

#### Övning 6

__a)__
```js
function foo() {
  console.log("test");
}
foo("hej");
```

Svar: `"test"`
Argumentet `"hej"` spelar ingen roll, vi använder det ändå inte så det försvinner bara när vi kallar på funktionen.

__b)__
```js
let a = foo(3);
console.log(a);
function foo(i) {
  return i * i;
}
```

Svar: `9`
Funktionen `foo` gångrar värdet som vi skickar in med sig själv. `a` blir därför 3*3 = 9.

__c)__
```js
console.log(foo(3, 5));
function foo(x, y) {
  return x * y;
}
```

Svar: `15`, vi kan kalla på en function declaration innan vi har skapat den. Den **hoistas** upp längst upp i scopet

__d)__
```js
console.log(foo(3, 5));
const foo = function(x, y) {
  return x * y;
}
```

Svar: `undefined is not a function` vi kan INTE kalla på en function expression innan vi har skapat den. Den **hoistas inte** upp längst upp i scopet

__e)__
```js
let x = 2;
let y = 3
let a = foo(foo(x) + foo(y));
console.log(a);
function foo(i) {
  return 5 * i;
}
```
Svar: `125`

`foo` returnernar det värde vi skickar in och gångrar det med 5. På rad tre plussar vi ihop 2 stycken returnvärden från två anrop till `foo`. Så rad tre blir

```
foo(2) === 15
foo(3) === 10
15 + 10 === 51
foo(25) === 125
```

---

__f)__
```js
const person = {
    name: "Steffe",
    sayName(){
        console.log(this.name);
    }
}
person.sayName();
```

Svar: `"Steffe"`

När vi använder `this` pekar vi mot de inre egenskaperna av ett objekt. `this.name` är där vi har skrivit `name: "Steffe`. När vi kallar på funktionen som vanligt så hämtas detta namn upp.

---

__g)__
```js
const person = {
    name: "Steffe",
}

function sayName(){
    console.log(this.name);
}
person.sayName = sayName;
person.sayName();
```
Svar: `"Steffe"`

Vi behöver inte direkt lägga funktionen i objektet. I första läget så kommer funktionen `sayName` INTE skriva ut Steffe då funktionen inte ligger i objektet. Men på näst sista raden så ger vi objektet funktionen så att objektet kommer att se ut som föregående övning och vi får samma resultat. Skulle vi kappa på funktionen som den är `sayName()` så får vi `this === window` medan om vi kallar på `person.sayName` så får vi objektets namn som är `"Steffe"`.

---

__h)__
```js
const animals = ["dog", "cat", "zebra", "horse", "cow"];
animals.shift();
console.log(`My favourite animal is ${animals[0]}`);
```
Svar: `"cat"`

---

__i)__

```js
let a = 5;
function foo(a) {
  a++;
}
a += 2;
console.log(a);
```

Svar: `7`

funktionen `foo` kallas aldrig på så det är bara den femte raden som gör någonting med `a`. Därför får vi 7 och inte 8.

---

__j)__
```js
function foo(a) {
  return a + 2;
};
function goo(x, y) {
  return x(y);
};
let a = goo(foo, 3);
console.log(a);
```

Svar: `5`

`goo`s första parameter föräntas vara en funktion eftersom vi kallar på den med den andra parametern `x(y)`. `foo` är den funktion som vi skickar med och kallar på den andra parametern med så det vi säger i `goo` är `return foo(3)`. `foo(3)` i sin tur returnerar `return 3 + 2` vilket gör att `a` är `4`;

---

__k)__
```js
var text = "";
var a = {
    value: "c"
};
var b = {
    value: "a"
};
var c = {
    value: "b"
};
text = a.value + b.value + c.value;
console.log(text);
```

Svar: `"cab"`

Vi hämtar värdet av varje egenskap `value` i de olika objekten. `value` är dock en sträng i samtliga fall och inte själva värdet. namnet `value` är nyckeln.

---

__l)__
```js
const a = 0;
const objekt = {
    a: 100,
    b: 200,
    c: 300
};
for(const value in objekt){
    a += value;
}

console.log(a);
```

Svar: **`"0abc"`**

`for..in` loopar inte igenom värdena utan enbart nyklarna. Så vi får `a,b,c` och inte `100,200,300`. Vi har redan `0` sen konkatenerar vi på bokstäverna vilket betyder att vi får **`"0abc"`**

---

__m)__
```js
function foo () {
  //Här returneras bar() innan funktionen har deklarerats.
  return bar();
  //Dock så hoistas bar() upp ovanför return vilket gör att funktionen ändå 
  //kallas på eftersom här blir funktionen deklarerad innan return p.g.a hoist
  function bar() {
    return "FOOBAR!!";
  }
}
console.log(foo());
```

Svar: `"FOOBAR!!"`

Märk också att funktionen kallas på när den returnernas. Om vi skulle skriva `return bar` så skulle vi behöva göra följande:

```js
function foo () {
  //Här returneras bar() innan funktionen har deklarerats.
  return bar();
  //Dock så hoistas bar() upp ovanför return vilket gör att funktionen ändå 
  //kallas på eftersom här blir funktionen deklarerad innan return p.g.a hoist
  function bar() {
    return "FOOBAR!!";
  }
}
const foobar = foo();
console.log(foobar());
```

Vi måste alltid kalla på funktionen `()` för att den ska köras. Annars så skickar vi bara runt variabeln som funktionen ligger i.

### DOM & Events

1.
```js
const div = document.createElement('div');
const p = document.createElement('p');
const text = document.createTextNode('Satan va JavaScript är kul!');
p.appendChild(text);
div.appendChild(p);
document.body.appendChild(div);
```

2.
```js
document.body.innerHTML = "<div><p>Satan va JavaScript är kul!</p></div>";
```

3.
```js
document.body.style.fontFamily = 'Comic Sans MS';
document.getElementById('nickname').innerHTML = 'Git McFetch';
document.getElementById('favoriteFood').innerHTML = '34';
document.getElementById('hometown').innerHTML = 'Alvesta';
const items = document.getElementsByTagName('li');
for (var i = 0; i < items.length; i++) {
    items[i].className = 'list-item';
}
var myPicture = document.createElement('img');
myPicture.src = 'waha.png";
document.body.appendChild(myPicture);
```

4.
```js
// 1-4
const books = [
  {
    title: 'The Design of EveryDay Things',
    author: 'Don Norman',
    isRead: true
  },
  {
    title: 'Darling River',
    author: 'Sara Stridsberg',
    isRead: true
  },
  {
    title: 'A book',
    author: 'Unknown',
    isRead: false
  }
];
    
for (let i = 0; i < books.length; i++) {
  const bookParagraph = document.createElement('p');
  const bookDescription = document
    .createTextNode(books[i].title + ' by ' + books[i].author);
  bookP.appendChild(bookDescription);
  document.body.appendChild(bookParagraph);
}

// 4 - 7
const bookList = document.createElement('ul');
for (let i = 0; i < books.length; i++) {
  const bookItem = document.createElement('li');
  const bookImg = document.createElement('img');
  bookImg.src = books[i].img;
  bookItem.appendChild(bookImg);
  const bookDescription = document
    .createTextNode(books[i].title + ' by ' + books[i].author);
  bookItem.appendChild(bookDescription);
  if (books[i].isRead) {
    bookItem.style.color = 'lightsalmon';
  }
  bookList.appendChild(bookItem);
}
document.body.appendChild(bookList);
```

5.
```js
//Put this in your main.js then work from there
const article = document.getElementById('first');

//Grab the first child that is an element
article.firstElementChild.innerText = "I've changed!";
article.lastElementChild.alt = "My picture!";
//Pick out the last child that is an element
const paragraphToRemove = article.lastElementChild;
//removechild needs both the parent and the child to remove
article.removeChild(paragraphToRemove);
// Go up a step with 'parentElement' and we get 'main'. We then have to select
// the sibling to that element and change the text.
article.parentElement.previousElementSibling.innerText = "Changin deluxe";
article.nextElementSibling.firstElementChild.innerText = "I've changed too!";
const img = document.createElement('img');
img.src = "haha.png";
img.alt = "Haha";
article.nextElementSibling.appendChild(img);
const span = document.createElement('span');
const spanText = document.createTextNode("I'm special");
span.appendChild(spanText);
// children is an array of elements. the p-tag is the second element, index 1
article.children[1].appendChild(span);
article.children[1].firstElementChild.style.color = 'lightcoral';
```

#### Övning 1

```js
const div = document.getElementById('output');
const paragraph = document.createElement('p');
paragraph.textContent = "JavaScript is great!";

//Get each button from the DOM
const addButton = document.getElementById("addButton");
const removeButton = document.getElementById("removeButton");
const sparkle = document.getElementById('sparkle');

//Add an event listener to the add button that listens on 'click'
addButton.addEventListener('click', function(){
    //JavaScript will not add a new paragraph if it already
    //exists on the page. We can clone the node and create
    //a copy of it with `cloneNode`. This way we can add 
    //multiple paragraphs. We can also do a variant with `innerHTML`
    const newParagraph = paragraph.cloneNode(true);
    div.appendChild(newParagraph);
});

removeButton.addEventListener('click', function(){
    //Easiest is to get the last child and remove it.
    //alternatively get the first child and remove it
    div.removeChild(div.lastElementChild);
});

sparkle.addEventListener('click', function(){
    //'div.children' contains all our paragraphs.
    //if we want to apply something to each of the paragraphs
    //we have to loop it
    for(let p of div.children){
        p.style.color = 'lightcoral';
    }
});
```

#### Övning 2 - Pizza Calculator

```js
const input = document.getElementById('numberOfPeople');
const button = document.getElementById('calculatePizzas');
const output = document.getElementById('output');

button.addEventListener('click', function(){
  const numberOfPeople = input.value;
  const pizzas = Math.ceil(numberOfPeople/3);
  output.textContent = pizzas;
})
```


```js
const input = document.getElementById('numberOfPeople');
const output = document.getElementById('output');

input.addEventListener('keyup', function(){
  const numberOfPeople = input.value;
  const pizzas = Math.ceil(numberOfPeople/3);
  output.textContent = pizzas;
});
```


#### Övning 3 - navbar

```js
// Get every a-tag in the #nav
const navLinks = document.querySelectorAll('#nav a');

//Loop through all of the navlinks to listen to every click
for(const link of navLinks){
  //Add an event listener for each of the links
  link.addEventListener('click', function(){
    //Each time we click a link we must loop through
    //every link again to remove any 'active' classes
    //we have added before, otherwise they will not be removed
    for(const sibling of navLinks){
      sibling.classList.remove('active');
    }
    // 'this' refers to the element clicked, JavaScript knows
    // what 'this' means. So if we click the middle link only
    // that link will get the 'active' class.
    this.classList.add('active');
  })
} 
```

#### Övning 4 - Discofredag

```js
// If we want to add an event listener to the whole page
// we can add it directly to the 'window' object
window.addEventListener('click', function(){

  /**
   * RGB stands for Red Green Blue and each color is set in a number
   * from 0-255. We can get 3 random numbers in that span with Math.Random()
   * Math.floor is to round down the number, otherwise we will get decimals.
   */

  const r = Math.floor(Math.random()*256);
  const g = Math.floor(Math.random()*256);
  const b = Math.floor(Math.random()*256);
  //Then we add them together to create the string that will
  // be for example rgb(255,10,24);
  const rgb = 'rgb(' + r + ',' + g + ',' + b + ')';
  //Then we set the body-tag to that background-color
  document.body.style.backgroundColor = rgb;
})
```

```js
// If we want to add an event listener to the whole page
// we can add it directly to the 'window' object
window.addEventListener('keyup', function(){

  /**
   * RGB stands for Red Green Blue and each color is set in a number
   * from 0-255. We can get 3 random numbers in that span with Math.Random()
   * Math.floor is to round down the number, otherwise we will get decimals.
   */

  const r = Math.floor(Math.random()*256);
  const g = Math.floor(Math.random()*256);
  const b = Math.floor(Math.random()*256);
  //Then we add them together to create the string that will
  // be for example rgb(255,10,24);
  const rgb = 'rgb(' + r + ',' + g + ',' + b + ')';
  //Then we set the body-tag to that background-color
  document.body.style.backgroundColor = rgb;
})
```

#### Övning 5 - Stryk mig!!

```js
const listItems = document.querySelectorAll('li');

for(const item of listItems){
    item.addEventListener('click', function(){
        this.parentElement.removeChild(this);
    })
}
```

#### Övning 6 - Stryk mig inte, flytta mig!

```js
const todo = document.getElementById('todo');
const done = document.getElementById('done')
const listItems = document.querySelectorAll('li');

for(const item of listItems){
    item.addEventListener('click', function(){
        todo.removeChild(this);
        done.appendChild(this);
    })
}
```

1.
```js
// Create an input with id of 'input' in your html
const input = document.getElementById('input');
// Create a div with id of 'output' in your html
const output = document.getElementById('output');

input.addEventListener('blur', function(){
  // the built in function 'isNaN' will return `true` if
  // the value from the input field is Not A Number. If
  // the value is a valid number, continue to else
  if(isNaN(input.value)){
    output.textContent = "That is not a number silly!";
  } else {
    output.textContent = input.value + "is really a number!";
  }
});
```

2.
```js
const input = document.getElementById('input');
const output = document.getElementById('output');

input.addEventListener('keyup', function(){
  if(input.value.length < 5){
    output.style.color = 'red';
  } else if (input.value.length >= 5 && input.value.length < 8) {
    output.style.color = 'yellow';
  } else {
    output.style.color = 'green';
  }
  output.textContent = input.value;
})
```

3.
```js
// Create an input with id of 'input' in your html
const input = document.getElementById('input');
// Create a div with id of 'output' in your html
const output = document.getElementById('output');

// event listeners always outputs an event, you can listen to
// this event and pick out the key or keyCode to get the key
input.addEventListener('keydown', function(event){
  output.textContent = event.key;
});
```

4. 
```js
// Get the initial button
const button = document.getElementById('button');

//Add an event listener to that button that calls a function
// named 'createButton'.
button.addEventListener('click', function(){
  createButton();
});

// createButton does two things, one: creates a new button
// with createElement, two: adds a new event listener to that button.
// WE must add new eventListeners to very dynamically added element 
function createButton(){
  const newButton = document.createElement('button');
  newButton.textContent = "Stäng";
  newButton.addEventListener('click', createButton);
  document.body.appendChild(newButton);
}
```

5.
```js
const button = document.getElementById('button');

button.addEventListener('click', function(){
  createButton();
});

//Create a function that creates a button
function createButton(){
  const newButton = document.createElement('button');
  newButton.textContent = "Stäng";
  // Set an absolute position
  newButton.style.position = "absolute";
  // Generate a random px value for top and left position, 
  // rememeber to add "px"
  const randomTop = Math.floor((Math.random() * 1200) + 1) + "px";
  const randomLeft = Math.floor((Math.random() * 1200) + 1) + "px";
  newButton.style.top = randomTop;
  newButton.style.left = randomLeft;
  newButton.addEventListener('click', createButton);
  document.body.appendChild(newButton);
}
```

6.
```js
const start = document.getElementById('start');
const stop = document.getElementById('stop');

// When you disable one of them you need to enable the other
// `disabled` will make it unclickable
stop.addEventListener('click', function(){
  stop.disabled = true;
  start.disabled = false;
});

start.addEventListener('click', function(){
  stop.disabled = false;
  start.disabled = true;
});
```

7.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style type="text/css">
        body {
            margin: 0;
        }
        #menu {
            height: 100vh;
            width: 400px;
            background-color: hotpink;
            transition: all 300ms;
            margin-left: -400px;
        }
        .show {
            transform: translateX(400px);
        }
    </style>
</head>
<body>
    <button id="burger">MENU</button>
    <div id="menu"></div>  
    <script src="main.js"></script>
</body>
</html>
```

```js
const burger = document.getElementById('burger');
const menu = document.getElementById('menu');

burger.addEventListener('click', function(){
    menu.classList.toggle('show');
})
```


Checkbox "lösning"
```js
const checks = document.querySelectorAll('input[type="checkbox"]');
const output = document.getElementById('output');

for (const check of checks) {
  check.addEventListener('click', function () {
    const labelText = this.nextElementSibling.innerText;
    if (this.checked) {
      const pTag = document.createElement('p');
      pTag.innerText = labelText;
      output.appendChild(pTag);
    } else {
      const childrenOfOutput = output.children;
      for (const child of childrenOfOutput) {
        if (child.innerText === labelText) {
          output.removeChild(child);
        }
      }
    }
  });
}
```

### Strings

####  Övning 1
__a)__
```js
const numberOfPeople = 10;
const pizzasPerPerson = 3;

console.log(`You are ${numberOfPeople} people and there is one pizza for every ${pizzasPerPerson} person. This means that you have to buy ${Math.ceil(numberOfPeople / pizzasPerPerson)} pizzas!`);
```

__b)__

```js
document.body.innerHTML = `
    <div class="img-container">
        <img src="images/img.png" alt="Wtf is this image, ugh!" height="200" width="200" />
    </div>`;
```

__c)__

```js
const content = document.getElementById('content');

content.insertAdjacentHTML('beforeend', `<span>picture</span>`);
content.insertAdjacentHTML('beforebegin', `<div class="img-container">
  <img src ="http://www.exoticanimalsforsale.net/img/Quokka-for-sale.jpg" alt = "Wtf is this image, ugh!" height = "200" width = "200" />`);
content.insertAdjacentHTML('afterend', `</div>`);

```

#### Övning 2
```js
function splitIntoArray(stringToSplit){
    // split is a built in function that takes an argument,
    // the argument tells the function how to split the
    // string, in this case we split at each space
    return stringToSplit.split(' ');
}

console.log(splitIntoArray('Hello my name is Jesper'));
```

#### Övning 3

```js
function capitalizeWord(stringToCapitalize){
    // extract first letter
    let firstLetter = stringToCapitalize.charAt(0);
    // convert it to uppercase
    firstLetter = firstLetter.toUpperCase();
    // slice extracts a part of the string, starting att index 1,
    // we start at 1 and proceed to the last index
    const restOfSentence = stringToCapitalize.slice(1);
    // Put first letter + first of sentence together, concat
    return firstLetter + restOfSentence;
}
```

#### Övning 4

```js
function splitIntoArray(stringToSplit) {
  return stringToSplit.split(' ');
}

function capitalizeWord(stringToCapitalize) {
  // extract first letter
  let firstLetter = stringToCapitalize.charAt(0);
  // convert it to uppercase
  firstLetter = firstLetter.toUpperCase();
  // slice extracts a part of the string, starting att index 1
  const restOfSentence = stringToCapitalize.slice(1);
  // Put first letter + first of sentence together, concat
  return firstLetter + restOfSentence;
}

/* Reuse the prevous functions! We have alread written half of
   the code already */

function capitalizeAllWords(stringToCapitalize) {
  // Split the string into an array with prevous method
  const arrayOfWords = splitIntoArray(stringToCapitalize);
  // Create a new array to store the transformed values
  const newArray = [];
  // Loop through all the words in the array
  for (const word of arrayOfWords) {
    // Use the function from before
    const uppercaseWord = capitalizeWord(word);
    // When the word has been capitalized, push it
    // to the new array
    newArray.push(uppercaseWord);
  }
  // We can easily join an array with 'join', the argument
  // ' ' specifies that each word should be glued together with
  // a space
  return newArray.join(' ');
}

console.log(capitalizeAllWords("hello my friend"));
```

#### Övning 5

```js
function excerpt(stringToShorten, amount){
    //substr(start index, end index)
    return stringToShorten.substr(0, amount);
}

console.log(excerpt("Hello how are you mister sister?", 12)) //Hello how are
```


#### Övning 6

```js
function capitalizeWord(stringToCapitalize) {
  // extract first letter
  let firstLetter = stringToCapitalize.charAt(0);
  // convert it to uppercase
  firstLetter = firstLetter.toUpperCase();
  // slice extracts a part of the string, starting att index 1
  const restOfSentence = stringToCapitalize.slice(1);
  // Put first letter + first of sentence together, concat
  return firstLetter + restOfSentence;
}

function changeCase(stringToConvert) {
  //Convert string to an array for easy handling
  const wordArray = stringToConvert.split('_')
  // We will create a new array again
  const newArray = [];
  // Loop through all strings in the array
  for (let i = 0; i < wordArray.length; i++) {
    // if it's the first word, no capitalizing
    if(i > 0){
      const capitalizedWord = capitalizeWord(wordArray[i]);
      newArray.push(capitalizedWord);
    } else {
      // Otherwise, just push the word
      newArray.push(wordArray[i]);
    }
    
  }
  // no space in the argument, just an empty string
  return newArray.join('');
}

console.log(changeCase('snake_case_casing'));
```

#### Övning 7

```js
function capitalizeWord(stringToCapitalize) {
  // extract first letter
  let firstLetter = stringToCapitalize.charAt(0);
  // convert it to uppercase
  firstLetter = firstLetter.toUpperCase();
  // slice extracts a part of the string, starting att index 1
  const restOfSentence = stringToCapitalize.slice(1);
  // Put first letter + first of sentence together, concat
  return firstLetter + restOfSentence;
}

function changeCase(stringToConvert, case) {
  //Convert string to an array for easy handling
  const wordArray = stringToConvert.split('_')
  // We will create a new array again
  const newArray = [];
  // Loop through all strings in the array
  for (let i = 0; i < wordArray.length; i++) {
    // if it's the first word, no capitalizing
    if(i > 0 && case === 'camel' ){
      const capitalizedWord = capitalizeWord(wordArray[i]);
      newArray.push(capitalizedWord);
    } else {
      // Otherwise, just push the word
      newArray.push(wordArray[i]);
    }
    
  }
  if(case === 'camel'){
    return newArray.join('');
  } else {
    return newArray.join('-');
  }  
}

console.log(changeCase('snake_case_casing', 'hypen'));
```

#### Övning 8

```js
function reverse(stringToReverse){
  return string.split('').reverse().join('');
}

// Same function as above but I have made the steps
// separate. This is what happens above
function reverse(stringToReverse){
    const wordArray = stringToReverse.split('');
    const reversed = wordArray.reverse();
    const joinedArray = reversed.join('');
    return joinedArray;
}

console.log(reverse("jesper"));
```

#### Övning 9

```js
function getDay(dateString){
    return dateString.split('-')[2];
}

function getMonth(dateString){
    return dateString.split('-')[1];
}

function daysBetween(firstDate, secondDate){
    const firstDay = getDay(firstDate);
    const secondDay = getDay(secondDate);
    return secondDate - firstDate;
}

```

#### Övning 10

```js
// Hold on tight
function yarr(string) {
  // Define which our vowels are so we can look for them
  const vowels = ["a", "e", "i", "o", "u", "y", "å", "ä", "ö"];
  // We first have to split the words
  const words = string.split(' ');
  // Create an empty array to hold all the finished words
  const yarrArray = [];
  // Loop through each word
  for(const word of words){
    // But we also have to loop through each char
    // so we split that too
    const charsInWord = word.split('');
    // An create a array to hold all the chars in a word
    let wordArray = [];
    // Loop through all chars
    for(const char of charsInWord){
      // If the array of vowels includes our char
      // we have a vowel and we can just push it to the
      // array
      if (vowels.includes(char)) {
        wordArray.push(char);
      } else {
        // else we have to apply our rule:
        // H -> HOH, F -> FOF and so on
        const yarredChar = `${char}o${char}`;
        // The we can push it
        wordArray.push(yarredChar);
      }
    }
    // When we are done with each word, join it again
    // then push it to the big array with all the words
    yarrArray.push(wordArray.join(''));
  }
  // When we are all done we can join the array of words
  // and return it
  return yarrArray.join(' ');
}

console.log(yarr('Hello everyone'));
```

#### Övning 11

_lösningsförslag 1_
```js
for (const review of reviews) {
  let htmlBlock = `
  <article class="review-container">
    <h2> ${review.location}: ${review.name} </h2>
    <p class="content"> ${review.message}</p>
    <footer>
      <p class="grade"> ${review.grade} /10 </p>
      <p class="metadata">By ${review.author} @ ${review.date} </p>
    </footer>
  </article>`;
  output.insertAdjacentHTML('beforeend', htmlBlock);
}

```

_lösningsförslag 2_
```js
let htmlBlock = "";
for(const review of reviews){
  htmlBlock += `
  <article class="review-container">
    <h2> ${review.location}: ${review.name} </h2>
    <p class="content"> ${review.message}</p>
    <footer>
      <p class="grade"> ${review.grade} /10 </p>
      <p class="metadata">By ${review.author} @ ${review.date} </p>
    </footer>
  </article>`;
}
output.innerHTML = htmlBlock;
```

### Object & Context

#### Övning 1 

```js
const album = {
    albumName: "Trouble Will Find Me",
    artist: "The National",
    year: 2013,
    printAlbum: function(){
        console.log(`The album ${this.albumName} by ${this.artist} was released in ${this.year}`);
    }
    getYear: function(currentYear){
        return `This album was released ${(currentYear - this.year)} years ago`;
    },
    getYear2: function(){
        const currentYear = (new Date()).getFullYear();
        return `This album was released ${(currentYear - this.year)} years ago`;
    }
};

//När vi kallar på funktionen skickar vi med 2016 som argument som blir till currentYear
console.log(album.getYear(2016));
console.log(album.getYear());

```

#### Övning 2

```js
function Album(albumName, artist, year){
    this.albumName = albumName;
    this.artist = artist;
    this.year = year;
    this.printAlbum = function() {
      console.log(`The album ${this.albumName} by ${this.artist} was released in ${this.year}`);
  }
}

const album1 = new Album("Blue", "Joni Mitchell", 1971);
const album2 = new Album("Panic Prevention", "Jamie T", 2007);

// We can use `printAlbum()` on both the albums. We create the function
// once and then it is bound to each album created. This is great if we have
// a lot of functions that we want to call on a lot of objects. If we have
// a 'records app' we would have thousands of albums. We would not save them
// as 'album1', 'album2' etc. tho.
album1.printAlbum();
album2.printAlbum();
```


#### Övning 3 - Create your weapon

```js
// Constructor pattern is a regular function, we write
// the function name with big letter at the start because
// that is best practice, but it doesn't change the function at all
function Weapon(type, damage){
    // Each parameter/argument is stored to `this.property`. `this`
    // will refere to all new objects created with this function
    this.type = type;
    this.damage = damage;
}

// To create a new object based on this function we must use `new`
// `new` will return a new object based on what the function do.
// Notice how there is no `return` in the function but `new` returns
// a new object for us that looks like this: { name: "Rusty Dagger", damage: 10000 }
const rustyDagger = new Weapon('Rusty Dagger', 10000);
```

#### Övning 4 - Slay the monster

```js
// The monster constructor is the same, it just has different value or
// different names on the values. It also got a function that speaks it name
// but it is not important, it is just an example
function Monster(name, health){
    this.name = name;
    this.health = health;
    this.speak = function(){
        console.log(`${this.name} hungry! ${this.name} kill!`);
    };
}

function Weapon(type, damage){
    this.type = type;
    this.damage = damage;
}

const rustyDagger = new Weapon('Rusty Dagger', 500);
// We call it exactly like the previous functions
const Grublak = new Monster('Grublak', 10000);

// We call the function `slayMonster` that is declared below
// we send along the two object: `rustyDagger` and `Grublak`
slayTheMonster(rustyDagger, Grublak);

function slayTheMonster(weapon, monster){
    // We can save the health of the monster
    // by extracting it for the object. This is just
    // so we don't have to write `monster.health` every time.
    let health = monster.health;
    // we do the same with damage and name for easier handling
    const damage = weapon.damage;
    const name = monster.name;
    // While the monster has health left we will continue to strike it
    while (health > damage){
        // We subtract the damage from the current health which is at the start
        // 10000, but will decrease with 500 each time.
        health = health - damage; 
        //Log every time we hit it to see that we are actually hitting it
        console.log(`${name} health remaining: ${health}`);

    }
    // If there is no health left the loop will exit, and the monster is slain
    console.log(`Ouch, me ${monster.name} dead!`);
}
```


#### Övning 5 - Critta monstret!

```js
function slayTheMonster(weapon, monster){
    // We can save the health of the monster
    // by extracting it for the object. This is just
    // so we don't have to write `monster.health` every time.
    let health = monster.health;
    // we do the same with damage and name for easier handling
    const damage = weapon.damage;
    const name = monster.name;
    let dice;
    // While the monster has health left we will continue to strike it
    while (health > damage){
        
        // Each time we hit the monster, generate a new random number 
        // between 0 and 1. That will be our percentage of crit
        dice = Math.random();

        //If the dice is below 0.2 (20% crit chance) we will do double damange 
        //You could also just check if the typ of the weapon is "tenta" and 
        //that will do double damage as well
        if (dice < 0.2 || weapon.type.toLowerCase() === "tenta"){
            // Multiply damage by 2
            health = health - (damage*2);
            
            // So we know that we are critting
            console.log(`Ya crit boi! Double damage!`); 
        } else {
            // Else, do the usual damage
            health = health - damage; 
        }
        console.log(`${name} health remaining: ${health}`);

    }
    console.log(`Ouch, me ${monster.name} dead!`);
}
```

#### Övning 6 - Slay all the monsters

```js
// We can either create a new monster with the constructor pattern,
// or we can just create a simple object
const monsters = [
    new Monster("Grublak", 10000),
    new Monster("Slutbossen", 12000),
    {
        name: "Frufflak",
        health: 1000
    }
];

for (const monster of monsters){
    slayTheMonster(Tenta, monster);
}
```

### Prototypes

```js
let animal = {
  eat: function() {
    console.log("Omnomnomnom");
  },
  sleep: function() {
    console.log("zzZZzzzZZ");
  },
  isDangerous: false
}

function Dog() {
  this.bark = function() {
    console.log("Voffvoff");
  }
}

function Bird () {
  this.fly = function () {
    console.log("Flapflapflapflap")
  }
  isDangerous = true;
}

Dog.prototype = animal;
Bird.prototype = animal;

var fido = new Dog();
var kalle = new Bird();

let animalsArray = [fido, kalle];

kalle.sleep();
kalle.fly();
```

```js
/*============================================
=            Constructor Function            =
============================================*/

/**
 * Remember that these are only two ways of doing this and 
 * none of them are really considered "standard". It all depends
 * on what your project is, how big it is, what it will do etc.
 * These are just base principles which almost every other pattern use.
 * The main thing here is the prototype chain and how it works not specific
 * implementations
 */

/**
 * Constructor function that creates a new Country
 * @param {String} name       Name of country
 * @param {String} continent  Which continent
 * @param {Number} population Population of country
 */
function CountryConstructor(name, continent, population, pFemale){
  this.name = name;               //Every property is stored in this
  this.continent = continent;     //this is the object that is created
  this.population = population;   //when you call this function with new
}

/**
 * Prototype function that prints the population of the object
 * The function is bound to the Constructor function that
 * creates the objects, therefore every new object that is created
 * with CountryFunction will have these prototype-functions
 * @return {void} console.log
 */
CountryConstructor.prototype.printPopulation = function(){

  //Prints the name and the population
  console.log(`${this.name} population is ${this.population}`);
}

/**
 * Prototype function that prints the population of the object
 * @return {void} console.log
 */
CountryConstructor.prototype.printContinent = function(){

  //Prints the name and which continent
  console.log(`${this.name} is situated in ${this.continent}`);
}

/**
 * Function that loops through every property in an object and print
 * its value. The this.hasOwnProperty() is used to stop the for..in loop
 * from looping through inherited properties. Try removing it and see what
 * happens. It does not always have to be used but it's best practice
 * if you want to ensure not to loop through inherited properties
 * @return {void} console.log
 */
CountryConstructor.prototype.toString = function(){
  for (let prop in this){
      if(this.hasOwnProperty(prop)){
        console.log(this[prop]);
      }
    }
}

/**
 * Object created with the Constructor. Will have all the functions that
 * the CountryConstructor has because we did 
 * @type {Country}
 */
var USA = new CountryConstructor('USA', 'North America', 5004040404);

/**
 * Constructor function that inherits from Country by calling
 * Country in the contructor
 * @param {String} name       Name of city
 * @param {String} country    Name of country
 * @param {String} continent  Name of continent
 * @param {Number} population Total population
 */
function CityConstructor(name, country, continent, population){

  //We borrow the CountryConstructor and call it with new context.
  //this refers to the created CityConstructor Object. But we have 
  //a new property that differs from the CountryConstructor. So we 
  //have to add that too. We don't have data on the pFemale variable so
  //we can skip that.
  CountryConstructor.call(this, name, continent, population);
  this.country = country;
}

//For the City contructor to inherit the Country constructors
//functions we must assign the property manually
CityConstructor.prototype = new CountryConstructor();


//We can not create new Cities and Countries with these two Constructor-functions
let USA = new CountryConstructor('USA', 'North America', 50003030, 0.45);
let NewYork = new CityConstructor('New York', 'USA', 'North America', 5000000);

USA.printContinent();


/*=====================================
=            Object.create            =
=====================================*/

/**
 * Prototype object used for creating Country objects. Basically just
 * an object with a set of functions inside. Remeber that everything is
 * an object so it's not that weird that this is just a simple object. It doesn't
 * do exactly everything the constructor do but the base principle is the same.
 * You let an object inherit functions from another object. 
 * @type {Object}
 */
var Country = {
  printPopulation: function(){
    console.log(`${this.name} is situated in ${this.continent}`);
  },
  printContinent: function(){
    console.log(`${this.name} is situated in ${this.continent}`);
  }
}

/**
 * City object created by creating an object based on the
 * Country object. Inherits the functions that the Country Object has.
 * @type {Object}
 */
var City = Object.create(Country)

/**
 * Create an single City Object based on the City object. The City
 * object basicly just have the two inherited functions.
 * @type {Object}
 */
var Stockholm = Object.create(
    City, 
    {   name: { value: 'Stockholm' },   // { name: { value: 'Stockholm' } }
        country: { value: 'Sweden'},    // Awkward syntax but must be written
        continent: { value: 'Europe'},  // This way because it takes more params
        population: { value: 5000000}   // than just value. 
    }
);


Stockholm.printPopulation();
```
