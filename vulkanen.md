Vulkanen
========

I utmaningen vulkanen får du lära dig att göra explosiva eldsprutande berg!

Du kan titta på [Elliots!](http://scratch.mit.edu/projects/44967008/) eller [min vulkan!](http://scratch.mit.edu/projects/44225694/) för att se hur det kan se ut.

Rita det eldsprutande berget
----------------------------

Börja med att rita en fint berg som bakgrund, du behöver inte rita någon rök, den kommer vi göra sedan

 * Klicka på [Scen, 1 bakgrund] 
![](bilder/scen.png)

 * Klicka sedan på bakgrund
![](bilder/bakgrund.png)

Nu kan du rita ditt bakgrundsberg, min ser ut så här:
![](bilder/vulkan_bakgrund.png)

Rita rök
--------

 * Nu kan du radera katten, högerklicka och välj radera.
 * Istället för en katt lägger vi till en ny sprite som du ritar själv. Rita ett litet moln av rök och aska
 * Flytta röken så att den är ovanför vulkanens öppning.
 
Få rök att välla ut ur vulkanen
------------------------------

 * Gå in på Script
 * Lägg ut en "när [grön flagga] klickas på 
 * Lägg ut en göm
 * klicka på den gröna flaggan, vad händer?
 
Nu vill vi att flera rökmoln ska skapas, vi vill ha något som kallas för "kloner"

 * Under "göm" sätt en "skapa klon av mig själv"

Om man klickar på gröna flaggan så händer inget, varför? Jo vi har gömt vår rök!

Nu ska vi visa röken och få den att röra sig

 * Sätt ut en "När jag startar som klon"
 * Under den sätt ut en "visa"
 * klicka på grön knapp nu och se vad som händer.
 
Rökmolnet som du ser nu är din klon!

![](bilder/en_klon.png)


Klon-röken ska röra på sig
-------------------------------------

 *  Under "visa" sätt en "för alltid"
 *  i för alltid sätt en "gå [10] steg"
 *  klicka på grön flagga, vad händer?
 *  Nu vill jag att du får den att åka uppåt istället, hur gör man det?
 *  Innan för alltid sätt en "peka i [0] riktning"

Har du lite otur nu så åker din sprite uppåt men startar från fel ställe!

 * Sätt ut en "gå till x: [] y:[]" där du anger x och y för vulkanens mynning. Du kan hålla musen över vulkanen och se i kanten vad x och y skall vara.
 
![](vulkanens_x_y.png)


 
 
