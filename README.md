# api documentation for  [acl (v0.4.10)](https://github.com/optimalbits/node_acl)  [![npm package](https://img.shields.io/npm/v/npmdoc-acl.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-acl) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-acl.svg)](https://travis-ci.org/npmdoc/node-npmdoc-acl)
#### An Access Control List module, based on Redis with Express middleware support

[![NPM](https://nodei.co/npm/acl.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/acl)

[![apidoc](https://npmdoc.github.io/node-npmdoc-acl/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-acl/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-acl/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-acl/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Manuel Astudillo"
    },
    "bugs": {
        "url": "https://github.com/optimalbits/node_acl/issues"
    },
    "dependencies": {
        "async": "^2.1.4",
        "bluebird": "^3.0.2",
        "lodash": "^4.17.3",
        "mongodb": "^2.0.47",
        "redis": "^2.2.5"
    },
    "description": "An Access Control List module, based on Redis with Express middleware support",
    "devDependencies": {
        "chai": "^3.4.0",
        "mocha": "^3.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f7aa672421cd1ef7da74674577b2c6a9052cf9bd",
        "tarball": "https://registry.npmjs.org/acl/-/acl-0.4.10.tgz"
    },
    "engines": {
        "node": ">= 0.10"
    },
    "gitHead": "e69042e5c415830196f4872ee3b753ceb7adfa19",
    "homepage": "https://github.com/optimalbits/node_acl",
    "keywords": [
        "middleware",
        "acl",
        "web"
    ],
    "main": "./index.js",
    "maintainers": [
        {
            "name": "manast"
        }
    ],
    "name": "acl",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/optimalbits/node_acl.git"
    },
    "scripts": {
        "cover": "istanbul cover -- _mocha test/runner.js --reporter spec",
        "test": "mocha test/runner.js --reporter spec"
    },
    "version": "0.4.10"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module acl](#apidoc.module.acl)
1.  [function <span class="apidocSignatureSpan"></span>acl (backend, logger, options)](#apidoc.element.acl.acl)
1.  [function <span class="apidocSignatureSpan">acl.</span>memoryBackend ()](#apidoc.element.acl.memoryBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>mongodbBackend (db, prefix, useSingle)](#apidoc.element.acl.mongodbBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>redisBackend (redis, prefix)](#apidoc.element.acl.redisBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>toString ()](#apidoc.element.acl.toString)
1.  object <span class="apidocSignatureSpan">acl.</span>memoryBackend.prototype
1.  object <span class="apidocSignatureSpan">acl.</span>mongodbBackend.prototype
1.  object <span class="apidocSignatureSpan">acl.</span>redisBackend.prototype

#### [module acl.memoryBackend](#apidoc.module.acl.memoryBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>memoryBackend ()](#apidoc.element.acl.memoryBackend.memoryBackend)

#### [module acl.memoryBackend.prototype](#apidoc.module.acl.memoryBackend.prototype)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.memoryBackend.prototype.add)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>begin ()](#apidoc.element.acl.memoryBackend.prototype.begin)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>clean (cb)](#apidoc.element.acl.memoryBackend.prototype.clean)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.memoryBackend.prototype.del)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.memoryBackend.prototype.end)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.memoryBackend.prototype.get)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.memoryBackend.prototype.remove)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.memoryBackend.prototype.union)
1.  [function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>unions (buckets, keys, cb)](#apidoc.element.acl.memoryBackend.prototype.unions)

#### [module acl.mongodbBackend](#apidoc.module.acl.mongodbBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>mongodbBackend (db, prefix, useSingle)](#apidoc.element.acl.mongodbBackend.mongodbBackend)

#### [module acl.mongodbBackend.prototype](#apidoc.module.acl.mongodbBackend.prototype)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.mongodbBackend.prototype.add)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>begin ()](#apidoc.element.acl.mongodbBackend.prototype.begin)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>clean (cb)](#apidoc.element.acl.mongodbBackend.prototype.clean)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.mongodbBackend.prototype.del)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.mongodbBackend.prototype.end)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.mongodbBackend.prototype.get)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.mongodbBackend.prototype.remove)
1.  [function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.mongodbBackend.prototype.union)

#### [module acl.redisBackend](#apidoc.module.acl.redisBackend)
1.  [function <span class="apidocSignatureSpan">acl.</span>redisBackend (redis, prefix)](#apidoc.element.acl.redisBackend.redisBackend)

#### [module acl.redisBackend.prototype](#apidoc.module.acl.redisBackend.prototype)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.redisBackend.prototype.add)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>begin ()](#apidoc.element.acl.redisBackend.prototype.begin)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>bucketKey (bucket, keys)](#apidoc.element.acl.redisBackend.prototype.bucketKey)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>clean (cb)](#apidoc.element.acl.redisBackend.prototype.clean)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.redisBackend.prototype.del)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.redisBackend.prototype.end)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.redisBackend.prototype.get)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.redisBackend.prototype.remove)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.redisBackend.prototype.union)
1.  [function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>unions (buckets, keys, cb)](#apidoc.element.acl.redisBackend.prototype.unions)



# <a name="apidoc.module.acl"></a>[module acl](#apidoc.module.acl)

#### <a name="apidoc.element.acl.acl"></a>[function <span class="apidocSignatureSpan"></span>acl (backend, logger, options)](#apidoc.element.acl.acl)
- description and source-code
```javascript
acl = function (backend, logger, options){
  contract(arguments)
    .params('object')
    .params('object','object')
    .params('object','object', 'object')
    .end();

  options = _.extend({
    buckets: {
      meta: 'meta',
      parents: 'parents',
      permissions: 'permissions',
      resources: 'resources',
      roles: 'roles',
      users: 'users'
    }
  }, options);

  this.logger = logger;
  this.backend = backend;
  this.options = options;

  // Promisify async methods
  backend.endAsync = bluebird.promisify(backend.end);
  backend.getAsync = bluebird.promisify(backend.get);
  backend.cleanAsync = bluebird.promisify(backend.clean);
  backend.unionAsync = bluebird.promisify(backend.union);
  if (backend.unions) {
    backend.unionsAsync = bluebird.promisify(backend.unions);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>memoryBackend ()](#apidoc.element.acl.memoryBackend)
- description and source-code
```javascript
function MemoryBackend(){
  this._buckets = {};
}
```
- example usage
```shell
...
'''javascript
var acl = require('acl');

// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''

All the following functions return a promise or optionally take a callback with
an err parameter as last parameter. We omit them in the examples for simplicity.
...
```

#### <a name="apidoc.element.acl.mongodbBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>mongodbBackend (db, prefix, useSingle)](#apidoc.element.acl.mongodbBackend)
- description and source-code
```javascript
function MongoDBBackend(db, prefix, useSingle){
  this.db = db;
  this.prefix = typeof prefix !== 'undefined' ? prefix : '';
  this.useSingle = (typeof useSingle !== 'undefined') ? useSingle : false;
}
```
- example usage
```shell
...
// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''

All the following functions return a promise or optionally take a callback with
an err parameter as last parameter. We omit them in the examples for simplicity.

Create roles implicitly by giving them permissions:
...
```

#### <a name="apidoc.element.acl.redisBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>redisBackend (redis, prefix)](#apidoc.element.acl.redisBackend)
- description and source-code
```javascript
function RedisBackend(redis, prefix){
  this.redis = redis;
  this.prefix = prefix || 'acl';
}
```
- example usage
```shell
...

Create your acl module by requiring it and instantiating it with a valid backend instance:

'''javascript
var acl = require('acl');

// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''
...
```

#### <a name="apidoc.element.acl.toString"></a>[function <span class="apidocSignatureSpan">acl.</span>toString ()](#apidoc.element.acl.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.acl.memoryBackend"></a>[module acl.memoryBackend](#apidoc.module.acl.memoryBackend)

#### <a name="apidoc.element.acl.memoryBackend.memoryBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>memoryBackend ()](#apidoc.element.acl.memoryBackend.memoryBackend)
- description and source-code
```javascript
function MemoryBackend(){
  this._buckets = {};
}
```
- example usage
```shell
...
'''javascript
var acl = require('acl');

// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''

All the following functions return a promise or optionally take a callback with
an err parameter as last parameter. We omit them in the examples for simplicity.
...
```



# <a name="apidoc.module.acl.memoryBackend.prototype"></a>[module acl.memoryBackend.prototype](#apidoc.module.acl.memoryBackend.prototype)

#### <a name="apidoc.element.acl.memoryBackend.prototype.add"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.memoryBackend.prototype.add)
- description and source-code
```javascript
add = function (transaction, bucket, key, values){
  contract(arguments)
      .params('array', 'string', 'string|number', 'string|array|number')
      .end();

  var self = this;
  values = makeArray(values);

  transaction.push(function(){
    if(!self._buckets[bucket]){
      self._buckets[bucket] = {};
    }
    if(!self._buckets[bucket][key]){
      self._buckets[bucket][key] = values;
    }else{
      self._buckets[bucket][key] = _.union(values, self._buckets[bucket][key]);
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.begin"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>begin ()](#apidoc.element.acl.memoryBackend.prototype.begin)
- description and source-code
```javascript
begin = function (){
  // returns a transaction object(just an array of functions will do here.)
  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.clean"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>clean (cb)](#apidoc.element.acl.memoryBackend.prototype.clean)
- description and source-code
```javascript
clean = function (cb){
  contract(arguments).params('function').end();
  this._buckets = {};
  cb();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.del"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.memoryBackend.prototype.del)
- description and source-code
```javascript
del = function (transaction, bucket, keys){
  contract(arguments)
      .params('array', 'string', 'string|array')
      .end();

  var self = this;
  keys = makeArray(keys);

  transaction.push(function(){
    if(self._buckets[bucket]){
      for(var i=0, len=keys.length;i<len;i++){
        delete self._buckets[bucket][keys[i]];
      }
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.end"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.memoryBackend.prototype.end)
- description and source-code
```javascript
end = function (transaction, cb){
  contract(arguments).params('array', 'function').end();

  // Execute transaction
  for(var i=0, len=transaction.length;i<len;i++){
    transaction[i]();
  }
  cb();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.get"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.memoryBackend.prototype.get)
- description and source-code
```javascript
get = function (bucket, key, cb){
  contract(arguments)
      .params('string', 'string|number', 'function')
      .end();

  if(this._buckets[bucket]){
    cb(null, this._buckets[bucket][key] || []);
  }else{
    cb(null, []);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.remove"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.memoryBackend.prototype.remove)
- description and source-code
```javascript
remove = function (transaction, bucket, key, values){
  contract(arguments)
      .params('array', 'string', 'string|number','string|array|number')
      .end();

  var self = this;
  values = makeArray(values);
  transaction.push(function(){
    var old;
    if(self._buckets[bucket] && (old = self._buckets[bucket][key])){
      self._buckets[bucket][key] = _.difference(old, values);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.union"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.memoryBackend.prototype.union)
- description and source-code
```javascript
union = function (bucket, keys, cb){
  contract(arguments)
    .params('string', 'array', 'function')
    .end();

  var match;
  var re;
  if (!this._buckets[bucket]) {
    Object.keys(this._buckets).some(function(b) {
      re = new RegExp("^"+b+"$");
      match = re.test(bucket);
      if (match) bucket = b;
      return match;
    });
  }

  if(this._buckets[bucket]){
    var keyArrays = [];
    for(var i=0,len=keys.length;i<len;i++){
      if(this._buckets[bucket][keys[i]]){
        keyArrays.push.apply(keyArrays, this._buckets[bucket][keys[i]]);
      }
    }
    cb(undefined, _.union(keyArrays));
  }else{
    cb(undefined, []);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.memoryBackend.prototype.unions"></a>[function <span class="apidocSignatureSpan">acl.memoryBackend.prototype.</span>unions (buckets, keys, cb)](#apidoc.element.acl.memoryBackend.prototype.unions)
- description and source-code
```javascript
unions = function (buckets, keys, cb){
  contract(arguments)
      .params('array', 'array', 'function')
      .end();

  var self = this;
  var results = {};

  buckets.forEach(function(bucket) {
    if(self._buckets[bucket]){
      results[bucket] = _.uniq(_.flatten(_.values(_.pick(self._buckets[bucket], keys))));
    }else{
      results[bucket] = [];
    }
  });

  cb(null, results);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.acl.mongodbBackend"></a>[module acl.mongodbBackend](#apidoc.module.acl.mongodbBackend)

#### <a name="apidoc.element.acl.mongodbBackend.mongodbBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>mongodbBackend (db, prefix, useSingle)](#apidoc.element.acl.mongodbBackend.mongodbBackend)
- description and source-code
```javascript
function MongoDBBackend(db, prefix, useSingle){
  this.db = db;
  this.prefix = typeof prefix !== 'undefined' ? prefix : '';
  this.useSingle = (typeof useSingle !== 'undefined') ? useSingle : false;
}
```
- example usage
```shell
...
// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''

All the following functions return a promise or optionally take a callback with
an err parameter as last parameter. We omit them in the examples for simplicity.

Create roles implicitly by giving them permissions:
...
```



# <a name="apidoc.module.acl.mongodbBackend.prototype"></a>[module acl.mongodbBackend.prototype](#apidoc.module.acl.mongodbBackend.prototype)

#### <a name="apidoc.element.acl.mongodbBackend.prototype.add"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.mongodbBackend.prototype.add)
- description and source-code
```javascript
add = function (transaction, bucket, key, values){
  contract(arguments)
      .params('array', 'string', 'string|number','string|array|number')
      .end();

  if(key=="key") throw new Error("Key name 'key' is not allowed.");
  key = encodeText(key);
  var self=this;
  var updateParams = (self.useSingle? {_bucketname: bucket, key:key} : {key:key});
  var collName = (self.useSingle? aclCollectionName : bucket);

  transaction.push(function(cb){
    values = makeArray(values);
    self.db.collection(self.prefix + collName, function(err,collection){
      if(err instanceof Error) return cb(err);

      // build doc from array values
      var doc = {};
      values.forEach(function(value){doc[value]=true;});

      // update document
      collection.update(updateParams,{$set:doc},{safe:true,upsert:true},function(err){
        if(err instanceof Error) return cb(err);
        cb(undefined);
      });
    });
  });

  transaction.push(function(cb) {
    self.db.collection(self.prefix + collName, function(err,collection){
      // Create index
      collection.ensureIndex({_bucketname: 1, key: 1}, function(err){
        if (err instanceof Error) {
          return cb(err);
        } else{
          cb(undefined);
        }
      });
    });
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.begin"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>begin ()](#apidoc.element.acl.mongodbBackend.prototype.begin)
- description and source-code
```javascript
begin = function (){
  // returns a transaction object(just an array of functions will do here.)
  return [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.clean"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>clean (cb)](#apidoc.element.acl.mongodbBackend.prototype.clean)
- description and source-code
```javascript
clean = function (cb){
  contract(arguments).params('function').end();
  this.db.collections(function(err, collections) {
    if (err instanceof Error) return cb(err);
    async.forEach(collections,function(coll,innercb){
      coll.drop(function(){innercb()}); // ignores errors
    },cb);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.del"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.mongodbBackend.prototype.del)
- description and source-code
```javascript
del = function (transaction, bucket, keys){
  contract(arguments)
      .params('array', 'string', 'string|array')
      .end();
  keys = makeArray(keys);
  var self= this;
  var updateParams = (self.useSingle? {_bucketname: bucket, key:{$in:keys}} : {key:{$in:keys}});
  var collName = (self.useSingle? aclCollectionName : bucket);

  transaction.push(function(cb){
    self.db.collection(self.prefix + collName,function(err,collection){
      if(err instanceof Error) return cb(err);
      collection.remove(updateParams,{safe:true},function(err){
        if(err instanceof Error) return cb(err);
        cb(undefined);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.end"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.mongodbBackend.prototype.end)
- description and source-code
```javascript
end = function (transaction, cb){
  contract(arguments).params('array', 'function').end();
  async.series(transaction,function(err){
    cb(err instanceof Error? err : undefined);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.get"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.mongodbBackend.prototype.get)
- description and source-code
```javascript
get = function (bucket, key, cb){
  contract(arguments)
      .params('string', 'string|number', 'function')
      .end();
  key = encodeText(key);
  var searchParams = (this.useSingle? {_bucketname: bucket, key:key} : {key:key});
  var collName = (this.useSingle? aclCollectionName : bucket);

  this.db.collection(this.prefix + collName,function(err,collection){
    if(err instanceof Error) return cb(err);
    // Excluding bucket field from search result
    collection.findOne(searchParams, {_bucketname: 0},function(err, doc){
      if(err) return cb(err);
      if(! _.isObject(doc) ) return cb(undefined,[]);
      doc = fixKeys(doc);
      cb(undefined,_.without(_.keys(doc),"key","_id"));
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.remove"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.mongodbBackend.prototype.remove)
- description and source-code
```javascript
remove = function (transaction, bucket, key, values){
  contract(arguments)
      .params('array', 'string', 'string|number','string|array|number')
      .end();
  key = encodeText(key);
  var self=this;
  var updateParams = (self.useSingle? {_bucketname: bucket, key:key} : {key:key});
  var collName = (self.useSingle? aclCollectionName : bucket);

  values = makeArray(values);
  transaction.push(function(cb){
    self.db.collection(self.prefix + collName,function(err,collection){
      if(err instanceof Error) return cb(err);

      // build doc from array values
      var doc = {};
      values.forEach(function(value){doc[value]=true;});

      // update document
      collection.update(updateParams,{$unset:doc},{safe:true,upsert:true},function(err){
        if(err instanceof Error) return cb(err);
        cb(undefined);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.mongodbBackend.prototype.union"></a>[function <span class="apidocSignatureSpan">acl.mongodbBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.mongodbBackend.prototype.union)
- description and source-code
```javascript
union = function (bucket, keys, cb){
  contract(arguments)
    .params('string', 'array', 'function')
    .end();
  keys = encodeAll(keys);
  var searchParams = (this.useSingle? {_bucketname: bucket, key: { $in: keys }} : {key: { $in: keys }});
  var collName = (this.useSingle? aclCollectionName : bucket);

  this.db.collection(this.prefix + collName,function(err,collection){
    if(err instanceof Error) return cb(err);
    // Excluding bucket field from search result
    collection.find(searchParams, {_bucketname: 0}).toArray(function(err,docs){
      if(err instanceof Error) return cb(err);
      if( ! docs.length ) return cb(undefined, []);
      var keyArrays = [];
      docs = fixAllKeys(docs);
      docs.forEach(function(doc){
        keyArrays.push.apply(keyArrays, _.keys(doc));
      });
      cb(undefined, _.without(_.union(keyArrays),"key","_id"));
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.acl.redisBackend"></a>[module acl.redisBackend](#apidoc.module.acl.redisBackend)

#### <a name="apidoc.element.acl.redisBackend.redisBackend"></a>[function <span class="apidocSignatureSpan">acl.</span>redisBackend (redis, prefix)](#apidoc.element.acl.redisBackend.redisBackend)
- description and source-code
```javascript
function RedisBackend(redis, prefix){
  this.redis = redis;
  this.prefix = prefix || 'acl';
}
```
- example usage
```shell
...

Create your acl module by requiring it and instantiating it with a valid backend instance:

'''javascript
var acl = require('acl');

// Using redis backend
acl = new acl(new acl.redisBackend(redisClient, prefix));

// Or Using the memory backend
acl = new acl(new acl.memoryBackend());

// Or Using the mongodb backend
acl = new acl(new acl.mongodbBackend(dbInstance, prefix));
'''
...
```



# <a name="apidoc.module.acl.redisBackend.prototype"></a>[module acl.redisBackend.prototype](#apidoc.module.acl.redisBackend.prototype)

#### <a name="apidoc.element.acl.redisBackend.prototype.add"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>add (transaction, bucket, key, values)](#apidoc.element.acl.redisBackend.prototype.add)
- description and source-code
```javascript
add = function (transaction, bucket, key, values){
		contract(arguments)
	      .params('object', 'string', 'string|number','string|array|number')
        .end();

    key = this.bucketKey(bucket, key);

    if (Array.isArray(values)){
      values.forEach(function(value){
        transaction.sadd(key, value);
      });
    }else{
      transaction.sadd(key, values);
    }
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.begin"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>begin ()](#apidoc.element.acl.redisBackend.prototype.begin)
- description and source-code
```javascript
begin = function (){
  return this.redis.multi();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.bucketKey"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>bucketKey (bucket, keys)](#apidoc.element.acl.redisBackend.prototype.bucketKey)
- description and source-code
```javascript
bucketKey = function (bucket, keys){
  var self = this;
  if(Array.isArray(keys)){
    return keys.map(function(key){
      return self.prefix+'_'+bucket+'@'+key;
    });
  }else{
    return self.prefix+'_'+bucket+'@'+keys;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.clean"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>clean (cb)](#apidoc.element.acl.redisBackend.prototype.clean)
- description and source-code
```javascript
clean = function (cb){
  contract(arguments).params('function').end();
  var self = this;
  self.redis.keys(self.prefix+'*', function(err, keys){
    if(keys.length){
      self.redis.del(keys, function(){cb()});
    }else{
      cb();
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.del"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>del (transaction, bucket, keys)](#apidoc.element.acl.redisBackend.prototype.del)
- description and source-code
```javascript
del = function (transaction, bucket, keys){
		contract(arguments)
	      .params('object', 'string', 'string|array')
	      .end();

  var self = this;

  keys = Array.isArray(keys) ? keys : [keys]

  keys = keys.map(function(key){
    return self.bucketKey(bucket, key);
  });

  transaction.del(keys);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.end"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>end (transaction, cb)](#apidoc.element.acl.redisBackend.prototype.end)
- description and source-code
```javascript
end = function (transaction, cb){
		contract(arguments).params('object', 'function').end();
  transaction.exec(function(){cb()});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.get"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>get (bucket, key, cb)](#apidoc.element.acl.redisBackend.prototype.get)
- description and source-code
```javascript
get = function (bucket, key, cb){
		contract(arguments)
	      .params('string', 'string|number', 'function')
	      .end();

  key = this.bucketKey(bucket, key);

  this.redis.smembers(key, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.remove"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>remove (transaction, bucket, key, values)](#apidoc.element.acl.redisBackend.prototype.remove)
- description and source-code
```javascript
remove = function (transaction, bucket, key, values){
		contract(arguments)
	      .params('object', 'string', 'string|number','string|array|number')
      .end();

  key = this.bucketKey(bucket, key);

  if (Array.isArray(values)){
    values.forEach(function(value){
      transaction.srem(key, value);
    });
  }else{
    transaction.srem(key, values);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.union"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>union (bucket, keys, cb)](#apidoc.element.acl.redisBackend.prototype.union)
- description and source-code
```javascript
union = function (bucket, keys, cb){
		contract(arguments)
	      .params('string', 'array', 'function')
	      .end();

    keys = this.bucketKey(bucket, keys);
    this.redis.sunion(keys, cb);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.acl.redisBackend.prototype.unions"></a>[function <span class="apidocSignatureSpan">acl.redisBackend.prototype.</span>unions (buckets, keys, cb)](#apidoc.element.acl.redisBackend.prototype.unions)
- description and source-code
```javascript
unions = function (buckets, keys, cb){
  contract(arguments)
    .params('array', 'array', 'function')
    .end();

  var redisKeys = {};
  var batch = this.redis.batch();
  var self = this;

  buckets.forEach(function(bucket) {
    redisKeys[bucket] = self.bucketKey(bucket, keys);
    batch.sunion(redisKeys[bucket], noop);
  });

  batch.exec(function(err, replies) {
    if (!Array.isArray(replies)) {
      return {};
    }

    var result = {};
    replies.forEach(function(reply, index) {
      if (reply instanceof Error) {
        throw reply;
      }

      result[buckets[index]] = reply;
    });
    cb(err, result);
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
