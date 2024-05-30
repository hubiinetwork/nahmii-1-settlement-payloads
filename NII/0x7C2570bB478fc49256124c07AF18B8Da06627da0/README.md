# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7C2570bB478fc49256124c07AF18B8Da06627da0`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000210f3cfcf5240896e000000000000000000000000000000000000000000000001e70bff85846c17090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001e70bff85846c170900000000000000000000000000000000000000000000000210f3cfcf5240896e2f0cec7e58a46c3d7524008f32d891af5865ae307bf1b3854a62cfd32398699016caf11b40a2e4cb17a215c7384edd55602c86f83a28b6be539a9e844b60908479e0f9ff61b29994f2b1201478984af5666fbd569f1ffc282400f15c97c490a3000000000000000000000000000000000000000000000000000000000000001c2dfb89bee32f2a0e6a56eea5cf30bb470b9b685f59586e257f4bf02be9771dadca26b13730e3b83fc08b6ee16760b99c69d8b7ae2d6dd5c54fb08970fca8f9ed151f7457db6fe10559b66905a97a6940d7ae81dd76c42d4a629bec3b7139bffa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012149000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002472b05972c1f571fd3d00000000000000000000000000000000000000000000247497e22161fa4183e900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007caf1a80636fa30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035930a2c3ae42a2c0ef0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a51794e574e6b4d43303059545a6d4c5455344d4445744f57526c59533078593249794e54686c596a686d4d54456966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000007c2570bb478fc49256124c07af18b8da06627da000000000000000000000000000000000000000000000000210f3cfcf5240896e00000000000000000000000000000000000000000000000029e7d049cdd4726500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f0cec7e58a46c3d7524008f32d891af5865ae307bf1b3854a62cfd323986990",
      "signature": {
        "s": "0x79e0f9ff61b29994f2b1201478984af5666fbd569f1ffc282400f15c97c490a3",
        "r": "0x16caf11b40a2e4cb17a215c7384edd55602c86f83a28b6be539a9e844b609084",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2dfb89bee32f2a0e6a56eea5cf30bb470b9b685f59586e257f4bf02be9771dad",
      "signature": {
        "s": "0x151f7457db6fe10559b66905a97a6940d7ae81dd76c42d4a629bec3b7139bffa",
        "r": "0xca26b13730e3b83fc08b6ee16760b99c69d8b7ae2d6dd5c54fb08970fca8f9ed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "35095425470132131593",
    "total": "38115036560711780718"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35095425470132131593",
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
            "amount": "15812364249782343090415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "35095425470132131"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzQyNWNkMC00YTZmLTU4MDEtOWRlYS0xY2IyNThlYjhmMTEifQ==",
    "nonce": 74057,
    "balances": {
      "current": "172120829521711091285309",
      "previous": "172155960042606693549033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7c2570bb478fc49256124c07af18b8da06627da0",
    "nonce": 2,
    "balances": {
      "current": "38115036560711780718",
      "previous": "3019611090579649125"
    }
  },
  "blockNumber": "12400708",
  "created": "2021-05-09T14:36:44.419Z",
  "updated": "2021-05-09T14:36:44.474Z",
  "id": "6097f37c4fb7c70010768b9c"
}
```
* *stageAmount*: `38115036560711780718`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001e70bff85846c17090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001e70bff85846c170900000000000000000000000000000000000000000000000210f3cfcf5240896e2f0cec7e58a46c3d7524008f32d891af5865ae307bf1b3854a62cfd32398699016caf11b40a2e4cb17a215c7384edd55602c86f83a28b6be539a9e844b60908479e0f9ff61b29994f2b1201478984af5666fbd569f1ffc282400f15c97c490a3000000000000000000000000000000000000000000000000000000000000001c2dfb89bee32f2a0e6a56eea5cf30bb470b9b685f59586e257f4bf02be9771dadca26b13730e3b83fc08b6ee16760b99c69d8b7ae2d6dd5c54fb08970fca8f9ed151f7457db6fe10559b66905a97a6940d7ae81dd76c42d4a629bec3b7139bffa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012149000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002472b05972c1f571fd3d00000000000000000000000000000000000000000000247497e22161fa4183e900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000007caf1a80636fa30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035930a2c3ae42a2c0ef0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d7a51794e574e6b4d43303059545a6d4c5455344d4445744f57526c59533078593249794e54686c596a686d4d54456966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000007c2570bb478fc49256124c07af18b8da06627da000000000000000000000000000000000000000000000000210f3cfcf5240896e00000000000000000000000000000000000000000000000029e7d049cdd4726500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2f0cec7e58a46c3d7524008f32d891af5865ae307bf1b3854a62cfd323986990",
      "signature": {
        "s": "0x79e0f9ff61b29994f2b1201478984af5666fbd569f1ffc282400f15c97c490a3",
        "r": "0x16caf11b40a2e4cb17a215c7384edd55602c86f83a28b6be539a9e844b609084",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2dfb89bee32f2a0e6a56eea5cf30bb470b9b685f59586e257f4bf02be9771dad",
      "signature": {
        "s": "0x151f7457db6fe10559b66905a97a6940d7ae81dd76c42d4a629bec3b7139bffa",
        "r": "0xca26b13730e3b83fc08b6ee16760b99c69d8b7ae2d6dd5c54fb08970fca8f9ed",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "35095425470132131593",
    "total": "38115036560711780718"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35095425470132131593",
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
            "amount": "15812364249782343090415"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "35095425470132131"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMzQyNWNkMC00YTZmLTU4MDEtOWRlYS0xY2IyNThlYjhmMTEifQ==",
    "nonce": 74057,
    "balances": {
      "current": "172120829521711091285309",
      "previous": "172155960042606693549033"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7c2570bb478fc49256124c07af18b8da06627da0",
    "nonce": 2,
    "balances": {
      "current": "38115036560711780718",
      "previous": "3019611090579649125"
    }
  },
  "blockNumber": "12400708",
  "created": "2021-05-09T14:36:44.419Z",
  "updated": "2021-05-09T14:36:44.474Z",
  "id": "6097f37c4fb7c70010768b9c"
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
0x0f200f9b00000000000000000000000000000000000000000000000210f3cfcf5240896e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `38115036560711780718`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`