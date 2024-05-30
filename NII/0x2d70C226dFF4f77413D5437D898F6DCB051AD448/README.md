# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2d70C226dFF4f77413D5437D898F6DCB051AD448`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000e27b7c2695ed0000000000000000000000000000000000000000000000000000055ea0c7810e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000055ea0c7810e000000000000000000000000000000000000000000000000000096ad664301568c879861a4330869a2904f05cc47dfe742eb1ac8a1df08733ba0de9ee74c5cb104c46bac7d21d3c8613a57fd7684ef34109512a6d6f2ef2b3aff6ef5fe794b740c363fbec9b9e9710e8def00a0418d043b8a4035918da4f4ad1e4aa88be21d8d000000000000000000000000000000000000000000000000000000000000001cb55f4610d738ec0dfcfb1c3db0230fdc04019b821007d1fb08424c1ce170072108df68a114d84e5d1b25d1f72f574aa8baf195ca865e87f2dab5cd18c359e1c84edc65dc388b3b777b61a5b730e01ca2aad5e8a602c8b09498ab6cc65d97a987000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b203000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c3306947b5b4aa3f080000000000000000000000000000000000000000000049c330694d15b5595fb300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000015fe79f9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984b9afee3e7dd7220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e44466c59544e694f5330334e7a526b4c54566a4e6d4d744f4468694f43316c593249324d6d5a6d597a49784e44636966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000002d70c226dff4f77413d5437d898f6dcb051ad4480000000000000000000000000000000000000000000000000000e27b7c2695ed0000000000000000000000000000000000000000000000000000dd1cdb5f14df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8c879861a4330869a2904f05cc47dfe742eb1ac8a1df08733ba0de9ee74c5cb1",
      "signature": {
        "s": "0x0c363fbec9b9e9710e8def00a0418d043b8a4035918da4f4ad1e4aa88be21d8d",
        "r": "0x04c46bac7d21d3c8613a57fd7684ef34109512a6d6f2ef2b3aff6ef5fe794b74",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb55f4610d738ec0dfcfb1c3db0230fdc04019b821007d1fb08424c1ce1700721",
      "signature": {
        "s": "0x4edc65dc388b3b777b61a5b730e01ca2aad5e8a602c8b09498ab6cc65d97a987",
        "r": "0x08df68a114d84e5d1b25d1f72f574aa8baf195ca865e87f2dab5cd18c359e1c8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5903982493966",
    "total": "165671489175894"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5903982493966",
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
            "amount": "27624339747064682239778"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5903982493"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDFlYTNiOS03NzRkLTVjNmMtODhiOC1lY2I2MmZmYzIxNDcifQ==",
    "nonce": 111107,
    "balances": {
      "current": "348333356742089584033544",
      "previous": "348333356747999470510003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d70c226dff4f77413d5437d898f6dcb051ad448",
    "nonce": 45,
    "balances": {
      "current": "249019991758317",
      "previous": "243116009264351"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:35.700Z",
  "updated": "2022-05-04T08:56:35.782Z",
  "id": "62723fc3bbd75600116d0649"
}
```
* *stageAmount*: `249019991758317`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000055ea0c7810e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000055ea0c7810e000000000000000000000000000000000000000000000000000096ad664301568c879861a4330869a2904f05cc47dfe742eb1ac8a1df08733ba0de9ee74c5cb104c46bac7d21d3c8613a57fd7684ef34109512a6d6f2ef2b3aff6ef5fe794b740c363fbec9b9e9710e8def00a0418d043b8a4035918da4f4ad1e4aa88be21d8d000000000000000000000000000000000000000000000000000000000000001cb55f4610d738ec0dfcfb1c3db0230fdc04019b821007d1fb08424c1ce170072108df68a114d84e5d1b25d1f72f574aa8baf195ca865e87f2dab5cd18c359e1c84edc65dc388b3b777b61a5b730e01ca2aad5e8a602c8b09498ab6cc65d97a987000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b203000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c3306947b5b4aa3f080000000000000000000000000000000000000000000049c330694d15b5595fb300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000015fe79f9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d984b9afee3e7dd7220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e44466c59544e694f5330334e7a526b4c54566a4e6d4d744f4468694f43316c593249324d6d5a6d597a49784e44636966513d3d000000000000000000000000000000000000000000000000000000000000002d0000000000000000000000002d70c226dff4f77413d5437d898f6dcb051ad4480000000000000000000000000000000000000000000000000000e27b7c2695ed0000000000000000000000000000000000000000000000000000dd1cdb5f14df00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8c879861a4330869a2904f05cc47dfe742eb1ac8a1df08733ba0de9ee74c5cb1",
      "signature": {
        "s": "0x0c363fbec9b9e9710e8def00a0418d043b8a4035918da4f4ad1e4aa88be21d8d",
        "r": "0x04c46bac7d21d3c8613a57fd7684ef34109512a6d6f2ef2b3aff6ef5fe794b74",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb55f4610d738ec0dfcfb1c3db0230fdc04019b821007d1fb08424c1ce1700721",
      "signature": {
        "s": "0x4edc65dc388b3b777b61a5b730e01ca2aad5e8a602c8b09498ab6cc65d97a987",
        "r": "0x08df68a114d84e5d1b25d1f72f574aa8baf195ca865e87f2dab5cd18c359e1c8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5903982493966",
    "total": "165671489175894"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5903982493966",
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
            "amount": "27624339747064682239778"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5903982493"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNDFlYTNiOS03NzRkLTVjNmMtODhiOC1lY2I2MmZmYzIxNDcifQ==",
    "nonce": 111107,
    "balances": {
      "current": "348333356742089584033544",
      "previous": "348333356747999470510003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d70c226dff4f77413d5437d898f6dcb051ad448",
    "nonce": 45,
    "balances": {
      "current": "249019991758317",
      "previous": "243116009264351"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:35.700Z",
  "updated": "2022-05-04T08:56:35.782Z",
  "id": "62723fc3bbd75600116d0649"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000e27b7c2695ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `249019991758317`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`