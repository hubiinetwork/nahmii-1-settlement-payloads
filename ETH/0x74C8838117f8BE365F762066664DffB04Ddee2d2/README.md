# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x74C8838117f8BE365F762066664DffB04Ddee2d2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000006a2a0000000000000000000000000000000000000000000000000000000000006a2a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006a2a0000000000000000000000000000000000000000000000000000000000006a2a2ec5601d9b84c30a56f30c3d2b1d9e0d0f18d31aacef9046cef8897a49500b1684db6481e7987b3674363e027eef16fbac2e096e30fe44197c021832dcd3756b609dee9fd7bf63fe3fdd7072f74ad6c915b68186af0e4c894c5ba448c3ea319d000000000000000000000000000000000000000000000000000000000000001c8034a441c34f349a3229d5a8976e0aec9c3fa49779aaa9995e60e246c0c1a2958826d8a3abf32e445e76b00bb131a232d9dd650cd64f056e2418cbdfeb3d49837d61310ad83bf6ecbee6af6afbd66d8115bf6ee41dcc628a6366f7be8f770924000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000025a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb15852a000000000000000000000000000000000000000000000000002386f2cb15ef6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ab500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d54566a596d51354f43316a5a57517a4c5455344f544574596a56695a6930354d6a6730596d593559324a685a57516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000074c8838117f8be365f762066664dffb04ddee2d20000000000000000000000000000000000000000000000000000000000006a2a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2ec5601d9b84c30a56f30c3d2b1d9e0d0f18d31aacef9046cef8897a49500b16",
      "signature": {
        "s": "0x609dee9fd7bf63fe3fdd7072f74ad6c915b68186af0e4c894c5ba448c3ea319d",
        "r": "0x84db6481e7987b3674363e027eef16fbac2e096e30fe44197c021832dcd3756b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8034a441c34f349a3229d5a8976e0aec9c3fa49779aaa9995e60e246c0c1a295",
      "signature": {
        "s": "0x7d61310ad83bf6ecbee6af6afbd66d8115bf6ee41dcc628a6366f7be8f770924",
        "r": "0x8826d8a3abf32e445e76b00bb131a232d9dd650cd64f056e2418cbdfeb3d4983",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27178",
    "total": "27178"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27178",
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
            "amount": "551605"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTVjYmQ5OC1jZWQzLTU4OTEtYjViZi05Mjg0YmY5Y2JhZWQifQ==",
    "nonce": 602,
    "balances": {
      "current": "10000001532265770",
      "previous": "10000001532292975"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74c8838117f8be365f762066664dffb04ddee2d2",
    "nonce": 20,
    "balances": {
      "current": "27178",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:14.737Z",
  "updated": "2020-05-22T08:03:14.814Z",
  "id": "5ec78742005df800101bc2db"
}
```
* *stageAmount*: `27178`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000006a2a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006a2a0000000000000000000000000000000000000000000000000000000000006a2a2ec5601d9b84c30a56f30c3d2b1d9e0d0f18d31aacef9046cef8897a49500b1684db6481e7987b3674363e027eef16fbac2e096e30fe44197c021832dcd3756b609dee9fd7bf63fe3fdd7072f74ad6c915b68186af0e4c894c5ba448c3ea319d000000000000000000000000000000000000000000000000000000000000001c8034a441c34f349a3229d5a8976e0aec9c3fa49779aaa9995e60e246c0c1a2958826d8a3abf32e445e76b00bb131a232d9dd650cd64f056e2418cbdfeb3d49837d61310ad83bf6ecbee6af6afbd66d8115bf6ee41dcc628a6366f7be8f770924000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000025a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb15852a000000000000000000000000000000000000000000000000002386f2cb15ef6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ab500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d54566a596d51354f43316a5a57517a4c5455344f544574596a56695a6930354d6a6730596d593559324a685a57516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000074c8838117f8be365f762066664dffb04ddee2d20000000000000000000000000000000000000000000000000000000000006a2a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2ec5601d9b84c30a56f30c3d2b1d9e0d0f18d31aacef9046cef8897a49500b16",
      "signature": {
        "s": "0x609dee9fd7bf63fe3fdd7072f74ad6c915b68186af0e4c894c5ba448c3ea319d",
        "r": "0x84db6481e7987b3674363e027eef16fbac2e096e30fe44197c021832dcd3756b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8034a441c34f349a3229d5a8976e0aec9c3fa49779aaa9995e60e246c0c1a295",
      "signature": {
        "s": "0x7d61310ad83bf6ecbee6af6afbd66d8115bf6ee41dcc628a6366f7be8f770924",
        "r": "0x8826d8a3abf32e445e76b00bb131a232d9dd650cd64f056e2418cbdfeb3d4983",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27178",
    "total": "27178"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27178",
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
            "amount": "551605"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTVjYmQ5OC1jZWQzLTU4OTEtYjViZi05Mjg0YmY5Y2JhZWQifQ==",
    "nonce": 602,
    "balances": {
      "current": "10000001532265770",
      "previous": "10000001532292975"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x74c8838117f8be365f762066664dffb04ddee2d2",
    "nonce": 20,
    "balances": {
      "current": "27178",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:14.737Z",
  "updated": "2020-05-22T08:03:14.814Z",
  "id": "5ec78742005df800101bc2db"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000006a2a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27178`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``