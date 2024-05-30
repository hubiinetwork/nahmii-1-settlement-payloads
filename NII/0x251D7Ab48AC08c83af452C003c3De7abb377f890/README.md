# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x251D7Ab48AC08c83af452C003c3De7abb377f890`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000549d53cf5ff64d2e100000000000000000000000000000000000000000000000000000001fd319f2d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001fd319f2d0000000000000000000000000000000000000000000000000000002e6b880a863d4ce80d4bccd638e2b21e1d64b08be53577ac64db4d29bab620af3e6a5a02987edbbf6fc6991b5f2a1994d8aff1934100f33c03a3823e23966b3f488cad5bed0c78325032dc78a78188547fe1c22f372e05f3499931f6a71c01aaf7ba29d496000000000000000000000000000000000000000000000000000000000000001c3a3e1892e53dfa51702329bb99be5b5eba6bc31bc94f9398e149e13916d9ce35cd10cda6c7cc56fdb20a950060371e83bb38324953381fbc0f0786fc0cc7acfc5d200fec8b364b786d62fa7ae82648aa623a292838419f5d0734af5b84266284000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b368000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bcf37421437000000000000000000000000000000000000000000003c8863632bd134f60dea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000825a860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556ccfe12ba50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a457a4d7a5530595330324e7a55314c54566b4e6a63744f4459344d6930324e6d59344e6d4534597a5979597a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000026000000000000000000000000251d7ab48ac08c83af452c003c3de7abb377f89000000000000000000000000000000000000000000000000549d53cf5ff64d2e100000000000000000000000000000000000000000000000549d53cf4023333b400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3d4ce80d4bccd638e2b21e1d64b08be53577ac64db4d29bab620af3e6a5a0298",
      "signature": {
        "s": "0x0c78325032dc78a78188547fe1c22f372e05f3499931f6a71c01aaf7ba29d496",
        "r": "0x7edbbf6fc6991b5f2a1994d8aff1934100f33c03a3823e23966b3f488cad5bed",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3a3e1892e53dfa51702329bb99be5b5eba6bc31bc94f9398e149e13916d9ce35",
      "signature": {
        "s": "0x5d200fec8b364b786d62fa7ae82648aa623a292838419f5d0734af5b84266284",
        "r": "0xcd10cda6c7cc56fdb20a950060371e83bb38324953381fbc0f0786fc0cc7acfc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8542854957",
    "total": "199372573318"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8542854957",
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
            "amount": "27686752782988643216293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8542854"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjEzMzU0YS02NzU1LTVkNjctODY4Mi02NmY4NmE4YzYyYzMifQ==",
    "nonce": 111464,
    "balances": {
      "current": "285857907782204646364215",
      "previous": "285857907782213197762026"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x251d7ab48ac08c83af452c003c3de7abb377f890",
    "nonce": 38,
    "balances": {
      "current": "97553945930605318881",
      "previous": "97553945922062463924"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:27.023Z",
  "updated": "2022-05-04T08:58:27.162Z",
  "id": "627240333592fd001130b63f"
}
```
* *stageAmount*: `97553945930605318881`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000001fd319f2d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001fd319f2d0000000000000000000000000000000000000000000000000000002e6b880a863d4ce80d4bccd638e2b21e1d64b08be53577ac64db4d29bab620af3e6a5a02987edbbf6fc6991b5f2a1994d8aff1934100f33c03a3823e23966b3f488cad5bed0c78325032dc78a78188547fe1c22f372e05f3499931f6a71c01aaf7ba29d496000000000000000000000000000000000000000000000000000000000000001c3a3e1892e53dfa51702329bb99be5b5eba6bc31bc94f9398e149e13916d9ce35cd10cda6c7cc56fdb20a950060371e83bb38324953381fbc0f0786fc0cc7acfc5d200fec8b364b786d62fa7ae82648aa623a292838419f5d0734af5b84266284000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b368000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bcf37421437000000000000000000000000000000000000000000003c8863632bd134f60dea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000825a860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556ccfe12ba50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a457a4d7a5530595330324e7a55314c54566b4e6a63744f4459344d6930324e6d59344e6d4534597a5979597a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000026000000000000000000000000251d7ab48ac08c83af452c003c3de7abb377f89000000000000000000000000000000000000000000000000549d53cf5ff64d2e100000000000000000000000000000000000000000000000549d53cf4023333b400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3d4ce80d4bccd638e2b21e1d64b08be53577ac64db4d29bab620af3e6a5a0298",
      "signature": {
        "s": "0x0c78325032dc78a78188547fe1c22f372e05f3499931f6a71c01aaf7ba29d496",
        "r": "0x7edbbf6fc6991b5f2a1994d8aff1934100f33c03a3823e23966b3f488cad5bed",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3a3e1892e53dfa51702329bb99be5b5eba6bc31bc94f9398e149e13916d9ce35",
      "signature": {
        "s": "0x5d200fec8b364b786d62fa7ae82648aa623a292838419f5d0734af5b84266284",
        "r": "0xcd10cda6c7cc56fdb20a950060371e83bb38324953381fbc0f0786fc0cc7acfc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8542854957",
    "total": "199372573318"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8542854957",
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
            "amount": "27686752782988643216293"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8542854"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjEzMzU0YS02NzU1LTVkNjctODY4Mi02NmY4NmE4YzYyYzMifQ==",
    "nonce": 111464,
    "balances": {
      "current": "285857907782204646364215",
      "previous": "285857907782213197762026"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x251d7ab48ac08c83af452c003c3de7abb377f890",
    "nonce": 38,
    "balances": {
      "current": "97553945930605318881",
      "previous": "97553945922062463924"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:27.023Z",
  "updated": "2022-05-04T08:58:27.162Z",
  "id": "627240333592fd001130b63f"
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
0x0f200f9b00000000000000000000000000000000000000000000000549d53cf5ff64d2e10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `97553945930605318881`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`