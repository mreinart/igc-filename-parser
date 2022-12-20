igc-filename-parser
==============================================================================

[![Build Status](https://travis-ci.org/Turbo87/igc-filename-parser.svg?branch=master)](https://travis-ci.org/Turbo87/igc-filename-parser)

IGC flight log filename parser
- adapt to conform with igc_fr_specification_2022_with_al7_2022-1-31.pdf 
  - A2.5.1 Long file name style
  - example: 2021-05-15-MMM-XXXXXX-01.IGC
      - MMM = manufacturer's three-letter IGC identifier
      - XXXXXX = unique FR Serial ID (S/ID); 6 alphanumeric characters - 6 digits for the logger id

Install
------------------------------------------------------------------------------

```bash
npm install --save igc-filename-parser
```

or using [`yarn`](https://yarnpkg.com/):

```bash
yarn add igc-filename-parser
```


Usage
------------------------------------------------------------------------------

```js
const parse = require('igc-filename-parser');

let result = parse('78_65dv1qz1.igc');
```

```js
{
  callsign: '78',
  date: '2016-05-13', 
  manufacturer: 'LXNAV', 
  loggerId: '1QZ', 
  numFlight: 1, 
}
```

For more examples have a look at our [test suite](test.js).

License
------------------------------------------------------------------------------

igc-filename-parser is licensed under the [MIT License](LICENSE).
