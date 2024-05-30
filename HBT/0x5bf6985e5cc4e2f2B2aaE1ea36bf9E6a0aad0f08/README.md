# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5bf6985e5cc4e2f2B2aaE1ea36bf9E6a0aad0f08`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000000000000000000000000000000000533205fefe0606d801af3331925186d93f0f788528a7f16e0be5560ebf451298a093eae8d395e7c03a610b18eb7fe0b8b510f7b3cc8befe6fd937397c2b2350b4e7e8ee4936074ed209d7103ed8eb8cab86a01097fdbebd05de931c70155c68b2f62e3d5d3000000000000000000000000000000000000000000000000000000000000001ce8ba3277923d612791cd9ec759d46b9e155d329f783df2ed56c1132c849c502d54358d1bfb63396cf460513f6ccd40e7694aa251a0928a1cb58a545af2dda3f4761736b51554c138935458296dbe49539dc45d0dc3a86df26238bc6c63244767000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e20de00d96505000000000000000000000000000000000000000000000000002e2131482baf4600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000154c4b43000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007d897cbbf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d57526c5a6d46694e6930314d6a4e6d4c54557a4f545974596a4a685a693034596a63344e3245784f5467355a54596966513d3d000000000000000000000000000000000000000000000000000000000000001a0000000000000000000000005bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0606d801af3331925186d93f0f788528a7f16e0be5560ebf451298a093eae8d3",
      "signature": {
        "s": "0x6074ed209d7103ed8eb8cab86a01097fdbebd05de931c70155c68b2f62e3d5d3",
        "r": "0x95e7c03a610b18eb7fe0b8b510f7b3cc8befe6fd937397c2b2350b4e7e8ee493",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe8ba3277923d612791cd9ec759d46b9e155d329f783df2ed56c1132c849c502d",
      "signature": {
        "s": "0x761736b51554c138935458296dbe49539dc45d0dc3a86df26238bc6c63244767",
        "r": "0x54358d1bfb63396cf460513f6ccd40e7694aa251a0928a1cb58a545af2dda3f4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "357321539326",
    "total": "357321539326"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "357321539326",
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
            "amount": "33698597823"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "357321539"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWRlZmFiNi01MjNmLTUzOTYtYjJhZi04Yjc4N2ExOTg5ZTYifQ==",
    "nonce": 5373,
    "balances": {
      "current": "12983986797765893",
      "previous": "12984344476626758"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08",
    "nonce": 26,
    "balances": {
      "current": "357321539326",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:40.265Z",
  "updated": "2020-05-22T08:40:40.327Z",
  "id": "5ec79008005df800101bc93d"
}
```
* *stageAmount*: `357321539326`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000000000000000000000000000000000533205fefe0606d801af3331925186d93f0f788528a7f16e0be5560ebf451298a093eae8d395e7c03a610b18eb7fe0b8b510f7b3cc8befe6fd937397c2b2350b4e7e8ee4936074ed209d7103ed8eb8cab86a01097fdbebd05de931c70155c68b2f62e3d5d3000000000000000000000000000000000000000000000000000000000000001ce8ba3277923d612791cd9ec759d46b9e155d329f783df2ed56c1132c849c502d54358d1bfb63396cf460513f6ccd40e7694aa251a0928a1cb58a545af2dda3f4761736b51554c138935458296dbe49539dc45d0dc3a86df26238bc6c63244767000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5665000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e20de00d96505000000000000000000000000000000000000000000000000002e2131482baf4600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000154c4b43000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007d897cbbf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d57526c5a6d46694e6930314d6a4e6d4c54557a4f545974596a4a685a693034596a63344e3245784f5467355a54596966513d3d000000000000000000000000000000000000000000000000000000000000001a0000000000000000000000005bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0606d801af3331925186d93f0f788528a7f16e0be5560ebf451298a093eae8d3",
      "signature": {
        "s": "0x6074ed209d7103ed8eb8cab86a01097fdbebd05de931c70155c68b2f62e3d5d3",
        "r": "0x95e7c03a610b18eb7fe0b8b510f7b3cc8befe6fd937397c2b2350b4e7e8ee493",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe8ba3277923d612791cd9ec759d46b9e155d329f783df2ed56c1132c849c502d",
      "signature": {
        "s": "0x761736b51554c138935458296dbe49539dc45d0dc3a86df26238bc6c63244767",
        "r": "0x54358d1bfb63396cf460513f6ccd40e7694aa251a0928a1cb58a545af2dda3f4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "357321539326",
    "total": "357321539326"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "357321539326",
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
            "amount": "33698597823"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "357321539"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MWRlZmFiNi01MjNmLTUzOTYtYjJhZi04Yjc4N2ExOTg5ZTYifQ==",
    "nonce": 5373,
    "balances": {
      "current": "12983986797765893",
      "previous": "12984344476626758"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bf6985e5cc4e2f2b2aae1ea36bf9e6a0aad0f08",
    "nonce": 26,
    "balances": {
      "current": "357321539326",
      "previous": "0"
    }
  },
  "blockNumber": "10114661",
  "created": "2020-05-22T08:40:40.265Z",
  "updated": "2020-05-22T08:40:40.327Z",
  "id": "5ec79008005df800101bc93d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000533205fefe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `357321539326`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`