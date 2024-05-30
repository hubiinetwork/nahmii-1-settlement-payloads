# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcE21E24525B2CA43a47FB10391EA4449662F1445`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000000000000000000000000000000ee19af15ecfab76acc852dc8be5ef74d2021e0d52bc5cc97e260a16848a49ed902eceb32b1f27ca4d68415c78fb5e85aa163fb067335f415d2b19f1c25b6ccf8da1dfab35f1881f545eb02995402ef10bccaf1cc1a9a89ae08c9a6eeb82df0f252471667e3f9b9d000000000000000000000000000000000000000000000000000000000000001b01547b3d61168931089c3712ab1f852f8bfe420dbb4ce5d93717ef554be7890e52803a7d26845f3d03ebec56e8e06a3bd69d0e4da607cdb759932585fadc3993497daf3ee4d8b7e0ab97254b11e64d3daa6b2daa2d434359eca39e8e5ac2c5eb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001234a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000006ae55f360f766420d4b0000000000000000000000000000000000000000000006ae64d8cb2b0f25e5b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000003cf424a142cf80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000360cd7f51617bcf4c060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a5a684e6d4a684e4331684e3249344c5455794d6d5574596a49334f5331684e7a51775a4445344e5751794d324d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ce21e24525b2ca43a47fb10391ea4449662f14450000000000000000000000000000000000000000000000000ee19af15ecfab76000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xacc852dc8be5ef74d2021e0d52bc5cc97e260a16848a49ed902eceb32b1f27ca",
      "signature": {
        "s": "0x545eb02995402ef10bccaf1cc1a9a89ae08c9a6eeb82df0f252471667e3f9b9d",
        "r": "0x4d68415c78fb5e85aa163fb067335f415d2b19f1c25b6ccf8da1dfab35f1881f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x01547b3d61168931089c3712ab1f852f8bfe420dbb4ce5d93717ef554be7890e",
      "signature": {
        "s": "0x497daf3ee4d8b7e0ab97254b11e64d3daa6b2daa2d434359eca39e8e5ac2c5eb",
        "r": "0x52803a7d26845f3d03ebec56e8e06a3bd69d0e4da607cdb759932585fadc3993",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1072308547759352694",
    "total": "1072308547759352694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1072308547759352694",
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
            "amount": "15952794523264000936966"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1072308547759352"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NjZhNmJhNC1hN2I4LTUyMmUtYjI3OS1hNzQwZDE4NWQyM2MifQ==",
    "nonce": 74570,
    "balances": {
      "current": "31550125766571586620747",
      "previous": "31551199147427893732793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce21e24525b2ca43a47fb10391ea4449662f1445",
    "nonce": 1,
    "balances": {
      "current": "1072308547759352694",
      "previous": "0"
    }
  },
  "blockNumber": "12400716",
  "created": "2021-05-09T14:38:41.714Z",
  "updated": "2021-05-09T14:38:41.806Z",
  "id": "6097f3f110d28200105e2a03"
}
```
* *stageAmount*: `1072308547759352694`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000000000000000000000000000000ee19af15ecfab76acc852dc8be5ef74d2021e0d52bc5cc97e260a16848a49ed902eceb32b1f27ca4d68415c78fb5e85aa163fb067335f415d2b19f1c25b6ccf8da1dfab35f1881f545eb02995402ef10bccaf1cc1a9a89ae08c9a6eeb82df0f252471667e3f9b9d000000000000000000000000000000000000000000000000000000000000001b01547b3d61168931089c3712ab1f852f8bfe420dbb4ce5d93717ef554be7890e52803a7d26845f3d03ebec56e8e06a3bd69d0e4da607cdb759932585fadc3993497daf3ee4d8b7e0ab97254b11e64d3daa6b2daa2d434359eca39e8e5ac2c5eb000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001234a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000006ae55f360f766420d4b0000000000000000000000000000000000000000000006ae64d8cb2b0f25e5b900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000003cf424a142cf80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000360cd7f51617bcf4c060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a5a684e6d4a684e4331684e3249344c5455794d6d5574596a49334f5331684e7a51775a4445344e5751794d324d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ce21e24525b2ca43a47fb10391ea4449662f14450000000000000000000000000000000000000000000000000ee19af15ecfab76000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xacc852dc8be5ef74d2021e0d52bc5cc97e260a16848a49ed902eceb32b1f27ca",
      "signature": {
        "s": "0x545eb02995402ef10bccaf1cc1a9a89ae08c9a6eeb82df0f252471667e3f9b9d",
        "r": "0x4d68415c78fb5e85aa163fb067335f415d2b19f1c25b6ccf8da1dfab35f1881f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x01547b3d61168931089c3712ab1f852f8bfe420dbb4ce5d93717ef554be7890e",
      "signature": {
        "s": "0x497daf3ee4d8b7e0ab97254b11e64d3daa6b2daa2d434359eca39e8e5ac2c5eb",
        "r": "0x52803a7d26845f3d03ebec56e8e06a3bd69d0e4da607cdb759932585fadc3993",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1072308547759352694",
    "total": "1072308547759352694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1072308547759352694",
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
            "amount": "15952794523264000936966"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1072308547759352"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NjZhNmJhNC1hN2I4LTUyMmUtYjI3OS1hNzQwZDE4NWQyM2MifQ==",
    "nonce": 74570,
    "balances": {
      "current": "31550125766571586620747",
      "previous": "31551199147427893732793"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce21e24525b2ca43a47fb10391ea4449662f1445",
    "nonce": 1,
    "balances": {
      "current": "1072308547759352694",
      "previous": "0"
    }
  },
  "blockNumber": "12400716",
  "created": "2021-05-09T14:38:41.714Z",
  "updated": "2021-05-09T14:38:41.806Z",
  "id": "6097f3f110d28200105e2a03"
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
0x0f200f9b0000000000000000000000000000000000000000000000000ee19af15ecfab760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1072308547759352694`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`