# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x64EaF5c483DF48F9Fa5c40C89BF7685D53945999`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002b7986321474abda7c00000000000000000000000000000000000000000000000000000007542c159f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000007542c159f00000000000000000000000000000000000000000000001942dba6efb03ad9f34ebac245828bcbbc53d5d8c74122338906a06f6f7d87a68a576a7ef8bc121568866e41c429d704507259bed93524b34c4590c0dffbc5e94b796afe775038a5e02663f7129065b3a6638065ce6ad0b74c5f18360cc428ca22458c5e8a4ddd2ae0000000000000000000000000000000000000000000000000000000000000001bfa19edcdc75d9bd2dd890f0519680971d1a1d3cc079c411b9216dd89c560c0c36c06c052d646e930ed723fa15e7a71d3c51e728fcd3cf37eefc0e0db87fc14dc222d49432c9208b96b23f4d214434aa5cff7839238132c332b4e6c5f3b14177b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b25a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000048eef5ed4de55eae92750000000000000000000000000000000000000000000048eef5ed4decb4baf4e600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001e04cd20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9bb006580bcea455b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325957557a593256695a4330315a5441784c545578597a4174596d4a695a5330775a5451304e446b774e44557a4d6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000064eaf5c483df48f9fa5c40c89bf7685d5394599900000000000000000000000000000000000000000000002b7986321474abda7c00000000000000000000000000000000000000000000002b7986320d207fc4dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4ebac245828bcbbc53d5d8c74122338906a06f6f7d87a68a576a7ef8bc121568",
      "signature": {
        "s": "0x2663f7129065b3a6638065ce6ad0b74c5f18360cc428ca22458c5e8a4ddd2ae0",
        "r": "0x866e41c429d704507259bed93524b34c4590c0dffbc5e94b796afe775038a5e0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa19edcdc75d9bd2dd890f0519680971d1a1d3cc079c411b9216dd89c560c0c3",
      "signature": {
        "s": "0x222d49432c9208b96b23f4d214434aa5cff7839238132c332b4e6c5f3b14177b",
        "r": "0x6c06c052d646e930ed723fa15e7a71d3c51e728fcd3cf37eefc0e0db87fc14dc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31476946335",
    "total": "465986229617525709299"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31476946335",
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
            "amount": "27628250760031890982235"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31476946"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YWUzY2ViZC01ZTAxLTUxYzAtYmJiZS0wZTQ0NDkwNDUzMjkifQ==",
    "nonce": 111194,
    "balances": {
      "current": "344418432761913632789109",
      "previous": "344418432761945141212390"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64eaf5c483df48f9fa5c40c89bf7685d53945999",
    "nonce": 46,
    "balances": {
      "current": "801966736758417382012",
      "previous": "801966736726940435677"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:02.489Z",
  "updated": "2022-05-04T08:57:02.600Z",
  "id": "62723fde7832e20011830cb4"
}
```
* *stageAmount*: `801966736758417382012`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000007542c159f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000007542c159f00000000000000000000000000000000000000000000001942dba6efb03ad9f34ebac245828bcbbc53d5d8c74122338906a06f6f7d87a68a576a7ef8bc121568866e41c429d704507259bed93524b34c4590c0dffbc5e94b796afe775038a5e02663f7129065b3a6638065ce6ad0b74c5f18360cc428ca22458c5e8a4ddd2ae0000000000000000000000000000000000000000000000000000000000000001bfa19edcdc75d9bd2dd890f0519680971d1a1d3cc079c411b9216dd89c560c0c36c06c052d646e930ed723fa15e7a71d3c51e728fcd3cf37eefc0e0db87fc14dc222d49432c9208b96b23f4d214434aa5cff7839238132c332b4e6c5f3b14177b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b25a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000048eef5ed4de55eae92750000000000000000000000000000000000000000000048eef5ed4decb4baf4e600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001e04cd20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9bb006580bcea455b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325957557a593256695a4330315a5441784c545578597a4174596d4a695a5330775a5451304e446b774e44557a4d6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000064eaf5c483df48f9fa5c40c89bf7685d5394599900000000000000000000000000000000000000000000002b7986321474abda7c00000000000000000000000000000000000000000000002b7986320d207fc4dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4ebac245828bcbbc53d5d8c74122338906a06f6f7d87a68a576a7ef8bc121568",
      "signature": {
        "s": "0x2663f7129065b3a6638065ce6ad0b74c5f18360cc428ca22458c5e8a4ddd2ae0",
        "r": "0x866e41c429d704507259bed93524b34c4590c0dffbc5e94b796afe775038a5e0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa19edcdc75d9bd2dd890f0519680971d1a1d3cc079c411b9216dd89c560c0c3",
      "signature": {
        "s": "0x222d49432c9208b96b23f4d214434aa5cff7839238132c332b4e6c5f3b14177b",
        "r": "0x6c06c052d646e930ed723fa15e7a71d3c51e728fcd3cf37eefc0e0db87fc14dc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31476946335",
    "total": "465986229617525709299"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31476946335",
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
            "amount": "27628250760031890982235"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31476946"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YWUzY2ViZC01ZTAxLTUxYzAtYmJiZS0wZTQ0NDkwNDUzMjkifQ==",
    "nonce": 111194,
    "balances": {
      "current": "344418432761913632789109",
      "previous": "344418432761945141212390"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64eaf5c483df48f9fa5c40c89bf7685d53945999",
    "nonce": 46,
    "balances": {
      "current": "801966736758417382012",
      "previous": "801966736726940435677"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:02.489Z",
  "updated": "2022-05-04T08:57:02.600Z",
  "id": "62723fde7832e20011830cb4"
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
0x0f200f9b00000000000000000000000000000000000000000000002b7986321474abda7c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `801966736758417382012`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`