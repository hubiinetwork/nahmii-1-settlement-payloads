# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4FeF95C773dA7c984A0B8B752930d49D0403D3a6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000161d86c2ba1f6556b000000000000000000000000000000000000000000000000001f0092ec907cbd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001f0092ec907cbd0000000000000000000000000000000000000000000000000365f3f878dcc050346fbc402fba71f07d1bbd86a2d2fd92f3dccaf7e1827bae3cb46a8b733026cc5c3eda0b53830c7148c30b99767d5c10308824856af402aad961b4c7a89bc791338c26e02632f9d0499615ad1bf2831b56fb6718649378842ae588de3e758408000000000000000000000000000000000000000000000000000000000000001b2f2f92c578eb76ab81e9b079a26607ba432991c658a19d2d8cab72a7f359b66566bec8f3dc7421d090fadd7f0cf8736dbacabc317ee708370f7e1df8a57177dc226e848cd085579d5e957d58b0e43eb63e80458d0c27e86ef174687c024f41e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d7e997ed50ab0f11840000000000000000000000000000000000000000000095d7e9b6f5d35aee8c5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000007efc34efe130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60faa4bc4ea1b07640000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a446c684e574d785a6930345a6a6c684c545668597a6b744f474a6d5969316a4d6d4d325a444a694e4467325a47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004fef95c773da7c984a0b8b752930d49d0403d3a600000000000000000000000000000000000000000000000161d86c2ba1f6556b00000000000000000000000000000000000000000000000161b96b98b565d8ae00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x346fbc402fba71f07d1bbd86a2d2fd92f3dccaf7e1827bae3cb46a8b733026cc",
      "signature": {
        "s": "0x338c26e02632f9d0499615ad1bf2831b56fb6718649378842ae588de3e758408",
        "r": "0x5c3eda0b53830c7148c30b99767d5c10308824856af402aad961b4c7a89bc791",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2f2f92c578eb76ab81e9b079a26607ba432991c658a19d2d8cab72a7f359b665",
      "signature": {
        "s": "0x226e848cd085579d5e957d58b0e43eb63e80458d0c27e86ef174687c024f41e0",
        "r": "0x66bec8f3dc7421d090fadd7f0cf8736dbacabc317ee708370f7e1df8a57177dc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8726355312147645",
    "total": "244870003266732112"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8726355312147645",
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
            "amount": "27265416538908440332132"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8726355312147"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZDlhNWMxZi04ZjlhLTVhYzktOGJmYi1jMmM2ZDJiNDg2ZGEifQ==",
    "nonce": 110305,
    "balances": {
      "current": "707615488106487734014340",
      "previous": "707615496841569401474132"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4fef95c773da7c984a0b8b752930d49d0403d3a6",
    "nonce": 46,
    "balances": {
      "current": "25497248225014732139",
      "previous": "25488521869702584494"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:35.311Z",
  "updated": "2022-05-04T08:52:35.390Z",
  "id": "62723ed3bbd75600116d053a"
}
```
* *stageAmount*: `25497248225014732139`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000001f0092ec907cbd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001f0092ec907cbd0000000000000000000000000000000000000000000000000365f3f878dcc050346fbc402fba71f07d1bbd86a2d2fd92f3dccaf7e1827bae3cb46a8b733026cc5c3eda0b53830c7148c30b99767d5c10308824856af402aad961b4c7a89bc791338c26e02632f9d0499615ad1bf2831b56fb6718649378842ae588de3e758408000000000000000000000000000000000000000000000000000000000000001b2f2f92c578eb76ab81e9b079a26607ba432991c658a19d2d8cab72a7f359b66566bec8f3dc7421d090fadd7f0cf8736dbacabc317ee708370f7e1df8a57177dc226e848cd085579d5e957d58b0e43eb63e80458d0c27e86ef174687c024f41e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aee1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d7e997ed50ab0f11840000000000000000000000000000000000000000000095d7e9b6f5d35aee8c5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000007efc34efe130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60faa4bc4ea1b07640000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a446c684e574d785a6930345a6a6c684c545668597a6b744f474a6d5969316a4d6d4d325a444a694e4467325a47456966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000004fef95c773da7c984a0b8b752930d49d0403d3a600000000000000000000000000000000000000000000000161d86c2ba1f6556b00000000000000000000000000000000000000000000000161b96b98b565d8ae00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x346fbc402fba71f07d1bbd86a2d2fd92f3dccaf7e1827bae3cb46a8b733026cc",
      "signature": {
        "s": "0x338c26e02632f9d0499615ad1bf2831b56fb6718649378842ae588de3e758408",
        "r": "0x5c3eda0b53830c7148c30b99767d5c10308824856af402aad961b4c7a89bc791",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2f2f92c578eb76ab81e9b079a26607ba432991c658a19d2d8cab72a7f359b665",
      "signature": {
        "s": "0x226e848cd085579d5e957d58b0e43eb63e80458d0c27e86ef174687c024f41e0",
        "r": "0x66bec8f3dc7421d090fadd7f0cf8736dbacabc317ee708370f7e1df8a57177dc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8726355312147645",
    "total": "244870003266732112"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8726355312147645",
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
            "amount": "27265416538908440332132"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8726355312147"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZDlhNWMxZi04ZjlhLTVhYzktOGJmYi1jMmM2ZDJiNDg2ZGEifQ==",
    "nonce": 110305,
    "balances": {
      "current": "707615488106487734014340",
      "previous": "707615496841569401474132"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4fef95c773da7c984a0b8b752930d49d0403d3a6",
    "nonce": 46,
    "balances": {
      "current": "25497248225014732139",
      "previous": "25488521869702584494"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:35.311Z",
  "updated": "2022-05-04T08:52:35.390Z",
  "id": "62723ed3bbd75600116d053a"
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
0x0f200f9b00000000000000000000000000000000000000000000000161d86c2ba1f6556b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `25497248225014732139`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`