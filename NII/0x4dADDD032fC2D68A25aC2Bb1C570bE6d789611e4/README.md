# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4dADDD032fC2D68A25aC2Bb1C570bE6d789611e4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000079e49c354235c9ee10000000000000000000000000000000000000000000000002e3d3763c31f50500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002e3d3763c31f50500000000000000000000000000000000000000000000000051183cceb0729e6e98254553fb65f5459c345f1712450df523d9e070f7138b5a3d1bb3dc78b211849c2faaedc76a2da31e3948a1ad652bb8711bfba83665a5cfd8eb4eefffef343272a0278ccbde5f8d27aedd67463bfaf17fff23500dec7498d07afe6baab50fd52000000000000000000000000000000000000000000000000000000000000001cf55729ee07defb597b9435bb2cf74b6b333b6fb5b0aa092f18e3ff4837507a646b487cc0adb189588d57e69e4dbcd3f4f6abde4f77e7935ab75113006a76600843b0e2be966f1d6c7c87aa0fd71ba7dd3bbcb8ee842d61d52d4ed921ae295ab5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae74000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009624337c8d22a655146300000000000000000000000000000000000000000000962461c59ada39440a6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000bd653cfcfa5b60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fc27a3546ed771780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6a4a6b596a466a4f5330774e7a4d784c5455784d3249744f446c6a597930785a44497a4d7a686c597a4d335a546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004daddd032fc2d68a25ac2bb1c570be6d789611e40000000000000000000000000000000000000000000000079e49c354235c9ee1000000000000000000000000000000000000000000000007700c8bf0603d4e9100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8254553fb65f5459c345f1712450df523d9e070f7138b5a3d1bb3dc78b211849",
      "signature": {
        "s": "0x2a0278ccbde5f8d27aedd67463bfaf17fff23500dec7498d07afe6baab50fd52",
        "r": "0xc2faaedc76a2da31e3948a1ad652bb8711bfba83665a5cfd8eb4eefffef34327",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf55729ee07defb597b9435bb2cf74b6b333b6fb5b0aa092f18e3ff4837507a64",
      "signature": {
        "s": "0x43b0e2be966f1d6c7c87aa0fd71ba7dd3bbcb8ee842d61d52d4ed921ae295ab5",
        "r": "0x6b487cc0adb189588d57e69e4dbcd3f4f6abde4f77e7935ab75113006a766008",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3331880200938934352",
    "total": "93495797998951196393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3331880200938934352",
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
            "amount": "27264010667673689485688"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3331880200938934"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZjJkYjFjOS0wNzMxLTUxM2ItODljYy0xZDIzMzhlYzM3ZTkifQ==",
    "nonce": 110196,
    "balances": {
      "current": "709022765212473331356771",
      "previous": "709026100424554471230057"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4daddd032fc2d68a25ac2bb1c570be6d789611e4",
    "nonce": 46,
    "balances": {
      "current": "140533070813397294817",
      "previous": "137201190612458360465"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:52:01.696Z",
  "updated": "2022-05-04T08:52:02.048Z",
  "id": "62723eb13592fd001130b48e"
}
```
* *stageAmount*: `140533070813397294817`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000002e3d3763c31f50500000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002e3d3763c31f50500000000000000000000000000000000000000000000000051183cceb0729e6e98254553fb65f5459c345f1712450df523d9e070f7138b5a3d1bb3dc78b211849c2faaedc76a2da31e3948a1ad652bb8711bfba83665a5cfd8eb4eefffef343272a0278ccbde5f8d27aedd67463bfaf17fff23500dec7498d07afe6baab50fd52000000000000000000000000000000000000000000000000000000000000001cf55729ee07defb597b9435bb2cf74b6b333b6fb5b0aa092f18e3ff4837507a646b487cc0adb189588d57e69e4dbcd3f4f6abde4f77e7935ab75113006a76600843b0e2be966f1d6c7c87aa0fd71ba7dd3bbcb8ee842d61d52d4ed921ae295ab5000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae74000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009624337c8d22a655146300000000000000000000000000000000000000000000962461c59ada39440a6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000bd653cfcfa5b60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5fc27a3546ed771780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6a4a6b596a466a4f5330774e7a4d784c5455784d3249744f446c6a597930785a44497a4d7a686c597a4d335a546b6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004daddd032fc2d68a25ac2bb1c570be6d789611e40000000000000000000000000000000000000000000000079e49c354235c9ee1000000000000000000000000000000000000000000000007700c8bf0603d4e9100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8254553fb65f5459c345f1712450df523d9e070f7138b5a3d1bb3dc78b211849",
      "signature": {
        "s": "0x2a0278ccbde5f8d27aedd67463bfaf17fff23500dec7498d07afe6baab50fd52",
        "r": "0xc2faaedc76a2da31e3948a1ad652bb8711bfba83665a5cfd8eb4eefffef34327",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf55729ee07defb597b9435bb2cf74b6b333b6fb5b0aa092f18e3ff4837507a64",
      "signature": {
        "s": "0x43b0e2be966f1d6c7c87aa0fd71ba7dd3bbcb8ee842d61d52d4ed921ae295ab5",
        "r": "0x6b487cc0adb189588d57e69e4dbcd3f4f6abde4f77e7935ab75113006a766008",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3331880200938934352",
    "total": "93495797998951196393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3331880200938934352",
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
            "amount": "27264010667673689485688"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3331880200938934"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZjJkYjFjOS0wNzMxLTUxM2ItODljYy0xZDIzMzhlYzM3ZTkifQ==",
    "nonce": 110196,
    "balances": {
      "current": "709022765212473331356771",
      "previous": "709026100424554471230057"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4daddd032fc2d68a25ac2bb1c570be6d789611e4",
    "nonce": 46,
    "balances": {
      "current": "140533070813397294817",
      "previous": "137201190612458360465"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:52:01.696Z",
  "updated": "2022-05-04T08:52:02.048Z",
  "id": "62723eb13592fd001130b48e"
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
0x0f200f9b0000000000000000000000000000000000000000000000079e49c354235c9ee10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `140533070813397294817`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`
