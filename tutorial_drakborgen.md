# Drakborgen
I denna utmaning ska vi göra ett häftigt spel! Dragborgen där du som spelare ska guida en katt genom drakens borg. Men akta dig så att inte draken tar dig!

## Spelplanen
Vi börjar med att skapa en bakgrund som vi döper till "Bana1"

![](bilder/tutorial_drakborgen/bana1.png)

Nu ska vi rita vår bana. Det är viktigt att vi använder den RÖDA pennan för att rita banans gränser. Gör inte första banan för svår.

![](bilder/tutorial_drakborgen/bana1_design.png)

## Sprajtsen
Nu ska vi skapa skapa våra sprajts.

![](bilder/tutorial_drakborgen/sprajtar1.png)

Viktigt! Döp dem till:
* Spelare
* Drake
* Mål

## Startvillkor
Vi måste se till att alla objekt startar på rätt ställe. Vi börjar med att placera ut spelaren. 

Sätt muspekaren där du vill ha spelaren och se vilken x/y-koordinat som är där.
![](bilder/tutorial_drakborgen/spelare0.png)

Gå till bakgrundens Skriptflik och tala om att när spelet startar så ska vi byta bakgrund till "Bana1". (Detta blir viktigt senare)

![](bilder/tutorial_drakborgen/bakgrund1.png)

Nu skapar vi två variabler, spelareX och spelareY, som talar om var spelaren (katten) ska börja på denna bana.

![](bilder/tutorial_drakborgen/nyvar.png)

Nu talar vi om att när bakgrunden växlar till "Bana1" så ska spelarens X och Y position sättas till de värden som jag tycker är lämpligt. I mitt fall 207/27.

Vi behöver nu tala om för omvärlden att vårt spel ska starta när vi placerat ut vår katt.

![](bilder/tutorial_drakborgen/bakgrund2.png)

![](bilder/tutorial_drakborgen/bakgrund3.png)

Nu kan vi gå in på vår spelare och tala om att den ska börja på dessa värden.

![](bilder/tutorial_drakborgen/spelare1.png)

Testa nu så att din spelare är på rätt ställe! Annars får du justera X- och Y-värdena på bakgrunden.

![](bilder/tutorial_drakborgen/spelare2.png)

Men vad stor den var. Vi minskar den:

![](bilder/tutorial_drakborgen/spelare3.png)

Nu vill vi få katten (musen?) att följa efter vår muspekare.

![](bilder/tutorial_drakborgen/spelare4.png)

Vi vill dock inte att spelaren ska följa efter muspekaren dirket när vi startar spelet så vi lägger till att man måste klicka på katten.

![](bilder/tutorial_drakborgen/spelare5.png)


