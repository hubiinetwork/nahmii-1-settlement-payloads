# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8a525d01f8bd4dd761A3f0e9F6E0F1e432804f22`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000048ce11339bec23877c600000000000000000000000000000000000000000000001b9e3333fec8c92c340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001b9e3333fec8c92c34000000000000000000000000000000000000000000000306fcafc79ea0aa5973a4f0fb9169c7a202effbb1f3687e181408ac6eda2a0cc38b79c695f0f40aa6d98c2376c6249e596d7ae521ea8f27b5d84b5b25136f95b200e55a0634588378040958143cc5e9370c0471b7fe79d67d39251eac0396910a7b8c2fbca65174419d000000000000000000000000000000000000000000000000000000000000001c900952b924bb9d3defbcd790d66f97f5b5e6fa19380461fe37edba016074505b4642274c12055b361d125d0cdcba74140223c9b3fc06b563f6b23191de6bee9974c2b5cbc0c26ab72b7eae01d791c63527ca3d17a278e557e612619f68c89ed1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b048000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f04cef88057650ff212000000000000000000000000000000000000000000004f20743dacf6f225186d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000711f8a0c44bfa270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82c9746406ea6a94f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4756684d3249314e6930354e7a45354c545578593251744f4455315a533078597a4a6b4f475a6b4e6d4e6d5a47516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008a525d01f8bd4dd761a3f0e9f6e0f1e432804f2200000000000000000000000000000000000000000000048ce11339bec23877c600000000000000000000000000000000000000000000047142e005bff96f4b9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4f0fb9169c7a202effbb1f3687e181408ac6eda2a0cc38b79c695f0f40aa6d9",
      "signature": {
        "s": "0x0958143cc5e9370c0471b7fe79d67d39251eac0396910a7b8c2fbca65174419d",
        "r": "0x8c2376c6249e596d7ae521ea8f27b5d84b5b25136f95b200e55a063458837804",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x900952b924bb9d3defbcd790d66f97f5b5e6fa19380461fe37edba016074505b",
      "signature": {
        "s": "0x74c2b5cbc0c26ab72b7eae01d791c63527ca3d17a278e557e612619f68c89ed1",
        "r": "0x4642274c12055b361d125d0cdcba74140223c9b3fc06b563f6b23191de6bee99",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "509461602241346087988",
    "total": "14295987904353789434227"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "509461602241346087988",
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
            "amount": "27599542248371189623119"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "509461602241346087"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGVhM2I1Ni05NzE5LTUxY2QtODU1ZS0xYzJkOGZkNmNmZGQifQ==",
    "nonce": 110664,
    "balances": {
      "current": "373155652934275693539858",
      "previous": "373665623998119280973933"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8a525d01f8bd4dd761a3f0e9f6e0f1e432804f22",
    "nonce": 46,
    "balances": {
      "current": "21488228471972474419142",
      "previous": "20978766869731128331154"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:24.762Z",
  "updated": "2022-05-04T08:54:24.831Z",
  "id": "62723f403592fd001130b521"
}
```
* *stageAmount*: `21488228471972474419142`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001b9e3333fec8c92c340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001b9e3333fec8c92c34000000000000000000000000000000000000000000000306fcafc79ea0aa5973a4f0fb9169c7a202effbb1f3687e181408ac6eda2a0cc38b79c695f0f40aa6d98c2376c6249e596d7ae521ea8f27b5d84b5b25136f95b200e55a0634588378040958143cc5e9370c0471b7fe79d67d39251eac0396910a7b8c2fbca65174419d000000000000000000000000000000000000000000000000000000000000001c900952b924bb9d3defbcd790d66f97f5b5e6fa19380461fe37edba016074505b4642274c12055b361d125d0cdcba74140223c9b3fc06b563f6b23191de6bee9974c2b5cbc0c26ab72b7eae01d791c63527ca3d17a278e557e612619f68c89ed1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b048000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f04cef88057650ff212000000000000000000000000000000000000000000004f20743dacf6f225186d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000711f8a0c44bfa270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d82c9746406ea6a94f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4756684d3249314e6930354e7a45354c545578593251744f4455315a533078597a4a6b4f475a6b4e6d4e6d5a47516966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008a525d01f8bd4dd761a3f0e9f6e0f1e432804f2200000000000000000000000000000000000000000000048ce11339bec23877c600000000000000000000000000000000000000000000047142e005bff96f4b9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa4f0fb9169c7a202effbb1f3687e181408ac6eda2a0cc38b79c695f0f40aa6d9",
      "signature": {
        "s": "0x0958143cc5e9370c0471b7fe79d67d39251eac0396910a7b8c2fbca65174419d",
        "r": "0x8c2376c6249e596d7ae521ea8f27b5d84b5b25136f95b200e55a063458837804",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x900952b924bb9d3defbcd790d66f97f5b5e6fa19380461fe37edba016074505b",
      "signature": {
        "s": "0x74c2b5cbc0c26ab72b7eae01d791c63527ca3d17a278e557e612619f68c89ed1",
        "r": "0x4642274c12055b361d125d0cdcba74140223c9b3fc06b563f6b23191de6bee99",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "509461602241346087988",
    "total": "14295987904353789434227"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "509461602241346087988",
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
            "amount": "27599542248371189623119"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "509461602241346087"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGVhM2I1Ni05NzE5LTUxY2QtODU1ZS0xYzJkOGZkNmNmZGQifQ==",
    "nonce": 110664,
    "balances": {
      "current": "373155652934275693539858",
      "previous": "373665623998119280973933"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8a525d01f8bd4dd761a3f0e9f6e0f1e432804f22",
    "nonce": 46,
    "balances": {
      "current": "21488228471972474419142",
      "previous": "20978766869731128331154"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:24.762Z",
  "updated": "2022-05-04T08:54:24.831Z",
  "id": "62723f403592fd001130b521"
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
0x0f200f9b00000000000000000000000000000000000000000000048ce11339bec23877c60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `21488228471972474419142`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`