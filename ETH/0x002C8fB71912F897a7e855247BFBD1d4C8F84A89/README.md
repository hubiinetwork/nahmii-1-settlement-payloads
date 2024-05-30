# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x002C8fB71912F897a7e855247BFBD1d4C8F84A89`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000154f700000000000000000000000000000000000000000000000000000000000154f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000154f700000000000000000000000000000000000000000000000000000000000154f76c8d6d1d133625664b93335aaef3212ffc15c033c26ecfbd3b97d9d0841e27efe236a0e99150b234ba3c93516def0a630c481f391f61ce3d6bcd9320e1998ce35a95d81944488ee43be6a8dfa1e31cf7803c766e25418580b9afbc0ad4f4aef0000000000000000000000000000000000000000000000000000000000000001c345b74d25f442ca184cbca71cb5745d0a34d14255f4f2b442f113b342210bba9aaa20724e7cb61117f4f54af47239d8653f0ea518853423df0b7da6617470b7911648e23d193cceb20c212504163157c4dfae7ac18405a9027d0543f0d844284000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005a600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6c1f8c4000000000000000000000000000000000000000000000000002386f2c6c34e1200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000570000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000984fd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596d49345a6d45774d7930344d7a466d4c5455314d446374596a56684f53316c593249774e474d784e7a46694f444d6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000002c8fb71912f897a7e855247bfbd1d4c8f84a8900000000000000000000000000000000000000000000000000000000000154f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c8d6d1d133625664b93335aaef3212ffc15c033c26ecfbd3b97d9d0841e27ef",
      "signature": {
        "s": "0x5a95d81944488ee43be6a8dfa1e31cf7803c766e25418580b9afbc0ad4f4aef0",
        "r": "0xe236a0e99150b234ba3c93516def0a630c481f391f61ce3d6bcd9320e1998ce3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x345b74d25f442ca184cbca71cb5745d0a34d14255f4f2b442f113b342210bba9",
      "signature": {
        "s": "0x11648e23d193cceb20c212504163157c4dfae7ac18405a9027d0543f0d844284",
        "r": "0xaaa20724e7cb61117f4f54af47239d8653f0ea518853423df0b7da6617470b79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "87287",
    "total": "87287"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "87287",
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
            "amount": "623869"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "87"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYmI4ZmEwMy04MzFmLTU1MDctYjVhOS1lY2IwNGMxNzFiODMifQ==",
    "nonce": 1446,
    "balances": {
      "current": "10000001459681476",
      "previous": "10000001459768850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x002c8fb71912f897a7e855247bfbd1d4c8f84a89",
    "nonce": 24,
    "balances": {
      "current": "87287",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:36.976Z",
  "updated": "2020-05-22T08:09:37.053Z",
  "id": "5ec788c0e5756b00111b813e"
}
```
* *stageAmount*: `87287`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000154f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000154f700000000000000000000000000000000000000000000000000000000000154f76c8d6d1d133625664b93335aaef3212ffc15c033c26ecfbd3b97d9d0841e27efe236a0e99150b234ba3c93516def0a630c481f391f61ce3d6bcd9320e1998ce35a95d81944488ee43be6a8dfa1e31cf7803c766e25418580b9afbc0ad4f4aef0000000000000000000000000000000000000000000000000000000000000001c345b74d25f442ca184cbca71cb5745d0a34d14255f4f2b442f113b342210bba9aaa20724e7cb61117f4f54af47239d8653f0ea518853423df0b7da6617470b7911648e23d193cceb20c212504163157c4dfae7ac18405a9027d0543f0d844284000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005a600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6c1f8c4000000000000000000000000000000000000000000000000002386f2c6c34e1200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000570000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000984fd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596d49345a6d45774d7930344d7a466d4c5455314d446374596a56684f53316c593249774e474d784e7a46694f444d6966513d3d0000000000000000000000000000000000000000000000000000000000000018000000000000000000000000002c8fb71912f897a7e855247bfbd1d4c8f84a8900000000000000000000000000000000000000000000000000000000000154f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c8d6d1d133625664b93335aaef3212ffc15c033c26ecfbd3b97d9d0841e27ef",
      "signature": {
        "s": "0x5a95d81944488ee43be6a8dfa1e31cf7803c766e25418580b9afbc0ad4f4aef0",
        "r": "0xe236a0e99150b234ba3c93516def0a630c481f391f61ce3d6bcd9320e1998ce3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x345b74d25f442ca184cbca71cb5745d0a34d14255f4f2b442f113b342210bba9",
      "signature": {
        "s": "0x11648e23d193cceb20c212504163157c4dfae7ac18405a9027d0543f0d844284",
        "r": "0xaaa20724e7cb61117f4f54af47239d8653f0ea518853423df0b7da6617470b79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "87287",
    "total": "87287"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "87287",
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
            "amount": "623869"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "87"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYmI4ZmEwMy04MzFmLTU1MDctYjVhOS1lY2IwNGMxNzFiODMifQ==",
    "nonce": 1446,
    "balances": {
      "current": "10000001459681476",
      "previous": "10000001459768850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x002c8fb71912f897a7e855247bfbd1d4c8f84a89",
    "nonce": 24,
    "balances": {
      "current": "87287",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:36.976Z",
  "updated": "2020-05-22T08:09:37.053Z",
  "id": "5ec788c0e5756b00111b813e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000154f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `87287`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``