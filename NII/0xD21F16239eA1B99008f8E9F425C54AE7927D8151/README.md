# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD21F16239eA1B99008f8E9F425C54AE7927D8151`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000106b41185bf264ac3400000000000000000000000000000000000000000000000bec1aa378de4954200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000bec1aa378de4954200000000000000000000000000000000000000000000000106b41185bf264ac34b18b3b27511cb584e835fdf1a6c7b7b0f04cbc3c7326b490d03a7e1c9c49405bbbaae433ab549cb5a831f0989e047075816767622192f97b5e21e5e3829a8ded048c5bf530b7acb4fc7fecf2634a0e25d9fff5dc8ab93e82dfd2661d2935a0f3000000000000000000000000000000000000000000000000000000000000001c8bf4f6ec7a405d6274e00ac8d3def145ae4befa3a375599badcd1c4e60a692e8f4df5479003366300a01df72c12a46cf7e66a7a96186c76cc593e33d13d153d45a19554abd9f2febf209fedf0cb1bdca2cadc03c99fdb6eef8282131f9176d82000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c6eb4300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000014872000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000001d2558f7cca6ae297f0000000000000000000000000000000000000000000000291480f1f68948f8d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000030d56b104517b380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000404f3394032ab8a52450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595449774d7a45784d53316b4d6a5a694c54557a4d6a49744f5442684e7930334d6d5a695a4755304e44646a4d6d516966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000d21f16239ea1b99008f8e9f425c54ae7927d81510000000000000000000000000000000000000000000000106b41185bf264ac340000000000000000000000000000000000000000000000047f2674e3141b581400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb18b3b27511cb584e835fdf1a6c7b7b0f04cbc3c7326b490d03a7e1c9c49405b",
      "signature": {
        "s": "0x048c5bf530b7acb4fc7fecf2634a0e25d9fff5dc8ab93e82dfd2661d2935a0f3",
        "r": "0xbbaae433ab549cb5a831f0989e047075816767622192f97b5e21e5e3829a8ded",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8bf4f6ec7a405d6274e00ac8d3def145ae4befa3a375599badcd1c4e60a692e8",
      "signature": {
        "s": "0x5a19554abd9f2febf209fedf0cb1bdca2cadc03c99fdb6eef8282131f9176d82",
        "r": "0xf4df5479003366300a01df72c12a46cf7e66a7a96186c76cc593e33d13d153d4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "219927275092671288352",
    "total": "302876390398085082164"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "219927275092671288352",
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
            "amount": "18980779017784678568517"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "219927275092671288"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YTIwMzExMS1kMjZiLTUzMjItOTBhNy03MmZiZGU0NDdjMmQifQ==",
    "nonce": 84082,
    "balances": {
      "current": "537646751373272689023",
      "previous": "757793953741036648663"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd21f16239ea1b99008f8e9f425c54ae7927d8151",
    "nonce": 2,
    "balances": {
      "current": "302876390398085082164",
      "previous": "82949115305413793812"
    }
  },
  "blockNumber": "13036355",
  "created": "2021-08-16T12:46:40.550Z",
  "updated": "2021-08-16T12:46:40.623Z",
  "id": "611a5e304cc8ab001184f2cc"
}
```
* *stageAmount*: `302876390398085082164`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000bec1aa378de4954200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000bec1aa378de4954200000000000000000000000000000000000000000000000106b41185bf264ac34b18b3b27511cb584e835fdf1a6c7b7b0f04cbc3c7326b490d03a7e1c9c49405bbbaae433ab549cb5a831f0989e047075816767622192f97b5e21e5e3829a8ded048c5bf530b7acb4fc7fecf2634a0e25d9fff5dc8ab93e82dfd2661d2935a0f3000000000000000000000000000000000000000000000000000000000000001c8bf4f6ec7a405d6274e00ac8d3def145ae4befa3a375599badcd1c4e60a692e8f4df5479003366300a01df72c12a46cf7e66a7a96186c76cc593e33d13d153d45a19554abd9f2febf209fedf0cb1bdca2cadc03c99fdb6eef8282131f9176d82000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000c6eb4300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000014872000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000001d2558f7cca6ae297f0000000000000000000000000000000000000000000000291480f1f68948f8d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000030d56b104517b380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000404f3394032ab8a52450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595449774d7a45784d53316b4d6a5a694c54557a4d6a49744f5442684e7930334d6d5a695a4755304e44646a4d6d516966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000d21f16239ea1b99008f8e9f425c54ae7927d81510000000000000000000000000000000000000000000000106b41185bf264ac340000000000000000000000000000000000000000000000047f2674e3141b581400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb18b3b27511cb584e835fdf1a6c7b7b0f04cbc3c7326b490d03a7e1c9c49405b",
      "signature": {
        "s": "0x048c5bf530b7acb4fc7fecf2634a0e25d9fff5dc8ab93e82dfd2661d2935a0f3",
        "r": "0xbbaae433ab549cb5a831f0989e047075816767622192f97b5e21e5e3829a8ded",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8bf4f6ec7a405d6274e00ac8d3def145ae4befa3a375599badcd1c4e60a692e8",
      "signature": {
        "s": "0x5a19554abd9f2febf209fedf0cb1bdca2cadc03c99fdb6eef8282131f9176d82",
        "r": "0xf4df5479003366300a01df72c12a46cf7e66a7a96186c76cc593e33d13d153d4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "219927275092671288352",
    "total": "302876390398085082164"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "219927275092671288352",
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
            "amount": "18980779017784678568517"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "219927275092671288"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YTIwMzExMS1kMjZiLTUzMjItOTBhNy03MmZiZGU0NDdjMmQifQ==",
    "nonce": 84082,
    "balances": {
      "current": "537646751373272689023",
      "previous": "757793953741036648663"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd21f16239ea1b99008f8e9f425c54ae7927d8151",
    "nonce": 2,
    "balances": {
      "current": "302876390398085082164",
      "previous": "82949115305413793812"
    }
  },
  "blockNumber": "13036355",
  "created": "2021-08-16T12:46:40.550Z",
  "updated": "2021-08-16T12:46:40.623Z",
  "id": "611a5e304cc8ab001184f2cc"
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
0x0f200f9b0000000000000000000000000000000000000000000000106b41185bf264ac340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `302876390398085082164`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`