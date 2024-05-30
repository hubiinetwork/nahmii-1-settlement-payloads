# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3a40C2eA7C29E946C8292e94a7055dAEc19e61bD`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000000000000000000000000000000000000a293ffc883e0a74408dcaf83cb7a8df469aeba307351a2a8ec8f48753f4ee552bfe5ada65985793fe0751d1f217f2331da51c4bf87e8b2cd5b9e79097100075c61fdb68212d2ff6a9d1c564c52a01fce739575ab10780e24e1db268c79d0de9ee51c8ec000000000000000000000000000000000000000000000000000000000000001b331926a907f0696a46cba886d4e95c7fe3f1a0efa26b11c62c59d9e67a9c31a5248fb38e8e66bf1e7c860e99dad3c0d452fdf7d7daf3ceb4cc6e1b59ed227c0829f2087550641075cd559bf4a4fe952e2282650d26bfdccdc730a2ce46b3ff50000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b3100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a4e5000e00000000000000000000000000000000000000000000000000002e15a4ef2be7e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000299eb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab75fbd58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f544a695932457859693031593249794c5455795a6d5974595452684d7930334e7a566a4f474d344d4751774e6d496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a40c2ea7c29e946c8292e94a7055daec19e61bd000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x883e0a74408dcaf83cb7a8df469aeba307351a2a8ec8f48753f4ee552bfe5ada",
      "signature": {
        "s": "0x212d2ff6a9d1c564c52a01fce739575ab10780e24e1db268c79d0de9ee51c8ec",
        "r": "0x65985793fe0751d1f217f2331da51c4bf87e8b2cd5b9e79097100075c61fdb68",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x331926a907f0696a46cba886d4e95c7fe3f1a0efa26b11c62c59d9e67a9c31a5",
      "signature": {
        "s": "0x29f2087550641075cd559bf4a4fe952e2282650d26bfdccdc730a2ce46b3ff50",
        "r": "0x248fb38e8e66bf1e7c860e99dad3c0d452fdf7d7daf3ceb4cc6e1b59ed227c08",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "170475516",
    "total": "170475516"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "170475516",
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
            "amount": "46026177880"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "170475"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmOTJiY2ExYi01Y2IyLTUyZmYtYTRhMy03NzVjOGM4MGQwNmIifQ==",
    "nonce": 6961,
    "balances": {
      "current": "12971646889496064",
      "previous": "12971647060142055"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a40c2ea7c29e946c8292e94a7055daec19e61bd",
    "nonce": 22,
    "balances": {
      "current": "170475516",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:03.515Z",
  "updated": "2020-05-22T08:53:03.583Z",
  "id": "5ec792ef005df800101bcb50"
}
```
* *stageAmount*: `170475516`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000000000000000000000000000000000000a293ffc883e0a74408dcaf83cb7a8df469aeba307351a2a8ec8f48753f4ee552bfe5ada65985793fe0751d1f217f2331da51c4bf87e8b2cd5b9e79097100075c61fdb68212d2ff6a9d1c564c52a01fce739575ab10780e24e1db268c79d0de9ee51c8ec000000000000000000000000000000000000000000000000000000000000001b331926a907f0696a46cba886d4e95c7fe3f1a0efa26b11c62c59d9e67a9c31a5248fb38e8e66bf1e7c860e99dad3c0d452fdf7d7daf3ceb4cc6e1b59ed227c0829f2087550641075cd559bf4a4fe952e2282650d26bfdccdc730a2ce46b3ff50000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b3100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a4e5000e00000000000000000000000000000000000000000000000000002e15a4ef2be7e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000299eb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab75fbd58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f544a695932457859693031593249794c5455795a6d5974595452684d7930334e7a566a4f474d344d4751774e6d496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003a40c2ea7c29e946c8292e94a7055daec19e61bd000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x883e0a74408dcaf83cb7a8df469aeba307351a2a8ec8f48753f4ee552bfe5ada",
      "signature": {
        "s": "0x212d2ff6a9d1c564c52a01fce739575ab10780e24e1db268c79d0de9ee51c8ec",
        "r": "0x65985793fe0751d1f217f2331da51c4bf87e8b2cd5b9e79097100075c61fdb68",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x331926a907f0696a46cba886d4e95c7fe3f1a0efa26b11c62c59d9e67a9c31a5",
      "signature": {
        "s": "0x29f2087550641075cd559bf4a4fe952e2282650d26bfdccdc730a2ce46b3ff50",
        "r": "0x248fb38e8e66bf1e7c860e99dad3c0d452fdf7d7daf3ceb4cc6e1b59ed227c08",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "170475516",
    "total": "170475516"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "170475516",
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
            "amount": "46026177880"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "170475"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmOTJiY2ExYi01Y2IyLTUyZmYtYTRhMy03NzVjOGM4MGQwNmIifQ==",
    "nonce": 6961,
    "balances": {
      "current": "12971646889496064",
      "previous": "12971647060142055"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3a40c2ea7c29e946c8292e94a7055daec19e61bd",
    "nonce": 22,
    "balances": {
      "current": "170475516",
      "previous": "0"
    }
  },
  "blockNumber": "10114723",
  "created": "2020-05-22T08:53:03.515Z",
  "updated": "2020-05-22T08:53:03.583Z",
  "id": "5ec792ef005df800101bcb50"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000a293ffc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `170475516`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`