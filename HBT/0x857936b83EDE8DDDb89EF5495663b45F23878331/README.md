# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x857936b83EDE8DDDb89EF5495663b45F23878331`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000000000000000000000000000000000000fc4498988e38ef17fbfe677ead558309089f6d9306249fefd536fe97c4da426353c14abf0747aacb4006a0f952b5a2a95e5a0e4fade6faf3bab5a91d490e6e0a80435fa2c893fd28422be216359430957baa4bd83f143757808b0e0355e6c3ddcc1835c000000000000000000000000000000000000000000000000000000000000001c1b4a0be12ae405c648e7a1f2d0ce58de494cb498306b2bfa278cd6a3090c525028b585720f3c8a6a97c5892a18320700425437402658a4eb533c12b8aa0f940663cc6eb0712e3f080a04247e081c9263a63aa18e01d84aac9dc1ca9fd781fb67000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a1cb9fcea8000000000000000000000000000000000000000000000000002e15a1db68217b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004094a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab82aa409000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d59335a5467314d79316b4d444a6b4c5455324e7a6b745957466b4e53316d5a6a646d4e4749774d6a55344f44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000857936b83ede8dddb89ef5495663b45f23878331000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x88e38ef17fbfe677ead558309089f6d9306249fefd536fe97c4da426353c14ab",
      "signature": {
        "s": "0x2c893fd28422be216359430957baa4bd83f143757808b0e0355e6c3ddcc1835c",
        "r": "0xf0747aacb4006a0f952b5a2a95e5a0e4fade6faf3bab5a91d490e6e0a80435fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1b4a0be12ae405c648e7a1f2d0ce58de494cb498306b2bfa278cd6a3090c5250",
      "signature": {
        "s": "0x63cc6eb0712e3f080a04247e081c9263a63aa18e01d84aac9dc1ca9fd781fb67",
        "r": "0x28b585720f3c8a6a97c5892a18320700425437402658a4eb533c12b8aa0f9406",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "264522121",
    "total": "264522121"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264522121",
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
            "amount": "46039475209"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264522"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NmY3ZTg1My1kMDJkLTU2NzktYWFkNS1mZjdmNGIwMjU4ODEifQ==",
    "nonce": 6987,
    "balances": {
      "current": "12971633578856104",
      "previous": "12971633843642747"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x857936b83ede8dddb89ef5495663b45f23878331",
    "nonce": 22,
    "balances": {
      "current": "264522121",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:12.817Z",
  "updated": "2020-05-22T08:53:12.895Z",
  "id": "5ec792f8b0c6090011d5b1ee"
}
```
* *stageAmount*: `264522121`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000000000000000000000000000000000000fc4498988e38ef17fbfe677ead558309089f6d9306249fefd536fe97c4da426353c14abf0747aacb4006a0f952b5a2a95e5a0e4fade6faf3bab5a91d490e6e0a80435fa2c893fd28422be216359430957baa4bd83f143757808b0e0355e6c3ddcc1835c000000000000000000000000000000000000000000000000000000000000001c1b4a0be12ae405c648e7a1f2d0ce58de494cb498306b2bfa278cd6a3090c525028b585720f3c8a6a97c5892a18320700425437402658a4eb533c12b8aa0f940663cc6eb0712e3f080a04247e081c9263a63aa18e01d84aac9dc1ca9fd781fb67000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a1cb9fcea8000000000000000000000000000000000000000000000000002e15a1db68217b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004094a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab82aa409000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6d59335a5467314d79316b4d444a6b4c5455324e7a6b745957466b4e53316d5a6a646d4e4749774d6a55344f44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000857936b83ede8dddb89ef5495663b45f23878331000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x88e38ef17fbfe677ead558309089f6d9306249fefd536fe97c4da426353c14ab",
      "signature": {
        "s": "0x2c893fd28422be216359430957baa4bd83f143757808b0e0355e6c3ddcc1835c",
        "r": "0xf0747aacb4006a0f952b5a2a95e5a0e4fade6faf3bab5a91d490e6e0a80435fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1b4a0be12ae405c648e7a1f2d0ce58de494cb498306b2bfa278cd6a3090c5250",
      "signature": {
        "s": "0x63cc6eb0712e3f080a04247e081c9263a63aa18e01d84aac9dc1ca9fd781fb67",
        "r": "0x28b585720f3c8a6a97c5892a18320700425437402658a4eb533c12b8aa0f9406",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "264522121",
    "total": "264522121"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264522121",
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
            "amount": "46039475209"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264522"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NmY3ZTg1My1kMDJkLTU2NzktYWFkNS1mZjdmNGIwMjU4ODEifQ==",
    "nonce": 6987,
    "balances": {
      "current": "12971633578856104",
      "previous": "12971633843642747"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x857936b83ede8dddb89ef5495663b45f23878331",
    "nonce": 22,
    "balances": {
      "current": "264522121",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:12.817Z",
  "updated": "2020-05-22T08:53:12.895Z",
  "id": "5ec792f8b0c6090011d5b1ee"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000fc44989000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `264522121`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`