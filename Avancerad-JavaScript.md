# Teorihandboken - Avancerad JavaScript (AJ)
Studerande: Shaker Nasser

## AJ 1.1 Node.js

Node.js är en välkänd och kraftfull plattform som används för att utveckla serverbaserade applikationer. Det är en öppen källkodsmiljö som kan köras på flera plattformar och gör det möjligt att använda JavaScript på serversidan. Node.js bygger på Googles V8-motor samma motor som driver webbläsaren Google Chrome vilket gör det möjligt att använda JavaScript utanför klientens webbläsare. Detta är en stor fördel för utvecklare då de kan använda samma programmeringsspråk både på servern och i webbläsaren vilket skapar en mer enhetlig kodbas och en smidigare utvecklingsprocess.

En av de mest framstående funktionerna i Node.js är dess händelsedrivna och asynkrona arkitektur. Till skillnad från traditionella serverplattformar där operationer vanligtvis blockeras tills de är färdiga. Node.js utformning är att utföra alla operationer asynkront. Detta innebär att servern inte behöver vänta på att ett anrop ska slutföras innan nästa uppgift hanteras vilket leder till snabbare och mer responsiva applikationer. Detta är särskilt användbart när man arbetar med stora mängder samtidiga användare eller vid hantering av realtidsdata.

Node.js är även mycket populärt för att utveckla Single Page Applications (SPA). SPA är webbapplikationer där allt innehåll laddas på en enda sida och interaktionen med sidan hanteras genom JavaScript utan att hela sidan behöver laddas om. Genom att använda Node.js som backend tillsammans med front-end-ramverk som React eller Angular kan utvecklare skapa moderna responsiva applikationer som ger användaren en snabb och smidig upplevelse.

![U08 projekt - NODEJS Express - REACT](images/node.js.png)

Den kraftfulla verktygen tillåter utvecklare att använda JavaScrit till för att skapa en backend-applikation som hanterar serverlogik filsystem och nätverksoperatoner samt mtcket mer. Innan Node.js så användes javascript endast till fron-end applikationer. 

Node.js erbjuder en mängd funktioner för webbutveckling. Det använder en asynkron och icke-blockerande I/O-modell, vilket innebär att det kan hantera flera uppgifter samtidigt utan att behöva vänta på att en uppgift ska slutföras innan nästa påbörjas. Node.js körs på en enda tråd men använder en händelsedriven arkitektur vilket möjliggör effektiv hantering av tusentals samtidiga anslutningar. Eftersom Node.js är byggt på Google V8-motorn kan det exekvera JavaScript-kod snabbt och effektivt. Dessutom har Node.js ett omfattande ekosystem av paket genom Node Package Manager (NPM), vilket gör det enkelt att återanvända kod och installera externa moduler för att underlätta utvecklingsprocessen.

1. https://dev.to/mehedihasan2810/nodejs-best-practices-a-guide-for-developers-4d65
2. https://medium.com/@asiandigitalhub/what-is-node-js-and-how-it-work-490f5ecba665
3. https://www.simplilearn.com/tutorials/nodejs-tutorial/nodejs-backend
4. https://javascript.plainenglish.io/what-is-node-js-5fe50e4332c8
5. https://dev.to/vyan/how-to-structure-your-backend-code-in-nodejs-expressjs-2bdd
6. https://www.simplilearn.com/tutorials/nodejs-tutorial/what-is-nodejs

## AJ 1.2 Express

Express är ett välkänt och kraftfull ramverk för webbapplikationer för Node.js som gör webbapplikations- och API-utveckling enklare och effektivare. Express är snabbt, anpassningsbart och "ointressant", vilket innebär att det inte kräver att utvecklare håller sig till en specifik struktur eller designfilosofi. Istället ger det ett enkelt sätt att bygga skalbara och lätta att underhålla applikationer. Express stöder också arkitekturen Model-View-Controller (MVC), som är ett vanligt mönster för att strukturera webbapplikationer.
Utvecklare kan ställa in och använda Express i sitt arbete med Node.js och npm (Node Package Manager). Det är ett toppval för att bygga enkla webbplatser pcj knepiga appar och API:er.

