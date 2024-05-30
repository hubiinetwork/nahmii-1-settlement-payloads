# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDcCeb0ec4f2f9c0B8cc6a2a369c9529b6533AbC0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000163b000000000000000000000000000000000000000000000000000000000000163b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000163b000000000000000000000000000000000000000000000000000000000000163b3fbf373d62f38663f1f4c66cb66316f31911045b46382631fb44971720bdaf75c5ac98ef6df8cf5e08f9371c23d33c02fa2ba7913698f2762fc4ad223b5dcaf20b91f8f6a13a65efa08ca31e20484770e55a0f04ad29fc16fc1df5e63da7fb3f000000000000000000000000000000000000000000000000000000000000001bc9ae0b402fbc94aebe1e8b3ad71ce00e817ce352c3bb1481756722184b3503414db61d20442e43cd582847d79cce3012d42ff5eb7ad9ed8c80c10ad69a3dbb5f1bc23f01afb1895b07a71de907b69c6a3915d3ec49981cc73ffbd0cab607f0be000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000082600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c0ac71bb000000000000000000000000000000000000000000000000002386f2c0ac87fb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b126b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a4d784e7a51335a5331694e445a6a4c5455345a6a4d74596a6c6d59693168595749774e57566b4e6a6b314d7a456966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000dcceb0ec4f2f9c0b8cc6a2a369c9529b6533abc0000000000000000000000000000000000000000000000000000000000000163b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3fbf373d62f38663f1f4c66cb66316f31911045b46382631fb44971720bdaf75",
      "signature": {
        "s": "0x0b91f8f6a13a65efa08ca31e20484770e55a0f04ad29fc16fc1df5e63da7fb3f",
        "r": "0xc5ac98ef6df8cf5e08f9371c23d33c02fa2ba7913698f2762fc4ad223b5dcaf2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc9ae0b402fbc94aebe1e8b3ad71ce00e817ce352c3bb1481756722184b350341",
      "signature": {
        "s": "0x1bc23f01afb1895b07a71de907b69c6a3915d3ec49981cc73ffbd0cab607f0be",
        "r": "0x4db61d20442e43cd582847d79cce3012d42ff5eb7ad9ed8c80c10ad69a3dbb5f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5691",
    "total": "5691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5691",
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
            "amount": "725611"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MzMxNzQ3ZS1iNDZjLTU4ZjMtYjlmYi1hYWIwNWVkNjk1MzEifQ==",
    "nonce": 2086,
    "balances": {
      "current": "10000001357607355",
      "previous": "10000001357613051"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdcceb0ec4f2f9c0b8cc6a2a369c9529b6533abc0",
    "nonce": 15,
    "balances": {
      "current": "5691",
      "previous": "0"
    }
  },
  "blockNumber": "10114545",
  "created": "2020-05-22T08:14:20.708Z",
  "updated": "2020-05-22T08:14:20.777Z",
  "id": "5ec789dce5756b00111b821a"
}
```
* *stageAmount*: `5691`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000163b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000163b000000000000000000000000000000000000000000000000000000000000163b3fbf373d62f38663f1f4c66cb66316f31911045b46382631fb44971720bdaf75c5ac98ef6df8cf5e08f9371c23d33c02fa2ba7913698f2762fc4ad223b5dcaf20b91f8f6a13a65efa08ca31e20484770e55a0f04ad29fc16fc1df5e63da7fb3f000000000000000000000000000000000000000000000000000000000000001bc9ae0b402fbc94aebe1e8b3ad71ce00e817ce352c3bb1481756722184b3503414db61d20442e43cd582847d79cce3012d42ff5eb7ad9ed8c80c10ad69a3dbb5f1bc23f01afb1895b07a71de907b69c6a3915d3ec49981cc73ffbd0cab607f0be000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000082600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c0ac71bb000000000000000000000000000000000000000000000000002386f2c0ac87fb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b126b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d7a4d784e7a51335a5331694e445a6a4c5455345a6a4d74596a6c6d59693168595749774e57566b4e6a6b314d7a456966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000dcceb0ec4f2f9c0b8cc6a2a369c9529b6533abc0000000000000000000000000000000000000000000000000000000000000163b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3fbf373d62f38663f1f4c66cb66316f31911045b46382631fb44971720bdaf75",
      "signature": {
        "s": "0x0b91f8f6a13a65efa08ca31e20484770e55a0f04ad29fc16fc1df5e63da7fb3f",
        "r": "0xc5ac98ef6df8cf5e08f9371c23d33c02fa2ba7913698f2762fc4ad223b5dcaf2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc9ae0b402fbc94aebe1e8b3ad71ce00e817ce352c3bb1481756722184b350341",
      "signature": {
        "s": "0x1bc23f01afb1895b07a71de907b69c6a3915d3ec49981cc73ffbd0cab607f0be",
        "r": "0x4db61d20442e43cd582847d79cce3012d42ff5eb7ad9ed8c80c10ad69a3dbb5f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5691",
    "total": "5691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5691",
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
            "amount": "725611"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0MzMxNzQ3ZS1iNDZjLTU4ZjMtYjlmYi1hYWIwNWVkNjk1MzEifQ==",
    "nonce": 2086,
    "balances": {
      "current": "10000001357607355",
      "previous": "10000001357613051"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdcceb0ec4f2f9c0b8cc6a2a369c9529b6533abc0",
    "nonce": 15,
    "balances": {
      "current": "5691",
      "previous": "0"
    }
  },
  "blockNumber": "10114545",
  "created": "2020-05-22T08:14:20.708Z",
  "updated": "2020-05-22T08:14:20.777Z",
  "id": "5ec789dce5756b00111b821a"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000163b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5691`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``