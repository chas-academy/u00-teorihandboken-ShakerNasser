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

De olika datatyperna och värdena som kan hanteras i JavaScript inkluderar:

- Strängar (Strings)
- Booleska värden (Boolean)
- Numeriska värden (Number)
- Arrayer (Arrays)
- Objekt (Objects)
- Odefinierat värde (Undefined)
- Null-värde (Null)

Här nedan följer ex på hur koden exkeveras (körs) med hjälp av console.log funktionen.

```js
let x = 1;
console.log(x);
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

JavaScript-ramverk är förpackningar av färdigskrivna kodbitar som gör det enklare att bygga webbapplikationer. De ger en strukturerad miljö för utvecklare att arbeta inom och följer ofta ett designmönster som heter Model-View-Controller (MVC). MVC delar upp kod i tre delar: modellen hanterar data, vyn visar data för användaren, och kontrollen tar emot användarinput och styr modellen eller vyn. Det här gör det lättare att bygga och underhålla webbapplikationer. Jämfört med kodbibliotek erbjuder ramverk fler verktyg för att skapa applikationer. JavaScript-ramverk är viktiga för att bygga moderna och starka webbapplikationer.

Angular: 
Angular är en open source plattform med Type-Script baserat utvecklingsform. Plattformen är utvecklat av Google och har en väldigt stark support samt dokumenation. Angular använder sig av komponententer för att kunna bygga starka och robust webbapplikationer. Genom att erbjuda en uppsättning utvecklarverktyg för att hjälpa till att utveckla, bygga, testa och uppdatera koden så är angular en väldigt attraktiv plattform bland utvecklare. 

React: 
React är ett open source verktyg på JavaScript som hjälper till att bygga användargränssnitt för webbplatser. Det skapades av Facebook och är perfekt för appar som behöver vara interaktiva och snabba. React är alltså bibliotek och inte ett ramverk, vilket innebär att det är mer flexibelt och kan användas tillsammans med andra verktyg och bibliotek för att skapa den perfekta lösningen för ett projekt. Med React kan man skapa dynamiska och effektiva webbapplikationer genom att använda koncept som virtuell DOM och effektiv hantering av tillstånd. React är ett omtyckt och populärt val bland utvecklare tack vare dess förmåga att effektivt hantera användargränssnitt, modularisera kod och skapa skalbara webbapplikationer.

Backend ramverken så som Express och NextJS:
Express och Next.js är två kraftfulla JavaScript-ramverk för backend-utveckling. Express är minimalistiskt och flexibelt medan Next.js erbjuder server-side rendering och API Routes. Dessa verktyg underlättar skapandet av skalbara och lättunderhållna webbapplikationer.


1. https://generalassemb.ly/blog/what-is-a-javascript-framework/
2. https://medium.com/@evincedevelop/top-10-most-popular-javascript-frameworks-to-choose-in-2024-269453cdaf35
3. https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks
4. https://builtin.com/software-engineering-perspectives/react-framework - React förklarad
5. https://www.entire.se/artiklar/javascript-ramverk-en-jamforelse-av-angular-react-och-vue 

## JS 1.3 Promises

Promises standardiserades efter den femte utgåvan av ECMAScript där de asynkrona funktionerna blir alltmer populära. Promises som även kallade "framtida löften" på svenska används för att hantera asynkrona operationer på ett mer strukturerat sätt och erbjuder ett sätt att hantera och samordna flera asynkrona operationer. Med promises kan man koppla ihop asynkrona uppgifter med metoderna async och await, vilket minskar användningen av callback-funktioner. Detta gör koden mer läsbar och lättare att utveckla för framtida projekt.

Promise presenterar värde så som pending (väntande), fullfied (uppfyllt) eller rejected (avvisat). När en promise är "pending", så väntar den på att en asynkron operation ska slutföras. När operationen slutförs, går promisen över till antingen "fulfilled" eller "rejected" beroende på om operationen lyckades eller misslyckades.

För att hantera resultatet eller felet från ett löfte används metoder som then() och catch(). Metoden then() tar en funktion som argument och körs när löftet uppfylls, medan catch() används för att hantera eventuella fel som uppstår under löftets exekvering.

Här nedan följs en enklare kod exempel på promises som används vid API anrop, StarWars API. 

```js
// Hämta data från API:et med Fetch och logga till konsolen
fetch('https://swapi.dev/api/people/')
  .then(response => response.json())
  .then(data => {
    data.results.forEach(person => {
      console.log(`Namn: ${person.name}, Hemvärld: ${person.homeworld}`);
    });
  })
  .catch(error => console.error('Något gick fel:', error));
