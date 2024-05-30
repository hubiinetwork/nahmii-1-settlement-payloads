# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB3bF66e38cd47C678cae2d4B4084849B2B82cD4D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000000000000000000000000000000000000f7670cefcc3c89632d20b9039439d0fec91d8e14d03a4b5999f712ff51e956f70ff5cc88c8e9006aa4a97d2dbf0242695a4ecbcb375d00c55a7799b26da7264d2635299352f4a590c62e256451d10565772d44702c660524e36d09ffc3d6f52b486e7aa000000000000000000000000000000000000000000000000000000000000001b37933be30559920f8d9aa0da817f277954ab8087038ee543863fb36ad6e89dca74fbe14e701fb41891f07eb486ab90a2c1a1d83453d055b0d6da11df3bf9e2eb327cb5b5e5f6ed77a254b979422d963018c41ec60e783c669177bf88b60bf2a0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d47dddf1585000000000000000000000000000000000000000000000000002e1d47ed597baf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003f55c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c366afbd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c595441794e6a526d4e43316b4e57597a4c54566b59545174596a6735596930314d474d784f4755784e445579596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b3bf66e38cd47c678cae2d4b4084849b2b82cd4d000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfcc3c89632d20b9039439d0fec91d8e14d03a4b5999f712ff51e956f70ff5cc8",
      "signature": {
        "s": "0x352f4a590c62e256451d10565772d44702c660524e36d09ffc3d6f52b486e7aa",
        "r": "0x8c8e9006aa4a97d2dbf0242695a4ecbcb375d00c55a7799b26da7264d2635299",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x37933be30559920f8d9aa0da817f277954ab8087038ee543863fb36ad6e89dca",
      "signature": {
        "s": "0x327cb5b5e5f6ed77a254b979422d963018c41ec60e783c669177bf88b60bf2a0",
        "r": "0x74fbe14e701fb41891f07eb486ab90a2c1a1d83453d055b0d6da11df3bf9e2eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "259420366",
    "total": "259420366"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "259420366",
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
            "amount": "37638025149"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "259420"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYTAyNjRmNC1kNWYzLTVkYTQtYjg5Yi01MGMxOGUxNDUyYjgifQ==",
    "nonce": 5605,
    "balances": {
      "current": "12980043430958469",
      "previous": "12980043690638255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bf66e38cd47c678cae2d4b4084849b2b82cd4d",
    "nonce": 22,
    "balances": {
      "current": "259420366",
      "previous": "0"
    }
  },
  "blockNumber": "10114670",
  "created": "2020-05-22T08:42:24.233Z",
  "updated": "2020-05-22T08:42:25.300Z",
  "id": "5ec79070b0c6090011d5b011"
}
```
* *stageAmount*: `259420366`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000000000000000000000000000000000000f7670cefcc3c89632d20b9039439d0fec91d8e14d03a4b5999f712ff51e956f70ff5cc88c8e9006aa4a97d2dbf0242695a4ecbcb375d00c55a7799b26da7264d2635299352f4a590c62e256451d10565772d44702c660524e36d09ffc3d6f52b486e7aa000000000000000000000000000000000000000000000000000000000000001b37933be30559920f8d9aa0da817f277954ab8087038ee543863fb36ad6e89dca74fbe14e701fb41891f07eb486ab90a2c1a1d83453d055b0d6da11df3bf9e2eb327cb5b5e5f6ed77a254b979422d963018c41ec60e783c669177bf88b60bf2a0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566e000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015e500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d47dddf1585000000000000000000000000000000000000000000000000002e1d47ed597baf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003f55c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c366afbd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c595441794e6a526d4e43316b4e57597a4c54566b59545174596a6735596930314d474d784f4755784e445579596a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b3bf66e38cd47c678cae2d4b4084849b2b82cd4d000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfcc3c89632d20b9039439d0fec91d8e14d03a4b5999f712ff51e956f70ff5cc8",
      "signature": {
        "s": "0x352f4a590c62e256451d10565772d44702c660524e36d09ffc3d6f52b486e7aa",
        "r": "0x8c8e9006aa4a97d2dbf0242695a4ecbcb375d00c55a7799b26da7264d2635299",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x37933be30559920f8d9aa0da817f277954ab8087038ee543863fb36ad6e89dca",
      "signature": {
        "s": "0x327cb5b5e5f6ed77a254b979422d963018c41ec60e783c669177bf88b60bf2a0",
        "r": "0x74fbe14e701fb41891f07eb486ab90a2c1a1d83453d055b0d6da11df3bf9e2eb",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "259420366",
    "total": "259420366"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "259420366",
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
            "amount": "37638025149"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "259420"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYTAyNjRmNC1kNWYzLTVkYTQtYjg5Yi01MGMxOGUxNDUyYjgifQ==",
    "nonce": 5605,
    "balances": {
      "current": "12980043430958469",
      "previous": "12980043690638255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3bf66e38cd47c678cae2d4b4084849b2b82cd4d",
    "nonce": 22,
    "balances": {
      "current": "259420366",
      "previous": "0"
    }
  },
  "blockNumber": "10114670",
  "created": "2020-05-22T08:42:24.233Z",
  "updated": "2020-05-22T08:42:25.300Z",
  "id": "5ec79070b0c6090011d5b011"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000f7670ce000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `259420366`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`