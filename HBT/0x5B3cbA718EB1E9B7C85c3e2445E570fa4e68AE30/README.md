# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5B3cbA718EB1E9B7C85c3e2445E570fa4e68AE30`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000000000000000000000000000000000001ceea3fec80bf9dc8b00086a65335c1dc410d3eb6068f3388de59c3021c2798327878ff6a76fae07433ef0b87d802e943c6e3c6fddbe703c846cc66f9f5b891c1663be3a71c6c43f21e0079441cf2fd63a0d83d26ce4d6046ec158002fe8f90ad87ff740000000000000000000000000000000000000000000000000000000000000001cd1d42d6dc67e54d24ea42b0a4c7718abaf509818daaf269d6664220ea8e1300cc36efcc8573b2f7124aa440668625784db682d65c8aeae930dc642aaed6b63d47b7e10de2ff56ab616dda7931a28b0cb923f76fc3758b6b1121d9b358da7123a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a3700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16f94e583263000000000000000000000000000000000000000000000000002e16f96b4e3e7a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000076819000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a6050d1e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596d55325a6a45324d7930794e7a56694c5455345a6a6b744f5759794e43303059574d314d7a49785a5755774f44596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005b3cba718eb1e9b7c85c3e2445e570fa4e68ae30000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc80bf9dc8b00086a65335c1dc410d3eb6068f3388de59c3021c2798327878ff6",
      "signature": {
        "s": "0x71c6c43f21e0079441cf2fd63a0d83d26ce4d6046ec158002fe8f90ad87ff740",
        "r": "0xa76fae07433ef0b87d802e943c6e3c6fddbe703c846cc66f9f5b891c1663be3a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd1d42d6dc67e54d24ea42b0a4c7718abaf509818daaf269d6664220ea8e1300c",
      "signature": {
        "s": "0x7b7e10de2ff56ab616dda7931a28b0cb923f76fc3758b6b1121d9b358da7123a",
        "r": "0xc36efcc8573b2f7124aa440668625784db682d65c8aeae930dc642aaed6b63d4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "485401598",
    "total": "485401598"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "485401598",
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
            "amount": "44565582313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "485401"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYmU2ZjE2My0yNzViLTU4ZjktOWYyNC00YWM1MzIxZWUwODYifQ==",
    "nonce": 6711,
    "balances": {
      "current": "12973108945760867",
      "previous": "12973109431647866"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5b3cba718eb1e9b7c85c3e2445e570fa4e68ae30",
    "nonce": 22,
    "balances": {
      "current": "485401598",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:51:08.004Z",
  "updated": "2020-05-22T08:51:08.081Z",
  "id": "5ec7927be5756b00111b87ff"
}
```
* *stageAmount*: `485401598`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000000000000000000000000000000000001ceea3fec80bf9dc8b00086a65335c1dc410d3eb6068f3388de59c3021c2798327878ff6a76fae07433ef0b87d802e943c6e3c6fddbe703c846cc66f9f5b891c1663be3a71c6c43f21e0079441cf2fd63a0d83d26ce4d6046ec158002fe8f90ad87ff740000000000000000000000000000000000000000000000000000000000000001cd1d42d6dc67e54d24ea42b0a4c7718abaf509818daaf269d6664220ea8e1300cc36efcc8573b2f7124aa440668625784db682d65c8aeae930dc642aaed6b63d47b7e10de2ff56ab616dda7931a28b0cb923f76fc3758b6b1121d9b358da7123a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a3700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16f94e583263000000000000000000000000000000000000000000000000002e16f96b4e3e7a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000076819000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a6050d1e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c596d55325a6a45324d7930794e7a56694c5455345a6a6b744f5759794e43303059574d314d7a49785a5755774f44596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005b3cba718eb1e9b7c85c3e2445e570fa4e68ae30000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc80bf9dc8b00086a65335c1dc410d3eb6068f3388de59c3021c2798327878ff6",
      "signature": {
        "s": "0x71c6c43f21e0079441cf2fd63a0d83d26ce4d6046ec158002fe8f90ad87ff740",
        "r": "0xa76fae07433ef0b87d802e943c6e3c6fddbe703c846cc66f9f5b891c1663be3a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd1d42d6dc67e54d24ea42b0a4c7718abaf509818daaf269d6664220ea8e1300c",
      "signature": {
        "s": "0x7b7e10de2ff56ab616dda7931a28b0cb923f76fc3758b6b1121d9b358da7123a",
        "r": "0xc36efcc8573b2f7124aa440668625784db682d65c8aeae930dc642aaed6b63d4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "485401598",
    "total": "485401598"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "485401598",
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
            "amount": "44565582313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "485401"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYmU2ZjE2My0yNzViLTU4ZjktOWYyNC00YWM1MzIxZWUwODYifQ==",
    "nonce": 6711,
    "balances": {
      "current": "12973108945760867",
      "previous": "12973109431647866"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5b3cba718eb1e9b7c85c3e2445e570fa4e68ae30",
    "nonce": 22,
    "balances": {
      "current": "485401598",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:51:08.004Z",
  "updated": "2020-05-22T08:51:08.081Z",
  "id": "5ec7927be5756b00111b87ff"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001ceea3fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `485401598`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`