# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7ce7aaA66d826b1Ec1BB73C6863d7c9D3f1C4432`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c766320000000000000000000000000000000000000000000000000000000052c76632000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c766320000000000000000000000000000000000000000000000000000000052c766324b21c1d76419a9fab40d5fd1a473ea2842470078718d47bddf2e9c9587f88e565bb9cc1b21b87eedaa53c1a577c025f10685774e35aa6445e1ff42702056369842f99cf272f2751482674dec44160f6da48972a7d4fa97fc6929a0e25d2db38d000000000000000000000000000000000000000000000000000000000000001c8a12a692a8c72068ed9a3f76b1bbc8bbd5f91e3d2eaf356a2d480ec6930b57ee2d99b8da18ca919d6f77652c0585eaf500befab975cfd6fba4c17b64b366aba5385d1c95e9a7fabcd1b5c1e57df589fb5829ea4f8b6629db2b57fa96cc2c5830000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2bfd51e961000000000000000000000000000000000000000000000000002e1b2c502e809200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d78ba35000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e446b304e6a466c5979316a5a47566a4c545579596d59744f445577597930304e7a6b324f574a6b4f4745334d6a416966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007ce7aaa66d826b1ec1bb73c6863d7c9d3f1c44320000000000000000000000000000000000000000000000000000000052c76632000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b21c1d76419a9fab40d5fd1a473ea2842470078718d47bddf2e9c9587f88e56",
      "signature": {
        "s": "0x42f99cf272f2751482674dec44160f6da48972a7d4fa97fc6929a0e25d2db38d",
        "r": "0x5bb9cc1b21b87eedaa53c1a577c025f10685774e35aa6445e1ff427020563698",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8a12a692a8c72068ed9a3f76b1bbc8bbd5f91e3d2eaf356a2d480ec6930b57ee",
      "signature": {
        "s": "0x385d1c95e9a7fabcd1b5c1e57df589fb5829ea4f8b6629db2b57fa96cc2c5830",
        "r": "0x2d99b8da18ca919d6f77652c0585eaf500befab975cfd6fba4c17b64b366aba5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1388799538",
    "total": "1388799538"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799538",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "39954463285"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNDk0NjFlYy1jZGVjLTUyYmYtODUwYy00Nzk2OWJkOGE3MjAifQ==",
    "nonce": 5950,
    "balances": {
      "current": "12977724676237665",
      "previous": "12977726066426002"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7ce7aaa66d826b1ec1bb73c6863d7c9d3f1c4432",
    "nonce": 22,
    "balances": {
      "current": "1388799538",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:15.726Z",
  "updated": "2020-05-22T08:45:15.790Z",
  "id": "5ec7911bb0c6090011d5b07d"
}
```
* *stageAmount*: `1388799538`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c76632000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c766320000000000000000000000000000000000000000000000000000000052c766324b21c1d76419a9fab40d5fd1a473ea2842470078718d47bddf2e9c9587f88e565bb9cc1b21b87eedaa53c1a577c025f10685774e35aa6445e1ff42702056369842f99cf272f2751482674dec44160f6da48972a7d4fa97fc6929a0e25d2db38d000000000000000000000000000000000000000000000000000000000000001c8a12a692a8c72068ed9a3f76b1bbc8bbd5f91e3d2eaf356a2d480ec6930b57ee2d99b8da18ca919d6f77652c0585eaf500befab975cfd6fba4c17b64b366aba5385d1c95e9a7fabcd1b5c1e57df589fb5829ea4f8b6629db2b57fa96cc2c5830000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2bfd51e961000000000000000000000000000000000000000000000000002e1b2c502e809200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d78ba35000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e446b304e6a466c5979316a5a47566a4c545579596d59744f445577597930304e7a6b324f574a6b4f4745334d6a416966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007ce7aaa66d826b1ec1bb73c6863d7c9d3f1c44320000000000000000000000000000000000000000000000000000000052c76632000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4b21c1d76419a9fab40d5fd1a473ea2842470078718d47bddf2e9c9587f88e56",
      "signature": {
        "s": "0x42f99cf272f2751482674dec44160f6da48972a7d4fa97fc6929a0e25d2db38d",
        "r": "0x5bb9cc1b21b87eedaa53c1a577c025f10685774e35aa6445e1ff427020563698",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8a12a692a8c72068ed9a3f76b1bbc8bbd5f91e3d2eaf356a2d480ec6930b57ee",
      "signature": {
        "s": "0x385d1c95e9a7fabcd1b5c1e57df589fb5829ea4f8b6629db2b57fa96cc2c5830",
        "r": "0x2d99b8da18ca919d6f77652c0585eaf500befab975cfd6fba4c17b64b366aba5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1388799538",
    "total": "1388799538"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799538",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "39954463285"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNDk0NjFlYy1jZGVjLTUyYmYtODUwYy00Nzk2OWJkOGE3MjAifQ==",
    "nonce": 5950,
    "balances": {
      "current": "12977724676237665",
      "previous": "12977726066426002"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7ce7aaa66d826b1ec1bb73c6863d7c9d3f1c4432",
    "nonce": 22,
    "balances": {
      "current": "1388799538",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:15.726Z",
  "updated": "2020-05-22T08:45:15.790Z",
  "id": "5ec7911bb0c6090011d5b07d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c76632000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388799538`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`