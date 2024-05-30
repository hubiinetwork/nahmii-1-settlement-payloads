# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8559D6fA6C3fdDc0E5eeDd0468Aa1E1A14eD0BF7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000005537ab0814a873000000000000000000000000000000000000000000000000000000000028fce10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000028fce10000000000000000000000000000000000000000000000000000000003bc92251e216555715e55c593505867b02a6b5fb9b674aff320201e40b9ae517f948d9c8c6af18c94b0d81aca1e5da1b5616e2163d1884999acb69ec5dcb37a2084b4046eee5ac30f5d3647a168a7686893a8e1a69cd3e437298c62cd086588757e0e2e000000000000000000000000000000000000000000000000000000000000001c03816ba70027747f6520a520becaf2eba73eb9a216f48e743fa56ad2f10a38d89ee4740b761fcb3b15c9cc4422f67dbe6d4fe71bee258263aa3139a84146cd5d6a517cfe74d2bbcc2eead8afacd3e161462d85627c81d5e00c30042aafe656d8000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af6e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000056fb2999ba39eabb9d840000000000000000000000000000000000000000000056fb2999ba39eae4a4e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000a7e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6234b28459399b4520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596d45344f5441344d5330354f5751784c5455325a4751744f44457a596930354d54646d4e4455314f4459344d54416966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000008559d6fa6c3fddc0e5eedd0468aa1e1a14ed0bf7000000000000000000000000000000000000000000000000005537ab0814a873000000000000000000000000000000000000000000000000005537ab07ebab9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1e216555715e55c593505867b02a6b5fb9b674aff320201e40b9ae517f948d9c",
      "signature": {
        "s": "0x6eee5ac30f5d3647a168a7686893a8e1a69cd3e437298c62cd086588757e0e2e",
        "r": "0x8c6af18c94b0d81aca1e5da1b5616e2163d1884999acb69ec5dcb37a2084b404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x03816ba70027747f6520a520becaf2eba73eb9a216f48e743fa56ad2f10a38d8",
      "signature": {
        "s": "0x6a517cfe74d2bbcc2eead8afacd3e161462d85627c81d5e00c30042aafe656d8",
        "r": "0x9ee4740b761fcb3b15c9cc4422f67dbe6d4fe71bee258263aa3139a84146cd5d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2686177",
    "total": "62689829"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2686177",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27561978816815945069650"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2686"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYmE4OTA4MS05OWQxLTU2ZGQtODEzYi05MTdmNDU1ODY4MTAifQ==",
    "nonce": 110446,
    "balances": {
      "current": "410756647921075491675524",
      "previous": "410756647921075494364387"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8559d6fa6c3fddc0e5eedd0468aa1e1a14ed0bf7",
    "nonce": 30,
    "balances": {
      "current": "23986580734912627",
      "previous": "23986580732226450"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:19.563Z",
  "updated": "2022-05-04T08:53:19.623Z",
  "id": "62723effbbd75600116d056c"
}
```
* *stageAmount*: `23986580734912627`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000028fce10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000028fce10000000000000000000000000000000000000000000000000000000003bc92251e216555715e55c593505867b02a6b5fb9b674aff320201e40b9ae517f948d9c8c6af18c94b0d81aca1e5da1b5616e2163d1884999acb69ec5dcb37a2084b4046eee5ac30f5d3647a168a7686893a8e1a69cd3e437298c62cd086588757e0e2e000000000000000000000000000000000000000000000000000000000000001c03816ba70027747f6520a520becaf2eba73eb9a216f48e743fa56ad2f10a38d89ee4740b761fcb3b15c9cc4422f67dbe6d4fe71bee258263aa3139a84146cd5d6a517cfe74d2bbcc2eead8afacd3e161462d85627c81d5e00c30042aafe656d8000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cf0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af6e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000056fb2999ba39eabb9d840000000000000000000000000000000000000000000056fb2999ba39eae4a4e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000a7e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d6234b28459399b4520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596d45344f5441344d5330354f5751784c5455325a4751744f44457a596930354d54646d4e4455314f4459344d54416966513d3d000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000008559d6fa6c3fddc0e5eedd0468aa1e1a14ed0bf7000000000000000000000000000000000000000000000000005537ab0814a873000000000000000000000000000000000000000000000000005537ab07ebab9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1e216555715e55c593505867b02a6b5fb9b674aff320201e40b9ae517f948d9c",
      "signature": {
        "s": "0x6eee5ac30f5d3647a168a7686893a8e1a69cd3e437298c62cd086588757e0e2e",
        "r": "0x8c6af18c94b0d81aca1e5da1b5616e2163d1884999acb69ec5dcb37a2084b404",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x03816ba70027747f6520a520becaf2eba73eb9a216f48e743fa56ad2f10a38d8",
      "signature": {
        "s": "0x6a517cfe74d2bbcc2eead8afacd3e161462d85627c81d5e00c30042aafe656d8",
        "r": "0x9ee4740b761fcb3b15c9cc4422f67dbe6d4fe71bee258263aa3139a84146cd5d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2686177",
    "total": "62689829"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2686177",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27561978816815945069650"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2686"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmYmE4OTA4MS05OWQxLTU2ZGQtODEzYi05MTdmNDU1ODY4MTAifQ==",
    "nonce": 110446,
    "balances": {
      "current": "410756647921075491675524",
      "previous": "410756647921075494364387"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8559d6fa6c3fddc0e5eedd0468aa1e1a14ed0bf7",
    "nonce": 30,
    "balances": {
      "current": "23986580734912627",
      "previous": "23986580732226450"
    }
  },
  "blockNumber": "14709967",
  "created": "2022-05-04T08:53:19.563Z",
  "updated": "2022-05-04T08:53:19.623Z",
  "id": "62723effbbd75600116d056c"
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
0x0f200f9b000000000000000000000000000000000000000000000000005537ab0814a8730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `23986580734912627`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`