# api documentation for  [is (v3.2.1)](https://github.com/enricomarino/is)  [![npm package](https://img.shields.io/npm/v/npmdoc-is.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-is) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-is.svg)](https://travis-ci.org/npmdoc/node-npmdoc-is)
#### the definitive JavaScript type testing library

[![NPM](https://nodei.co/npm/is.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/is)

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
    "version": "3.2.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module is](#apidoc.module.is)
1.  [function <span class="apidocSignatureSpan">is.</span>a (value, type)](#apidoc.element.is.a)
1.  [function <span class="apidocSignatureSpan">is.</span>args (value)](#apidoc.element.is.args)
1.  [function <span class="apidocSignatureSpan">is.</span>arguments (value)](#apidoc.element.is.arguments)
1.  [function <span class="apidocSignatureSpan">is.</span>array ()](#apidoc.element.is.array)
1.  [function <span class="apidocSignatureSpan">is.</span>arraylike (value)](#apidoc.element.is.arraylike)
1.  [function <span class="apidocSignatureSpan">is.</span>base64 (value)](#apidoc.element.is.base64)
1.  [function <span class="apidocSignatureSpan">is.</span>bool (value)](#apidoc.element.is.bool)
1.  [function <span class="apidocSignatureSpan">is.</span>boolean (value)](#apidoc.element.is.boolean)
1.  [function <span class="apidocSignatureSpan">is.</span>date (value)](#apidoc.element.is.date)
1.  [function <span class="apidocSignatureSpan">is.</span>decimal (value)](#apidoc.element.is.decimal)
1.  [function <span class="apidocSignatureSpan">is.</span>defined (value)](#apidoc.element.is.defined)
1.  [function <span class="apidocSignatureSpan">is.</span>divisibleBy (value, n)](#apidoc.element.is.divisibleBy)
1.  [function <span class="apidocSignatureSpan">is.</span>element (value)](#apidoc.element.is.element)
1.  [function <span class="apidocSignatureSpan">is.</span>empty (value)](#apidoc.element.is.empty)
1.  [function <span class="apidocSignatureSpan">is.</span>equal (value, other)](#apidoc.element.is.equal)
1.  [function <span class="apidocSignatureSpan">is.</span>error (value)](#apidoc.element.is.error)
1.  [function <span class="apidocSignatureSpan">is.</span>even (value)](#apidoc.element.is.even)
1.  [function <span class="apidocSignatureSpan">is.</span>false (value)](#apidoc.element.is.false)
1.  [function <span class="apidocSignatureSpan">is.</span>fn (value)](#apidoc.element.is.fn)
1.  [function <span class="apidocSignatureSpan">is.</span>function (value)](#apidoc.element.is.function)
1.  [function <span class="apidocSignatureSpan">is.</span>ge (value, other)](#apidoc.element.is.ge)
1.  [function <span class="apidocSignatureSpan">is.</span>gt (value, other)](#apidoc.element.is.gt)
1.  [function <span class="apidocSignatureSpan">is.</span>hash (value)](#apidoc.element.is.hash)
1.  [function <span class="apidocSignatureSpan">is.</span>hex (value)](#apidoc.element.is.hex)
1.  [function <span class="apidocSignatureSpan">is.</span>hosted (value, host)](#apidoc.element.is.hosted)
1.  [function <span class="apidocSignatureSpan">is.</span>infinite (value)](#apidoc.element.is.infinite)
1.  [function <span class="apidocSignatureSpan">is.</span>instance (value, constructor)](#apidoc.element.is.instance)
1.  [function <span class="apidocSignatureSpan">is.</span>instanceof (value, constructor)](#apidoc.element.is.instanceof)
1.  [function <span class="apidocSignatureSpan">is.</span>int (value)](#apidoc.element.is.int)
1.  [function <span class="apidocSignatureSpan">is.</span>integer (value)](#apidoc.element.is.integer)
1.  [function <span class="apidocSignatureSpan">is.</span>le (value, other)](#apidoc.element.is.le)
1.  [function <span class="apidocSignatureSpan">is.</span>lt (value, other)](#apidoc.element.is.lt)
1.  [function <span class="apidocSignatureSpan">is.</span>maximum (value, others)](#apidoc.element.is.maximum)
1.  [function <span class="apidocSignatureSpan">is.</span>minimum (value, others)](#apidoc.element.is.minimum)
1.  [function <span class="apidocSignatureSpan">is.</span>nan (value)](#apidoc.element.is.nan)
1.  [function <span class="apidocSignatureSpan">is.</span>nil (value)](#apidoc.element.is.nil)
1.  [function <span class="apidocSignatureSpan">is.</span>null (value)](#apidoc.element.is.null)
1.  [function <span class="apidocSignatureSpan">is.</span>number (value)](#apidoc.element.is.number)
1.  [function <span class="apidocSignatureSpan">is.</span>object (value)](#apidoc.element.is.object)
1.  [function <span class="apidocSignatureSpan">is.</span>odd (value)](#apidoc.element.is.odd)
1.  [function <span class="apidocSignatureSpan">is.</span>primitive (value)](#apidoc.element.is.primitive)
1.  [function <span class="apidocSignatureSpan">is.</span>regexp (value)](#apidoc.element.is.regexp)
1.  [function <span class="apidocSignatureSpan">is.</span>string (value)](#apidoc.element.is.string)
1.  [function <span class="apidocSignatureSpan">is.</span>symbol (value)](#apidoc.element.is.symbol)
1.  [function <span class="apidocSignatureSpan">is.</span>true (value)](#apidoc.element.is.true)
1.  [function <span class="apidocSignatureSpan">is.</span>type (value, type)](#apidoc.element.is.type)
1.  [function <span class="apidocSignatureSpan">is.</span>undef (value)](#apidoc.element.is.undef)
1.  [function <span class="apidocSignatureSpan">is.</span>undefined (value)](#apidoc.element.is.undefined)
1.  [function <span class="apidocSignatureSpan">is.</span>within (value, start, finish)](#apidoc.element.is.within)

#### [module is.arguments](#apidoc.module.is.arguments)
1.  [function <span class="apidocSignatureSpan">is.arguments.</span>empty (value)](#apidoc.element.is.arguments.empty)

#### [module is.array](#apidoc.module.is.array)
1.  [function <span class="apidocSignatureSpan">is.</span>array ()](#apidoc.element.is.array.array)
1.  [function <span class="apidocSignatureSpan">is.array.</span>empty (value)](#apidoc.element.is.array.empty)

#### [module is.date](#apidoc.module.is.date)
1.  [function <span class="apidocSignatureSpan">is.</span>date (value)](#apidoc.element.is.date.date)
1.  [function <span class="apidocSignatureSpan">is.date.</span>valid (value)](#apidoc.element.is.date.valid)



# <a name="apidoc.module.is"></a>[module is](#apidoc.module.is)

#### <a name="apidoc.element.is.a"></a>[function <span class="apidocSignatureSpan">is.</span>a (value, type)](#apidoc.element.is.a)
- description and source-code
```javascript
a = function (value, type) {
  return typeof value === type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.args"></a>[function <span class="apidocSignatureSpan">is.</span>args (value)](#apidoc.element.is.args)
- description and source-code
```javascript
args = function (value) {
  var isStandardArguments = toStr.call(value) === '[object Arguments]';
  var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
  return isStandardArguments || isOldArguments;
}
```
- example usage
```shell
...
* Test if 'value' is an empty arguments object.
*
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an empty arguments object, false otherwise
* @api public
*/
is.args.empty = function (value) {
 return is.args(value) && value.length === 0;
};

/**
* is.array.empty
* Test if 'value' is an empty array.
*
* @param {Mixed} value value to test
...
```

#### <a name="apidoc.element.is.arguments"></a>[function <span class="apidocSignatureSpan">is.</span>arguments (value)](#apidoc.element.is.arguments)
- description and source-code
```javascript
arguments = function (value) {
  var isStandardArguments = toStr.call(value) === '[object Arguments]';
  var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
  return isStandardArguments || isOldArguments;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.array"></a>[function <span class="apidocSignatureSpan">is.</span>array ()](#apidoc.element.is.array)
- description and source-code
```javascript
function isArray() { [native code] }
```
- example usage
```shell
...
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an arguments object, false otherwise
* @api public
*/

is.args = is.arguments = function (value) {
 var isStandardArguments = toStr.call(value) === '[object Arguments]';
 var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
 return isStandardArguments || isOldArguments;
};

/**
* Test array.
*/
...
```

#### <a name="apidoc.element.is.arraylike"></a>[function <span class="apidocSignatureSpan">is.</span>arraylike (value)](#apidoc.element.is.arraylike)
- description and source-code
```javascript
arraylike = function (value) {
  return !!value && !is.bool(value)
    && owns.call(value, 'length')
    && isFinite(value.length)
    && is.number(value.length)
    && value.length >= 0;
}
```
- example usage
```shell
...
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an arguments object, false otherwise
* @api public
*/

is.args = is.arguments = function (value) {
 var isStandardArguments = toStr.call(value) === '[object Arguments]';
 var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
 return isStandardArguments || isOldArguments;
};

/**
* Test array.
*/
...
```

#### <a name="apidoc.element.is.base64"></a>[function <span class="apidocSignatureSpan">is.</span>base64 (value)](#apidoc.element.is.base64)
- description and source-code
```javascript
base64 = function (value) {
  return is.string(value) && (!value.length || base64Regex.test(value));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.bool"></a>[function <span class="apidocSignatureSpan">is.</span>bool (value)](#apidoc.element.is.bool)
- description and source-code
```javascript
bool = function (value) {
  return toStr.call(value) === '[object Boolean]';
}
```
- example usage
```shell
...
 *
 * @param {Mixed} value value to test
 * @return {Boolean} true if 'value' is an arguments object, false otherwise
 * @api public
 */

is.arraylike = function (value) {
  return !!value && !is.bool(value)
    && owns.call(value, 'length')
    && isFinite(value.length)
    && is.number(value.length)
    && value.length >= 0;
};

/**
...
```

#### <a name="apidoc.element.is.boolean"></a>[function <span class="apidocSignatureSpan">is.</span>boolean (value)](#apidoc.element.is.boolean)
- description and source-code
```javascript
boolean = function (value) {
  return toStr.call(value) === '[object Boolean]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.date"></a>[function <span class="apidocSignatureSpan">is.</span>date (value)](#apidoc.element.is.date)
- description and source-code
```javascript
date = function (value) {
  return toStr.call(value) === '[object Date]';
}
```
- example usage
```shell
...
 * is.date.valid
 * Test if 'value' is a valid date.
 *
 * @param {Mixed} value value to test
 * @returns {Boolean} true if 'value' is a valid date, false otherwise
 */
is.date.valid = function (value) {
  return is.date(value) && !isNaN(Number(value));
};

/**
 * Test element.
 */

/**
...
```

#### <a name="apidoc.element.is.decimal"></a>[function <span class="apidocSignatureSpan">is.</span>decimal (value)](#apidoc.element.is.decimal)
- description and source-code
```javascript
decimal = function (value) {
  return is.number(value) && !isActualNaN(value) && !is.infinite(value) && value % 1 !== 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.defined"></a>[function <span class="apidocSignatureSpan">is.</span>defined (value)](#apidoc.element.is.defined)
- description and source-code
```javascript
defined = function (value) {
  return typeof value !== 'undefined';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.divisibleBy"></a>[function <span class="apidocSignatureSpan">is.</span>divisibleBy (value, n)](#apidoc.element.is.divisibleBy)
- description and source-code
```javascript
divisibleBy = function (value, n) {
  var isDividendInfinite = is.infinite(value);
  var isDivisorInfinite = is.infinite(n);
  var isNonZeroNumber = is.number(value) && !isActualNaN(value) && is.number(n) && !isActualNaN(n) && n !== 0;
  return isDividendInfinite || isDivisorInfinite || (isNonZeroNumber && value % n === 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.element"></a>[function <span class="apidocSignatureSpan">is.</span>element (value)](#apidoc.element.is.element)
- description and source-code
```javascript
element = function (value) {
  return value !== undefined
    && typeof HTMLElement !== 'undefined'
    && value instanceof HTMLElement
    && value.nodeType === 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.empty"></a>[function <span class="apidocSignatureSpan">is.</span>empty (value)](#apidoc.element.is.empty)
- description and source-code
```javascript
empty = function (value) {
  var type = toStr.call(value);
  var key;

  if (type === '[object Array]' || type === '[object Arguments]' || type === '[object String]') {
    return value.length === 0;
  }

  if (type === '[object Object]') {
    for (key in value) {
      if (owns.call(value, key)) {
        return false;
      }
    }
    return true;
  }

  return !value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.equal"></a>[function <span class="apidocSignatureSpan">is.</span>equal (value, other)](#apidoc.element.is.equal)
- description and source-code
```javascript
function equal(value, other) {
  if (value === other) {
    return true;
  }

  var type = toStr.call(value);
  var key;

  if (type !== toStr.call(other)) {
    return false;
  }

  if (type === '[object Object]') {
    for (key in value) {
      if (!is.equal(value[key], other[key]) || !(key in other)) {
        return false;
      }
    }
    for (key in other) {
      if (!is.equal(value[key], other[key]) || !(key in value)) {
        return false;
      }
    }
    return true;
  }

  if (type === '[object Array]') {
    key = value.length;
    if (key !== other.length) {
      return false;
    }
    while (key--) {
      if (!is.equal(value[key], other[key])) {
        return false;
      }
    }
    return true;
  }

  if (type === '[object Function]') {
    return value.prototype === other.prototype;
  }

  if (type === '[object Date]') {
    return value.getTime() === other.getTime();
  }

  return false;
}
```
- example usage
```shell
...

if (type !== toStr.call(other)) {
  return false;
}

if (type === '[object Object]') {
  for (key in value) {
    if (!is.equal(value[key], other[key]) || !(key in other)) {
      return false;
    }
  }
  for (key in other) {
    if (!is.equal(value[key], other[key]) || !(key in value)) {
      return false;
    }
...
```

#### <a name="apidoc.element.is.error"></a>[function <span class="apidocSignatureSpan">is.</span>error (value)](#apidoc.element.is.error)
- description and source-code
```javascript
error = function (value) {
  return toStr.call(value) === '[object Error]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.even"></a>[function <span class="apidocSignatureSpan">is.</span>even (value)](#apidoc.element.is.even)
- description and source-code
```javascript
even = function (value) {
  return is.infinite(value) || (is.number(value) && value === value && value % 2 === 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.false"></a>[function <span class="apidocSignatureSpan">is.</span>false (value)](#apidoc.element.is.false)
- description and source-code
```javascript
false = function (value) {
  return is.bool(value) && Boolean(Number(value)) === false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.fn"></a>[function <span class="apidocSignatureSpan">is.</span>fn (value)](#apidoc.element.is.fn)
- description and source-code
```javascript
fn = function (value) {
  var isAlert = typeof window !== 'undefined' && value === window.alert;
  if (isAlert) {
    return true;
  }
  var str = toStr.call(value);
  return str === '[object Function]' || str === '[object GeneratorFunction]' || str === '[object AsyncFunction]';
}
```
- example usage
```shell
...
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an arguments object, false otherwise
* @api public
*/

is.args = is.arguments = function (value) {
 var isStandardArguments = toStr.call(value) === '[object Arguments]';
 var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
 return isStandardArguments || isOldArguments;
};

/**
* Test array.
*/
...
```

#### <a name="apidoc.element.is.function"></a>[function <span class="apidocSignatureSpan">is.</span>function (value)](#apidoc.element.is.function)
- description and source-code
```javascript
function = function (value) {
  var isAlert = typeof window !== 'undefined' && value === window.alert;
  if (isAlert) {
    return true;
  }
  var str = toStr.call(value);
  return str === '[object Function]' || str === '[object GeneratorFunction]' || str === '[object AsyncFunction]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.ge"></a>[function <span class="apidocSignatureSpan">is.</span>ge (value, other)](#apidoc.element.is.ge)
- description and source-code
```javascript
ge = function (value, other) {
  if (isActualNaN(value) || isActualNaN(other)) {
    throw new TypeError('NaN is not a valid value');
  }
  return !is.infinite(value) && !is.infinite(other) && value >= other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.gt"></a>[function <span class="apidocSignatureSpan">is.</span>gt (value, other)](#apidoc.element.is.gt)
- description and source-code
```javascript
gt = function (value, other) {
  if (isActualNaN(value) || isActualNaN(other)) {
    throw new TypeError('NaN is not a valid value');
  }
  return !is.infinite(value) && !is.infinite(other) && value > other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.hash"></a>[function <span class="apidocSignatureSpan">is.</span>hash (value)](#apidoc.element.is.hash)
- description and source-code
```javascript
hash = function (value) {
  return is.object(value) && value.constructor === Object && !value.nodeType && !value.setInterval;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.hex"></a>[function <span class="apidocSignatureSpan">is.</span>hex (value)](#apidoc.element.is.hex)
- description and source-code
```javascript
hex = function (value) {
  return is.string(value) && (!value.length || hexRegex.test(value));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.hosted"></a>[function <span class="apidocSignatureSpan">is.</span>hosted (value, host)](#apidoc.element.is.hosted)
- description and source-code
```javascript
hosted = function (value, host) {
  var type = typeof host[value];
  return type === 'object' ? !!host[value] : !NON_HOST_TYPES[type];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.infinite"></a>[function <span class="apidocSignatureSpan">is.</span>infinite (value)](#apidoc.element.is.infinite)
- description and source-code
```javascript
infinite = function (value) {
  return value === Infinity || value === -Infinity;
}
```
- example usage
```shell
...
*
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is a decimal number, false otherwise
* @api public
*/

is.decimal = function (value) {
 return is.number(value) && !isActualNaN(value) && !is.infinite(value) && value % 1 !== 0;
};

/**
* is.divisibleBy
* Test if 'value' is divisible by 'n'.
*
* @param {Number} value value to test
...
```

#### <a name="apidoc.element.is.instance"></a>[function <span class="apidocSignatureSpan">is.</span>instance (value, constructor)](#apidoc.element.is.instance)
- description and source-code
```javascript
instance = function (value, constructor) {
  return value instanceof constructor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.instanceof"></a>[function <span class="apidocSignatureSpan">is.</span>instanceof (value, constructor)](#apidoc.element.is.instanceof)
- description and source-code
```javascript
instanceof = function (value, constructor) {
  return value instanceof constructor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.int"></a>[function <span class="apidocSignatureSpan">is.</span>int (value)](#apidoc.element.is.int)
- description and source-code
```javascript
int = function (value) {
  return is.number(value) && !isActualNaN(value) && value % 1 === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.integer"></a>[function <span class="apidocSignatureSpan">is.</span>integer (value)](#apidoc.element.is.integer)
- description and source-code
```javascript
integer = function (value) {
  return is.number(value) && !isActualNaN(value) && value % 1 === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.le"></a>[function <span class="apidocSignatureSpan">is.</span>le (value, other)](#apidoc.element.is.le)
- description and source-code
```javascript
le = function (value, other) {
  if (isActualNaN(value) || isActualNaN(other)) {
    throw new TypeError('NaN is not a valid value');
  }
  return !is.infinite(value) && !is.infinite(other) && value <= other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.lt"></a>[function <span class="apidocSignatureSpan">is.</span>lt (value, other)](#apidoc.element.is.lt)
- description and source-code
```javascript
lt = function (value, other) {
  if (isActualNaN(value) || isActualNaN(other)) {
    throw new TypeError('NaN is not a valid value');
  }
  return !is.infinite(value) && !is.infinite(other) && value < other;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.maximum"></a>[function <span class="apidocSignatureSpan">is.</span>maximum (value, others)](#apidoc.element.is.maximum)
- description and source-code
```javascript
maximum = function (value, others) {
  if (isActualNaN(value)) {
    throw new TypeError('NaN is not a valid value');
  } else if (!is.arraylike(others)) {
    throw new TypeError('second argument must be array-like');
  }
  var len = others.length;

  while (--len >= 0) {
    if (value < others[len]) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.minimum"></a>[function <span class="apidocSignatureSpan">is.</span>minimum (value, others)](#apidoc.element.is.minimum)
- description and source-code
```javascript
minimum = function (value, others) {
  if (isActualNaN(value)) {
    throw new TypeError('NaN is not a valid value');
  } else if (!is.arraylike(others)) {
    throw new TypeError('second argument must be array-like');
  }
  var len = others.length;

  while (--len >= 0) {
    if (value > others[len]) {
      return false;
    }
  }

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.nan"></a>[function <span class="apidocSignatureSpan">is.</span>nan (value)](#apidoc.element.is.nan)
- description and source-code
```javascript
nan = function (value) {
  return !is.number(value) || value !== value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.nil"></a>[function <span class="apidocSignatureSpan">is.</span>nil (value)](#apidoc.element.is.nil)
- description and source-code
```javascript
nil = function (value) {
  return value === null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.null"></a>[function <span class="apidocSignatureSpan">is.</span>null (value)](#apidoc.element.is.null)
- description and source-code
```javascript
null = function (value) {
  return value === null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.number"></a>[function <span class="apidocSignatureSpan">is.</span>number (value)](#apidoc.element.is.number)
- description and source-code
```javascript
number = function (value) {
  return toStr.call(value) === '[object Number]';
}
```
- example usage
```shell
...
* @api public
*/

is.arraylike = function (value) {
 return !!value && !is.bool(value)
   && owns.call(value, 'length')
   && isFinite(value.length)
   && is.number(value.length)
   && value.length >= 0;
};

/**
* Test boolean.
*/
...
```

#### <a name="apidoc.element.is.object"></a>[function <span class="apidocSignatureSpan">is.</span>object (value)](#apidoc.element.is.object)
- description and source-code
```javascript
object = function (value) {
  return toStr.call(value) === '[object Object]';
}
```
- example usage
```shell
...
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an arguments object, false otherwise
* @api public
*/

is.args = is.arguments = function (value) {
 var isStandardArguments = toStr.call(value) === '[object Arguments]';
 var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
 return isStandardArguments || isOldArguments;
};

/**
* Test array.
*/
...
```

#### <a name="apidoc.element.is.odd"></a>[function <span class="apidocSignatureSpan">is.</span>odd (value)](#apidoc.element.is.odd)
- description and source-code
```javascript
odd = function (value) {
  return is.infinite(value) || (is.number(value) && value === value && value % 2 !== 0);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.primitive"></a>[function <span class="apidocSignatureSpan">is.</span>primitive (value)](#apidoc.element.is.primitive)
- description and source-code
```javascript
function isPrimitive(value) {
  if (!value) {
    return true;
  }
  if (typeof value === 'object' || is.object(value) || is.fn(value) || is.array(value)) {
    return false;
  }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.regexp"></a>[function <span class="apidocSignatureSpan">is.</span>regexp (value)](#apidoc.element.is.regexp)
- description and source-code
```javascript
regexp = function (value) {
  return toStr.call(value) === '[object RegExp]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.string"></a>[function <span class="apidocSignatureSpan">is.</span>string (value)](#apidoc.element.is.string)
- description and source-code
```javascript
string = function (value) {
  return toStr.call(value) === '[object String]';
}
```
- example usage
```shell
...
 *
 * @param {Mixed} value value to test
 * @return {Boolean} true if 'value' is a base64 encoded string, false otherwise
 * @api public
 */

is.base64 = function (value) {
  return is.string(value) && (!value.length || base64Regex.test(value));
};

/**
 * Test base64 string.
 */

/**
...
```

#### <a name="apidoc.element.is.symbol"></a>[function <span class="apidocSignatureSpan">is.</span>symbol (value)](#apidoc.element.is.symbol)
- description and source-code
```javascript
symbol = function (value) {
  return typeof Symbol === 'function' && toStr.call(value) === '[object Symbol]' && typeof symbolValueOf.call(value) === 'symbol
';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.true"></a>[function <span class="apidocSignatureSpan">is.</span>true (value)](#apidoc.element.is.true)
- description and source-code
```javascript
true = function (value) {
  return is.bool(value) && Boolean(Number(value)) === true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.type"></a>[function <span class="apidocSignatureSpan">is.</span>type (value, type)](#apidoc.element.is.type)
- description and source-code
```javascript
type = function (value, type) {
  return typeof value === type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.undef"></a>[function <span class="apidocSignatureSpan">is.</span>undef (value)](#apidoc.element.is.undef)
- description and source-code
```javascript
undef = function (value) {
  return typeof value === 'undefined';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.undefined"></a>[function <span class="apidocSignatureSpan">is.</span>undefined (value)](#apidoc.element.is.undefined)
- description and source-code
```javascript
undefined = function (value) {
  return typeof value === 'undefined';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.is.within"></a>[function <span class="apidocSignatureSpan">is.</span>within (value, start, finish)](#apidoc.element.is.within)
- description and source-code
```javascript
within = function (value, start, finish) {
  if (isActualNaN(value) || isActualNaN(start) || isActualNaN(finish)) {
    throw new TypeError('NaN is not a valid value');
  } else if (!is.number(value) || !is.number(start) || !is.number(finish)) {
    throw new TypeError('all arguments must be numbers');
  }
  var isAnyInfinite = is.infinite(value) || is.infinite(start) || is.infinite(finish);
  return isAnyInfinite || (value >= start && value <= finish);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.is.arguments"></a>[module is.arguments](#apidoc.module.is.arguments)

#### <a name="apidoc.element.is.arguments.empty"></a>[function <span class="apidocSignatureSpan">is.arguments.</span>empty (value)](#apidoc.element.is.arguments.empty)
- description and source-code
```javascript
empty = function (value) {
  return is.args(value) && value.length === 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.is.array"></a>[module is.array](#apidoc.module.is.array)

#### <a name="apidoc.element.is.array.array"></a>[function <span class="apidocSignatureSpan">is.</span>array ()](#apidoc.element.is.array.array)
- description and source-code
```javascript
function isArray() { [native code] }
```
- example usage
```shell
...
* @param {Mixed} value value to test
* @return {Boolean} true if 'value' is an arguments object, false otherwise
* @api public
*/

is.args = is.arguments = function (value) {
 var isStandardArguments = toStr.call(value) === '[object Arguments]';
 var isOldArguments = !is.array(value) && is.arraylike(value) && is.object(value) && is.fn(value.callee);
 return isStandardArguments || isOldArguments;
};

/**
* Test array.
*/
...
```

#### <a name="apidoc.element.is.array.empty"></a>[function <span class="apidocSignatureSpan">is.array.</span>empty (value)](#apidoc.element.is.array.empty)
- description and source-code
```javascript
empty = function (value) {
  return is.array(value) && value.length === 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.is.date"></a>[module is.date](#apidoc.module.is.date)

#### <a name="apidoc.element.is.date.date"></a>[function <span class="apidocSignatureSpan">is.</span>date (value)](#apidoc.element.is.date.date)
- description and source-code
```javascript
date = function (value) {
  return toStr.call(value) === '[object Date]';
}
```
- example usage
```shell
...
 * is.date.valid
 * Test if 'value' is a valid date.
 *
 * @param {Mixed} value value to test
 * @returns {Boolean} true if 'value' is a valid date, false otherwise
 */
is.date.valid = function (value) {
  return is.date(value) && !isNaN(Number(value));
};

/**
 * Test element.
 */

/**
...
```

#### <a name="apidoc.element.is.date.valid"></a>[function <span class="apidocSignatureSpan">is.date.</span>valid (value)](#apidoc.element.is.date.valid)
- description and source-code
```javascript
valid = function (value) {
  return is.date(value) && !isNaN(Number(value));
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
