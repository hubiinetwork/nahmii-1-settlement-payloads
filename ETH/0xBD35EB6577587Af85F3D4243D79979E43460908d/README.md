# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBD35EB6577587Af85F3D4243D79979E43460908d`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000248ca08ad7704a4cde50439a8bbc45682102f6610b76d3a683c817c8888ce07d675a8c17082886924169e1b5107a3c9c18e99402ecfc71a3391b95774edabe6feb10821cf4a25f4cf21e0aff16997dedd1d282719f84433de7198db384d2f1ed51000000000000000000000000000000000000000000000000000000000000001b51846ee35ff43e4ee34db7df336a9510214663bd4cd80620221f348c5173133792de38d06513a04df82d97cc599e84fed5d96bb53ad5e6b4fe8d80bfa628f01e74d197012b7f6cf82e7d72894569ed76803638deeabcce38a1b8c6c36db9d11b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000093300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc50fe44000000000000000000000000000000000000000000000000002386f2bc50fe6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a5463315a5751785a5330785a4455344c5455795a544174595751315a43316d5a6a41344d6a52694e4755774e574d6966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000bd35eb6577587af85f3d4243d79979e43460908d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8ca08ad7704a4cde50439a8bbc45682102f6610b76d3a683c817c8888ce07d67",
      "signature": {
        "s": "0x10821cf4a25f4cf21e0aff16997dedd1d282719f84433de7198db384d2f1ed51",
        "r": "0x5a8c17082886924169e1b5107a3c9c18e99402ecfc71a3391b95774edabe6feb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x51846ee35ff43e4ee34db7df336a9510214663bd4cd80620221f348c51731337",
      "signature": {
        "s": "0x74d197012b7f6cf82e7d72894569ed76803638deeabcce38a1b8c6c36db9d11b",
        "r": "0x92de38d06513a04df82d97cc599e84fed5d96bb53ad5e6b4fe8d80bfa628f01e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "36",
    "total": "36"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36",
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
            "amount": "798620"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZTc1ZWQxZS0xZDU4LTUyZTAtYWQ1ZC1mZjA4MjRiNGUwNWMifQ==",
    "nonce": 2355,
    "balances": {
      "current": "10000001284505156",
      "previous": "10000001284505193"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd35eb6577587af85f3d4243d79979e43460908d",
    "nonce": 3,
    "balances": {
      "current": "36",
      "previous": "0"
    }
  },
  "blockNumber": "10114553",
  "created": "2020-05-22T08:15:58.433Z",
  "updated": "2020-05-22T08:15:58.507Z",
  "id": "5ec78a3e005df800101bc539"
}
```
* *stageAmount*: `36`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000248ca08ad7704a4cde50439a8bbc45682102f6610b76d3a683c817c8888ce07d675a8c17082886924169e1b5107a3c9c18e99402ecfc71a3391b95774edabe6feb10821cf4a25f4cf21e0aff16997dedd1d282719f84433de7198db384d2f1ed51000000000000000000000000000000000000000000000000000000000000001b51846ee35ff43e4ee34db7df336a9510214663bd4cd80620221f348c5173133792de38d06513a04df82d97cc599e84fed5d96bb53ad5e6b4fe8d80bfa628f01e74d197012b7f6cf82e7d72894569ed76803638deeabcce38a1b8c6c36db9d11b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000093300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc50fe44000000000000000000000000000000000000000000000000002386f2bc50fe6900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f9c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a5463315a5751785a5330785a4455344c5455795a544174595751315a43316d5a6a41344d6a52694e4755774e574d6966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000bd35eb6577587af85f3d4243d79979e43460908d0000000000000000000000000000000000000000000000000000000000000024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8ca08ad7704a4cde50439a8bbc45682102f6610b76d3a683c817c8888ce07d67",
      "signature": {
        "s": "0x10821cf4a25f4cf21e0aff16997dedd1d282719f84433de7198db384d2f1ed51",
        "r": "0x5a8c17082886924169e1b5107a3c9c18e99402ecfc71a3391b95774edabe6feb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x51846ee35ff43e4ee34db7df336a9510214663bd4cd80620221f348c51731337",
      "signature": {
        "s": "0x74d197012b7f6cf82e7d72894569ed76803638deeabcce38a1b8c6c36db9d11b",
        "r": "0x92de38d06513a04df82d97cc599e84fed5d96bb53ad5e6b4fe8d80bfa628f01e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "36",
    "total": "36"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36",
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
            "amount": "798620"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZTc1ZWQxZS0xZDU4LTUyZTAtYWQ1ZC1mZjA4MjRiNGUwNWMifQ==",
    "nonce": 2355,
    "balances": {
      "current": "10000001284505156",
      "previous": "10000001284505193"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd35eb6577587af85f3d4243d79979e43460908d",
    "nonce": 3,
    "balances": {
      "current": "36",
      "previous": "0"
    }
  },
  "blockNumber": "10114553",
  "created": "2020-05-22T08:15:58.433Z",
  "updated": "2020-05-22T08:15:58.507Z",
  "id": "5ec78a3e005df800101bc539"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``