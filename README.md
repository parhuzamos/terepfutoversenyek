# Terepfutó versenyek itthon és külföldön

Hova menjek, hogy szép tájakat lássak és közben még versenyezhessek is?

Közösség által beküldött versenyek (és beszámolóik) listája.

## Érdemes címek

* https://bit.ly/terepfutoversenyek
* https://www.facebook.com/groups/221951301177041/permalink/1589000697805421/
* https://github.com/parhuzamos/terepfutoversenyek
* https://airtable.com/wsp3X36caxKBczgDV/ (privát)
* https://api.airtable.com/v0/appJCMaMRAC9BiZkt/versenyek?api_key=keyxGZ3Vo2s0bXFrn (api_key változhat! owner: john.doe455)

## Közösségi hozzáférés (a versenyek adataihoz, JSON formátumban)

Az Airtable lehetőséget ad API-n keresztüli adathozzáféréshez. Ennek a segítségével kikerülhető 
    a https://bit.ly/terepfutoversenyek felület 
    és bárki megjelenítheti az adatokat saját oldalán. Ha csak bizonyos versenyekre vagy kiváncsi és az oldaladon már szerepel
    egy verseny/versenynaptár adatbázis (vagy hasonló), akkor a neked is lesz saját oszlopod az adatbázisban, 
    amivel megjelölheted a számodra érdekes versenyeket. Az alábbi címen visszakapott adatokból egy valamirevaló webmester
    már szép és odaillő versenybejegyzéseket tud készíteni a honlapod számára.

Például: A terepfutas.hu sok versenyt rendez és egy csomó versennyel/versenyszervezővel van kapcsolatban. Vannak saját, 
    támogatott és ajánlott versenyeik. Számukra a `mindenki_terepfutas` nevű oszlop áll rendelkezésre. Ebben az oszlopban
    szereplő érték jelenti, hogy milyen kapcsolatban állnak a versennyel.
    
* 1 - ajánlott verseny 
    * https://api.airtable.com/v0/appJCMaMRAC9BiZkt/versenyek?api_key=keyxGZ3Vo2s0bXFrn&filterByFormula=IF(mindenki_terepfutas=1,%20TRUE(),%20FALSE())
* 2 - partner verseny 
    * https://api.airtable.com/v0/appJCMaMRAC9BiZkt/versenyek?api_key=keyxGZ3Vo2s0bXFrn&filterByFormula=IF(mindenki_terepfutas=2,%20TRUE(),%20FALSE())
* 3 - saját rendezésű verseny 
    * https://api.airtable.com/v0/appJCMaMRAC9BiZkt/versenyek?api_key=keyxGZ3Vo2s0bXFrn&filterByFormula=IF(mindenki_terepfutas=3,%20TRUE(),%20FALSE())

Jelenlegi extra oszlopok, amely lista bővíthető, csak kérni kell:

* mindenki_terepfutas
* mindenki_nyulcipo
* mindenki_futonaptar

## Statisztika

* https://bit.ly/terepfutoversenyek+
* https://analytics.google.com/analytics/web/#embed/report-home/a22333493w163062287p163988941/ (privát)

## Átirányítások

* https://bit.ly/terepfutoversenyek -> http://terepfutoversenyek.s3-website.eu-west-2.amazonaws.com/ -> https://parhuzamos.github.io/terepfutoversenyek/


## Teendők és kérdések:
* Feltüntetni, hogy az oldal nem a futonaptar.hu, terepfutas.hu (és társaik) "ellen/helyére/kiváltására" készült. A lényeg a közösségi szerkesztés lehetősége, mert egy-két embertől nem elvárható az "adatbázis" bővítése/karbantartása.
* Több, mint egy admin. Jelszó megosztás?
* Google Sheets? 
* Kártya szerű verseny megjelenítés?
* Több táv egy versenyen? Hogy lehetne felvinni és megjeleníteni?

    ### Csillagromboló
    
    * Track gpsies-be és onnan szintrajz (```//*[@id="chartImage"]```): https://www.gpsies.com/charts/sl/map/slggtidmqysaljxu_map.png?cacheId=1510313764110
    