```

Promises gör det möjligt att skriva mer läsbar och underhållbar asynkron kod jämfört med callback-metoden. De är också grunden för async/await-syntaxen som introducerades i ECMAScript 2017 och gör asynkron kod ännu lättare att läsa och skriva. Innan det var möjligt att använda sig av asynkrona metoder så kunde utvecklare hamna i så kallade callback-hell. Callback-hell uppstod när man hade flera inbäddade eller nästlade callback-funktioner, vilket resulterade i djupt nästlad och svåråtkomlig kod.

1. https://sunlightmedia.org/sv/tips-f%C3%B6r-javascript/
2. https://www.freecodecamp.org/news/javascript-promise-object-explained/
3. https://medium.com/@shriharim006/javascript-promises-from-beginner-to-expert-a-comprehensive-tutorial-899454b6f17f
4. https://dev.to/alexmercedcoder/understanding-javascript-promises-in-depth-5ga9


## JS 1.4 OOP i JavaScript

JavaScript är ett OOP-skriptspråk. OOP är fortkortning till Obejktorinterad programmering (Eng: Object Oriented Programming). Programmeringsmetoden gör det möljigt att använda sig av uppsättning av objekt som integerar med varandra och detta skapar effektiv och kraftfulla konstruktion vid stora program.

Inom OOP representerar objekten verkliga entiteter med specifika egenskaper och beteenden. Ett objekt är en instans av en klass, där klassen kan ses som en mall eller ett blåtryck för objektet. Klassen definierar vilka egenskaper (attribut) och metoder (funktioner) objektet kommer att ha.

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
Genom att använda objekt på detta sätt kan man skapa strukturerade och modulära program där olika delar av programmet kan hantera sina egna data och funktioner. Detta gör koden mer organiserad och lättare att underhålla särskilt när programmen blir större och mer komplexa. JavaScript gör det också möjligt att skapa och hantera objekt dynamiskt, vilket ger stor flexibilitet och kraft till utvecklarna.

1. https://www.freecodecamp.org/news/how-javascript-implements-oop/
2. https://sv.khanacademy.org/computing/computer-programming/programming/objects/a/review-objects
3. https://medium.com/@priyam_mondal/exploring-object-oriented-programming-in-javascript-25ebb1cc13c9
4. 

## JS 1.5 DOM-manipulation

DOM-manipulation är en viktigt verktyg i Javascript där utvecklare kan integerera med HTML element för att skapa en dymanisk och interaktiv plattform. Genom att komma åt element och modifera struktur, styling och innehåll så blir användarupplevelsen mer dynamisk än att bara använda en statisk sida. DOM är en representation av HTML-dokumentet som en trädlika struktur där varje nod är en del av dokumentet (t.ex., element, attribut, text).

För att manipulera DOM-trädet behöver man komma åt elementen genom att använda DOM-objekt, vilket representerar hela HTML-dokumentet. Detta kan göras med metoder som getElementById, getElementsByClassName, och getElementsByTagName, som visat i exemplen ovan. När man har lyckats komma åt dessa element kan man modifiera deras innehåll, struktur och stil med hjälp av JavaScript.

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

DOM används i en mängd olika scenarier inom webbutveckling. Det kan användas för att skapa interaktiva formulär, dynamiskt ladda innehåll från en server via AJAX eller Fetch API, samt hantera händelser och användarinteraktioner på sidan. Genom att använda DOM kan man skapa webbapplikationer som är mer användarvänliga och responsiva.

I JavaScript ramverket Angular och biblotket React så är DOM manipulation en väldigt stor del av deras mekanism. Genom att använda virtuell DOM, komponentbaserad arkitektur och avancerade datahanteringsmekanismer, gör dessa ramverk det enklare och effektivare att bygga dynamiska och responsiva webbapplikationer. 

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

Det finns massor av olika händelser som kan hanteras i JavaScript, som när en användare integerar applikationen med klicka med musen, trycker på en tangent, rör musen, fyller i ett formulärfält, laddar en sida, och mycket mer. Genom att lyssna och hantera dessa händelser kan webbsidor bli interaktiva och reagera på det användaren integerar med görs på ett smidigt sätt.

När eventhanteraren körs, kan den också få reda på information om själva händelsen, som vilket element användaren klickade på, vilken knapp användaren tryckte ner eller vilken tangent användaren tryckte på. Den här informationen kan vara användbar för att göra olika saker beroende på vad som hände och när det hände.

Eventhantering är viktigt för webbutveckling eftersom det gör det möjligt att skapa användarvänliga gränssnitt och ge användarna en bra upplevelse när de använder webbapplikationer.

Det finns olika typ av events där den mest användbara är 'onlick'.

```js
// Hämta referens till knappen
var minKnapp = document.getElementById("minKnapp");

