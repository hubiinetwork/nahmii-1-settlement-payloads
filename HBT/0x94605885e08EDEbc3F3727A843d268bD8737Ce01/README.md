# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x94605885e08EDEbc3F3727A843d268bD8737Ce01`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000000000000000000000000000000000000000003d62b6748befb5ad48c19a1c6e222a7c8086f4087e7555032a4c78de211ce48e663107fe24113a2706d67dae61f54208d8d94e030c5ebf1cd8c5cee7dc189037e75abf8a9b5a6547bb41173947c643eb70b2dfe7b4725155ac8d1802e76799d4a1000000000000000000000000000000000000000000000000000000000000001c89597a5ccbdbcb3c8de26addd352306e69fbda66871af36638cdedefc6ae302387a498f31dd147e646385bd75fe57a87ca2b06c96bb5d10f746ffd49591927343674061d16e42c809da111945287360152a34df111048d69fc39a62cf3dbf8c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4fe0351c9e000000000000000000000000000000000000000000000000002e1d4fe0351cdc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c15a5332000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6a6b7a4e4464694d6931684f474a6c4c54557a595459744f44686b4d43316c5a6d4d784e7a6730596d4d334f47596966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000094605885e08edebc3f3727a843d268bd8737ce01000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x62b6748befb5ad48c19a1c6e222a7c8086f4087e7555032a4c78de211ce48e66",
      "signature": {
        "s": "0x5abf8a9b5a6547bb41173947c643eb70b2dfe7b4725155ac8d1802e76799d4a1",
        "r": "0x3107fe24113a2706d67dae61f54208d8d94e030c5ebf1cd8c5cee7dc189037e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x89597a5ccbdbcb3c8de26addd352306e69fbda66871af36638cdedefc6ae3023",
      "signature": {
        "s": "0x3674061d16e42c809da111945287360152a34df111048d69fc39a62cf3dbf8c4",
        "r": "0x87a498f31dd147e646385bd75fe57a87ca2b06c96bb5d10f746ffd4959192734",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "61",
    "total": "61"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61",
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
            "amount": "37603660594"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MjkzNDdiMi1hOGJlLTUzYTYtODhkMC1lZmMxNzg0YmM3OGYifQ==",
    "nonce": 5545,
    "balances": {
      "current": "12980077829889182",
      "previous": "12980077829889244"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94605885e08edebc3f3727a843d268bd8737ce01",
    "nonce": 21,
    "balances": {
      "current": "61",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:58.167Z",
  "updated": "2020-05-22T08:41:59.239Z",
  "id": "5ec79056005df800101bc976"
}
```
* *stageAmount*: `61`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000000000000000000000000000000000000000003d62b6748befb5ad48c19a1c6e222a7c8086f4087e7555032a4c78de211ce48e663107fe24113a2706d67dae61f54208d8d94e030c5ebf1cd8c5cee7dc189037e75abf8a9b5a6547bb41173947c643eb70b2dfe7b4725155ac8d1802e76799d4a1000000000000000000000000000000000000000000000000000000000000001c89597a5ccbdbcb3c8de26addd352306e69fbda66871af36638cdedefc6ae302387a498f31dd147e646385bd75fe57a87ca2b06c96bb5d10f746ffd49591927343674061d16e42c809da111945287360152a34df111048d69fc39a62cf3dbf8c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4fe0351c9e000000000000000000000000000000000000000000000000002e1d4fe0351cdc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c15a5332000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d6a6b7a4e4464694d6931684f474a6c4c54557a595459744f44686b4d43316c5a6d4d784e7a6730596d4d334f47596966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000094605885e08edebc3f3727a843d268bd8737ce01000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x62b6748befb5ad48c19a1c6e222a7c8086f4087e7555032a4c78de211ce48e66",
      "signature": {
        "s": "0x5abf8a9b5a6547bb41173947c643eb70b2dfe7b4725155ac8d1802e76799d4a1",
        "r": "0x3107fe24113a2706d67dae61f54208d8d94e030c5ebf1cd8c5cee7dc189037e7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x89597a5ccbdbcb3c8de26addd352306e69fbda66871af36638cdedefc6ae3023",
      "signature": {
        "s": "0x3674061d16e42c809da111945287360152a34df111048d69fc39a62cf3dbf8c4",
        "r": "0x87a498f31dd147e646385bd75fe57a87ca2b06c96bb5d10f746ffd4959192734",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "61",
    "total": "61"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61",
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
            "amount": "37603660594"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MjkzNDdiMi1hOGJlLTUzYTYtODhkMC1lZmMxNzg0YmM3OGYifQ==",
    "nonce": 5545,
    "balances": {
      "current": "12980077829889182",
      "previous": "12980077829889244"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x94605885e08edebc3f3727a843d268bd8737ce01",
    "nonce": 21,
    "balances": {
      "current": "61",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:41:58.167Z",
  "updated": "2020-05-22T08:41:59.239Z",
  "id": "5ec79056005df800101bc976"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000003d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `61`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`