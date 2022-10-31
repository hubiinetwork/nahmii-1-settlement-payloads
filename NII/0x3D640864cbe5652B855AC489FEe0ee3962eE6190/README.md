# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x3D640864cbe5652B855AC489FEe0ee3962eE6190`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b7262971bdfd0000000000000000000000000000000000000000000000000000000cb9aea4360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000cb9aea43600000000000000000000000000000000000000000000018f4c811fa45d33c00c9174e9e6a03b0c3186e3759f9b5962bf435b7ad31945684cd0eb2291e0439984bb13115321109b0f373b27dc19dc7d1b0964b8b24014da96f7fb6c7e1a0308c253f0f77a67ad3a152f299725065a3a3698bdde6354120e9bbeb7b51e9c258cd8000000000000000000000000000000000000000000000000000000000000001b4e381ab2cbd2ce21d401b2f7bf2eb64030269011c9466dffc7d01bedcd8aee894bba956c161490749c75e06c8373d72321422270cdd15b48ad977b187eca2f505f1097a51a84801c473f45735c7dc4fb9531fdb544af779e03dea14c48d15f79000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b365000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bdf6e0c1a63000000000000000000000000000000000000000000003c8863632bec2afcb60e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000341f7750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556ccbbba14a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f544d79593249354e4331694e47597a4c5455355a444574596d4d31597930325a545a694d6d51324d475a6b4e7a516966513d3d000000000000000000000000000000000000000000000000000000000000002c0000000000000000000000003d640864cbe5652b855ac489fee0ee3962ee61900000000000000000000000000000000000000000000000000de0b7262971bdfd0000000000000000000000000000000000000000000000000de0b7196fc319c700000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001a9dbfff18caaa000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x9174e9e6a03b0c3186e3759f9b5962bf435b7ad31945684cd0eb2291e0439984",
      "signature": {
        "s": "0x53f0f77a67ad3a152f299725065a3a3698bdde6354120e9bbeb7b51e9c258cd8",
        "r": "0xbb13115321109b0f373b27dc19dc7d1b0964b8b24014da96f7fb6c7e1a0308c2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4e381ab2cbd2ce21d401b2f7bf2eb64030269011c9466dffc7d01bedcd8aee89",
      "signature": {
        "s": "0x5f1097a51a84801c473f45735c7dc4fb9531fdb544af779e03dea14c48d15f79",
        "r": "0x4bba956c161490749c75e06c8373d72321422270cdd15b48ad977b187eca2f50",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "54654837814",
    "total": "7365763607619788062732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54654837814",
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
            "amount": "27686752782988573647178"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "54654837"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTMyY2I5NC1iNGYzLTU5ZDEtYmM1Yy02ZTZiMmQ2MGZkNzQifQ==",
    "nonce": 111461,
    "balances": {
      "current": "285857907782274285050467",
      "previous": "285857907782328994543118"
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
            "amount": "1917900118683200000"
          }
        }
      ]
    },
    "wallet": "0x3d640864cbe5652b855ac489fee0ee3962ee6190",
    "nonce": 44,
    "balances": {
      "current": "1000000491808210429",
      "previous": "1000000437153372615"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:26.029Z",
  "updated": "2022-05-04T08:58:26.095Z",
  "id": "62724032bbd75600116d06ad"
}
```
* *stageAmount*: `1000000491808210429`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000000000000cb9aea4360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000cb9aea43600000000000000000000000000000000000000000000018f4c811fa45d33c00c9174e9e6a03b0c3186e3759f9b5962bf435b7ad31945684cd0eb2291e0439984bb13115321109b0f373b27dc19dc7d1b0964b8b24014da96f7fb6c7e1a0308c253f0f77a67ad3a152f299725065a3a3698bdde6354120e9bbeb7b51e9c258cd8000000000000000000000000000000000000000000000000000000000000001b4e381ab2cbd2ce21d401b2f7bf2eb64030269011c9466dffc7d01bedcd8aee894bba956c161490749c75e06c8373d72321422270cdd15b48ad977b187eca2f505f1097a51a84801c473f45735c7dc4fb9531fdb544af779e03dea14c48d15f79000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b365000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003c8863632bdf6e0c1a63000000000000000000000000000000000000000000003c8863632bec2afcb60e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000341f7750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dce6e1556ccbbba14a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f544d79593249354e4331694e47597a4c5455355a444574596d4d31597930325a545a694d6d51324d475a6b4e7a516966513d3d000000000000000000000000000000000000000000000000000000000000002c0000000000000000000000003d640864cbe5652b855ac489fee0ee3962ee61900000000000000000000000000000000000000000000000000de0b7262971bdfd0000000000000000000000000000000000000000000000000de0b7196fc319c700000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001a9dbfff18caaa000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x9174e9e6a03b0c3186e3759f9b5962bf435b7ad31945684cd0eb2291e0439984",
      "signature": {
        "s": "0x53f0f77a67ad3a152f299725065a3a3698bdde6354120e9bbeb7b51e9c258cd8",
        "r": "0xbb13115321109b0f373b27dc19dc7d1b0964b8b24014da96f7fb6c7e1a0308c2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4e381ab2cbd2ce21d401b2f7bf2eb64030269011c9466dffc7d01bedcd8aee89",
      "signature": {
        "s": "0x5f1097a51a84801c473f45735c7dc4fb9531fdb544af779e03dea14c48d15f79",
        "r": "0x4bba956c161490749c75e06c8373d72321422270cdd15b48ad977b187eca2f50",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "54654837814",
    "total": "7365763607619788062732"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "54654837814",
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
            "amount": "27686752782988573647178"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "54654837"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTMyY2I5NC1iNGYzLTU5ZDEtYmM1Yy02ZTZiMmQ2MGZkNzQifQ==",
    "nonce": 111461,
    "balances": {
      "current": "285857907782274285050467",
      "previous": "285857907782328994543118"
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
            "amount": "1917900118683200000"
          }
        }
      ]
    },
    "wallet": "0x3d640864cbe5652b855ac489fee0ee3962ee6190",
    "nonce": 44,
    "balances": {
      "current": "1000000491808210429",
      "previous": "1000000437153372615"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:26.029Z",
  "updated": "2022-05-04T08:58:26.095Z",
  "id": "62724032bbd75600116d06ad"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b7262971bdfd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1000000491808210429`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`