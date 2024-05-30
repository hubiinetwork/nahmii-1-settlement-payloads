# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x68A3e60A90a742D4b0e81BAbcd634966AAc77bfb`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000000000000000000000000000000000021ddcbb74d7fb2f2ed7f59217373ae259661738562768079d06f491453f91fddbb3b9ff986f597cecc6d466c4e0b398c3134636703336c48d316c04f33575f6f7c4fe7af66909a5491eaee9b7a0da4e3c327bd12c015808ac4873b029158a39365c461465000000000000000000000000000000000000000000000000000000000000001c4b4bc077507cc6af40dc58c82e0c8777ed45c6761330495f298df0608ebb7c0f868921505e7c0e10325fda747b21348ec4c3b89a03478b39cd72d926c7a35b170e573bde66fd3ed0d46d243db832b22d4c527957ce4b0d7c91f079d7de31c645000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000166900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bc8d496489b000000000000000000000000000000000000000000000000002e1bcaf2fdbb8a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008ab77b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009255c45e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d4441335932517a5a53316a597a51794c5455314e5441744f5745344e69316a5a5759325a574535596a4e694e546b6966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000068a3e60a90a742d4b0e81babcd634966aac77bfb000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd7fb2f2ed7f59217373ae259661738562768079d06f491453f91fddbb3b9ff98",
      "signature": {
        "s": "0x6909a5491eaee9b7a0da4e3c327bd12c015808ac4873b029158a39365c461465",
        "r": "0x6f597cecc6d466c4e0b398c3134636703336c48d316c04f33575f6f7c4fe7af6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4b4bc077507cc6af40dc58c82e0c8777ed45c6761330495f298df0608ebb7c0f",
      "signature": {
        "s": "0x0e573bde66fd3ed0d46d243db832b22d4c527957ce4b0d7c91f079d7de31c645",
        "r": "0x868921505e7c0e10325fda747b21348ec4c3b89a03478b39cd72d926c7a35b17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9090939764",
    "total": "9090939764"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9090939764",
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
            "amount": "39281509863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9090939"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDA3Y2QzZS1jYzQyLTU1NTAtOWE4Ni1jZWY2ZWE5YjNiNTkifQ==",
    "nonce": 5737,
    "balances": {
      "current": "12978398302718107",
      "previous": "12978407402748810"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68a3e60a90a742d4b0e81babcd634966aac77bfb",
    "nonce": 11,
    "balances": {
      "current": "9090939764",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:26.175Z",
  "updated": "2020-05-22T08:43:26.247Z",
  "id": "5ec790aeb0c6090011d5b03e"
}
```
* *stageAmount*: `9090939764`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000000000000000000000000000000000021ddcbb74d7fb2f2ed7f59217373ae259661738562768079d06f491453f91fddbb3b9ff986f597cecc6d466c4e0b398c3134636703336c48d316c04f33575f6f7c4fe7af66909a5491eaee9b7a0da4e3c327bd12c015808ac4873b029158a39365c461465000000000000000000000000000000000000000000000000000000000000001c4b4bc077507cc6af40dc58c82e0c8777ed45c6761330495f298df0608ebb7c0f868921505e7c0e10325fda747b21348ec4c3b89a03478b39cd72d926c7a35b170e573bde66fd3ed0d46d243db832b22d4c527957ce4b0d7c91f079d7de31c645000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56730000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000166900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1bc8d496489b000000000000000000000000000000000000000000000000002e1bcaf2fdbb8a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008ab77b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009255c45e7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d4441335932517a5a53316a597a51794c5455314e5441744f5745344e69316a5a5759325a574535596a4e694e546b6966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000068a3e60a90a742d4b0e81babcd634966aac77bfb000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd7fb2f2ed7f59217373ae259661738562768079d06f491453f91fddbb3b9ff98",
      "signature": {
        "s": "0x6909a5491eaee9b7a0da4e3c327bd12c015808ac4873b029158a39365c461465",
        "r": "0x6f597cecc6d466c4e0b398c3134636703336c48d316c04f33575f6f7c4fe7af6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4b4bc077507cc6af40dc58c82e0c8777ed45c6761330495f298df0608ebb7c0f",
      "signature": {
        "s": "0x0e573bde66fd3ed0d46d243db832b22d4c527957ce4b0d7c91f079d7de31c645",
        "r": "0x868921505e7c0e10325fda747b21348ec4c3b89a03478b39cd72d926c7a35b17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9090939764",
    "total": "9090939764"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9090939764",
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
            "amount": "39281509863"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9090939"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDA3Y2QzZS1jYzQyLTU1NTAtOWE4Ni1jZWY2ZWE5YjNiNTkifQ==",
    "nonce": 5737,
    "balances": {
      "current": "12978398302718107",
      "previous": "12978407402748810"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x68a3e60a90a742d4b0e81babcd634966aac77bfb",
    "nonce": 11,
    "balances": {
      "current": "9090939764",
      "previous": "0"
    }
  },
  "blockNumber": "10114675",
  "created": "2020-05-22T08:43:26.175Z",
  "updated": "2020-05-22T08:43:26.247Z",
  "id": "5ec790aeb0c6090011d5b03e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000021ddcbb74000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9090939764`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`