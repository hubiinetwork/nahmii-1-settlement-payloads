# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8C36c05Bc5fBee577670A3ea9764AEb8F07E27D5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000deedb2f9291277e0000000000000000000000000000000000000000000000466b3f119a606c00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000466b3f119a606c00000000000000000000000000000000000000000000000000466b3f119a606c0000444c16aa651399048240a43777462e60b27e45f4219a767f909a17ea0c496aef64abb56bd6aa45f316f281af0c0a4f74e6d5716819a0392d81668f04ec5f5fd82fc3c006e904abc9e4bb9a0be673895986828d1a9aba65599bc46b8ea988910d000000000000000000000000000000000000000000000000000000000000001b55a3e6b27e34ef1af779ef54238ce1dccaeb4203d1c546c28ad6b908dff845c727f8518b3af0fd8e574deb268d5b77d104b33f77997bd2c9effce74c76c178ea42a60630af9905cc196d6023000c3aab02311c69ffd22cd0f06ba50baaa6287b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2f35d000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000060000000000000000000000008c36c05bc5fbee577670a3ea9764aeb8f07e27d50000000000000000000000000000000000000000000000000deedb2f9291277e0000000000000000000000000000000000000000000000468b34e6680e38a77e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001206f99e1b3b80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001206f99e1b3b80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e544131593256684d6931684e7a6b304c54526a4f5451744f444934596930344e6a63314d5451344f546c6b4f44636966513d3d00000000000000000000000000000000000000000000000000000000000000d3000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a883ee51c1a645e8c89f00000000000000000000000000000000000000000000a83d8312b00be57cc89f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x444c16aa651399048240a43777462e60b27e45f4219a767f909a17ea0c496aef",
      "signature": {
        "s": "0x2fc3c006e904abc9e4bb9a0be673895986828d1a9aba65599bc46b8ea988910d",
        "r": "0x64abb56bd6aa45f316f281af0c0a4f74e6d5716819a0392d81668f04ec5f5fd8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x55a3e6b27e34ef1af779ef54238ce1dccaeb4203d1c546c28ad6b908dff845c7",
      "signature": {
        "s": "0x42a60630af9905cc196d6023000c3aab02311c69ffd22cd0f06ba50baaa6287b",
        "r": "0x27f8518b3af0fd8e574deb268d5b77d104b33f77997bd2c9effce74c76c178ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1299000000000000000000",
    "total": "1299000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1299000000000000000000",
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
            "amount": "1299000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1299000000000000000"
      }
    },
    "wallet": "0x8c36c05bc5fbee577670a3ea9764aeb8f07e27d5",
    "data": "eyJyZWYiOiJmNTA1Y2VhMi1hNzk0LTRjOTQtODI4Yi04Njc1MTQ4OTlkODcifQ==",
    "nonce": 6,
    "balances": {
      "current": "1003980764319131518",
      "previous": "1301302980764319131518"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 211,
    "balances": {
      "current": "795791265315530369190047",
      "previous": "794492265315530369190047"
    }
  },
  "blockNumber": "14873437",
  "created": "2022-05-30T15:54:17.034Z",
  "updated": "2022-05-30T15:54:17.522Z",
  "id": "6294e8a9bbd75600116d0905"
}
```
* *stageAmount*: `1003980764319131518`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000466b3f119a606c00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000466b3f119a606c00000000000000000000000000000000000000000000000000466b3f119a606c0000444c16aa651399048240a43777462e60b27e45f4219a767f909a17ea0c496aef64abb56bd6aa45f316f281af0c0a4f74e6d5716819a0392d81668f04ec5f5fd82fc3c006e904abc9e4bb9a0be673895986828d1a9aba65599bc46b8ea988910d000000000000000000000000000000000000000000000000000000000000001b55a3e6b27e34ef1af779ef54238ce1dccaeb4203d1c546c28ad6b908dff845c727f8518b3af0fd8e574deb268d5b77d104b33f77997bd2c9effce74c76c178ea42a60630af9905cc196d6023000c3aab02311c69ffd22cd0f06ba50baaa6287b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e2f35d000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000060000000000000000000000008c36c05bc5fbee577670a3ea9764aeb8f07e27d50000000000000000000000000000000000000000000000000deedb2f9291277e0000000000000000000000000000000000000000000000468b34e6680e38a77e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000001206f99e1b3b80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001206f99e1b3b80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e544131593256684d6931684e7a6b304c54526a4f5451744f444934596930344e6a63314d5451344f546c6b4f44636966513d3d00000000000000000000000000000000000000000000000000000000000000d3000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000a883ee51c1a645e8c89f00000000000000000000000000000000000000000000a83d8312b00be57cc89f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x444c16aa651399048240a43777462e60b27e45f4219a767f909a17ea0c496aef",
      "signature": {
        "s": "0x2fc3c006e904abc9e4bb9a0be673895986828d1a9aba65599bc46b8ea988910d",
        "r": "0x64abb56bd6aa45f316f281af0c0a4f74e6d5716819a0392d81668f04ec5f5fd8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x55a3e6b27e34ef1af779ef54238ce1dccaeb4203d1c546c28ad6b908dff845c7",
      "signature": {
        "s": "0x42a60630af9905cc196d6023000c3aab02311c69ffd22cd0f06ba50baaa6287b",
        "r": "0x27f8518b3af0fd8e574deb268d5b77d104b33f77997bd2c9effce74c76c178ea",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1299000000000000000000",
    "total": "1299000000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1299000000000000000000",
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
            "amount": "1299000000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1299000000000000000"
      }
    },
    "wallet": "0x8c36c05bc5fbee577670a3ea9764aeb8f07e27d5",
    "data": "eyJyZWYiOiJmNTA1Y2VhMi1hNzk0LTRjOTQtODI4Yi04Njc1MTQ4OTlkODcifQ==",
    "nonce": 6,
    "balances": {
      "current": "1003980764319131518",
      "previous": "1301302980764319131518"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 211,
    "balances": {
      "current": "795791265315530369190047",
      "previous": "794492265315530369190047"
    }
  },
  "blockNumber": "14873437",
  "created": "2022-05-30T15:54:17.034Z",
  "updated": "2022-05-30T15:54:17.522Z",
  "id": "6294e8a9bbd75600116d0905"
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
0x0f200f9b0000000000000000000000000000000000000000000000000deedb2f9291277e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1003980764319131518`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`