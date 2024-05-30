# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2D6535A1410dF5D3827BA81B7C011772b0aF8110`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000c17807e0d580f9efb30000000000000000000000000000000000000000000000049640ed915e868f900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000049640ed915e868f90000000000000000000000000000000000000000000000080b6b2cca103e98ae1ae993ff665d5bffb040710108e966d3ccc666d544e500a5e1f719cc5b41e268c690d14a2ef8ccdf469958740d4f31978dcd5fca521c6cb20232797852ec73dad1231232b38a27ffcb71b55e81832efcf462db9bb0389028bad1b81a8b799aef6000000000000000000000000000000000000000000000000000000000000001c72ea0612dcc004d4024fced0bb8b74355e1f63535440c1c52b5f8069950fd02e378e8427e36fa06d49ca6a0a1773579d8d6e47f61c6b88f9b61bc979cfe07a236b71155c82cd66d6af7b5f311ac1baa153f4179a17cd455a824423a3a1db017d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b652000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000031201e50e7ef948e4843000000000000000000000000000000000000000000003124b5be7163a7a7ebef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000012c9be2b493141c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfd1b8f1c0a9efaa880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4752694f446b774d69316c4d324d7a4c54566a5a6a45744f5442694e533032595749794f4449794e444a6d596d596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002d6535a1410df5d3827ba81b7c011772b0af81100000000000000000000000000000000000000000000000c17807e0d580f9efb30000000000000000000000000000000000000000000000bce1c6f3442273602300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae993ff665d5bffb040710108e966d3ccc666d544e500a5e1f719cc5b41e268c",
      "signature": {
        "s": "0x1231232b38a27ffcb71b55e81832efcf462db9bb0389028bad1b81a8b799aef6",
        "r": "0x690d14a2ef8ccdf469958740d4f31978dcd5fca521c6cb20232797852ec73dad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x72ea0612dcc004d4024fced0bb8b74355e1f63535440c1c52b5f8069950fd02e",
      "signature": {
        "s": "0x6b71155c82cd66d6af7b5f311ac1baa153f4179a17cd455a824423a3a1db017d",
        "r": "0x378e8427e36fa06d49ca6a0a1773579d8d6e47f61c6b88f9b61bc979cfe07a23",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "84613891007648796560",
    "total": "2374348051087507426017"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "84613891007648796560",
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
            "amount": "27740568437144884849288"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "84613891007648796"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMGRiODkwMi1lM2MzLTVjZjEtOTBiNS02YWIyODIyNDJmYmYifQ==",
    "nonce": 112210,
    "balances": {
      "current": "231988437971806771365955",
      "previous": "232073136476705427811311"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d6535a1410df5d3827ba81b7c011772b0af8110",
    "nonce": 46,
    "balances": {
      "current": "3568870735042928308147",
      "previous": "3484256844035279511587"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:34.453Z",
  "updated": "2022-05-04T09:02:34.532Z",
  "id": "6272412abbd75600116d079f"
}
```
* *stageAmount*: `3568870735042928308147`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000049640ed915e868f900000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000049640ed915e868f90000000000000000000000000000000000000000000000080b6b2cca103e98ae1ae993ff665d5bffb040710108e966d3ccc666d544e500a5e1f719cc5b41e268c690d14a2ef8ccdf469958740d4f31978dcd5fca521c6cb20232797852ec73dad1231232b38a27ffcb71b55e81832efcf462db9bb0389028bad1b81a8b799aef6000000000000000000000000000000000000000000000000000000000000001c72ea0612dcc004d4024fced0bb8b74355e1f63535440c1c52b5f8069950fd02e378e8427e36fa06d49ca6a0a1773579d8d6e47f61c6b88f9b61bc979cfe07a236b71155c82cd66d6af7b5f311ac1baa153f4179a17cd455a824423a3a1db017d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b652000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000031201e50e7ef948e4843000000000000000000000000000000000000000000003124b5be7163a7a7ebef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000012c9be2b493141c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dfd1b8f1c0a9efaa880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d4752694f446b774d69316c4d324d7a4c54566a5a6a45744f5442694e533032595749794f4449794e444a6d596d596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000002d6535a1410df5d3827ba81b7c011772b0af81100000000000000000000000000000000000000000000000c17807e0d580f9efb30000000000000000000000000000000000000000000000bce1c6f3442273602300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xae993ff665d5bffb040710108e966d3ccc666d544e500a5e1f719cc5b41e268c",
      "signature": {
        "s": "0x1231232b38a27ffcb71b55e81832efcf462db9bb0389028bad1b81a8b799aef6",
        "r": "0x690d14a2ef8ccdf469958740d4f31978dcd5fca521c6cb20232797852ec73dad",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x72ea0612dcc004d4024fced0bb8b74355e1f63535440c1c52b5f8069950fd02e",
      "signature": {
        "s": "0x6b71155c82cd66d6af7b5f311ac1baa153f4179a17cd455a824423a3a1db017d",
        "r": "0x378e8427e36fa06d49ca6a0a1773579d8d6e47f61c6b88f9b61bc979cfe07a23",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "84613891007648796560",
    "total": "2374348051087507426017"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "84613891007648796560",
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
            "amount": "27740568437144884849288"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "84613891007648796"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMGRiODkwMi1lM2MzLTVjZjEtOTBiNS02YWIyODIyNDJmYmYifQ==",
    "nonce": 112210,
    "balances": {
      "current": "231988437971806771365955",
      "previous": "232073136476705427811311"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d6535a1410df5d3827ba81b7c011772b0af8110",
    "nonce": 46,
    "balances": {
      "current": "3568870735042928308147",
      "previous": "3484256844035279511587"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:02:34.453Z",
  "updated": "2022-05-04T09:02:34.532Z",
  "id": "6272412abbd75600116d079f"
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
0x0f200f9b0000000000000000000000000000000000000000000000c17807e0d580f9efb30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3568870735042928308147`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`