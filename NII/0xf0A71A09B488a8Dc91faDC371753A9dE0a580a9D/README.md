# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf0A71A09B488a8Dc91faDC371753A9dE0a580a9D`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000400ff6383686a31a1000000000000000000000000000000000000000000000000171e9bb1fcb6b7f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000171e9bb1fcb6b7f800000000000000000000000000000000000000000000000288c1e677fd4c5bdd54ab0f1039c808fd5147cfe9490b616f93db64fe162a95fd4a19098922b6b14e76cc7bdbe40a18c25a9319b3991400fcfa119567a8c63eb2316c8682d2c694de173878b84bb86c3a830cf425691a9d32ff1abc8617073ac781c388357c8791bf000000000000000000000000000000000000000000000000000000000000001b8fbd964433f95a8e2ea7f839aaff0702b4275de3433148ee05570322a0d7ab44da22d43c4f26068436714997e612740990dda72b49ab82c9094e37f722636d0e13e4d13fbba570ac47c515a7571bb50ad8d66d4e11919f095435ea8fa6b35f20000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d78b2e1d59392d8b6b0000000000000000000000000000000000000000000095d7a252a4351dd309b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005eb29e7eec6530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60fc2710f53d77b5c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a63774e446332595330784d444d774c54553459325974595459784f53316b4d5467314d7a646b5a6a426d4e54596966513d3d0000000000000000000000000000000000000000000000000000000000000032000000000000000000000000f0a71a09b488a8dc91fadc371753a9de0a580a9d00000000000000000000000000000000000000000000000400ff6383686a31a1000000000000000000000000000000000000000000000003e9e0c7d16bb379a900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x54ab0f1039c808fd5147cfe9490b616f93db64fe162a95fd4a19098922b6b14e",
      "signature": {
        "s": "0x173878b84bb86c3a830cf425691a9d32ff1abc8617073ac781c388357c8791bf",
        "r": "0x76cc7bdbe40a18c25a9319b3991400fcfa119567a8c63eb2316c8682d2c694de",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8fbd964433f95a8e2ea7f839aaff0702b4275de3433148ee05570322a0d7ab44",
      "signature": {
        "s": "0x13e4d13fbba570ac47c515a7571bb50ad8d66d4e11919f095435ea8fa6b35f20",
        "r": "0xda22d43c4f26068436714997e612740990dda72b49ab82c9094e37f722636d0e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1665940100925011960",
    "total": "46747899010107595741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1665940100925011960",
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
            "amount": "27265423335309413153628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1665940100925011"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzcwNDc2YS0xMDMwLTU4Y2YtYTYxOS1kMTg1MzdkZjBmNTYifQ==",
    "nonce": 110312,
    "balances": {
      "current": "707608684909113939692395",
      "previous": "707610352515154965629366"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf0a71a09b488a8dc91fadc371753a9de0a580a9d",
    "nonce": 50,
    "balances": {
      "current": "73858861829943079329",
      "previous": "72192921729018067369"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:37.583Z",
  "updated": "2022-05-04T08:52:37.659Z",
  "id": "62723ed5bbd75600116d053d"
}
```
* *stageAmount*: `73858861829943079329`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000171e9bb1fcb6b7f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000171e9bb1fcb6b7f800000000000000000000000000000000000000000000000288c1e677fd4c5bdd54ab0f1039c808fd5147cfe9490b616f93db64fe162a95fd4a19098922b6b14e76cc7bdbe40a18c25a9319b3991400fcfa119567a8c63eb2316c8682d2c694de173878b84bb86c3a830cf425691a9d32ff1abc8617073ac781c388357c8791bf000000000000000000000000000000000000000000000000000000000000001b8fbd964433f95a8e2ea7f839aaff0702b4275de3433148ee05570322a0d7ab44da22d43c4f26068436714997e612740990dda72b49ab82c9094e37f722636d0e13e4d13fbba570ac47c515a7571bb50ad8d66d4e11919f095435ea8fa6b35f20000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d78b2e1d59392d8b6b0000000000000000000000000000000000000000000095d7a252a4351dd309b600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005eb29e7eec6530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60fc2710f53d77b5c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694932597a63774e446332595330784d444d774c54553459325974595459784f53316b4d5467314d7a646b5a6a426d4e54596966513d3d0000000000000000000000000000000000000000000000000000000000000032000000000000000000000000f0a71a09b488a8dc91fadc371753a9de0a580a9d00000000000000000000000000000000000000000000000400ff6383686a31a1000000000000000000000000000000000000000000000003e9e0c7d16bb379a900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x54ab0f1039c808fd5147cfe9490b616f93db64fe162a95fd4a19098922b6b14e",
      "signature": {
        "s": "0x173878b84bb86c3a830cf425691a9d32ff1abc8617073ac781c388357c8791bf",
        "r": "0x76cc7bdbe40a18c25a9319b3991400fcfa119567a8c63eb2316c8682d2c694de",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8fbd964433f95a8e2ea7f839aaff0702b4275de3433148ee05570322a0d7ab44",
      "signature": {
        "s": "0x13e4d13fbba570ac47c515a7571bb50ad8d66d4e11919f095435ea8fa6b35f20",
        "r": "0xda22d43c4f26068436714997e612740990dda72b49ab82c9094e37f722636d0e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1665940100925011960",
    "total": "46747899010107595741"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1665940100925011960",
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
            "amount": "27265423335309413153628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1665940100925011"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2YzcwNDc2YS0xMDMwLTU4Y2YtYTYxOS1kMTg1MzdkZjBmNTYifQ==",
    "nonce": 110312,
    "balances": {
      "current": "707608684909113939692395",
      "previous": "707610352515154965629366"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf0a71a09b488a8dc91fadc371753a9de0a580a9d",
    "nonce": 50,
    "balances": {
      "current": "73858861829943079329",
      "previous": "72192921729018067369"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:37.583Z",
  "updated": "2022-05-04T08:52:37.659Z",
  "id": "62723ed5bbd75600116d053d"
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
0x0f200f9b00000000000000000000000000000000000000000000000400ff6383686a31a10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `73858861829943079329`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`