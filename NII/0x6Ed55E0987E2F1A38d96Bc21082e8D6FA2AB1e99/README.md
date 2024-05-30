# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6Ed55E0987E2F1A38d96Bc21082e8D6FA2AB1e99`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000029c81977a16d23d677000000000000000000000000000000000000000000000001d7c5e2a9a9ea70770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001d7c5e2a9a9ea7077000000000000000000000000000000000000000000000029c81977a16d23d677144c711b84047d978d6ac62917794aa9641a68f8430d0e17e4a68dcd09ee20e084803287608409ada3edc05b68f1743db2189bb765dec6036ab5f3ad5bf759c764399591c48aa691891b9c6f2e56f00589421ec3b3dd7aab64791c3c7136564b000000000000000000000000000000000000000000000000000000000000001bc0a31a82956b68f9aa2f884dbb2ee7a74b7ce3ca4a3bad99d43314737a57546a872e969751e872b3925d5c20eba5512258999d738b6395320ddd49eb29b82eb608963ad463bd3c202fa4a39dd52db03d4b217d19a7403b6912b4f74268f5e53d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000adaa0b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000e797000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023576b742f3ab9958d4200000000000000000000000000000000000000000000235943b2d801be09b29200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000078c61d5a89b4d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024ab175f8f13c856b9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a46694f4451795a5330355a6d51784c5455355a474d744f546b304d5330324e6a6b304f47466d597a45354d54516966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000006ed55e0987e2f1a38d96bc21082e8d6fa2ab1e99000000000000000000000000000000000000000000000029c81977a16d23d677000000000000000000000000000000000000000000000027f05394f7c339660000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x144c711b84047d978d6ac62917794aa9641a68f8430d0e17e4a68dcd09ee20e0",
      "signature": {
        "s": "0x64399591c48aa691891b9c6f2e56f00589421ec3b3dd7aab64791c3c7136564b",
        "r": "0x84803287608409ada3edc05b68f1743db2189bb765dec6036ab5f3ad5bf759c7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc0a31a82956b68f9aa2f884dbb2ee7a74b7ce3ca4a3bad99d43314737a57546a",
      "signature": {
        "s": "0x08963ad463bd3c202fa4a39dd52db03d4b217d19a7403b6912b4f74268f5e53d",
        "r": "0x872e969751e872b3925d5c20eba5512258999d738b6395320ddd49eb29b82eb6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "33994826580604121207",
    "total": "770735194239299475063"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33994826580604121207",
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
            "amount": "10822579427625771821980"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "33994826580604121"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzFiODQyZS05ZmQxLTU5ZGMtOTk0MS02Njk0OGFmYzE5MTQifQ==",
    "nonce": 59287,
    "balances": {
      "current": "166895436500438938389826",
      "previous": "166929465321846123115154"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6ed55e0987e2f1a38d96bc21082e8d6fa2ab1e99",
    "nonce": 3,
    "balances": {
      "current": "770735194239299475063",
      "previous": "736740367658695353856"
    }
  },
  "blockNumber": "11381259",
  "created": "2020-12-03T18:25:38.444Z",
  "updated": "2020-12-03T18:25:38.521Z",
  "id": "5fc92da25ca34d0011dac461"
}
```
* *stageAmount*: `770735194239299475063`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001d7c5e2a9a9ea70770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001d7c5e2a9a9ea7077000000000000000000000000000000000000000000000029c81977a16d23d677144c711b84047d978d6ac62917794aa9641a68f8430d0e17e4a68dcd09ee20e084803287608409ada3edc05b68f1743db2189bb765dec6036ab5f3ad5bf759c764399591c48aa691891b9c6f2e56f00589421ec3b3dd7aab64791c3c7136564b000000000000000000000000000000000000000000000000000000000000001bc0a31a82956b68f9aa2f884dbb2ee7a74b7ce3ca4a3bad99d43314737a57546a872e969751e872b3925d5c20eba5512258999d738b6395320ddd49eb29b82eb608963ad463bd3c202fa4a39dd52db03d4b217d19a7403b6912b4f74268f5e53d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000adaa0b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000e797000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023576b742f3ab9958d4200000000000000000000000000000000000000000000235943b2d801be09b29200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000078c61d5a89b4d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024ab175f8f13c856b9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a46694f4451795a5330355a6d51784c5455355a474d744f546b304d5330324e6a6b304f47466d597a45354d54516966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000006ed55e0987e2f1a38d96bc21082e8d6fa2ab1e99000000000000000000000000000000000000000000000029c81977a16d23d677000000000000000000000000000000000000000000000027f05394f7c339660000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x144c711b84047d978d6ac62917794aa9641a68f8430d0e17e4a68dcd09ee20e0",
      "signature": {
        "s": "0x64399591c48aa691891b9c6f2e56f00589421ec3b3dd7aab64791c3c7136564b",
        "r": "0x84803287608409ada3edc05b68f1743db2189bb765dec6036ab5f3ad5bf759c7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc0a31a82956b68f9aa2f884dbb2ee7a74b7ce3ca4a3bad99d43314737a57546a",
      "signature": {
        "s": "0x08963ad463bd3c202fa4a39dd52db03d4b217d19a7403b6912b4f74268f5e53d",
        "r": "0x872e969751e872b3925d5c20eba5512258999d738b6395320ddd49eb29b82eb6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "33994826580604121207",
    "total": "770735194239299475063"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33994826580604121207",
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
            "amount": "10822579427625771821980"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "33994826580604121"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzFiODQyZS05ZmQxLTU5ZGMtOTk0MS02Njk0OGFmYzE5MTQifQ==",
    "nonce": 59287,
    "balances": {
      "current": "166895436500438938389826",
      "previous": "166929465321846123115154"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6ed55e0987e2f1a38d96bc21082e8d6fa2ab1e99",
    "nonce": 3,
    "balances": {
      "current": "770735194239299475063",
      "previous": "736740367658695353856"
    }
  },
  "blockNumber": "11381259",
  "created": "2020-12-03T18:25:38.444Z",
  "updated": "2020-12-03T18:25:38.521Z",
  "id": "5fc92da25ca34d0011dac461"
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
0x0f200f9b000000000000000000000000000000000000000000000029c81977a16d23d6770000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `770735194239299475063`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`