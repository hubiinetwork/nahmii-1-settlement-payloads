# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2E5461283325A0B8F114bd7e35d6Dc2114ABB8A9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000272497c6454cbda1b00000000000000000000000000000000000000000000000057f09ee6c9a772250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000057f09ee6c9a7722500000000000000000000000000000000000000000000000272497c6454cbda1b7c92e83a467b38fbb2e5b2a15ab5dfa0497d5f2dd27e0b163b15e90b4fe65b89f6fcae9837ff078caa8bf3632fa8ccb879b75e8cbc7e978c8926b4abe80d471c70d858c9df75c0189c102672b764b8b4c20a086ed9d8703ea2513b4960f8150d000000000000000000000000000000000000000000000000000000000000001bbaf99c8f1f4a2cc70a4af51e173d55ec1cb037e70d56f18d4776a815275242b7d34de1ef9f4222febf4819d61fd27a1edfe5f97f11693bdb44f6850174586bfd60e1f582af493f9c1e460661b0d7de596862fae8bf027c5032aa8e2981b37ea4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dbc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023807d05327df4f747b7000000000000000000000000000000000000000000002380d50c549fdafb4f3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000016833b1c5c955c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9680461f9ac5e38f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6d4d795a444e694e4331694e4445774c54566b4e7a6b744f474d78597930304e6a56684d44466c4d7a4e6d4d32556966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000002e5461283325a0b8f114bd7e35d6dc2114abb8a900000000000000000000000000000000000000000000000272497c6454cbda1b0000000000000000000000000000000000000000000000021a58dd7d8b2467f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c92e83a467b38fbb2e5b2a15ab5dfa0497d5f2dd27e0b163b15e90b4fe65b89",
      "signature": {
        "s": "0x70d858c9df75c0189c102672b764b8b4c20a086ed9d8703ea2513b4960f8150d",
        "r": "0xf6fcae9837ff078caa8bf3632fa8ccb879b75e8cbc7e978c8926b4abe80d471c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbaf99c8f1f4a2cc70a4af51e173d55ec1cb037e70d56f18d4776a815275242b7",
      "signature": {
        "s": "0x60e1f582af493f9c1e460661b0d7de596862fae8bf027c5032aa8e2981b37ea4",
        "r": "0xd34de1ef9f4222febf4819d61fd27a1edfe5f97f11693bdb44f6850174586bfd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6336739389773148709",
    "total": "45128738311403985435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6336739389773148709",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "16815828596153664267151"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6336739389773148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNmMyZDNiNC1iNDEwLTVkNzktOGMxYy00NjVhMDFlMzNmM2UifQ==",
    "nonce": 77244,
    "balances": {
      "current": "167653018804018591778743",
      "previous": "167659361880147754700600"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2e5461283325a0b8f114bd7e35d6dc2114abb8a9",
    "nonce": 2,
    "balances": {
      "current": "45128738311403985435",
      "previous": "38791998921630836726"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:15.760Z",
  "updated": "2021-06-04T12:46:15.944Z",
  "id": "60ba20970779920010014b99"
}
```
* *stageAmount*: `45128738311403985435`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000057f09ee6c9a772250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000057f09ee6c9a7722500000000000000000000000000000000000000000000000272497c6454cbda1b7c92e83a467b38fbb2e5b2a15ab5dfa0497d5f2dd27e0b163b15e90b4fe65b89f6fcae9837ff078caa8bf3632fa8ccb879b75e8cbc7e978c8926b4abe80d471c70d858c9df75c0189c102672b764b8b4c20a086ed9d8703ea2513b4960f8150d000000000000000000000000000000000000000000000000000000000000001bbaf99c8f1f4a2cc70a4af51e173d55ec1cb037e70d56f18d4776a815275242b7d34de1ef9f4222febf4819d61fd27a1edfe5f97f11693bdb44f6850174586bfd60e1f582af493f9c1e460661b0d7de596862fae8bf027c5032aa8e2981b37ea4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dbc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023807d05327df4f747b7000000000000000000000000000000000000000000002380d50c549fdafb4f3800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000016833b1c5c955c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9680461f9ac5e38f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6d4d795a444e694e4331694e4445774c54566b4e7a6b744f474d78597930304e6a56684d44466c4d7a4e6d4d32556966513d3d00000000000000000000000000000000000000000000000000000000000000020000000000000000000000002e5461283325a0b8f114bd7e35d6dc2114abb8a900000000000000000000000000000000000000000000000272497c6454cbda1b0000000000000000000000000000000000000000000000021a58dd7d8b2467f600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c92e83a467b38fbb2e5b2a15ab5dfa0497d5f2dd27e0b163b15e90b4fe65b89",
      "signature": {
        "s": "0x70d858c9df75c0189c102672b764b8b4c20a086ed9d8703ea2513b4960f8150d",
        "r": "0xf6fcae9837ff078caa8bf3632fa8ccb879b75e8cbc7e978c8926b4abe80d471c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbaf99c8f1f4a2cc70a4af51e173d55ec1cb037e70d56f18d4776a815275242b7",
      "signature": {
        "s": "0x60e1f582af493f9c1e460661b0d7de596862fae8bf027c5032aa8e2981b37ea4",
        "r": "0xd34de1ef9f4222febf4819d61fd27a1edfe5f97f11693bdb44f6850174586bfd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6336739389773148709",
    "total": "45128738311403985435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6336739389773148709",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "16815828596153664267151"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6336739389773148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNmMyZDNiNC1iNDEwLTVkNzktOGMxYy00NjVhMDFlMzNmM2UifQ==",
    "nonce": 77244,
    "balances": {
      "current": "167653018804018591778743",
      "previous": "167659361880147754700600"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2e5461283325a0b8f114bd7e35d6dc2114abb8a9",
    "nonce": 2,
    "balances": {
      "current": "45128738311403985435",
      "previous": "38791998921630836726"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:15.760Z",
  "updated": "2021-06-04T12:46:15.944Z",
  "id": "60ba20970779920010014b99"
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
0x0f200f9b00000000000000000000000000000000000000000000000272497c6454cbda1b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `45128738311403985435`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`