# Teorihandboken - Backendutveckling (BE)
Studerande: Shaker Nasser
![Alt text](images/Backend-utveckling.png)
## BE 1.1 PHP

PHP (Hypertext Preprcessor) är en server-by-side skriptspråk. Ett skriptspråk som kan exekterveras (köras) utan ett komplitationssteg. Detta innebär att PHP hjälper märkspråk så som HTML till att genera sidor. Detta sker genom att man kopplar upp mot en databas. PHP är en väldigt användbar skriptspråk.

PHP kan användas för programmering av konsolapplikationer och grafiskt användargränssnitt. Det används först och främst för programmering av dynamiska webbsidor på Internet. Genom PHP-programmering kan man skapa en dynamisk hemsida. En dynamisk hemsida gör att en besökare kan interagera med innehållet på ett helt annat sätt än om hemsidan enbart använde HTML. Det går exempelvis att köpa en produkt eller skriva ett meddelande på en dynamisk hemsida. Något värt att veta är att alla hemsidor har en del som är ren HTML-kodning. Detta för att besökarnas webbläsare ska få relevant information om hur den ska tolka kodningen.

1. https://www.oxfordwebstudio.com/sv/vet-du/vad-ar-php 
2. https://dbwebb.se/kunskap/kom-i-gang-med-php-pa-20-steg

## BE 1.2 OOP i PHP

OOP är objektorinterad progammering som används även i PHP. Detta gör att det är lättare att strukutera och läsa av en koden. Koden organiseras genom att använda objekt, som instanser av klasser. Modifiering blir enklare och avläsning både maskinellet och mänskligt blir enklare. Klasser definerar egenskaper (varibaler) och metoder(funktionerna) som kan användas från den klassen. OOP-koncept som inkapsling, arv är centrala för att förstå och använda objektorienterad programmering i PHP. 
Konstruktor används 

``` php
<?php

class Person {
    public $name;
    public $age;

    public function __construct($name, $age) {
        $this->name = $name;
        $this->age = $age;
        echo "En ny person har skapats.";
    }
}

$person1 = new Person("Alice", 25);

?>
```

Ett objekt är en konkret instans av en klass. När du skapar ett objekt från en klass, får objektet tillgång till de egenskaper och metoder som definierats i klassen. Objekten är de faktiska "föremålen" eller "instanserna" som skapas enligt klassens specifikationer.

```php

$minBil = new Bil();
$minBil->modell = "Volvo";
$minBil->färg = "Blå";
$minBil->köra();

```

Publika medlemmar (variabler och metoder) är de som kan nås och användas utanför klassen. De är synliga och tillgängliga för andra delar av koden, inklusive andra klasser.

```php

class Konto {
    public $saldo;

    public function sättSaldo($belopp) {
        $this->saldo = $belopp;
    }
}

```

Privata medlemmar är begränsade till att endast vara åtkomliga inom den klass där de är deklarerade. De är inte synliga eller tillgängliga utanför klassen och används för att skydda interna detaljer och säkerställa att de inte påverkas externt.

```php
class Användare {
    private $användarnamn;
    private $lösenord;

    public function sättAnvändarnamn($namn) {
        $this->användarnamn = $namn;
    }

    public function sättLösenord($lösen) {
        $this->lösenord = $lösen;
    }
}

```

En konstruktor är en särskild metod i en klass som körs automatiskt när ett objekt skapas. Dess huvudsakliga syfte är att initialisera objektets egenskaper eller utföra andra förberedande åtgärder. Konstruktorn kallas automatiskt när du skapar ett objekt och används för att ge objektet

```php

class Person {
    public $namn;


    public function __construct($startNamn) {
        $this->namn = $startNamn;
        echo "En ny person skapades med namnet $startNamn.";
    }
}


$nyPerson = new Person("Anna");

```

## BE 1.3 Säkerhet i PHP

Säkerhet är en viktig aspekt för att skydda information och system från obehörig åtkomst, skadlig kod och andra hot, särskilt inom IT. Här följer några relaterade begrepp:

