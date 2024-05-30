# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb7304Cf69Ae1F7Ab1743831D98D772B550BEA548`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000362c91008c7f69a42d000000000000000000000000000000000000000000000013418c48082ecc9ffb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000013418c48082ecc9ffb0000000000000000000000000000000000000000000000362c91008c7f69a42d0d662650ef06f42d9f81aa9afb51782bf9ba203db924a38d6860b5e6cdfe66d3bd952e8a449eb61f92dcacc0b0e25e484fb2afa3a999d7cf608986e6d33e92fd33b2034c1a0d3bcb747910ce9f2a32d24e0623915371fc90da5ae43b6355377b000000000000000000000000000000000000000000000000000000000000001c82c220115bd77a627f08c26886812a1d8109f59420a0ea0267300cdb86e86b75892ba0f2c4cdaa019c33b76a21ebb51133a232497d9c08fe7588ddc82cebc9a14004e24d221e749b9cb7fcfce46795cbe51b61a4798c03f47d805deb49a5ae23000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012357000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000238f1cd541787a7e70f00000000000000000000000000000000000000000000024c384792fadb5db12e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004edf6db24e92a240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000361f166cdf0ec8f424e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6d51304d474a694d4330344d6a49774c54566d4e7a67744f546b785a4331684e4745784f5755794e4445325954416966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000b7304cf69ae1f7ab1743831d98d772b550bea5480000000000000000000000000000000000000000000000362c91008c7f69a42d000000000000000000000000000000000000000000000022eb04b884509d043200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d662650ef06f42d9f81aa9afb51782bf9ba203db924a38d6860b5e6cdfe66d3",
      "signature": {
        "s": "0x33b2034c1a0d3bcb747910ce9f2a32d24e0623915371fc90da5ae43b6355377b",
        "r": "0xbd952e8a449eb61f92dcacc0b0e25e484fb2afa3a999d7cf608986e6d33e92fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x82c220115bd77a627f08c26886812a1d8109f59420a0ea0267300cdb86e86b75",
      "signature": {
        "s": "0x4004e24d221e749b9cb7fcfce46795cbe51b61a4798c03f47d805deb49a5ae23",
        "r": "0x892ba0f2c4cdaa019c33b76a21ebb51133a232497d9c08fe7588ddc82cebc9a1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "355211366709668388859",
    "total": "999335528593040712749"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "355211366709668388859",
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
            "amount": "15973828440804171924046"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "355211366709668388"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMmQ0MGJiMC04MjIwLTVmNzgtOTkxZC1hNGExOWUyNDE2YTAifQ==",
    "nonce": 74583,
    "balances": {
      "current": "10495174308860428543759",
      "previous": "10850740886936806601006"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb7304cf69ae1f7ab1743831d98d772b550bea548",
    "nonce": 2,
    "balances": {
      "current": "999335528593040712749",
      "previous": "644124161883372323890"
    }
  },
  "blockNumber": "12400716",
  "created": "2021-05-09T14:38:44.426Z",
  "updated": "2021-05-09T14:38:44.531Z",
  "id": "6097f3f40f95a80011b4b4fb"
}
```
* *stageAmount*: `999335528593040712749`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000013418c48082ecc9ffb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000013418c48082ecc9ffb0000000000000000000000000000000000000000000000362c91008c7f69a42d0d662650ef06f42d9f81aa9afb51782bf9ba203db924a38d6860b5e6cdfe66d3bd952e8a449eb61f92dcacc0b0e25e484fb2afa3a999d7cf608986e6d33e92fd33b2034c1a0d3bcb747910ce9f2a32d24e0623915371fc90da5ae43b6355377b000000000000000000000000000000000000000000000000000000000000001c82c220115bd77a627f08c26886812a1d8109f59420a0ea0267300cdb86e86b75892ba0f2c4cdaa019c33b76a21ebb51133a232497d9c08fe7588ddc82cebc9a14004e24d221e749b9cb7fcfce46795cbe51b61a4798c03f47d805deb49a5ae23000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384c00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012357000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000238f1cd541787a7e70f00000000000000000000000000000000000000000000024c384792fadb5db12e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000004edf6db24e92a240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000361f166cdf0ec8f424e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d6d51304d474a694d4330344d6a49774c54566d4e7a67744f546b785a4331684e4745784f5755794e4445325954416966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000b7304cf69ae1f7ab1743831d98d772b550bea5480000000000000000000000000000000000000000000000362c91008c7f69a42d000000000000000000000000000000000000000000000022eb04b884509d043200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d662650ef06f42d9f81aa9afb51782bf9ba203db924a38d6860b5e6cdfe66d3",
      "signature": {
        "s": "0x33b2034c1a0d3bcb747910ce9f2a32d24e0623915371fc90da5ae43b6355377b",
        "r": "0xbd952e8a449eb61f92dcacc0b0e25e484fb2afa3a999d7cf608986e6d33e92fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x82c220115bd77a627f08c26886812a1d8109f59420a0ea0267300cdb86e86b75",
      "signature": {
        "s": "0x4004e24d221e749b9cb7fcfce46795cbe51b61a4798c03f47d805deb49a5ae23",
        "r": "0x892ba0f2c4cdaa019c33b76a21ebb51133a232497d9c08fe7588ddc82cebc9a1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "355211366709668388859",
    "total": "999335528593040712749"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "355211366709668388859",
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
            "amount": "15973828440804171924046"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "355211366709668388"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMmQ0MGJiMC04MjIwLTVmNzgtOTkxZC1hNGExOWUyNDE2YTAifQ==",
    "nonce": 74583,
    "balances": {
      "current": "10495174308860428543759",
      "previous": "10850740886936806601006"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb7304cf69ae1f7ab1743831d98d772b550bea548",
    "nonce": 2,
    "balances": {
      "current": "999335528593040712749",
      "previous": "644124161883372323890"
    }
  },
  "blockNumber": "12400716",
  "created": "2021-05-09T14:38:44.426Z",
  "updated": "2021-05-09T14:38:44.531Z",
  "id": "6097f3f40f95a80011b4b4fb"
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
0x0f200f9b0000000000000000000000000000000000000000000000362c91008c7f69a42d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `999335528593040712749`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`