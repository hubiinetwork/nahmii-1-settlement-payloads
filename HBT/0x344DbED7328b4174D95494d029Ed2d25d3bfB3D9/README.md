# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x344DbED7328b4174D95494d029Ed2d25d3bfB3D9`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000026a0bb930000000000000000000000000000000000000000000000000000000026a0bb93000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000026a0bb930000000000000000000000000000000000000000000000000000000026a0bb932fda9b98ea880e1cbcd45a864a543676579f4c6d0cc9dfdf9e7d0645964992c586e7b5ec58d99fac86daf0f1e5d4ffe015f0a66bf37f99dc7d08c9d6c3d1d334354815a77a2a03386f2fc5eb2cd15547a21a7eb25d11e686d1920136d108023e000000000000000000000000000000000000000000000000000000000000001b74bfc453805eacae1f1dfcdc9d6382d2e37e5c2b19b0b3561fc9e8968371cf6c9f14987777a3ed0d8b1899b2027efb191052966de69a80f481822a067a3ec6b84988a56a2ae74d85b35ec06fe6ee6850f3fc33c5c3e16fd29f1ed9966367b7fa000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ae00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c7f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13541f1f98ce000000000000000000000000000000000000000000000000002e135445ca37e400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000009e383000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4ef8e57c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a546b304d474e6a59793033595463304c545578596a41744f4455304e5330795a546b3359574532595759314d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000344dbed7328b4174d95494d029ed2d25d3bfb3d90000000000000000000000000000000000000000000000000000000026a0bb93000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2fda9b98ea880e1cbcd45a864a543676579f4c6d0cc9dfdf9e7d0645964992c5",
      "signature": {
        "s": "0x354815a77a2a03386f2fc5eb2cd15547a21a7eb25d11e686d1920136d108023e",
        "r": "0x86e7b5ec58d99fac86daf0f1e5d4ffe015f0a66bf37f99dc7d08c9d6c3d1d334",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x74bfc453805eacae1f1dfcdc9d6382d2e37e5c2b19b0b3561fc9e8968371cf6c",
      "signature": {
        "s": "0x4988a56a2ae74d85b35ec06fe6ee6850f3fc33c5c3e16fd29f1ed9966367b7fa",
        "r": "0x9f14987777a3ed0d8b1899b2027efb191052966de69a80f481822a067a3ec6b8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "648067987",
    "total": "648067987"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "648067987",
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
            "amount": "48569574780"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "648067"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZTk0MGNjYy03YTc0LTUxYjAtODU0NS0yZTk3YWE2YWY1MmMifQ==",
    "nonce": 7295,
    "balances": {
      "current": "12969100949035214",
      "previous": "12969101597751268"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x344dbed7328b4174d95494d029ed2d25d3bfb3d9",
    "nonce": 22,
    "balances": {
      "current": "648067987",
      "previous": "0"
    }
  },
  "blockNumber": "10114734",
  "created": "2020-05-22T08:55:43.700Z",
  "updated": "2020-05-22T08:55:44.811Z",
  "id": "5ec7938f005df800101bcbd0"
}
```
* *stageAmount*: `648067987`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000026a0bb93000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000026a0bb930000000000000000000000000000000000000000000000000000000026a0bb932fda9b98ea880e1cbcd45a864a543676579f4c6d0cc9dfdf9e7d0645964992c586e7b5ec58d99fac86daf0f1e5d4ffe015f0a66bf37f99dc7d08c9d6c3d1d334354815a77a2a03386f2fc5eb2cd15547a21a7eb25d11e686d1920136d108023e000000000000000000000000000000000000000000000000000000000000001b74bfc453805eacae1f1dfcdc9d6382d2e37e5c2b19b0b3561fc9e8968371cf6c9f14987777a3ed0d8b1899b2027efb191052966de69a80f481822a067a3ec6b84988a56a2ae74d85b35ec06fe6ee6850f3fc33c5c3e16fd29f1ed9966367b7fa000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ae00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c7f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13541f1f98ce000000000000000000000000000000000000000000000000002e135445ca37e400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000009e383000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4ef8e57c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a546b304d474e6a59793033595463304c545578596a41744f4455304e5330795a546b3359574532595759314d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000344dbed7328b4174d95494d029ed2d25d3bfb3d90000000000000000000000000000000000000000000000000000000026a0bb93000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2fda9b98ea880e1cbcd45a864a543676579f4c6d0cc9dfdf9e7d0645964992c5",
      "signature": {
        "s": "0x354815a77a2a03386f2fc5eb2cd15547a21a7eb25d11e686d1920136d108023e",
        "r": "0x86e7b5ec58d99fac86daf0f1e5d4ffe015f0a66bf37f99dc7d08c9d6c3d1d334",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x74bfc453805eacae1f1dfcdc9d6382d2e37e5c2b19b0b3561fc9e8968371cf6c",
      "signature": {
        "s": "0x4988a56a2ae74d85b35ec06fe6ee6850f3fc33c5c3e16fd29f1ed9966367b7fa",
        "r": "0x9f14987777a3ed0d8b1899b2027efb191052966de69a80f481822a067a3ec6b8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "648067987",
    "total": "648067987"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "648067987",
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
            "amount": "48569574780"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "648067"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZTk0MGNjYy03YTc0LTUxYjAtODU0NS0yZTk3YWE2YWY1MmMifQ==",
    "nonce": 7295,
    "balances": {
      "current": "12969100949035214",
      "previous": "12969101597751268"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x344dbed7328b4174d95494d029ed2d25d3bfb3d9",
    "nonce": 22,
    "balances": {
      "current": "648067987",
      "previous": "0"
    }
  },
  "blockNumber": "10114734",
  "created": "2020-05-22T08:55:43.700Z",
  "updated": "2020-05-22T08:55:44.811Z",
  "id": "5ec7938f005df800101bcbd0"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000026a0bb93000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `648067987`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`