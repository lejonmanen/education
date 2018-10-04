# General exercises

> All exercises are in swedish for now and all exercises are primarly written in PHP but can for the most part be applied to any programming language. This document is inconsistent, not complete and will be filled with more exercises

## Data types

### Dynamic types
Skapa dessa 6 olika variabler lägg ihop dem enligt instruktionerna nedan och `echoa` ut resultatet, diskutera med en klasskamrat och försök komma fram till varför vi får det resultat vi får. Svar finns under lösningsförslag. Litet exempel på hur dynamiskt typade språk fungerar!
```php
$firstName = "5Jesper";  //new name law since this summer, probably valid name
$lastName = "Gormy";
$age = "42";
$z_index = 999;          // I'm in front of you
$is_human = true;        // 🤖?
$is_a_chair = false;     //don't label me!
```
   
* Multiplicera `$age` med `$z_index`
* Dividera `$z_index` med `$is_a_chair`;
* Dividera `$z_index` med `$is_human`;
* Multiplicera `$is_human` med `$z_index`;
* Addera `$lastName` med `$age`;
* Addera `$firstName` med `$z_index`;
* Multiplicera `$lastName` med `$is_human`;


### Syntax error
**Vilka** av nedanstående alternativ sparar en sträng på rätt sätt och varför? Varför funkar inte de alternativ som inte fungerar?:
```
$_message = 'These are not the potatotes you're looking for';
$1message = "These are not the potatoes you're looking for";
$message = "These are not the potatoes you're looking for";
$jävla_skit = "These are not the potatoes you're looking for";
$Message1 = 'These are not the potatoes you\'re looking for';
```

## Control statements

### Has heading
Skapa en variabel vid namn `$has_heading` som innehåller värdet `true` eller `false`. Om värdet är `true` så ska en `<h1>`-tagg skrivas ut, annars ska inte en `<h1>`-tagg skrivas ut.

### Has heading or paragraph
Går så att föregående kod istället gör ett val så att den antingen skriver ut `<h1>`-tagg eller en `<p>`-tagg. Om värdet är `true` så ska en h1 skrivas ut, om värdet är `false` så ska en `<p>`-tagg skrivas ut.

### Energy drink
Skapa en variabel `$age`. Om värdet är under 18 så ska dina sida skriva ut _"Den där energidrycken är bara för vuxna unge man!_. Annars ska din sida skriva ut _"500kr tack"_


### Does it boil?
_Ms. Syntax Error_ vill ha ett alarm som anger om vattnet kokar eller inte. Hon vill även att man visar när det når 50 grader så att hon är beredd! Om det inte är 50 eller 100 grader så skall det endast säga att det inte kokar.

* Ange hur många grader vattnet är i en variabel.
* Om vattnet är 100 grader skriv ut: "_Vattnet kokar!_"
* Om vattnet är 50 grader skriv ut: _"Det är halvägs nu!"_
* Annars skriv ut: _"Vattnet kokar inte!"_


### A nice bath
_Boolean_ gillar att bada, dock tar vattnet ibland slut hemma och dessutom kan värmen variera ganska mycket. Skriv i PHP ett program som kollar om det finns vatten och om det är tillräckligt varmt. _Tips_ du kan ha en `if`-sats inuti en annan `if`-sats.

* Läs in om det finns vatten (`true` / `false`)
* Läs in hur många grader vattnet är.
* Om det finns vatten och det är varmare än 30 grader skriv ut: _”Varsågod och bada!”_
* Om det **INTE** finns vatten eller det är kallare än 30 grader skriv ut: _”Det går inte att bada.”__


### Sleep tight
Vi bestämmer oss för att ta sovmorgon och `echoar` ut att vi tar sovmorgon om det är en helgdag `$weekend` eller om vi har semester `$vacation`.

### Life puzzle
Skriv ut _"Gå upp, gå till jobbet, jobba, jobba, äta lunch"_ om variabeln `$age` är mellan 18 och 65. Om den är under 18 så skriv ut _"EFTERFEST!"_. Om den är över 65 skriv ut _"mmm, finska pinnar."_.

### All My Horses
_Iffy_ äger ett stall med hästar av typerna **A-ponny**, **B-ponny** och C-ponny**. _Iffy_ ska för första gången anordna en tävling. Tävlingsreglerna är följande: För att få tävla måste man fyllt **12 år**. För att få tävla på **A-ponny måste man väga under 30kg**, **B-ponny under 50kg** och **C-Ponny under 65kg**.

* Läs in användarens ålder med en variabel.
* Om åldern är under 12 år så:
    * Skriv ut: ”Du är för ung för att tävla!”
* Om åldern inte är under 12 år så
    * Läs in användarens vikt från variabel
    * Om vikten är under eller lika med 30kg skriv ut: ”A-ponny”
    * Om vikten är under eller lika med 50kg, och över 30kg skriv ut ”B-ponny”
    * Om vikten är under eller lika med 65kg och över 50kg skriv ut ”C-ponny”
    * Om vikten är över 65kg skriv ut ”Det finns inga ponnys för denna viktklass”

### Birthday boy

Du kör för snabbt och en polis stoppar dig. Skriv kod som beräknar följande:

* Om du kör under eller lika med 110 så får du ingen böter
* Om du kör mellan 110 och 120 så får du en lite böter
* Om du kör över 120 så får du en skitstor böter
* Om det dock är din födelsedag så höjs alla fartgränser så du får i alla lägen köra 5km/h fortare. Så gränserna för stor och liten böter ska höjas baserat på t.ex. variabeln `$is_birthday = true;`


