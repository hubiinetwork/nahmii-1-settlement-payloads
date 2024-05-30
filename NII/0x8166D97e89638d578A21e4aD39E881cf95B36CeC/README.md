# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8166D97e89638d578A21e4aD39E881cf95B36CeC`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000003dc1d753df9331b000000000000000000000000000000000000000000000000000000000031fe6c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000031fe6c00000000000000000000000000000000000000000000000003611a279b4d229b3a6fe35d62c55156d5d2dfb31dd1843ea8def99ecadfb406ae1136283ac7c94d3b4f011b6a78bf9ade0d03fceaa93a32b1270cdc6ebc53af1d6e4ae135e5edbd6298ae90cfb15dac54cfe3e305e5538bbd428483216bf018587b7407f085b3c5000000000000000000000000000000000000000000000000000000000000001b007b4955d6f205a649061a8c3eab3b29c64b96007731d9a6c0ec392f9f55b480592cce7de12d79460e35388f06eb8b61ce57cc6cd0eaf0ea0aa0da669bca05091bee71dc0521dfa1170de731fdb539cd18ccac813c73e8651b27e51037e49442000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0df000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bab897733023a500549000000000000000000000000000000000000000000004bab897733023a82108100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000ccc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907d54b3026516ef00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e445979597a4e6b4e5330774d54646d4c5455324e474d744f47566c4e433168593252684f54426c5a6a526b4d57456966513d3d00000000000000000000000000000000000000000000000000000000000000210000000000000000000000008166d97e89638d578a21e4ad39e881cf95b36cec00000000000000000000000000000000000000000000000003dc1d753df9331b00000000000000000000000000000000000000000000000003dc1d753dc734af00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a6fe35d62c55156d5d2dfb31dd1843ea8def99ecadfb406ae1136283ac7c94d",
      "signature": {
        "s": "0x6298ae90cfb15dac54cfe3e305e5538bbd428483216bf018587b7407f085b3c5",
        "r": "0x3b4f011b6a78bf9ade0d03fceaa93a32b1270cdc6ebc53af1d6e4ae135e5edbd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x007b4955d6f205a649061a8c3eab3b29c64b96007731d9a6c0ec392f9f55b480",
      "signature": {
        "s": "0x1bee71dc0521dfa1170de731fdb539cd18ccac813c73e8651b27e51037e49442",
        "r": "0x592cce7de12d79460e35388f06eb8b61ce57cc6cd0eaf0ea0aa0da669bca0509",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3276396",
    "total": "243504612266287771"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3276396",
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
            "amount": "27615340318341677018864"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3276"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNDYyYzNkNS0wMTdmLTU2NGMtOGVlNC1hY2RhOTBlZjRkMWEifQ==",
    "nonce": 110815,
    "balances": {
      "current": "357341784893817810322761",
      "previous": "357341784893817813602433"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8166d97e89638d578a21e4ad39e881cf95b36cec",
    "nonce": 33,
    "balances": {
      "current": "278129666378248987",
      "previous": "278129666374972591"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:10.653Z",
  "updated": "2022-05-04T08:55:10.759Z",
  "id": "62723f6ebbd75600116d05ec"
}
```
* *stageAmount*: `278129666378248987`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000031fe6c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000031fe6c00000000000000000000000000000000000000000000000003611a279b4d229b3a6fe35d62c55156d5d2dfb31dd1843ea8def99ecadfb406ae1136283ac7c94d3b4f011b6a78bf9ade0d03fceaa93a32b1270cdc6ebc53af1d6e4ae135e5edbd6298ae90cfb15dac54cfe3e305e5538bbd428483216bf018587b7407f085b3c5000000000000000000000000000000000000000000000000000000000000001b007b4955d6f205a649061a8c3eab3b29c64b96007731d9a6c0ec392f9f55b480592cce7de12d79460e35388f06eb8b61ce57cc6cd0eaf0ea0aa0da669bca05091bee71dc0521dfa1170de731fdb539cd18ccac813c73e8651b27e51037e49442000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0df000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bab897733023a500549000000000000000000000000000000000000000000004bab897733023a82108100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000ccc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907d54b3026516ef00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e445979597a4e6b4e5330774d54646d4c5455324e474d744f47566c4e433168593252684f54426c5a6a526b4d57456966513d3d00000000000000000000000000000000000000000000000000000000000000210000000000000000000000008166d97e89638d578a21e4ad39e881cf95b36cec00000000000000000000000000000000000000000000000003dc1d753df9331b00000000000000000000000000000000000000000000000003dc1d753dc734af00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a6fe35d62c55156d5d2dfb31dd1843ea8def99ecadfb406ae1136283ac7c94d",
      "signature": {
        "s": "0x6298ae90cfb15dac54cfe3e305e5538bbd428483216bf018587b7407f085b3c5",
        "r": "0x3b4f011b6a78bf9ade0d03fceaa93a32b1270cdc6ebc53af1d6e4ae135e5edbd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x007b4955d6f205a649061a8c3eab3b29c64b96007731d9a6c0ec392f9f55b480",
      "signature": {
        "s": "0x1bee71dc0521dfa1170de731fdb539cd18ccac813c73e8651b27e51037e49442",
        "r": "0x592cce7de12d79460e35388f06eb8b61ce57cc6cd0eaf0ea0aa0da669bca0509",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3276396",
    "total": "243504612266287771"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3276396",
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
            "amount": "27615340318341677018864"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3276"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNDYyYzNkNS0wMTdmLTU2NGMtOGVlNC1hY2RhOTBlZjRkMWEifQ==",
    "nonce": 110815,
    "balances": {
      "current": "357341784893817810322761",
      "previous": "357341784893817813602433"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8166d97e89638d578a21e4ad39e881cf95b36cec",
    "nonce": 33,
    "balances": {
      "current": "278129666378248987",
      "previous": "278129666374972591"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:10.653Z",
  "updated": "2022-05-04T08:55:10.759Z",
  "id": "62723f6ebbd75600116d05ec"
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
0x0f200f9b00000000000000000000000000000000000000000000000003dc1d753df9331b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `278129666378248987`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`