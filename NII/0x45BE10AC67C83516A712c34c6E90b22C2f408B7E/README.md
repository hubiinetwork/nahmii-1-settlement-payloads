# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x45BE10AC67C83516A712c34c6E90b22C2f408B7E`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b6b64e65cb4b0000000000000000000000000000000000000000000000620ebbe7808bd898000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000620ebbe7808bd898000000000000000000000000000000000000000000000000620ebbe7808bd89800f996c9f3e39d416882368b68cdbd775f50274a70015c6ea9bb0fd85fb982586256130c3e74f398b3e68ebabe1c8c2ed6bb5b47c75f5e36a88fb8ecf3c75821ae6041f5a5435f13919d7580e45d51ce16726210e8e070f64c558cc0b11721d154000000000000000000000000000000000000000000000000000000000000001b5a211d8bf6378f77ad1371165f780f46ce5cbc4d5c01339159ecd0e70d15b1ef9b495442ee8dc27119bab963d1d0e4819ad316aa513e9fd03bbd2cd81d6920010720c1be418c6d4179a6d842243a01e87b2897ee12ca292640d3353a7cf2546f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1cb700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000045be10ac67c83516a712c34c6e90b22c2f408b7e0000000000000000000000000000000000000000000000000de0b6b64e65cb4b00000000000000000000000000000000000000000000006235b6eafd618d324b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000191a4cc6874ecf000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000191a4cc6874ecf000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a526c4d574e6c4e6930334d5755304c5451315a444d74595749794e5330314d6a6b784d6d5a6b5a6a4a6d597a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001becb1b867ad5122fa47000000000000000000000000000000000000000000001b8aa2fc802cc54a624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf996c9f3e39d416882368b68cdbd775f50274a70015c6ea9bb0fd85fb9825862",
      "signature": {
        "s": "0x6041f5a5435f13919d7580e45d51ce16726210e8e070f64c558cc0b11721d154",
        "r": "0x56130c3e74f398b3e68ebabe1c8c2ed6bb5b47c75f5e36a88fb8ecf3c75821ae",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5a211d8bf6378f77ad1371165f780f46ce5cbc4d5c01339159ecd0e70d15b1ef",
      "signature": {
        "s": "0x0720c1be418c6d4179a6d842243a01e87b2897ee12ca292640d3353a7cf2546f",
        "r": "0x9b495442ee8dc27119bab963d1d0e4819ad316aa513e9fd03bbd2cd81d692001",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1808842615900000000000",
    "total": "1808842615900000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1808842615900000000000",
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
            "amount": "1808842615900000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1808842615900000000"
      }
    },
    "wallet": "0x45be10ac67c83516a712c34c6e90b22c2f408b7e",
    "data": "eyJyZWYiOiI4NjRlMWNlNi03MWU0LTQ1ZDMtYWIyNS01MjkxMmZkZjJmYzkifQ==",
    "nonce": 14,
    "balances": {
      "current": "1000000011391847243",
      "previous": "1811651458527291847243"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 32,
    "balances": {
      "current": "131870132738410391206471",
      "previous": "130061290122510391206471"
    }
  },
  "blockNumber": "14797680",
  "created": "2022-05-18T08:05:26.265Z",
  "updated": "2022-05-18T08:05:26.553Z",
  "id": "6284a8c63592fd001130b836"
}
```
* *stageAmount*: `1000000011391847243`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000620ebbe7808bd898000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000620ebbe7808bd898000000000000000000000000000000000000000000000000620ebbe7808bd89800f996c9f3e39d416882368b68cdbd775f50274a70015c6ea9bb0fd85fb982586256130c3e74f398b3e68ebabe1c8c2ed6bb5b47c75f5e36a88fb8ecf3c75821ae6041f5a5435f13919d7580e45d51ce16726210e8e070f64c558cc0b11721d154000000000000000000000000000000000000000000000000000000000000001b5a211d8bf6378f77ad1371165f780f46ce5cbc4d5c01339159ecd0e70d15b1ef9b495442ee8dc27119bab963d1d0e4819ad316aa513e9fd03bbd2cd81d6920010720c1be418c6d4179a6d842243a01e87b2897ee12ca292640d3353a7cf2546f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1cb700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000045be10ac67c83516a712c34c6e90b22c2f408b7e0000000000000000000000000000000000000000000000000de0b6b64e65cb4b00000000000000000000000000000000000000000000006235b6eafd618d324b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000191a4cc6874ecf000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000191a4cc6874ecf000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a526c4d574e6c4e6930334d5755304c5451315a444d74595749794e5330314d6a6b784d6d5a6b5a6a4a6d597a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000020000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001becb1b867ad5122fa47000000000000000000000000000000000000000000001b8aa2fc802cc54a624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf996c9f3e39d416882368b68cdbd775f50274a70015c6ea9bb0fd85fb9825862",
      "signature": {
        "s": "0x6041f5a5435f13919d7580e45d51ce16726210e8e070f64c558cc0b11721d154",
        "r": "0x56130c3e74f398b3e68ebabe1c8c2ed6bb5b47c75f5e36a88fb8ecf3c75821ae",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5a211d8bf6378f77ad1371165f780f46ce5cbc4d5c01339159ecd0e70d15b1ef",
      "signature": {
        "s": "0x0720c1be418c6d4179a6d842243a01e87b2897ee12ca292640d3353a7cf2546f",
        "r": "0x9b495442ee8dc27119bab963d1d0e4819ad316aa513e9fd03bbd2cd81d692001",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1808842615900000000000",
    "total": "1808842615900000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1808842615900000000000",
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
            "amount": "1808842615900000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1808842615900000000"
      }
    },
    "wallet": "0x45be10ac67c83516a712c34c6e90b22c2f408b7e",
    "data": "eyJyZWYiOiI4NjRlMWNlNi03MWU0LTQ1ZDMtYWIyNS01MjkxMmZkZjJmYzkifQ==",
    "nonce": 14,
    "balances": {
      "current": "1000000011391847243",
      "previous": "1811651458527291847243"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 32,
    "balances": {
      "current": "131870132738410391206471",
      "previous": "130061290122510391206471"
    }
  },
  "blockNumber": "14797680",
  "created": "2022-05-18T08:05:26.265Z",
  "updated": "2022-05-18T08:05:26.553Z",
  "id": "6284a8c63592fd001130b836"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b6b64e65cb4b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000000011391847243`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`