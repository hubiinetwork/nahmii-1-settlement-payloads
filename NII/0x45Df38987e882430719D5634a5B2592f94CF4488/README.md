# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x45Df38987e882430719D5634a5B2592f94CF4488`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003a0b568eb2e4953cf0000000000000000000000000000000000000000000000001604c50aef330ed10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50aef330ed100000000000000000000000000000000000000000000000269dd3d023420287424067f0e9430985fc185dcbec4ff0f16c7b854908eae45cb1731ad8dd8db88d4ed8d5032f76c7d82313d9d678516b2ceeec3d2b38b4d36cb1c0c670ce3a946282b506d26ff7b5e8658cabb433073f150775e6c5a2f6581b7a5e0dab3a5b1ca3d000000000000000000000000000000000000000000000000000000000000001beb0a4e6190540ff0aaf32e678917aecc8de6b248e776e008c04baebe634723fdb2f26f4e378397a0ebf39043553378430459349eb3b72345b356d2e46faba135298ea23570ece087028e57da4e84d01dcacd1267a49af162d2a34ea7d6365891000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afcb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052bb6554ca559a89aef10000000000000000000000000000000000000000000052bb7b5f3263e08124f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356c4672e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7397bd14d7a1b29010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e6d59345a444d784e793078593259354c54557a5a47517459546c6d4d53316859544130597a59334d6d51304e54676966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000045df38987e882430719d5634a5b2592f94cf4488000000000000000000000000000000000000000000000003a0b568eb2e4953cf0000000000000000000000000000000000000000000000038ab0a3e03f1644fe00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24067f0e9430985fc185dcbec4ff0f16c7b854908eae45cb1731ad8dd8db88d4",
      "signature": {
        "s": "0x2b506d26ff7b5e8658cabb433073f150775e6c5a2f6581b7a5e0dab3a5b1ca3d",
        "r": "0xed8d5032f76c7d82313d9d678516b2ceeec3d2b38b4d36cb1c0c670ce3a94628",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xeb0a4e6190540ff0aaf32e678917aecc8de6b248e776e008c04baebe634723fd",
      "signature": {
        "s": "0x298ea23570ece087028e57da4e84d01dcacd1267a49af162d2a34ea7d6365891",
        "r": "0xb2f26f4e378397a0ebf39043553378430459349eb3b72345b356d2e46faba135",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1586609619494702801",
    "total": "44521808570928343156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609619494702801",
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
            "amount": "27582024524608768256257"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609619494702"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNmY4ZDMxNy0xY2Y5LTUzZGQtYTlmMS1hYTA0YzY3MmQ0NTgifQ==",
    "nonce": 110539,
    "balances": {
      "current": "390690894420459481837297",
      "previous": "390692482616688596034800"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x45df38987e882430719d5634a5b2592f94cf4488",
    "nonce": 46,
    "balances": {
      "current": "66920509597284914127",
      "previous": "65333899977790211326"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:48.196Z",
  "updated": "2022-05-04T08:53:48.306Z",
  "id": "62723f1c7832e20011830bd8"
}
```
* *stageAmount*: `66920509597284914127`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001604c50aef330ed10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001604c50aef330ed100000000000000000000000000000000000000000000000269dd3d023420287424067f0e9430985fc185dcbec4ff0f16c7b854908eae45cb1731ad8dd8db88d4ed8d5032f76c7d82313d9d678516b2ceeec3d2b38b4d36cb1c0c670ce3a946282b506d26ff7b5e8658cabb433073f150775e6c5a2f6581b7a5e0dab3a5b1ca3d000000000000000000000000000000000000000000000000000000000000001beb0a4e6190540ff0aaf32e678917aecc8de6b248e776e008c04baebe634723fdb2f26f4e378397a0ebf39043553378430459349eb3b72345b356d2e46faba135298ea23570ece087028e57da4e84d01dcacd1267a49af162d2a34ea7d6365891000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001afcb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052bb6554ca559a89aef10000000000000000000000000000000000000000000052bb7b5f3263e08124f000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005a30356c4672e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7397bd14d7a1b29010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e6d59345a444d784e793078593259354c54557a5a47517459546c6d4d53316859544130597a59334d6d51304e54676966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000045df38987e882430719d5634a5b2592f94cf4488000000000000000000000000000000000000000000000003a0b568eb2e4953cf0000000000000000000000000000000000000000000000038ab0a3e03f1644fe00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x24067f0e9430985fc185dcbec4ff0f16c7b854908eae45cb1731ad8dd8db88d4",
      "signature": {
        "s": "0x2b506d26ff7b5e8658cabb433073f150775e6c5a2f6581b7a5e0dab3a5b1ca3d",
        "r": "0xed8d5032f76c7d82313d9d678516b2ceeec3d2b38b4d36cb1c0c670ce3a94628",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xeb0a4e6190540ff0aaf32e678917aecc8de6b248e776e008c04baebe634723fd",
      "signature": {
        "s": "0x298ea23570ece087028e57da4e84d01dcacd1267a49af162d2a34ea7d6365891",
        "r": "0xb2f26f4e378397a0ebf39043553378430459349eb3b72345b356d2e46faba135",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1586609619494702801",
    "total": "44521808570928343156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1586609619494702801",
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
            "amount": "27582024524608768256257"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1586609619494702"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlNmY4ZDMxNy0xY2Y5LTUzZGQtYTlmMS1hYTA0YzY3MmQ0NTgifQ==",
    "nonce": 110539,
    "balances": {
      "current": "390690894420459481837297",
      "previous": "390692482616688596034800"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x45df38987e882430719d5634a5b2592f94cf4488",
    "nonce": 46,
    "balances": {
      "current": "66920509597284914127",
      "previous": "65333899977790211326"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:48.196Z",
  "updated": "2022-05-04T08:53:48.306Z",
  "id": "62723f1c7832e20011830bd8"
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
0x0f200f9b000000000000000000000000000000000000000000000003a0b568eb2e4953cf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `66920509597284914127`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`