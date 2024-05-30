# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4eC0B6Bf31A00F85D82a194FEd6da8a7eC311b52`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000218f7395d5439c91600000000000000000000000000000000000000000000000000000000b58318aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000b58318aa000000000000000000000000000000000000000000000000000000108c1d4298db20096b3b4040da611d80118bd9e10d19a8112055134a3dccf085e2211a276b8cee318b187d033c4da2439e12bad37780edbda8edabf0e38a175656dc2d54af74e8d7d7387be7dcf02c8a358df5a267d9ec25add9f4c6569c76c77fff5e7a1e000000000000000000000000000000000000000000000000000000000000001b5a618d2edee46634c5878b007d5e1b024d654383a614af1afd5d76300f128ff01d98ea3102162d86b458fe6e8ca89fe76e9fd42971049745189cdab9278858a66d23ec045b6aa675725f54a5d1b93ca02857918351339b013b7d0417731192af000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3e6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003a31c957ef2d29f980a4000000000000000000000000000000000000000000003a31c957ef2ddfab10e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002e77930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd7ff81b2d09b0e80a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e47526a5a6d593059793079593245314c5455324e546774596a67794f4330334d6a5578596a4a6c4d3256694d6a596966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000004ec0b6bf31a00f85d82a194fed6da8a7ec311b5200000000000000000000000000000000000000000000000218f7395d5439c91600000000000000000000000000000000000000000000000218f7395c9eb6b06c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb20096b3b4040da611d80118bd9e10d19a8112055134a3dccf085e2211a276b",
      "signature": {
        "s": "0x74e8d7d7387be7dcf02c8a358df5a267d9ec25add9f4c6569c76c77fff5e7a1e",
        "r": "0x8cee318b187d033c4da2439e12bad37780edbda8edabf0e38a175656dc2d54af",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5a618d2edee46634c5878b007d5e1b024d654383a614af1afd5d76300f128ff0",
      "signature": {
        "s": "0x6d23ec045b6aa675725f54a5d1b93ca02857918351339b013b7d0417731192af",
        "r": "0x1d98ea3102162d86b458fe6e8ca89fe76e9fd42971049745189cdab9278858a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3045267626",
    "total": "71070204568"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3045267626",
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
            "amount": "27697784004755328133130"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3045267"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NGRjZmY0Yy0yY2E1LTU2NTgtYjgyOC03MjUxYjJlM2ViMjYifQ==",
    "nonce": 111590,
    "balances": {
      "current": "274815654793753044549796",
      "previous": "274815654793756092862689"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4ec0b6bf31a00f85d82a194fed6da8a7ec311b52",
    "nonce": 29,
    "balances": {
      "current": "38692457796584720662",
      "previous": "38692457793539453036"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:08.083Z",
  "updated": "2022-05-04T08:59:08.178Z",
  "id": "6272405c7832e20011830d39"
}
```
* *stageAmount*: `38692457796584720662`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000b58318aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000b58318aa000000000000000000000000000000000000000000000000000000108c1d4298db20096b3b4040da611d80118bd9e10d19a8112055134a3dccf085e2211a276b8cee318b187d033c4da2439e12bad37780edbda8edabf0e38a175656dc2d54af74e8d7d7387be7dcf02c8a358df5a267d9ec25add9f4c6569c76c77fff5e7a1e000000000000000000000000000000000000000000000000000000000000001b5a618d2edee46634c5878b007d5e1b024d654383a614af1afd5d76300f128ff01d98ea3102162d86b458fe6e8ca89fe76e9fd42971049745189cdab9278858a66d23ec045b6aa675725f54a5d1b93ca02857918351339b013b7d0417731192af000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3e6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003a31c957ef2d29f980a4000000000000000000000000000000000000000000003a31c957ef2ddfab10e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002e77930000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd7ff81b2d09b0e80a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e47526a5a6d593059793079593245314c5455324e546774596a67794f4330334d6a5578596a4a6c4d3256694d6a596966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000004ec0b6bf31a00f85d82a194fed6da8a7ec311b5200000000000000000000000000000000000000000000000218f7395d5439c91600000000000000000000000000000000000000000000000218f7395c9eb6b06c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb20096b3b4040da611d80118bd9e10d19a8112055134a3dccf085e2211a276b",
      "signature": {
        "s": "0x74e8d7d7387be7dcf02c8a358df5a267d9ec25add9f4c6569c76c77fff5e7a1e",
        "r": "0x8cee318b187d033c4da2439e12bad37780edbda8edabf0e38a175656dc2d54af",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5a618d2edee46634c5878b007d5e1b024d654383a614af1afd5d76300f128ff0",
      "signature": {
        "s": "0x6d23ec045b6aa675725f54a5d1b93ca02857918351339b013b7d0417731192af",
        "r": "0x1d98ea3102162d86b458fe6e8ca89fe76e9fd42971049745189cdab9278858a6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3045267626",
    "total": "71070204568"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3045267626",
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
            "amount": "27697784004755328133130"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3045267"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NGRjZmY0Yy0yY2E1LTU2NTgtYjgyOC03MjUxYjJlM2ViMjYifQ==",
    "nonce": 111590,
    "balances": {
      "current": "274815654793753044549796",
      "previous": "274815654793756092862689"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4ec0b6bf31a00f85d82a194fed6da8a7ec311b52",
    "nonce": 29,
    "balances": {
      "current": "38692457796584720662",
      "previous": "38692457793539453036"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:08.083Z",
  "updated": "2022-05-04T08:59:08.178Z",
  "id": "6272405c7832e20011830d39"
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
0x0f200f9b00000000000000000000000000000000000000000000000218f7395d5439c9160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `38692457796584720662`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`