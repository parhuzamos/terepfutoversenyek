# Terepfutó versenyek itthon és külföldön

Hova menjek, hogy szép tájakat lássak és közben még versenyezhessek is?

Közösség által beküldött versenyek (és beszámolóik) listája.

## Érdemes címek

* https://bit.ly/terepfutoversenyek
* https://www.facebook.com/groups/221951301177041/permalink/1589000697805421/
* https://github.com/parhuzamos/terepfutoversenyek
* https://airtable.com/wsp3X36caxKBczgDV/ (privát)
* https://api.airtable.com/v0/appJCMaMRAC9BiZkt/versenyek?api_key=keyxGZ3Vo2s0bXFrn (api_key változhat! owner: john.doe455)
* http://www.futonaptar.info/cimke/trail
* http://futonaptar.hu/
* http://www.teljesitmenyturazoktarsasaga.hu/naptar
* https://www.fiverr.com/search/gigs?utf8=✓&source=guest-homepage&locale=en&search_in=everywhere&query=draw+an+icon&ref=delivery_time%3A3%7Cseller_language%3Aen%7Cgig_price_range%3A0%7Cdelivery_time%3A3%7Cseller_language%3Aen%7Cgig_price_range%3A0%2C5%7Corigin%3Aheader&filter=auto
* https://www.fiverr.com/navipainter/an-awesome-fanart-in-my-style?context&context_referrer=search_gigs&context_type=auto&filtered_duration=3&filtered_price=0.0%2C5.0&pckg_id=1&pos=23&ref_ctx_id=7e8f0dd4-8b6c-41d7-9691-3d253c948450&funnel=b2b67fbf-ce39-4ac2-a289-9291d8ee5923
* https://getbootstrap.com/docs/4.0/content/reboot/
* http://getbootstrap.com/docs/4.0/examples/narrow-jumbotron/

## Közösségi hozzáférés (a versenyek adataihoz, JSON formátumban)

Az Airtable lehetőséget ad API-n keresztüli adathozzáféréshez. Ennek a segítségével kikerülhető 
    a https://bit.ly/terepfutoversenyek felület 
    és bárki megjelenítheti az adatokat saját oldalán. Ha csak bizonyos versenyekre vagy kiváncsi és az oldaladon már szerepel
    egy verseny/versenynaptár adatbázis (vagy hasonló), akkor a neked is lesz saját oszlopod az adatbázisban, 
    amivel megjelölheted a számodra érdekes versenyeket. Az alábbi címen visszakapott adatokból egy valamirevaló webmester
    már szép és odaillő versenybejegyzéseket tud készíteni a honlapod számára.

Például: A terepfutas.hu sok versenyt rendez és egy csomó versennyel/versenyszervezővel van kapcsolatban. Vannak saját, 
    támogatott és ajánlott versenyeik. Számukra a `mindenki_terepfutas` nevű oszlop áll rendelkezésre. Ebben az oszlopban
    szereplő érték jelenti, hogy milyen kapcsolatban állnak a versennyel. (Ez csak egy példa, nem muszáj így használni ;).)
    
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
* mindenki_wadkanz

## Statisztika

* https://bit.ly/terepfutoversenyek+
* https://analytics.google.com/analytics/web/#embed/report-home/a22333493w163062287p163988941/ (privát)
* https://developers.facebook.com/apps/1284990944938281/dashboard/ (privát)

## Átirányítások

* https://bit.ly/terepfutoversenyek -> http://terepfutoversenyek.s3-website.eu-west-2.amazonaws.com/ -> https://parhuzamos.github.io/terepfutoversenyek/


## Teendők és kérdések:
* Google Calendar link a menüben Firefox-ból nem használható
* Valamiféle értesítő az új bejegyzésekről
    * Böngésző notification?
    * Pushbullet channel? https://www.pushbullet.com/channel?tag=terepfutoversenyek
* Gallery view
* Kártya szerű verseny megjelenítés?
    * Like gombbal és/vagy facebook-os fórummal?
    * Színes kártya, amelyre már lehet előregisztrálni
    * Színes kártya, ami hamarosan lesz
    * Színes kártya, ami már elmúlt
* Cookie-ban tároljuk az utolsó látogatás időpontját, vagy automatikusan vagy egy gomb megnyomásával állíthatja a user: "Eddig a percig láttam mindent"
    * Legközelebb szűrhessen, hogy csak az újonnan beengedett (approved) versenyeket listázzuk
    * Ehhez készült az "approval date" oszlop, amelyet arra az időpontra kell állítani, mint az "approval" oszlop bekapcsolása
* Feltüntetni, hogy az oldal nem a futonaptar.hu, terepfutas.hu (és társaik) "ellen/helyére/kiváltására" készült. A lényeg a közösségi szerkesztés lehetősége, mert egy-két embertől nem elvárható az "adatbázis" bővítése/karbantartása.
* ~~Több, mint egy admin. Jelszó megosztás?~~ Lehet meghívni több szerkesztőt is az ingyenes verzióban.
* ~~Google Sheets?~~ Úgy néz ki, hogy nem lesz rá szükség, elég sokmindent meg lehet csinálni az Airtable-ban is. 
* ~~Több táv egy versenyen? Hogy lehetne felvinni és megjeleníteni?~~ Csak jelöljük a megfelelő oszlopban és a leírásban.
* facebook login `user_events` jogosultsággal -> kell login review-ra küldeni az app-ot
* facebook login után a felhasználó versenyei alapján színezzük a dobozokat, az `attending` mező alapján. 
    a facebook event az url-ben levő azonosítóval lőhető be
    



### Csillagromboló
    
* Track gpsies-be és onnan szintrajz (```//*[@id="chartImage"]```): https://www.gpsies.com/charts/sl/map/slggtidmqysaljxu_map.png?cacheId=1510313764110
    