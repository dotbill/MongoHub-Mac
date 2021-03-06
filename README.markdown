## What is MongoHub
**[MongoHub](http://mongohub.todayclose.com/)** is a **[mongodb](http://mongodb.org)** GUI application.
This repository is a fork of [MongoHub](https://github.com/bububa/MongoHub-Mac).

## System Requirements

Mac OS X(10.6.x or 10.7.x), intel(64bit/32bit) based.

## Installation

You can either download the compiled executable file from [here](https://github.com/downloads/fotonauts/MongoHub-Mac/MongoHub.zip) 
or clone the source code and compile it on your own system.

## Build

Just build it, it should work (but let me know if you have an errors or warnings).

## Current Status

This project is very new. Any issues or bug reports are welcome. And I still don't have time to write a **usage guide**.

** Known bugs **
    
    - Don't trust the grey default value in textfields
    - Most of errors are not handled correctly
    - Simple quote is not supported yet for json

** To do list **
    
    - Should manage a list of database/user/password for each connections
    - Should save the password into the keychain
    - Create a document editor to edit using an outline view (like the plist editor in Xcode)
    - Need a better UI to replace the tabs in a collection window
    
** Current **

    - Problem to parse binary values
    - Problem to parse an hash with $type

## History

** 2.4.16(90) - jan 29, 2012 **

    - Adding autosave for the connection list window
    - Adding back the index icon
    - Better error message when not having the authorization to get the server status
    - Crash fixed when not having the authorization to get the server status

** 2.4.15(89) - dec 30, 2011 **

    - Crash fixed when remove all documents : https://github.com/fotonauts/MongoHub-Mac/issues/18
    - Change minimum size of MainMenu window to avoid display bug (thanks ohardy)
    - Bug fixes (thanks ohardy)
    - Double click on database name collapse or expand item (thanks ohardy)

** 2.4.14(88) - dec 23, 2011 **

    - Adding full-screen support (lion only), thanks callumj
    - Fix when you don't have the right to get the database list (you need to set the database you want to use in the connection panel)

** 2.4.13(87) - nov 30, 2011 **

	- Key order is preserved in a document
    - Support for UTF-8
    - Fix for Mysql import/export
    - Support for symbol type
    - fix for the UI selection in the connexion window

** 2.4.12(86) - nov 22, 2011 **

    - Problem to update document with boolean values and regexp values

** 2.4.11(85) - nov 22, 2011 **

    - Toolbar items are enabled/disabled according to the selection
    - Connecting to localhost is not an issue anymore
    - Bug to parse json with arrays

** 2.4.10(84) - nov 19, 2011 **

    - Bug to add a new connection

** 2.4.9(83) - nov 18, 2011 **

    - Changing the NSBundle application id
    - Database stats works again
    - History combo-box for the criteria
    - Fix to use database with an admin user/password

** 2.4.8(82) - nov 1, 2011 **

    - Problem to display and parse date types
    
** 2.4.7(81) - nov 1, 2011 **
    
    - Connections are sorted after being loaded (still not sorted after being updated)
    - Adding short cuts to delete a document or an index (Command+delete)
    - Adding tooltips for the buttons with short cuts
    - Queries are sorted by default
    - Problem to display regex and timestamp values in documents

** 2.4.6(80) - oct 28, 2011 **
    
    - Can insert an array of documents
    - MapReduce feature working
    - Fix for parsing: "$oid":"4E9321AF3768CF514A00000C"}
    - Crash when getting stats for some servers
    - New outline view for the databases and collections

** 2.4.5(79) - oct 22, 2011 **

    - Fix to parse { "empty_array": [], "zob": 1}
    - Fix to parse { "empty_hash": {}, "zob": 1}
    - Implementing reIndex

** 2.4.4(78) - oct 20, 2011 **

    - Can create indexes with the UI
    - Can remove indexes with the UI
    - Fix to parse { "_id": { "$oid" : "4E9807F88157F608B4000002" }, "_type": "Activity" }
    - Fix to edit a document when "_id" is an objectid

** 2.4.3(77) - oct 17, 2011 **

    - Fix to parse { "toto" : [ { "1" : 2 }, { "2" : 3 } ] }
    - Display errors (if any) when inserting a document
    - Display errors (if any) when removing a document
    - Fix to remove a document
    - Search for updates at each launch

** 2.4.2(76) - oct 15, 2011 **

    - Crash fixed when using an authenticated database
    - Show all the databases when using authentication
    - Use "admin" database when there is no database set for the authentication
    - Crash fixed when searching for mongo document with "{ "$oid" : "4E40C5111F85DD1BE9FAF825" }"
    - Adding the error message when the search criteria is invalid
    - Trying to be nice to complete your criteria. To search for an id, you can either type: 
            * 123
            * "abc"
            * "$oid" : "123"
            * {"$oid" : "123"}
    - Adding Command-R in the index view to reload the index list


** [Update 2.4.1(75)] **
    
    - Can do export and import (mysql)

** [Update 2.3.2] **
	
	- Fixed a bug in jsoneditor related to Date() object;
	- Add import/export to JSON/CSV functions;
	- Add support for ssh access use public key;
	- Add a function to remove single record in find query window;
	- Fixed a bug to create collection in a database which doesn't have collection;
	
** [Update 2.3.1] **
	
	- Fixed a bug in jsoneditor related to Date() object;
	- Add execution time in find panel;
	- Add reconnect support;
	- Fixed a bug in remove function.

** [2.3.0] **
	
	- Add mongo stat monitor;
	- Add replica set connection support;
	- Add reconnect support;
	- Add an JSON editor for found results with syntax highlight;
	- More flexible query style in find window;
	- Fixed long long int value overflow;
	- Fixed application crash during open/close connection window.

** [2.2.0] **
	
	- SSH Tunnel connection support;
	- Fixed a bug in display ObjectID type fields;
	- Fixed some UI bugs;
	- Fixed some memory leaks and random crashes;
	- Add confirm panel before drop database or collection;
	- Run queries in a seperate thread so that won't block the UI;
	- Fixed a bug to install on some 10.6.x(64bit) system.

** [2.1.0] **
	
	- Auto expand and collaspe finding results;
	- Display Date_t or Timestamp as GMT time format;
	- Fixed a bug in display ObjectIds in Array element;
	- Import data from mysql database to mongodb;
	- Export data from mongodb to mysql database.

** [2.0.9] **
	
	- Add support for mongohq.com;
	- Changed update behavior;
	- Fixed a bug to detect NumberLong type of BSONElement;
	- Fixed a bug in Array type of BSONElement.

** [2.0.8] **
	
	- Fix several UI bugs in Query Window;
	- Fix bugs in Find Query and Update Query;
	- Fix bugs related to ObjectId;
	- Fix copy&paste bugs.

** [2.0.7] **
	
	- Add sparkle framework to check application updates.

** [2.0.6] **
	
	- fixed some UI bugs;
	- add admin auth support.

## Contribute

I'd love to include your contributions, friend.

Then [send me a pull request](https://github.com/fotonauts/MongoHub-Mac/pull/new/master)!
