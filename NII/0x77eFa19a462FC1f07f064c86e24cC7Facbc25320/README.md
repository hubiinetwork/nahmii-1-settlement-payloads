# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x77eFa19a462FC1f07f064c86e24cC7Facbc25320`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000037d522b3c066319ae0000000000000000000000000000000000000000000000000000000233a83a140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000233a83a140000000000000000000000000000000000000000000000000000003362a3fdb6d350f50f0b79584e48547b59da1e29e6e63cfe7df2b4112862c338fc312587e136939f91773689ce16a67a9a46808339bfd9f82acde9b3f69d5b70077c2aaa4d7769c895eca094b291e33d691cd0ac2300ae3e74ebb9008afb03da3928a7409d000000000000000000000000000000000000000000000000000000000000001c953c0b600baf21dded2fcf35276aa3edda0a508c3b0c1885a4da4bff7ff733dec984573e9e1c6fab80abccbfd3d1b0385670493394143a96ef14337488f41a3843afae68d4e87dd3b11fc07efb92dfb21fde3eb9adb0cb6431fb994036dd1f03000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b297000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000479827af2eb7f438924900000000000000000000000000000000000000000000479827af2eba2871183200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000904bd50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da12ac101d8df6eb7b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a544534595445794d6930775a6d45354c5455775a6a4d74596d59794e533168596d4d325a4445354e325a6b4f57596966513d3d000000000000000000000000000000000000000000000000000000000000001f00000000000000000000000077efa19a462fc1f07f064c86e24cc7facbc253200000000000000000000000000000000000000000000000037d522b3c066319ae0000000000000000000000000000000000000000000000037d522b39d2badf9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd350f50f0b79584e48547b59da1e29e6e63cfe7df2b4112862c338fc312587e1",
      "signature": {
        "s": "0x7769c895eca094b291e33d691cd0ac2300ae3e74ebb9008afb03da3928a7409d",
        "r": "0x36939f91773689ce16a67a9a46808339bfd9f82acde9b3f69d5b70077c2aaa4d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x953c0b600baf21dded2fcf35276aa3edda0a508c3b0c1885a4da4bff7ff733de",
      "signature": {
        "s": "0x43afae68d4e87dd3b11fc07efb92dfb21fde3eb9adb0cb6431fb994036dd1f03",
        "r": "0xc984573e9e1c6fab80abccbfd3d1b0385670493394143a96ef14337488f41a38",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9456597524",
    "total": "220698246582"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9456597524",
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
            "amount": "27634568090524707122043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9456597"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTE4YTEyMi0wZmE5LTUwZjMtYmYyNS1hYmM2ZDE5N2ZkOWYifQ==",
    "nonce": 111255,
    "balances": {
      "current": "338094784938604676813385",
      "previous": "338094784938614142867506"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77efa19a462fc1f07f064c86e24cc7facbc25320",
    "nonce": 31,
    "balances": {
      "current": "64370559960765110702",
      "previous": "64370559951308513178"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:21.449Z",
  "updated": "2022-05-04T08:57:21.517Z",
  "id": "62723ff1bbd75600116d0672"
}
```
* *stageAmount*: `64370559960765110702`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000233a83a140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000233a83a140000000000000000000000000000000000000000000000000000003362a3fdb6d350f50f0b79584e48547b59da1e29e6e63cfe7df2b4112862c338fc312587e136939f91773689ce16a67a9a46808339bfd9f82acde9b3f69d5b70077c2aaa4d7769c895eca094b291e33d691cd0ac2300ae3e74ebb9008afb03da3928a7409d000000000000000000000000000000000000000000000000000000000000001c953c0b600baf21dded2fcf35276aa3edda0a508c3b0c1885a4da4bff7ff733dec984573e9e1c6fab80abccbfd3d1b0385670493394143a96ef14337488f41a3843afae68d4e87dd3b11fc07efb92dfb21fde3eb9adb0cb6431fb994036dd1f03000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b297000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000479827af2eb7f438924900000000000000000000000000000000000000000000479827af2eba2871183200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000904bd50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da12ac101d8df6eb7b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a544534595445794d6930775a6d45354c5455775a6a4d74596d59794e533168596d4d325a4445354e325a6b4f57596966513d3d000000000000000000000000000000000000000000000000000000000000001f00000000000000000000000077efa19a462fc1f07f064c86e24cc7facbc253200000000000000000000000000000000000000000000000037d522b3c066319ae0000000000000000000000000000000000000000000000037d522b39d2badf9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd350f50f0b79584e48547b59da1e29e6e63cfe7df2b4112862c338fc312587e1",
      "signature": {
        "s": "0x7769c895eca094b291e33d691cd0ac2300ae3e74ebb9008afb03da3928a7409d",
        "r": "0x36939f91773689ce16a67a9a46808339bfd9f82acde9b3f69d5b70077c2aaa4d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x953c0b600baf21dded2fcf35276aa3edda0a508c3b0c1885a4da4bff7ff733de",
      "signature": {
        "s": "0x43afae68d4e87dd3b11fc07efb92dfb21fde3eb9adb0cb6431fb994036dd1f03",
        "r": "0xc984573e9e1c6fab80abccbfd3d1b0385670493394143a96ef14337488f41a38",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9456597524",
    "total": "220698246582"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9456597524",
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
            "amount": "27634568090524707122043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9456597"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTE4YTEyMi0wZmE5LTUwZjMtYmYyNS1hYmM2ZDE5N2ZkOWYifQ==",
    "nonce": 111255,
    "balances": {
      "current": "338094784938604676813385",
      "previous": "338094784938614142867506"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77efa19a462fc1f07f064c86e24cc7facbc25320",
    "nonce": 31,
    "balances": {
      "current": "64370559960765110702",
      "previous": "64370559951308513178"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:21.449Z",
  "updated": "2022-05-04T08:57:21.517Z",
  "id": "62723ff1bbd75600116d0672"
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
0x0f200f9b0000000000000000000000000000000000000000000000037d522b3c066319ae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `64370559960765110702`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`