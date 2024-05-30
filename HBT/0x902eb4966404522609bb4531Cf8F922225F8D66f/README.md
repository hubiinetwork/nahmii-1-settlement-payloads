# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x902eb4966404522609bb4531Cf8F922225F8D66f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000000000000000000000000000000000008de5cb29b5188454842d8ce6351d73161bdbffdf7d7ada66a103f6efb0a0f535ce413ae579e13e46e2c72b971397da7bd93c871df8aa646539f99aa26fa862350db4b4cf0307c797c5d9b9889ff28a35527ee2b344cbc7c94d3a8129aeb7a6cd7fcaa6c7000000000000000000000000000000000000000000000000000000000000001c1f8852a542e8a167dfcc0b5704907970cb37bc8692ea2d5d3b0e838a2050f912f6bdf4739ac6a3658b76739b55c235acdb56f361b35651d78bb6bb0d5a3a510e61c4551d9a28d977ceb9340d7e486e68e9fa220eefdada31c3e69e581e7d3465000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ce600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12ec8eec1345000000000000000000000000000000000000000000000000002e12ed1cf631d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000245367000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b69753d27000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d3249784e6a4a6d4e5330794e474e6b4c5456694d5459744f44646d4e7930324d47526b596d557a5a474d31596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000902eb4966404522609bb4531cf8f922225f8d66f000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb5188454842d8ce6351d73161bdbffdf7d7ada66a103f6efb0a0f535ce413ae5",
      "signature": {
        "s": "0x0307c797c5d9b9889ff28a35527ee2b344cbc7c94d3a8129aeb7a6cd7fcaa6c7",
        "r": "0x79e13e46e2c72b971397da7bd93c871df8aa646539f99aa26fa862350db4b4cf",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1f8852a542e8a167dfcc0b5704907970cb37bc8692ea2d5d3b0e838a2050f912",
      "signature": {
        "s": "0x61c4551d9a28d977ceb9340d7e486e68e9fa220eefdada31c3e69e581e7d3465",
        "r": "0xf6bdf4739ac6a3658b76739b55c235acdb56f361b35651d78bb6bb0d5a3a510e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2380647209",
    "total": "2380647209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2380647209",
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
            "amount": "49013931303"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2380647"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlM2IxNjJmNS0yNGNkLTViMTYtODdmNy02MGRkYmUzZGM1YjgifQ==",
    "nonce": 7398,
    "balances": {
      "current": "12968656148108101",
      "previous": "12968658531135957"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x902eb4966404522609bb4531cf8f922225f8d66f",
    "nonce": 22,
    "balances": {
      "current": "2380647209",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:28.474Z",
  "updated": "2020-05-22T08:56:28.535Z",
  "id": "5ec793bce5756b00111b88d4"
}
```
* *stageAmount*: `2380647209`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000000000000000000000000000000000008de5cb29b5188454842d8ce6351d73161bdbffdf7d7ada66a103f6efb0a0f535ce413ae579e13e46e2c72b971397da7bd93c871df8aa646539f99aa26fa862350db4b4cf0307c797c5d9b9889ff28a35527ee2b344cbc7c94d3a8129aeb7a6cd7fcaa6c7000000000000000000000000000000000000000000000000000000000000001c1f8852a542e8a167dfcc0b5704907970cb37bc8692ea2d5d3b0e838a2050f912f6bdf4739ac6a3658b76739b55c235acdb56f361b35651d78bb6bb0d5a3a510e61c4551d9a28d977ceb9340d7e486e68e9fa220eefdada31c3e69e581e7d3465000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ce600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e12ec8eec1345000000000000000000000000000000000000000000000000002e12ed1cf631d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000245367000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b69753d27000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d3249784e6a4a6d4e5330794e474e6b4c5456694d5459744f44646d4e7930324d47526b596d557a5a474d31596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000902eb4966404522609bb4531cf8f922225f8d66f000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb5188454842d8ce6351d73161bdbffdf7d7ada66a103f6efb0a0f535ce413ae5",
      "signature": {
        "s": "0x0307c797c5d9b9889ff28a35527ee2b344cbc7c94d3a8129aeb7a6cd7fcaa6c7",
        "r": "0x79e13e46e2c72b971397da7bd93c871df8aa646539f99aa26fa862350db4b4cf",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1f8852a542e8a167dfcc0b5704907970cb37bc8692ea2d5d3b0e838a2050f912",
      "signature": {
        "s": "0x61c4551d9a28d977ceb9340d7e486e68e9fa220eefdada31c3e69e581e7d3465",
        "r": "0xf6bdf4739ac6a3658b76739b55c235acdb56f361b35651d78bb6bb0d5a3a510e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2380647209",
    "total": "2380647209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2380647209",
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
            "amount": "49013931303"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2380647"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlM2IxNjJmNS0yNGNkLTViMTYtODdmNy02MGRkYmUzZGM1YjgifQ==",
    "nonce": 7398,
    "balances": {
      "current": "12968656148108101",
      "previous": "12968658531135957"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x902eb4966404522609bb4531cf8f922225f8d66f",
    "nonce": 22,
    "balances": {
      "current": "2380647209",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:28.474Z",
  "updated": "2020-05-22T08:56:28.535Z",
  "id": "5ec793bce5756b00111b88d4"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000008de5cb29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2380647209`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`