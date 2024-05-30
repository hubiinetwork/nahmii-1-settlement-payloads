# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x870eF949FD58929a4a4Dc815Dd2C8Ac97A94cC8b`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000030394c04909b00150000000000000000000000000000000000000000000000000000000019eb4205d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019eb4205d00000000000000000000000000000000000000000000000000000025ce7fab66ffa63dc9d1f8f5850b8a1c83cd97f33fdea9ba26e5fac23c874eda018d972d7fa6b621634f571491e5f414ec00af52620122590560033a3bfd08fff5cc80e248263bfa3dc06b17de21252802ded9d5bd5ef0216a126d40f1bcde236936d6ed20000000000000000000000000000000000000000000000000000000000000001b587011daa81a9e3ea36b54be3fd4465aa3bcd60ea409e4f68baf127675954e70132d0ba577fbcf4cbfc6336120b246221709f6161cfc997ac373a829ee29bc037a1db7bc821d1b1ddfa20ce4f1514724c99dcb367a0bb11869e885185af54369000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b736000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002db33c31a80e8d34eef3000000000000000000000000000000000000000000002db33c31a8102c53395400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006a2a040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b1faf5241e0d2a0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a546c6a4e44517a4d4330354f474d334c5456684e3251744f544a694e7930774d4749784d324e6a4e6d51334f44636966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000870ef949fd58929a4a4dc815dd2c8ac97a94cc8b0000000000000000000000000000000000000000000000030394c04909b001500000000000000000000000000000000000000000000000030394c0476afbe0f300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffa63dc9d1f8f5850b8a1c83cd97f33fdea9ba26e5fac23c874eda018d972d7f",
      "signature": {
        "s": "0x263bfa3dc06b17de21252802ded9d5bd5ef0216a126d40f1bcde236936d6ed20",
        "r": "0xa6b621634f571491e5f414ec00af52620122590560033a3bfd08fff5cc80e248",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x587011daa81a9e3ea36b54be3fd4465aa3bcd60ea409e4f68baf127675954e70",
      "signature": {
        "s": "0x7a1db7bc821d1b1ddfa20ce4f1514724c99dcb367a0bb11869e885185af54369",
        "r": "0x132d0ba577fbcf4cbfc6336120b246221709f6161cfc997ac373a829ee29bc03",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6957572189",
    "total": "162378263398"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6957572189",
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
            "amount": "27756727919283528346123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6957572"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZTljNDQzMC05OGM3LTVhN2QtOTJiNy0wMGIxM2NjNmQ3ODcifQ==",
    "nonce": 112438,
    "balances": {
      "current": "215812796351024630918899",
      "previous": "215812796351031595448660"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x870ef949fd58929a4a4dc815dd2c8ac97a94cc8b",
    "nonce": 36,
    "balances": {
      "current": "55598274719723290960",
      "previous": "55598274712765718771"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:47.769Z",
  "updated": "2022-05-04T09:03:47.873Z",
  "id": "627241733592fd001130b78b"
}
```
* *stageAmount*: `55598274719723290960`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000019eb4205d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000019eb4205d00000000000000000000000000000000000000000000000000000025ce7fab66ffa63dc9d1f8f5850b8a1c83cd97f33fdea9ba26e5fac23c874eda018d972d7fa6b621634f571491e5f414ec00af52620122590560033a3bfd08fff5cc80e248263bfa3dc06b17de21252802ded9d5bd5ef0216a126d40f1bcde236936d6ed20000000000000000000000000000000000000000000000000000000000000001b587011daa81a9e3ea36b54be3fd4465aa3bcd60ea409e4f68baf127675954e70132d0ba577fbcf4cbfc6336120b246221709f6161cfc997ac373a829ee29bc037a1db7bc821d1b1ddfa20ce4f1514724c99dcb367a0bb11869e885185af54369000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b736000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002db33c31a80e8d34eef3000000000000000000000000000000000000000000002db33c31a8102c53395400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006a2a040000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b1faf5241e0d2a0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a546c6a4e44517a4d4330354f474d334c5456684e3251744f544a694e7930774d4749784d324e6a4e6d51334f44636966513d3d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000870ef949fd58929a4a4dc815dd2c8ac97a94cc8b0000000000000000000000000000000000000000000000030394c04909b001500000000000000000000000000000000000000000000000030394c0476afbe0f300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffa63dc9d1f8f5850b8a1c83cd97f33fdea9ba26e5fac23c874eda018d972d7f",
      "signature": {
        "s": "0x263bfa3dc06b17de21252802ded9d5bd5ef0216a126d40f1bcde236936d6ed20",
        "r": "0xa6b621634f571491e5f414ec00af52620122590560033a3bfd08fff5cc80e248",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x587011daa81a9e3ea36b54be3fd4465aa3bcd60ea409e4f68baf127675954e70",
      "signature": {
        "s": "0x7a1db7bc821d1b1ddfa20ce4f1514724c99dcb367a0bb11869e885185af54369",
        "r": "0x132d0ba577fbcf4cbfc6336120b246221709f6161cfc997ac373a829ee29bc03",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6957572189",
    "total": "162378263398"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6957572189",
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
            "amount": "27756727919283528346123"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6957572"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZTljNDQzMC05OGM3LTVhN2QtOTJiNy0wMGIxM2NjNmQ3ODcifQ==",
    "nonce": 112438,
    "balances": {
      "current": "215812796351024630918899",
      "previous": "215812796351031595448660"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x870ef949fd58929a4a4dc815dd2c8ac97a94cc8b",
    "nonce": 36,
    "balances": {
      "current": "55598274719723290960",
      "previous": "55598274712765718771"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:47.769Z",
  "updated": "2022-05-04T09:03:47.873Z",
  "id": "627241733592fd001130b78b"
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
0x0f200f9b0000000000000000000000000000000000000000000000030394c04909b001500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `55598274719723290960`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`