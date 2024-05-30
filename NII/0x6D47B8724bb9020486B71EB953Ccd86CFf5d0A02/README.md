# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6D47B8724bb9020486B71EB953Ccd86CFf5d0A02`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e28ea8b2caeda60000000000000000000000000000000000000000000000008ffb6787e8ad800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000008ffb6787e8ad80000000000000000000000000000000000000000000000000008ffb6787e8ad80000f4403c9bbe7f25d79782c3e513a7e186752464b3e60ab3019fd5eb8e71fbd5c27ded8a66530aa0ab61848207d1b8db10ecaba613da49f8c07b091cbec75c0fbc42c8d5f4de6d64d88b3a9ea61d22b2370aa602ab5134417219e1a319fa64e0bc000000000000000000000000000000000000000000000000000000000000001bdfd79ce97f8b4ccd0b86603bbb9b800c86a7e6632316b9c216d6badd03a223049095f5d93f3171fc4ef2caac5360272d6be51541cad7e1dac26a219bf30aacb23240c5380a5b14069d9bec0b41e866e08bc19f4a71a2ebda098ff3ad3506e389000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2f4620000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000006d47b8724bb9020486b71eb953ccd86cff5d0a020000000000000000000000000000000000000000000000000e28ea8b2caeda60000000000000000000000000000000000000000000000009102d2328903dda6000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000024dc01ed8b700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024dc01ed8b700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e5445344e6a41774e79307a5a6d52694c5451324d7a6b744f47597a5a5330794d44526d4d474d775a6a6b325a6a676966513d3d00000000000000000000000000000000000000000000000000000000000000d6000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a8a43f256f4537c4c89f00000000000000000000000000000000000000000000a89b3f6ef6c6acecc89f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf4403c9bbe7f25d79782c3e513a7e186752464b3e60ab3019fd5eb8e71fbd5c2",
      "signature": {
        "s": "0x42c8d5f4de6d64d88b3a9ea61d22b2370aa602ab5134417219e1a319fa64e0bc",
        "r": "0x7ded8a66530aa0ab61848207d1b8db10ecaba613da49f8c07b091cbec75c0fbc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdfd79ce97f8b4ccd0b86603bbb9b800c86a7e6632316b9c216d6badd03a22304",
      "signature": {
        "s": "0x3240c5380a5b14069d9bec0b41e866e08bc19f4a71a2ebda098ff3ad3506e389",
        "r": "0x9095f5d93f3171fc4ef2caac5360272d6be51541cad7e1dac26a219bf30aacb2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "166000000000000000000",
    "total": "166000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "166000000000000000000",
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
            "amount": "166000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "166000000000000000"
      }
    },
    "wallet": "0x6d47b8724bb9020486b71eb953ccd86cff5d0a02",
    "data": "eyJyZWYiOiIzNTE4NjAwNy0zZmRiLTQ2MzktOGYzZS0yMDRmMGMwZjk2ZjgifQ==",
    "nonce": 14,
    "balances": {
      "current": "1020323199070427744",
      "previous": "167186323199070427744"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 214,
    "balances": {
      "current": "796387385315530369190047",
      "previous": "796221385315530369190047"
    }
  },
  "blockNumber": "14873698",
  "created": "2022-05-30T16:54:28.308Z",
  "updated": "2022-05-30T16:54:28.428Z",
  "id": "6294f6c4bbd75600116d0906"
}
```
* *stageAmount*: `1020323199070427744`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000008ffb6787e8ad800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000008ffb6787e8ad80000000000000000000000000000000000000000000000000008ffb6787e8ad80000f4403c9bbe7f25d79782c3e513a7e186752464b3e60ab3019fd5eb8e71fbd5c27ded8a66530aa0ab61848207d1b8db10ecaba613da49f8c07b091cbec75c0fbc42c8d5f4de6d64d88b3a9ea61d22b2370aa602ab5134417219e1a319fa64e0bc000000000000000000000000000000000000000000000000000000000000001bdfd79ce97f8b4ccd0b86603bbb9b800c86a7e6632316b9c216d6badd03a223049095f5d93f3171fc4ef2caac5360272d6be51541cad7e1dac26a219bf30aacb23240c5380a5b14069d9bec0b41e866e08bc19f4a71a2ebda098ff3ad3506e389000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2f4620000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000006d47b8724bb9020486b71eb953ccd86cff5d0a020000000000000000000000000000000000000000000000000e28ea8b2caeda60000000000000000000000000000000000000000000000009102d2328903dda6000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000024dc01ed8b700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024dc01ed8b700000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e5445344e6a41774e79307a5a6d52694c5451324d7a6b744f47597a5a5330794d44526d4d474d775a6a6b325a6a676966513d3d00000000000000000000000000000000000000000000000000000000000000d6000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a8a43f256f4537c4c89f00000000000000000000000000000000000000000000a89b3f6ef6c6acecc89f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf4403c9bbe7f25d79782c3e513a7e186752464b3e60ab3019fd5eb8e71fbd5c2",
      "signature": {
        "s": "0x42c8d5f4de6d64d88b3a9ea61d22b2370aa602ab5134417219e1a319fa64e0bc",
        "r": "0x7ded8a66530aa0ab61848207d1b8db10ecaba613da49f8c07b091cbec75c0fbc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdfd79ce97f8b4ccd0b86603bbb9b800c86a7e6632316b9c216d6badd03a22304",
      "signature": {
        "s": "0x3240c5380a5b14069d9bec0b41e866e08bc19f4a71a2ebda098ff3ad3506e389",
        "r": "0x9095f5d93f3171fc4ef2caac5360272d6be51541cad7e1dac26a219bf30aacb2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "166000000000000000000",
    "total": "166000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "166000000000000000000",
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
            "amount": "166000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "166000000000000000"
      }
    },
    "wallet": "0x6d47b8724bb9020486b71eb953ccd86cff5d0a02",
    "data": "eyJyZWYiOiIzNTE4NjAwNy0zZmRiLTQ2MzktOGYzZS0yMDRmMGMwZjk2ZjgifQ==",
    "nonce": 14,
    "balances": {
      "current": "1020323199070427744",
      "previous": "167186323199070427744"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 214,
    "balances": {
      "current": "796387385315530369190047",
      "previous": "796221385315530369190047"
    }
  },
  "blockNumber": "14873698",
  "created": "2022-05-30T16:54:28.308Z",
  "updated": "2022-05-30T16:54:28.428Z",
  "id": "6294f6c4bbd75600116d0906"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e28ea8b2caeda600000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1020323199070427744`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`