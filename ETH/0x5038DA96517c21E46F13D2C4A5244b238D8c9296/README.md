# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5038DA96517c21E46F13D2C4A5244b238D8c9296`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002150900000000000000000000000000000000000000000000000000000000000215090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002150900000000000000000000000000000000000000000000000000000000000215099258995d353e74cd9aeedf6baa887dfb23d616bb7f9f9782962fa16d89aa7605b9446bb71724ca422a09841f3327fe245f3b156feb0a30d122de89694b2bcc2619a394fcb97ed452f3f66e09ff816083d887842da815595280ef9f231ec0a85b000000000000000000000000000000000000000000000000000000000000001c26d4e5131e4e5f7fba70a97dbd75d2fc88c40c951687d4f7c489ec48feb9686e45fa815aefe1d867777912e43e48cb546f46371ae336509dccc11dce6f1c39a611e73e8aa56aef2fcf1952741aed5ff0fff01b1fb21c1f5e4c60ad74c6366922000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d0a60db5000000000000000000000000000000000000000000000000002386f2d0a8234600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006fed000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f544e685a445a6b597931684d57526b4c5455784e6d4d744f445933596930354e544e6c4f57466d4d44597a4d6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000005038da96517c21e46f13d2c4a5244b238d8c92960000000000000000000000000000000000000000000000000000000000021509000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9258995d353e74cd9aeedf6baa887dfb23d616bb7f9f9782962fa16d89aa7605",
      "signature": {
        "s": "0x19a394fcb97ed452f3f66e09ff816083d887842da815595280ef9f231ec0a85b",
        "r": "0xb9446bb71724ca422a09841f3327fe245f3b156feb0a30d122de89694b2bcc26",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26d4e5131e4e5f7fba70a97dbd75d2fc88c40c951687d4f7c489ec48feb9686e",
      "signature": {
        "s": "0x11e73e8aa56aef2fcf1952741aed5ff0fff01b1fb21c1f5e4c60ad74c6366922",
        "r": "0x45fa815aefe1d867777912e43e48cb546f46371ae336509dccc11dce6f1c39a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "136457",
    "total": "136457"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "136457",
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
            "amount": "458448"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "136"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTNhZDZkYy1hMWRkLTUxNmMtODY3Yi05NTNlOWFmMDYzMjMifQ==",
    "nonce": 192,
    "balances": {
      "current": "10000001625623989",
      "previous": "10000001625760582"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5038da96517c21e46f13d2c4a5244b238d8c9296",
    "nonce": 10,
    "balances": {
      "current": "136457",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:18.198Z",
  "updated": "2020-05-22T08:00:18.275Z",
  "id": "5ec78692b0c6090011d5a913"
}
```
* *stageAmount*: `136457`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000215090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002150900000000000000000000000000000000000000000000000000000000000215099258995d353e74cd9aeedf6baa887dfb23d616bb7f9f9782962fa16d89aa7605b9446bb71724ca422a09841f3327fe245f3b156feb0a30d122de89694b2bcc2619a394fcb97ed452f3f66e09ff816083d887842da815595280ef9f231ec0a85b000000000000000000000000000000000000000000000000000000000000001c26d4e5131e4e5f7fba70a97dbd75d2fc88c40c951687d4f7c489ec48feb9686e45fa815aefe1d867777912e43e48cb546f46371ae336509dccc11dce6f1c39a611e73e8aa56aef2fcf1952741aed5ff0fff01b1fb21c1f5e4c60ad74c6366922000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d0a60db5000000000000000000000000000000000000000000000000002386f2d0a8234600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006fed000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f544e685a445a6b597931684d57526b4c5455784e6d4d744f445933596930354e544e6c4f57466d4d44597a4d6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000005038da96517c21e46f13d2c4a5244b238d8c92960000000000000000000000000000000000000000000000000000000000021509000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9258995d353e74cd9aeedf6baa887dfb23d616bb7f9f9782962fa16d89aa7605",
      "signature": {
        "s": "0x19a394fcb97ed452f3f66e09ff816083d887842da815595280ef9f231ec0a85b",
        "r": "0xb9446bb71724ca422a09841f3327fe245f3b156feb0a30d122de89694b2bcc26",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26d4e5131e4e5f7fba70a97dbd75d2fc88c40c951687d4f7c489ec48feb9686e",
      "signature": {
        "s": "0x11e73e8aa56aef2fcf1952741aed5ff0fff01b1fb21c1f5e4c60ad74c6366922",
        "r": "0x45fa815aefe1d867777912e43e48cb546f46371ae336509dccc11dce6f1c39a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "136457",
    "total": "136457"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "136457",
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
            "amount": "458448"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "136"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTNhZDZkYy1hMWRkLTUxNmMtODY3Yi05NTNlOWFmMDYzMjMifQ==",
    "nonce": 192,
    "balances": {
      "current": "10000001625623989",
      "previous": "10000001625760582"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5038da96517c21e46f13d2c4a5244b238d8c9296",
    "nonce": 10,
    "balances": {
      "current": "136457",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:18.198Z",
  "updated": "2020-05-22T08:00:18.275Z",
  "id": "5ec78692b0c6090011d5a913"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000215090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `136457`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``