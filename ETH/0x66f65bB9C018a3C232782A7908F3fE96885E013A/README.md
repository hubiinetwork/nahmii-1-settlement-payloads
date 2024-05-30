# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x66f65bB9C018a3C232782A7908F3fE96885E013A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000784a52f5ba87ed07d354ffbaa5d60ae524b0c3b020d1458e0d9ea76529180f9cce24f3dedf3becf7872b7711c20f1a2cc47dfd3870d021628776e6783b313a7108138d15f1b0d949e9ba19a7bb1b5e4a7a8cde53c9520766b9c2bcf0c25e7d08242000000000000000000000000000000000000000000000000000000000000001c92ce886b759a2de3cf47ecc16c862e432c1a567021595bdb691eb09d0a0bff24fd238cde177d7ce5a41141da6b35e2d87bb15c75752da0944e5c4c4581a5793618ecc00973ee4f5028177379ecd6f5f598c4dcaaf36ca15f71a3df434a5f6c2a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003b000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caac3ab8000000000000000000000000000000000000000000000000002386f2caac423d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008852200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a51794d44457a4d5330785a4463794c5455344e475974595446694f4330314e57466c597a4d794e6d49324d54516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000066f65bb9c018a3c232782a7908f3fe96885e013a0000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa52f5ba87ed07d354ffbaa5d60ae524b0c3b020d1458e0d9ea76529180f9cce2",
      "signature": {
        "s": "0x38d15f1b0d949e9ba19a7bb1b5e4a7a8cde53c9520766b9c2bcf0c25e7d08242",
        "r": "0x4f3dedf3becf7872b7711c20f1a2cc47dfd3870d021628776e6783b313a71081",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x92ce886b759a2de3cf47ecc16c862e432c1a567021595bdb691eb09d0a0bff24",
      "signature": {
        "s": "0x18ecc00973ee4f5028177379ecd6f5f598c4dcaaf36ca15f71a3df434a5f6c2a",
        "r": "0xfd238cde177d7ce5a41141da6b35e2d87bb15c75752da0944e5c4c4581a57936",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1924",
    "total": "1924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1924",
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
            "amount": "558370"
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
    "data": "eyJyZWYiOiJmYjQyMDEzMS0xZDcyLTU4NGYtYTFiOC01NWFlYzMyNmI2MTQifQ==",
    "nonce": 944,
    "balances": {
      "current": "10000001525365432",
      "previous": "10000001525367357"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x66f65bb9c018a3c232782a7908f3fe96885e013a",
    "nonce": 20,
    "balances": {
      "current": "1924",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:40.640Z",
  "updated": "2020-05-22T08:05:40.712Z",
  "id": "5ec787d4e5756b00111b80a4"
}
```
* *stageAmount*: `1924`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000784a52f5ba87ed07d354ffbaa5d60ae524b0c3b020d1458e0d9ea76529180f9cce24f3dedf3becf7872b7711c20f1a2cc47dfd3870d021628776e6783b313a7108138d15f1b0d949e9ba19a7bb1b5e4a7a8cde53c9520766b9c2bcf0c25e7d08242000000000000000000000000000000000000000000000000000000000000001c92ce886b759a2de3cf47ecc16c862e432c1a567021595bdb691eb09d0a0bff24fd238cde177d7ce5a41141da6b35e2d87bb15c75752da0944e5c4c4581a5793618ecc00973ee4f5028177379ecd6f5f598c4dcaaf36ca15f71a3df434a5f6c2a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003b000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caac3ab8000000000000000000000000000000000000000000000000002386f2caac423d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008852200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a51794d44457a4d5330785a4463794c5455344e475974595446694f4330314e57466c597a4d794e6d49324d54516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000066f65bb9c018a3c232782a7908f3fe96885e013a0000000000000000000000000000000000000000000000000000000000000784000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa52f5ba87ed07d354ffbaa5d60ae524b0c3b020d1458e0d9ea76529180f9cce2",
      "signature": {
        "s": "0x38d15f1b0d949e9ba19a7bb1b5e4a7a8cde53c9520766b9c2bcf0c25e7d08242",
        "r": "0x4f3dedf3becf7872b7711c20f1a2cc47dfd3870d021628776e6783b313a71081",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x92ce886b759a2de3cf47ecc16c862e432c1a567021595bdb691eb09d0a0bff24",
      "signature": {
        "s": "0x18ecc00973ee4f5028177379ecd6f5f598c4dcaaf36ca15f71a3df434a5f6c2a",
        "r": "0xfd238cde177d7ce5a41141da6b35e2d87bb15c75752da0944e5c4c4581a57936",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1924",
    "total": "1924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1924",
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
            "amount": "558370"
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
    "data": "eyJyZWYiOiJmYjQyMDEzMS0xZDcyLTU4NGYtYTFiOC01NWFlYzMyNmI2MTQifQ==",
    "nonce": 944,
    "balances": {
      "current": "10000001525365432",
      "previous": "10000001525367357"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x66f65bb9c018a3c232782a7908f3fe96885e013a",
    "nonce": 20,
    "balances": {
      "current": "1924",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:40.640Z",
  "updated": "2020-05-22T08:05:40.712Z",
  "id": "5ec787d4e5756b00111b80a4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000007840000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1924`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``