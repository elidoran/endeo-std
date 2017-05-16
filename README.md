# endeo-std
[![Dependency Status](https://gemnasium.com/elidoran/endeo.png)](https://gemnasium.com/elidoran/endeo)
[![npm version](https://badge.fury.io/js/endeo.svg)](http://badge.fury.io/js/endeo)

Aggregates standard endeo implementations for easy install.


See packages:

1. [endeo](https://www.npmjs.com/package/endeo)
2. [enbyte](https://www.npmjs.com/package/enbyte)
3. [debyte](https://www.npmjs.com/package/debyte)
4. [unstring](https://www.npmjs.com/package/unstring)
5. [@endeo/decoder](https://www.npmjs.com/package/@endeo/decoder)
5. [@endeo/bytes](https://www.npmjs.com/package/@endeo/bytes)
5. [@endeo/types](https://www.npmjs.com/package/@endeo/types)
5. [@endeo/input](https://www.npmjs.com/package/@endeo/input)
5. [@endeo/output](https://www.npmjs.com/package/@endeo/output)


## Install

```sh
npm install --save endeo-std
```


## Usage

See [endeo](https://www.npmjs.com/package/endeo) for usage. This package depends on all the standard component implementations so they can be installed conveniently via `npm install -S endeo-std`.

```javascript
// the super short version:

// get builder
var buildEndeo = require('endeo')

// build it
var endeo = buildEndeo()

// encode object/array/string
var buffer = endeo.encode({ some: 'object' })

// decode buffer back into an object
var object = endeo.decode(buffer)


// streaming version...
var encoder = endeo.encoder()
encoder.pipe(someTargetStream)
encoder.write({ some: 'object' })
encoder.write([ 'some', 'array'])

var decoder = endeo.decoder()
decoder.pipe(someTargetStream)
decoder.on('data', function(thing){
  // thing = object/array
})
```


# [MIT License](LICENSE)
