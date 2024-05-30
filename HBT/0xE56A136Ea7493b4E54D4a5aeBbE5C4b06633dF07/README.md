# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE56A136Ea7493b4E54D4a5aeBbE5C4b06633dF07`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000000000000000000000000000000000004ed51b7b6f82cd0f5997d3bc1882d67187c564ef23b9886c6ea10d5976f025cd292a4d42ececfc02134d375dd370309b71305ee365078648aa6d63236d3a6437bd079abd3815576867e33b851e8ecbc218dcef954b51552ef6227ae322d83df2a8e6aa81000000000000000000000000000000000000000000000000000000000000001cd61836f2feca7b231a8ca69800ce49e79108aee8f046f0b0377d3c7144684453c1e7fa7795bda3e44fe071ac39cdc4d3645bab2c1b455d8800f0335daf4eee8d4f0c2b51bc8675816c5a4f6b321c21b38399e00404a8d1ad7400dec0dde0b771000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ae00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c8100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1353bc7bfdea000000000000000000000000000000000000000000000000002e13540b6547c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4f121f6f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a55774d6a52695953316d4e5745304c54566a4d475974596d526d4d4330794e47597a4d4751314e574e694d47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e56a136ea7493b4e54d4a5aebbe5c4b06633df07000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f82cd0f5997d3bc1882d67187c564ef23b9886c6ea10d5976f025cd292a4d42",
      "signature": {
        "s": "0x3815576867e33b851e8ecbc218dcef954b51552ef6227ae322d83df2a8e6aa81",
        "r": "0xececfc02134d375dd370309b71305ee365078648aa6d63236d3a6437bd079abd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd61836f2feca7b231a8ca69800ce49e79108aee8f046f0b0377d3c7144684453",
      "signature": {
        "s": "0x4f0c2b51bc8675816c5a4f6b321c21b38399e00404a8d1ad7400dec0dde0b771",
        "r": "0xc1e7fa7795bda3e44fe071ac39cdc4d3645bab2c1b455d8800f0335daf4eee8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322589051",
    "total": "1322589051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322589051",
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
            "amount": "48571228015"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322589"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMzUwMjRiYS1mNWE0LTVjMGYtYmRmMC0yNGYzMGQ1NWNiMGYifQ==",
    "nonce": 7297,
    "balances": {
      "current": "12969099294146026",
      "previous": "12969100618057666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe56a136ea7493b4e54d4a5aebbe5c4b06633df07",
    "nonce": 22,
    "balances": {
      "current": "1322589051",
      "previous": "0"
    }
  },
  "blockNumber": "10114734",
  "created": "2020-05-22T08:55:45.104Z",
  "updated": "2020-05-22T08:55:45.177Z",
  "id": "5ec79391b0c6090011d5b24e"
}
```
* *stageAmount*: `1322589051`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000000000000000000000000000000000004ed51b7b6f82cd0f5997d3bc1882d67187c564ef23b9886c6ea10d5976f025cd292a4d42ececfc02134d375dd370309b71305ee365078648aa6d63236d3a6437bd079abd3815576867e33b851e8ecbc218dcef954b51552ef6227ae322d83df2a8e6aa81000000000000000000000000000000000000000000000000000000000000001cd61836f2feca7b231a8ca69800ce49e79108aee8f046f0b0377d3c7144684453c1e7fa7795bda3e44fe071ac39cdc4d3645bab2c1b455d8800f0335daf4eee8d4f0c2b51bc8675816c5a4f6b321c21b38399e00404a8d1ad7400dec0dde0b771000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ae00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c8100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1353bc7bfdea000000000000000000000000000000000000000000000000002e13540b6547c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4f121f6f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a55774d6a52695953316d4e5745304c54566a4d475974596d526d4d4330794e47597a4d4751314e574e694d47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e56a136ea7493b4e54d4a5aebbe5c4b06633df07000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f82cd0f5997d3bc1882d67187c564ef23b9886c6ea10d5976f025cd292a4d42",
      "signature": {
        "s": "0x3815576867e33b851e8ecbc218dcef954b51552ef6227ae322d83df2a8e6aa81",
        "r": "0xececfc02134d375dd370309b71305ee365078648aa6d63236d3a6437bd079abd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd61836f2feca7b231a8ca69800ce49e79108aee8f046f0b0377d3c7144684453",
      "signature": {
        "s": "0x4f0c2b51bc8675816c5a4f6b321c21b38399e00404a8d1ad7400dec0dde0b771",
        "r": "0xc1e7fa7795bda3e44fe071ac39cdc4d3645bab2c1b455d8800f0335daf4eee8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322589051",
    "total": "1322589051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322589051",
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
            "amount": "48571228015"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322589"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMzUwMjRiYS1mNWE0LTVjMGYtYmRmMC0yNGYzMGQ1NWNiMGYifQ==",
    "nonce": 7297,
    "balances": {
      "current": "12969099294146026",
      "previous": "12969100618057666"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe56a136ea7493b4e54d4a5aebbe5c4b06633df07",
    "nonce": 22,
    "balances": {
      "current": "1322589051",
      "previous": "0"
    }
  },
  "blockNumber": "10114734",
  "created": "2020-05-22T08:55:45.104Z",
  "updated": "2020-05-22T08:55:45.177Z",
  "id": "5ec79391b0c6090011d5b24e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed51b7b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322589051`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`