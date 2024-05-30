# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4F461dbfD8968d61ab822a29bC5410C049eBDA3A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000000000000000000000000000000000003af03d58a0ca34fcc1fb4c78342e76bd5bf038087ab72b47344543f745c237d8d8c858c7b29bc9ec6ecc8772c27f3e3d497af5d866899e5eefb227eb04fe9f4ac73c5ed05f1a37d385fb35471c437eef7310f1eb2aa0be957aea209c5742dabd3b13e9d6000000000000000000000000000000000000000000000000000000000000001cdaa8623335f9eb02723930eb19430eb6b3935137848ee5ab13aa06d1d8fecd0f7776239bad626b314d05af05c1942294a8f5d81683599a909173dd6481e2789e52c120f43adbd9d948eafb078f75415234ac661d97b58e8d52e317e98f3298ed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000181600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aef76f13990000000000000000000000000000000000000000000000000002e1aefb1f08d7e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000f1696000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095cf352e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e324a6b4d6d4a6d4f5330774d574d774c54557a4d546b744f5756694e693033595749304d54646c597a466d597a496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004f461dbfd8968d61ab822a29bc5410c049ebda3a000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa0ca34fcc1fb4c78342e76bd5bf038087ab72b47344543f745c237d8d8c858c7",
      "signature": {
        "s": "0x5f1a37d385fb35471c437eef7310f1eb2aa0be957aea209c5742dabd3b13e9d6",
        "r": "0xb29bc9ec6ecc8772c27f3e3d497af5d866899e5eefb227eb04fe9f4ac73c5ed0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdaa8623335f9eb02723930eb19430eb6b3935137848ee5ab13aa06d1d8fecd0f",
      "signature": {
        "s": "0x52c120f43adbd9d948eafb078f75415234ac661d97b58e8d52e317e98f3298ed",
        "r": "0x7776239bad626b314d05af05c1942294a8f5d81683599a909173dd6481e2789e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "988822872",
    "total": "988822872"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "988822872",
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
            "amount": "40214156008"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "988822"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3N2JkMmJmOS0wMWMwLTUzMTktOWViNi03YWI0MTdlYzFmYzIifQ==",
    "nonce": 6166,
    "balances": {
      "current": "12977464723716496",
      "previous": "12977465713528190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f461dbfd8968d61ab822a29bc5410c049ebda3a",
    "nonce": 22,
    "balances": {
      "current": "988822872",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:03.607Z",
  "updated": "2020-05-22T08:47:03.685Z",
  "id": "5ec79187e5756b00111b875a"
}
```
* *stageAmount*: `988822872`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000000000000000000000000000000000003af03d58a0ca34fcc1fb4c78342e76bd5bf038087ab72b47344543f745c237d8d8c858c7b29bc9ec6ecc8772c27f3e3d497af5d866899e5eefb227eb04fe9f4ac73c5ed05f1a37d385fb35471c437eef7310f1eb2aa0be957aea209c5742dabd3b13e9d6000000000000000000000000000000000000000000000000000000000000001cdaa8623335f9eb02723930eb19430eb6b3935137848ee5ab13aa06d1d8fecd0f7776239bad626b314d05af05c1942294a8f5d81683599a909173dd6481e2789e52c120f43adbd9d948eafb078f75415234ac661d97b58e8d52e317e98f3298ed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000181600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aef76f13990000000000000000000000000000000000000000000000000002e1aefb1f08d7e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000f1696000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095cf352e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e324a6b4d6d4a6d4f5330774d574d774c54557a4d546b744f5756694e693033595749304d54646c597a466d597a496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004f461dbfd8968d61ab822a29bc5410c049ebda3a000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa0ca34fcc1fb4c78342e76bd5bf038087ab72b47344543f745c237d8d8c858c7",
      "signature": {
        "s": "0x5f1a37d385fb35471c437eef7310f1eb2aa0be957aea209c5742dabd3b13e9d6",
        "r": "0xb29bc9ec6ecc8772c27f3e3d497af5d866899e5eefb227eb04fe9f4ac73c5ed0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdaa8623335f9eb02723930eb19430eb6b3935137848ee5ab13aa06d1d8fecd0f",
      "signature": {
        "s": "0x52c120f43adbd9d948eafb078f75415234ac661d97b58e8d52e317e98f3298ed",
        "r": "0x7776239bad626b314d05af05c1942294a8f5d81683599a909173dd6481e2789e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "988822872",
    "total": "988822872"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "988822872",
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
            "amount": "40214156008"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "988822"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3N2JkMmJmOS0wMWMwLTUzMTktOWViNi03YWI0MTdlYzFmYzIifQ==",
    "nonce": 6166,
    "balances": {
      "current": "12977464723716496",
      "previous": "12977465713528190"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4f461dbfd8968d61ab822a29bc5410c049ebda3a",
    "nonce": 22,
    "balances": {
      "current": "988822872",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:03.607Z",
  "updated": "2020-05-22T08:47:03.685Z",
  "id": "5ec79187e5756b00111b875a"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000003af03d58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `988822872`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`