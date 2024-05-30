# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x296997E7Edd9E4D8510b97386AcF5a278c927b05`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000005609a000000000000000000000000000000000000000000000000000000000005609a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000005609a000000000000000000000000000000000000000000000000000000000005609aa3c73f3c5286ac9848489c6261f8a75fecafa9b58fb504d3ddf99781b5818881a3ad2b86adb3fe50617778bc85616468cd2740f10ddc61b51ab24b8a4e6bdd843da45ba59777797f5adbd13c80c4f8553566a2cbcbfe73c6167100f09bc87500000000000000000000000000000000000000000000000000000000000000001bd57a6eb0d1bb52dac43d9a06f0aa30f84429d09e4883b506e7fef2a93c498eacdfa82317744951c8dbe03d2effb508af77961e832e911c8f9b0e8e6be0025a9d69c1db1c41e6235248ad312f5dc5a84956b1744e1c86eb4209699c378ab861e9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c816215f000000000000000000000000000000000000000000000000002386f2c81b835900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092e5d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a49324d6d4e694f53307a4e5445774c54566d595751744f474a6c4e693030596a4d30596a5135596a4a6859574d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000296997e7edd9e4d8510b97386acf5a278c927b05000000000000000000000000000000000000000000000000000000000005609a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa3c73f3c5286ac9848489c6261f8a75fecafa9b58fb504d3ddf99781b5818881",
      "signature": {
        "s": "0x3da45ba59777797f5adbd13c80c4f8553566a2cbcbfe73c6167100f09bc87500",
        "r": "0xa3ad2b86adb3fe50617778bc85616468cd2740f10ddc61b51ab24b8a4e6bdd84",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd57a6eb0d1bb52dac43d9a06f0aa30f84429d09e4883b506e7fef2a93c498eac",
      "signature": {
        "s": "0x69c1db1c41e6235248ad312f5dc5a84956b1744e1c86eb4209699c378ab861e9",
        "r": "0xdfa82317744951c8dbe03d2effb508af77961e832e911c8f9b0e8e6be0025a9d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "352410",
    "total": "352410"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "352410",
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
            "amount": "601693"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "352"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjI2MmNiOS0zNTEwLTVmYWQtOGJlNi00YjM0YjQ5YjJhYWMifQ==",
    "nonce": 1155,
    "balances": {
      "current": "10000001481974111",
      "previous": "10000001482326873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x296997e7edd9e4d8510b97386acf5a278c927b05",
    "nonce": 20,
    "balances": {
      "current": "352410",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:09.557Z",
  "updated": "2020-05-22T08:07:09.623Z",
  "id": "5ec7882d005df800101bc3a1"
}
```
* *stageAmount*: `352410`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000005609a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000005609a000000000000000000000000000000000000000000000000000000000005609aa3c73f3c5286ac9848489c6261f8a75fecafa9b58fb504d3ddf99781b5818881a3ad2b86adb3fe50617778bc85616468cd2740f10ddc61b51ab24b8a4e6bdd843da45ba59777797f5adbd13c80c4f8553566a2cbcbfe73c6167100f09bc87500000000000000000000000000000000000000000000000000000000000000001bd57a6eb0d1bb52dac43d9a06f0aa30f84429d09e4883b506e7fef2a93c498eacdfa82317744951c8dbe03d2effb508af77961e832e911c8f9b0e8e6be0025a9d69c1db1c41e6235248ad312f5dc5a84956b1744e1c86eb4209699c378ab861e9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000048300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c816215f000000000000000000000000000000000000000000000000002386f2c81b835900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000092e5d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e6a49324d6d4e694f53307a4e5445774c54566d595751744f474a6c4e693030596a4d30596a5135596a4a6859574d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000296997e7edd9e4d8510b97386acf5a278c927b05000000000000000000000000000000000000000000000000000000000005609a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa3c73f3c5286ac9848489c6261f8a75fecafa9b58fb504d3ddf99781b5818881",
      "signature": {
        "s": "0x3da45ba59777797f5adbd13c80c4f8553566a2cbcbfe73c6167100f09bc87500",
        "r": "0xa3ad2b86adb3fe50617778bc85616468cd2740f10ddc61b51ab24b8a4e6bdd84",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd57a6eb0d1bb52dac43d9a06f0aa30f84429d09e4883b506e7fef2a93c498eac",
      "signature": {
        "s": "0x69c1db1c41e6235248ad312f5dc5a84956b1744e1c86eb4209699c378ab861e9",
        "r": "0xdfa82317744951c8dbe03d2effb508af77961e832e911c8f9b0e8e6be0025a9d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "352410",
    "total": "352410"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "352410",
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
            "amount": "601693"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "352"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4NjI2MmNiOS0zNTEwLTVmYWQtOGJlNi00YjM0YjQ5YjJhYWMifQ==",
    "nonce": 1155,
    "balances": {
      "current": "10000001481974111",
      "previous": "10000001482326873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x296997e7edd9e4d8510b97386acf5a278c927b05",
    "nonce": 20,
    "balances": {
      "current": "352410",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:09.557Z",
  "updated": "2020-05-22T08:07:09.623Z",
  "id": "5ec7882d005df800101bc3a1"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000005609a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `352410`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``