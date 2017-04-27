# npmdoc-is

#### basic api documentation for  [is (v3.2.1)](https://github.com/enricomarino/is)  [![npm package](https://img.shields.io/npm/v/npmdoc-is.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-is) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-is.svg)](https://travis-ci.org/npmdoc/node-npmdoc-is)

#### the definitive JavaScript type testing library

[![NPM](https://nodei.co/npm/is.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/is)

- [https://npmdoc.github.io/node-npmdoc-is/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-is/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-is/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-is/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-is/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-is/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Enrico Marino",
        "url": "http://onirame.com"
    },
    "bugs": {
        "url": "https://github.com/enricomarino/is/issues"
    },
    "contributors": [
        {
            "name": "Jordan Harband",
            "url": "https://github.com/ljharb"
        }
    ],
    "dependencies": {},
    "description": "the definitive JavaScript type testing library",
    "devDependencies": {
        "@ljharb/eslint-config": "^11.0.0",
        "covert": "^1.1.0",
        "eslint": "^3.16.1",
        "foreach": "^2.0.5",
        "jscs": "^3.0.7",
        "make-generator-function": "^1.1.0",
        "safe-publish-latest": "^1.1.1",
        "tape": "^4.6.3"
    },
    "directories": {},
    "dist": {
        "shasum": "d0ac2ad55eb7b0bec926a5266f6c662aaa83dca5",
        "tarball": "https://registry.npmjs.org/is/-/is-3.2.1.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "f6952692d5b864da8db24267166fe2683e338581",
    "homepage": "https://github.com/enricomarino/is",
    "keywords": [
        "util",
        "type",
        "test"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "ljharb"
        },
        {
            "name": "enricomarino"
        }
    ],
    "name": "is",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/enricomarino/is.git"
    },
    "scripts": {
        "coverage": "covert test/index.js",
        "coverage-quiet": "covert test/index.js --quiet",
        "eslint": "eslint *.js */*.js",
        "jscs": "jscs *.js */*.js",
        "lint": "npm run jscs && npm run eslint",
        "prepublish": "safe-publish-latest",
        "pretest": "npm run lint",
        "test": "npm run --silent tests-only",
        "tests-only": "node test/index.js"
    },
    "testling": {
        "files": "test/index.js",
        "browsers": [
            "iexplore/6.0..latest",
            "firefox/3.0",
            "firefox/15.0..latest",
            "firefox/nightly",
            "chrome/4.0",
            "chrome/22.0..latest",
            "chrome/canary",
            "opera/10.0..latest",
            "opera/next",
            "safari/5.0.5..latest",
            "ipad/6.0..latest",
            "iphone/6.0..latest"
        ]
    },
    "version": "3.2.1",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
