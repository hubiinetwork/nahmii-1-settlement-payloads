# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3D5F7E48AefafB3CB23CB7A9840F4AEf5B6d9158`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000001bdb25feb00000000000000000000000000000000000000000000000000000001bdb25feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001bdb25feb00000000000000000000000000000000000000000000000000000001bdb25feb8f19ea692daffb8c6c0d671b94d16620b8de5ef11a0de369a9e2134cfb6e134eabfe9408d6d6ca72f1eef091f3280651fb88cb48096256053a62cece14001f105155bcaadfd91e20db8104313b677dd57d0aff862e91309be8aff7f88171b217000000000000000000000000000000000000000000000000000000000000001cd595e4931a9b1856ebc84fcb5589b35a69c10ef173a0a9fabd215acfa4e279a037294d1a36d5bdc13a3a58ace59abc81f05b00972fcab2e0aebfa7b661214afd6d63c1ea5548f79be50c8f2f935cfa62bade424515ca07bca21b4eb4053386aa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000162400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ce9e06378aa000000000000000000000000000000000000000000000000002e1ceb9e87f1c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000072192f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008db7045b8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a4755774f4455314e4331684f5752684c5455354d7a6b744f5759344e533031597a4d3559574a6a4e575a6c5a6a456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003d5f7e48aefafb3cb23cb7a9840f4aef5b6d915800000000000000000000000000000000000000000000000000000001bdb25feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f19ea692daffb8c6c0d671b94d16620b8de5ef11a0de369a9e2134cfb6e134e",
      "signature": {
        "s": "0x5155bcaadfd91e20db8104313b677dd57d0aff862e91309be8aff7f88171b217",
        "r": "0xabfe9408d6d6ca72f1eef091f3280651fb88cb48096256053a62cece14001f10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd595e4931a9b1856ebc84fcb5589b35a69c10ef173a0a9fabd215acfa4e279a0",
      "signature": {
        "s": "0x6d63c1ea5548f79be50c8f2f935cfa62bade424515ca07bca21b4eb4053386aa",
        "r": "0x37294d1a36d5bdc13a3a58ace59abc81f05b00972fcab2e0aebfa7b661214afd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7477551083",
    "total": "7477551083"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7477551083",
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
            "amount": "38041306552"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7477551"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGUwODU1NC1hOWRhLTU5MzktOWY4NS01YzM5YWJjNWZlZjEifQ==",
    "nonce": 5668,
    "balances": {
      "current": "12979639746263210",
      "previous": "12979647231291844"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3d5f7e48aefafb3cb23cb7a9840f4aef5b6d9158",
    "nonce": 22,
    "balances": {
      "current": "7477551083",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:57.984Z",
  "updated": "2020-05-22T08:42:58.083Z",
  "id": "5ec79091b0c6090011d5b02a"
}
```
* *stageAmount*: `7477551083`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000001bdb25feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001bdb25feb00000000000000000000000000000000000000000000000000000001bdb25feb8f19ea692daffb8c6c0d671b94d16620b8de5ef11a0de369a9e2134cfb6e134eabfe9408d6d6ca72f1eef091f3280651fb88cb48096256053a62cece14001f105155bcaadfd91e20db8104313b677dd57d0aff862e91309be8aff7f88171b217000000000000000000000000000000000000000000000000000000000000001cd595e4931a9b1856ebc84fcb5589b35a69c10ef173a0a9fabd215acfa4e279a037294d1a36d5bdc13a3a58ace59abc81f05b00972fcab2e0aebfa7b661214afd6d63c1ea5548f79be50c8f2f935cfa62bade424515ca07bca21b4eb4053386aa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000162400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ce9e06378aa000000000000000000000000000000000000000000000000002e1ceb9e87f1c400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000072192f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008db7045b8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a4755774f4455314e4331684f5752684c5455354d7a6b744f5759344e533031597a4d3559574a6a4e575a6c5a6a456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003d5f7e48aefafb3cb23cb7a9840f4aef5b6d915800000000000000000000000000000000000000000000000000000001bdb25feb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f19ea692daffb8c6c0d671b94d16620b8de5ef11a0de369a9e2134cfb6e134e",
      "signature": {
        "s": "0x5155bcaadfd91e20db8104313b677dd57d0aff862e91309be8aff7f88171b217",
        "r": "0xabfe9408d6d6ca72f1eef091f3280651fb88cb48096256053a62cece14001f10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd595e4931a9b1856ebc84fcb5589b35a69c10ef173a0a9fabd215acfa4e279a0",
      "signature": {
        "s": "0x6d63c1ea5548f79be50c8f2f935cfa62bade424515ca07bca21b4eb4053386aa",
        "r": "0x37294d1a36d5bdc13a3a58ace59abc81f05b00972fcab2e0aebfa7b661214afd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7477551083",
    "total": "7477551083"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7477551083",
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
            "amount": "38041306552"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7477551"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZGUwODU1NC1hOWRhLTU5MzktOWY4NS01YzM5YWJjNWZlZjEifQ==",
    "nonce": 5668,
    "balances": {
      "current": "12979639746263210",
      "previous": "12979647231291844"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3d5f7e48aefafb3cb23cb7a9840f4aef5b6d9158",
    "nonce": 22,
    "balances": {
      "current": "7477551083",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:57.984Z",
  "updated": "2020-05-22T08:42:58.083Z",
  "id": "5ec79091b0c6090011d5b02a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000001bdb25feb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7477551083`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`