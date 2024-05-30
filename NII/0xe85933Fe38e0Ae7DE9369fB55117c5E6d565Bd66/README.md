# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe85933Fe38e0Ae7DE9369fB55117c5E6d565Bd66`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000012eed9801ea86d37000000000000000000000000000000000000000000000000100db0f1d6bd3c7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000100db0f1d6bd3c7a00000000000000000000000000000000000000000000000012eed9801ea86d3754e918ca106bc94d11d48398bb10a702d9b230637e5ac20d7380454c7e9afa287189353b298cce20523c04d32845dc8d953a3dd416430c48b0f22dff22918112511a1c3632736b264a38faaf5559759569f9d76fe9168d9922f122f7fd216da5000000000000000000000000000000000000000000000000000000000000001bbb3947ef954bc5a0cb22f1b44af48ab1e1a740c789e45e364c9dc3048fc3438cae66b3a869c0b38cb32807136730ca62a8e8104f6bec8778f255dcedb836075561fa24238919f9b858566a22bc53e49a2bc0f375e4df7c235ca0c9c8fa5772ea000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dd8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002371f24f1a0f8a00c3570000000000000000000000000000000000000000000023720260e71619886db300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000041c14b8ca6de20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9a385601068c56350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a6c6a5a544d7a5953316a4d6a49774c5455355a6a63744f54526b4f53316c5a5755314e325a6d4e6d45344f54596966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000e85933fe38e0ae7de9369fb55117c5e6d565bd6600000000000000000000000000000000000000000000000012eed9801ea86d3700000000000000000000000000000000000000000000000002e1288e47eb30bd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x54e918ca106bc94d11d48398bb10a702d9b230637e5ac20d7380454c7e9afa28",
      "signature": {
        "s": "0x511a1c3632736b264a38faaf5559759569f9d76fe9168d9922f122f7fd216da5",
        "r": "0x7189353b298cce20523c04d32845dc8d953a3dd416430c48b0f22dff22918112",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb3947ef954bc5a0cb22f1b44af48ab1e1a740c789e45e364c9dc3048fc3438c",
      "signature": {
        "s": "0x61fa24238919f9b858566a22bc53e49a2bc0f375e4df7c235ca0c9c8fa5772ea",
        "r": "0xae66b3a869c0b38cb32807136730ca62a8e8104f6bec8778f255dcedb8360755",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1156775232040418426",
    "total": "1364266881433234743"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1156775232040418426",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "16816096577792343037493"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1156775232040418"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NzljZTMzYS1jMjIwLTU5ZjctOTRkOS1lZWU1N2ZmNmE4OTYifQ==",
    "nonce": 77272,
    "balances": {
      "current": "167384769183701142651735",
      "previous": "167385927115708415110579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe85933fe38e0ae7de9369fb55117c5e6d565bd66",
    "nonce": 2,
    "balances": {
      "current": "1364266881433234743",
      "previous": "207491649392816317"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:23.215Z",
  "updated": "2021-06-04T12:46:23.268Z",
  "id": "60ba209f0779920010014ba1"
}
```
* *stageAmount*: `1364266881433234743`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000100db0f1d6bd3c7a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000100db0f1d6bd3c7a00000000000000000000000000000000000000000000000012eed9801ea86d3754e918ca106bc94d11d48398bb10a702d9b230637e5ac20d7380454c7e9afa287189353b298cce20523c04d32845dc8d953a3dd416430c48b0f22dff22918112511a1c3632736b264a38faaf5559759569f9d76fe9168d9922f122f7fd216da5000000000000000000000000000000000000000000000000000000000000001bbb3947ef954bc5a0cb22f1b44af48ab1e1a740c789e45e364c9dc3048fc3438cae66b3a869c0b38cb32807136730ca62a8e8104f6bec8778f255dcedb836075561fa24238919f9b858566a22bc53e49a2bc0f375e4df7c235ca0c9c8fa5772ea000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dd8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002371f24f1a0f8a00c3570000000000000000000000000000000000000000000023720260e71619886db300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000041c14b8ca6de20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9a385601068c56350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a6c6a5a544d7a5953316a4d6a49774c5455355a6a63744f54526b4f53316c5a5755314e325a6d4e6d45344f54596966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000e85933fe38e0ae7de9369fb55117c5e6d565bd6600000000000000000000000000000000000000000000000012eed9801ea86d3700000000000000000000000000000000000000000000000002e1288e47eb30bd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x54e918ca106bc94d11d48398bb10a702d9b230637e5ac20d7380454c7e9afa28",
      "signature": {
        "s": "0x511a1c3632736b264a38faaf5559759569f9d76fe9168d9922f122f7fd216da5",
        "r": "0x7189353b298cce20523c04d32845dc8d953a3dd416430c48b0f22dff22918112",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb3947ef954bc5a0cb22f1b44af48ab1e1a740c789e45e364c9dc3048fc3438c",
      "signature": {
        "s": "0x61fa24238919f9b858566a22bc53e49a2bc0f375e4df7c235ca0c9c8fa5772ea",
        "r": "0xae66b3a869c0b38cb32807136730ca62a8e8104f6bec8778f255dcedb8360755",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1156775232040418426",
    "total": "1364266881433234743"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1156775232040418426",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "16816096577792343037493"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1156775232040418"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NzljZTMzYS1jMjIwLTU5ZjctOTRkOS1lZWU1N2ZmNmE4OTYifQ==",
    "nonce": 77272,
    "balances": {
      "current": "167384769183701142651735",
      "previous": "167385927115708415110579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe85933fe38e0ae7de9369fb55117c5e6d565bd66",
    "nonce": 2,
    "balances": {
      "current": "1364266881433234743",
      "previous": "207491649392816317"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:23.215Z",
  "updated": "2021-06-04T12:46:23.268Z",
  "id": "60ba209f0779920010014ba1"
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
0x0f200f9b00000000000000000000000000000000000000000000000012eed9801ea86d370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1364266881433234743`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`