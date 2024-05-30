# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x111b58C01afa72D04bc0aDb523266Aa55749ED92`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000044236ec91121e00000000000000000000000000000000000000000000000000027420fe3c829f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000027420fe3c829f00000000000000000000000000000000000000000000000000044236ec91121e07bdc616a3e34788f2f04d64dc411236347df063ae397d4f4bf9bf43d23b9fc2337e7c8440481642a7e65f5a891483b0c60752bd5ba0698ee3e8fecc54b4a3cd64d235b7560122e751bb446dcb9e1d805ae21b259d277a42b50559597ba44295000000000000000000000000000000000000000000000000000000000000001b3f72baaa0a73d2d4fc8a6b25e77319c3f2b329cdae8d99286dabcaa52e473e95ad0ed042633e84af511a748ed8c55ae0a1b725f135a14c023bdaacce56b1beee030b4a14a3c71e5bf5ea3826becbd4ae49e91f341777973a074daf34f22b105e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d69000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026f97cbeceb080d030890000000000000000000000000000000000000000000026f97cc143724c1a959700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000a0cd0de26f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038eb3250b256fab13520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954686c5a6d4979597930784e6d51344c5455304e4455744f4468684e4331685a57597a4f5455304e6a56695a44556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000111b58c01afa72d04bc0adb523266aa55749ed9200000000000000000000000000000000000000000000000000044236ec91121e0000000000000000000000000000000000000000000000000001ce15ee548f7f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x07bdc616a3e34788f2f04d64dc411236347df063ae397d4f4bf9bf43d23b9fc2",
      "signature": {
        "s": "0x64d235b7560122e751bb446dcb9e1d805ae21b259d277a42b50559597ba44295",
        "r": "0x337e7c8440481642a7e65f5a891483b0c60752bd5ba0698ee3e8fecc54b4a3cd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f72baaa0a73d2d4fc8a6b25e77319c3f2b329cdae8d99286dabcaa52e473e95",
      "signature": {
        "s": "0x030b4a14a3c71e5bf5ea3826becbd4ae49e91f341777973a074daf34f22b105e",
        "r": "0xad0ed042633e84af511a748ed8c55ae0a1b725f135a14c023bdaacce56b1beee",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "690635006575263",
    "total": "1198703571440158"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "690635006575263",
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
            "amount": "16799445843238034543442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "690635006575"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYThlZmIyYy0xNmQ4LTU0NDUtODhhNC1hZWYzOTU0NjViZDUifQ==",
    "nonce": 77161,
    "balances": {
      "current": "184052154472563945255049",
      "previous": "184052155163889586836887"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x111b58c01afa72d04bc0adb523266aa55749ed92",
    "nonce": 2,
    "balances": {
      "current": "1198703571440158",
      "previous": "508068564864895"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:45:52.640Z",
  "updated": "2021-06-04T12:45:52.744Z",
  "id": "60ba20800779920010014b81"
}
```
* *stageAmount*: `1198703571440158`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000027420fe3c829f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000027420fe3c829f00000000000000000000000000000000000000000000000000044236ec91121e07bdc616a3e34788f2f04d64dc411236347df063ae397d4f4bf9bf43d23b9fc2337e7c8440481642a7e65f5a891483b0c60752bd5ba0698ee3e8fecc54b4a3cd64d235b7560122e751bb446dcb9e1d805ae21b259d277a42b50559597ba44295000000000000000000000000000000000000000000000000000000000000001b3f72baaa0a73d2d4fc8a6b25e77319c3f2b329cdae8d99286dabcaa52e473e95ad0ed042633e84af511a748ed8c55ae0a1b725f135a14c023bdaacce56b1beee030b4a14a3c71e5bf5ea3826becbd4ae49e91f341777973a074daf34f22b105e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d69000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000026f97cbeceb080d030890000000000000000000000000000000000000000000026f97cc143724c1a959700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000a0cd0de26f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038eb3250b256fab13520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5954686c5a6d4979597930784e6d51344c5455304e4455744f4468684e4331685a57597a4f5455304e6a56695a44556966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000111b58c01afa72d04bc0adb523266aa55749ed9200000000000000000000000000000000000000000000000000044236ec91121e0000000000000000000000000000000000000000000000000001ce15ee548f7f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x07bdc616a3e34788f2f04d64dc411236347df063ae397d4f4bf9bf43d23b9fc2",
      "signature": {
        "s": "0x64d235b7560122e751bb446dcb9e1d805ae21b259d277a42b50559597ba44295",
        "r": "0x337e7c8440481642a7e65f5a891483b0c60752bd5ba0698ee3e8fecc54b4a3cd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f72baaa0a73d2d4fc8a6b25e77319c3f2b329cdae8d99286dabcaa52e473e95",
      "signature": {
        "s": "0x030b4a14a3c71e5bf5ea3826becbd4ae49e91f341777973a074daf34f22b105e",
        "r": "0xad0ed042633e84af511a748ed8c55ae0a1b725f135a14c023bdaacce56b1beee",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "690635006575263",
    "total": "1198703571440158"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "690635006575263",
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
            "amount": "16799445843238034543442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "690635006575"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYThlZmIyYy0xNmQ4LTU0NDUtODhhNC1hZWYzOTU0NjViZDUifQ==",
    "nonce": 77161,
    "balances": {
      "current": "184052154472563945255049",
      "previous": "184052155163889586836887"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x111b58c01afa72d04bc0adb523266aa55749ed92",
    "nonce": 2,
    "balances": {
      "current": "1198703571440158",
      "previous": "508068564864895"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:45:52.640Z",
  "updated": "2021-06-04T12:45:52.744Z",
  "id": "60ba20800779920010014b81"
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
0x0f200f9b00000000000000000000000000000000000000000000000000044236ec91121e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1198703571440158`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`