# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb6Dc48BA1ab5F7fA6f406760986407C244CFf261`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000010b4f4cd0000000000000000000000000000000000000000000000000000000010b4f4cd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000010b4f4cd0000000000000000000000000000000000000000000000000000000010b4f4cd4dc6b3ab193b550c99b99122c9e291a07965126a44b47b2b7a07fc587a0dc76fa2e6426eace2068483a738c9ca20cbdd0a189bde90359c0288fb54c25f47cc232fed332e8c9acbad3cf42edbcc0aebfd5e6aae8e58d5f465a0b0a5d9c9ea3b4e000000000000000000000000000000000000000000000000000000000000001c26dcd2e108bfcc43571ab6c635056e9f354ece65fd864557654cbc41914e8edb42b42a9ed6472f2f8089ea3d342822bf063e82e92a3d3acb0d039ad29c21bda0388e827dcffe62c5f6545f760ae2eaccd4745e13fa5e45f5640a17f2f53a4ccd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6109b700a8000000000000000000000000000000000000000000000000002e1d611a703c5b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000446e6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcf6b5fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e546c6d5a444578596930774e47557a4c5455784e6d4574595459784e4330315a54677a596a4e6d59324a685a474d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6dc48ba1ab5f7fa6f406760986407c244cff2610000000000000000000000000000000000000000000000000000000010b4f4cd000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4dc6b3ab193b550c99b99122c9e291a07965126a44b47b2b7a07fc587a0dc76f",
      "signature": {
        "s": "0x2fed332e8c9acbad3cf42edbcc0aebfd5e6aae8e58d5f465a0b0a5d9c9ea3b4e",
        "r": "0xa2e6426eace2068483a738c9ca20cbdd0a189bde90359c0288fb54c25f47cc23",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26dcd2e108bfcc43571ab6c635056e9f354ece65fd864557654cbc41914e8edb",
      "signature": {
        "s": "0x388e827dcffe62c5f6545f760ae2eaccd4745e13fa5e45f5640a17f2f53a4ccd",
        "r": "0x42b42a9ed6472f2f8089ea3d342822bf063e82e92a3d3acb0d039ad29c21bda0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "280294605",
    "total": "280294605"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "280294605",
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
            "amount": "37530023422"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "280294"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNTlmZDExYi0wNGUzLTUxNmEtYTYxNC01ZTgzYjNmY2JhZGMifQ==",
    "nonce": 5486,
    "balances": {
      "current": "12980151540711592",
      "previous": "12980151821286491"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6dc48ba1ab5f7fa6f406760986407c244cff261",
    "nonce": 22,
    "balances": {
      "current": "280294605",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:27.495Z",
  "updated": "2020-05-22T08:41:27.565Z",
  "id": "5ec79037b0c6090011d5afe6"
}
```
* *stageAmount*: `280294605`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000010b4f4cd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000010b4f4cd0000000000000000000000000000000000000000000000000000000010b4f4cd4dc6b3ab193b550c99b99122c9e291a07965126a44b47b2b7a07fc587a0dc76fa2e6426eace2068483a738c9ca20cbdd0a189bde90359c0288fb54c25f47cc232fed332e8c9acbad3cf42edbcc0aebfd5e6aae8e58d5f465a0b0a5d9c9ea3b4e000000000000000000000000000000000000000000000000000000000000001c26dcd2e108bfcc43571ab6c635056e9f354ece65fd864557654cbc41914e8edb42b42a9ed6472f2f8089ea3d342822bf063e82e92a3d3acb0d039ad29c21bda0388e827dcffe62c5f6545f760ae2eaccd4745e13fa5e45f5640a17f2f53a4ccd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6109b700a8000000000000000000000000000000000000000000000000002e1d611a703c5b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000446e6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bcf6b5fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e546c6d5a444578596930774e47557a4c5455784e6d4574595459784e4330315a54677a596a4e6d59324a685a474d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000b6dc48ba1ab5f7fa6f406760986407c244cff2610000000000000000000000000000000000000000000000000000000010b4f4cd000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4dc6b3ab193b550c99b99122c9e291a07965126a44b47b2b7a07fc587a0dc76f",
      "signature": {
        "s": "0x2fed332e8c9acbad3cf42edbcc0aebfd5e6aae8e58d5f465a0b0a5d9c9ea3b4e",
        "r": "0xa2e6426eace2068483a738c9ca20cbdd0a189bde90359c0288fb54c25f47cc23",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26dcd2e108bfcc43571ab6c635056e9f354ece65fd864557654cbc41914e8edb",
      "signature": {
        "s": "0x388e827dcffe62c5f6545f760ae2eaccd4745e13fa5e45f5640a17f2f53a4ccd",
        "r": "0x42b42a9ed6472f2f8089ea3d342822bf063e82e92a3d3acb0d039ad29c21bda0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "280294605",
    "total": "280294605"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "280294605",
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
            "amount": "37530023422"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "280294"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNTlmZDExYi0wNGUzLTUxNmEtYTYxNC01ZTgzYjNmY2JhZGMifQ==",
    "nonce": 5486,
    "balances": {
      "current": "12980151540711592",
      "previous": "12980151821286491"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb6dc48ba1ab5f7fa6f406760986407c244cff261",
    "nonce": 22,
    "balances": {
      "current": "280294605",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:27.495Z",
  "updated": "2020-05-22T08:41:27.565Z",
  "id": "5ec79037b0c6090011d5afe6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000010b4f4cd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `280294605`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`