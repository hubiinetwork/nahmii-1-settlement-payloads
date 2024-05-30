# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x60e88D4027E2F38D0e2E347B6c8993Cc5a225200`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000014bd4ca5227ea60cfed000000000000000000000000000000000000000000000000000000414880ade30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000414880ade30000000000000000000000000000000000000000000000a997edf9ed4793d63c6a104bdf2df762e2fcf9290a3de8faf0cb2bbf470a7d6e0d5cccb5965a13570c12edddbef5ecddb06be81d14a821102abf70423cac665db4c07c8daa532e6d5019809d13e2aad4b62399b26fb4c37cfa4f01865506b19381741cfb0a3cc2e572000000000000000000000000000000000000000000000000000000000000001c269362ba4791a2e6f106d4f604d946ebc34b312616a2f81778f14ccaf5803411b738737f5c89c4deb58248ce36b81595dfbbfab1f092578460a05e7e74126ac34be5900b7bbaca432d112b6b9508c7ec2b874e3e08ecaa593711427a07dd1805000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af93000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783569fc39f0301600000000000000000000000000000000000000000000538478356a3d9327448b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000010b666920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d28da3a0290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a4577597a6b325a4330794d6a49304c54566d4d6d45744f544e6c595330305a6a45795a54526a5a574d344d7a416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000060e88d4027e2f38d0e2e347b6c8993cc5a22520000000000000000000000000000000000000000000000014bd4ca5227ea60cfed00000000000000000000000000000000000000000000014bd4ca51e6a1e0220a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a104bdf2df762e2fcf9290a3de8faf0cb2bbf470a7d6e0d5cccb5965a13570c",
      "signature": {
        "s": "0x19809d13e2aad4b62399b26fb4c37cfa4f01865506b19381741cfb0a3cc2e572",
        "r": "0x12edddbef5ecddb06be81d14a821102abf70423cac665db4c07c8daa532e6d50",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x269362ba4791a2e6f106d4f604d946ebc34b312616a2f81778f14ccaf5803411",
      "signature": {
        "s": "0x4be5900b7bbaca432d112b6b9508c7ec2b874e3e08ecaa593711427a07dd1805",
        "r": "0xb738737f5c89c4deb58248ce36b81595dfbbfab1f092578460a05e7e74126ac3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "280389266915",
    "total": "3128447429523625203260"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "280389266915",
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
            "amount": "27578319074237698252841"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "280389266"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MjEwYzk2ZC0yMjI0LTVmMmEtOTNlYS00ZjEyZTRjZWM4MzAifQ==",
    "nonce": 110483,
    "balances": {
      "current": "394400050241900555284502",
      "previous": "394400050242181224940683"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60e88d4027e2f38d0e2e347b6c8993cc5a225200",
    "nonce": 46,
    "balances": {
      "current": "6121205446610587275245",
      "previous": "6121205446330198008330"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.157Z",
  "updated": "2022-05-04T08:53:31.284Z",
  "id": "62723f0b7832e20011830bc6"
}
```
* *stageAmount*: `6121205446610587275245`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000414880ade30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000414880ade30000000000000000000000000000000000000000000000a997edf9ed4793d63c6a104bdf2df762e2fcf9290a3de8faf0cb2bbf470a7d6e0d5cccb5965a13570c12edddbef5ecddb06be81d14a821102abf70423cac665db4c07c8daa532e6d5019809d13e2aad4b62399b26fb4c37cfa4f01865506b19381741cfb0a3cc2e572000000000000000000000000000000000000000000000000000000000000001c269362ba4791a2e6f106d4f604d946ebc34b312616a2f81778f14ccaf5803411b738737f5c89c4deb58248ce36b81595dfbbfab1f092578460a05e7e74126ac34be5900b7bbaca432d112b6b9508c7ec2b874e3e08ecaa593711427a07dd1805000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af93000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000005384783569fc39f0301600000000000000000000000000000000000000000000538478356a3d9327448b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000010b666920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d28da3a0290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6a4577597a6b325a4330794d6a49304c54566d4d6d45744f544e6c595330305a6a45795a54526a5a574d344d7a416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000060e88d4027e2f38d0e2e347b6c8993cc5a22520000000000000000000000000000000000000000000000014bd4ca5227ea60cfed00000000000000000000000000000000000000000000014bd4ca51e6a1e0220a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a104bdf2df762e2fcf9290a3de8faf0cb2bbf470a7d6e0d5cccb5965a13570c",
      "signature": {
        "s": "0x19809d13e2aad4b62399b26fb4c37cfa4f01865506b19381741cfb0a3cc2e572",
        "r": "0x12edddbef5ecddb06be81d14a821102abf70423cac665db4c07c8daa532e6d50",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x269362ba4791a2e6f106d4f604d946ebc34b312616a2f81778f14ccaf5803411",
      "signature": {
        "s": "0x4be5900b7bbaca432d112b6b9508c7ec2b874e3e08ecaa593711427a07dd1805",
        "r": "0xb738737f5c89c4deb58248ce36b81595dfbbfab1f092578460a05e7e74126ac3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "280389266915",
    "total": "3128447429523625203260"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "280389266915",
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
            "amount": "27578319074237698252841"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "280389266"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MjEwYzk2ZC0yMjI0LTVmMmEtOTNlYS00ZjEyZTRjZWM4MzAifQ==",
    "nonce": 110483,
    "balances": {
      "current": "394400050241900555284502",
      "previous": "394400050242181224940683"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x60e88d4027e2f38d0e2e347b6c8993cc5a225200",
    "nonce": 46,
    "balances": {
      "current": "6121205446610587275245",
      "previous": "6121205446330198008330"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:31.157Z",
  "updated": "2022-05-04T08:53:31.284Z",
  "id": "62723f0b7832e20011830bc6"
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
0x0f200f9b00000000000000000000000000000000000000000000014bd4ca5227ea60cfed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6121205446610587275245`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`