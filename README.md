# api documentation for  [nsqjs (v0.7.13)](https://github.com/dudleycarr/nsqjs)  [![npm package](https://img.shields.io/npm/v/npmdoc-nsqjs.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-nsqjs) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-nsqjs.svg)](https://travis-ci.org/npmdoc/node-npmdoc-nsqjs)
#### NodeJS client for NSQ

[![NPM](https://nodei.co/npm/nsqjs.png?downloads=true)](https://www.npmjs.com/package/nsqjs)

[![apidoc](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-nsqjs_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-nsqjs/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-nsqjs/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dudley Carr",
        "email": "dudley.carr@gmail.com"
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
        "shasum": "08adb62bc1e7cc6954c402d3b2772ad2ec8dc5fc",
        "tarball": "https://registry.npmjs.org/nsqjs/-/nsqjs-0.7.13.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "792d200304526b06f50bd54fe0c73574ed8179f7",
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
            "name": "dudley",
            "email": "dudley.carr@gmail.com"
        }
    ],
    "name": "nsqjs",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "0.7.13"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module nsqjs](#apidoc.module.nsqjs)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>NSQDConnection (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>Reader (topic, channel, options)](#apidoc.element.nsqjs.Reader)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>Writer (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>WriterNSQDConnection (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>backofftimer (minInterval, maxInterval, ratio, shortLength, longLength)](#apidoc.element.nsqjs.backofftimer)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>framebuffer ()](#apidoc.element.nsqjs.framebuffer)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>message (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>roundrobinlist (lst)](#apidoc.element.nsqjs.roundrobinlist)
1.  object <span class="apidocSignatureSpan">nsqjs.</span>NSQDConnection.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>Reader.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>Writer.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>WriterNSQDConnection.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>backofftimer.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>config
1.  object <span class="apidocSignatureSpan">nsqjs.</span>framebuffer.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>message.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>readerrdy
1.  object <span class="apidocSignatureSpan">nsqjs.</span>roundrobinlist.prototype
1.  object <span class="apidocSignatureSpan">nsqjs.</span>wire

#### [module nsqjs.NSQDConnection](#apidoc.module.nsqjs.NSQDConnection)
1.  boolean <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>NSQDConnection (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection.NSQDConnection)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>EventEmitter ()](#apidoc.element.nsqjs.NSQDConnection.EventEmitter)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>init ()](#apidoc.element.nsqjs.NSQDConnection.init)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.NSQDConnection.listenerCount)
1.  number <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>__super__
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>BACKOFF
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>CLOSED
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>CONNECTED
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>CONNECTION_ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>FINISHED
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>MESSAGE
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>READY
1.  string <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>REQUEUED

#### [module nsqjs.NSQDConnection.prototype](#apidoc.module.nsqjs.NSQDConnection.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>clearIdentifyTimeout ()](#apidoc.element.nsqjs.NSQDConnection.prototype.clearIdentifyTimeout)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>connect ()](#apidoc.element.nsqjs.NSQDConnection.prototype.connect)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>connectionState ()](#apidoc.element.nsqjs.NSQDConnection.prototype.connectionState)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>constructor (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>createMessage (msgPayload)](#apidoc.element.nsqjs.NSQDConnection.prototype.createMessage)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>destroy ()](#apidoc.element.nsqjs.NSQDConnection.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>id ()](#apidoc.element.nsqjs.NSQDConnection.prototype.id)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>identify ()](#apidoc.element.nsqjs.NSQDConnection.prototype.identify)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>identifyTimeout ()](#apidoc.element.nsqjs.NSQDConnection.prototype.identifyTimeout)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>receiveData (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.receiveData)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>receiveRawData (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.receiveRawData)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>reconsumeFrameBuffer ()](#apidoc.element.nsqjs.NSQDConnection.prototype.reconsumeFrameBuffer)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>registerStreamListeners (conn)](#apidoc.element.nsqjs.NSQDConnection.prototype.registerStreamListeners)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>setRdy (rdyCount)](#apidoc.element.nsqjs.NSQDConnection.prototype.setRdy)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startDeflate (level)](#apidoc.element.nsqjs.NSQDConnection.prototype.startDeflate)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startSnappy ()](#apidoc.element.nsqjs.NSQDConnection.prototype.startSnappy)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startTLS (callback)](#apidoc.element.nsqjs.NSQDConnection.prototype.startTLS)
1.  [function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>write (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.write)

#### [module nsqjs.Reader](#apidoc.module.nsqjs.Reader)
1.  boolean <span class="apidocSignatureSpan">nsqjs.Reader.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>Reader (topic, channel, options)](#apidoc.element.nsqjs.Reader.Reader)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.</span>EventEmitter ()](#apidoc.element.nsqjs.Reader.EventEmitter)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.</span>init ()](#apidoc.element.nsqjs.Reader.init)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.Reader.listenerCount)
1.  number <span class="apidocSignatureSpan">nsqjs.Reader.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">nsqjs.Reader.</span>__super__
1.  string <span class="apidocSignatureSpan">nsqjs.Reader.</span>DISCARD
1.  string <span class="apidocSignatureSpan">nsqjs.Reader.</span>ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.Reader.</span>MESSAGE
1.  string <span class="apidocSignatureSpan">nsqjs.Reader.</span>NSQD_CLOSED
1.  string <span class="apidocSignatureSpan">nsqjs.Reader.</span>NSQD_CONNECTED

#### [module nsqjs.Reader.prototype](#apidoc.module.nsqjs.Reader.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>close ()](#apidoc.element.nsqjs.Reader.prototype.close)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>connect ()](#apidoc.element.nsqjs.Reader.prototype.connect)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>connectToNSQD (host, port)](#apidoc.element.nsqjs.Reader.prototype.connectToNSQD)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>constructor (topic, channel, options)](#apidoc.element.nsqjs.Reader.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>handleMessage (message)](#apidoc.element.nsqjs.Reader.prototype.handleMessage)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>isPaused ()](#apidoc.element.nsqjs.Reader.prototype.isPaused)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>pause ()](#apidoc.element.nsqjs.Reader.prototype.pause)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>queryLookupd ()](#apidoc.element.nsqjs.Reader.prototype.queryLookupd)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>registerConnectionListeners (conn)](#apidoc.element.nsqjs.Reader.prototype.registerConnectionListeners)
1.  [function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>unpause ()](#apidoc.element.nsqjs.Reader.prototype.unpause)

#### [module nsqjs.Writer](#apidoc.module.nsqjs.Writer)
1.  boolean <span class="apidocSignatureSpan">nsqjs.Writer.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>Writer (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer.Writer)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.</span>EventEmitter ()](#apidoc.element.nsqjs.Writer.EventEmitter)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.</span>init ()](#apidoc.element.nsqjs.Writer.init)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.Writer.listenerCount)
1.  number <span class="apidocSignatureSpan">nsqjs.Writer.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">nsqjs.Writer.</span>__super__
1.  string <span class="apidocSignatureSpan">nsqjs.Writer.</span>CLOSED
1.  string <span class="apidocSignatureSpan">nsqjs.Writer.</span>ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.Writer.</span>READY

#### [module nsqjs.Writer.prototype](#apidoc.module.nsqjs.Writer.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>close ()](#apidoc.element.nsqjs.Writer.prototype.close)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>connect ()](#apidoc.element.nsqjs.Writer.prototype.connect)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>constructor (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>publish (topic, msgs, callback)](#apidoc.element.nsqjs.Writer.prototype.publish)

#### [module nsqjs.WriterNSQDConnection](#apidoc.module.nsqjs.WriterNSQDConnection)
1.  boolean <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>WriterNSQDConnection (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection.WriterNSQDConnection)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>EventEmitter ()](#apidoc.element.nsqjs.WriterNSQDConnection.EventEmitter)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>init ()](#apidoc.element.nsqjs.WriterNSQDConnection.init)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.WriterNSQDConnection.listenerCount)
1.  number <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>__super__
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>BACKOFF
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>CLOSED
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>CONNECTED
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>CONNECTION_ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>ERROR
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>FINISHED
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>MESSAGE
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>READY
1.  string <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>REQUEUED

#### [module nsqjs.WriterNSQDConnection.prototype](#apidoc.module.nsqjs.WriterNSQDConnection.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>connectionState ()](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.connectionState)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>constructor (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>produceMessages (topic, msgs, callback)](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.produceMessages)

#### [module nsqjs.backofftimer](#apidoc.module.nsqjs.backofftimer)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>backofftimer (minInterval, maxInterval, ratio, shortLength, longLength)](#apidoc.element.nsqjs.backofftimer.backofftimer)

#### [module nsqjs.backofftimer.prototype](#apidoc.module.nsqjs.backofftimer.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>failure ()](#apidoc.element.nsqjs.backofftimer.prototype.failure)
1.  [function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>getInterval ()](#apidoc.element.nsqjs.backofftimer.prototype.getInterval)
1.  [function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>success ()](#apidoc.element.nsqjs.backofftimer.prototype.success)

#### [module nsqjs.config](#apidoc.module.nsqjs.config)
1.  [function <span class="apidocSignatureSpan">nsqjs.config.</span>ConnectionConfig (options)](#apidoc.element.nsqjs.config.ConnectionConfig)
1.  [function <span class="apidocSignatureSpan">nsqjs.config.</span>ReaderConfig ()](#apidoc.element.nsqjs.config.ReaderConfig)

#### [module nsqjs.framebuffer](#apidoc.module.nsqjs.framebuffer)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>framebuffer ()](#apidoc.element.nsqjs.framebuffer.framebuffer)

#### [module nsqjs.framebuffer.prototype](#apidoc.module.nsqjs.framebuffer.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>consume (raw)](#apidoc.element.nsqjs.framebuffer.prototype.consume)
1.  [function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>frameSize (offset)](#apidoc.element.nsqjs.framebuffer.prototype.frameSize)
1.  [function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>nextFrame ()](#apidoc.element.nsqjs.framebuffer.prototype.nextFrame)
1.  [function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>nextOffset (offset)](#apidoc.element.nsqjs.framebuffer.prototype.nextOffset)
1.  [function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>pluckFrame (offset)](#apidoc.element.nsqjs.framebuffer.prototype.pluckFrame)

#### [module nsqjs.message](#apidoc.module.nsqjs.message)
1.  boolean <span class="apidocSignatureSpan">nsqjs.message.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>message (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message.message)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.</span>EventEmitter ()](#apidoc.element.nsqjs.message.EventEmitter)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.</span>init ()](#apidoc.element.nsqjs.message.init)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.message.listenerCount)
1.  number <span class="apidocSignatureSpan">nsqjs.message.</span>FINISH
1.  number <span class="apidocSignatureSpan">nsqjs.message.</span>REQUEUE
1.  number <span class="apidocSignatureSpan">nsqjs.message.</span>TOUCH
1.  number <span class="apidocSignatureSpan">nsqjs.message.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">nsqjs.message.</span>__super__
1.  string <span class="apidocSignatureSpan">nsqjs.message.</span>BACKOFF
1.  string <span class="apidocSignatureSpan">nsqjs.message.</span>RESPOND

#### [module nsqjs.message.prototype](#apidoc.module.nsqjs.message.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>constructor (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>finish ()](#apidoc.element.nsqjs.message.prototype.finish)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>json ()](#apidoc.element.nsqjs.message.prototype.json)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>requeue (delay, backoff)](#apidoc.element.nsqjs.message.prototype.requeue)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>respond (responseType, wireData)](#apidoc.element.nsqjs.message.prototype.respond)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>timeUntilTimeout (hard)](#apidoc.element.nsqjs.message.prototype.timeUntilTimeout)
1.  [function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>touch ()](#apidoc.element.nsqjs.message.prototype.touch)

#### [module nsqjs.readerrdy](#apidoc.module.nsqjs.readerrdy)
1.  [function <span class="apidocSignatureSpan">nsqjs.readerrdy.</span>ConnectionRdy (conn1)](#apidoc.element.nsqjs.readerrdy.ConnectionRdy)
1.  [function <span class="apidocSignatureSpan">nsqjs.readerrdy.</span>ReaderRdy (maxInFlight, maxBackoffDuration, readerId1, lowRdyTimeout)](#apidoc.element.nsqjs.readerrdy.ReaderRdy)

#### [module nsqjs.roundrobinlist](#apidoc.module.nsqjs.roundrobinlist)
1.  [function <span class="apidocSignatureSpan">nsqjs.</span>roundrobinlist (lst)](#apidoc.element.nsqjs.roundrobinlist.roundrobinlist)

#### [module nsqjs.roundrobinlist.prototype](#apidoc.module.nsqjs.roundrobinlist.prototype)
1.  [function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>add (item)](#apidoc.element.nsqjs.roundrobinlist.prototype.add)
1.  [function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>length ()](#apidoc.element.nsqjs.roundrobinlist.prototype.length)
1.  [function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>next (count)](#apidoc.element.nsqjs.roundrobinlist.prototype.next)
1.  [function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>remove (item)](#apidoc.element.nsqjs.roundrobinlist.prototype.remove)

#### [module nsqjs.wire](#apidoc.module.nsqjs.wire)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>auth (token)](#apidoc.element.nsqjs.wire.auth)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>finish (id)](#apidoc.element.nsqjs.wire.finish)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>identify (data)](#apidoc.element.nsqjs.wire.identify)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>mpub (topic, data)](#apidoc.element.nsqjs.wire.mpub)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>nop ()](#apidoc.element.nsqjs.wire.nop)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>pub (topic, data)](#apidoc.element.nsqjs.wire.pub)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>ready (count)](#apidoc.element.nsqjs.wire.ready)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>requeue (id, timeMs)](#apidoc.element.nsqjs.wire.requeue)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>subscribe (topic, channel)](#apidoc.element.nsqjs.wire.subscribe)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>touch (id)](#apidoc.element.nsqjs.wire.touch)
1.  [function <span class="apidocSignatureSpan">nsqjs.wire.</span>unpackMessage (data)](#apidoc.element.nsqjs.wire.unpackMessage)
1.  number <span class="apidocSignatureSpan">nsqjs.wire.</span>FRAME_TYPE_ERROR
1.  number <span class="apidocSignatureSpan">nsqjs.wire.</span>FRAME_TYPE_MESSAGE
1.  number <span class="apidocSignatureSpan">nsqjs.wire.</span>FRAME_TYPE_RESPONSE
1.  string <span class="apidocSignatureSpan">nsqjs.wire.</span>MAGIC_V2



# <a name="apidoc.module.nsqjs"></a>[module nsqjs](#apidoc.module.nsqjs)

#### <a name="apidoc.element.nsqjs.NSQDConnection"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>NSQDConnection (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection)
- description and source-code
```javascript
function NSQDConnection(nsqdHost1, nsqdPort1, topic1, channel, options) {
  var connId;
  this.nsqdHost = nsqdHost1;
  this.nsqdPort = nsqdPort1;
  this.topic = topic1;
  this.channel = channel;
  if (options == null) {
    options = {};
  }
  NSQDConnection.__super__.constructor.apply(this, arguments);
  connId = this.id().replace(':', '/');
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel + ":conn:" + connId);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.frameBuffer = new FrameBuffer();
  this.statemachine = this.connectionState();
  this.maxRdyCount = 0;
  this.msgTimeout = 0;
  this.maxMsgTimeout = 0;
  this.nsqdVersion = null;
  this.lastMessageTimestamp = null;
  this.lastReceivedTimestamp = null;
  this.conn = null;
  this.identifyTimeoutId = null;
  this.messageCallbacks = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>Reader (topic, channel, options)](#apidoc.element.nsqjs.Reader)
- description and source-code
```javascript
function Reader(topic, channel, options) {
  this.topic = topic;
  this.channel = channel;
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel);
  this.config = new ReaderConfig(options);
  this.config.validate();
  this.debug('Configuration');
  this.debug(this.config);
  this.roundrobinLookupd = new RoundRobinList(this.config.lookupdHTTPAddresses);
  this.readerRdy = new ReaderRdy(this.config.maxInFlight, this.config.maxBackoffDuration, this.topic + "/" + this.channel);
  this.connectIntervalId = null;
  this.connectionIds = [];
}
```
- example usage
```shell
...
$ nsqd --lookupd-tcp-address=127.0.0.1:4160 &
'''

#### JavaScript
'''js
var nsq = require('nsqjs');

var reader = new nsq.Reader('sample_topic', 'test_channel', {
lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
console.log('Received message [%s]: %s', msg.id, msg.body.toString());
...
```

#### <a name="apidoc.element.nsqjs.Writer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>Writer (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer)
- description and source-code
```javascript
function Writer(nsqdHost, nsqdPort, options) {
  this.nsqdHost = nsqdHost;
  this.nsqdPort = nsqdPort;
  Writer.__super__.constructor.apply(this, arguments);
  this.setMaxListeners(10000);
  this.debug = Debug("nsqjs:writer:" + this.nsqdHost + "/" + this.nsqdPort);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.ready = false;
  this.debug('Configuration');
  this.debug(this.config);
}
```
- example usage
```shell
...

The writer sends a single message and then a list of messages.

#### JavaScript
'''js
var nsq = require('nsqjs');

var w = new nsq.Writer('127.0.0.1', 4150);

w.connect();

w.on('ready', function () {
w.publish('sample_topic', 'it really tied the room together');
w.publish('sample_topic', [
  'Uh, excuse me. Mark it zero. Next frame.',
...
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>WriterNSQDConnection (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection)
- description and source-code
```javascript
function WriterNSQDConnection(nsqdHost, nsqdPort, options) {
  if (options == null) {
    options = {};
  }
  WriterNSQDConnection.__super__.constructor.call(this, nsqdHost, nsqdPort, null, null, options);
  this.debug = Debug("nsqjs:writer:conn:" + nsqdHost + "/" + nsqdPort);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.backofftimer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>backofftimer (minInterval, maxInterval, ratio, shortLength, longLength)](#apidoc.element.nsqjs.backofftimer)
- description and source-code
```javascript
function BackoffTimer(minInterval, maxInterval, ratio, shortLength, longLength) {
  var intervalDelta;
  if (ratio == null) {
    ratio = .25;
  }
  if (shortLength == null) {
    shortLength = 10;
  }
  if (longLength == null) {
    longLength = 250;
  }
  this.minInterval = decimal(minInterval);
  this.maxInterval = decimal(maxInterval);
  ratio = decimal(ratio);
  intervalDelta = decimal(this.maxInterval - this.minInterval);
  this.maxShortTimer = intervalDelta.times(ratio);
  this.maxLongTimer = intervalDelta.times(decimal(1).minus(ratio));
  this.shortUnit = this.maxShortTimer.dividedBy(shortLength);
  this.longUnit = this.maxLongTimer.dividedBy(longLength);
  this.shortInterval = decimal(0);
  this.longInterval = decimal(0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.framebuffer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>framebuffer ()](#apidoc.element.nsqjs.framebuffer)
- description and source-code
```javascript
function FrameBuffer() {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>message (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message)
- description and source-code
```javascript
function Message(id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout) {
  var trackTimeout;
  this.id = id;
  this.timestamp = timestamp;
  this.attempts = attempts;
  this.body = body;
  this.requeueDelay = requeueDelay;
  this.msgTimeout = msgTimeout;
  this.maxMsgTimeout = maxMsgTimeout;
  this.hasResponded = false;
  this.receivedOn = Date.now();
  this.lastTouched = this.receivedOn;
  this.touchCount = 0;
  this.timedOut = false;
  (trackTimeout = (function(_this) {
    return function() {
      var hard, soft;
      if (_this.hasResponded) {
        return;
      }
      soft = _this.timeUntilTimeout();
      hard = _this.timeUntilTimeout(true);
      _this.timedOut = !soft || !hard;
      if (!_this.timedOut) {
        return setTimeout(trackTimeout, Math.min(soft, hard));
      }
    };
  })(this))();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.roundrobinlist"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>roundrobinlist (lst)](#apidoc.element.nsqjs.roundrobinlist)
- description and source-code
```javascript
function RoundRobinList(lst) {
  this.lst = lst.slice(0);
  this.index = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.NSQDConnection"></a>[module nsqjs.NSQDConnection](#apidoc.module.nsqjs.NSQDConnection)

#### <a name="apidoc.element.nsqjs.NSQDConnection.NSQDConnection"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>NSQDConnection (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection.NSQDConnection)
- description and source-code
```javascript
function NSQDConnection(nsqdHost1, nsqdPort1, topic1, channel, options) {
  var connId;
  this.nsqdHost = nsqdHost1;
  this.nsqdPort = nsqdPort1;
  this.topic = topic1;
  this.channel = channel;
  if (options == null) {
    options = {};
  }
  NSQDConnection.__super__.constructor.apply(this, arguments);
  connId = this.id().replace(':', '/');
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel + ":conn:" + connId);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.frameBuffer = new FrameBuffer();
  this.statemachine = this.connectionState();
  this.maxRdyCount = 0;
  this.msgTimeout = 0;
  this.maxMsgTimeout = 0;
  this.nsqdVersion = null;
  this.lastMessageTimestamp = null;
  this.lastReceivedTimestamp = null;
  this.conn = null;
  this.identifyTimeoutId = null;
  this.messageCallbacks = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.EventEmitter"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>EventEmitter ()](#apidoc.element.nsqjs.NSQDConnection.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.init"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>init ()](#apidoc.element.nsqjs.NSQDConnection.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.listenerCount"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.NSQDConnection.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.NSQDConnection.prototype"></a>[module nsqjs.NSQDConnection.prototype](#apidoc.module.nsqjs.NSQDConnection.prototype)

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.clearIdentifyTimeout"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>clearIdentifyTimeout ()](#apidoc.element.nsqjs.NSQDConnection.prototype.clearIdentifyTimeout)
- description and source-code
```javascript
clearIdentifyTimeout = function () {
  clearTimeout(this.identifyTimeoutId);
  return this.identifyTimeoutId = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.connect"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>connect ()](#apidoc.element.nsqjs.NSQDConnection.prototype.connect)
- description and source-code
```javascript
connect = function () {
  this.statemachine.raise('connecting');
  return process.nextTick((function(_this) {
    return function() {
      _this.conn = net.connect(_this.nsqdPort, _this.nsqdHost, function() {
        _this.statemachine.raise('connected');
        _this.emit(NSQDConnection.CONNECTED);
        return _this.identifyTimeoutId = setTimeout(_this.identifyTimeout.bind(_this), 5000);
      });
      return _this.registerStreamListeners(_this.conn);
    };
  })(this));
}
```
- example usage
```shell
...
'''js
var nsq = require('nsqjs');

var reader = new nsq.Reader('sample_topic', 'test_channel', {
  lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
  console.log('Received message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
});
'''
...
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.connectionState"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>connectionState ()](#apidoc.element.nsqjs.NSQDConnection.prototype.connectionState)
- description and source-code
```javascript
connectionState = function () {
  return this.statemachine || new ConnectionState(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.constructor"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>constructor (nsqdHost1, nsqdPort1, topic1, channel, options)](#apidoc.element.nsqjs.NSQDConnection.prototype.constructor)
- description and source-code
```javascript
function NSQDConnection(nsqdHost1, nsqdPort1, topic1, channel, options) {
  var connId;
  this.nsqdHost = nsqdHost1;
  this.nsqdPort = nsqdPort1;
  this.topic = topic1;
  this.channel = channel;
  if (options == null) {
    options = {};
  }
  NSQDConnection.__super__.constructor.apply(this, arguments);
  connId = this.id().replace(':', '/');
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel + ":conn:" + connId);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.frameBuffer = new FrameBuffer();
  this.statemachine = this.connectionState();
  this.maxRdyCount = 0;
  this.msgTimeout = 0;
  this.maxMsgTimeout = 0;
  this.nsqdVersion = null;
  this.lastMessageTimestamp = null;
  this.lastReceivedTimestamp = null;
  this.conn = null;
  this.identifyTimeoutId = null;
  this.messageCallbacks = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.createMessage"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>createMessage (msgPayload)](#apidoc.element.nsqjs.NSQDConnection.prototype.createMessage)
- description and source-code
```javascript
createMessage = function (msgPayload) {
  var msg, msgComponents;
  msgComponents = wire.unpackMessage(msgPayload);
  msg = (function(func, args, ctor) {
    ctor.prototype = func.prototype;
    var child = new ctor, result = func.apply(child, args);
    return Object(result) === result ? result : child;
  })(Message, slice.call(msgComponents).concat([this.config.requeueDelay], [this.msgTimeout], [this.maxMsgTimeout]), function(){});
  this.debug("Received message [" + msg.id + "] [attempts: " + msg.attempts + "]");
  msg.on(Message.RESPOND, (function(_this) {
    return function(responseType, wireData) {
      _this.write(wireData);
      if (responseType === Message.FINISH) {
        _this.debug("Finished message [" + msg.id + "] [timedout=" + (msg.timedout === true) + ", elapsed=" + (Date.now() - msg.
receivedOn) + "ms, touch_count=" + msg.touchCount + "]");
        return _this.emit(NSQDConnection.FINISHED);
      } else if (responseType === Message.REQUEUE) {
        _this.debug("Requeued message [" + msg.id + "]");
        return _this.emit(NSQDConnection.REQUEUED);
      }
    };
  })(this));
  msg.on(Message.BACKOFF, (function(_this) {
    return function() {
      return _this.emit(NSQDConnection.BACKOFF);
    };
  })(this));
  return msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.destroy"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>destroy ()](#apidoc.element.nsqjs.NSQDConnection.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
  return this.conn.destroy();
}
```
- example usage
```shell
...
    return function() {
      return _this.start();
    };
  })(this));
}

ConnectionRdy.prototype.close = function() {
  return this.conn.destroy();
};

ConnectionRdy.prototype.name = function() {
  return String(this.conn.conn.localPort);
};

ConnectionRdy.prototype.start = function() {
...
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.id"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>id ()](#apidoc.element.nsqjs.NSQDConnection.prototype.id)
- description and source-code
```javascript
id = function () {
  return this.nsqdHost + ":" + this.nsqdPort;
}
```
- example usage
```shell
...

ConnectionRdy.STATE_CHANGE = 'statechange';

function ConnectionRdy(conn1) {
  var connId, readerId;
  this.conn = conn1;
  readerId = this.conn.topic + "/" + this.conn.channel;
  connId = "" + (this.conn.id().replace(':', '/'));
  this.debug = Debug("nsqjs:reader:" + readerId + ":rdy:conn:" + connId);
  this.maxConnRdy = 0;
  this.inFlight = 0;
  this.lastRdySent = 0;
  this.availableRdy = 0;
  this.statemachine = new ConnectionRdyState(this);
  this.conn.on(NSQDConnection.ERROR, (function(_this) {
...
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.identify"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>identify ()](#apidoc.element.nsqjs.NSQDConnection.prototype.identify)
- description and source-code
```javascript
identify = function () {
  var i, identify, key, len, longName, removableKeys, shortName;
  longName = os.hostname();
  shortName = longName.split('.')[0];
  identify = {
    client_id: this.config.clientId || shortName,
    deflate: this.config.deflate,
    deflate_level: this.config.deflateLevel,
    feature_negotiation: true,
    heartbeat_interval: this.config.heartbeatInterval * 1000,
    long_id: longName,
    msg_timeout: this.config.messageTimeout,
    output_buffer_size: this.config.outputBufferSize,
    output_buffer_timeout: this.config.outputBufferTimeout,
    sample_rate: this.config.sampleRate,
    short_id: shortName,
    snappy: this.config.snappy,
    tls_v1: this.config.tls,
    user_agent: "nsqjs/" + version
  };
  removableKeys = ['msg_timeout', 'output_buffer_size', 'output_buffer_timeout', 'sample_rate'];
  for (i = 0, len = removableKeys.length; i < len; i++) {
    key = removableKeys[i];
    if (identify[key] === null) {
      delete identify[key];
    }
  }
  return identify;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.identifyTimeout"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>identifyTimeout ()](#apidoc.element.nsqjs.NSQDConnection.prototype.identifyTimeout)
- description and source-code
```javascript
identifyTimeout = function () {
  return this.statemachine.goto('ERROR', new Error('Timed out identifying with nsqd'));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.receiveData"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>receiveData (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.receiveData)
- description and source-code
```javascript
receiveData = function (data) {
  var frame, frameId, payload, results;
  this.lastReceivedTimestamp = Date.now();
  this.frameBuffer.consume(data);
  results = [];
  while (frame = this.frameBuffer.nextFrame()) {
    frameId = frame[0], payload = frame[1];
    switch (frameId) {
      case wire.FRAME_TYPE_RESPONSE:
        results.push(this.statemachine.raise('response', payload));
        break;
      case wire.FRAME_TYPE_ERROR:
        results.push(this.statemachine.goto('ERROR', new Error(payload.toString())));
        break;
      case wire.FRAME_TYPE_MESSAGE:
        this.lastMessageTimestamp = this.lastReceivedTimestamp;
        results.push(this.statemachine.raise('consumeMessage', this.createMessage(payload)));
        break;
      default:
        results.push(void 0);
    }
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.receiveRawData"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>receiveRawData (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.receiveRawData)
- description and source-code
```javascript
receiveRawData = function (data) {
  if (!this.inflater) {
    return this.receiveData(data);
  } else {
    return this.inflater.write(data, (function(_this) {
      return function() {
        var uncompressedData;
        uncompressedData = _this.inflater.read();
        if (uncompressedData) {
          return _this.receiveData(uncompressedData);
        }
      };
    })(this));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.reconsumeFrameBuffer"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>reconsumeFrameBuffer ()](#apidoc.element.nsqjs.NSQDConnection.prototype.reconsumeFrameBuffer)
- description and source-code
```javascript
reconsumeFrameBuffer = function () {
  var data;
  if (this.frameBuffer.buffer && this.frameBuffer.buffer.length) {
    data = this.frameBuffer.buffer;
    delete this.frameBuffer.buffer;
    return this.receiveRawData(data);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.registerStreamListeners"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>registerStreamListeners (conn)](#apidoc.element.nsqjs.NSQDConnection.prototype.registerStreamListeners)
- description and source-code
```javascript
registerStreamListeners = function (conn) {
  conn.on('data', (function(_this) {
    return function(data) {
      return _this.receiveRawData(data);
    };
  })(this));
  conn.on('error', (function(_this) {
    return function(err) {
      _this.statemachine.goto('CLOSED');
      return _this.emit('connection_error', err);
    };
  })(this));
  return conn.on('close', (function(_this) {
    return function(err) {
      return _this.statemachine.raise('close');
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.setRdy"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>setRdy (rdyCount)](#apidoc.element.nsqjs.NSQDConnection.prototype.setRdy)
- description and source-code
```javascript
setRdy = function (rdyCount) {
  return this.statemachine.raise('ready', rdyCount);
}
```
- example usage
```shell
...
};

ConnectionRdy.prototype.setRdy = function(rdyCount) {
  this.log("RDY " + rdyCount);
  if (rdyCount < 0 || rdyCount > this.maxConnRdy) {
    return;
  }
  this.conn.setRdy(rdyCount);
  return this.availableRdy = this.lastRdySent = rdyCount;
};

ConnectionRdy.prototype.log = function(message) {
  if (message) {
    return this.debug(message);
  }
...
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.startDeflate"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startDeflate (level)](#apidoc.element.nsqjs.NSQDConnection.prototype.startDeflate)
- description and source-code
```javascript
startDeflate = function (level) {
  this.inflater = zlib.createInflateRaw({
    flush: zlib.Z_SYNC_FLUSH
  });
  this.deflater = zlib.createDeflateRaw({
    level: level,
    flush: zlib.Z_SYNC_FLUSH
  });
  return this.reconsumeFrameBuffer();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.startSnappy"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startSnappy ()](#apidoc.element.nsqjs.NSQDConnection.prototype.startSnappy)
- description and source-code
```javascript
startSnappy = function () {
  this.inflater = new UnsnappyStream();
  this.deflater = new SnappyStream();
  return this.reconsumeFrameBuffer();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.startTLS"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>startTLS (callback)](#apidoc.element.nsqjs.NSQDConnection.prototype.startTLS)
- description and source-code
```javascript
startTLS = function (callback) {
  var event, i, len, options, ref1, tlsConn;
  ref1 = ['data', 'error', 'close'];
  for (i = 0, len = ref1.length; i < len; i++) {
    event = ref1[i];
    this.conn.removeAllListeners(event);
  }
  options = {
    socket: this.conn,
    rejectUnauthorized: this.config.tlsVerification
  };
  tlsConn = tls.connect(options, (function(_this) {
    return function() {
      _this.conn = tlsConn;
      return typeof callback === "function" ? callback() : void 0;
    };
  })(this));
  return this.registerStreamListeners(tlsConn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.NSQDConnection.prototype.write"></a>[function <span class="apidocSignatureSpan">nsqjs.NSQDConnection.prototype.</span>write (data)](#apidoc.element.nsqjs.NSQDConnection.prototype.write)
- description and source-code
```javascript
write = function (data) {
  if (this.deflater) {
    return this.deflater.write(data, (function(_this) {
      return function() {
        return _this.conn.write(_this.deflater.read());
      };
    })(this));
  } else {
    return this.conn.write(data);
  }
}
```
- example usage
```shell
...
  throw new Error("MPUB requires an array of message");
}
messages = _.map(data, function(message) {
  var buffer;
  buffer = new Buffer(4 + byteLength(message));
  buffer.writeInt32BE(byteLength(message), 0);
  if (_.isString(message)) {
    buffer.write(message, 4);
  } else {
    message.copy(buffer, 4, 0, buffer.length);
  }
  return buffer;
});
numMessagesBuffer = Buffer(4);
numMessagesBuffer.writeInt32BE(messages.length, 0);
...
```



# <a name="apidoc.module.nsqjs.Reader"></a>[module nsqjs.Reader](#apidoc.module.nsqjs.Reader)

#### <a name="apidoc.element.nsqjs.Reader.Reader"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>Reader (topic, channel, options)](#apidoc.element.nsqjs.Reader.Reader)
- description and source-code
```javascript
function Reader(topic, channel, options) {
  this.topic = topic;
  this.channel = channel;
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel);
  this.config = new ReaderConfig(options);
  this.config.validate();
  this.debug('Configuration');
  this.debug(this.config);
  this.roundrobinLookupd = new RoundRobinList(this.config.lookupdHTTPAddresses);
  this.readerRdy = new ReaderRdy(this.config.maxInFlight, this.config.maxBackoffDuration, this.topic + "/" + this.channel);
  this.connectIntervalId = null;
  this.connectionIds = [];
}
```
- example usage
```shell
...
$ nsqd --lookupd-tcp-address=127.0.0.1:4160 &
'''

#### JavaScript
'''js
var nsq = require('nsqjs');

var reader = new nsq.Reader('sample_topic', 'test_channel', {
lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
console.log('Received message [%s]: %s', msg.id, msg.body.toString());
...
```

#### <a name="apidoc.element.nsqjs.Reader.EventEmitter"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.</span>EventEmitter ()](#apidoc.element.nsqjs.Reader.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.init"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.</span>init ()](#apidoc.element.nsqjs.Reader.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.listenerCount"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.Reader.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.Reader.prototype"></a>[module nsqjs.Reader.prototype](#apidoc.module.nsqjs.Reader.prototype)

#### <a name="apidoc.element.nsqjs.Reader.prototype.close"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>close ()](#apidoc.element.nsqjs.Reader.prototype.close)
- description and source-code
```javascript
close = function () {
  clearInterval(this.connectIntervalId);
  return this.readerRdy.close();
}
```
- example usage
```shell
...
  w.publish('sample_topic', [
    'Uh, excuse me. Mark it zero. Next frame.',
    'Smokey, this is not \'Nam. This is bowling. There are rules.'
  ]);
  w.publish('sample_topic', 'Wu?', function (err) {
    if (err) { return console.error(err.message); }
    console.log('Message sent successfully');
    w.close();
  });
});

w.on('closed', function () {
  console.log('Writer closed');
});
'''
...
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.connect"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>connect ()](#apidoc.element.nsqjs.Reader.prototype.connect)
- description and source-code
```javascript
connect = function () {
  var delay, delayedStart, directConnect, interval;
  interval = this.config.lookupdPollInterval * 1000;
  delay = Math.random() * this.config.lookupdPollJitter * interval;
  if (this.config.nsqdTCPAddresses.length) {
    directConnect = (function(_this) {
      return function() {
        var addr, address, i, len, port, ref, ref1, results;
        if (_this.isPaused()) {
          return;
        }
        if (_this.connectionIds.length < _this.config.nsqdTCPAddresses.length) {
          ref = _this.config.nsqdTCPAddresses;
          results = [];
          for (i = 0, len = ref.length; i < len; i++) {
            addr = ref[i];
            ref1 = addr.split(':'), address = ref1[0], port = ref1[1];
            results.push(_this.connectToNSQD(address, Number(port)));
          }
          return results;
        }
      };
    })(this);
    delayedStart = (function(_this) {
      return function() {
        return _this.connectIntervalId = setInterval(directConnect.bind(_this), interval);
      };
    })(this);
    directConnect();
    return setTimeout(delayedStart, delay);
  } else {
    delayedStart = (function(_this) {
      return function() {
        return _this.connectIntervalId = setInterval(_this.queryLookupd.bind(_this), interval);
      };
    })(this);
    this.queryLookupd();
    return setTimeout(delayedStart, delay);
  }
}
```
- example usage
```shell
...
'''js
var nsq = require('nsqjs');

var reader = new nsq.Reader('sample_topic', 'test_channel', {
  lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
  console.log('Received message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
});
'''
...
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.connectToNSQD"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>connectToNSQD (host, port)](#apidoc.element.nsqjs.Reader.prototype.connectToNSQD)
- description and source-code
```javascript
connectToNSQD = function (host, port) {
  var conn;
  this.debug("discovered " + host + ":" + port + " for " + this.topic + " topic");
  conn = new NSQDConnection(host, port, this.topic, this.channel, this.config);
  if (this.connectionIds.indexOf(conn.id()) !== -1) {
    return;
  }
  this.debug("connecting to " + host + ":" + port);
  this.connectionIds.push(conn.id());
  this.registerConnectionListeners(conn);
  this.readerRdy.addConnection(conn);
  return conn.connect();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.constructor"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>constructor (topic, channel, options)](#apidoc.element.nsqjs.Reader.prototype.constructor)
- description and source-code
```javascript
function Reader(topic, channel, options) {
  this.topic = topic;
  this.channel = channel;
  this.debug = Debug("nsqjs:reader:" + this.topic + "/" + this.channel);
  this.config = new ReaderConfig(options);
  this.config.validate();
  this.debug('Configuration');
  this.debug(this.config);
  this.roundrobinLookupd = new RoundRobinList(this.config.lookupdHTTPAddresses);
  this.readerRdy = new ReaderRdy(this.config.maxInFlight, this.config.maxBackoffDuration, this.topic + "/" + this.channel);
  this.connectIntervalId = null;
  this.connectionIds = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.handleMessage"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>handleMessage (message)](#apidoc.element.nsqjs.Reader.prototype.handleMessage)
- description and source-code
```javascript
handleMessage = function (message) {
  return process.nextTick((function(_this) {
    return function() {
      var autoFinishMessage, numDiscardListeners, ref;
      autoFinishMessage = (0 < (ref = _this.config.maxAttempts) && ref <= message.attempts);
      numDiscardListeners = _this.listeners(Reader.DISCARD).length;
      if (autoFinishMessage && numDiscardListeners > 0) {
        _this.emit(Reader.DISCARD, message);
      } else {
        _this.emit(Reader.MESSAGE, message);
      }
      if (autoFinishMessage) {
        return message.finish();
      }
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.isPaused"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>isPaused ()](#apidoc.element.nsqjs.Reader.prototype.isPaused)
- description and source-code
```javascript
isPaused = function () {
  return this.readerRdy.isPaused();
}
```
- example usage
```shell
...
};

ReaderRdy.prototype.isLowRdy = function() {
  return this.maxInFlight < this.connections.length;
};

ReaderRdy.prototype.onMessageSuccess = function(connectionRdy) {
  if (!this.isPaused()) {
    if (this.isLowRdy()) {
      return this.balance();
    } else {
      return connectionRdy.bump();
    }
  }
};
...
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.pause"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>pause ()](#apidoc.element.nsqjs.Reader.prototype.pause)
- description and source-code
```javascript
pause = function () {
  this.debug('pause');
  return this.readerRdy.pause();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.queryLookupd"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>queryLookupd ()](#apidoc.element.nsqjs.Reader.prototype.queryLookupd)
- description and source-code
```javascript
queryLookupd = function () {
  var endpoint;
  if (this.isPaused()) {
    return;
  }
  endpoint = this.roundrobinLookupd.next();
  return lookup(endpoint, this.topic, (function(_this) {
    return function(err, nodes) {
      var i, len, n, results;
      if (!err) {
        results = [];
        for (i = 0, len = nodes.length; i < len; i++) {
          n = nodes[i];
          results.push(_this.connectToNSQD(n.broadcast_address, n.tcp_port));
        }
        return results;
      }
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.registerConnectionListeners"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>registerConnectionListeners (conn)](#apidoc.element.nsqjs.Reader.prototype.registerConnectionListeners)
- description and source-code
```javascript
registerConnectionListeners = function (conn) {
  conn.on(NSQDConnection.CONNECTED, (function(_this) {
    return function() {
      _this.debug(Reader.NSQD_CONNECTED);
      return _this.emit(Reader.NSQD_CONNECTED, conn.nsqdHost, conn.nsqdPort);
    };
  })(this));
  conn.on(NSQDConnection.ERROR, (function(_this) {
    return function(err) {
      _this.debug(Reader.ERROR);
      _this.debug(err);
      return _this.emit(Reader.ERROR, err);
    };
  })(this));
  conn.on(NSQDConnection.CONNECTION_ERROR, (function(_this) {
    return function(err) {
      _this.debug(Reader.ERROR);
      _this.debug(err);
      return _this.emit(Reader.ERROR, err);
    };
  })(this));
  conn.on(NSQDConnection.CLOSED, (function(_this) {
    return function() {
      var index;
      _this.debug(Reader.NSQD_CLOSED);
      index = _this.connectionIds.indexOf(conn.id());
      if (index === -1) {
        return;
      }
      _this.connectionIds.splice(index, 1);
      return _this.emit(Reader.NSQD_CLOSED, conn.nsqdHost, conn.nsqdPort);
    };
  })(this));
  return conn.on(NSQDConnection.MESSAGE, (function(_this) {
    return function(message) {
      return _this.handleMessage(message);
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Reader.prototype.unpause"></a>[function <span class="apidocSignatureSpan">nsqjs.Reader.prototype.</span>unpause ()](#apidoc.element.nsqjs.Reader.prototype.unpause)
- description and source-code
```javascript
unpause = function () {
  this.debug('unpause');
  return this.readerRdy.unpause();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.Writer"></a>[module nsqjs.Writer](#apidoc.module.nsqjs.Writer)

#### <a name="apidoc.element.nsqjs.Writer.Writer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>Writer (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer.Writer)
- description and source-code
```javascript
function Writer(nsqdHost, nsqdPort, options) {
  this.nsqdHost = nsqdHost;
  this.nsqdPort = nsqdPort;
  Writer.__super__.constructor.apply(this, arguments);
  this.setMaxListeners(10000);
  this.debug = Debug("nsqjs:writer:" + this.nsqdHost + "/" + this.nsqdPort);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.ready = false;
  this.debug('Configuration');
  this.debug(this.config);
}
```
- example usage
```shell
...

The writer sends a single message and then a list of messages.

#### JavaScript
'''js
var nsq = require('nsqjs');

var w = new nsq.Writer('127.0.0.1', 4150);

w.connect();

w.on('ready', function () {
w.publish('sample_topic', 'it really tied the room together');
w.publish('sample_topic', [
  'Uh, excuse me. Mark it zero. Next frame.',
...
```

#### <a name="apidoc.element.nsqjs.Writer.EventEmitter"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.</span>EventEmitter ()](#apidoc.element.nsqjs.Writer.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Writer.init"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.</span>init ()](#apidoc.element.nsqjs.Writer.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Writer.listenerCount"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.Writer.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.Writer.prototype"></a>[module nsqjs.Writer.prototype](#apidoc.module.nsqjs.Writer.prototype)

#### <a name="apidoc.element.nsqjs.Writer.prototype.close"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>close ()](#apidoc.element.nsqjs.Writer.prototype.close)
- description and source-code
```javascript
close = function () {
  return this.conn.destroy();
}
```
- example usage
```shell
...
  w.publish('sample_topic', [
    'Uh, excuse me. Mark it zero. Next frame.',
    'Smokey, this is not \'Nam. This is bowling. There are rules.'
  ]);
  w.publish('sample_topic', 'Wu?', function (err) {
    if (err) { return console.error(err.message); }
    console.log('Message sent successfully');
    w.close();
  });
});

w.on('closed', function () {
  console.log('Writer closed');
});
'''
...
```

#### <a name="apidoc.element.nsqjs.Writer.prototype.connect"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>connect ()](#apidoc.element.nsqjs.Writer.prototype.connect)
- description and source-code
```javascript
connect = function () {
  this.conn = new WriterNSQDConnection(this.nsqdHost, this.nsqdPort, this.config);
  this.debug('connect');
  this.conn.connect();
  this.conn.on(WriterNSQDConnection.READY, (function(_this) {
    return function() {
      _this.debug('ready');
      _this.ready = true;
      return _this.emit(Writer.READY);
    };
  })(this));
  this.conn.on(WriterNSQDConnection.CLOSED, (function(_this) {
    return function() {
      _this.debug('closed');
      _this.ready = false;
      return _this.emit(Writer.CLOSED);
    };
  })(this));
  this.conn.on(WriterNSQDConnection.ERROR, (function(_this) {
    return function(err) {
      _this.debug('error', err);
      _this.ready = false;
      return _this.emit(Writer.ERROR, err);
    };
  })(this));
  return this.conn.on(WriterNSQDConnection.CONNECTION_ERROR, (function(_this) {
    return function(err) {
      _this.debug('error', err);
      _this.ready = false;
      return _this.emit(Writer.ERROR, err);
    };
  })(this));
}
```
- example usage
```shell
...
'''js
var nsq = require('nsqjs');

var reader = new nsq.Reader('sample_topic', 'test_channel', {
  lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
  console.log('Received message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
});
'''
...
```

#### <a name="apidoc.element.nsqjs.Writer.prototype.constructor"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>constructor (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.Writer.prototype.constructor)
- description and source-code
```javascript
function Writer(nsqdHost, nsqdPort, options) {
  this.nsqdHost = nsqdHost;
  this.nsqdPort = nsqdPort;
  Writer.__super__.constructor.apply(this, arguments);
  this.setMaxListeners(10000);
  this.debug = Debug("nsqjs:writer:" + this.nsqdHost + "/" + this.nsqdPort);
  this.config = new ConnectionConfig(options);
  this.config.validate();
  this.ready = false;
  this.debug('Configuration');
  this.debug(this.config);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.Writer.prototype.publish"></a>[function <span class="apidocSignatureSpan">nsqjs.Writer.prototype.</span>publish (topic, msgs, callback)](#apidoc.element.nsqjs.Writer.prototype.publish)
- description and source-code
```javascript
publish = function (topic, msgs, callback) {
  var connState, err, failed, msg, ready, ref, ref1, remove;
  connState = (ref = this.conn) != null ? (ref1 = ref.statemachine) != null ? ref1.current_state_name : void 0 : void 0;
  if (!this.conn || (connState === 'CLOSED' || connState === 'ERROR')) {
    err = new Error('No active Writer connection to send messages');
  }
  if (!msgs || _.isEmpty(msgs)) {
    err = new Error('Attempting to publish an empty message');
  }
  if (err) {
    if (callback) {
      return callback(err);
    }
    throw err;
  }
  if (!this.ready) {
    ready = (function(_this) {
      return function() {
        remove();
        return _this.publish(topic, msgs, callback);
      };
    })(this);
    failed = function(err) {
      err || (err = new Error('Connection closed!'));
      remove();
      return callback(err);
    };
    remove = (function(_this) {
      return function() {
        _this.removeListener(Writer.READY, ready);
        _this.removeListener(Writer.ERROR, failed);
        return _this.removeListener(Writer.CLOSED, failed);
      };
    })(this);
    this.on(Writer.READY, ready);
    this.on(Writer.ERROR, failed);
    this.on(Writer.CLOSED, failed);
    return;
  }
  if (!_.isArray(msgs)) {
    msgs = [msgs];
  }
  msgs = (function() {
    var i, len, results;
    results = [];
    for (i = 0, len = msgs.length; i < len; i++) {
      msg = msgs[i];
      if (_.isString(msg) || Buffer.isBuffer(msg)) {
        results.push(msg);
      } else {
        results.push(JSON.stringify(msg));
      }
    }
    return results;
  })();
  return this.conn.produceMessages(topic, msgs, callback);
}
```
- example usage
```shell
...
var nsq = require('nsqjs');

var w = new nsq.Writer('127.0.0.1', 4150);

w.connect();

w.on('ready', function () {
w.publish('sample_topic', 'it really tied the room together');
w.publish('sample_topic', [
  'Uh, excuse me. Mark it zero. Next frame.',
  'Smokey, this is not \'Nam. This is bowling. There are rules.'
]);
w.publish('sample_topic', 'Wu?', function (err) {
  if (err) { return console.error(err.message); }
  console.log('Message sent successfully');
...
```



# <a name="apidoc.module.nsqjs.WriterNSQDConnection"></a>[module nsqjs.WriterNSQDConnection](#apidoc.module.nsqjs.WriterNSQDConnection)

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.WriterNSQDConnection"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>WriterNSQDConnection (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection.WriterNSQDConnection)
- description and source-code
```javascript
function WriterNSQDConnection(nsqdHost, nsqdPort, options) {
  if (options == null) {
    options = {};
  }
  WriterNSQDConnection.__super__.constructor.call(this, nsqdHost, nsqdPort, null, null, options);
  this.debug = Debug("nsqjs:writer:conn:" + nsqdHost + "/" + nsqdPort);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.EventEmitter"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>EventEmitter ()](#apidoc.element.nsqjs.WriterNSQDConnection.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.init"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>init ()](#apidoc.element.nsqjs.WriterNSQDConnection.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.listenerCount"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.WriterNSQDConnection.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.WriterNSQDConnection.prototype"></a>[module nsqjs.WriterNSQDConnection.prototype](#apidoc.module.nsqjs.WriterNSQDConnection.prototype)

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.prototype.connectionState"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>connectionState ()](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.connectionState)
- description and source-code
```javascript
connectionState = function () {
  return this.statemachine || new WriterConnectionState(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.prototype.constructor"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>constructor (nsqdHost, nsqdPort, options)](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.constructor)
- description and source-code
```javascript
function WriterNSQDConnection(nsqdHost, nsqdPort, options) {
  if (options == null) {
    options = {};
  }
  WriterNSQDConnection.__super__.constructor.call(this, nsqdHost, nsqdPort, null, null, options);
  this.debug = Debug("nsqjs:writer:conn:" + nsqdHost + "/" + nsqdPort);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.WriterNSQDConnection.prototype.produceMessages"></a>[function <span class="apidocSignatureSpan">nsqjs.WriterNSQDConnection.prototype.</span>produceMessages (topic, msgs, callback)](#apidoc.element.nsqjs.WriterNSQDConnection.prototype.produceMessages)
- description and source-code
```javascript
produceMessages = function (topic, msgs, callback) {
  return this.statemachine.raise('produceMessages', [topic, msgs, callback]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.backofftimer"></a>[module nsqjs.backofftimer](#apidoc.module.nsqjs.backofftimer)

#### <a name="apidoc.element.nsqjs.backofftimer.backofftimer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>backofftimer (minInterval, maxInterval, ratio, shortLength, longLength)](#apidoc.element.nsqjs.backofftimer.backofftimer)
- description and source-code
```javascript
function BackoffTimer(minInterval, maxInterval, ratio, shortLength, longLength) {
  var intervalDelta;
  if (ratio == null) {
    ratio = .25;
  }
  if (shortLength == null) {
    shortLength = 10;
  }
  if (longLength == null) {
    longLength = 250;
  }
  this.minInterval = decimal(minInterval);
  this.maxInterval = decimal(maxInterval);
  ratio = decimal(ratio);
  intervalDelta = decimal(this.maxInterval - this.minInterval);
  this.maxShortTimer = intervalDelta.times(ratio);
  this.maxLongTimer = intervalDelta.times(decimal(1).minus(ratio));
  this.shortUnit = this.maxShortTimer.dividedBy(shortLength);
  this.longUnit = this.maxLongTimer.dividedBy(longLength);
  this.shortInterval = decimal(0);
  this.longInterval = decimal(0);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.backofftimer.prototype"></a>[module nsqjs.backofftimer.prototype](#apidoc.module.nsqjs.backofftimer.prototype)

#### <a name="apidoc.element.nsqjs.backofftimer.prototype.failure"></a>[function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>failure ()](#apidoc.element.nsqjs.backofftimer.prototype.failure)
- description and source-code
```javascript
failure = function () {
  this.shortInterval = this.shortInterval.plus(this.shortUnit);
  this.longInterval = this.longInterval.plus(this.longUnit);
  this.shortInterval = min(this.shortInterval, this.maxShortTimer);
  return this.longInterval = min(this.longInterval, this.maxLongTimer);
}
```
- example usage
```shell
...
  pause: function() {
    return this.goto('PAUSE');
  },
  unpause: function() {}
},
BACKOFF: {
  Enter: function() {
    this.backoffTimer.failure();
    return this.backoff();
  },
  backoff: function() {
    this.backoffTimer.failure();
    return this.backoff();
  },
  success: function() {},
...
```

#### <a name="apidoc.element.nsqjs.backofftimer.prototype.getInterval"></a>[function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>getInterval ()](#apidoc.element.nsqjs.backofftimer.prototype.getInterval)
- description and source-code
```javascript
getInterval = function () {
  return this.minInterval.plus(this.shortInterval.plus(this.longInterval));
}
```
- example usage
```shell
...
  }
  onTimeout = (function(_this) {
    return function() {
      _this.log('Backoff done');
      return _this.raise('try');
    };
  })(this);
  delay = new Number(this.backoffTimer.getInterval().valueOf()) * 1000;
  this.backoffId = setTimeout(onTimeout, delay);
  return this.log("Backoff for " + delay);
};

ReaderRdy.prototype.inFlight = function() {
  var add;
  add = function(previous, conn) {
...
```

#### <a name="apidoc.element.nsqjs.backofftimer.prototype.success"></a>[function <span class="apidocSignatureSpan">nsqjs.backofftimer.prototype.</span>success ()](#apidoc.element.nsqjs.backofftimer.prototype.success)
- description and source-code
```javascript
success = function () {
  this.shortInterval = this.shortInterval.minus(this.shortUnit);
  this.longInterval = this.longInterval.minus(this.longUnit);
  this.shortInterval = max(this.shortInterval, decimal(0));
  return this.longInterval = max(this.longInterval, decimal(0));
}
```
- example usage
```shell
...
Enter: function() {
  return this["try"]();
},
backoff: function() {
  return this.goto('BACKOFF');
},
success: function(connectionRdy) {
  this.backoffTimer.success();
  this.onMessageSuccess(connectionRdy);
  return this.goto('MAX');
},
"try": function() {},
pause: function() {
  return this.goto('PAUSE');
},
...
```



# <a name="apidoc.module.nsqjs.config"></a>[module nsqjs.config](#apidoc.module.nsqjs.config)

#### <a name="apidoc.element.nsqjs.config.ConnectionConfig"></a>[function <span class="apidocSignatureSpan">nsqjs.config.</span>ConnectionConfig (options)](#apidoc.element.nsqjs.config.ConnectionConfig)
- description and source-code
```javascript
function ConnectionConfig(options) {
  if (options == null) {
    options = {};
  }
  options = _.chain(options).pick(_.keys(this.constructor.DEFAULTS)).defaults(this.constructor.DEFAULTS).value();
  _.extend(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.config.ReaderConfig"></a>[function <span class="apidocSignatureSpan">nsqjs.config.</span>ReaderConfig ()](#apidoc.element.nsqjs.config.ReaderConfig)
- description and source-code
```javascript
function ReaderConfig() {
  return ReaderConfig.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.framebuffer"></a>[module nsqjs.framebuffer](#apidoc.module.nsqjs.framebuffer)

#### <a name="apidoc.element.nsqjs.framebuffer.framebuffer"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>framebuffer ()](#apidoc.element.nsqjs.framebuffer.framebuffer)
- description and source-code
```javascript
function FrameBuffer() {}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.framebuffer.prototype"></a>[module nsqjs.framebuffer.prototype](#apidoc.module.nsqjs.framebuffer.prototype)

#### <a name="apidoc.element.nsqjs.framebuffer.prototype.consume"></a>[function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>consume (raw)](#apidoc.element.nsqjs.framebuffer.prototype.consume)
- description and source-code
```javascript
consume = function (raw) {
  return this.buffer = Buffer.concat(_.compact([this.buffer, raw]));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.framebuffer.prototype.frameSize"></a>[function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>frameSize (offset)](#apidoc.element.nsqjs.framebuffer.prototype.frameSize)
- description and source-code
```javascript
frameSize = function (offset) {
  if (!(this.buffer && this.buffer.length > 4)) {
    return;
  }
  if (offset + 4 <= this.buffer.length) {
    return 4 + this.buffer.readInt32BE(offset);
  }
}
```
- example usage
```shell
...
};

FrameBuffer.prototype.nextFrame = function() {
  var frame, nextOffset;
  if (!this.buffer) {
    return;
  }
  if (!(this.frameSize(0) && this.frameSize(0) <= this.buffer.length)) {
    return;
  }
  frame = this.pluckFrame();
  nextOffset = this.nextOffset();
  this.buffer = this.buffer.slice(nextOffset);
  if (!this.buffer.length) {
    delete this.buffer;
...
```

#### <a name="apidoc.element.nsqjs.framebuffer.prototype.nextFrame"></a>[function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>nextFrame ()](#apidoc.element.nsqjs.framebuffer.prototype.nextFrame)
- description and source-code
```javascript
nextFrame = function () {
  var frame, nextOffset;
  if (!this.buffer) {
    return;
  }
  if (!(this.frameSize(0) && this.frameSize(0) <= this.buffer.length)) {
    return;
  }
  frame = this.pluckFrame();
  nextOffset = this.nextOffset();
  this.buffer = this.buffer.slice(nextOffset);
  if (!this.buffer.length) {
    delete this.buffer;
  }
  return frame;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.framebuffer.prototype.nextOffset"></a>[function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>nextOffset (offset)](#apidoc.element.nsqjs.framebuffer.prototype.nextOffset)
- description and source-code
```javascript
nextOffset = function (offset) {
  var size;
  if (offset == null) {
    offset = 0;
  }
  size = this.frameSize(offset);
  if (size) {
    return offset + size;
  }
}
```
- example usage
```shell
...
  if (!this.buffer) {
    return;
  }
  if (!(this.frameSize(0) && this.frameSize(0) <= this.buffer.length)) {
    return;
  }
  frame = this.pluckFrame();
  nextOffset = this.nextOffset();
  this.buffer = this.buffer.slice(nextOffset);
  if (!this.buffer.length) {
    delete this.buffer;
  }
  return frame;
};
...
```

#### <a name="apidoc.element.nsqjs.framebuffer.prototype.pluckFrame"></a>[function <span class="apidocSignatureSpan">nsqjs.framebuffer.prototype.</span>pluckFrame (offset)](#apidoc.element.nsqjs.framebuffer.prototype.pluckFrame)
- description and source-code
```javascript
pluckFrame = function (offset) {
  var frame, frameId;
  if (offset == null) {
    offset = 0;
  }
  frame = this.buffer.slice(offset, offset + this.frameSize(offset));
  frameId = frame.readInt32BE(4);
  return [frameId, frame.slice(8)];
}
```
- example usage
```shell
...
  var frame, nextOffset;
  if (!this.buffer) {
    return;
  }
  if (!(this.frameSize(0) && this.frameSize(0) <= this.buffer.length)) {
    return;
  }
  frame = this.pluckFrame();
  nextOffset = this.nextOffset();
  this.buffer = this.buffer.slice(nextOffset);
  if (!this.buffer.length) {
    delete this.buffer;
  }
  return frame;
};
...
```



# <a name="apidoc.module.nsqjs.message"></a>[module nsqjs.message](#apidoc.module.nsqjs.message)

#### <a name="apidoc.element.nsqjs.message.message"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>message (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message.message)
- description and source-code
```javascript
function Message(id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout) {
  var trackTimeout;
  this.id = id;
  this.timestamp = timestamp;
  this.attempts = attempts;
  this.body = body;
  this.requeueDelay = requeueDelay;
  this.msgTimeout = msgTimeout;
  this.maxMsgTimeout = maxMsgTimeout;
  this.hasResponded = false;
  this.receivedOn = Date.now();
  this.lastTouched = this.receivedOn;
  this.touchCount = 0;
  this.timedOut = false;
  (trackTimeout = (function(_this) {
    return function() {
      var hard, soft;
      if (_this.hasResponded) {
        return;
      }
      soft = _this.timeUntilTimeout();
      hard = _this.timeUntilTimeout(true);
      _this.timedOut = !soft || !hard;
      if (!_this.timedOut) {
        return setTimeout(trackTimeout, Math.min(soft, hard));
      }
    };
  })(this))();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message.EventEmitter"></a>[function <span class="apidocSignatureSpan">nsqjs.message.</span>EventEmitter ()](#apidoc.element.nsqjs.message.EventEmitter)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message.init"></a>[function <span class="apidocSignatureSpan">nsqjs.message.</span>init ()](#apidoc.element.nsqjs.message.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message.listenerCount"></a>[function <span class="apidocSignatureSpan">nsqjs.message.</span>listenerCount (emitter, type)](#apidoc.element.nsqjs.message.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.message.prototype"></a>[module nsqjs.message.prototype](#apidoc.module.nsqjs.message.prototype)

#### <a name="apidoc.element.nsqjs.message.prototype.constructor"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>constructor (id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout)](#apidoc.element.nsqjs.message.prototype.constructor)
- description and source-code
```javascript
function Message(id, timestamp, attempts, body, requeueDelay, msgTimeout, maxMsgTimeout) {
  var trackTimeout;
  this.id = id;
  this.timestamp = timestamp;
  this.attempts = attempts;
  this.body = body;
  this.requeueDelay = requeueDelay;
  this.msgTimeout = msgTimeout;
  this.maxMsgTimeout = maxMsgTimeout;
  this.hasResponded = false;
  this.receivedOn = Date.now();
  this.lastTouched = this.receivedOn;
  this.touchCount = 0;
  this.timedOut = false;
  (trackTimeout = (function(_this) {
    return function() {
      var hard, soft;
      if (_this.hasResponded) {
        return;
      }
      soft = _this.timeUntilTimeout();
      hard = _this.timeUntilTimeout(true);
      _this.timedOut = !soft || !hard;
      if (!_this.timedOut) {
        return setTimeout(trackTimeout, Math.min(soft, hard));
      }
    };
  })(this))();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message.prototype.finish"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>finish ()](#apidoc.element.nsqjs.message.prototype.finish)
- description and source-code
```javascript
finish = function () {
  return this.respond(Message.FINISH, wire.finish(this.id));
}
```
- example usage
```shell
...
  lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
  console.log('Received message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
});
'''

#### CoffeeScript
'''coffee-script
nsq = require 'nsqjs'
...
```

#### <a name="apidoc.element.nsqjs.message.prototype.json"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>json ()](#apidoc.element.nsqjs.message.prototype.json)
- description and source-code
```javascript
json = function () {
  var err;
  if (this.parsed == null) {
    try {
      this.parsed = JSON.parse(this.body);
    } catch (error) {
      err = error;
      throw new Error("Invalid JSON in Message");
    }
  }
  return this.parsed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.message.prototype.requeue"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>requeue (delay, backoff)](#apidoc.element.nsqjs.message.prototype.requeue)
- description and source-code
```javascript
requeue = function (delay, backoff) {
  if (delay == null) {
    delay = this.requeueDelay;
  }
  if (backoff == null) {
    backoff = true;
  }
  this.respond(Message.REQUEUE, wire.requeue(this.id, delay));
  if (backoff) {
    return this.emit(Message.BACKOFF);
  }
}
```
- example usage
```shell
...
Message.prototype.requeue = function(delay, backoff) {
  if (delay == null) {
    delay = this.requeueDelay;
  }
  if (backoff == null) {
    backoff = true;
  }
  this.respond(Message.REQUEUE, wire.requeue(this.id, delay));
  if (backoff) {
    return this.emit(Message.BACKOFF);
  }
};

Message.prototype.touch = function() {
  this.touchCount += 1;
...
```

#### <a name="apidoc.element.nsqjs.message.prototype.respond"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>respond (responseType, wireData)](#apidoc.element.nsqjs.message.prototype.respond)
- description and source-code
```javascript
respond = function (responseType, wireData) {
  if (this.hasResponded) {
    return;
  }
  return process.nextTick((function(_this) {
    return function() {
      if (responseType !== Message.TOUCH) {
        _this.hasResponded = true;
      } else {
        _this.lastTouched = Date.now();
      }
      return _this.emit(Message.RESPOND, responseType, wireData);
    };
  })(this));
}
```
- example usage
```shell
...
    return delta;
  } else {
    return null;
  }
};

Message.prototype.finish = function() {
  return this.respond(Message.FINISH, wire.finish(this.id));
};

Message.prototype.requeue = function(delay, backoff) {
  if (delay == null) {
    delay = this.requeueDelay;
  }
  if (backoff == null) {
...
```

#### <a name="apidoc.element.nsqjs.message.prototype.timeUntilTimeout"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>timeUntilTimeout (hard)](#apidoc.element.nsqjs.message.prototype.timeUntilTimeout)
- description and source-code
```javascript
timeUntilTimeout = function (hard) {
  var delta;
  if (hard == null) {
    hard = false;
  }
  if (this.hasResponded) {
    return null;
  }
  delta = hard ? this.receivedOn + this.maxMsgTimeout - Date.now() : this.lastTouched + this.msgTimeout - Date.now();
  if (delta > 0) {
    return delta;
  } else {
    return null;
  }
}
```
- example usage
```shell
...
console.log('Received message [%s]', msg.id);

function touch() {
  if (!msg.hasResponded) {
    console.log('Touch [%s]', msg.id);
    msg.touch();
    // Touch the message again a second before the next timeout.
    setTimeout(touch, msg.timeUntilTimeout() - 1000);
  }
}

function finish() {
  console.log('Finished message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
}
...
```

#### <a name="apidoc.element.nsqjs.message.prototype.touch"></a>[function <span class="apidocSignatureSpan">nsqjs.message.prototype.</span>touch ()](#apidoc.element.nsqjs.message.prototype.touch)
- description and source-code
```javascript
touch = function () {
  this.touchCount += 1;
  this.lastTouched = Date.now();
  return this.respond(Message.TOUCH, wire.touch(this.id));
}
```
- example usage
```shell
...

reader.on('message', function (msg) {
console.log('Received message [%s]', msg.id);

function touch() {
  if (!msg.hasResponded) {
    console.log('Touch [%s]', msg.id);
    msg.touch();
    // Touch the message again a second before the next timeout.
    setTimeout(touch, msg.timeUntilTimeout() - 1000);
  }
}

function finish() {
  console.log('Finished message [%s]: %s', msg.id, msg.body.toString());
...
```



# <a name="apidoc.module.nsqjs.readerrdy"></a>[module nsqjs.readerrdy](#apidoc.module.nsqjs.readerrdy)

#### <a name="apidoc.element.nsqjs.readerrdy.ConnectionRdy"></a>[function <span class="apidocSignatureSpan">nsqjs.readerrdy.</span>ConnectionRdy (conn1)](#apidoc.element.nsqjs.readerrdy.ConnectionRdy)
- description and source-code
```javascript
function ConnectionRdy(conn1) {
  var connId, readerId;
  this.conn = conn1;
  readerId = this.conn.topic + "/" + this.conn.channel;
  connId = "" + (this.conn.id().replace(':', '/'));
  this.debug = Debug("nsqjs:reader:" + readerId + ":rdy:conn:" + connId);
  this.maxConnRdy = 0;
  this.inFlight = 0;
  this.lastRdySent = 0;
  this.availableRdy = 0;
  this.statemachine = new ConnectionRdyState(this);
  this.conn.on(NSQDConnection.ERROR, (function(_this) {
    return function(err) {
      return _this.log(err);
    };
  })(this));
  this.conn.on(NSQDConnection.MESSAGE, (function(_this) {
    return function() {
      if (_this.idleId != null) {
        clearTimeout(_this.idleId);
      }
      _this.idleId = null;
      _this.inFlight += 1;
      return _this.availableRdy -= 1;
    };
  })(this));
  this.conn.on(NSQDConnection.FINISHED, (function(_this) {
    return function() {
      return _this.inFlight -= 1;
    };
  })(this));
  this.conn.on(NSQDConnection.REQUEUED, (function(_this) {
    return function() {
      return _this.inFlight -= 1;
    };
  })(this));
  this.conn.on(NSQDConnection.READY, (function(_this) {
    return function() {
      return _this.start();
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.readerrdy.ReaderRdy"></a>[function <span class="apidocSignatureSpan">nsqjs.readerrdy.</span>ReaderRdy (maxInFlight, maxBackoffDuration, readerId1, lowRdyTimeout)](#apidoc.element.nsqjs.readerrdy.ReaderRdy)
- description and source-code
```javascript
function ReaderRdy(maxInFlight, maxBackoffDuration, readerId1, lowRdyTimeout) {
  this.maxInFlight = maxInFlight;
  this.maxBackoffDuration = maxBackoffDuration;
  this.readerId = readerId1;
  this.lowRdyTimeout = lowRdyTimeout != null ? lowRdyTimeout : 1.5;
  this.debug = Debug("nsqjs:reader:" + this.readerId + ":rdy");
  ReaderRdy.__super__.constructor.call(this, {
    autostart: true,
    initial_state: 'ZERO',
    sync_goto: true
  });
  this.id = ReaderRdy.getId();
  this.backoffTimer = new BackoffTimer(0, this.maxBackoffDuration);
  this.backoffId = null;
  this.balanceId = null;
  this.connections = [];
  this.roundRobinConnections = new RoundRobinList([]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.roundrobinlist"></a>[module nsqjs.roundrobinlist](#apidoc.module.nsqjs.roundrobinlist)

#### <a name="apidoc.element.nsqjs.roundrobinlist.roundrobinlist"></a>[function <span class="apidocSignatureSpan">nsqjs.</span>roundrobinlist (lst)](#apidoc.element.nsqjs.roundrobinlist.roundrobinlist)
- description and source-code
```javascript
function RoundRobinList(lst) {
  this.lst = lst.slice(0);
  this.index = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.nsqjs.roundrobinlist.prototype"></a>[module nsqjs.roundrobinlist.prototype](#apidoc.module.nsqjs.roundrobinlist.prototype)

#### <a name="apidoc.element.nsqjs.roundrobinlist.prototype.add"></a>[function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>add (item)](#apidoc.element.nsqjs.roundrobinlist.prototype.add)
- description and source-code
```javascript
add = function (item) {
  return this.lst.push(item);
}
```
- example usage
```shell
...
    return _this.raise('backoff');
  };
})(this));
return connectionRdy.on(ConnectionRdy.READY, (function(_this) {
  return function() {
    var ref;
    _this.connections.push(connectionRdy);
    _this.roundRobinConnections.add(connectionRdy);
    _this.balance();
    if (_this.current_state_name === 'ZERO') {
      return _this.goto('MAX');
    } else if ((ref = _this.current_state_name) === 'TRY_ONE' || ref === 'MAX') {
      return connectionRdy.bump();
    }
  };
...
```

#### <a name="apidoc.element.nsqjs.roundrobinlist.prototype.length"></a>[function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>length ()](#apidoc.element.nsqjs.roundrobinlist.prototype.length)
- description and source-code
```javascript
length = function () {
  return this.lst.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.roundrobinlist.prototype.next"></a>[function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>next (count)](#apidoc.element.nsqjs.roundrobinlist.prototype.next)
- description and source-code
```javascript
next = function (count) {
  var index;
  if (count == null) {
    count = 1;
  }
  index = this.index;
  this.index = (this.index + count) % this.lst.length;
  return this.lst.slice(index, index + count);
}
```
- example usage
```shell
...
perConnectionMax = Math.floor(max / this.connections.length);
if (perConnectionMax === 0) {
  ref = this.connections;
  for (i = 0, len = ref.length; i < len; i++) {
    c = ref[i];
    c.backoff();
  }
  ref1 = this.roundRobinConnections.next(max - this.inFlight());
  for (j = 0, len1 = ref1.length; j < len1; j++) {
    c = ref1[j];
    c.setConnectionRdyMax(1);
    c.bump();
  }
  return this.balanceId = setTimeout(this.balance.bind(this), this.lowRdyTimeout * 1000);
} else {
...
```

#### <a name="apidoc.element.nsqjs.roundrobinlist.prototype.remove"></a>[function <span class="apidocSignatureSpan">nsqjs.roundrobinlist.prototype.</span>remove (item)](#apidoc.element.nsqjs.roundrobinlist.prototype.remove)
- description and source-code
```javascript
remove = function (item) {
  var itemIndex;
  itemIndex = this.lst.indexOf(item);
  if (itemIndex === -1) {
    return;
  }
  if (this.index > itemIndex) {
    this.index -= 1;
  }
  return this.lst.splice(itemIndex, 1);
}
```
- example usage
```shell
...
      }
    };
  })(this));
};

ReaderRdy.prototype.removeConnection = function(conn) {
  this.connections.splice(this.connections.indexOf(conn), 1);
  this.roundRobinConnections.remove(conn);
  if (this.connections.length === 0) {
    return this.goto('ZERO');
  }
};

ReaderRdy.prototype.bump = function() {
  var conn, i, len, ref, results;
...
```



# <a name="apidoc.module.nsqjs.wire"></a>[module nsqjs.wire](#apidoc.module.nsqjs.wire)

#### <a name="apidoc.element.nsqjs.wire.auth"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>auth (token)](#apidoc.element.nsqjs.wire.auth)
- description and source-code
```javascript
auth = function (token) {
  return command('AUTH', token);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.finish"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>finish (id)](#apidoc.element.nsqjs.wire.finish)
- description and source-code
```javascript
finish = function (id) {
  if (!(Buffer.byteLength(id) <= 16)) {
    throw new Error("FINISH invalid id (" + id + ")");
  }
  return command('FIN', null, id);
}
```
- example usage
```shell
...
  lookupdHTTPAddresses: '127.0.0.1:4161'
});

reader.connect();

reader.on('message', function (msg) {
  console.log('Received message [%s]: %s', msg.id, msg.body.toString());
  msg.finish();
});
'''

#### CoffeeScript
'''coffee-script
nsq = require 'nsqjs'
...
```

#### <a name="apidoc.element.nsqjs.wire.identify"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>identify (data)](#apidoc.element.nsqjs.wire.identify)
- description and source-code
```javascript
identify = function (data) {
  var unexpectedKeys, validIdentifyKeys;
  validIdentifyKeys = ['client_id', 'deflate', 'deflate_level', 'feature_negotiation', 'heartbeat_interval', 'long_id', 'msg_timeout
', 'output_buffer_size', 'output_buffer_timeout', 'sample_rate', 'short_id', 'snappy', 'tls_v1', 'user_agent'];
  unexpectedKeys = _.filter(_.keys(data), function(k) {
    return indexOf.call(validIdentifyKeys, k) < 0;
  });
  if (unexpectedKeys.length) {
    throw new Error("Unexpected IDENTIFY keys: " + unexpectedKeys);
  }
  return command('IDENTIFY', JSON_stringify(data));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.mpub"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>mpub (topic, data)](#apidoc.element.nsqjs.wire.mpub)
- description and source-code
```javascript
mpub = function (topic, data) {
  var messages, numMessagesBuffer;
  if (!_.isArray(data)) {
    throw new Error("MPUB requires an array of message");
  }
  messages = _.map(data, function(message) {
    var buffer;
    buffer = new Buffer(4 + byteLength(message));
    buffer.writeInt32BE(byteLength(message), 0);
    if (_.isString(message)) {
      buffer.write(message, 4);
    } else {
      message.copy(buffer, 4, 0, buffer.length);
    }
    return buffer;
  });
  numMessagesBuffer = Buffer(4);
  numMessagesBuffer.writeInt32BE(messages.length, 0);
  messages.unshift(numMessagesBuffer);
  return command('MPUB', Buffer.concat(messages), topic);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.nop"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>nop ()](#apidoc.element.nsqjs.wire.nop)
- description and source-code
```javascript
nop = function () {
  return command('NOP', null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.pub"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>pub (topic, data)](#apidoc.element.nsqjs.wire.pub)
- description and source-code
```javascript
pub = function (topic, data) {
  return command('PUB', data, topic);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.ready"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>ready (count)](#apidoc.element.nsqjs.wire.ready)
- description and source-code
```javascript
ready = function (count) {
  if (!_.isNumber(count)) {
    throw new Error("RDY count (" + count + ") is not a number");
  }
  if (!(count >= 0)) {
    throw new Error("RDY count (" + count + ") is not positive");
  }
  return command('RDY', null, count.toString());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.requeue"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>requeue (id, timeMs)](#apidoc.element.nsqjs.wire.requeue)
- description and source-code
```javascript
requeue = function (id, timeMs) {
  var parameters;
  if (timeMs == null) {
    timeMs = 0;
  }
  if (!(Buffer.byteLength(id) <= 16)) {
    throw new Error("REQUEUE invalid id (" + id + ")");
  }
  if (!_.isNumber(timeMs)) {
    throw new Error("REQUEUE delay time is invalid (" + timeMs + ")");
  }
  parameters = ['REQ', null, id, timeMs];
  return command.apply(null, parameters);
}
```
- example usage
```shell
...
Message.prototype.requeue = function(delay, backoff) {
  if (delay == null) {
    delay = this.requeueDelay;
  }
  if (backoff == null) {
    backoff = true;
  }
  this.respond(Message.REQUEUE, wire.requeue(this.id, delay));
  if (backoff) {
    return this.emit(Message.BACKOFF);
  }
};

Message.prototype.touch = function() {
  this.touchCount += 1;
...
```

#### <a name="apidoc.element.nsqjs.wire.subscribe"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>subscribe (topic, channel)](#apidoc.element.nsqjs.wire.subscribe)
- description and source-code
```javascript
subscribe = function (topic, channel) {
  if (!validTopicName(topic)) {
    throw new Error("Invalid topic: " + topic);
  }
  if (!validChannelName(channel)) {
    throw new Error("Invalid channel: " + channel);
  }
  return command('SUB', null, topic, channel);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.nsqjs.wire.touch"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>touch (id)](#apidoc.element.nsqjs.wire.touch)
- description and source-code
```javascript
touch = function (id) {
  return command('TOUCH', null, id);
}
```
- example usage
```shell
...

reader.on('message', function (msg) {
console.log('Received message [%s]', msg.id);

function touch() {
  if (!msg.hasResponded) {
    console.log('Touch [%s]', msg.id);
    msg.touch();
    // Touch the message again a second before the next timeout.
    setTimeout(touch, msg.timeUntilTimeout() - 1000);
  }
}

function finish() {
  console.log('Finished message [%s]: %s', msg.id, msg.body.toString());
...
```

#### <a name="apidoc.element.nsqjs.wire.unpackMessage"></a>[function <span class="apidocSignatureSpan">nsqjs.wire.</span>unpackMessage (data)](#apidoc.element.nsqjs.wire.unpackMessage)
- description and source-code
```javascript
unpackMessage = function (data) {
  var attempts, body, id, timestamp;
  timestamp = (new Int64(data, 0)).toOctetString();
  timestamp = new BigNumber(timestamp, 16);
  attempts = data.readInt16BE(8);
  id = data.slice(10, 26).toString();
  body = data.slice(26);
  return [id, timestamp, attempts, body];
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
