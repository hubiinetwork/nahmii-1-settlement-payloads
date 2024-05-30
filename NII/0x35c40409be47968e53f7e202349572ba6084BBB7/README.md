# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x35c40409be47968e53f7e202349572ba6084BBB7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000007461c8eab24f127b7c00000000000000000000000000000000000000000000000210aad71b258637b80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000210aad71b258637b8000000000000000000000000000000000000000000000048ab62bff0c83f5dd5de4bdea46393fd14bd36fd71f43dc977b1c794f607e1edd78796b7936cce5bad309defdc190f7d34a54b7b1e61e7198e58d1e2712afd082c6353e6fe48cba8661ec287ee011199f1c9f843145a9cbce25fb6e29954062415be17ee59907db833000000000000000000000000000000000000000000000000000000000000001c53383c7e2e567afd1c5aca46c597d7b449c5d842e7a0ae4c16a3a9978d37b74e6c430d6c0a75c73b20a177f4a58dfd9f095d62392aed8432f4ebab67fab064db36df49f0fd0e379482aeccf09506926611bee3394d28fba799acf6c04c3270a1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aff8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ff6ae7e725083b6d4b9000000000000000000000000000000000000000000004ff8bfb0a029e56f9d6400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000008756be3c3290f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7eebbb6481c86c8750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934597a5a684e6a6b345a53316d597a63774c5455794e5751744f54526a595330305a6a51774e5455324d545579596d556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000035c40409be47968e53f7e202349572ba6084bbb700000000000000000000000000000000000000000000007461c8eab24f127b7c000000000000000000000000000000000000000000000072511e1397298c43c400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde4bdea46393fd14bd36fd71f43dc977b1c794f607e1edd78796b7936cce5bad",
      "signature": {
        "s": "0x1ec287ee011199f1c9f843145a9cbce25fb6e29954062415be17ee59907db833",
        "r": "0x309defdc190f7d34a54b7b1e61e7198e58d1e2712afd082c6353e6fe48cba866",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x53383c7e2e567afd1c5aca46c597d7b449c5d842e7a0ae4c16a3a9978d37b74e",
      "signature": {
        "s": "0x36df49f0fd0e379482aeccf09506926611bee3394d28fba799acf6c04c3270a1",
        "r": "0x6c430d6c0a75c73b20a177f4a58dfd9f095d62392aed8432f4ebab67fab064db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "38094496909660403640",
    "total": "1340515217476163689941"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38094496909660403640",
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
            "amount": "27595084933818283903093"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "38094496909660403"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YzZhNjk4ZS1mYzcwLTUyNWQtOTRjYS00ZjQwNTU2MTUyYmUifQ==",
    "nonce": 110584,
    "balances": {
      "current": "377617424801734319330489",
      "previous": "377655557393140889394532"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x35c40409be47968e53f7e202349572ba6084bbb7",
    "nonce": 46,
    "balances": {
      "current": "2146868452218880818044",
      "previous": "2108773955309220414404"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:54:01.147Z",
  "updated": "2022-05-04T08:54:01.257Z",
  "id": "62723f29bbd75600116d059f"
}
```
* *stageAmount*: `2146868452218880818044`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000210aad71b258637b80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000210aad71b258637b8000000000000000000000000000000000000000000000048ab62bff0c83f5dd5de4bdea46393fd14bd36fd71f43dc977b1c794f607e1edd78796b7936cce5bad309defdc190f7d34a54b7b1e61e7198e58d1e2712afd082c6353e6fe48cba8661ec287ee011199f1c9f843145a9cbce25fb6e29954062415be17ee59907db833000000000000000000000000000000000000000000000000000000000000001c53383c7e2e567afd1c5aca46c597d7b449c5d842e7a0ae4c16a3a9978d37b74e6c430d6c0a75c73b20a177f4a58dfd9f095d62392aed8432f4ebab67fab064db36df49f0fd0e379482aeccf09506926611bee3394d28fba799acf6c04c3270a1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aff8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004ff6ae7e725083b6d4b9000000000000000000000000000000000000000000004ff8bfb0a029e56f9d6400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000008756be3c3290f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7eebbb6481c86c8750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934597a5a684e6a6b345a53316d597a63774c5455794e5751744f54526a595330305a6a51774e5455324d545579596d556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000035c40409be47968e53f7e202349572ba6084bbb700000000000000000000000000000000000000000000007461c8eab24f127b7c000000000000000000000000000000000000000000000072511e1397298c43c400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xde4bdea46393fd14bd36fd71f43dc977b1c794f607e1edd78796b7936cce5bad",
      "signature": {
        "s": "0x1ec287ee011199f1c9f843145a9cbce25fb6e29954062415be17ee59907db833",
        "r": "0x309defdc190f7d34a54b7b1e61e7198e58d1e2712afd082c6353e6fe48cba866",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x53383c7e2e567afd1c5aca46c597d7b449c5d842e7a0ae4c16a3a9978d37b74e",
      "signature": {
        "s": "0x36df49f0fd0e379482aeccf09506926611bee3394d28fba799acf6c04c3270a1",
        "r": "0x6c430d6c0a75c73b20a177f4a58dfd9f095d62392aed8432f4ebab67fab064db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "38094496909660403640",
    "total": "1340515217476163689941"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38094496909660403640",
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
            "amount": "27595084933818283903093"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "38094496909660403"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YzZhNjk4ZS1mYzcwLTUyNWQtOTRjYS00ZjQwNTU2MTUyYmUifQ==",
    "nonce": 110584,
    "balances": {
      "current": "377617424801734319330489",
      "previous": "377655557393140889394532"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x35c40409be47968e53f7e202349572ba6084bbb7",
    "nonce": 46,
    "balances": {
      "current": "2146868452218880818044",
      "previous": "2108773955309220414404"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:54:01.147Z",
  "updated": "2022-05-04T08:54:01.257Z",
  "id": "62723f29bbd75600116d059f"
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
0x0f200f9b00000000000000000000000000000000000000000000007461c8eab24f127b7c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2146868452218880818044`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`