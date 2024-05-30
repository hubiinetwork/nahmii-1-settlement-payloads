# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAad583e97aA38F443025188c0a4037596eeFEEe7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000fa916d4a55f7262e2000000000000000000000000000000000000000000000000000000097f73a5e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000097f73a5e6000000000000000000000000000000000000000000000000000000dda9e41746f0bb64871507877018677738e4122095bb685ba016aa7702c0fd0c7259730da9177f9a8a48431c83593389fb6e5edca0ebc9d0c7f9f4cd1bb31c3091e6b53966166264e57dcd7980fb3285b79e3b4493e78f8ff6770f68e50d4c07266f6019ef000000000000000000000000000000000000000000000000000000000000001b323d6e1283e295a419f150f1772afea6f559aae86e623ba96c0e5cabcb6b5483fa6d8ca68697a9e993f3c6634d5c9ea4158039c9fc3b1e5624ca0443d37232c01c10df804bc07bdc0ce5d6c14f4fe0ce0c02a7106e2d0682b1c3bd81bf6244d2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad2d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096dc58b5eabf5ec6c12f0000000000000000000000000000000000000000000096dc58b5eac8e0a8dab400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000026e739f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cd0f8a6dd9d06d580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6a646a4d54566b4d4330324f4442684c5456694d5755744f5451784d53316c4f54686a4e7a677a4f5751355954516966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000aad583e97aa38f443025188c0a4037596eefeee700000000000000000000000000000000000000000000000fa916d4a55f7262e200000000000000000000000000000000000000000000000fa916d49bdffebcfc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0bb64871507877018677738e4122095bb685ba016aa7702c0fd0c7259730da9",
      "signature": {
        "s": "0x166264e57dcd7980fb3285b79e3b4493e78f8ff6770f68e50d4c07266f6019ef",
        "r": "0x177f9a8a48431c83593389fb6e5edca0ebc9d0c7f9f4cd1bb31c3091e6b53966",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x323d6e1283e295a419f150f1772afea6f559aae86e623ba96c0e5cabcb6b5483",
      "signature": {
        "s": "0x1c10df804bc07bdc0ce5d6c14f4fe0ce0c02a7106e2d0682b1c3bd81bf6244d2",
        "r": "0xfa6d8ca68697a9e993f3c6634d5c9ea4158039c9fc3b1e5624ca0443d37232c0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "40792991206",
    "total": "952038070086"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "40792991206",
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
            "amount": "27260617177975844007256"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "40792991"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMjdjMTVkMC02ODBhLTViMWUtOTQxMS1lOThjNzgzOWQ5YTQifQ==",
    "nonce": 109869,
    "balances": {
      "current": "712419648400016655434031",
      "previous": "712419648400057489218228"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaad583e97aa38f443025188c0a4037596eefeee7",
    "nonce": 35,
    "balances": {
      "current": "288885320754276754146",
      "previous": "288885320713483762940"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:21.907Z",
  "updated": "2022-05-04T08:50:21.970Z",
  "id": "62723e4d7832e20011830aff"
}
```
* *stageAmount*: `288885320754276754146`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000097f73a5e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000097f73a5e6000000000000000000000000000000000000000000000000000000dda9e41746f0bb64871507877018677738e4122095bb685ba016aa7702c0fd0c7259730da9177f9a8a48431c83593389fb6e5edca0ebc9d0c7f9f4cd1bb31c3091e6b53966166264e57dcd7980fb3285b79e3b4493e78f8ff6770f68e50d4c07266f6019ef000000000000000000000000000000000000000000000000000000000000001b323d6e1283e295a419f150f1772afea6f559aae86e623ba96c0e5cabcb6b5483fa6d8ca68697a9e993f3c6634d5c9ea4158039c9fc3b1e5624ca0443d37232c01c10df804bc07bdc0ce5d6c14f4fe0ce0c02a7106e2d0682b1c3bd81bf6244d2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad2d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096dc58b5eabf5ec6c12f0000000000000000000000000000000000000000000096dc58b5eac8e0a8dab400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000026e739f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cd0f8a6dd9d06d580000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d6a646a4d54566b4d4330324f4442684c5456694d5755744f5451784d53316c4f54686a4e7a677a4f5751355954516966513d3d0000000000000000000000000000000000000000000000000000000000000023000000000000000000000000aad583e97aa38f443025188c0a4037596eefeee700000000000000000000000000000000000000000000000fa916d4a55f7262e200000000000000000000000000000000000000000000000fa916d49bdffebcfc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf0bb64871507877018677738e4122095bb685ba016aa7702c0fd0c7259730da9",
      "signature": {
        "s": "0x166264e57dcd7980fb3285b79e3b4493e78f8ff6770f68e50d4c07266f6019ef",
        "r": "0x177f9a8a48431c83593389fb6e5edca0ebc9d0c7f9f4cd1bb31c3091e6b53966",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x323d6e1283e295a419f150f1772afea6f559aae86e623ba96c0e5cabcb6b5483",
      "signature": {
        "s": "0x1c10df804bc07bdc0ce5d6c14f4fe0ce0c02a7106e2d0682b1c3bd81bf6244d2",
        "r": "0xfa6d8ca68697a9e993f3c6634d5c9ea4158039c9fc3b1e5624ca0443d37232c0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "40792991206",
    "total": "952038070086"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "40792991206",
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
            "amount": "27260617177975844007256"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "40792991"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiMjdjMTVkMC02ODBhLTViMWUtOTQxMS1lOThjNzgzOWQ5YTQifQ==",
    "nonce": 109869,
    "balances": {
      "current": "712419648400016655434031",
      "previous": "712419648400057489218228"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaad583e97aa38f443025188c0a4037596eefeee7",
    "nonce": 35,
    "balances": {
      "current": "288885320754276754146",
      "previous": "288885320713483762940"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:21.907Z",
  "updated": "2022-05-04T08:50:21.970Z",
  "id": "62723e4d7832e20011830aff"
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
0x0f200f9b00000000000000000000000000000000000000000000000fa916d4a55f7262e20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `288885320754276754146`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`