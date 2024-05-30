# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x98d67bc5bA8e43721972204e5e1e4EAEf43CADb1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000a58d1e3f00000000000000000000000000000000000000000000000000000000a58d1e3f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a58d1e3f00000000000000000000000000000000000000000000000000000000a58d1e3fcae1966514531fde8d7c0bb9da868f2c5d6a9637d0d50fbcf5fb7d0e760f46afeae99facb6366e049769b1a6d0759858250d023db62b0148917faf85727f695c16a26969bebc29e08dc5d90a4be1adf59f4eea6fb8c61db5eb2abb36275f1a0d000000000000000000000000000000000000000000000000000000000000001c4c9015da31d29f333c9d32ef56673c90aa005043cf7db492b869737cb75fe5b0c08dbaddf840386b750a268bcb534994536476831c7b1eae7720bf004398d1ac575d3b3699591df6d2bbea4beb30b4b2c5617416551ce260d6985862e35e56de000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b1e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15bed80834c5000000000000000000000000000000000000000000000000002e15bf7dbfb49400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002a6190000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab0bcd28f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d4d304e4751774d5330354d6d59794c54566c4d7a4d744f474d785979316c595451795a6d55305a6d51794d44516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000098d67bc5ba8e43721972204e5e1e4eaef43cadb100000000000000000000000000000000000000000000000000000000a58d1e3f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcae1966514531fde8d7c0bb9da868f2c5d6a9637d0d50fbcf5fb7d0e760f46af",
      "signature": {
        "s": "0x16a26969bebc29e08dc5d90a4be1adf59f4eea6fb8c61db5eb2abb36275f1a0d",
        "r": "0xeae99facb6366e049769b1a6d0759858250d023db62b0148917faf85727f695c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c9015da31d29f333c9d32ef56673c90aa005043cf7db492b869737cb75fe5b0",
      "signature": {
        "s": "0x575d3b3699591df6d2bbea4beb30b4b2c5617416551ce260d6985862e35e56de",
        "r": "0xc08dbaddf840386b750a268bcb534994536476831c7b1eae7720bf004398d1ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2777488959",
    "total": "2777488959"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2777488959",
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
            "amount": "45914837647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2777488"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZmM0NGQwMS05MmYyLTVlMzMtOGMxYy1lYTQyZmU0ZmQyMDQifQ==",
    "nonce": 6942,
    "balances": {
      "current": "12971758341076165",
      "previous": "12971761121342612"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98d67bc5ba8e43721972204e5e1e4eaef43cadb1",
    "nonce": 22,
    "balances": {
      "current": "2777488959",
      "previous": "0"
    }
  },
  "blockNumber": "10114722",
  "created": "2020-05-22T08:52:54.705Z",
  "updated": "2020-05-22T08:52:54.772Z",
  "id": "5ec792e6b0c6090011d5b1dd"
}
```
* *stageAmount*: `2777488959`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000a58d1e3f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a58d1e3f00000000000000000000000000000000000000000000000000000000a58d1e3fcae1966514531fde8d7c0bb9da868f2c5d6a9637d0d50fbcf5fb7d0e760f46afeae99facb6366e049769b1a6d0759858250d023db62b0148917faf85727f695c16a26969bebc29e08dc5d90a4be1adf59f4eea6fb8c61db5eb2abb36275f1a0d000000000000000000000000000000000000000000000000000000000000001c4c9015da31d29f333c9d32ef56673c90aa005043cf7db492b869737cb75fe5b0c08dbaddf840386b750a268bcb534994536476831c7b1eae7720bf004398d1ac575d3b3699591df6d2bbea4beb30b4b2c5617416551ce260d6985862e35e56de000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56a200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001b1e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15bed80834c5000000000000000000000000000000000000000000000000002e15bf7dbfb49400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002a6190000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ab0bcd28f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d4d304e4751774d5330354d6d59794c54566c4d7a4d744f474d785979316c595451795a6d55305a6d51794d44516966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000098d67bc5ba8e43721972204e5e1e4eaef43cadb100000000000000000000000000000000000000000000000000000000a58d1e3f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcae1966514531fde8d7c0bb9da868f2c5d6a9637d0d50fbcf5fb7d0e760f46af",
      "signature": {
        "s": "0x16a26969bebc29e08dc5d90a4be1adf59f4eea6fb8c61db5eb2abb36275f1a0d",
        "r": "0xeae99facb6366e049769b1a6d0759858250d023db62b0148917faf85727f695c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4c9015da31d29f333c9d32ef56673c90aa005043cf7db492b869737cb75fe5b0",
      "signature": {
        "s": "0x575d3b3699591df6d2bbea4beb30b4b2c5617416551ce260d6985862e35e56de",
        "r": "0xc08dbaddf840386b750a268bcb534994536476831c7b1eae7720bf004398d1ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2777488959",
    "total": "2777488959"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2777488959",
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
            "amount": "45914837647"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2777488"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlZmM0NGQwMS05MmYyLTVlMzMtOGMxYy1lYTQyZmU0ZmQyMDQifQ==",
    "nonce": 6942,
    "balances": {
      "current": "12971758341076165",
      "previous": "12971761121342612"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98d67bc5ba8e43721972204e5e1e4eaef43cadb1",
    "nonce": 22,
    "balances": {
      "current": "2777488959",
      "previous": "0"
    }
  },
  "blockNumber": "10114722",
  "created": "2020-05-22T08:52:54.705Z",
  "updated": "2020-05-22T08:52:54.772Z",
  "id": "5ec792e6b0c6090011d5b1dd"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000a58d1e3f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2777488959`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`