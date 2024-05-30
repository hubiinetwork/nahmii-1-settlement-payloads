# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc68731Bf63C251Ea420Cd75D4dE9d07898bBdb61`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000b7e7406911ca7eaf00000000000000000000000000000000000000000000000000000000740982d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000740982d90000000000000000000000000000000000000000000000000000000a94158fc7260985c49b42298bd8417b8c5209781442c6d0725324952de12921653d21837a93f144c7c6e37aa8b0cd55b84087615ab05bd296c5e43e27b0524f3f1f73fee4533d75016e89b27b29a94d106cd0027801684c8026d8c223efd8606c47b2e96b000000000000000000000000000000000000000000000000000000000000001b97b9b830dae527e3abbb78db901940949352fb83eac87a1f979b6acd7dc915c4914711aa3f849cfd97f57f089284ea313c640ae475ccd875f78157eee5ea01d1192d1d6e9df6abb577aef95fc7d0c086710fff46688da667595ecf46ab1f3632000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b165000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004af18bdd569cd06ada6a000000000000000000000000000000000000000000004af18bdd569d449211df00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001db49c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9376632db5809cc0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a466b4e6a67784e5331694e3259784c5455315a5451744f5746695a69307a4e4452695a6a45345a6d56684d47516966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000c68731bf63c251ea420cd75d4de9d07898bbdb61000000000000000000000000000000000000000000000000b7e7406911ca7eaf000000000000000000000000000000000000000000000000b7e740689dc0fbd600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x260985c49b42298bd8417b8c5209781442c6d0725324952de12921653d21837a",
      "signature": {
        "s": "0x533d75016e89b27b29a94d106cd0027801684c8026d8c223efd8606c47b2e96b",
        "r": "0x93f144c7c6e37aa8b0cd55b84087615ab05bd296c5e43e27b0524f3f1f73fee4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x97b9b830dae527e3abbb78db901940949352fb83eac87a1f979b6acd7dc915c4",
      "signature": {
        "s": "0x192d1d6e9df6abb577aef95fc7d0c086710fff46688da667595ecf46ab1f3632",
        "r": "0x914711aa3f849cfd97f57f089284ea313c640ae475ccd875f78157eee5ea01d1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1946780377",
    "total": "45434113991"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1946780377",
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
            "amount": "27618767812380565556239"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1946780"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MjFkNjgxNS1iN2YxLTU1ZTQtOWFiZi0zNDRiZjE4ZmVhMGQifQ==",
    "nonce": 110949,
    "balances": {
      "current": "353910863360890384341610",
      "previous": "353910863360892333068767"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc68731bf63c251ea420cd75d4de9d07898bbdb61",
    "nonce": 31,
    "balances": {
      "current": "13251631248575200943",
      "previous": "13251631246628420566"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:49.261Z",
  "updated": "2022-05-04T08:55:49.352Z",
  "id": "62723f957832e20011830c5d"
}
```
* *stageAmount*: `13251631248575200943`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000740982d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000740982d90000000000000000000000000000000000000000000000000000000a94158fc7260985c49b42298bd8417b8c5209781442c6d0725324952de12921653d21837a93f144c7c6e37aa8b0cd55b84087615ab05bd296c5e43e27b0524f3f1f73fee4533d75016e89b27b29a94d106cd0027801684c8026d8c223efd8606c47b2e96b000000000000000000000000000000000000000000000000000000000000001b97b9b830dae527e3abbb78db901940949352fb83eac87a1f979b6acd7dc915c4914711aa3f849cfd97f57f089284ea313c640ae475ccd875f78157eee5ea01d1192d1d6e9df6abb577aef95fc7d0c086710fff46688da667595ecf46ab1f3632000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b165000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004af18bdd569cd06ada6a000000000000000000000000000000000000000000004af18bdd569d449211df00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001db49c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9376632db5809cc0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a466b4e6a67784e5331694e3259784c5455315a5451744f5746695a69307a4e4452695a6a45345a6d56684d47516966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000c68731bf63c251ea420cd75d4de9d07898bbdb61000000000000000000000000000000000000000000000000b7e7406911ca7eaf000000000000000000000000000000000000000000000000b7e740689dc0fbd600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x260985c49b42298bd8417b8c5209781442c6d0725324952de12921653d21837a",
      "signature": {
        "s": "0x533d75016e89b27b29a94d106cd0027801684c8026d8c223efd8606c47b2e96b",
        "r": "0x93f144c7c6e37aa8b0cd55b84087615ab05bd296c5e43e27b0524f3f1f73fee4",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x97b9b830dae527e3abbb78db901940949352fb83eac87a1f979b6acd7dc915c4",
      "signature": {
        "s": "0x192d1d6e9df6abb577aef95fc7d0c086710fff46688da667595ecf46ab1f3632",
        "r": "0x914711aa3f849cfd97f57f089284ea313c640ae475ccd875f78157eee5ea01d1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1946780377",
    "total": "45434113991"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1946780377",
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
            "amount": "27618767812380565556239"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1946780"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MjFkNjgxNS1iN2YxLTU1ZTQtOWFiZi0zNDRiZjE4ZmVhMGQifQ==",
    "nonce": 110949,
    "balances": {
      "current": "353910863360890384341610",
      "previous": "353910863360892333068767"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc68731bf63c251ea420cd75d4de9d07898bbdb61",
    "nonce": 31,
    "balances": {
      "current": "13251631248575200943",
      "previous": "13251631246628420566"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:55:49.261Z",
  "updated": "2022-05-04T08:55:49.352Z",
  "id": "62723f957832e20011830c5d"
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
0x0f200f9b000000000000000000000000000000000000000000000000b7e7406911ca7eaf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13251631248575200943`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`