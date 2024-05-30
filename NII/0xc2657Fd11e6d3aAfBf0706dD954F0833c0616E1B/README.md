# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc2657Fd11e6d3aAfBf0706dD954F0833c0616E1B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002447161059cc8e3ce0000000000000000000000000000000000000000000000000dc2fb26d57f16fb90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f16fb900000000000000000000000000000000000000000000001822a4621607d99280fecff2e9867597b648596c53711173d19c9bc5761206dfdcd1c50b8e8e0f6efff76f57ec680a7e528a23ba0d5acb651c1f2327793bb050ea7ffb8d8659b6549033dee1ddd2f7b2fb38801684f0e9222251ee2c6f7d1eb975021591dd0fddb48c000000000000000000000000000000000000000000000000000000000000001b0696255e3baf6f802a19e7a4ab734d0a0f0b99f48435fac527bdcfadcf034b94c689f9292152ab52ab700fdd64790aef96dd372bc4f2b42270e3983417c7022541082be4c76716bb84a4cda82ac41011ab35f42822c069f9ddc18f77c8edd9de000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6e6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fcc69bf114b4a0d8404000000000000000000000000000000000000000000002fcd462721da05aaf83300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02899a22cc08420120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d7a45315a5451305979316b596d466c4c5455355a5455744f47457a4d43316a5a575535596a4e684e6a45304f574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c2657fd11e6d3aafbf0706dd954f0833c0616e1b00000000000000000000000000000000000000000000002447161059cc8e3ce00000000000000000000000000000000000000000000000236ae65dec749ccd2700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfecff2e9867597b648596c53711173d19c9bc5761206dfdcd1c50b8e8e0f6eff",
      "signature": {
        "s": "0x33dee1ddd2f7b2fb38801684f0e9222251ee2c6f7d1eb975021591dd0fddb48c",
        "r": "0xf76f57ec680a7e528a23ba0d5acb651c1f2327793bb050ea7ffb8d8659b65490",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0696255e3baf6f802a19e7a4ab734d0a0f0b99f48435fac527bdcfadcf034b94",
      "signature": {
        "s": "0x41082be4c76716bb84a4cda82ac41011ab35f42822c069f9ddc18f77c8edd9de",
        "r": "0xc689f9292152ab52ab700fdd64790aef96dd372bc4f2b42270e3983417c70225",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946166713",
    "total": "445218085709259838080"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946166713",
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
            "amount": "27746828634605211623442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946166"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMzE1ZTQ0Yy1kYmFlLTU5ZTUtOGEzMC1jZWU5YjNhNjE0OWMifQ==",
    "nonce": 112358,
    "balances": {
      "current": "225721980314019670361092",
      "previous": "225737862276310811473971"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2657fd11e6d3aafbf0706dd954f0833c0616e1b",
    "nonce": 46,
    "balances": {
      "current": "669205086257594383584",
      "previous": "653338990062648216871"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:23.076Z",
  "updated": "2022-05-04T09:03:23.171Z",
  "id": "6272415b3592fd001130b76f"
}
```
* *stageAmount*: `669205086257594383584`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f16fb90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f16fb900000000000000000000000000000000000000000000001822a4621607d99280fecff2e9867597b648596c53711173d19c9bc5761206dfdcd1c50b8e8e0f6efff76f57ec680a7e528a23ba0d5acb651c1f2327793bb050ea7ffb8d8659b6549033dee1ddd2f7b2fb38801684f0e9222251ee2c6f7d1eb975021591dd0fddb48c000000000000000000000000000000000000000000000000000000000000001b0696255e3baf6f802a19e7a4ab734d0a0f0b99f48435fac527bdcfadcf034b94c689f9292152ab52ab700fdd64790aef96dd372bc4f2b42270e3983417c7022541082be4c76716bb84a4cda82ac41011ab35f42822c069f9ddc18f77c8edd9de000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6e6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fcc69bf114b4a0d8404000000000000000000000000000000000000000000002fcd462721da05aaf83300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02899a22cc08420120000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d7a45315a5451305979316b596d466c4c5455355a5455744f47457a4d43316a5a575535596a4e684e6a45304f574d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c2657fd11e6d3aafbf0706dd954f0833c0616e1b00000000000000000000000000000000000000000000002447161059cc8e3ce00000000000000000000000000000000000000000000000236ae65dec749ccd2700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfecff2e9867597b648596c53711173d19c9bc5761206dfdcd1c50b8e8e0f6eff",
      "signature": {
        "s": "0x33dee1ddd2f7b2fb38801684f0e9222251ee2c6f7d1eb975021591dd0fddb48c",
        "r": "0xf76f57ec680a7e528a23ba0d5acb651c1f2327793bb050ea7ffb8d8659b65490",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0696255e3baf6f802a19e7a4ab734d0a0f0b99f48435fac527bdcfadcf034b94",
      "signature": {
        "s": "0x41082be4c76716bb84a4cda82ac41011ab35f42822c069f9ddc18f77c8edd9de",
        "r": "0xc689f9292152ab52ab700fdd64790aef96dd372bc4f2b42270e3983417c70225",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946166713",
    "total": "445218085709259838080"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946166713",
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
            "amount": "27746828634605211623442"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946166"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMzE1ZTQ0Yy1kYmFlLTU5ZTUtOGEzMC1jZWU5YjNhNjE0OWMifQ==",
    "nonce": 112358,
    "balances": {
      "current": "225721980314019670361092",
      "previous": "225737862276310811473971"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2657fd11e6d3aafbf0706dd954f0833c0616e1b",
    "nonce": 46,
    "balances": {
      "current": "669205086257594383584",
      "previous": "653338990062648216871"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:23.076Z",
  "updated": "2022-05-04T09:03:23.171Z",
  "id": "6272415b3592fd001130b76f"
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
0x0f200f9b00000000000000000000000000000000000000000000002447161059cc8e3ce00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205086257594383584`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`