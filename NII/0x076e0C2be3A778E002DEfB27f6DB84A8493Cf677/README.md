# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x076e0C2be3A778E002DEfB27f6DB84A8493Cf677`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000009e45fb8f872102b89f000000000000000000000000000000000000000000000011549f5475ba58a6350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000011549f5475ba58a6350000000000000000000000000000000000000000000001e8a3537ce652fd5ac8a4caa6c5c493adf29ff4ede8a920afebd8e9ce565595a0ee5690d6ea7fda5c5596f1d5ae29cea2251727cf4b03fab26ec6d5f3bad51cdbcab4dd431d6d30fddc6e56ad858dbd315c9c41353f8267fffff26635111ebe2bfe1304e3a3ef7c3986000000000000000000000000000000000000000000000000000000000000001c6ae59e101ced5cad5979dc06a96dac678b9c0d171242145ecbc509ac974ff171394030d3ed914fb4b3a79e716ff64593faa63f5879b715b39e6918207d3c1b0a45ef7b75ffc7231a4f0a17413247ee09e011ddd8d2f5ccb0ebe2ba0741b5823c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b098000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c68aa24d30b6ccb1e1e000000000000000000000000000000000000000000004c7a0333edfd2cb3ba4000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000046fc67c058ff5ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8d77701a12df0a3bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4455794e7a4d775969316a5a5755344c5455324f444974596a41324d7930794e6a63774d475935597a63784d32496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000076e0c2be3a778e002defb27f6db84a8493cf67700000000000000000000000000000000000000000000009e45fb8f872102b89f00000000000000000000000000000000000000000000008cf15c3b1166aa126a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xa4caa6c5c493adf29ff4ede8a920afebd8e9ce565595a0ee5690d6ea7fda5c55",
      "signature": {
        "s": "0x6e56ad858dbd315c9c41353f8267fffff26635111ebe2bfe1304e3a3ef7c3986",
        "r": "0x96f1d5ae29cea2251727cf4b03fab26ec6d5f3bad51cdbcab4dd431d6d30fddc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6ae59e101ced5cad5979dc06a96dac678b9c0d171242145ecbc509ac974ff171",
      "signature": {
        "s": "0x45ef7b75ffc7231a4f0a17413247ee09e011ddd8d2f5ccb0ebe2ba0741b5823c",
        "r": "0x394030d3ed914fb4b3a79e716ff64593faa63f5879b715b39e6918207d3c1b0a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "319692334538159597109",
    "total": "9013779995550187084488"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "319692334538159597109",
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
            "amount": "27611855014301644399548"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "319692334538159597"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjODUyNzMwYi1jZWU4LTU2ODItYjA2My0yNjcwMGY5YzcxM2IifQ==",
    "nonce": 110744,
    "balances": {
      "current": "360830574237890462293534",
      "previous": "361150586264763160050240"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x076e0c2be3a778e002defb27f6db84a8493cf677",
    "nonce": 46,
    "balances": {
      "current": "2919628345664417740959",
      "previous": "2599936011126258143850"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:48.368Z",
  "updated": "2022-05-04T08:54:48.453Z",
  "id": "62723f58bbd75600116d05cf"
}
```
* *stageAmount*: `2919628345664417740959`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000011549f5475ba58a6350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000011549f5475ba58a6350000000000000000000000000000000000000000000001e8a3537ce652fd5ac8a4caa6c5c493adf29ff4ede8a920afebd8e9ce565595a0ee5690d6ea7fda5c5596f1d5ae29cea2251727cf4b03fab26ec6d5f3bad51cdbcab4dd431d6d30fddc6e56ad858dbd315c9c41353f8267fffff26635111ebe2bfe1304e3a3ef7c3986000000000000000000000000000000000000000000000000000000000000001c6ae59e101ced5cad5979dc06a96dac678b9c0d171242145ecbc509ac974ff171394030d3ed914fb4b3a79e716ff64593faa63f5879b715b39e6918207d3c1b0a45ef7b75ffc7231a4f0a17413247ee09e011ddd8d2f5ccb0ebe2ba0741b5823c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b098000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004c68aa24d30b6ccb1e1e000000000000000000000000000000000000000000004c7a0333edfd2cb3ba4000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000046fc67c058ff5ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8d77701a12df0a3bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4455794e7a4d775969316a5a5755344c5455324f444974596a41324d7930794e6a63774d475935597a63784d32496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000076e0c2be3a778e002defb27f6db84a8493cf67700000000000000000000000000000000000000000000009e45fb8f872102b89f00000000000000000000000000000000000000000000008cf15c3b1166aa126a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xa4caa6c5c493adf29ff4ede8a920afebd8e9ce565595a0ee5690d6ea7fda5c55",
      "signature": {
        "s": "0x6e56ad858dbd315c9c41353f8267fffff26635111ebe2bfe1304e3a3ef7c3986",
        "r": "0x96f1d5ae29cea2251727cf4b03fab26ec6d5f3bad51cdbcab4dd431d6d30fddc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6ae59e101ced5cad5979dc06a96dac678b9c0d171242145ecbc509ac974ff171",
      "signature": {
        "s": "0x45ef7b75ffc7231a4f0a17413247ee09e011ddd8d2f5ccb0ebe2ba0741b5823c",
        "r": "0x394030d3ed914fb4b3a79e716ff64593faa63f5879b715b39e6918207d3c1b0a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "319692334538159597109",
    "total": "9013779995550187084488"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "319692334538159597109",
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
            "amount": "27611855014301644399548"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "319692334538159597"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjODUyNzMwYi1jZWU4LTU2ODItYjA2My0yNjcwMGY5YzcxM2IifQ==",
    "nonce": 110744,
    "balances": {
      "current": "360830574237890462293534",
      "previous": "361150586264763160050240"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x076e0c2be3a778e002defb27f6db84a8493cf677",
    "nonce": 46,
    "balances": {
      "current": "2919628345664417740959",
      "previous": "2599936011126258143850"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:48.368Z",
  "updated": "2022-05-04T08:54:48.453Z",
  "id": "62723f58bbd75600116d05cf"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000009e45fb8f872102b89f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `2919628345664417740959`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`