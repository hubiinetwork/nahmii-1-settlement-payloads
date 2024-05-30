# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x69315DC4386b72a9B9fF5Ba07c14F9CD242F6ccE`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000012a022df2d22ae33cc1d8234294b51283db8ec0c51dc81c895623f64dafd832447cf92986da502d656dff12b3e5d9e0360a69f981abacb4fda7658724640659dd1123676e27197fe6573bb8ca7c80a1ab9af2385ecfd7a7c1348f1b6ce60ecab8000000000000000000000000000000000000000000000000000000000000001ca9227a8992c21312e471854329b9a48f060af2709dabc0ce96afbfd5c01834c18d7be97398bc6eca41728789d4f6a7b8be2fcfa31693654e1a1edae96cf546bd0e5d04687c3e4bdbe3b5745e8757321bd830a0188525e1764406b5a0244c566e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b99e1000000000000000000000000000000000000000000000000002386f2bc8b99e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20a200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a574d78595442694f4330334d6d49354c5455794d545574596a41774f43316b4f44646d4d445a6c4d54566b4d47596966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000069315dc4386b72a9b9ff5ba07c14f9cd242f6cce0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a022df2d22ae33cc1d8234294b51283db8ec0c51dc81c895623f64dafd83244",
      "signature": {
        "s": "0x1123676e27197fe6573bb8ca7c80a1ab9af2385ecfd7a7c1348f1b6ce60ecab8",
        "r": "0x7cf92986da502d656dff12b3e5d9e0360a69f981abacb4fda7658724640659dd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa9227a8992c21312e471854329b9a48f060af2709dabc0ce96afbfd5c01834c1",
      "signature": {
        "s": "0x0e5d04687c3e4bdbe3b5745e8757321bd830a0188525e1764406b5a0244c566e",
        "r": "0x8d7be97398bc6eca41728789d4f6a7b8be2fcfa31693654e1a1edae96cf546bd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1",
    "total": "1"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1",
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
            "amount": "794786"
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
    "data": "eyJyZWYiOiJkZWMxYTBiOC03MmI5LTUyMTUtYjAwOC1kODdmMDZlMTVkMGYifQ==",
    "nonce": 2165,
    "balances": {
      "current": "10000001288346081",
      "previous": "10000001288346083"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x69315dc4386b72a9b9ff5ba07c14f9cd242f6cce",
    "nonce": 4,
    "balances": {
      "current": "1",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:44.885Z",
  "updated": "2020-05-22T08:14:44.954Z",
  "id": "5ec789f4e5756b00111b8233"
}
```
* *stageAmount*: `1`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000012a022df2d22ae33cc1d8234294b51283db8ec0c51dc81c895623f64dafd832447cf92986da502d656dff12b3e5d9e0360a69f981abacb4fda7658724640659dd1123676e27197fe6573bb8ca7c80a1ab9af2385ecfd7a7c1348f1b6ce60ecab8000000000000000000000000000000000000000000000000000000000000001ca9227a8992c21312e471854329b9a48f060af2709dabc0ce96afbfd5c01834c18d7be97398bc6eca41728789d4f6a7b8be2fcfa31693654e1a1edae96cf546bd0e5d04687c3e4bdbe3b5745e8757321bd830a0188525e1764406b5a0244c566e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b99e1000000000000000000000000000000000000000000000000002386f2bc8b99e300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20a200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a574d78595442694f4330334d6d49354c5455794d545574596a41774f43316b4f44646d4d445a6c4d54566b4d47596966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000069315dc4386b72a9b9ff5ba07c14f9cd242f6cce0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2a022df2d22ae33cc1d8234294b51283db8ec0c51dc81c895623f64dafd83244",
      "signature": {
        "s": "0x1123676e27197fe6573bb8ca7c80a1ab9af2385ecfd7a7c1348f1b6ce60ecab8",
        "r": "0x7cf92986da502d656dff12b3e5d9e0360a69f981abacb4fda7658724640659dd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa9227a8992c21312e471854329b9a48f060af2709dabc0ce96afbfd5c01834c1",
      "signature": {
        "s": "0x0e5d04687c3e4bdbe3b5745e8757321bd830a0188525e1764406b5a0244c566e",
        "r": "0x8d7be97398bc6eca41728789d4f6a7b8be2fcfa31693654e1a1edae96cf546bd",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1",
    "total": "1"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1",
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
            "amount": "794786"
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
    "data": "eyJyZWYiOiJkZWMxYTBiOC03MmI5LTUyMTUtYjAwOC1kODdmMDZlMTVkMGYifQ==",
    "nonce": 2165,
    "balances": {
      "current": "10000001288346081",
      "previous": "10000001288346083"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x69315dc4386b72a9b9ff5ba07c14f9cd242f6cce",
    "nonce": 4,
    "balances": {
      "current": "1",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:44.885Z",
  "updated": "2020-05-22T08:14:44.954Z",
  "id": "5ec789f4e5756b00111b8233"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``