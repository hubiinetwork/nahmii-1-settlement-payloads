# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4014F22D590d8f3371ce9AdED1383E0Bd11DC53B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000030f299f0248395777a00000000000000000000000000000000000000000000000129161d7a927a171e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000129161d7a927a171e00000000000000000000000000000000000000000000002090886affa81c6ce1c079ce320673baa67f83758743db5738ca1f5d9ff1c805885ca2b4e0f6e487369d4697533643d9cc71f3ec640703627c8707b44884158bde7e85880c731dad736c236f2f781534b5b45de736b2183bb7f86dad93cae5df4ac385fd4e288307be000000000000000000000000000000000000000000000000000000000000001cd3df8a27cd6a94aac462564a49219feab866fb6b00c317a859a52f4a16d41d925c18adcc02925ab9e31cbd8d12cbac995b2d506aa94c46f2ba825af56afd905a5302d9505c049e383514a7073565e78ae2ab05b4fac09d5d9f8ffd0bbfbcaf2b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad79000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000968afd5aff716addb67b00000000000000000000000000000000000000000000968c26bd2ac67aedf0f200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000004c0dda7d9623590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e1de04660029ea040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e6a45304d6a63785979316b5a4749344c545669597a51744f5445334e533169596d49794e4451345a546c6d4e7a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004014f22d590d8f3371ce9aded1383e0bd11dc53b000000000000000000000000000000000000000000000030f299f0248395777a00000000000000000000000000000000000000000000002fc983d2a9f11b605c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc079ce320673baa67f83758743db5738ca1f5d9ff1c805885ca2b4e0f6e48736",
      "signature": {
        "s": "0x6c236f2f781534b5b45de736b2183bb7f86dad93cae5df4ac385fd4e288307be",
        "r": "0x9d4697533643d9cc71f3ec640703627c8707b44884158bde7e85880c731dad73",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd3df8a27cd6a94aac462564a49219feab866fb6b00c317a859a52f4a16d41d92",
      "signature": {
        "s": "0x5302d9505c049e383514a7073565e78ae2ab05b4fac09d5d9f8ffd0bbfbcaf2b",
        "r": "0x5c18adcc02925ab9e31cbd8d12cbac995b2d506aa94c46f2ba825af56afd905a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "21407330291032921886",
    "total": "600710502143269563617"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21407330291032921886",
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
            "amount": "27262116447808507210244"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21407330291032921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNjE0MjcxYy1kZGI4LTViYzQtOTE3NS1iYmIyNDQ4ZTlmNzIifQ==",
    "nonce": 109945,
    "balances": {
      "current": "710918879297520789206651",
      "previous": "710940308035142113161458"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4014f22d590d8f3371ce9aded1383e0bd11dc53b",
    "nonce": 46,
    "balances": {
      "current": "902924983006290868090",
      "previous": "881517652715257946204"
    }
  },
  "blockNumber": "14709956",
  "created": "2022-05-04T08:50:44.595Z",
  "updated": "2022-05-04T08:50:44.692Z",
  "id": "62723e647832e20011830b14"
}
```
* *stageAmount*: `902924983006290868090`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000129161d7a927a171e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000129161d7a927a171e00000000000000000000000000000000000000000000002090886affa81c6ce1c079ce320673baa67f83758743db5738ca1f5d9ff1c805885ca2b4e0f6e487369d4697533643d9cc71f3ec640703627c8707b44884158bde7e85880c731dad736c236f2f781534b5b45de736b2183bb7f86dad93cae5df4ac385fd4e288307be000000000000000000000000000000000000000000000000000000000000001cd3df8a27cd6a94aac462564a49219feab866fb6b00c317a859a52f4a16d41d925c18adcc02925ab9e31cbd8d12cbac995b2d506aa94c46f2ba825af56afd905a5302d9505c049e383514a7073565e78ae2ab05b4fac09d5d9f8ffd0bbfbcaf2b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad79000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000968afd5aff716addb67b00000000000000000000000000000000000000000000968c26bd2ac67aedf0f200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000004c0dda7d9623590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e1de04660029ea040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e6a45304d6a63785979316b5a4749344c545669597a51744f5445334e533169596d49794e4451345a546c6d4e7a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004014f22d590d8f3371ce9aded1383e0bd11dc53b000000000000000000000000000000000000000000000030f299f0248395777a00000000000000000000000000000000000000000000002fc983d2a9f11b605c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc079ce320673baa67f83758743db5738ca1f5d9ff1c805885ca2b4e0f6e48736",
      "signature": {
        "s": "0x6c236f2f781534b5b45de736b2183bb7f86dad93cae5df4ac385fd4e288307be",
        "r": "0x9d4697533643d9cc71f3ec640703627c8707b44884158bde7e85880c731dad73",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd3df8a27cd6a94aac462564a49219feab866fb6b00c317a859a52f4a16d41d92",
      "signature": {
        "s": "0x5302d9505c049e383514a7073565e78ae2ab05b4fac09d5d9f8ffd0bbfbcaf2b",
        "r": "0x5c18adcc02925ab9e31cbd8d12cbac995b2d506aa94c46f2ba825af56afd905a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "21407330291032921886",
    "total": "600710502143269563617"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21407330291032921886",
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
            "amount": "27262116447808507210244"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21407330291032921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNjE0MjcxYy1kZGI4LTViYzQtOTE3NS1iYmIyNDQ4ZTlmNzIifQ==",
    "nonce": 109945,
    "balances": {
      "current": "710918879297520789206651",
      "previous": "710940308035142113161458"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4014f22d590d8f3371ce9aded1383e0bd11dc53b",
    "nonce": 46,
    "balances": {
      "current": "902924983006290868090",
      "previous": "881517652715257946204"
    }
  },
  "blockNumber": "14709956",
  "created": "2022-05-04T08:50:44.595Z",
  "updated": "2022-05-04T08:50:44.692Z",
  "id": "62723e647832e20011830b14"
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
0x0f200f9b000000000000000000000000000000000000000000000030f299f0248395777a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `902924983006290868090`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`