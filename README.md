ZF2 Lucene Search Module
Nigel Lundsten
Mar 28 2014


NOTE: 
- zendsearch is not currently in packagist
- this module is not currently in packagist
- composer wont resolve nested dependencies that are not on packagist if their repo is not defined in the root composer.json

you need to add these lines to the composer.json in the root of your project

"repositories": [
    {
        "type": "vcs",
        "url": "https://github.com/zendframework/ZendSearch"
    },
    {
        "type": "vcs",
        "url": "https://github.com/nclundsten/LuceneSearch"
    }
],
"require": {
    "zendframework/zendsearch" : "dev-master"
    "nclundsten/LuceneSearch"  : "dev-master"
}

Quick Start / Demo:
- add the lines above into your root composer.json
- run composer update
- _note_ default storage location for indexes is /dev/shm
- use temp route of /search/build-index to build an index from the example mapper data (this will be replaced later)

How to Use:
- build your own mapper that implements the same interfaces as the example mapper, configure the index/search services in servicemanager

Todo:
- factories
- build index route for console
- lots of other misc
