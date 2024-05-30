# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x64A99d17F40F276B3fB6B58C53Bf1c8627d7279e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000107000000000000000000000000000000000000000000000000000000000000010700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000107000000000000000000000000000000000000000000000000000000000000010703b38db96942f4723f666ac29310ebf5d88d8d35f97331a9b6f211075ea05f98657e62605a344913d2fef3b6b8a3e7924ecc40392f9b9cca60a94d52d06d937603de354a510c8d82d5758b5ab95493cd8dd39d29361d79ddf0d182782e063fcc000000000000000000000000000000000000000000000000000000000000001c4df5ec9db306496598780b265bd3550542210dcc0e1dd65bd6a7fd528a59ace8d7803dec1b2d1b70360b5efab52317b9876e4d50ab4b2f3a0718e2e4ead3d3282c09adfb65d54efa49042c63bf7acb2ded9fbc9531dfe56d445beaa1b93095cb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f7000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5e21a2000000000000000000000000000000000000000000000000002386f2bc5e22aa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c3200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a4e684d324d774d4330324e6a67794c5455325a445974595755354d4331694d7a646a4d5456694e6a4e6b4e44596966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000064a99d17f40f276b3fb6b58c53bf1c8627d7279e0000000000000000000000000000000000000000000000000000000000000107000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x03b38db96942f4723f666ac29310ebf5d88d8d35f97331a9b6f211075ea05f98",
      "signature": {
        "s": "0x03de354a510c8d82d5758b5ab95493cd8dd39d29361d79ddf0d182782e063fcc",
        "r": "0x657e62605a344913d2fef3b6b8a3e7924ecc40392f9b9cca60a94d52d06d9376",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4df5ec9db306496598780b265bd3550542210dcc0e1dd65bd6a7fd528a59ace8",
      "signature": {
        "s": "0x2c09adfb65d54efa49042c63bf7acb2ded9fbc9531dfe56d445beaa1b93095cb",
        "r": "0xd7803dec1b2d1b70360b5efab52317b9876e4d50ab4b2f3a0718e2e4ead3d328",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "263",
    "total": "263"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "263",
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
            "amount": "797746"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjNhM2MwMC02NjgyLTU2ZDYtYWU5MC1iMzdjMTViNjNkNDYifQ==",
    "nonce": 2270,
    "balances": {
      "current": "10000001285366178",
      "previous": "10000001285366442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64a99d17f40f276b3fb6b58c53bf1c8627d7279e",
    "nonce": 4,
    "balances": {
      "current": "263",
      "previous": "0"
    }
  },
  "blockNumber": "10114551",
  "created": "2020-05-22T08:15:25.622Z",
  "updated": "2020-05-22T08:15:25.692Z",
  "id": "5ec78a1de5756b00111b8256"
}
```
* *stageAmount*: `263`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000010700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000107000000000000000000000000000000000000000000000000000000000000010703b38db96942f4723f666ac29310ebf5d88d8d35f97331a9b6f211075ea05f98657e62605a344913d2fef3b6b8a3e7924ecc40392f9b9cca60a94d52d06d937603de354a510c8d82d5758b5ab95493cd8dd39d29361d79ddf0d182782e063fcc000000000000000000000000000000000000000000000000000000000000001c4df5ec9db306496598780b265bd3550542210dcc0e1dd65bd6a7fd528a59ace8d7803dec1b2d1b70360b5efab52317b9876e4d50ab4b2f3a0718e2e4ead3d3282c09adfb65d54efa49042c63bf7acb2ded9fbc9531dfe56d445beaa1b93095cb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f7000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008de00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5e21a2000000000000000000000000000000000000000000000000002386f2bc5e22aa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c3200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4e6a4e684d324d774d4330324e6a67794c5455325a445974595755354d4331694d7a646a4d5456694e6a4e6b4e44596966513d3d000000000000000000000000000000000000000000000000000000000000000400000000000000000000000064a99d17f40f276b3fb6b58c53bf1c8627d7279e0000000000000000000000000000000000000000000000000000000000000107000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x03b38db96942f4723f666ac29310ebf5d88d8d35f97331a9b6f211075ea05f98",
      "signature": {
        "s": "0x03de354a510c8d82d5758b5ab95493cd8dd39d29361d79ddf0d182782e063fcc",
        "r": "0x657e62605a344913d2fef3b6b8a3e7924ecc40392f9b9cca60a94d52d06d9376",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4df5ec9db306496598780b265bd3550542210dcc0e1dd65bd6a7fd528a59ace8",
      "signature": {
        "s": "0x2c09adfb65d54efa49042c63bf7acb2ded9fbc9531dfe56d445beaa1b93095cb",
        "r": "0xd7803dec1b2d1b70360b5efab52317b9876e4d50ab4b2f3a0718e2e4ead3d328",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "263",
    "total": "263"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "263",
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
            "amount": "797746"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmNjNhM2MwMC02NjgyLTU2ZDYtYWU5MC1iMzdjMTViNjNkNDYifQ==",
    "nonce": 2270,
    "balances": {
      "current": "10000001285366178",
      "previous": "10000001285366442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x64a99d17f40f276b3fb6b58c53bf1c8627d7279e",
    "nonce": 4,
    "balances": {
      "current": "263",
      "previous": "0"
    }
  },
  "blockNumber": "10114551",
  "created": "2020-05-22T08:15:25.622Z",
  "updated": "2020-05-22T08:15:25.692Z",
  "id": "5ec78a1de5756b00111b8256"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `263`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``