Routing spelar en nyckelroll i Express och syftar till att hantera hur en webbapp svarar på olika klientförfrågningar till specifika slutpunkter. Dessa slutpunkter består ofta av en URI (som /home eller /about) och en HTTP-metod (GET, POST, PUT DELETE). Genom att använda routing kan utvecklare bygga responsiva och interaktiva webbappar som hanterar olika typer av förfrågningar baserat på vad användaren behöver.
En enkel routermetod i Express:

```js
app.get('/books', (req, res) => {
  res.send('books page');
});
app.get('/about', (req, res) => {
  res.send('about');
});
```

Express har en annan nyckelfunktion: middleware. Det här är funktioner som har tillgång till begäran (req), svaret (res) och nästa funktion i appens begäran-svar-cykel. De behandlar förfrågningar innan de når sina slutdestinationer eller ändrar svar innan appen skickar dem till kunden. Du kan använda mellanprogram för att hantera uppgifter som att kontrollera om en användare är inloggad för att hålla loggar eller lägga till specifika rubriker till svar.
Express har ett grundläggande sätt att ställa in en routermetod. Det ser ut så här:

```js
app.use((req, res, next) => {
  console.log('En ny begäran mottogs vid ' + Date.now());
  next();  // Går vidare till nästa middleware eller rutt
});
```

När man utvecklar en Express (Express.js) applikation är det oerhört viktigt att tänka på strukturen av både koden och mappstrukturen. Detta underlättar underhåll, skalbarhet och samarbetet med andra utvecklare. En välorganiserad kod och mappstruktur kommer att förenkla navigering och förståelse av koden.

Här nedan följer ett ex på hur jag struktuerat min FJSu09 projket:

![Express](images/express.png)

1. https://www.codecademy.com/article/what-is-express-js
2. https://medium.com/@Brilworks/what-is-express-js-a-comprehensive-guide-to-beginners-b289a25bd414
3. https://dev.to/bilal1718/how-to-create-a-backend-api-in-express-js-e0k
4. https://dev.to/dipakahirav/modern-api-development-with-nodejs-express-and-typescript-using-clean-architecture-1m77
5. https://www.freecodecamp.org/news/the-express-handbook/
6. https://www.freecodecamp.org/news/express-explained-with-examples-installation-routing-middleware-and-more/

## AJ 1.3 Progressive Web Apps

En Progressiv Webbapp (PWA) kombinerar de bästa delarna av webbplatser och mobilappar. Den utnyttjar den senaste webbläsartekniken för att ge användarna en upplevelse som känns mer som en vanlig app. Detta inkluderar att kunna fungera offline, skicka notiser och ladda snabbare än vanliga webbsidor.

Problem som PWAs försöker lösa:

Internetberoende: Vanliga webbappar kräver en bra internetanslutning för att fungera. PWAs kan fungera offline eller när internetanslutningen är långsam.

Hastighet: Webbappar kan vara långsammare än appar du laddar ner. PWAs är byggda för att starta snabbt och fungera smidigt.

Svårt att lägga till på hemskärmen: Du kan inte lägga till vanliga webbappar på din hemskärm som vanliga appar. Men du kan lägga till PWAs direkt från din webbläsare utan att behöva gå till en appbutik.

Hur PWAs hjälper:

Fungerar offline: PWAs använder särskilda verktyg för att spara vad de behöver. Detta gör att de kan fortsätta fungera även när du inte är online.

Snabbare prestanda: PWAs hämtar det de behöver från sparad data. Detta ger användarna en smidig och snabb upplevelse.

### Dessa kritier måste uppfyllas för att få en fungerande PWA applikation:

HTTPS: Din webbapp måste köras på en säker anslutning. Detta håller den säker och gör att servicearbetare kan utföra sitt jobb.

