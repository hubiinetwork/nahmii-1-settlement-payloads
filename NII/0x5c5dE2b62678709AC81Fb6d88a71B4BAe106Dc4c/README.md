# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5c5dE2b62678709AC81Fb6d88a71B4BAe106Dc4c`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000012a99198d25000000000000000000000000000000000000000000000000000000071454ffd70b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000071454ffd70b0000000000000000000000000000000000000000000000000000c6a7cc8111088d8367f5b00ea329880a18162cbd5e82bc208cc0a2177cdd82555056ed2a5de8ea0817a5f955168f16bbaab210624ae924ed118f6f508703ef3edb4f16828e354f86679e50fb5a9c91153197eeb67b5ea36b1f5ff3a33a175df2f65402c83556000000000000000000000000000000000000000000000000000000000000001c637902c35dc9c780ac9896bdfd92d3668432c443bc65c75c281dfb1f95b221de165921412e24c976e40df5d42d1cb5f3318188b90623d81e68664c47b5d3e35a66ed7a80e0b1e28ae0bbc54a3b8bfd477b75f210ee2ba86dd67d8d89b4de11c6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074bd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac9b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000099d1a27029f7465e0d260000000000000000000000000000000000000000000099d1a270310d6b52e21a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001cff4fde90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c50b637e9a09eb215e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a45794e7a4a684d6930344f44466c4c54566d4f5455744f4755314f43316b4f575a6a4d445578597a5a6b4d32496966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000005c5de2b62678709ac81fb6d88a71b4bae106dc4c00000000000000000000000000000000000000000000000000012a99198d250000000000000000000000000000000000000000000000000000012384c48d4df500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8d8367f5b00ea329880a18162cbd5e82bc208cc0a2177cdd82555056ed2a5de8",
      "signature": {
        "s": "0x4f86679e50fb5a9c91153197eeb67b5ea36b1f5ff3a33a175df2f65402c83556",
        "r": "0xea0817a5f955168f16bbaab210624ae924ed118f6f508703ef3edb4f16828e35",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x637902c35dc9c780ac9896bdfd92d3668432c443bc65c75c281dfb1f95b221de",
      "signature": {
        "s": "0x66ed7a80e0b1e28ae0bbc54a3b8bfd477b75f210ee2ba86dd67d8d89b4de11c6",
        "r": "0x165921412e24c976e40df5d42d1cb5f3318188b90623d81e68664c47b5d3e35a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7783906793227",
    "total": "218423992848648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7783906793227",
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
            "amount": "27246661635626175766878"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7783906793"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMzEyNzJhMi04ODFlLTVmOTUtOGU1OC1kOWZjMDUxYzZkM2IifQ==",
    "nonce": 109723,
    "balances": {
      "current": "726389146292034564132134",
      "previous": "726389146299826254832154"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c5de2b62678709ac81fb6d88a71b4bae106dc4c",
    "nonce": 45,
    "balances": {
      "current": "328312023753984",
      "previous": "320528116960757"
    }
  },
  "blockNumber": "14709949",
  "created": "2022-05-04T08:49:35.654Z",
  "updated": "2022-05-04T08:49:35.721Z",
  "id": "62723e1f3592fd001130b3f0"
}
```
* *stageAmount*: `328312023753984`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000071454ffd70b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000071454ffd70b0000000000000000000000000000000000000000000000000000c6a7cc8111088d8367f5b00ea329880a18162cbd5e82bc208cc0a2177cdd82555056ed2a5de8ea0817a5f955168f16bbaab210624ae924ed118f6f508703ef3edb4f16828e354f86679e50fb5a9c91153197eeb67b5ea36b1f5ff3a33a175df2f65402c83556000000000000000000000000000000000000000000000000000000000000001c637902c35dc9c780ac9896bdfd92d3668432c443bc65c75c281dfb1f95b221de165921412e24c976e40df5d42d1cb5f3318188b90623d81e68664c47b5d3e35a66ed7a80e0b1e28ae0bbc54a3b8bfd477b75f210ee2ba86dd67d8d89b4de11c6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074bd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac9b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000099d1a27029f7465e0d260000000000000000000000000000000000000000000099d1a270310d6b52e21a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001cff4fde90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c50b637e9a09eb215e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a45794e7a4a684d6930344f44466c4c54566d4f5455744f4755314f43316b4f575a6a4d445578597a5a6b4d32496966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000005c5de2b62678709ac81fb6d88a71b4bae106dc4c00000000000000000000000000000000000000000000000000012a99198d250000000000000000000000000000000000000000000000000000012384c48d4df500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8d8367f5b00ea329880a18162cbd5e82bc208cc0a2177cdd82555056ed2a5de8",
      "signature": {
        "s": "0x4f86679e50fb5a9c91153197eeb67b5ea36b1f5ff3a33a175df2f65402c83556",
        "r": "0xea0817a5f955168f16bbaab210624ae924ed118f6f508703ef3edb4f16828e35",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x637902c35dc9c780ac9896bdfd92d3668432c443bc65c75c281dfb1f95b221de",
      "signature": {
        "s": "0x66ed7a80e0b1e28ae0bbc54a3b8bfd477b75f210ee2ba86dd67d8d89b4de11c6",
        "r": "0x165921412e24c976e40df5d42d1cb5f3318188b90623d81e68664c47b5d3e35a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7783906793227",
    "total": "218423992848648"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7783906793227",
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
            "amount": "27246661635626175766878"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7783906793"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMzEyNzJhMi04ODFlLTVmOTUtOGU1OC1kOWZjMDUxYzZkM2IifQ==",
    "nonce": 109723,
    "balances": {
      "current": "726389146292034564132134",
      "previous": "726389146299826254832154"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c5de2b62678709ac81fb6d88a71b4bae106dc4c",
    "nonce": 45,
    "balances": {
      "current": "328312023753984",
      "previous": "320528116960757"
    }
  },
  "blockNumber": "14709949",
  "created": "2022-05-04T08:49:35.654Z",
  "updated": "2022-05-04T08:49:35.721Z",
  "id": "62723e1f3592fd001130b3f0"
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
0x0f200f9b00000000000000000000000000000000000000000000000000012a99198d25000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `328312023753984`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`