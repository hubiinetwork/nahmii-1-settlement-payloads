# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x42F3FF62b8cE69C09093DA6e95FAe95157c6D407`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000f4d4000000000000000000000000000000000000000000000000000000000000f4d40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000f4d4000000000000000000000000000000000000000000000000000000000000f4d45d45f707da6d4d4dcc06accc2aa02f27f8c9630228bf497239ff23cd6ff94d7aeaebefe69b2a8433fb984a7e90f7c26067f1adab07a4645338396e7afd6565423af8d80029526455cab836a428fb7e25b6554b4dd726d45a8bacb4657bfe9534000000000000000000000000000000000000000000000000000000000000001c79f8959d14dafc5f557b80894c566e53714111dd314646d1b183c52afbbd4bbf0b8a1a6fc3e78912b77320928a5dc1af5294c193fe4ed4b368042d2a2e4861490a2665eb0c86818fa0bf7ceae22cb67c68ba704eb71797337cae7eef4021cfe6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005a200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6cb0165000000000000000000000000000000000000000000000000002386f2c6cbf67700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000982af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d55314f5441344e5330774d474e6b4c5455305a6d51744f444179597931685954646c4d474e684d545179597a596966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000042f3ff62b8ce69c09093da6e95fae95157c6d407000000000000000000000000000000000000000000000000000000000000f4d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d45f707da6d4d4dcc06accc2aa02f27f8c9630228bf497239ff23cd6ff94d7a",
      "signature": {
        "s": "0x3af8d80029526455cab836a428fb7e25b6554b4dd726d45a8bacb4657bfe9534",
        "r": "0xeaebefe69b2a8433fb984a7e90f7c26067f1adab07a4645338396e7afd656542",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x79f8959d14dafc5f557b80894c566e53714111dd314646d1b183c52afbbd4bbf",
      "signature": {
        "s": "0x0a2665eb0c86818fa0bf7ceae22cb67c68ba704eb71797337cae7eef4021cfe6",
        "r": "0x0b8a1a6fc3e78912b77320928a5dc1af5294c193fe4ed4b368042d2a2e486149",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62676",
    "total": "62676"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62676",
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
            "amount": "623279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "62"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMmU1OTA4NS0wMGNkLTU0ZmQtODAyYy1hYTdlMGNhMTQyYzYifQ==",
    "nonce": 1442,
    "balances": {
      "current": "10000001460273509",
      "previous": "10000001460336247"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42f3ff62b8ce69c09093da6e95fae95157c6d407",
    "nonce": 13,
    "balances": {
      "current": "62676",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:35.070Z",
  "updated": "2020-05-22T08:09:35.301Z",
  "id": "5ec788bfb0c6090011d5aaad"
}
```
* *stageAmount*: `62676`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000f4d40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000f4d4000000000000000000000000000000000000000000000000000000000000f4d45d45f707da6d4d4dcc06accc2aa02f27f8c9630228bf497239ff23cd6ff94d7aeaebefe69b2a8433fb984a7e90f7c26067f1adab07a4645338396e7afd6565423af8d80029526455cab836a428fb7e25b6554b4dd726d45a8bacb4657bfe9534000000000000000000000000000000000000000000000000000000000000001c79f8959d14dafc5f557b80894c566e53714111dd314646d1b183c52afbbd4bbf0b8a1a6fc3e78912b77320928a5dc1af5294c193fe4ed4b368042d2a2e4861490a2665eb0c86818fa0bf7ceae22cb67c68ba704eb71797337cae7eef4021cfe6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005a200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c6cb0165000000000000000000000000000000000000000000000000002386f2c6cbf67700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000982af00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6d55314f5441344e5330774d474e6b4c5455305a6d51744f444179597931685954646c4d474e684d545179597a596966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000042f3ff62b8ce69c09093da6e95fae95157c6d407000000000000000000000000000000000000000000000000000000000000f4d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d45f707da6d4d4dcc06accc2aa02f27f8c9630228bf497239ff23cd6ff94d7a",
      "signature": {
        "s": "0x3af8d80029526455cab836a428fb7e25b6554b4dd726d45a8bacb4657bfe9534",
        "r": "0xeaebefe69b2a8433fb984a7e90f7c26067f1adab07a4645338396e7afd656542",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x79f8959d14dafc5f557b80894c566e53714111dd314646d1b183c52afbbd4bbf",
      "signature": {
        "s": "0x0a2665eb0c86818fa0bf7ceae22cb67c68ba704eb71797337cae7eef4021cfe6",
        "r": "0x0b8a1a6fc3e78912b77320928a5dc1af5294c193fe4ed4b368042d2a2e486149",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62676",
    "total": "62676"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62676",
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
            "amount": "623279"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "62"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMmU1OTA4NS0wMGNkLTU0ZmQtODAyYy1hYTdlMGNhMTQyYzYifQ==",
    "nonce": 1442,
    "balances": {
      "current": "10000001460273509",
      "previous": "10000001460336247"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42f3ff62b8ce69c09093da6e95fae95157c6d407",
    "nonce": 13,
    "balances": {
      "current": "62676",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:35.070Z",
  "updated": "2020-05-22T08:09:35.301Z",
  "id": "5ec788bfb0c6090011d5aaad"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000f4d40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `62676`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``