### Ain't no party like my nannas tea party

Dags för kalas. Men är det ett bra kalas? Det baseras på om vi har tillräckligt med kaffe och finska pinnar.

* Om liter kaffe är minst `5` (liter) och mängden finska pinnar är minst `5` (kg :open_mouth:) så är det ett `echo "Bra kalas";`
* Om antingen kaffet är dubbelt så stor mängd som finska pinnar eller om finska pinnar är dubbelt så stor mängd som kaffet är det ett `echo "Nannas super party";`
* Om någon av mängderna dock är under `5` så blir det automatiskt ett `echo "Dåligt kalas";`
* Om det är någon som otroligt nog har bjudit in en clown så måste alla mängder dubblas för att det ska bli ett bra kalas.

### Black Jack

Om du har två värden som är större än 0. Skriv ut det värde som är **närmast 21** utan att gå över 21. Skriv ut `"Nu blev du tjock"` om båda värdena är över 21.

### Unlucky Sum

Om vi har 3 värden, returnera deras summa. Men om ett av värdena är **13** så räknas inte det värdet och alla värden som kommer efter det.
_exempel_
```
(1, 2, 3)    → 6
(1, 2, 13)   → 3
(1, 13, 3)   → 1
```

### Even or oddy

Om du har 3 värden, ett av dem är litet, ett är medium och ett är stort (t.ex. 1, 6, 12). `echoa` ut om värdena är jämnt fördelade. Alltså om det är lika långt mellan t.ex. 1 och 6 som det är mellan 6 och 12.
_exempel_
```
(2, 4, 6) → jämnt
(4, 6, 2) → jämnt
(4, 6, 3) → ojämnt
```

### What's for dinner?

Ditt program ska skriva ut vilket rätt som ska tillagas beroende på vilken dag som skickas in till switchen.

1. Läs in dag ifrån variabel
2. Om dagen är…
    * måndag skriv ut: Kyckling
    * tisdag skriv ut: Pannkaka
    * onsdag skriv ut: Ärtsoppa
    * torsdag skriv ut: Gryta
    * fredag skriv ut: Kalv
    * lördag skriv ut: Vegetariskt
    * söndag skriv ut: Kålsoppa, varför kålsoppa?


### What's for dinner 2

Ta din kod som du gjorde från förra uppgiften. Nu ska du dock med hjälp av en __fall-through__ göra så att programmet skriver ut "Kålsoppa" för fredag, lördag och söndag. Du ska alltså skriva "Kålsoppa" endast en gång men den switchen ska gälla för flera dagar.


## Loops

### Sum
Använd loopen från innan, fast istället för att skriva ut varje siffra: Lägg ihop sifforna i en ny variabel samt skriv ut den variabeln med `echo` efter loopen är slut. Du ska alltså lägga ihop alla värden till en variabel `$sum`.


### Every other number numbers
Skapa en `for`-loop som skriver ut varannat tal. Loopen ska gå från 0 till 10. Använd loopen från ovan.

### Reverse loop
Skriv en `for`-loop som skriver ut värden åt andra hållet, så att siffrorna skrivs ut **10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0**

### Even numbers
Skriv en `for`-loop med ett **condition**(`if`-sats) som gör så att endast siffror som är __jämna tal__ skrivs ut till sidan.

### Even while numbers
Skriv en `while`-loop som gör samma som övning _"Even numbers"_.

### do vs. whiles
Vad är skillnaden på de här två scripten? Vad kommer de båda skriva ut och varför?

```php
$num = 0;
while($num < 0){
    echo $num;
    $num++;
}
```

```php
$num = 0;
do{
    echo $num;
    $num++;
}while($num < 0);
```

### Sheeple
Mina får förökar sig snabbt och jag behöver ett php-script som kan räkna ut hur många de kommer att vara inom ett år. Varje månad kommer fåren att
multipliceras med 4. 

Använd dessa tre variabler nedanför:

```php
$numberOfSheep = 4;
$monthNumber = 1;
$monthsToPrint = 12;
```

För att sedan skriva ut detta för varje månad:

```bash
Output:
There will be 16 sheep after 1 month(s)!
There will be 64 sheep after 2 month(s)!

```

### You are the mjau machine

Jag vill ha ett program som mjauar!

Programmet fungerar som så att den frågar användaren efter hur många mjau den vill ha. Om användaren skriver "3", ska programmet svara med "mjau mjau mjau". Om användaren skriver "4" ska programmet svara med "mjau mjau mjau mjau". Om användaren skriver "0" ska programmet "avslutas", d.v.s. inte ta in mer input.
Programmet ska fungera som följande: 

* Läs in ett tal från en variabel.
* Om talet är inte är `0`
    a. Skriv lika många _"mjau"_ som talet, i rad
* Annars skriv ut **"😾"** eller något annat.


### Bus Card

Du ska köpa ett busskort. Det är ett kort som du laddar med pengar, därefter kan du åka på kortet tills pengarna tagit slut. Du vet att du ska åka för **K** kronor, där **K** är mindre än 10000. Att ladda kortet tar sin tid eftersom du endast kan ladda kortet med 500, 200 eller 100 kr i taget. Du vill utföra så några transaktioner som möjligt, men inte tanka på mer pengar än nödvändigt.

