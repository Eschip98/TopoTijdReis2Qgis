# TopoTijdReis2Qgis
Qgis Plugin to import topotijdreis wms and wmts layers in to qgis

Deze pluging bestaat uit een sliderwidget waarmee je gemakelijk door de lagen van topotijdreis navigeerd en deze inlaad in QGIS. Een enkel jaartal kan simpel worden ingeladen door het jaartal door te geven via een textvak in de Qgis werkblak.
Met de 'vergelijk' functie word een tweede canvas aangemaakt waarop een tweede jaartal kan worden weergegeven. Alle overige projectlagen worden hierbij op zowel het tweede als het hoofdcanvas weergegeven.
- zowel de topografiesche kaarten als de luchtfoto's zijn beschikbaar

## Instalatie

Je hebt QGIS versie >3.30 nodig. Zoek in het pluging-menu (Plugins beheren en instaleren...) naar "TopoTijdReis2Qgis" en selecteer deze:

## Topokaart enkele jaar toevoegen
Om de topografische kaart van een enkle jaar in te laden type in het tekstbalk langs het plugingteken een jaartal en druk op enter. de topografische kaart van dat jaar in topotijdreis zal in het project worden geladen. de laag krijgt de naam "Topotijdreis 'jaartal'" 

## Wisselen tussen jaren met de slider
Druk op het pictogram van Topotijdreis om de enkele slider te starten. 
Er word nu automatisch het een lagengroep "Topotijdreis" met de meest recente topografische kaart op topotijdreis ingeladen in het project. Door met de slider een ander jaartal te selecten word de huidige laag verwijderd en word de kaart van het geselecteerden jaar ingeladen in het project. Het jaartal kan ook gewijzigd worden door een jaartal in de spinbox boven de slider te type, vergeet hier bij niet op enter te druken anders word de kaartlaag niet aangepast. 
Met het dropdown menu boven in de widget kan worden gewisseld tussen topografische kaarten en luchtfoto's. De range van jaartallen op de slider widget zal mee veranderen met de beschikbaren jaren in luchtfoto's of topografische kaarten.

## Twee kaarten vergelijken
Via de menubalk "Web" -> "TopoTijdReis2QGIS" -> "Vergelijken" start een widget met een tweede canvas en een widget met twee sliders. Er word een lagengroep "Topotijdreis" gemaakt met hierin weer twee groepen "Topotijdreis_hoofdcanvas" en "Topotijdreis_tweedecanvas".  De linker slider bestuurd de laag in "Topotijdreis_hoofdcanvas" de rechter slider in "Topotijdreis_tweedecanvas". Wijzige van kaartlagen en topo/luchtfoto werkt op dezelfde manier als bij de enkele slider. 
De extent/schaal van het tweede canvas is niet automatisch gelinkt aan het hoofd canvas. Dit moet nog handmatig ingesteld worden in het venster. Vink "Midden van weergaven synchroniseren met hoofdkaart" en "Schaalsynchroniseren" aan zodat bijde kaarten alstijd het zelfde gebied weergeven. 

Het renderen van lagen van het tweede canvas word aangestuurd door een kaartthema wat bij wijzigen van een van de twee sliders word ververst. Dit kaartthema is een clone van de lagensymbologie en render volgorden van het hoofdcanvas minus de topotijdreis laag van het hoofdcanvas. Waneer er een laag word toegevoegd aan het project en deze niet op het tweede canvas verschijnt kan het nodig zijn om even in de spinbox van het tweede canvas te gaan staan en op enter te druken. Hiermee word het maptheme namelijk ververst.
- LETOP: waneer je de volgorden in het lagen paneel aanpast dan alleen schuiven met heel de groep "Topotijdreis" en niet met de groepen of lagen in deze groep. Waneer deze volgorden in de groep verander werkt de het tweede canvas niet meer naar behoren


