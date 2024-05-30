# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1F56e6269790D3Ef1135d1a3eF7AcBEcF4517731`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000bd9ab8c33196d736c00000000000000000000000000000000000000000000000464bd60db2eb5690d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000464bd60db2eb5690d00000000000000000000000000000000000000000000000bd9ab8c33196d736c06da50037daef194d905b4caa8de1b5ce9059c1dab99dce91099488dd8e368f63d0354510b505c51c1e895b2cecd111069bada327e97b285ba9178e3478ed3247a8a040aa1c0ccc2d6981d9657114695e72270cfb894c5b207df42ebfc64023b000000000000000000000000000000000000000000000000000000000000001cc4a9bf50a58887f1d7a9a6aded9cb382a34b825416b8cce79e3ab7b9f6148fb8528b8d08a446ff02aec5077681fdf023843a85fa0a3a83079ff287dd6232adf92ba63c6ce103497491e6d0a6070b37950da40716964a2808cb23546ade1a0e1f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000d7741500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000015f27000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000299d8e7303176ba291320000000000000000000000000000000000000000000029a1f45052e47c70391200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000011feef1e2183ed30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000466a5f07ebdf075d4430000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e7a55355a4745345a69316b5a6d4e6c4c5455334e4751744f474578597930344e7a6c684e446b784d6d56684d54516966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000001f56e6269790d3ef1135d1a3ef7acbecf451773100000000000000000000000000000000000000000000000bd9ab8c33196d736c00000000000000000000000000000000000000000000000774ee2b57eab80a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x06da50037daef194d905b4caa8de1b5ce9059c1dab99dce91099488dd8e368f6",
      "signature": {
        "s": "0x7a8a040aa1c0ccc2d6981d9657114695e72270cfb894c5b207df42ebfc64023b",
        "r": "0x3d0354510b505c51c1e895b2cecd111069bada327e97b285ba9178e3478ed324",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc4a9bf50a58887f1d7a9a6aded9cb382a34b825416b8cce79e3ab7b9f6148fb8",
      "signature": {
        "s": "0x2ba63c6ce103497491e6d0a6070b37950da40716964a2808cb23546ade1a0e1f",
        "r": "0x528b8d08a446ff02aec5077681fdf023843a85fa0a3a83079ff287dd6232adf9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "81046040963727059213",
    "total": "218598969089150776172"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81046040963727059213",
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
            "amount": "20782991023361871959107"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "81046040963727059"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2NzU5ZGE4Zi1kZmNlLTU3NGQtOGExYy04NzlhNDkxMmVhMTQifQ==",
    "nonce": 89895,
    "balances": {
      "current": "196523429168602685804850",
      "previous": "196604556255607376591122"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f56e6269790d3ef1135d1a3ef7acbecf4517731",
    "nonce": 3,
    "balances": {
      "current": "218598969089150776172",
      "previous": "137552928125423716959"
    }
  },
  "blockNumber": "14119957",
  "created": "2022-02-01T11:58:32.398Z",
  "updated": "2022-02-01T11:58:32.508Z",
  "id": "61f92068b7e258001221f32c"
}
```
* *stageAmount*: `218598969089150776172`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000464bd60db2eb5690d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000464bd60db2eb5690d00000000000000000000000000000000000000000000000bd9ab8c33196d736c06da50037daef194d905b4caa8de1b5ce9059c1dab99dce91099488dd8e368f63d0354510b505c51c1e895b2cecd111069bada327e97b285ba9178e3478ed3247a8a040aa1c0ccc2d6981d9657114695e72270cfb894c5b207df42ebfc64023b000000000000000000000000000000000000000000000000000000000000001cc4a9bf50a58887f1d7a9a6aded9cb382a34b825416b8cce79e3ab7b9f6148fb8528b8d08a446ff02aec5077681fdf023843a85fa0a3a83079ff287dd6232adf92ba63c6ce103497491e6d0a6070b37950da40716964a2808cb23546ade1a0e1f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000d7741500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000015f27000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000299d8e7303176ba291320000000000000000000000000000000000000000000029a1f45052e47c70391200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000011feef1e2183ed30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000466a5f07ebdf075d4430000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e7a55355a4745345a69316b5a6d4e6c4c5455334e4751744f474578597930344e7a6c684e446b784d6d56684d54516966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000001f56e6269790d3ef1135d1a3ef7acbecf451773100000000000000000000000000000000000000000000000bd9ab8c33196d736c00000000000000000000000000000000000000000000000774ee2b57eab80a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x06da50037daef194d905b4caa8de1b5ce9059c1dab99dce91099488dd8e368f6",
      "signature": {
        "s": "0x7a8a040aa1c0ccc2d6981d9657114695e72270cfb894c5b207df42ebfc64023b",
        "r": "0x3d0354510b505c51c1e895b2cecd111069bada327e97b285ba9178e3478ed324",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc4a9bf50a58887f1d7a9a6aded9cb382a34b825416b8cce79e3ab7b9f6148fb8",
      "signature": {
        "s": "0x2ba63c6ce103497491e6d0a6070b37950da40716964a2808cb23546ade1a0e1f",
        "r": "0x528b8d08a446ff02aec5077681fdf023843a85fa0a3a83079ff287dd6232adf9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "81046040963727059213",
    "total": "218598969089150776172"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "81046040963727059213",
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
            "amount": "20782991023361871959107"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "81046040963727059"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2NzU5ZGE4Zi1kZmNlLTU3NGQtOGExYy04NzlhNDkxMmVhMTQifQ==",
    "nonce": 89895,
    "balances": {
      "current": "196523429168602685804850",
      "previous": "196604556255607376591122"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f56e6269790d3ef1135d1a3ef7acbecf4517731",
    "nonce": 3,
    "balances": {
      "current": "218598969089150776172",
      "previous": "137552928125423716959"
    }
  },
  "blockNumber": "14119957",
  "created": "2022-02-01T11:58:32.398Z",
  "updated": "2022-02-01T11:58:32.508Z",
  "id": "61f92068b7e258001221f32c"
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
0x0f200f9b00000000000000000000000000000000000000000000000bd9ab8c33196d736c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `218598969089150776172`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`