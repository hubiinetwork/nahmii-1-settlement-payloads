# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4965Bda3b34c30e67BFeF41607a1Ea1E7d51118e`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000294eeda300000000000000000000000000000000000000000000000000000000294eeda3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000294eeda300000000000000000000000000000000000000000000000000000000294eeda3f01e17f1573a000edbe3b264ab23021c60b6aeed76071b7f74b6be63a98a589a20d3f4c6c52fa1ed7db7f1751191e8918318654eacc3f2c5ab179140c386e59d71a008649f20ecd940d8644826ffe3242e633579ee65158a62ab1e727f72a6a9000000000000000000000000000000000000000000000000000000000000001cd69d9a9f9f0a9e6ca4bf867465339ca71d978d585846c468ca87d0fc2678e5816029d8b333d31bbb87dfe6017826eb21440d6f5b1fe799b7a1cb4aa32cfacfbf1ac95d6168aaf2a09aab989155e67fcb620c97ff028cc06987f18f9dbd7dc6ba000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000179d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1749676e0c000000000000000000000000000000000000000000000000002e1b1772c0eedd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a932e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000952c42654000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a544a6d4e5441314e6930355a4751774c5455304e6d4974596d49774e793078596a4e6a4f47526d4d6a566c5a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000130000000000000000000000004965bda3b34c30e67bfef41607a1ea1e7d51118e00000000000000000000000000000000000000000000000000000000294eeda3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf01e17f1573a000edbe3b264ab23021c60b6aeed76071b7f74b6be63a98a589a",
      "signature": {
        "s": "0x71a008649f20ecd940d8644826ffe3242e633579ee65158a62ab1e727f72a6a9",
        "r": "0x20d3f4c6c52fa1ed7db7f1751191e8918318654eacc3f2c5ab179140c386e59d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd69d9a9f9f0a9e6ca4bf867465339ca71d978d585846c468ca87d0fc2678e581",
      "signature": {
        "s": "0x1ac95d6168aaf2a09aab989155e67fcb620c97ff028cc06987f18f9dbd7dc6ba",
        "r": "0x6029d8b333d31bbb87dfe6017826eb21440d6f5b1fe799b7a1cb4aa32cfacfbf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "693038499",
    "total": "693038499"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "693038499",
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
            "amount": "40043292244"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "693038"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZTJmNTA1Ni05ZGQwLTU0NmItYmIwNy0xYjNjOGRmMjVlZmUifQ==",
    "nonce": 6045,
    "balances": {
      "current": "12977635758403084",
      "previous": "12977636452134621"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4965bda3b34c30e67bfef41607a1ea1e7d51118e",
    "nonce": 19,
    "balances": {
      "current": "693038499",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:45:58.039Z",
  "updated": "2020-05-22T08:45:58.104Z",
  "id": "5ec79146e5756b00111b872c"
}
```
* *stageAmount*: `693038499`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000294eeda3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000294eeda300000000000000000000000000000000000000000000000000000000294eeda3f01e17f1573a000edbe3b264ab23021c60b6aeed76071b7f74b6be63a98a589a20d3f4c6c52fa1ed7db7f1751191e8918318654eacc3f2c5ab179140c386e59d71a008649f20ecd940d8644826ffe3242e633579ee65158a62ab1e727f72a6a9000000000000000000000000000000000000000000000000000000000000001cd69d9a9f9f0a9e6ca4bf867465339ca71d978d585846c468ca87d0fc2678e5816029d8b333d31bbb87dfe6017826eb21440d6f5b1fe799b7a1cb4aa32cfacfbf1ac95d6168aaf2a09aab989155e67fcb620c97ff028cc06987f18f9dbd7dc6ba000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000179d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1749676e0c000000000000000000000000000000000000000000000000002e1b1772c0eedd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a932e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000952c42654000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a544a6d4e5441314e6930355a4751774c5455304e6d4974596d49774e793078596a4e6a4f47526d4d6a566c5a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000130000000000000000000000004965bda3b34c30e67bfef41607a1ea1e7d51118e00000000000000000000000000000000000000000000000000000000294eeda3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf01e17f1573a000edbe3b264ab23021c60b6aeed76071b7f74b6be63a98a589a",
      "signature": {
        "s": "0x71a008649f20ecd940d8644826ffe3242e633579ee65158a62ab1e727f72a6a9",
        "r": "0x20d3f4c6c52fa1ed7db7f1751191e8918318654eacc3f2c5ab179140c386e59d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd69d9a9f9f0a9e6ca4bf867465339ca71d978d585846c468ca87d0fc2678e581",
      "signature": {
        "s": "0x1ac95d6168aaf2a09aab989155e67fcb620c97ff028cc06987f18f9dbd7dc6ba",
        "r": "0x6029d8b333d31bbb87dfe6017826eb21440d6f5b1fe799b7a1cb4aa32cfacfbf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "693038499",
    "total": "693038499"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "693038499",
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
            "amount": "40043292244"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "693038"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZTJmNTA1Ni05ZGQwLTU0NmItYmIwNy0xYjNjOGRmMjVlZmUifQ==",
    "nonce": 6045,
    "balances": {
      "current": "12977635758403084",
      "previous": "12977636452134621"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4965bda3b34c30e67bfef41607a1ea1e7d51118e",
    "nonce": 19,
    "balances": {
      "current": "693038499",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:45:58.039Z",
  "updated": "2020-05-22T08:45:58.104Z",
  "id": "5ec79146e5756b00111b872c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000294eeda3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `693038499`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`