# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF372a0b130054525a384eF72A478c249eC3bDE99`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000352857ef00000000000000000000000000000000000000000000000000000000352857ef0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000352857ef00000000000000000000000000000000000000000000000000000000352857ef03de4a9b9589e22c8b7cbbecb71704065a659ad99a830853b90291fd3070b29104a3ff2a0b78bd5094add4657c920a7c023889754993adb0c3142ce8fd8f959dd70d5a482c58206fd139a968c6733f7ee0608d49bcaa42f148fd8184cd3c7a229000000000000000000000000000000000000000000000000000000000000001caa18060102bb421d72868fb8283255b3bc352a5c7e322a58acc04f4015c77473b71aeea30daae5d51ac2691976791165969657b4116df9b5f48a064936acc91f25aae0c80f5ee2d5dfdbd0ccbe3edb5f35a16e24871d9206ce4abd9879991086000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e2e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b06733cf276000000000000000000000000000000000000000000000000002e0b09c69c2d2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000d9bbc6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6e99ba26000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e7a46684f475534595331694e4759794c545579596a45744f5445324e5331694e444d324d5759775932517a4d57556966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f372a0b130054525a384ef72a478c249ec3bde990000000000000000000000000000000000000000000000000000000352857ef0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3de4a9b9589e22c8b7cbbecb71704065a659ad99a830853b90291fd3070b2910",
      "signature": {
        "s": "0x70d5a482c58206fd139a968c6733f7ee0608d49bcaa42f148fd8184cd3c7a229",
        "r": "0x4a3ff2a0b78bd5094add4657c920a7c023889754993adb0c3142ce8fd8f959dd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaa18060102bb421d72868fb8283255b3bc352a5c7e322a58acc04f4015c77473",
      "signature": {
        "s": "0x25aae0c80f5ee2d5dfdbd0ccbe3edb5f35a16e24871d9206ce4abd9879991086",
        "r": "0xb71aeea30daae5d51ac2691976791165969657b4116df9b5f48a064936acc91f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "14269382384",
    "total": "14269382384"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14269382384",
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
            "amount": "57690143270"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "14269382"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NzFhOGU4YS1iNGYyLTUyYjEtOTE2NS1iNDM2MWYwY2QzMWUifQ==",
    "nonce": 7726,
    "balances": {
      "current": "12959971259773558",
      "previous": "12959985543425324"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf372a0b130054525a384ef72a478c249ec3bde99",
    "nonce": 13,
    "balances": {
      "current": "14269382384",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:04.167Z",
  "updated": "2020-05-22T08:59:05.223Z",
  "id": "5ec79458b0c6090011d5b2ed"
}
```
* *stageAmount*: `14269382384`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000352857ef0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000352857ef00000000000000000000000000000000000000000000000000000000352857ef03de4a9b9589e22c8b7cbbecb71704065a659ad99a830853b90291fd3070b29104a3ff2a0b78bd5094add4657c920a7c023889754993adb0c3142ce8fd8f959dd70d5a482c58206fd139a968c6733f7ee0608d49bcaa42f148fd8184cd3c7a229000000000000000000000000000000000000000000000000000000000000001caa18060102bb421d72868fb8283255b3bc352a5c7e322a58acc04f4015c77473b71aeea30daae5d51ac2691976791165969657b4116df9b5f48a064936acc91f25aae0c80f5ee2d5dfdbd0ccbe3edb5f35a16e24871d9206ce4abd9879991086000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e2e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b06733cf276000000000000000000000000000000000000000000000000002e0b09c69c2d2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000d9bbc6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6e99ba26000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e7a46684f475534595331694e4759794c545579596a45744f5445324e5331694e444d324d5759775932517a4d57556966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000f372a0b130054525a384ef72a478c249ec3bde990000000000000000000000000000000000000000000000000000000352857ef0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3de4a9b9589e22c8b7cbbecb71704065a659ad99a830853b90291fd3070b2910",
      "signature": {
        "s": "0x70d5a482c58206fd139a968c6733f7ee0608d49bcaa42f148fd8184cd3c7a229",
        "r": "0x4a3ff2a0b78bd5094add4657c920a7c023889754993adb0c3142ce8fd8f959dd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaa18060102bb421d72868fb8283255b3bc352a5c7e322a58acc04f4015c77473",
      "signature": {
        "s": "0x25aae0c80f5ee2d5dfdbd0ccbe3edb5f35a16e24871d9206ce4abd9879991086",
        "r": "0xb71aeea30daae5d51ac2691976791165969657b4116df9b5f48a064936acc91f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "14269382384",
    "total": "14269382384"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14269382384",
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
            "amount": "57690143270"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "14269382"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NzFhOGU4YS1iNGYyLTUyYjEtOTE2NS1iNDM2MWYwY2QzMWUifQ==",
    "nonce": 7726,
    "balances": {
      "current": "12959971259773558",
      "previous": "12959985543425324"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf372a0b130054525a384ef72a478c249ec3bde99",
    "nonce": 13,
    "balances": {
      "current": "14269382384",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:04.167Z",
  "updated": "2020-05-22T08:59:05.223Z",
  "id": "5ec79458b0c6090011d5b2ed"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000352857ef0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14269382384`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`