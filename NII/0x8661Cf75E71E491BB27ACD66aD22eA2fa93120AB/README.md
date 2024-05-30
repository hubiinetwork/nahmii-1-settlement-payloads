# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8661Cf75E71E491BB27ACD66aD22eA2fa93120AB`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de22c8ebb413e9a00000000000000000000000000000000000000000000001e0325523f72bc80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001e0325523f72bc800000000000000000000000000000000000000000000000001e0325523f72bc8000e7a7c11c93631aad1590853aeac9b3243a0d41a88933403fe3c791fe4d9d236cb473ace3d3aaa485d1785de083b48afd3d58e0eeb3321255e291f221fb863002133d7cc51e4779060051c4d5600a15876b0dc4af1c50bd3e67b76ec14d6bb5c0000000000000000000000000000000000000000000000000000000000000001c7d5b51e188dfdf6d563ae27b238147e4cc6fa5f876cef6d46813e1cda4994a427e65fc8f5c0f06448a02d8dbbb42d2f2e1902b0fb5d267c74e448bac363debdc2f21550edf3976ef75d7202197eb2e925847a15924904f44bd55bbad21b86603000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1cf580000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000008661cf75e71e491bb27acd66ad22ea2fa93120ab0000000000000000000000000000000000000000000000000de22c8ebb413e9a00000000000000000000000000000000000000000000001e18b6617298588e9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000007aee2a46a5ad0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007aee2a46a5ad0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d7a67334d6a59774d69307a4d54646d4c54517959544d744f57517a4f433077597a55324e6a41345a5445334d32596966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d9f17fb4baddaf2b668000000000000000000000000000000000000000000001d8114d5f96e6836366800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7a7c11c93631aad1590853aeac9b3243a0d41a88933403fe3c791fe4d9d236c",
      "signature": {
        "s": "0x133d7cc51e4779060051c4d5600a15876b0dc4af1c50bd3e67b76ec14d6bb5c0",
        "r": "0xb473ace3d3aaa485d1785de083b48afd3d58e0eeb3321255e291f221fb863002",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7d5b51e188dfdf6d563ae27b238147e4cc6fa5f876cef6d46813e1cda4994a42",
      "signature": {
        "s": "0x2f21550edf3976ef75d7202197eb2e925847a15924904f44bd55bbad21b86603",
        "r": "0x7e65fc8f5c0f06448a02d8dbbb42d2f2e1902b0fb5d267c74e448bac363debdc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "553629000000000000000",
    "total": "553629000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "553629000000000000000",
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
            "amount": "553629000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "553629000000000000"
      }
    },
    "wallet": "0x8661cf75e71e491bb27acd66ad22ea2fa93120ab",
    "data": "eyJyZWYiOiJiMzg3MjYwMi0zMTdmLTQyYTMtOWQzOC0wYzU2NjA4ZTE3M2YifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000411058768264858",
      "previous": "555183040058768264858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 41,
    "balances": {
      "current": "139883388369031631386216",
      "previous": "139329759369031631386216"
    }
  },
  "blockNumber": "14798680",
  "created": "2022-05-18T11:52:07.524Z",
  "updated": "2022-05-18T11:52:07.663Z",
  "id": "6284dde73592fd001130b838"
}
```
* *stageAmount*: `1000411058768264858`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001e0325523f72bc80000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001e0325523f72bc800000000000000000000000000000000000000000000000001e0325523f72bc8000e7a7c11c93631aad1590853aeac9b3243a0d41a88933403fe3c791fe4d9d236cb473ace3d3aaa485d1785de083b48afd3d58e0eeb3321255e291f221fb863002133d7cc51e4779060051c4d5600a15876b0dc4af1c50bd3e67b76ec14d6bb5c0000000000000000000000000000000000000000000000000000000000000001c7d5b51e188dfdf6d563ae27b238147e4cc6fa5f876cef6d46813e1cda4994a427e65fc8f5c0f06448a02d8dbbb42d2f2e1902b0fb5d267c74e448bac363debdc2f21550edf3976ef75d7202197eb2e925847a15924904f44bd55bbad21b86603000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1cf580000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000008661cf75e71e491bb27acd66ad22ea2fa93120ab0000000000000000000000000000000000000000000000000de22c8ebb413e9a00000000000000000000000000000000000000000000001e18b6617298588e9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000007aee2a46a5ad0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007aee2a46a5ad0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d7a67334d6a59774d69307a4d54646d4c54517959544d744f57517a4f433077597a55324e6a41345a5445334d32596966513d3d0000000000000000000000000000000000000000000000000000000000000029000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001d9f17fb4baddaf2b668000000000000000000000000000000000000000000001d8114d5f96e6836366800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7a7c11c93631aad1590853aeac9b3243a0d41a88933403fe3c791fe4d9d236c",
      "signature": {
        "s": "0x133d7cc51e4779060051c4d5600a15876b0dc4af1c50bd3e67b76ec14d6bb5c0",
        "r": "0xb473ace3d3aaa485d1785de083b48afd3d58e0eeb3321255e291f221fb863002",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7d5b51e188dfdf6d563ae27b238147e4cc6fa5f876cef6d46813e1cda4994a42",
      "signature": {
        "s": "0x2f21550edf3976ef75d7202197eb2e925847a15924904f44bd55bbad21b86603",
        "r": "0x7e65fc8f5c0f06448a02d8dbbb42d2f2e1902b0fb5d267c74e448bac363debdc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "553629000000000000000",
    "total": "553629000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "553629000000000000000",
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
            "amount": "553629000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "553629000000000000"
      }
    },
    "wallet": "0x8661cf75e71e491bb27acd66ad22ea2fa93120ab",
    "data": "eyJyZWYiOiJiMzg3MjYwMi0zMTdmLTQyYTMtOWQzOC0wYzU2NjA4ZTE3M2YifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000411058768264858",
      "previous": "555183040058768264858"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 41,
    "balances": {
      "current": "139883388369031631386216",
      "previous": "139329759369031631386216"
    }
  },
  "blockNumber": "14798680",
  "created": "2022-05-18T11:52:07.524Z",
  "updated": "2022-05-18T11:52:07.663Z",
  "id": "6284dde73592fd001130b838"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de22c8ebb413e9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000411058768264858`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`