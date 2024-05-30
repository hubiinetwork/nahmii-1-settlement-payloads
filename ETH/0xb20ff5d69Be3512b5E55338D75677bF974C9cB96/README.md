# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb20ff5d69Be3512b5E55338D75677bF974C9cB96`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000026a000000000000000000000000000000000000000000000000000000000000026a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000026a000000000000000000000000000000000000000000000000000000000000026a85ce3fe1f099fa0f9fb7ce6fae19398e9d29e2b56333ffbfc3fdf7c784836790b3bec0d6c3b8812b9e117dce1d5d99e785ec679960d3a2ab363da4ed3976bd910dc4af36d516e04d1b308d95c6726dd3abeffa5c3ffef227c9e5dc4f0114c92d000000000000000000000000000000000000000000000000000000000000001b9aa9e036003a1bed9607722e99776861fd113b51c7673e8f248e57f535463bbdf2a284d785ce3e1104e62a2b8dc2fd89a6e3da250558f2a00f3b866e5f403bb1357bb272670c3c6c10e4f9aa609396b43e490b148401115b64d13d66d699eea7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ec000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c4742489000000000000000000000000000000000000000000000000002386f2c47426f400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b6e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6d51794d3245794e4330774e7a4e6c4c5455304d5449744f44597a4e4330784e5445354d4459334d57457a4e54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b20ff5d69be3512b5e55338d75677bf974c9cb96000000000000000000000000000000000000000000000000000000000000026a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85ce3fe1f099fa0f9fb7ce6fae19398e9d29e2b56333ffbfc3fdf7c784836790",
      "signature": {
        "s": "0x0dc4af36d516e04d1b308d95c6726dd3abeffa5c3ffef227c9e5dc4f0114c92d",
        "r": "0xb3bec0d6c3b8812b9e117dce1d5d99e785ec679960d3a2ab363da4ed3976bd91",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9aa9e036003a1bed9607722e99776861fd113b51c7673e8f248e57f535463bbd",
      "signature": {
        "s": "0x357bb272670c3c6c10e4f9aa609396b43e490b148401115b64d13d66d699eea7",
        "r": "0xf2a284d785ce3e1104e62a2b8dc2fd89a6e3da250558f2a00f3b866e5f403bb1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "618",
    "total": "618"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "618",
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
            "amount": "662382"
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
    "data": "eyJyZWYiOiIzZmQyM2EyNC0wNzNlLTU0MTItODYzNC0xNTE5MDY3MWEzNTgifQ==",
    "nonce": 1789,
    "balances": {
      "current": "10000001421026441",
      "previous": "10000001421027060"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb20ff5d69be3512b5e55338d75677bf974c9cb96",
    "nonce": 20,
    "balances": {
      "current": "618",
      "previous": "0"
    }
  },
  "blockNumber": "10114540",
  "created": "2020-05-22T08:12:04.775Z",
  "updated": "2020-05-22T08:12:05.842Z",
  "id": "5ec78954005df800101bc479"
}
```
* *stageAmount*: `618`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000026a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000026a000000000000000000000000000000000000000000000000000000000000026a85ce3fe1f099fa0f9fb7ce6fae19398e9d29e2b56333ffbfc3fdf7c784836790b3bec0d6c3b8812b9e117dce1d5d99e785ec679960d3a2ab363da4ed3976bd910dc4af36d516e04d1b308d95c6726dd3abeffa5c3ffef227c9e5dc4f0114c92d000000000000000000000000000000000000000000000000000000000000001b9aa9e036003a1bed9607722e99776861fd113b51c7673e8f248e57f535463bbdf2a284d785ce3e1104e62a2b8dc2fd89a6e3da250558f2a00f3b866e5f403bb1357bb272670c3c6c10e4f9aa609396b43e490b148401115b64d13d66d699eea7000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ec000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c4742489000000000000000000000000000000000000000000000000002386f2c47426f400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b6e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a6d51794d3245794e4330774e7a4e6c4c5455304d5449744f44597a4e4330784e5445354d4459334d57457a4e54676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b20ff5d69be3512b5e55338d75677bf974c9cb96000000000000000000000000000000000000000000000000000000000000026a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85ce3fe1f099fa0f9fb7ce6fae19398e9d29e2b56333ffbfc3fdf7c784836790",
      "signature": {
        "s": "0x0dc4af36d516e04d1b308d95c6726dd3abeffa5c3ffef227c9e5dc4f0114c92d",
        "r": "0xb3bec0d6c3b8812b9e117dce1d5d99e785ec679960d3a2ab363da4ed3976bd91",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9aa9e036003a1bed9607722e99776861fd113b51c7673e8f248e57f535463bbd",
      "signature": {
        "s": "0x357bb272670c3c6c10e4f9aa609396b43e490b148401115b64d13d66d699eea7",
        "r": "0xf2a284d785ce3e1104e62a2b8dc2fd89a6e3da250558f2a00f3b866e5f403bb1",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "618",
    "total": "618"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "618",
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
            "amount": "662382"
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
    "data": "eyJyZWYiOiIzZmQyM2EyNC0wNzNlLTU0MTItODYzNC0xNTE5MDY3MWEzNTgifQ==",
    "nonce": 1789,
    "balances": {
      "current": "10000001421026441",
      "previous": "10000001421027060"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb20ff5d69be3512b5e55338d75677bf974c9cb96",
    "nonce": 20,
    "balances": {
      "current": "618",
      "previous": "0"
    }
  },
  "blockNumber": "10114540",
  "created": "2020-05-22T08:12:04.775Z",
  "updated": "2020-05-22T08:12:05.842Z",
  "id": "5ec78954005df800101bc479"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000026a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `618`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``