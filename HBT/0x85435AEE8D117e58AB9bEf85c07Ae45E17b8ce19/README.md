# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x85435AEE8D117e58AB9bEf85c07Ae45E17b8ce19`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000000000000000000000000000000000000000214b40783dddf273657ba00d165999cbaf5f903d3f11d46d9dd463b2d9fe4c648ed87a906ef016eab53f376ba832ddb407743df70e9b75423338787ce71355c9b79d638d37bc6e4f7fa0fd92b624b21690455dff85f5e8d9fbc5be1bec933d21d625000000000000000000000000000000000000000000000000000000000000001c6475a302399f0d39715ce251ba226b925513b6cbac7920f8eb633136dd7fc3a5b3d6b3ef0cbb0ea050f487f3369eb8f9b6e2e7e4962cb732fb347f87000be23232ed3e696fc353ef44427b9794516a49b78f3f9b7d319f226f8d71f268088b0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dcd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b18c7f6ac73000000000000000000000000000000000000000000000000002e0b18c7f6cdc600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000008000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d69e9971d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f575a6d4f4445774d4330305a444d7a4c5455354e44557459544e6b4e79316c595463314f574d7a4d6a55344e57556966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000085435aee8d117e58ab9bef85c07ae45e17b8ce19000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40783dddf273657ba00d165999cbaf5f903d3f11d46d9dd463b2d9fe4c648ed8",
      "signature": {
        "s": "0x638d37bc6e4f7fa0fd92b624b21690455dff85f5e8d9fbc5be1bec933d21d625",
        "r": "0x7a906ef016eab53f376ba832ddb407743df70e9b75423338787ce71355c9b79d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6475a302399f0d39715ce251ba226b925513b6cbac7920f8eb633136dd7fc3a5",
      "signature": {
        "s": "0x32ed3e696fc353ef44427b9794516a49b78f3f9b7d319f226f8d71f268088b0d",
        "r": "0xb3d6b3ef0cbb0ea050f487f3369eb8f9b6e2e7e4962cb732fb347f87000be232",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8523",
    "total": "8523"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8523",
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
            "amount": "57611491101"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OWZmODEwMC00ZDMzLTU5NDUtYTNkNy1lYTc1OWMzMjU4NWUifQ==",
    "nonce": 7629,
    "balances": {
      "current": "12960049990642803",
      "previous": "12960049990651334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x85435aee8d117e58ab9bef85c07ae45e17b8ce19",
    "nonce": 4,
    "balances": {
      "current": "8523",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:11.790Z",
  "updated": "2020-05-22T08:58:11.884Z",
  "id": "5ec79423e5756b00111b8925"
}
```
* *stageAmount*: `8523`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000000000000000000000000000000000000000214b40783dddf273657ba00d165999cbaf5f903d3f11d46d9dd463b2d9fe4c648ed87a906ef016eab53f376ba832ddb407743df70e9b75423338787ce71355c9b79d638d37bc6e4f7fa0fd92b624b21690455dff85f5e8d9fbc5be1bec933d21d625000000000000000000000000000000000000000000000000000000000000001c6475a302399f0d39715ce251ba226b925513b6cbac7920f8eb633136dd7fc3a5b3d6b3ef0cbb0ea050f487f3369eb8f9b6e2e7e4962cb732fb347f87000be23232ed3e696fc353ef44427b9794516a49b78f3f9b7d319f226f8d71f268088b0d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001dcd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b18c7f6ac73000000000000000000000000000000000000000000000000002e0b18c7f6cdc600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000008000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d69e9971d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f575a6d4f4445774d4330305a444d7a4c5455354e44557459544e6b4e79316c595463314f574d7a4d6a55344e57556966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000085435aee8d117e58ab9bef85c07ae45e17b8ce19000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40783dddf273657ba00d165999cbaf5f903d3f11d46d9dd463b2d9fe4c648ed8",
      "signature": {
        "s": "0x638d37bc6e4f7fa0fd92b624b21690455dff85f5e8d9fbc5be1bec933d21d625",
        "r": "0x7a906ef016eab53f376ba832ddb407743df70e9b75423338787ce71355c9b79d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6475a302399f0d39715ce251ba226b925513b6cbac7920f8eb633136dd7fc3a5",
      "signature": {
        "s": "0x32ed3e696fc353ef44427b9794516a49b78f3f9b7d319f226f8d71f268088b0d",
        "r": "0xb3d6b3ef0cbb0ea050f487f3369eb8f9b6e2e7e4962cb732fb347f87000be232",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8523",
    "total": "8523"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8523",
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
            "amount": "57611491101"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OWZmODEwMC00ZDMzLTU5NDUtYTNkNy1lYTc1OWMzMjU4NWUifQ==",
    "nonce": 7629,
    "balances": {
      "current": "12960049990642803",
      "previous": "12960049990651334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x85435aee8d117e58ab9bef85c07ae45e17b8ce19",
    "nonce": 4,
    "balances": {
      "current": "8523",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:11.790Z",
  "updated": "2020-05-22T08:58:11.884Z",
  "id": "5ec79423e5756b00111b8925"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000214b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8523`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`