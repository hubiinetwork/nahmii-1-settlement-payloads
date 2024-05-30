# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x357741326F9A4D4ED6d923DB5942092a3Ec01147`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000008ee30000000000000000000000000000000000000000000000000000000000008ee300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008ee30000000000000000000000000000000000000000000000000000000000008ee33e7ba7adefaf0f6b6e49e2be30f1073bd558586fa999810604bd006bddc720acaff8d20d3a1b3dcf28d085eae32fa665b4be7f50afff71e99d4815b2e1aea5a14e5df69db79a3696e2d3c6e8b5da2082bf78365d908916c3b86042b1cbd23fd5000000000000000000000000000000000000000000000000000000000000001c18cd2199e15a52b1afb4877d0eb9257361f816682a6b85871710db9a896f76f8e097cc9bf7dbaa5fbfeaa5fae9e71a95c8d8e8f78421ab036547ca2dd81f5efb342a2fb1719712864106f4672f6e09b01ffb7480c32085df6ea6ed57699150d7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000065c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5f4a5d6000000000000000000000000000000000000000000000000002386f2c5f534dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b95400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5467315a574d344d6931684f474d774c5455354f57517459575a6d4f43316d4e546c6a4d44426b596a6b7a4e57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000357741326f9a4d4ed6d923db5942092a3ec011470000000000000000000000000000000000000000000000000000000000008ee3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e7ba7adefaf0f6b6e49e2be30f1073bd558586fa999810604bd006bddc720ac",
      "signature": {
        "s": "0x4e5df69db79a3696e2d3c6e8b5da2082bf78365d908916c3b86042b1cbd23fd5",
        "r": "0xaff8d20d3a1b3dcf28d085eae32fa665b4be7f50afff71e99d4815b2e1aea5a1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x18cd2199e15a52b1afb4877d0eb9257361f816682a6b85871710db9a896f76f8",
      "signature": {
        "s": "0x342a2fb1719712864106f4672f6e09b01ffb7480c32085df6ea6ed57699150d7",
        "r": "0xe097cc9bf7dbaa5fbfeaa5fae9e71a95c8d8e8f78421ab036547ca2dd81f5efb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "36579",
    "total": "36579"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36579",
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
            "amount": "637268"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTg1ZWM4Mi1hOGMwLTU5OWQtYWZmOC1mNTljMDBkYjkzNWUifQ==",
    "nonce": 1628,
    "balances": {
      "current": "10000001446225366",
      "previous": "10000001446261981"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x357741326f9a4d4ed6d923db5942092a3ec01147",
    "nonce": 20,
    "balances": {
      "current": "36579",
      "previous": "0"
    }
  },
  "blockNumber": "10114536",
  "created": "2020-05-22T08:10:57.010Z",
  "updated": "2020-05-22T08:10:57.083Z",
  "id": "5ec78911e5756b00111b817b"
}
```
* *stageAmount*: `36579`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000008ee300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008ee30000000000000000000000000000000000000000000000000000000000008ee33e7ba7adefaf0f6b6e49e2be30f1073bd558586fa999810604bd006bddc720acaff8d20d3a1b3dcf28d085eae32fa665b4be7f50afff71e99d4815b2e1aea5a14e5df69db79a3696e2d3c6e8b5da2082bf78365d908916c3b86042b1cbd23fd5000000000000000000000000000000000000000000000000000000000000001c18cd2199e15a52b1afb4877d0eb9257361f816682a6b85871710db9a896f76f8e097cc9bf7dbaa5fbfeaa5fae9e71a95c8d8e8f78421ab036547ca2dd81f5efb342a2fb1719712864106f4672f6e09b01ffb7480c32085df6ea6ed57699150d7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000065c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5f4a5d6000000000000000000000000000000000000000000000000002386f2c5f534dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b95400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5467315a574d344d6931684f474d774c5455354f57517459575a6d4f43316d4e546c6a4d44426b596a6b7a4e57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000357741326f9a4d4ed6d923db5942092a3ec011470000000000000000000000000000000000000000000000000000000000008ee3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e7ba7adefaf0f6b6e49e2be30f1073bd558586fa999810604bd006bddc720ac",
      "signature": {
        "s": "0x4e5df69db79a3696e2d3c6e8b5da2082bf78365d908916c3b86042b1cbd23fd5",
        "r": "0xaff8d20d3a1b3dcf28d085eae32fa665b4be7f50afff71e99d4815b2e1aea5a1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x18cd2199e15a52b1afb4877d0eb9257361f816682a6b85871710db9a896f76f8",
      "signature": {
        "s": "0x342a2fb1719712864106f4672f6e09b01ffb7480c32085df6ea6ed57699150d7",
        "r": "0xe097cc9bf7dbaa5fbfeaa5fae9e71a95c8d8e8f78421ab036547ca2dd81f5efb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "36579",
    "total": "36579"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36579",
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
            "amount": "637268"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTg1ZWM4Mi1hOGMwLTU5OWQtYWZmOC1mNTljMDBkYjkzNWUifQ==",
    "nonce": 1628,
    "balances": {
      "current": "10000001446225366",
      "previous": "10000001446261981"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x357741326f9a4d4ed6d923db5942092a3ec01147",
    "nonce": 20,
    "balances": {
      "current": "36579",
      "previous": "0"
    }
  },
  "blockNumber": "10114536",
  "created": "2020-05-22T08:10:57.010Z",
  "updated": "2020-05-22T08:10:57.083Z",
  "id": "5ec78911e5756b00111b817b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000008ee30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36579`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``