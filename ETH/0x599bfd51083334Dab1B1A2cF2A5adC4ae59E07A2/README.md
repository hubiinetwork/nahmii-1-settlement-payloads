# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x599bfd51083334Dab1B1A2cF2A5adC4ae59E07A2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000012a300000000000000000000000000000000000000000000000000000000000012a3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000012a300000000000000000000000000000000000000000000000000000000000012a3016b8a58c49f72248ff44e8494173c7da97acb8f38ce364e970928316f4dbb18ea391ef535cce08c7943097ea23d1f846fa8ef6f32d74385de8add6f9a71c8a9044a41523e533c516e2f5453c087c56d8c722fdb0ed63c1086fb4fecd181166b1000000000000000000000000000000000000000000000000000000000000001c515365ef32e13fd82c899ac93d22498fb6b866c91862c56a6972d5c89f3766ec3da0d87b233f46168802acdeb2f9605665aabea1c5c8944967b968c1bdb652c97ca79db42188f205d36842b0bcfeb2543ab8a4dbe8c646f7f4a4db2feb8aef02000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000053300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7547735000000000000000000000000000000000000000000000000002386f2c755a1b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095fad00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f474d334e544d794d7930324d7a49304c54553359574d744f4467345a4330785a54646c4e4441774e324533597a416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000599bfd51083334dab1b1a2cf2a5adc4ae59e07a20000000000000000000000000000000000000000000000000000000000012a30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x16b8a58c49f72248ff44e8494173c7da97acb8f38ce364e970928316f4dbb18e",
      "signature": {
        "s": "0x44a41523e533c516e2f5453c087c56d8c722fdb0ed63c1086fb4fecd181166b1",
        "r": "0xa391ef535cce08c7943097ea23d1f846fa8ef6f32d74385de8add6f9a71c8a90",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x515365ef32e13fd82c899ac93d22498fb6b866c91862c56a6972d5c89f3766ec",
      "signature": {
        "s": "0x7ca79db42188f205d36842b0bcfeb2543ab8a4dbe8c646f7f4a4db2feb8aef02",
        "r": "0x3da0d87b233f46168802acdeb2f9605665aabea1c5c8944967b968c1bdb652c9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76336",
    "total": "76336"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76336",
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
            "amount": "614317"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "76"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OGM3NTMyMy02MzI0LTU3YWMtODg4ZC0xZTdlNDAwN2E3YzAifQ==",
    "nonce": 1331,
    "balances": {
      "current": "10000001469282101",
      "previous": "10000001469358513"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x599bfd51083334dab1b1a2cf2a5adc4ae59e07a2",
    "nonce": 20,
    "balances": {
      "current": "76336",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:35.514Z",
  "updated": "2020-05-22T08:08:35.578Z",
  "id": "5ec78883e5756b00111b811b"
}
```
* *stageAmount*: `76336`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000012a3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000012a300000000000000000000000000000000000000000000000000000000000012a3016b8a58c49f72248ff44e8494173c7da97acb8f38ce364e970928316f4dbb18ea391ef535cce08c7943097ea23d1f846fa8ef6f32d74385de8add6f9a71c8a9044a41523e533c516e2f5453c087c56d8c722fdb0ed63c1086fb4fecd181166b1000000000000000000000000000000000000000000000000000000000000001c515365ef32e13fd82c899ac93d22498fb6b866c91862c56a6972d5c89f3766ec3da0d87b233f46168802acdeb2f9605665aabea1c5c8944967b968c1bdb652c97ca79db42188f205d36842b0bcfeb2543ab8a4dbe8c646f7f4a4db2feb8aef02000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000053300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7547735000000000000000000000000000000000000000000000000002386f2c755a1b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095fad00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f474d334e544d794d7930324d7a49304c54553359574d744f4467345a4330785a54646c4e4441774e324533597a416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000599bfd51083334dab1b1a2cf2a5adc4ae59e07a20000000000000000000000000000000000000000000000000000000000012a30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x16b8a58c49f72248ff44e8494173c7da97acb8f38ce364e970928316f4dbb18e",
      "signature": {
        "s": "0x44a41523e533c516e2f5453c087c56d8c722fdb0ed63c1086fb4fecd181166b1",
        "r": "0xa391ef535cce08c7943097ea23d1f846fa8ef6f32d74385de8add6f9a71c8a90",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x515365ef32e13fd82c899ac93d22498fb6b866c91862c56a6972d5c89f3766ec",
      "signature": {
        "s": "0x7ca79db42188f205d36842b0bcfeb2543ab8a4dbe8c646f7f4a4db2feb8aef02",
        "r": "0x3da0d87b233f46168802acdeb2f9605665aabea1c5c8944967b968c1bdb652c9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "76336",
    "total": "76336"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "76336",
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
            "amount": "614317"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "76"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OGM3NTMyMy02MzI0LTU3YWMtODg4ZC0xZTdlNDAwN2E3YzAifQ==",
    "nonce": 1331,
    "balances": {
      "current": "10000001469282101",
      "previous": "10000001469358513"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x599bfd51083334dab1b1a2cf2a5adc4ae59e07a2",
    "nonce": 20,
    "balances": {
      "current": "76336",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:35.514Z",
  "updated": "2020-05-22T08:08:35.578Z",
  "id": "5ec78883e5756b00111b811b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000012a300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `76336`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``