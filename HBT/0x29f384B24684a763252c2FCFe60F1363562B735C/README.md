# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x29f384B24684a763252c2FCFe60F1363562B735C`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000000000000000000000000000000000001b626406ad86fb5909b22fe0470b3c76a330762c40caa9cf0e67155aa10038d5ea45efe8e93fc699155309ff578499341f329f51399391fac616459fc327fbf5a359aa6b6eb734dfbf0170cd9f8078dd740b862615fc416720b704cd2619387ddfba5699000000000000000000000000000000000000000000000000000000000000001cba6b2f1385c18e0990ea2d0f7e04f0496994cf9e2026a05b8130b0360f348e2139c0cf16f09d048041c307d555d963e6f9b09523cb94daaeca137cd92a496cf73e2c7e3c0abd53bca0ffacc4ae1230bbc80a573672039ec3b6195ee4e5950a31000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cc500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1327cf1f4864000000000000000000000000000000000000000000000000002e1327ea88af1200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000702a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b5a4e0f20000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f4451314d324934597930314d6a67334c5455334f545574595459784e5330794d54426a5a4755325a5452684e47456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000029f384b24684a763252c2fcfe60f1363562b735c000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad86fb5909b22fe0470b3c76a330762c40caa9cf0e67155aa10038d5ea45efe8",
      "signature": {
        "s": "0x6eb734dfbf0170cd9f8078dd740b862615fc416720b704cd2619387ddfba5699",
        "r": "0xe93fc699155309ff578499341f329f51399391fac616459fc327fbf5a359aa6b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba6b2f1385c18e0990ea2d0f7e04f0496994cf9e2026a05b8130b0360f348e21",
      "signature": {
        "s": "0x3e2c7e3c0abd53bca0ffacc4ae1230bbc80a573672039ec3b6195ee4e5950a31",
        "r": "0x39c0cf16f09d048041c307d555d963e6f9b09523cb94daaeca137cd92a496cf7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "459432966",
    "total": "459432966"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "459432966",
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
            "amount": "48759705376"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "459432"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ODQ1M2I4Yy01Mjg3LTU3OTUtYTYxNS0yMTBjZGU2ZTRhNGEifQ==",
    "nonce": 7365,
    "balances": {
      "current": "12968910628276324",
      "previous": "12968911088168722"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29f384b24684a763252c2fcfe60f1363562b735c",
    "nonce": 22,
    "balances": {
      "current": "459432966",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:14.305Z",
  "updated": "2020-05-22T08:56:14.367Z",
  "id": "5ec793aeb0c6090011d5b26a"
}
```
* *stageAmount*: `459432966`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000000000000000000000000000000000001b626406ad86fb5909b22fe0470b3c76a330762c40caa9cf0e67155aa10038d5ea45efe8e93fc699155309ff578499341f329f51399391fac616459fc327fbf5a359aa6b6eb734dfbf0170cd9f8078dd740b862615fc416720b704cd2619387ddfba5699000000000000000000000000000000000000000000000000000000000000001cba6b2f1385c18e0990ea2d0f7e04f0496994cf9e2026a05b8130b0360f348e2139c0cf16f09d048041c307d555d963e6f9b09523cb94daaeca137cd92a496cf73e2c7e3c0abd53bca0ffacc4ae1230bbc80a573672039ec3b6195ee4e5950a31000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001cc500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1327cf1f4864000000000000000000000000000000000000000000000000002e1327ea88af1200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000702a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b5a4e0f20000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f4451314d324934597930314d6a67334c5455334f545574595459784e5330794d54426a5a4755325a5452684e47456966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000029f384b24684a763252c2fcfe60f1363562b735c000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad86fb5909b22fe0470b3c76a330762c40caa9cf0e67155aa10038d5ea45efe8",
      "signature": {
        "s": "0x6eb734dfbf0170cd9f8078dd740b862615fc416720b704cd2619387ddfba5699",
        "r": "0xe93fc699155309ff578499341f329f51399391fac616459fc327fbf5a359aa6b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba6b2f1385c18e0990ea2d0f7e04f0496994cf9e2026a05b8130b0360f348e21",
      "signature": {
        "s": "0x3e2c7e3c0abd53bca0ffacc4ae1230bbc80a573672039ec3b6195ee4e5950a31",
        "r": "0x39c0cf16f09d048041c307d555d963e6f9b09523cb94daaeca137cd92a496cf7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "459432966",
    "total": "459432966"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "459432966",
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
            "amount": "48759705376"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "459432"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ODQ1M2I4Yy01Mjg3LTU3OTUtYTYxNS0yMTBjZGU2ZTRhNGEifQ==",
    "nonce": 7365,
    "balances": {
      "current": "12968910628276324",
      "previous": "12968911088168722"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x29f384b24684a763252c2fcfe60f1363562b735c",
    "nonce": 22,
    "balances": {
      "current": "459432966",
      "previous": "0"
    }
  },
  "blockNumber": "10114738",
  "created": "2020-05-22T08:56:14.305Z",
  "updated": "2020-05-22T08:56:14.367Z",
  "id": "5ec793aeb0c6090011d5b26a"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001b626406000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `459432966`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`