# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcAC276b7492C4C788eFDb02464127216426AF6bC`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000025e6ef4536c1096100000000000000000000000000000000000000000000000000000023bd0fc2f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000023bd0fc2f500000000000000000000000000000000000000000000000000000342143e31da7691d16b7dbd29210642eb4d7b9e8fd5c903c2588ca128e352bd7465c5d56cce4ffd5eaf9045dc535b4b463b5283b1a67bd89f8a7f502d90dcec25e48f7333e038087b15e0ad42a347d743d36bb2294f99a877dc13398afe69e864b36b0d92eb000000000000000000000000000000000000000000000000000000000000001b645fda7661441e971100c3790777039a2f8bd0f9b6a2eadacae5db493f8b7fd62ef51134eebd77aefdf408c0dd48fc17bbd610e9e9068075bef71b3a92bbc3b77a978655562a074d9481650f5af5eed31d7f53426b3648cf051b51c33eefd483000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b095000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c7a7432af842da24f3a000000000000000000000000000000000000000000004c7a7432afa7f3d83b1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000092628e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8d2ea554b20f5cb960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5932517a4e6a497a5a4330774d54417a4c54566959545174596d59784f4330774f474d315a5468684d32466d597a556966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000cac276b7492c4c788efdb02464127216426af6bc00000000000000000000000000000000000000000000000025e6ef4536c1096100000000000000000000000000000000000000000000000025e6ef2179b1466c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7691d16b7dbd29210642eb4d7b9e8fd5c903c2588ca128e352bd7465c5d56cce",
      "signature": {
        "s": "0x38087b15e0ad42a347d743d36bb2294f99a877dc13398afe69e864b36b0d92eb",
        "r": "0x4ffd5eaf9045dc535b4b463b5283b1a67bd89f8a7f502d90dcec25e48f7333e0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x645fda7661441e971100c3790777039a2f8bd0f9b6a2eadacae5db493f8b7fd6",
      "signature": {
        "s": "0x7a978655562a074d9481650f5af5eed31d7f53426b3648cf051b51c33eefd483",
        "r": "0x2ef51134eebd77aefdf408c0dd48fc17bbd610e9e9068075bef71b3a92bbc3b7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "153495782133",
    "total": "3582342345178"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "153495782133",
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
            "amount": "27611527187943168265110"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "153495782"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjY2QzNjIzZC0wMTAzLTViYTQtYmYxOC0wOGM1ZThhM2FmYzUifQ==",
    "nonce": 110741,
    "balances": {
      "current": "361158728422725072867130",
      "previous": "361158728422878722145045"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcac276b7492c4c788efdb02464127216426af6bc",
    "nonce": 41,
    "balances": {
      "current": "2731133304597186913",
      "previous": "2731133151101404780"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:47.410Z",
  "updated": "2022-05-04T08:54:47.479Z",
  "id": "62723f573592fd001130b541"
}
```
* *stageAmount*: `2731133304597186913`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000023bd0fc2f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000023bd0fc2f500000000000000000000000000000000000000000000000000000342143e31da7691d16b7dbd29210642eb4d7b9e8fd5c903c2588ca128e352bd7465c5d56cce4ffd5eaf9045dc535b4b463b5283b1a67bd89f8a7f502d90dcec25e48f7333e038087b15e0ad42a347d743d36bb2294f99a877dc13398afe69e864b36b0d92eb000000000000000000000000000000000000000000000000000000000000001b645fda7661441e971100c3790777039a2f8bd0f9b6a2eadacae5db493f8b7fd62ef51134eebd77aefdf408c0dd48fc17bbd610e9e9068075bef71b3a92bbc3b77a978655562a074d9481650f5af5eed31d7f53426b3648cf051b51c33eefd483000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b095000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c7a7432af842da24f3a000000000000000000000000000000000000000000004c7a7432afa7f3d83b1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000092628e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8d2ea554b20f5cb960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5932517a4e6a497a5a4330774d54417a4c54566959545174596d59784f4330774f474d315a5468684d32466d597a556966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000cac276b7492c4c788efdb02464127216426af6bc00000000000000000000000000000000000000000000000025e6ef4536c1096100000000000000000000000000000000000000000000000025e6ef2179b1466c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7691d16b7dbd29210642eb4d7b9e8fd5c903c2588ca128e352bd7465c5d56cce",
      "signature": {
        "s": "0x38087b15e0ad42a347d743d36bb2294f99a877dc13398afe69e864b36b0d92eb",
        "r": "0x4ffd5eaf9045dc535b4b463b5283b1a67bd89f8a7f502d90dcec25e48f7333e0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x645fda7661441e971100c3790777039a2f8bd0f9b6a2eadacae5db493f8b7fd6",
      "signature": {
        "s": "0x7a978655562a074d9481650f5af5eed31d7f53426b3648cf051b51c33eefd483",
        "r": "0x2ef51134eebd77aefdf408c0dd48fc17bbd610e9e9068075bef71b3a92bbc3b7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "153495782133",
    "total": "3582342345178"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "153495782133",
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
            "amount": "27611527187943168265110"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "153495782"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjY2QzNjIzZC0wMTAzLTViYTQtYmYxOC0wOGM1ZThhM2FmYzUifQ==",
    "nonce": 110741,
    "balances": {
      "current": "361158728422725072867130",
      "previous": "361158728422878722145045"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcac276b7492c4c788efdb02464127216426af6bc",
    "nonce": 41,
    "balances": {
      "current": "2731133304597186913",
      "previous": "2731133151101404780"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:47.410Z",
  "updated": "2022-05-04T08:54:47.479Z",
  "id": "62723f573592fd001130b541"
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
0x0f200f9b00000000000000000000000000000000000000000000000025e6ef4536c109610000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2731133304597186913`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`