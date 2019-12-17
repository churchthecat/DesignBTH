Laddningstid
=======================

En kortfattad analys av tre hemsidors laddningstid för både för desktop och mobil.


Urval
-----------------------

Jag har valt att utgå från tre skilda typer av hemsidor:

1) En intensiv reklambaserad nyhetssajt - aftonbladet.se med antagandet att det inte är en bland de snabbare hemsidorna. Detta då det är många bilder som ska laddas, reklamvideos och annonser. Det som också gör Aftonbladet intressant ur perspektivet att den hypotetisk tar en längre tid att ladda är också att de vill ha många läsare. Det blir en därmed en balans mellan faktumen att man vill ha många läsare men även många annonsörer. Det är enligt (Cloudflare) mindre troligt att personer är benägna att vänta på att hemsidor laddar utan vid en sådan upplevelse skulle välja en annan nyhetssida som ger respons snabbare.

2) Andra valet föll på min egen blogg twocatsinacaravan.xyz som är rätt så bildintensiv och ligger på en budgetvariant av webbhotell. Självklart finns det en önskan från min sida att bloggen läses av många, men den riktar sig snarare till familj och vänner som är nyfikna till skillnad. Det gör att den skiljer sig från en kommersiell webbsida som är beroende av att personer väljer stanna kvar på sidan.

3) Ytterligare en som enligt min hypotes bör ligga rätt bra till i laddningstid, who.is en sida för att kolla Ipadresser, domäner och tillhörigheter bland annat. De som väljer den hemsidan gör det av ett specifikt skäl och med en viss avsikt. Det kan vara för att få reda på om ett visst domännamn är tillgängligt men även för att veta vem som ligger bakom en viss hemsida. Det handlar därmed inte om att snabbt uppdatera sig om vad som hänt i nyhetsvärlden eller titta på bilder.


Metod och möjliga felkällor
-----------------------
Metoden blir en komparativ analys av tre hemsidor då det handlar om jämförande snarare än en djupare kvalitativ studie av hemsidornas innehåll. För att kunna få en rättvis jämförelse har jag stängt av allt som jag vanligtvis använder för att snabba upp sidor. När jag själv besöker webbsidor blockerar jag även det mesta av spårare och reklam. För detta använder jag själv Hostblock och adblocker (ublock) vilket ger en snabbare laddning av webbsidor bland annat. Själva mätningarna har jag gjort i Firefox dev via network i devtools samt med Google page speed. Trots att jag stängde ner det mesta av optimeringarna på min dator så är det en hel del kvar som påverkar, både i min setup och nätuppkoppling.

Den första anledningen är min dator vid jämförelse av en ny helt enkelt är en dinosaur. Det är en gammal HP Elitebook med som snart är 10 år. Jag har satt in en ny SSD, 2 gig ram extra och jag har gjort en mängd optimeringar i mjukvaran vilket gör att den fungerar bra trots sin ålder. Det jag har gjort är även att jag har krypterad DNS, VPN alltid aktiverat, jag använde blockerare i browser och brandvägg. När det kommer till själva internetuppkopplingen så sitter jag på 4G uppkoppling via vanliga Vodafone. Det som kan ibland dra ned hastigheten och göra uppkopplingen är det faktum att jag bor i bergen i Asturien, norra Spanien.
Sammantaget så är det svårt att reproducera resultaten för någon annan men avvikelserna mellan de olika sidorna bör vara mera korrekt. Google speed poängen bör inte heller påverkas av min setup.


#### Aftonbladet - [https://www.aftonbladet.se](https://www.aftonbladet.se)

