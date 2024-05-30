# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9713fe8824c70C2987CD7c649a319F6cf8977165`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000069b000000000000000000000000000000000000000000000000000000000000069b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000069b000000000000000000000000000000000000000000000000000000000000069b2e90fbe7f83fadea44d2a18f12fc7fbc8d6f7a05ed7990bb4313e3ce6fe4efd9872cf39fc37d49a9122cec5c6cbe80667b8fee471b10323b5cd36a718b4cbaf51d2fa93666e4adf20a92ef50c8b728ad073874a50ab9293ff80250ba3645f4e2000000000000000000000000000000000000000000000000000000000000001cafb5f14c8a50976bf54709db5b8407577a8be027846be9ac8b2acf1ff7ee3b37fea604d2ee1dd4345aebb9583f3ec6bde3d6b710856383da85a54356a97ba290346ffac355a47f682b453b5b3afe43b01a13c28ddb9cb20b9269c1a86851a8ef000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2e00163b8000000000000000000000000000000000000000000000000002386f2e0016a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003119a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a5a6c4e4459355953316d4f4442694c54566c5a6a41745954566b5a43316d4d6a686b4f544a685a54426c596a676966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000009713fe8824c70c2987cd7c649a319f6cf8977165000000000000000000000000000000000000000000000000000000000000069b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2e90fbe7f83fadea44d2a18f12fc7fbc8d6f7a05ed7990bb4313e3ce6fe4efd9",
      "signature": {
        "s": "0x1d2fa93666e4adf20a92ef50c8b728ad073874a50ab9293ff80250ba3645f4e2",
        "r": "0x872cf39fc37d49a9122cec5c6cbe80667b8fee471b10323b5cd36a718b4cbaf5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xafb5f14c8a50976bf54709db5b8407577a8be027846be9ac8b2acf1ff7ee3b37",
      "signature": {
        "s": "0x346ffac355a47f682b453b5b3afe43b01a13c28ddb9cb20b9269c1a86851a8ef",
        "r": "0xfea604d2ee1dd4345aebb9583f3ec6bde3d6b710856383da85a54356a97ba290",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1691",
    "total": "1691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1691",
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
            "amount": "201114"
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
    "data": "eyJyZWYiOiIzNzZlNDY5YS1mODBiLTVlZjAtYTVkZC1mMjhkOTJhZTBlYjgifQ==",
    "nonce": 43,
    "balances": {
      "current": "10000001883268024",
      "previous": "10000001883269716"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9713fe8824c70c2987cd7c649a319f6cf8977165",
    "nonce": 23,
    "balances": {
      "current": "1691",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:20.338Z",
  "updated": "2020-05-22T07:59:20.410Z",
  "id": "5ec78658e5756b00111b7f7e"
}
```
* *stageAmount*: `1691`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000069b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000069b000000000000000000000000000000000000000000000000000000000000069b2e90fbe7f83fadea44d2a18f12fc7fbc8d6f7a05ed7990bb4313e3ce6fe4efd9872cf39fc37d49a9122cec5c6cbe80667b8fee471b10323b5cd36a718b4cbaf51d2fa93666e4adf20a92ef50c8b728ad073874a50ab9293ff80250ba3645f4e2000000000000000000000000000000000000000000000000000000000000001cafb5f14c8a50976bf54709db5b8407577a8be027846be9ac8b2acf1ff7ee3b37fea604d2ee1dd4345aebb9583f3ec6bde3d6b710856383da85a54356a97ba290346ffac355a47f682b453b5b3afe43b01a13c28ddb9cb20b9269c1a86851a8ef000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2e00163b8000000000000000000000000000000000000000000000000002386f2e0016a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003119a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a5a6c4e4459355953316d4f4442694c54566c5a6a41745954566b5a43316d4d6a686b4f544a685a54426c596a676966513d3d00000000000000000000000000000000000000000000000000000000000000170000000000000000000000009713fe8824c70c2987cd7c649a319f6cf8977165000000000000000000000000000000000000000000000000000000000000069b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2e90fbe7f83fadea44d2a18f12fc7fbc8d6f7a05ed7990bb4313e3ce6fe4efd9",
      "signature": {
        "s": "0x1d2fa93666e4adf20a92ef50c8b728ad073874a50ab9293ff80250ba3645f4e2",
        "r": "0x872cf39fc37d49a9122cec5c6cbe80667b8fee471b10323b5cd36a718b4cbaf5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xafb5f14c8a50976bf54709db5b8407577a8be027846be9ac8b2acf1ff7ee3b37",
      "signature": {
        "s": "0x346ffac355a47f682b453b5b3afe43b01a13c28ddb9cb20b9269c1a86851a8ef",
        "r": "0xfea604d2ee1dd4345aebb9583f3ec6bde3d6b710856383da85a54356a97ba290",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1691",
    "total": "1691"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1691",
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
            "amount": "201114"
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
    "data": "eyJyZWYiOiIzNzZlNDY5YS1mODBiLTVlZjAtYTVkZC1mMjhkOTJhZTBlYjgifQ==",
    "nonce": 43,
    "balances": {
      "current": "10000001883268024",
      "previous": "10000001883269716"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9713fe8824c70c2987cd7c649a319f6cf8977165",
    "nonce": 23,
    "balances": {
      "current": "1691",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:20.338Z",
  "updated": "2020-05-22T07:59:20.410Z",
  "id": "5ec78658e5756b00111b7f7e"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000069b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1691`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``