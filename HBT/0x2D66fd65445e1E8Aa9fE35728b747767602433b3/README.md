# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2D66fd65445e1E8Aa9fE35728b747767602433b3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000000000000000000000000000000000003ebd56844eb1fd51e91ab8624d39625fe62570bc0d018039a889e4883da5a8fd9d2b9fafeca5365f618e553235e8078b961d2ee766deec2f1258b0b7f0fbfeb32722a1d36d382f71fba9938ebd38006fa5cc402824c184729d6be91f218c1d0cbdabff03000000000000000000000000000000000000000000000000000000000000001b436411bce110f772d3acb8de8908d0fb74662ec528d177e1e63c541c99cc568fd0d83079848917627c14c344de9e0de955c6f4fe2ff120370bb668b0a7043e4b1aa5e7f5fa46a3e4dfa565a4fff58f70d0d41a603815af6529e2e76053282625000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d60cae99a71000000000000000000000000000000000000000000000000002e1d6109b700a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000100fb3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd06c5b1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d475133596a55314d5330314e5468684c5455324d6a67744f444d785a6930334e5441774d4759304e7a59774e54636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002d66fd65445e1e8aa9fe35728b747767602433b3000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4eb1fd51e91ab8624d39625fe62570bc0d018039a889e4883da5a8fd9d2b9faf",
      "signature": {
        "s": "0x6d382f71fba9938ebd38006fa5cc402824c184729d6be91f218c1d0cbdabff03",
        "r": "0xeca5365f618e553235e8078b961d2ee766deec2f1258b0b7f0fbfeb32722a1d3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x436411bce110f772d3acb8de8908d0fb74662ec528d177e1e63c541c99cc568f",
      "signature": {
        "s": "0x1aa5e7f5fa46a3e4dfa565a4fff58f70d0d41a603815af6529e2e76053282625",
        "r": "0xd0d83079848917627c14c344de9e0de955c6f4fe2ff120370bb668b0a7043e4b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1052595844",
    "total": "1052595844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1052595844",
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
            "amount": "37531076017"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1052595"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMGQ3YjU1MS01NThhLTU2MjgtODMxZi03NTAwMGY0NzYwNTcifQ==",
    "nonce": 5487,
    "balances": {
      "current": "12980150487063153",
      "previous": "12980151540711592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d66fd65445e1e8aa9fe35728b747767602433b3",
    "nonce": 22,
    "balances": {
      "current": "1052595844",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:27.738Z",
  "updated": "2020-05-22T08:41:27.806Z",
  "id": "5ec79037005df800101bc965"
}
```
* *stageAmount*: `1052595844`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000000000000000000000000000000000003ebd56844eb1fd51e91ab8624d39625fe62570bc0d018039a889e4883da5a8fd9d2b9fafeca5365f618e553235e8078b961d2ee766deec2f1258b0b7f0fbfeb32722a1d36d382f71fba9938ebd38006fa5cc402824c184729d6be91f218c1d0cbdabff03000000000000000000000000000000000000000000000000000000000000001b436411bce110f772d3acb8de8908d0fb74662ec528d177e1e63c541c99cc568fd0d83079848917627c14c344de9e0de955c6f4fe2ff120370bb668b0a7043e4b1aa5e7f5fa46a3e4dfa565a4fff58f70d0d41a603815af6529e2e76053282625000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56680000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000156f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d60cae99a71000000000000000000000000000000000000000000000000002e1d6109b700a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000100fb3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd06c5b1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d475133596a55314d5330314e5468684c5455324d6a67744f444d785a6930334e5441774d4759304e7a59774e54636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002d66fd65445e1e8aa9fe35728b747767602433b3000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4eb1fd51e91ab8624d39625fe62570bc0d018039a889e4883da5a8fd9d2b9faf",
      "signature": {
        "s": "0x6d382f71fba9938ebd38006fa5cc402824c184729d6be91f218c1d0cbdabff03",
        "r": "0xeca5365f618e553235e8078b961d2ee766deec2f1258b0b7f0fbfeb32722a1d3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x436411bce110f772d3acb8de8908d0fb74662ec528d177e1e63c541c99cc568f",
      "signature": {
        "s": "0x1aa5e7f5fa46a3e4dfa565a4fff58f70d0d41a603815af6529e2e76053282625",
        "r": "0xd0d83079848917627c14c344de9e0de955c6f4fe2ff120370bb668b0a7043e4b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1052595844",
    "total": "1052595844"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1052595844",
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
            "amount": "37531076017"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1052595"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMGQ3YjU1MS01NThhLTU2MjgtODMxZi03NTAwMGY0NzYwNTcifQ==",
    "nonce": 5487,
    "balances": {
      "current": "12980150487063153",
      "previous": "12980151540711592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d66fd65445e1e8aa9fe35728b747767602433b3",
    "nonce": 22,
    "balances": {
      "current": "1052595844",
      "previous": "0"
    }
  },
  "blockNumber": "10114664",
  "created": "2020-05-22T08:41:27.738Z",
  "updated": "2020-05-22T08:41:27.806Z",
  "id": "5ec79037005df800101bc965"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000003ebd5684000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1052595844`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`