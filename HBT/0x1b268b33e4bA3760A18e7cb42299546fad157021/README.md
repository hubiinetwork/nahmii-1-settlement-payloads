# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1b268b33e4bA3760A18e7cb42299546fad157021`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000bd4e37fe00000000000000000000000000000000000000000000000000000000bd4e37fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000bd4e37fe00000000000000000000000000000000000000000000000000000000bd4e37fee569e5f89bfafb15fe88406356dd82ea1f5eaec8b9d34b12a05a0c0b7f2ba277bf869923a044b1929e9a2e557e20b8cb4031bdda37aec6302ca12e263858d1ee0792ac15dd3adec9149e72f2b41e788dc57a4a0f2f2678281de792a6c3ba578f000000000000000000000000000000000000000000000000000000000000001b4b66fcf68019038ec53b5701c9749247c0e4ad53f9fe7bb8deac6c530f8842fa78f4e7f5a890e40d4e411bde74a389b722bbea7887e3b2d0e03f9d43758ae7c166c7a02cfde250ae79705daa245f2761574dad4f7c6b4f12a4773f65029f923e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17f64785f35d000000000000000000000000000000000000000000000000002e17f70504a1ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000307653000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1f9e85aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a6d593159546734595330325a5456684c5455334d4449744f5449785a4330774e445a6a5a6d55304e546c6c596a556966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000001b268b33e4ba3760a18e7cb42299546fad15702100000000000000000000000000000000000000000000000000000000bd4e37fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe569e5f89bfafb15fe88406356dd82ea1f5eaec8b9d34b12a05a0c0b7f2ba277",
      "signature": {
        "s": "0x0792ac15dd3adec9149e72f2b41e788dc57a4a0f2f2678281de792a6c3ba578f",
        "r": "0xbf869923a044b1929e9a2e557e20b8cb4031bdda37aec6302ca12e263858d1ee",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4b66fcf68019038ec53b5701c9749247c0e4ad53f9fe7bb8deac6c530f8842fa",
      "signature": {
        "s": "0x66c7a02cfde250ae79705daa245f2761574dad4f7c6b4f12a4773f65029f923e",
        "r": "0x78f4e7f5a890e40d4e411bde74a389b722bbea7887e3b2d0e03f9d43758ae7c1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3176019966",
    "total": "3176019966"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3176019966",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43480155562"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3176019"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZmY1YTg4YS02ZTVhLTU3MDItOTIxZC0wNDZjZmU0NTllYjUifQ==",
    "nonce": 6480,
    "balances": {
      "current": "12974195458044765",
      "previous": "12974198637240750"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1b268b33e4ba3760a18e7cb42299546fad157021",
    "nonce": 23,
    "balances": {
      "current": "3176019966",
      "previous": "0"
    }
  },
  "blockNumber": "10114706",
  "created": "2020-05-22T08:49:26.772Z",
  "updated": "2020-05-22T08:49:26.836Z",
  "id": "5ec79216005df800101bcaaf"
}
```
* *stageAmount*: `3176019966`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000bd4e37fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000bd4e37fe00000000000000000000000000000000000000000000000000000000bd4e37fee569e5f89bfafb15fe88406356dd82ea1f5eaec8b9d34b12a05a0c0b7f2ba277bf869923a044b1929e9a2e557e20b8cb4031bdda37aec6302ca12e263858d1ee0792ac15dd3adec9149e72f2b41e788dc57a4a0f2f2678281de792a6c3ba578f000000000000000000000000000000000000000000000000000000000000001b4b66fcf68019038ec53b5701c9749247c0e4ad53f9fe7bb8deac6c530f8842fa78f4e7f5a890e40d4e411bde74a389b722bbea7887e3b2d0e03f9d43758ae7c166c7a02cfde250ae79705daa245f2761574dad4f7c6b4f12a4773f65029f923e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000195000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17f64785f35d000000000000000000000000000000000000000000000000002e17f70504a1ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000307653000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1f9e85aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a6d593159546734595330325a5456684c5455334d4449744f5449785a4330774e445a6a5a6d55304e546c6c596a556966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000001b268b33e4ba3760a18e7cb42299546fad15702100000000000000000000000000000000000000000000000000000000bd4e37fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe569e5f89bfafb15fe88406356dd82ea1f5eaec8b9d34b12a05a0c0b7f2ba277",
      "signature": {
        "s": "0x0792ac15dd3adec9149e72f2b41e788dc57a4a0f2f2678281de792a6c3ba578f",
        "r": "0xbf869923a044b1929e9a2e557e20b8cb4031bdda37aec6302ca12e263858d1ee",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4b66fcf68019038ec53b5701c9749247c0e4ad53f9fe7bb8deac6c530f8842fa",
      "signature": {
        "s": "0x66c7a02cfde250ae79705daa245f2761574dad4f7c6b4f12a4773f65029f923e",
        "r": "0x78f4e7f5a890e40d4e411bde74a389b722bbea7887e3b2d0e03f9d43758ae7c1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3176019966",
    "total": "3176019966"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3176019966",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "43480155562"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3176019"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZmY1YTg4YS02ZTVhLTU3MDItOTIxZC0wNDZjZmU0NTllYjUifQ==",
    "nonce": 6480,
    "balances": {
      "current": "12974195458044765",
      "previous": "12974198637240750"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1b268b33e4ba3760a18e7cb42299546fad157021",
    "nonce": 23,
    "balances": {
      "current": "3176019966",
      "previous": "0"
    }
  },
  "blockNumber": "10114706",
  "created": "2020-05-22T08:49:26.772Z",
  "updated": "2020-05-22T08:49:26.836Z",
  "id": "5ec79216005df800101bcaaf"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000bd4e37fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3176019966`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`