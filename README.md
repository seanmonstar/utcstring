# utc

UTC date format utilities.

## Usage

```js
var utc = require('utc');

utc() // now in UTC string format
utc(new Date()) // date in UTC string; same as (new Date).toUTCString();

utc.is('Thu, 30 Oct 2013 11:15:21 GMT') // returns true
utc.is('Thu, 30 Oct 2013') // returns false

utc.has('Today is Thu, 30 Oct 2013 11:15:21 GMT, hurray!') // true

utc.match('Today is Thu, 30 Oct 2013 11:15:21 GMT, hurray!') // ['Thu, 30 Oct 2013 11:15:21 GMT']

// essentially utc.match()[0]
utc.get('Today is Thu, 30 Oct 2013 11:15:21 GMT, hurray!') // 'Thu, 30 Oct 2013 11:15:21 GMT'

// checks utc.is(str) before parsing as Date
utc.from('Thu, 30 Oct 2013 11:15:21 GMT') // Date instance
utc.from('2013-10-30') // null
```

## License

MPLv2.0
