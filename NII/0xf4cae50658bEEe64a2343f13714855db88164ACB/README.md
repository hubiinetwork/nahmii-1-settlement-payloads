# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf4cae50658bEEe64a2343f13714855db88164ACB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000194784f576e7ebcf30000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c00000000000000000000000000000000000000000000000194784f576e7ebcf37de35c14e929413a0a075bae80bed072f3845a0adcc47e6c9e9b6b4f8fa469487a156bc7ace0291a9d9c4b05640592b2215e948e0150a1b9d83aebd32b1721d811cba830aba7e814b19720b1d66ebeeef43014a7233de42b3c0453ce61c74e20000000000000000000000000000000000000000000000000000000000000001c2492ceb8a78216e9d322393528795d0ebda051cf4253c6d58e41d0a5d81c4481ee776dc449c5398ace5236cd1ae5bd1b5c3830de9626dd59b3a627680010088625b7e2937afb254e57d442b8e063a43ebeb217be1c161cea95ee0a8c45f81f0b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139ac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026a56788035971dbb34f0000000000000000000000000000000000000000000026a5c55e1f546c0c8d2700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4f09281f6b420ae990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6a64685a5456685a5330345a4759784c54557a4e54597459544a695a5331694d546c6d5a5459314d6d49784e6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000f4cae50658beee64a2343f13714855db88164acb00000000000000000000000000000000000000000000000194784f576e7ebcf300000000000000000000000000000000000000000000000136ba32e0ab4890b700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7de35c14e929413a0a075bae80bed072f3845a0adcc47e6c9e9b6b4f8fa46948",
      "signature": {
        "s": "0x11cba830aba7e814b19720b1d66ebeeef43014a7233de42b3c0453ce61c74e20",
        "r": "0x7a156bc7ace0291a9d9c4b05640592b2215e948e0150a1b9d83aebd32b1721d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2492ceb8a78216e9d322393528795d0ebda051cf4253c6d58e41d0a5d81c4481",
      "signature": {
        "s": "0x25b7e2937afb254e57d442b8e063a43ebeb217be1c161cea95ee0a8c45f81f0b",
        "r": "0xee776dc449c5398ace5236cd1ae5bd1b5c3830de9626dd59b3a6276800100886",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "29145132225462713587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6754867787509148732",
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
            "amount": "17799996347868294196889"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6754867787509148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZjdhZTVhZS04ZGYxLTUzNTYtYTJiZS1iMTlmZTY1MmIxNjkifQ==",
    "nonce": 80300,
    "balances": {
      "current": "182501099337674030560079",
      "previous": "182507860960329327217959"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf4cae50658beee64a2343f13714855db88164acb",
    "nonce": 4,
    "balances": {
      "current": "29145132225462713587",
      "previous": "22390264437953564855"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:46.638Z",
  "updated": "2021-07-05T11:14:46.734Z",
  "id": "60e2e9a6abca510010d04450"
}
```
* *stageAmount*: `29145132225462713587`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c00000000000000000000000000000000000000000000000194784f576e7ebcf37de35c14e929413a0a075bae80bed072f3845a0adcc47e6c9e9b6b4f8fa469487a156bc7ace0291a9d9c4b05640592b2215e948e0150a1b9d83aebd32b1721d811cba830aba7e814b19720b1d66ebeeef43014a7233de42b3c0453ce61c74e20000000000000000000000000000000000000000000000000000000000000001c2492ceb8a78216e9d322393528795d0ebda051cf4253c6d58e41d0a5d81c4481ee776dc449c5398ace5236cd1ae5bd1b5c3830de9626dd59b3a627680010088625b7e2937afb254e57d442b8e063a43ebeb217be1c161cea95ee0a8c45f81f0b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139ac000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026a56788035971dbb34f0000000000000000000000000000000000000000000026a5c55e1f546c0c8d2700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4f09281f6b420ae990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6a64685a5456685a5330345a4759784c54557a4e54597459544a695a5331694d546c6d5a5459314d6d49784e6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000f4cae50658beee64a2343f13714855db88164acb00000000000000000000000000000000000000000000000194784f576e7ebcf300000000000000000000000000000000000000000000000136ba32e0ab4890b700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7de35c14e929413a0a075bae80bed072f3845a0adcc47e6c9e9b6b4f8fa46948",
      "signature": {
        "s": "0x11cba830aba7e814b19720b1d66ebeeef43014a7233de42b3c0453ce61c74e20",
        "r": "0x7a156bc7ace0291a9d9c4b05640592b2215e948e0150a1b9d83aebd32b1721d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2492ceb8a78216e9d322393528795d0ebda051cf4253c6d58e41d0a5d81c4481",
      "signature": {
        "s": "0x25b7e2937afb254e57d442b8e063a43ebeb217be1c161cea95ee0a8c45f81f0b",
        "r": "0xee776dc449c5398ace5236cd1ae5bd1b5c3830de9626dd59b3a6276800100886",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "29145132225462713587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6754867787509148732",
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
            "amount": "17799996347868294196889"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6754867787509148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZjdhZTVhZS04ZGYxLTUzNTYtYTJiZS1iMTlmZTY1MmIxNjkifQ==",
    "nonce": 80300,
    "balances": {
      "current": "182501099337674030560079",
      "previous": "182507860960329327217959"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf4cae50658beee64a2343f13714855db88164acb",
    "nonce": 4,
    "balances": {
      "current": "29145132225462713587",
      "previous": "22390264437953564855"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:46.638Z",
  "updated": "2021-07-05T11:14:46.734Z",
  "id": "60e2e9a6abca510010d04450"
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
0x0f200f9b00000000000000000000000000000000000000000000000194784f576e7ebcf30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `29145132225462713587`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`