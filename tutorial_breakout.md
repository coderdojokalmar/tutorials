# Breakout
I denna utmaning....


## Plattan
Vi börjar med att skapa plattan som bollen ska studsa på.

### Skapa och placera ut plattan
Ta bort katten! Den får inte vara med i detta projekt.

![](bilder/common/tabort_katt.png)

Skapa en ny sprite

![](bilder/common/ny_sprite.png)

Rita nu en fyrkant och fyll den med en färg.

![](bilder/tutorial_breakout/pad1.png)

Nu ligger palattan i mitten men vi vill ha den längst ner i mitten när spelet börjar. Gå därför in till "Skrip" på plattan och tala om var den ska ligga när spelet börjar:

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

![](bilder/tutorial_breakout/ball_skript1.png)

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