Web App Manifest: Denna JSON-fil talar om för PWA:n hur den ska bete sig. Den inkluderar saker som appikoner, namn, startpunkt och hur den ska visas.

Service Worker: Detta är ett skript som körs i bakgrunden. Det möjliggör caching, push-meddelanden och offlineanvändning.

### Fördelar och nackdelar med att göra en app till en PWA

Fördelar:
Fungerar på alla plattformar och enheter.
Kostar mindre än att skapa separata appar för iOS och Android.
Laddar snabbare och fungerar offline, vilket gör användarna nöjda.

Nackdelar:
Kan inte använda vissa enhetsfunktioner, som Bluetooth eller avancerade kamerakontroller.
Vissa funktioner kanske inte fungerar lika bra på vissa plattformar, särskilt på iOS där PWAs inte har lika stort stöd.

Vad kan en serviceworker göra?

En service worker är ett skript som körs i bakgrunden och hanterar olika uppgifter som:

Lagra resurser: Detta gör att PWAs kan fungera utan internetanslutning eller snabba upp laddningen genom att hämta resurser från lagring.

Hantera nätverksförfrågningar: Den kan styra hur appen hanterar nätverksförfrågningar, vilket hjälper till att optimera resurser och förbättra prestandan.

1. https://medium.com/@blockchain_simplified/what-is-a-pwa-an-intro-to-progressive-web-apps-3f280071f909
2. https://dev.to/udoka033/progressive-web-apps-pwa-a-comprehensive-guide-57ii
3. https://www.rabitsolutions.com/blog/examples-of-pwa-development/
4. https://www.freecodecamp.org/news/what-are-progressive-web-apps/

## AJ 1.4 Typningssystem för Javascript (ex TypeScript, Flow)

TypeScript är ett kodningsspråk som utökar JavaScript och lägger till statisk typkontroll. Microsoft skapade det och folk använder det ofta för att bygga stora skalbara appar. En av de viktigaste fördelarna med TypeScript är att det hjälper kodare att skriva starkare kod som är lättare att underhålla genom att föra in typer i JavaScript som är ett dynamiskt språk. JavaScript är ett tolkat språk som räknar ut typer när det körs men TypeScript introducerar typer innan programet körs.

TypeScript fungerar genom att utvecklare skriver kod i TypeScript, som sedan konverteras till JavaScript. Denna konvertering upptäcker potentiella fel och andra problem innan koden körs, vilket leder till färre fel och problem när programvaran är aktiv. TypeScript använder också "duck typing", vilket innebär att det kan gissa en variabels typ baserat på dess användning, utan att utvecklaren behöver stava det.
Konverteringen sker genom kommandot tsc (TypeScript Compiler). Detta kommando ändrar TypeScript-filer (som slutar med .ts) till standard JavaScript-filer som kan köras i alla inställningar som stöder JavaScript.
Anteckningar i TypeScript

TypeScript ger dig massor av alternativ för att lägga till typinformation till din kod. Här är några vanliga sätt att göra det:

Nummer: värden som är siffror.
Sträng: bitar av text.
Boolean: sanna eller falska värden.
Any: När du inte vill fästa en specifik typ. Detta kan vara praktiskt men också Riskabelt eftersom det stänger av typkontroll.
Void: Visar att en funktion inte ger tillbaka något värde.
Array: Typen för en lista med saker, som nummer[] för en lista med nummer.

TypeScriptkod har vissa fördelar jämfört med vanlig JavaScript. Den stora är statisk typkontroll som upptäcker fel när du kompilerar istället för när du kör koden. Det betyder att din kod är starkare och lättare att hålla koll på. Så här skiljer sig JavaScript och TypeScript.

TypeScript har några starka skrividéer som gör koden mer anpassningsbar och återanvändbar. Här är några:
Generika: 
Med generika kan du bygga återanvändbara delar som fungerar med många typer utan att förlora typkontrollen. Här är ett exempel på en generisk funktion:
```js
function identity<T>(arg: T): T {
  return arg;
}
let result = identity<number>(42); 
```

