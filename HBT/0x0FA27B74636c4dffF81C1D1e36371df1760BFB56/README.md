# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0FA27B74636c4dffF81C1D1e36371df1760BFB56`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000e23bb6fd00000000000000000000000000000000000000000000000000000000e23bb6fd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000e23bb6fd00000000000000000000000000000000000000000000000000000000e23bb6fd055e0b1e68740073f4ee769f7c2d5147414a89fb9acce947b45768a0de4944c05f20020781b8ab28e2633c1b388f70e851cf4787554e91fac2f17a9af016f379b4ab98a94165d128c329b7eb03f60f7cf7582b07a4aa250856aa8c36d7226fbee000000000000000000000000000000000000000000000000000000000000001ba13902de3b570b51d284ea7f35d9def6acf5365fd5beb1bf61561f1baa7685843a07db14b7707b112f3edec36e8331697acfe3a0155efcb5c362e07030e2489f43955daf8396e4bffd211fd583edb33c27d3eed78c94af7a1c79d2462813c004000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a98c054f578000000000000000000000000000000000000000000000000002e1aa6e7af0c0c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000039ea6c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000973207d75000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e6d4a6a4d57517a596930315a6a49354c5455304f5755744f5751314e43316c4d6a59335a54646c4e5755784f54596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000fa27b74636c4dfff81c1d1e36371df1760bfb560000000000000000000000000000000000000000000000000000000e23bb6fd0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55e0b1e68740073f4ee769f7c2d5147414a89fb9acce947b45768a0de4944c05",
      "signature": {
        "s": "0x4ab98a94165d128c329b7eb03f60f7cf7582b07a4aa250856aa8c36d7226fbee",
        "r": "0xf20020781b8ab28e2633c1b388f70e851cf4787554e91fac2f17a9af016f379b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa13902de3b570b51d284ea7f35d9def6acf5365fd5beb1bf61561f1baa768584",
      "signature": {
        "s": "0x43955daf8396e4bffd211fd583edb33c27d3eed78c94af7a1c79d2462813c004",
        "r": "0x3a07db14b7707b112f3edec36e8331697acfe3a0155efcb5c362e07030e2489f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "60729028560",
    "total": "60729028560"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "60729028560",
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
            "amount": "40586214773"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "60729028"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNmJjMWQzYi01ZjI5LTU0OWUtOWQ1NC1lMjY3ZTdlNWUxOTYifQ==",
    "nonce": 6299,
    "balances": {
      "current": "12977092292834680",
      "previous": "12977153082592268"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fa27b74636c4dfff81c1d1e36371df1760bfb56",
    "nonce": 22,
    "balances": {
      "current": "60729028560",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:47:57.921Z",
  "updated": "2020-05-22T08:47:57.989Z",
  "id": "5ec791bd005df800101bca6d"
}
```
* *stageAmount*: `60729028560`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000e23bb6fd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000e23bb6fd00000000000000000000000000000000000000000000000000000000e23bb6fd055e0b1e68740073f4ee769f7c2d5147414a89fb9acce947b45768a0de4944c05f20020781b8ab28e2633c1b388f70e851cf4787554e91fac2f17a9af016f379b4ab98a94165d128c329b7eb03f60f7cf7582b07a4aa250856aa8c36d7226fbee000000000000000000000000000000000000000000000000000000000000001ba13902de3b570b51d284ea7f35d9def6acf5365fd5beb1bf61561f1baa7685843a07db14b7707b112f3edec36e8331697acfe3a0155efcb5c362e07030e2489f43955daf8396e4bffd211fd583edb33c27d3eed78c94af7a1c79d2462813c004000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a568b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a98c054f578000000000000000000000000000000000000000000000000002e1aa6e7af0c0c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000039ea6c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000973207d75000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784e6d4a6a4d57517a596930315a6a49354c5455304f5755744f5751314e43316c4d6a59335a54646c4e5755784f54596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000fa27b74636c4dfff81c1d1e36371df1760bfb560000000000000000000000000000000000000000000000000000000e23bb6fd0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x55e0b1e68740073f4ee769f7c2d5147414a89fb9acce947b45768a0de4944c05",
      "signature": {
        "s": "0x4ab98a94165d128c329b7eb03f60f7cf7582b07a4aa250856aa8c36d7226fbee",
        "r": "0xf20020781b8ab28e2633c1b388f70e851cf4787554e91fac2f17a9af016f379b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa13902de3b570b51d284ea7f35d9def6acf5365fd5beb1bf61561f1baa768584",
      "signature": {
        "s": "0x43955daf8396e4bffd211fd583edb33c27d3eed78c94af7a1c79d2462813c004",
        "r": "0x3a07db14b7707b112f3edec36e8331697acfe3a0155efcb5c362e07030e2489f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "60729028560",
    "total": "60729028560"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "60729028560",
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
            "amount": "40586214773"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "60729028"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxNmJjMWQzYi01ZjI5LTU0OWUtOWQ1NC1lMjY3ZTdlNWUxOTYifQ==",
    "nonce": 6299,
    "balances": {
      "current": "12977092292834680",
      "previous": "12977153082592268"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0fa27b74636c4dfff81c1d1e36371df1760bfb56",
    "nonce": 22,
    "balances": {
      "current": "60729028560",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:47:57.921Z",
  "updated": "2020-05-22T08:47:57.989Z",
  "id": "5ec791bd005df800101bca6d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000e23bb6fd0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `60729028560`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`