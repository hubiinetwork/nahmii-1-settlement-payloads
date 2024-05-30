# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xded490b47323B4020f1f5D196ab11b9509491277`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000fe7ce9f648e9132e000000000000000000000000000000000000000000000000c8c35c4d3d5d4b720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000c8c35c4d3d5d4b72000000000000000000000000000000000000000000000000fe7ce9f648e9132e27e9249d929e92c534175b24dbf0ae3d913d774cd66754e8fb8562f07d2facac6006b6c894735321c0e0a9e9dd49f1a8a80a6b636555dda0ec43ee1640dd3a9932199f292ff9b53928f347b5f1a8a8063c2f05ca662a1cddbba7d7f2eacbff36000000000000000000000000000000000000000000000000000000000000001b66a640567ed7535417069d656d4bc525ec72898ef784323a032c943e1e3155e6df4aa3bf0a57a1348406751726a101ef6b4bed4f14cf4dda3e4d762082aa170e261677a39cbc4cd182fffde9dd5dbc933f589105790bc78a5ad5e96e9ed1f227000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021d641aa1b5453c0b9e70000000000000000000000000000000000000000000021d70aa0dcd7ea85cb4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003365365967c5f60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c62b6e69e6575293c90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6a67354d4446685a533168596a41334c545532597a6b74596d597a4f43316a5a6d5a6b4f5463774e6a4a6a596a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000ded490b47323b4020f1f5d196ab11b9509491277000000000000000000000000000000000000000000000000fe7ce9f648e9132e00000000000000000000000000000000000000000000000035b98da90b8bc7bc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27e9249d929e92c534175b24dbf0ae3d913d774cd66754e8fb8562f07d2facac",
      "signature": {
        "s": "0x32199f292ff9b53928f347b5f1a8a8063c2f05ca662a1cddbba7d7f2eacbff36",
        "r": "0x6006b6c894735321c0e0a9e9dd49f1a8a80a6b636555dda0ec43ee1640dd3a99",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x66a640567ed7535417069d656d4bc525ec72898ef784323a032c943e1e3155e6",
      "signature": {
        "s": "0x261677a39cbc4cd182fffde9dd5dbc933f589105790bc78a5ad5e96e9ed1f227",
        "r": "0xdf4aa3bf0a57a1348406751726a101ef6b4bed4f14cf4dda3e4d762082aa170e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14466507914855926642",
    "total": "18337789026740278062"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14466507914855926642",
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
            "amount": "17822684330432524358601"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14466507914855926"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Zjg5MDFhZS1hYjA3LTU2YzktYmYzOC1jZmZkOTcwNjJjYjMifQ==",
    "nonce": 80533,
    "balances": {
      "current": "159790428790879638567399",
      "previous": "159804909765302409349967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xded490b47323b4020f1f5d196ab11b9509491277",
    "nonce": 2,
    "balances": {
      "current": "18337789026740278062",
      "previous": "3871281111884351420"
    }
  },
  "blockNumber": "12767129",
  "created": "2021-07-05T11:15:55.935Z",
  "updated": "2021-07-05T11:15:56.014Z",
  "id": "60e2e9ebf2deeb00101fcb5a"
}
```
* *stageAmount*: `18337789026740278062`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000c8c35c4d3d5d4b720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000c8c35c4d3d5d4b72000000000000000000000000000000000000000000000000fe7ce9f648e9132e27e9249d929e92c534175b24dbf0ae3d913d774cd66754e8fb8562f07d2facac6006b6c894735321c0e0a9e9dd49f1a8a80a6b636555dda0ec43ee1640dd3a9932199f292ff9b53928f347b5f1a8a8063c2f05ca662a1cddbba7d7f2eacbff36000000000000000000000000000000000000000000000000000000000000001b66a640567ed7535417069d656d4bc525ec72898ef784323a032c943e1e3155e6df4aa3bf0a57a1348406751726a101ef6b4bed4f14cf4dda3e4d762082aa170e261677a39cbc4cd182fffde9dd5dbc933f589105790bc78a5ad5e96e9ed1f227000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021d641aa1b5453c0b9e70000000000000000000000000000000000000000000021d70aa0dcd7ea85cb4f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003365365967c5f60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c62b6e69e6575293c90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6a67354d4446685a533168596a41334c545532597a6b74596d597a4f43316a5a6d5a6b4f5463774e6a4a6a596a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000ded490b47323b4020f1f5d196ab11b9509491277000000000000000000000000000000000000000000000000fe7ce9f648e9132e00000000000000000000000000000000000000000000000035b98da90b8bc7bc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27e9249d929e92c534175b24dbf0ae3d913d774cd66754e8fb8562f07d2facac",
      "signature": {
        "s": "0x32199f292ff9b53928f347b5f1a8a8063c2f05ca662a1cddbba7d7f2eacbff36",
        "r": "0x6006b6c894735321c0e0a9e9dd49f1a8a80a6b636555dda0ec43ee1640dd3a99",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x66a640567ed7535417069d656d4bc525ec72898ef784323a032c943e1e3155e6",
      "signature": {
        "s": "0x261677a39cbc4cd182fffde9dd5dbc933f589105790bc78a5ad5e96e9ed1f227",
        "r": "0xdf4aa3bf0a57a1348406751726a101ef6b4bed4f14cf4dda3e4d762082aa170e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14466507914855926642",
    "total": "18337789026740278062"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14466507914855926642",
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
            "amount": "17822684330432524358601"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "14466507914855926"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Zjg5MDFhZS1hYjA3LTU2YzktYmYzOC1jZmZkOTcwNjJjYjMifQ==",
    "nonce": 80533,
    "balances": {
      "current": "159790428790879638567399",
      "previous": "159804909765302409349967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xded490b47323b4020f1f5d196ab11b9509491277",
    "nonce": 2,
    "balances": {
      "current": "18337789026740278062",
      "previous": "3871281111884351420"
    }
  },
  "blockNumber": "12767129",
  "created": "2021-07-05T11:15:55.935Z",
  "updated": "2021-07-05T11:15:56.014Z",
  "id": "60e2e9ebf2deeb00101fcb5a"
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
0x0f200f9b000000000000000000000000000000000000000000000000fe7ce9f648e9132e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18337789026740278062`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`