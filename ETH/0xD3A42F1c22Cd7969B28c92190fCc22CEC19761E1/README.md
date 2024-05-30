# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD3A42F1c22Cd7969B28c92190fCc22CEC19761E1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000005b430000000000000000000000000000000000000000000000000000000000005b4300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000005b430000000000000000000000000000000000000000000000000000000000005b43ccc65c3d15766d6f3d1a955e73e8be8e8880311c1bec2fbdce02dd8972dc5efdb72018818ed3f4eda15161e021bfe0d0903cd52e6a38d8f70dd7e3de2d4676626bf81804f92c7de3e0900505d26b98840344a03b31b4c1cddf48157dddc3accd000000000000000000000000000000000000000000000000000000000000001be39c8964f6a0dc72ed919c6ecbd23f149fa08c79d8aa4d9a4104b7f3dc558b229129003c022841d389fc6997a83ec55d0e0753b8383d5d8a6b9f7ba2927b79e22cca91ef1b652d2b4e7dedb44aff311befc82209bc8450888afa171a423d2d98000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000018d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca445b0000000000000000000000000000000000000000000000000002386f2cca4a10a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008050600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f574a6c4e7a4a685a6930784d5468684c54566d59324d74595756694e5331684d6a4134596a4a684d4445354e7a516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d3a42f1c22cd7969b28c92190fcc22cec19761e10000000000000000000000000000000000000000000000000000000000005b43000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccc65c3d15766d6f3d1a955e73e8be8e8880311c1bec2fbdce02dd8972dc5efd",
      "signature": {
        "s": "0x6bf81804f92c7de3e0900505d26b98840344a03b31b4c1cddf48157dddc3accd",
        "r": "0xb72018818ed3f4eda15161e021bfe0d0903cd52e6a38d8f70dd7e3de2d467662",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe39c8964f6a0dc72ed919c6ecbd23f149fa08c79d8aa4d9a4104b7f3dc558b22",
      "signature": {
        "s": "0x2cca91ef1b652d2b4e7dedb44aff311befc82209bc8450888afa171a423d2d98",
        "r": "0x9129003c022841d389fc6997a83ec55d0e0753b8383d5d8a6b9f7ba2927b79e2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23363",
    "total": "23363"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23363",
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
            "amount": "525574"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "23"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOWJlNzJhZi0xMThhLTVmY2MtYWViNS1hMjA4YjJhMDE5NzQifQ==",
    "nonce": 397,
    "balances": {
      "current": "10000001558398384",
      "previous": "10000001558421770"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3a42f1c22cd7969b28c92190fcc22cec19761e1",
    "nonce": 20,
    "balances": {
      "current": "23363",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.036Z",
  "updated": "2020-05-22T08:01:49.113Z",
  "id": "5ec786ed005df800101bc29d"
}
```
* *stageAmount*: `23363`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000005b4300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000005b430000000000000000000000000000000000000000000000000000000000005b43ccc65c3d15766d6f3d1a955e73e8be8e8880311c1bec2fbdce02dd8972dc5efdb72018818ed3f4eda15161e021bfe0d0903cd52e6a38d8f70dd7e3de2d4676626bf81804f92c7de3e0900505d26b98840344a03b31b4c1cddf48157dddc3accd000000000000000000000000000000000000000000000000000000000000001be39c8964f6a0dc72ed919c6ecbd23f149fa08c79d8aa4d9a4104b7f3dc558b229129003c022841d389fc6997a83ec55d0e0753b8383d5d8a6b9f7ba2927b79e22cca91ef1b652d2b4e7dedb44aff311befc82209bc8450888afa171a423d2d98000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000018d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cca445b0000000000000000000000000000000000000000000000000002386f2cca4a10a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008050600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f574a6c4e7a4a685a6930784d5468684c54566d59324d74595756694e5331684d6a4134596a4a684d4445354e7a516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d3a42f1c22cd7969b28c92190fcc22cec19761e10000000000000000000000000000000000000000000000000000000000005b43000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xccc65c3d15766d6f3d1a955e73e8be8e8880311c1bec2fbdce02dd8972dc5efd",
      "signature": {
        "s": "0x6bf81804f92c7de3e0900505d26b98840344a03b31b4c1cddf48157dddc3accd",
        "r": "0xb72018818ed3f4eda15161e021bfe0d0903cd52e6a38d8f70dd7e3de2d467662",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe39c8964f6a0dc72ed919c6ecbd23f149fa08c79d8aa4d9a4104b7f3dc558b22",
      "signature": {
        "s": "0x2cca91ef1b652d2b4e7dedb44aff311befc82209bc8450888afa171a423d2d98",
        "r": "0x9129003c022841d389fc6997a83ec55d0e0753b8383d5d8a6b9f7ba2927b79e2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23363",
    "total": "23363"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23363",
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
            "amount": "525574"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "23"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOWJlNzJhZi0xMThhLTVmY2MtYWViNS1hMjA4YjJhMDE5NzQifQ==",
    "nonce": 397,
    "balances": {
      "current": "10000001558398384",
      "previous": "10000001558421770"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3a42f1c22cd7969b28c92190fcc22cec19761e1",
    "nonce": 20,
    "balances": {
      "current": "23363",
      "previous": "0"
    }
  },
  "blockNumber": "10114500",
  "created": "2020-05-22T08:01:49.036Z",
  "updated": "2020-05-22T08:01:49.113Z",
  "id": "5ec786ed005df800101bc29d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000005b430000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `23363`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``