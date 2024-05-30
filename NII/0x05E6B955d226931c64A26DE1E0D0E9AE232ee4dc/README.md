# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x05E6B955d226931c64A26DE1E0D0E9AE232ee4dc`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000003923293c61cd8beeb60000000000000000000000000000000000000000000000015acb1f6c376fef9e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000015acb1f6c376fef9e000000000000000000000000000000000000000000000026035c80e2b651f62ed823338908f3ce173c0a349e3cc0130c900a4bf707f60857c243b7542a4ec54544930e4c51d49a45d909b9bb56b4b331ffeb0be4e2da32825f4776711c5755463ed27cd597bde75232516f09669aca10482b5cfdc05b4635297034d59f5f85f7000000000000000000000000000000000000000000000000000000000000001b3918c5417e46578a6697c5c6626059c73bc525f3b777922cddc1b178ee72d538a649b1be58046f602f8f6808f0fd1af3bd58b7af810728512f873c6d36e5db77756d9d4a49754c3c2e6025a541f1a91348ad3cff5b3fb8c03174a3fc3cfaf00d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad7c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009688471331a81ac82082000000000000000000000000000000000000000000009689a2371888e8cd6c4400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000058c77496955c240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e28f934f2f4cf8fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474e694e5441345953316b4d6a45794c5455784f5745744f4449345a533032597a5269596a67304e6a42684e44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000005e6b955d226931c64a26de1e0d0e9ae232ee4dc00000000000000000000000000000000000000000000003923293c61cd8beeb6000000000000000000000000000000000000000000000037c85e1cf5961bff1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd823338908f3ce173c0a349e3cc0130c900a4bf707f60857c243b7542a4ec545",
      "signature": {
        "s": "0x3ed27cd597bde75232516f09669aca10482b5cfdc05b4635297034d59f5f85f7",
        "r": "0x44930e4c51d49a45d909b9bb56b4b331ffeb0be4e2da32825f4776711c575546",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3918c5417e46578a6697c5c6626059c73bc525f3b777922cddc1b178ee72d538",
      "signature": {
        "s": "0x756d9d4a49754c3c2e6025a541f1a91348ad3cff5b3fb8c03174a3fc3cfaf00d",
        "r": "0xa649b1be58046f602f8f6808f0fd1af3bd58b7af810728512f873c6d36e5db77",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24989101507042340766",
    "total": "701218484992143914542"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24989101507042340766",
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
            "amount": "27262166426011554347262"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24989101507042340"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhOGNiNTA4YS1kMjEyLTUxOWEtODI4ZS02YzRiYjg0NjBhNDYifQ==",
    "nonce": 109948,
    "balances": {
      "current": "710868851116270605049986",
      "previous": "710893865206879154433092"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05e6b955d226931c64a26de1e0d0e9ae232ee4dc",
    "nonce": 46,
    "balances": {
      "current": "1053998034857575050934",
      "previous": "1029008933350532710168"
    }
  },
  "blockNumber": "14709956",
  "created": "2022-05-04T08:50:45.453Z",
  "updated": "2022-05-04T08:50:45.606Z",
  "id": "62723e657832e20011830b16"
}
```
* *stageAmount*: `1053998034857575050934`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000015acb1f6c376fef9e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000015acb1f6c376fef9e000000000000000000000000000000000000000000000026035c80e2b651f62ed823338908f3ce173c0a349e3cc0130c900a4bf707f60857c243b7542a4ec54544930e4c51d49a45d909b9bb56b4b331ffeb0be4e2da32825f4776711c5755463ed27cd597bde75232516f09669aca10482b5cfdc05b4635297034d59f5f85f7000000000000000000000000000000000000000000000000000000000000001b3918c5417e46578a6697c5c6626059c73bc525f3b777922cddc1b178ee72d538a649b1be58046f602f8f6808f0fd1af3bd58b7af810728512f873c6d36e5db77756d9d4a49754c3c2e6025a541f1a91348ad3cff5b3fb8c03174a3fc3cfaf00d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad7c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009688471331a81ac82082000000000000000000000000000000000000000000009689a2371888e8cd6c4400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000058c77496955c240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e28f934f2f4cf8fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f474e694e5441345953316b4d6a45794c5455784f5745744f4449345a533032597a5269596a67304e6a42684e44596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000005e6b955d226931c64a26de1e0d0e9ae232ee4dc00000000000000000000000000000000000000000000003923293c61cd8beeb6000000000000000000000000000000000000000000000037c85e1cf5961bff1800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd823338908f3ce173c0a349e3cc0130c900a4bf707f60857c243b7542a4ec545",
      "signature": {
        "s": "0x3ed27cd597bde75232516f09669aca10482b5cfdc05b4635297034d59f5f85f7",
        "r": "0x44930e4c51d49a45d909b9bb56b4b331ffeb0be4e2da32825f4776711c575546",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3918c5417e46578a6697c5c6626059c73bc525f3b777922cddc1b178ee72d538",
      "signature": {
        "s": "0x756d9d4a49754c3c2e6025a541f1a91348ad3cff5b3fb8c03174a3fc3cfaf00d",
        "r": "0xa649b1be58046f602f8f6808f0fd1af3bd58b7af810728512f873c6d36e5db77",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24989101507042340766",
    "total": "701218484992143914542"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24989101507042340766",
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
            "amount": "27262166426011554347262"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "24989101507042340"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhOGNiNTA4YS1kMjEyLTUxOWEtODI4ZS02YzRiYjg0NjBhNDYifQ==",
    "nonce": 109948,
    "balances": {
      "current": "710868851116270605049986",
      "previous": "710893865206879154433092"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x05e6b955d226931c64a26de1e0d0e9ae232ee4dc",
    "nonce": 46,
    "balances": {
      "current": "1053998034857575050934",
      "previous": "1029008933350532710168"
    }
  },
  "blockNumber": "14709956",
  "created": "2022-05-04T08:50:45.453Z",
  "updated": "2022-05-04T08:50:45.606Z",
  "id": "62723e657832e20011830b16"
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
0x0f200f9b00000000000000000000000000000000000000000000003923293c61cd8beeb60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1053998034857575050934`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`