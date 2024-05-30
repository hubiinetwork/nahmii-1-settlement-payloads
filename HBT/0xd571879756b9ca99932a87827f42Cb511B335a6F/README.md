# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd571879756b9ca99932a87827f42Cb511B335a6F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000000000000000000000000000000000000007d39991a0f75152f12ace5507e9aaad4f05597ecec0f01124ab0373416b7d6f57b5dbd2cf4682b1836edec82cc51a6d7a2ee06df7d6380a27736219c4c46d22f9ae8b3b18f99e173c1c8bc2191cc7ee88485bd18a3b838df008ea8312f6795af8cb76000000000000000000000000000000000000000000000000000000000000001b347f4f8bb218b21b92ad5861819ae24b2698d7ad766dbbaa6c4239f019bff83956a3df12308d699c25948811e6ab1d8cf1d51826a9dd4e2241685e1ec7f3a203143a7b1b2701901ddd2abf3ccda5f3008ea662b5a701c232ed9ecd0106d12b8f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d4800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b74bbaaa4f6000000000000000000000000000000000000000000000000002e0b74bbb27a8f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000200000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d52657288000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e7a67774e3251785a4330774f4455784c545530595455744f544a6a4f5330785a4752684f5468684d6a51304d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000d571879756b9ca99932a87827f42cb511b335a6f000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91a0f75152f12ace5507e9aaad4f05597ecec0f01124ab0373416b7d6f57b5db",
      "signature": {
        "s": "0x3b18f99e173c1c8bc2191cc7ee88485bd18a3b838df008ea8312f6795af8cb76",
        "r": "0xd2cf4682b1836edec82cc51a6d7a2ee06df7d6380a27736219c4c46d22f9ae8b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x347f4f8bb218b21b92ad5861819ae24b2698d7ad766dbbaa6c4239f019bff839",
      "signature": {
        "s": "0x143a7b1b2701901ddd2abf3ccda5f3008ea662b5a701c232ed9ecd0106d12b8f",
        "r": "0x56a3df12308d699c25948811e6ab1d8cf1d51826a9dd4e2241685e1ec7f3a203",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "512921",
    "total": "512921"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "512921",
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
            "amount": "57216955016"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "512"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNzgwN2QxZC0wODUxLTU0YTUtOTJjOS0xZGRhOThhMjQ0MmMifQ==",
    "nonce": 7496,
    "balances": {
      "current": "12960444921324790",
      "previous": "12960444921838223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd571879756b9ca99932a87827f42cb511b335a6f",
    "nonce": 6,
    "balances": {
      "current": "512921",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:14.235Z",
  "updated": "2020-05-22T08:57:14.306Z",
  "id": "5ec793eab0c6090011d5b298"
}
```
* *stageAmount*: `512921`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000000000000000000000000000000000000007d39991a0f75152f12ace5507e9aaad4f05597ecec0f01124ab0373416b7d6f57b5dbd2cf4682b1836edec82cc51a6d7a2ee06df7d6380a27736219c4c46d22f9ae8b3b18f99e173c1c8bc2191cc7ee88485bd18a3b838df008ea8312f6795af8cb76000000000000000000000000000000000000000000000000000000000000001b347f4f8bb218b21b92ad5861819ae24b2698d7ad766dbbaa6c4239f019bff83956a3df12308d699c25948811e6ab1d8cf1d51826a9dd4e2241685e1ec7f3a203143a7b1b2701901ddd2abf3ccda5f3008ea662b5a701c232ed9ecd0106d12b8f000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d4800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b74bbaaa4f6000000000000000000000000000000000000000000000000002e0b74bbb27a8f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000200000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d52657288000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e7a67774e3251785a4330774f4455784c545530595455744f544a6a4f5330785a4752684f5468684d6a51304d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000006000000000000000000000000d571879756b9ca99932a87827f42cb511b335a6f000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91a0f75152f12ace5507e9aaad4f05597ecec0f01124ab0373416b7d6f57b5db",
      "signature": {
        "s": "0x3b18f99e173c1c8bc2191cc7ee88485bd18a3b838df008ea8312f6795af8cb76",
        "r": "0xd2cf4682b1836edec82cc51a6d7a2ee06df7d6380a27736219c4c46d22f9ae8b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x347f4f8bb218b21b92ad5861819ae24b2698d7ad766dbbaa6c4239f019bff839",
      "signature": {
        "s": "0x143a7b1b2701901ddd2abf3ccda5f3008ea662b5a701c232ed9ecd0106d12b8f",
        "r": "0x56a3df12308d699c25948811e6ab1d8cf1d51826a9dd4e2241685e1ec7f3a203",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "512921",
    "total": "512921"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "512921",
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
            "amount": "57216955016"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "512"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNzgwN2QxZC0wODUxLTU0YTUtOTJjOS0xZGRhOThhMjQ0MmMifQ==",
    "nonce": 7496,
    "balances": {
      "current": "12960444921324790",
      "previous": "12960444921838223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd571879756b9ca99932a87827f42cb511b335a6f",
    "nonce": 6,
    "balances": {
      "current": "512921",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:14.235Z",
  "updated": "2020-05-22T08:57:14.306Z",
  "id": "5ec793eab0c6090011d5b298"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000007d399000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `512921`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`