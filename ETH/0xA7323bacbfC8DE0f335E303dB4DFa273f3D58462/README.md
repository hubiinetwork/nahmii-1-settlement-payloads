# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA7323bacbfC8DE0f335E303dB4DFa273f3D58462`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792b363b54479d2d5147d6a683f8711923de2c50a73bd8378fcba12dd0a8f2132ec2167b2409f68ad1326c166e4f90a62c91f5878de8e405c5a4486004998afff653e1c96629e6902a5e727ca3f2c82b4e2300ef1f40e670b697e955b1977a23c59000000000000000000000000000000000000000000000000000000000000001c5f3e926d8a44af2122113bb69a1587a0969fda51fb6b4e4d07296912d32c2f2d9da30fa81e3dd8e32c5f6a8852b24b1ad5928f9b8c3c3266182e274571382bf81cc27d00609df166955ab45f4cd255c707849a44f9f79b8e9eca1200d197d0a5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007bc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3be2c6a000000000000000000000000000000000000000000000000002386f2c3be740e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a49ab00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a6b344d5745784e69316d4e325a6c4c5455334f4751745954466c4d7930784e474d355a6a45344e7a55794e6a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a7323bacbfc8de0f335e303db4dfa273f3d584620000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb363b54479d2d5147d6a683f8711923de2c50a73bd8378fcba12dd0a8f2132ec",
      "signature": {
        "s": "0x3e1c96629e6902a5e727ca3f2c82b4e2300ef1f40e670b697e955b1977a23c59",
        "r": "0x2167b2409f68ad1326c166e4f90a62c91f5878de8e405c5a4486004998afff65",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5f3e926d8a44af2122113bb69a1587a0969fda51fb6b4e4d07296912d32c2f2d",
      "signature": {
        "s": "0x1cc27d00609df166955ab45f4cd255c707849a44f9f79b8e9eca1200d197d0a5",
        "r": "0x9da30fa81e3dd8e32c5f6a8852b24b1ad5928f9b8c3c3266182e274571382bf8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzk4MWExNi1mN2ZlLTU3OGQtYTFlMy0xNGM5ZjE4NzUyNjEifQ==",
    "nonce": 1980,
    "balances": {
      "current": "10000001409100906",
      "previous": "10000001409119246"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa7323bacbfc8de0f335e303db4dfa273f3d58462",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.199Z",
  "updated": "2020-05-22T08:13:33.266Z",
  "id": "5ec789adb0c6090011d5ab64"
}
```
* *stageAmount*: `18322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792b363b54479d2d5147d6a683f8711923de2c50a73bd8378fcba12dd0a8f2132ec2167b2409f68ad1326c166e4f90a62c91f5878de8e405c5a4486004998afff653e1c96629e6902a5e727ca3f2c82b4e2300ef1f40e670b697e955b1977a23c59000000000000000000000000000000000000000000000000000000000000001c5f3e926d8a44af2122113bb69a1587a0969fda51fb6b4e4d07296912d32c2f2d9da30fa81e3dd8e32c5f6a8852b24b1ad5928f9b8c3c3266182e274571382bf81cc27d00609df166955ab45f4cd255c707849a44f9f79b8e9eca1200d197d0a5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007bc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3be2c6a000000000000000000000000000000000000000000000000002386f2c3be740e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a49ab00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a6b344d5745784e69316d4e325a6c4c5455334f4751745954466c4d7930784e474d355a6a45344e7a55794e6a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a7323bacbfc8de0f335e303db4dfa273f3d584620000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb363b54479d2d5147d6a683f8711923de2c50a73bd8378fcba12dd0a8f2132ec",
      "signature": {
        "s": "0x3e1c96629e6902a5e727ca3f2c82b4e2300ef1f40e670b697e955b1977a23c59",
        "r": "0x2167b2409f68ad1326c166e4f90a62c91f5878de8e405c5a4486004998afff65",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5f3e926d8a44af2122113bb69a1587a0969fda51fb6b4e4d07296912d32c2f2d",
      "signature": {
        "s": "0x1cc27d00609df166955ab45f4cd255c707849a44f9f79b8e9eca1200d197d0a5",
        "r": "0x9da30fa81e3dd8e32c5f6a8852b24b1ad5928f9b8c3c3266182e274571382bf8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674219"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzk4MWExNi1mN2ZlLTU3OGQtYTFlMy0xNGM5ZjE4NzUyNjEifQ==",
    "nonce": 1980,
    "balances": {
      "current": "10000001409100906",
      "previous": "10000001409119246"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa7323bacbfc8de0f335e303db4dfa273f3d58462",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:33.199Z",
  "updated": "2020-05-22T08:13:33.266Z",
  "id": "5ec789adb0c6090011d5ab64"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18322`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``