---
# category: Stuff
# path: '/stuff'
title: 'Entstehungsgeschichte'
# type: 'GET'

# layout: nil
---

<img src="/../img/cylairLogo.png" alt="Cyclair-Logo" style="max-width: 200px" />

Die [Cyclair Webapp](https://cyclair.herokuapp.com) entstand im Rahmen der Lehrveranstaltung Methoden und Werkzeuge in BUI Projekten an der HTW Berlin im Sommersemester 2018/19. Ziel war die Erstellung eines Fahrradroutenplaners der nicht nur die schnellste Verbindung ausgibt, sondern auch die Luftqualität berücksichtigt und abhängig davon eine 

Zum gegenwärtigen Zeitpunkt berücksichtigt die App ausschließlich die Feinstaubbelastung der Luft, keine Stickoxide o.ä. Entwickelt wurde die App für den Raum Berlin, [architekturbedingt](#Architektur) funktioniert sie prinzipiell auch außerhalb.

Die Daten zur Luftqualität sind leider noch etwas lückenhaft, in [Schnittstellen](#Schnittstellen) ist beschrieben, woher diese Daten kommen.

## How to build

If you would like to run the app on your own computer you need to have [Node.js and NPM](https://nodejs.org/en/) installed.

After cloning the repository run `npm install` from your console. Then navigate into the *client folder* `cd client` and run `npm install` again.

In the root *root folder* you need to add a file called *config.json* which contains the API keys. The *config.json* should look like this:
```
{
    “GRAPHHOPPER_KEY”: “XXXXXXXXXXXXXXXXXXXX”,
    “API_KEY_GOOGLE”: “XXXXXXXXXXXXXXXXXXXX”
}
```

In your *root folder* (`cd ..`) run the app with 
`npm run dev`. You can access the website at <http://127.0.0.1:3000/>.
