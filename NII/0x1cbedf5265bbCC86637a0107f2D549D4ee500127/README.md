# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1cbedf5265bbCC86637a0107f2D549D4ee500127`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000012b753148ab1ca4cc0000000000000000000000000000000000000000000000001dc87cd9c3ca580f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001dc87cd9c3ca580f0000000000000000000000000000000000000000000000012b753148ab1ca4ccfb5e034880ca8c06fefff5f41c42e64a62adc2e2e97ff8b5008f378e6a0c71275e312bfa3c747f054c506ebca9d750bf64ca07cc4d3d0479862e3cb5b067253d0d459b36a24dd8b4797a4f70165eb8e095b2192e93a83e9e0f98de63d610aa42000000000000000000000000000000000000000000000000000000000000001b3cdea7e5d89fc1fc04aa9931ef2ec6c058a7f34e73ec0d41204b464850636fb1e3b38cce9a5814b9e975031e10db421aa364be670cb2b8dc3a6d60bc068a4c3871025a268354255a48a22232c5f5f9e0229a9fb576acbedfce9f4ad4ab65cc5c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5e7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000328c095b950daba157d800000000000000000000000000000000000000000000328c272bb1c5dc6a9c0500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000079fde6cfeec1e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df74a70815cbed58a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a4441774f474668596930775a5445304c54566b597a6b74596a63774e4330355a574d324d3256694e54457a4d47516966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000001cbedf5265bbcc86637a0107f2d549d4ee5001270000000000000000000000000000000000000000000000012b753148ab1ca4cc0000000000000000000000000000000000000000000000010dacb46ee7524cbd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfb5e034880ca8c06fefff5f41c42e64a62adc2e2e97ff8b5008f378e6a0c7127",
      "signature": {
        "s": "0x0d459b36a24dd8b4797a4f70165eb8e095b2192e93a83e9e0f98de63d610aa42",
        "r": "0x5e312bfa3c747f054c506ebca9d750bf64ca07cc4d3d0479862e3cb5b067253d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3cdea7e5d89fc1fc04aa9931ef2ec6c058a7f34e73ec0d41204b464850636fb1",
      "signature": {
        "s": "0x71025a268354255a48a22232c5f5f9e0229a9fb576acbedfce9f4ad4ab65cc5c",
        "r": "0xe3b38cce9a5814b9e975031e10db421aa364be670cb2b8dc3a6d60bc068a4c38",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2146102497176606735",
    "total": "21578207377793787084"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2146102497176606735",
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
            "amount": "27733862038904675063970"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2146102497176606"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZDAwOGFhYi0wZTE0LTVkYzktYjcwNC05ZWM2M2ViNTEzMGQifQ==",
    "nonce": 112103,
    "balances": {
      "current": "238701542610256766523352",
      "previous": "238703690858856440306693"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1cbedf5265bbcc86637a0107f2d549d4ee500127",
    "nonce": 11,
    "balances": {
      "current": "21578207377793787084",
      "previous": "19432104880617180349"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:01.710Z",
  "updated": "2022-05-04T09:02:01.812Z",
  "id": "62724109bbd75600116d0782"
}
```
* *stageAmount*: `21578207377793787084`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001dc87cd9c3ca580f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001dc87cd9c3ca580f0000000000000000000000000000000000000000000000012b753148ab1ca4ccfb5e034880ca8c06fefff5f41c42e64a62adc2e2e97ff8b5008f378e6a0c71275e312bfa3c747f054c506ebca9d750bf64ca07cc4d3d0479862e3cb5b067253d0d459b36a24dd8b4797a4f70165eb8e095b2192e93a83e9e0f98de63d610aa42000000000000000000000000000000000000000000000000000000000000001b3cdea7e5d89fc1fc04aa9931ef2ec6c058a7f34e73ec0d41204b464850636fb1e3b38cce9a5814b9e975031e10db421aa364be670cb2b8dc3a6d60bc068a4c3871025a268354255a48a22232c5f5f9e0229a9fb576acbedfce9f4ad4ab65cc5c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5e7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000328c095b950daba157d800000000000000000000000000000000000000000000328c272bb1c5dc6a9c0500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000079fde6cfeec1e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df74a70815cbed58a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a4441774f474668596930775a5445304c54566b597a6b74596a63774e4330355a574d324d3256694e54457a4d47516966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000001cbedf5265bbcc86637a0107f2d549d4ee5001270000000000000000000000000000000000000000000000012b753148ab1ca4cc0000000000000000000000000000000000000000000000010dacb46ee7524cbd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfb5e034880ca8c06fefff5f41c42e64a62adc2e2e97ff8b5008f378e6a0c7127",
      "signature": {
        "s": "0x0d459b36a24dd8b4797a4f70165eb8e095b2192e93a83e9e0f98de63d610aa42",
        "r": "0x5e312bfa3c747f054c506ebca9d750bf64ca07cc4d3d0479862e3cb5b067253d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3cdea7e5d89fc1fc04aa9931ef2ec6c058a7f34e73ec0d41204b464850636fb1",
      "signature": {
        "s": "0x71025a268354255a48a22232c5f5f9e0229a9fb576acbedfce9f4ad4ab65cc5c",
        "r": "0xe3b38cce9a5814b9e975031e10db421aa364be670cb2b8dc3a6d60bc068a4c38",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2146102497176606735",
    "total": "21578207377793787084"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2146102497176606735",
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
            "amount": "27733862038904675063970"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2146102497176606"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZDAwOGFhYi0wZTE0LTVkYzktYjcwNC05ZWM2M2ViNTEzMGQifQ==",
    "nonce": 112103,
    "balances": {
      "current": "238701542610256766523352",
      "previous": "238703690858856440306693"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1cbedf5265bbcc86637a0107f2d549d4ee500127",
    "nonce": 11,
    "balances": {
      "current": "21578207377793787084",
      "previous": "19432104880617180349"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:01.710Z",
  "updated": "2022-05-04T09:02:01.812Z",
  "id": "62724109bbd75600116d0782"
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
0x0f200f9b0000000000000000000000000000000000000000000000012b753148ab1ca4cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `21578207377793787084`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`