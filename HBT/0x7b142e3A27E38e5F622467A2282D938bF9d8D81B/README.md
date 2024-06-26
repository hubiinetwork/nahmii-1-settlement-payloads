# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7b142e3A27E38e5F622467A2282D938bF9d8D81B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000211c843e00000000000000000000000000000000000000000000000000000000211c843e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000211c843e00000000000000000000000000000000000000000000000000000000211c843e7dc99690ccd7b6b962efa896bf59f7b6ca1065a776c82e22a5f5d8ebef761e2b5bf8b3ed2d96ff5c5ba4f2166085b66f99197b9f9e151391791acdfe353ea6f5624e8876ec9c8084e7bc1e379635584c3add87a17ad7b1bd9a22be14ed6b3920000000000000000000000000000000000000000000000000000000000000001c12019d508784074daf372e9e57b3f625ca8104312b18037c7928de3a5b8bc1f6f108ba73e764083df66816700d973d6ec6372bafe997d9774bf6a5fa127163691bd4bd2fcd64abda206beca95df79be05ca53f29f88cf2eb70ba66b24714dba1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b11c971094a000000000000000000000000000000000000000000000000002e1b11ea96078400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000879fc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009542c3a4e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596d553359545978597930774e444a684c5455355a545574596d526a5a693077597a67314d574534596a6b345a47516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007b142e3a27e38e5f622467a2282d938bf9d8d81b00000000000000000000000000000000000000000000000000000000211c843e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7dc99690ccd7b6b962efa896bf59f7b6ca1065a776c82e22a5f5d8ebef761e2b",
      "signature": {
        "s": "0x624e8876ec9c8084e7bc1e379635584c3add87a17ad7b1bd9a22be14ed6b3920",
        "r": "0x5bf8b3ed2d96ff5c5ba4f2166085b66f99197b9f9e151391791acdfe353ea6f5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x12019d508784074daf372e9e57b3f625ca8104312b18037c7928de3a5b8bc1f6",
      "signature": {
        "s": "0x1bd4bd2fcd64abda206beca95df79be05ca53f29f88cf2eb70ba66b24714dba1",
        "r": "0xf108ba73e764083df66816700d973d6ec6372bafe997d9774bf6a5fa12716369",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "555516990",
    "total": "555516990"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "555516990",
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
            "amount": "40066890318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "555516"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYmU3YTYxYy0wNDJhLTU5ZTUtYmRjZi0wYzg1MWE4Yjk4ZGQifQ==",
    "nonce": 6082,
    "balances": {
      "current": "12977612136712522",
      "previous": "12977612692785028"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b142e3a27e38e5f622467a2282d938bf9d8d81b",
    "nonce": 22,
    "balances": {
      "current": "555516990",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:17.381Z",
  "updated": "2020-05-22T08:46:17.448Z",
  "id": "5ec79159e5756b00111b873a"
}
```
* *stageAmount*: `555516990`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000211c843e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000211c843e00000000000000000000000000000000000000000000000000000000211c843e7dc99690ccd7b6b962efa896bf59f7b6ca1065a776c82e22a5f5d8ebef761e2b5bf8b3ed2d96ff5c5ba4f2166085b66f99197b9f9e151391791acdfe353ea6f5624e8876ec9c8084e7bc1e379635584c3add87a17ad7b1bd9a22be14ed6b3920000000000000000000000000000000000000000000000000000000000000001c12019d508784074daf372e9e57b3f625ca8104312b18037c7928de3a5b8bc1f6f108ba73e764083df66816700d973d6ec6372bafe997d9774bf6a5fa127163691bd4bd2fcd64abda206beca95df79be05ca53f29f88cf2eb70ba66b24714dba1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017c200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b11c971094a000000000000000000000000000000000000000000000000002e1b11ea96078400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000879fc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009542c3a4e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596d553359545978597930774e444a684c5455355a545574596d526a5a693077597a67314d574534596a6b345a47516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000007b142e3a27e38e5f622467a2282d938bf9d8d81b00000000000000000000000000000000000000000000000000000000211c843e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7dc99690ccd7b6b962efa896bf59f7b6ca1065a776c82e22a5f5d8ebef761e2b",
      "signature": {
        "s": "0x624e8876ec9c8084e7bc1e379635584c3add87a17ad7b1bd9a22be14ed6b3920",
        "r": "0x5bf8b3ed2d96ff5c5ba4f2166085b66f99197b9f9e151391791acdfe353ea6f5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x12019d508784074daf372e9e57b3f625ca8104312b18037c7928de3a5b8bc1f6",
      "signature": {
        "s": "0x1bd4bd2fcd64abda206beca95df79be05ca53f29f88cf2eb70ba66b24714dba1",
        "r": "0xf108ba73e764083df66816700d973d6ec6372bafe997d9774bf6a5fa12716369",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "555516990",
    "total": "555516990"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "555516990",
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
            "amount": "40066890318"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "555516"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYmU3YTYxYy0wNDJhLTU5ZTUtYmRjZi0wYzg1MWE4Yjk4ZGQifQ==",
    "nonce": 6082,
    "balances": {
      "current": "12977612136712522",
      "previous": "12977612692785028"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7b142e3a27e38e5f622467a2282d938bf9d8d81b",
    "nonce": 22,
    "balances": {
      "current": "555516990",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:17.381Z",
  "updated": "2020-05-22T08:46:17.448Z",
  "id": "5ec79159e5756b00111b873a"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000211c843e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `555516990`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`
