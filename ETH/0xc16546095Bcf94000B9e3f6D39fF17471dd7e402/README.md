# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc16546095Bcf94000B9e3f6D39fF17471dd7e402`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000097200000000000000000000000000000000000000000000000000000000000009720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000097200000000000000000000000000000000000000000000000000000000000009728460efe9d5550b45b8357631807b183c88bfd4be9588f2688dd3a26abafde554b8db6381025c4e2ec7ab631c966244d46139493d47d51756061f41b9584d21513ca6b199239c5702528f9926714519f3c79e4b351a05ac42b499f4df28778d6d000000000000000000000000000000000000000000000000000000000000001ca65edb4e89aa1152d8bb5c41794f363129525662660c35fa60aa726b70167427153bab319213cc13696af85ac660f92493db814dd1e78aa3df1c87a2b054bbba2cee2ce4b458ef44db77345d740d33f413273c3eb534eef6ec824918d7e161d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a4de3000000000000000000000000000000000000000000000000002386f2c74a575700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009623d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4749354e445a6d4e53316b4f474a6d4c54566a5a446b744f44686c4e6931694d7a4a695a6d4933596a67354d7a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000c16546095bcf94000b9e3f6d39ff17471dd7e4020000000000000000000000000000000000000000000000000000000000000972000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8460efe9d5550b45b8357631807b183c88bfd4be9588f2688dd3a26abafde554",
      "signature": {
        "s": "0x3ca6b199239c5702528f9926714519f3c79e4b351a05ac42b499f4df28778d6d",
        "r": "0xb8db6381025c4e2ec7ab631c966244d46139493d47d51756061f41b9584d2151",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa65edb4e89aa1152d8bb5c41794f363129525662660c35fa60aa726b70167427",
      "signature": {
        "s": "0x2cee2ce4b458ef44db77345d740d33f413273c3eb534eef6ec824918d7e161d1",
        "r": "0x153bab319213cc13696af85ac660f92493db814dd1e78aa3df1c87a2b054bbba",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2418",
    "total": "2418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2418",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "614973"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGI5NDZmNS1kOGJmLTVjZDktODhlNi1iMzJiZmI3Yjg5MzUifQ==",
    "nonce": 1358,
    "balances": {
      "current": "10000001468616163",
      "previous": "10000001468618583"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc16546095bcf94000b9e3f6d39ff17471dd7e402",
    "nonce": 20,
    "balances": {
      "current": "2418",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:46.630Z",
  "updated": "2020-05-22T08:08:46.701Z",
  "id": "5ec7888eb0c6090011d5aa91"
}
```
* *stageAmount*: `2418`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000009720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000097200000000000000000000000000000000000000000000000000000000000009728460efe9d5550b45b8357631807b183c88bfd4be9588f2688dd3a26abafde554b8db6381025c4e2ec7ab631c966244d46139493d47d51756061f41b9584d21513ca6b199239c5702528f9926714519f3c79e4b351a05ac42b499f4df28778d6d000000000000000000000000000000000000000000000000000000000000001ca65edb4e89aa1152d8bb5c41794f363129525662660c35fa60aa726b70167427153bab319213cc13696af85ac660f92493db814dd1e78aa3df1c87a2b054bbba2cee2ce4b458ef44db77345d740d33f413273c3eb534eef6ec824918d7e161d1000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a4de3000000000000000000000000000000000000000000000000002386f2c74a575700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009623d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4749354e445a6d4e53316b4f474a6d4c54566a5a446b744f44686c4e6931694d7a4a695a6d4933596a67354d7a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000c16546095bcf94000b9e3f6d39ff17471dd7e4020000000000000000000000000000000000000000000000000000000000000972000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8460efe9d5550b45b8357631807b183c88bfd4be9588f2688dd3a26abafde554",
      "signature": {
        "s": "0x3ca6b199239c5702528f9926714519f3c79e4b351a05ac42b499f4df28778d6d",
        "r": "0xb8db6381025c4e2ec7ab631c966244d46139493d47d51756061f41b9584d2151",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa65edb4e89aa1152d8bb5c41794f363129525662660c35fa60aa726b70167427",
      "signature": {
        "s": "0x2cee2ce4b458ef44db77345d740d33f413273c3eb534eef6ec824918d7e161d1",
        "r": "0x153bab319213cc13696af85ac660f92493db814dd1e78aa3df1c87a2b054bbba",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2418",
    "total": "2418"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2418",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "614973"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2ZGI5NDZmNS1kOGJmLTVjZDktODhlNi1iMzJiZmI3Yjg5MzUifQ==",
    "nonce": 1358,
    "balances": {
      "current": "10000001468616163",
      "previous": "10000001468618583"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc16546095bcf94000b9e3f6d39ff17471dd7e402",
    "nonce": 20,
    "balances": {
      "current": "2418",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:46.630Z",
  "updated": "2020-05-22T08:08:46.701Z",
  "id": "5ec7888eb0c6090011d5aa91"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000009720000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2418`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``