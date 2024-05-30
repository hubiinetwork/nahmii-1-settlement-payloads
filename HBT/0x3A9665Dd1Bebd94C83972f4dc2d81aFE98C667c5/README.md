# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3A9665Dd1Bebd94C83972f4dc2d81aFE98C667c5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000069f4ab600000000000000000000000000000000000000000000000000000000069f4ab6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000069f4ab600000000000000000000000000000000000000000000000000000000069f4ab6229743051febf2fca1d21a2bf30bb463785452e95b84754564776a3fc3a5f159160f73adea34e5f31fe721173bebcb7830847297d066112f8845dc91ada00e9f3fbd0056a9310d646cf6478aa668f5bacdd1aad4012bede6cdf726fd3802a8ea000000000000000000000000000000000000000000000000000000000000001b8f5de11254cf5ba4c7d6ce15a58a395e5d14a92f3eadd0c6347449c4f4b37f1c64add3c96a053d97c5719786ffc776094df8a0548710100799f2a6e3eb7f16862aaa6ed9a18a3ccbdb798bc1e292ba69ff7290e754de6275b5cc8e32983d498e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56870000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000185a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad4c0b0fd78000000000000000000000000000000000000000000000000002e1ad4c751fa2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001b1fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963c82aac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a47526b5a6a4a695a533034597a49334c545534597a45744f444d324e79316c596a5932597a49324e5459344e54416966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a9665dd1bebd94c83972f4dc2d81afe98c667c500000000000000000000000000000000000000000000000000000000069f4ab6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x229743051febf2fca1d21a2bf30bb463785452e95b84754564776a3fc3a5f159",
      "signature": {
        "s": "0x3fbd0056a9310d646cf6478aa668f5bacdd1aad4012bede6cdf726fd3802a8ea",
        "r": "0x160f73adea34e5f31fe721173bebcb7830847297d066112f8845dc91ada00e9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f5de11254cf5ba4c7d6ce15a58a395e5d14a92f3eadd0c6347449c4f4b37f1c",
      "signature": {
        "s": "0x2aaa6ed9a18a3ccbdb798bc1e292ba69ff7290e754de6275b5cc8e32983d498e",
        "r": "0x64add3c96a053d97c5719786ffc776094df8a0548710100799f2a6e3eb7f1686",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "111102646",
    "total": "111102646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "111102646",
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
            "amount": "40328768172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "111102"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZGRkZjJiZS04YzI3LTU4YzEtODM2Ny1lYjY2YzI2NTY4NTAifQ==",
    "nonce": 6234,
    "balances": {
      "current": "12977349996903800",
      "previous": "12977350108117548"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a9665dd1bebd94c83972f4dc2d81afe98c667c5",
    "nonce": 22,
    "balances": {
      "current": "111102646",
      "previous": "0"
    }
  },
  "blockNumber": "10114695",
  "created": "2020-05-22T08:47:34.232Z",
  "updated": "2020-05-22T08:47:34.302Z",
  "id": "5ec791a6b0c6090011d5b0e4"
}
```
* *stageAmount*: `111102646`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000069f4ab6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000069f4ab600000000000000000000000000000000000000000000000000000000069f4ab6229743051febf2fca1d21a2bf30bb463785452e95b84754564776a3fc3a5f159160f73adea34e5f31fe721173bebcb7830847297d066112f8845dc91ada00e9f3fbd0056a9310d646cf6478aa668f5bacdd1aad4012bede6cdf726fd3802a8ea000000000000000000000000000000000000000000000000000000000000001b8f5de11254cf5ba4c7d6ce15a58a395e5d14a92f3eadd0c6347449c4f4b37f1c64add3c96a053d97c5719786ffc776094df8a0548710100799f2a6e3eb7f16862aaa6ed9a18a3ccbdb798bc1e292ba69ff7290e754de6275b5cc8e32983d498e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56870000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000185a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad4c0b0fd78000000000000000000000000000000000000000000000000002e1ad4c751fa2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001b1fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963c82aac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a47526b5a6a4a695a533034597a49334c545534597a45744f444d324e79316c596a5932597a49324e5459344e54416966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a9665dd1bebd94c83972f4dc2d81afe98c667c500000000000000000000000000000000000000000000000000000000069f4ab6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x229743051febf2fca1d21a2bf30bb463785452e95b84754564776a3fc3a5f159",
      "signature": {
        "s": "0x3fbd0056a9310d646cf6478aa668f5bacdd1aad4012bede6cdf726fd3802a8ea",
        "r": "0x160f73adea34e5f31fe721173bebcb7830847297d066112f8845dc91ada00e9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f5de11254cf5ba4c7d6ce15a58a395e5d14a92f3eadd0c6347449c4f4b37f1c",
      "signature": {
        "s": "0x2aaa6ed9a18a3ccbdb798bc1e292ba69ff7290e754de6275b5cc8e32983d498e",
        "r": "0x64add3c96a053d97c5719786ffc776094df8a0548710100799f2a6e3eb7f1686",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "111102646",
    "total": "111102646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "111102646",
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
            "amount": "40328768172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "111102"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZGRkZjJiZS04YzI3LTU4YzEtODM2Ny1lYjY2YzI2NTY4NTAifQ==",
    "nonce": 6234,
    "balances": {
      "current": "12977349996903800",
      "previous": "12977350108117548"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a9665dd1bebd94c83972f4dc2d81afe98c667c5",
    "nonce": 22,
    "balances": {
      "current": "111102646",
      "previous": "0"
    }
  },
  "blockNumber": "10114695",
  "created": "2020-05-22T08:47:34.232Z",
  "updated": "2020-05-22T08:47:34.302Z",
  "id": "5ec791a6b0c6090011d5b0e4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000069f4ab6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `111102646`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`