IT-säkerhet (Informationstekniksäkerhet):
IT-säkerhet handlar om att skydda informationstekniksystem från obehörig åtkomst, användning, förändring eller förstörelse. Det innefattar olika åtgärder och tekniker för att säkerställa konfidentialitet, integritet och tillgänglighet av data och system.

Applikationssäkerhet:
Applikationssäkerhet fokuserar på att säkra programvaror och applikationer från olika hot och sårbarheter. Det innebär att implementera säkerhetsåtgärder i design, utveckling och drift av applikationer för att minimera riskerna för attacker och obehörig åtkomst.

SQL-injektioner:
SQL-injektioner är en typ av säkerhetshot som riktar sig mot databasdrivna applikationer. Vid en SQL-injektion kan en angripare infoga skadlig SQL-kod i en SQL-fråga som utförs av en applikation. Om sårbarheten utnyttjas framgångsrikt kan detta leda till obehörig åtkomst, manipulation eller förstörelse av databasen. För att förhindra SQL-injektioner bör utvecklare använda parametriserade frågor och sanitisering.

## BE 1.4 MVC

MVC, eller Model-View-Controller, är en designmönster som används inom mjukvaruutveckling för att organisera och strukturera koden på ett sätt som gör den mer modulär, underhållbar och skalbar. Genom att dela upp applikationen i tre huvudkomponenter separeras logik, presentation och datahantering. Modellen representerar data och regler för att hantera den, vyn är ansvarig för presentationen av data till användaren, och kontrollern hanterar interaktionen mellan modellen och vyn. Genom att använda sig av MVC-mönstret kan utvecklare skapa robusta applikationer med en tydlig separation av ansvar och möjliggöra enkel återanvändning av kod.

Klienten skickar en HTTP-förfrågan till servern (hårdvara): I denna begäran specificeras en IP-adress och olika HTTP-metoder som GET, POST eller andra beroende på ändamålet med förfrågan.

Förfrågan passerar genom webbservern (mjukvara): Webbservern tar emot och hanterar HTTP-förfrågan. Den är ansvarig för att vidarebefordra förfrågan till rätt del av applikationen och för att kommunicera med den.

Kontrollerar kod och ger svar i form av HTTP-respons: Nu kommer MVC-arkitekturen in i bilden. Kontrollern tar emot förfrågan och bearbetar den. Den anropar den relevanta modellen för att hämta eller manipulera data, och kan även interagera med vyn för att få information om hur datan ska visas. Slutligen skickar kontrollern en HTTP-respons tillbaka till klienten.

MVC gör det enkelt att återanvända en skriven kod och reducerar komplixtet i koden. Med detta så ökar flexibitet i kodskrivningen. Det minskar även återupprepning av händeleser. 

Model: Bearbeta och skicka vidare data. Modellen har ansvaret för att behandla och hantera applikationens data. Det innebär att hämta information från externa källor, till exempel en databas, bearbeta och manipulera datan enligt affärsreglerna och sedan skicka den vidare till andra delar av systemet, särskilt till vyn för att visas för användaren.

View: Här skriver vi våra frågor. Modellen innehåller vanligtvis metoder och funktioner för att skapa och utföra frågor (queries) för att hämta, uppdatera och spara data i en databas eller annan form av datalagring. Dessa frågor används för att interagera med datakällor och återspegla de önskade operationerna på datan.

Controller: Vanligtvis ansluten till en databas. Modellen är oftast kopplad till en databas eller annan typ av datalagring. Den är ansvarig för att kommunicera med databasen och utföra de nödvändiga operationerna för att hämta eller uppdatera datan. Detta gör det möjligt att separera hanteringen av databasen från resten av applikationslogiken.

----------------------------
Separation av ansvar (Ansvarsfördelning) i MVC-strukturen innebär att varje komponent har ett specifikt ansvarsområde:

Modeller (Models): Hanterar data och utför operationer relaterade till datalagring. Modellen behandlar och manipulerar data enligt applikationens affärslogik.

