# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8AC61Abb240FF496566e372AcDEdB7601A3da735`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000bd2e7d17fdca4374000000000000000000000000000000000000000000000000000000006448de8000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000006448de8000000000000000000000000000000000000000000000000000000009246fb0a64122fa40773093c68c01ed49a6e2fb7b73f47fe73b9812a4c2f386caca1324559b1e8ae671127a74f845cfe6a15ef05a43bb457f443e585e4ce29433f5097a760651c0acae68f9aef3de3aa63510d0f0a8f303314e4b5116cfb86d25fc077c271000000000000000000000000000000000000000000000000000000000000001b8bb94db2b889d3595aca7ebbb87d277f49c36283bcdecef3e3cfa596029900803ca403edc7f3218ccda8d29c07275e785aee90280212367a353d9a2992a3a60e4b881cac8d89ccba0d56c0b109fda4c19958e957a90fb74803c328ec96b8ee51000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b351000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d091a4d71b7c43cbe01000000000000000000000000000000000000000000003d091a4d71be0a656a1300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000019ac4120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc5f65390a3c02f5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f575133596a4a694e6930304e47526c4c54557859325574596a526a4f4331694d5759304d545535593259304f544d6966513d3d00000000000000000000000000000000000000000000000000000000000000210000000000000000000000008ac61abb240ff496566e372acdedb7601a3da73500000000000000000000000000000000000000000000000bd2e7d17fdca4374000000000000000000000000000000000000000000000000bd2e7d17998164f4000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x122fa40773093c68c01ed49a6e2fb7b73f47fe73b9812a4c2f386caca1324559",
      "signature": {
        "s": "0x651c0acae68f9aef3de3aa63510d0f0a8f303314e4b5116cfb86d25fc077c271",
        "r": "0xb1e8ae671127a74f845cfe6a15ef05a43bb457f443e585e4ce29433f5097a760",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8bb94db2b889d3595aca7ebbb87d277f49c36283bcdecef3e3cfa59602990080",
      "signature": {
        "s": "0x4b881cac8d89ccba0d56c0b109fda4c19958e957a90fb74803c328ec96b8ee51",
        "r": "0x3ca403edc7f3218ccda8d29c07275e785aee90280212367a353d9a2992a3a60e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26919954432",
    "total": "628256082532"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26919954432",
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
            "amount": "27684380791314757726043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26919954"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiOWQ3YjJiNi00NGRlLTUxY2UtYjRjOC1iMWY0MTU5Y2Y0OTMifQ==",
    "nonce": 111441,
    "balances": {
      "current": "288232271447764022115841",
      "previous": "288232271447790968990227"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8ac61abb240ff496566e372acdedb7601a3da735",
    "nonce": 33,
    "balances": {
      "current": "218111530625482897216",
      "previous": "218111530598562942784"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:19.466Z",
  "updated": "2022-05-04T08:58:19.546Z",
  "id": "6272402b3592fd001130b633"
}
```
* *stageAmount*: `218111530625482897216`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000006448de8000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000006448de8000000000000000000000000000000000000000000000000000000009246fb0a64122fa40773093c68c01ed49a6e2fb7b73f47fe73b9812a4c2f386caca1324559b1e8ae671127a74f845cfe6a15ef05a43bb457f443e585e4ce29433f5097a760651c0acae68f9aef3de3aa63510d0f0a8f303314e4b5116cfb86d25fc077c271000000000000000000000000000000000000000000000000000000000000001b8bb94db2b889d3595aca7ebbb87d277f49c36283bcdecef3e3cfa596029900803ca403edc7f3218ccda8d29c07275e785aee90280212367a353d9a2992a3a60e4b881cac8d89ccba0d56c0b109fda4c19958e957a90fb74803c328ec96b8ee51000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b351000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003d091a4d71b7c43cbe01000000000000000000000000000000000000000000003d091a4d71be0a656a1300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000019ac4120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dcc5f65390a3c02f5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694f575133596a4a694e6930304e47526c4c54557859325574596a526a4f4331694d5759304d545535593259304f544d6966513d3d00000000000000000000000000000000000000000000000000000000000000210000000000000000000000008ac61abb240ff496566e372acdedb7601a3da73500000000000000000000000000000000000000000000000bd2e7d17fdca4374000000000000000000000000000000000000000000000000bd2e7d17998164f4000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x122fa40773093c68c01ed49a6e2fb7b73f47fe73b9812a4c2f386caca1324559",
      "signature": {
        "s": "0x651c0acae68f9aef3de3aa63510d0f0a8f303314e4b5116cfb86d25fc077c271",
        "r": "0xb1e8ae671127a74f845cfe6a15ef05a43bb457f443e585e4ce29433f5097a760",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8bb94db2b889d3595aca7ebbb87d277f49c36283bcdecef3e3cfa59602990080",
      "signature": {
        "s": "0x4b881cac8d89ccba0d56c0b109fda4c19958e957a90fb74803c328ec96b8ee51",
        "r": "0x3ca403edc7f3218ccda8d29c07275e785aee90280212367a353d9a2992a3a60e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "26919954432",
    "total": "628256082532"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26919954432",
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
            "amount": "27684380791314757726043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26919954"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiOWQ3YjJiNi00NGRlLTUxY2UtYjRjOC1iMWY0MTU5Y2Y0OTMifQ==",
    "nonce": 111441,
    "balances": {
      "current": "288232271447764022115841",
      "previous": "288232271447790968990227"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8ac61abb240ff496566e372acdedb7601a3da735",
    "nonce": 33,
    "balances": {
      "current": "218111530625482897216",
      "previous": "218111530598562942784"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:19.466Z",
  "updated": "2022-05-04T08:58:19.546Z",
  "id": "6272402b3592fd001130b633"
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
0x0f200f9b00000000000000000000000000000000000000000000000bd2e7d17fdca437400000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `218111530625482897216`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`