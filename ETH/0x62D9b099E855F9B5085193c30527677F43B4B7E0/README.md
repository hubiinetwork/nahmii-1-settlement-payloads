# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x62D9b099E855F9B5085193c30527677F43B4B7E0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28a4a1ee6d986ce837b174a76b25320b50ca95ca80abf84a93b54ed2b6d4ebb87736a5da82c1f5817869f8a0b1102d754d9daac03277e86a3cd17b6d4f76c562d53ec201e50c4e4f05b5010761d00d29a34d5697b058155a3fad659fb333850ebf000000000000000000000000000000000000000000000000000000000000001b8373a3d6a3f7de8779a0baa28aba4881cfd695f1ec6a6b7e0df666c846cee4dcc925de041d90a7182d558df6f86d1b3244dac3d715b02d1369883133793620b52eae0d21927918e9152e5b172686134a8c709d5c1ad630989ce7bc9bf4337a59000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ca000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002b300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf8c754000000000000000000000000000000000000000000000000002386f2caf9128f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000871f100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d544d334e5445345a5330314d5759324c54557859324d744f445a6a4e793078596a4179593245314e4755354e7a416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000062d9b099e855f9b5085193c30527677f43b4b7e00000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4a1ee6d986ce837b174a76b25320b50ca95ca80abf84a93b54ed2b6d4ebb877",
      "signature": {
        "s": "0x3ec201e50c4e4f05b5010761d00d29a34d5697b058155a3fad659fb333850ebf",
        "r": "0x36a5da82c1f5817869f8a0b1102d754d9daac03277e86a3cd17b6d4f76c562d5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8373a3d6a3f7de8779a0baa28aba4881cfd695f1ec6a6b7e0df666c846cee4dc",
      "signature": {
        "s": "0x2eae0d21927918e9152e5b172686134a8c709d5c1ad630989ce7bc9bf4337a59",
        "r": "0xc925de041d90a7182d558df6f86d1b3244dac3d715b02d1369883133793620b5",
        "v": 28
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
            "amount": "553457"
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
    "data": "eyJyZWYiOiI0MTM3NTE4ZS01MWY2LTUxY2MtODZjNy0xYjAyY2E1NGU5NzAifQ==",
    "nonce": 691,
    "balances": {
      "current": "10000001530382164",
      "previous": "10000001530401423"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62d9b099e855f9b5085193c30527677f43b4b7e0",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:57.660Z",
  "updated": "2020-05-22T08:03:57.732Z",
  "id": "5ec7876d005df800101bc2fe"
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
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004b2800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b280000000000000000000000000000000000000000000000000000000000004b28a4a1ee6d986ce837b174a76b25320b50ca95ca80abf84a93b54ed2b6d4ebb87736a5da82c1f5817869f8a0b1102d754d9daac03277e86a3cd17b6d4f76c562d53ec201e50c4e4f05b5010761d00d29a34d5697b058155a3fad659fb333850ebf000000000000000000000000000000000000000000000000000000000000001b8373a3d6a3f7de8779a0baa28aba4881cfd695f1ec6a6b7e0df666c846cee4dcc925de041d90a7182d558df6f86d1b3244dac3d715b02d1369883133793620b52eae0d21927918e9152e5b172686134a8c709d5c1ad630989ce7bc9bf4337a59000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ca000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002b300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf8c754000000000000000000000000000000000000000000000000002386f2caf9128f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000871f100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d544d334e5445345a5330314d5759324c54557859324d744f445a6a4e793078596a4179593245314e4755354e7a416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000062d9b099e855f9b5085193c30527677f43b4b7e00000000000000000000000000000000000000000000000000000000000004b28000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4a1ee6d986ce837b174a76b25320b50ca95ca80abf84a93b54ed2b6d4ebb877",
      "signature": {
        "s": "0x3ec201e50c4e4f05b5010761d00d29a34d5697b058155a3fad659fb333850ebf",
        "r": "0x36a5da82c1f5817869f8a0b1102d754d9daac03277e86a3cd17b6d4f76c562d5",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8373a3d6a3f7de8779a0baa28aba4881cfd695f1ec6a6b7e0df666c846cee4dc",
      "signature": {
        "s": "0x2eae0d21927918e9152e5b172686134a8c709d5c1ad630989ce7bc9bf4337a59",
        "r": "0xc925de041d90a7182d558df6f86d1b3244dac3d715b02d1369883133793620b5",
        "v": 28
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
            "amount": "553457"
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
    "data": "eyJyZWYiOiI0MTM3NTE4ZS01MWY2LTUxY2MtODZjNy0xYjAyY2E1NGU5NzAifQ==",
    "nonce": 691,
    "balances": {
      "current": "10000001530382164",
      "previous": "10000001530401423"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62d9b099e855f9b5085193c30527677f43b4b7e0",
    "nonce": 20,
    "balances": {
      "current": "19240",
      "previous": "0"
    }
  },
  "blockNumber": "10114506",
  "created": "2020-05-22T08:03:57.660Z",
  "updated": "2020-05-22T08:03:57.732Z",
  "id": "5ec7876d005df800101bc2fe"
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