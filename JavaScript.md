# Teorihandboken - JavaScript (JS)

Studerande Shaker Nasser
![Teroihandboken - Tips](images/JavaS-tips.png)

## JS 1.1 JavaScript / ECMAScript

Javascript är ett programmeringsspråk som utgavs 1995 och skapades av Brendan Eich och utvecklades tillsammans med många andra utvecklare. Programmeringsspråket utgör funktionalitet till webbsidor och gör dem dynamiska. Javascript tillsammans med HTML och CSS utgör dem tre grundläggande byggstenar i en dymanisk och full funktionuell webbsida. För att enklare kunna förklara javacript så kan man förklara med vad som "händer" på en webbsida när man navigerar, fyller i formulär eller trycker på en knapp. Javascripts vanligaste användningsområden är att det bestämmer vad som händer när användaren intergerar på olika sätt.

För att koden skall köras på ett rätt sätt så ska man definera variabler i dem ordningen som koden skall köras. Detta gör man pga att JavaScript läser koden uppifrån och nedåt.
En variabel är en placeholder för en typ av datatyp/värde. I Javascript finns det följande varibaler:
Automatically

- Using var (äldre webbläsare)
- Using let
- Using const

Dessa datatyper/värden finns i JavaScript:

- String
- Boolean
- Number
- Array
- Object
- Undefined
- Null

Här nedan följer ex på hur koden exkeveras (körs) med hjälp av console.log funktionen.

```js
let x = 1
console.log(x)
```

Javascript har väldigt många funktioner, en av dem mesta användabara i den nuvarande webbutveckling är API:er. Vi använder API:er i tex väderprogonos webbsidor (Klart.se) eller tex bilupplysningssidor (biluppgifter.se)
Dessa webbsidor hämtar information från en annan källa. Dett kallas för Applikationsprogrammeringsgränssnitt. JavaScript underlättar hämtning av API:er som kan matas ut i HTML format som visas till användaren.

ECMAScript (förkortat ES) är en standard för skriptspråk och används huvudsakligen för att definiera JavaScript. ECMAScript-standarden har utvecklats av organisationen Ecma International och syftar till att standardisera kärnan i JavaScript för att säkerställa att olika webbläsare kan tolka och köra JavaScript på ett enhetligt sätt.

Skillnaden mellan ECMAScript och JavaScript är subtil eftersom JavaScript är en praktiskt genomförande av ECMAScript-standarden. ECMAScript kan ses som den formella specifikationen, medan JavaScript är den mest kända genomförandet av denna specifikation. Termerna används ofta utbytbart, och i praktiken hänvisar de oftast till samma sak, särskilt när det gäller webbutveckling.

Nya versioner av ECMAScript släpps med nya funktioner och förbättringar. Till exempel används termen "ES6" ofta för att referera till ECMAScript 2015, som var en betydande uppdatering med många nya funktioner som arrow functions, template literals och block scope variables.

1. https://www.exsitec.se/blogg/vad-ar-javascript
2. https://www.freecodecamp.org/news/javascript
3. Bok Eloquent JavaScript - Third Edt. - Marijn Haverbeke ISBN: 8006636608372

## JS 1.2 JavaScript-ramverk och -bibliotek

v. 11

## JS 1.3 Promises

Promises standardiserades efter den femte utgåvan av ECMAScript där de asynkrona funktionerna blir alltmer populära. Promises, även kallade "framtida löften" på svenska, används för att hantera asynkrona operationer på ett mer strukturerat sätt och erbjuder ett sätt att hantera och samordna flera asynkrona operationer. Med promises kan man koppla ihop asynkrona uppgifter med metoderna async och await, vilket minskar användningen av callback-funktioner. Detta gör koden mer läsbar och lättare att utveckla för framtida projekt.

Promise presenterar värde så som pending (väntande), fullfied (uppfyllt) eller rejected (avvisat). När en promise är "pending", så väntar den på att en asynkron operation ska slutföras. När operationen slutförs, går promisen över till antingen "fulfilled" eller "rejected" beroende på om operationen lyckades eller misslyckades.


1. https://sunlightmedia.org/sv/tips-f%C3%B6r-javascript/
2. https://www.freecodecamp.org/news/javascript-promise-object-explained/

## JS 1.4 OOP i JavaScript

