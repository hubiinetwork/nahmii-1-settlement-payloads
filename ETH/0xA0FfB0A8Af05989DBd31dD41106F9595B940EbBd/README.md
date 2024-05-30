# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA0FfB0A8Af05989DBd31dD41106F9595B940EbBd`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000099a400000000000000000000000000000000000000000000000000000000000099a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000099a400000000000000000000000000000000000000000000000000000000000099a418b9ad13f1fa21382a6ef817f1367876a43567b413c37cbe229000d8862fc6436a26863efa85106fc0558cf85ac79ab9e429a1c01f1f3f39a98c3cdd3c454ba4026c0c29dbb593c21afcc61311ab87ba484379173597e2a0e5ac1553023bd820000000000000000000000000000000000000000000000000000000000000001c9cd639cac2d3209dbdc40d20aab94e09d251d184c3f1ba6ac0a9c27bea9d0a918e41c7d5caa9c4e0f4710bf373340d54eb3689b1ec833c1256020e4209bb750a75d7bf6869d297ac5c46d7df204fe868c4c1a5649536370e912bbb033a036024000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000049500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c80a81db000000000000000000000000000000000000000000000000002386f2c80b1ba600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009315100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a4d794f44526a4f4330774e7a45774c5455334e5755745957526a4e4331694e44557a4d5467784d57526b4e7a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a0ffb0a8af05989dbd31dd41106f9595b940ebbd00000000000000000000000000000000000000000000000000000000000099a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18b9ad13f1fa21382a6ef817f1367876a43567b413c37cbe229000d8862fc643",
      "signature": {
        "s": "0x026c0c29dbb593c21afcc61311ab87ba484379173597e2a0e5ac1553023bd820",
        "r": "0x6a26863efa85106fc0558cf85ac79ab9e429a1c01f1f3f39a98c3cdd3c454ba4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9cd639cac2d3209dbdc40d20aab94e09d251d184c3f1ba6ac0a9c27bea9d0a91",
      "signature": {
        "s": "0x75d7bf6869d297ac5c46d7df204fe868c4c1a5649536370e912bbb033a036024",
        "r": "0x8e41c7d5caa9c4e0f4710bf373340d54eb3689b1ec833c1256020e4209bb750a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "39332",
    "total": "39332"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "39332",
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
            "amount": "602449"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "39"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZjMyODRjOC0wNzEwLTU3NWUtYWRjNC1iNDUzMTgxMWRkNzEifQ==",
    "nonce": 1173,
    "balances": {
      "current": "10000001481212379",
      "previous": "10000001481251750"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa0ffb0a8af05989dbd31dd41106f9595b940ebbd",
    "nonce": 20,
    "balances": {
      "current": "39332",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:19.988Z",
  "updated": "2020-05-22T08:07:21.084Z",
  "id": "5ec78837005df800101bc3a8"
}
```
* *stageAmount*: `39332`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000099a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000099a400000000000000000000000000000000000000000000000000000000000099a418b9ad13f1fa21382a6ef817f1367876a43567b413c37cbe229000d8862fc6436a26863efa85106fc0558cf85ac79ab9e429a1c01f1f3f39a98c3cdd3c454ba4026c0c29dbb593c21afcc61311ab87ba484379173597e2a0e5ac1553023bd820000000000000000000000000000000000000000000000000000000000000001c9cd639cac2d3209dbdc40d20aab94e09d251d184c3f1ba6ac0a9c27bea9d0a918e41c7d5caa9c4e0f4710bf373340d54eb3689b1ec833c1256020e4209bb750a75d7bf6869d297ac5c46d7df204fe868c4c1a5649536370e912bbb033a036024000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000049500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c80a81db000000000000000000000000000000000000000000000000002386f2c80b1ba600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009315100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a6a4d794f44526a4f4330774e7a45774c5455334e5755745957526a4e4331694e44557a4d5467784d57526b4e7a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a0ffb0a8af05989dbd31dd41106f9595b940ebbd00000000000000000000000000000000000000000000000000000000000099a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18b9ad13f1fa21382a6ef817f1367876a43567b413c37cbe229000d8862fc643",
      "signature": {
        "s": "0x026c0c29dbb593c21afcc61311ab87ba484379173597e2a0e5ac1553023bd820",
        "r": "0x6a26863efa85106fc0558cf85ac79ab9e429a1c01f1f3f39a98c3cdd3c454ba4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9cd639cac2d3209dbdc40d20aab94e09d251d184c3f1ba6ac0a9c27bea9d0a91",
      "signature": {
        "s": "0x75d7bf6869d297ac5c46d7df204fe868c4c1a5649536370e912bbb033a036024",
        "r": "0x8e41c7d5caa9c4e0f4710bf373340d54eb3689b1ec833c1256020e4209bb750a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "39332",
    "total": "39332"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "39332",
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
            "amount": "602449"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "39"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZjMyODRjOC0wNzEwLTU3NWUtYWRjNC1iNDUzMTgxMWRkNzEifQ==",
    "nonce": 1173,
    "balances": {
      "current": "10000001481212379",
      "previous": "10000001481251750"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa0ffb0a8af05989dbd31dd41106f9595b940ebbd",
    "nonce": 20,
    "balances": {
      "current": "39332",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:19.988Z",
  "updated": "2020-05-22T08:07:21.084Z",
  "id": "5ec78837005df800101bc3a8"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000099a40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `39332`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``