Vyer (Views): Innehåller mallar eller templates för att definiera hur data ska representeras visuellt. Vyn är ansvarig för att presentera informationen för användaren på ett sätt som är användarvänligt och förståeligt.

Kontrollanter (Controllers): Hanterar och bearbetar HTTP-förfrågningar. Kontrollanten samordnar interaktionen mellan modellen och vyn. Den avgör vilken modell och vy som ska användas för att svara på en specifik förfrågan och skickar därefter lämplig HTTP-respons till klienten.

## BE 1.5 Wordpress

Wordpress är en hemsideverktyg med öppen källkod. Wordpress ger möljghet till att starta en sida och hosta besökare. Starten av Wordpress var att underlätta möjligheten till bloggplattformar att utvecklas. Nu används Wordpress av flera stora miljardföretag så som Microsoft och Spotify. 

Plugins är tillägg som läggs till WordPress för att lägga till funktionalitet. Det finns tusentals plugins som täcker allt från sökmotoroptimering (SEO) till sociala medier och säkerhet. WordPress stöder olika typer av innehåll, inklusive text, bilder, ljud och video.

WordPress använder teman för att styra webbplatsens utseende och känsla. Det finns tusentals gratis och premiumteman tillgängliga för att anpassa utseendet på webbplatsen.

WordPress har utvecklats över tid och har blivit ett av de mest använda CMS-systemen globalt. Det har även blivit ett populärt val för både små och stora företag samt enskilda användare som vill skapa och underhålla sina egna webbplatser.

## BE 1.6 Heirarkiska databaser

En data bas är samling av data som finns lagrad för hämtas i bitar. Förr i tiden använde man papper och penna för att spara data. Detta kallades för analog databas. Nu förtiden sköts det mesta genom elektroniskt databas. 

Hierarkiska databaser är en specifik modell inom databasvärlden som organiserar data i en trädliknande struktur. I denna struktur kallas varje datatopp för en nod och kan ha noll eller flera underordnade noder. Root-noden representerar den översta nivån av hierarkin, och därifrån grenar sig trädet ut med föräldrar, barn och segment.

Denna modell används inom olika områden, till exempel för att representera organisationsträd där avdelningar och anställda struktureras hierarkiskt. Likaså återspeglar filsystemet på datorer en hierarkisk struktur, där varje mapp representerar en nod och filer ligger som löv i trädet. Hierarkiska databaser lämpar sig också väl för att hantera produktstrukturer där varje komponent kan ha underdelar.

Fördelarna med hierarkiska databaser inkluderar deras effektivitet när det gäller att hantera naturligt hierarkisk data och möjligheten att snabbt navigera mellan närliggande noder. Genom att använda hierarkiska databaser kan man enkelt organisera och strukturera data på ett sätt som återspeglar verkliga hierarkier.

Strukturen i hirearkiska databaser är väldigt minneskrävande till skillnad från relationsdatabaser. Sökningen av data generaras långsamt. Dessutom erbjuder hierarkiska databaser enkelhetsfaktor vid sökning och åtkomst av data. Eftersom varje nod har tydliga föräldrar och underordnade noder, kan man snabbt hitta och manipulera specifika datapunkter utan att behöva söka igenom hela databasen.

![Bild på hur Hirarkiska databaser kan se ut](images/hierarchical-database-model-l.jpg)

1. https://www.heavy.ai/technical-glossary/hierarchical-database
2. https://www.redswitches.com/blog/hierarchical-databases/
3. https://www.c-sharpcorner.com/article/what-is-a-hierarchical-database/

## BE 1.7 Relationsdatabaser, SQL och ER-modellering

Relationella databaser utgör en grundläggande modell inom hanteringen av databaser och arbetar med tabeller och de relationer som finns mellan dessa tabeller. Genom att organisera data i tabellformat minskar relationella databaser onödig upprepning av information och främjar därmed en effektiv och strukturerad lagring av data.

