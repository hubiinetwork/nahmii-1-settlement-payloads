# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4b1A826ab542cd59a8AaC457E5636BD526be379A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000005d700000000000000000000000000000000000000000000000000000000000005d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005d700000000000000000000000000000000000000000000000000000000000005d72899b13d6e873a6f689b25fbab05603cab1288fd8fefec4686f3a9aa62b3e7989649d8f67ab24a981673905cbb90f73ffba5f87b2391d6c495fd8b0e0383b5e000a2ecc260955d43f23d8411654f08b215ee9d3c8eacd0d020f44fac2670a8ba000000000000000000000000000000000000000000000000000000000000001c3bacf82e7ffbf5b7d4b8fe8aa9191e9635768634ced0dd6fa89c478885ee228704720782b0aab4e5a5603d5a25f557132bf44ecf2484b68d256ee9db9043c2586402f441e8622f5e635ee29f19958480a758401e0b3f40ba5aadf2c5e4623710000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caafd258000000000000000000000000000000000000000000000000002386f2caafd83000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008844100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e6d51794e44426c4d533034595449344c5455325a6a4974596a51325a69303159574a694e54426b4d7a646d596d456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004b1a826ab542cd59a8aac457e5636bd526be379a00000000000000000000000000000000000000000000000000000000000005d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2899b13d6e873a6f689b25fbab05603cab1288fd8fefec4686f3a9aa62b3e798",
      "signature": {
        "s": "0x00a2ecc260955d43f23d8411654f08b215ee9d3c8eacd0d020f44fac2670a8ba",
        "r": "0x9649d8f67ab24a981673905cbb90f73ffba5f87b2391d6c495fd8b0e0383b5e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3bacf82e7ffbf5b7d4b8fe8aa9191e9635768634ced0dd6fa89c478885ee2287",
      "signature": {
        "s": "0x6402f441e8622f5e635ee29f19958480a758401e0b3f40ba5aadf2c5e4623710",
        "r": "0x04720782b0aab4e5a5603d5a25f557132bf44ecf2484b68d256ee9db9043c258",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1495",
    "total": "1495"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1495",
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
            "amount": "558145"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NmQyNDBlMS04YTI4LTU2ZjItYjQ2Zi01YWJiNTBkMzdmYmEifQ==",
    "nonce": 916,
    "balances": {
      "current": "10000001525600856",
      "previous": "10000001525602352"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4b1a826ab542cd59a8aac457e5636bd526be379a",
    "nonce": 20,
    "balances": {
      "current": "1495",
      "previous": "0"
    }
  },
  "blockNumber": "10114515",
  "created": "2020-05-22T08:05:26.478Z",
  "updated": "2020-05-22T08:05:26.540Z",
  "id": "5ec787c6e5756b00111b809c"
}
```
* *stageAmount*: `1495`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000005d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005d700000000000000000000000000000000000000000000000000000000000005d72899b13d6e873a6f689b25fbab05603cab1288fd8fefec4686f3a9aa62b3e7989649d8f67ab24a981673905cbb90f73ffba5f87b2391d6c495fd8b0e0383b5e000a2ecc260955d43f23d8411654f08b215ee9d3c8eacd0d020f44fac2670a8ba000000000000000000000000000000000000000000000000000000000000001c3bacf82e7ffbf5b7d4b8fe8aa9191e9635768634ced0dd6fa89c478885ee228704720782b0aab4e5a5603d5a25f557132bf44ecf2484b68d256ee9db9043c2586402f441e8622f5e635ee29f19958480a758401e0b3f40ba5aadf2c5e4623710000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caafd258000000000000000000000000000000000000000000000000002386f2caafd83000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008844100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e6d51794e44426c4d533034595449344c5455325a6a4974596a51325a69303159574a694e54426b4d7a646d596d456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004b1a826ab542cd59a8aac457e5636bd526be379a00000000000000000000000000000000000000000000000000000000000005d7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2899b13d6e873a6f689b25fbab05603cab1288fd8fefec4686f3a9aa62b3e798",
      "signature": {
        "s": "0x00a2ecc260955d43f23d8411654f08b215ee9d3c8eacd0d020f44fac2670a8ba",
        "r": "0x9649d8f67ab24a981673905cbb90f73ffba5f87b2391d6c495fd8b0e0383b5e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3bacf82e7ffbf5b7d4b8fe8aa9191e9635768634ced0dd6fa89c478885ee2287",
      "signature": {
        "s": "0x6402f441e8622f5e635ee29f19958480a758401e0b3f40ba5aadf2c5e4623710",
        "r": "0x04720782b0aab4e5a5603d5a25f557132bf44ecf2484b68d256ee9db9043c258",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1495",
    "total": "1495"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1495",
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
            "amount": "558145"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2NmQyNDBlMS04YTI4LTU2ZjItYjQ2Zi01YWJiNTBkMzdmYmEifQ==",
    "nonce": 916,
    "balances": {
      "current": "10000001525600856",
      "previous": "10000001525602352"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4b1a826ab542cd59a8aac457e5636bd526be379a",
    "nonce": 20,
    "balances": {
      "current": "1495",
      "previous": "0"
    }
  },
  "blockNumber": "10114515",
  "created": "2020-05-22T08:05:26.478Z",
  "updated": "2020-05-22T08:05:26.540Z",
  "id": "5ec787c6e5756b00111b809c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000005d70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1495`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``