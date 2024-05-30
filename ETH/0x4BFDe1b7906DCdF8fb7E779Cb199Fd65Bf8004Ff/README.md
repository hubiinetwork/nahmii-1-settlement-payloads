# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4BFDe1b7906DCdF8fb7E779Cb199Fd65Bf8004Ff`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004ac20000000000000000000000000000000000000000000000000000000000004ac200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004ac20000000000000000000000000000000000000000000000000000000000004ac2b1ffd0bf2ec995567ea5d86462507e0e41ae58c43f12c165b28e4b51fdbc2a59bf9859a4c701b79ffd882d5080f75efd9e57b9c7b2dc614a05e08a9ea23b9f2a264237c4d3ffb26df61c164393866873b39c958024164fcd16dde84b77472fb8000000000000000000000000000000000000000000000000000000000000001c3b9a4307e7365133ac170deeee62bb4135a7e2c532a3f786e0daef6757efe5da321e060a9e11eb7e98b86f5c13f6ba7456cec23d8aba87b33926d86ab22e6f2519e384f00a9b8881fbbf99338db1e292194b0aa3d4d2e9dc8b25435d4e17d2b6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ec00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5d27df000000000000000000000000000000000000000000000000002386f2bc5d72b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d4751794d575a6d4d6930304d7a49794c545530597a6774596a55334d6930314d446b334f474d32597a59314d57516966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000004bfde1b7906dcdf8fb7e779cb199fd65bf8004ff0000000000000000000000000000000000000000000000000000000000004ac2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb1ffd0bf2ec995567ea5d86462507e0e41ae58c43f12c165b28e4b51fdbc2a59",
      "signature": {
        "s": "0x264237c4d3ffb26df61c164393866873b39c958024164fcd16dde84b77472fb8",
        "r": "0xbf9859a4c701b79ffd882d5080f75efd9e57b9c7b2dc614a05e08a9ea23b9f2a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3b9a4307e7365133ac170deeee62bb4135a7e2c532a3f786e0daef6757efe5da",
      "signature": {
        "s": "0x19e384f00a9b8881fbbf99338db1e292194b0aa3d4d2e9dc8b25435d4e17d2b6",
        "r": "0x321e060a9e11eb7e98b86f5c13f6ba7456cec23d8aba87b33926d86ab22e6f25",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19138",
    "total": "19138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19138",
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
            "amount": "797814"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MGQyMWZmMi00MzIyLTU0YzgtYjU3Mi01MDk3OGM2YzY1MWQifQ==",
    "nonce": 2284,
    "balances": {
      "current": "10000001285302239",
      "previous": "10000001285321396"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4bfde1b7906dcdf8fb7e779cb199fd65bf8004ff",
    "nonce": 13,
    "balances": {
      "current": "19138",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:32.586Z",
  "updated": "2020-05-22T08:15:32.685Z",
  "id": "5ec78a24b0c6090011d5abc5"
}
```
* *stageAmount*: `19138`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004ac200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004ac20000000000000000000000000000000000000000000000000000000000004ac2b1ffd0bf2ec995567ea5d86462507e0e41ae58c43f12c165b28e4b51fdbc2a59bf9859a4c701b79ffd882d5080f75efd9e57b9c7b2dc614a05e08a9ea23b9f2a264237c4d3ffb26df61c164393866873b39c958024164fcd16dde84b77472fb8000000000000000000000000000000000000000000000000000000000000001c3b9a4307e7365133ac170deeee62bb4135a7e2c532a3f786e0daef6757efe5da321e060a9e11eb7e98b86f5c13f6ba7456cec23d8aba87b33926d86ab22e6f2519e384f00a9b8881fbbf99338db1e292194b0aa3d4d2e9dc8b25435d4e17d2b6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ec00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5d27df000000000000000000000000000000000000000000000000002386f2bc5d72b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000130000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c7600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d4751794d575a6d4d6930304d7a49794c545530597a6774596a55334d6930314d446b334f474d32597a59314d57516966513d3d000000000000000000000000000000000000000000000000000000000000000d0000000000000000000000004bfde1b7906dcdf8fb7e779cb199fd65bf8004ff0000000000000000000000000000000000000000000000000000000000004ac2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb1ffd0bf2ec995567ea5d86462507e0e41ae58c43f12c165b28e4b51fdbc2a59",
      "signature": {
        "s": "0x264237c4d3ffb26df61c164393866873b39c958024164fcd16dde84b77472fb8",
        "r": "0xbf9859a4c701b79ffd882d5080f75efd9e57b9c7b2dc614a05e08a9ea23b9f2a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3b9a4307e7365133ac170deeee62bb4135a7e2c532a3f786e0daef6757efe5da",
      "signature": {
        "s": "0x19e384f00a9b8881fbbf99338db1e292194b0aa3d4d2e9dc8b25435d4e17d2b6",
        "r": "0x321e060a9e11eb7e98b86f5c13f6ba7456cec23d8aba87b33926d86ab22e6f25",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19138",
    "total": "19138"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19138",
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
            "amount": "797814"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5MGQyMWZmMi00MzIyLTU0YzgtYjU3Mi01MDk3OGM2YzY1MWQifQ==",
    "nonce": 2284,
    "balances": {
      "current": "10000001285302239",
      "previous": "10000001285321396"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4bfde1b7906dcdf8fb7e779cb199fd65bf8004ff",
    "nonce": 13,
    "balances": {
      "current": "19138",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:32.586Z",
  "updated": "2020-05-22T08:15:32.685Z",
  "id": "5ec78a24b0c6090011d5abc5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004ac20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19138`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``