Tuples: 
En tuple är en maskinskriven lista där varje objekt kan ha en annan typ. Detta hjälper till att representera ett snabbt element med specifika typer.

```js
let tuple: [string, number];
tuple = ['hello', 10]; 
```

Unions: Unions låter en variabel ha flera möjliga typer. Till exempel kan en variabel vara antingen ett tal eller en sträng:,

```js
function printId(id: number | string) {
  console.log(id);
}
```


1. https://dev.to/janvierjr/intro-to-typescript-5dhi 
2. https://medium.com/@krishsurya1249/typescript-tutorial-f8d45ce5766b
3. https://www.freecodecamp.org/news/learn-typescript-beginners-guide/


## AJ 1.5 Funktionell programmering i JavaScript

Functional programming (FP) har sina rötter i matematik och logik, med en stark betoning på att definiera program som en sekvens av funktioner snarare än som en serie av instruktioner. Dess tidiga historia sträcker sig tillbaka till 1930-talet med utvecklingen av lambda-kalkyl av Alonzo Church, en formellism som används för att definiera beräkningar genom funktioner och variabler. Lambda-kalkyl lade grunden för många av de koncept som senare skulle komma att definiera funktionell programmering.

Lambdakalkyl
Lambda-kalkyl är en matematisk teori som möjliggör representation och manipulation av funktioner. I lambda-kalkyl används lambda-notation för att definiera anonyma funktioner, vilket gör det möjligt att skapa och använda funktioner som förstklassiga objekt. Det ger en kraftfull och elegant metod för att hantera funktionell abstraktion och möjliggör skapandet av komplexa program genom enkla byggstenar.

Haskell
Haskell, som introducerades i slutet av 1980-talet, är ett av de mest kända funktionella programmeringsspråken. Det är ett rent funktionellt språk, vilket innebär att alla funktioner är renodlade och inga sidoeffekter är tillåtna. Haskell använder laziness (fördröjd utvärdering), vilket innebär att uttryck utvärderas först när deras värden behövs. Detta ger möjlighet att skriva mer deklarativ kod och gör att programmerare kan fokusera på att specificera vad de vill uppnå snarare än hur. Haskell
typ-system är också mycket kraftfullt och möjliggör typinference, vilket gör att programmerare kan skriva mer robust och felresistent kod.

Deklarativ vs imperativ programmeringsparadigm
Programmeringsparadigmer kan delas in i deklarativa och imperativa. Deklarativ programmering handlar om att specificera vad som ska göras utan att ange hur, vilket gör att programmeraren kan fokusera på problemets lösning snarare än detaljerna i genomförandet. Exempel på detta inkluderar SQL och HTML. Imperativ programmering å sin sida innebär att man ger en serie instruktioner som direkt styr hur något ska utföras. Det handlar om att beskriva steg-för-steg hur uppgiften ska utföras, vilket kan göra koden mer komplex och svår att underhålla.

Programmeringsexempel
Ett enkelt exempel på funktionell programmering i JavaScript kan vara att beräkna summan av en lista med nummer med hjälp av den inbyggda metoden reduce(). Istället för att använda en loop för att iterera genom listan och ackumulera summan, kan vi skriva:

```js
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((acc, current) => acc + current, 0);
```

Här använder vi en högre ordningens funktion för att summera elementen, vilket ger en mer deklarativ och kompakt kod.

Higher order functions
Högre ordningens funktioner är funktioner som kan ta andra funktioner som argument eller returnera dem som resultat. Detta tillåter programmerare att skapa mer abstrakta och återanvändbara kodblock. Exempel på högre ordningens funktioner i JavaScript inkluderar map, filter och reduce, vilka alla möjliggör olika typer av listbearbetning på ett funktionellt sätt.

