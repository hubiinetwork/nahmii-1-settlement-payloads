# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x97c6421e4aB0Bb2fA51E0af004C4fc6c6DEab5D6`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000001ad72000000000000000000000000000000000000000000000000000000000001ad720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001ad72000000000000000000000000000000000000000000000000000000000001ad7242e08cab08762cbadf25a1a4409ed896ec4225a87aaa645831531c9922184dc5413b285a2343aae2c0d637d3652a4a13133426a55673f04a7cad168933585f0d558c4c02ce5611f500855fa19f32f7721ebb251949f834ddf24b9ea340590aed000000000000000000000000000000000000000000000000000000000000001cd002f26fe46de2bde31d2edc335d8cbb8d55bc183bf96a329d278c38506b31542c95d3290dd6fc0f279db72d20dbec97dff3cec019b5448e3ff901526f71355c1c7dae6ef945758243bb8a460fbbca80f46f6ea2df254afc7d492f211800f5df000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000072900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42a1767000000000000000000000000000000000000000000000000002386f2c42bc54600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000006d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2e4b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596a5131597a59304e43316d596d526c4c5456684e5749744f4751304e53316c5a574669597a59344e445132597a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000097c6421e4ab0bb2fa51e0af004c4fc6c6deab5d6000000000000000000000000000000000000000000000000000000000001ad72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x42e08cab08762cbadf25a1a4409ed896ec4225a87aaa645831531c9922184dc5",
      "signature": {
        "s": "0x558c4c02ce5611f500855fa19f32f7721ebb251949f834ddf24b9ea340590aed",
        "r": "0x413b285a2343aae2c0d637d3652a4a13133426a55673f04a7cad168933585f0d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd002f26fe46de2bde31d2edc335d8cbb8d55bc183bf96a329d278c38506b3154",
      "signature": {
        "s": "0x1c7dae6ef945758243bb8a460fbbca80f46f6ea2df254afc7d492f211800f5df",
        "r": "0x2c95d3290dd6fc0f279db72d20dbec97dff3cec019b5448e3ff901526f71355c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "109938",
    "total": "109938"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "109938",
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
            "amount": "667211"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "109"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYjQ1YzY0NC1mYmRlLTVhNWItOGQ0NS1lZWFiYzY4NDQ2YzcifQ==",
    "nonce": 1833,
    "balances": {
      "current": "10000001416173415",
      "previous": "10000001416283462"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x97c6421e4ab0bb2fa51e0af004c4fc6c6deab5d6",
    "nonce": 20,
    "balances": {
      "current": "109938",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:25.018Z",
  "updated": "2020-05-22T08:12:25.085Z",
  "id": "5ec78969b0c6090011d5ab2f"
}
```
* *stageAmount*: `109938`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000001ad720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001ad72000000000000000000000000000000000000000000000000000000000001ad7242e08cab08762cbadf25a1a4409ed896ec4225a87aaa645831531c9922184dc5413b285a2343aae2c0d637d3652a4a13133426a55673f04a7cad168933585f0d558c4c02ce5611f500855fa19f32f7721ebb251949f834ddf24b9ea340590aed000000000000000000000000000000000000000000000000000000000000001cd002f26fe46de2bde31d2edc335d8cbb8d55bc183bf96a329d278c38506b31542c95d3290dd6fc0f279db72d20dbec97dff3cec019b5448e3ff901526f71355c1c7dae6ef945758243bb8a460fbbca80f46f6ea2df254afc7d492f211800f5df000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000072900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c42a1767000000000000000000000000000000000000000000000000002386f2c42bc54600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000006d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2e4b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596a5131597a59304e43316d596d526c4c5456684e5749744f4751304e53316c5a574669597a59344e445132597a636966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000097c6421e4ab0bb2fa51e0af004c4fc6c6deab5d6000000000000000000000000000000000000000000000000000000000001ad72000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x42e08cab08762cbadf25a1a4409ed896ec4225a87aaa645831531c9922184dc5",
      "signature": {
        "s": "0x558c4c02ce5611f500855fa19f32f7721ebb251949f834ddf24b9ea340590aed",
        "r": "0x413b285a2343aae2c0d637d3652a4a13133426a55673f04a7cad168933585f0d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd002f26fe46de2bde31d2edc335d8cbb8d55bc183bf96a329d278c38506b3154",
      "signature": {
        "s": "0x1c7dae6ef945758243bb8a460fbbca80f46f6ea2df254afc7d492f211800f5df",
        "r": "0x2c95d3290dd6fc0f279db72d20dbec97dff3cec019b5448e3ff901526f71355c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "109938",
    "total": "109938"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "109938",
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
            "amount": "667211"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "109"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwYjQ1YzY0NC1mYmRlLTVhNWItOGQ0NS1lZWFiYzY4NDQ2YzcifQ==",
    "nonce": 1833,
    "balances": {
      "current": "10000001416173415",
      "previous": "10000001416283462"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x97c6421e4ab0bb2fa51e0af004c4fc6c6deab5d6",
    "nonce": 20,
    "balances": {
      "current": "109938",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:25.018Z",
  "updated": "2020-05-22T08:12:25.085Z",
  "id": "5ec78969b0c6090011d5ab2f"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000001ad720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `109938`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``