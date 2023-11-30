# Teorihandboken - Backendutveckling (BE)
Studerande: Shaker Nasser

## BE 1.1 PHP

PHP (Hypertext Preprcessor) är en server-by-side skriptspråk. Ett skriptspråk som kan exekterveras (köras) utan ett komplitationssteg. Detta innebär att PHP hjälper märkspråk så som HTML till att genera sidor. Detta sker genom att man kopplar upp mot en databas. PHP är en väldigt användbar skriptspråk, runt 78% av dem undersökta webbsidor använder sig av PHP (W3techs, mars 2013).
Skriptspråket har sin grund i programmeringsspråket C och C++. PHP utveckaldes och utvidgades till en objektorienterad programmeringspråk.

PHP kan användas för programmering av konsolapplikationer och grafiskt användargränssnitt. Det används först och främst för programmering av dynamiska webbsidor på Internet. Genom PHP-programmering kan man skapa en dynamisk hemsida. En dynamisk hemsida gör att en besökare kan interagera med innehållet på ett helt annat sätt än om hemsidan enbart använde HTML. Det går exempelvis att köpa en produkt eller skriva ett meddelande på en dynamisk hemsida. Något värt att veta är att alla hemsidor har en del som är ren HTML-kodning. Detta för att besökarnas webbläsare ska få relevant information om hur den ska tolka kodningen.

1. https://www.oxfordwebstudio.com/sv/vet-du/vad-ar-php 
2. https://dbwebb.se/kunskap/kom-i-gang-med-php-pa-20-steg

## BE 1.2 OOP i PHP

OOP är objektorinterad progammering som används även i PHP. Detta gör att det är lättare att strukutera och läsa av en koden. Koden organiseras genom att använda objekt, som instanser av klasser. Modifiering blir enklare och avläsning både maskinellet och mänskligt blir enklare. Klasser definerar egenskaper (varibaler) och metoder(funktionerna) som kan användas från den klassen. OOP-koncept som inkapsling, arv och polymorfism är centrala för att förstå och använda objektorienterad programmering i PHP. 
Konstruktor används 

``` php
<?php

class Person {
    public $name;
    public $age;

    // Konstruktor
    public function __construct($name, $age) {
        $this->name = $name;
        $this->age = $age;
        echo "En ny person har skapats.";
    }
}

// Skapa en instans av klassen (och kalla på konstruktorn)
$person1 = new Person("Alice", 25);

?>
```

Ett objekt är en konkret instans av en klass. När du skapar ett objekt från en klass, får objektet tillgång till de egenskaper och metoder som definierats i klassen. Objekten är de faktiska "föremålen" eller "instanserna" som skapas enligt klassens specifikationer.

```php

$minBil = new Bil();
$minBil->modell = "Volvo";
$minBil->färg = "Blå";
$minBil->köra(); // Anropar metoden köra från klassen Bil

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

    // Konstruktor
    public function __construct($startNamn) {
        $this->namn = $startNamn;
        echo "En ny person skapades med namnet $startNamn.";
    }
}

// Skapa ett objekt och anropa konstruktorn automatiskt
$nyPerson = new Person("Anna");


```

## BE 1.3 Säkerhet i PHP

Beskriv rubriken här

## BE 1.4 MVC

Beskriv rubriken här

## BE 1.5 Wordpress

Beskriv rubriken här

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
CREATE TABLE UserData (
    UserId INT PRIMARY KEY AUTO_INCREMENT,
    Username VARCHAR(100),
    Email VARCHAR(100),
    Phonenumber VARCHAR(20)
);

```

Efter att tabellen är skapad så skapar man input data genom kommando (Insert):


```sql
INSERT INTO UserData (Username, Email, Phonenumber)
VALUES ('newuser', 'newuser@example.com', '123-456-7890');

```

För att söka data i SQL genom kommando (Read (SELECT)) 

```sql
SELECT * FROM UserData;

```

Select har väldigt många avändbara kommandon. Här räknar man anatal användare: 

```sql
SELECT COUNT(*) AS AntalAnvandare FROM UserData;

```

Här tar man ut den specifika datan från tabellen:

```sql 
SELECT username, email FROM UserData;

```

Uppdatera (Lägga till ex en rad till) data i SQL genom kommando (update) 

```sql
UPDATE UserData
SET Phonenumber = '987-654-3210'
WHERE UserId = 1; -- Replace 1 with the actual user ID you want to update

```

För att radera data med kommando(delete)

```sql
DELETE FROM UserData WHERE UserId = 2;

```

1. https://herovired.com/learning-hub/blogs/difference-between-primary-key-and-foreign-key/
2. https://www.tutorialspoint.com/dbms/er_diagram_representation.htm
3. https://aws.amazon.com/what-is/sql/
4. https://svenskatack.wordpress.com/teknik-och-data/databaser/sql/

## BE 1.8 OAuth i backend

Beskriv rubriken här

## BE 1.9 HTTP-protokollet

Beskriv rubriken här

## BE 1.10 cURL

Beskriv rubriken här

## BE 1.11 REST

Beskriv rubriken här

## BE 1.12 XML och andra dataformat

Beskriv rubriken här

## BE 1.13 Webbservrar

Beskriv rubriken här
