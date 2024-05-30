# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc17d8114fabcf0C38F1877E4aA46e4041A23604a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000000000000000000000000000000000005f310febf153e35d162f9f59add78c51abd050a98a53b2195bd3f4cab158f2e23216f3d6de4ab33cc4892feaf37fac1ffdba7c2d1e22f6856d7dba1e39c2fef5a4b0c62622cb611d30c09e487ad27dbb0d74cd60c4ec48145d9e5b223b4f33c29ef5af4f000000000000000000000000000000000000000000000000000000000000001cffa15c532c87afc57f49221144d54ca9ea58887569729839c7022fe465f631109358c27b37fae9110fc5d1a3366f654f9b2a42d9738b7b19aa276a30a38034457c4b8d4321bbb44d6b0398dac7b8e209ea905cacaf12ecba266a220184e417d7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a16c566043000000000000000000000000000000000000000000000000002e15a1cb9fcea800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000185e7a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8430283000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5745314e5467784f43316d4e4755304c545534597a4974596a49334d53316a5932526a4d6d526a596a49334f54456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c17d8114fabcf0c38f1877e4aa46e4041a23604a000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf153e35d162f9f59add78c51abd050a98a53b2195bd3f4cab158f2e23216f3d6",
      "signature": {
        "s": "0x22cb611d30c09e487ad27dbb0d74cd60c4ec48145d9e5b223b4f33c29ef5af4f",
        "r": "0xde4ab33cc4892feaf37fac1ffdba7c2d1e22f6856d7dba1e39c2fef5a4b0c626",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xffa15c532c87afc57f49221144d54ca9ea58887569729839c7022fe465f63110",
      "signature": {
        "s": "0x7c4b8d4321bbb44d6b0398dac7b8e209ea905cacaf12ecba266a220184e417d7",
        "r": "0x9358c27b37fae9110fc5d1a3366f654f9b2a42d9738b7b19aa276a30a3803445",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1597050859",
    "total": "1597050859"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1597050859",
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
            "amount": "46041072259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1597050"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NWE1NTgxOC1mNGU0LTU4YzItYjI3MS1jY2RjMmRjYjI3OTEifQ==",
    "nonce": 6988,
    "balances": {
      "current": "12971631980208195",
      "previous": "12971633578856104"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc17d8114fabcf0c38f1877e4aa46e4041a23604a",
    "nonce": 22,
    "balances": {
      "current": "1597050859",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:13.013Z",
  "updated": "2020-05-22T08:53:13.102Z",
  "id": "5ec792f9005df800101bcb59"
}
```
* *stageAmount*: `1597050859`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000000000000000000000000000000000005f310febf153e35d162f9f59add78c51abd050a98a53b2195bd3f4cab158f2e23216f3d6de4ab33cc4892feaf37fac1ffdba7c2d1e22f6856d7dba1e39c2fef5a4b0c62622cb611d30c09e487ad27dbb0d74cd60c4ec48145d9e5b223b4f33c29ef5af4f000000000000000000000000000000000000000000000000000000000000001cffa15c532c87afc57f49221144d54ca9ea58887569729839c7022fe465f631109358c27b37fae9110fc5d1a3366f654f9b2a42d9738b7b19aa276a30a38034457c4b8d4321bbb44d6b0398dac7b8e209ea905cacaf12ecba266a220184e417d7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a16c566043000000000000000000000000000000000000000000000000002e15a1cb9fcea800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000185e7a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8430283000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5745314e5467784f43316d4e4755304c545534597a4974596a49334d53316a5932526a4d6d526a596a49334f54456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c17d8114fabcf0c38f1877e4aa46e4041a23604a000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf153e35d162f9f59add78c51abd050a98a53b2195bd3f4cab158f2e23216f3d6",
      "signature": {
        "s": "0x22cb611d30c09e487ad27dbb0d74cd60c4ec48145d9e5b223b4f33c29ef5af4f",
        "r": "0xde4ab33cc4892feaf37fac1ffdba7c2d1e22f6856d7dba1e39c2fef5a4b0c626",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xffa15c532c87afc57f49221144d54ca9ea58887569729839c7022fe465f63110",
      "signature": {
        "s": "0x7c4b8d4321bbb44d6b0398dac7b8e209ea905cacaf12ecba266a220184e417d7",
        "r": "0x9358c27b37fae9110fc5d1a3366f654f9b2a42d9738b7b19aa276a30a3803445",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1597050859",
    "total": "1597050859"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1597050859",
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
            "amount": "46041072259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1597050"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NWE1NTgxOC1mNGU0LTU4YzItYjI3MS1jY2RjMmRjYjI3OTEifQ==",
    "nonce": 6988,
    "balances": {
      "current": "12971631980208195",
      "previous": "12971633578856104"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc17d8114fabcf0c38f1877e4aa46e4041a23604a",
    "nonce": 22,
    "balances": {
      "current": "1597050859",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:13.013Z",
  "updated": "2020-05-22T08:53:13.102Z",
  "id": "5ec792f9005df800101bcb59"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000005f310feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1597050859`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`