Varje tabell i en relationsdatabas följer ett fördefinierat schema som beskriver strukturen och innehållet i tabellen. Detta schemas beskrivning fungerar som en vägledning för vilken typ av data som kan lagras i tabellen. Schemat ger en tydlig översikt över databasens struktur och underlättar både förståelsen och hanteringen av dess innehåll.

Inom relationsdatabaser används även dimensionstabeller för att organisera data. Dessa tabeller består av rader, också kallade tupler, där varje rad representerar en entitet eller objekt, och varje kolumn, eller attribut, ger en beskrivning av data som är relaterad till entiteten.

I en relationsdatabas är det viktigt att förstå skillnaden mellan en primärnyckel och en främmande nyckel för att säkerställa integriteten och relationerna inom datastrukturen.

En primärnyckel fungerar som en unik identifierare för varje post i en tabell och säkerställer att varje rad kan identifieras på ett entydigt sätt. Den måste ha unika värden och får inte vara NULL. Primärnyckeln är avgörande för att upprätthålla dataintegriteten och underlättar effektiv hämtning av data.

Å andra sidan är en främmande nyckel ett fält i en tabell som skapar en länk till primärnyckeln i en annan tabell. Denna länk skapar en relation mellan de två tabellerna och möjliggör implementeringen av referentiell integritet. Med andra ord motsvarar en främmande nyckel i en tabell primärnyckeln i en annan tabell och främjar anslutningen mellan relaterade data över olika tabeller i databasen.

![Bild på Realtionsdatabas](images/Relationsdatabas.png)

ER-diagram (Entity-Relationship) är en grafisk representation som används för att visualisera och planera strukturen av en relationsdatabas. Genom att använda symboler och linjer för att representera entiteter och deras relationer ger ER-diagrammet en visuell översikt över databasens struktur och hjälper till att förstå hur olika tabeller är kopplade till varandra.

SQL, eller Strukturerat Frågespråk, är det standardspråk som används för att interagera med relationsdatabaser. SQL har två huvudsakliga komponenter:

DDL (Data Definition Language) denna del hanterar strukturer och definitioner av databasobjekt, inklusive skapandet och ändringen av tabeller, index och andra strukturer.

DML (Data Manipulation Language) fokuserar på manipulation av data i databasen, inklusive insättning, uppdatering och borttagning av data.

Genom att använda SQL kan användare effektivt definiera och hantera både databasens struktur och dess innehåll, vilket gör det till ett kraftfullt verktyg för att interagera med relationella databaser.

Exempel på hur man kan skapa en SQL tabell med kommando (Create):

```sql
DROP TABLE IF EXISTS `tasks`;
CREATE TABLE `tasks` (
  `id` int(255) NOT NULL AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `description` text DEFAULT NULL,
  `is_completed` tinyint(1) DEFAULT 0,
  PRIMARY KEY (`id`)
) ;

```

Efter att tabellen är skapad så skapar man input data genom kommando (Insert):


```sql
INSERT INTO `tasks` (`title`, `description`, `is_completed`)
VALUES ('Min första uppgift', 'Detta är beskrivningen för min första uppgift', 0);

```

För att söka data i SQL genom kommando (Read (SELECT)) 

```sql
SELECT * FROM tasks;

```

Select har väldigt många avändbara kommandon. Här räknar man anatal användare: 

```sql
SELECT COUNT(*) AS AntalUppgifter FROM tasks;

```

Här tar man ut den specifika datan från tabellen:

```sql 
SELECT title, description FROM tasks;

```

Uppdatera (Lägga till ex en rad till) data i SQL genom kommando (update) 

```sql
UPDATE tasks
SET is_completed = 1
WHERE id = 1;

```

För att radera data med kommando(delete)

```sql
DELETE FROM tasks WHERE id = 2;

```

1. https://herovired.com/learning-hub/blogs/difference-between-primary-key-and-foreign-key/
2. https://www.tutorialspoint.com/dbms/er_diagram_representation.htm
3. https://aws.amazon.com/what-is/sql/
4. https://svenskatack.wordpress.com/teknik-och-data/databaser/sql/

