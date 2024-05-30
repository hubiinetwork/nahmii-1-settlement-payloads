# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1fa8B8Da6AeC2b0d2236c074EF6191618F1ecB07`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000920400000000000000000000000000000000000000000000000000000000000092040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000920400000000000000000000000000000000000000000000000000000000000092040ca0a309a6566fa8ea20114f05950333a5141ef8dcdb3d646ebff0a925870710c1bd74f2f75904cf1c137780ad4a193d4b848ba132ed965cb218a0fd2a231a1050831dacbd8b5f13304305494354c2ea1b9e89a2d36e0cd9728693d7f7837ede000000000000000000000000000000000000000000000000000000000000001c74d5a829fefc86d96fe8c41be5feaad72f95c55aa1aa85b4a00e61c41ac0af6a4a05d2e839dc51a06a5a511c8b69be13943cd008dfc3c2ecd6decdaf00fa5efd494ad5282e00edae06b2d64d808208a82ee3e0283ccb21c9c16d581bb70bbaab000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003a100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caad91dc000000000000000000000000000000000000000000000000002386f2caae240500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000250000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884cf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e54686b4e5459334d7930794e6a45354c5455774f44597459546b315a4330354e6a68695a4445354d6a5669596a456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001fa8b8da6aec2b0d2236c074ef6191618f1ecb070000000000000000000000000000000000000000000000000000000000009204000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ca0a309a6566fa8ea20114f05950333a5141ef8dcdb3d646ebff0a925870710",
      "signature": {
        "s": "0x50831dacbd8b5f13304305494354c2ea1b9e89a2d36e0cd9728693d7f7837ede",
        "r": "0xc1bd74f2f75904cf1c137780ad4a193d4b848ba132ed965cb218a0fd2a231a10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x74d5a829fefc86d96fe8c41be5feaad72f95c55aa1aa85b4a00e61c41ac0af6a",
      "signature": {
        "s": "0x494ad5282e00edae06b2d64d808208a82ee3e0283ccb21c9c16d581bb70bbaab",
        "r": "0x4a05d2e839dc51a06a5a511c8b69be13943cd008dfc3c2ecd6decdaf00fa5efd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37380",
    "total": "37380"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37380",
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
            "amount": "558287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "37"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NThkNTY3My0yNjE5LTUwODYtYTk1ZC05NjhiZDE5MjViYjEifQ==",
    "nonce": 929,
    "balances": {
      "current": "10000001525453276",
      "previous": "10000001525490693"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1fa8b8da6aec2b0d2236c074ef6191618f1ecb07",
    "nonce": 20,
    "balances": {
      "current": "37380",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:29.910Z",
  "updated": "2020-05-22T08:05:31.966Z",
  "id": "5ec787c9005df800101bc34e"
}
```
* *stageAmount*: `37380`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000092040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000920400000000000000000000000000000000000000000000000000000000000092040ca0a309a6566fa8ea20114f05950333a5141ef8dcdb3d646ebff0a925870710c1bd74f2f75904cf1c137780ad4a193d4b848ba132ed965cb218a0fd2a231a1050831dacbd8b5f13304305494354c2ea1b9e89a2d36e0cd9728693d7f7837ede000000000000000000000000000000000000000000000000000000000000001c74d5a829fefc86d96fe8c41be5feaad72f95c55aa1aa85b4a00e61c41ac0af6a4a05d2e839dc51a06a5a511c8b69be13943cd008dfc3c2ecd6decdaf00fa5efd494ad5282e00edae06b2d64d808208a82ee3e0283ccb21c9c16d581bb70bbaab000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d4000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000003a100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caad91dc000000000000000000000000000000000000000000000000002386f2caae240500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000250000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884cf00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e54686b4e5459334d7930794e6a45354c5455774f44597459546b315a4330354e6a68695a4445354d6a5669596a456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000001fa8b8da6aec2b0d2236c074ef6191618f1ecb070000000000000000000000000000000000000000000000000000000000009204000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0ca0a309a6566fa8ea20114f05950333a5141ef8dcdb3d646ebff0a925870710",
      "signature": {
        "s": "0x50831dacbd8b5f13304305494354c2ea1b9e89a2d36e0cd9728693d7f7837ede",
        "r": "0xc1bd74f2f75904cf1c137780ad4a193d4b848ba132ed965cb218a0fd2a231a10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x74d5a829fefc86d96fe8c41be5feaad72f95c55aa1aa85b4a00e61c41ac0af6a",
      "signature": {
        "s": "0x494ad5282e00edae06b2d64d808208a82ee3e0283ccb21c9c16d581bb70bbaab",
        "r": "0x4a05d2e839dc51a06a5a511c8b69be13943cd008dfc3c2ecd6decdaf00fa5efd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37380",
    "total": "37380"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37380",
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
            "amount": "558287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "37"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3NThkNTY3My0yNjE5LTUwODYtYTk1ZC05NjhiZDE5MjViYjEifQ==",
    "nonce": 929,
    "balances": {
      "current": "10000001525453276",
      "previous": "10000001525490693"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1fa8b8da6aec2b0d2236c074ef6191618f1ecb07",
    "nonce": 20,
    "balances": {
      "current": "37380",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:29.910Z",
  "updated": "2020-05-22T08:05:31.966Z",
  "id": "5ec787c9005df800101bc34e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000092040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `37380`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``