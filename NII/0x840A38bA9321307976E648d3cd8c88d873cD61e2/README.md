# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x840A38bA9321307976E648d3cd8c88d873cD61e2`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000a58cb71f27f1000000000000000000000000000000000000000000000000000003eccc80e7150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000003eccc80e71500000000000000000000000000000000000000000000000000006e23a1e9010107cba29e512a5950cc12c19324d20fa0ededacac87325b78c0113dbf4404a17745a15b1bee45da1920e91018f2bbf0218de5dd88003b3686f75c1db68bf7854423a59e93f8b12a392be6e12ca5b0d6ceb5b01f33d483b532fae48e4c79d06bc4000000000000000000000000000000000000000000000000000000000000001b895b6e8254d85174c67080059a0323ec11012f3f2f2683c580650cd51ae7eccaf9e7e9cd08bc9bf1347917784fac9cef5d55d4285d1398b1d59ae5328ad7c16637012ef04cc2266f51597322c50dc9a2dd8e444b53f6d0bc71dd329750c407e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af82000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000054927ad5d32523cbd8b70000000000000000000000000000000000000000000054927ad5d712f1873f0100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001013a7f350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6c101b2dc3b0e4eb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a6b774d7a68695a6931694d4756684c545669597a59744f54686c5a6930344e57466a4f5441324f546b344e7a516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000840a38ba9321307976e648d3cd8c88d873cd61e20000000000000000000000000000000000000000000000000000a58cb71f27f10000000000000000000000000000000000000000000000000000a19fea9e40dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x07cba29e512a5950cc12c19324d20fa0ededacac87325b78c0113dbf4404a177",
      "signature": {
        "s": "0x23a59e93f8b12a392be6e12ca5b0d6ceb5b01f33d483b532fae48e4c79d06bc4",
        "r": "0x45a15b1bee45da1920e91018f2bbf0218de5dd88003b3686f75c1db68bf78544",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x895b6e8254d85174c67080059a0323ec11012f3f2f2683c580650cd51ae7ecca",
      "signature": {
        "s": "0x37012ef04cc2266f51597322c50dc9a2dd8e444b53f6d0bc71dd329750c407e0",
        "r": "0xf9e7e9cd08bc9bf1347917784fac9cef5d55d4285d1398b1d59ae5328ad7c166",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4315578165013",
    "total": "121099319312641"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4315578165013",
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
            "amount": "27573343239905320259252"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4315578165"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjkwMzhiZi1iMGVhLTViYzYtOThlZi04NWFjOTA2OTk4NzQifQ==",
    "nonce": 110466,
    "balances": {
      "current": "399380860408610926876855",
      "previous": "399380860412930820620033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x840a38ba9321307976e648d3cd8c88d873cd61e2",
    "nonce": 45,
    "balances": {
      "current": "182023786276849",
      "previous": "177708208111836"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:25.555Z",
  "updated": "2022-05-04T08:53:25.674Z",
  "id": "62723f057832e20011830bbe"
}
```
* *stageAmount*: `182023786276849`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000003eccc80e7150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000003eccc80e71500000000000000000000000000000000000000000000000000006e23a1e9010107cba29e512a5950cc12c19324d20fa0ededacac87325b78c0113dbf4404a17745a15b1bee45da1920e91018f2bbf0218de5dd88003b3686f75c1db68bf7854423a59e93f8b12a392be6e12ca5b0d6ceb5b01f33d483b532fae48e4c79d06bc4000000000000000000000000000000000000000000000000000000000000001b895b6e8254d85174c67080059a0323ec11012f3f2f2683c580650cd51ae7eccaf9e7e9cd08bc9bf1347917784fac9cef5d55d4285d1398b1d59ae5328ad7c16637012ef04cc2266f51597322c50dc9a2dd8e444b53f6d0bc71dd329750c407e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af82000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000054927ad5d32523cbd8b70000000000000000000000000000000000000000000054927ad5d712f1873f0100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000001013a7f350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6c101b2dc3b0e4eb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a6b774d7a68695a6931694d4756684c545669597a59744f54686c5a6930344e57466a4f5441324f546b344e7a516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000840a38ba9321307976e648d3cd8c88d873cd61e20000000000000000000000000000000000000000000000000000a58cb71f27f10000000000000000000000000000000000000000000000000000a19fea9e40dc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x07cba29e512a5950cc12c19324d20fa0ededacac87325b78c0113dbf4404a177",
      "signature": {
        "s": "0x23a59e93f8b12a392be6e12ca5b0d6ceb5b01f33d483b532fae48e4c79d06bc4",
        "r": "0x45a15b1bee45da1920e91018f2bbf0218de5dd88003b3686f75c1db68bf78544",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x895b6e8254d85174c67080059a0323ec11012f3f2f2683c580650cd51ae7ecca",
      "signature": {
        "s": "0x37012ef04cc2266f51597322c50dc9a2dd8e444b53f6d0bc71dd329750c407e0",
        "r": "0xf9e7e9cd08bc9bf1347917784fac9cef5d55d4285d1398b1d59ae5328ad7c166",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4315578165013",
    "total": "121099319312641"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4315578165013",
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
            "amount": "27573343239905320259252"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4315578165"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjkwMzhiZi1iMGVhLTViYzYtOThlZi04NWFjOTA2OTk4NzQifQ==",
    "nonce": 110466,
    "balances": {
      "current": "399380860408610926876855",
      "previous": "399380860412930820620033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x840a38ba9321307976e648d3cd8c88d873cd61e2",
    "nonce": 45,
    "balances": {
      "current": "182023786276849",
      "previous": "177708208111836"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:25.555Z",
  "updated": "2022-05-04T08:53:25.674Z",
  "id": "62723f057832e20011830bbe"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000a58cb71f27f10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `182023786276849`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`