# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x18207Cf829BC91c6987280C210ca74C6388A7403`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000f24cb18a65e1f290000000000000000000000000000000000000000000000374b57f3cef27000000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000374b57f3cef27000000000000000000000000000000000000000000000000000375938aa8299d40000e7f376986f71f2353c15cbcddee23c5e345818939008145ef2983db9e34ec04c3dd9934727b1cb705942b1d658691ef96b7e674b51aa89434cdd2fe29d8df7571a117254a64d5cd729d4393d48cc7197a13063ed71694e750b2abd1bbf1957a8000000000000000000000000000000000000000000000000000000000000001b7820784a3ebdd4e68d6e791fa79eb72d5e117b7d21f672bdbccf8822ce77b09db08adef7b3fa8f39ac1e89d727bd6691a789820fc4203d55f13de868ae69d6e3730c8d10b0de3f6face314bc49b6ab2105c2a6d8587b9d746a97199e746a0317000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1fa1b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003000000000000000000000000018207cf829bc91c6987280c210ca74c6388a74030000000000000000000000000000000000000000000000000f24cb18a65e1f2900000000000000000000000000000000000000000000003768a483801fb41f2900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000e27c49886e600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000e2b52172bac80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d52685a5745315953316b4e4755784c5451344e3255744f4751304f4331684d544668595449354d7a566c4d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000051000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000003527e1686630202056280000000000000000000000000000000000000000000034f0961072612db0562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7f376986f71f2353c15cbcddee23c5e345818939008145ef2983db9e34ec04c",
      "signature": {
        "s": "0x1a117254a64d5cd729d4393d48cc7197a13063ed71694e750b2abd1bbf1957a8",
        "r": "0x3dd9934727b1cb705942b1d658691ef96b7e674b51aa89434cdd2fe29d8df757",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7820784a3ebdd4e68d6e791fa79eb72d5e117b7d21f672bdbccf8822ce77b09d",
      "signature": {
        "s": "0x730c8d10b0de3f6face314bc49b6ab2105c2a6d8587b9d746a97199e746a0317",
        "r": "0xb08adef7b3fa8f39ac1e89d727bd6691a789820fc4203d55f13de868ae69d6e3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1020000000000000000000",
    "total": "1021000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1020000000000000000000",
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
            "amount": "1021000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1020000000000000000"
      }
    },
    "wallet": "0x18207cf829bc91c6987280c210ca74c6388a7403",
    "data": "eyJyZWYiOiJkZmRhZWE1YS1kNGUxLTQ4N2UtOGQ0OC1hMTFhYTI5MzVlMmUifQ==",
    "nonce": 48,
    "balances": {
      "current": "1091220316461342505",
      "previous": "1022111220316461342505"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 81,
    "balances": {
      "current": "251021088955378863986216",
      "previous": "250001088955378863986216"
    }
  },
  "blockNumber": "14809627",
  "created": "2022-05-20T06:51:50.621Z",
  "updated": "2022-05-20T06:51:50.761Z",
  "id": "62873a867832e20011830f26"
}
```
* *stageAmount*: `1091220316461342505`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000374b57f3cef27000000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000374b57f3cef27000000000000000000000000000000000000000000000000000375938aa8299d40000e7f376986f71f2353c15cbcddee23c5e345818939008145ef2983db9e34ec04c3dd9934727b1cb705942b1d658691ef96b7e674b51aa89434cdd2fe29d8df7571a117254a64d5cd729d4393d48cc7197a13063ed71694e750b2abd1bbf1957a8000000000000000000000000000000000000000000000000000000000000001b7820784a3ebdd4e68d6e791fa79eb72d5e117b7d21f672bdbccf8822ce77b09db08adef7b3fa8f39ac1e89d727bd6691a789820fc4203d55f13de868ae69d6e3730c8d10b0de3f6face314bc49b6ab2105c2a6d8587b9d746a97199e746a0317000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1fa1b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003000000000000000000000000018207cf829bc91c6987280c210ca74c6388a74030000000000000000000000000000000000000000000000000f24cb18a65e1f2900000000000000000000000000000000000000000000003768a483801fb41f2900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000e27c49886e600000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000e2b52172bac80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d52685a5745315953316b4e4755784c5451344e3255744f4751304f4331684d544668595449354d7a566c4d6d556966513d3d0000000000000000000000000000000000000000000000000000000000000051000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000003527e1686630202056280000000000000000000000000000000000000000000034f0961072612db0562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7f376986f71f2353c15cbcddee23c5e345818939008145ef2983db9e34ec04c",
      "signature": {
        "s": "0x1a117254a64d5cd729d4393d48cc7197a13063ed71694e750b2abd1bbf1957a8",
        "r": "0x3dd9934727b1cb705942b1d658691ef96b7e674b51aa89434cdd2fe29d8df757",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7820784a3ebdd4e68d6e791fa79eb72d5e117b7d21f672bdbccf8822ce77b09d",
      "signature": {
        "s": "0x730c8d10b0de3f6face314bc49b6ab2105c2a6d8587b9d746a97199e746a0317",
        "r": "0xb08adef7b3fa8f39ac1e89d727bd6691a789820fc4203d55f13de868ae69d6e3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1020000000000000000000",
    "total": "1021000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1020000000000000000000",
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
            "amount": "1021000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1020000000000000000"
      }
    },
    "wallet": "0x18207cf829bc91c6987280c210ca74c6388a7403",
    "data": "eyJyZWYiOiJkZmRhZWE1YS1kNGUxLTQ4N2UtOGQ0OC1hMTFhYTI5MzVlMmUifQ==",
    "nonce": 48,
    "balances": {
      "current": "1091220316461342505",
      "previous": "1022111220316461342505"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 81,
    "balances": {
      "current": "251021088955378863986216",
      "previous": "250001088955378863986216"
    }
  },
  "blockNumber": "14809627",
  "created": "2022-05-20T06:51:50.621Z",
  "updated": "2022-05-20T06:51:50.761Z",
  "id": "62873a867832e20011830f26"
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
0x0f200f9b0000000000000000000000000000000000000000000000000f24cb18a65e1f290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1091220316461342505`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`