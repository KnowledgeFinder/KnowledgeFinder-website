Title: KnowledgeFinder v2.0 
Date: 2018-07-06 15:00
Category: Releases
Author: KF
Image: 

KnowledgeFinder v2.0 has been released. A major release with changes in the overall architecture and supports for updated external libraries.

## Features and improvements

### Core

* Git submodules are introduced for better architecture of the whole project
* KnowledgeFinder-core acts as the parent project and all other works as submodules
* The sole purpose of the core pom is now to build the whole project at the same time

### Dataimport and webapp

* adapted to work with solr 7.2.0
* all solr configuration files are moved to the configuration projects
* maven builds are now generated in the configuration projects

### Portlet

* major refactoring of the code structure
* each panel now only handles the drawing, events are forwarded to the pageManger
* the pageManager handles all events, calls if necessary the connector to request new information form the webservice and forwards the information from the server to the panels for GUI updates
* the connector builds the query url and sends the request to the webservice 
* the urlManager allows to create and manipulate a url
* there is now a knowledgefinder namespace
* pageManager, urlManager and connector are now modules
