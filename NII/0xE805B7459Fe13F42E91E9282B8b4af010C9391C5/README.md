# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE805B7459Fe13F42E91E9282B8b4af010C9391C5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000e49412ff580ca145300000000000000000000000000000000000000000000000000000002c538ed2b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002c538ed2b00000000000000000000000000000000000000000000000766c44944cae3ae602557ade6d7af910a3a68a76448f5ea685f8d0f60f26ac8c36fcb3bab6ffa44832e0495dacb49d9bb5854ac018e9c813652e828ba90e36c4355b4f0d76424259a2bf02994803f49adabf0ec3490b11713e019d9c3e544d42a618bb51880eb7827000000000000000000000000000000000000000000000000000000000000001c030f0afc4f72bfe82164ae6d73927675e21b38fd68e29e6ba6225ef1324a46269ea03540675454c55286d7fbc147e574585164fb6ca931e26d2565d3f0cc656042ad70396f3d9ad8cf95149b2d9198d17cb9cc3b419bc47a829eeb6fa9d45ab9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae01000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963eef703c0d82e7c1f100000000000000000000000000000000000000000000963eef703c1048d63eb400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000b58f980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f551562d11c93b510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5759305a474d7a4e7930344d6a41344c5455314d544974596d4e6a5a6930344e7a41325a4459325a6d51335a44416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e805b7459fe13f42e91e9282b8b4af010c9391c500000000000000000000000000000000000000000000000e49412ff580ca145300000000000000000000000000000000000000000000000e49412ff2bb91272800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2557ade6d7af910a3a68a76448f5ea685f8d0f60f26ac8c36fcb3bab6ffa4483",
      "signature": {
        "s": "0x2bf02994803f49adabf0ec3490b11713e019d9c3e544d42a618bb51880eb7827",
        "r": "0x2e0495dacb49d9bb5854ac018e9c813652e828ba90e36c4355b4f0d76424259a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x030f0afc4f72bfe82164ae6d73927675e21b38fd68e29e6ba6225ef1324a4626",
      "signature": {
        "s": "0x42ad70396f3d9ad8cf95149b2d9198d17cb9cc3b419bc47a829eeb6fa9d45ab9",
        "r": "0x9ea03540675454c55286d7fbc147e574585164fb6ca931e26d2565d3f0cc6560",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "11898776875",
    "total": "136532332763081322080"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11898776875",
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
            "amount": "27263518001632985561937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11898776"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZWY0ZGMzNy04MjA4LTU1MTItYmNjZi04NzA2ZDY2ZmQ3ZDAifQ==",
    "nonce": 110081,
    "balances": {
      "current": "709515923919217959092721",
      "previous": "709515923919229869768372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe805b7459fe13f42e91e9282b8b4af010c9391c5",
    "nonce": 46,
    "balances": {
      "current": "263532970001662874707",
      "previous": "263532969989764097832"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:27.387Z",
  "updated": "2022-05-04T08:51:27.447Z",
  "id": "62723e8f3592fd001130b465"
}
```
* *stageAmount*: `263532970001662874707`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000002c538ed2b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000002c538ed2b00000000000000000000000000000000000000000000000766c44944cae3ae602557ade6d7af910a3a68a76448f5ea685f8d0f60f26ac8c36fcb3bab6ffa44832e0495dacb49d9bb5854ac018e9c813652e828ba90e36c4355b4f0d76424259a2bf02994803f49adabf0ec3490b11713e019d9c3e544d42a618bb51880eb7827000000000000000000000000000000000000000000000000000000000000001c030f0afc4f72bfe82164ae6d73927675e21b38fd68e29e6ba6225ef1324a46269ea03540675454c55286d7fbc147e574585164fb6ca931e26d2565d3f0cc656042ad70396f3d9ad8cf95149b2d9198d17cb9cc3b419bc47a829eeb6fa9d45ab9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae01000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963eef703c0d82e7c1f100000000000000000000000000000000000000000000963eef703c1048d63eb400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000b58f980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f551562d11c93b510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5759305a474d7a4e7930344d6a41344c5455314d544974596d4e6a5a6930344e7a41325a4459325a6d51335a44416966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e805b7459fe13f42e91e9282b8b4af010c9391c500000000000000000000000000000000000000000000000e49412ff580ca145300000000000000000000000000000000000000000000000e49412ff2bb91272800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2557ade6d7af910a3a68a76448f5ea685f8d0f60f26ac8c36fcb3bab6ffa4483",
      "signature": {
        "s": "0x2bf02994803f49adabf0ec3490b11713e019d9c3e544d42a618bb51880eb7827",
        "r": "0x2e0495dacb49d9bb5854ac018e9c813652e828ba90e36c4355b4f0d76424259a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x030f0afc4f72bfe82164ae6d73927675e21b38fd68e29e6ba6225ef1324a4626",
      "signature": {
        "s": "0x42ad70396f3d9ad8cf95149b2d9198d17cb9cc3b419bc47a829eeb6fa9d45ab9",
        "r": "0x9ea03540675454c55286d7fbc147e574585164fb6ca931e26d2565d3f0cc6560",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "11898776875",
    "total": "136532332763081322080"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11898776875",
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
            "amount": "27263518001632985561937"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11898776"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZWY0ZGMzNy04MjA4LTU1MTItYmNjZi04NzA2ZDY2ZmQ3ZDAifQ==",
    "nonce": 110081,
    "balances": {
      "current": "709515923919217959092721",
      "previous": "709515923919229869768372"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe805b7459fe13f42e91e9282b8b4af010c9391c5",
    "nonce": 46,
    "balances": {
      "current": "263532970001662874707",
      "previous": "263532969989764097832"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:27.387Z",
  "updated": "2022-05-04T08:51:27.447Z",
  "id": "62723e8f3592fd001130b465"
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
0x0f200f9b00000000000000000000000000000000000000000000000e49412ff580ca14530000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `263532970001662874707`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`