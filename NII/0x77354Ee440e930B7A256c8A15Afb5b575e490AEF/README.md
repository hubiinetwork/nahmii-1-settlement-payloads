# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x77354Ee440e930B7A256c8A15Afb5b575e490AEF`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de4480e9ec328730000000000000000000000000000000000000000000000000000003a242f03940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000003a242f039400000000000000000000000000000000000000000000002621cb6fa76835bc2c6b3a74082556367dd14e761d00b50afc726b689fe476049bb87f3dd1bbfab818e146b1adc53df34cc70121b4d2c29eafd85cd0b4bb5f0f00a8b754850f73a7bb68ba256971ef21569d1b9ecda8a6bbf427c31941a7e56d0669137c0c568cfe71000000000000000000000000000000000000000000000000000000000000001bf7c363f62b434e1bbbf9b89f3ae254822e20167ec1ddeaa5ee1263e1b4831c0b0d5ad0b1ffe0b42a0910bee8e9eb6f073071df3b525b19ef52f2288d4ffc545d1c988dabe2d154a16ed3be4774193f58d54fa14c2caf59bb90d19762cd5ead7e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b399000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bce792e59ef1ee78bde000000000000000000000000000000000000000000003bce792e5a2951f8e94e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000ee259dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd166d47502305520d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e5468695a6a4d354d5330784f44526a4c5455304e7a4974596a49354d5330315a6d4a6b4f4451345954466d4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000077354ee440e930b7a256c8a15afb5b575e490aef0000000000000000000000000000000000000000000000000de4480e9ec328730000000000000000000000000000000000000000000000000de447d47a9424df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046d26fabd31a9490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x6b3a74082556367dd14e761d00b50afc726b689fe476049bb87f3dd1bbfab818",
      "signature": {
        "s": "0x68ba256971ef21569d1b9ecda8a6bbf427c31941a7e56d0669137c0c568cfe71",
        "r": "0xe146b1adc53df34cc70121b4d2c29eafd85cd0b4bb5f0f00a8b754850f73a7bb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf7c363f62b434e1bbbf9b89f3ae254822e20167ec1ddeaa5ee1263e1b4831c0b",
      "signature": {
        "s": "0x1c988dabe2d154a16ed3be4774193f58d54fa14c2caf59bb90d19762cd5ead7e",
        "r": "0x0d5ad0b1ffe0b42a0910bee8e9eb6f073071df3b525b19ef52f2288d4ffc545d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "249715164052",
    "total": "703411437589285420076"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "249715164052",
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
            "amount": "27690178880888843358733"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "249715164"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNThiZjM5MS0xODRjLTU0NzItYjI5MS01ZmJkODQ4YTFmNjIifQ==",
    "nonce": 111513,
    "balances": {
      "current": "282428383784104303758302",
      "previous": "282428383784354268637518"
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
            "amount": "318954006971001161"
          }
        }
      ]
    },
    "wallet": "0x77354ee440e930b7a256c8a15afb5b575e490aef",
    "nonce": 46,
    "balances": {
      "current": "1001004244813424755",
      "previous": "1001003995098260703"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:42.310Z",
  "updated": "2022-05-04T08:58:42.416Z",
  "id": "627240427832e20011830d1b"
}
```
* *stageAmount*: `1001004244813424755`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000000000003a242f03940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000003a242f039400000000000000000000000000000000000000000000002621cb6fa76835bc2c6b3a74082556367dd14e761d00b50afc726b689fe476049bb87f3dd1bbfab818e146b1adc53df34cc70121b4d2c29eafd85cd0b4bb5f0f00a8b754850f73a7bb68ba256971ef21569d1b9ecda8a6bbf427c31941a7e56d0669137c0c568cfe71000000000000000000000000000000000000000000000000000000000000001bf7c363f62b434e1bbbf9b89f3ae254822e20167ec1ddeaa5ee1263e1b4831c0b0d5ad0b1ffe0b42a0910bee8e9eb6f073071df3b525b19ef52f2288d4ffc545d1c988dabe2d154a16ed3be4774193f58d54fa14c2caf59bb90d19762cd5ead7e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b399000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bce792e59ef1ee78bde000000000000000000000000000000000000000000003bce792e5a2951f8e94e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000ee259dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd166d47502305520d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e5468695a6a4d354d5330784f44526a4c5455304e7a4974596a49354d5330315a6d4a6b4f4451345954466d4e6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000077354ee440e930b7a256c8a15afb5b575e490aef0000000000000000000000000000000000000000000000000de4480e9ec328730000000000000000000000000000000000000000000000000de447d47a9424df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046d26fabd31a9490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x6b3a74082556367dd14e761d00b50afc726b689fe476049bb87f3dd1bbfab818",
      "signature": {
        "s": "0x68ba256971ef21569d1b9ecda8a6bbf427c31941a7e56d0669137c0c568cfe71",
        "r": "0xe146b1adc53df34cc70121b4d2c29eafd85cd0b4bb5f0f00a8b754850f73a7bb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf7c363f62b434e1bbbf9b89f3ae254822e20167ec1ddeaa5ee1263e1b4831c0b",
      "signature": {
        "s": "0x1c988dabe2d154a16ed3be4774193f58d54fa14c2caf59bb90d19762cd5ead7e",
        "r": "0x0d5ad0b1ffe0b42a0910bee8e9eb6f073071df3b525b19ef52f2288d4ffc545d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "249715164052",
    "total": "703411437589285420076"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "249715164052",
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
            "amount": "27690178880888843358733"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "249715164"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNThiZjM5MS0xODRjLTU0NzItYjI5MS01ZmJkODQ4YTFmNjIifQ==",
    "nonce": 111513,
    "balances": {
      "current": "282428383784104303758302",
      "previous": "282428383784354268637518"
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
            "amount": "318954006971001161"
          }
        }
      ]
    },
    "wallet": "0x77354ee440e930b7a256c8a15afb5b575e490aef",
    "nonce": 46,
    "balances": {
      "current": "1001004244813424755",
      "previous": "1001003995098260703"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:42.310Z",
  "updated": "2022-05-04T08:58:42.416Z",
  "id": "627240427832e20011830d1b"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000de4480e9ec328730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1001004244813424755`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`