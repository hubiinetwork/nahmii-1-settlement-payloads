# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd3E66b41A214D52547Fe367b937D0D31fe82e05e`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000000000000000000000000000000000013b5749e3a05b3157d59f472a538aa26fe63e3824dd278eb8209c5748d035b09368b49251bb98decb3cc2f590b0400aba92ff6c2b7a86f03b153ddfe9ab6a0e2a42d91c5035aefe75b1ab63afa20c7d446e55194f904ffc3b4006fe74112db70d2937c187000000000000000000000000000000000000000000000000000000000000001c57d0d80efeff3c01f83c5608494338373a9d3ccb172ff8bca60a8abaf0d1fb0d30160a931444b9155a62af22b0b36ab2747aab994e6a55beb362c8de0e6ae030237ad71422fac094e99127baaf8adfb768b1acba7fe069bbc842c1c81589c5d4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56940000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e3c551b883000000000000000000000000000000000000000000000000002e17e500f9bc9500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000050ba2f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a245a4a5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d44686a593259784f5330774d475a684c5455324e324d74596a41314d69316d4e5455324e6a52694e7a5a6c4e32516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d3e66b41a214d52547fe367b937d0d31fe82e05e000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa05b3157d59f472a538aa26fe63e3824dd278eb8209c5748d035b09368b49251",
      "signature": {
        "s": "0x35aefe75b1ab63afa20c7d446e55194f904ffc3b4006fe74112db70d2937c187",
        "r": "0xbb98decb3cc2f590b0400aba92ff6c2b7a86f03b153ddfe9ab6a0e2a42d91c50",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57d0d80efeff3c01f83c5608494338373a9d3ccb172ff8bca60a8abaf0d1fb0d",
      "signature": {
        "s": "0x237ad71422fac094e99127baaf8adfb768b1acba7fe069bbc842c1c81589c5d4",
        "r": "0x30160a931444b9155a62af22b0b36ab2747aab994e6a55beb362c8de0e6ae030",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5290543587",
    "total": "5290543587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5290543587",
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
            "amount": "43559570011"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5290543"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDhjY2YxOS0wMGZhLTU2N2MtYjA1Mi1mNTU2NjRiNzZlN2QifQ==",
    "nonce": 6502,
    "balances": {
      "current": "12974115964172419",
      "previous": "12974121260006549"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3e66b41a214d52547fe367b937d0d31fe82e05e",
    "nonce": 22,
    "balances": {
      "current": "5290543587",
      "previous": "0"
    }
  },
  "blockNumber": "10114708",
  "created": "2020-05-22T08:49:37.025Z",
  "updated": "2020-05-22T08:49:38.112Z",
  "id": "5ec79221b0c6090011d5b144"
}
```
* *stageAmount*: `5290543587`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000000000000000000000000000000000013b5749e3a05b3157d59f472a538aa26fe63e3824dd278eb8209c5748d035b09368b49251bb98decb3cc2f590b0400aba92ff6c2b7a86f03b153ddfe9ab6a0e2a42d91c5035aefe75b1ab63afa20c7d446e55194f904ffc3b4006fe74112db70d2937c187000000000000000000000000000000000000000000000000000000000000001c57d0d80efeff3c01f83c5608494338373a9d3ccb172ff8bca60a8abaf0d1fb0d30160a931444b9155a62af22b0b36ab2747aab994e6a55beb362c8de0e6ae030237ad71422fac094e99127baaf8adfb768b1acba7fe069bbc842c1c81589c5d4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56940000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000196600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17e3c551b883000000000000000000000000000000000000000000000000002e17e500f9bc9500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000050ba2f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a245a4a5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d44686a593259784f5330774d475a684c5455324e324d74596a41314d69316d4e5455324e6a52694e7a5a6c4e32516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d3e66b41a214d52547fe367b937d0d31fe82e05e000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa05b3157d59f472a538aa26fe63e3824dd278eb8209c5748d035b09368b49251",
      "signature": {
        "s": "0x35aefe75b1ab63afa20c7d446e55194f904ffc3b4006fe74112db70d2937c187",
        "r": "0xbb98decb3cc2f590b0400aba92ff6c2b7a86f03b153ddfe9ab6a0e2a42d91c50",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x57d0d80efeff3c01f83c5608494338373a9d3ccb172ff8bca60a8abaf0d1fb0d",
      "signature": {
        "s": "0x237ad71422fac094e99127baaf8adfb768b1acba7fe069bbc842c1c81589c5d4",
        "r": "0x30160a931444b9155a62af22b0b36ab2747aab994e6a55beb362c8de0e6ae030",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5290543587",
    "total": "5290543587"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5290543587",
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
            "amount": "43559570011"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5290543"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMDhjY2YxOS0wMGZhLTU2N2MtYjA1Mi1mNTU2NjRiNzZlN2QifQ==",
    "nonce": 6502,
    "balances": {
      "current": "12974115964172419",
      "previous": "12974121260006549"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3e66b41a214d52547fe367b937d0d31fe82e05e",
    "nonce": 22,
    "balances": {
      "current": "5290543587",
      "previous": "0"
    }
  },
  "blockNumber": "10114708",
  "created": "2020-05-22T08:49:37.025Z",
  "updated": "2020-05-22T08:49:38.112Z",
  "id": "5ec79221b0c6090011d5b144"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000013b5749e3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5290543587`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`