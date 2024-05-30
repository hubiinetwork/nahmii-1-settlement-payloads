# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcE1E4bE64C714F0F68515cd5CF65221Fe76A5597`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000002aed0000000000000000000000000000000000000000000000000000000000002aed00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002aed0000000000000000000000000000000000000000000000000000000000002aed855b1a6122e914d064dd6d87c16516da0c3405864bcfccf6cc57cd4cd449c3e7efb4634883dabc4c1e6e653c13f64c331e014ee7ae33921baba5f2a76f03615a0dcd6d06180dc19a9702804237bf0ae5d74696ea730f1bb9887993d920921bf0000000000000000000000000000000000000000000000000000000000000001c81ba12c471134ee2846c91dda55c5a5430847f1ec58ee3ccd1a250940e1e4637d368714c3396f859145dbfa0839dfe21f2f6c8c53b725c0c300ddcfdf608a29e2a805a1efa3372eddacf76f8be5548c22e6ee13eb4866549662b7d0f829b58f8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000058600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6ff1c54000000000000000000000000000000000000000000000000002386f2c6ff474b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009756300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a44646a593251325a4330334e4749324c5455314e5759744f4459324e4330304f4751795a6a45354e5759324e6a636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ce1e4be64c714f0f68515cd5cf65221fe76a55970000000000000000000000000000000000000000000000000000000000002aed000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x855b1a6122e914d064dd6d87c16516da0c3405864bcfccf6cc57cd4cd449c3e7",
      "signature": {
        "s": "0x0dcd6d06180dc19a9702804237bf0ae5d74696ea730f1bb9887993d920921bf0",
        "r": "0xefb4634883dabc4c1e6e653c13f64c331e014ee7ae33921baba5f2a76f03615a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x81ba12c471134ee2846c91dda55c5a5430847f1ec58ee3ccd1a250940e1e4637",
      "signature": {
        "s": "0x2a805a1efa3372eddacf76f8be5548c22e6ee13eb4866549662b7d0f829b58f8",
        "r": "0xd368714c3396f859145dbfa0839dfe21f2f6c8c53b725c0c300ddcfdf608a29e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10989",
    "total": "10989"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10989",
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
            "amount": "619875"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZDdjY2Q2ZC03NGI2LTU1NWYtODY2NC00OGQyZjE5NWY2NjcifQ==",
    "nonce": 1414,
    "balances": {
      "current": "10000001463688276",
      "previous": "10000001463699275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce1e4be64c714f0f68515cd5cf65221fe76a5597",
    "nonce": 20,
    "balances": {
      "current": "10989",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:14.761Z",
  "updated": "2020-05-22T08:09:15.902Z",
  "id": "5ec788aa005df800101bc3ff"
}
```
* *stageAmount*: `10989`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002aed00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000002aed0000000000000000000000000000000000000000000000000000000000002aed855b1a6122e914d064dd6d87c16516da0c3405864bcfccf6cc57cd4cd449c3e7efb4634883dabc4c1e6e653c13f64c331e014ee7ae33921baba5f2a76f03615a0dcd6d06180dc19a9702804237bf0ae5d74696ea730f1bb9887993d920921bf0000000000000000000000000000000000000000000000000000000000000001c81ba12c471134ee2846c91dda55c5a5430847f1ec58ee3ccd1a250940e1e4637d368714c3396f859145dbfa0839dfe21f2f6c8c53b725c0c300ddcfdf608a29e2a805a1efa3372eddacf76f8be5548c22e6ee13eb4866549662b7d0f829b58f8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000058600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6ff1c54000000000000000000000000000000000000000000000000002386f2c6ff474b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009756300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a44646a593251325a4330334e4749324c5455314e5759744f4459324e4330304f4751795a6a45354e5759324e6a636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000ce1e4be64c714f0f68515cd5cf65221fe76a55970000000000000000000000000000000000000000000000000000000000002aed000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x855b1a6122e914d064dd6d87c16516da0c3405864bcfccf6cc57cd4cd449c3e7",
      "signature": {
        "s": "0x0dcd6d06180dc19a9702804237bf0ae5d74696ea730f1bb9887993d920921bf0",
        "r": "0xefb4634883dabc4c1e6e653c13f64c331e014ee7ae33921baba5f2a76f03615a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x81ba12c471134ee2846c91dda55c5a5430847f1ec58ee3ccd1a250940e1e4637",
      "signature": {
        "s": "0x2a805a1efa3372eddacf76f8be5548c22e6ee13eb4866549662b7d0f829b58f8",
        "r": "0xd368714c3396f859145dbfa0839dfe21f2f6c8c53b725c0c300ddcfdf608a29e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10989",
    "total": "10989"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10989",
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
            "amount": "619875"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "10"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ZDdjY2Q2ZC03NGI2LTU1NWYtODY2NC00OGQyZjE5NWY2NjcifQ==",
    "nonce": 1414,
    "balances": {
      "current": "10000001463688276",
      "previous": "10000001463699275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce1e4be64c714f0f68515cd5cf65221fe76a5597",
    "nonce": 20,
    "balances": {
      "current": "10989",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:14.761Z",
  "updated": "2020-05-22T08:09:15.902Z",
  "id": "5ec788aa005df800101bc3ff"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000002aed0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10989`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``