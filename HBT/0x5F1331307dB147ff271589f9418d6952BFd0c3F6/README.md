# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5F1331307dB147ff271589f9418d6952BFd0c3F6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000033aa00000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000033aa00000000000000000000000000000000000000000000000000000000000033aabb363b5be313d880e644e9732f64e4d22e14803c1f56dd96cda9b378e379814ac911c5dc0dd0d86833ac7bd80ff7af680b16886dda2256398319a15ee08a0a51558aa410671d9ea2354cfc49b7968281e8cd7d018dd084b5fa522bf999cc279a000000000000000000000000000000000000000000000000000000000000001bf80538efdab10fbe091f98747bc3aea2cf37a73554b2f949c6caea2ce9424d06498cdb92c9dbb089625a012a05f163638b9cae336ba39193cbecf3550a44e81319530cd70474486877b5da91edfac762dc3ca81226aa426e73280bcbc867c975000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ce57e3d9706000000000000000000000000000000000000000000000000002e1ce57e3dcabd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008dc8f4153000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d4456684f5755304d79316b5a5464684c54566d4e6a63744f4445334d53316b5a6a6c695a6d557a4e44566a4f474d6966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000005f1331307db147ff271589f9418d6952bfd0c3f600000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb363b5be313d880e644e9732f64e4d22e14803c1f56dd96cda9b378e379814a",
      "signature": {
        "s": "0x558aa410671d9ea2354cfc49b7968281e8cd7d018dd084b5fa522bf999cc279a",
        "r": "0xc911c5dc0dd0d86833ac7bd80ff7af680b16886dda2256398319a15ee08a0a51",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf80538efdab10fbe091f98747bc3aea2cf37a73554b2f949c6caea2ce9424d06",
      "signature": {
        "s": "0x19530cd70474486877b5da91edfac762dc3ca81226aa426e73280bcbc867c975",
        "r": "0x498cdb92c9dbb089625a012a05f163638b9cae336ba39193cbecf3550a44e813",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13226",
    "total": "13226"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226",
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
            "amount": "38060114259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMDVhOWU0My1kZTdhLTVmNjctODE3MS1kZjliZmUzNDVjOGMifQ==",
    "nonce": 5682,
    "balances": {
      "current": "12979620919744262",
      "previous": "12979620919757501"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f1331307db147ff271589f9418d6952bfd0c3f6",
    "nonce": 21,
    "balances": {
      "current": "13226",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:02.628Z",
  "updated": "2020-05-22T08:43:02.697Z",
  "id": "5ec79096e5756b00111b86b4"
}
```
* *stageAmount*: `13226`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000033aa00000000000000000000000000000000000000000000000000000000000033aabb363b5be313d880e644e9732f64e4d22e14803c1f56dd96cda9b378e379814ac911c5dc0dd0d86833ac7bd80ff7af680b16886dda2256398319a15ee08a0a51558aa410671d9ea2354cfc49b7968281e8cd7d018dd084b5fa522bf999cc279a000000000000000000000000000000000000000000000000000000000000001bf80538efdab10fbe091f98747bc3aea2cf37a73554b2f949c6caea2ce9424d06498cdb92c9dbb089625a012a05f163638b9cae336ba39193cbecf3550a44e81319530cd70474486877b5da91edfac762dc3ca81226aa426e73280bcbc867c975000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ce57e3d9706000000000000000000000000000000000000000000000000002e1ce57e3dcabd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008dc8f4153000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d4456684f5755304d79316b5a5464684c54566d4e6a63744f4445334d53316b5a6a6c695a6d557a4e44566a4f474d6966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000005f1331307db147ff271589f9418d6952bfd0c3f600000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb363b5be313d880e644e9732f64e4d22e14803c1f56dd96cda9b378e379814a",
      "signature": {
        "s": "0x558aa410671d9ea2354cfc49b7968281e8cd7d018dd084b5fa522bf999cc279a",
        "r": "0xc911c5dc0dd0d86833ac7bd80ff7af680b16886dda2256398319a15ee08a0a51",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf80538efdab10fbe091f98747bc3aea2cf37a73554b2f949c6caea2ce9424d06",
      "signature": {
        "s": "0x19530cd70474486877b5da91edfac762dc3ca81226aa426e73280bcbc867c975",
        "r": "0x498cdb92c9dbb089625a012a05f163638b9cae336ba39193cbecf3550a44e813",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "13226",
    "total": "13226"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226",
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
            "amount": "38060114259"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMDVhOWU0My1kZTdhLTVmNjctODE3MS1kZjliZmUzNDVjOGMifQ==",
    "nonce": 5682,
    "balances": {
      "current": "12979620919744262",
      "previous": "12979620919757501"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f1331307db147ff271589f9418d6952bfd0c3f6",
    "nonce": 21,
    "balances": {
      "current": "13226",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:02.628Z",
  "updated": "2020-05-22T08:43:02.697Z",
  "id": "5ec79096e5756b00111b86b4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13226`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`