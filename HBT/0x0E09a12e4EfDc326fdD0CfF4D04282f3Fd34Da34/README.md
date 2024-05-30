# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0E09a12e4EfDc326fdD0CfF4D04282f3Fd34Da34`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000004374e541b00000000000000000000000000000000000000000000000000000004374e541b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004374e541b00000000000000000000000000000000000000000000000000000004374e541b52a7e8609966c735e3e07771547e2155fc728b564c7421a4748d90c271db2fb570e5b3b52b1ab254b4128910c78fc23fcd17c3d1eed825d6168103465fd7704c25055b7275f375130409fa47a86ec13ec95f208a27d31494474f860b807823e1000000000000000000000000000000000000000000000000000000000000001ca4d2a73a9a7708b3814c93901b4a78abf488a8024760008a5a6a1ba5f016cde1137c56abf757beb30de0f6fca805189f0978ae9f4e97e59d399c1b274f1d5bae5ccc77ad5d4ca7c5738290a9bef492a40f95d9d20b2b5ed29ba08b107d2b8cec000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d2300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0dc4ab70b6f0000000000000000000000000000000000000000000000000002e0dc8e3d3587000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001144d65000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cbb030b46000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d595455784e6a566c4e433077597a59784c5455324f446b74595459784e6930784d4755354e7a413059546b35596a636966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000e09a12e4efdc326fdd0cff4d04282f3fd34da3400000000000000000000000000000000000000000000000000000004374e541b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52a7e8609966c735e3e07771547e2155fc728b564c7421a4748d90c271db2fb5",
      "signature": {
        "s": "0x25055b7275f375130409fa47a86ec13ec95f208a27d31494474f860b807823e1",
        "r": "0x70e5b3b52b1ab254b4128910c78fc23fcd17c3d1eed825d6168103465fd7704c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa4d2a73a9a7708b3814c93901b4a78abf488a8024760008a5a6a1ba5f016cde1",
      "signature": {
        "s": "0x5ccc77ad5d4ca7c5738290a9bef492a40f95d9d20b2b5ed29ba08b107d2b8cec",
        "r": "0x137c56abf757beb30de0f6fca805189f0978ae9f4e97e59d399c1b274f1d5bae",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18107749403",
    "total": "18107749403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18107749403",
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
            "amount": "54677146438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "18107749"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYTUxNjVlNC0wYzYxLTU2ODktYTYxNi0xMGU5NzA0YTk5YjcifQ==",
    "nonce": 7459,
    "balances": {
      "current": "12962987269732080",
      "previous": "12963005395589232"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e09a12e4efdc326fdd0cff4d04282f3fd34da34",
    "nonce": 11,
    "balances": {
      "current": "18107749403",
      "previous": "0"
    }
  },
  "blockNumber": "10114739",
  "created": "2020-05-22T08:57:00.033Z",
  "updated": "2020-05-22T08:57:00.109Z",
  "id": "5ec793dcb0c6090011d5b289"
}
```
* *stageAmount*: `18107749403`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000004374e541b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004374e541b00000000000000000000000000000000000000000000000000000004374e541b52a7e8609966c735e3e07771547e2155fc728b564c7421a4748d90c271db2fb570e5b3b52b1ab254b4128910c78fc23fcd17c3d1eed825d6168103465fd7704c25055b7275f375130409fa47a86ec13ec95f208a27d31494474f860b807823e1000000000000000000000000000000000000000000000000000000000000001ca4d2a73a9a7708b3814c93901b4a78abf488a8024760008a5a6a1ba5f016cde1137c56abf757beb30de0f6fca805189f0978ae9f4e97e59d399c1b274f1d5bae5ccc77ad5d4ca7c5738290a9bef492a40f95d9d20b2b5ed29ba08b107d2b8cec000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d2300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0dc4ab70b6f0000000000000000000000000000000000000000000000000002e0dc8e3d3587000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001144d65000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cbb030b46000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d595455784e6a566c4e433077597a59784c5455324f446b74595459784e6930784d4755354e7a413059546b35596a636966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000000e09a12e4efdc326fdd0cff4d04282f3fd34da3400000000000000000000000000000000000000000000000000000004374e541b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52a7e8609966c735e3e07771547e2155fc728b564c7421a4748d90c271db2fb5",
      "signature": {
        "s": "0x25055b7275f375130409fa47a86ec13ec95f208a27d31494474f860b807823e1",
        "r": "0x70e5b3b52b1ab254b4128910c78fc23fcd17c3d1eed825d6168103465fd7704c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa4d2a73a9a7708b3814c93901b4a78abf488a8024760008a5a6a1ba5f016cde1",
      "signature": {
        "s": "0x5ccc77ad5d4ca7c5738290a9bef492a40f95d9d20b2b5ed29ba08b107d2b8cec",
        "r": "0x137c56abf757beb30de0f6fca805189f0978ae9f4e97e59d399c1b274f1d5bae",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18107749403",
    "total": "18107749403"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18107749403",
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
            "amount": "54677146438"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "18107749"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYTUxNjVlNC0wYzYxLTU2ODktYTYxNi0xMGU5NzA0YTk5YjcifQ==",
    "nonce": 7459,
    "balances": {
      "current": "12962987269732080",
      "previous": "12963005395589232"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e09a12e4efdc326fdd0cff4d04282f3fd34da34",
    "nonce": 11,
    "balances": {
      "current": "18107749403",
      "previous": "0"
    }
  },
  "blockNumber": "10114739",
  "created": "2020-05-22T08:57:00.033Z",
  "updated": "2020-05-22T08:57:00.109Z",
  "id": "5ec793dcb0c6090011d5b289"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000004374e541b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18107749403`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`