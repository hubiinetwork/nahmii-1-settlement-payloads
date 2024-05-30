# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb8efFE4Cd13B9b269abA6BE8920fD235A555bCa2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000032b950000000000000000000000000000000000000000000000000000000000032b95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000032b950000000000000000000000000000000000000000000000000000000000032b954cc703e009a3ee98d964caafe483d01c59cf22b57df377c41f657f60f70c41ab2276cc5251f3d2f62959daa99f94e8d78b64d05d08a0be4d8c9d4a06b25f52ca5945d87b68f1e4396ba60b94d9475a8cf09c4dc3839a3c03e0a6a89586798dca000000000000000000000000000000000000000000000000000000000000001bb410ef68526ba104a31afcd74e83b8266d4f78d368925bc0eadc10506b81661361494436fef24d20de89b06f532cee85ea9cda377b618beed9d9f656190260447b79ef72e9292839cc7035fb1b7e1a3063f6e5bdfcf4a97b0a8b4e5cfa00f325000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e184b26423786000000000000000000000000000000000000000000000000002e184b264563ea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a09ea08e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4752694d5441784e4330774d325a6c4c5455784d6a63745957526a5a5330315a574e685a5445794d54686c597a556966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000b8effe4cd13b9b269aba6be8920fd235a555bca20000000000000000000000000000000000000000000000000000000000032b95000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4cc703e009a3ee98d964caafe483d01c59cf22b57df377c41f657f60f70c41ab",
      "signature": {
        "s": "0x5945d87b68f1e4396ba60b94d9475a8cf09c4dc3839a3c03e0a6a89586798dca",
        "r": "0x2276cc5251f3d2f62959daa99f94e8d78b64d05d08a0be4d8c9d4a06b25f52ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb410ef68526ba104a31afcd74e83b8266d4f78d368925bc0eadc10506b816613",
      "signature": {
        "s": "0x7b79ef72e9292839cc7035fb1b7e1a3063f6e5bdfcf4a97b0a8b4e5cfa00f325",
        "r": "0x61494436fef24d20de89b06f532cee85ea9cda377b618beed9d9f65619026044",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "207765",
    "total": "207765"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "207765",
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
            "amount": "43116005609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "207"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNGRiMTAxNC0wM2ZlLTUxMjctYWRjZS01ZWNhZTEyMThlYzUifQ==",
    "nonce": 6397,
    "balances": {
      "current": "12974559972177798",
      "previous": "12974559972385770"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8effe4cd13b9b269aba6be8920fd235a555bca2",
    "nonce": 6,
    "balances": {
      "current": "207765",
      "previous": "0"
    }
  },
  "blockNumber": "10114703",
  "created": "2020-05-22T08:48:45.848Z",
  "updated": "2020-05-22T08:48:45.924Z",
  "id": "5ec791edb0c6090011d5b118"
}
```
* *stageAmount*: `207765`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000032b95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000032b950000000000000000000000000000000000000000000000000000000000032b954cc703e009a3ee98d964caafe483d01c59cf22b57df377c41f657f60f70c41ab2276cc5251f3d2f62959daa99f94e8d78b64d05d08a0be4d8c9d4a06b25f52ca5945d87b68f1e4396ba60b94d9475a8cf09c4dc3839a3c03e0a6a89586798dca000000000000000000000000000000000000000000000000000000000000001bb410ef68526ba104a31afcd74e83b8266d4f78d368925bc0eadc10506b81661361494436fef24d20de89b06f532cee85ea9cda377b618beed9d9f656190260447b79ef72e9292839cc7035fb1b7e1a3063f6e5bdfcf4a97b0a8b4e5cfa00f325000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e184b26423786000000000000000000000000000000000000000000000000002e184b264563ea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a09ea08e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e4752694d5441784e4330774d325a6c4c5455784d6a63745957526a5a5330315a574e685a5445794d54686c597a556966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000b8effe4cd13b9b269aba6be8920fd235a555bca20000000000000000000000000000000000000000000000000000000000032b95000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4cc703e009a3ee98d964caafe483d01c59cf22b57df377c41f657f60f70c41ab",
      "signature": {
        "s": "0x5945d87b68f1e4396ba60b94d9475a8cf09c4dc3839a3c03e0a6a89586798dca",
        "r": "0x2276cc5251f3d2f62959daa99f94e8d78b64d05d08a0be4d8c9d4a06b25f52ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb410ef68526ba104a31afcd74e83b8266d4f78d368925bc0eadc10506b816613",
      "signature": {
        "s": "0x7b79ef72e9292839cc7035fb1b7e1a3063f6e5bdfcf4a97b0a8b4e5cfa00f325",
        "r": "0x61494436fef24d20de89b06f532cee85ea9cda377b618beed9d9f65619026044",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "207765",
    "total": "207765"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "207765",
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
            "amount": "43116005609"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "207"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNGRiMTAxNC0wM2ZlLTUxMjctYWRjZS01ZWNhZTEyMThlYzUifQ==",
    "nonce": 6397,
    "balances": {
      "current": "12974559972177798",
      "previous": "12974559972385770"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8effe4cd13b9b269aba6be8920fd235a555bca2",
    "nonce": 6,
    "balances": {
      "current": "207765",
      "previous": "0"
    }
  },
  "blockNumber": "10114703",
  "created": "2020-05-22T08:48:45.848Z",
  "updated": "2020-05-22T08:48:45.924Z",
  "id": "5ec791edb0c6090011d5b118"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000032b95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `207765`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`