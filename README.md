# Widget Writing env boilerplate

### Build the project

First run
```
npm install
```

To set up the dev env run
```
grunt build
```

This will setup the stage server and will copy your widgets to the widget library of the server.

then starting the server by running:

```
npm start
```

For development purposes setup the server as described above
also run both grunt tasks in different command windows:

```
grunt widgets
```

This will compile the widgets (from widget src folder) and create widget.js from it.


```
grunt widgetsCopy
```

This will start a listener on the widgets library and will copy any changes you make on the fly to the server
You will have to click refresh on the browser for it to take effect.


** Note: im trying to combine those but it took too much effort so i left it like this.


In order to deploy this to prod environment,  need to run the first 2 steps (copy stage server files and run 'grunt build').
then copy the dist lib (zip it and unzip in server)

Start the server by running
```
cd backend
node server.js
```

** Note i will create a task to zip this if needed


### other grunt tasks
If you add another widget library and want it to take effect (copy to dist) either run "grunt build", or simply run - "grunt registerWidget"
