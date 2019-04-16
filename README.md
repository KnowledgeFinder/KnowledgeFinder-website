# Website for KnowlegeFinder

Homepage (landing page) and announcements for KnowledgeFinder (http://knowledgefinder.github.io).

Based on [Pelican](http://blog.getpelican.com/) and a modified Polar theme by [CodePassenger](http://www.codepassenger.com/).

## Local Installation

* Install Python ([Anaconda](https://store.continuum.io/cshop/anaconda/) works perfectly)

* Install Pelican and supporting libraries

```
pip install pelican
pip install markdown
pip install fabric
pip install ghp-import
```
  or if you are using Windows
```
pip install https://github.com/chevah/ghp-import/archive/win-support.zip 
```

* Clone KnowledgeFinder

```
git clone https://github.com/KnowledgeFinder/knowledgefinder.github.io.git
```
  or
```
git clone git@github.com:KnowledgeFinder/knowledgefinder.github.io.git
```

* Change to ```KnowledgeFinder/```

* Switch to ```source``` branch.
  
```
git checkout source
```

### Configuration

 * Set proper port for local testing which works on your machine in `fabfile.py`

```
# Port for `serve`
PORT = 8001
```

## Build 

 * Generate website 
```
fab build
```
   (If you are using Windows and are getting the error ```ImportError: No module named Crypto.PublicKey```, rename the crypto folder in site-packages to Crypto.)
 * Start local server for testing (accessible via http://localhost:[port]/)
```
fab serve
```

 * Convenience target for rebuild and starting local server
```
fab reserve
```

## Deployment

## Writing Content

Use either [Markdown](http://daringfireball.net/projects/markdown/) or HTML for new articles, as described in [Writing content](http://docs.getpelican.com/en/3.6.3/content.html).

Add new articles to `content`.

### Metadata

The required meta data for KnowledgeFinder release announcements are:
```
Title: Release 1.0 
Date: 2016-09-20 12:00
Category: Releases
Author: KnowledgeFinder
```

### Image sizes

 * Article image: 870x440 px (doesn't apply for the overview image of the article)
 * Thumbnail large: 100x108
 * Thumbnail small: 67x73

### Deploy output to master

After building the website, deploy the page to master and push it:
  ```
fab gh_pages
```
