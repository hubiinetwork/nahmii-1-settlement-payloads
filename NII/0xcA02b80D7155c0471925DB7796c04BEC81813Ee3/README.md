# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcA02b80D7155c0471925DB7796c04BEC81813Ee3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000015bdc5aa3341b44000000000000000000000000000000000000000000000000015bdc5aa3341b440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000015bdc5aa3341b44000000000000000000000000000000000000000000000000015bdc5aa3341b4477c693c8603b3f0cd1fb57b4bce485903acc48cf11a8318b2da196218b5dd8902d46dca3ec3494caf74b96c146179a8fedf39b3ee5f1ce6a571feb72c38244973e27dcb8cae8415be34172d7c22ac97bf28f142e18c6a5d956876a4b57c9214a000000000000000000000000000000000000000000000000000000000000001b1ecbda046674fa1edc53667ec89baf438859bb5b85c6fb03937e0f7cfc90bff50afd8fc07ec155413418006aa02f1439ffb59486a28312f24b82308d95d8fb503c3081ed91fc8a19ff170e0e502fd7f52db7eb331630bc9e7c0a5d6edde78bbe000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e07000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000235c4bddeb41d699da7400000000000000000000000000000000000000000000235c4d3a20a9e0e1364200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000590d6713408a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9fc1c89fcae21d0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f5759324d3249784d5330354e5745774c54566a4e4745744f4751344d6930334e546b314e57597a4e54526b4f574d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ca02b80d7155c0471925db7796c04bec81813ee3000000000000000000000000000000000000000000000000015bdc5aa3341b44000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77c693c8603b3f0cd1fb57b4bce485903acc48cf11a8318b2da196218b5dd890",
      "signature": {
        "s": "0x3e27dcb8cae8415be34172d7c22ac97bf28f142e18c6a5d956876a4b57c9214a",
        "r": "0x2d46dca3ec3494caf74b96c146179a8fedf39b3ee5f1ce6a571feb72c3824497",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1ecbda046674fa1edc53667ec89baf438859bb5b85c6fb03937e0f7cfc90bff5",
      "signature": {
        "s": "0x3c3081ed91fc8a19ff170e0e502fd7f52db7eb331630bc9e7c0a5d6edde78bbe",
        "r": "0x0afd8fc07ec155413418006aa02f1439ffb59486a28312f24b82308d95d8fb50",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "97914098761866052",
    "total": "97914098761866052"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "97914098761866052",
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
            "amount": "16816495553860566392079"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "97914098761866"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOWY2M2IxMS05NWEwLTVjNGEtOGQ4Mi03NTk1NWYzNTRkOWMifQ==",
    "nonce": 77319,
    "balances": {
      "current": "166985394139409564686964",
      "previous": "166985492151422425314882"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca02b80d7155c0471925db7796c04bec81813ee3",
    "nonce": 1,
    "balances": {
      "current": "97914098761866052",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:36.194Z",
  "updated": "2021-06-04T12:46:36.265Z",
  "id": "60ba20ac010ba300120bfdd4"
}
```
* *stageAmount*: `97914098761866052`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000015bdc5aa3341b440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000015bdc5aa3341b44000000000000000000000000000000000000000000000000015bdc5aa3341b4477c693c8603b3f0cd1fb57b4bce485903acc48cf11a8318b2da196218b5dd8902d46dca3ec3494caf74b96c146179a8fedf39b3ee5f1ce6a571feb72c38244973e27dcb8cae8415be34172d7c22ac97bf28f142e18c6a5d956876a4b57c9214a000000000000000000000000000000000000000000000000000000000000001b1ecbda046674fa1edc53667ec89baf438859bb5b85c6fb03937e0f7cfc90bff50afd8fc07ec155413418006aa02f1439ffb59486a28312f24b82308d95d8fb503c3081ed91fc8a19ff170e0e502fd7f52db7eb331630bc9e7c0a5d6edde78bbe000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e07000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000235c4bddeb41d699da7400000000000000000000000000000000000000000000235c4d3a20a9e0e1364200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000590d6713408a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9fc1c89fcae21d0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f5759324d3249784d5330354e5745774c54566a4e4745744f4751344d6930334e546b314e57597a4e54526b4f574d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ca02b80d7155c0471925db7796c04bec81813ee3000000000000000000000000000000000000000000000000015bdc5aa3341b44000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77c693c8603b3f0cd1fb57b4bce485903acc48cf11a8318b2da196218b5dd890",
      "signature": {
        "s": "0x3e27dcb8cae8415be34172d7c22ac97bf28f142e18c6a5d956876a4b57c9214a",
        "r": "0x2d46dca3ec3494caf74b96c146179a8fedf39b3ee5f1ce6a571feb72c3824497",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1ecbda046674fa1edc53667ec89baf438859bb5b85c6fb03937e0f7cfc90bff5",
      "signature": {
        "s": "0x3c3081ed91fc8a19ff170e0e502fd7f52db7eb331630bc9e7c0a5d6edde78bbe",
        "r": "0x0afd8fc07ec155413418006aa02f1439ffb59486a28312f24b82308d95d8fb50",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "97914098761866052",
    "total": "97914098761866052"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "97914098761866052",
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
            "amount": "16816495553860566392079"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "97914098761866"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOWY2M2IxMS05NWEwLTVjNGEtOGQ4Mi03NTk1NWYzNTRkOWMifQ==",
    "nonce": 77319,
    "balances": {
      "current": "166985394139409564686964",
      "previous": "166985492151422425314882"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xca02b80d7155c0471925db7796c04bec81813ee3",
    "nonce": 1,
    "balances": {
      "current": "97914098761866052",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:36.194Z",
  "updated": "2021-06-04T12:46:36.265Z",
  "id": "60ba20ac010ba300120bfdd4"
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
0x0f200f9b000000000000000000000000000000000000000000000000015bdc5aa3341b440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `97914098761866052`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`