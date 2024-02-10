Vad är skillnaden mellan Javascript och Ecmascrpit?

JavaS Programmeringsspråk
Javascript är objektorinterad sppråk 
Ecama – specifaktion som definerar språket – den senaste ECMA vi jobbar på är ES2015-ES6
Vad är en variabel?
En variabel är en placeholder för en typ av datatyp/värde.
Variabler används för att hålla specifika värden ochknyta dessa
 Till ett specifikt namn.
I javaS finns det dessa varibaler:
Automatically
- Using var (äldre webbläsare) 
- Using let
- Using const
Dessa datatyper/värden:
- string
- boolean
- number
- array
- object
- undefined
- null
JavaScript innehåller operatorer som är samma som andraspråk.
 Enoperatör utför någon operation på enstaka eller flera
 operander (datavärde) och producerarettresultat.
 Till exempel ,
 1+2 är “+” tecknet enoperator och 1 är
 vänster sida operand och 2 är höger sida operand. Operatorn “+”
 utför tillägg av två numer i ska värden och returnerar ett resultat.
Vad är en Array och när används Arrayer?

-En variabel som kan innehålla mer än en värde/datatyp.
-Man kan komma åt (kalla på) världens genom att använda indexnumret som börjar med 0.
Vad gör en loop? Vilka olika sorters loopar finns det?
En bit kod som upprepas och körs så länge kriterna (kraven) för loopandet fylls. uttrycket skapas av kombination av jämföresle och logiska operatorer och loopen fortsätter så länge uttrycket är sant. 
for - loop
while - loop
do while - loop
for-of
for-in
Varför är felsökning (debugging) viktigt? 

För att kunna söka efter specifika fel utan att behöva köra om hela koden. Detta görs genom brytpunkt. 
Hjälper till att hitta fel i koden och ökar tillförlighet av koden och pålitlighet. 
Sparar tid och resuser genom att minska felaktiga kodning när det når produktion fas.
Ökar förmågan som programerare att uppfatta koden på enklare sätt.
Möljghet att kontrollera variabler, inspektera koden steg för steg och lösa problem efffikt. 

vad är  en funktion?
Funktioner är gruppering av instruktioner som tillsammans ger ett specifkt reslutat. Detta används för att slippa skriva samma set av kod flera gånger i programmet. 

Hur definerar man funktionen? 
Defineras genom ett uttryck som börjar med nyckelordet "function". En funktion har parametrar och en body som innehåller statement som körs när funktionen anropas (kallas på). En funktion kan ha flera parametrar eller inga parametrar överhuvudtaget. 

Vad är scope?

vad är push?
push lägger till ett item längst bak på en array

vad är pop?
pop tar bort det senaste tillagda item i en array

OOP – objekt oriternade programering 
Oriterande programmering - centerar kring objekt- hur man strukterar och ordnar sin kod. 
De fyra grundpelarna i OOP 
1. Inkapsling
- Data och funktioner kopplade till en entitet
- Bara visa de detaljer som är viktiga att interagera med
2. Abstraktion -  
3. Arv - Hierarkier där klasser bygger på andra klasser 
Prototype inheritance
4. Polymorfism – 
Vad är en klass? 
I JavaScript är en "klass" en grundläggande komponent för att skapa objekt med liknande egenskaper och beteenden. Där man skapar en mall (blueprint) för att skaKlasser är en viktig del av objektorienterad programmering (OOP) och de tillåter oss att organisera och strukturera vår kod på ett sätt som underlättar återanvändning och hantering av komplexa system.pa objekt. 
Hur skapar man en klass? 
Man skapar en klass genom att använda ordet (keyboard reserved) ”class”. Den mest grundläggande syntaxten: 
class ChasAcademyStudent {
  // Här kan man definiera egenskaper och metoder för klassen
}


Vilka delar finns i en klass? 
Inuti klassen kan du definiera egenskaper och metoder. Ett exempel på en enkel klass med en egenskap och en metod skulle kunna se ut så här:

class Person {
  constructor(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }
  getFullName() {
    return `${this.firstName} ${this.lastName}`;
  }
}
För att skapa en instans av klassen, används nyckelordet new följt av klassens namn:
let person1 = new Person("John", "Doe");
Det är viktigt att notera att constructor är en speciell metod som körs när en instans av klassen skapas. Den används för att initialisera egenskaper för objektet.

Hur skapar man ett nytt objekt från en nuvarande class?

Dett genom att sätta Keyboard ordet ”New” före den nuvarande klassen. 

Hur kan man ärva ifrån en annan klass? 
Genom att använda ordet extend.

Hur kan man skapa privata fält och metoder i en klass?
Get och setters
Varför är det bra och använda getters och setters?

Hur skapar man objekt ifrån en klass? 

Asynkront fall – synkront fall 
Asynkrontf fall- flera olika fall körs 
Synkront fall – man måste vänta på varje fall ska vara slutförd tills man uppnår mål. 
asynkroʹn (av grekiska nekande a och synkron), icke samtidig, dvs. motsatsen till synkron.
https://webbling.se/index.php/Introduktion_till_asynkron_programmering

Callbacks 
Promieses

Fullfied, rejected och resolve
 
Then. 

Begrepp 
 Exekvera kod – Att köra kod
Koden exekveras på följande vis:
en webbläsare eller med Node Js 
Roadmap för JavaScript 

 
V.43 
Variabler 
Operatorer och operander 
V.44
Funktioner scopes olika loopar, if satser 
Inyggda metoder, mera om arrays, felsökning 
JavaScript OOP, Prototype interheritance 
Klasser och arv, getters och setters 
Asykrona funktioner, promises, Async/wait 
V.45
JavaScript DOM, DOM manipulation och eventhandling 
Api fetch 



