# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x50C4A39CbC66d7258a0805Ac48B1Aa0d386BA571`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28e6125d6467543b98ea09ee1dbf1c0cbe182310233da3fca2895bf0de75136f406995c7d8add7981e9a1dd661ce6b5f995184bef9449e0d5f4cfcf5001c21806336cac3896a5ed480ce8cfcce215cc434ae805d251bc2ee4ab42c147da404c049000000000000000000000000000000000000000000000000000000000000001b6ef146ec34fe238584b421e6b6453dc33cff5384170db9662437c20654aedd3cead90c4245d4c82511404113a46fb17efd6b3c1ac12da6e10724d04bee47b0ee6613595c06353abab7e8bb73df1847e59bc70c4fb3992a5d5817b33b68d507c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002a400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cafcacc8000000000000000000000000000000000000000000000000002386f2cafcf80300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000870f600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e5449334e6d5a6c4d4330775a6a55314c54566c4f446774596d55314d43316b4d7a4d315a4452694f47566a596a556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe6125d6467543b98ea09ee1dbf1c0cbe182310233da3fca2895bf0de75136f40",
      "signature": {
        "s": "0x36cac3896a5ed480ce8cfcce215cc434ae805d251bc2ee4ab42c147da404c049",
        "r": "0x6995c7d8add7981e9a1dd661ce6b5f995184bef9449e0d5f4cfcf5001c218063",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6ef146ec34fe238584b421e6b6453dc33cff5384170db9662437c20654aedd3c",
      "signature": {
        "s": "0x6613595c06353abab7e8bb73df1847e59bc70c4fb3992a5d5817b33b68d507c9",
        "r": "0xead90c4245d4c82511404113a46fb17efd6b3c1ac12da6e10724d04bee47b0ee",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "553206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NTI3NmZlMC0wZjU1LTVlODgtYmU1MC1kMzM1ZDRiOGVjYjUifQ==",
    "nonce": 676,
    "balances": {
      "current": "10000001530637512",
      "previous": "10000001530656771"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:53.914Z",
  "updated": "2020-05-22T08:03:53.995Z",
  "id": "5ec78769005df800101bc2f9"
}
```
* *stageAmount*: `19240`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28e6125d6467543b98ea09ee1dbf1c0cbe182310233da3fca2895bf0de75136f406995c7d8add7981e9a1dd661ce6b5f995184bef9449e0d5f4cfcf5001c21806336cac3896a5ed480ce8cfcce215cc434ae805d251bc2ee4ab42c147da404c049000000000000000000000000000000000000000000000000000000000000001b6ef146ec34fe238584b421e6b6453dc33cff5384170db9662437c20654aedd3cead90c4245d4c82511404113a46fb17efd6b3c1ac12da6e10724d04bee47b0ee6613595c06353abab7e8bb73df1847e59bc70c4fb3992a5d5817b33b68d507c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ca000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002a400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cafcacc8000000000000000000000000000000000000000000000000002386f2cafcf80300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000870f600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e5449334e6d5a6c4d4330775a6a55314c54566c4f446774596d55314d43316b4d7a4d315a4452694f47566a596a556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000050c4a39cbc66d7258a0805ac48b1aa0d386ba5710000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe6125d6467543b98ea09ee1dbf1c0cbe182310233da3fca2895bf0de75136f40",
      "signature": {
        "s": "0x36cac3896a5ed480ce8cfcce215cc434ae805d251bc2ee4ab42c147da404c049",
        "r": "0x6995c7d8add7981e9a1dd661ce6b5f995184bef9449e0d5f4cfcf5001c218063",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6ef146ec34fe238584b421e6b6453dc33cff5384170db9662437c20654aedd3c",
      "signature": {
        "s": "0x6613595c06353abab7e8bb73df1847e59bc70c4fb3992a5d5817b33b68d507c9",
        "r": "0xead90c4245d4c82511404113a46fb17efd6b3c1ac12da6e10724d04bee47b0ee",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19240",
    "total": "19240"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19240",
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
            "amount": "553206"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NTI3NmZlMC0wZjU1LTVlODgtYmU1MC1kMzM1ZDRiOGVjYjUifQ==",
    "nonce": 676,
    "balances": {
      "current": "10000001530637512",
      "previous": "10000001530656771"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x50c4a39cbc66d7258a0805ac48b1aa0d386ba571",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:53.914Z",
  "updated": "2020-05-22T08:03:53.995Z",
  "id": "5ec78769005df800101bc2f9"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19240`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``