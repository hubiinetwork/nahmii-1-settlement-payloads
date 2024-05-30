# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbA38f5990Cc8e6b0267eD1092338788B78CA05e8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000000000000000000000000000000000000fc460f4df37a96a4975d2c8d01299a3c06d94d0ee47794de51f11e5852dda786026fc497144d3eaa866b6199974c73a42fae1b4130752118ae44f3d387214accc1d09c440191fda90ba782f95bbe35cfd19e0efcb3a93fbe916f45fabda779af2e8a4a7000000000000000000000000000000000000000000000000000000000000001c3f88f071fbc54e644fb407e6e4cdd1b13dbdf6d9974ccc8cf19ad496b209f18ef82911117692aab2b59f0036619e77eda8cc5f29ce406321faec83ddcefcb95f5779a311c0d36168d2bc425f42f0c8494ef009a92d44fdbeb1546d56674ca6c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000191800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18216607012c000000000000000000000000000000000000000000000000002e182175cf6b7000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000040950000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a14977d08000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d444d334e6a63344e6930324e6a5a684c5455784d544174596a45334d4331685a6d4e6c597a526a595445794e54596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ba38f5990cc8e6b0267ed1092338788b78ca05e8000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf37a96a4975d2c8d01299a3c06d94d0ee47794de51f11e5852dda786026fc49",
      "signature": {
        "s": "0x40191fda90ba782f95bbe35cfd19e0efcb3a93fbe916f45fabda779af2e8a4a7",
        "r": "0x7144d3eaa866b6199974c73a42fae1b4130752118ae44f3d387214accc1d09c4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f88f071fbc54e644fb407e6e4cdd1b13dbdf6d9974ccc8cf19ad496b209f18e",
      "signature": {
        "s": "0x5779a311c0d36168d2bc425f42f0c8494ef009a92d44fdbeb1546d56674ca6c9",
        "r": "0xf82911117692aab2b59f0036619e77eda8cc5f29ce406321faec83ddcefcb95f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "264528116",
    "total": "264528116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264528116",
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
            "amount": "43295145224"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264528"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDM3Njc4Ni02NjZhLTUxMTAtYjE3MC1hZmNlYzRjYTEyNTYifQ==",
    "nonce": 6424,
    "balances": {
      "current": "12974380653412652",
      "previous": "12974380918205296"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xba38f5990cc8e6b0267ed1092338788b78ca05e8",
    "nonce": 22,
    "balances": {
      "current": "264528116",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:01.427Z",
  "updated": "2020-05-22T08:49:01.487Z",
  "id": "5ec791fde5756b00111b87ab"
}
```
* *stageAmount*: `264528116`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000000000000000000000000000000000000fc460f4df37a96a4975d2c8d01299a3c06d94d0ee47794de51f11e5852dda786026fc497144d3eaa866b6199974c73a42fae1b4130752118ae44f3d387214accc1d09c440191fda90ba782f95bbe35cfd19e0efcb3a93fbe916f45fabda779af2e8a4a7000000000000000000000000000000000000000000000000000000000000001c3f88f071fbc54e644fb407e6e4cdd1b13dbdf6d9974ccc8cf19ad496b209f18ef82911117692aab2b59f0036619e77eda8cc5f29ce406321faec83ddcefcb95f5779a311c0d36168d2bc425f42f0c8494ef009a92d44fdbeb1546d56674ca6c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000191800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18216607012c000000000000000000000000000000000000000000000000002e182175cf6b7000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000040950000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a14977d08000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d444d334e6a63344e6930324e6a5a684c5455784d544174596a45334d4331685a6d4e6c597a526a595445794e54596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000ba38f5990cc8e6b0267ed1092338788b78ca05e8000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdf37a96a4975d2c8d01299a3c06d94d0ee47794de51f11e5852dda786026fc49",
      "signature": {
        "s": "0x40191fda90ba782f95bbe35cfd19e0efcb3a93fbe916f45fabda779af2e8a4a7",
        "r": "0x7144d3eaa866b6199974c73a42fae1b4130752118ae44f3d387214accc1d09c4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f88f071fbc54e644fb407e6e4cdd1b13dbdf6d9974ccc8cf19ad496b209f18e",
      "signature": {
        "s": "0x5779a311c0d36168d2bc425f42f0c8494ef009a92d44fdbeb1546d56674ca6c9",
        "r": "0xf82911117692aab2b59f0036619e77eda8cc5f29ce406321faec83ddcefcb95f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "264528116",
    "total": "264528116"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264528116",
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
            "amount": "43295145224"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264528"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDM3Njc4Ni02NjZhLTUxMTAtYjE3MC1hZmNlYzRjYTEyNTYifQ==",
    "nonce": 6424,
    "balances": {
      "current": "12974380653412652",
      "previous": "12974380918205296"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xba38f5990cc8e6b0267ed1092338788b78ca05e8",
    "nonce": 22,
    "balances": {
      "current": "264528116",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:01.427Z",
  "updated": "2020-05-22T08:49:01.487Z",
  "id": "5ec791fde5756b00111b87ab"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000fc460f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `264528116`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`