// Lägg till en eventhanterare för klickhändelser på knappen
minKnapp.addEventListener("click", function() {
    // Kod som ska köras när knappen klickas på
    alert("Knappen klickades på!");
});

```
Event handling i ramverket Angular (ex tagen från Recipe-APP): 

<button [disabled]="!loginObj.email || !loginObj.password" type="submit" (click) ="onLogin()">Sign in</button>

Mouseover och Mouseout events är användbara för hover-effekter på webbsidor, där något aktiveras när muspekaren går över eller lämnar ett element. Det kan vara att ändra färg på en knapp eller visa mer information när musen sveper över en bild.

Keydown, Keypress och Keyup events fångar tangenttryckningar från användaren, vilket är avgörande för att hantera användarinmatning på webbsidor. De är särskilt användbara för att skapa interaktiva formulär eller möjliggöra tangentbordsnavigering.

Att förstå sig på eventhandling kommer även att underlätta hur man testar sin applikation och använder sig av benchmarking verktyg så som DevTools. Detta kommer hjälpa en att inspektera i konsolen och leta efter sårbarheter i koden och förminska spillotiden.

1. https://dev.to/shubhankarval/event-handling-in-javascript-51n3
2. https://www.scaler.com/topics/javascript/event-handling-in-javascript/
3. https://medium.com/@theriyasharma24/event-handling-in-angular-a5854a61b4a5
4. https://medium.com/@ratnesh4209211786/mastering-event-handling-in-javascript-a-comprehensive-guide-51204c2cf552

## JS 1.9 Prototype inheritance

Beskriv rubriken här

1. https://www.freecodecamp.org/news/prototypes-and-inheritance-in-javascript/
2. https://medium.com/@kevincennis/prototypal-inheritance-781bccc97edb
3. https://medium.com/@amitbadala/understanding-and-implementing-prototype-inheritance-in-javascript-fef72c2341fa
4. https://reference.codeproject.com/javascript/inheritance_and_the_prototype_chain

## JS 1.10 Higher-order functions

I JavaScript är 'higher-order functions' (högre ordningens funktioner) funktioner som antingen tar andra funktioner som argument eller returnerar en funktion som resultat, eller både och. En funktion i sig är en serie instruktioner för att utföra en viss typ av operation, och dessa funktioner använder parametrar för att definiera de värden som ska behandlas när koden körs. Dessa funktioner är kraftfulla eftersom det går att återanvända dem i koden. 

För att kunna förstå sig på högre higher-order functions så är det bättre att bryta ner dem och förstå de mindre delarna innan man närmar sig konceptet som helhet. 

I detta exempel nedan så är `greet` namnet av funktionen och `name` är det parametern som skickas in i funktionen.  

En defintion av en enkel JavaScript function:

```js
function greet(name) {
  console.log("Hello, " + name + "!");
}
```

Callbackfunktioner är som instruktioner som man ger till någon annan att använda vid behov. När den andra personen är klar med sin uppgift, följer de  instruktioner och gör det som har ombetts att gör.

I det här enkla exemplet:

```javascript
function promptInput(callbackFn) {
  const name = prompt('Vad är ditt namn?');
  callbackFn(name);
}

promptInput(name => console.log(`Hej ${name}!`));
```

Funktionen `promptInput` ber användaren att ange sitt namn. När användaren gör det, anropar den den medföljande instruktionen (callbackfunktionen) för att säga hej med det namn som angavs.

Callbackfunktioner är användbara när man behöver att något ska hända efter en viss händelse eller efter en uppgift är klar, som att hämta data från en databas eller när man vill reagera på en knapptryckning på en webbsida.

Här nedan följs ett enklare exempel på Higher-order funktion: 

```js
function sayHello() {
  console.log("Hej!");
}

function sayGoodbye() {
  console.log("Hejdå!");
}

function greet(saySomething) {
  saySomething(); // Här används higher-order funktionen 
}

