# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8d02EB339eBaEdFc6c058066cB30Fc9D20aDf14A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000cc90400000000000000000000000000000000000000000000000000000000000cc904000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000cc90400000000000000000000000000000000000000000000000000000000000cc904ba3e1042bd221f69fe58fd18bbf14db5f7ef34dc8688ee1a9ffa4f7db577020f2a9e34f0c10f67fb5ee397907b624c48257b9fa0417a96706817603a90b2d92e2bdd2c1be513987934ce46f35ec82f4122a53f787c3795dd3a77873fe6bcc377000000000000000000000000000000000000000000000000000000000000001c64f9c1e1d047d30f7b8268a96dff40b9508482c864ba49441f2f811c0e1c2524783417a07e527123330f4a1e21b99f1f14829cd017a760b2899b2eb0f0ee18360699128cb9c728d01da6c26bca3c47c8c01ec56a82f8ea42857bf4f0de4a7519000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56690000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000157c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d600e397ddf000000000000000000000000000000000000000000000000002e1d600e464a2800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000345000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd37072c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e5452694e6a5a694d4330344d6a4a6b4c5456694f5467744f5451304e433169597a45304e7a45314d474e694f57496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008d02eb339ebaedfc6c058066cb30fc9d20adf14a00000000000000000000000000000000000000000000000000000000000cc904000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba3e1042bd221f69fe58fd18bbf14db5f7ef34dc8688ee1a9ffa4f7db577020f",
      "signature": {
        "s": "0x2bdd2c1be513987934ce46f35ec82f4122a53f787c3795dd3a77873fe6bcc377",
        "r": "0x2a9e34f0c10f67fb5ee397907b624c48257b9fa0417a96706817603a90b2d92e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x64f9c1e1d047d30f7b8268a96dff40b9508482c864ba49441f2f811c0e1c2524",
      "signature": {
        "s": "0x0699128cb9c728d01da6c26bca3c47c8c01ec56a82f8ea42857bf4f0de4a7519",
        "r": "0x783417a07e527123330f4a1e21b99f1f14829cd017a760b2899b2eb0f0ee1836",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "837892",
    "total": "837892"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "837892",
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
            "amount": "37534238508"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NTRiNjZiMC04MjJkLTViOTgtOTQ0NC1iYzE0NzE1MGNiOWIifQ==",
    "nonce": 5500,
    "balances": {
      "current": "12980147321404895",
      "previous": "12980147322243624"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d02eb339ebaedfc6c058066cb30fc9d20adf14a",
    "nonce": 22,
    "balances": {
      "current": "837892",
      "previous": "0"
    }
  },
  "blockNumber": "10114665",
  "created": "2020-05-22T08:41:36.098Z",
  "updated": "2020-05-22T08:41:36.276Z",
  "id": "5ec79040e5756b00111b8679"
}
```
* *stageAmount*: `837892`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000cc904000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000cc90400000000000000000000000000000000000000000000000000000000000cc904ba3e1042bd221f69fe58fd18bbf14db5f7ef34dc8688ee1a9ffa4f7db577020f2a9e34f0c10f67fb5ee397907b624c48257b9fa0417a96706817603a90b2d92e2bdd2c1be513987934ce46f35ec82f4122a53f787c3795dd3a77873fe6bcc377000000000000000000000000000000000000000000000000000000000000001c64f9c1e1d047d30f7b8268a96dff40b9508482c864ba49441f2f811c0e1c2524783417a07e527123330f4a1e21b99f1f14829cd017a760b2899b2eb0f0ee18360699128cb9c728d01da6c26bca3c47c8c01ec56a82f8ea42857bf4f0de4a7519000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56690000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000157c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d600e397ddf000000000000000000000000000000000000000000000000002e1d600e464a2800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000345000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bd37072c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e5452694e6a5a694d4330344d6a4a6b4c5456694f5467744f5451304e433169597a45304e7a45314d474e694f57496966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008d02eb339ebaedfc6c058066cb30fc9d20adf14a00000000000000000000000000000000000000000000000000000000000cc904000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba3e1042bd221f69fe58fd18bbf14db5f7ef34dc8688ee1a9ffa4f7db577020f",
      "signature": {
        "s": "0x2bdd2c1be513987934ce46f35ec82f4122a53f787c3795dd3a77873fe6bcc377",
        "r": "0x2a9e34f0c10f67fb5ee397907b624c48257b9fa0417a96706817603a90b2d92e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x64f9c1e1d047d30f7b8268a96dff40b9508482c864ba49441f2f811c0e1c2524",
      "signature": {
        "s": "0x0699128cb9c728d01da6c26bca3c47c8c01ec56a82f8ea42857bf4f0de4a7519",
        "r": "0x783417a07e527123330f4a1e21b99f1f14829cd017a760b2899b2eb0f0ee1836",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "837892",
    "total": "837892"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "837892",
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
            "amount": "37534238508"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "837"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0NTRiNjZiMC04MjJkLTViOTgtOTQ0NC1iYzE0NzE1MGNiOWIifQ==",
    "nonce": 5500,
    "balances": {
      "current": "12980147321404895",
      "previous": "12980147322243624"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8d02eb339ebaedfc6c058066cb30fc9d20adf14a",
    "nonce": 22,
    "balances": {
      "current": "837892",
      "previous": "0"
    }
  },
  "blockNumber": "10114665",
  "created": "2020-05-22T08:41:36.098Z",
  "updated": "2020-05-22T08:41:36.276Z",
  "id": "5ec79040e5756b00111b8679"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000cc904000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `837892`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`