## BE 1.8 OAuth i backend


Autentisering (Eng: Authentication) handlar om att verifiera vem någon påstår sig vara.

Autentisering används av en server för att känna igen vem som försöker få tillgång till specifik information. En användare eller dator bekräftar sin identitet för servern genom att ange användarnamn eller lösenord. Det kan också göras med andra autentiseringsmetoder som kort eller appar, samt moderna igenkänningsverktyg som röst- eller näthinneigenkänning.

Exempel:

1. På ChasAcademy använder de appen Securitas Flow för att komma in i skollokalen.
2. Fingeravtryck används i många moderna telefoner för att bekräfta identitet.

Det här steget handlar inte om att bestämma vad personen får göra i systemet, utan bara om att identifiera dem.

Auktorisering: Står för vad autensierad entiet har för rättigheter att göra på en (plattform).

I denna process så handlar det om att avgöra vad en klient har för rättigheter att använda resuresen. Detta sker oftast i sammband med autisering för att få en uppfattning om vem klieten är. 

Oauth2: 

Oauth2 används för autentisering och behörighetskontroll och denna standard är de vnaligaste sättet att sköta authorization och öka säkerheten i en applikation. I många aplikkationer kan man hitta andra befientliga leverantörer av Oauth som även går under namnet "Third Party Auth Providers". 
Dessa kan oftast se om man tex vill logga in på TikTok där det står "Sign in with [AppleLogin]".
Genom att använda detta steg så slipper man implemntera hantering av lösenord och kryptering då dessa sköts av Oauth leverantören. 

Grant types:
Olika sätt att applikationer får tillgång till användardata från autentiserande tjänster som Google eller Facebook, innefattar följande:

Client Credentials: Används när två maskiner, som till exempel två olika applikationer eller API:er, behöver kommunicera med varandra. 

Authorization Code: Typiskt används denna typ för att logga in på en tjänst eller applikation. Till exempel, när en användare loggar in på en webbplats med sitt Google-konto, används denna metod för att verifiera användarens identitet och ge dem åtkomst till tjänsten.

Password Grant: Denna typ kräver att användaren anger sina faktiska inloggningsuppgifter, som användarnamn och lösenord, för att få åtkomst till resurser. Detta sker när en användare loggar in direkt på en tjänst.

Refresh Grant: Används för att skapa en ny åtkomsttoken när en tidigare token har utgått. 

1. https://medium.com/web-security/understanding-oauth2-a50f29f0fbf7
2. https://developers.google.com/identity/protocols/oauth2/javascript-implicit-flow

## BE 1.9 HTTP-protokollet

GET och POST anrop som kommuuncerar med servar. 

Finns och nackdelar med båda protokollen. 

https://developer.mozilla.org/en-US/docs/Web/HTTP
https://www.w3schools.com/php/php_forms.asp

## BE 1.10 cURL

Beskriv rubriken här

## BE 1.11 REST

Förklara API:er:

REST står för regler och struktur av API:er. Detta är samling av konveationer för hur API:er ska utformas och fungera. 

Konveationer:

Seperation av klient och server:
Frontend och backend ska kunna utvecklas oberonende av varandra. 
Utvecklning av kod som sker i Frontend ska inte påverka Backend och vice versa. 

Statelessness:

Svar som går att cache:a:



Uniformt interface:


REST (Representational, State och transfer.)

Apier:
Öppna
Stängda

https://restfulapi.net/rest-api-design-tutorial-with-example/

## BE 1.12 XML och andra dataformat

XML (Extensible Markup Language):
XML är en förkortning av "Extensible Markup Language". Det är ett strukturerat metaspråk som används för att definiera och organisera data. XML tillåter användare att skapa sina egna märkesspråk och definiera egna taggar för att strukturera och beskriva information. Det är användbart för att överföra och lagra data mellan olika program och plattformar. Eftersom det är textbaserat och strukturerat underlättar det för både datorer och människor att förstå och hantera data på ett enhetligt sätt.

