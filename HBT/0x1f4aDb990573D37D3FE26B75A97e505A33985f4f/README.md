# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1f4aDb990573D37D3FE26B75A97e505A33985f4f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f4f57c91b1a00f7d2b3fc2898c861f1c6ade7c1fbc8112417b10062cbe827ea1b0a7ebed8849f29a65df8953747c2b2d31b7ee2f2edd545a3ab0f05b342f7d629099ad54fba6ec21434c412416b09f0f26bc34c9ea682b9d8c1bff6c22dd8f073000000000000000000000000000000000000000000000000000000000000001bbdb80544b8599ceb42bb5002af13fc2d33ce0f43977384776c908e2b264451121ec717146c66b46dc10bf81f27b9dbcb3d95fc760a4a0b0b6116b2472a6d78ac5abb674e12af1bc5296e495bca5f332cf55feabd9c30bfd1cabda4cd16d40ece000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e19c55ea4a650000000000000000000000000000000000000000000000000002e19c55ea4a66000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009a92fc144000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f4755785954646d4e4330354e5745784c5456685a5449744f5752695a43307759544d7a4f4464684e7a63324d44676966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001f4adb990573d37d3fe26b75a97e505a33985f4f000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f57c91b1a00f7d2b3fc2898c861f1c6ade7c1fbc8112417b10062cbe827ea1b",
      "signature": {
        "s": "0x099ad54fba6ec21434c412416b09f0f26bc34c9ea682b9d8c1bff6c22dd8f073",
        "r": "0x0a7ebed8849f29a65df8953747c2b2d31b7ee2f2edd545a3ab0f05b342f7d629",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbdb80544b8599ceb42bb5002af13fc2d33ce0f43977384776c908e2b26445112",
      "signature": {
        "s": "0x5abb674e12af1bc5296e495bca5f332cf55feabd9c30bfd1cabda4cd16d40ece",
        "r": "0x1ec717146c66b46dc10bf81f27b9dbcb3d95fc760a4a0b0b6116b2472a6d78ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15",
    "total": "15"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15",
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
            "amount": "41493184836"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmOGUxYTdmNC05NWExLTVhZTItOWRiZC0wYTMzODdhNzc2MDgifQ==",
    "nonce": 6335,
    "balances": {
      "current": "12976184415790672",
      "previous": "12976184415790688"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f4adb990573d37d3fe26b75a97e505a33985f4f",
    "nonce": 21,
    "balances": {
      "current": "15",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:16.732Z",
  "updated": "2020-05-22T08:48:16.850Z",
  "id": "5ec791d0b0c6090011d5b105"
}
```
* *stageAmount*: `15`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000f4f57c91b1a00f7d2b3fc2898c861f1c6ade7c1fbc8112417b10062cbe827ea1b0a7ebed8849f29a65df8953747c2b2d31b7ee2f2edd545a3ab0f05b342f7d629099ad54fba6ec21434c412416b09f0f26bc34c9ea682b9d8c1bff6c22dd8f073000000000000000000000000000000000000000000000000000000000000001bbdb80544b8599ceb42bb5002af13fc2d33ce0f43977384776c908e2b264451121ec717146c66b46dc10bf81f27b9dbcb3d95fc760a4a0b0b6116b2472a6d78ac5abb674e12af1bc5296e495bca5f332cf55feabd9c30bfd1cabda4cd16d40ece000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e19c55ea4a650000000000000000000000000000000000000000000000000002e19c55ea4a66000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009a92fc144000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f4755785954646d4e4330354e5745784c5456685a5449744f5752695a43307759544d7a4f4464684e7a63324d44676966513d3d00000000000000000000000000000000000000000000000000000000000000150000000000000000000000001f4adb990573d37d3fe26b75a97e505a33985f4f000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f57c91b1a00f7d2b3fc2898c861f1c6ade7c1fbc8112417b10062cbe827ea1b",
      "signature": {
        "s": "0x099ad54fba6ec21434c412416b09f0f26bc34c9ea682b9d8c1bff6c22dd8f073",
        "r": "0x0a7ebed8849f29a65df8953747c2b2d31b7ee2f2edd545a3ab0f05b342f7d629",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbdb80544b8599ceb42bb5002af13fc2d33ce0f43977384776c908e2b26445112",
      "signature": {
        "s": "0x5abb674e12af1bc5296e495bca5f332cf55feabd9c30bfd1cabda4cd16d40ece",
        "r": "0x1ec717146c66b46dc10bf81f27b9dbcb3d95fc760a4a0b0b6116b2472a6d78ac",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15",
    "total": "15"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15",
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
            "amount": "41493184836"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmOGUxYTdmNC05NWExLTVhZTItOWRiZC0wYTMzODdhNzc2MDgifQ==",
    "nonce": 6335,
    "balances": {
      "current": "12976184415790672",
      "previous": "12976184415790688"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f4adb990573d37d3fe26b75a97e505a33985f4f",
    "nonce": 21,
    "balances": {
      "current": "15",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:16.732Z",
  "updated": "2020-05-22T08:48:16.850Z",
  "id": "5ec791d0b0c6090011d5b105"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`