# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000ee60000000000000000000000000000000000000000000000000000000000000ee600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000ee60000000000000000000000000000000000000000000000000000000000000ee60cea9bc4153e0a5b5265bcc7cd5070d3745043a1f184c63355fb660fa807ccfec742896479bbf4fbc638820f996e81e5a794a34bb385c3a9e1a54f3d29cfced0d3c5d258fa56a3cf522e9f189784c78fd1cda68a6e951cd1522eca31988575889000000000000000000000000000000000000000000000000000000000000001b7bb026f879f471924806219bbdb1e72f6bd342bbf64d244ccf35475fcd1455a49887ccb308d558cf2bd8d2f0395c7b269fd2e40d8767ba88b770cf763fe6c9c44830589c9fb4c064c86c5e2813ee7ad29118e99c1844c004f18e9e182f95ca1e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cdd9e9e2000000000000000000000000000000000000000000000000002386f2cddad87f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b5e100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d4445344e7a49324d53316d4e7a466c4c5455774e4455744f57466a4e693078596a4668595749324e44517a597a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000ee60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcea9bc4153e0a5b5265bcc7cd5070d3745043a1f184c63355fb660fa807ccfec",
      "signature": {
        "s": "0x3c5d258fa56a3cf522e9f189784c78fd1cda68a6e951cd1522eca31988575889",
        "r": "0x742896479bbf4fbc638820f996e81e5a794a34bb385c3a9e1a54f3d29cfced0d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7bb026f879f471924806219bbdb1e72f6bd342bbf64d244ccf35475fcd1455a4",
      "signature": {
        "s": "0x4830589c9fb4c064c86c5e2813ee7ad29118e99c1844c004f18e9e182f95ca1e",
        "r": "0x9887ccb308d558cf2bd8d2f0395c7b269fd2e40d8767ba88b770cf763fe6c9c4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "61024",
    "total": "61024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61024",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "505313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "61"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDE4NzI2MS1mNzFlLTUwNDUtOWFjNi0xYjFhYWI2NDQzYzIifQ==",
    "nonce": 242,
    "balances": {
      "current": "10000001578691042",
      "previous": "10000001578752127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "nonce": 20,
    "balances": {
      "current": "61024",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:35.851Z",
  "updated": "2020-05-22T08:00:35.923Z",
  "id": "5ec786a3e5756b00111b7fc0"
}
```
* *stageAmount*: `61024`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000ee600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000ee60000000000000000000000000000000000000000000000000000000000000ee60cea9bc4153e0a5b5265bcc7cd5070d3745043a1f184c63355fb660fa807ccfec742896479bbf4fbc638820f996e81e5a794a34bb385c3a9e1a54f3d29cfced0d3c5d258fa56a3cf522e9f189784c78fd1cda68a6e951cd1522eca31988575889000000000000000000000000000000000000000000000000000000000000001b7bb026f879f471924806219bbdb1e72f6bd342bbf64d244ccf35475fcd1455a49887ccb308d558cf2bd8d2f0395c7b269fd2e40d8767ba88b770cf763fe6c9c44830589c9fb4c064c86c5e2813ee7ad29118e99c1844c004f18e9e182f95ca1e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cdd9e9e2000000000000000000000000000000000000000000000000002386f2cddad87f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b5e100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d4445344e7a49324d53316d4e7a466c4c5455774e4455744f57466a4e693078596a4668595749324e44517a597a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000ee60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcea9bc4153e0a5b5265bcc7cd5070d3745043a1f184c63355fb660fa807ccfec",
      "signature": {
        "s": "0x3c5d258fa56a3cf522e9f189784c78fd1cda68a6e951cd1522eca31988575889",
        "r": "0x742896479bbf4fbc638820f996e81e5a794a34bb385c3a9e1a54f3d29cfced0d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7bb026f879f471924806219bbdb1e72f6bd342bbf64d244ccf35475fcd1455a4",
      "signature": {
        "s": "0x4830589c9fb4c064c86c5e2813ee7ad29118e99c1844c004f18e9e182f95ca1e",
        "r": "0x9887ccb308d558cf2bd8d2f0395c7b269fd2e40d8767ba88b770cf763fe6c9c4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "61024",
    "total": "61024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61024",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "505313"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "61"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDE4NzI2MS1mNzFlLTUwNDUtOWFjNi0xYjFhYWI2NDQzYzIifQ==",
    "nonce": 242,
    "balances": {
      "current": "10000001578691042",
      "previous": "10000001578752127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "nonce": 20,
    "balances": {
      "current": "61024",
      "previous": "0"
    }
  },
  "blockNumber": "10114493",
  "created": "2020-05-22T08:00:35.851Z",
  "updated": "2020-05-22T08:00:35.923Z",
  "id": "5ec786a3e5756b00111b7fc0"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000000000ee600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `61024`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``