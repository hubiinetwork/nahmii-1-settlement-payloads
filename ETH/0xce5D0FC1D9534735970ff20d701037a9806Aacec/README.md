# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xce5D0FC1D9534735970ff20d701037a9806Aacec`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000078400000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000078400000000000000000000000000000000000000000000000000000000000007847a70103517760a3e14016366e38d2f2a7616e1034c045c1ffd2e550a9091ffb5e3fcf243202c3357b5e7c05be229b3dbf12c17b333b1c194653311112af05c852fbdbcd03bd5265b1e4045ffd94d89050d9a929e0f487e8346c33ecb99d07823000000000000000000000000000000000000000000000000000000000000001be5aa0a59d562a961e108ab1451fdb77db9007e2341e6c535694cd47732708d268600bfb172e159f73758cc157846a527d8cfd3c4a32b4117f2651de2ce557ea365a137a88b740fa50a34b4d9971e682014f36fbd13c327d8a551fa88ca59a4c3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003c100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caabaa6e000000000000000000000000000000000000000000000000002386f2caabb1f300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008853d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d49314d4441335a433033596a4e6d4c5456684d6a4d744f446b79596930784e3255794f474a685a6a41314d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ce5d0fc1d9534735970ff20d701037a9806aacec0000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7a70103517760a3e14016366e38d2f2a7616e1034c045c1ffd2e550a9091ffb5",
      "signature": {
        "s": "0x2fbdbcd03bd5265b1e4045ffd94d89050d9a929e0f487e8346c33ecb99d07823",
        "r": "0xe3fcf243202c3357b5e7c05be229b3dbf12c17b333b1c194653311112af05c85",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5aa0a59d562a961e108ab1451fdb77db9007e2341e6c535694cd47732708d26",
      "signature": {
        "s": "0x65a137a88b740fa50a34b4d9971e682014f36fbd13c327d8a551fa88ca59a4c3",
        "r": "0x8600bfb172e159f73758cc157846a527d8cfd3c4a32b4117f2651de2ce557ea3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1924",
    "total": "1924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1924",
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
            "amount": "558397"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMmI1MDA3ZC03YjNmLTVhMjMtODkyYi0xN2UyOGJhZjA1MmUifQ==",
    "nonce": 961,
    "balances": {
      "current": "10000001525328494",
      "previous": "10000001525330419"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce5d0fc1d9534735970ff20d701037a9806aacec",
    "nonce": 20,
    "balances": {
      "current": "1924",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:51.934Z",
  "updated": "2020-05-22T08:05:52.006Z",
  "id": "5ec787df005df800101bc358"
}
```
* *stageAmount*: `1924`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000078400000000000000000000000000000000000000000000000000000000000007847a70103517760a3e14016366e38d2f2a7616e1034c045c1ffd2e550a9091ffb5e3fcf243202c3357b5e7c05be229b3dbf12c17b333b1c194653311112af05c852fbdbcd03bd5265b1e4045ffd94d89050d9a929e0f487e8346c33ecb99d07823000000000000000000000000000000000000000000000000000000000000001be5aa0a59d562a961e108ab1451fdb77db9007e2341e6c535694cd47732708d268600bfb172e159f73758cc157846a527d8cfd3c4a32b4117f2651de2ce557ea365a137a88b740fa50a34b4d9971e682014f36fbd13c327d8a551fa88ca59a4c3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003c100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caabaa6e000000000000000000000000000000000000000000000000002386f2caabb1f300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008853d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d49314d4441335a433033596a4e6d4c5456684d6a4d744f446b79596930784e3255794f474a685a6a41314d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ce5d0fc1d9534735970ff20d701037a9806aacec0000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7a70103517760a3e14016366e38d2f2a7616e1034c045c1ffd2e550a9091ffb5",
      "signature": {
        "s": "0x2fbdbcd03bd5265b1e4045ffd94d89050d9a929e0f487e8346c33ecb99d07823",
        "r": "0xe3fcf243202c3357b5e7c05be229b3dbf12c17b333b1c194653311112af05c85",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5aa0a59d562a961e108ab1451fdb77db9007e2341e6c535694cd47732708d26",
      "signature": {
        "s": "0x65a137a88b740fa50a34b4d9971e682014f36fbd13c327d8a551fa88ca59a4c3",
        "r": "0x8600bfb172e159f73758cc157846a527d8cfd3c4a32b4117f2651de2ce557ea3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1924",
    "total": "1924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1924",
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
            "amount": "558397"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMmI1MDA3ZC03YjNmLTVhMjMtODkyYi0xN2UyOGJhZjA1MmUifQ==",
    "nonce": 961,
    "balances": {
      "current": "10000001525328494",
      "previous": "10000001525330419"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce5d0fc1d9534735970ff20d701037a9806aacec",
    "nonce": 20,
    "balances": {
      "current": "1924",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:51.934Z",
  "updated": "2020-05-22T08:05:52.006Z",
  "id": "5ec787df005df800101bc358"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1924`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``