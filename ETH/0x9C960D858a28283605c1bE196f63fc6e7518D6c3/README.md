# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9C960D858a28283605c1bE196f63fc6e7518D6c3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000002080000000000000000000000000000000000000000000000000000000000000208000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000002080000000000000000000000000000000000000000000000000000000000000208703d6b96ff3cffa2cb3c29ce94a53b49f1866d07d82b4758235116bef24880848e349624bf3f10d65c9d1c060704b646cce5123ab6ba7c4314c753a294eb2dcb06c96484170ccb736cba846e16032c627577e4fc2a2e50282140e70557f6252a000000000000000000000000000000000000000000000000000000000000001c5913339991089f409c47157d49b20b303ff419c1854269bce1ec72f4a46609bc9d24a0cb8d1ba1db2f1f5c3098c58c51715df74dee62613c5be1ed4f92b36a6436b50664055e08d04cfce15853e4b53060e97a5407f17e38160a7f39c9b99821000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000017100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cce5f7be000000000000000000000000000000000000000000000000002386f2cce5f9c700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007f43b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b597a4931595745774f4330354d574d304c5455794d5759745954426d596930354d44426c596a45354f47466c4e546b6966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000009c960d858a28283605c1be196f63fc6e7518d6c30000000000000000000000000000000000000000000000000000000000000208000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x703d6b96ff3cffa2cb3c29ce94a53b49f1866d07d82b4758235116bef2488084",
      "signature": {
        "s": "0x06c96484170ccb736cba846e16032c627577e4fc2a2e50282140e70557f6252a",
        "r": "0x8e349624bf3f10d65c9d1c060704b646cce5123ab6ba7c4314c753a294eb2dcb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5913339991089f409c47157d49b20b303ff419c1854269bce1ec72f4a46609bc",
      "signature": {
        "s": "0x36b50664055e08d04cfce15853e4b53060e97a5407f17e38160a7f39c9b99821",
        "r": "0x9d24a0cb8d1ba1db2f1f5c3098c58c51715df74dee62613c5be1ed4f92b36a64",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "520",
    "total": "520"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "520",
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
            "amount": "521275"
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
    "data": "eyJyZWYiOiJkYzI1YWEwOC05MWM0LTUyMWYtYTBmYi05MDBlYjE5OGFlNTkifQ==",
    "nonce": 369,
    "balances": {
      "current": "10000001562703806",
      "previous": "10000001562704327"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c960d858a28283605c1be196f63fc6e7518d6c3",
    "nonce": 5,
    "balances": {
      "current": "520",
      "previous": "0"
    }
  },
  "blockNumber": "10114498",
  "created": "2020-05-22T08:01:35.074Z",
  "updated": "2020-05-22T08:01:35.144Z",
  "id": "5ec786df005df800101bc293"
}
```
* *stageAmount*: `520`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000208000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000002080000000000000000000000000000000000000000000000000000000000000208703d6b96ff3cffa2cb3c29ce94a53b49f1866d07d82b4758235116bef24880848e349624bf3f10d65c9d1c060704b646cce5123ab6ba7c4314c753a294eb2dcb06c96484170ccb736cba846e16032c627577e4fc2a2e50282140e70557f6252a000000000000000000000000000000000000000000000000000000000000001c5913339991089f409c47157d49b20b303ff419c1854269bce1ec72f4a46609bc9d24a0cb8d1ba1db2f1f5c3098c58c51715df74dee62613c5be1ed4f92b36a6436b50664055e08d04cfce15853e4b53060e97a5407f17e38160a7f39c9b99821000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000017100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cce5f7be000000000000000000000000000000000000000000000000002386f2cce5f9c700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007f43b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b597a4931595745774f4330354d574d304c5455794d5759745954426d596930354d44426c596a45354f47466c4e546b6966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000009c960d858a28283605c1be196f63fc6e7518d6c30000000000000000000000000000000000000000000000000000000000000208000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x703d6b96ff3cffa2cb3c29ce94a53b49f1866d07d82b4758235116bef2488084",
      "signature": {
        "s": "0x06c96484170ccb736cba846e16032c627577e4fc2a2e50282140e70557f6252a",
        "r": "0x8e349624bf3f10d65c9d1c060704b646cce5123ab6ba7c4314c753a294eb2dcb",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5913339991089f409c47157d49b20b303ff419c1854269bce1ec72f4a46609bc",
      "signature": {
        "s": "0x36b50664055e08d04cfce15853e4b53060e97a5407f17e38160a7f39c9b99821",
        "r": "0x9d24a0cb8d1ba1db2f1f5c3098c58c51715df74dee62613c5be1ed4f92b36a64",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "520",
    "total": "520"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "520",
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
            "amount": "521275"
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
    "data": "eyJyZWYiOiJkYzI1YWEwOC05MWM0LTUyMWYtYTBmYi05MDBlYjE5OGFlNTkifQ==",
    "nonce": 369,
    "balances": {
      "current": "10000001562703806",
      "previous": "10000001562704327"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c960d858a28283605c1be196f63fc6e7518d6c3",
    "nonce": 5,
    "balances": {
      "current": "520",
      "previous": "0"
    }
  },
  "blockNumber": "10114498",
  "created": "2020-05-22T08:01:35.074Z",
  "updated": "2020-05-22T08:01:35.144Z",
  "id": "5ec786df005df800101bc293"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000002080000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `520`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``