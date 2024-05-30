# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc4d47ddF26E5239F2831f5e1E9203665747A365f`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002060f5daf404f2e87100000000000000000000000000000000000000000000000000000009c59b88dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009c59b88dc0000000000000000000000000000000000000000000000081812989c7b41d623eeb1a8a0dc5d148bbbb6c3c66f8579f2065c955482baa689adf92b19c4baf164523e8d8e33e1cd7c19e873e03357f50b31823b91b47e640de465c052468e7e5f1503ae9abc0f2b4ff5dd583cecd921ef6fb6ffcb618ebf9abe8090ea986720ca000000000000000000000000000000000000000000000000000000000000001bb156475334291f9a9c29dead5e2003b9106e12a76fdad5e5fdb19df438e82588ff20cf8d5bc96bc56855be723fa8356ef458d2bf30dff0d28830e0d0bef9421e19abec444647a3f76c7da6ac3556f31875121ce96cabf0018ca5e84a1be75a43000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0ddaeafaf02bb000000000000000000000000000000000000000000004eeec5b0ddb877caf4f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000280695a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd42a4af21b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6d4d325a6a67334d69316d4d324e6c4c5455324e575974596a466d4e43316a59546c6a4f57557859324e6d4d7a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c4d47ddf26e5239f2831f5e1e9203665747a365f00000000000000000000000000000000000000000000002060f5daf404f2e87100000000000000000000000000000000000000000000002060f5daea3f575f9500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeeb1a8a0dc5d148bbbb6c3c66f8579f2065c955482baa689adf92b19c4baf164",
      "signature": {
        "s": "0x1503ae9abc0f2b4ff5dd583cecd921ef6fb6ffcb618ebf9abe8090ea986720ca",
        "r": "0x523e8d8e33e1cd7c19e873e03357f50b31823b91b47e640de465c052468e7e5f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb156475334291f9a9c29dead5e2003b9106e12a76fdad5e5fdb19df438e82588",
      "signature": {
        "s": "0x19abec444647a3f76c7da6ac3556f31875121ce96cabf0018ca5e84a1be75a43",
        "r": "0xff20cf8d5bc96bc56855be723fa8356ef458d2bf30dff0d28830e0d0bef9421e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "41970010332",
    "total": "149308569194017707555"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "41970010332",
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
            "amount": "27599948339331765826075"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "41970010"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNmM2Zjg3Mi1mM2NlLTU2NWYtYjFmNC1jYTljOWUxY2NmMzEifQ==",
    "nonce": 110699,
    "balances": {
      "current": "372749155882738914362043",
      "previous": "372749155882780926342385"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4d47ddf26e5239f2831f5e1e9203665747a365f",
    "nonce": 46,
    "balances": {
      "current": "597282541497230747761",
      "previous": "597282541455260737429"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:35.023Z",
  "updated": "2022-05-04T08:54:35.089Z",
  "id": "62723f4b3592fd001130b530"
}
```
* *stageAmount*: `597282541497230747761`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000009c59b88dc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009c59b88dc0000000000000000000000000000000000000000000000081812989c7b41d623eeb1a8a0dc5d148bbbb6c3c66f8579f2065c955482baa689adf92b19c4baf164523e8d8e33e1cd7c19e873e03357f50b31823b91b47e640de465c052468e7e5f1503ae9abc0f2b4ff5dd583cecd921ef6fb6ffcb618ebf9abe8090ea986720ca000000000000000000000000000000000000000000000000000000000000001bb156475334291f9a9c29dead5e2003b9106e12a76fdad5e5fdb19df438e82588ff20cf8d5bc96bc56855be723fa8356ef458d2bf30dff0d28830e0d0bef9421e19abec444647a3f76c7da6ac3556f31875121ce96cabf0018ca5e84a1be75a43000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0ddaeafaf02bb000000000000000000000000000000000000000000004eeec5b0ddb877caf4f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000280695a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd42a4af21b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6d4d325a6a67334d69316d4d324e6c4c5455324e575974596a466d4e43316a59546c6a4f57557859324e6d4d7a456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c4d47ddf26e5239f2831f5e1e9203665747a365f00000000000000000000000000000000000000000000002060f5daf404f2e87100000000000000000000000000000000000000000000002060f5daea3f575f9500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeeb1a8a0dc5d148bbbb6c3c66f8579f2065c955482baa689adf92b19c4baf164",
      "signature": {
        "s": "0x1503ae9abc0f2b4ff5dd583cecd921ef6fb6ffcb618ebf9abe8090ea986720ca",
        "r": "0x523e8d8e33e1cd7c19e873e03357f50b31823b91b47e640de465c052468e7e5f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb156475334291f9a9c29dead5e2003b9106e12a76fdad5e5fdb19df438e82588",
      "signature": {
        "s": "0x19abec444647a3f76c7da6ac3556f31875121ce96cabf0018ca5e84a1be75a43",
        "r": "0xff20cf8d5bc96bc56855be723fa8356ef458d2bf30dff0d28830e0d0bef9421e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "41970010332",
    "total": "149308569194017707555"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "41970010332",
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
            "amount": "27599948339331765826075"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "41970010"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNmM2Zjg3Mi1mM2NlLTU2NWYtYjFmNC1jYTljOWUxY2NmMzEifQ==",
    "nonce": 110699,
    "balances": {
      "current": "372749155882738914362043",
      "previous": "372749155882780926342385"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4d47ddf26e5239f2831f5e1e9203665747a365f",
    "nonce": 46,
    "balances": {
      "current": "597282541497230747761",
      "previous": "597282541455260737429"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:35.023Z",
  "updated": "2022-05-04T08:54:35.089Z",
  "id": "62723f4b3592fd001130b530"
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
0x0f200f9b00000000000000000000000000000000000000000000002060f5daf404f2e8710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `597282541497230747761`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`