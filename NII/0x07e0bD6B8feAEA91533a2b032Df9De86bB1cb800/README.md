# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x07e0bD6B8feAEA91533a2b032Df9De86bB1cb800`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000238d582f7176dce2ac000000000000000000000000000000000000000000000000d7c857d18e8220cf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d7c857d18e8220cf000000000000000000000000000000000000000000000017a711bc48ca60efa68484eeecf7a823ff020133a346a88f68e6073a8c08b8dd4f1a2bcb821cf36cb83fb6ece590dab3655b61b55900f367a91ebd09463f2614c00323c2ac48fbd9685e9b52f0c9c7b945e9b8a33bd3b6581a453df22e08877378710b0e82e82851b5000000000000000000000000000000000000000000000000000000000000001b2603795fea43596fc042f1632f1bd53d9d09c34ad03464a37d62e429660fe92cfd44cebecc75cda53fca245fb7deaf40ada588e274f8cf2758ed39dd92bcf444655ef2ce3a3367d10efda4639a37b9beece587c519d18ea4f025d30e68e2187c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6b6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030229c6402a288994411000000000000000000000000000000000000000000003023746397fb3639bb6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000373d871f1e568f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0128e3749d1d8203c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a5459785a5441324d4330794e5751324c54566b4f545574596a6b304d69307a4e7a4177597a4e6d4e574e684e47556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007e0bd6b8feaea91533a2b032df9de86bb1cb8000000000000000000000000000000000000000000000000238d582f7176dce2ac000000000000000000000000000000000000000000000022b58fd79fe85ac1dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8484eeecf7a823ff020133a346a88f68e6073a8c08b8dd4f1a2bcb821cf36cb8",
      "signature": {
        "s": "0x5e9b52f0c9c7b945e9b8a33bd3b6581a453df22e08877378710b0e82e82851b5",
        "r": "0x3fb6ece590dab3655b61b55900f367a91ebd09463f2614c00323c2ac48fbd968",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2603795fea43596fc042f1632f1bd53d9d09c34ad03464a37d62e429660fe92c",
      "signature": {
        "s": "0x655ef2ce3a3367d10efda4639a37b9beece587c519d18ea4f025d30e68e2187c",
        "r": "0xfd44cebecc75cda53fca245fb7deaf40ada588e274f8cf2758ed39dd92bcf444",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15548774271047311567",
    "total": "436313723995076751270"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15548774271047311567",
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
            "amount": "27745240153788733988924"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15548774271047311"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTYxZTA2MC0yNWQ2LTVkOTUtYjk0Mi0zNzAwYzNmNWNhNGUifQ==",
    "nonce": 112310,
    "balances": {
      "current": "227312049611313782539281",
      "previous": "227327613934359100898159"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07e0bd6b8feaea91533a2b032df9de86bb1cb800",
    "nonce": 46,
    "balances": {
      "current": "655820985301504680620",
      "previous": "640272211030457369053"
    }
  },
  "blockNumber": "14709991",
  "created": "2022-05-04T09:03:06.651Z",
  "updated": "2022-05-04T09:03:06.733Z",
  "id": "6272414a3592fd001130b760"
}
```
* *stageAmount*: `655820985301504680620`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000d7c857d18e8220cf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d7c857d18e8220cf000000000000000000000000000000000000000000000017a711bc48ca60efa68484eeecf7a823ff020133a346a88f68e6073a8c08b8dd4f1a2bcb821cf36cb83fb6ece590dab3655b61b55900f367a91ebd09463f2614c00323c2ac48fbd9685e9b52f0c9c7b945e9b8a33bd3b6581a453df22e08877378710b0e82e82851b5000000000000000000000000000000000000000000000000000000000000001b2603795fea43596fc042f1632f1bd53d9d09c34ad03464a37d62e429660fe92cfd44cebecc75cda53fca245fb7deaf40ada588e274f8cf2758ed39dd92bcf444655ef2ce3a3367d10efda4639a37b9beece587c519d18ea4f025d30e68e2187c000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6b6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030229c6402a288994411000000000000000000000000000000000000000000003023746397fb3639bb6f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000373d871f1e568f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0128e3749d1d8203c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a5459785a5441324d4330794e5751324c54566b4f545574596a6b304d69307a4e7a4177597a4e6d4e574e684e47556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000007e0bd6b8feaea91533a2b032df9de86bb1cb8000000000000000000000000000000000000000000000000238d582f7176dce2ac000000000000000000000000000000000000000000000022b58fd79fe85ac1dd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8484eeecf7a823ff020133a346a88f68e6073a8c08b8dd4f1a2bcb821cf36cb8",
      "signature": {
        "s": "0x5e9b52f0c9c7b945e9b8a33bd3b6581a453df22e08877378710b0e82e82851b5",
        "r": "0x3fb6ece590dab3655b61b55900f367a91ebd09463f2614c00323c2ac48fbd968",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2603795fea43596fc042f1632f1bd53d9d09c34ad03464a37d62e429660fe92c",
      "signature": {
        "s": "0x655ef2ce3a3367d10efda4639a37b9beece587c519d18ea4f025d30e68e2187c",
        "r": "0xfd44cebecc75cda53fca245fb7deaf40ada588e274f8cf2758ed39dd92bcf444",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15548774271047311567",
    "total": "436313723995076751270"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15548774271047311567",
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
            "amount": "27745240153788733988924"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15548774271047311"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZTYxZTA2MC0yNWQ2LTVkOTUtYjk0Mi0zNzAwYzNmNWNhNGUifQ==",
    "nonce": 112310,
    "balances": {
      "current": "227312049611313782539281",
      "previous": "227327613934359100898159"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x07e0bd6b8feaea91533a2b032df9de86bb1cb800",
    "nonce": 46,
    "balances": {
      "current": "655820985301504680620",
      "previous": "640272211030457369053"
    }
  },
  "blockNumber": "14709991",
  "created": "2022-05-04T09:03:06.651Z",
  "updated": "2022-05-04T09:03:06.733Z",
  "id": "6272414a3592fd001130b760"
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
0x0f200f9b0000000000000000000000000000000000000000000000238d582f7176dce2ac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `655820985301504680620`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`