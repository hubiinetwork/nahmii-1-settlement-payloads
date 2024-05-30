# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x75fF006263B5Bd121CD2785A43cdc8cA1FB512E9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000d23de8aa9d931ce220000000000000000000000000000000000000000000000000000000290afc92c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000290afc92c000000000000000000000000000000000000000000000006c3efa238b5883f43981203a9d8487b16d29c6e032d20c03ed6b191929e37acfc4d29b5ee8fc761093183ab6c4ff3ddcfce6b30c3dd8335c6df4d009f9a36d7377787eadac9ee8d82470389b0792ad24630d8dcfee668d1da403a8ee78b43cfd5a9648131f8378c67000000000000000000000000000000000000000000000000000000000000001b2213ecb8d5a700d7ca6b8b5703073485e78084a30c12e45c56f2505cec0d1bea648a4bd3b59d160c58164ca8957c7edb956a4cacad2dd92f410823c361d667b41dd19fd20a25076db27d4e374ef1f3148e472ce66d9222cacab65669fc7b5e67000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae32000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096325cc586152cd804ca0000000000000000000000000000000000000000000096325cc58617be2fea9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a81c9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f8887dff8a1263ce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a686d5a6a45324e7930784e4451774c5455784e545574596a6c684f53316b5a6d45325a4455795a546b344d57596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000075ff006263b5bd121cd2785a43cdc8ca1fb512e900000000000000000000000000000000000000000000000d23de8aa9d931ce2200000000000000000000000000000000000000000000000d23de8aa7488204f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x981203a9d8487b16d29c6e032d20c03ed6b191929e37acfc4d29b5ee8fc76109",
      "signature": {
        "s": "0x470389b0792ad24630d8dcfee668d1da403a8ee78b43cfd5a9648131f8378c67",
        "r": "0x3183ab6c4ff3ddcfce6b30c3dd8335c6df4d009f9a36d7377787eadac9ee8d82",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2213ecb8d5a700d7ca6b8b5703073485e78084a30c12e45c56f2505cec0d1bea",
      "signature": {
        "s": "0x1dd19fd20a25076db27d4e374ef1f3148e472ce66d9222cacab65669fc7b5e67",
        "r": "0x648a4bd3b59d160c58164ca8957c7edb956a4cacad2dd92f410823c361d667b4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11017373996",
    "total": "124799146163534577475"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11017373996",
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
            "amount": "27263749699323733107662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11017373"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMjhmZjE2Ny0xNDQwLTUxNTUtYjlhOS1kZmE2ZDUyZTk4MWYifQ==",
    "nonce": 110130,
    "balances": {
      "current": "709283994530779665794250",
      "previous": "709283994530790694185619"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x75ff006263b5bd121cd2785a43cdc8ca1fb512e9",
    "nonce": 46,
    "balances": {
      "current": "242392328656479440418",
      "previous": "242392328645462066422"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:41.647Z",
  "updated": "2022-05-04T08:51:41.749Z",
  "id": "62723e9d7832e20011830b4d"
}
```
* *stageAmount*: `242392328656479440418`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000290afc92c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000290afc92c000000000000000000000000000000000000000000000006c3efa238b5883f43981203a9d8487b16d29c6e032d20c03ed6b191929e37acfc4d29b5ee8fc761093183ab6c4ff3ddcfce6b30c3dd8335c6df4d009f9a36d7377787eadac9ee8d82470389b0792ad24630d8dcfee668d1da403a8ee78b43cfd5a9648131f8378c67000000000000000000000000000000000000000000000000000000000000001b2213ecb8d5a700d7ca6b8b5703073485e78084a30c12e45c56f2505cec0d1bea648a4bd3b59d160c58164ca8957c7edb956a4cacad2dd92f410823c361d667b41dd19fd20a25076db27d4e374ef1f3148e472ce66d9222cacab65669fc7b5e67000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae32000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096325cc586152cd804ca0000000000000000000000000000000000000000000096325cc58617be2fea9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a81c9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f8887dff8a1263ce0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a686d5a6a45324e7930784e4451774c5455784e545574596a6c684f53316b5a6d45325a4455795a546b344d57596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000075ff006263b5bd121cd2785a43cdc8ca1fb512e900000000000000000000000000000000000000000000000d23de8aa9d931ce2200000000000000000000000000000000000000000000000d23de8aa7488204f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x981203a9d8487b16d29c6e032d20c03ed6b191929e37acfc4d29b5ee8fc76109",
      "signature": {
        "s": "0x470389b0792ad24630d8dcfee668d1da403a8ee78b43cfd5a9648131f8378c67",
        "r": "0x3183ab6c4ff3ddcfce6b30c3dd8335c6df4d009f9a36d7377787eadac9ee8d82",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2213ecb8d5a700d7ca6b8b5703073485e78084a30c12e45c56f2505cec0d1bea",
      "signature": {
        "s": "0x1dd19fd20a25076db27d4e374ef1f3148e472ce66d9222cacab65669fc7b5e67",
        "r": "0x648a4bd3b59d160c58164ca8957c7edb956a4cacad2dd92f410823c361d667b4",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11017373996",
    "total": "124799146163534577475"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11017373996",
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
            "amount": "27263749699323733107662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11017373"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjMjhmZjE2Ny0xNDQwLTUxNTUtYjlhOS1kZmE2ZDUyZTk4MWYifQ==",
    "nonce": 110130,
    "balances": {
      "current": "709283994530779665794250",
      "previous": "709283994530790694185619"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x75ff006263b5bd121cd2785a43cdc8ca1fb512e9",
    "nonce": 46,
    "balances": {
      "current": "242392328656479440418",
      "previous": "242392328645462066422"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:41.647Z",
  "updated": "2022-05-04T08:51:41.749Z",
  "id": "62723e9d7832e20011830b4d"
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
0x0f200f9b00000000000000000000000000000000000000000000000d23de8aa9d931ce220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `242392328656479440418`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`