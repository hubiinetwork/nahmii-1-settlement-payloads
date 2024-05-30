# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x99891C3EE39876449427B2028048305Eefcb69eD`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000001249ac18220000000000000000000000000000000000000000000000000000001249ac1822000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001249ac18220000000000000000000000000000000000000000000000000000001249ac18224c281d3ef2673730e5a3f6f0ef16c5e2b1c96bd214d76c846c0e31f70e4fa741c137b4756227bbaa958625f91ee6ddaa98f575384371082b94b976aa5baecbe63a440a02687d5bb7f76252bc59bcbd0e882dfe56c8c2eb2f939d4647ffa09195000000000000000000000000000000000000000000000000000000000000001b9295ab477399a96b2187ae9b2960c640bc178458258d6a14d0f5e14fec6cc171318a2d1638d29035fc3dc31d45497f4c3e54bdc17f5d02776a10b10fc6b79f144f924490f6113d314ca16fd547984f6e3ec0868fa73b1b5f845cda30006a2225000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000146100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e3c60dc5eb816000000000000000000000000000000000000000000000000002e3c732ab9524a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000004ae8212000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cf6c2ffc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a68685a4755785979316a4f5751794c5455344d575974596a55785a4330325a47517a4f544d345a6a63344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000099891c3ee39876449427b2028048305eefcb69ed0000000000000000000000000000000000000000000000000000001249ac1822000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c281d3ef2673730e5a3f6f0ef16c5e2b1c96bd214d76c846c0e31f70e4fa741",
      "signature": {
        "s": "0x3a440a02687d5bb7f76252bc59bcbd0e882dfe56c8c2eb2f939d4647ffa09195",
        "r": "0xc137b4756227bbaa958625f91ee6ddaa98f575384371082b94b976aa5baecbe6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9295ab477399a96b2187ae9b2960c640bc178458258d6a14d0f5e14fec6cc171",
      "signature": {
        "s": "0x4f924490f6113d314ca16fd547984f6e3ec0868fa73b1b5f845cda30006a2225",
        "r": "0x318a2d1638d29035fc3dc31d45497f4c3e54bdc17f5d02776a10b10fc6b79f14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "78545426466",
    "total": "78545426466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78545426466",
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
            "amount": "3479973884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "78545426"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjhhZGUxYy1jOWQyLTU4MWYtYjUxZC02ZGQzOTM4Zjc4MjcifQ==",
    "nonce": 5217,
    "balances": {
      "current": "13014235640412182",
      "previous": "13014314264384074"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x99891c3ee39876449427b2028048305eefcb69ed",
    "nonce": 15,
    "balances": {
      "current": "78545426466",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:25.084Z",
  "updated": "2020-05-22T08:39:25.241Z",
  "id": "5ec78fbd005df800101bc904"
}
```
* *stageAmount*: `78545426466`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000001249ac1822000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001249ac18220000000000000000000000000000000000000000000000000000001249ac18224c281d3ef2673730e5a3f6f0ef16c5e2b1c96bd214d76c846c0e31f70e4fa741c137b4756227bbaa958625f91ee6ddaa98f575384371082b94b976aa5baecbe63a440a02687d5bb7f76252bc59bcbd0e882dfe56c8c2eb2f939d4647ffa09195000000000000000000000000000000000000000000000000000000000000001b9295ab477399a96b2187ae9b2960c640bc178458258d6a14d0f5e14fec6cc171318a2d1638d29035fc3dc31d45497f4c3e54bdc17f5d02776a10b10fc6b79f144f924490f6113d314ca16fd547984f6e3ec0868fa73b1b5f845cda30006a2225000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56600000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000146100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e3c60dc5eb816000000000000000000000000000000000000000000000000002e3c732ab9524a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000004ae8212000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cf6c2ffc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a68685a4755785979316a4f5751794c5455344d575974596a55785a4330325a47517a4f544d345a6a63344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000000f00000000000000000000000099891c3ee39876449427b2028048305eefcb69ed0000000000000000000000000000000000000000000000000000001249ac1822000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4c281d3ef2673730e5a3f6f0ef16c5e2b1c96bd214d76c846c0e31f70e4fa741",
      "signature": {
        "s": "0x3a440a02687d5bb7f76252bc59bcbd0e882dfe56c8c2eb2f939d4647ffa09195",
        "r": "0xc137b4756227bbaa958625f91ee6ddaa98f575384371082b94b976aa5baecbe6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9295ab477399a96b2187ae9b2960c640bc178458258d6a14d0f5e14fec6cc171",
      "signature": {
        "s": "0x4f924490f6113d314ca16fd547984f6e3ec0868fa73b1b5f845cda30006a2225",
        "r": "0x318a2d1638d29035fc3dc31d45497f4c3e54bdc17f5d02776a10b10fc6b79f14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "78545426466",
    "total": "78545426466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78545426466",
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
            "amount": "3479973884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "78545426"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNjhhZGUxYy1jOWQyLTU4MWYtYjUxZC02ZGQzOTM4Zjc4MjcifQ==",
    "nonce": 5217,
    "balances": {
      "current": "13014235640412182",
      "previous": "13014314264384074"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x99891c3ee39876449427b2028048305eefcb69ed",
    "nonce": 15,
    "balances": {
      "current": "78545426466",
      "previous": "0"
    }
  },
  "blockNumber": "10114656",
  "created": "2020-05-22T08:39:25.084Z",
  "updated": "2020-05-22T08:39:25.241Z",
  "id": "5ec78fbd005df800101bc904"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000001249ac1822000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `78545426466`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`