# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x49E8242Bb7F6542f4464CeB9259fF4B8270001de`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000033fb90ef71fe5f3300000000000000000000000000000000000000000000000033fb90ef71fe5f330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000033fb90ef71fe5f3300000000000000000000000000000000000000000000000033fb90ef71fe5f33948e2b071ac43addbc0101c3ccbad1c6f480517140979337022d44f1d48db2993669eee45c762b85aae2c0e7c47a160d6cf9ec7ef3b56c624100305855d58404020dc142d523bbfe5569bfe68af38673b10561a2c3f77218aafb3dcc633b68f8000000000000000000000000000000000000000000000000000000000000001ccdc00c9711e7b3465864bf9e48fe65a9cc7f1e5bd1e502df6947283df7ce75305ea130aff0b2aaec70f910a82698d2f910cfbb6df33e9ef41364faf662717a53269824b9ba0d14ba92e43e9eacf796e03b08f0a5a210e002a2caf7ec43e3f7b2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000984e3800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000009b1c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017c21ad335447075bf390000000000000000000000000000000000000000000017c24edc14f08a3f619600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000d4ebca7cb432a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d28fca79bd424d79a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4756684f57526b595331684e324e694c5455354d474d744f5751795a53316a4e6a4d354f5746684e32526a4d44416966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000049e8242bb7f6542f4464ceb9259ff4b8270001de00000000000000000000000000000000000000000000000033fb90ef71fe5f33000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x948e2b071ac43addbc0101c3ccbad1c6f480517140979337022d44f1d48db299",
      "signature": {
        "s": "0x020dc142d523bbfe5569bfe68af38673b10561a2c3f77218aafb3dcc633b68f8",
        "r": "0x3669eee45c762b85aae2c0e7c47a160d6cf9ec7ef3b56c624100305855d58404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcdc00c9711e7b3465864bf9e48fe65a9cc7f1e5bd1e502df6947283df7ce7530",
      "signature": {
        "s": "0x269824b9ba0d14ba92e43e9eacf796e03b08f0a5a210e002a2caf7ec43e3f7b2",
        "r": "0x5ea130aff0b2aaec70f910a82698d2f910cfbb6df33e9ef41364faf662717a53",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3745746873172778803",
    "total": "3745746873172778803"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3745746873172778803",
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
            "amount": "3884177483225493240229"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3745746873172778"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGVhOWRkYS1hN2NiLTU5MGMtOWQyZS1jNjM5OWFhN2RjMDAifQ==",
    "nonce": 39708,
    "balances": {
      "current": "112195030403534625816377",
      "previous": "112198779896154671767958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49e8242bb7f6542f4464ceb9259ff4b8270001de",
    "nonce": 1,
    "balances": {
      "current": "3745746873172778803",
      "previous": "0"
    }
  },
  "blockNumber": "9981496",
  "created": "2020-05-01T16:53:42.559Z",
  "updated": "2020-05-01T16:53:42.633Z",
  "id": "5eac54166c9eef001169ec34"
}
```
* *stageAmount*: `3745746873172778803`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000033fb90ef71fe5f330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000033fb90ef71fe5f3300000000000000000000000000000000000000000000000033fb90ef71fe5f33948e2b071ac43addbc0101c3ccbad1c6f480517140979337022d44f1d48db2993669eee45c762b85aae2c0e7c47a160d6cf9ec7ef3b56c624100305855d58404020dc142d523bbfe5569bfe68af38673b10561a2c3f77218aafb3dcc633b68f8000000000000000000000000000000000000000000000000000000000000001ccdc00c9711e7b3465864bf9e48fe65a9cc7f1e5bd1e502df6947283df7ce75305ea130aff0b2aaec70f910a82698d2f910cfbb6df33e9ef41364faf662717a53269824b9ba0d14ba92e43e9eacf796e03b08f0a5a210e002a2caf7ec43e3f7b2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000984e3800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000009b1c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017c21ad335447075bf390000000000000000000000000000000000000000000017c24edc14f08a3f619600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000d4ebca7cb432a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d28fca79bd424d79a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4756684f57526b595331684e324e694c5455354d474d744f5751795a53316a4e6a4d354f5746684e32526a4d44416966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000049e8242bb7f6542f4464ceb9259ff4b8270001de00000000000000000000000000000000000000000000000033fb90ef71fe5f33000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x948e2b071ac43addbc0101c3ccbad1c6f480517140979337022d44f1d48db299",
      "signature": {
        "s": "0x020dc142d523bbfe5569bfe68af38673b10561a2c3f77218aafb3dcc633b68f8",
        "r": "0x3669eee45c762b85aae2c0e7c47a160d6cf9ec7ef3b56c624100305855d58404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcdc00c9711e7b3465864bf9e48fe65a9cc7f1e5bd1e502df6947283df7ce7530",
      "signature": {
        "s": "0x269824b9ba0d14ba92e43e9eacf796e03b08f0a5a210e002a2caf7ec43e3f7b2",
        "r": "0x5ea130aff0b2aaec70f910a82698d2f910cfbb6df33e9ef41364faf662717a53",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3745746873172778803",
    "total": "3745746873172778803"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3745746873172778803",
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
            "amount": "3884177483225493240229"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3745746873172778"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGVhOWRkYS1hN2NiLTU5MGMtOWQyZS1jNjM5OWFhN2RjMDAifQ==",
    "nonce": 39708,
    "balances": {
      "current": "112195030403534625816377",
      "previous": "112198779896154671767958"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x49e8242bb7f6542f4464ceb9259ff4b8270001de",
    "nonce": 1,
    "balances": {
      "current": "3745746873172778803",
      "previous": "0"
    }
  },
  "blockNumber": "9981496",
  "created": "2020-05-01T16:53:42.559Z",
  "updated": "2020-05-01T16:53:42.633Z",
  "id": "5eac54166c9eef001169ec34"
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
0x0f200f9b00000000000000000000000000000000000000000000000033fb90ef71fe5f330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3745746873172778803`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`