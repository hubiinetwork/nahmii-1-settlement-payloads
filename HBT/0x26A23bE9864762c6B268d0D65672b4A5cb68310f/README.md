# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x26A23bE9864762c6B268d0D65672b4A5cb68310f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000000000000000000000000000000000009a14c47e7c3bee25d19f5375336e2f365cbe37dbe3bf41812d4428a549ede30dc982c30389704d0118fb46723026cadd93a5830078afb9d2d7a0678e085432c27abb9c3f5b7f2de6627bdb51e848fb6eb4aa5b9c5eda0e84d3b89b5880fe58a8eaf84d46000000000000000000000000000000000000000000000000000000000000001b3c592af1c1556aef1b515a90def02aadc803eb7e9b9f82968fcf05f60e137822d6a1ffdcb8c9bd7182098b573386dee59e97dc3bef020d134e733b2f46bd030f3ece6595b625d8cff7100d83cd71eb77c98dce89b61e6f7dbebc7179303128f6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d5f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b6ddbec9042000000000000000000000000000000000000000000000000002e0b6e7628c69c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002771dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d54277dc4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4463324f4468685a4330784e7a67354c5455334f574d74596a41354d53316c596d59304e4759784e324a695957556966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000026a23be9864762c6b268d0d65672b4a5cb68310f000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c3bee25d19f5375336e2f365cbe37dbe3bf41812d4428a549ede30dc982c303",
      "signature": {
        "s": "0x5b7f2de6627bdb51e848fb6eb4aa5b9c5eda0e84d3b89b5880fe58a8eaf84d46",
        "r": "0x89704d0118fb46723026cadd93a5830078afb9d2d7a0678e085432c27abb9c3f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3c592af1c1556aef1b515a90def02aadc803eb7e9b9f82968fcf05f60e137822",
      "signature": {
        "s": "0x3ece6595b625d8cff7100d83cd71eb77c98dce89b61e6f7dbebc7179303128f6",
        "r": "0xd6a1ffdcb8c9bd7182098b573386dee59e97dc3bef020d134e733b2f46bd030f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2585052286",
    "total": "2585052286"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2585052286",
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
            "amount": "57246449092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2585052"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDc2ODhhZC0xNzg5LTU3OWMtYjA5MS1lYmY0NGYxN2JiYWUifQ==",
    "nonce": 7519,
    "balances": {
      "current": "12960415397744706",
      "previous": "12960417985382044"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x26a23be9864762c6b268d0d65672b4a5cb68310f",
    "nonce": 10,
    "balances": {
      "current": "2585052286",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:22.474Z",
  "updated": "2020-05-22T08:57:22.549Z",
  "id": "5ec793f2e5756b00111b88fd"
}
```
* *stageAmount*: `2585052286`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000000000000000000000000000000000009a14c47e7c3bee25d19f5375336e2f365cbe37dbe3bf41812d4428a549ede30dc982c30389704d0118fb46723026cadd93a5830078afb9d2d7a0678e085432c27abb9c3f5b7f2de6627bdb51e848fb6eb4aa5b9c5eda0e84d3b89b5880fe58a8eaf84d46000000000000000000000000000000000000000000000000000000000000001b3c592af1c1556aef1b515a90def02aadc803eb7e9b9f82968fcf05f60e137822d6a1ffdcb8c9bd7182098b573386dee59e97dc3bef020d134e733b2f46bd030f3ece6595b625d8cff7100d83cd71eb77c98dce89b61e6f7dbebc7179303128f6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d5f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b6ddbec9042000000000000000000000000000000000000000000000000002e0b6e7628c69c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002771dc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d54277dc4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a4463324f4468685a4330784e7a67354c5455334f574d74596a41354d53316c596d59304e4759784e324a695957556966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000026a23be9864762c6b268d0d65672b4a5cb68310f000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c3bee25d19f5375336e2f365cbe37dbe3bf41812d4428a549ede30dc982c303",
      "signature": {
        "s": "0x5b7f2de6627bdb51e848fb6eb4aa5b9c5eda0e84d3b89b5880fe58a8eaf84d46",
        "r": "0x89704d0118fb46723026cadd93a5830078afb9d2d7a0678e085432c27abb9c3f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3c592af1c1556aef1b515a90def02aadc803eb7e9b9f82968fcf05f60e137822",
      "signature": {
        "s": "0x3ece6595b625d8cff7100d83cd71eb77c98dce89b61e6f7dbebc7179303128f6",
        "r": "0xd6a1ffdcb8c9bd7182098b573386dee59e97dc3bef020d134e733b2f46bd030f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2585052286",
    "total": "2585052286"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2585052286",
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
            "amount": "57246449092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2585052"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZDc2ODhhZC0xNzg5LTU3OWMtYjA5MS1lYmY0NGYxN2JiYWUifQ==",
    "nonce": 7519,
    "balances": {
      "current": "12960415397744706",
      "previous": "12960417985382044"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x26a23be9864762c6b268d0d65672b4a5cb68310f",
    "nonce": 10,
    "balances": {
      "current": "2585052286",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:22.474Z",
  "updated": "2020-05-22T08:57:22.549Z",
  "id": "5ec793f2e5756b00111b88fd"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000009a14c47e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2585052286`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`