# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x93845A63D42960304F4BDb0318Db27c58EaD5ba4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000000000000000000000000000000000000ce435f75be1f7ba87936427a68d102ad5bee084a9a96cc2c4714635841a3ea6e493226d9503fd6c6d2984ece44ce9a45b9a6d2f43a38bcb0397247d38bd6cad62ba5eb00d96a5739e946d91bbdbf87b86e5c564ce0eac7eb352abc5d1e2adae90734e04000000000000000000000000000000000000000000000000000000000000001c99fc75ff707240646ee6ba4d2e8f30655ff35f4c04c7129e315882f15953580ebef2a35e0e2737ebbd0386c22a609e77be41de5dee0656f3a190aa7f4aad61ba73edd69935407cfd0a9db061574cbc97db00929570f1eb43f9eb5f66971d8b6f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000183200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1adb65cb0a39000000000000000000000000000000000000000000000000002e1adb72b28d0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000034cda000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000962151eb9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d4e6a4f5445325a6930785a5449784c5456694d6a4d745954597a5a5331694d325a6b4e7a45334e6a517a5a57556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000093845a63d42960304f4bdb0318db27c58ead5ba4000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5be1f7ba87936427a68d102ad5bee084a9a96cc2c4714635841a3ea6e493226d",
      "signature": {
        "s": "0x0d96a5739e946d91bbdbf87b86e5c564ce0eac7eb352abc5d1e2adae90734e04",
        "r": "0x9503fd6c6d2984ece44ce9a45b9a6d2f43a38bcb0397247d38bd6cad62ba5eb0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x99fc75ff707240646ee6ba4d2e8f30655ff35f4c04c7129e315882f15953580e",
      "signature": {
        "s": "0x73edd69935407cfd0a9db061574cbc97db00929570f1eb43f9eb5f66971d8b6f",
        "r": "0xbef2a35e0e2737ebbd0386c22a609e77be41de5dee0656f3a190aa7f4aad61ba",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "216282615",
    "total": "216282615"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "216282615",
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
            "amount": "40300256953"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "216282"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmNjOTE2Zi0xZTIxLTViMjMtYTYzZS1iM2ZkNzE3NjQzZWUifQ==",
    "nonce": 6194,
    "balances": {
      "current": "12977378536655417",
      "previous": "12977378753154314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x93845a63d42960304f4bdb0318db27c58ead5ba4",
    "nonce": 22,
    "balances": {
      "current": "216282615",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:15.053Z",
  "updated": "2020-05-22T08:47:15.117Z",
  "id": "5ec79193b0c6090011d5b0d9"
}
```
* *stageAmount*: `216282615`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000000000000000000000000000000000000ce435f75be1f7ba87936427a68d102ad5bee084a9a96cc2c4714635841a3ea6e493226d9503fd6c6d2984ece44ce9a45b9a6d2f43a38bcb0397247d38bd6cad62ba5eb00d96a5739e946d91bbdbf87b86e5c564ce0eac7eb352abc5d1e2adae90734e04000000000000000000000000000000000000000000000000000000000000001c99fc75ff707240646ee6ba4d2e8f30655ff35f4c04c7129e315882f15953580ebef2a35e0e2737ebbd0386c22a609e77be41de5dee0656f3a190aa7f4aad61ba73edd69935407cfd0a9db061574cbc97db00929570f1eb43f9eb5f66971d8b6f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56850000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000183200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1adb65cb0a39000000000000000000000000000000000000000000000000002e1adb72b28d0a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000034cda000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000962151eb9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d6d4e6a4f5445325a6930785a5449784c5456694d6a4d745954597a5a5331694d325a6b4e7a45334e6a517a5a57556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000093845a63d42960304f4bdb0318db27c58ead5ba4000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5be1f7ba87936427a68d102ad5bee084a9a96cc2c4714635841a3ea6e493226d",
      "signature": {
        "s": "0x0d96a5739e946d91bbdbf87b86e5c564ce0eac7eb352abc5d1e2adae90734e04",
        "r": "0x9503fd6c6d2984ece44ce9a45b9a6d2f43a38bcb0397247d38bd6cad62ba5eb0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x99fc75ff707240646ee6ba4d2e8f30655ff35f4c04c7129e315882f15953580e",
      "signature": {
        "s": "0x73edd69935407cfd0a9db061574cbc97db00929570f1eb43f9eb5f66971d8b6f",
        "r": "0xbef2a35e0e2737ebbd0386c22a609e77be41de5dee0656f3a190aa7f4aad61ba",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "216282615",
    "total": "216282615"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "216282615",
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
            "amount": "40300256953"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "216282"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MmNjOTE2Zi0xZTIxLTViMjMtYTYzZS1iM2ZkNzE3NjQzZWUifQ==",
    "nonce": 6194,
    "balances": {
      "current": "12977378536655417",
      "previous": "12977378753154314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x93845a63d42960304f4bdb0318db27c58ead5ba4",
    "nonce": 22,
    "balances": {
      "current": "216282615",
      "previous": "0"
    }
  },
  "blockNumber": "10114693",
  "created": "2020-05-22T08:47:15.053Z",
  "updated": "2020-05-22T08:47:15.117Z",
  "id": "5ec79193b0c6090011d5b0d9"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000ce435f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `216282615`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`