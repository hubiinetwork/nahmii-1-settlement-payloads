# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbEe7Bd99b1Ad96dc7d6AB7D5b77E5dec28316465`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000000000000000000000000000000000000034ff1ebcc5bd6f80355c632e9e129819c858a506b473bb5ccde813288eccbf3b88d138d50f159add14d8ba03801b71c95eb311d55395b32e9667a267a77b7e83a31cb24d327a542c41995473e9a44ef86ba575f71a53bfebfec4d6413b09315c9610bf000000000000000000000000000000000000000000000000000000000000001c52cc209b07af0545d28c42ae4450236f01e7434cef8448032550bd90d45ec79f73eb65a8bfd982a5cb4d8a6634f57255187c8f8355316503c849aabeb7b3c98e60fbdcebb28f8f0ab39b876d881ca61d5752c319feb8a63bf8168b1fdac9e13e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02c866bfd5000000000000000000000000000000000000000000000000002e0b02c89bcc8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000d91000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f89d418000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f545977596a45354f4330345a6d4e694c5455324e6a49745954566c4f5330794e44426c4f546c684e4455304e44636966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000bee7bd99b1ad96dc7d6ab7d5b77e5dec28316465000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbcc5bd6f80355c632e9e129819c858a506b473bb5ccde813288eccbf3b88d138",
      "signature": {
        "s": "0x4d327a542c41995473e9a44ef86ba575f71a53bfebfec4d6413b09315c9610bf",
        "r": "0xd50f159add14d8ba03801b71c95eb311d55395b32e9667a267a77b7e83a31cb2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x52cc209b07af0545d28c42ae4450236f01e7434cef8448032550bd90d45ec79f",
      "signature": {
        "s": "0x60fbdcebb28f8f0ab39b876d881ca61d5752c319feb8a63bf8168b1fdac9e13e",
        "r": "0x73eb65a8bfd982a5cb4d8a6634f57255187c8f8355316503c849aabeb7b3c98e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3473182",
    "total": "3473182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3473182",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57705878552"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3473"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTYwYjE5OC04ZmNiLTU2NjItYTVlOS0yNDBlOTlhNDU0NDcifQ==",
    "nonce": 7830,
    "balances": {
      "current": "12959955508707285",
      "previous": "12959955512183940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbee7bd99b1ad96dc7d6ab7d5b77e5dec28316465",
    "nonce": 12,
    "balances": {
      "current": "3473182",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:53.299Z",
  "updated": "2020-05-22T08:59:54.399Z",
  "id": "5ec79489e5756b00111b8962"
}
```
* *stageAmount*: `3473182`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000000000000000000000000000000000000034ff1ebcc5bd6f80355c632e9e129819c858a506b473bb5ccde813288eccbf3b88d138d50f159add14d8ba03801b71c95eb311d55395b32e9667a267a77b7e83a31cb24d327a542c41995473e9a44ef86ba575f71a53bfebfec4d6413b09315c9610bf000000000000000000000000000000000000000000000000000000000000001c52cc209b07af0545d28c42ae4450236f01e7434cef8448032550bd90d45ec79f73eb65a8bfd982a5cb4d8a6634f57255187c8f8355316503c849aabeb7b3c98e60fbdcebb28f8f0ab39b876d881ca61d5752c319feb8a63bf8168b1fdac9e13e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02c866bfd5000000000000000000000000000000000000000000000000002e0b02c89bcc8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000d91000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f89d418000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f545977596a45354f4330345a6d4e694c5455324e6a49745954566c4f5330794e44426c4f546c684e4455304e44636966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000bee7bd99b1ad96dc7d6ab7d5b77e5dec28316465000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbcc5bd6f80355c632e9e129819c858a506b473bb5ccde813288eccbf3b88d138",
      "signature": {
        "s": "0x4d327a542c41995473e9a44ef86ba575f71a53bfebfec4d6413b09315c9610bf",
        "r": "0xd50f159add14d8ba03801b71c95eb311d55395b32e9667a267a77b7e83a31cb2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x52cc209b07af0545d28c42ae4450236f01e7434cef8448032550bd90d45ec79f",
      "signature": {
        "s": "0x60fbdcebb28f8f0ab39b876d881ca61d5752c319feb8a63bf8168b1fdac9e13e",
        "r": "0x73eb65a8bfd982a5cb4d8a6634f57255187c8f8355316503c849aabeb7b3c98e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3473182",
    "total": "3473182"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3473182",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "57705878552"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3473"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOTYwYjE5OC04ZmNiLTU2NjItYTVlOS0yNDBlOTlhNDU0NDcifQ==",
    "nonce": 7830,
    "balances": {
      "current": "12959955508707285",
      "previous": "12959955512183940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbee7bd99b1ad96dc7d6ab7d5b77e5dec28316465",
    "nonce": 12,
    "balances": {
      "current": "3473182",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:53.299Z",
  "updated": "2020-05-22T08:59:54.399Z",
  "id": "5ec79489e5756b00111b8962"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000034ff1e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3473182`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`