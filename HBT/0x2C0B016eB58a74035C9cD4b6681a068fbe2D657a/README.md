# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2C0B016eB58a74035C9cD4b6681a068fbe2D657a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000196a359500000000000000000000000000000000000000000000000000000000196a3595000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000196a359500000000000000000000000000000000000000000000000000000000196a3595085bf05a5c3b2721dfd125bd7a9437adcf1ea9579de846bcb034fda4e293bcbf59de2c8a64441058ef3a7659e8d6d042920beef528200e4d3d71775d93ddbe17229d0219524f2d0022b90d7708f72ffaa6788f334ee7caa6fbb7b12cac433912000000000000000000000000000000000000000000000000000000000000001bc8fc61b47fe83fd70252b731bf77e1af53817a782ba20b556a158e78feb93a44da8211d651b35e4ab4ff848e37a47b60743642726444d55211e8e001441abf494f5aff594312be899bc31d50152ee3f24aa7e0b009b345a8246dee92af106605000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a1eb307396000000000000000000000000000000000000000000000000002e15a204a12ac100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000068196000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8229176000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d544d774d7a67324d5330775a6a4e684c54566c4e5455744f54566c4d5330355a57466c596a41334d7a41345a544d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002c0b016eb58a74035c9cd4b6681a068fbe2d657a00000000000000000000000000000000000000000000000000000000196a3595000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x085bf05a5c3b2721dfd125bd7a9437adcf1ea9579de846bcb034fda4e293bcbf",
      "signature": {
        "s": "0x229d0219524f2d0022b90d7708f72ffaa6788f334ee7caa6fbb7b12cac433912",
        "r": "0x59de2c8a64441058ef3a7659e8d6d042920beef528200e4d3d71775d93ddbe17",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc8fc61b47fe83fd70252b731bf77e1af53817a782ba20b556a158e78feb93a44",
      "signature": {
        "s": "0x4f5aff594312be899bc31d50152ee3f24aa7e0b009b345a8246dee92af106605",
        "r": "0xda8211d651b35e4ab4ff848e37a47b60743642726444d55211e8e001441abf49",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "426390933",
    "total": "426390933"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "426390933",
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
            "amount": "46038946166"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "426390"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMTMwMzg2MS0wZjNhLTVlNTUtOTVlMS05ZWFlYjA3MzA4ZTMifQ==",
    "nonce": 6984,
    "balances": {
      "current": "12971634108429206",
      "previous": "12971634535246529"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c0b016eb58a74035c9cd4b6681a068fbe2d657a",
    "nonce": 22,
    "balances": {
      "current": "426390933",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:12.298Z",
  "updated": "2020-05-22T08:53:12.368Z",
  "id": "5ec792f8e5756b00111b8855"
}
```
* *stageAmount*: `426390933`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000196a3595000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000196a359500000000000000000000000000000000000000000000000000000000196a3595085bf05a5c3b2721dfd125bd7a9437adcf1ea9579de846bcb034fda4e293bcbf59de2c8a64441058ef3a7659e8d6d042920beef528200e4d3d71775d93ddbe17229d0219524f2d0022b90d7708f72ffaa6788f334ee7caa6fbb7b12cac433912000000000000000000000000000000000000000000000000000000000000001bc8fc61b47fe83fd70252b731bf77e1af53817a782ba20b556a158e78feb93a44da8211d651b35e4ab4ff848e37a47b60743642726444d55211e8e001441abf494f5aff594312be899bc31d50152ee3f24aa7e0b009b345a8246dee92af106605000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b4800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15a1eb307396000000000000000000000000000000000000000000000000002e15a204a12ac100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000068196000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab8229176000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d544d774d7a67324d5330775a6a4e684c54566c4e5455744f54566c4d5330355a57466c596a41334d7a41345a544d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002c0b016eb58a74035c9cd4b6681a068fbe2d657a00000000000000000000000000000000000000000000000000000000196a3595000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x085bf05a5c3b2721dfd125bd7a9437adcf1ea9579de846bcb034fda4e293bcbf",
      "signature": {
        "s": "0x229d0219524f2d0022b90d7708f72ffaa6788f334ee7caa6fbb7b12cac433912",
        "r": "0x59de2c8a64441058ef3a7659e8d6d042920beef528200e4d3d71775d93ddbe17",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc8fc61b47fe83fd70252b731bf77e1af53817a782ba20b556a158e78feb93a44",
      "signature": {
        "s": "0x4f5aff594312be899bc31d50152ee3f24aa7e0b009b345a8246dee92af106605",
        "r": "0xda8211d651b35e4ab4ff848e37a47b60743642726444d55211e8e001441abf49",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "426390933",
    "total": "426390933"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "426390933",
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
            "amount": "46038946166"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "426390"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMTMwMzg2MS0wZjNhLTVlNTUtOTVlMS05ZWFlYjA3MzA4ZTMifQ==",
    "nonce": 6984,
    "balances": {
      "current": "12971634108429206",
      "previous": "12971634535246529"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2c0b016eb58a74035c9cd4b6681a068fbe2d657a",
    "nonce": 22,
    "balances": {
      "current": "426390933",
      "previous": "0"
    }
  },
  "blockNumber": "10114724",
  "created": "2020-05-22T08:53:12.298Z",
  "updated": "2020-05-22T08:53:12.368Z",
  "id": "5ec792f8e5756b00111b8855"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000196a3595000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `426390933`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`