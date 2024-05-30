# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBDF693901B2aDf333e2361fb4035BBe379B81724`.

The ordered steps of contract function invocations are included below and in
the corresponding [steps.json](./steps.json). Please read [the general recipe
for settling Nahmii 1 balance](../../README.md) before starting on the first
step of settlement.

## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001fb40000000000000000000000000000000000000000000000000000000000001fb400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001fb40000000000000000000000000000000000000000000000000000000000001fb460c869da7f28f87e608902a84af06105f3ade720cb85d50bf63feb091907c0471f6369eb0c06ae38c6680d964a1888704f227bc7bc18bd1851838da89c8b2b814748f496fd1eaee934b25d1fa7bc2c04bbadc092d7edd0779b82f929a50830ea000000000000000000000000000000000000000000000000000000000000001b9ee4b458597baab14ba51ea89de63c5f805b28cf2cdc7883e7d621d00fff8ac6a757bb2f03ce1c0a7fa682fec8560488838ffe7ac3998161b16800aeb56ca36909b5bbe0881173aba1f2eb015d38084c05ebde9ba32553cfdf6cd3d7a08f55a1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ba7b05000000000000000000000000000000000000000000000000002386f2c7ba9ac100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000945ae00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5467344e4441795a4331694f546c6b4c54566c5a4749744f54526b4e6930784e7a49344d545930596a4d304f57496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bdf693901b2adf333e2361fb4035bbe379b817240000000000000000000000000000000000000000000000000000000000001fb4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60c869da7f28f87e608902a84af06105f3ade720cb85d50bf63feb091907c047",
      "signature": {
        "s": "0x4748f496fd1eaee934b25d1fa7bc2c04bbadc092d7edd0779b82f929a50830ea",
        "r": "0x1f6369eb0c06ae38c6680d964a1888704f227bc7bc18bd1851838da89c8b2b81",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9ee4b458597baab14ba51ea89de63c5f805b28cf2cdc7883e7d621d00fff8ac6",
      "signature": {
        "s": "0x09b5bbe0881173aba1f2eb015d38084c05ebde9ba32553cfdf6cd3d7a08f55a1",
        "r": "0xa757bb2f03ce1c0a7fa682fec8560488838ffe7ac3998161b16800aeb56ca369",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8116",
    "total": "8116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8116",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "607662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZTg4NDAyZC1iOTlkLTVlZGItOTRkNi0xNzI4MTY0YjM0OWIifQ==",
    "nonce": 1270,
    "balances": {
      "current": "10000001475967749",
      "previous": "10000001475975873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdf693901b2adf333e2361fb4035bbe379b81724",
    "nonce": 20,
    "balances": {
      "current": "8116",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:07.796Z",
  "updated": "2020-05-22T08:08:07.868Z",
  "id": "5ec78867b0c6090011d5aa6f"
}
```
* *stageAmount*: `8116`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001fb400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001fb40000000000000000000000000000000000000000000000000000000000001fb460c869da7f28f87e608902a84af06105f3ade720cb85d50bf63feb091907c0471f6369eb0c06ae38c6680d964a1888704f227bc7bc18bd1851838da89c8b2b814748f496fd1eaee934b25d1fa7bc2c04bbadc092d7edd0779b82f929a50830ea000000000000000000000000000000000000000000000000000000000000001b9ee4b458597baab14ba51ea89de63c5f805b28cf2cdc7883e7d621d00fff8ac6a757bb2f03ce1c0a7fa682fec8560488838ffe7ac3998161b16800aeb56ca36909b5bbe0881173aba1f2eb015d38084c05ebde9ba32553cfdf6cd3d7a08f55a1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ba7b05000000000000000000000000000000000000000000000000002386f2c7ba9ac100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000945ae00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a5467344e4441795a4331694f546c6b4c54566c5a4749744f54526b4e6930784e7a49344d545930596a4d304f57496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bdf693901b2adf333e2361fb4035bbe379b817240000000000000000000000000000000000000000000000000000000000001fb4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60c869da7f28f87e608902a84af06105f3ade720cb85d50bf63feb091907c047",
      "signature": {
        "s": "0x4748f496fd1eaee934b25d1fa7bc2c04bbadc092d7edd0779b82f929a50830ea",
        "r": "0x1f6369eb0c06ae38c6680d964a1888704f227bc7bc18bd1851838da89c8b2b81",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9ee4b458597baab14ba51ea89de63c5f805b28cf2cdc7883e7d621d00fff8ac6",
      "signature": {
        "s": "0x09b5bbe0881173aba1f2eb015d38084c05ebde9ba32553cfdf6cd3d7a08f55a1",
        "r": "0xa757bb2f03ce1c0a7fa682fec8560488838ffe7ac3998161b16800aeb56ca369",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8116",
    "total": "8116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8116",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "607662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZTg4NDAyZC1iOTlkLTVlZGItOTRkNi0xNzI4MTY0YjM0OWIifQ==",
    "nonce": 1270,
    "balances": {
      "current": "10000001475967749",
      "previous": "10000001475975873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbdf693901b2adf333e2361fb4035bbe379b81724",
    "nonce": 20,
    "balances": {
      "current": "8116",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:07.796Z",
  "updated": "2020-05-22T08:08:07.868Z",
  "id": "5ec78867b0c6090011d5aa6f"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000000000000001fb40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8116`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``