[Google pagespeed](https://developers.google.com/speed/pagespeed/insights/?url=www.aftonbladet.se)

![Aftonbladet](../htdocs/img/aftonbladet.png "Aftonbladet")

Mitt antagande var som väntat. Aftonbladet ligger sist i mätningarna med bred marginal, med page speed poäng för desktop på 32 respektive 28 på mobilen. Jag antar att Aftonbladet klarar sig bra utifrån att Sverige har en bra digital infrastruktur snarare än själva innehållet. Det var en stor skillnad att besöka sidan med alla blockerare avstängda. Google gav som förslag att optimera koden och ta bort resurser som hindrar rendering. Det går att anta att Aftonbladet lägger mer fokus på annonsalgoritmer än fokus på journalistik. Det kan dock vara något av en subjektiv åsikt. Det finns en del åtgärder som kan göras men med tanke på Aftonbladets digitala resurser verkar de nöjda med hur hemsidan interagerar med besökare.




#### Two cats in a caravan - [https://twocatsinacaravan.xyz](https://twocatsinacaravan.xyz)
[Google pagespeed](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Ftwocatsinacaravan.xyz%2F)

![Two cats in a caravan](../htdocs/img/twocatsinacaravan.png "Two cats in a caravan")

Bloggen Two Cats in a Caravan valde min fru och jag att göra i Wordpress. Den hamnade på andra plats i mätningen med page speedpoäng för desktop på 76 och 51 på mobilen. Eftersom den mesta koden på sidan är tredjepartskod det vill säga genom diverse plugins så var det också där Google rekommenderade förbättringar. Bland annat så tog mailchimp en hel del resurser. Efter att ha gjort mätningen och sett resultaten så överväger jag att ta bort tillägget då det inte kan räknas som bärande för hemsidan.
Jag ser också fördelen med att använda dessa mätningar om jag i framtiden kommer att välja en mer kommersiell hemsida för att använda till det egna företaget.

#### Who.is - [https://www.who.is](https://www.who.is)
[Google pagespeed](https://developers.google.com/speed/pagespeed/insights/?url=who.is)


![Who is](../htdocs/img/whois.png "Who is")
På första plats hamnar Who is  vilket var mitt förväntade resultat. Who is är en resultatorienterad sida som inte har bilder eller många annonser. Besökare vill hitta resultat snabbt och inte surfa runt bland artiklar eller titta på bilder och video därmed har hemsidan inte heller många val.  
Med en page speed poäng för desktop på 97 respektive 85 på mobilen så går det snabbt, 2,6 sekunder jämfört med aftonbladets 39,7 sekunder i network stats.
Det är mycket lite som laddas in och who.is håller sig under en megabyte i transfered data,  med god marginal.
Förbättringsförslag som Google tog upp var att ta bort onödig CSS och att slå på textkomprimering.


Övrigt
------------------
En gemensam nämnare var att onödig CSS kod var en förbättring som återkom till samtliga hemsidor. Det var även förväntat att servern min egen blogg på är seg men den är billig så det får jag stå ut med.
Det finns många faktorer som korrelerar när det kommer till att sätta en gräns för vad som är en snabbt respektive vad som är en långsam hemsida. Det blir en skev komparation när man jämför bildintesiva hemsidor med resultatorienterade hemsidor. Det vill säga att jämföra Aftonblade med Who is. Det går dock att utan djupare analys konstatera att Aftonbladets hemsida är långsam i förhållande till Who is.

 Jag vill sätta gränsen så min blogg kommer över vad som är upplevt långsam. 47% ska enligt Cloudflare vara av åsikten att laddningstiden ska vara max två sekunder dock.



Referenser
-------------------

1.  [Mätningar](https://docs.google.com/spreadsheets/d/1_6rT-kF5Gqhd0t_V3oK6qQ4_90kTcLv4cwVeKAeKVx0/edit?usp=sharing)

2. [https://www.who.is](https://www.who.is)

3. [https://twocatsinacaravan.xyz](https://twocatsinacaravan.xyz)

4. [https://www.aftonbladet.se](https://www.aftonbladet.se)

5. [Cloudflare](https://www.cloudflare.com/learning/performance/more/website-performance-conversion-rates/)


Anders Johansson 2019-12-13
