# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA35c838a032eF880b3E2c50d66256D1BCecab89D`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000a59bb5b50f7bdc6000000000000000000000000000000000000000000000000003ed2783c4aca280000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000003ed2783c4aca2800000000000000000000000000000000000000000000000006e2d9bc5d3239e9ad2919cffaa4ce28f1f99e2f6716f4a66ad1b28683951e5993756cdf8d8e82de5210228fbecde11697b106a4d751927c5127f3b95bb45622220ab482489b56787e5502c54692fbb28b28ac52dce6041e7b340074435c068bc042f5905aeedb8a000000000000000000000000000000000000000000000000000000000000001b177f77a3752e9e85dc7ce8daa181c0e04abb233596dd07c8e2f2d25fa97c03c78fa38f789238b2020a5db7277b3c9ab96bee22a3645da184892fc8d155269a1e295100f1ef030828c056a0ef841396120124b09441e0ae54784026ef030b8c3a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2c2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000046b76cb850dd9d23f0670000000000000000000000000000000000000000000046b76cf7336af62a320e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000010151cbb777f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da4c2546cf83d25e650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e6a49774d57526d5a6931684d5745794c5455324d4445744f574d324d5331684e4455354f47526c4d32566c4f54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a35c838a032ef880b3e2c50d66256d1bcecab89d0000000000000000000000000000000000000000000000000a59bb5b50f7bdc60000000000000000000000000000000000000000000000000a1ae8e314acf39e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad2919cffaa4ce28f1f99e2f6716f4a66ad1b28683951e5993756cdf8d8e82de",
      "signature": {
        "s": "0x7e5502c54692fbb28b28ac52dce6041e7b340074435c068bc042f5905aeedb8a",
        "r": "0x5210228fbecde11697b106a4d751927c5127f3b95bb45622220ab482489b5678",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x177f77a3752e9e85dc7ce8daa181c0e04abb233596dd07c8e2f2d25fa97c03c7",
      "signature": {
        "s": "0x295100f1ef030828c056a0ef841396120124b09441e0ae54784026ef030b8c3a",
        "r": "0x8fa38f789238b2020a5db7277b3c9ab96bee22a3645da184892fc8d155269a1e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "17682862405503528",
    "total": "496198312004827625"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17682862405503528",
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
            "amount": "27638709491995012914789"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "17682862405503"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNjIwMWRmZi1hMWEyLTU2MDEtOWM2MS1hNDU5OGRlM2VlOTgifQ==",
    "nonce": 111298,
    "balances": {
      "current": "333949242066828578254951",
      "previous": "333949259767373846163982"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa35c838a032ef880b3e2c50d66256d1bcecab89d",
    "nonce": 46,
    "balances": {
      "current": "745833214181359046",
      "previous": "728150351775855518"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:34.780Z",
  "updated": "2022-05-04T08:57:34.853Z",
  "id": "62723ffe3592fd001130b600"
}
```
* *stageAmount*: `745833214181359046`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000003ed2783c4aca280000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000003ed2783c4aca2800000000000000000000000000000000000000000000000006e2d9bc5d3239e9ad2919cffaa4ce28f1f99e2f6716f4a66ad1b28683951e5993756cdf8d8e82de5210228fbecde11697b106a4d751927c5127f3b95bb45622220ab482489b56787e5502c54692fbb28b28ac52dce6041e7b340074435c068bc042f5905aeedb8a000000000000000000000000000000000000000000000000000000000000001b177f77a3752e9e85dc7ce8daa181c0e04abb233596dd07c8e2f2d25fa97c03c78fa38f789238b2020a5db7277b3c9ab96bee22a3645da184892fc8d155269a1e295100f1ef030828c056a0ef841396120124b09441e0ae54784026ef030b8c3a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2c2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000046b76cb850dd9d23f0670000000000000000000000000000000000000000000046b76cf7336af62a320e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000010151cbb777f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da4c2546cf83d25e650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e6a49774d57526d5a6931684d5745794c5455324d4445744f574d324d5331684e4455354f47526c4d32566c4f54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a35c838a032ef880b3e2c50d66256d1bcecab89d0000000000000000000000000000000000000000000000000a59bb5b50f7bdc60000000000000000000000000000000000000000000000000a1ae8e314acf39e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad2919cffaa4ce28f1f99e2f6716f4a66ad1b28683951e5993756cdf8d8e82de",
      "signature": {
        "s": "0x7e5502c54692fbb28b28ac52dce6041e7b340074435c068bc042f5905aeedb8a",
        "r": "0x5210228fbecde11697b106a4d751927c5127f3b95bb45622220ab482489b5678",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x177f77a3752e9e85dc7ce8daa181c0e04abb233596dd07c8e2f2d25fa97c03c7",
      "signature": {
        "s": "0x295100f1ef030828c056a0ef841396120124b09441e0ae54784026ef030b8c3a",
        "r": "0x8fa38f789238b2020a5db7277b3c9ab96bee22a3645da184892fc8d155269a1e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "17682862405503528",
    "total": "496198312004827625"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17682862405503528",
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
            "amount": "27638709491995012914789"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "17682862405503"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNjIwMWRmZi1hMWEyLTU2MDEtOWM2MS1hNDU5OGRlM2VlOTgifQ==",
    "nonce": 111298,
    "balances": {
      "current": "333949242066828578254951",
      "previous": "333949259767373846163982"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa35c838a032ef880b3e2c50d66256d1bcecab89d",
    "nonce": 46,
    "balances": {
      "current": "745833214181359046",
      "previous": "728150351775855518"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:34.780Z",
  "updated": "2022-05-04T08:57:34.853Z",
  "id": "62723ffe3592fd001130b600"
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
0x0f200f9b0000000000000000000000000000000000000000000000000a59bb5b50f7bdc60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `745833214181359046`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`