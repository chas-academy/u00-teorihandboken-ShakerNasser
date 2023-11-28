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

```
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

Klasser och objekt 

Publika och privata 

Konstruktören

## BE 1.3 Säkerhet i PHP

Beskriv rubriken här

## BE 1.4 MVC

Beskriv rubriken här

## BE 1.5 Wordpress

Beskriv rubriken här

## BE 1.6 Heirarkiska databaser

Beskriv rubriken här

## BE 1.7 Relationsdatabaser, SQL och ER-modellering

Beskriv rubriken här

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
