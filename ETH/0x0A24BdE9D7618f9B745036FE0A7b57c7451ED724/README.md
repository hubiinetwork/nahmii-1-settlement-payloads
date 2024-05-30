# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0A24BdE9D7618f9B745036FE0A7b57c7451ED724`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000000000000000000000000000000000000000000bb4c7e92aa45cb8a9f904a60c33d8fde560fefc2c333d6043947049cd0be5329ab9dc6ddc22c351217b10eff25955924cc1ba3da601908b0b4e5c64f64a79a427413eb4471e6ba886214b820e017d47fa54b8ac9628f60451e9fd7ac2e3882feb000000000000000000000000000000000000000000000000000000000000001bfd04ded9479773638c5e2c4a478f06d0361acee806152f2a40aa62396d87dd24b8a88a74f8c3c4f14e8bd3f9fc582852718d5afb5ca51629e634cb3db0d8f7123d8aae73ec4ede8d0b72062a6d05049445fc32e0db6a2067d3155f89183a6f90000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcadccbf000000000000000000000000000000000000000000000000002386f2bcadcccb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c17e400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d7a5a6c4e325a6c4d4330784e324e6b4c54566c4e6a517459574978597930344d4755334d7a42694e4455344e54516966513d3d00000000000000000000000000000000000000000000000000000000000000130000000000000000000000000a24bde9d7618f9b745036fe0a7b57c7451ed724000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4c7e92aa45cb8a9f904a60c33d8fde560fefc2c333d6043947049cd0be5329a",
      "signature": {
        "s": "0x413eb4471e6ba886214b820e017d47fa54b8ac9628f60451e9fd7ac2e3882feb",
        "r": "0xb9dc6ddc22c351217b10eff25955924cc1ba3da601908b0b4e5c64f64a79a427",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfd04ded9479773638c5e2c4a478f06d0361acee806152f2a40aa62396d87dd24",
      "signature": {
        "s": "0x3d8aae73ec4ede8d0b72062a6d05049445fc32e0db6a2067d3155f89183a6f90",
        "r": "0xb8a88a74f8c3c4f14e8bd3f9fc582852718d5afb5ca51629e634cb3db0d8f712",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11",
    "total": "11"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11",
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
            "amount": "792548"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMzZlN2ZlMC0xN2NkLTVlNjQtYWIxYy04MGU3MzBiNDU4NTQifQ==",
    "nonce": 2157,
    "balances": {
      "current": "10000001290587327",
      "previous": "10000001290587339"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0a24bde9d7618f9b745036fe0a7b57c7451ed724",
    "nonce": 19,
    "balances": {
      "current": "11",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:42.465Z",
  "updated": "2020-05-22T08:14:42.528Z",
  "id": "5ec789f2b0c6090011d5aba2"
}
```
* *stageAmount*: `11`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000000000000000000000000000000000000000000bb4c7e92aa45cb8a9f904a60c33d8fde560fefc2c333d6043947049cd0be5329ab9dc6ddc22c351217b10eff25955924cc1ba3da601908b0b4e5c64f64a79a427413eb4471e6ba886214b820e017d47fa54b8ac9628f60451e9fd7ac2e3882feb000000000000000000000000000000000000000000000000000000000000001bfd04ded9479773638c5e2c4a478f06d0361acee806152f2a40aa62396d87dd24b8a88a74f8c3c4f14e8bd3f9fc582852718d5afb5ca51629e634cb3db0d8f7123d8aae73ec4ede8d0b72062a6d05049445fc32e0db6a2067d3155f89183a6f90000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcadccbf000000000000000000000000000000000000000000000000002386f2bcadcccb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c17e400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d7a5a6c4e325a6c4d4330784e324e6b4c54566c4e6a517459574978597930344d4755334d7a42694e4455344e54516966513d3d00000000000000000000000000000000000000000000000000000000000000130000000000000000000000000a24bde9d7618f9b745036fe0a7b57c7451ed724000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4c7e92aa45cb8a9f904a60c33d8fde560fefc2c333d6043947049cd0be5329a",
      "signature": {
        "s": "0x413eb4471e6ba886214b820e017d47fa54b8ac9628f60451e9fd7ac2e3882feb",
        "r": "0xb9dc6ddc22c351217b10eff25955924cc1ba3da601908b0b4e5c64f64a79a427",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfd04ded9479773638c5e2c4a478f06d0361acee806152f2a40aa62396d87dd24",
      "signature": {
        "s": "0x3d8aae73ec4ede8d0b72062a6d05049445fc32e0db6a2067d3155f89183a6f90",
        "r": "0xb8a88a74f8c3c4f14e8bd3f9fc582852718d5afb5ca51629e634cb3db0d8f712",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11",
    "total": "11"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11",
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
            "amount": "792548"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMzZlN2ZlMC0xN2NkLTVlNjQtYWIxYy04MGU3MzBiNDU4NTQifQ==",
    "nonce": 2157,
    "balances": {
      "current": "10000001290587327",
      "previous": "10000001290587339"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0a24bde9d7618f9b745036fe0a7b57c7451ed724",
    "nonce": 19,
    "balances": {
      "current": "11",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:42.465Z",
  "updated": "2020-05-22T08:14:42.528Z",
  "id": "5ec789f2b0c6090011d5aba2"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `11`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``