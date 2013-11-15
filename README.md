# yahoo-finance

`yahoo-finance` is [Yahoo Finance](http://finance.yahoo.com/) client library for [Node.js](http://nodejs.org/).


## Installation

    $ npm install yahoo-finance


## Usage

```js
var yahooFinance = require('yahoo-finance');

yahooFinance.historical({
  symbol: 'AAPL'
}, function (err, quotes, url, symbol) {
  // ...
}

yahooFinance.historical({
  symbols: ['AAPL', 'GOOG', 'YHOO']
}, function (err, results) {
  // ...
}

yahooFinance.snapshot({
  symbols: ['AAPL', 'GOOG', 'YHOO'],
  fields: 'snd1l1yr'  // or ['s', 'n', 'd1', 'l1', 'y', 'r']
}, function (err, results) {
  // ...
}
```

* [See more comprehensive examples here.](https://github.com/pilwon/node-yahoo-finance/tree/master/examples)


## API

```js
.historical({
  symbol: SYMBOL
}, function (err, quotes, url, symbol) {
  //...
});

.historical({
  symbols: [
    SYMBOL1,
    SYMBOL2
  ]
}, function (err, results) {
  //...
});

.snapshot({
  symbols: [
    SYMBOL1,
    SYMBOL2
  ]
}, function (err, results) {
  //...
});
```


## License

<pre>
The MIT License (MIT)

Copyright (c) 2013 Pilwon Huh

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
</pre>