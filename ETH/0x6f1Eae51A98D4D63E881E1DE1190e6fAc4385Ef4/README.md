# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6f1Eae51A98D4D63E881E1DE1190e6fAc4385Ef4`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000002740990000000000000000000000000000000000000000000000000000000000274099000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002740990000000000000000000000000000000000000000000000000000000000274099c96106531ae87ce3cb1a7f23a013a5832afa64c7d4fe2be189077aa80c681889eeba2b3bdea07f896882ceb400583e8b3ef8ad4ca5ac4bf82af0f8639880eea177c7e9972238589edf2c4c2271d88aa82e445373d1739794fdfcfb6b1dbd5c44000000000000000000000000000000000000000000000000000000000000001bbc9a25d86f16172957f09d37c4e944935d18e057190533ca4926c45e55919719f30a817c6f0ab13be19961a9b3b9118c3d9e15a6afd2bc475c47a4489be782f81cba3fa662e51046b5c25271cacb1bb0df7c1296c78031605be8e3d3cec94c33000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d25e2bbd000000000000000000000000000000000000000000000000002386f2d285766200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000a0c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000068e5400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a574d314d7a4e6b5a4330304f5445354c545533597a6b7459544a685953316b5932457a4e6a41774d4452684e574d6966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000006f1eae51a98d4d63e881e1de1190e6fac4385ef40000000000000000000000000000000000000000000000000000000000274099000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc96106531ae87ce3cb1a7f23a013a5832afa64c7d4fe2be189077aa80c681889",
      "signature": {
        "s": "0x77c7e9972238589edf2c4c2271d88aa82e445373d1739794fdfcfb6b1dbd5c44",
        "r": "0xeeba2b3bdea07f896882ceb400583e8b3ef8ad4ca5ac4bf82af0f8639880eea1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbc9a25d86f16172957f09d37c4e944935d18e057190533ca4926c45e55919719",
      "signature": {
        "s": "0x1cba3fa662e51046b5c25271cacb1bb0df7c1296c78031605be8e3d3cec94c33",
        "r": "0xf30a817c6f0ab13be19961a9b3b9118c3d9e15a6afd2bc475c47a4489be782f8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2572441",
    "total": "2572441"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2572441",
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
            "amount": "429652"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2572"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWM1MzNkZC00OTE5LTU3YzktYTJhYS1kY2EzNjAwMDRhNWMifQ==",
    "nonce": 129,
    "balances": {
      "current": "10000001654467517",
      "previous": "10000001657042530"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f1eae51a98d4d63e881e1de1190e6fac4385ef4",
    "nonce": 9,
    "balances": {
      "current": "2572441",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:44.706Z",
  "updated": "2020-05-22T07:59:44.773Z",
  "id": "5ec78670005df800101bc23b"
}
```
* *stageAmount*: `2572441`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000274099000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002740990000000000000000000000000000000000000000000000000000000000274099c96106531ae87ce3cb1a7f23a013a5832afa64c7d4fe2be189077aa80c681889eeba2b3bdea07f896882ceb400583e8b3ef8ad4ca5ac4bf82af0f8639880eea177c7e9972238589edf2c4c2271d88aa82e445373d1739794fdfcfb6b1dbd5c44000000000000000000000000000000000000000000000000000000000000001bbc9a25d86f16172957f09d37c4e944935d18e057190533ca4926c45e55919719f30a817c6f0ab13be19961a9b3b9118c3d9e15a6afd2bc475c47a4489be782f81cba3fa662e51046b5c25271cacb1bb0df7c1296c78031605be8e3d3cec94c33000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000008100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d25e2bbd000000000000000000000000000000000000000000000000002386f2d285766200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000a0c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000068e5400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a574d314d7a4e6b5a4330304f5445354c545533597a6b7459544a685953316b5932457a4e6a41774d4452684e574d6966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000006f1eae51a98d4d63e881e1de1190e6fac4385ef40000000000000000000000000000000000000000000000000000000000274099000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc96106531ae87ce3cb1a7f23a013a5832afa64c7d4fe2be189077aa80c681889",
      "signature": {
        "s": "0x77c7e9972238589edf2c4c2271d88aa82e445373d1739794fdfcfb6b1dbd5c44",
        "r": "0xeeba2b3bdea07f896882ceb400583e8b3ef8ad4ca5ac4bf82af0f8639880eea1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbc9a25d86f16172957f09d37c4e944935d18e057190533ca4926c45e55919719",
      "signature": {
        "s": "0x1cba3fa662e51046b5c25271cacb1bb0df7c1296c78031605be8e3d3cec94c33",
        "r": "0xf30a817c6f0ab13be19961a9b3b9118c3d9e15a6afd2bc475c47a4489be782f8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2572441",
    "total": "2572441"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2572441",
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
            "amount": "429652"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2572"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZWM1MzNkZC00OTE5LTU3YzktYTJhYS1kY2EzNjAwMDRhNWMifQ==",
    "nonce": 129,
    "balances": {
      "current": "10000001654467517",
      "previous": "10000001657042530"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f1eae51a98d4d63e881e1de1190e6fac4385ef4",
    "nonce": 9,
    "balances": {
      "current": "2572441",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:44.706Z",
  "updated": "2020-05-22T07:59:44.773Z",
  "id": "5ec78670005df800101bc23b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000002740990000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2572441`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``