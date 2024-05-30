# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x561bBbbFc0fb061EE03507334fc178EcDb478d31`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000421d100000000000000000000000000000000000000000000000000000000000421d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000421d100000000000000000000000000000000000000000000000000000000000421d12c33965e4cbd6ef18b5224f3a03d5c5641e60e5df6962899f680f3047f52a9d8d4b9a55df333e3e2289bcf3dac18a6e8e26097c0a57152617db9340446002b602b88cfa2c4417ed290630184c19cdc9315b6b07f9c0a7b68d9a65533dd076d16000000000000000000000000000000000000000000000000000000000000001c6a6741108e32c9b5cdae3d90947974f471c7539bbf4a74e8da204229db10b92d4562caa99c0f9dfc6645ef249691d7702d2c18a5759af3b493f128c13e222b0e3d24adda91daad9ff7ec4b0a6297665ace7e013705a6dc81bf0fb3fd6f8904ea000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd274ec9000000000000000000000000000000000000000000000000002386f2bd2b71a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000010e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bf8d500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a646c4d6a5a6a5a6930334e4463354c54566c4f4459744f5745315a5330314e7a49334e6a426b4d4746685a44596966513d3d0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000561bbbbfc0fb061ee03507334fc178ecdb478d3100000000000000000000000000000000000000000000000000000000000421d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2c33965e4cbd6ef18b5224f3a03d5c5641e60e5df6962899f680f3047f52a9d8",
      "signature": {
        "s": "0x2b88cfa2c4417ed290630184c19cdc9315b6b07f9c0a7b68d9a65533dd076d16",
        "r": "0xd4b9a55df333e3e2289bcf3dac18a6e8e26097c0a57152617db9340446002b60",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a6741108e32c9b5cdae3d90947974f471c7539bbf4a74e8da204229db10b92d",
      "signature": {
        "s": "0x3d24adda91daad9ff7ec4b0a6297665ace7e013705a6dc81bf0fb3fd6f8904ea",
        "r": "0x4562caa99c0f9dfc6645ef249691d7702d2c18a5759af3b493f128c13e222b0e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "270801",
    "total": "270801"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "270801",
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
            "amount": "784597"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "270"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzdlMjZjZi03NDc5LTVlODYtOWE1ZS01NzI3NjBkMGFhZDYifQ==",
    "nonce": 2117,
    "balances": {
      "current": "10000001298550473",
      "previous": "10000001298821544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x561bbbbfc0fb061ee03507334fc178ecdb478d31",
    "nonce": 9,
    "balances": {
      "current": "270801",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:30.822Z",
  "updated": "2020-05-22T08:14:30.899Z",
  "id": "5ec789e6b0c6090011d5ab93"
}
```
* *stageAmount*: `270801`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000421d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000421d100000000000000000000000000000000000000000000000000000000000421d12c33965e4cbd6ef18b5224f3a03d5c5641e60e5df6962899f680f3047f52a9d8d4b9a55df333e3e2289bcf3dac18a6e8e26097c0a57152617db9340446002b602b88cfa2c4417ed290630184c19cdc9315b6b07f9c0a7b68d9a65533dd076d16000000000000000000000000000000000000000000000000000000000000001c6a6741108e32c9b5cdae3d90947974f471c7539bbf4a74e8da204229db10b92d4562caa99c0f9dfc6645ef249691d7702d2c18a5759af3b493f128c13e222b0e3d24adda91daad9ff7ec4b0a6297665ace7e013705a6dc81bf0fb3fd6f8904ea000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000084500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bd274ec9000000000000000000000000000000000000000000000000002386f2bd2b71a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000010e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000bf8d500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a646c4d6a5a6a5a6930334e4463354c54566c4f4459744f5745315a5330314e7a49334e6a426b4d4746685a44596966513d3d0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000561bbbbfc0fb061ee03507334fc178ecdb478d3100000000000000000000000000000000000000000000000000000000000421d1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2c33965e4cbd6ef18b5224f3a03d5c5641e60e5df6962899f680f3047f52a9d8",
      "signature": {
        "s": "0x2b88cfa2c4417ed290630184c19cdc9315b6b07f9c0a7b68d9a65533dd076d16",
        "r": "0xd4b9a55df333e3e2289bcf3dac18a6e8e26097c0a57152617db9340446002b60",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a6741108e32c9b5cdae3d90947974f471c7539bbf4a74e8da204229db10b92d",
      "signature": {
        "s": "0x3d24adda91daad9ff7ec4b0a6297665ace7e013705a6dc81bf0fb3fd6f8904ea",
        "r": "0x4562caa99c0f9dfc6645ef249691d7702d2c18a5759af3b493f128c13e222b0e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "270801",
    "total": "270801"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "270801",
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
            "amount": "784597"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "270"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzdlMjZjZi03NDc5LTVlODYtOWE1ZS01NzI3NjBkMGFhZDYifQ==",
    "nonce": 2117,
    "balances": {
      "current": "10000001298550473",
      "previous": "10000001298821544"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x561bbbbfc0fb061ee03507334fc178ecdb478d31",
    "nonce": 9,
    "balances": {
      "current": "270801",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:30.822Z",
  "updated": "2020-05-22T08:14:30.899Z",
  "id": "5ec789e6b0c6090011d5ab93"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000421d10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `270801`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``