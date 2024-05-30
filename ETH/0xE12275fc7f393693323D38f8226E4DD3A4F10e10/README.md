# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE12275fc7f393693323D38f8226E4DD3A4F10e10`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000056e300000000000000000000000000000000000000000000000000000000000056e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000056e300000000000000000000000000000000000000000000000000000000000056e3d1f547fa48b0c6c7f0a387806dc55a479d92931421288343734fcbbac133325a970ffc3f2d0ce1a72e3b8981cfaf58589bfbc434cc33b7d3860098a58cfb5d3d083c88516683214cc0386d3acd9c0817ce939dea5ee937b82e51481588f24a9b000000000000000000000000000000000000000000000000000000000000001b7845d9d59b1b44ebbcbfba7e976887d9a9a8b007d462ed58bf8cf3dd231c456c56c02033a94610fde9d51b24d15e520246d9a48e862b0266636ca01983028b3c27c777821a38d81bbddea74eda2fe31a5ba032580695c414debf38ffafb6ea08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f7000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008e300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5daaaf000000000000000000000000000000000000000000000000002386f2bc5e01a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5441784e4463334d43307a4d5464694c54566c4e324d744f474d7a597930774e546b7a59574a6a4d6a6c6c4f44416966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000e12275fc7f393693323d38f8226e4dd3a4f10e1000000000000000000000000000000000000000000000000000000000000056e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1f547fa48b0c6c7f0a387806dc55a479d92931421288343734fcbbac133325a",
      "signature": {
        "s": "0x083c88516683214cc0386d3acd9c0817ce939dea5ee937b82e51481588f24a9b",
        "r": "0x970ffc3f2d0ce1a72e3b8981cfaf58589bfbc434cc33b7d3860098a58cfb5d3d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7845d9d59b1b44ebbcbfba7e976887d9a9a8b007d462ed58bf8cf3dd231c456c",
      "signature": {
        "s": "0x27c777821a38d81bbddea74eda2fe31a5ba032580695c414debf38ffafb6ea08",
        "r": "0x56c02033a94610fde9d51b24d15e520246d9a48e862b0266636ca01983028b3c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22243",
    "total": "22243"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22243",
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
            "amount": "797777"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "22"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNTAxNDc3MC0zMTdiLTVlN2MtOGMzYy0wNTkzYWJjMjllODAifQ==",
    "nonce": 2275,
    "balances": {
      "current": "10000001285335727",
      "previous": "10000001285357992"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe12275fc7f393693323d38f8226e4dd3a4f10e10",
    "nonce": 4,
    "balances": {
      "current": "22243",
      "previous": "0"
    }
  },
  "blockNumber": "10114551",
  "created": "2020-05-22T08:15:27.581Z",
  "updated": "2020-05-22T08:15:27.650Z",
  "id": "5ec78a1f005df800101bc51b"
}
```
* *stageAmount*: `22243`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000056e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000056e300000000000000000000000000000000000000000000000000000000000056e3d1f547fa48b0c6c7f0a387806dc55a479d92931421288343734fcbbac133325a970ffc3f2d0ce1a72e3b8981cfaf58589bfbc434cc33b7d3860098a58cfb5d3d083c88516683214cc0386d3acd9c0817ce939dea5ee937b82e51481588f24a9b000000000000000000000000000000000000000000000000000000000000001b7845d9d59b1b44ebbcbfba7e976887d9a9a8b007d462ed58bf8cf3dd231c456c56c02033a94610fde9d51b24d15e520246d9a48e862b0266636ca01983028b3c27c777821a38d81bbddea74eda2fe31a5ba032580695c414debf38ffafb6ea08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f7000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008e300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5daaaf000000000000000000000000000000000000000000000000002386f2bc5e01a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c5100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5441784e4463334d43307a4d5464694c54566c4e324d744f474d7a597930774e546b7a59574a6a4d6a6c6c4f44416966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000e12275fc7f393693323d38f8226e4dd3a4f10e1000000000000000000000000000000000000000000000000000000000000056e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd1f547fa48b0c6c7f0a387806dc55a479d92931421288343734fcbbac133325a",
      "signature": {
        "s": "0x083c88516683214cc0386d3acd9c0817ce939dea5ee937b82e51481588f24a9b",
        "r": "0x970ffc3f2d0ce1a72e3b8981cfaf58589bfbc434cc33b7d3860098a58cfb5d3d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7845d9d59b1b44ebbcbfba7e976887d9a9a8b007d462ed58bf8cf3dd231c456c",
      "signature": {
        "s": "0x27c777821a38d81bbddea74eda2fe31a5ba032580695c414debf38ffafb6ea08",
        "r": "0x56c02033a94610fde9d51b24d15e520246d9a48e862b0266636ca01983028b3c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "22243",
    "total": "22243"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "22243",
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
            "amount": "797777"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "22"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNTAxNDc3MC0zMTdiLTVlN2MtOGMzYy0wNTkzYWJjMjllODAifQ==",
    "nonce": 2275,
    "balances": {
      "current": "10000001285335727",
      "previous": "10000001285357992"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe12275fc7f393693323d38f8226e4dd3a4f10e10",
    "nonce": 4,
    "balances": {
      "current": "22243",
      "previous": "0"
    }
  },
  "blockNumber": "10114551",
  "created": "2020-05-22T08:15:27.581Z",
  "updated": "2020-05-22T08:15:27.650Z",
  "id": "5ec78a1f005df800101bc51b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000056e30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `22243`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``