# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x38CcD183e94419d15359dDE2DC597167130A908B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000022600000000000000000000000000000000000000000000000000000000000002260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000022600000000000000000000000000000000000000000000000000000000000002260b4200620ad3541aa31c320d4ab8a2c19016dc89b3653db6d50a469c87c8bbfba2fd84a78195a7011cc74f32b29976ac996874838028aace3990735f91008d94a2acb74ff1b0b844d1e6636111d441f39f2a3c68ca17ca2be2e0b28a76e1ea8cb000000000000000000000000000000000000000000000000000000000000001ce5a2df2f6d401396e2552dcd615bb5237a618552f688ae49d0795b5b1c591e3568a86f6263714ac26534319d7c04fbce7c89a55a736a09934bc7babe56fe4bb22481eebe6c42ddf1c66ff97b6115050060abb36053d87d41ce97784ca9071799000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004b400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fbb0c0000000000000000000000000000000000000000000000000002386f2c7fbd32800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009351200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f574e6a4f57566a4f5330774d4445784c5455304d4749744f444e6a4e7930334d44686b4d3249335a6d52695954416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000038ccd183e94419d15359dde2dc597167130a908b0000000000000000000000000000000000000000000000000000000000002260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4200620ad3541aa31c320d4ab8a2c19016dc89b3653db6d50a469c87c8bbfba",
      "signature": {
        "s": "0x2acb74ff1b0b844d1e6636111d441f39f2a3c68ca17ca2be2e0b28a76e1ea8cb",
        "r": "0x2fd84a78195a7011cc74f32b29976ac996874838028aace3990735f91008d94a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe5a2df2f6d401396e2552dcd615bb5237a618552f688ae49d0795b5b1c591e35",
      "signature": {
        "s": "0x2481eebe6c42ddf1c66ff97b6115050060abb36053d87d41ce97784ca9071799",
        "r": "0x68a86f6263714ac26534319d7c04fbce7c89a55a736a09934bc7babe56fe4bb2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8800",
    "total": "8800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8800",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "603410"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzOWNjOWVjOS0wMDExLTU0MGItODNjNy03MDhkM2I3ZmRiYTAifQ==",
    "nonce": 1204,
    "balances": {
      "current": "10000001480241344",
      "previous": "10000001480250152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38ccd183e94419d15359dde2dc597167130a908b",
    "nonce": 20,
    "balances": {
      "current": "8800",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:34.818Z",
  "updated": "2020-05-22T08:07:35.886Z",
  "id": "5ec78846005df800101bc3b1"
}
```
* *stageAmount*: `8800`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000002260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000022600000000000000000000000000000000000000000000000000000000000002260b4200620ad3541aa31c320d4ab8a2c19016dc89b3653db6d50a469c87c8bbfba2fd84a78195a7011cc74f32b29976ac996874838028aace3990735f91008d94a2acb74ff1b0b844d1e6636111d441f39f2a3c68ca17ca2be2e0b28a76e1ea8cb000000000000000000000000000000000000000000000000000000000000001ce5a2df2f6d401396e2552dcd615bb5237a618552f688ae49d0795b5b1c591e3568a86f6263714ac26534319d7c04fbce7c89a55a736a09934bc7babe56fe4bb22481eebe6c42ddf1c66ff97b6115050060abb36053d87d41ce97784ca9071799000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004b400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7fbb0c0000000000000000000000000000000000000000000000000002386f2c7fbd32800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009351200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f574e6a4f57566a4f5330774d4445784c5455304d4749744f444e6a4e7930334d44686b4d3249335a6d52695954416966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000038ccd183e94419d15359dde2dc597167130a908b0000000000000000000000000000000000000000000000000000000000002260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb4200620ad3541aa31c320d4ab8a2c19016dc89b3653db6d50a469c87c8bbfba",
      "signature": {
        "s": "0x2acb74ff1b0b844d1e6636111d441f39f2a3c68ca17ca2be2e0b28a76e1ea8cb",
        "r": "0x2fd84a78195a7011cc74f32b29976ac996874838028aace3990735f91008d94a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe5a2df2f6d401396e2552dcd615bb5237a618552f688ae49d0795b5b1c591e35",
      "signature": {
        "s": "0x2481eebe6c42ddf1c66ff97b6115050060abb36053d87d41ce97784ca9071799",
        "r": "0x68a86f6263714ac26534319d7c04fbce7c89a55a736a09934bc7babe56fe4bb2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8800",
    "total": "8800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8800",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "603410"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "8"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzOWNjOWVjOS0wMDExLTU0MGItODNjNy03MDhkM2I3ZmRiYTAifQ==",
    "nonce": 1204,
    "balances": {
      "current": "10000001480241344",
      "previous": "10000001480250152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38ccd183e94419d15359dde2dc597167130a908b",
    "nonce": 20,
    "balances": {
      "current": "8800",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:34.818Z",
  "updated": "2020-05-22T08:07:35.886Z",
  "id": "5ec78846005df800101bc3b1"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000022600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8800`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``