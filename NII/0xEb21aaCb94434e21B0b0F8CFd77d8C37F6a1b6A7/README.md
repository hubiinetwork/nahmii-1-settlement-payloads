# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEb21aaCb94434e21B0b0F8CFd77d8C37F6a1b6A7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000024238f271470a0000000000000000000000000000000000000000000000000000000000006cc50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006cc5000000000000000000000000000000000000000000000000000000000009ea7629ed0cf914864f0b927ca228b6d93c9eba61178cc4cbb8b8494ef329cb25f11fd8c8e281543ad749ca590faa7014dca25fc3884d44a99372eafcbc3ed719b7e030c61bd4e9099bd4166dea9bdd0de1a94231d016f12a9606baf868bf26d56284000000000000000000000000000000000000000000000000000000000000001c28c5ae44ff9fdd6d571cf2af0d5d2fc95f58e05a80a33ce317355195e62cfe2c17f37aa0e4d19a60f39de0668e6457ec62c5afe3c6cc32dc05844ffac8600d215daff51b3f6712521915393cb993d734d141ada703956d83cbeed1a6d66965a7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b48e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395c7368a0b9503583b700000000000000000000000000000000000000000000395c7368a0b95035f09700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb6874e6735211def0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6a42685a474e6d5a53316c4d5441304c5455334e6a6b74595463774d6930345a57526a4e474a6a4f544d7a4e6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000eb21aacb94434e21b0b0f8cfd77d8c37f6a1b6a700000000000000000000000000000000000000000000000000024238f271470a00000000000000000000000000000000000000000000000000024238f270da4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x29ed0cf914864f0b927ca228b6d93c9eba61178cc4cbb8b8494ef329cb25f11f",
      "signature": {
        "s": "0x30c61bd4e9099bd4166dea9bdd0de1a94231d016f12a9606baf868bf26d56284",
        "r": "0xd8c8e281543ad749ca590faa7014dca25fc3884d44a99372eafcbc3ed719b7e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x28c5ae44ff9fdd6d571cf2af0d5d2fc95f58e05a80a33ce317355195e62cfe2c",
      "signature": {
        "s": "0x5daff51b3f6712521915393cb993d734d141ada703956d83cbeed1a6d66965a7",
        "r": "0x17f37aa0e4d19a60f39de0668e6457ec62c5afe3c6cc32dc05844ffac8600d21",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27845",
    "total": "649846"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27845",
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
            "amount": "27701715422079975759343"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMjBhZGNmZS1lMTA0LTU3NjktYTcwMi04ZWRjNGJjOTMzNjkifQ==",
    "nonce": 111758,
    "balances": {
      "current": "270880306051780770628535",
      "previous": "270880306051780770656407"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb21aacb94434e21b0b0f8cfd77d8c37f6a1b6a7",
    "nonce": 28,
    "balances": {
      "current": "635762306533130",
      "previous": "635762306505285"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:59.482Z",
  "updated": "2022-05-04T08:59:59.566Z",
  "id": "6272408f3592fd001130b69c"
}
```
* *stageAmount*: `635762306533130`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000006cc50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000006cc5000000000000000000000000000000000000000000000000000000000009ea7629ed0cf914864f0b927ca228b6d93c9eba61178cc4cbb8b8494ef329cb25f11fd8c8e281543ad749ca590faa7014dca25fc3884d44a99372eafcbc3ed719b7e030c61bd4e9099bd4166dea9bdd0de1a94231d016f12a9606baf868bf26d56284000000000000000000000000000000000000000000000000000000000000001c28c5ae44ff9fdd6d571cf2af0d5d2fc95f58e05a80a33ce317355195e62cfe2c17f37aa0e4d19a60f39de0668e6457ec62c5afe3c6cc32dc05844ffac8600d215daff51b3f6712521915393cb993d734d141ada703956d83cbeed1a6d66965a7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074de0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b48e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000395c7368a0b9503583b700000000000000000000000000000000000000000000395c7368a0b95035f09700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ddb6874e6735211def0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6a42685a474e6d5a53316c4d5441304c5455334e6a6b74595463774d6930345a57526a4e474a6a4f544d7a4e6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000eb21aacb94434e21b0b0f8cfd77d8c37f6a1b6a700000000000000000000000000000000000000000000000000024238f271470a00000000000000000000000000000000000000000000000000024238f270da4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x29ed0cf914864f0b927ca228b6d93c9eba61178cc4cbb8b8494ef329cb25f11f",
      "signature": {
        "s": "0x30c61bd4e9099bd4166dea9bdd0de1a94231d016f12a9606baf868bf26d56284",
        "r": "0xd8c8e281543ad749ca590faa7014dca25fc3884d44a99372eafcbc3ed719b7e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x28c5ae44ff9fdd6d571cf2af0d5d2fc95f58e05a80a33ce317355195e62cfe2c",
      "signature": {
        "s": "0x5daff51b3f6712521915393cb993d734d141ada703956d83cbeed1a6d66965a7",
        "r": "0x17f37aa0e4d19a60f39de0668e6457ec62c5afe3c6cc32dc05844ffac8600d21",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "27845",
    "total": "649846"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "27845",
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
            "amount": "27701715422079975759343"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "27"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMjBhZGNmZS1lMTA0LTU3NjktYTcwMi04ZWRjNGJjOTMzNjkifQ==",
    "nonce": 111758,
    "balances": {
      "current": "270880306051780770628535",
      "previous": "270880306051780770656407"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb21aacb94434e21b0b0f8cfd77d8c37f6a1b6a7",
    "nonce": 28,
    "balances": {
      "current": "635762306533130",
      "previous": "635762306505285"
    }
  },
  "blockNumber": "14709982",
  "created": "2022-05-04T08:59:59.482Z",
  "updated": "2022-05-04T08:59:59.566Z",
  "id": "6272408f3592fd001130b69c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000024238f271470a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `635762306533130`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`