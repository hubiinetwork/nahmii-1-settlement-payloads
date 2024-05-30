# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x37234be19d8a698d0764bb0c353dac8309E5cF50`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000488e2c43d4f6e4689f000000000000000000000000000000000000000000000001b85f64dab01721f90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64dab01721f90000000000000000000000000000000000000000000000304548c42c156f7f075b6ea52c4fe4ea8de3800848f230e7bf2293a15ac0c2971898a9d05ab4aa0c402c5f12eee5224a23c4b38cf756d1587cd061f4ce02efb99d75ea0d2a08def75f5b9e7e5781c3a73e95708b71f6fb12eac5625b286d60a2380a74c3061940d419000000000000000000000000000000000000000000000000000000000000001c57d68e2f8f54616988d655ad7f7d2874049a9c987f0f9e9d29696c990680b8152d71604210f00eb4683c2df3e5b511c6507a0cf2ad2a77066fdcb908f05b3d7a05ae66bc3a4538e33f76954db20b0608322d216d1e29c03df8f54d29d05447c5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000d1d721a496c2e8211e2500000000000000000000000000000000000000000000d1d8da74b7e05f90566c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c758164e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b6b7a219795b15641c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a5467334e7a59334f4330784d7a45344c54557a5a4749744f574935597930305a446b345a6d49314e6a5a685a54596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000037234be19d8a698d0764bb0c353dac8309e5cf500000000000000000000000000000000000000000000000488e2c43d4f6e4689f000000000000000000000000000000000000000000000046d5ccdefa46cd46a600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5b6ea52c4fe4ea8de3800848f230e7bf2293a15ac0c2971898a9d05ab4aa0c40",
      "signature": {
        "s": "0x5b9e7e5781c3a73e95708b71f6fb12eac5625b286d60a2380a74c3061940d419",
        "r": "0x2c5f12eee5224a23c4b38cf756d1587cd061f4ce02efb99d75ea0d2a08def75f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57d68e2f8f54616988d655ad7f7d2874049a9c987f0f9e9d29696c990680b815",
      "signature": {
        "s": "0x05ae66bc3a4538e33f76954db20b0608322d216d1e29c03df8f54d29d05447c5",
        "r": "0x2d71604210f00eb4683c2df3e5b511c6507a0cf2ad2a77066fdcb908f05b3d7a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31732192389895758329",
    "total": "890436171418615906055"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389895758329",
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
            "amount": "26982372002427542266908"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389895758"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZTg3NzY3OC0xMzE4LTUzZGItOWI5Yy00ZDk4ZmI1NjZhZTYifQ==",
    "nonce": 109461,
    "balances": {
      "current": "990943069123866697735717",
      "previous": "990974833048448983389804"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37234be19d8a698d0764bb0c353dac8309e5cf50",
    "nonce": 46,
    "balances": {
      "current": "1338410211141403043999",
      "previous": "1306678018751507285670"
    }
  },
  "blockNumber": "14709939",
  "created": "2022-05-04T08:48:12.776Z",
  "updated": "2022-05-04T08:48:13.292Z",
  "id": "62723dcc7832e20011830a6f"
}
```
* *stageAmount*: `1338410211141403043999`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001b85f64dab01721f90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64dab01721f90000000000000000000000000000000000000000000000304548c42c156f7f075b6ea52c4fe4ea8de3800848f230e7bf2293a15ac0c2971898a9d05ab4aa0c402c5f12eee5224a23c4b38cf756d1587cd061f4ce02efb99d75ea0d2a08def75f5b9e7e5781c3a73e95708b71f6fb12eac5625b286d60a2380a74c3061940d419000000000000000000000000000000000000000000000000000000000000001c57d68e2f8f54616988d655ad7f7d2874049a9c987f0f9e9d29696c990680b8152d71604210f00eb4683c2df3e5b511c6507a0cf2ad2a77066fdcb908f05b3d7a05ae66bc3a4538e33f76954db20b0608322d216d1e29c03df8f54d29d05447c5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ab95000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000d1d721a496c2e8211e2500000000000000000000000000000000000000000000d1d8da74b7e05f90566c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c758164e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b6b7a219795b15641c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a5467334e7a59334f4330784d7a45344c54557a5a4749744f574935597930305a446b345a6d49314e6a5a685a54596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000037234be19d8a698d0764bb0c353dac8309e5cf500000000000000000000000000000000000000000000000488e2c43d4f6e4689f000000000000000000000000000000000000000000000046d5ccdefa46cd46a600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5b6ea52c4fe4ea8de3800848f230e7bf2293a15ac0c2971898a9d05ab4aa0c40",
      "signature": {
        "s": "0x5b9e7e5781c3a73e95708b71f6fb12eac5625b286d60a2380a74c3061940d419",
        "r": "0x2c5f12eee5224a23c4b38cf756d1587cd061f4ce02efb99d75ea0d2a08def75f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57d68e2f8f54616988d655ad7f7d2874049a9c987f0f9e9d29696c990680b815",
      "signature": {
        "s": "0x05ae66bc3a4538e33f76954db20b0608322d216d1e29c03df8f54d29d05447c5",
        "r": "0x2d71604210f00eb4683c2df3e5b511c6507a0cf2ad2a77066fdcb908f05b3d7a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31732192389895758329",
    "total": "890436171418615906055"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389895758329",
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
            "amount": "26982372002427542266908"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389895758"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2ZTg3NzY3OC0xMzE4LTUzZGItOWI5Yy00ZDk4ZmI1NjZhZTYifQ==",
    "nonce": 109461,
    "balances": {
      "current": "990943069123866697735717",
      "previous": "990974833048448983389804"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x37234be19d8a698d0764bb0c353dac8309e5cf50",
    "nonce": 46,
    "balances": {
      "current": "1338410211141403043999",
      "previous": "1306678018751507285670"
    }
  },
  "blockNumber": "14709939",
  "created": "2022-05-04T08:48:12.776Z",
  "updated": "2022-05-04T08:48:13.292Z",
  "id": "62723dcc7832e20011830a6f"
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
0x0f200f9b0000000000000000000000000000000000000000000000488e2c43d4f6e4689f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1338410211141403043999`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`