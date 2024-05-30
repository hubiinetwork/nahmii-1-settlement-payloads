# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7764595c73fbCB19963D951708ff579e516f875a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000005410000000000000000000000000000000000000000000000000000000000000541000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005410000000000000000000000000000000000000000000000000000000000000541566f81a160c06e05e47b7aea086f21893944d4e31302b41ddadaa0be7790ad84d4a37be2147d1e71ed92da6e3d1894b76c0b879d4ba2255fd29a72d950b55f2731552a6c992ec1f90da4cd3d335b6b9ee33fb266528e600e34f1f108e29eb23b000000000000000000000000000000000000000000000000000000000000001ce71e79ee974aaa6751e704507c3b33093b9e6a05a7ba5a7d419d0f462baf2a698b9b7f09f3b83f46fc4ad600ba7bbd7097a029d9b01b4702591d2ebc4a9f1deb2b6e353ad233c0957b7c9e350a33ad4f2f0c5e5f14eb486ac6ebd3d70fa6ff6a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008f500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc574610000000000000000000000000000000000000000000000000002386f2bc574b5200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2df500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d4749784e5752685a533033596d5a6a4c5455794d5451744f4459774d4330794d6a4d784d6a517a4e44457a4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000007764595c73fbcb19963d951708ff579e516f875a0000000000000000000000000000000000000000000000000000000000000541000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x566f81a160c06e05e47b7aea086f21893944d4e31302b41ddadaa0be7790ad84",
      "signature": {
        "s": "0x31552a6c992ec1f90da4cd3d335b6b9ee33fb266528e600e34f1f108e29eb23b",
        "r": "0xd4a37be2147d1e71ed92da6e3d1894b76c0b879d4ba2255fd29a72d950b55f27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe71e79ee974aaa6751e704507c3b33093b9e6a05a7ba5a7d419d0f462baf2a69",
      "signature": {
        "s": "0x2b6e353ad233c0957b7c9e350a33ad4f2f0c5e5f14eb486ac6ebd3d70fa6ff6a",
        "r": "0x8b9b7f09f3b83f46fc4ad600ba7bbd7097a029d9b01b4702591d2ebc4a9f1deb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1345",
    "total": "1345"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1345",
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
            "amount": "798197"
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
    "data": "eyJyZWYiOiIzMGIxNWRhZS03YmZjLTUyMTQtODYwMC0yMjMxMjQzNDEzMDYifQ==",
    "nonce": 2293,
    "balances": {
      "current": "10000001284916752",
      "previous": "10000001284918098"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7764595c73fbcb19963d951708ff579e516f875a",
    "nonce": 4,
    "balances": {
      "current": "1345",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:35.273Z",
  "updated": "2020-05-22T08:15:35.343Z",
  "id": "5ec78a27b0c6090011d5abc9"
}
```
* *stageAmount*: `1345`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000541000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000005410000000000000000000000000000000000000000000000000000000000000541566f81a160c06e05e47b7aea086f21893944d4e31302b41ddadaa0be7790ad84d4a37be2147d1e71ed92da6e3d1894b76c0b879d4ba2255fd29a72d950b55f2731552a6c992ec1f90da4cd3d335b6b9ee33fb266528e600e34f1f108e29eb23b000000000000000000000000000000000000000000000000000000000000001ce71e79ee974aaa6751e704507c3b33093b9e6a05a7ba5a7d419d0f462baf2a698b9b7f09f3b83f46fc4ad600ba7bbd7097a029d9b01b4702591d2ebc4a9f1deb2b6e353ad233c0957b7c9e350a33ad4f2f0c5e5f14eb486ac6ebd3d70fa6ff6a000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008f500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc574610000000000000000000000000000000000000000000000000002386f2bc574b5200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2df500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d4749784e5752685a533033596d5a6a4c5455794d5451744f4459774d4330794d6a4d784d6a517a4e44457a4d44596966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000007764595c73fbcb19963d951708ff579e516f875a0000000000000000000000000000000000000000000000000000000000000541000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x566f81a160c06e05e47b7aea086f21893944d4e31302b41ddadaa0be7790ad84",
      "signature": {
        "s": "0x31552a6c992ec1f90da4cd3d335b6b9ee33fb266528e600e34f1f108e29eb23b",
        "r": "0xd4a37be2147d1e71ed92da6e3d1894b76c0b879d4ba2255fd29a72d950b55f27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe71e79ee974aaa6751e704507c3b33093b9e6a05a7ba5a7d419d0f462baf2a69",
      "signature": {
        "s": "0x2b6e353ad233c0957b7c9e350a33ad4f2f0c5e5f14eb486ac6ebd3d70fa6ff6a",
        "r": "0x8b9b7f09f3b83f46fc4ad600ba7bbd7097a029d9b01b4702591d2ebc4a9f1deb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1345",
    "total": "1345"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1345",
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
            "amount": "798197"
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
    "data": "eyJyZWYiOiIzMGIxNWRhZS03YmZjLTUyMTQtODYwMC0yMjMxMjQzNDEzMDYifQ==",
    "nonce": 2293,
    "balances": {
      "current": "10000001284916752",
      "previous": "10000001284918098"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7764595c73fbcb19963d951708ff579e516f875a",
    "nonce": 4,
    "balances": {
      "current": "1345",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:35.273Z",
  "updated": "2020-05-22T08:15:35.343Z",
  "id": "5ec78a27b0c6090011d5abc9"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000005410000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1345`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``