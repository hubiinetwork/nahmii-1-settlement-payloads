# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x812DED039dB8026dF8b86B1f43991CD3CD51E237`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000000000000000000000000000000000044a91644668e354dd8a9c92b5d85bf97b1c7449e8ac44fd0a0c6145d94c961d2149f99a5acd849a9a007d233559cc86d19a3967b0bbbb17c7c592ca295f8c99cb154efb3b018bb52aa27290cbbc77e84bfe8f1694490dabe990350f596f8ce99fdff5b10b000000000000000000000000000000000000000000000000000000000000001bc0077257a916ec0d75ff5f69986a57b85c71b581ac03df46c56d16ca89e1bb65d4cda7c0ef1161365659de6bc5496da17a65b873dd9b4210fe48cd620b9d3f9a534488be6d1df930bdb82cdfce23d0b662898d511be40feb98228f726e42a4a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5664000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2185d76449d8000000000000000000000000000000000000000000000000002e218a230ee9dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001193bbf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007adab597d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d4451795954593359693079596d51354c54566c4d475974596d55774e43316a4e574e6c5a574d334d6a646a4e57496966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000812ded039db8026df8b86b1f43991cd3cd51e237000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x68e354dd8a9c92b5d85bf97b1c7449e8ac44fd0a0c6145d94c961d2149f99a5a",
      "signature": {
        "s": "0x018bb52aa27290cbbc77e84bfe8f1694490dabe990350f596f8ce99fdff5b10b",
        "r": "0xcd849a9a007d233559cc86d19a3967b0bbbb17c7c592ca295f8c99cb154efb3b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc0077257a916ec0d75ff5f69986a57b85c71b581ac03df46c56d16ca89e1bb65",
      "signature": {
        "s": "0x534488be6d1df930bdb82cdfce23d0b662898d511be40feb98228f726e42a4a3",
        "r": "0xd4cda7c0ef1161365659de6bc5496da17a65b873dd9b4210fe48cd620b9d3f9a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18430911558",
    "total": "18430911558"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18430911558",
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
            "amount": "32978459005"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "18430911"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MDQyYTY3Yi0yYmQ5LTVlMGYtYmUwNC1jNWNlZWM3MjdjNWIifQ==",
    "nonce": 5354,
    "balances": {
      "current": "12984707656731096",
      "previous": "12984726106073565"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x812ded039db8026df8b86b1f43991cd3cd51e237",
    "nonce": 26,
    "balances": {
      "current": "18430911558",
      "previous": "0"
    }
  },
  "blockNumber": "10114660",
  "created": "2020-05-22T08:40:32.360Z",
  "updated": "2020-05-22T08:40:32.443Z",
  "id": "5ec79000005df800101bc937"
}
```
* *stageAmount*: `18430911558`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000000000000000000000000000000000044a91644668e354dd8a9c92b5d85bf97b1c7449e8ac44fd0a0c6145d94c961d2149f99a5acd849a9a007d233559cc86d19a3967b0bbbb17c7c592ca295f8c99cb154efb3b018bb52aa27290cbbc77e84bfe8f1694490dabe990350f596f8ce99fdff5b10b000000000000000000000000000000000000000000000000000000000000001bc0077257a916ec0d75ff5f69986a57b85c71b581ac03df46c56d16ca89e1bb65d4cda7c0ef1161365659de6bc5496da17a65b873dd9b4210fe48cd620b9d3f9a534488be6d1df930bdb82cdfce23d0b662898d511be40feb98228f726e42a4a3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5664000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2185d76449d8000000000000000000000000000000000000000000000000002e218a230ee9dd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001193bbf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007adab597d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d4451795954593359693079596d51354c54566c4d475974596d55774e43316a4e574e6c5a574d334d6a646a4e57496966513d3d000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000812ded039db8026df8b86b1f43991cd3cd51e237000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x68e354dd8a9c92b5d85bf97b1c7449e8ac44fd0a0c6145d94c961d2149f99a5a",
      "signature": {
        "s": "0x018bb52aa27290cbbc77e84bfe8f1694490dabe990350f596f8ce99fdff5b10b",
        "r": "0xcd849a9a007d233559cc86d19a3967b0bbbb17c7c592ca295f8c99cb154efb3b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc0077257a916ec0d75ff5f69986a57b85c71b581ac03df46c56d16ca89e1bb65",
      "signature": {
        "s": "0x534488be6d1df930bdb82cdfce23d0b662898d511be40feb98228f726e42a4a3",
        "r": "0xd4cda7c0ef1161365659de6bc5496da17a65b873dd9b4210fe48cd620b9d3f9a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18430911558",
    "total": "18430911558"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18430911558",
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
            "amount": "32978459005"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "18430911"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MDQyYTY3Yi0yYmQ5LTVlMGYtYmUwNC1jNWNlZWM3MjdjNWIifQ==",
    "nonce": 5354,
    "balances": {
      "current": "12984707656731096",
      "previous": "12984726106073565"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x812ded039db8026df8b86b1f43991cd3cd51e237",
    "nonce": 26,
    "balances": {
      "current": "18430911558",
      "previous": "0"
    }
  },
  "blockNumber": "10114660",
  "created": "2020-05-22T08:40:32.360Z",
  "updated": "2020-05-22T08:40:32.443Z",
  "id": "5ec79000005df800101bc937"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000044a916446000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18430911558`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`