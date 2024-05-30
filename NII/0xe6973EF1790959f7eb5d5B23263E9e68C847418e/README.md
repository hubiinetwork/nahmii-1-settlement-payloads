# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe6973EF1790959f7eb5d5B23263E9e68C847418e`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000d5f452e87950000000000000000000000000000000000000000000000000000000000000283f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000283f100000000000000000000000000000000000000000000000000000000003ab43eb1bf473635b3f095be419ed4b0f43091ace8b428a1828a730279c81cabf62fce42b3379f2312c003c092c8f37d464747f4063d27dd11af358c1b131003ed7350528f7419b1bba8bd8c72ed6f9528d3edd08ac67caf664d9d6fc4a7ca5462528f000000000000000000000000000000000000000000000000000000000000001c5c9ead8e010a828438c41f8d4f07d8ec8d19c4c0e8966733bc2648a37ec96115ae0891ebb880b4c6746f2a9e4c59b2b85642903bfe89b1d393f8657d58fdae460984187e6cdc6f3a40df24a2e69bb1653701edc3ca4880dc424baaf301f291f5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b42e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039cf1200ff83deddea180000000000000000000000000000000000000000000039cf1200ff83dee06ead00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd99371b28dbfce3b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d4759775a575133596930314f4467344c545578596a6374595745784f4330355a6a51784f574669596d46684d32596966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000e6973ef1790959f7eb5d5b23263e9e68c847418e000000000000000000000000000000000000000000000000000d5f452e879500000000000000000000000000000000000000000000000000000d5f452e85110f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb1bf473635b3f095be419ed4b0f43091ace8b428a1828a730279c81cabf62fce",
      "signature": {
        "s": "0x528f7419b1bba8bd8c72ed6f9528d3edd08ac67caf664d9d6fc4a7ca5462528f",
        "r": "0x42b3379f2312c003c092c8f37d464747f4063d27dd11af358c1b131003ed7350",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5c9ead8e010a828438c41f8d4f07d8ec8d19c4c0e8966733bc2648a37ec96115",
      "signature": {
        "s": "0x0984187e6cdc6f3a40df24a2e69bb1653701edc3ca4880dc424baaf301f291f5",
        "r": "0xae0891ebb880b4c6746f2a9e4c59b2b85642903bfe89b1d393f8657d58fdae46",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "164849",
    "total": "3847230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "164849",
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
            "amount": "27699603177511862461364"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "164"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMGYwZWQ3Yi01ODg4LTUxYjctYWExOC05ZjQxOWFiYmFhM2YifQ==",
    "nonce": 111662,
    "balances": {
      "current": "272994662864462181952024",
      "previous": "272994662864462182117037"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6973ef1790959f7eb5d5b23263e9e68c847418e",
    "nonce": 31,
    "balances": {
      "current": "3763925435258112",
      "previous": "3763925435093263"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:30.067Z",
  "updated": "2022-05-04T08:59:30.162Z",
  "id": "62724072bbd75600116d06ec"
}
```
* *stageAmount*: `3763925435258112`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000283f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000283f100000000000000000000000000000000000000000000000000000000003ab43eb1bf473635b3f095be419ed4b0f43091ace8b428a1828a730279c81cabf62fce42b3379f2312c003c092c8f37d464747f4063d27dd11af358c1b131003ed7350528f7419b1bba8bd8c72ed6f9528d3edd08ac67caf664d9d6fc4a7ca5462528f000000000000000000000000000000000000000000000000000000000000001c5c9ead8e010a828438c41f8d4f07d8ec8d19c4c0e8966733bc2648a37ec96115ae0891ebb880b4c6746f2a9e4c59b2b85642903bfe89b1d393f8657d58fdae460984187e6cdc6f3a40df24a2e69bb1653701edc3ca4880dc424baaf301f291f5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b42e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039cf1200ff83deddea180000000000000000000000000000000000000000000039cf1200ff83dee06ead00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd99371b28dbfce3b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d4759775a575133596930314f4467344c545578596a6374595745784f4330355a6a51784f574669596d46684d32596966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000e6973ef1790959f7eb5d5b23263e9e68c847418e000000000000000000000000000000000000000000000000000d5f452e879500000000000000000000000000000000000000000000000000000d5f452e85110f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb1bf473635b3f095be419ed4b0f43091ace8b428a1828a730279c81cabf62fce",
      "signature": {
        "s": "0x528f7419b1bba8bd8c72ed6f9528d3edd08ac67caf664d9d6fc4a7ca5462528f",
        "r": "0x42b3379f2312c003c092c8f37d464747f4063d27dd11af358c1b131003ed7350",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5c9ead8e010a828438c41f8d4f07d8ec8d19c4c0e8966733bc2648a37ec96115",
      "signature": {
        "s": "0x0984187e6cdc6f3a40df24a2e69bb1653701edc3ca4880dc424baaf301f291f5",
        "r": "0xae0891ebb880b4c6746f2a9e4c59b2b85642903bfe89b1d393f8657d58fdae46",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "164849",
    "total": "3847230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "164849",
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
            "amount": "27699603177511862461364"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "164"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMGYwZWQ3Yi01ODg4LTUxYjctYWExOC05ZjQxOWFiYmFhM2YifQ==",
    "nonce": 111662,
    "balances": {
      "current": "272994662864462181952024",
      "previous": "272994662864462182117037"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6973ef1790959f7eb5d5b23263e9e68c847418e",
    "nonce": 31,
    "balances": {
      "current": "3763925435258112",
      "previous": "3763925435093263"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:30.067Z",
  "updated": "2022-05-04T08:59:30.162Z",
  "id": "62724072bbd75600116d06ec"
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
0x0f200f9b000000000000000000000000000000000000000000000000000d5f452e8795000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3763925435258112`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`