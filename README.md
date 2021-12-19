# truffle-bsc-deploy-investigation
This is a minimal set of the code to reproduce the issue that Truffle failed to deploy a contract to BSC main net while it worked for test net.
I basically followed [the official doc](https://docs.binance.org/smart-chain/developer/deploy/truffle.html).


## Steps to reproduce
```
$ echo ${YOUR MNEMONIC} > .secret
$ npm install
$ truffle compile
$ truffle migrate --network testnet # This should work
$ truffle migrate --network bsc     # This will fail
...
Unhandled error.({ code: -32000, message: 'header not found' })
...
```

## Truffle version
```
$ truffle version
Truffle v5.4.25 (core: 5.4.25)
Solidity v0.5.16 (solc-js)
Node v14.15.1
Web3.js v1.5.3
```