JavaScript är ett OOP-skriptspråk. OOP är fortkortning till Obejktorinterad programmering (Eng: Object Oriented Programming). Programmeringsmetoden gör det möljigt att använda sig av uppsättning av objekt som integerar med varandra och detta skapar effektiv och kraftfulla konstruktion vid stora program.

Objekter är instanser av olika klasser.

För att skapa en objekt börjar man med att deklarera variabeln och sedan namnger man egenskaperna mellan måsvingarna.

```Js

function Person(hometown, hobby, birthday) {
  this.hometown = hometown;
  this.hobby = hobby;
  this.birthday = birthday;
}

// Skapa en instans av Person
var aboutShaker = new Person("Skärholmen, Stockholm", "eating", {month: 4, day: 18, year: 1997});
```


1. https://www.freecodecamp.org/news/how-javascript-implements-oop/
2. https://sv.khanacademy.org/computing/computer-programming/programming/objects/a/review-objects

## JS 1.5 DOM-manipulation

DOM-manipulation är en viktigt verktyg i Javascript där utvecklare kan integerera med HTML element för att skapa en dymanisk och interaktiv plattform. Genom att komma åt element och modifera struktur, styling och innehåll så blir användarupplevelsen mer dynamisk än att bara använda en statisk sida. 

För att manilupera DOM trädet så behöver man komma åt elementen genom att använda DOM objekt vilket representerar hela HTML dokumentet. För att komma åt dessa element kan man använda följande exempel:

```Js

// Hämtar ett element efter dess ID
const headerElement = document.getElementById('header');

// Hämtar element efter klassnamn
const paragraphs = document.getElementsByClassName('paragraph');

// Hämtar element efter taggnamn
const images = document.getElementsByTagName('img');
```

När man har lyckats komma åt dessa element så kan man modifera dess innehåll genom att använda detta egenskap: 

```Js

// Modifiera innehållet i ett element
headerElement.innerHTML = 'Chas Academy';

// Här nedan så kan vi se exempel på hur man kan modifera stylingen. 

// Lägger till en klickhändelselyssnare på knappen
colorButton.addEventListener('click', function() {
// Ändrar färgstilen på stycket
myParagraph.style.color = 'blue';
});

```

1. https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents
2. https://www.freecodecamp.org/news/dom-manipulation-in-javascript/
3. https://www.honeybadger.io/blog/javascript-oop/


## JS 1.6 HTTP-requests

Kommunikationen mellan frontend och backend bygger på HTTP-förfrågningar. Genom detta protokoll kan vi använda funktioner som kräver integration med backend, vilket förenklar hanteringen av data som behöver lagras på en server. För att interagera med en server behöver vi förstå HTTP-protokollet och dess metoder. Vi kan använda HTTP-metoder såsom CRUD (Create, Read, Update, Delete) med hjälp av dedikerade HTTP-verb som POST, GET, PUT/PATCH och DELETE.

När vi kommunicerar med servern skickar den tillbaka ett svar beroende på förfrågans giltighet. Om förfrågan lyckas, skickar servern tillbaka data vanligtvis i JSON-format (ibland XML). Om förfrågan misslyckas, skickar servern tillbaka ett felmeddelande. Felmeddelandet beskrivs oftast med en statuskod, till exempel:

```Bash 
”HTTP 401 error – unauthorized”
”401 unauthorized ”
”Access denied”
```

GET. Detta är den mest använda HTTP-förfrågningsmetoden. En GET-förfrågan ber servern om en specifik bit information eller resurs. När du ansluter till en webbplats skickar din webbläsare vanligtvis flera GET-förfrågningar för att få den data den behöver för att sidan ska laddas.

POST. Din webbläsare använder POST-HTTP-förfrågningsmetoden när den behöver skicka data till servern. Till exempel, om du fyller i ett kontaktformulär på en webbplats och skickar det, använder du en POST-förfrågan så att servern tar emot den informationen.

PUT. PUT-förfrågningar är liknande i funktionalitet som POST-metoden. Men istället för att skicka data använder du PUT-förfrågningar för att uppdatera information som redan finns på slutservern.

