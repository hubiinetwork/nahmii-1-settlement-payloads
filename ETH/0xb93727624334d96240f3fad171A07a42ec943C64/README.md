# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb93727624334d96240f3fad171A07a42ec943C64`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000011200000000000000000000000000000000000000000000000000000000000001120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000011200000000000000000000000000000000000000000000000000000000000001123e2c7e58c1c0fa65db5e5541b8b5b24941ea730ecd88681a421328e672b816e8e6f566414ff4fdb5c0ef471bfd1475c0f1f310f4bdf38f1917cf59a9ec13ed331f66673a1a487d2f6bf65d407ea7c27ba4f87f0950497bb8809ce91abafd92dc000000000000000000000000000000000000000000000000000000000000001b4fcdb6237d4324c6674967ac8249590e6f76e72b17ad6ffe7ca99373b984f0101ec9e1efc9129e227910af76e74d407db8a5a31395492855a95a33c3a7290f3e1e431dbf9a07cf48ff1107dfcf70a50ce86d46cadf56c6160968393c24fe4681000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004ca00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7eba048000000000000000000000000000000000000000000000000002386f2c7eba15b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009392700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e3245794f57457a4d6930354d7a566a4c5455335a6a41744f4752695a69316b4e47557a4e545977596a51795a6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b93727624334d96240f3fad171a07a42ec943c640000000000000000000000000000000000000000000000000000000000000112000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e2c7e58c1c0fa65db5e5541b8b5b24941ea730ecd88681a421328e672b816e8",
      "signature": {
        "s": "0x1f66673a1a487d2f6bf65d407ea7c27ba4f87f0950497bb8809ce91abafd92dc",
        "r": "0xe6f566414ff4fdb5c0ef471bfd1475c0f1f310f4bdf38f1917cf59a9ec13ed33",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4fcdb6237d4324c6674967ac8249590e6f76e72b17ad6ffe7ca99373b984f010",
      "signature": {
        "s": "0x1e431dbf9a07cf48ff1107dfcf70a50ce86d46cadf56c6160968393c24fe4681",
        "r": "0x1ec9e1efc9129e227910af76e74d407db8a5a31395492855a95a33c3a7290f3e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "274",
    "total": "274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "274",
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
            "amount": "604455"
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
    "data": "eyJyZWYiOiJkN2EyOWEzMi05MzVjLTU3ZjAtOGRiZi1kNGUzNTYwYjQyZjIifQ==",
    "nonce": 1226,
    "balances": {
      "current": "10000001479188552",
      "previous": "10000001479188827"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb93727624334d96240f3fad171a07a42ec943c64",
    "nonce": 20,
    "balances": {
      "current": "274",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:43.005Z",
  "updated": "2020-05-22T08:07:43.076Z",
  "id": "5ec7884eb0c6090011d5aa62"
}
```
* *stageAmount*: `274`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000011200000000000000000000000000000000000000000000000000000000000001123e2c7e58c1c0fa65db5e5541b8b5b24941ea730ecd88681a421328e672b816e8e6f566414ff4fdb5c0ef471bfd1475c0f1f310f4bdf38f1917cf59a9ec13ed331f66673a1a487d2f6bf65d407ea7c27ba4f87f0950497bb8809ce91abafd92dc000000000000000000000000000000000000000000000000000000000000001b4fcdb6237d4324c6674967ac8249590e6f76e72b17ad6ffe7ca99373b984f0101ec9e1efc9129e227910af76e74d407db8a5a31395492855a95a33c3a7290f3e1e431dbf9a07cf48ff1107dfcf70a50ce86d46cadf56c6160968393c24fe4681000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55da000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004ca00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7eba048000000000000000000000000000000000000000000000000002386f2c7eba15b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009392700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e3245794f57457a4d6930354d7a566a4c5455335a6a41744f4752695a69316b4e47557a4e545977596a51795a6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b93727624334d96240f3fad171a07a42ec943c640000000000000000000000000000000000000000000000000000000000000112000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e2c7e58c1c0fa65db5e5541b8b5b24941ea730ecd88681a421328e672b816e8",
      "signature": {
        "s": "0x1f66673a1a487d2f6bf65d407ea7c27ba4f87f0950497bb8809ce91abafd92dc",
        "r": "0xe6f566414ff4fdb5c0ef471bfd1475c0f1f310f4bdf38f1917cf59a9ec13ed33",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4fcdb6237d4324c6674967ac8249590e6f76e72b17ad6ffe7ca99373b984f010",
      "signature": {
        "s": "0x1e431dbf9a07cf48ff1107dfcf70a50ce86d46cadf56c6160968393c24fe4681",
        "r": "0x1ec9e1efc9129e227910af76e74d407db8a5a31395492855a95a33c3a7290f3e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "274",
    "total": "274"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "274",
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
            "amount": "604455"
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
    "data": "eyJyZWYiOiJkN2EyOWEzMi05MzVjLTU3ZjAtOGRiZi1kNGUzNTYwYjQyZjIifQ==",
    "nonce": 1226,
    "balances": {
      "current": "10000001479188552",
      "previous": "10000001479188827"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb93727624334d96240f3fad171a07a42ec943c64",
    "nonce": 20,
    "balances": {
      "current": "274",
      "previous": "0"
    }
  },
  "blockNumber": "10114522",
  "created": "2020-05-22T08:07:43.005Z",
  "updated": "2020-05-22T08:07:43.076Z",
  "id": "5ec7884eb0c6090011d5aa62"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `274`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``