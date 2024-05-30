# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0913b57463C8f62Eb4DD2fA91819d3c5B36889bc`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000000000000000000000000000000000000000017f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000000000000000000000000000000000000000017fdcb2eff84a9a481f5af1e3701c0416f5f852a5897dc55b2ca226bd40a0858a35d4ea57f1a94df90197c6c68931cb3fb233da9035b198d2bf38a95bb232d5c4047c67f66e4092d16b32bf235fa48e63e7d4a5a2c3a7095ec342735556f902232c000000000000000000000000000000000000000000000000000000000000001c3a68dfd48a5624e8be1051648942159765839c920a0d054b74c3cadf7d98c4ee3a5ea22264d5a790e33d5b8eee95bd3875eec7c51e0faadd577674ed6dabfca727b40c9d754e6681ca80f3773cc9d99a8e4a4f0e8dd97b90149a1cf15e0f5701000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6b972d000000000000000000000000000000000000000000000000002386f2bc6b98ad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28c500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d57466c4d6a51304e43316b4d6d51314c54566d5a546374595449774e5331684d3259324e44566c4e4452695a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000913b57463c8f62eb4dd2fa91819d3c5b36889bc000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcb2eff84a9a481f5af1e3701c0416f5f852a5897dc55b2ca226bd40a0858a35",
      "signature": {
        "s": "0x7c67f66e4092d16b32bf235fa48e63e7d4a5a2c3a7095ec342735556f902232c",
        "r": "0xd4ea57f1a94df90197c6c68931cb3fb233da9035b198d2bf38a95bb232d5c404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3a68dfd48a5624e8be1051648942159765839c920a0d054b74c3cadf7d98c4ee",
      "signature": {
        "s": "0x27b40c9d754e6681ca80f3773cc9d99a8e4a4f0e8dd97b90149a1cf15e0f5701",
        "r": "0x3a5ea22264d5a790e33d5b8eee95bd3875eec7c51e0faadd577674ed6dabfca7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "383",
    "total": "383"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "383",
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
            "amount": "796869"
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
    "data": "eyJyZWYiOiJlMWFlMjQ0NC1kMmQ1LTVmZTctYTIwNS1hM2Y2NDVlNDRiZjMifQ==",
    "nonce": 2211,
    "balances": {
      "current": "10000001286248237",
      "previous": "10000001286248621"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0913b57463c8f62eb4dd2fa91819d3c5b36889bc",
    "nonce": 10,
    "balances": {
      "current": "383",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:04.744Z",
  "updated": "2020-05-22T08:15:04.815Z",
  "id": "5ec78a08b0c6090011d5abaf"
}
```
* *stageAmount*: `383`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000017f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000000000000000000000000000000000000000017fdcb2eff84a9a481f5af1e3701c0416f5f852a5897dc55b2ca226bd40a0858a35d4ea57f1a94df90197c6c68931cb3fb233da9035b198d2bf38a95bb232d5c4047c67f66e4092d16b32bf235fa48e63e7d4a5a2c3a7095ec342735556f902232c000000000000000000000000000000000000000000000000000000000000001c3a68dfd48a5624e8be1051648942159765839c920a0d054b74c3cadf7d98c4ee3a5ea22264d5a790e33d5b8eee95bd3875eec7c51e0faadd577674ed6dabfca727b40c9d754e6681ca80f3773cc9d99a8e4a4f0e8dd97b90149a1cf15e0f5701000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6b972d000000000000000000000000000000000000000000000000002386f2bc6b98ad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28c500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d57466c4d6a51304e43316b4d6d51314c54566d5a546374595449774e5331684d3259324e44566c4e4452695a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000913b57463c8f62eb4dd2fa91819d3c5b36889bc000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdcb2eff84a9a481f5af1e3701c0416f5f852a5897dc55b2ca226bd40a0858a35",
      "signature": {
        "s": "0x7c67f66e4092d16b32bf235fa48e63e7d4a5a2c3a7095ec342735556f902232c",
        "r": "0xd4ea57f1a94df90197c6c68931cb3fb233da9035b198d2bf38a95bb232d5c404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3a68dfd48a5624e8be1051648942159765839c920a0d054b74c3cadf7d98c4ee",
      "signature": {
        "s": "0x27b40c9d754e6681ca80f3773cc9d99a8e4a4f0e8dd97b90149a1cf15e0f5701",
        "r": "0x3a5ea22264d5a790e33d5b8eee95bd3875eec7c51e0faadd577674ed6dabfca7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "383",
    "total": "383"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "383",
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
            "amount": "796869"
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
    "data": "eyJyZWYiOiJlMWFlMjQ0NC1kMmQ1LTVmZTctYTIwNS1hM2Y2NDVlNDRiZjMifQ==",
    "nonce": 2211,
    "balances": {
      "current": "10000001286248237",
      "previous": "10000001286248621"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0913b57463c8f62eb4dd2fa91819d3c5b36889bc",
    "nonce": 10,
    "balances": {
      "current": "383",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:04.744Z",
  "updated": "2020-05-22T08:15:04.815Z",
  "id": "5ec78a08b0c6090011d5abaf"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000017f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `383`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``