greet(sayHello);    // Output: Hej!
greet(sayGoodbye);  // Output: Hejdå!
```
I greet-funktionen tar den parameter saySomething, vilket förväntas vara en annan funktion. Sedan använder den denna funktion genom att helt enkelt kalla den, vilket innebär att den andra funktionen utförs när greet kallas.

I de två anropen till greet, skickar vi sayHello respektive sayGoodbye som argument. Så när vi kallar greet(sayHello), kör den sayHello-funktionen och skriver ut "Hej!" på konsolen. När vi kallar greet(sayGoodbye), kör den sayGoodbye-funktionen och skriver ut "Hejdå!".

1. https://www.reddit.com/r/learnjavascript/comments/r1z131/can_someone_help_explain_what_a_higherorder/ 
(Tog reddit för just denna förklarar väldigt bra)
2. https://medium.com/@rabailzaheer/first-class-and-higher-order-functions-86d14e40c688
3. https://www.telerik.com/blogs/master-higher-order-functions-javascript (Förklarar alla slags (användbara) funktioner också)
4. https://www.almabetter.com/bytes/tutorials/javascript/higher-order-functions


## JS 1.11 Single-thread programming

I ett single-thread (Enkeltrådad programmering) programmerings språk innebär det att språket använder sig av bara ett tråd. Trådet ekuveras innan den ekuverar nästa tråd.

JavaScripts enkeltrådiga karaktär kommer av dess rötter som ett språk för webbläsare, där dess huvudsyfte är att interagera med användaren genom att manipulera HTML, CSS samt hantera händelser. Att bara ha en tråd kan förenkla utvecklingsprocessen då det tar bort behovet av att hantera trådsynkronisering och andra komplexa problem som kan uppstå vid användning av flera trådar.

Dock kan JavaScripts enkeltrådiga natur även vara en begränsning i vissa fall. Till exempel kan intensiva beräkningar eller långsamma I/O-operationer ge intrycket att webbläsaren fastnar eftersom den enda tråden är upptagen med att utföra dessa operationer och kan inte svara på andra användarinteraktioner under tiden.

För att bemöta detta har JavaScript infört koncept såsom asynkron programmering och händelsebaserade arkitekturer. Med hjälp av funktioner som callbacks, promises och async/await kan utvecklare skapa icke-blockerande kod som tillåter andra operationer att fortsätta samtidigt som intensiva eller långsamma operationer behandlas i bakgrunden.

React och Angular hjälper till med enkeltrådad programmering genom att erbjuda möjligheter till komponentbaserad utveckling och hantering av tillstånd. Dessa ramverk tillåter utvecklare att skapa modulära och återanvändbara komponenter som kan interagera med varandra utan att orsaka problem med enkeltrådadhet. Genom att hantera DOM-manipulation och tillståndshantering åt utvecklaren, underlättar dessa ramverk processen att bygga responsiva och dynamiska användargränssnitt utan att behöva oroa sig för att hantera flera trådar manuellt.


1. https://medium.com/swlh/what-does-it-mean-by-javascript-is-single-threaded-language-f4130645d8a9
2. https://dev.to/bbarbour/if-javascript-is-single-threaded-how-is-it-asynchronous-56gd
3. https://elijahtrillionz.com/why-is-javascript-single-threaded-and-non-blocking


## JS 1.12 OAuth från frontend

OAuth (Open Authorization) är en standard för hantering av åtkomst som tillåter användare att ge tredjepartsapplikationer åtkomst till sina resurser utan att dela sina lösenord. Från ett frontend-perspektiv innebär detta att en applikation kan begära åtkomst till data från en annan tjänst, som Google eller Facebook med användarens tillstånd.

Processen påbörjas genom att användaren klickar på en knapp med texten "Logga in med [tjänst]". Användaren blir då omdirigerad till tjänstens OAuth-autoriseringsserver där applikationen specificerar vilka resurser den vill få åtkomst till genom att inkludera olika "scopes" i förfrågan. Användaren loggar in på tjänsten och ombeds sedan att godkänna åtkomsten som applikationen begär.

Om användaren godkänner skickar tjänsten tillbaka en auktoriseringskod till applikationen via en omdirigering till en fördefinierad URL. Denna kod skickas sedan från frontend till backend-servern. På backend-servern begärs ett åtkomsttoken från tjänsten med hjälp av koden och en klienthemlighet. Detta steg utförs på backend för att skydda känslig information från att exponeras i frontend-koden.

En enkel illustration på vad som händer om en användare väljer att använda sig av google login:

- Användaren klickar på "Logga in med Google".
- Användaren omdirigeras till Googles inloggningssida och loggar in.
- Användaren godkänner att applikationen får åtkomst till deras Google-profil och e-postadress.
- Google omdirigerar användaren tillbaka till webbapplikationen med en auktoriseringskod.
- Webbapplikationens frontend skickar koden till sin backend.
- Backend begär och får ett åtkomsttoken från Google.
- Backend använder åtkomsttoken för att hämta användarens Google-profil och e-postadress från Googles API och skickar tillbaka denna information till frontend.

* [tjänst] innebär annan tjänst som Google, Facebook eller Twitter med användarens tillstånd.

1. https://medium.com/web-security/understanding-oauth2-a50f29f0fbf7
2. https://medium.com/@tony.infisical/guide-to-using-oauth-2-0-to-access-google-apis-dead94d6866d
3. https://stackoverflow.blog/2022/12/22/the-complete-guide-to-protecting-your-apis-with-oauth2/

## JS 1.13 Websockets

Websockets möjliggör snabb och effektiv tvåvägskommunikation mellan en webbläsare och en webbserver. Genom att använda full duplex-kommunikation kan både klienten och servern skicka och ta emot meddelanden samtidigt, vilket ger en mer responsiv och interaktiv användarupplevelse. För att etablera en websocket-anslutning initierar klienten en HTTP-förfrågan till servern, vilket sedan leder till att en ihållande kommunikationskanal skapas mellan dem. Denna teknik är särskilt användbar för realtidsapplikationer såsom chattprogram, spel och dataströmning, där snabb och kontinuerlig kommunikation är avgörande för en bra användarupplevelse. Websockets gör det möjligt för webbapplikationer att erbjuda snabb och responsiv kommunikation i realtid. Detta förbättrar användarupplevelsen och skapar möjligheter för olika applikationer som behöver omedelbar dataöverföring och interaktivitet.

Websockets inte bara möjliggör snabbare kommunikation jämfört med traditionella HTTP-förfrågningar. utan de minskar också överföringen av onödig data. Genom att ha en öppen anslutning kan både klienten och servern skicka och ta emot data utan att behöva upprepa handskakningsprocessen som krävs för varje HTTP-förfrågan och svar. Detta leder till lägre latens och minskad belastning på nätverks- och serverresurser.

WebSocket-anslutningar skapas normalt sett med klient-sidan JavaScript enligt följande:

```js
var ws = new WebSocket("wss://normal-website.com/chat");

