# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x37C9e87c62c9f7DeD65b533A575B79ae3eD4ef65`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000001e767542e68fef758df00000000000000000000000000000000000000000000003627ec83a842e8fba70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000003627ec83a842e8fba70000000000000000000000000000000000000000000001e76750a0ea5a30d8df922372ccbd55fb431a06d476b7c647c456d67a18bd6ffcab3f99d460cc4e089733211fba302ef7b6f08d946e5dff9fc9751031718b9383dea634bf7a4e3b629f2436117806b2df6082385d3125acf301cfb0aac614e8bcaf951b9ee99dcee200000000000000000000000000000000000000000000000000000000000000001c7b78ea7427bfc93b613d1f67a6dba97c963c833cac0bb981d1692a7c5fafbf1a3defd214a74d96881fb005b900a646547d8909cba4c18aea60bdd7dc0cb8bb5926e0ea816b68a625e3f198651f1b3fdaa20dfe2563e0e89524df9710dc0ee629000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd381b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011749000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000947ed321302a7ddd18980000000000000000000000000000000000000000000094b508eaddf05c7d189700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ddd2a1d9bb704580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000033c88d533c361f4c2910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6d566c4e7a67354f4331694f4463354c54566d4e6a5174596d4979596930794e7a6c6d4e3249785a6a4579596d596966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000037c9e87c62c9f7ded65b533a575b79ae3ed4ef650000000000000000000000000000000000000000000001e767542e68fef758df0000000000000000000000000000000000000000000001b13f67aac0bc0e5d3800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x922372ccbd55fb431a06d476b7c647c456d67a18bd6ffcab3f99d460cc4e0897",
      "signature": {
        "s": "0x2436117806b2df6082385d3125acf301cfb0aac614e8bcaf951b9ee99dcee200",
        "r": "0x33211fba302ef7b6f08d946e5dff9fc9751031718b9383dea634bf7a4e3b629f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7b78ea7427bfc93b613d1f67a6dba97c963c833cac0bb981d1692a7c5fafbf1a",
      "signature": {
        "s": "0x26e0ea816b68a625e3f198651f1b3fdaa20dfe2563e0e89524df9710dc0ee629",
        "r": "0x3defd214a74d96881fb005b900a646547d8909cba4c18aea60bdd7dc0cb8bb59",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "999000999000999000999",
    "total": "8991008991008991008991"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "999000999000999000999",
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
            "amount": "15283763936904961376913"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "999000999000999000"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZmVlNzg5OC1iODc5LTVmNjQtYmIyYi0yNzlmN2IxZjEyYmYifQ==",
    "nonce": 71497,
    "balances": {
      "current": "701249742711970187778200",
      "previous": "702249742711970187778199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37c9e87c62c9f7ded65b533a575b79ae3ed4ef65",
    "nonce": 10,
    "balances": {
      "current": "8991009991008991008991",
      "previous": "7992008992007992007992"
    }
  },
  "blockNumber": "12400667",
  "created": "2021-05-09T14:26:30.720Z",
  "updated": "2021-05-09T14:26:31.025Z",
  "id": "6097f1160f95a80011b4b0fd"
}
```
* *stageAmount*: `8991009991008991008991`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000003627ec83a842e8fba70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000003627ec83a842e8fba70000000000000000000000000000000000000000000001e76750a0ea5a30d8df922372ccbd55fb431a06d476b7c647c456d67a18bd6ffcab3f99d460cc4e089733211fba302ef7b6f08d946e5dff9fc9751031718b9383dea634bf7a4e3b629f2436117806b2df6082385d3125acf301cfb0aac614e8bcaf951b9ee99dcee200000000000000000000000000000000000000000000000000000000000000001c7b78ea7427bfc93b613d1f67a6dba97c963c833cac0bb981d1692a7c5fafbf1a3defd214a74d96881fb005b900a646547d8909cba4c18aea60bdd7dc0cb8bb5926e0ea816b68a625e3f198651f1b3fdaa20dfe2563e0e89524df9710dc0ee629000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bd381b00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011749000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000947ed321302a7ddd18980000000000000000000000000000000000000000000094b508eaddf05c7d189700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000ddd2a1d9bb704580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000033c88d533c361f4c2910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6d566c4e7a67354f4331694f4463354c54566d4e6a5174596d4979596930794e7a6c6d4e3249785a6a4579596d596966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000037c9e87c62c9f7ded65b533a575b79ae3ed4ef650000000000000000000000000000000000000000000001e767542e68fef758df0000000000000000000000000000000000000000000001b13f67aac0bc0e5d3800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x922372ccbd55fb431a06d476b7c647c456d67a18bd6ffcab3f99d460cc4e0897",
      "signature": {
        "s": "0x2436117806b2df6082385d3125acf301cfb0aac614e8bcaf951b9ee99dcee200",
        "r": "0x33211fba302ef7b6f08d946e5dff9fc9751031718b9383dea634bf7a4e3b629f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7b78ea7427bfc93b613d1f67a6dba97c963c833cac0bb981d1692a7c5fafbf1a",
      "signature": {
        "s": "0x26e0ea816b68a625e3f198651f1b3fdaa20dfe2563e0e89524df9710dc0ee629",
        "r": "0x3defd214a74d96881fb005b900a646547d8909cba4c18aea60bdd7dc0cb8bb59",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "999000999000999000999",
    "total": "8991008991008991008991"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "999000999000999000999",
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
            "amount": "15283763936904961376913"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "999000999000999000"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZmVlNzg5OC1iODc5LTVmNjQtYmIyYi0yNzlmN2IxZjEyYmYifQ==",
    "nonce": 71497,
    "balances": {
      "current": "701249742711970187778200",
      "previous": "702249742711970187778199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37c9e87c62c9f7ded65b533a575b79ae3ed4ef65",
    "nonce": 10,
    "balances": {
      "current": "8991009991008991008991",
      "previous": "7992008992007992007992"
    }
  },
  "blockNumber": "12400667",
  "created": "2021-05-09T14:26:30.720Z",
  "updated": "2021-05-09T14:26:31.025Z",
  "id": "6097f1160f95a80011b4b0fd"
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
0x0f200f9b0000000000000000000000000000000000000000000001e767542e68fef758df0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8991009991008991008991`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`