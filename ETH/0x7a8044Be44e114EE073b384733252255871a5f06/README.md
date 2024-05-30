# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7a8044Be44e114EE073b384733252255871a5f06`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000030cb00000000000000000000000000000000000000000000000000000000000030cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000030cb00000000000000000000000000000000000000000000000000000000000030cb01605925207f24b71854bbdc0f825043aa336173eb5a36c0dbfa2ac891347638bb890ef421865a959f3c64aadf1e937398734ff87539494d3a80da3c80f4b9c31dbf7d9c0abda1beeee31fc7c1eb5b4e7a103ee2e49057019dcce3a9d6534b70000000000000000000000000000000000000000000000000000000000000001b7c045baabe7146907c5ace8ca204d2e472c7f5deff9227f48208d67c453b8445560e5babda1bae53412db8065e3b6ef0e11b67090898c40d0795df5c252419f20665b5fe5743cb9117ac6dc1cad0e715eb03713087764e97f169283e099e5392000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6bf57e000000000000000000000000000000000000000000000000002386f2bc6c265500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28ad00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a57466d4d32466a4d4331694e6a51304c545579596a5174596a466c4e43316c4f4441774e6a41334e444d7a5a44676966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000007a8044be44e114ee073b384733252255871a5f0600000000000000000000000000000000000000000000000000000000000030cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x01605925207f24b71854bbdc0f825043aa336173eb5a36c0dbfa2ac891347638",
      "signature": {
        "s": "0x1dbf7d9c0abda1beeee31fc7c1eb5b4e7a103ee2e49057019dcce3a9d6534b70",
        "r": "0xbb890ef421865a959f3c64aadf1e937398734ff87539494d3a80da3c80f4b9c3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c045baabe7146907c5ace8ca204d2e472c7f5deff9227f48208d67c453b8445",
      "signature": {
        "s": "0x0665b5fe5743cb9117ac6dc1cad0e715eb03713087764e97f169283e099e5392",
        "r": "0x560e5babda1bae53412db8065e3b6ef0e11b67090898c40d0795df5c252419f2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12491",
    "total": "12491"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12491",
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
            "amount": "796845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZWFmM2FjMC1iNjQ0LTUyYjQtYjFlNC1lODAwNjA3NDMzZDgifQ==",
    "nonce": 2209,
    "balances": {
      "current": "10000001286272382",
      "previous": "10000001286284885"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 10,
    "balances": {
      "current": "12491",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:03.280Z",
  "updated": "2020-05-22T08:15:03.353Z",
  "id": "5ec78a07e5756b00111b8242"
}
```
* *stageAmount*: `12491`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000030cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000030cb00000000000000000000000000000000000000000000000000000000000030cb01605925207f24b71854bbdc0f825043aa336173eb5a36c0dbfa2ac891347638bb890ef421865a959f3c64aadf1e937398734ff87539494d3a80da3c80f4b9c31dbf7d9c0abda1beeee31fc7c1eb5b4e7a103ee2e49057019dcce3a9d6534b70000000000000000000000000000000000000000000000000000000000000001b7c045baabe7146907c5ace8ca204d2e472c7f5deff9227f48208d67c453b8445560e5babda1bae53412db8065e3b6ef0e11b67090898c40d0795df5c252419f20665b5fe5743cb9117ac6dc1cad0e715eb03713087764e97f169283e099e5392000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f3000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008a100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6bf57e000000000000000000000000000000000000000000000000002386f2bc6c265500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c28ad00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a57466d4d32466a4d4331694e6a51304c545579596a5174596a466c4e43316c4f4441774e6a41334e444d7a5a44676966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000007a8044be44e114ee073b384733252255871a5f0600000000000000000000000000000000000000000000000000000000000030cb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x01605925207f24b71854bbdc0f825043aa336173eb5a36c0dbfa2ac891347638",
      "signature": {
        "s": "0x1dbf7d9c0abda1beeee31fc7c1eb5b4e7a103ee2e49057019dcce3a9d6534b70",
        "r": "0xbb890ef421865a959f3c64aadf1e937398734ff87539494d3a80da3c80f4b9c3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7c045baabe7146907c5ace8ca204d2e472c7f5deff9227f48208d67c453b8445",
      "signature": {
        "s": "0x0665b5fe5743cb9117ac6dc1cad0e715eb03713087764e97f169283e099e5392",
        "r": "0x560e5babda1bae53412db8065e3b6ef0e11b67090898c40d0795df5c252419f2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12491",
    "total": "12491"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12491",
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
            "amount": "796845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZWFmM2FjMC1iNjQ0LTUyYjQtYjFlNC1lODAwNjA3NDMzZDgifQ==",
    "nonce": 2209,
    "balances": {
      "current": "10000001286272382",
      "previous": "10000001286284885"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a8044be44e114ee073b384733252255871a5f06",
    "nonce": 10,
    "balances": {
      "current": "12491",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:03.280Z",
  "updated": "2020-05-22T08:15:03.353Z",
  "id": "5ec78a07e5756b00111b8242"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000030cb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12491`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``