# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB8A084475D5010C74070b5DbAE9686f5bf396502`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000000000000000000000000000000000004a7fb20b0e98b1ce5d3dd9cce1f7214cc363f0fc0e47cb8ebb1c71a5f0eb59ac68e61f6bf0f9041b607ae245f6bf5e001ee589bab9f743225ed34c68f57e8ab9ee8a6df807b467008f8a61f4460c7ba08deb66edded0762a83e57d323f9a8bf3feddaf6a000000000000000000000000000000000000000000000000000000000000001cf47239db7b98319ed8f2a39ef937a8f2f736a737709656587bc5cb9b56a95e88c87655122820d2bc3c6a07061005389979fc17b27515edc9dbde679f3def302f078b1a3de97c125a44cd92a366892d490ca5f24b1b1f960dbee1a6a370153cbd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a1000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e171cb8678f15000000000000000000000000000000000000000000000000002e171d02fa537a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000013125a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a57423a3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a466d4d4455775a693078596a6b774c5455355a5459745957526d5a4330784d444e684f444179597a45335957496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b8a084475d5010c74070b5dbae9686f5bf396502000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0e98b1ce5d3dd9cce1f7214cc363f0fc0e47cb8ebb1c71a5f0eb59ac68e61f6b",
      "signature": {
        "s": "0x07b467008f8a61f4460c7ba08deb66edded0762a83e57d323f9a8bf3feddaf6a",
        "r": "0xf0f9041b607ae245f6bf5e001ee589bab9f743225ed34c68f57e8ab9ee8a6df8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf47239db7b98319ed8f2a39ef937a8f2f736a737709656587bc5cb9b56a95e88",
      "signature": {
        "s": "0x078b1a3de97c125a44cd92a366892d490ca5f24b1b1f960dbee1a6a370153cbd",
        "r": "0xc87655122820d2bc3c6a07061005389979fc17b27515edc9dbde679f3def302f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1249882635",
    "total": "1249882635"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1249882635",
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
            "amount": "44413631034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1249882"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzFmMDUwZi0xYjkwLTU5ZTYtYWRmZC0xMDNhODAyYzE3YWIifQ==",
    "nonce": 6672,
    "balances": {
      "current": "12973261049007893",
      "previous": "12973262300140410"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8a084475d5010c74070b5dbae9686f5bf396502",
    "nonce": 20,
    "balances": {
      "current": "1249882635",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.484Z",
  "updated": "2020-05-22T08:50:54.576Z",
  "id": "5ec7926ee5756b00111b87f2"
}
```
* *stageAmount*: `1249882635`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000000000000000000000000000000000004a7fb20b0e98b1ce5d3dd9cce1f7214cc363f0fc0e47cb8ebb1c71a5f0eb59ac68e61f6bf0f9041b607ae245f6bf5e001ee589bab9f743225ed34c68f57e8ab9ee8a6df807b467008f8a61f4460c7ba08deb66edded0762a83e57d323f9a8bf3feddaf6a000000000000000000000000000000000000000000000000000000000000001cf47239db7b98319ed8f2a39ef937a8f2f736a737709656587bc5cb9b56a95e88c87655122820d2bc3c6a07061005389979fc17b27515edc9dbde679f3def302f078b1a3de97c125a44cd92a366892d490ca5f24b1b1f960dbee1a6a370153cbd000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a1000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e171cb8678f15000000000000000000000000000000000000000000000000002e171d02fa537a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000013125a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a57423a3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a466d4d4455775a693078596a6b774c5455355a5459745957526d5a4330784d444e684f444179597a45335957496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b8a084475d5010c74070b5dbae9686f5bf396502000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0e98b1ce5d3dd9cce1f7214cc363f0fc0e47cb8ebb1c71a5f0eb59ac68e61f6b",
      "signature": {
        "s": "0x07b467008f8a61f4460c7ba08deb66edded0762a83e57d323f9a8bf3feddaf6a",
        "r": "0xf0f9041b607ae245f6bf5e001ee589bab9f743225ed34c68f57e8ab9ee8a6df8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf47239db7b98319ed8f2a39ef937a8f2f736a737709656587bc5cb9b56a95e88",
      "signature": {
        "s": "0x078b1a3de97c125a44cd92a366892d490ca5f24b1b1f960dbee1a6a370153cbd",
        "r": "0xc87655122820d2bc3c6a07061005389979fc17b27515edc9dbde679f3def302f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1249882635",
    "total": "1249882635"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1249882635",
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
            "amount": "44413631034"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1249882"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzFmMDUwZi0xYjkwLTU5ZTYtYWRmZC0xMDNhODAyYzE3YWIifQ==",
    "nonce": 6672,
    "balances": {
      "current": "12973261049007893",
      "previous": "12973262300140410"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb8a084475d5010c74070b5dbae9686f5bf396502",
    "nonce": 20,
    "balances": {
      "current": "1249882635",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.484Z",
  "updated": "2020-05-22T08:50:54.576Z",
  "id": "5ec7926ee5756b00111b87f2"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004a7fb20b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1249882635`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`