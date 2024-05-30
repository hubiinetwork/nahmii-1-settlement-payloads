# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x067134Eaf65E507Aa066BA58443DA431E2d81F27`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000084054de8fbcb1e17000000000000000000000000000000000000000000000000000000001cee59f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001cee59f300000000000000000000000000000000000000000000000000000002a330a151d3935f219db3827054ab9663ed281846cf6cb4a347a942885fbc535b5aead0be7e90fb5f8f1a73ad5f2b42e01af9aa1d40dfbec2a2aadb60ad491088f97cd2a5070ce838dacd9a527672102c67ef96784f46f7e6b26b865898e85d5d30375e7b000000000000000000000000000000000000000000000000000000000000001c19359e1c6f30db05dbbbe4c330bdc64033b08479a7bf26ab9e6dea81076d8c054b4de5674d671d6f085d3b5a3f38839f31c6df5eb62d8c170c15523880f6a93522fad0e95f7d34877c7f5916d53f729aae24ff732d7be192d38cddb9b1c04fba000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b439000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039cd11b3aac3912cb31b0000000000000000000000000000000000000000000039cd11b3aac3ae22751400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000768060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd99ba1fd900e483d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a475130596a51345979316b4e44566b4c54553059324574596d49324d69316d5a546c6d4d4464684d544a6c4d546b6966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000067134eaf65e507aa066ba58443da431e2d81f2700000000000000000000000000000000000000000000000084054de8fbcb1e1700000000000000000000000000000000000000000000000084054de8dedcc42400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd3935f219db3827054ab9663ed281846cf6cb4a347a942885fbc535b5aead0be",
      "signature": {
        "s": "0x070ce838dacd9a527672102c67ef96784f46f7e6b26b865898e85d5d30375e7b",
        "r": "0x7e90fb5f8f1a73ad5f2b42e01af9aa1d40dfbec2a2aadb60ad491088f97cd2a5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x19359e1c6f30db05dbbbe4c330bdc64033b08479a7bf26ab9e6dea81076d8c05",
      "signature": {
        "s": "0x22fad0e95f7d34877c7f5916d53f729aae24ff732d7be192d38cddb9b1c04fba",
        "r": "0x4b4de5674d671d6f085d3b5a3f38839f31c6df5eb62d8c170c15523880f6a935",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "485382643",
    "total": "11327807825"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "485382643",
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
            "amount": "27699640055888391472085"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "485382"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZGQ0YjQ4Yy1kNDVkLTU0Y2EtYmI2Mi1mZTlmMDdhMTJlMTkifQ==",
    "nonce": 111673,
    "balances": {
      "current": "272957747609556642214683",
      "previous": "272957747609557128082708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x067134eaf65e507aa066ba58443da431e2d81f27",
    "nonce": 30,
    "balances": {
      "current": "9513095450942184983",
      "previous": "9513095450456802340"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:33.496Z",
  "updated": "2022-05-04T08:59:33.604Z",
  "id": "627240753592fd001130b682"
}
```
* *stageAmount*: `9513095450942184983`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001cee59f30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001cee59f300000000000000000000000000000000000000000000000000000002a330a151d3935f219db3827054ab9663ed281846cf6cb4a347a942885fbc535b5aead0be7e90fb5f8f1a73ad5f2b42e01af9aa1d40dfbec2a2aadb60ad491088f97cd2a5070ce838dacd9a527672102c67ef96784f46f7e6b26b865898e85d5d30375e7b000000000000000000000000000000000000000000000000000000000000001c19359e1c6f30db05dbbbe4c330bdc64033b08479a7bf26ab9e6dea81076d8c054b4de5674d671d6f085d3b5a3f38839f31c6df5eb62d8c170c15523880f6a93522fad0e95f7d34877c7f5916d53f729aae24ff732d7be192d38cddb9b1c04fba000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b439000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039cd11b3aac3912cb31b0000000000000000000000000000000000000000000039cd11b3aac3ae22751400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000768060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd99ba1fd900e483d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a475130596a51345979316b4e44566b4c54553059324574596d49324d69316d5a546c6d4d4464684d544a6c4d546b6966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000067134eaf65e507aa066ba58443da431e2d81f2700000000000000000000000000000000000000000000000084054de8fbcb1e1700000000000000000000000000000000000000000000000084054de8dedcc42400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd3935f219db3827054ab9663ed281846cf6cb4a347a942885fbc535b5aead0be",
      "signature": {
        "s": "0x070ce838dacd9a527672102c67ef96784f46f7e6b26b865898e85d5d30375e7b",
        "r": "0x7e90fb5f8f1a73ad5f2b42e01af9aa1d40dfbec2a2aadb60ad491088f97cd2a5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x19359e1c6f30db05dbbbe4c330bdc64033b08479a7bf26ab9e6dea81076d8c05",
      "signature": {
        "s": "0x22fad0e95f7d34877c7f5916d53f729aae24ff732d7be192d38cddb9b1c04fba",
        "r": "0x4b4de5674d671d6f085d3b5a3f38839f31c6df5eb62d8c170c15523880f6a935",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "485382643",
    "total": "11327807825"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "485382643",
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
            "amount": "27699640055888391472085"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "485382"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxZGQ0YjQ4Yy1kNDVkLTU0Y2EtYmI2Mi1mZTlmMDdhMTJlMTkifQ==",
    "nonce": 111673,
    "balances": {
      "current": "272957747609556642214683",
      "previous": "272957747609557128082708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x067134eaf65e507aa066ba58443da431e2d81f27",
    "nonce": 30,
    "balances": {
      "current": "9513095450942184983",
      "previous": "9513095450456802340"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:33.496Z",
  "updated": "2022-05-04T08:59:33.604Z",
  "id": "627240753592fd001130b682"
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
0x0f200f9b00000000000000000000000000000000000000000000000084054de8fbcb1e170000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9513095450942184983`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`