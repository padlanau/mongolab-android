# How-to.

# MongoLabAndroid #

A simple library to connect to a mongolab db and save boilerplate code (httpget, httppost etc.)


# Usage #

In your android activity, include the following:

```
private final String DB = "db-name";
private final String API_KEY = "your-api-key";
private final String COLLECTION = "your-collection";
...
MongoLabDB db = new MongoLabDB(DB, API_KEY);

// All results are either JSONObject or JSONArray
Log.i("INFO", db.listDatabases().toString()); // prints databases
Log.i("INFO", db.listCollections().toString()); // prints collections

// get collection
MongoLabDB.MongoLabCollection coll = db.getCollection(COLLECTION);
Log.i("INFO", coll.getById("some-id-here").toString());


```