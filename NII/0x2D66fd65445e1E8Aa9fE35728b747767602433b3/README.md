# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2D66fd65445e1E8Aa9fE35728b747767602433b3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000014aa78d216c3202d8400000000000000000000000000000000000000000000000000000003e36ebb8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003e36ebb8e00000000000000000000000000000000000000000000000b00c5c58bd92a55b8bdd1704b0df6466b892be4730047d1df07c6b293b5adee933af568f8f0bf5eee93a3c693907bd12d75d65e21afba65af39438bb9d27c854f576c18c551ae04880f8bea0f21305c47fce8fe3de48deca00e108d2d82fed24b8d7bc2f27fa0b76c000000000000000000000000000000000000000000000000000000000000001b10d24a55469de9c5daf2b5b3f9ce183aa83f60b84ba946b4c0c65148587bc6036a4c06e0fe556a3809457cf2a428455c7e8e5bce25057f3efc2db425d122955b225eed9d580112c1feb92661be9c06352d8fc300b8d90d1296ae4e8696fcad56000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abd8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c192da0118eec3efa54000000000000000000000000000000000000000000009c192da01192d0ac8a8c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000fed4aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47626945d469eb2010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459574a6b4d7a63304e53316b4f544d304c54566a4d445574596a5a6d4d433079597a49314e4451324e44497a5a6d556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002d66fd65445e1e8aa9fe35728b747767602433b3000000000000000000000000000000000000000000000014aa78d216c3202d84000000000000000000000000000000000000000000000014aa78d212dfb171f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbdd1704b0df6466b892be4730047d1df07c6b293b5adee933af568f8f0bf5eee",
      "signature": {
        "s": "0x0f8bea0f21305c47fce8fe3de48deca00e108d2d82fed24b8d7bc2f27fa0b76c",
        "r": "0x93a3c693907bd12d75d65e21afba65af39438bb9d27c854f576c18c551ae0488",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x10d24a55469de9c5daf2b5b3f9ce183aa83f60b84ba946b4c0c65148587bc603",
      "signature": {
        "s": "0x225eed9d580112c1feb92661be9c06352d8fc300b8d90d1296ae4e8696fcad56",
        "r": "0x6a4c06e0fe556a3809457cf2a428455c7e8e5bce25057f3efc2db425d122955b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16700586894",
    "total": "202969852585651623352"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16700586894",
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
            "amount": "27235907908069226361345"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16700586"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YWJkMzc0NS1kOTM0LTVjMDUtYjZmMC0yYzI1NDQ2NDIzZmUifQ==",
    "nonce": 109528,
    "balances": {
      "current": "737153627576540919167572",
      "previous": "737153627576557636455052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d66fd65445e1e8aa9fe35728b747767602433b3",
    "nonce": 46,
    "balances": {
      "current": "381218680453048839556",
      "previous": "381218680436348252662"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:34.226Z",
  "updated": "2022-05-04T08:48:34.299Z",
  "id": "62723de27832e20011830a88"
}
```
* *stageAmount*: `381218680453048839556`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000003e36ebb8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003e36ebb8e00000000000000000000000000000000000000000000000b00c5c58bd92a55b8bdd1704b0df6466b892be4730047d1df07c6b293b5adee933af568f8f0bf5eee93a3c693907bd12d75d65e21afba65af39438bb9d27c854f576c18c551ae04880f8bea0f21305c47fce8fe3de48deca00e108d2d82fed24b8d7bc2f27fa0b76c000000000000000000000000000000000000000000000000000000000000001b10d24a55469de9c5daf2b5b3f9ce183aa83f60b84ba946b4c0c65148587bc6036a4c06e0fe556a3809457cf2a428455c7e8e5bce25057f3efc2db425d122955b225eed9d580112c1feb92661be9c06352d8fc300b8d90d1296ae4e8696fcad56000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abd8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c192da0118eec3efa54000000000000000000000000000000000000000000009c192da01192d0ac8a8c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000fed4aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47626945d469eb2010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459574a6b4d7a63304e53316b4f544d304c54566a4d445574596a5a6d4d433079597a49314e4451324e44497a5a6d556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002d66fd65445e1e8aa9fe35728b747767602433b3000000000000000000000000000000000000000000000014aa78d216c3202d84000000000000000000000000000000000000000000000014aa78d212dfb171f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbdd1704b0df6466b892be4730047d1df07c6b293b5adee933af568f8f0bf5eee",
      "signature": {
        "s": "0x0f8bea0f21305c47fce8fe3de48deca00e108d2d82fed24b8d7bc2f27fa0b76c",
        "r": "0x93a3c693907bd12d75d65e21afba65af39438bb9d27c854f576c18c551ae0488",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x10d24a55469de9c5daf2b5b3f9ce183aa83f60b84ba946b4c0c65148587bc603",
      "signature": {
        "s": "0x225eed9d580112c1feb92661be9c06352d8fc300b8d90d1296ae4e8696fcad56",
        "r": "0x6a4c06e0fe556a3809457cf2a428455c7e8e5bce25057f3efc2db425d122955b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16700586894",
    "total": "202969852585651623352"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16700586894",
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
            "amount": "27235907908069226361345"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16700586"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YWJkMzc0NS1kOTM0LTVjMDUtYjZmMC0yYzI1NDQ2NDIzZmUifQ==",
    "nonce": 109528,
    "balances": {
      "current": "737153627576540919167572",
      "previous": "737153627576557636455052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d66fd65445e1e8aa9fe35728b747767602433b3",
    "nonce": 46,
    "balances": {
      "current": "381218680453048839556",
      "previous": "381218680436348252662"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:34.226Z",
  "updated": "2022-05-04T08:48:34.299Z",
  "id": "62723de27832e20011830a88"
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
0x0f200f9b000000000000000000000000000000000000000000000014aa78d216c3202d840000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `381218680453048839556`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`