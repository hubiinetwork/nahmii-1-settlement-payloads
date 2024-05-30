# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7Fa53eCE171EeE69c9E28F03D360A1132874eBe9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000a6d795def1036f66d0000000000000000000000000000000000000000000000012130920dbe9a97680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000012130920dbe9a976800000000000000000000000000000000000000000000000a6d795def1036f66df0ce62ad9199871402495db8c675bf1070b83ca9f5333b7743cd4926eecc44bca14695f89240e3a57aa06c15fb81f32d1ca1d04b0574d32c2ca65c0ba4f4d23d12c0e8e3203410fd5c2643d2f715c77253b55e46cfa10e25ef137fa36bdf130a000000000000000000000000000000000000000000000000000000000000001b201090f3967f3535bc3fb96aa9f78c5b567b5f6cf19229c1c34e5b2176c99a8f99506c72107b8216cfe9237bee78121b0629aca2ce333115f0bbc4a2824720b005622720b160168b7832d02d772a10605298b7d8f13f13f117590cf8904ce01e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000b0d2740000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000f28d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023f931b27c37bebeb20b0000000000000000000000000000000000000000000023fa532d169c08090eb800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000004a08568aafc5450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000280b0030828b7b0942b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e4745354d44677a5a53316a5a474a694c5455315a475174596a55354d69316959574e6d4e6a52694f4759334f54496966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000007fa53ece171eee69c9e28f03d360a1132874ebe900000000000000000000000000000000000000000000000a6d795def1036f66d0000000000000000000000000000000000000000000000094c48cbe1519c5f0500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0ce62ad9199871402495db8c675bf1070b83ca9f5333b7743cd4926eecc44bc",
      "signature": {
        "s": "0x12c0e8e3203410fd5c2643d2f715c77253b55e46cfa10e25ef137fa36bdf130a",
        "r": "0xa14695f89240e3a57aa06c15fb81f32d1ca1d04b0574d32c2ca65c0ba4f4d23d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x201090f3967f3535bc3fb96aa9f78c5b567b5f6cf19229c1c34e5b2176c99a8f",
      "signature": {
        "s": "0x05622720b160168b7832d02d772a10605298b7d8f13f13f117590cf8904ce01e",
        "r": "0x99506c72107b8216cfe9237bee78121b0629aca2ce333115f0bbc4a2824720b0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20838316063573317480",
    "total": "192355880240762254957"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20838316063573317480",
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
            "amount": "11818599197120691999787"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20838316063573317"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNGE5MDgzZS1jZGJiLTU1ZGQtYjU5Mi1iYWNmNjRiOGY3OTIifQ==",
    "nonce": 62093,
    "balances": {
      "current": "169879647236023839011339",
      "previous": "169900506390403475902136"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7fa53ece171eee69c9e28f03d360a1132874ebe9",
    "nonce": 8,
    "balances": {
      "current": "192355880240762254957",
      "previous": "171517564177188937477"
    }
  },
  "blockNumber": "11588212",
  "created": "2021-01-04T13:26:24.316Z",
  "updated": "2021-01-04T13:26:24.408Z",
  "id": "5ff3178051d7830010241ee9"
}
```
* *stageAmount*: `192355880240762254957`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000012130920dbe9a97680000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000012130920dbe9a976800000000000000000000000000000000000000000000000a6d795def1036f66df0ce62ad9199871402495db8c675bf1070b83ca9f5333b7743cd4926eecc44bca14695f89240e3a57aa06c15fb81f32d1ca1d04b0574d32c2ca65c0ba4f4d23d12c0e8e3203410fd5c2643d2f715c77253b55e46cfa10e25ef137fa36bdf130a000000000000000000000000000000000000000000000000000000000000001b201090f3967f3535bc3fb96aa9f78c5b567b5f6cf19229c1c34e5b2176c99a8f99506c72107b8216cfe9237bee78121b0629aca2ce333115f0bbc4a2824720b005622720b160168b7832d02d772a10605298b7d8f13f13f117590cf8904ce01e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000b0d2740000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000f28d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023f931b27c37bebeb20b0000000000000000000000000000000000000000000023fa532d169c08090eb800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000004a08568aafc5450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000280b0030828b7b0942b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e4745354d44677a5a53316a5a474a694c5455315a475174596a55354d69316959574e6d4e6a52694f4759334f54496966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000007fa53ece171eee69c9e28f03d360a1132874ebe900000000000000000000000000000000000000000000000a6d795def1036f66d0000000000000000000000000000000000000000000000094c48cbe1519c5f0500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0ce62ad9199871402495db8c675bf1070b83ca9f5333b7743cd4926eecc44bc",
      "signature": {
        "s": "0x12c0e8e3203410fd5c2643d2f715c77253b55e46cfa10e25ef137fa36bdf130a",
        "r": "0xa14695f89240e3a57aa06c15fb81f32d1ca1d04b0574d32c2ca65c0ba4f4d23d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x201090f3967f3535bc3fb96aa9f78c5b567b5f6cf19229c1c34e5b2176c99a8f",
      "signature": {
        "s": "0x05622720b160168b7832d02d772a10605298b7d8f13f13f117590cf8904ce01e",
        "r": "0x99506c72107b8216cfe9237bee78121b0629aca2ce333115f0bbc4a2824720b0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "20838316063573317480",
    "total": "192355880240762254957"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "20838316063573317480",
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
            "amount": "11818599197120691999787"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "20838316063573317"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNGE5MDgzZS1jZGJiLTU1ZGQtYjU5Mi1iYWNmNjRiOGY3OTIifQ==",
    "nonce": 62093,
    "balances": {
      "current": "169879647236023839011339",
      "previous": "169900506390403475902136"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7fa53ece171eee69c9e28f03d360a1132874ebe9",
    "nonce": 8,
    "balances": {
      "current": "192355880240762254957",
      "previous": "171517564177188937477"
    }
  },
  "blockNumber": "11588212",
  "created": "2021-01-04T13:26:24.316Z",
  "updated": "2021-01-04T13:26:24.408Z",
  "id": "5ff3178051d7830010241ee9"
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
0x0f200f9b00000000000000000000000000000000000000000000000a6d795def1036f66d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `192355880240762254957`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`