```

För realtidsapplikationer är fördelarna med websockets särskilt tydliga. Till exempel kan chattapplikationer dra nytta av omedelbar leverans av meddelanden utan fördröjning. Spel kan använda websockets för att synkronisera spelstatus och möjliggöra realtidsinteraktion mellan flera spelare. Även inom dataströmning kan websockets användas för att leverera kontinuerlig information, som aktiekurser eller sensoravläsningar, till användare i realtid.


Detta sker även genom en "handskakning" som sker via en HTTP förfråga:

```js
GET /chat HTTP/1.1
Host: normal-website.com
Sec-WebSocket-Version: 13
Sec-WebSocket-Key: wDqumtseNBJdhkihL6PW7w==
Connection: keep-alive, Upgrade
Cookie: session=KOsEJNuflw4Rd9BDNrVmvwBF9rEijeE2
Upgrade: websocket

```

När server har accepterat kommunaktionen så får man föjande som svar:

```js
HTTP/1.1 101 Switching Protocols
Connection: Upgrade
Upgrade: websocket
Sec-WebSocket-Accept: 0FFP+2nmNIf/h+4BP36k9uzrYGk=

```

Google Docs är en väldigt bra exempel att använda. Där kan flera medlemmar skriva samtidigt och få en realatidförändring. 
Även inom aktiedataströmmning så är det viktigt med WebSockets för att prenumerera på och strömma kontinuerliga uppdateringar från en server. Genom att använda WebSockets kan användare få omedelbar tillgång till den senaste marknadsinformationen utan att behöva uppdatera sidan manuellt. 


1. https://it-ord.idg.se/ord/websocket/
2. https://www.geeksforgeeks.org/what-is-web-socket-and-how-it-is-different-from-the-http/
3. https://medium.com/@Arockne/networking-introduction-to-websockets-7c0ffc3c2d6e
4. https://www.educative.io/answers/what-is-websocket
5. https://portswigger.net/web-security/websockets/what-are-websockets