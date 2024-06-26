# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC9Df2e8b0d31c0a438D51f0649d4B094396f3E6d`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000000000000000000000000000000000004533f9d720f496cc918609f93335819f4eccec5744e6d29438081f6db720772c8729328b3d6abf9c77b6ea047adc08e79ecc6e0d9f3bfb75fef7d7bd58555a3f1d5c134e24d54df8e1bfe15da10c5a8ad7b2e39cb1cf24618485e81ab73191d564debb60000000000000000000000000000000000000000000000000000000000000001ca924ef0095ca2cdd0d3b946d09208b13c418b2409ffe50934f5e60869ebe7f51ce38ade6b1105bcd5286a80721b57c9fe0168a924dc8912a47b2251bbc7f15385438dd242ec7f208bc2667849a696a8f1aa1d0b050e58c97e770a6958231737e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c6c7634d4000000000000000000000000000000000000000000000000002e1b1cb1bbe5f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000011b74a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095173d4e1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6a4d354e44686c4d6930355a6d457a4c5455324f474d744f4441345a4331694e4449344e6a686c4e544d325a54676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c9df2e8b0d31c0a438d51f0649d4b094396f3e6d000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x20f496cc918609f93335819f4eccec5744e6d29438081f6db720772c8729328b",
      "signature": {
        "s": "0x24d54df8e1bfe15da10c5a8ad7b2e39cb1cf24618485e81ab73191d564debb60",
        "r": "0x3d6abf9c77b6ea047adc08e79ecc6e0d9f3bfb75fef7d7bd58555a3f1d5c134e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa924ef0095ca2cdd0d3b946d09208b13c418b2409ffe50934f5e60869ebe7f51",
      "signature": {
        "s": "0x5438dd242ec7f208bc2667849a696a8f1aa1d0b050e58c97e770a6958231737e",
        "r": "0xce38ade6b1105bcd5286a80721b57c9fe0168a924dc8912a47b2251bbc7f1538",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1161034199",
    "total": "1161034199"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1161034199",
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
            "amount": "40021251297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1161034"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NjM5NDhlMi05ZmEzLTU2OGMtODA4ZC1iNDI4NjhlNTM2ZTgifQ==",
    "nonce": 6009,
    "balances": {
      "current": "12977657821410516",
      "previous": "12977658983605749"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc9df2e8b0d31c0a438d51f0649d4b094396f3e6d",
    "nonce": 22,
    "balances": {
      "current": "1161034199",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:40.889Z",
  "updated": "2020-05-22T08:45:40.970Z",
  "id": "5ec79134005df800101bca14"
}
```
* *stageAmount*: `1161034199`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000000000000000000000000000000000004533f9d720f496cc918609f93335819f4eccec5744e6d29438081f6db720772c8729328b3d6abf9c77b6ea047adc08e79ecc6e0d9f3bfb75fef7d7bd58555a3f1d5c134e24d54df8e1bfe15da10c5a8ad7b2e39cb1cf24618485e81ab73191d564debb60000000000000000000000000000000000000000000000000000000000000001ca924ef0095ca2cdd0d3b946d09208b13c418b2409ffe50934f5e60869ebe7f51ce38ade6b1105bcd5286a80721b57c9fe0168a924dc8912a47b2251bbc7f15385438dd242ec7f208bc2667849a696a8f1aa1d0b050e58c97e770a6958231737e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1c6c7634d4000000000000000000000000000000000000000000000000002e1b1cb1bbe5f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000011b74a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095173d4e1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e6a4d354e44686c4d6930355a6d457a4c5455324f474d744f4441345a4331694e4449344e6a686c4e544d325a54676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c9df2e8b0d31c0a438d51f0649d4b094396f3e6d000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x20f496cc918609f93335819f4eccec5744e6d29438081f6db720772c8729328b",
      "signature": {
        "s": "0x24d54df8e1bfe15da10c5a8ad7b2e39cb1cf24618485e81ab73191d564debb60",
        "r": "0x3d6abf9c77b6ea047adc08e79ecc6e0d9f3bfb75fef7d7bd58555a3f1d5c134e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa924ef0095ca2cdd0d3b946d09208b13c418b2409ffe50934f5e60869ebe7f51",
      "signature": {
        "s": "0x5438dd242ec7f208bc2667849a696a8f1aa1d0b050e58c97e770a6958231737e",
        "r": "0xce38ade6b1105bcd5286a80721b57c9fe0168a924dc8912a47b2251bbc7f1538",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1161034199",
    "total": "1161034199"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1161034199",
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
            "amount": "40021251297"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1161034"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NjM5NDhlMi05ZmEzLTU2OGMtODA4ZC1iNDI4NjhlNTM2ZTgifQ==",
    "nonce": 6009,
    "balances": {
      "current": "12977657821410516",
      "previous": "12977658983605749"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc9df2e8b0d31c0a438d51f0649d4b094396f3e6d",
    "nonce": 22,
    "balances": {
      "current": "1161034199",
      "previous": "0"
    }
  },
  "blockNumber": "10114682",
  "created": "2020-05-22T08:45:40.889Z",
  "updated": "2020-05-22T08:45:40.970Z",
  "id": "5ec79134005df800101bca14"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004533f9d7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1161034199`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`
