# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0476Da34411e3D1c254932C0B6B50492A072d770`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000110000000000000000000000000000000000000000000000000000000000000011000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000110000000000000000000000000000000000000000000000000000000000000011805d12d2f2e66a375aa0ec7a343267752f873dfd57b7bb3d7d8ac02df68539c4eaa914f60b86e87a7c3f3b84dd8ad42851c04bd13b0fa391b63d1841f47d4f8b4b245216fa02f50f5a9051d9feb05ecfaf58a497e71abbfcd36d00943aa67b2a000000000000000000000000000000000000000000000000000000000000001c2c341abeb14b3dbf50259620b475295bf3e3e50f91d3f5fef75b34b0a747e968bd2986f9c6e5aaada17fe78d0a14c143e2595fb1c7064375ed2fdb6f13fe03381a6ddf25dcf932f207b86c4c908cccad4d0721a1d9869a753a191271db806781000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015ae00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4eeed38d22000000000000000000000000000000000000000000000000002e1d4eeed38d3400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c1980e8b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a544d354e445130595330315a6a56694c54566c5a6d51744f5445314d5330794d474e6a4e6a51345a6a41784e57596966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000000476da34411e3d1c254932c0b6b50492a072d7700000000000000000000000000000000000000000000000000000000000000011000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x805d12d2f2e66a375aa0ec7a343267752f873dfd57b7bb3d7d8ac02df68539c4",
      "signature": {
        "s": "0x4b245216fa02f50f5a9051d9feb05ecfaf58a497e71abbfcd36d00943aa67b2a",
        "r": "0xeaa914f60b86e87a7c3f3b84dd8ad42851c04bd13b0fa391b63d1841f47d4f8b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2c341abeb14b3dbf50259620b475295bf3e3e50f91d3f5fef75b34b0a747e968",
      "signature": {
        "s": "0x1a6ddf25dcf932f207b86c4c908cccad4d0721a1d9869a753a191271db806781",
        "r": "0xbd2986f9c6e5aaada17fe78d0a14c143e2595fb1c7064375ed2fdb6f13fe0338",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "17",
    "total": "17"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17",
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
            "amount": "37607706251"
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
    "data": "eyJyZWYiOiJlZTM5NDQ0YS01ZjViLTVlZmQtOTE1MS0yMGNjNjQ4ZjAxNWYifQ==",
    "nonce": 5550,
    "balances": {
      "current": "12980073780186402",
      "previous": "12980073780186420"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0476da34411e3d1c254932c0b6b50492a072d770",
    "nonce": 21,
    "balances": {
      "current": "17",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:02.167Z",
  "updated": "2020-05-22T08:42:02.236Z",
  "id": "5ec7905ab0c6090011d5affe"
}
```
* *stageAmount*: `17`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000011000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000110000000000000000000000000000000000000000000000000000000000000011805d12d2f2e66a375aa0ec7a343267752f873dfd57b7bb3d7d8ac02df68539c4eaa914f60b86e87a7c3f3b84dd8ad42851c04bd13b0fa391b63d1841f47d4f8b4b245216fa02f50f5a9051d9feb05ecfaf58a497e71abbfcd36d00943aa67b2a000000000000000000000000000000000000000000000000000000000000001c2c341abeb14b3dbf50259620b475295bf3e3e50f91d3f5fef75b34b0a747e968bd2986f9c6e5aaada17fe78d0a14c143e2595fb1c7064375ed2fdb6f13fe03381a6ddf25dcf932f207b86c4c908cccad4d0721a1d9869a753a191271db806781000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a566a000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000015ae00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d4eeed38d22000000000000000000000000000000000000000000000000002e1d4eeed38d3400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008c1980e8b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a544d354e445130595330315a6a56694c54566c5a6d51744f5445314d5330794d474e6a4e6a51345a6a41784e57596966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000000476da34411e3d1c254932c0b6b50492a072d7700000000000000000000000000000000000000000000000000000000000000011000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x805d12d2f2e66a375aa0ec7a343267752f873dfd57b7bb3d7d8ac02df68539c4",
      "signature": {
        "s": "0x4b245216fa02f50f5a9051d9feb05ecfaf58a497e71abbfcd36d00943aa67b2a",
        "r": "0xeaa914f60b86e87a7c3f3b84dd8ad42851c04bd13b0fa391b63d1841f47d4f8b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2c341abeb14b3dbf50259620b475295bf3e3e50f91d3f5fef75b34b0a747e968",
      "signature": {
        "s": "0x1a6ddf25dcf932f207b86c4c908cccad4d0721a1d9869a753a191271db806781",
        "r": "0xbd2986f9c6e5aaada17fe78d0a14c143e2595fb1c7064375ed2fdb6f13fe0338",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "17",
    "total": "17"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17",
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
            "amount": "37607706251"
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
    "data": "eyJyZWYiOiJlZTM5NDQ0YS01ZjViLTVlZmQtOTE1MS0yMGNjNjQ4ZjAxNWYifQ==",
    "nonce": 5550,
    "balances": {
      "current": "12980073780186402",
      "previous": "12980073780186420"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0476da34411e3d1c254932c0b6b50492a072d770",
    "nonce": 21,
    "balances": {
      "current": "17",
      "previous": "0"
    }
  },
  "blockNumber": "10114666",
  "created": "2020-05-22T08:42:02.167Z",
  "updated": "2020-05-22T08:42:02.236Z",
  "id": "5ec7905ab0c6090011d5affe"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000011000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `17`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`