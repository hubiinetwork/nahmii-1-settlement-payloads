# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe73e84fc055C0207c767E30913bC4A54c32Ffe9B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000259400000000000000000000000000000000000000000000000000000000000025940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000259400000000000000000000000000000000000000000000000000000000000025946c359d48e62dce37249e9f9c8285b8f660284be3b7379a7b76510c06afaf9694702543d0d684777ebd2557b625e75de37a75a16cdd7ee813aaa30bc1a78a179338c3bd09c792a77c5b6af3d792305dd757ad1bcc454235154f60a9a589f5c8ec000000000000000000000000000000000000000000000000000000000000001b70ddfb9e6ffb6a8caebfc3c6abc31f2675eabd78cec592b30186b2ff018985c67d96312045f33d9b30d2ffd8e6e5633da7443477cce1d39c49fc52704187efbd2fe8326f25160a148086e2095bd5c7bfe6c65d93c45b24d8f5c0f5342d723432000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caecb54f000000000000000000000000000000000000000000000000002386f2caecdaec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000874f400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5455314d7a6334597930344d7a686c4c5455314f4463745954526c4e5330304e6d4d795a6d45305a47457a5a44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e73e84fc055c0207c767e30913bc4a54c32ffe9b0000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c359d48e62dce37249e9f9c8285b8f660284be3b7379a7b76510c06afaf9694",
      "signature": {
        "s": "0x38c3bd09c792a77c5b6af3d792305dd757ad1bcc454235154f60a9a589f5c8ec",
        "r": "0x702543d0d684777ebd2557b625e75de37a75a16cdd7ee813aaa30bc1a78a1793",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x70ddfb9e6ffb6a8caebfc3c6abc31f2675eabd78cec592b30186b2ff018985c6",
      "signature": {
        "s": "0x2fe8326f25160a148086e2095bd5c7bfe6c65d93c45b24d8f5c0f5342d723432",
        "r": "0x7d96312045f33d9b30d2ffd8e6e5633da7443477cce1d39c49fc52704187efbd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9620",
    "total": "9620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9620",
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
            "amount": "554228"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlOTU1Mzc4Yy04MzhlLTU1ODctYTRlNS00NmMyZmE0ZGEzZDQifQ==",
    "nonce": 746,
    "balances": {
      "current": "10000001529591119",
      "previous": "10000001529600748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe73e84fc055c0207c767e30913bc4a54c32ffe9b",
    "nonce": 20,
    "balances": {
      "current": "9620",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:29.283Z",
  "updated": "2020-05-22T08:04:29.354Z",
  "id": "5ec7878db0c6090011d5a9c7"
}
```
* *stageAmount*: `9620`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000025940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000259400000000000000000000000000000000000000000000000000000000000025946c359d48e62dce37249e9f9c8285b8f660284be3b7379a7b76510c06afaf9694702543d0d684777ebd2557b625e75de37a75a16cdd7ee813aaa30bc1a78a179338c3bd09c792a77c5b6af3d792305dd757ad1bcc454235154f60a9a589f5c8ec000000000000000000000000000000000000000000000000000000000000001b70ddfb9e6ffb6a8caebfc3c6abc31f2675eabd78cec592b30186b2ff018985c67d96312045f33d9b30d2ffd8e6e5633da7443477cce1d39c49fc52704187efbd2fe8326f25160a148086e2095bd5c7bfe6c65d93c45b24d8f5c0f5342d723432000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002ea00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caecb54f000000000000000000000000000000000000000000000000002386f2caecdaec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000874f400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4f5455314d7a6334597930344d7a686c4c5455314f4463745954526c4e5330304e6d4d795a6d45305a47457a5a44516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e73e84fc055c0207c767e30913bc4a54c32ffe9b0000000000000000000000000000000000000000000000000000000000002594000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c359d48e62dce37249e9f9c8285b8f660284be3b7379a7b76510c06afaf9694",
      "signature": {
        "s": "0x38c3bd09c792a77c5b6af3d792305dd757ad1bcc454235154f60a9a589f5c8ec",
        "r": "0x702543d0d684777ebd2557b625e75de37a75a16cdd7ee813aaa30bc1a78a1793",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x70ddfb9e6ffb6a8caebfc3c6abc31f2675eabd78cec592b30186b2ff018985c6",
      "signature": {
        "s": "0x2fe8326f25160a148086e2095bd5c7bfe6c65d93c45b24d8f5c0f5342d723432",
        "r": "0x7d96312045f33d9b30d2ffd8e6e5633da7443477cce1d39c49fc52704187efbd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9620",
    "total": "9620"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9620",
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
            "amount": "554228"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlOTU1Mzc4Yy04MzhlLTU1ODctYTRlNS00NmMyZmE0ZGEzZDQifQ==",
    "nonce": 746,
    "balances": {
      "current": "10000001529591119",
      "previous": "10000001529600748"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe73e84fc055c0207c767e30913bc4a54c32ffe9b",
    "nonce": 20,
    "balances": {
      "current": "9620",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:29.283Z",
  "updated": "2020-05-22T08:04:29.354Z",
  "id": "5ec7878db0c6090011d5a9c7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000025940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9620`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``