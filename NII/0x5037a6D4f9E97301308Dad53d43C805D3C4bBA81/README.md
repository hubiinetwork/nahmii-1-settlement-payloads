# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5037a6D4f9E97301308Dad53d43C805D3C4bBA81`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000015c01cced814f180d00000000000000000000000000000000000000000000000000000003ca4bc5000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003ca4bc500000000000000000000000000000000000000000000000001d6aa08fbfc0d218342ebc753c611ca8691c52635dfe9dcbbf9b3d6416096f256a706dfe27cfa76c263525ef11c57296883f67d911b79d9eec4e49a73beb1560faa8bdb35466f8010473dd868d7ab5a7c3708ffc2b79f51e99e3ed3a15da9628b814f5784994b9866000000000000000000000000000000000000000000000000000000000000001c4ea953932b807464061d9825b4f064ab8b39b403545a2da90d7aa0560c31ace6447b2c28f964714310cb5c5e560264a028e01be19992e33241bb5b9c340c8dc964d498213f54e0cf9a707461b31f67042628c37476f9b228c9c3950ef910bd68000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cb00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001ae90000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009617d57b7bd5ff178425000000000000000000000000000000000000000000009617d57b7bd9ca5bae7600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f865510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ff51534c94dbda290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459544a6959546c6b4d6930784e6d45784c5455344e575174596a6b784e4330784f44646b4d6d5a684d4449774f54416966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000005037a6d4f9e97301308dad53d43c805d3c4bba810000000000000000000000000000000000000000000000015c01cced814f180d0000000000000000000000000000000000000000000000015c01cce9b703530d00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004b7ec32d7a200000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x42ebc753c611ca8691c52635dfe9dcbbf9b3d6416096f256a706dfe27cfa76c2",
      "signature": {
        "s": "0x473dd868d7ab5a7c3708ffc2b79f51e99e3ed3a15da9628b814f5784994b9866",
        "r": "0x63525ef11c57296883f67d911b79d9eec4e49a73beb1560faa8bdb35466f8010",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4ea953932b807464061d9825b4f064ab8b39b403545a2da90d7aa0560c31ace6",
      "signature": {
        "s": "0x64d498213f54e0cf9a707461b31f67042628c37476f9b228c9c3950ef910bd68",
        "r": "0x447b2c28f964714310cb5c5e560264a028e01be19992e33241bb5b9c340c8dc9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16278865152",
    "total": "33914929822225473923"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16278865152",
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
            "amount": "27264238574410172979753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16278865"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YTJiYTlkMi0xNmExLTU4NWQtYjkxNC0xODdkMmZhMDIwOTAifQ==",
    "nonce": 110224,
    "balances": {
      "current": "708794630569253353784357",
      "previous": "708794630569269648928374"
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
            "amount": "340000000000000000"
          }
        }
      ]
    },
    "wallet": "0x5037a6d4f9e97301308dad53d43c805d3c4bba81",
    "nonce": 36,
    "balances": {
      "current": "25076549520624392205",
      "previous": "25076549504345527053"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:11.518Z",
  "updated": "2022-05-04T08:52:11.613Z",
  "id": "62723ebbbbd75600116d051d"
}
```
* *stageAmount*: `25076549520624392205`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000068000000000000000000000000000000000000000000000000000000003ca4bc5000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003ca4bc500000000000000000000000000000000000000000000000001d6aa08fbfc0d218342ebc753c611ca8691c52635dfe9dcbbf9b3d6416096f256a706dfe27cfa76c263525ef11c57296883f67d911b79d9eec4e49a73beb1560faa8bdb35466f8010473dd868d7ab5a7c3708ffc2b79f51e99e3ed3a15da9628b814f5784994b9866000000000000000000000000000000000000000000000000000000000000001c4ea953932b807464061d9825b4f064ab8b39b403545a2da90d7aa0560c31ace6447b2c28f964714310cb5c5e560264a028e01be19992e33241bb5b9c340c8dc964d498213f54e0cf9a707461b31f67042628c37476f9b228c9c3950ef910bd68000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cb00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001ae90000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009617d57b7bd5ff178425000000000000000000000000000000000000000000009617d57b7bd9ca5bae7600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f865510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ff51534c94dbda290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493459544a6959546c6b4d6930784e6d45784c5455344e575174596a6b784e4330784f44646b4d6d5a684d4449774f54416966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000005037a6d4f9e97301308dad53d43c805d3c4bba810000000000000000000000000000000000000000000000015c01cced814f180d0000000000000000000000000000000000000000000000015c01cce9b703530d00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004b7ec32d7a200000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x42ebc753c611ca8691c52635dfe9dcbbf9b3d6416096f256a706dfe27cfa76c2",
      "signature": {
        "s": "0x473dd868d7ab5a7c3708ffc2b79f51e99e3ed3a15da9628b814f5784994b9866",
        "r": "0x63525ef11c57296883f67d911b79d9eec4e49a73beb1560faa8bdb35466f8010",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4ea953932b807464061d9825b4f064ab8b39b403545a2da90d7aa0560c31ace6",
      "signature": {
        "s": "0x64d498213f54e0cf9a707461b31f67042628c37476f9b228c9c3950ef910bd68",
        "r": "0x447b2c28f964714310cb5c5e560264a028e01be19992e33241bb5b9c340c8dc9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16278865152",
    "total": "33914929822225473923"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16278865152",
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
            "amount": "27264238574410172979753"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16278865"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YTJiYTlkMi0xNmExLTU4NWQtYjkxNC0xODdkMmZhMDIwOTAifQ==",
    "nonce": 110224,
    "balances": {
      "current": "708794630569253353784357",
      "previous": "708794630569269648928374"
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
            "amount": "340000000000000000"
          }
        }
      ]
    },
    "wallet": "0x5037a6d4f9e97301308dad53d43c805d3c4bba81",
    "nonce": 36,
    "balances": {
      "current": "25076549520624392205",
      "previous": "25076549504345527053"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:11.518Z",
  "updated": "2022-05-04T08:52:11.613Z",
  "id": "62723ebbbbd75600116d051d"
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
0x0f200f9b0000000000000000000000000000000000000000000000015c01cced814f180d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `25076549520624392205`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`