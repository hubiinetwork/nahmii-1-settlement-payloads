# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x09B07a368990EE983a6dD174dF48220B63149a90`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001356045a6888dd3a97000000000000000000000000000000000000000000000000755bfb84852bcfaf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000755bfb84852bcfaf00000000000000000000000000000000000000000000000cdd375c3743d92b12255082c64b88ff0bdc0de80315899c4a4cbc472ef6e62d482a7e5035926ee77d5f15b22b5037dcba5332d2d3e77dab56d5887104dd0144bbadd1ae046be5d9cb7959826ca926dcfa575f50f2ec048a37cc831738c0f8465bda708b0f5cb34624000000000000000000000000000000000000000000000000000000000000001c38c4894731dc285e669fc51a020c0d61a7161e420c2d1ece2ff34e7830d706cf92dffd597d785999f461942dcff538638e5cb2dfba463a0f1c616614374725cd057d18919443fb615e73aea336b7114a5ab6da7b42f34586bfccf23e34163f16000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b039000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f8843f7929687ec36f0000000000000000000000000000000000000000000004f88b971995d7cd7d04c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001e0b426fbfc9ad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d80af8b6c2cc796e320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a54466a4d7a597a4e5330785a6a466d4c5455794d475974596a566a4f4330354d54526b4f54426c4f44566c4d6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000009b07a368990ee983a6dd174df48220b63149a9000000000000000000000000000000000000000000000001356045a6888dd3a97000000000000000000000000000000000000000000000012e0a85ee403b16ae800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x255082c64b88ff0bdc0de80315899c4a4cbc472ef6e62d482a7e5035926ee77d",
      "signature": {
        "s": "0x7959826ca926dcfa575f50f2ec048a37cc831738c0f8465bda708b0f5cb34624",
        "r": "0x5f15b22b5037dcba5332d2d3e77dab56d5887104dd0144bbadd1ae046be5d9cb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38c4894731dc285e669fc51a020c0d61a7161e420c2d1ece2ff34e7830d706cf",
      "signature": {
        "s": "0x057d18919443fb615e73aea336b7114a5ab6da7b42f34586bfccf23e34163f16",
        "r": "0x92dffd597d785999f461942dcff538638e5cb2dfba463a0f1c616614374725cd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8456629271906733999",
    "total": "237301239683047041810"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8456629271906733999",
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
            "amount": "27597119716951863160370"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8456629271906733"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZTFjMzYzNS0xZjFmLTUyMGYtYjVjOC05MTRkOTBlODVlMmYifQ==",
    "nonce": 110649,
    "balances": {
      "current": "375580606885021482759920",
      "previous": "375589071970922661400652"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09b07a368990ee983a6dd174df48220b63149a90",
    "nonce": 46,
    "balances": {
      "current": "356686315792669424279",
      "previous": "348229686520762690280"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:20.444Z",
  "updated": "2022-05-04T08:54:20.532Z",
  "id": "62723f3cbbd75600116d05b4"
}
```
* *stageAmount*: `356686315792669424279`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000755bfb84852bcfaf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000755bfb84852bcfaf00000000000000000000000000000000000000000000000cdd375c3743d92b12255082c64b88ff0bdc0de80315899c4a4cbc472ef6e62d482a7e5035926ee77d5f15b22b5037dcba5332d2d3e77dab56d5887104dd0144bbadd1ae046be5d9cb7959826ca926dcfa575f50f2ec048a37cc831738c0f8465bda708b0f5cb34624000000000000000000000000000000000000000000000000000000000000001c38c4894731dc285e669fc51a020c0d61a7161e420c2d1ece2ff34e7830d706cf92dffd597d785999f461942dcff538638e5cb2dfba463a0f1c616614374725cd057d18919443fb615e73aea336b7114a5ab6da7b42f34586bfccf23e34163f16000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b039000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f8843f7929687ec36f0000000000000000000000000000000000000000000004f88b971995d7cd7d04c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001e0b426fbfc9ad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d80af8b6c2cc796e320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a54466a4d7a597a4e5330785a6a466d4c5455794d475974596a566a4f4330354d54526b4f54426c4f44566c4d6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000009b07a368990ee983a6dd174df48220b63149a9000000000000000000000000000000000000000000000001356045a6888dd3a97000000000000000000000000000000000000000000000012e0a85ee403b16ae800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x255082c64b88ff0bdc0de80315899c4a4cbc472ef6e62d482a7e5035926ee77d",
      "signature": {
        "s": "0x7959826ca926dcfa575f50f2ec048a37cc831738c0f8465bda708b0f5cb34624",
        "r": "0x5f15b22b5037dcba5332d2d3e77dab56d5887104dd0144bbadd1ae046be5d9cb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x38c4894731dc285e669fc51a020c0d61a7161e420c2d1ece2ff34e7830d706cf",
      "signature": {
        "s": "0x057d18919443fb615e73aea336b7114a5ab6da7b42f34586bfccf23e34163f16",
        "r": "0x92dffd597d785999f461942dcff538638e5cb2dfba463a0f1c616614374725cd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8456629271906733999",
    "total": "237301239683047041810"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8456629271906733999",
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
            "amount": "27597119716951863160370"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8456629271906733"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZTFjMzYzNS0xZjFmLTUyMGYtYjVjOC05MTRkOTBlODVlMmYifQ==",
    "nonce": 110649,
    "balances": {
      "current": "375580606885021482759920",
      "previous": "375589071970922661400652"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09b07a368990ee983a6dd174df48220b63149a90",
    "nonce": 46,
    "balances": {
      "current": "356686315792669424279",
      "previous": "348229686520762690280"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:20.444Z",
  "updated": "2022-05-04T08:54:20.532Z",
  "id": "62723f3cbbd75600116d05b4"
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
0x0f200f9b00000000000000000000000000000000000000000000001356045a6888dd3a970000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `356686315792669424279`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`