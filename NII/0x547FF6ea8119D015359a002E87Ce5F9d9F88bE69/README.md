# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x547FF6ea8119D015359a002E87Ce5F9d9F88bE69`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000000000000000000000000000000004eb6a6a355c62f091bbea6ffc6f0cbb5ccf998504c358169d08746341542541c9dc02c24d613b58e37b6a07bd29dcf9b5532ede7f595456dc5ad0dd70e349d0c746fbd5b73f9f369f102b2c2e34bf9df98403c18b5c141b5de21d02219c60e5537fba3b160c0a000000000000000000000000000000000000000000000000000000000000001b5e9a69dcd3d112972d544e59eacb218312549a5e4f5e525f03e9f365aa0f2158618e764d95bfacac541fbafe4ca9cf423bf74a3787c56c08c6752fdba8af700475edb0a9d04d2497a04d9c205207157ae339a22aa96b5570db164d7a5859fe6d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e6c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021ed8aa34777f89bcee20000000000000000000000000000000000000000000021ed8aa83424cbe21e4d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000001426910f3090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038ffd8d6a2995a78ba00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a6a4d325a546b79596930324e5451344c54566d4e544d74596a49794e793079596a4933595463354e6a64695a54676966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000547ff6ea8119d015359a002e87ce5f9d9f88be690000000000000000000000000000000000000000000000000004eb6a6a355c62000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf091bbea6ffc6f0cbb5ccf998504c358169d08746341542541c9dc02c24d613b",
      "signature": {
        "s": "0x369f102b2c2e34bf9df98403c18b5c141b5de21d02219c60e5537fba3b160c0a",
        "r": "0x58e37b6a07bd29dcf9b5532ede7f595456dc5ad0dd70e349d0c746fbd5b73f9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5e9a69dcd3d112972d544e59eacb218312549a5e4f5e525f03e9f365aa0f2158",
      "signature": {
        "s": "0x75edb0a9d04d2497a04d9c205207157ae339a22aa96b5570db164d7a5859fe6d",
        "r": "0x618e764d95bfacac541fbafe4ca9cf423bf74a3787c56c08c6752fdba8af7004",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1384742187785314",
    "total": "1384742187785314"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1384742187785314",
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
            "amount": "16823254227139550481312"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1384742187785"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZjM2ZTkyYi02NTQ4LTVmNTMtYjIyNy0yYjI3YTc5NjdiZTgifQ==",
    "nonce": 77420,
    "balances": {
      "current": "160219962187146491317986",
      "previous": "160219963573273421291085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x547ff6ea8119d015359a002e87ce5f9d9f88be69",
    "nonce": 1,
    "balances": {
      "current": "1384742187785314",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:47:02.858Z",
  "updated": "2021-06-04T12:47:02.942Z",
  "id": "60ba20c60779920010014bdb"
}
```
* *stageAmount*: `1384742187785314`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000000000000000000000000000000004eb6a6a355c62f091bbea6ffc6f0cbb5ccf998504c358169d08746341542541c9dc02c24d613b58e37b6a07bd29dcf9b5532ede7f595456dc5ad0dd70e349d0c746fbd5b73f9f369f102b2c2e34bf9df98403c18b5c141b5de21d02219c60e5537fba3b160c0a000000000000000000000000000000000000000000000000000000000000001b5e9a69dcd3d112972d544e59eacb218312549a5e4f5e525f03e9f365aa0f2158618e764d95bfacac541fbafe4ca9cf423bf74a3787c56c08c6752fdba8af700475edb0a9d04d2497a04d9c205207157ae339a22aa96b5570db164d7a5859fe6d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e6c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021ed8aa34777f89bcee20000000000000000000000000000000000000000000021ed8aa83424cbe21e4d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000001426910f3090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038ffd8d6a2995a78ba00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a6a4d325a546b79596930324e5451344c54566d4e544d74596a49794e793079596a4933595463354e6a64695a54676966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000547ff6ea8119d015359a002e87ce5f9d9f88be690000000000000000000000000000000000000000000000000004eb6a6a355c62000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf091bbea6ffc6f0cbb5ccf998504c358169d08746341542541c9dc02c24d613b",
      "signature": {
        "s": "0x369f102b2c2e34bf9df98403c18b5c141b5de21d02219c60e5537fba3b160c0a",
        "r": "0x58e37b6a07bd29dcf9b5532ede7f595456dc5ad0dd70e349d0c746fbd5b73f9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5e9a69dcd3d112972d544e59eacb218312549a5e4f5e525f03e9f365aa0f2158",
      "signature": {
        "s": "0x75edb0a9d04d2497a04d9c205207157ae339a22aa96b5570db164d7a5859fe6d",
        "r": "0x618e764d95bfacac541fbafe4ca9cf423bf74a3787c56c08c6752fdba8af7004",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1384742187785314",
    "total": "1384742187785314"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1384742187785314",
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
            "amount": "16823254227139550481312"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1384742187785"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwZjM2ZTkyYi02NTQ4LTVmNTMtYjIyNy0yYjI3YTc5NjdiZTgifQ==",
    "nonce": 77420,
    "balances": {
      "current": "160219962187146491317986",
      "previous": "160219963573273421291085"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x547ff6ea8119d015359a002e87ce5f9d9f88be69",
    "nonce": 1,
    "balances": {
      "current": "1384742187785314",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:47:02.858Z",
  "updated": "2021-06-04T12:47:02.942Z",
  "id": "60ba20c60779920010014bdb"
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
0x0f200f9b0000000000000000000000000000000000000000000000000004eb6a6a355c620000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1384742187785314`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`