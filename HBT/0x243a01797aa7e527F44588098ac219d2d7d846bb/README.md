# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x243a01797aa7e527F44588098ac219d2d7d846bb`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000050aba73b0000000000000000000000000000000000000000000000000000000050aba73b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000050aba73b0000000000000000000000000000000000000000000000000000000050aba73bf0ee574cd0e797a06a0a3b48de0536dc08d6a37ac1f18c3e90aff6570441a2c9020e0a85c06bc194ad712deedee54c6e416a33108b68d01dd2183c5b2c56eb1f512936d3639a8610194074f11e1e34fa21c229e39a6e38bfd635d331cc166e95000000000000000000000000000000000000000000000000000000000000001bd792f28bda299a99f32633aab919072f1c05c079ae0903ccaf951456b77fe754d3e1b4d654fc1537b1f58b91867ed7508e6176f764db4beefffca170ff3d1d077a0fc857f4cc982e0500e7038eee1ac7efca57b6853eea9f28f15954a78c6b14000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2ee03edf5f0b000000000000000000000000000000000000000000000000002e2ee08f9fad1800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000014a6d2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004436e9db2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a63334f574a684d43316d5a4441324c5455774e4445744f47566a4e7930335954557a4e4451304d7a6c694e7a456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000243a01797aa7e527f44588098ac219d2d7d846bb0000000000000000000000000000000000000000000000000000000050aba73b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0ee574cd0e797a06a0a3b48de0536dc08d6a37ac1f18c3e90aff6570441a2c9",
      "signature": {
        "s": "0x512936d3639a8610194074f11e1e34fa21c229e39a6e38bfd635d331cc166e95",
        "r": "0x020e0a85c06bc194ad712deedee54c6e416a33108b68d01dd2183c5b2c56eb1f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd792f28bda299a99f32633aab919072f1c05c079ae0903ccaf951456b77fe754",
      "signature": {
        "s": "0x7a0fc857f4cc982e0500e7038eee1ac7efca57b6853eea9f28f15954a78c6b14",
        "r": "0xd3e1b4d654fc1537b1f58b91867ed7508e6176f764db4beefffca170ff3d1d07",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1353426747",
    "total": "1353426747"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1353426747",
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
            "amount": "18311191986"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1353426"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzc3OWJhMC1mZDA2LTUwNDEtOGVjNy03YTUzNDQ0MzliNzEifQ==",
    "nonce": 5260,
    "balances": {
      "current": "12999389591068427",
      "previous": "12999390945848600"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x243a01797aa7e527f44588098ac219d2d7d846bb",
    "nonce": 22,
    "balances": {
      "current": "1353426747",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:45.732Z",
  "updated": "2020-05-22T08:39:45.812Z",
  "id": "5ec78fd1e5756b00111b8630"
}
```
* *stageAmount*: `1353426747`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000050aba73b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000050aba73b0000000000000000000000000000000000000000000000000000000050aba73bf0ee574cd0e797a06a0a3b48de0536dc08d6a37ac1f18c3e90aff6570441a2c9020e0a85c06bc194ad712deedee54c6e416a33108b68d01dd2183c5b2c56eb1f512936d3639a8610194074f11e1e34fa21c229e39a6e38bfd635d331cc166e95000000000000000000000000000000000000000000000000000000000000001bd792f28bda299a99f32633aab919072f1c05c079ae0903ccaf951456b77fe754d3e1b4d654fc1537b1f58b91867ed7508e6176f764db4beefffca170ff3d1d077a0fc857f4cc982e0500e7038eee1ac7efca57b6853eea9f28f15954a78c6b14000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000148c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2ee03edf5f0b000000000000000000000000000000000000000000000000002e2ee08f9fad1800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000014a6d2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004436e9db2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a63334f574a684d43316d5a4441324c5455774e4445744f47566a4e7930335954557a4e4451304d7a6c694e7a456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000243a01797aa7e527f44588098ac219d2d7d846bb0000000000000000000000000000000000000000000000000000000050aba73b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0ee574cd0e797a06a0a3b48de0536dc08d6a37ac1f18c3e90aff6570441a2c9",
      "signature": {
        "s": "0x512936d3639a8610194074f11e1e34fa21c229e39a6e38bfd635d331cc166e95",
        "r": "0x020e0a85c06bc194ad712deedee54c6e416a33108b68d01dd2183c5b2c56eb1f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd792f28bda299a99f32633aab919072f1c05c079ae0903ccaf951456b77fe754",
      "signature": {
        "s": "0x7a0fc857f4cc982e0500e7038eee1ac7efca57b6853eea9f28f15954a78c6b14",
        "r": "0xd3e1b4d654fc1537b1f58b91867ed7508e6176f764db4beefffca170ff3d1d07",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1353426747",
    "total": "1353426747"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1353426747",
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
            "amount": "18311191986"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1353426"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzc3OWJhMC1mZDA2LTUwNDEtOGVjNy03YTUzNDQ0MzliNzEifQ==",
    "nonce": 5260,
    "balances": {
      "current": "12999389591068427",
      "previous": "12999390945848600"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x243a01797aa7e527f44588098ac219d2d7d846bb",
    "nonce": 22,
    "balances": {
      "current": "1353426747",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:45.732Z",
  "updated": "2020-05-22T08:39:45.812Z",
  "id": "5ec78fd1e5756b00111b8630"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000050aba73b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1353426747`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`