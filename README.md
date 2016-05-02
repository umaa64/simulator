# simulator

-> simulator is an ionic application based on angularjs html and jquery can run on browser and android mobiles.
we are able to add individual sensors name,devices,type,value and last modified date to the list. and able store in the database.
->Database: pouchdb,couchDB,couchbase to store data
-> It is using pouchdb plugin to connect to the database couchdb database.
we are configuring the pouchDB plugin in app.js file and we can  access the remote database from the app.js like this.


 if(ionic.Platform.isAndroid()) {
        $pouchDB.sync("http://52.67.20.14:5984/sensornew");
    } else {
        $pouchDB.sync("http://52.67.20.14:5984/sensornew");
    }
    

-> we are able to replicate data from couchdb to couchbase.
->  app.js page contains all the templates configured on it. ie.. list.html,login.html,items.htnkl

-> able to get data from database using  value from(key,value) from each attribute

 <ion-item class="item item-avatar" ng-repeat="(key, value) in items" ui-sref="item({documentId: key, documentRevision: value._rev})">
                {{value.sensorname}} {{value.sensorType}} <br> Last modified on  {{value.date}} </br>
                
