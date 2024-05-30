# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcDdaAE986621874097ABaDB1B1Aef7aCa599D6f1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000000000000000000000000000000000000012c8e00884809e92ccbd2090dcad3e6a3a409165c846e25788f83a8eb56a4025db4394d164c57c1c1ace2a4727ab1f5404ec0d6f4b2c1f3b042c97910168c9cd81ccf155d339a99145115e11a277a3dcfe19248a270b3250b429a547ff934b35fda251000000000000000000000000000000000000000000000000000000000000001cb209454660fe220bcb62844e25654e277213b6d151e1099ea9af841d47a05387fad4a5de6445844cbd4396a612a75b943c9ab88d72a41cdb1ef945b984644e0513c92ab7f04033cab2deea0e8f56d1594b87e6007a27cf7ebf0d53db55fd53bc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180b4ff61368000000000000000000000000000000000000000000000000002e180b5008e11700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1a3d7bb3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a526a597a493259793077595755304c5455314f5455744f475a6d4d5331684e5745344e5751784d444179596a596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000cddaae986621874097abadb1b1aef7aca599d6f1000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0884809e92ccbd2090dcad3e6a3a409165c846e25788f83a8eb56a4025db4394",
      "signature": {
        "s": "0x55d339a99145115e11a277a3dcfe19248a270b3250b429a547ff934b35fda251",
        "r": "0xd164c57c1c1ace2a4727ab1f5404ec0d6f4b2c1f3b042c97910168c9cd81ccf1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb209454660fe220bcb62844e25654e277213b6d151e1099ea9af841d47a05387",
      "signature": {
        "s": "0x13c92ab7f04033cab2deea0e8f56d1594b87e6007a27cf7ebf0d53db55fd53bc",
        "r": "0xfad4a5de6445844cbd4396a612a75b943c9ab88d72a41cdb1ef945b984644e05",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1231072",
    "total": "1231072"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1231072",
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
            "amount": "43389909939"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1231"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjRjYzI2Yy0wYWU0LTU1OTUtOGZmMS1hNWE4NWQxMDAyYjYifQ==",
    "nonce": 6444,
    "balances": {
      "current": "12974285793923944",
      "previous": "12974285795156247"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcddaae986621874097abadb1b1aef7aca599d6f1",
    "nonce": 22,
    "balances": {
      "current": "1231072",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:13.728Z",
  "updated": "2020-05-22T08:49:13.790Z",
  "id": "5ec79209e5756b00111b87af"
}
```
* *stageAmount*: `1231072`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000000000000000000000000000000000000012c8e00884809e92ccbd2090dcad3e6a3a409165c846e25788f83a8eb56a4025db4394d164c57c1c1ace2a4727ab1f5404ec0d6f4b2c1f3b042c97910168c9cd81ccf155d339a99145115e11a277a3dcfe19248a270b3250b429a547ff934b35fda251000000000000000000000000000000000000000000000000000000000000001cb209454660fe220bcb62844e25654e277213b6d151e1099ea9af841d47a05387fad4a5de6445844cbd4396a612a75b943c9ab88d72a41cdb1ef945b984644e0513c92ab7f04033cab2deea0e8f56d1594b87e6007a27cf7ebf0d53db55fd53bc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000192c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e180b4ff61368000000000000000000000000000000000000000000000000002e180b5008e11700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1a3d7bb3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a526a597a493259793077595755304c5455314f5455744f475a6d4d5331684e5745344e5751784d444179596a596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000cddaae986621874097abadb1b1aef7aca599d6f1000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0884809e92ccbd2090dcad3e6a3a409165c846e25788f83a8eb56a4025db4394",
      "signature": {
        "s": "0x55d339a99145115e11a277a3dcfe19248a270b3250b429a547ff934b35fda251",
        "r": "0xd164c57c1c1ace2a4727ab1f5404ec0d6f4b2c1f3b042c97910168c9cd81ccf1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb209454660fe220bcb62844e25654e277213b6d151e1099ea9af841d47a05387",
      "signature": {
        "s": "0x13c92ab7f04033cab2deea0e8f56d1594b87e6007a27cf7ebf0d53db55fd53bc",
        "r": "0xfad4a5de6445844cbd4396a612a75b943c9ab88d72a41cdb1ef945b984644e05",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1231072",
    "total": "1231072"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1231072",
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
            "amount": "43389909939"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1231"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjRjYzI2Yy0wYWU0LTU1OTUtOGZmMS1hNWE4NWQxMDAyYjYifQ==",
    "nonce": 6444,
    "balances": {
      "current": "12974285793923944",
      "previous": "12974285795156247"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcddaae986621874097abadb1b1aef7aca599d6f1",
    "nonce": 22,
    "balances": {
      "current": "1231072",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:13.728Z",
  "updated": "2020-05-22T08:49:13.790Z",
  "id": "5ec79209e5756b00111b87af"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000012c8e0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1231072`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`