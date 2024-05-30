# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEb0cA775f52aDDa54cC71757E2BD40aeBC3002E9`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000002197d7f3a6fcaa24000000000000000000000000000000000000000000000000000000000d933561d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000d933561d00000000000000000000000000000000000000000000000000000013cd037a7b8af793a60bd6ffb8d3a42be7d2049054d168dc70b0016fd67d9e8df198292c69752a9f522bdcfa9b89c44a5146e8b48d03d7aacbb3e2d345a423342088a9f10250a3d0bcccdf7e363804732a038b661792243bceafb87129fc669149e23cb8c3000000000000000000000000000000000000000000000000000000000000001b071fd3245514d711be070a84542ca1eb15d189e2b0de6fa9f1fcaa07252910627e1404ba5aa73e64b1c161881c9ee6cddcd213fa095ec17ff5ae07abcf57c4ea63c436a1100a2906dfbf692a0d4e39a8739817e330101b5964333d01869d13f3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b341000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d0c0a9f4d7516e844db000000000000000000000000000000000000000000003d0c0a9f4d75f053356c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000379a740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc535eccac29cfa0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6959546c68596a6b354e5330354e4445324c54566b596a4d744f544d304d5330784e7a4e6d4e4759775a5467354e6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000028000000000000000000000000eb0ca775f52adda54cc71757e2bd40aebc3002e9000000000000000000000000000000000000000000000002197d7f3a6fcaa240000000000000000000000000000000000000000000000002197d7f3996974c2300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8af793a60bd6ffb8d3a42be7d2049054d168dc70b0016fd67d9e8df198292c69",
      "signature": {
        "s": "0x50a3d0bcccdf7e363804732a038b661792243bceafb87129fc669149e23cb8c3",
        "r": "0x752a9f522bdcfa9b89c44a5146e8b48d03d7aacbb3e2d345a423342088a9f102",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x071fd3245514d711be070a84542ca1eb15d189e2b0de6fa9f1fcaa0725291062",
      "signature": {
        "s": "0x63c436a1100a2906dfbf692a0d4e39a8739817e330101b5964333d01869d13f3",
        "r": "0x7e1404ba5aa73e64b1c161881c9ee6cddcd213fa095ec17ff5ae07abcf57c4ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3644020253",
    "total": "85043935867"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3644020253",
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
            "amount": "27684326635119157508623"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3644020"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYTlhYjk5NS05NDE2LTVkYjMtOTM0MS0xNzNmNGYwZTg5NjMifQ==",
    "nonce": 111425,
    "balances": {
      "current": "288286481799559839761627",
      "previous": "288286481799563487425900"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb0ca775f52adda54cc71757e2bd40aebc3002e9",
    "nonce": 40,
    "balances": {
      "current": "38730252259416515136",
      "previous": "38730252255772494883"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:14.526Z",
  "updated": "2022-05-04T08:58:14.612Z",
  "id": "62724026bbd75600116d06a5"
}
```
* *stageAmount*: `38730252259416515136`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000d933561d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000d933561d00000000000000000000000000000000000000000000000000000013cd037a7b8af793a60bd6ffb8d3a42be7d2049054d168dc70b0016fd67d9e8df198292c69752a9f522bdcfa9b89c44a5146e8b48d03d7aacbb3e2d345a423342088a9f10250a3d0bcccdf7e363804732a038b661792243bceafb87129fc669149e23cb8c3000000000000000000000000000000000000000000000000000000000000001b071fd3245514d711be070a84542ca1eb15d189e2b0de6fa9f1fcaa07252910627e1404ba5aa73e64b1c161881c9ee6cddcd213fa095ec17ff5ae07abcf57c4ea63c436a1100a2906dfbf692a0d4e39a8739817e330101b5964333d01869d13f3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b341000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d0c0a9f4d7516e844db000000000000000000000000000000000000000000003d0c0a9f4d75f053356c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000379a740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc535eccac29cfa0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6959546c68596a6b354e5330354e4445324c54566b596a4d744f544d304d5330784e7a4e6d4e4759775a5467354e6a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000028000000000000000000000000eb0ca775f52adda54cc71757e2bd40aebc3002e9000000000000000000000000000000000000000000000002197d7f3a6fcaa240000000000000000000000000000000000000000000000002197d7f3996974c2300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8af793a60bd6ffb8d3a42be7d2049054d168dc70b0016fd67d9e8df198292c69",
      "signature": {
        "s": "0x50a3d0bcccdf7e363804732a038b661792243bceafb87129fc669149e23cb8c3",
        "r": "0x752a9f522bdcfa9b89c44a5146e8b48d03d7aacbb3e2d345a423342088a9f102",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x071fd3245514d711be070a84542ca1eb15d189e2b0de6fa9f1fcaa0725291062",
      "signature": {
        "s": "0x63c436a1100a2906dfbf692a0d4e39a8739817e330101b5964333d01869d13f3",
        "r": "0x7e1404ba5aa73e64b1c161881c9ee6cddcd213fa095ec17ff5ae07abcf57c4ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3644020253",
    "total": "85043935867"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3644020253",
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
            "amount": "27684326635119157508623"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3644020"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiYTlhYjk5NS05NDE2LTVkYjMtOTM0MS0xNzNmNGYwZTg5NjMifQ==",
    "nonce": 111425,
    "balances": {
      "current": "288286481799559839761627",
      "previous": "288286481799563487425900"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb0ca775f52adda54cc71757e2bd40aebc3002e9",
    "nonce": 40,
    "balances": {
      "current": "38730252259416515136",
      "previous": "38730252255772494883"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:14.526Z",
  "updated": "2022-05-04T08:58:14.612Z",
  "id": "62724026bbd75600116d06a5"
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
0x0f200f9b000000000000000000000000000000000000000000000002197d7f3a6fcaa2400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `38730252259416515136`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`