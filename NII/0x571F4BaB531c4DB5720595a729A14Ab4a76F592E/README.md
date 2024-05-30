# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x571F4BaB531c4DB5720595a729A14Ab4a76F592E`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de169fc9a8fae15000000000000000000000000000000000000000000000000f36a9911b05a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000f36a9911b05a0000000000000000000000000000000000000000000000000000f36a9911b05a0000ba2b17e711c5731d0e9448dc62287435fccc8373fefa926ba929b5d96dfb53b16047859e5c52d14808b4728e683d05eac2ad41d55992644a78e55973c59398282e415e4c537e35dc5b1d5ebe5f21636442ab3729484eaf30fba0e17a2e9bc032000000000000000000000000000000000000000000000000000000000000001b33c71824529e50a2753d76fc0082a1710872d95d6547a1e59660bc9ad00d5cba8cfbf165437375f48a6126a5c9e2d98fb83efd7358f27b340d70322d6304a45c73b9378f1481d86b26f589667c65fdd0f43027ac9df52220831f0f16ddedae57000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2520a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000571f4bab531c4db5720595a729a14ab4a76f592e0000000000000000000000000000000000000000000000000de169fc9a8fae15000000000000000000000000000000000000000000000001018a5397c845ee1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003e50897d5c40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e50897d5c40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595451784e57466b4e5330784f5749304c54526b595755744f5451774d4330784e6a466a5a6a5a684f4449314d32556966513d3d000000000000000000000000000000000000000000000000000000000000007f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000673e8478fff22e099b7000000000000000000000000000000000000000000000673d910e66e07daf9b7000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba2b17e711c5731d0e9448dc62287435fccc8373fefa926ba929b5d96dfb53b1",
      "signature": {
        "s": "0x2e415e4c537e35dc5b1d5ebe5f21636442ab3729484eaf30fba0e17a2e9bc032",
        "r": "0x6047859e5c52d14808b4728e683d05eac2ad41d55992644a78e55973c5939828",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x33c71824529e50a2753d76fc0082a1710872d95d6547a1e59660bc9ad00d5cba",
      "signature": {
        "s": "0x73b9378f1481d86b26f589667c65fdd0f43027ac9df52220831f0f16ddedae57",
        "r": "0x8cfbf165437375f48a6126a5c9e2d98fb83efd7358f27b340d70322d6304a45c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "17540000000000000000",
    "total": "17540000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17540000000000000000",
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
            "amount": "17540000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "17540000000000000"
      }
    },
    "wallet": "0x571f4bab531c4db5720595a729a14ab4a76f592e",
    "data": "eyJyZWYiOiI4YTQxNWFkNS0xOWI0LTRkYWUtOTQwMC0xNjFjZjZhODI1M2UifQ==",
    "nonce": 13,
    "balances": {
      "current": "1000197125898743317",
      "previous": "18557737125898743317"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 127,
    "balances": {
      "current": "487556991528969280527216",
      "previous": "487539451528969280527216"
    }
  },
  "blockNumber": "14832138",
  "created": "2022-05-23T22:29:39.918Z",
  "updated": "2022-05-23T22:29:40.031Z",
  "id": "628c0ad37832e20011830f40"
}
```
* *stageAmount*: `1000197125898743317`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000f36a9911b05a00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000f36a9911b05a0000000000000000000000000000000000000000000000000000f36a9911b05a0000ba2b17e711c5731d0e9448dc62287435fccc8373fefa926ba929b5d96dfb53b16047859e5c52d14808b4728e683d05eac2ad41d55992644a78e55973c59398282e415e4c537e35dc5b1d5ebe5f21636442ab3729484eaf30fba0e17a2e9bc032000000000000000000000000000000000000000000000000000000000000001b33c71824529e50a2753d76fc0082a1710872d95d6547a1e59660bc9ad00d5cba8cfbf165437375f48a6126a5c9e2d98fb83efd7358f27b340d70322d6304a45c73b9378f1481d86b26f589667c65fdd0f43027ac9df52220831f0f16ddedae57000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e2520a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000571f4bab531c4db5720595a729a14ab4a76f592e0000000000000000000000000000000000000000000000000de169fc9a8fae15000000000000000000000000000000000000000000000001018a5397c845ee1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003e50897d5c40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003e50897d5c40000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934595451784e57466b4e5330784f5749304c54526b595755744f5451774d4330784e6a466a5a6a5a684f4449314d32556966513d3d000000000000000000000000000000000000000000000000000000000000007f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000673e8478fff22e099b7000000000000000000000000000000000000000000000673d910e66e07daf9b7000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba2b17e711c5731d0e9448dc62287435fccc8373fefa926ba929b5d96dfb53b1",
      "signature": {
        "s": "0x2e415e4c537e35dc5b1d5ebe5f21636442ab3729484eaf30fba0e17a2e9bc032",
        "r": "0x6047859e5c52d14808b4728e683d05eac2ad41d55992644a78e55973c5939828",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x33c71824529e50a2753d76fc0082a1710872d95d6547a1e59660bc9ad00d5cba",
      "signature": {
        "s": "0x73b9378f1481d86b26f589667c65fdd0f43027ac9df52220831f0f16ddedae57",
        "r": "0x8cfbf165437375f48a6126a5c9e2d98fb83efd7358f27b340d70322d6304a45c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "17540000000000000000",
    "total": "17540000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17540000000000000000",
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
            "amount": "17540000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "17540000000000000"
      }
    },
    "wallet": "0x571f4bab531c4db5720595a729a14ab4a76f592e",
    "data": "eyJyZWYiOiI4YTQxNWFkNS0xOWI0LTRkYWUtOTQwMC0xNjFjZjZhODI1M2UifQ==",
    "nonce": 13,
    "balances": {
      "current": "1000197125898743317",
      "previous": "18557737125898743317"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 127,
    "balances": {
      "current": "487556991528969280527216",
      "previous": "487539451528969280527216"
    }
  },
  "blockNumber": "14832138",
  "created": "2022-05-23T22:29:39.918Z",
  "updated": "2022-05-23T22:29:40.031Z",
  "id": "628c0ad37832e20011830f40"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de169fc9a8fae150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000197125898743317`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`