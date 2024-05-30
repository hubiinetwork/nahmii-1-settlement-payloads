# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6A665D472aE6cD38378c74420A5f4DBb1987bfFd`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c7676d0000000000000000000000000000000000000000000000000000000052c7676d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c7676d0000000000000000000000000000000000000000000000000000000052c7676d25c6498bd14183775492c32100c26f947265314ca9c1b4282f2f9ce5db9f83bfc17de4d3dca768726bc05ef761c63350e1fe39e0d228e7ac9f0e10823185a3e87e996f0b0ad1fb903e02fda90528c1d51fb242adbb42d58c061ffad1c9aecf5d000000000000000000000000000000000000000000000000000000000000001b1920c7f90bf35e3e5c615f4259a8ca019e06197c07eb32d5198d0640b9528c28ab908c9f415ed16907b9b489d9b91b4ee714b94e0695d2e56569a9c50e71b71a45d226711222dc9070002c2fb018f5d5fa7cfb0d6685de9d29e6ace1d5355bd2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2fe83ced1d000000000000000000000000000000000000000000000000002e1b303b19858900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094c783ca8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4746694e7a67344e7930775a444a6a4c5455795a5459745954517a4e79316d596a59314d574d355a5451304f44596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006a665d472ae6cd38378c74420a5f4dbb1987bffd0000000000000000000000000000000000000000000000000000000052c7676d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25c6498bd14183775492c32100c26f947265314ca9c1b4282f2f9ce5db9f83bf",
      "signature": {
        "s": "0x7e996f0b0ad1fb903e02fda90528c1d51fb242adbb42d58c061ffad1c9aecf5d",
        "r": "0xc17de4d3dca768726bc05ef761c63350e1fe39e0d228e7ac9f0e10823185a3e8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1920c7f90bf35e3e5c615f4259a8ca019e06197c07eb32d5198d0640b9528c28",
      "signature": {
        "s": "0x45d226711222dc9070002c2fb018f5d5fa7cfb0d6685de9d29e6ace1d5355bd2",
        "r": "0xab908c9f415ed16907b9b489d9b91b4ee714b94e0695d2e56569a9c50e71b71a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799853",
    "total": "1388799853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799853",
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
            "amount": "39937653928"
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
    "data": "eyJyZWYiOiI2ZGFiNzg4Ny0wZDJjLTUyZTYtYTQzNy1mYjY1MWM5ZTQ0ODYifQ==",
    "nonce": 5939,
    "balances": {
      "current": "12977741502410013",
      "previous": "12977742892598665"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a665d472ae6cd38378c74420a5f4dbb1987bffd",
    "nonce": 22,
    "balances": {
      "current": "1388799853",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:10.569Z",
  "updated": "2020-05-22T08:45:10.644Z",
  "id": "5ec79116005df800101bc9f9"
}
```
* *stageAmount*: `1388799853`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c7676d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c7676d0000000000000000000000000000000000000000000000000000000052c7676d25c6498bd14183775492c32100c26f947265314ca9c1b4282f2f9ce5db9f83bfc17de4d3dca768726bc05ef761c63350e1fe39e0d228e7ac9f0e10823185a3e87e996f0b0ad1fb903e02fda90528c1d51fb242adbb42d58c061ffad1c9aecf5d000000000000000000000000000000000000000000000000000000000000001b1920c7f90bf35e3e5c615f4259a8ca019e06197c07eb32d5198d0640b9528c28ab908c9f415ed16907b9b489d9b91b4ee714b94e0695d2e56569a9c50e71b71a45d226711222dc9070002c2fb018f5d5fa7cfb0d6685de9d29e6ace1d5355bd2000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2fe83ced1d000000000000000000000000000000000000000000000000002e1b303b19858900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094c783ca8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325a4746694e7a67344e7930775a444a6a4c5455795a5459745954517a4e79316d596a59314d574d355a5451304f44596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006a665d472ae6cd38378c74420a5f4dbb1987bffd0000000000000000000000000000000000000000000000000000000052c7676d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25c6498bd14183775492c32100c26f947265314ca9c1b4282f2f9ce5db9f83bf",
      "signature": {
        "s": "0x7e996f0b0ad1fb903e02fda90528c1d51fb242adbb42d58c061ffad1c9aecf5d",
        "r": "0xc17de4d3dca768726bc05ef761c63350e1fe39e0d228e7ac9f0e10823185a3e8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1920c7f90bf35e3e5c615f4259a8ca019e06197c07eb32d5198d0640b9528c28",
      "signature": {
        "s": "0x45d226711222dc9070002c2fb018f5d5fa7cfb0d6685de9d29e6ace1d5355bd2",
        "r": "0xab908c9f415ed16907b9b489d9b91b4ee714b94e0695d2e56569a9c50e71b71a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799853",
    "total": "1388799853"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799853",
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
            "amount": "39937653928"
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
    "data": "eyJyZWYiOiI2ZGFiNzg4Ny0wZDJjLTUyZTYtYTQzNy1mYjY1MWM5ZTQ0ODYifQ==",
    "nonce": 5939,
    "balances": {
      "current": "12977741502410013",
      "previous": "12977742892598665"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6a665d472ae6cd38378c74420a5f4dbb1987bffd",
    "nonce": 22,
    "balances": {
      "current": "1388799853",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:10.569Z",
  "updated": "2020-05-22T08:45:10.644Z",
  "id": "5ec79116005df800101bc9f9"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c7676d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388799853`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`