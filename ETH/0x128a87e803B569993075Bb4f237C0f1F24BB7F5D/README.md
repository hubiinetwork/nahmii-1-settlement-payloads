# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x128a87e803B569993075Bb4f237C0f1F24BB7F5D`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c26a5b1dfbb2be051bfcf81b80f21fada1eed80f5b7cf45dc5835fc6194e0e103e1d6cc3cb01665809fad5d8f1b182a01df6917e364ec02da1a8c7b5f7ac3b31720bf70fa4934386f299fc458fa67e9f3ceaa38dd74470f25b076a64fa60e4001e000000000000000000000000000000000000000000000000000000000000001b97b09c117ec379589c7324d710d86fa7a9721e6c2125f5ad9b84288ca2a0ff9a343eb3c6759aed3ea8208df8f6965ee9518874334b593756ccd02f6f3ad80aea2f8ce9216c500745dc29a98bee84ccd3438b86c9a01910e0a3ba10784ffec66d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003ce00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca9528ce000000000000000000000000000000000000000000000000002386f2ca952c9100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000088af900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a55774d47526a4e43316b4d7a426d4c54557a4e6d45744f475a6a595331695a574a6c4e47466b4d57466a4e32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000128a87e803b569993075bb4f237c0f1f24bb7f5d00000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a5b1dfbb2be051bfcf81b80f21fada1eed80f5b7cf45dc5835fc6194e0e103e",
      "signature": {
        "s": "0x0bf70fa4934386f299fc458fa67e9f3ceaa38dd74470f25b076a64fa60e4001e",
        "r": "0x1d6cc3cb01665809fad5d8f1b182a01df6917e364ec02da1a8c7b5f7ac3b3172",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x97b09c117ec379589c7324d710d86fa7a9721e6c2125f5ad9b84288ca2a0ff9a",
      "signature": {
        "s": "0x2f8ce9216c500745dc29a98bee84ccd3438b86c9a01910e0a3ba10784ffec66d",
        "r": "0x343eb3c6759aed3ea8208df8f6965ee9518874334b593756ccd02f6f3ad80aea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "962",
    "total": "962"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "962",
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
            "amount": "559865"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzUwMGRjNC1kMzBmLTUzNmEtOGZjYS1iZWJlNGFkMWFjN2QifQ==",
    "nonce": 974,
    "balances": {
      "current": "10000001523853518",
      "previous": "10000001523854481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x128a87e803b569993075bb4f237c0f1f24bb7f5d",
    "nonce": 20,
    "balances": {
      "current": "962",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:57.335Z",
  "updated": "2020-05-22T08:05:57.410Z",
  "id": "5ec787e5e5756b00111b80b0"
}
```
* *stageAmount*: `962`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003c200000000000000000000000000000000000000000000000000000000000003c26a5b1dfbb2be051bfcf81b80f21fada1eed80f5b7cf45dc5835fc6194e0e103e1d6cc3cb01665809fad5d8f1b182a01df6917e364ec02da1a8c7b5f7ac3b31720bf70fa4934386f299fc458fa67e9f3ceaa38dd74470f25b076a64fa60e4001e000000000000000000000000000000000000000000000000000000000000001b97b09c117ec379589c7324d710d86fa7a9721e6c2125f5ad9b84288ca2a0ff9a343eb3c6759aed3ea8208df8f6965ee9518874334b593756ccd02f6f3ad80aea2f8ce9216c500745dc29a98bee84ccd3438b86c9a01910e0a3ba10784ffec66d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003ce00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca9528ce000000000000000000000000000000000000000000000000002386f2ca952c9100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000088af900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a55774d47526a4e43316b4d7a426d4c54557a4e6d45744f475a6a595331695a574a6c4e47466b4d57466a4e32516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000128a87e803b569993075bb4f237c0f1f24bb7f5d00000000000000000000000000000000000000000000000000000000000003c2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a5b1dfbb2be051bfcf81b80f21fada1eed80f5b7cf45dc5835fc6194e0e103e",
      "signature": {
        "s": "0x0bf70fa4934386f299fc458fa67e9f3ceaa38dd74470f25b076a64fa60e4001e",
        "r": "0x1d6cc3cb01665809fad5d8f1b182a01df6917e364ec02da1a8c7b5f7ac3b3172",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x97b09c117ec379589c7324d710d86fa7a9721e6c2125f5ad9b84288ca2a0ff9a",
      "signature": {
        "s": "0x2f8ce9216c500745dc29a98bee84ccd3438b86c9a01910e0a3ba10784ffec66d",
        "r": "0x343eb3c6759aed3ea8208df8f6965ee9518874334b593756ccd02f6f3ad80aea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "962",
    "total": "962"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "962",
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
            "amount": "559865"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzUwMGRjNC1kMzBmLTUzNmEtOGZjYS1iZWJlNGFkMWFjN2QifQ==",
    "nonce": 974,
    "balances": {
      "current": "10000001523853518",
      "previous": "10000001523854481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x128a87e803b569993075bb4f237c0f1f24bb7f5d",
    "nonce": 20,
    "balances": {
      "current": "962",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:57.335Z",
  "updated": "2020-05-22T08:05:57.410Z",
  "id": "5ec787e5e5756b00111b80b0"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000003c20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `962`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``