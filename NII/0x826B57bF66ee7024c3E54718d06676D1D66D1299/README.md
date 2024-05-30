# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x826B57bF66ee7024c3E54718d06676D1D66D1299`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001b97105518fcb7233500000000000000000000000000000000000000000000000000000004fbe0d6710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004fbe0d67100000000000000000000000000000000000000000000000f34735926a58bcf68d612e51d0421e37dd3c26b92e9507f4969faab8d349f2252a97627d35fdfa5d2edc5e67f23f2daff4187d58b04335d1b1b41df0c327179b2f5e26761f3285f3564dec6a3e6e8db2c96f9c4f7ceb40a1f584256b0033d99ac731e417c77e25444000000000000000000000000000000000000000000000000000000000000001b4434aaef78a7e84665a8c38130e29d28ff0961cbe42f91164e4f71d06b0ab8dda6be7bfa8cfad46ddaa44e7e09778dec57d9971b2d62772c0b105d872ffcfb0c76775d30fa6e4dbfa59f7bdfca1f714e581090ab2c72ea8e13af42f72a2c4d88000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000dcf81bfb8040a52aa65c00000000000000000000000000000000000000000000dcf81bfb8045a2521cc200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001469ff50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b3df0602394b4b57f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4751324d4445784e43316a5a574a6b4c5455304d544174596a637a4d5330344e4463784e6d55304e444a6c4e54456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000826b57bf66ee7024c3e54718d06676d1d66d129900000000000000000000000000000000000000000000001b97105518fcb7233500000000000000000000000000000000000000000000001b9710551400d64cc400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd612e51d0421e37dd3c26b92e9507f4969faab8d349f2252a97627d35fdfa5d2",
      "signature": {
        "s": "0x64dec6a3e6e8db2c96f9c4f7ceb40a1f584256b0033d99ac731e417c77e25444",
        "r": "0xedc5e67f23f2daff4187d58b04335d1b1b41df0c327179b2f5e26761f3285f35",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4434aaef78a7e84665a8c38130e29d28ff0961cbe42f91164e4f71d06b0ab8dd",
      "signature": {
        "s": "0x76775d30fa6e4dbfa59f7bdfca1f714e581090ab2c72ea8e13af42f72a2c4d88",
        "r": "0xa6be7bfa8cfad46ddaa44e7e09778dec57d9971b2d62772c0b105d872ffcfb0c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "21405685361",
    "total": "280480623640458284904"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21405685361",
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
            "amount": "26929870138307653621752"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21405685"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGQ2MDExNC1jZWJkLTU0MTAtYjczMS04NDcxNmU0NDJlNTEifQ==",
    "nonce": 109453,
    "balances": {
      "current": "1043497435107875231540828",
      "previous": "1043497435107896658631874"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x826b57bf66ee7024c3e54718d06676d1d66d1299",
    "nonce": 46,
    "balances": {
      "current": "508947383855319819061",
      "previous": "508947383833914133700"
    }
  },
  "blockNumber": "14709939",
  "created": "2022-05-04T08:48:10.392Z",
  "updated": "2022-05-04T08:48:10.523Z",
  "id": "62723dca3592fd001130b39b"
}
```
* *stageAmount*: `508947383855319819061`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000004fbe0d6710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004fbe0d67100000000000000000000000000000000000000000000000f34735926a58bcf68d612e51d0421e37dd3c26b92e9507f4969faab8d349f2252a97627d35fdfa5d2edc5e67f23f2daff4187d58b04335d1b1b41df0c327179b2f5e26761f3285f3564dec6a3e6e8db2c96f9c4f7ceb40a1f584256b0033d99ac731e417c77e25444000000000000000000000000000000000000000000000000000000000000001b4434aaef78a7e84665a8c38130e29d28ff0961cbe42f91164e4f71d06b0ab8dda6be7bfa8cfad46ddaa44e7e09778dec57d9971b2d62772c0b105d872ffcfb0c76775d30fa6e4dbfa59f7bdfca1f714e581090ab2c72ea8e13af42f72a2c4d88000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000dcf81bfb8040a52aa65c00000000000000000000000000000000000000000000dcf81bfb8045a2521cc200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001469ff50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b3df0602394b4b57f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334d4751324d4445784e43316a5a574a6b4c5455304d544174596a637a4d5330344e4463784e6d55304e444a6c4e54456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000826b57bf66ee7024c3e54718d06676d1d66d129900000000000000000000000000000000000000000000001b97105518fcb7233500000000000000000000000000000000000000000000001b9710551400d64cc400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd612e51d0421e37dd3c26b92e9507f4969faab8d349f2252a97627d35fdfa5d2",
      "signature": {
        "s": "0x64dec6a3e6e8db2c96f9c4f7ceb40a1f584256b0033d99ac731e417c77e25444",
        "r": "0xedc5e67f23f2daff4187d58b04335d1b1b41df0c327179b2f5e26761f3285f35",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4434aaef78a7e84665a8c38130e29d28ff0961cbe42f91164e4f71d06b0ab8dd",
      "signature": {
        "s": "0x76775d30fa6e4dbfa59f7bdfca1f714e581090ab2c72ea8e13af42f72a2c4d88",
        "r": "0xa6be7bfa8cfad46ddaa44e7e09778dec57d9971b2d62772c0b105d872ffcfb0c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "21405685361",
    "total": "280480623640458284904"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21405685361",
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
            "amount": "26929870138307653621752"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21405685"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3MGQ2MDExNC1jZWJkLTU0MTAtYjczMS04NDcxNmU0NDJlNTEifQ==",
    "nonce": 109453,
    "balances": {
      "current": "1043497435107875231540828",
      "previous": "1043497435107896658631874"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x826b57bf66ee7024c3e54718d06676d1d66d1299",
    "nonce": 46,
    "balances": {
      "current": "508947383855319819061",
      "previous": "508947383833914133700"
    }
  },
  "blockNumber": "14709939",
  "created": "2022-05-04T08:48:10.392Z",
  "updated": "2022-05-04T08:48:10.523Z",
  "id": "62723dca3592fd001130b39b"
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
0x0f200f9b00000000000000000000000000000000000000000000001b97105518fcb723350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `508947383855319819061`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`