Title: KnowledgeFinder v1.0 
Date: 2016-09-14 15:00
Category: Releases
Author: KF
Image: 

We are proud to announce the first open source version of KnowledgeFinder.

## Source Code

The source code can be found on [GitHub](https://github.com/KnowledgeFinder). It consist of four projects:

* [KnowledgeFinder Core](https://github.com/KnowledgeFinder/knowledgefinder-core)
* [KnowledgeFinder Dataimport](https://github.com/KnowledgeFinder/knowledgefinder-dataimport)
* [KnowledgeFinder Webservice](https://github.com/KnowledgeFinder/knowledgefinder-webservice)
* [KnowledgeFinder Example Configuration](https://github.com/KnowledgeFinder/knowledgefinder-config-example)

## Feature

### Dataimport

* SVN data store crawler and parser
* Category parser
* Solr Transformer
	* ArrayToStringTransformer
	* AuthorFormatingTransformer
	* CategoriesSeparatedTransformer
	* DateIncompleteFormatTransformer
	* DateToStringTransformer
	* DictToStringTransformer
	* ExcludeValuesTransformer
	* FilePathTransformer
	* FormatingStringTransformer
	* IntToDateTransformer
	* SelectLatestDateTransformer
	* TrimTransformer
	* URLDecodeTransformer

### Webservice

* Queries for Documents, Nodes and Document export in BibTeX
* Role Based Access Control

### Portlet

* Free text search
* Full-text search
* Facets filter
* Date range filter
* Metadata graph
* BibTeX export

### Example Configuration

* 5 example documents
* Metadata import over XML
* Example configuration
	* Role Based Access Control
	* BibTeX export
	* Facets filter
	* Date range filter
	* Full-text search
	* Metadata graph

## Documentation

The documentation can be found in the respective repository. The main documentation can be found in the [core project](https://github.com/KnowledgeFinder/knowledgefinder-core/wiki).

## How to start

Follow the installation instructions in the documentation. Therewith an example project will be installed, allowing you to experience KnowledgeFinder with some data.