För att följa dem WCAG riktlinjer så är det völidgt vitkigt at använda enkel och lättförståelig språklig stil i felmeddelanden så att användaren inte känner sig förvirrad eller överväldigad av tekniska termer. Åroblemet ska förkalras på ett sätt som gör det möjligt för användaren att vidta åtgärder för att lösa det.

![HTTP](images/HTTP-JS.png)

1. https://kinsta.com/knowledgebase/javascript-http-request/
2. https://www.freecodecamp.org/news/here-is-the-most-popular-ways-to-make-an-http-request-in-javascript-954ce8c95aaa/
3. https://kinsta.com/se/kunskapsbas/401-felet/
4. https://kinsta.com/knowledgebase/what-is-an-http-request/

## JS 1.7 Lexical scope

Lexical scope är ett fundamentalt koncept inom programmering, framför allt inom JavaScript-programmering. Lexical scope avgör tillgängligheten för variabler som deklareras i den fullständiga källkoden. När en variabel deklareras i en global scope är den tillgänglig över hela JavaScript-koden. Nackdelen med en global scope är att den kan leda till svårigheter med felsökning och testning, eftersom variabler lätt kan skrivas över av misstag eller påverka andra delar av programmet oavsiktligt. Lexical scope löser detta genom att tillåta variabler att endast vara tillgängliga inom den funktion där de är deklarerade eller i de inre funktionerna, vilket skapar en tydligare struktur och minskar risken för oväntade bieffekter.

Däremot finns det lokala scop som deklareras inuti en funktion och är endast tillgängliga inuti den funktionen. Dessa variabler är vanligtvis att föredra eftersom de minskar risken för namnkonflikter och håller variabler begränsade till de delar av koden där de verkligen behövs.

```js

function outerFunction() {
  var outerVar = "I'm in outer-scope";
  
  function innerFunction() {
    var innerVar = "I'm in inner-scope";
    console.log(outerVar); // Vi kan komma åt outerVar här eftersom den är i det omfånget där innerFunction() definieras.
  }
  
  innerFunction();
  console.log(innerVar); // Detta skulle orsaka en fel, eftersom innerVar bara är definierad i det omfånget av innerFunction().
}

outerFunction();
```

En förändring som kom med ECMAScript 2015 (ES6) var möjligheten att använda `let` och `const` för att skapa block scope. Detta innebär att variabler som deklareras med `let` eller `const` är endast tillgängliga inom det block där de är deklarerade. Till exempel, om vi deklarerar variabler inuti ett `if`-block eller en loop med `let` eller `const`, kommer de endast vara tillgängliga inuti det specifika blocket och inte utanför det. Detta ger utvecklare bättre kontroll över variabler och minimerar risken för oönskade sido effekter. Block scope med `let` och `const` bidrar till att förbättra kodens läsbarhet och underhållbarhet genom att tydligt definiera var variabler är tillgängliga och när de går ut ur omfånget. Detta är särskilt användbart i komplexa kodbaser där olika delar av koden kan ha olika krav på variabler.


1. https://cleverzone.medium.com/lexical-scope-in-javascript-929789101dab
2. https://www.freecodecamp.org/news/javascript-lexical-scope-tutorial/
3. https://www.freecodecamp.org/news/write-less-do-more-with-javascript-es6-5fd4a8e50ee2/

## JS 1.8 Event handling

Event referar till en handling där användaren interagerar med sidan och förväntar sig en dynamisk upplevelsen. En användaren vill till exempel kunna integerara genom att klicka på element så som knappar eller inmatningsfältar. Detta handling notiferar till webbläsaren att användaren har försökt komma åt en handling och behöver få respons. Detta sker genom en verktygsfunktion som kallas för event handler som lystnar på en särskild typ av begärd event. 

Det finns olika typ av events där den mest användbara är 'onlick'. 


```js
// Lägg till en klickhändelselyssnare på knappen
myButton.addEventListener('click', function() {
    // Ändra färgen på texten när knappen klickas
    myParagraph.style.color = 'blue';
});

```

1. https://dev.to/shubhankarval/event-handling-in-javascript-51n3


## JS 1.9 Prototype inheritance

Beskriv rubriken här

## JS 1.10 Higher-order functions

v. 11

## JS 1.11 Single-thread programming

Beskriv rubriken här

asynkrona metoder

## JS 1.12 OAuth från frontend

v 21

## JS 1.13 Websockets

v 20
