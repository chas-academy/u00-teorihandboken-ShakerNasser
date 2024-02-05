# Teorihandboken - Programmeringsmetodik (PG)
Studerande: Shaker Nasser
![Alt text](images/Programmeringsmetodik.png)

## PG 1.1 Versionshantering (Git)
GIT är ett kraftfullt verktyg för versionshantering som används av utvecklare för att effektivt spåra och hantera ändringar i källkoden under projektutveckling. Det ger en strukturerad och samarbetsvänlig metod för att spåra historiken över projektet och underlättar samtidigt arbete från flera utvecklare. Nedan presenteras en översikt över viktiga koncept inom GIT-versionshantering.

GIT möjliggör hantering av kodversioner över tid. Det skapar en tidslinje av ändringar, vilket gör det möjligt att återställa eller jämföra olika versioner av koden. Det är särskilt användbart när flera personer arbetar på samma projekt samtidigt.

I GIT kallas den centrala lagringen för källkoden för ett "repository". Det finns två typer av repositories: lokala och fjärr(remote). Lokala repositories lagras på utvecklarens dator, medan fjärrrepositories används för samarbete mellan flera utvecklare (Grupparbeten som u02 och u05).

GIT möjliggör utveckling på olika "grenar" samtidigt. En gren är en oberoende linje av utveckling där ändringar kan göras utan att påverka huvudkoden. Merging används för att kombinera ändringar från en gren till en annan.
Ibland uppstår konflikter när två grenar ändrar samma rad i koden. GIT erbjuder verktyg för att manuellt lösa konflikter innan de fusioneras, vilket säkerställer att koden förblir korrekt.

GIT tillåter användning av .gitignore-filer för att ange vilka filer eller mappar som ska ignoreras och inte spåras av versionshanteringen. Det är användbart för att undvika att känslig information och onödiga filer läggs till i repositoryt.

"Git Flow" är en populär metodik för att organisera arbetsflödet med GIT. Den inkluderar användningen av specifika grenar för funktioner, utveckling och utgåvor för att strukturera utvecklingsprocessen på ett organiserat sätt.

Git har blivit det föredragna verktyget för versionshantering inom öppen källkodsprojekt och används av miljontals utvecklare över hela världen.

![GIT](images/GIT-Branchand-its-Operations.webp)

Här nedan följer ett par grundläggande git kommandon:

Skapa en ny Git-repo:

```bash
git init

```

För att klona ner ett bifentligt repo:
```bash
git clone <repo-url>

```

Lägg till alla ändringar för att staging-området:

```bash
git add .

```

Skicka in stageade ändringar:

```bash
git push

```

Den mest användbara kommandon (enligt mig):

```bash
git status

```

1. https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners
2. https://www.atlassian.com/git/tutorials/what-is-git
3. https://www.freecodecamp.org/news/what-is-git-and-how-to-use-it-c341b049ae61/

## PG 1.2 Benchmarking

Inom webbutveckling är benchmark ett vanligt begrepp som används för att mäta och jämföra prestanda eller effektivitet hos olika webbplatser eller webbapplikationer. Det kan inkludera hastighetstester, laddningstider och andra metriker för att utvärdera hur väl en webbplats eller en specifik funktion presterar i jämförelse med branschstandarder eller konkurrenter. Att använda benchmarking i utvecklingsprocessen hjälper till att identifiera områden för förbättring och säkerställa en bättre användarupplevelse.

Lighthouse är en av dem verkygen som Goolge har utvecklat för att testa webbsidor när det gäller prestanda, tillgänglighet, bästa praxis och SEO. Det ger en övergripande bild av hur bra en webbplats presterar och ger förslag på förbättringar. Lighthouse kan betraktas som ett benchmarkverktyg eftersom det ger objektiva mätningar och riktlinjer för att jämföra en webbplats prestanda med etablerade standarder.

Goolge DevTools är en uppsättning av webbutvecklingsverktyg som ingår i de flesta webbläsare. Inom DevTools kan man använda olika flikar såsom Audits. För att utföra prestandamätningar och få förslag på förbättringar. Detta gör det möjligt för utvecklare att identifiera och lösa problem som kan påverka prestandan. Goolge DevTools ger även möjlighet att följa dem vanliga HTML och CSS fel innan koden kan implenteras. Detta är en utmärkt verktyg för nybörjare inom webbutveckling. 

![DevTools LightHouse](images/DevTools-LightHouse.png)
![DevTools Verktygsfunktion ](images/DevTools.png)

1. https://developer.chrome.com/docs/lighthouse/overview/
2. https://developer.chrome.com/docs/devtools/open/
3. https://nira.com/chrome-developer-tools/

## PG 1.3 Testdriven utveckling
Beskriv rubriken här

## PG 1.4 Deploy och staging
Beskriv rubriken här

## PG 1.5 Debugging

Debbugging (Felsökning) är en användbar felsökningsprocess inom programmeringsmiljö och systemutveckling. Utvecklare som skriver väldigt långa och omfattande koder brukar oftast stöta på syntaxfel och logiska fel, detta gör det svårt att diagnotisera. Debuggning kan ske genom att felsöka hela filen eller använda sig av brytpunkter. 

