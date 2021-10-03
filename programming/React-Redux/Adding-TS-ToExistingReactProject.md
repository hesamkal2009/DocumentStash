# How to add TS to Existing React Project
---

- yarn add typescript @types/react @types/react-dom @types/node
- npm i --save-dev @types/react-router-dom
- npm install @types/react-redux
- yarn add -D react-query-swagger
- yarn remove prop-types
---
- npm i ts-polyfill
#### Modify your project tsconfig.json to add type definitions required.\

(Obviously, you don't need EVERYTHING. Pick the ones you actually need to minimize bandwidth!)\

In this example, we are targeting ES2015 so only ES2016 and above polyfills are needed:\

<pre>
{
  "compilerOptions": {
    "target": "ES2015",
    "lib": [
      "DOM",
      "DOM.Iterable",
      "ES2015",
      "ES2016.Array.Include",
      "ES2017.Object",
      "ES2017.String",
      "ES2018.AsyncIterable",
      "ES2018.Promise",
      "ES2019.Array",
      "ES2019.Object",
      "ES2019.String",
      "ES2019.Symbol",
      "ES2020.Promise",
      "ES2020.String",
      "ES2020.Symbol.WellKnown"
    ]
  }
}
</pre>
##### ___It is 2020 and you should be targeting ES2015. Internet Explorer 11 and Windows 7 are no longer supported by Microsoft and no longer receive security patches.___

#### Then, in the entry point of your application, import the polyfills.

The complete list of available polyfills (including ES2015 polyfills for poor souls targeting ES5) can be found here: https://github.com/ryanelian/ts-polyfill/tree/master/lib\
<pre>
// index.ts
import 'ts-polyfill/lib/es2016-array-include';
import 'ts-polyfill/lib/es2017-object';
import 'ts-polyfill/lib/es2017-string';
import 'ts-polyfill/lib/es2018-async-iterable';   // for-await-of
import 'ts-polyfill/lib/es2018-promise';
import 'ts-polyfill/lib/es2019-array';
import 'ts-polyfill/lib/es2019-object';
import 'ts-polyfill/lib/es2019-string';
import 'ts-polyfill/lib/es2019-symbol';
import 'ts-polyfill/lib/es2020-promise';
import 'ts-polyfill/lib/es2020-string';
import 'ts-polyfill/lib/es2020-symbol-wellknown';
 
import 'ts-polyfill/lib/es2020-global-this';      // globalThis (no tsconfig.json lib)
</pre> 
---

