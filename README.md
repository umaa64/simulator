# simulator

-> simulator is an ionic application based on angularjs html and jquery can run on browser and android mobiles.
we are able to add simulator name,devices,type,value and last modified date to the list. and able store in the database.
->Database: pouchdb,couchDB,couchbase to store data
-> It is using pouchdb plugin to connect to the database couchdb database.
we are configuring the pouchDB plugin in app.js file and we can  access the remote database from the app.js 


 if(ionic.Platform.isAndroid()) {
        $pouchDB.sync("http://52.67.20.14:5984/sensornew");
    } else {
        $pouchDB.sync("http://52.67.20.14:5984/sensornew");
    }
    

