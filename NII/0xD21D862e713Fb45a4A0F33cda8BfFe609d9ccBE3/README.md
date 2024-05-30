# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD21D862e713Fb45a4A0F33cda8BfFe609d9ccBE3`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de1c6279f11accd0000000000000000000000000000000000000000000000066429d659810100000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000066429d659810100000000000000000000000000000000000000000000000000066429d65981010000e1a81a44c2ac2ebdad988867743c56234fa5d596f1faef58819b133d5d46f6e4f75275e6cd16b9ad58990c0bc3b70f46889f63f2f4d7e53669b88ce402dd87a92c41cf02d6fa63c7afe72f02269e5724739e0f2d251d24e7198b0870657c34f5000000000000000000000000000000000000000000000000000000000000001b2c1148789c874cc3275a00ff5ed99d2cf88e7a45884eaa7176736739440a3a344f1c385bcae12980a9a7f77ac0714ed7d528b37cf48301bcdb4d89eb119b5790295b4d610b29f8e65af4020a621ead77fd0df5e5cd56404545fc4be4cc98a7a5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e30a2c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000d21d862e713fb45a4a0f33cda8bffe609d9ccbe30000000000000000000000000000000000000000000000000de1c6279f11accd00000000000000000000000000000000000000000000000673ae781c59cd4ccd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001a2db9b39baa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001a2db9b39baa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a5669596d4d794d5330784d7a4a694c54526c4e7a4d744f5463324e533169593255335a4442684e3251774d57596966513d3d000000000000000000000000000000000000000000000000000000000000011f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001da736205d76a1814bc2f00000000000000000000000000000000000000000001da6cfddc01109713bc2f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1a81a44c2ac2ebdad988867743c56234fa5d596f1faef58819b133d5d46f6e4",
      "signature": {
        "s": "0x2c41cf02d6fa63c7afe72f02269e5724739e0f2d251d24e7198b0870657c34f5",
        "r": "0xf75275e6cd16b9ad58990c0bc3b70f46889f63f2f4d7e53669b88ce402dd87a9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2c1148789c874cc3275a00ff5ed99d2cf88e7a45884eaa7176736739440a3a34",
      "signature": {
        "s": "0x295b4d610b29f8e65af4020a621ead77fd0df5e5cd56404545fc4be4cc98a7a5",
        "r": "0x4f1c385bcae12980a9a7f77ac0714ed7d528b37cf48301bcdb4d89eb119b5790",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "117898000000000000000",
    "total": "117898000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "117898000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "117898000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "117898000000000000"
      }
    },
    "wallet": "0xd21d862e713fb45a4a0f33cda8bffe609d9ccbe3",
    "data": "eyJyZWYiOiI5MjViYmMyMS0xMzJiLTRlNzMtOTc2NS1iY2U3ZDBhN2QwMWYifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000298465727720653",
      "previous": "119016196465727720653"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 287,
    "balances": {
      "current": "2240530151737129700736047",
      "previous": "2240412253737129700736047"
    }
  },
  "blockNumber": "14879276",
  "created": "2022-05-31T14:47:17.219Z",
  "updated": "2022-05-31T14:47:17.320Z",
  "id": "62962a757832e20011830f7d"
}
```
* *stageAmount*: `1000298465727720653`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000066429d659810100000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000066429d659810100000000000000000000000000000000000000000000000000066429d65981010000e1a81a44c2ac2ebdad988867743c56234fa5d596f1faef58819b133d5d46f6e4f75275e6cd16b9ad58990c0bc3b70f46889f63f2f4d7e53669b88ce402dd87a92c41cf02d6fa63c7afe72f02269e5724739e0f2d251d24e7198b0870657c34f5000000000000000000000000000000000000000000000000000000000000001b2c1148789c874cc3275a00ff5ed99d2cf88e7a45884eaa7176736739440a3a344f1c385bcae12980a9a7f77ac0714ed7d528b37cf48301bcdb4d89eb119b5790295b4d610b29f8e65af4020a621ead77fd0df5e5cd56404545fc4be4cc98a7a5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e30a2c0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000d21d862e713fb45a4a0f33cda8bffe609d9ccbe30000000000000000000000000000000000000000000000000de1c6279f11accd00000000000000000000000000000000000000000000000673ae781c59cd4ccd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001a2db9b39baa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001a2db9b39baa0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a5669596d4d794d5330784d7a4a694c54526c4e7a4d744f5463324e533169593255335a4442684e3251774d57596966513d3d000000000000000000000000000000000000000000000000000000000000011f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000001da736205d76a1814bc2f00000000000000000000000000000000000000000001da6cfddc01109713bc2f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1a81a44c2ac2ebdad988867743c56234fa5d596f1faef58819b133d5d46f6e4",
      "signature": {
        "s": "0x2c41cf02d6fa63c7afe72f02269e5724739e0f2d251d24e7198b0870657c34f5",
        "r": "0xf75275e6cd16b9ad58990c0bc3b70f46889f63f2f4d7e53669b88ce402dd87a9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2c1148789c874cc3275a00ff5ed99d2cf88e7a45884eaa7176736739440a3a34",
      "signature": {
        "s": "0x295b4d610b29f8e65af4020a621ead77fd0df5e5cd56404545fc4be4cc98a7a5",
        "r": "0x4f1c385bcae12980a9a7f77ac0714ed7d528b37cf48301bcdb4d89eb119b5790",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "117898000000000000000",
    "total": "117898000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "117898000000000000000",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "117898000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "117898000000000000"
      }
    },
    "wallet": "0xd21d862e713fb45a4a0f33cda8bffe609d9ccbe3",
    "data": "eyJyZWYiOiI5MjViYmMyMS0xMzJiLTRlNzMtOTc2NS1iY2U3ZDBhN2QwMWYifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000298465727720653",
      "previous": "119016196465727720653"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 287,
    "balances": {
      "current": "2240530151737129700736047",
      "previous": "2240412253737129700736047"
    }
  },
  "blockNumber": "14879276",
  "created": "2022-05-31T14:47:17.219Z",
  "updated": "2022-05-31T14:47:17.320Z",
  "id": "62962a757832e20011830f7d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de1c6279f11accd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000298465727720653`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`