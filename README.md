Fabians Geotweeter
==================

Fabians Geotweeter ist mein kleiner, fast komplett in Javascript geschriebener, "privater" Twitter-Client.

Geschichte
----------

Es fing damit an, dass ich einfach einen Twitter-Client haben wollte, der Tweets mit beliebigen, von mir
festgelegten Geotags absenden konnte. Genau das konnte der Geotweeter damals halt (und daher kommt halt auch
der Name).

Dann fand ich es ganz praktisch, auch Tweets anzuzeigen, damit man komfortabler auf Tweets antworten konnte.

Dann wurde die Anzeige aufgehübscht. Twitter führte User-Streams ein... Und so führte eins zum anderen und
der Geotweeter wurde mein privater, selbstgeschriebener und an meine Wünsche und Anforderungen angepasster
Twitter-Client.

Installation
------------

Der Geotweeter war nie dafür gedacht, von jemand anderem als mir genutzt zu werden. Dementsprechend
"komfortabel" lässt er sich an andere User anpassen.

### Ein grober Überblick
In der `.htaccess` werden ein paar Proxys definiert, um die Same-Origin-Policy
zu umgehen. Dafür sollte der Geotweeter auf einem Apache-Server laufen, der entsprechend mod_proxy und
so zur Verfügung hat.

In der `settings.js` werden Twitter-OAuth-Tokens und -Secrets hinterlegt.

`setmaxreadid.php` und `getmaxreadid.php` sind minimale PHP-Skripte, über die eine Echofon-mäßige Sync-
Funktionalität realisiert wird. Diese müssen Schreibzugriff auf eine Datei `maxreadid.dat` im gleichen
Ordner haben.

Und im Haupt-Code in `geotweeter.js` dürfte noch an einigen Stellen mein Twitter-Username fest kodiert
sein. Einfach mal nach "fabianonline" suchen und evtl. ersetzen. Oder gleich forken, ordentlich
konfigurierbar machen (oder gar direkt via verify_credentials abfragen) und nen Pull-Request absetzen.

