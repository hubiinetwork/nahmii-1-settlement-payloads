# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x259720ce5a98dD93F8da91e6908e65832fE5C22B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000001bad9000000000000000000000000000000000000000000000000000000000001bad90000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001bad9000000000000000000000000000000000000000000000000000000000001bad945993e8b6665174f82f768e0d2616b0b93c25d48cef8a22056f89ab0aeb25bf2fa778e19aa6238e935f4575b3cf77eec046588f9d8d39b4642f41446d01d15f801b90cd010996d7e566e9c1f4c22e6a3b1e134f1a32fff53500a3cc1caed373d000000000000000000000000000000000000000000000000000000000000001b58213c7183dd0bd03f2ca1e38d16a201ac13ebb5f2eaf72c290c66928fbd1e2eec499d5e073d0cc1732ab667943184510133b6335c78121d1b82fda59689bb6a2830966a9dc6fbc09589177064a2fdff2f159204eaf2fb92a7c6743194fe80b5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2dec67504000000000000000000000000000000000000000000000000002386f2dec8304e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000007100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003621600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a526d4e6d51784e69316c4f446b774c5455794f5759744f44686b4f5331695a6a45795a546b335a6a4269596a456966513d3d0000000000000000000000000000000000000000000000000000000000000012000000000000000000000000259720ce5a98dd93f8da91e6908e65832fe5c22b000000000000000000000000000000000000000000000000000000000001bad9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x45993e8b6665174f82f768e0d2616b0b93c25d48cef8a22056f89ab0aeb25bf2",
      "signature": {
        "s": "0x01b90cd010996d7e566e9c1f4c22e6a3b1e134f1a32fff53500a3cc1caed373d",
        "r": "0xfa778e19aa6238e935f4575b3cf77eec046588f9d8d39b4642f41446d01d15f8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x58213c7183dd0bd03f2ca1e38d16a201ac13ebb5f2eaf72c290c66928fbd1e2e",
      "signature": {
        "s": "0x2830966a9dc6fbc09589177064a2fdff2f159204eaf2fb92a7c6743194fe80b5",
        "r": "0xec499d5e073d0cc1732ab667943184510133b6335c78121d1b82fda59689bb6a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "113369",
    "total": "113369"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "113369",
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
            "amount": "221718"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YjRmNmQxNi1lODkwLTUyOWYtODhkOS1iZjEyZTk3ZjBiYjEifQ==",
    "nonce": 78,
    "balances": {
      "current": "10000001862628612",
      "previous": "10000001862742094"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x259720ce5a98dd93f8da91e6908e65832fe5c22b",
    "nonce": 18,
    "balances": {
      "current": "113369",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:30.207Z",
  "updated": "2020-05-22T07:59:30.275Z",
  "id": "5ec78662b0c6090011d5a8ee"
}
```
* *stageAmount*: `113369`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000001bad90000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001bad9000000000000000000000000000000000000000000000000000000000001bad945993e8b6665174f82f768e0d2616b0b93c25d48cef8a22056f89ab0aeb25bf2fa778e19aa6238e935f4575b3cf77eec046588f9d8d39b4642f41446d01d15f801b90cd010996d7e566e9c1f4c22e6a3b1e134f1a32fff53500a3cc1caed373d000000000000000000000000000000000000000000000000000000000000001b58213c7183dd0bd03f2ca1e38d16a201ac13ebb5f2eaf72c290c66928fbd1e2eec499d5e073d0cc1732ab667943184510133b6335c78121d1b82fda59689bb6a2830966a9dc6fbc09589177064a2fdff2f159204eaf2fb92a7c6743194fe80b5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2dec67504000000000000000000000000000000000000000000000000002386f2dec8304e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000007100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003621600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a526d4e6d51784e69316c4f446b774c5455794f5759744f44686b4f5331695a6a45795a546b335a6a4269596a456966513d3d0000000000000000000000000000000000000000000000000000000000000012000000000000000000000000259720ce5a98dd93f8da91e6908e65832fe5c22b000000000000000000000000000000000000000000000000000000000001bad9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x45993e8b6665174f82f768e0d2616b0b93c25d48cef8a22056f89ab0aeb25bf2",
      "signature": {
        "s": "0x01b90cd010996d7e566e9c1f4c22e6a3b1e134f1a32fff53500a3cc1caed373d",
        "r": "0xfa778e19aa6238e935f4575b3cf77eec046588f9d8d39b4642f41446d01d15f8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x58213c7183dd0bd03f2ca1e38d16a201ac13ebb5f2eaf72c290c66928fbd1e2e",
      "signature": {
        "s": "0x2830966a9dc6fbc09589177064a2fdff2f159204eaf2fb92a7c6743194fe80b5",
        "r": "0xec499d5e073d0cc1732ab667943184510133b6335c78121d1b82fda59689bb6a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "113369",
    "total": "113369"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "113369",
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
            "amount": "221718"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1YjRmNmQxNi1lODkwLTUyOWYtODhkOS1iZjEyZTk3ZjBiYjEifQ==",
    "nonce": 78,
    "balances": {
      "current": "10000001862628612",
      "previous": "10000001862742094"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x259720ce5a98dd93f8da91e6908e65832fe5c22b",
    "nonce": 18,
    "balances": {
      "current": "113369",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:30.207Z",
  "updated": "2020-05-22T07:59:30.275Z",
  "id": "5ec78662b0c6090011d5a8ee"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000001bad90000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `113369`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``