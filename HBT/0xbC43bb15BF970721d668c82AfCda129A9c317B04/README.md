# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbC43bb15BF970721d668c82AfCda129A9c317B04`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000000000000000000000000000000000009daa4f5cf344ccd5548c659e9b8d32c3d95bce8dbd594ebdba23908685101b2d62221e7a12aecb4999057ed033f998fd63cd37a1bd8dd195af5bee5c7ef6831a718452bb56ad7b369f8d9a49621b2f05c2cec96af30ba2fce793c18b60302eff733c6d4b000000000000000000000000000000000000000000000000000000000000001c5ea778ec8d9d32de25a5c6195a15711282e522c98c4b15b5325f3476d62e559ed2ffd4b78f93b5ad1873f1aa1ae2a60fa4517e56d217759ad1cbfe189876fd8d13dc02edb8f17c45fbbaea030cc8d3c0a28bed9a13522dd079ac24d846053227000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c3000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139966e199ee000000000000000000000000000000000000000000000000002e139a04b4460a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285cc0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3d411432000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d5455344f57566d4d793169597a46684c5455794f4745744f444e6b4d5330345a4451324e6d4a6c4d5455304d6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000bc43bb15bf970721d668c82afcda129a9c317b04000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf344ccd5548c659e9b8d32c3d95bce8dbd594ebdba23908685101b2d62221e7a",
      "signature": {
        "s": "0x56ad7b369f8d9a49621b2f05c2cec96af30ba2fce793c18b60302eff733c6d4b",
        "r": "0x12aecb4999057ed033f998fd63cd37a1bd8dd195af5bee5c7ef6831a718452bb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5ea778ec8d9d32de25a5c6195a15711282e522c98c4b15b5325f3476d62e559e",
      "signature": {
        "s": "0x13dc02edb8f17c45fbbaea030cc8d3c0a28bed9a13522dd079ac24d846053227",
        "r": "0xd2ffd4b78f93b5ad1873f1aa1ae2a60fa4517e56d217759ad1cbfe189876fd8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2645184348",
    "total": "2645184348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645184348",
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
            "amount": "48272315442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645184"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTU4OWVmMy1iYzFhLTUyOGEtODNkMS04ZDQ2NmJlMTU0MjkifQ==",
    "nonce": 7216,
    "balances": {
      "current": "12969398505675246",
      "previous": "12969401153504778"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbc43bb15bf970721d668c82afcda129a9c317b04",
    "nonce": 22,
    "balances": {
      "current": "2645184348",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:05.808Z",
  "updated": "2020-05-22T08:55:06.876Z",
  "id": "5ec79369005df800101bcbab"
}
```
* *stageAmount*: `2645184348`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000000000000000000000000000000000009daa4f5cf344ccd5548c659e9b8d32c3d95bce8dbd594ebdba23908685101b2d62221e7a12aecb4999057ed033f998fd63cd37a1bd8dd195af5bee5c7ef6831a718452bb56ad7b369f8d9a49621b2f05c2cec96af30ba2fce793c18b60302eff733c6d4b000000000000000000000000000000000000000000000000000000000000001c5ea778ec8d9d32de25a5c6195a15711282e522c98c4b15b5325f3476d62e559ed2ffd4b78f93b5ad1873f1aa1ae2a60fa4517e56d217759ad1cbfe189876fd8d13dc02edb8f17c45fbbaea030cc8d3c0a28bed9a13522dd079ac24d846053227000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c3000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139966e199ee000000000000000000000000000000000000000000000000002e139a04b4460a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000285cc0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3d411432000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d5455344f57566d4d793169597a46684c5455794f4745744f444e6b4d5330345a4451324e6d4a6c4d5455304d6a6b6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000bc43bb15bf970721d668c82afcda129a9c317b04000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf344ccd5548c659e9b8d32c3d95bce8dbd594ebdba23908685101b2d62221e7a",
      "signature": {
        "s": "0x56ad7b369f8d9a49621b2f05c2cec96af30ba2fce793c18b60302eff733c6d4b",
        "r": "0x12aecb4999057ed033f998fd63cd37a1bd8dd195af5bee5c7ef6831a718452bb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5ea778ec8d9d32de25a5c6195a15711282e522c98c4b15b5325f3476d62e559e",
      "signature": {
        "s": "0x13dc02edb8f17c45fbbaea030cc8d3c0a28bed9a13522dd079ac24d846053227",
        "r": "0xd2ffd4b78f93b5ad1873f1aa1ae2a60fa4517e56d217759ad1cbfe189876fd8d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2645184348",
    "total": "2645184348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2645184348",
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
            "amount": "48272315442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2645184"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlMTU4OWVmMy1iYzFhLTUyOGEtODNkMS04ZDQ2NmJlMTU0MjkifQ==",
    "nonce": 7216,
    "balances": {
      "current": "12969398505675246",
      "previous": "12969401153504778"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbc43bb15bf970721d668c82afcda129a9c317b04",
    "nonce": 22,
    "balances": {
      "current": "2645184348",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:05.808Z",
  "updated": "2020-05-22T08:55:06.876Z",
  "id": "5ec79369005df800101bcbab"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000009daa4f5c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2645184348`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`