# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x37175d4447AB2aAABba2eBF8A6D18f617c320D67`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000000000000000000000000000000000000a67978796c73b7c21a896edd1bc576f0db5b7ec6167b27c72cdfae9c854a988d7d6a4a60f6d2d21d5a5f93c6a58c90e4dac0b9f52d04a6f1bcf0a2ff7edbbe1fe94f4a0237e61937d7845eedd09ce701e4d08081e1034aa6d2ad9ba1a3f3bfc7b0cf4fd000000000000000000000000000000000000000000000000000000000000001c37ed796ccc16f691df945edd47b17910c97c37de957201507e20ccc08c63ae02f10683a1d8127270f9d51b72c755dea50fb0df3c28164d7a1bafeff51d55fea65dda2df4fd60c618511e616b8123a0fd03a06e43894c67078ba13b6298c9c9e1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001de600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b13b2f2b572000000000000000000000000000000000000000000000000002e0b13bd5cf6da00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002a9e1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b36513d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5957566c597a6b7a4d79316c4e4456684c5455774e574574596a55304e6931694f4463344e6a4d304f546b30596a496966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000037175d4447ab2aaabba2ebf8a6d18f617c320d67000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x96c73b7c21a896edd1bc576f0db5b7ec6167b27c72cdfae9c854a988d7d6a4a6",
      "signature": {
        "s": "0x237e61937d7845eedd09ce701e4d08081e1034aa6d2ad9ba1a3f3bfc7b0cf4fd",
        "r": "0x0f6d2d21d5a5f93c6a58c90e4dac0b9f52d04a6f1bcf0a2ff7edbbe1fe94f4a0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x37ed796ccc16f691df945edd47b17910c97c37de957201507e20ccc08c63ae02",
      "signature": {
        "s": "0x5dda2df4fd60c618511e616b8123a0fd03a06e43894c67078ba13b6298c9c9e1",
        "r": "0xf10683a1d8127270f9d51b72c755dea50fb0df3c28164d7a1bafeff51d55fea6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "174561159",
    "total": "174561159"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "174561159",
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
            "amount": "57633296701"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "174561"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYWVlYzkzMy1lNDVhLTUwNWEtYjU0Ni1iODc4NjM0OTk0YjIifQ==",
    "nonce": 7654,
    "balances": {
      "current": "12960028163224946",
      "previous": "12960028337960666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37175d4447ab2aaabba2ebf8a6d18f617c320d67",
    "nonce": 10,
    "balances": {
      "current": "174561159",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:26.504Z",
  "updated": "2020-05-22T08:58:26.572Z",
  "id": "5ec79432b0c6090011d5b2d1"
}
```
* *stageAmount*: `174561159`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000000000000000000000000000000000000a67978796c73b7c21a896edd1bc576f0db5b7ec6167b27c72cdfae9c854a988d7d6a4a60f6d2d21d5a5f93c6a58c90e4dac0b9f52d04a6f1bcf0a2ff7edbbe1fe94f4a0237e61937d7845eedd09ce701e4d08081e1034aa6d2ad9ba1a3f3bfc7b0cf4fd000000000000000000000000000000000000000000000000000000000000001c37ed796ccc16f691df945edd47b17910c97c37de957201507e20ccc08c63ae02f10683a1d8127270f9d51b72c755dea50fb0df3c28164d7a1bafeff51d55fea65dda2df4fd60c618511e616b8123a0fd03a06e43894c67078ba13b6298c9c9e1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001de600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b13b2f2b572000000000000000000000000000000000000000000000000002e0b13bd5cf6da00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002a9e1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b36513d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5957566c597a6b7a4d79316c4e4456684c5455774e574574596a55304e6931694f4463344e6a4d304f546b30596a496966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000037175d4447ab2aaabba2ebf8a6d18f617c320d67000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x96c73b7c21a896edd1bc576f0db5b7ec6167b27c72cdfae9c854a988d7d6a4a6",
      "signature": {
        "s": "0x237e61937d7845eedd09ce701e4d08081e1034aa6d2ad9ba1a3f3bfc7b0cf4fd",
        "r": "0x0f6d2d21d5a5f93c6a58c90e4dac0b9f52d04a6f1bcf0a2ff7edbbe1fe94f4a0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x37ed796ccc16f691df945edd47b17910c97c37de957201507e20ccc08c63ae02",
      "signature": {
        "s": "0x5dda2df4fd60c618511e616b8123a0fd03a06e43894c67078ba13b6298c9c9e1",
        "r": "0xf10683a1d8127270f9d51b72c755dea50fb0df3c28164d7a1bafeff51d55fea6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "174561159",
    "total": "174561159"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "174561159",
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
            "amount": "57633296701"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "174561"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYWVlYzkzMy1lNDVhLTUwNWEtYjU0Ni1iODc4NjM0OTk0YjIifQ==",
    "nonce": 7654,
    "balances": {
      "current": "12960028163224946",
      "previous": "12960028337960666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37175d4447ab2aaabba2ebf8a6d18f617c320d67",
    "nonce": 10,
    "balances": {
      "current": "174561159",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:26.504Z",
  "updated": "2020-05-22T08:58:26.572Z",
  "id": "5ec79432b0c6090011d5b2d1"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000a679787000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `174561159`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`