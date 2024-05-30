# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x80A21a86555aA95aB467915ec42c0d77391798E7`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b758224ef99e00000000000000000000000000000000000000000000007af7f86f66751e30000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000007af7f86f66751e300000000000000000000000000000000000000000000000007af7f86f66751e3000a1aa14c290aadf53326759158b34f7f32c6ce9464e9cad7591f628071a0bbf86ce1f7d2f443931f51f5ab9912f3a1177a8a3a5ec95d04e365bb9719f721f4e4e5515a0a5c17056bbb8382fc3d0b03f512355fd3133579f380da6fe948464ab00000000000000000000000000000000000000000000000000000000000000001bbc3eafd1e895ec25d35c1a373121f484db2196eabf3bca7e0446dd8a3c2e09e4ce800c281432a22c2e2c53382eea2b55b6e593ddcae860829652849d1f25d2e21ff090b7a9092e35790e46964ab4587f4fcb56c1c0b8fa71528624535f975a2d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e236500000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000080a21a86555aa95ab467915ec42c0d77391798e70000000000000000000000000000000000000000000000000de0b758224ef99e00000000000000000000000000000000000000000000007b255406168080e79e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001f7adf57e913be000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f7adf57e913be000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593255314d4467795a43316b4f544d304c5451784e544d74596d45334f43316d5a5463774f475a694f5759334e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000072000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000064161f4cb7fd9455977000000000000000000000000000000000000000000000639b275448971f37677000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1aa14c290aadf53326759158b34f7f32c6ce9464e9cad7591f628071a0bbf86",
      "signature": {
        "s": "0x5515a0a5c17056bbb8382fc3d0b03f512355fd3133579f380da6fe948464ab00",
        "r": "0xce1f7d2f443931f51f5ab9912f3a1177a8a3a5ec95d04e365bb9719f721f4e4e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbc3eafd1e895ec25d35c1a373121f484db2196eabf3bca7e0446dd8a3c2e09e4",
      "signature": {
        "s": "0x1ff090b7a9092e35790e46964ab4587f4fcb56c1c0b8fa71528624535f975a2d",
        "r": "0xce800c281432a22c2e2c53382eea2b55b6e593ddcae860829652849d1f25d2e2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2268370931000000000000",
    "total": "2268370931000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2268370931000000000000",
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
            "amount": "2268370931000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2268370931000000000"
      }
    },
    "wallet": "0x80a21a86555aa95ab467915ec42c0d77391798e7",
    "data": "eyJyZWYiOiI4Y2U1MDgyZC1kOTM0LTQxNTMtYmE3OC1mZTcwOGZiOWY3NzMifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000000706436856222",
      "previous": "2271639302637436856222"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 114,
    "balances": {
      "current": "472644732036399280527216",
      "previous": "470376361105399280527216"
    }
  },
  "blockNumber": "14825040",
  "created": "2022-05-22T18:55:48.259Z",
  "updated": "2022-05-22T18:55:48.376Z",
  "id": "628a87347832e20011830f37"
}
```
* *stageAmount*: `1000000706436856222`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000007af7f86f66751e30000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000007af7f86f66751e300000000000000000000000000000000000000000000000007af7f86f66751e3000a1aa14c290aadf53326759158b34f7f32c6ce9464e9cad7591f628071a0bbf86ce1f7d2f443931f51f5ab9912f3a1177a8a3a5ec95d04e365bb9719f721f4e4e5515a0a5c17056bbb8382fc3d0b03f512355fd3133579f380da6fe948464ab00000000000000000000000000000000000000000000000000000000000000001bbc3eafd1e895ec25d35c1a373121f484db2196eabf3bca7e0446dd8a3c2e09e4ce800c281432a22c2e2c53382eea2b55b6e593ddcae860829652849d1f25d2e21ff090b7a9092e35790e46964ab4587f4fcb56c1c0b8fa71528624535f975a2d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e236500000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000080a21a86555aa95ab467915ec42c0d77391798e70000000000000000000000000000000000000000000000000de0b758224ef99e00000000000000000000000000000000000000000000007b255406168080e79e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001f7adf57e913be000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001f7adf57e913be000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593255314d4467795a43316b4f544d304c5451784e544d74596d45334f43316d5a5463774f475a694f5759334e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000072000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000064161f4cb7fd9455977000000000000000000000000000000000000000000000639b275448971f37677000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1aa14c290aadf53326759158b34f7f32c6ce9464e9cad7591f628071a0bbf86",
      "signature": {
        "s": "0x5515a0a5c17056bbb8382fc3d0b03f512355fd3133579f380da6fe948464ab00",
        "r": "0xce1f7d2f443931f51f5ab9912f3a1177a8a3a5ec95d04e365bb9719f721f4e4e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbc3eafd1e895ec25d35c1a373121f484db2196eabf3bca7e0446dd8a3c2e09e4",
      "signature": {
        "s": "0x1ff090b7a9092e35790e46964ab4587f4fcb56c1c0b8fa71528624535f975a2d",
        "r": "0xce800c281432a22c2e2c53382eea2b55b6e593ddcae860829652849d1f25d2e2",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2268370931000000000000",
    "total": "2268370931000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2268370931000000000000",
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
            "amount": "2268370931000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2268370931000000000"
      }
    },
    "wallet": "0x80a21a86555aa95ab467915ec42c0d77391798e7",
    "data": "eyJyZWYiOiI4Y2U1MDgyZC1kOTM0LTQxNTMtYmE3OC1mZTcwOGZiOWY3NzMifQ==",
    "nonce": 12,
    "balances": {
      "current": "1000000706436856222",
      "previous": "2271639302637436856222"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 114,
    "balances": {
      "current": "472644732036399280527216",
      "previous": "470376361105399280527216"
    }
  },
  "blockNumber": "14825040",
  "created": "2022-05-22T18:55:48.259Z",
  "updated": "2022-05-22T18:55:48.376Z",
  "id": "628a87347832e20011830f37"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b758224ef99e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000000706436856222`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`