CSV (Comma-Separated Values):
CSV står för "Comma-Separated Values". Det är ett enkelt filformat som används för att representera tabulära data, såsom en databastabell eller ett kalkylblad, i en textfil. I en CSV-fil separeras varje datapost med kommatecken, och varje rad representerar en rad i tabellen. CSV-filer är lätta att skapa, läsa och redigera manuellt, vilket gör dem mycket användbara för att överföra och dela tabulära data mellan olika program. CSV-filer stöds av många program, inklusive kalkylbladsprogram och databasverktyg.

## BE 1.13 Webbservrar

En webbserver är en central komponent i den digitala världen, och dess roll är avgörande för att möjliggöra kommunikation och överföring av information över internet. Begreppet "webbserver" syftar vanligtvis till både hårdvaran och mjukvaran som krävs för att hantera och svara på förfrågningar från klientdatorer. I denna text kommer vi att utforska olika aspekter av webbservrar, inklusive deras historia, funktioner och några exempel på populära webbserverprogram.

Webbserverns historia kan spåras tillbaka till 1989 när Sir Tim Berners-Lee, en brittisk fysiker, föreslog en modell för ett hypertextsystem. Ursprungligen hade modellen bara stöd för GET-metoden, men senare lades POST-metoden till för att möjliggöra interaktion med servrar på ett mer komplett sätt. Det var detta innovativa förslag som lade grunden för den moderna webbservern.

En webbserver är i grund och botten en dator som är specialdesignad för att hantera förfrågningar och överföra data till och från andra servrar. Dessa servrar är oftast placerade hos driftbolag som erbjuder snabb och kraftfull internetuppkoppling.

Webbserverns huvudsakliga uppgifter inkluderar att ta emot förfrågningar från klientdatorer, utföra HTTP-metoder, generera och skicka tillbaka HTTP-respons och vid behov logga händelser och generera statiska sidor.

Vanliga Uppgifter för Webbservern:

Ta emot Förfrågningar: Webbservern fungerar som en mottagare för förfrågningar från klientdatorer, vilket kan vara allt från att hämta en webbsida till att skicka data till en databas.

Hantera HTTP-metoder: En central del av webbserverns arbete är att hantera olika HTTP-metoder som GET och POST för att möjliggöra kommunikation mellan klient och server.

Skicka HTTP-svar till Klienten: Webbservern genererar och skickar tillbaka HTTP-svar till klienten, vilket kan inkludera den begärda webbsidan eller annan data.

Logga Händelser (valfritt): Många webbservrar erbjuder möjlighet att logga olika händelser och aktiviteter för övervakning och felsökning.

Generera Statiskt Innehåll (valfritt): Vissa webbservrar kan också generera statiska sidor för att accelerera sidbelastningstider och minska belastningen på servern.

De viktigaste serverprogrammen:

En av de mest använda serverprogrammen är HTTPd, som fungerar i bakgrunden och agerar som en server i den övergripande klient-server-modellen. Det använder HTTP/HTTPS-protokollet för att underlätta kommunikationen mellan webbservern och klientdatorerna.

Hur används en webbserver?

En webbserver används genom att klientdatorer skickar förfrågningar till den för att hämta webbsidor eller annan information. Klienten gör detta genom att skicka HTTP-förfrågningar, och webbservern svarar med den begärda informationen i form av HTML eller andra filformat.

Apache HTTP Server: En av de äldsta och mest använda webbserverprogrammen är Apache HTTP Server. Det är känt för sin stabilitet och flexibilitet.

Nginx HTTP Server: En annan populär webbserver är Nginx HTTP Server, som är känd för sin höga prestanda och skalbarhet, särskilt när det gäller hantering av många samtidiga anslutningar.

Lighttpd: En lättviktig webbserver som fokuserar på hög prestanda och låg minnesanvändning är Lighttpd.

CERN HTTPd HTTP Server: CERN HTTPd HTTP Server är en tidigare webbserver som spelade en viktig roll i webbens historia och utveckling.

Intranet:
