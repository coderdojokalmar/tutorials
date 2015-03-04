# Drakborgen
I denna utmaning ska vi göra ett häftigt spel! Dragborgen där du som spelare ska guida en katt genom drakens borg. Men akta dig så att inte draken tar dig!

Här hittar du en [version av spelet](http://scratch.mit.edu/projects/50419786/).

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

Vi vill dock inte att spelaren ska följa efter muspekaren direkt när vi startar spelet så vi lägger till att man måste klicka på katten.

![](bilder/tutorial_drakborgen/spelare5.png)

Nu ska vi se till att spelet tar slut om vi rör kanten. Men först gömmer vi vår drake och vårt mål så länge:

![](bilder/tutorial_drakborgen/gom.png)

Skicka meddelandet "gameover" om spelaren rör kanten

![](bilder/tutorial_drakborgen/spelare6.png)

Vi talar på bakgrunden om att hela spelet ska stannas om det blir Game over

![](bilder/tutorial_drakborgen/bakgrund4.png)

Och så skapar vi oss en ny sprajt som vi kan visa och tala om att spelet är slut.

![](bilder/tutorial_drakborgen/gameover.png)

### Målet
Nu sätter vi ut målet. Vi gör på samma sätt som med spelaren. Vi skapar en X- och en Y-variabel och sätter dess värden till där vi vill ha målet. 

![](bilder/tutorial_drakborgen/bakgrund5.png)

![](bilder/tutorial_drakborgen/mal1.png)

![](bilder/tutorial_drakborgen/overview1.png)

När vår spelare kommer till målet så ska vi skicka ett meddelande om att vi ska skapa en ny bana.

![](bilder/tutorial_drakborgen/spelare7.png)

Nu kan vi enkelt göra en ny bana.

Rita en ny bakgrund. Döp den till "Bana2". Gör den lite svårare och kanske åt andra hållet.

![](bilder/tutorial_drakborgen/bakgrund6.png)
![](bilder/tutorial_drakborgen/bakgrund7.png)

Nu måste vi se till att när man klarat en bana så ska nästa "laddas". 

![](bilder/tutorial_drakborgen/bakgrund8.png)

Men, nu ligger ju målet och katten kvar på samma ställe som förra gången. Vi måste flytta dem när en ny bana laddas. Vi behöver *kopiera* *startvillkoren* för vår spelare och vårt mål. På bakgrunden kopierar vi därför dessa.

![](bilder/common/kopiera.png)

![](bilder/tutorial_drakborgen/bakgrund9.png)

Sedan byter vi till "Bana2" och ändrar X- och Y-värdena till de som vi vill att vår objekt ska ha när banan startar.

![](bilder/tutorial_drakborgen/bakgrund10.png)

## Draken
Är det för lätt? Kanske kan du lägga till en drake som flyger omkring på banan och om den rör vår spelare så blir det Game Over. Klarar du det själv?

Försök gärna själv. Annars har du lösningen nedan:

![](bilder/tutorial_drakborgen/bakgrund11.png)
![](bilder/tutorial_drakborgen/drake1.png)

Observera att vi skapade två nya variabler, drakeX och drakeY för att tala om var draken skulle börja. Sedan har vi lite kod för att få draken att röra sig lite oregelbundet och studsa mot väggarna. Draken tål de varma väggarna!

##Utöka spelet
Nu kan du utöka spelet. Det finna massvis med grejor man kan göra

Lätt:
* Gör fler spännande banor. Kanske måste man springa igenom drakens stora rum.

Knepigt:
* Skapa en timer så att man ska försöka få så kort tid som möjligt på banorna
* Lägg till en skatt som draken vaktar som man måste hämta, eller så räknas tiden ner när man hittar skatten.
* Speciella hinder som rör sig i banan. Dörrar som öppnas och stängs?
