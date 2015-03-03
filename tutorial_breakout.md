# Breakout
I denna utmaning ska du få bygga ett spel! Spelet heter Breakout och är en riktig tv-spelsklassiker. Du kan se hur spelet kan komma att se ut när du är klar: [Testa Breakout](http://scratch.mit.edu/projects/45924598/)

Testa spelet och fundera lite över vilka delar som finns:
* Vad ska spelaren kunna kontrollera?
* Vad ska finnas från början, innan spelet startar?

_Fuska? Du kan titta på [färdiga lösningen](#user-content-färdiga-lösningen) direkt._

## Plattan
Vi börjar med att skapa plattan som bollen ska studsa på.

### Skapa och placera ut plattan
Ta bort katten! Den får inte vara med i detta projekt.

![](bilder/common/tabort_katt.png)

Skapa en ny sprite

![](bilder/common/ny_sprite.png)

Rita nu en fyrkant och fyll den med en färg.

![](bilder/tutorial_breakout/pad1.png)

Du kan nu namnge plattan så att den inte heter "Sprite2". Högerklicka och välj "Info". Där kan du sedan ändra namn.

Nu ligger plattan i mitten men vi vill ha den längst ner i mitten när spelet börjar. Gå därför in till "Skript" på plattan och tala om var den ska ligga när spelet börjar:

![](bilder/tutorial_breakout/pad_skript1.png)

Testa genom att klicka på den gröna flaggan

### Få plattan att röra sig
Vi vil nu att plattan rör sig när du rör musen. Vi gör det genom

![](bilder/tutorial_breakout/pad_skript2.png)

Men vad nu då? Den stannar ju inte kvar där nere? Vi måste tala om att den inte får lämna sitt y-värde.

![](bilder/tutorial_breakout/pad_skript3.png)

Testa!

## Bollen
Nu ska vi skapa en boll och placera ut den.

### Skapa bollen
Många vanliga saker finns det redan andra som har gjort så nu ska vi låna en färdig boll.

![](bilder/common/ny_sprite_bibliotek.png)

Eftersom vi letar efter en boll så väljer vi "Sport"

![](bilder/common/sport.png)

Välj en boll som du tycker passar

### Placera ut bollen och få den att studsa
På samma sätt som med plattan så behöver bollen ha en fast startposition.

![](bilder/tutorial_breakout/ball_skript1.png)

Nu vill vi att bollen börjar röra sig. 

![](bilder/tutorial_breakout/ball_skript2.png)

Testa hela tiden!

Bollen studsar fram och tillbaka på en rak linje. Vi kan få den att studsa lite roligare genom att tala om att den från början ska ge sig av lite snett. 

![](bilder/tutorial_breakout/ball_skript3.png)

Nu händer det ingenting när bollen rör vår platta. Detta måste vi fixa. Vi talar om att bollen ska studsa när den träffar plattan. Detta block är lite knepigt och består av många olika delar:

![](bilder/tutorial_breakout/ball_skript4.png)

*Om* bollen rör *plattan* då ska vi peka om bollen i en annan riktning. Riktningen måste vi räkna ut för att det ska fungera oavsett om bollen kommer från höger eller vänster.

Dra sedan in blocket i din *för alltid*-loop. 

![](bilder/tutorial_breakout/ball_skript5.png)

![](bilder/tutorial_breakout/overview1.png)

### Få bollen att brinna upp
Om vi missar bollen nu så gör det inte så mycket eftersom den bara studsar mot botten. Istället vill vi att bollen brinner upp och spelet tar slut när detta händer!

Börja med att rita lite lava i din bakgrund:

![](bilder/tutorial_breakout/lava1.png)

Det är viktigt att lavan inte sticker upp ovanför vår platta!

Nu behöver tala om för bollen att den ska göra någon när den träffar lavan. Eftersom vi har målat lavan med en och samma färg så kan vi använda kontrollblocket *om bollen rör färgen*

![](bilder/tutorial_breakout/ball_skript7.png)

För att välja färg klickar du i färgrutan och klickar sedan på lavan.

När bollen rör lavan ska vi utnyttja något som heter "Meddelanden" för tala om för andra delar i spelet att "nu är spelet slut". Vi lägger därför till händelsen *skicka* och skriver ett eget meddelande: "gameover"

![](bilder/tutorial_breakout/ball_skript6.png)

Vi lägger sedan till *om*-blocket i vår loop. Vi lägger också till kontrollblocket *stoppa skript* så att bollen inte fortsätter studsa när vi förlorat.

![](bilder/tutorial_breakout/ball_skript8.png)

Skapa nu en ny "klädsel" till bollen och rita hur du vill att den ska se ut när spelet är slut.

![](bilder/tutorial_breakout/ball_skript9.png)

Nu ska vi se till att byta klädsel på bollen. Vi skulle kunna göra detta innuti blocket när vi rör lavan, men för att undvika att vårt block blir jättestort och svårt att läsa så delar vi upp detta i en separat del. Kom du ihåg att vi skickar meddelandet "gameover"? Vi kan nu lyssna efter detta meddelande och byta klädsel när det inträffar.

![](bilder/tutorial_breakout/ball_gameover1.png)

Nu märker vi att vi har några *buggar* i kod. När bollen träffar lavan så lutar den så vår eld hamnar snett. När vi startar om spelet så har bollen fortfarande på sig den brinnande klädseln. Vi får buggfixa fixa genom att:

* Se till att bollen inte roterar när den studsar.
* Se till att rätt klädsel väljs när vi startar spelet.

![](bilder/tutorial_breakout/ball_buggfix1.png)

Bra jobbat! Nu har vi kommit ganska långt!

## Skapa block
Vi börjar med att skapa ett block. Jag har valt den färdiga "Button2" som du hittar i sprajt-bibloteket.

![](bilder/tutorial_breakout/block_create1.png)

Vi börjar med att lägga ut det första blocket längst upp till vänster:

![](bilder/tutorial_breakout/block_create2.png)

Vi skapar nu en klon av denna och flyttar sedan vårt block en bit till höger. 

![](bilder/tutorial_breakout/block_create3.png)

Vi skulle nu kunna upprepa detta flera gånger för att skapa fler block, men gör inte det!

![](bilder/tutorial_breakout/block_create4.png)

Om vi har många block så blir det väldigt mycket kod och det är dessutom jobbigt att ändra något eftersom vi får ändra på många ställen. Istället använder vi kontrollblock som repeterar flerar gånger. 7 block fick jag plats med på en rad.

![](bilder/tutorial_breakout/block_create5.png)

![](bilder/tutorial_breakout/block_create6.png)

Nu vill vi göra en ny rad så vi flyttar tillbaka _x_ till _-200_ och minskar _y_ med _35_. Sedan gör vi detta en gång för varje rad som vi vill ha. Men vi märker nu att vi får samma problem som innan. Samma kod flera gånger eftervarandra vilket blir väldigt mycket!

![](bilder/tutorial_breakout/block_create7.png)

Vi väljer därför att skapa en ny repeterare som repeterar vår kod för varje rad. Fyra rader var lagom för mig.

![](bilder/tutorial_breakout/block_create8.png)

Som du kanske ser så har vi en liten bugg. Knappen som vi skapar kloner av syns den också. Vi fixar det på samma sätt som i vulkanen genom att först gömma brickan och sedan för varje klon, visa igen

![](bilder/tutorial_breakout/block_create9.png)


## Få bollen att studsa mot brickorna och förstöra dem
Kan du själv klura ut hur du ska göra för att få bollen att:
1. Studsa mot blocken
2. Få brickorna att försvinna när bollen studsat mot dem?

Testa själv, du hittar sedan en lösning nedan.

### Studsa mot brickorna
Gå in till skriptet för bollen och titta på hur vi fick den att studsa mot plattan. Kan vi göra på motsvarande sätt för brickorna?

![](bilder/tutorial_breakout/ball_skript10.png)

### Få brickorna att försvinna
I skriptet för brickorna:

![](bilder/tutorial_breakout/block_create10.png)

## Buggfix
Även om vi har en fullt spelbar version nu så finns det några saker att jobba vidare på. Vi ser att det tar ett tag att rita upp alla brickor och kanske ska inte bollen starta förrän vi är klara med det. 

Fundera om det finns ett sätt att tala om för bollen att börja röra sig när alla brickor är utritade? 

Tips: Kan vi kanske skicka ett meddelande från brickorna till bollen på något sätt?

## Färdiga lösningen

Här nedanför ser du nu den färdiga lösningen:

![](bilder/tutorial_breakout/block_final.png)

![](bilder/tutorial_breakout/ball_final.png)

![](bilder/tutorial_breakout/pad_final.png)


## Fortsätta arbeta med spelet
Du har nu gjort ett kul grundspel, men det finns så mycket mer roliga saker vi kan bygga ut vårt spel med:

Några förslag:
* När brickor träffas så skulle vi kunna se till att det ibland trillar ner lite bonusar i form av elaka saker som gör att vår platta blir mindre, eller bra saker som gör den större.
* Kanske skulle vi ha lite meddelanden till vår spelara där det står "Game Over" när spelet är slut?
* På något sätt ta reda på när alla brickor är borta och då skriva att man vann?
* Kanske skulle man kunna göra en ny bana när denna är färdig?
* Vi borde kanske ha tre liv och inte bara ett?
* Bollen studsar lite tråkigt just nu. Kan vi lägga till en viss slumpfaktor så att bollen inte studsar "perfekt" varje gång?
* Lägg tillljudeffekter när bollen studsar på plattan, träffar en bricka och brinner upp i lavan. 

För inspiration kan du söka på "Breakout" på scratch eller titta på [vår version](http://scratch.mit.edu/projects/45924598/).

