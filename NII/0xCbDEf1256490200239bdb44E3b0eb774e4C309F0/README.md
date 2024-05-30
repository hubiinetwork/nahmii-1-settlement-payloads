# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCbDEf1256490200239bdb44E3b0eb774e4C309F0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de1f20bce5c1e4e000000000000000000000000000000000000000000000000d35bd44ed93300000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d35bd44ed9330000000000000000000000000000000000000000000000000000d35bd44ed9330000e49374991fff2f8e2fae56437c0ad28ed4c0250958376f274cd2d2022a0c2dd8515b0982142b8db11c13111fdcc8a52ffeb6a6d39da99e42ce2ada48e9860e7a6b36f7435b0f8b847f2fca9a17645df4e558a5c0aeda1edce7a4c40665241d92000000000000000000000000000000000000000000000000000000000000001cd547411734b1f49d0909d223ef73b704f1236174e8ba86a09632159f7a6038aa550ec1272cc542f9f2348223562bb2a41c24d87c27d2a6c976f0bc377a0631490fd54ec38ecc536f63e4554017ad3cd2c1e217433f04be4e186922d94c45a2ab000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2158100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000003000000000000000000000000cbdef1256490200239bdb44e3b0eb774e4c309f00000000000000000000000000000000000000000000000000de1f20bce5c1e4e000000000000000000000000000000000000000000000000e173e1f55b7cfe4e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000361b9ab3ede0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000361b9ab3ede0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d5467345a6d4d7a5a5330795a57566d4c5451774e546b7459574d314e6930325a5449794e544d304d3259304e6a556966513d3d000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000554303f288a57f867b680000000000000000000000000000000000000000000055423096b456a6537b6800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe49374991fff2f8e2fae56437c0ad28ed4c0250958376f274cd2d2022a0c2dd8",
      "signature": {
        "s": "0x6b36f7435b0f8b847f2fca9a17645df4e558a5c0aeda1edce7a4c40665241d92",
        "r": "0x515b0982142b8db11c13111fdcc8a52ffeb6a6d39da99e42ce2ada48e9860e7a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd547411734b1f49d0909d223ef73b704f1236174e8ba86a09632159f7a6038aa",
      "signature": {
        "s": "0x0fd54ec38ecc536f63e4554017ad3cd2c1e217433f04be4e186922d94c45a2ab",
        "r": "0x550ec1272cc542f9f2348223562bb2a41c24d87c27d2a6c976f0bc377a063149",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15230000000000000000",
    "total": "15230000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15230000000000000000",
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
            "amount": "15230000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15230000000000000"
      }
    },
    "wallet": "0xcbdef1256490200239bdb44e3b0eb774e4c309f0",
    "data": "eyJyZWYiOiI4MTg4ZmMzZS0yZWVmLTQwNTktYWM1Ni02ZTIyNTM0M2Y0NjUifQ==",
    "nonce": 3,
    "balances": {
      "current": "1000346724773666382",
      "previous": "16245576724773666382"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 92,
    "balances": {
      "current": "402637367336829251386216",
      "previous": "402622137336829251386216"
    }
  },
  "blockNumber": "14816641",
  "created": "2022-05-21T10:13:15.670Z",
  "updated": "2022-05-21T10:13:15.774Z",
  "id": "6288bb3b3592fd001130b85f"
}
```
* *stageAmount*: `1000346724773666382`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000d35bd44ed93300000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000d35bd44ed9330000000000000000000000000000000000000000000000000000d35bd44ed9330000e49374991fff2f8e2fae56437c0ad28ed4c0250958376f274cd2d2022a0c2dd8515b0982142b8db11c13111fdcc8a52ffeb6a6d39da99e42ce2ada48e9860e7a6b36f7435b0f8b847f2fca9a17645df4e558a5c0aeda1edce7a4c40665241d92000000000000000000000000000000000000000000000000000000000000001cd547411734b1f49d0909d223ef73b704f1236174e8ba86a09632159f7a6038aa550ec1272cc542f9f2348223562bb2a41c24d87c27d2a6c976f0bc377a0631490fd54ec38ecc536f63e4554017ad3cd2c1e217433f04be4e186922d94c45a2ab000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2158100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000003000000000000000000000000cbdef1256490200239bdb44e3b0eb774e4c309f00000000000000000000000000000000000000000000000000de1f20bce5c1e4e000000000000000000000000000000000000000000000000e173e1f55b7cfe4e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000361b9ab3ede0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000361b9ab3ede0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d5467345a6d4d7a5a5330795a57566d4c5451774e546b7459574d314e6930325a5449794e544d304d3259304e6a556966513d3d000000000000000000000000000000000000000000000000000000000000005c000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000554303f288a57f867b680000000000000000000000000000000000000000000055423096b456a6537b6800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe49374991fff2f8e2fae56437c0ad28ed4c0250958376f274cd2d2022a0c2dd8",
      "signature": {
        "s": "0x6b36f7435b0f8b847f2fca9a17645df4e558a5c0aeda1edce7a4c40665241d92",
        "r": "0x515b0982142b8db11c13111fdcc8a52ffeb6a6d39da99e42ce2ada48e9860e7a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd547411734b1f49d0909d223ef73b704f1236174e8ba86a09632159f7a6038aa",
      "signature": {
        "s": "0x0fd54ec38ecc536f63e4554017ad3cd2c1e217433f04be4e186922d94c45a2ab",
        "r": "0x550ec1272cc542f9f2348223562bb2a41c24d87c27d2a6c976f0bc377a063149",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15230000000000000000",
    "total": "15230000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15230000000000000000",
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
            "amount": "15230000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15230000000000000"
      }
    },
    "wallet": "0xcbdef1256490200239bdb44e3b0eb774e4c309f0",
    "data": "eyJyZWYiOiI4MTg4ZmMzZS0yZWVmLTQwNTktYWM1Ni02ZTIyNTM0M2Y0NjUifQ==",
    "nonce": 3,
    "balances": {
      "current": "1000346724773666382",
      "previous": "16245576724773666382"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 92,
    "balances": {
      "current": "402637367336829251386216",
      "previous": "402622137336829251386216"
    }
  },
  "blockNumber": "14816641",
  "created": "2022-05-21T10:13:15.670Z",
  "updated": "2022-05-21T10:13:15.774Z",
  "id": "6288bb3b3592fd001130b85f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de1f20bce5c1e4e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000346724773666382`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`