Läs mer om high order functions: [JS 1.10 High Order Functions](JavaScript.md#JS-1.10-Higher-order-functions)

Pure components i React
I React refererar "pure components" till komponenter som ger samma utdata för samma indata och inte ändrar sitt interna tillstånd. Detta gör dem enklare att förutsäga och testas, och kan leda till förbättrad prestanda genom att undvika onödiga omrenderingar. Pure components i React optimerar renderingsprocessen genom att endast uppdatera komponenter när deras props eller state förändras, vilket gör applikationen mer effektiv.

Map()
map() är en högre ordningens funktion i JavaScript som skapar en ny array genom att applicera en given funktion på varje element i den ursprungliga arrayen. Till exempel, om vi har en array med tal och vill skapa en ny array med dessa tal multiplicerade med två, kan vi skriva:

``` js
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]


```

Denna funktion är ett exempel på deklarativ programmering, där vi uttrycker vad vi vill åstadkomma utan att specificera hur iterationen genomförs.

Filter()
filter() är en annan högre ordningens funktion som skapar en ny array med alla element som uppfyller ett visst villkor. Till exempel, för att extrahera alla jämna tal från en array kan vi använda:

``` js
const numbers = [1, 2, 3, 4, 5];
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]

```

Reduce()
reduce() är en kraftfull metod som används för att ackumulera värden i en array till ett enda värde. Det kan användas för att summera tal, som i det tidigare exemplet, eller för att skapa en objektstruktur från en lista. Här är ett exempel där vi räknar antalet förekomster av varje element i en array:

```js
const fruits = ['apple', 'banana', 'orange', 'apple', 'orange'];
const fruitCount = fruits.reduce((acc, fruit) => {
  acc[fruit] = (acc[fruit] || 0) + 1;
  return acc;
}, {});
// { apple: 2, banana: 1, orange: 2 }

```



1. https://thecodest.co/sv/blog/kraften-i-funktionell-programmering-i-javascript-del-1-introduktion/
2. https://dev.to/alexmercedcoder/deep-dive-into-functional-programming-in-javascript-851
3. https://www.freecodecamp.org/news/functional-programming-in-javascript/

## AJ 1.6 Avancerad funktionalitet i ES.next

ECMASprict är en standard för JavaScript som gör att det fungerar likadant i olika webbläsare och miljöer. Den bestämmer regler, funktioner och hur språket ska se ut. Standard uppdateras ofta för att lägga till nya funktioner och förbättringar.

ES.next är ett samlingsnamn för framtida versioner av ECMAScript, standarden för programmeringsspråket JavaScript. ES.next syftar specifikt på den version av ECMAScript som är i utveckling och som följer efter den nuvarande standarden.

Man kan bidra med nya feature i form av ider men dessa måste skickas in till TC-39 kommiten. Nya funktioner och förslag granskas och godkänns av TC39-kommittén som ansvarar för att utveckla och underhålla ECMAScript-standarden. Deras uppgift är att säkerställa att bidragsgivare följer standarden och att JavaScript fortsätter att utvecklas och förbättras.
Varje feature behöver gå genom dem fyra olika stegen i procecessn för att inkuderas i standarden.

De fyra stegen är:
0: Idéstadium (Strawman) - Förslag lämnas in till specifikationen.
1: Förslag (Proposal) - Förklara varför förslaget behövs, beskriv en möjlig lösning och identifiera eventuella problem.
2: Utkast (Draft) - Beskriv hur det ska fungera med korrekt syntax och tekniskt språk.
3: Kandidat (Candidate) - Det behövs mer feedback från utvecklare och användare för att förbättra förslaget.
4: Färdig (Finished) - Förslaget är redo att läggas till i den officiella ECMAScript-standarden.

ECMAscirpt är ständigt inom förändring vilket innebär att som utvecklare så ska man vara förberdd på att läsa sig in i nya förändringar. Några av dessa features som har kommit in den seanste året:

`replaceAll()` - En metod som låter dig byta ut alla förekomster av en sträng mot en annan i ett textstycke. Tidigare kunde `replace()` endast byta ut den första matchningen, men med `replaceAll()` byts alla förekomster ut på en gång.

`Promise.any()` - Denna metod tar en lista av löften (Promises) och returnerar det första löftet som uppfylls (resolves). Om inget löfte uppfylls, och alla misslyckas, returnerar det ett fel. Detta skiljer sig från `Promise.all()`, som väntar på att alla löften ska uppfyllas eller misslyckas.

Kodexempel:

```js
const paragraph = "I think Ruth's dog is cuter than your dog!";

console.log(paragraph.replaceAll('dog', 'monkey'));
// Expected output: "I think Ruth's monkey is cuter than your monkey!"

// Global flag required when calling replaceAll with regex
const regex = /Dog/gi;
console.log(paragraph.replaceAll(regex, 'ferret'));
// Expected output: "I think Ruth's ferret is cuter than your ferret!"
```

1. https://github.com/tc39/proposals
2. https://tc39.es/process-document/
3. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replaceAll


## AJ 1.7 JavaScript i integrerade system

JavaScript är ett mycket användbart skriptspråk inom webbutveckling. Det används både på klientsidan (frontend) och alltmer inom backend-utveckling med hjälp av olika ramverk och plattformar som Node.js. Detta gör JavaScript till ett kraftfull och ett av de mest populära och användbara programmeringsspråken idag. JavaScript används också utanför webben i prylar som har inbyggda och integrerade system. För att förstå hur JavaScript tillämpas i dessa system är det viktigt att kunna skilja på begreppen inbyggda och integrerade system:

Inbyggda system: 
Inbyggda system är datorer som är designade för att utföra specifika uppgifter inom en större produkt. De finns ofta i saker som hushållsapparater, bilar eller medicinsk utrustning och arbetar i bakgrunden utan att vi märker det. Dessa system är ofta små och optimerade för att använda så lite hårdvara och energi som möjligt.

Ett par exempel på inbyggda system är mikrokontroller i diskmaskiner, termostater eller sensorer i smarta hem-enheter.

Fördelar av inbyggdad system:
- Optimering: Eftersom inbyggda system är designade för specifika uppgifter, kan de optimeras för att vara både energieffektiva och snabba. De är alltså riktigt bra på just det de är skapade för att göra.
- Tillförlitlighet: Dessa system är ofta byggda för att vara väldigt stabila och kunna fungera utan problem under lång tid, även i tuffa miljöer. Du kan lita på att de gör sitt jobb utan att krångla.
- Lägre kostnader: Eftersom inbyggda system är optimerade för specifika funktioner, kan de tillverkas med billigare och enklare hårdvara. Det betyder att produktionskostnaderna kan hållas nere.

Integrerade system:
Integrerade system är som en avancerad version av inbyggda system. De består av flera komponenter eller delsystem som samarbetar för att nå ett gemensamt mål. Dessa system kombinerar både mjukvara och hårdvara som kommunicerar och arbetar tillsammans för att utföra mer komplexa uppgifter. Du hittar integrerade system i avancerade tekniska lösningar som intelligenta trafiksystem eller stora nätverksbaserade IoT-arkitekturer.

Integrerade system inkluderar smarta hem automatiserade fabriker och självkörande bilar där flera inbyggda system samarbetar för att säkerställa att allt fungerar smidigt och koordinerat.

Fördelar med integerade sytem:
- Skalbarhet: Integrerade system kan byggas ut med nya komponenter och funktioner utan att det påverkar stabiliteten hos den övergripande lösningen vilket gör det enkelt att anpassa till förändrade behov.

- Komplexitetshantering: Eftersom flera olika komponenter samarbetar kan dessa system hantera mer komplexa uppgifter och erbjuda mer avancerade funktioner än enskilda inbyggda system.

- Flexibilitet: De kan anpassas till olika miljöer och krav genom att nya moduler eller delsystem läggs till och interagerar med befintliga system.

JavaScript har många viktiga användningsområden inom integrerade system. För det första används det ofta i IoT-applikationer för att möjliggöra kommunikation mellan olika enheter och servrar. Med hjälp av ramverk som Node.js kan utvecklare skapa serverlösningar som effektivt samlar in och bearbetar data från olika sensorer och enheter i realtid. Dessutom används webbläsarbaserade gränssnitt i många integrerade system vilket gör det möjligt för användare att styra och övervaka enheter. JavaScript spelar en stor central roll genom att skapa dynamiska och responsiva användargränssnitt vilket gör det enkelt för användare att interagera med systemet via sina smartphones eller datorer.

JavaScript används också för datahantering och analys inom integrerade system. Genom att använda bibliotek som D3.js eller Chart.js kan utvecklare effektivt visualisera data som samlas in från olika källor. Slutligen kan JavaScript användas för att automatisera uppgifter och processer i dessa system som leder till ökad efiktivet. 

1. https://www.techtarget.com/iotagenda/definition/embedded-system
2. https://www.kth.se/social/upload/214/Lecture2_2.pdf
3. https://www.spiceworks.com/tech/tech-general/articles/what-are-embedded-systems/
4. https://skillupwards.com/blog/data-visualization-with-javascript-chart-js-and-d3-js

## AJ 1.8 Native bundeling av JavaScript för olika operativsystem och enheter

Native bundling packar en app och dess nödvändiga beroenden i ett format som kan köras direkt på en specifik plattform eller ett operativsystem. Detta gör att appen beter sig som om den var byggd med plattformens egna språk och verktyg. Syftet är att ge användarna en upplevelse som känns mer "native" och låta appen använda plattformens resurser för att prestera optimalt.

Ett kraftfullt verktyg för native bundling i JavaScript-ekosystemet är React Native, som utvecklades av Facebook. Till skillnad från traditionella web-to-desktop-ramverk, tillåter React Native utvecklare att bygga mobila applikationer för både Android och iOS med hjälp av JavaScript, samtidigt som koden kompileras till faktiskt native kod. Världskända företag som Instagram, Airbnb och Tesla använder React Native, vilket visar på dess styrka och mångsidighet. Plattformen har en stor och aktiv community som erbjuder ett brett utbud av moduler och bibliotek, vilket underlättar för utvecklare att snabbt implementera komplexa funktioner.

Fördelar med native bundling:

Korsplattformskod: Utvecklare kan skriva koden en gång och sedan distribuera den på flera operativsystem. Detta sparar tid och minskar behovet av att underhålla separata kodbaser för varje plattform.

Enklare distribution: Genom att paketera alla beroenden tillsammans säkerställer native bundling att applikationen kan köras på olika system. Detta eliminerar behovet av komplexa installationsprocesser eller versioneringsproblem.

Tillgång till native API:
Applikationen kan använda systemfunktioner som filhantering, notifikationer och systemintegration utan behov av en webbläsare, vilket ger en smidig användarupplevelse.

Nackdelar med native bundling:

Stora filstorlekar: Bundlade appar kan bli ganska stora eftersom hela runtime-miljön ofta inkluderas, vilket kräver mycket lagringsutrymme.

Prestandaproblem: Native bundlade appar, såsom de som byggts med Electron, använder mer minne och CPU-resurser än appar som utvecklats med språk som Swift eller C++.

Avsaknad av plattformspecifika förbättringar: Även om appen fungerar på flera plattformar kanske den inte utnyttjar plattformspecifika optimeringar eller designelement, vilket kan leda till en mindre polerad användarupplevelse.

Native bundling är utmärkt när man behöver lansera en app snabbt på flera plattformar utan att skriva om koden för varje plattform. Det är också idealiskt för prototyper intern verktyg eller appar där snabb leverans är viktigare än maximal prestanda. Däremot är det kanske inte det bästa valet för appar som kräver hög prestanda som spel eller resurskrävande applikationer/program.

1. https://www.freecodecamp.org/news/react-js-vs-react-native-whats-the-difference/
2. https://www.computer.org/publications/tech-news/trends/benefits-of-react-native
3. https://www.netguru.com/glossary/react-native