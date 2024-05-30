# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3Bd40c2671D121458b985C4f6d682d520E9961DD`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000003c54339ba47afdf0000000000000000000000000000000000000000000000000016e2a2093c1d570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000016e2a2093c1d5700000000000000000000000000000000000000000000000002822eefdd970a381600d2c2812b3c8303f6a4ba5bb9ee42cbe8c325cfb7280339d0df33acad0510a63dbf6b90b3d039de93a099a10bdd792db782bdffb46bc4de18bb059f577b5928bb0cc03e726afcbf0db919fc0940accc0a0f66f15af98c6342d21d5f508ddf000000000000000000000000000000000000000000000000000000000000001c9ccc8ba7e160e407ec1d0f17684b1bca4beb709ce62a9aad16842d8a5bca69dc050aca1df2e9908ec6237bf8a2d2841a73ac491e7b9aefec8b864f3e5fa7e40e4b463f7b90744b97335f7337d6746dfdebf298277f35862a0fbd48f57b378189000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b130000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004affb1ad5824c77d76a9000000000000000000000000000000000000000000004affb1c440a2a0181a2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000005dbcf5e862c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d933c7f0df8e43d5380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e7a426b5a6d55324e53307a4f544d784c5455774f444d74596a6c6b4d6930794f47497a4e6d566a59545a6a59544d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000003bd40c2671d121458b985c4f6d682d520e9961dd00000000000000000000000000000000000000000000000003c54339ba47afdf00000000000000000000000000000000000000000000000003ae6097b10b928800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1600d2c2812b3c8303f6a4ba5bb9ee42cbe8c325cfb7280339d0df33acad0510",
      "signature": {
        "s": "0x28bb0cc03e726afcbf0db919fc0940accc0a0f66f15af98c6342d21d5f508ddf",
        "r": "0xa63dbf6b90b3d039de93a099a10bdd792db782bdffb46bc4de18bb059f577b59",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9ccc8ba7e160e407ec1d0f17684b1bca4beb709ce62a9aad16842d8a5bca69dc",
      "signature": {
        "s": "0x4b463f7b90744b97335f7337d6746dfdebf298277f35862a0fbd48f57b378189",
        "r": "0x050aca1df2e9908ec6237bf8a2d2841a73ac491e7b9aefec8b864f3e5fa7e40e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6441635055148375",
    "total": "180758542797965880"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6441635055148375",
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
            "amount": "27618507094002453697848"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6441635055148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNzBkZmU2NS0zOTMxLTUwODMtYjlkMi0yOGIzNmVjYTZjYTMifQ==",
    "nonce": 110896,
    "balances": {
      "current": "354171842457380354619049",
      "previous": "354171848905457044822572"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3bd40c2671d121458b985c4f6d682d520e9961dd",
    "nonce": 46,
    "balances": {
      "current": "271697267743240159",
      "previous": "265255632688091784"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:34.004Z",
  "updated": "2022-05-04T08:55:34.083Z",
  "id": "62723f85bbd75600116d0607"
}
```
* *stageAmount*: `271697267743240159`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000016e2a2093c1d570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000016e2a2093c1d5700000000000000000000000000000000000000000000000002822eefdd970a381600d2c2812b3c8303f6a4ba5bb9ee42cbe8c325cfb7280339d0df33acad0510a63dbf6b90b3d039de93a099a10bdd792db782bdffb46bc4de18bb059f577b5928bb0cc03e726afcbf0db919fc0940accc0a0f66f15af98c6342d21d5f508ddf000000000000000000000000000000000000000000000000000000000000001c9ccc8ba7e160e407ec1d0f17684b1bca4beb709ce62a9aad16842d8a5bca69dc050aca1df2e9908ec6237bf8a2d2841a73ac491e7b9aefec8b864f3e5fa7e40e4b463f7b90744b97335f7337d6746dfdebf298277f35862a0fbd48f57b378189000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b130000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004affb1ad5824c77d76a9000000000000000000000000000000000000000000004affb1c440a2a0181a2c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000005dbcf5e862c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d933c7f0df8e43d5380000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e7a426b5a6d55324e53307a4f544d784c5455774f444d74596a6c6b4d6930794f47497a4e6d566a59545a6a59544d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000003bd40c2671d121458b985c4f6d682d520e9961dd00000000000000000000000000000000000000000000000003c54339ba47afdf00000000000000000000000000000000000000000000000003ae6097b10b928800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1600d2c2812b3c8303f6a4ba5bb9ee42cbe8c325cfb7280339d0df33acad0510",
      "signature": {
        "s": "0x28bb0cc03e726afcbf0db919fc0940accc0a0f66f15af98c6342d21d5f508ddf",
        "r": "0xa63dbf6b90b3d039de93a099a10bdd792db782bdffb46bc4de18bb059f577b59",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9ccc8ba7e160e407ec1d0f17684b1bca4beb709ce62a9aad16842d8a5bca69dc",
      "signature": {
        "s": "0x4b463f7b90744b97335f7337d6746dfdebf298277f35862a0fbd48f57b378189",
        "r": "0x050aca1df2e9908ec6237bf8a2d2841a73ac491e7b9aefec8b864f3e5fa7e40e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6441635055148375",
    "total": "180758542797965880"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6441635055148375",
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
            "amount": "27618507094002453697848"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6441635055148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNzBkZmU2NS0zOTMxLTUwODMtYjlkMi0yOGIzNmVjYTZjYTMifQ==",
    "nonce": 110896,
    "balances": {
      "current": "354171842457380354619049",
      "previous": "354171848905457044822572"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3bd40c2671d121458b985c4f6d682d520e9961dd",
    "nonce": 46,
    "balances": {
      "current": "271697267743240159",
      "previous": "265255632688091784"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:34.004Z",
  "updated": "2022-05-04T08:55:34.083Z",
  "id": "62723f85bbd75600116d0607"
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
0x0f200f9b00000000000000000000000000000000000000000000000003c54339ba47afdf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `271697267743240159`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`