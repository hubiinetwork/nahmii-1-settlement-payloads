# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x875739a60A7C9a90b6d48bE4322B6aB2577e4c22`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000406a000000000000000000000000000000000000000000000000000000000000406a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000406a000000000000000000000000000000000000000000000000000000000000406a97527962d40247ee700ce418279b3d909e76942c0d49e38ca407de7a9122d893c94c9d6ee709a540d1486fc1f5394a3316ac734645f30fb753777913f0ac5b600cba81c2509d8c5cdac5d60a9b7d18238f4a1ba3690436c6202cb239bf1ef9ac000000000000000000000000000000000000000000000000000000000000001b371da68d2d1d21c21df48022e8fd7728d9d4d2a2ba2179f3dafc34ab8e4d3cce33bbaf2c8d03be17f5dcb3ce731cd52a7b4ab46c5666300f1821f7c482e949e30c1cbc2c9e67441f3c55c97a0ecd527e53bf76ffebfaa19f5d86610e797ffab6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000068800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5d7066b000000000000000000000000000000000000000000000000002386f2c5d746e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c0d900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a466d4d3255794d5330314d54526d4c5455304d6d45744f446b775a6930794d4451354d7a63774d7a56695932596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000875739a60a7c9a90b6d48be4322b6ab2577e4c22000000000000000000000000000000000000000000000000000000000000406a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97527962d40247ee700ce418279b3d909e76942c0d49e38ca407de7a9122d893",
      "signature": {
        "s": "0x0cba81c2509d8c5cdac5d60a9b7d18238f4a1ba3690436c6202cb239bf1ef9ac",
        "r": "0xc94c9d6ee709a540d1486fc1f5394a3316ac734645f30fb753777913f0ac5b60",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x371da68d2d1d21c21df48022e8fd7728d9d4d2a2ba2179f3dafc34ab8e4d3cce",
      "signature": {
        "s": "0x0c1cbc2c9e67441f3c55c97a0ecd527e53bf76ffebfaa19f5d86610e797ffab6",
        "r": "0x33bbaf2c8d03be17f5dcb3ce731cd52a7b4ab46c5666300f1821f7c482e949e3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16490",
    "total": "16490"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16490",
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
            "amount": "639193"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YjFmM2UyMS01MTRmLTU0MmEtODkwZi0yMDQ5MzcwMzViY2YifQ==",
    "nonce": 1672,
    "balances": {
      "current": "10000001444284011",
      "previous": "10000001444300517"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x875739a60a7c9a90b6d48be4322b6ab2577e4c22",
    "nonce": 20,
    "balances": {
      "current": "16490",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:18.481Z",
  "updated": "2020-05-22T08:11:18.543Z",
  "id": "5ec78926005df800101bc456"
}
```
* *stageAmount*: `16490`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000406a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000406a000000000000000000000000000000000000000000000000000000000000406a97527962d40247ee700ce418279b3d909e76942c0d49e38ca407de7a9122d893c94c9d6ee709a540d1486fc1f5394a3316ac734645f30fb753777913f0ac5b600cba81c2509d8c5cdac5d60a9b7d18238f4a1ba3690436c6202cb239bf1ef9ac000000000000000000000000000000000000000000000000000000000000001b371da68d2d1d21c21df48022e8fd7728d9d4d2a2ba2179f3dafc34ab8e4d3cce33bbaf2c8d03be17f5dcb3ce731cd52a7b4ab46c5666300f1821f7c482e949e30c1cbc2c9e67441f3c55c97a0ecd527e53bf76ffebfaa19f5d86610e797ffab6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000068800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5d7066b000000000000000000000000000000000000000000000000002386f2c5d746e500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c0d900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a466d4d3255794d5330314d54526d4c5455304d6d45744f446b775a6930794d4451354d7a63774d7a56695932596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000875739a60a7c9a90b6d48be4322b6ab2577e4c22000000000000000000000000000000000000000000000000000000000000406a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97527962d40247ee700ce418279b3d909e76942c0d49e38ca407de7a9122d893",
      "signature": {
        "s": "0x0cba81c2509d8c5cdac5d60a9b7d18238f4a1ba3690436c6202cb239bf1ef9ac",
        "r": "0xc94c9d6ee709a540d1486fc1f5394a3316ac734645f30fb753777913f0ac5b60",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x371da68d2d1d21c21df48022e8fd7728d9d4d2a2ba2179f3dafc34ab8e4d3cce",
      "signature": {
        "s": "0x0c1cbc2c9e67441f3c55c97a0ecd527e53bf76ffebfaa19f5d86610e797ffab6",
        "r": "0x33bbaf2c8d03be17f5dcb3ce731cd52a7b4ab46c5666300f1821f7c482e949e3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16490",
    "total": "16490"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16490",
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
            "amount": "639193"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "16"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YjFmM2UyMS01MTRmLTU0MmEtODkwZi0yMDQ5MzcwMzViY2YifQ==",
    "nonce": 1672,
    "balances": {
      "current": "10000001444284011",
      "previous": "10000001444300517"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x875739a60a7c9a90b6d48be4322b6ab2577e4c22",
    "nonce": 20,
    "balances": {
      "current": "16490",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:18.481Z",
  "updated": "2020-05-22T08:11:18.543Z",
  "id": "5ec78926005df800101bc456"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000406a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `16490`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``