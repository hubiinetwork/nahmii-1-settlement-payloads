# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x860dE17415A13EEF864baa3e57b0D4EE42356D0e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000017db2474f17fc98ed000000000000000000000000000000000000000000000000d97b9e323fc55c620000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d97b9e323fc55c620000000000000000000000000000000000000000000000017db2474f17fc98edf794158f6e89a324de23fc99cce669a5de3b0e502498123994b40fb349ab0d64dcadcb70d0336b34777e21fd2dc052c3d8e5019c5e38f9805359d50ccdd8b3030c9a4f789e1d5cd0a10e23dff2477070e03bba3c3465caafad9767c5be43a461000000000000000000000000000000000000000000000000000000000000001bb9bb53b5f22e80af4e3053c35842e56eaecb4232d7ecc8cc6792bd79bbe07fc553b6046ae941e53acb560c242d74aae8e60ca913545e8ff075375805c9dc212077397faae7f6446076a30ec3bb7bfd60fbf0b84d0db9ac3bf0d759fc703bf7aa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf9700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a69000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022a931ac4e7ea206fca30000000000000000000000000000000000000000000022aa0b5f99a62e2666ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000037acf54c5a0da90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5f57c38beea0aa4af0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e4759785a4449324d79316a4e6a4a684c5455795a47597459574579596930314e6d497a4d6a4d77597a55345a54496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000860de17415a13eef864baa3e57b0d4ee42356d0e0000000000000000000000000000000000000000000000017db2474f17fc98ed000000000000000000000000000000000000000000000000a436a91cd8373c8b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf794158f6e89a324de23fc99cce669a5de3b0e502498123994b40fb349ab0d64",
      "signature": {
        "s": "0x0c9a4f789e1d5cd0a10e23dff2477070e03bba3c3465caafad9767c5be43a461",
        "r": "0xdcadcb70d0336b34777e21fd2dc052c3d8e5019c5e38f9805359d50ccdd8b303",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9bb53b5f22e80af4e3053c35842e56eaecb4232d7ecc8cc6792bd79bbe07fc5",
      "signature": {
        "s": "0x77397faae7f6446076a30ec3bb7bfd60fbf0b84d0db9ac3bf0d759fc703bf7aa",
        "r": "0x53b6046ae941e53acb560c242d74aae8e60ca913545e8ff075375805c9dc2120",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15671293267021225058",
    "total": "27504124279335459053"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15671293267021225058",
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
            "amount": "17818797106958743282863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15671293267021225"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NGYxZDI2My1jNjJhLTUyZGYtYWEyYi01NmIzMjMwYzU4ZTIifQ==",
    "nonce": 80489,
    "balances": {
      "current": "163681539488134495403171",
      "previous": "163697226452694783649454"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x860de17415a13eef864baa3e57b0d4ee42356d0e",
    "nonce": 2,
    "balances": {
      "current": "27504124279335459053",
      "previous": "11832831012314233995"
    }
  },
  "blockNumber": "12767127",
  "created": "2021-07-05T11:15:43.049Z",
  "updated": "2021-07-05T11:15:43.141Z",
  "id": "60e2e9dfabca510010d04491"
}
```
* *stageAmount*: `27504124279335459053`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000d97b9e323fc55c620000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d97b9e323fc55c620000000000000000000000000000000000000000000000017db2474f17fc98edf794158f6e89a324de23fc99cce669a5de3b0e502498123994b40fb349ab0d64dcadcb70d0336b34777e21fd2dc052c3d8e5019c5e38f9805359d50ccdd8b3030c9a4f789e1d5cd0a10e23dff2477070e03bba3c3465caafad9767c5be43a461000000000000000000000000000000000000000000000000000000000000001bb9bb53b5f22e80af4e3053c35842e56eaecb4232d7ecc8cc6792bd79bbe07fc553b6046ae941e53acb560c242d74aae8e60ca913545e8ff075375805c9dc212077397faae7f6446076a30ec3bb7bfd60fbf0b84d0db9ac3bf0d759fc703bf7aa000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c2cf9700000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a69000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022a931ac4e7ea206fca30000000000000000000000000000000000000000000022aa0b5f99a62e2666ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000037acf54c5a0da90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5f57c38beea0aa4af0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e4759785a4449324d79316a4e6a4a684c5455795a47597459574579596930314e6d497a4d6a4d77597a55345a54496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000860de17415a13eef864baa3e57b0d4ee42356d0e0000000000000000000000000000000000000000000000017db2474f17fc98ed000000000000000000000000000000000000000000000000a436a91cd8373c8b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf794158f6e89a324de23fc99cce669a5de3b0e502498123994b40fb349ab0d64",
      "signature": {
        "s": "0x0c9a4f789e1d5cd0a10e23dff2477070e03bba3c3465caafad9767c5be43a461",
        "r": "0xdcadcb70d0336b34777e21fd2dc052c3d8e5019c5e38f9805359d50ccdd8b303",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb9bb53b5f22e80af4e3053c35842e56eaecb4232d7ecc8cc6792bd79bbe07fc5",
      "signature": {
        "s": "0x77397faae7f6446076a30ec3bb7bfd60fbf0b84d0db9ac3bf0d759fc703bf7aa",
        "r": "0x53b6046ae941e53acb560c242d74aae8e60ca913545e8ff075375805c9dc2120",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15671293267021225058",
    "total": "27504124279335459053"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15671293267021225058",
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
            "amount": "17818797106958743282863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15671293267021225"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5NGYxZDI2My1jNjJhLTUyZGYtYWEyYi01NmIzMjMwYzU4ZTIifQ==",
    "nonce": 80489,
    "balances": {
      "current": "163681539488134495403171",
      "previous": "163697226452694783649454"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x860de17415a13eef864baa3e57b0d4ee42356d0e",
    "nonce": 2,
    "balances": {
      "current": "27504124279335459053",
      "previous": "11832831012314233995"
    }
  },
  "blockNumber": "12767127",
  "created": "2021-07-05T11:15:43.049Z",
  "updated": "2021-07-05T11:15:43.141Z",
  "id": "60e2e9dfabca510010d04491"
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
0x0f200f9b0000000000000000000000000000000000000000000000017db2474f17fc98ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `27504124279335459053`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`