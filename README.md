# npmdoc-nsqjs

#### basic api documentation for  [nsqjs (v0.8.4)](https://github.com/dudleycarr/nsqjs)  [![npm package](https://img.shields.io/npm/v/npmdoc-nsqjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nsqjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nsqjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nsqjs)

#### NodeJS client for NSQ

[![NPM](https://nodei.co/npm/nsqjs.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/nsqjs)

- [https://npmdoc.github.io/node-npmdoc-nsqjs/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-nsqjs/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nsqjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dudley Carr"
    },
    "bugs": {
        "url": "https://github.com/dudleycarr/nsqjs/issues"
    },
    "dependencies": {
        "async": "^2.1.4",
        "bignumber.js": "~1.2.1",
        "debug": "^2.6.0",
        "moment": "^2.17.1",
        "node-int64": "~0.3.0",
        "node-state": "~1.4.4",
        "request": "^2.79.0",
        "snappystream": "^0.3.4",
        "underscore": "~1.5.2"
    },
    "description": "NodeJS client for NSQ",
    "devDependencies": {
        "coffee-errors": "^0.8.6",
        "coffee-script": "^1.12.2",
        "coffeelint": "~1.0.2",
        "grunt": "^1.0.0",
        "grunt-cli": "^1.2",
        "grunt-coffeelint": "0.0.16",
        "grunt-contrib-coffee": "^1.0",
        "grunt-contrib-watch": "^1.0.0",
        "grunt-mocha-cli": "^3.0.0",
        "mocha": "^3.2",
        "nock": "~0.27.1",
        "should": "^11.1.2",
        "sinon": "~1.7.3",
        "temp": "^0.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "7c6d769b5f67ab7bc4a03eb2745f5f1fdf7e74b2",
        "tarball": "https://registry.npmjs.org/nsqjs/-/nsqjs-0.8.4.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "1c6b2aff3493bca7d515e722543dc5aeb3ad1566",
    "homepage": "https://github.com/dudleycarr/nsqjs",
    "keywords": [
        "nsq",
        "nsq client",
        "nsq client official",
        "nsqjs",
        "distributed messaging",
        "messaging",
        "task",
        "task management"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/dudleycarr/nsqjs/blob/master/LICENSE-MIT"
        }
    ],
    "main": "lib/nsq",
    "maintainers": [
        {
            "name": "dudley"
        }
    ],
    "name": "nsqjs",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/dudleycarr/nsqjs.git"
    },
    "scripts": {
        "build": "coffee --bare --compile --output lib src/*.coffee",
        "postpublish": "rm -rf lib",
        "prepublish": "coffee --bare --compile --output lib src/*.coffee",
        "test": "grunt test"
    },
    "version": "0.8.4",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
