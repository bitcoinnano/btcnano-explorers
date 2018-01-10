# Blockchain APIs for btcnano

[![NPM Package](https://img.shields.io/npm/v/btcnano-explorers.svg?style=flat-square)](https://www.npmjs.org/package/btcnano-explorers)
[![Build Status](https://img.shields.io/travis/bitcoinnano/btcnano-explorers.svg?branch=master&style=flat-square)](https://travis-ci.org/bitcoinnano/btcnano-explorers)
[![Coverage Status](https://img.shields.io/coveralls/bitcoinnano/btcnano-explorers.svg?style=flat-square)](https://coveralls.io/r/bitcoinnano/btcnano-explorers)

A module for [bitcore](https://github.com/bitpay/bitcore) that implements HTTP requests to different Web APIs to query the state of the blockchain.

## Getting started

Be careful! When using this module, the information retrieved from remote servers may be compromised and not reflect the actual state of the blockchain.

```sh
npm install btcnano-explorers
bower install btcnano-explorers
```

At the moment, only Insight is supported, and only getting the UTXOs for an address and broadcasting a transaction.

```javascript
var explorers = require('bitcore-explorers');
var insight = new explorers.Insight();

insight.getUtxos('1Btcnano...', function(err, utxos) {
  if (err) {
    // Handle errors...
  } else {
    // Maybe use the UTXOs to create a transaction
  }
});
```

## Contributing

See [CONTRIBUTING.md](https://github.com/bitpay/bitcore/blob/master/CONTRIBUTING.md) on the main bitcore repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2015-2021 Btcnano, Inc. Btcnano is a trademark maintained by Btcnano, Inc.
