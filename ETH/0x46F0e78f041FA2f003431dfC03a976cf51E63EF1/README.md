# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x46F0e78f041FA2f003431dfC03a976cf51E63EF1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000174c000000000000000000000000000000000000000000000000000000000000174c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000174c000000000000000000000000000000000000000000000000000000000000174c7937cf87d401c26d9fbb6709a080dc4b9005c482d7d6d2d345b0cee2ef1769fae9a93a6adb696a0181a7d44dab792134d96cb3d9a5b103c13c4d34265fddc6ed33cb03f8d559e3fc7d2d4d6c903687a3114954f9b8074cf4217a8fa8bfe0b4b4000000000000000000000000000000000000000000000000000000000000001c614ec562a552c5a175cc20d3dbe786eff14b3b99836fd28a5246b0762d9ed14de8a790479b9169f093d17b63dacccf238581e765d9107636146ae7a564af90793c8dc4c92509661b17dc87c34ed8f8e4d6a636ccb4348a363ceb6fae03388253000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000047300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c8259d5b000000000000000000000000000000000000000000000000002386f2c825b4ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092a6f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e446b33596d557a4d7930784e3255794c5455334d5441744f475a6c597930344e446c6d4e7a41794d446b344e6d556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000046f0e78f041fa2f003431dfc03a976cf51e63ef1000000000000000000000000000000000000000000000000000000000000174c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7937cf87d401c26d9fbb6709a080dc4b9005c482d7d6d2d345b0cee2ef1769fa",
      "signature": {
        "s": "0x33cb03f8d559e3fc7d2d4d6c903687a3114954f9b8074cf4217a8fa8bfe0b4b4",
        "r": "0xe9a93a6adb696a0181a7d44dab792134d96cb3d9a5b103c13c4d34265fddc6ed",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x614ec562a552c5a175cc20d3dbe786eff14b3b99836fd28a5246b0762d9ed14d",
      "signature": {
        "s": "0x3c8dc4c92509661b17dc87c34ed8f8e4d6a636ccb4348a363ceb6fae03388253",
        "r": "0xe8a790479b9169f093d17b63dacccf238581e765d9107636146ae7a564af9079",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5964",
    "total": "5964"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5964",
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
            "amount": "600687"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNDk3YmUzMy0xN2UyLTU3MTAtOGZlYy04NDlmNzAyMDk4NmUifQ==",
    "nonce": 1139,
    "balances": {
      "current": "10000001482988891",
      "previous": "10000001482994860"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x46f0e78f041fa2f003431dfc03a976cf51e63ef1",
    "nonce": 20,
    "balances": {
      "current": "5964",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:07:04.173Z",
  "updated": "2020-05-22T08:07:04.522Z",
  "id": "5ec78828e5756b00111b80e4"
}
```
* *stageAmount*: `5964`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000174c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000174c000000000000000000000000000000000000000000000000000000000000174c7937cf87d401c26d9fbb6709a080dc4b9005c482d7d6d2d345b0cee2ef1769fae9a93a6adb696a0181a7d44dab792134d96cb3d9a5b103c13c4d34265fddc6ed33cb03f8d559e3fc7d2d4d6c903687a3114954f9b8074cf4217a8fa8bfe0b4b4000000000000000000000000000000000000000000000000000000000000001c614ec562a552c5a175cc20d3dbe786eff14b3b99836fd28a5246b0762d9ed14de8a790479b9169f093d17b63dacccf238581e765d9107636146ae7a564af90793c8dc4c92509661b17dc87c34ed8f8e4d6a636ccb4348a363ceb6fae03388253000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000047300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c8259d5b000000000000000000000000000000000000000000000000002386f2c825b4ac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000005000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092a6f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e446b33596d557a4d7930784e3255794c5455334d5441744f475a6c597930344e446c6d4e7a41794d446b344e6d556966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000046f0e78f041fa2f003431dfc03a976cf51e63ef1000000000000000000000000000000000000000000000000000000000000174c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7937cf87d401c26d9fbb6709a080dc4b9005c482d7d6d2d345b0cee2ef1769fa",
      "signature": {
        "s": "0x33cb03f8d559e3fc7d2d4d6c903687a3114954f9b8074cf4217a8fa8bfe0b4b4",
        "r": "0xe9a93a6adb696a0181a7d44dab792134d96cb3d9a5b103c13c4d34265fddc6ed",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x614ec562a552c5a175cc20d3dbe786eff14b3b99836fd28a5246b0762d9ed14d",
      "signature": {
        "s": "0x3c8dc4c92509661b17dc87c34ed8f8e4d6a636ccb4348a363ceb6fae03388253",
        "r": "0xe8a790479b9169f093d17b63dacccf238581e765d9107636146ae7a564af9079",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5964",
    "total": "5964"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5964",
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
            "amount": "600687"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNDk3YmUzMy0xN2UyLTU3MTAtOGZlYy04NDlmNzAyMDk4NmUifQ==",
    "nonce": 1139,
    "balances": {
      "current": "10000001482988891",
      "previous": "10000001482994860"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x46f0e78f041fa2f003431dfc03a976cf51e63ef1",
    "nonce": 20,
    "balances": {
      "current": "5964",
      "previous": "0"
    }
  },
  "blockNumber": "10114519",
  "created": "2020-05-22T08:07:04.173Z",
  "updated": "2020-05-22T08:07:04.522Z",
  "id": "5ec78828e5756b00111b80e4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000174c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5964`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``