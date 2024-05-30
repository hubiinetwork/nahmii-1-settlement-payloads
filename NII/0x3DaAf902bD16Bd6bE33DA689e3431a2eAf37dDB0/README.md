# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3DaAf902bD16Bd6bE33DA689e3431a2eAf37dDB0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000137e18a3e29602241b0000000000000000000000000000000000000000000000086a9a2f3807bdb23e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000086a9a2f3807bdb23e0000000000000000000000000000000000000000000000137e18a3e29602241b7646ef0f3d9cfeaddb50bf8c8e8653b3f9f7467b7458cd81b8c3930f7c877891d02dc75cdf31cdf70da635fc8b8f87b0a8ae7d9c4de0188bcc32216e6ce5a5226d399de10384fcab7575540ff831186db845e7e0acd79995b3ce30b61fd552b7000000000000000000000000000000000000000000000000000000000000001bfa7c3e6286e73daaa0716cd2500007b827d31406f3b0448992c5b8cdd7e10d7c9662dbc602625955fdad6231b159fef39620e4dfa20410970251ebbf6461e613537881417bc32752b599449f80d1f26ea6dec225183d7c137341f551ff9cd91b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bac19b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011720000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000846341f844e19bf175100000000000000000000000000000000000000000000084ea0e1478a06df066800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000002279403e5623cd90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000032a3d437a924334b9f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d5759794e44417a4f4330774e6a55314c5455354e7a51744f4455304d6930345a6a4d3459324a6a4e6a646a596a496966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000003daaf902bd16bd6be33da689e3431a2eaf37ddb00000000000000000000000000000000000000000000000137e18a3e29602241b00000000000000000000000000000000000000000000000b137e74aa8e4471dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7646ef0f3d9cfeaddb50bf8c8e8653b3f9f7467b7458cd81b8c3930f7c877891",
      "signature": {
        "s": "0x6d399de10384fcab7575540ff831186db845e7e0acd79995b3ce30b61fd552b7",
        "r": "0xd02dc75cdf31cdf70da635fc8b8f87b0a8ae7d9c4de0188bcc32216e6ce5a522",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa7c3e6286e73daaa0716cd2500007b827d31406f3b0448992c5b8cdd7e10d7c",
      "signature": {
        "s": "0x537881417bc32752b599449f80d1f26ea6dec225183d7c137341f551ff9cd91b",
        "r": "0x9662dbc602625955fdad6231b159fef39620e4dfa20410970251ebbf6461e613",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "155255456621804761662",
    "total": "359574329842276115483"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "155255456621804761662",
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
            "amount": "14946277206533101369845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "155255456621804761"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MWYyNDAzOC0wNjU1LTU5NzQtODU0Mi04ZjM4Y2JjNjdjYjIifQ==",
    "nonce": 71456,
    "balances": {
      "current": "39073959814202054874961",
      "previous": "39229370526280481441384"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3daaf902bd16bd6be33da689e3431a2eaf37ddb0",
    "nonce": 2,
    "balances": {
      "current": "359574329842276115483",
      "previous": "204318873220471353821"
    }
  },
  "blockNumber": "12239259",
  "created": "2021-04-14T16:24:15.901Z",
  "updated": "2021-04-14T16:24:15.966Z",
  "id": "6077172f50c3ba0010570ec2"
}
```
* *stageAmount*: `359574329842276115483`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000086a9a2f3807bdb23e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000086a9a2f3807bdb23e0000000000000000000000000000000000000000000000137e18a3e29602241b7646ef0f3d9cfeaddb50bf8c8e8653b3f9f7467b7458cd81b8c3930f7c877891d02dc75cdf31cdf70da635fc8b8f87b0a8ae7d9c4de0188bcc32216e6ce5a5226d399de10384fcab7575540ff831186db845e7e0acd79995b3ce30b61fd552b7000000000000000000000000000000000000000000000000000000000000001bfa7c3e6286e73daaa0716cd2500007b827d31406f3b0448992c5b8cdd7e10d7c9662dbc602625955fdad6231b159fef39620e4dfa20410970251ebbf6461e613537881417bc32752b599449f80d1f26ea6dec225183d7c137341f551ff9cd91b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bac19b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011720000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000846341f844e19bf175100000000000000000000000000000000000000000000084ea0e1478a06df066800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000002279403e5623cd90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000032a3d437a924334b9f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d5759794e44417a4f4330774e6a55314c5455354e7a51744f4455304d6930345a6a4d3459324a6a4e6a646a596a496966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000003daaf902bd16bd6be33da689e3431a2eaf37ddb00000000000000000000000000000000000000000000000137e18a3e29602241b00000000000000000000000000000000000000000000000b137e74aa8e4471dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7646ef0f3d9cfeaddb50bf8c8e8653b3f9f7467b7458cd81b8c3930f7c877891",
      "signature": {
        "s": "0x6d399de10384fcab7575540ff831186db845e7e0acd79995b3ce30b61fd552b7",
        "r": "0xd02dc75cdf31cdf70da635fc8b8f87b0a8ae7d9c4de0188bcc32216e6ce5a522",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa7c3e6286e73daaa0716cd2500007b827d31406f3b0448992c5b8cdd7e10d7c",
      "signature": {
        "s": "0x537881417bc32752b599449f80d1f26ea6dec225183d7c137341f551ff9cd91b",
        "r": "0x9662dbc602625955fdad6231b159fef39620e4dfa20410970251ebbf6461e613",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "155255456621804761662",
    "total": "359574329842276115483"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "155255456621804761662",
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
            "amount": "14946277206533101369845"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "155255456621804761"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MWYyNDAzOC0wNjU1LTU5NzQtODU0Mi04ZjM4Y2JjNjdjYjIifQ==",
    "nonce": 71456,
    "balances": {
      "current": "39073959814202054874961",
      "previous": "39229370526280481441384"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3daaf902bd16bd6be33da689e3431a2eaf37ddb0",
    "nonce": 2,
    "balances": {
      "current": "359574329842276115483",
      "previous": "204318873220471353821"
    }
  },
  "blockNumber": "12239259",
  "created": "2021-04-14T16:24:15.901Z",
  "updated": "2021-04-14T16:24:15.966Z",
  "id": "6077172f50c3ba0010570ec2"
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
0x0f200f9b0000000000000000000000000000000000000000000000137e18a3e29602241b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `359574329842276115483`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`