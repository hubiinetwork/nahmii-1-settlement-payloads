# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc5c15B678E08A7d361d29d8f32a120FCa98369Fc`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001024000000000000000000000000000000000000000000000000000000000000102400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001024000000000000000000000000000000000000000000000000000000000000102447afdcadecf729a57205d24990d6716d5b62d49c155c65a40d29ae7b2a136062869eb393012dc5f6b837f4a685ea8dc2054ce367feaa1ad595df89b74a1036871ce7fdffa4ef159fd867fa400980730b29d5225d308fe54a4e051d809f6a917e000000000000000000000000000000000000000000000000000000000000001c4fe49d4088a4f96c6d13bcefc4f38c4739e80230135b452021b714b3eb700ac9ecf79e0f7a6df6b33e431c061ebee4886e4a817cc55c1aa0b5f61ebfcda018c264ef5d57a98746c4c9de9b3435d460ba4e99506a961981b386683b83b12343b3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000092f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc512a75000000000000000000000000000000000000000000000000002386f2bc513a9d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f8f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5759794d3259775a6931684f5746684c54566c4e446b74596a6c684d4330785a446c6d4d7a686d4d6a55305a6a516966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000c5c15b678e08a7d361d29d8f32a120fca98369fc0000000000000000000000000000000000000000000000000000000000001024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47afdcadecf729a57205d24990d6716d5b62d49c155c65a40d29ae7b2a136062",
      "signature": {
        "s": "0x1ce7fdffa4ef159fd867fa400980730b29d5225d308fe54a4e051d809f6a917e",
        "r": "0x869eb393012dc5f6b837f4a685ea8dc2054ce367feaa1ad595df89b74a103687",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4fe49d4088a4f96c6d13bcefc4f38c4739e80230135b452021b714b3eb700ac9",
      "signature": {
        "s": "0x64ef5d57a98746c4c9de9b3435d460ba4e99506a961981b386683b83b12343b3",
        "r": "0xecf79e0f7a6df6b33e431c061ebee4886e4a817cc55c1aa0b5f61ebfcda018c2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4132",
    "total": "4132"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4132",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798607"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZWYyM2YwZi1hOWFhLTVlNDktYjlhMC0xZDlmMzhmMjU0ZjQifQ==",
    "nonce": 2351,
    "balances": {
      "current": "10000001284516469",
      "previous": "10000001284520605"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc5c15b678e08a7d361d29d8f32a120fca98369fc",
    "nonce": 11,
    "balances": {
      "current": "4132",
      "previous": "0"
    }
  },
  "blockNumber": "10114553",
  "created": "2020-05-22T08:15:56.713Z",
  "updated": "2020-05-22T08:15:57.790Z",
  "id": "5ec78a3cb0c6090011d5abe0"
}
```
* *stageAmount*: `4132`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000102400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001024000000000000000000000000000000000000000000000000000000000000102447afdcadecf729a57205d24990d6716d5b62d49c155c65a40d29ae7b2a136062869eb393012dc5f6b837f4a685ea8dc2054ce367feaa1ad595df89b74a1036871ce7fdffa4ef159fd867fa400980730b29d5225d308fe54a4e051d809f6a917e000000000000000000000000000000000000000000000000000000000000001c4fe49d4088a4f96c6d13bcefc4f38c4739e80230135b452021b714b3eb700ac9ecf79e0f7a6df6b33e431c061ebee4886e4a817cc55c1aa0b5f61ebfcda018c264ef5d57a98746c4c9de9b3435d460ba4e99506a961981b386683b83b12343b3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000092f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc512a75000000000000000000000000000000000000000000000000002386f2bc513a9d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f8f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5759794d3259775a6931684f5746684c54566c4e446b74596a6c684d4330785a446c6d4d7a686d4d6a55305a6a516966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000c5c15b678e08a7d361d29d8f32a120fca98369fc0000000000000000000000000000000000000000000000000000000000001024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47afdcadecf729a57205d24990d6716d5b62d49c155c65a40d29ae7b2a136062",
      "signature": {
        "s": "0x1ce7fdffa4ef159fd867fa400980730b29d5225d308fe54a4e051d809f6a917e",
        "r": "0x869eb393012dc5f6b837f4a685ea8dc2054ce367feaa1ad595df89b74a103687",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4fe49d4088a4f96c6d13bcefc4f38c4739e80230135b452021b714b3eb700ac9",
      "signature": {
        "s": "0x64ef5d57a98746c4c9de9b3435d460ba4e99506a961981b386683b83b12343b3",
        "r": "0xecf79e0f7a6df6b33e431c061ebee4886e4a817cc55c1aa0b5f61ebfcda018c2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4132",
    "total": "4132"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4132",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798607"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZWYyM2YwZi1hOWFhLTVlNDktYjlhMC0xZDlmMzhmMjU0ZjQifQ==",
    "nonce": 2351,
    "balances": {
      "current": "10000001284516469",
      "previous": "10000001284520605"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc5c15b678e08a7d361d29d8f32a120fca98369fc",
    "nonce": 11,
    "balances": {
      "current": "4132",
      "previous": "0"
    }
  },
  "blockNumber": "10114553",
  "created": "2020-05-22T08:15:56.713Z",
  "updated": "2020-05-22T08:15:57.790Z",
  "id": "5ec78a3cb0c6090011d5abe0"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000010240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4132`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``