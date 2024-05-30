# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3D27a1dCEd86a2E624393163326adcFAF992852B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000006f271a72c94a0b40000000000000000000000000000000000000000000000000000000a52a9955e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a52a9955e000000000000000000000000000000000000000000000000000000f0eb6ff8caba60a058e61302e6e44004f0805c3618d7fc39457cbb61cb97e1d3cd95b5cdb613c606764b33c2ab65c30d80d1ccd8ea90bdc6b1521833d7fa9b1d48cbbbc77e0b16e7db9ba7e419e7ae6bc02fa2ead59121b6eec294c0f4da085bf0789084a7000000000000000000000000000000000000000000000000000000000000001c1e7002992de161ad94857d37e873e25ef9a3bd75b0ce0ecc7a3c348cff69e8d328a3e8ba0aecdc78491bef199f2b5aa5672150dcad1fa2a90298ecec55f748051257229de90d9f7af950fd09c58bdf17e20e2eed94e13b49085bddfb7b8df0ec000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abdc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c192da0117698297da4000000000000000000000000000000000000000000009c192da01180ed77988800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a485860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47626945d4cd77df30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a474d794d5759334e4331684e475a6a4c5455355a5463744f57517a5a43316b4e7a45324d4751354f5464684e57456966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000003d27a1dced86a2e624393163326adcfaf992852b00000000000000000000000000000000000000000000000006f271a72c94a0b400000000000000000000000000000000000000000000000006f2719cd9eb0b5600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba60a058e61302e6e44004f0805c3618d7fc39457cbb61cb97e1d3cd95b5cdb6",
      "signature": {
        "s": "0x0b16e7db9ba7e419e7ae6bc02fa2ead59121b6eec294c0f4da085bf0789084a7",
        "r": "0x13c606764b33c2ab65c30d80d1ccd8ea90bdc6b1521833d7fa9b1d48cbbbc77e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1e7002992de161ad94857d37e873e25ef9a3bd75b0ce0ecc7a3c348cff69e8d3",
      "signature": {
        "s": "0x1257229de90d9f7af950fd09c58bdf17e20e2eed94e13b49085bddfb7b8df0ec",
        "r": "0x28a3e8ba0aecdc78491bef199f2b5aa5672150dcad1fa2a90298ecec55f74805",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "44336518494",
    "total": "1034742134986"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44336518494",
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
            "amount": "27235907908069330746867"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44336518"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGMyMWY3NC1hNGZjLTU5ZTctOWQzZC1kNzE2MGQ5OTdhNWEifQ==",
    "nonce": 109532,
    "balances": {
      "current": "737153627576436429258148",
      "previous": "737153627576480810113160"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3d27a1dced86a2e624393163326adcfaf992852b",
    "nonce": 36,
    "balances": {
      "current": "500587471412961460",
      "previous": "500587427076442966"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:35.316Z",
  "updated": "2022-05-04T08:48:35.398Z",
  "id": "62723de3bbd75600116d042e"
}
```
* *stageAmount*: `500587471412961460`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000a52a9955e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000a52a9955e000000000000000000000000000000000000000000000000000000f0eb6ff8caba60a058e61302e6e44004f0805c3618d7fc39457cbb61cb97e1d3cd95b5cdb613c606764b33c2ab65c30d80d1ccd8ea90bdc6b1521833d7fa9b1d48cbbbc77e0b16e7db9ba7e419e7ae6bc02fa2ead59121b6eec294c0f4da085bf0789084a7000000000000000000000000000000000000000000000000000000000000001c1e7002992de161ad94857d37e873e25ef9a3bd75b0ce0ecc7a3c348cff69e8d328a3e8ba0aecdc78491bef199f2b5aa5672150dcad1fa2a90298ecec55f748051257229de90d9f7af950fd09c58bdf17e20e2eed94e13b49085bddfb7b8df0ec000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abdc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c192da0117698297da4000000000000000000000000000000000000000000009c192da01180ed77988800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000002a485860000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47626945d4cd77df30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a474d794d5759334e4331684e475a6a4c5455355a5463744f57517a5a43316b4e7a45324d4751354f5464684e57456966513d3d00000000000000000000000000000000000000000000000000000000000000240000000000000000000000003d27a1dced86a2e624393163326adcfaf992852b00000000000000000000000000000000000000000000000006f271a72c94a0b400000000000000000000000000000000000000000000000006f2719cd9eb0b5600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba60a058e61302e6e44004f0805c3618d7fc39457cbb61cb97e1d3cd95b5cdb6",
      "signature": {
        "s": "0x0b16e7db9ba7e419e7ae6bc02fa2ead59121b6eec294c0f4da085bf0789084a7",
        "r": "0x13c606764b33c2ab65c30d80d1ccd8ea90bdc6b1521833d7fa9b1d48cbbbc77e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1e7002992de161ad94857d37e873e25ef9a3bd75b0ce0ecc7a3c348cff69e8d3",
      "signature": {
        "s": "0x1257229de90d9f7af950fd09c58bdf17e20e2eed94e13b49085bddfb7b8df0ec",
        "r": "0x28a3e8ba0aecdc78491bef199f2b5aa5672150dcad1fa2a90298ecec55f74805",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "44336518494",
    "total": "1034742134986"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "44336518494",
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
            "amount": "27235907908069330746867"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "44336518"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGMyMWY3NC1hNGZjLTU5ZTctOWQzZC1kNzE2MGQ5OTdhNWEifQ==",
    "nonce": 109532,
    "balances": {
      "current": "737153627576436429258148",
      "previous": "737153627576480810113160"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3d27a1dced86a2e624393163326adcfaf992852b",
    "nonce": 36,
    "balances": {
      "current": "500587471412961460",
      "previous": "500587427076442966"
    }
  },
  "blockNumber": "14709943",
  "created": "2022-05-04T08:48:35.316Z",
  "updated": "2022-05-04T08:48:35.398Z",
  "id": "62723de3bbd75600116d042e"
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
0x0f200f9b00000000000000000000000000000000000000000000000006f271a72c94a0b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `500587471412961460`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`