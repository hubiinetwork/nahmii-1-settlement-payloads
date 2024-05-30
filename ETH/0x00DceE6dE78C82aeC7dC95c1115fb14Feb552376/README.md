# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x00DceE6dE78C82aeC7dC95c1115fb14Feb552376`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000db07000000000000000000000000000000000000000000000000000000000000db070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000db07000000000000000000000000000000000000000000000000000000000000db071a1932c355db87e1a840cc72551015ddcb5cbf13ba3b52b6658ee8f4d7d4dc6a3bf7483004e0b179257075213db6799492ea34c024b99ac490fb78003178903c6f6c070180ec5bc5e5b5380418450db93330ababbda66ee07f22199af3e05015000000000000000000000000000000000000000000000000000000000000001bb9e0033c9a2c55cd40778361ce5e4c2c5d6006d4434f149a39133fddf818df471620d20f2afb6f95a35a9a874c2e597f797c75e17d351710c8aa2b0fed8fe0182e1008d821f9f9de678c3c866264b3f1219e3202e9ce0c63c3e09268411b92d8000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000038a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cab40c46000000000000000000000000000000000000000000000000002386f2cab4e78500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008832f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e5455355957466b4e79316c4e444d354c5456684f4451744f5467355a4330355a44597a4e5455304d3259304d54416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000000dcee6de78c82aec7dc95c1115fb14feb552376000000000000000000000000000000000000000000000000000000000000db07000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1a1932c355db87e1a840cc72551015ddcb5cbf13ba3b52b6658ee8f4d7d4dc6a",
      "signature": {
        "s": "0x6f6c070180ec5bc5e5b5380418450db93330ababbda66ee07f22199af3e05015",
        "r": "0x3bf7483004e0b179257075213db6799492ea34c024b99ac490fb78003178903c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9e0033c9a2c55cd40778361ce5e4c2c5d6006d4434f149a39133fddf818df47",
      "signature": {
        "s": "0x2e1008d821f9f9de678c3c866264b3f1219e3202e9ce0c63c3e09268411b92d8",
        "r": "0x1620d20f2afb6f95a35a9a874c2e597f797c75e17d351710c8aa2b0fed8fe018",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56071",
    "total": "56071"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56071",
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
            "amount": "557871"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "56"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NTU5YWFkNy1lNDM5LTVhODQtOTg5ZC05ZDYzNTU0M2Y0MTAifQ==",
    "nonce": 906,
    "balances": {
      "current": "10000001525877830",
      "previous": "10000001525933957"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00dcee6de78c82aec7dc95c1115fb14feb552376",
    "nonce": 20,
    "balances": {
      "current": "56071",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:23.231Z",
  "updated": "2020-05-22T08:05:23.299Z",
  "id": "5ec787c3b0c6090011d5a9ff"
}
```
* *stageAmount*: `56071`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000db070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000db07000000000000000000000000000000000000000000000000000000000000db071a1932c355db87e1a840cc72551015ddcb5cbf13ba3b52b6658ee8f4d7d4dc6a3bf7483004e0b179257075213db6799492ea34c024b99ac490fb78003178903c6f6c070180ec5bc5e5b5380418450db93330ababbda66ee07f22199af3e05015000000000000000000000000000000000000000000000000000000000000001bb9e0033c9a2c55cd40778361ce5e4c2c5d6006d4434f149a39133fddf818df471620d20f2afb6f95a35a9a874c2e597f797c75e17d351710c8aa2b0fed8fe0182e1008d821f9f9de678c3c866264b3f1219e3202e9ce0c63c3e09268411b92d8000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000038a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cab40c46000000000000000000000000000000000000000000000000002386f2cab4e78500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008832f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e5455355957466b4e79316c4e444d354c5456684f4451744f5467355a4330355a44597a4e5455304d3259304d54416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000000dcee6de78c82aec7dc95c1115fb14feb552376000000000000000000000000000000000000000000000000000000000000db07000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1a1932c355db87e1a840cc72551015ddcb5cbf13ba3b52b6658ee8f4d7d4dc6a",
      "signature": {
        "s": "0x6f6c070180ec5bc5e5b5380418450db93330ababbda66ee07f22199af3e05015",
        "r": "0x3bf7483004e0b179257075213db6799492ea34c024b99ac490fb78003178903c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9e0033c9a2c55cd40778361ce5e4c2c5d6006d4434f149a39133fddf818df47",
      "signature": {
        "s": "0x2e1008d821f9f9de678c3c866264b3f1219e3202e9ce0c63c3e09268411b92d8",
        "r": "0x1620d20f2afb6f95a35a9a874c2e597f797c75e17d351710c8aa2b0fed8fe018",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56071",
    "total": "56071"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56071",
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
            "amount": "557871"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "56"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NTU5YWFkNy1lNDM5LTVhODQtOTg5ZC05ZDYzNTU0M2Y0MTAifQ==",
    "nonce": 906,
    "balances": {
      "current": "10000001525877830",
      "previous": "10000001525933957"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x00dcee6de78c82aec7dc95c1115fb14feb552376",
    "nonce": 20,
    "balances": {
      "current": "56071",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:23.231Z",
  "updated": "2020-05-22T08:05:23.299Z",
  "id": "5ec787c3b0c6090011d5a9ff"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000db070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `56071`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``