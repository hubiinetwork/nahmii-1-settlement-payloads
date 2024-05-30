# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4641f76fe9B1cDbDC65A125254aB0aba5DCb9f5C`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000008abee190000000000000000000000000000000000000000000000000000000008abee19000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008abee190000000000000000000000000000000000000000000000000000000008abee19f7f515fa9ff4d051512c9b0f0a4cbea8f43307b95da22c86df4103030503bb197290270aa5ea365ddcad4152da409c440cd8b2270d008753178015472e41274c49053a615080b3c204c97693349e88d0bed49a1cec4da9970da8538f0dc6bd4f000000000000000000000000000000000000000000000000000000000000001c27b81327ba0514d53e598ec3355df0825279d2059cc74e3656bcdb2b427529163099672629f8a5ca1c4c92ae8752e8c9b4f6a2e4cadd4926fc46e8c249374ed745d532c13f1556aba09505418ab712821eb051b17f5ed026581f0638d68363a7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139cea78d8eb000000000000000000000000000000000000000000000000002e139cf326ff5100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002384d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3c5b0384000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a545178597a41775a4330784f57466c4c5455344e5451744f574d774e6930345a6d4d785a4452694d6a64694e57456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004641f76fe9b1cdbdc65a125254ab0aba5dcb9f5c0000000000000000000000000000000000000000000000000000000008abee19000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7f515fa9ff4d051512c9b0f0a4cbea8f43307b95da22c86df4103030503bb19",
      "signature": {
        "s": "0x49053a615080b3c204c97693349e88d0bed49a1cec4da9970da8538f0dc6bd4f",
        "r": "0x7290270aa5ea365ddcad4152da409c440cd8b2270d008753178015472e41274c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27b81327ba0514d53e598ec3355df0825279d2059cc74e3656bcdb2b42752916",
      "signature": {
        "s": "0x45d532c13f1556aba09505418ab712821eb051b17f5ed026581f0638d68363a7",
        "r": "0x3099672629f8a5ca1c4c92ae8752e8c9b4f6a2e4cadd4926fc46e8c249374ed7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "145485337",
    "total": "145485337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "145485337",
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
            "amount": "48257237892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "145485"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZTQxYzAwZC0xOWFlLTU4NTQtOWMwNi04ZmMxZDRiMjdiNWEifQ==",
    "nonce": 7210,
    "balances": {
      "current": "12969413598304491",
      "previous": "12969413743935313"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4641f76fe9b1cdbdc65a125254ab0aba5dcb9f5c",
    "nonce": 22,
    "balances": {
      "current": "145485337",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:03.676Z",
  "updated": "2020-05-22T08:55:03.736Z",
  "id": "5ec79367e5756b00111b88a1"
}
```
* *stageAmount*: `145485337`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000008abee19000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008abee190000000000000000000000000000000000000000000000000000000008abee19f7f515fa9ff4d051512c9b0f0a4cbea8f43307b95da22c86df4103030503bb197290270aa5ea365ddcad4152da409c440cd8b2270d008753178015472e41274c49053a615080b3c204c97693349e88d0bed49a1cec4da9970da8538f0dc6bd4f000000000000000000000000000000000000000000000000000000000000001c27b81327ba0514d53e598ec3355df0825279d2059cc74e3656bcdb2b427529163099672629f8a5ca1c4c92ae8752e8c9b4f6a2e4cadd4926fc46e8c249374ed745d532c13f1556aba09505418ab712821eb051b17f5ed026581f0638d68363a7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139cea78d8eb000000000000000000000000000000000000000000000000002e139cf326ff5100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000002384d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3c5b0384000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a545178597a41775a4330784f57466c4c5455344e5451744f574d774e6930345a6d4d785a4452694d6a64694e57456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004641f76fe9b1cdbdc65a125254ab0aba5dcb9f5c0000000000000000000000000000000000000000000000000000000008abee19000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7f515fa9ff4d051512c9b0f0a4cbea8f43307b95da22c86df4103030503bb19",
      "signature": {
        "s": "0x49053a615080b3c204c97693349e88d0bed49a1cec4da9970da8538f0dc6bd4f",
        "r": "0x7290270aa5ea365ddcad4152da409c440cd8b2270d008753178015472e41274c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27b81327ba0514d53e598ec3355df0825279d2059cc74e3656bcdb2b42752916",
      "signature": {
        "s": "0x45d532c13f1556aba09505418ab712821eb051b17f5ed026581f0638d68363a7",
        "r": "0x3099672629f8a5ca1c4c92ae8752e8c9b4f6a2e4cadd4926fc46e8c249374ed7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "145485337",
    "total": "145485337"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "145485337",
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
            "amount": "48257237892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "145485"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZTQxYzAwZC0xOWFlLTU4NTQtOWMwNi04ZmMxZDRiMjdiNWEifQ==",
    "nonce": 7210,
    "balances": {
      "current": "12969413598304491",
      "previous": "12969413743935313"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4641f76fe9b1cdbdc65a125254ab0aba5dcb9f5c",
    "nonce": 22,
    "balances": {
      "current": "145485337",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:03.676Z",
  "updated": "2020-05-22T08:55:03.736Z",
  "id": "5ec79367e5756b00111b88a1"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000008abee19000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `145485337`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`