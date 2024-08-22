# Teorihandboken - Avancerad JavaScript (AJ)
Studerande: Förnamn Efternamn

## AJ 1.1 Node.js

Node.js är en välkänd och kraftfull plattform som används för att utveckla serverbaserade applikationer. Det är en öppen källkodsmiljö som kan köras på flera plattformar och gör det möjligt att använda JavaScript på serversidan. Node.js bygger på Googles V8-motor, samma motor som driver webbläsaren Google Chrome, vilket gör det möjligt att använda JavaScript utanför klientens webbläsare. Detta är en stor fördel för utvecklare då de kan använda samma programmeringsspråk både på servern och i webbläsaren, vilket skapar en mer enhetlig kodbas och en smidigare utvecklingsprocess.

En av de mest framstående funktionerna i Node.js är dess händelsedrivna och asynkrona arkitektur. Till skillnad från traditionella serverplattformar där operationer vanligtvis blockeras tills de är färdiga, är Node.js utformat för att utföra alla operationer asynkront. Detta innebär att servern inte behöver vänta på att ett anrop ska slutföras innan nästa uppgift hanteras, vilket leder till snabbare och mer responsiva applikationer. Detta är särskilt användbart när man arbetar med stora mängder samtidiga användare eller vid hantering av realtidsdata.

Node.js är även mycket populärt för att utveckla Single Page Applications (SPA). SPA är webbapplikationer där allt innehåll laddas på en enda sida och interaktionen med sidan hanteras genom JavaScript utan att hela sidan behöver laddas om. Genom att använda Node.js som backend tillsammans med front-end-ramverk som React eller Angular kan utvecklare skapa moderna, responsiva applikationer som ger användaren en snabb och smidig upplevelse.

![U08 projekt - NODEJS Express - REACT](images/node.js.png)

Den kraftfulla verktygen tillåter utvecklare att använda JavaScrit till för att skapa en backend-applikation som hanterar serverlogik, filsystem och nätverksoperatoner samt mtcket mer. Innan Node.js så användes javascript endast till fron-end applikationer. 

Node.js erbjuder en mängd funktioner för webbutveckling. Det använder en asynkron och icke-blockerande I/O-modell, vilket innebär att det kan hantera flera uppgifter samtidigt utan att behöva vänta på att en uppgift ska slutföras innan nästa påbörjas. Node.js körs på en enda tråd men använder en händelsedriven arkitektur, vilket möjliggör effektiv hantering av tusentals samtidiga anslutningar. Eftersom Node.js är byggt på Google V8-motorn, kan det exekvera JavaScript-kod snabbt och effektivt. Dessutom har Node.js ett omfattande ekosystem av paket genom Node Package Manager (NPM), vilket gör det enkelt att återanvända kod och installera externa moduler för att underlätta utvecklingsprocessen.

1. https://dev.to/mehedihasan2810/nodejs-best-practices-a-guide-for-developers-4d65
2. https://medium.com/@asiandigitalhub/what-is-node-js-and-how-it-work-490f5ecba665
3. https://www.simplilearn.com/tutorials/nodejs-tutorial/nodejs-backend
4. https://javascript.plainenglish.io/what-is-node-js-5fe50e4332c8
5. https://dev.to/vyan/how-to-structure-your-backend-code-in-nodejs-expressjs-2bdd
6. https://www.simplilearn.com/tutorials/nodejs-tutorial/what-is-nodejs

## AJ 1.2 Express

1. https://www.codecademy.com/article/what-is-express-js
2. https://medium.com/@Brilworks/what-is-express-js-a-comprehensive-guide-to-beginners-b289a25bd414
3. https://dev.to/bilal1718/how-to-create-a-backend-api-in-express-js-e0k
4. https://dev.to/dipakahirav/modern-api-development-with-nodejs-express-and-typescript-using-clean-architecture-1m77

## AJ 1.3 Progressive Web Apps
Beskriv rubriken här

## AJ 1.4 Typningssystem för Javascript (ex TypeScript, Flow)
Beskriv rubriken här

## AJ 1.5 Funktionell programmering i JavaScript
Beskriv rubriken här

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
Beskriv rubriken här

## AJ 1.8 Native bundeling av JavaScript för olika operativsystem och enheter
Beskriv rubriken här