Om du ska åka för 800 kronor ska du alltså först ladda med 500, sen med 200, därefter med 100 kr. Om du däremot ska åka för 850 kronor ska du först ladda med 500 och därefter ladda med 200 två gånger. Visserligen går 50 kronor till spillo, men det är ändå det bästa alternativet.

Skriv en `if/else/else if`-sats som beräknar det minsta antalet transaktioner du behöver göra för att åka buss med de pengar du har, testa och kolla med 4 olika fall så att det blir rätt:

```
Körningsexempel 1:

Åka för? 850

Antal transaktioner: 3

Körningsexempel 2:

Åka för? 1800

Antal transaktioner: 5
```



### Sheeple epidemic

Det här funkar inte! Även om vi halverar antalet får är
det fortfarande alldeles för många. Implementera följande 
conditions innan vi går mot en epedemi!

1. Om månaden är en multipel av 4, hitta 75% av populationen.
Logga ut antalet i formatet som visas nedanför. Ta sedan bort
detta antal från totala antalet får.

2. Annars, om populationen är över 10000, hitta hälften av populationen.
Logga ut antalet i formatet som visas nedanför. Ta sedan bort 
detta antal från totala antalet får.

Använd följande format för att logga ut information:
Removing `<number>` sheep from the population.

Antalet får ska fortfarande alltid multipliceras med 4,
du behöver alltså inte editera någon redan existerande kod sedan tidigare


KORREKT OUTPUT:

There will be 16 sheep after 1 month(s)!

There will be 64 sheep after 2 month(s)!

There will be 256 sheep after 3 month(s)!

Removing 192 sheep from the population.

There will be 256 sheep after 4 month(s)!

There will be 1024 sheep after 5 month(s)!

There will be 4096 sheep after 6 month(s)!

There will be 16384 sheep after 7 month(s)!

Removing 12288 sheep from the population.

There will be 16384 sheep after 8 month(s)!

Removing 8192 sheep from the population.

There will be 32768 sheep after 9 month(s)!

Removing 16384 sheep from the population.

There will be 65536 sheep after 10 month(s)!

Removing 32768 sheep from the population.

There will be 131072 sheep after 11 month(s)!

Removing 98304 sheep from the population.

There will be 131072 sheep after 12 month(s)!


### FOR FOR - Multiplikation

Använd nested for loops, alltså en `for`-loop i en `for`-loop för att lösa denna uppgift.

Din kod ska skriva ut multiplikationstabellen upp till 10 enligt följande struktur:

```
1 2 3 4 5 6 7 8 9 10
2 4 6 8 10 12 14 16 20
3 6 9 12 15 18 21 24 27 30
```



## Arrays

### Access array
Vi ska börja med att skriva ut olika värden i en array. Om vi har en array som denna:

```php
$your_array = [23, 45, 54, 12, 77];
```

* Skriv ut det första och sista värdet (23 & 77) i denna array med hjälp av `echo`
* Vilka index ligger värdena på?

### Change array

Om vi redan har en array som den ovan kan vi även direkt ändra på ett visst värde på samma sätt som när vi tilldelar en variabel ett värde med `=`.

* Ändra sista värdet i `$your_array` genom att tilldela det nya värdet `1`.
* `echo`a arrayen efter att du har lagrat det nya värdet för att se att värdet verkligen har ändrats.

### Loop array

För att komma åt alla värden i en array vill vi ju inte skriva in varenda index, speciellt inte om vi inte vet hur lång arrayen är, alltså hur många värden som finns inuti den. Vi kan inte bara skriva ut hela innehållet i  arrayen med `echo $my_array` heller, det kommer bara att skriva ut hela arrayen och inte alla värden för sig. Tur att loopar finns.

Du har denna array:

```php
$best_array = [1, 2, 3, 4, 5];
```

Nu ska du loopa igenom arrayen och skriva ut varje värde i arrayen. Tänk på att längden av en array kan man ta ut med `count($best_array)` samt att varje värde i en array har ett index som man kommer åt värdet ifrån. Indexet är då detsamma som det nuvarande värdet på räknaren i loopen.

