# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9Af41c3f89FED7C6db78Fa2920A3EeB1617a3bb8`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de412634b2b119700000000000000000000000000000000000000000000000a3d839d2a374a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000a3d839d2a374a000000000000000000000000000000000000000000000000000a3d839d2a374a00006fa1d0fbc248b3e7ac784419e2e58ba5b6b4303b6aa5d1eeeebae19d8e72ae0aa43281895a0f58c769ae96c528d066d35e99ded1aa7cdb8d448c13e02ba9b85070c4c0ee4bbfaf58d3017d7b1be2edf3ea7b185589228cec173053871c1d465d000000000000000000000000000000000000000000000000000000000000001cd5c8e55f41eacee7bfeba2bc642b533e082b176fe624b0b10040fa8addaead1d4b944339f3e2328e8dd205266480427443ac3367658038e0b9aa7ee170087bd15271e9e515a86a4014aa2ad17f005b8af3c4b73f60d2789009f00dfe7a6b3f58000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1d83b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000009af41c3f89fed7c6db78fa2920a3eeb1617a3bb80000000000000000000000000000000000000000000000000de412634b2b119700000000000000000000000000000000000000000000000a4e06cb1a1887519700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000029f1b8c961240000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000029f1b8c961240000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e546c6c5a6a4a695a69316d596a67354c54526d5a6d5974596a457a596930334e544979596d493459545a6d4e47496966513d3d0000000000000000000000000000000000000000000000000000000000000037000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000026c0e836f32b4f3026680000000000000000000000000000000000000000000026b6aab3560117e6266800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6fa1d0fbc248b3e7ac784419e2e58ba5b6b4303b6aa5d1eeeebae19d8e72ae0a",
      "signature": {
        "s": "0x70c4c0ee4bbfaf58d3017d7b1be2edf3ea7b185589228cec173053871c1d465d",
        "r": "0xa43281895a0f58c769ae96c528d066d35e99ded1aa7cdb8d448c13e02ba9b850",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd5c8e55f41eacee7bfeba2bc642b533e082b176fe624b0b10040fa8addaead1d",
      "signature": {
        "s": "0x5271e9e515a86a4014aa2ad17f005b8af3c4b73f60d2789009f00dfe7a6b3f58",
        "r": "0x4b944339f3e2328e8dd205266480427443ac3367658038e0b9aa7ee170087bd1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "188900000000000000000",
    "total": "188900000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "188900000000000000000",
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
            "amount": "188900000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "188900000000000000"
      }
    },
    "wallet": "0x9af41c3f89fed7c6db78fa2920a3eeb1617a3bb8",
    "data": "eyJyZWYiOiIyNTllZjJiZi1mYjg5LTRmZmYtYjEzYi03NTIyYmI4YTZmNGIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000945234855268759",
      "previous": "190089845234855268759"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 55,
    "balances": {
      "current": "183008434040031631386216",
      "previous": "182819534040031631386216"
    }
  },
  "blockNumber": "14800955",
  "created": "2022-05-18T20:46:25.114Z",
  "updated": "2022-05-18T20:46:25.227Z",
  "id": "62855b21bbd75600116d08b1"
}
```
* *stageAmount*: `1000945234855268759`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000a3d839d2a374a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000a3d839d2a374a000000000000000000000000000000000000000000000000000a3d839d2a374a00006fa1d0fbc248b3e7ac784419e2e58ba5b6b4303b6aa5d1eeeebae19d8e72ae0aa43281895a0f58c769ae96c528d066d35e99ded1aa7cdb8d448c13e02ba9b85070c4c0ee4bbfaf58d3017d7b1be2edf3ea7b185589228cec173053871c1d465d000000000000000000000000000000000000000000000000000000000000001cd5c8e55f41eacee7bfeba2bc642b533e082b176fe624b0b10040fa8addaead1d4b944339f3e2328e8dd205266480427443ac3367658038e0b9aa7ee170087bd15271e9e515a86a4014aa2ad17f005b8af3c4b73f60d2789009f00dfe7a6b3f58000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1d83b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000009af41c3f89fed7c6db78fa2920a3eeb1617a3bb80000000000000000000000000000000000000000000000000de412634b2b119700000000000000000000000000000000000000000000000a4e06cb1a1887519700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000029f1b8c961240000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000029f1b8c961240000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e546c6c5a6a4a695a69316d596a67354c54526d5a6d5974596a457a596930334e544979596d493459545a6d4e47496966513d3d0000000000000000000000000000000000000000000000000000000000000037000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000026c0e836f32b4f3026680000000000000000000000000000000000000000000026b6aab3560117e6266800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6fa1d0fbc248b3e7ac784419e2e58ba5b6b4303b6aa5d1eeeebae19d8e72ae0a",
      "signature": {
        "s": "0x70c4c0ee4bbfaf58d3017d7b1be2edf3ea7b185589228cec173053871c1d465d",
        "r": "0xa43281895a0f58c769ae96c528d066d35e99ded1aa7cdb8d448c13e02ba9b850",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd5c8e55f41eacee7bfeba2bc642b533e082b176fe624b0b10040fa8addaead1d",
      "signature": {
        "s": "0x5271e9e515a86a4014aa2ad17f005b8af3c4b73f60d2789009f00dfe7a6b3f58",
        "r": "0x4b944339f3e2328e8dd205266480427443ac3367658038e0b9aa7ee170087bd1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "188900000000000000000",
    "total": "188900000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "188900000000000000000",
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
            "amount": "188900000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "188900000000000000"
      }
    },
    "wallet": "0x9af41c3f89fed7c6db78fa2920a3eeb1617a3bb8",
    "data": "eyJyZWYiOiIyNTllZjJiZi1mYjg5LTRmZmYtYjEzYi03NTIyYmI4YTZmNGIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000945234855268759",
      "previous": "190089845234855268759"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 55,
    "balances": {
      "current": "183008434040031631386216",
      "previous": "182819534040031631386216"
    }
  },
  "blockNumber": "14800955",
  "created": "2022-05-18T20:46:25.114Z",
  "updated": "2022-05-18T20:46:25.227Z",
  "id": "62855b21bbd75600116d08b1"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de412634b2b11970000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000945234855268759`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`