# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x44c76C2DCf3D200f30200Fff82C49C579ba49eA5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e7770808f3faceb0000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000000000000000000000000004806bdb138ef0588000951e87826aedf3ad3d8b198e45540a57ed5f9b83117aa1c3ffcc9c302342fdce82038f1e9644d0f54c82c7f822bbb37eb8a64e1e50b326e6b4685d31b9e97ecd354d3d7f2be5bb6dfb7506e4f758d99a440c6ae94ccc2e1006ea856f356ec2d7000000000000000000000000000000000000000000000000000000000000001b9762a684d976bffdf0517af64facbfcf6caf802cdcfaf89373be8b93729b20e41b1e5539d8c0bc3144443121752ba7f5e5e0ff66a51adfe7002ef5bef94f4e340f4e4d463f3bf3de05b9fbeb8af84c380831dadc7859634401c9dd8123282a23000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304bd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f00000000000000000000000044c76c2dcf3d200f30200fff82c49c579ba49ea50000000000000000000000000000000000000000000000000e7770808f3faceb000000000000000000000000000000000000000000000481a1579953fe4c7ceb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e574e694d6d5a6a595330335a54686c4c5451334e5467744f44566c5a6930315a44673059325269596a6b784e54636966513d3d00000000000000000000000000000000000000000000000000000000000000e6000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000ced327f587a96d918a5f00000000000000000000000000000000000000000000ca52bc1a741a7d390a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x951e87826aedf3ad3d8b198e45540a57ed5f9b83117aa1c3ffcc9c302342fdce",
      "signature": {
        "s": "0x354d3d7f2be5bb6dfb7506e4f758d99a440c6ae94ccc2e1006ea856f356ec2d7",
        "r": "0x82038f1e9644d0f54c82c7f822bbb37eb8a64e1e50b326e6b4685d31b9e97ecd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9762a684d976bffdf0517af64facbfcf6caf802cdcfaf89373be8b93729b20e4",
      "signature": {
        "s": "0x0f4e4d463f3bf3de05b9fbeb8af84c380831dadc7859634401c9dd8123282a23",
        "r": "0x1b1e5539d8c0bc3144443121752ba7f5e5e0ff66a51adfe7002ef5bef94f4e34",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258421000000000000000",
    "total": "21258421000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258421000000000000000",
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
            "amount": "21258421000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258421000000000000"
      }
    },
    "wallet": "0x44c76c2dcf3d200f30200fff82c49c579ba49ea5",
    "data": "eyJyZWYiOiIyNWNiMmZjYS03ZThlLTQ3NTgtODVlZi01ZDg0Y2RiYjkxNTcifQ==",
    "nonce": 47,
    "balances": {
      "current": "1042425536220998891",
      "previous": "21280721846536220998891"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 230,
    "balances": {
      "current": "976702637827398160190047",
      "previous": "955444216827398160190047"
    }
  },
  "blockNumber": "14877885",
  "created": "2022-05-31T09:16:04.366Z",
  "updated": "2022-05-31T09:16:04.724Z",
  "id": "6295dcd4bbd75600116d0910"
}
```
* *stageAmount*: `1042425536220998891`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806bdb138ef05880000000000000000000000000000000000000000000000004806bdb138ef0588000951e87826aedf3ad3d8b198e45540a57ed5f9b83117aa1c3ffcc9c302342fdce82038f1e9644d0f54c82c7f822bbb37eb8a64e1e50b326e6b4685d31b9e97ecd354d3d7f2be5bb6dfb7506e4f758d99a440c6ae94ccc2e1006ea856f356ec2d7000000000000000000000000000000000000000000000000000000000000001b9762a684d976bffdf0517af64facbfcf6caf802cdcfaf89373be8b93729b20e41b1e5539d8c0bc3144443121752ba7f5e5e0ff66a51adfe7002ef5bef94f4e340f4e4d463f3bf3de05b9fbeb8af84c380831dadc7859634401c9dd8123282a23000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304bd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f00000000000000000000000044c76c2dcf3d200f30200fff82c49c579ba49ea50000000000000000000000000000000000000000000000000e7770808f3faceb000000000000000000000000000000000000000000000481a1579953fe4c7ceb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001270515447eb450000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e574e694d6d5a6a595330335a54686c4c5451334e5467744f44566c5a6930315a44673059325269596a6b784e54636966513d3d00000000000000000000000000000000000000000000000000000000000000e6000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000ced327f587a96d918a5f00000000000000000000000000000000000000000000ca52bc1a741a7d390a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x951e87826aedf3ad3d8b198e45540a57ed5f9b83117aa1c3ffcc9c302342fdce",
      "signature": {
        "s": "0x354d3d7f2be5bb6dfb7506e4f758d99a440c6ae94ccc2e1006ea856f356ec2d7",
        "r": "0x82038f1e9644d0f54c82c7f822bbb37eb8a64e1e50b326e6b4685d31b9e97ecd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9762a684d976bffdf0517af64facbfcf6caf802cdcfaf89373be8b93729b20e4",
      "signature": {
        "s": "0x0f4e4d463f3bf3de05b9fbeb8af84c380831dadc7859634401c9dd8123282a23",
        "r": "0x1b1e5539d8c0bc3144443121752ba7f5e5e0ff66a51adfe7002ef5bef94f4e34",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258421000000000000000",
    "total": "21258421000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258421000000000000000",
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
            "amount": "21258421000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258421000000000000"
      }
    },
    "wallet": "0x44c76c2dcf3d200f30200fff82c49c579ba49ea5",
    "data": "eyJyZWYiOiIyNWNiMmZjYS03ZThlLTQ3NTgtODVlZi01ZDg0Y2RiYjkxNTcifQ==",
    "nonce": 47,
    "balances": {
      "current": "1042425536220998891",
      "previous": "21280721846536220998891"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 230,
    "balances": {
      "current": "976702637827398160190047",
      "previous": "955444216827398160190047"
    }
  },
  "blockNumber": "14877885",
  "created": "2022-05-31T09:16:04.366Z",
  "updated": "2022-05-31T09:16:04.724Z",
  "id": "6295dcd4bbd75600116d0910"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e7770808f3faceb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1042425536220998891`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`