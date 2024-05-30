# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5F483A54911aCbb7Fc7e3D4eCfF4868C7D46D4A3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000017c84cb97b0ffd9e00000000000000000000000000000000000000000000000340aad21b3b7000000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000340aad21b3b70000000000000000000000000000000000000000000000000000340aad21b3b70000015c81b3f2132be5983126e44af2786294ab9151afb829fce8c16b3b4cb3a32dde0f514ce7f48b4e11a7648e89428a5f84f6822c1c45d308c6d2a3d625863f384366731e292aac54fc86c9dfab2bb018f77e5370b3fe5abba78c1a14c5c6abae8000000000000000000000000000000000000000000000000000000000000001b89c0bd5f6980c536b62fb5461466613686fd0e6360c42cfaa56c3079db1ee5ccc896b312db145747e34f2b8c8311674160bb20d062e281adec6d130b77f01a3a02f97c985729af5589a1340343e25e084154df944a8b5540d9749efc373cd6ff000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1cc94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000040000000000000000000000005f483a54911acbb7fc7e3d4ecff4868c7d46d4a300000000000000000000000000000000000000000000000017c84cb97b0ffd9e000000000000000000000000000000000000000000000003594848835505fd9e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000d529ae9e8600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d529ae9e8600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f444d304e7a45334e43316a5a6a4a684c54526a4e325574596d45344e5330774d6d49334d3246685a6a46694d54496966513d3d0000000000000000000000000000000000000000000000000000000000000025000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d70b6af2a790c223a47000000000000000000000000000000000000000000001d6d7604585dd0b23a4700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x15c81b3f2132be5983126e44af2786294ab9151afb829fce8c16b3b4cb3a32dd",
      "signature": {
        "s": "0x366731e292aac54fc86c9dfab2bb018f77e5370b3fe5abba78c1a14c5c6abae8",
        "r": "0xe0f514ce7f48b4e11a7648e89428a5f84f6822c1c45d308c6d2a3d625863f384",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x89c0bd5f6980c536b62fb5461466613686fd0e6360c42cfaa56c3079db1ee5cc",
      "signature": {
        "s": "0x02f97c985729af5589a1340343e25e084154df944a8b5540d9749efc373cd6ff",
        "r": "0xc896b312db145747e34f2b8c8311674160bb20d062e281adec6d130b77f01a3a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "60000000000000000000",
    "total": "60000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "60000000000000000000",
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
            "amount": "60000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "60000000000000000"
      }
    },
    "wallet": "0x5f483a54911acbb7fc7e3d4ecff4868c7d46d4a3",
    "data": "eyJyZWYiOiI4ODM0NzE3NC1jZjJhLTRjN2UtYmE4NS0wMmI3M2FhZjFiMTIifQ==",
    "nonce": 4,
    "balances": {
      "current": "1713704017731779998",
      "previous": "61773704017731779998"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 37,
    "balances": {
      "current": "139027827126410391206471",
      "previous": "138967827126410391206471"
    }
  },
  "blockNumber": "14797972",
  "created": "2022-05-18T09:12:34.158Z",
  "updated": "2022-05-18T09:12:34.234Z",
  "id": "6284b8827832e20011830f00"
}
```
* *stageAmount*: `1713704017731779998`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000340aad21b3b7000000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000340aad21b3b70000000000000000000000000000000000000000000000000000340aad21b3b70000015c81b3f2132be5983126e44af2786294ab9151afb829fce8c16b3b4cb3a32dde0f514ce7f48b4e11a7648e89428a5f84f6822c1c45d308c6d2a3d625863f384366731e292aac54fc86c9dfab2bb018f77e5370b3fe5abba78c1a14c5c6abae8000000000000000000000000000000000000000000000000000000000000001b89c0bd5f6980c536b62fb5461466613686fd0e6360c42cfaa56c3079db1ee5ccc896b312db145747e34f2b8c8311674160bb20d062e281adec6d130b77f01a3a02f97c985729af5589a1340343e25e084154df944a8b5540d9749efc373cd6ff000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1cc94000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000040000000000000000000000005f483a54911acbb7fc7e3d4ecff4868c7d46d4a300000000000000000000000000000000000000000000000017c84cb97b0ffd9e000000000000000000000000000000000000000000000003594848835505fd9e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000d529ae9e8600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d529ae9e8600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f444d304e7a45334e43316a5a6a4a684c54526a4e325574596d45344e5330774d6d49334d3246685a6a46694d54496966513d3d0000000000000000000000000000000000000000000000000000000000000025000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d70b6af2a790c223a47000000000000000000000000000000000000000000001d6d7604585dd0b23a4700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x15c81b3f2132be5983126e44af2786294ab9151afb829fce8c16b3b4cb3a32dd",
      "signature": {
        "s": "0x366731e292aac54fc86c9dfab2bb018f77e5370b3fe5abba78c1a14c5c6abae8",
        "r": "0xe0f514ce7f48b4e11a7648e89428a5f84f6822c1c45d308c6d2a3d625863f384",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x89c0bd5f6980c536b62fb5461466613686fd0e6360c42cfaa56c3079db1ee5cc",
      "signature": {
        "s": "0x02f97c985729af5589a1340343e25e084154df944a8b5540d9749efc373cd6ff",
        "r": "0xc896b312db145747e34f2b8c8311674160bb20d062e281adec6d130b77f01a3a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "60000000000000000000",
    "total": "60000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "60000000000000000000",
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
            "amount": "60000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "60000000000000000"
      }
    },
    "wallet": "0x5f483a54911acbb7fc7e3d4ecff4868c7d46d4a3",
    "data": "eyJyZWYiOiI4ODM0NzE3NC1jZjJhLTRjN2UtYmE4NS0wMmI3M2FhZjFiMTIifQ==",
    "nonce": 4,
    "balances": {
      "current": "1713704017731779998",
      "previous": "61773704017731779998"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 37,
    "balances": {
      "current": "139027827126410391206471",
      "previous": "138967827126410391206471"
    }
  },
  "blockNumber": "14797972",
  "created": "2022-05-18T09:12:34.158Z",
  "updated": "2022-05-18T09:12:34.234Z",
  "id": "6284b8827832e20011830f00"
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
0x0f200f9b00000000000000000000000000000000000000000000000017c84cb97b0ffd9e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1713704017731779998`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`