# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8c72f8cE2F3A56Ad5E44df24a16c16CC7a85C2a1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4eea4f971a9e6db0d336102622a44cc4fa1de0cd1b34ff9e3efff7e624c26f6a089db5e9b213d4f25d239a011bea081c5ae3170b877d2274f04b7a0d9c62dcd7854cd1d51d734e11259dceb45f0464dde444805232aae1ad15789c0d4d489b1ff000000000000000000000000000000000000000000000000000000000000001b0eb8fdc3069f8e4532b47996e2a0be700dbb172d689adae92a43f4a3cadc3a83250dbdd0d35311f7811ecef2ca9fc4a79366f5688ac69fdc9b4b651e6f69387952c42efa0a494f9f0d9a5283118f27de863ec669ea2534f1e89d6ea3116a6295000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74ce7a4000000000000000000000000000000000000000000000000002386f2c74d1f8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009619400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d445a6d5a6a6868596930774d5751784c54566b4d7a4d74596a49314e53316d4d57466a597a686b4e474a6d5a6a556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a100000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeea4f971a9e6db0d336102622a44cc4fa1de0cd1b34ff9e3efff7e624c26f6a0",
      "signature": {
        "s": "0x54cd1d51d734e11259dceb45f0464dde444805232aae1ad15789c0d4d489b1ff",
        "r": "0x89db5e9b213d4f25d239a011bea081c5ae3170b877d2274f04b7a0d9c62dcd78",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0eb8fdc3069f8e4532b47996e2a0be700dbb172d689adae92a43f4a3cadc3a83",
      "signature": {
        "s": "0x52c42efa0a494f9f0d9a5283118f27de863ec669ea2534f1e89d6ea3116a6295",
        "r": "0x250dbdd0d35311f7811ecef2ca9fc4a79366f5688ac69fdc9b4b651e6f693879",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14292",
    "total": "14292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14292",
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
            "amount": "614804"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "14"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDZmZjhhYi0wMWQxLTVkMzMtYjI1NS1mMWFjYzhkNGJmZjUifQ==",
    "nonce": 1346,
    "balances": {
      "current": "10000001468786596",
      "previous": "10000001468800902"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a1",
    "nonce": 20,
    "balances": {
      "current": "14292",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:42.415Z",
  "updated": "2020-05-22T08:08:42.480Z",
  "id": "5ec7888a005df800101bc3e8"
}
```
* *stageAmount*: `14292`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4eea4f971a9e6db0d336102622a44cc4fa1de0cd1b34ff9e3efff7e624c26f6a089db5e9b213d4f25d239a011bea081c5ae3170b877d2274f04b7a0d9c62dcd7854cd1d51d734e11259dceb45f0464dde444805232aae1ad15789c0d4d489b1ff000000000000000000000000000000000000000000000000000000000000001b0eb8fdc3069f8e4532b47996e2a0be700dbb172d689adae92a43f4a3cadc3a83250dbdd0d35311f7811ecef2ca9fc4a79366f5688ac69fdc9b4b651e6f69387952c42efa0a494f9f0d9a5283118f27de863ec669ea2534f1e89d6ea3116a6295000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74ce7a4000000000000000000000000000000000000000000000000002386f2c74d1f8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009619400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d445a6d5a6a6868596930774d5751784c54566b4d7a4d74596a49314e53316d4d57466a597a686b4e474a6d5a6a556966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000008c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a100000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeea4f971a9e6db0d336102622a44cc4fa1de0cd1b34ff9e3efff7e624c26f6a0",
      "signature": {
        "s": "0x54cd1d51d734e11259dceb45f0464dde444805232aae1ad15789c0d4d489b1ff",
        "r": "0x89db5e9b213d4f25d239a011bea081c5ae3170b877d2274f04b7a0d9c62dcd78",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0eb8fdc3069f8e4532b47996e2a0be700dbb172d689adae92a43f4a3cadc3a83",
      "signature": {
        "s": "0x52c42efa0a494f9f0d9a5283118f27de863ec669ea2534f1e89d6ea3116a6295",
        "r": "0x250dbdd0d35311f7811ecef2ca9fc4a79366f5688ac69fdc9b4b651e6f693879",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14292",
    "total": "14292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14292",
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
            "amount": "614804"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "14"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4MDZmZjhhYi0wMWQxLTVkMzMtYjI1NS1mMWFjYzhkNGJmZjUifQ==",
    "nonce": 1346,
    "balances": {
      "current": "10000001468786596",
      "previous": "10000001468800902"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a1",
    "nonce": 20,
    "balances": {
      "current": "14292",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:42.415Z",
  "updated": "2020-05-22T08:08:42.480Z",
  "id": "5ec7888a005df800101bc3e8"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000037d40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14292`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``