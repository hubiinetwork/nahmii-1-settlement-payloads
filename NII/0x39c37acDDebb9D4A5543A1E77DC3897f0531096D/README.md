# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x39c37acDDebb9D4A5543A1E77DC3897f0531096D`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001993576dda8815b9f0000000000000000000000000000000000000000000000000000000db1e7bfe90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000db1e7bfe9000000000000000000000000000000000000000000000023719aa0d19767150695a7497590f3ff51f4c8decf6c8cbc41ba59b1285a2b17ae6208d81799e9d2a1cf1e54b93b874a00e0277ebd4ce07919bcca18375389b16afcef3839e0689c5568ab3b02149b486c3b33ada2dfcb27e6df7a6f7ca8dd56d7e173acdf0a8294f9000000000000000000000000000000000000000000000000000000000000001be600e2b9ac100ec1abcc23ffbcdde79ba70dd9b87c4116d505686b87c03185720d0b697850f1a93fbc06124cee1bc1fcb8531028d1528297996f94b8891b5b6a7cff6152a3c589eb578cc19930f9b2893cbd02853f6e4bcb483fc662c07392d5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b007000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004fd395b200b035afb191000000000000000000000000000000000000000000004fd395b200bdeb18f47c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000038183020000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7f7b585cdc523d1290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a446b774e6a49324d5330774d7a51784c5455314d7a6b744f4455774d7930304d4745794d474a6a4d4445334d474d6966513d3d000000000000000000000000000000000000000000000000000000000000002f00000000000000000000000039c37acddebb9d4a5543a1e77dc3897f0531096d000000000000000000000000000000000000000000000001993576dda8815b9f000000000000000000000000000000000000000000000001993576cff6999bb600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000115c16ec258940000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95a7497590f3ff51f4c8decf6c8cbc41ba59b1285a2b17ae6208d81799e9d2a1",
      "signature": {
        "s": "0x68ab3b02149b486c3b33ada2dfcb27e6df7a6f7ca8dd56d7e173acdf0a8294f9",
        "r": "0xcf1e54b93b874a00e0277ebd4ce07919bcca18375389b16afcef3839e0689c55",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe600e2b9ac100ec1abcc23ffbcdde79ba70dd9b87c4116d505686b87c0318572",
      "signature": {
        "s": "0x7cff6152a3c589eb578cc19930f9b2893cbd02853f6e4bcb483fc662c07392d5",
        "r": "0x0d0b697850f1a93fbc06124cee1bc1fcb8531028d1528297996f94b8891b5b6a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "58819330025",
    "total": "653822074674582328582"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "58819330025",
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
            "amount": "27595731710012754743593"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "58819330"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZDkwNjI2MS0wMzQxLTU1MzktODUwMy00MGEyMGJjMDE3MGMifQ==",
    "nonce": 110599,
    "balances": {
      "current": "376970001831069007982993",
      "previous": "376970001831127886132348"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "1250900000000000000"
          }
        }
      ]
    },
    "wallet": "0x39c37acddebb9d4a5543a1e77dc3897f0531096d",
    "nonce": 47,
    "balances": {
      "current": "29486604829665090463",
      "previous": "29486604770845760438"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:54:05.993Z",
  "updated": "2022-05-04T08:54:06.099Z",
  "id": "62723f2d7832e20011830bec"
}
```
* *stageAmount*: `29486604829665090463`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000000000000db1e7bfe90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000db1e7bfe9000000000000000000000000000000000000000000000023719aa0d19767150695a7497590f3ff51f4c8decf6c8cbc41ba59b1285a2b17ae6208d81799e9d2a1cf1e54b93b874a00e0277ebd4ce07919bcca18375389b16afcef3839e0689c5568ab3b02149b486c3b33ada2dfcb27e6df7a6f7ca8dd56d7e173acdf0a8294f9000000000000000000000000000000000000000000000000000000000000001be600e2b9ac100ec1abcc23ffbcdde79ba70dd9b87c4116d505686b87c03185720d0b697850f1a93fbc06124cee1bc1fcb8531028d1528297996f94b8891b5b6a7cff6152a3c589eb578cc19930f9b2893cbd02853f6e4bcb483fc662c07392d5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b007000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004fd395b200b035afb191000000000000000000000000000000000000000000004fd395b200bdeb18f47c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000038183020000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7f7b585cdc523d1290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a446b774e6a49324d5330774d7a51784c5455314d7a6b744f4455774d7930304d4745794d474a6a4d4445334d474d6966513d3d000000000000000000000000000000000000000000000000000000000000002f00000000000000000000000039c37acddebb9d4a5543a1e77dc3897f0531096d000000000000000000000000000000000000000000000001993576dda8815b9f000000000000000000000000000000000000000000000001993576cff6999bb600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000115c16ec258940000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95a7497590f3ff51f4c8decf6c8cbc41ba59b1285a2b17ae6208d81799e9d2a1",
      "signature": {
        "s": "0x68ab3b02149b486c3b33ada2dfcb27e6df7a6f7ca8dd56d7e173acdf0a8294f9",
        "r": "0xcf1e54b93b874a00e0277ebd4ce07919bcca18375389b16afcef3839e0689c55",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe600e2b9ac100ec1abcc23ffbcdde79ba70dd9b87c4116d505686b87c0318572",
      "signature": {
        "s": "0x7cff6152a3c589eb578cc19930f9b2893cbd02853f6e4bcb483fc662c07392d5",
        "r": "0x0d0b697850f1a93fbc06124cee1bc1fcb8531028d1528297996f94b8891b5b6a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "58819330025",
    "total": "653822074674582328582"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "58819330025",
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
            "amount": "27595731710012754743593"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "58819330"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZDkwNjI2MS0wMzQxLTU1MzktODUwMy00MGEyMGJjMDE3MGMifQ==",
    "nonce": 110599,
    "balances": {
      "current": "376970001831069007982993",
      "previous": "376970001831127886132348"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "1250900000000000000"
          }
        }
      ]
    },
    "wallet": "0x39c37acddebb9d4a5543a1e77dc3897f0531096d",
    "nonce": 47,
    "balances": {
      "current": "29486604829665090463",
      "previous": "29486604770845760438"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:54:05.993Z",
  "updated": "2022-05-04T08:54:06.099Z",
  "id": "62723f2d7832e20011830bec"
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
0x0f200f9b000000000000000000000000000000000000000000000001993576dda8815b9f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `29486604829665090463`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`