* [**`count`** @ php.net](http://php.net/manual/en/function.count.php)

### Sum array

Använd samma array som tidigare. Nu ska du dock loopa igenom arrayen och multiplicera varje värde i arrayen med summan av det föregående värdet. D.v.s, 1 * 2 * 3.. etc.

Spara värdet i en `$sum` och echoa sedan ut denna variabel efter att loopen har körts klart

### Filter array

Du ska utgå från följande array:

```php
$ok_array = ["fine", "FINE", "good", "what is this stuff?", "sweet", "i don't even live here"];
```

Du ska loopa igenom arrayen och echoa dess värden. Dock ska din loop inte skriva ut strängar som är längre än 5 tecken. `"fine"`, `"FINE"`, `"good"` och `"sweet"` ska alltså skrivas ut men inte `"whatisthisstuff?"` och `"i don't even live here"`. 

För att komma åt hur lång en sträng är kan man använda `strlen()`, en inbyggd funktion: [**`strlen()`** @ php.net](http://php.net/manual/en/function.strlen.php)

### Filter array 2

```php
$worst_array_yet = ["string", true, 42, "another string", 54, true, 1];
```

För att få ut vilket värde en variabel är kan vi använda `is_string()` t.e.x. som returnerar true eller false baserat på om värdet är en sträng. Detta kan vi sedan använda i en if-sats.

Du ska loopa igenom arrayen `$worst_array_yet` och ska sedan `echoa` ut varje sträng som förekommer i arrayen. Men om värdet i arrayen är något annat ska det värdet läggas till i `$sum;` för att sedan efter att loopen är klar `echo`a ut.

## Functions

### Multiply
* Skapa en funktion: `multiply`, som tar in 2 _parametrar_.
I funktionen, multiplicera dessa nummer med varandra och  `echo` resultatet av multiplikationen. Du får använda vilka namn du vill på parametrarna.
* Kalla på din funktion multiply med siffrorna 8,4 som _argument_
* Om du gjort rätt ska du få siffran 32.

### Calculate
* Skapa en funktion som heter `calculate` och som istället tar 3 parametrar och sedan multiplicerar de två första parametrarna med varandra och delar värdet med den tredje parametern, alltså: `param1 * param2 / param3`. Funktionen ska sedan `echo` ut svaret.
* Kalla sedan på din funktion med valfria värden.

### Highest number
* Skriv en funktion som heter `highest_number` som tar två tal som parametrar.
* Funktionen ska sedan jämföra vilket av talet som är störst och `echo` det största talet.
* Kalla på din funktion med två valfria värden.

### Refactor
Koden ovan är dock inte optimal. För det mesta vill vi att funktioner endast returnerar värden. En funktions uppgift ska vara att returnera värden så att vi kan återanvända det värdet och sedan forsätta göra mer beräkningar på det. När vi har massa `echo` på det här sättet blir koden svårare att återanvända så vi vill nu skriva om våra funktioner så att de endast returnerar värden.

__Refaktorera__ dina funktioner som du tidigare skapade: 

* De två första funktionerna (multiply och calculate) ska __returnera__ det slutgiltiga värdet av beräkningarna. Sedan måste du spara värdena för att sedan använda `echo` på dem.
* Den tredje funktionen `highest_number` ska __returnera__ det högsta värdet av de två värden som skickas in som parametrar. Om dock värdet inte är ett nummer ska funktionen returnera `false` och om de båda parametrarna är samma värde ska funktionen returnera _"Samma värde"_

Spara värdena som returneras på följande sätt:

```php
$multiply_answer = multiply(5,5);
echo $multiply_answer;
```

### Refactor mjau machine
Eftersom __alla__ gillar katter så ska vi refaktorera vår Mjau Machine 🙀

Du ska skriva en funktion som ska ha samma funktionalitet som vår ursprungliga Mjau Machine från tidigare övningar men nu i form av en funktion.


### Even or odd function

Använd while-loopen du skapade från en av de tidigare uppgifter.

Denna loop ska du nu göra om till en funktion som tar 2 parametrar.
* Första parametern ska vara siffran som loppen ska räkna ner ifrån, alltså hur många värden funktionen ska gå igenom.
* Andra parametern ska vara om funktionen ska skriva ut jämna eller ojämna värden.

### Multiply without multiplication

Skriv en funktion som tar 2 parametrar. Parametrarna ska vara två heltal. Funktionen ska multiplicera heltalen utan att använda `*`-operatorn.


### Print string length
Skriv en funktion som tar in en parameter. Parametern ska vara en string. Funktionen ska sedan returnera strängens längd på detta sätt:

```bash
"Strängen du matade in är 14 tecken lång"
```

### Convert string

Skapa en funktion som heter `convert_string`, funktionen ska ta **två parametrar**. Den första parametern ska vara en sträng som skickas med, typ: _"Goodbye World"_. Den andra parametern som skickas med ska bestämma om strängen ska konverteras till bara stora bokstäver eller bara små bokstäver. Till detta kan man använda hjälpfunktionen: `strtolower($string)` och `strtoupper($string)`

### Return last char
Skapa en funktion som tar en parameter, argumentet som skickas in ska vara en sträng. Funktionen ska sedan returnera det sista tecknet i strängen som skickas in.

### Make paragraph
Skriv en funktion med namnet make_paragraph som skriver ut en sträng som HTML-elementet `<p>`. Exempel: _"hej"__ ska skrivas ut som _"`<p>hej</p>`"_. Funktionen ska ha en parameter, som är strängen som ska skrivas ut, och den ska inte returnera något bara `echo`a ut.

### Evolve make paragraph
Funktionen `make_paragraph()` är lite begränsad. Tänk om vi vill göra `<h1>`-taggar? Eller `<h2>`, `<h3>` osv. Skriv en ny funktion med namnet make_heading. Funktionen behöver veta strängen som ska skrivas ut och vilken heading det ska vara. Den behöver alltså två parametrar.

### Make tag
Nu har vi två funktioner som vi kan använda för att skapa HTML-paragrafer och headings. Men det blir väldigt många funktioner om vi ska ha en funktion för varje möjligt HTML-element. Vi behöver en funktion som kan göra flera sorters element. Skriv en funktion make_tag som kan göra alla sorters HTML-element.

### Make tag with style
Förbättra `make_tag` så att man kan ange inline styles också. (Eller href för länkar)
Exempel: `<p style="color: hotpink;">Exempeltext</p>`

### Newline
Skriv en funktion som gör om alla nyrader i en sträng till `<br>`-element. Funktionen ska ta strängen som parameter och returnera en ny sträng. En nyrad i PHP skrivs `'\n'`.

### Random array generator
Skriv en funktion som returnerar en array med slumpade tal. Använd [`mt_rand()`](http://php.net/manual/en/function.mt-rand.php) för att göra slumptal. Hur många parametrar behöver funktionen?

### Array to list
Skriv en funktion som gör om en array till en lista i HTML. Använd funktionen make_tag. Exempel: `make_list( [1, 2] )` → `"<ul> <li>1</li> <li>2</li> </ul>"`

### Generate random color
Skriv en funktion som genererar en random färg.

### Round my number
Skriv en funktion som avrundar en float till närmaste heltal med hjälp av typecast.
```
Exempel: round(3.9) → 3, round(5.5) → 6.
```

### Decimal to string
Skriv en funktion som gör om ett decimaltal till en sträng. Strängen ska använda decimalkomma i stället för decimalpunkt. Exempel: float_to_string(75.5) → "75,5".

### Mean value
Skriv en funktion som räknar ut summan av alla tal i en array. Skriv en annan som räknar ut medelvärdet.

### Weekday to number
Skriv en funktion som tar en sträng som motsvarar en veckodag som parameter och returnerar en siffra. Om strängen är "måndag" ska funktionen returnera 1, "tisdag" ska bli 2 och "söndag" ska bli 7.
Funktionen ska fungera oavsett om veckodagen står med små eller stora bokstäver.

## Strings

### Split strings
Skriv kod som gör om en sträng, en mening, till en array av strängar som exemplet nedan.

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

### Capitalize first word

Skriv kod som gör om första tecknet i en mening till stor bokstav.

_exempel_
```
'hello my name is jesper' ->
'Hello my name is jesper'
```

### Capitalize words

Skriv kod som gör om alla första tecken i samtliga ord till stor bokstav.

_exempel_
```
'hello my name is jesper' ->
'Hello My Name Is Jesper'
```

### Excerpt

Skriv kod som gör om en större text till ett excerpt och där du kan bestämma hur långt utdraget ska vara.

_exempel_
```
'This is a long text that describes the content of my blogpost, on some sites I wish to shorten this text' ->
'This is a long text that describes the content of my blogpost...'
```

### Case converter
Skriv kod som gör om snake_case till camelCase.

_exempel_
```
'my_snake_function' ->
'mySnakeFunction'
```

### Reverse string

Skriv kod som returnerar strängen baklänges

exempel
```
'jesper' ->
'repsej'
```

### Rovarspraaak

Skriv kod som översätter en sträng till rövarspråk.

_exempel_
```
"Hej mitt namn är Waboo" ->
"Hohejoj momitottot nonamomnon äror Wawaboboo"
```

## Solutions

### Data types

* Multiplicera `$age` med `$z_index`
    *  Alla strängar som bara är nummer blir automatiskt castade, konverterade, till ett nummer så vi kan använda operatorer på strängar.
* Dividera `$z_index` med `$is_a_chair`
    *  `false`  blir alltid **0**, och vi får inte dividera med 0 så här kommer vi att få ett error.  
* Dividera `$z_index` med `$is_human`
    * `true` blir alltid **1**, så här får vi dock ett värde! 
* Multiplicera `$is_human` med `$z_index`
    * Samma här, detta blir 999 * 1
* Addera `$lastName` med `$age`
    * Om dock strängen inte är ett nummer så kommer strängen att ignoreras och enbart det ena värdet kommer att skrivas ut 
* Addera `$firstName` med `$z_index`
    * Dock om strängen har en siffra INNAN själva strängen börjar så kommer den siffran att användas och göra en beräkning, så det här blir faktiskt 5 * 999 
* Multiplicera `$lastName` med `$is_human`;
    * Samma här, `"5Jesper"` blir till 5 och `true` blir till 1. Så 5*1 == 5

Relaterat till detta: [**PHP.net ~ Type Juggling**](http://php.net/manual/en/language.types.type-juggling.php)

2.
```
// the you're makes it so that the string ends at you'
$_message = 'These are not the potatotes you're looking for';
// variable can not start with number
$1message = "These are not the potatoes you're looking for";
//this is fine
$message = "These are not the potatoes you're looking for";
//this is also fine but not recommended to have åäö in name
$jävla_skit = "These are not the potatoes you're looking for";
//this is also fine because we escaped the ' with \'
$Message1 = 'These are not the potatoes you\'re looking for';
```

### Control statements

1.
```php
$has_header = true;
if($has_heading){
    echo "<h1> It'sa heading! </h1>";
}
```

2.
```php
$has_header = true;
if($has_heading){
    echo "<h1> It'sa heading! </h1>";
} else {
    echo "<p> It'sa paragraph! </p>";
}
```

3.
```php
$age = 17;
//$age is less than 18 so this evaluates to `true`
if($age < 18){
    echo "Den där energidrycken är bara för vuxna unge man!";
} else {
    echo "500kr tack";
}

```

4.
```php
$does_it_boil = 100;

if($doesItBoil == 100){
    echo "Det kokar!";
}else if ($doesItBoil == 50){
    echo "Det är halvvägs nu!";
}else{
    echo "Vattnet kokar inte";
}
```

5.
```php
$water = true;
$degrees = 35;

if($water){
    /*Bara om det finns vatten behöver vi kolla hur många grader vattnet är
    annars kan vi hoppa direkt till else-satsen i slutet*/
    //Kolla om graderna är över 30
    if ($degrees > 30){
        echo "Varsågod och bada!";
    /*Om det inte är över 30 så är det under 30, d.v.s vi behöver 
    inte göra en ytterligare if-sats som kollar det */
    }else{
       echo "Det går inte att bada";
    }
    //Om det inte finns vatten kan vi hoppa till en else-sats istället
}else{
    echo "Det går inte att bada";
}
```

6.
```php
$weekend = true;
$vacation = false;

if($vacation){
    echo "Sleeeep";
} else if ($weekend){
    echo "Sleeeep";
} else {
    echo "Gotta work!";
}

```

7.
```php
$age = 78;

if($age > 18 && $age < 65){
    echo "Gå upp, gå till jobbet, jobba, jobba, äta lunch";
} else if ($age < 18) {
    echo "EFTERFEST!";
} else {
    echo "mm, finska pinnar";
}
```

8.
```php
/*Vi behöver bara kolla vilken ponny som behövs om ålder är inne, därför kan
vi lägga till de if-satser som kollar vikt inuti vår första if-sats. Det gör 
så att vi slipper köra kod som inte behövs köras. */
$age = 12;
$weight = 50;

if ($age > 12){
    /*Kollar först om vikten är mindre än 30. Vad vi kollar först är dock beroende av
    vilka värden vi förväntar oss, nu förväntar vi oss att de flesta värden ska vara
    under 65. Vi skulle t.ex. kunna kolla först om vikten är över 65*/
    if($weight <= 30){
        echo 'A-ponny';
    //Sedan kollar vi spannet mellan 30 och 50
    }else if($weight <= 50 && $weight > 30){
        echo 'B-ponny';
    //Till sist kollar vi spannet mellan 50 och 65
    }else if($weight <= 65 && $weight > 50){
        echo 'C-ponny';
    }else{
        echo 'Det finns inga ponnys för denna viktklass';
    }
}else{
    echo 'Du är för ung för att tävla!';
}
```
#### Birthday boy
```php
$speed = 80;
$is_birthday = true;
$birthdayBonus = 0;

//Add the bonus only if it birthday is true, else it will be zero
if($is_birthday){
    $birthdayBonus = 5;
}

//Subtract the bonus from the speed, then compare
if(($speed - $birthdayBonus) <= 110){
    echo "Relax you are doing fine";
} else if (($speed - $birthdayBonus) > 110 && ($speed - $birthdayBonus) <= 120){
    echo "You get the small ticket";
} else{
    echo "You are breaking the law and your mothers heart! This ticket is huge!";
}
```


#### Nannas tea party
```php
$kaffe = 10;
$finska_pinnar = 5;
$clown = true;

//Divide all values if the clown is present
if($clown){
    $kaffe = $kaffe/2;
    $finska_pinnar = $finska_pinnar/2;
}

//If any of the values is bad, we know the party is bad at the start
if( $kaffe < 5 || $finska_pinnar < 5 ){
    echo "Dåligt kalas!";
//else we continue with our checks
} else if( ($kaffe/$finska_pinnar) >= 2 || ($finska_pinnar/$kaffe) >= 2){
    echo "Nannas super party!";
} else{
    echo "Bra kalas!";
}   
```

#### Black Jack

```php
$card_1 = 19;
$card_2 = 21;

if($card_1 > 21 && $card_2 > 21){
    echo "Nu blev du tjock";
} else{
    //We know we need to check against 21, so check the difference against 21
    //the value that is the smallest wins!
    $diff_card_1 = 21 - $card_1;
    $diff_card_2 = 21 - $card_2;
    if($diff_card_1 < $diff_card_2 && $card_1 < 22){
        echo $card_1;
    } else if($card_2 < 22){
        echo $card_2;
    } else{
      echo $card_1;
    }
}
```

#### Unlucky sum

```php
$a = 1;
$b = 13;
$c = 5;
$sum = 0; //store the sum

if($a != 13){
  //Take the previous value of $sum and add the new value
  $sum = $sum + $a;
  if($b != 13){
    $sum = $sum + $b;
    if($c != 13){
        $sum = $sum + $c;
    }
  }
}

//Either way, we want to show the sum.
echo $sum;

```

#### Jämn fördelning

```php
$a = 2;
$b = 4;
$c = 6;

//It would also be a good idea to check if any of the values is negative and
//run multiple checks here, but i think you get the gist of it :)
if(($b - $a) == ($c  - $b)){
    echo "Jämnt fördelat!";
} else{
    echo "Ojämnt fördelat!";
}
```

#### Vad blir det för middag 1

```php
$day = "måndag";

switch($day){
    case "måndag":
        echo 'Kyckling';
        break;
    case "tisdag":
        echo 'Pannkaka';
        break;
    case "onsdag":
        echo 'Ärtsoppa';
        break;
    case "torsdag":
        echo 'Gryta';
        break;
    case "fredag":
        echo 'Kalv';
        break;
    case "lördag":
        echo 'Vegetariskt';
        break;
    case "söndag":
        echo 'Kålsoppa';
        break;
}
```

#### Vad blir det för middag 2


```php
switch($day){
    case "måndag":
        echo 'Kyckling';
        break;
    case "tisdag":
        echo 'Pannkaka';
        break;
    case "onsdag":
        echo 'Ärtsoppa';
        break;
    case "torsdag":
        echo 'Gryta';
        break;
    //Just remove the echos and breaks, it will go through and print kålsoppa
    //for every case here
    case "fredag":
    case "lördag":
    case "söndag":
        echo 'Kålsoppa';
        break;
}
```

### Loops

1.
```php
//them sum is zero from start
$sum = 0;
//i++ is a shorthand for writing '$i = $i + 1'
for($i = 0; $i <= 10; i++){
    //we must always add the new value + the old sum
    //otherwise we will only store the newest value
    $sum = $sum + $i;
}
```

2.
```php
for($i = 0; $i < 10; $i = $i + 2){
    echo $i;
}
```

3.

```php
//start from 10, and as long as $i is above 0, echo.
//instead of doing $i = $i + 1 we are doing $i = $i - 1; reverse!
for($i = 10; $i > 0; i--){
    echo $i;
}
```

4.
```php
for($i = 0; $i < 10; $i++){
    if( $i % 2 == 0){
        echo $i;
    }
}
```


5.
```php
$number = 0;

while($number < 10){
    //If it's a even number, we wont get rest value, we will have 0
    if( $number % 2 == 0){
        echo $number
    }
    //If we don't change the value of number, this loop will never end
    //the condition will always be met
    $number++;
}
```

6.

Eftersom vårt **condition** redan är mött så går vi aldrig in i `while`-loopen, vilket betyder att loopen aldrig körs. Men med en `do while` så går vi alltid in i loopen minst 1 gång, SEDAN kollar vi villkoret. Villkoret stämmer fortfarande inte men då har vi redan hunnit köra vår `do`.

7.
```php
$numberOfSheep = 4;
$monthNumber = 1;
$monthsToPrint = 12;

for ($monthNumber; $monthNumber <= $monthsToPrint; $monthNumber++){

    $numberOfSheep = $numberOfSheep * 4;
    echo 'There will be ' . $numberOfSheep . ' sheeps after ' . $monthNumber +' months(s)!';
}
```

8.
```php
$number_of_mjau = 10;    
if($number_of_mjau == 0){
    echo '😾';
} else {
    $all_the_mjaus = '';
    for($i = 0; $i <= $number_of_mjau; $i++){
        $all_the_mjaus = $all_the_mjaus . 'mjau ';
    }
    echo $all_the_mjaus;
}
```

### Arrays

1.
```php
$your_array = [23, 45, 54, 12, 77];
echo $your_array[0]; //index 0
echo $your_array[4]; //Last index is 4, but length is 5
```

2.
```php
$your_array = [23, 45, 54, 12, 77];
$your_array[4] = 1;
echo $your_array[4];
```

3.
```php
$best_array = [1, 2, 3, 4, 5];
//The number of times the loop will runt is based on the length of the array
//5 items in the array == count($best_array) returns 5. 
for($i = 0; $i < count($best_array); $i++){
    //$i is 0,1,2,3,4, this can be used to access the value at these indexes
    echo $best_array[$i];
}

```

4.
```php
$best_array = [1, 2, 3, 4, 5];
$sum = 1
//The number of times the loop will runt is based on the length of the array
//5 items in the array == count($best_array) returns 5. 
for($i = 0; $i < count($best_array); $i++){
    //$i is 0,1,2,3,4, this can be used to access the value at these indexes
    $sum = $sum * $best_array[$i];
}
echo $sum;
```

5.
```php
$ok_array = ["fine", "FINE", "good", "what is this stuff?", "sweet", "i don't even live here"];

for($i = 0; $i < count($ok_array); $i++){
    //$i is 0,1,2,3,4, this can be used to access the value at these indexes
    $current_string = $ok_array[$i];
    if(strlen($current_string) <= 5){
        echo $current_string;
    }
}
```


6.

```php
$worst_array_yet = ["string", true, 42, "another string", 54, true, 12];
$sum = 0;

for($i = 0; $i < count($worst_array_yet); $i++){
    //$i is 0,1,2,3,4, this can be used to access the value at these indexes
    $current_value = $ok_array[$i];
    if(is_string($current_value)){
        echo $current_value;
    } else{
        $sum = $sum + $current_value;
    }
}

echo $sum;
```

### Functions

1.
```php
/*
 * x, y are parameters
 */
function multiply($x,$y){
   echo $x * $y;
}

//Use case, when called, it will echo the result of the arguments
multiply(5,5);
```

2.
```php
function calculate($x,$y,$z){
    echo ($x*$y) / $z;
}

//use case
calculate(5,10,2);
```

3.
```php
function highest_number($x,$y){
    /* If x is higher than y, return x */
    if( $x > $y){
        echo $x;
    }
    /* or else y is higher */
    else{
        echo $y;
    }
}

//Use case
highestNumber(5,4);

```

4.
```php
function multiply($x,$y){
   return $x * $y;
}

//Use case, we must first store the value
$answer = multiply(5,5);
echo $answer;
//or we can print it directly
//echo multiply(5,5);

function calculate($x,$y,$z){
    return ($x*$y) / $z;
}

//use case
$answer = calculate(5,10,2);
echo $answer

```

5. 
```php
function mjau_machine($number_of_mjau){ 
    if($number_of_mjau == 0){
        return '😾';
    } else {
        $all_the_mjaus = '';
        for($i = 0; $i <= $number_of_mjau; $i++){
            $all_the_mjaus = $all_the_mjaus . 'mjau ';
     }
    return $all_the_mjaus;
    }
}

echo mjau_machine(10);
```

6.
```php
function even_or_odd($number, $is_even){
    $numbers = '';
    while($number < 10){
        //If it's a even number, we wont get rest value, we will have 0
        if( $number % 2 == $is_even){
            $numbers = $numbers . $number;
        }
        $number++;
    }
    return $numbers;
}

even_or_odd(10, 0)
```

7.
```php
function calcy($x,$y){
    $sum = 0;
    /* x * y är samma sak som att addera x, y antal gånger. Vi kör alltså loopen
    i det här fallet y antal gånger, alltså 4 i vårat fall.
    Värdet som läggs till i sum är 5 i detta fall, alltså:
    5 + 5 + 5 + 5 */
    for ($i = 0; $i <= $y ; $i++){
        $sum = $sum + $x;
    }
    return $sum;
}

$calcyAnswer = calcy(5,4);
echo $calcyAnswer;

```

8.
```php
function string_checker($string_to_check){
    //Use the built in function `strlen`
    $string_length = strlen($string_to_check);
    return "Strängen du matade in är " + $string_length + " tecken lång";
}

//Vi skickar in en valfri sträng som argument
echo string_checker('Huburru Hubburru');

```

9.
```php
function string_converter($string_to_convert, $up_or_down){
    if($up_or_down == 1){
        return strtoupper($string_to_convert);
    } else{
        return strtolower($string_to_convert);
    }
}

echo string_converter("Hello", 1);
```

10.
```php
function string_checker($string_to_check){
    //Use substring, which extract a part of a string,
    //we can use a negative index to start from the back
    return substr($stringToCheck, -1);
}

echo string_checker("Hubburu"); //u
```


11, 12, 13
```php
function make_paragraph($hej) {
    echo "<p> $hej </p>";
}
function make_heading($text, $number) {
    /*  
     *  Alternative syntax:
     *  echo "<h" . $number . ">" 
     *  . $text . "</h" . $number . ">";
     */
    echo "<h$number> $text </h$number>";
}
function make_tag($text, $tag) {
    echo "<$tag> $text </$tag>";
}
```

14. 
```php
function make_tag($text, $tag, $style, $href) {
    //if values are empty, return tag as is 
    if ( $style === '' && $href === '' ) {
        echo "<$tag> $text </$tag>";
    }
    /*
     * Escape "" with \ like this: \" so they are treated as actual quotes and 
     * not a part of the string in PHP.
     */
    else if ( $style === '' && $href !== '' ) {
        echo "<$tag href=\"$href\">$text</$tag>";
    }
    else if ( $style !== '' && $href === '' ) {
        echo "<$tag style=\"$style\">$text</$tag>";
    }
    else {
        echo "<$tag style=\"$style\" href=\"$href\">$text</$tag>";
    }
}
```

15. 
```php
function replace_linebreaks($string) {
    /* str_replace, built in function to replace every occurence of a character */
    $resultat = str_replace("\n", '<br />', $string);
    return $resultat;
}
//Use case
$proper_linebreaks = replace_linebreaks("en\nsträng\nmed\nmassa\nradbrytningar");
echo $proper_linebreaks;
```

16.
```php
function random_number_array_generator() {
    //array to store the values
    $array = [];
    //create 5 random numbers
    for ($i=0; $i < 5; $i++) {
        /*
         * `mt_rand`, built in function that returns number between
         * a range, in this case: 1 to 100
         */
        $random = mt_rand(1, 100);
        //push each value to the array, add it at the end
        array_push($array, $random);
    }
    //When the array is created, when the loop is finished. Return it.
    return $array;
}

//Store the  returned array in `$my_array`
$my_array = random_number_array_generator();
//Then loop through each value
foreach( $my_array as $value ) {
    echo "<p>Random value is: $value</p>";
}
```


17.
```php
function make_list($array) {
    //Open up a `<ul>`-element
    $list = "<ul> ";
    foreach( $array as $value ) {
        //$text, $tag, $style, $href, function we created before
        $li = make_tag($value, "li", "", "");
        $list = $list . $li;
    }
    //close the list when all items are added
    $list = $list . " </ul>";
    //Return the list
    return $list
}

//Use case
$my_array = random_number_array_generator();
$html_lista = make_list($my_array);
echo $html_lista;
```


18, 19.
```php
function capitalize($text) {
        // "david" ska bli "David"
        // plocka ut första bokstaven
        // och gör den stor
        // lägg ihop med resten av strängen
        // returnera
        $first = substr($text, 0, 1);
        $first = strtoupper($first);
        $rest = substr($text, 1);
        return $first . $rest;
    }
//Use case
$text = capitalize($text);
echo "<p>$text</p>";
```

20.
```php
function random_color(){
    //A color is a combination of red, green and blue values
    $r = mt_rand(0, 256);
    $g = mt_rand(0, 256);
    $b = mt_rand(0, 256);
    echo "rgb($r,$g,$b)";
}
```

21 .
```php
function my_round($x) {
    //(int) casts variable to int if not int, will convert float to int
    return (int)($x + 0.5);
}
```

22 .
```php
function float_to_string($float) {
    //converts our float to a string so we can replace certain
    //values in the string, for example switch . to ,
    return str_replace(".", ",", (string)$float);
}
```

23.
```php
function sum($array) {
    $sum_of_array = 0;
    for( $i=0; $i < count($array); $i++ ) {
        $sum_of_array = $sum_of_array + $array[$i];
    }
    return $sum_of_array;
}
```

24.
```php
function weekday_to_number($weekday) {
    /*
     * Always be sure to convert to lowercase or uppercase
     * when comparing case sensitive strings
     */
    $weekday = strtolower($weekday);
    switch($weekday) {
        case "måndag": 
            return 1;
        case "tisdag": 
            return 2;
        case "onsdag": 
            return 3;
        case "torsdag": 
            return 4;
        case "fredag": 
            return 5;
        case "lördag": 
            return 6;
        case "söndag": 
            return 7;
        default: 
            return "ERROR";
        }
    }
```
