# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb1c19270Ec8eB9B00973B6310878D0BC96fAb3D2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000031a700000000000000000000000000000000000000000000000000000000000031a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000031a700000000000000000000000000000000000000000000000000000000000031a727b6f65a68682bea7a1dcd9fdc9577a555d1a867683b4c510ea989f75db4cc05eed937ec836bd27c362099488aad0c71e9f67d0f5a09de77d3a59347eb8dee9f3d0c0f4c02c5d4cdc21563c72dc80485923dd95d656f2d6da82a4761e2564e68000000000000000000000000000000000000000000000000000000000000001b493dcdb2613d3f359f75cae2cfc7b7738291ddd642a0b7b6546117b3ce2e15216bd8e474b1c2c80b67a3174d9baebb0f5dbf482080bd221f0680625c8b325eb86778192aecf2dce97cd1704fafe8c2d9bc6299d6cc7accacb1d251273ac1c5ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caeae0da000000000000000000000000000000000000000000000000002386f2caeb128d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008756700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d474d7a5a546b315a69316b4e546b324c5456695a474d745957566c5969316c4d6a646d5a4749324f44426d5a6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b1c19270ec8eb9b00973b6310878d0bc96fab3d200000000000000000000000000000000000000000000000000000000000031a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27b6f65a68682bea7a1dcd9fdc9577a555d1a867683b4c510ea989f75db4cc05",
      "signature": {
        "s": "0x3d0c0f4c02c5d4cdc21563c72dc80485923dd95d656f2d6da82a4761e2564e68",
        "r": "0xeed937ec836bd27c362099488aad0c71e9f67d0f5a09de77d3a59347eb8dee9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x493dcdb2613d3f359f75cae2cfc7b7738291ddd642a0b7b6546117b3ce2e1521",
      "signature": {
        "s": "0x6778192aecf2dce97cd1704fafe8c2d9bc6299d6cc7accacb1d251273ac1c5ff",
        "r": "0x6bd8e474b1c2c80b67a3174d9baebb0f5dbf482080bd221f0680625c8b325eb8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12711",
    "total": "12711"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12711",
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
            "amount": "554343"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMGMzZTk1Zi1kNTk2LTViZGMtYWVlYi1lMjdmZGI2ODBmZjIifQ==",
    "nonce": 756,
    "balances": {
      "current": "10000001529471194",
      "previous": "10000001529483917"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb1c19270ec8eb9b00973b6310878d0bc96fab3d2",
    "nonce": 20,
    "balances": {
      "current": "12711",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:32.187Z",
  "updated": "2020-05-22T08:04:32.263Z",
  "id": "5ec78790b0c6090011d5a9cb"
}
```
* *stageAmount*: `12711`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000031a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000031a700000000000000000000000000000000000000000000000000000000000031a727b6f65a68682bea7a1dcd9fdc9577a555d1a867683b4c510ea989f75db4cc05eed937ec836bd27c362099488aad0c71e9f67d0f5a09de77d3a59347eb8dee9f3d0c0f4c02c5d4cdc21563c72dc80485923dd95d656f2d6da82a4761e2564e68000000000000000000000000000000000000000000000000000000000000001b493dcdb2613d3f359f75cae2cfc7b7738291ddd642a0b7b6546117b3ce2e15216bd8e474b1c2c80b67a3174d9baebb0f5dbf482080bd221f0680625c8b325eb86778192aecf2dce97cd1704fafe8c2d9bc6299d6cc7accacb1d251273ac1c5ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cd000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caeae0da000000000000000000000000000000000000000000000000002386f2caeb128d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008756700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d474d7a5a546b315a69316b4e546b324c5456695a474d745957566c5969316c4d6a646d5a4749324f44426d5a6a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b1c19270ec8eb9b00973b6310878d0bc96fab3d200000000000000000000000000000000000000000000000000000000000031a7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27b6f65a68682bea7a1dcd9fdc9577a555d1a867683b4c510ea989f75db4cc05",
      "signature": {
        "s": "0x3d0c0f4c02c5d4cdc21563c72dc80485923dd95d656f2d6da82a4761e2564e68",
        "r": "0xeed937ec836bd27c362099488aad0c71e9f67d0f5a09de77d3a59347eb8dee9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x493dcdb2613d3f359f75cae2cfc7b7738291ddd642a0b7b6546117b3ce2e1521",
      "signature": {
        "s": "0x6778192aecf2dce97cd1704fafe8c2d9bc6299d6cc7accacb1d251273ac1c5ff",
        "r": "0x6bd8e474b1c2c80b67a3174d9baebb0f5dbf482080bd221f0680625c8b325eb8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12711",
    "total": "12711"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12711",
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
            "amount": "554343"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMGMzZTk1Zi1kNTk2LTViZGMtYWVlYi1lMjdmZGI2ODBmZjIifQ==",
    "nonce": 756,
    "balances": {
      "current": "10000001529471194",
      "previous": "10000001529483917"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb1c19270ec8eb9b00973b6310878d0bc96fab3d2",
    "nonce": 20,
    "balances": {
      "current": "12711",
      "previous": "0"
    }
  },
  "blockNumber": "10114509",
  "created": "2020-05-22T08:04:32.187Z",
  "updated": "2020-05-22T08:04:32.263Z",
  "id": "5ec78790b0c6090011d5a9cb"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000031a70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12711`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``