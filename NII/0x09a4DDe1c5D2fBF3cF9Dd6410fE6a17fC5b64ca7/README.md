# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x09a4DDe1c5D2fBF3cF9Dd6410fE6a17fC5b64ca7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000007d7fb6c7e4b5c578a50000000000000000000000000000000000000000000000000000001ae12987360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001ae129873600000000000000000000000000000000000000000000003ab30562dc630d15018cbc47257e3a64a5307ab16bf912922ccc43a317261a710716ae8812d31d9ccbc636907a66a7d1e523bbb576a807e56df5e9ea93f5a4b6b532a94322eac7db1a348cecb7e94d9a159c5fc224251e2b61266c60c6cfff8bf64737982037e6e093000000000000000000000000000000000000000000000000000000000000001cb70a803b0ff90b3f0979ad70152bf0a793909d9be9c609e83871a715f614bc41294dd9e2c822191a5a00c830a38c9d767f2393fbfdf20eca48e3c7c18492f91e39934805492133b5660e71f1ca4ed6e02d4e0ca9919759318ae28d59576771b4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afe8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000517bdbca605fef35bea300000000000000000000000000000000000000000000517bdbca607ad740d9b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006e193d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d78b34177b8028cc590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68595745304d546c694d7930785a44557a4c54566c4e6a51744f545a6d4e4330794d5751354d474a685a474a6a5a57456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000009a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca700000000000000000000000000000000000000000000007d7fb6c7e4b5c578a500000000000000000000000000000000000000000000007d7fb6c7c9d49bf16f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8cbc47257e3a64a5307ab16bf912922ccc43a317261a710716ae8812d31d9ccb",
      "signature": {
        "s": "0x348cecb7e94d9a159c5fc224251e2b61266c60c6cfff8bf64737982037e6e093",
        "r": "0xc636907a66a7d1e523bbb576a807e56df5e9ea93f5a4b6b532a94322eac7db1a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb70a803b0ff90b3f0979ad70152bf0a793909d9be9c609e83871a715f614bc41",
      "signature": {
        "s": "0x39934805492133b5660e71f1ca4ed6e02d4e0ca9919759318ae28d59576771b4",
        "r": "0x294dd9e2c822191a5a00c830a38c9d767f2393fbfdf20eca48e3c7c18492f91e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "115446744886",
    "total": "1082810981681520776449"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "115446744886",
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
            "amount": "27587913058285039176793"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "115446744"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYWE0MTliMy0xZDUzLTVlNjQtOTZmNC0yMWQ5MGJhZGJjZWEifQ==",
    "nonce": 110568,
    "balances": {
      "current": "384796472210512290365091",
      "previous": "384796472210627852556721"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca7",
    "nonce": 46,
    "balances": {
      "current": "2315045771887388227749",
      "previous": "2315045771771941482863"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:56.399Z",
  "updated": "2022-05-04T08:53:56.484Z",
  "id": "62723f243592fd001130b500"
}
```
* *stageAmount*: `2315045771887388227749`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000001ae12987360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001ae129873600000000000000000000000000000000000000000000003ab30562dc630d15018cbc47257e3a64a5307ab16bf912922ccc43a317261a710716ae8812d31d9ccbc636907a66a7d1e523bbb576a807e56df5e9ea93f5a4b6b532a94322eac7db1a348cecb7e94d9a159c5fc224251e2b61266c60c6cfff8bf64737982037e6e093000000000000000000000000000000000000000000000000000000000000001cb70a803b0ff90b3f0979ad70152bf0a793909d9be9c609e83871a715f614bc41294dd9e2c822191a5a00c830a38c9d767f2393fbfdf20eca48e3c7c18492f91e39934805492133b5660e71f1ca4ed6e02d4e0ca9919759318ae28d59576771b4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afe8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000517bdbca605fef35bea300000000000000000000000000000000000000000000517bdbca607ad740d9b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006e193d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d78b34177b8028cc590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68595745304d546c694d7930785a44557a4c54566c4e6a51744f545a6d4e4330794d5751354d474a685a474a6a5a57456966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000009a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca700000000000000000000000000000000000000000000007d7fb6c7e4b5c578a500000000000000000000000000000000000000000000007d7fb6c7c9d49bf16f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8cbc47257e3a64a5307ab16bf912922ccc43a317261a710716ae8812d31d9ccb",
      "signature": {
        "s": "0x348cecb7e94d9a159c5fc224251e2b61266c60c6cfff8bf64737982037e6e093",
        "r": "0xc636907a66a7d1e523bbb576a807e56df5e9ea93f5a4b6b532a94322eac7db1a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb70a803b0ff90b3f0979ad70152bf0a793909d9be9c609e83871a715f614bc41",
      "signature": {
        "s": "0x39934805492133b5660e71f1ca4ed6e02d4e0ca9919759318ae28d59576771b4",
        "r": "0x294dd9e2c822191a5a00c830a38c9d767f2393fbfdf20eca48e3c7c18492f91e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "115446744886",
    "total": "1082810981681520776449"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "115446744886",
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
            "amount": "27587913058285039176793"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "115446744"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYWE0MTliMy0xZDUzLTVlNjQtOTZmNC0yMWQ5MGJhZGJjZWEifQ==",
    "nonce": 110568,
    "balances": {
      "current": "384796472210512290365091",
      "previous": "384796472210627852556721"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca7",
    "nonce": 46,
    "balances": {
      "current": "2315045771887388227749",
      "previous": "2315045771771941482863"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:56.399Z",
  "updated": "2022-05-04T08:53:56.484Z",
  "id": "62723f243592fd001130b500"
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
0x0f200f9b00000000000000000000000000000000000000000000007d7fb6c7e4b5c578a50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2315045771887388227749`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`