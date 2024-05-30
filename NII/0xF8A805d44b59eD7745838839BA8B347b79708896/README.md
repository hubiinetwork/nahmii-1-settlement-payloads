# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF8A805d44b59eD7745838839BA8B347b79708896`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000050d88f69a8bd1bdb830000000000000000000000000000000000000000000000000000000f726887790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f7268877900000000000000000000000000000000000000000000002a75674285334c2dd8c11cf70b5e2cd191c7e9e3e0785d3ca66345cce0aa224581bec02de90b29ade207a359fc939d04b776eab2589c183bd8d25ce10824453f94cf03b3dc762ebbb400d2b5d9761f02b0ef79ca807b65b36f920a0c1cca48c196fbff033f3fb86114000000000000000000000000000000000000000000000000000000000000001bdc5f1c3866c6bbf5434b4daf44e5442db0074bb6175b2164ccfe991fd9f917435e6b97e0793ac7c11ea039ad7164e22045577a6b9c8c385f660d837a54e13f386424b019a5eab39aa06d685a7016309db80ebecd912e699d901d2df338a72d9a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae9c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000961242de0a473ccb3b0a00000000000000000000000000000000000000000000961242de0a56b328169d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003f4541a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c600be2c8a1a4bb0450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f544d325a6d51794f5330794d7a41304c5456684e6a6b744f5745354f4330345a4451344f474e68596a55795954516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f8a805d44b59ed7745838839ba8b347b79708896000000000000000000000000000000000000000000000050d88f69a8bd1bdb83000000000000000000000000000000000000000000000050d88f69994ab3540a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc11cf70b5e2cd191c7e9e3e0785d3ca66345cce0aa224581bec02de90b29ade2",
      "signature": {
        "s": "0x00d2b5d9761f02b0ef79ca807b65b36f920a0c1cca48c196fbff033f3fb86114",
        "r": "0x07a359fc939d04b776eab2589c183bd8d25ce10824453f94cf03b3dc762ebbb4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdc5f1c3866c6bbf5434b4daf44e5442db0074bb6175b2164ccfe991fd9f91743",
      "signature": {
        "s": "0x6424b019a5eab39aa06d685a7016309db80ebecd912e699d901d2df338a72d9a",
        "r": "0x5e6b97e0793ac7c11ea039ad7164e22045577a6b9c8c385f660d837a54e13f38",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66343962489",
    "total": "783223054660698648024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66343962489",
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
            "amount": "27264341270159950590021"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "66343962"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxOTM2ZmQyOS0yMzA0LTVhNjktOWE5OC04ZDQ4OGNhYjUyYTQifQ==",
    "nonce": 110236,
    "balances": {
      "current": "708691832123725965900554",
      "previous": "708691832123792376207005"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf8a805d44b59ed7745838839ba8b347b79708896",
    "nonce": 46,
    "balances": {
      "current": "1491344333304074328963",
      "previous": "1491344333237730366474"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:15.057Z",
  "updated": "2022-05-04T08:52:15.141Z",
  "id": "62723ebfbbd75600116d0522"
}
```
* *stageAmount*: `1491344333304074328963`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000f726887790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f7268877900000000000000000000000000000000000000000000002a75674285334c2dd8c11cf70b5e2cd191c7e9e3e0785d3ca66345cce0aa224581bec02de90b29ade207a359fc939d04b776eab2589c183bd8d25ce10824453f94cf03b3dc762ebbb400d2b5d9761f02b0ef79ca807b65b36f920a0c1cca48c196fbff033f3fb86114000000000000000000000000000000000000000000000000000000000000001bdc5f1c3866c6bbf5434b4daf44e5442db0074bb6175b2164ccfe991fd9f917435e6b97e0793ac7c11ea039ad7164e22045577a6b9c8c385f660d837a54e13f386424b019a5eab39aa06d685a7016309db80ebecd912e699d901d2df338a72d9a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae9c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000961242de0a473ccb3b0a00000000000000000000000000000000000000000000961242de0a56b328169d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003f4541a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c600be2c8a1a4bb0450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f544d325a6d51794f5330794d7a41304c5456684e6a6b744f5745354f4330345a4451344f474e68596a55795954516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f8a805d44b59ed7745838839ba8b347b79708896000000000000000000000000000000000000000000000050d88f69a8bd1bdb83000000000000000000000000000000000000000000000050d88f69994ab3540a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc11cf70b5e2cd191c7e9e3e0785d3ca66345cce0aa224581bec02de90b29ade2",
      "signature": {
        "s": "0x00d2b5d9761f02b0ef79ca807b65b36f920a0c1cca48c196fbff033f3fb86114",
        "r": "0x07a359fc939d04b776eab2589c183bd8d25ce10824453f94cf03b3dc762ebbb4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xdc5f1c3866c6bbf5434b4daf44e5442db0074bb6175b2164ccfe991fd9f91743",
      "signature": {
        "s": "0x6424b019a5eab39aa06d685a7016309db80ebecd912e699d901d2df338a72d9a",
        "r": "0x5e6b97e0793ac7c11ea039ad7164e22045577a6b9c8c385f660d837a54e13f38",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "66343962489",
    "total": "783223054660698648024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "66343962489",
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
            "amount": "27264341270159950590021"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "66343962"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxOTM2ZmQyOS0yMzA0LTVhNjktOWE5OC04ZDQ4OGNhYjUyYTQifQ==",
    "nonce": 110236,
    "balances": {
      "current": "708691832123725965900554",
      "previous": "708691832123792376207005"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf8a805d44b59ed7745838839ba8b347b79708896",
    "nonce": 46,
    "balances": {
      "current": "1491344333304074328963",
      "previous": "1491344333237730366474"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:15.057Z",
  "updated": "2022-05-04T08:52:15.141Z",
  "id": "62723ebfbbd75600116d0522"
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
0x0f200f9b000000000000000000000000000000000000000000000050d88f69a8bd1bdb830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1491344333304074328963`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`