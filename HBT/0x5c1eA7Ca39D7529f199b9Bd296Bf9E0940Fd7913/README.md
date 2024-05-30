# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5c1eA7Ca39D7529f199b9Bd296Bf9E0940Fd7913`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000b5ca04fe00000000000000000000000000000000000000000000000000000000b5ca04fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000b5ca04fe00000000000000000000000000000000000000000000000000000000b5ca04fef17af1c5071fc374c4c8843fb7842dbc937b1b19ee4eaa10161374d331577293d9ec7c20a3df3142697265067a397716e92054470f8ef96034fbbb263020aa0822ac1f389be33e1b01e5259d4f6fd490184950d96e3f9fac87170347aaf9e76a000000000000000000000000000000000000000000000000000000000000001b62da58b4d7476d494e539a5154816d7de9876e3ac05a6354581792456d2f218bda1c8108dcf26f90141ba2ee656839c1da318de7f7ae690a2e9dab5d1cc1d83221c1309d66a0ea01502317ec4bc2816b4706389e1452f58a51e2a7c797d750c0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a565e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000144c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e3ee9a931ed1a000000000000000000000000000000000000000000000000002e3eea5f2a7bd300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002e89bb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000297ee6d5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5445354d3245794e7930324e6a4a6b4c5455315a5463744f54686c5a69303159544d334d5756694d6a517a4f44456966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000005c1ea7ca39d7529f199b9bd296bf9e0940fd791300000000000000000000000000000000000000000000000000000000b5ca04fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf17af1c5071fc374c4c8843fb7842dbc937b1b19ee4eaa10161374d331577293",
      "signature": {
        "s": "0x22ac1f389be33e1b01e5259d4f6fd490184950d96e3f9fac87170347aaf9e76a",
        "r": "0xd9ec7c20a3df3142697265067a397716e92054470f8ef96034fbbb263020aa08",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x62da58b4d7476d494e539a5154816d7de9876e3ac05a6354581792456d2f218b",
      "signature": {
        "s": "0x21c1309d66a0ea01502317ec4bc2816b4706389e1452f58a51e2a7c797d750c0",
        "r": "0xda1c8108dcf26f90141ba2ee656839c1da318de7f7ae690a2e9dab5d1cc1d832",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3049915646",
    "total": "3049915646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3049915646",
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
            "amount": "696182485"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3049915"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTE5M2EyNy02NjJkLTU1ZTctOThlZi01YTM3MWViMjQzODEifQ==",
    "nonce": 5196,
    "balances": {
      "current": "13017022215613722",
      "previous": "13017025268579283"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c1ea7ca39d7529f199b9bd296bf9e0940fd7913",
    "nonce": 16,
    "balances": {
      "current": "3049915646",
      "previous": "0"
    }
  },
  "blockNumber": "10114654",
  "created": "2020-05-22T08:39:17.651Z",
  "updated": "2020-05-22T08:39:17.834Z",
  "id": "5ec78fb5e5756b00111b861c"
}
```
* *stageAmount*: `3049915646`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000b5ca04fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000b5ca04fe00000000000000000000000000000000000000000000000000000000b5ca04fef17af1c5071fc374c4c8843fb7842dbc937b1b19ee4eaa10161374d331577293d9ec7c20a3df3142697265067a397716e92054470f8ef96034fbbb263020aa0822ac1f389be33e1b01e5259d4f6fd490184950d96e3f9fac87170347aaf9e76a000000000000000000000000000000000000000000000000000000000000001b62da58b4d7476d494e539a5154816d7de9876e3ac05a6354581792456d2f218bda1c8108dcf26f90141ba2ee656839c1da318de7f7ae690a2e9dab5d1cc1d83221c1309d66a0ea01502317ec4bc2816b4706389e1452f58a51e2a7c797d750c0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a565e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000144c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e3ee9a931ed1a000000000000000000000000000000000000000000000000002e3eea5f2a7bd300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002e89bb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000297ee6d5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949315a5445354d3245794e7930324e6a4a6b4c5455315a5463744f54686c5a69303159544d334d5756694d6a517a4f44456966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000005c1ea7ca39d7529f199b9bd296bf9e0940fd791300000000000000000000000000000000000000000000000000000000b5ca04fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf17af1c5071fc374c4c8843fb7842dbc937b1b19ee4eaa10161374d331577293",
      "signature": {
        "s": "0x22ac1f389be33e1b01e5259d4f6fd490184950d96e3f9fac87170347aaf9e76a",
        "r": "0xd9ec7c20a3df3142697265067a397716e92054470f8ef96034fbbb263020aa08",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x62da58b4d7476d494e539a5154816d7de9876e3ac05a6354581792456d2f218b",
      "signature": {
        "s": "0x21c1309d66a0ea01502317ec4bc2816b4706389e1452f58a51e2a7c797d750c0",
        "r": "0xda1c8108dcf26f90141ba2ee656839c1da318de7f7ae690a2e9dab5d1cc1d832",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3049915646",
    "total": "3049915646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3049915646",
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
            "amount": "696182485"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3049915"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1ZTE5M2EyNy02NjJkLTU1ZTctOThlZi01YTM3MWViMjQzODEifQ==",
    "nonce": 5196,
    "balances": {
      "current": "13017022215613722",
      "previous": "13017025268579283"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c1ea7ca39d7529f199b9bd296bf9e0940fd7913",
    "nonce": 16,
    "balances": {
      "current": "3049915646",
      "previous": "0"
    }
  },
  "blockNumber": "10114654",
  "created": "2020-05-22T08:39:17.651Z",
  "updated": "2020-05-22T08:39:17.834Z",
  "id": "5ec78fb5e5756b00111b861c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000b5ca04fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3049915646`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`