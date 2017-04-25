# npmdoc-acl

#### basic api documentation for  [acl (v0.4.10)](https://github.com/optimalbits/node_acl)  [![npm package](https://img.shields.io/npm/v/npmdoc-acl.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-acl) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-acl.svg)](https://travis-ci.org/npmdoc/node-npmdoc-acl)

#### An Access Control List module, based on Redis with Express middleware support

[![NPM](https://nodei.co/npm/acl.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/acl)

- [https://npmdoc.github.io/node-npmdoc-acl/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-acl/build/apidoc.html)

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
    "version": "0.4.10",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
