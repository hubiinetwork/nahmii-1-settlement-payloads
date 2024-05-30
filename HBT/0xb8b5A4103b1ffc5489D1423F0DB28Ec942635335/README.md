# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb8b5A4103b1ffc5489D1423F0DB28Ec942635335`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000015fb6e380000000000000000000000000000000000000000000000000000000015fb6e38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000015fb6e380000000000000000000000000000000000000000000000000000000015fb6e389aaba4dfda647583dbceeebcf8607b313b51d626708ae77ba1451a6aa5e99db941de456f4798c733809ab2508609acca279de0be0026142b1f9fe299a50a2eff38ce32dd2e383e60c5bf4b96214b48a52c67d05c12e7be99f2d67d82aa79f9cb000000000000000000000000000000000000000000000000000000000000001b0112cd3c51db4871e2b05f27c586b206d89a26e9226aa43ab12963698ee1564cd125ec388b0b6103e433092e7dd1e8324a89bd7408d05e8cd6357322c09a9f73194b3e7080ccf55b12eefe080bfb1c1d6b2a1ea872c277f76e10dd0952f624b7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5664000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014e400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e21a871297f9b000000000000000000000000000000000000000000000000002e21a8872a8e7200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005a09f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007a4d20696000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497959544d795a544a694e6930324f546c6c4c54553259324d74595456694d5330794d574e6a596a51344e44526b4d47496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000b8b5a4103b1ffc5489d1423f0db28ec9426353350000000000000000000000000000000000000000000000000000000015fb6e38000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9aaba4dfda647583dbceeebcf8607b313b51d626708ae77ba1451a6aa5e99db9",
      "signature": {
        "s": "0x38ce32dd2e383e60c5bf4b96214b48a52c67d05c12e7be99f2d67d82aa79f9cb",
        "r": "0x41de456f4798c733809ab2508609acca279de0be0026142b1f9fe299a50a2eff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0112cd3c51db4871e2b05f27c586b206d89a26e9226aa43ab12963698ee1564c",
      "signature": {
        "s": "0x194b3e7080ccf55b12eefe080bfb1c1d6b2a1ea872c277f76e10dd0952f624b7",
        "r": "0xd125ec388b0b6103e433092e7dd1e8324a89bd7408d05e8cd6357322c09a9f73",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "368799288",
    "total": "368799288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "368799288",
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
            "amount": "32829998742"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "368799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTMyZTJiNi02OTllLTU2Y2MtYTViMS0yMWNjYjQ4NDRkMGIifQ==",
    "nonce": 5348,
    "balances": {
      "current": "12984856265457563",
      "previous": "12984856634625650"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8b5a4103b1ffc5489d1423f0db28ec942635335",
    "nonce": 13,
    "balances": {
      "current": "368799288",
      "previous": "0"
    }
  },
  "blockNumber": "10114660",
  "created": "2020-05-22T08:40:27.873Z",
  "updated": "2020-05-22T08:40:27.944Z",
  "id": "5ec78ffb005df800101bc935"
}
```
* *stageAmount*: `368799288`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000015fb6e38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000015fb6e380000000000000000000000000000000000000000000000000000000015fb6e389aaba4dfda647583dbceeebcf8607b313b51d626708ae77ba1451a6aa5e99db941de456f4798c733809ab2508609acca279de0be0026142b1f9fe299a50a2eff38ce32dd2e383e60c5bf4b96214b48a52c67d05c12e7be99f2d67d82aa79f9cb000000000000000000000000000000000000000000000000000000000000001b0112cd3c51db4871e2b05f27c586b206d89a26e9226aa43ab12963698ee1564cd125ec388b0b6103e433092e7dd1e8324a89bd7408d05e8cd6357322c09a9f73194b3e7080ccf55b12eefe080bfb1c1d6b2a1ea872c277f76e10dd0952f624b7000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5664000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014e400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e21a871297f9b000000000000000000000000000000000000000000000000002e21a8872a8e7200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005a09f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007a4d20696000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497959544d795a544a694e6930324f546c6c4c54553259324d74595456694d5330794d574e6a596a51344e44526b4d47496966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000b8b5a4103b1ffc5489d1423f0db28ec9426353350000000000000000000000000000000000000000000000000000000015fb6e38000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9aaba4dfda647583dbceeebcf8607b313b51d626708ae77ba1451a6aa5e99db9",
      "signature": {
        "s": "0x38ce32dd2e383e60c5bf4b96214b48a52c67d05c12e7be99f2d67d82aa79f9cb",
        "r": "0x41de456f4798c733809ab2508609acca279de0be0026142b1f9fe299a50a2eff",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0112cd3c51db4871e2b05f27c586b206d89a26e9226aa43ab12963698ee1564c",
      "signature": {
        "s": "0x194b3e7080ccf55b12eefe080bfb1c1d6b2a1ea872c277f76e10dd0952f624b7",
        "r": "0xd125ec388b0b6103e433092e7dd1e8324a89bd7408d05e8cd6357322c09a9f73",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "368799288",
    "total": "368799288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "368799288",
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
            "amount": "32829998742"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "368799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTMyZTJiNi02OTllLTU2Y2MtYTViMS0yMWNjYjQ4NDRkMGIifQ==",
    "nonce": 5348,
    "balances": {
      "current": "12984856265457563",
      "previous": "12984856634625650"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8b5a4103b1ffc5489d1423f0db28ec942635335",
    "nonce": 13,
    "balances": {
      "current": "368799288",
      "previous": "0"
    }
  },
  "blockNumber": "10114660",
  "created": "2020-05-22T08:40:27.873Z",
  "updated": "2020-05-22T08:40:27.944Z",
  "id": "5ec78ffb005df800101bc935"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000015fb6e38000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `368799288`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`