1. https://aws.amazon.com/what-is/debugging/
2. 

## PG 1.6 Dokumentation
v. 36

## PG 1.7 Struktur av kod i projekt
v. 4 

## PG 1.8 Automatisering av arbetsflöde
Beskriv rubriken här

## PG 1.9 Virtualisering av utvecklingsmiljö

Virtualisering av utvecklingsmiljö innebär att skapa och använda virtuella versioner av hårdvaruenheter och/eller operativsystem för att simulera en komplett utvecklingsmiljö. Detta ger flera fördelar för utvecklare och organisationer.

Virtuella miljöer är separerade från varandra, vilket innebär att eventuella ändringar eller problem i en virtuell miljö inte påverkar andra miljöer. Detta är särskilt användbart när man arbetar med flera projekt som kan ha olika beroenden eller krav.

Utvecklare kan skapa exakta kopior av en utvecklingsmiljö och distribuera dem över olika system. Detta underlättar samarbete, testning och ser till att varje utvecklare arbetar i en konsekvent miljö. Virtualisering gör det möjligt att snabbt konfigurera och anpassa utvecklingsmiljöer. Utvecklare kan enkelt växla mellan olika verktyg, bibliotek och versioner av programvara utan att påverka andra delar av systemet.

Genom att använda virtuella maskiner kan utvecklare undvika kostnaderna för att skaffa och underhålla fysisk hårdvara. Dessutom minimeras risken för konflikter mellan olika programvaror och tjänster. Virtualisering gör att programvaran enkelt och snabbt testas i olika miljöer och konfigurationer, vilket är viktigt för att säkerställa att applikationen fungerar korrekt i olika scenarier.

Det finns olika sätt att implementera virtualisering av utvecklingsmiljöer, inklusive användning av virtualiseringsprogram, containerteknik (som Docker) och molnbaserade utvecklingsmiljöer. Valet beror på specifika behov och krav för projektet och organisationen.

Docker-container
En körbar mjukvarupaket som innehåller allt som behövs för att köras, och som finns i en isolerad miljö (som ett eget operativsystem).

 * Kan byggas och köras oberoende av plattform
 * Isolerar mjukvaran från sin omgivning
 * Gör det enklare att testa på ett annat sätt
 * Om något går fel, påverkar det bara behållaren och inte ens eget operativsystem
 * Minskar konflikter som kan uppstå i teamet
 * Olika lokala inställningar står inte i konflikt med varandra

1. https://barrazacarlos.com/sv/fordelar-och-nackdelar-med-virtualisering/
2. https://www.dustin.se/solutions/kunskapsbanken/archive/docker-ett-trovaerdigt-alternativ-i-datahallen
3. https://docker-curriculum.com/
4. https://www.ibm.com/topics/docker


## PG 1.10 Bundeling-verktyg
Beskriv rubriken här

## PG 1.11 Terminalinterface

Terminalgränssnittet och Git Bash är verktyg för att interagera med datorns operativsystem genom kommandoraden. De möjliggör för användare att utföra kommandon och genomföra olika uppgifter utan att använda en grafisk användargränssnitt.

Ett terminalgränssnitt är en textbaserad miljö där användaren interagerar med datorn genom att skriva kommandon i en kommandorad eller terminal. I Unix-baserade system, såsom Linux och macOS, används ofta Terminal-appen. I Windows används kommandotolken (Command Prompt) eller PowerShell som exempel på terminalgränssnitt.

Git Bash är en terminalapplikation som ingår i Git-paketet. Den erbjuder en kommandoradsmiljö för användning med Git och andra Unix-verktyg direkt på Windows-systemet. Git Bash ger användare tillgång till Git-kommandon och Unix-liknande kommandon i en bekväm miljö på Windows-plattformen. Resultatet av kommandon och operationer visas vanligtvis som text direkt i terminalfönstret, vilket ger användaren tydlig feedback.

Terminalgränssnitt är vanligtvis beroende av operativsystemet. Till exempel används Terminal-appen i Linux eller macOS, medan Git Bash är specifikt utformad för Windows.Terminalgränssnitt kan vara allmänt och används för att utföra olika systemrelaterade uppgifter. Git Bash är mer specialiserad och fokuserar på Git-kommandon och verktyg.

Båda dessa verktyg är kraftfulla och ger avancerad kontroll och flexibilitet för användare som föredrar att använda kommandoraden för att hantera sina system och Git-repositorier.

![Git- Bash- terminal](<images/Git-Bash -.png>)

Grundläggande kommandon för Bash terminal: 

Navigera mellan mappar:

```bash 

cd <mappnamn>

```

Visa innehållet i en mapp:


```bash 
ls

```

Skapa en ny mapp:

```bash 
mkdir <mappnamn>

```

Ta bort en fil: 

```bash 

rm <filnamn>


```

1. https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line
2. https://www.redhat.com/sysadmin/shortcuts-command-line-navigation
3. https://gist.github.com/bradtraversy/cc180de0edee05075a6139e42d5f28ce