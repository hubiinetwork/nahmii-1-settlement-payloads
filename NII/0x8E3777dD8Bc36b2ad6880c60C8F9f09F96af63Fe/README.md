# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8E3777dD8Bc36b2ad6880c60C8F9f09F96af63Fe`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000027e93754dfabe08db0000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000000000000000000000000000027e93754dfabe08db444c89b61ad788ee4c1b8709c16e0829e6a6c6868cdeb967d5f508e773e9b475220b796972ad6856f69eb63bb9f8967a1bc10d0c26482fc88e46efc1d3d4784d598e559ca608cf5f9c509755bf06c16cdd478f70b6f394451b2846ad2394aeb5000000000000000000000000000000000000000000000000000000000000001b6bc184b702b0b49b9d8d4e78ad187c897d50dae3981e52c1d56ffd5ccec51bc0992b0ce7affc202db77791e7d7e3b87adeae6f4a396011bf35ba8c60e395a5ce476c50c1c1daae501230303fe700bef1bf386dd698f90d8958ce91f8e9516ff6000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026a721533e0e4a65e0590000000000000000000000000000000000000000000026a77f295a094496ba3100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4f021857c46f6db920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4467784d44426b5a4330354e6a6b784c54557a4f546774595464694f5330784e54466d4d7a4d784e57566c5a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000008e3777dd8bc36b2ad6880c60c8f9f09f96af63fe0000000000000000000000000000000000000000000000027e93754dfabe08db00000000000000000000000000000000000000000000000220d558d73787dc9f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x444c89b61ad788ee4c1b8709c16e0829e6a6c6868cdeb967d5f508e773e9b475",
      "signature": {
        "s": "0x598e559ca608cf5f9c509755bf06c16cdd478f70b6f394451b2846ad2394aeb5",
        "r": "0x220b796972ad6856f69eb63bb9f8967a1bc10d0c26482fc88e46efc1d3d4784d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6bc184b702b0b49b9d8d4e78ad187c897d50dae3981e52c1d56ffd5ccec51bc0",
      "signature": {
        "s": "0x476c50c1c1daae501230303fe700bef1bf386dd698f90d8958ce91f8e9516ff6",
        "r": "0x992b0ce7affc202db77791e7d7e3b87adeae6f4a396011bf35ba8c60e395a5ce",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "46014250795554179291"
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
            "amount": "17799964545068154936210"
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
    "data": "eyJyZWYiOiI3MDgxMDBkZC05NjkxLTUzOTgtYTdiOS0xNTFmMzMxNWVlZTgifQ==",
    "nonce": 80297,
    "balances": {
      "current": "182532933940613430501465",
      "previous": "182539695563268727159345"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8e3777dd8bc36b2ad6880c60c8f9f09f96af63fe",
    "nonce": 6,
    "balances": {
      "current": "46014250795554179291",
      "previous": "39259383008045030559"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:45.774Z",
  "updated": "2021-07-05T11:14:45.866Z",
  "id": "60e2e9a5abca510010d0444f"
}
```
* *stageAmount*: `46014250795554179291`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000000000000000000000000000027e93754dfabe08db444c89b61ad788ee4c1b8709c16e0829e6a6c6868cdeb967d5f508e773e9b475220b796972ad6856f69eb63bb9f8967a1bc10d0c26482fc88e46efc1d3d4784d598e559ca608cf5f9c509755bf06c16cdd478f70b6f394451b2846ad2394aeb5000000000000000000000000000000000000000000000000000000000000001b6bc184b702b0b49b9d8d4e78ad187c897d50dae3981e52c1d56ffd5ccec51bc0992b0ce7affc202db77791e7d7e3b87adeae6f4a396011bf35ba8c60e395a5ce476c50c1c1daae501230303fe700bef1bf386dd698f90d8958ce91f8e9516ff6000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000139a9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026a721533e0e4a65e0590000000000000000000000000000000000000000000026a77f295a094496ba3100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c4f021857c46f6db920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4467784d44426b5a4330354e6a6b784c54557a4f546774595464694f5330784e54466d4d7a4d784e57566c5a54676966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000008e3777dd8bc36b2ad6880c60c8f9f09f96af63fe0000000000000000000000000000000000000000000000027e93754dfabe08db00000000000000000000000000000000000000000000000220d558d73787dc9f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x444c89b61ad788ee4c1b8709c16e0829e6a6c6868cdeb967d5f508e773e9b475",
      "signature": {
        "s": "0x598e559ca608cf5f9c509755bf06c16cdd478f70b6f394451b2846ad2394aeb5",
        "r": "0x220b796972ad6856f69eb63bb9f8967a1bc10d0c26482fc88e46efc1d3d4784d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6bc184b702b0b49b9d8d4e78ad187c897d50dae3981e52c1d56ffd5ccec51bc0",
      "signature": {
        "s": "0x476c50c1c1daae501230303fe700bef1bf386dd698f90d8958ce91f8e9516ff6",
        "r": "0x992b0ce7affc202db77791e7d7e3b87adeae6f4a396011bf35ba8c60e395a5ce",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "46014250795554179291"
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
            "amount": "17799964545068154936210"
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
    "data": "eyJyZWYiOiI3MDgxMDBkZC05NjkxLTUzOTgtYTdiOS0xNTFmMzMxNWVlZTgifQ==",
    "nonce": 80297,
    "balances": {
      "current": "182532933940613430501465",
      "previous": "182539695563268727159345"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8e3777dd8bc36b2ad6880c60c8f9f09f96af63fe",
    "nonce": 6,
    "balances": {
      "current": "46014250795554179291",
      "previous": "39259383008045030559"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:45.774Z",
  "updated": "2021-07-05T11:14:45.866Z",
  "id": "60e2e9a5abca510010d0444f"
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
0x0f200f9b0000000000000000000000000000000000000000000000027e93754dfabe08db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `46014250795554179291`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`