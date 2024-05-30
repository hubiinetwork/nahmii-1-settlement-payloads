# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe6C50494FF60F097204CB80fDa6B68a60791C9B7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000000000000000000000000000000000019de20973422963489f81b0b0acb892b07b93860c5257658edb3d643536698430ffefa62d68a889067cbdc0c2796fbc67e1ddb5736eabad39c162522b8943c7c1be708f391e9781025768fb354fa3eadbba1473e87a53dacb4732ffb61f8b269a9d18ddf4000000000000000000000000000000000000000000000000000000000000001bd26dd075aac105d2b6c914f0f25d95e4f6eff0cfc12adef5799d55ad5cbf88fc47621e350c80931b97b44fb641706a3338e106eb3fba2eebb0f226910845d78f5d43d194d0232670d3e47f0876e6efd0cbf1c90205158b6581c64ddd5b8dd096000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019e600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1744bab6b2a9000000000000000000000000000000000000000000000000002e17465902b05700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000069f43b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4d06d0e5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d4445314d6d49354d4331694e6a68684c54566a4d324d74596a4a6c5a6930314d54426d5a6d5a6b595451334d44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e6c50494ff60f097204cb80fda6b68a60791c9b7000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x422963489f81b0b0acb892b07b93860c5257658edb3d643536698430ffefa62d",
      "signature": {
        "s": "0x1e9781025768fb354fa3eadbba1473e87a53dacb4732ffb61f8b269a9d18ddf4",
        "r": "0x68a889067cbdc0c2796fbc67e1ddb5736eabad39c162522b8943c7c1be708f39",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd26dd075aac105d2b6c914f0f25d95e4f6eff0cfc12adef5799d55ad5cbf88fc",
      "signature": {
        "s": "0x5d43d194d0232670d3e47f0876e6efd0cbf1c90205158b6581c64ddd5b8dd096",
        "r": "0x47621e350c80931b97b44fb641706a3338e106eb3fba2eebb0f226910845d78f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6943803763",
    "total": "6943803763"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6943803763",
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
            "amount": "44241965285"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6943803"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMDE1MmI5MC1iNjhhLTVjM2MtYjJlZi01MTBmZmZkYTQ3MDEifQ==",
    "nonce": 6630,
    "balances": {
      "current": "12973432886440617",
      "previous": "12973439837188183"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6c50494ff60f097204cb80fda6b68a60791c9b7",
    "nonce": 22,
    "balances": {
      "current": "6943803763",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:39.048Z",
  "updated": "2020-05-22T08:50:39.121Z",
  "id": "5ec7925fe5756b00111b87e9"
}
```
* *stageAmount*: `6943803763`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000000000000000000000000000000000019de20973422963489f81b0b0acb892b07b93860c5257658edb3d643536698430ffefa62d68a889067cbdc0c2796fbc67e1ddb5736eabad39c162522b8943c7c1be708f391e9781025768fb354fa3eadbba1473e87a53dacb4732ffb61f8b269a9d18ddf4000000000000000000000000000000000000000000000000000000000000001bd26dd075aac105d2b6c914f0f25d95e4f6eff0cfc12adef5799d55ad5cbf88fc47621e350c80931b97b44fb641706a3338e106eb3fba2eebb0f226910845d78f5d43d194d0232670d3e47f0876e6efd0cbf1c90205158b6581c64ddd5b8dd096000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019e600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1744bab6b2a9000000000000000000000000000000000000000000000000002e17465902b05700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000069f43b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4d06d0e5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d4445314d6d49354d4331694e6a68684c54566a4d324d74596a4a6c5a6930314d54426d5a6d5a6b595451334d44456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e6c50494ff60f097204cb80fda6b68a60791c9b7000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x422963489f81b0b0acb892b07b93860c5257658edb3d643536698430ffefa62d",
      "signature": {
        "s": "0x1e9781025768fb354fa3eadbba1473e87a53dacb4732ffb61f8b269a9d18ddf4",
        "r": "0x68a889067cbdc0c2796fbc67e1ddb5736eabad39c162522b8943c7c1be708f39",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd26dd075aac105d2b6c914f0f25d95e4f6eff0cfc12adef5799d55ad5cbf88fc",
      "signature": {
        "s": "0x5d43d194d0232670d3e47f0876e6efd0cbf1c90205158b6581c64ddd5b8dd096",
        "r": "0x47621e350c80931b97b44fb641706a3338e106eb3fba2eebb0f226910845d78f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6943803763",
    "total": "6943803763"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6943803763",
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
            "amount": "44241965285"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6943803"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMDE1MmI5MC1iNjhhLTVjM2MtYjJlZi01MTBmZmZkYTQ3MDEifQ==",
    "nonce": 6630,
    "balances": {
      "current": "12973432886440617",
      "previous": "12973439837188183"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe6c50494ff60f097204cb80fda6b68a60791c9b7",
    "nonce": 22,
    "balances": {
      "current": "6943803763",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:39.048Z",
  "updated": "2020-05-22T08:50:39.121Z",
  "id": "5ec7925fe5756b00111b87e9"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000019de20973000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6943803763`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`