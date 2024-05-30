# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBF06789Ee859698ed737d6C9eB404791a85f5E9e`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000ae9a52fbd5eba000000000000000000000000000000000000000000000000000ae9a52fbd5eba0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000ae9a52fbd5eba000000000000000000000000000000000000000000000000000ae9a52fbd5eba0dcb253b46490821860a303ba4798c18896f24ece898b0629916aebe5dca530c3fad5b6727aa09e23ac0e469436eb0d26018fcc7fec70fc7606a1f7449ea18222e586b2b96075657a6899d237052756166a2334277596f5ce46fc67039d4af45000000000000000000000000000000000000000000000000000000000000001b0f6997dc8450125a42c6771e0a1fa9742845b3887d44a71c8d80bc283afcd36848d7b3acb3e86cc1d2dc78fac4b511ffc6abe38f99ddbba12368311e8858f3ad329605c6ad8b39f97e2142a6604f5a4af7dcba00f680b14934fc106f3a1e1671000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000a800d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000d174000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017af1e6a2512e7bb44a80000000000000000000000000000000000000000000017af1e75118343ce966b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000002cb2c55f3090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001e15cd4b4c5532ba8db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e4751354e7a67794e6930784e6a526a4c5456685957497459546c6b4f53316b4d6d4d324e7a49344e446c6b4f474d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000bf06789ee859698ed737d6c9eb404791a85f5e9e000000000000000000000000000000000000000000000000000ae9a52fbd5eba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0dcb253b46490821860a303ba4798c18896f24ece898b0629916aebe5dca530c",
      "signature": {
        "s": "0x2e586b2b96075657a6899d237052756166a2334277596f5ce46fc67039d4af45",
        "r": "0x3fad5b6727aa09e23ac0e469436eb0d26018fcc7fec70fc7606a1f7449ea1822",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0f6997dc8450125a42c6771e0a1fa9742845b3887d44a71c8d80bc283afcd368",
      "signature": {
        "s": "0x329605c6ad8b39f97e2142a6604f5a4af7dcba00f680b14934fc106f3a1e1671",
        "r": "0x48d7b3acb3e86cc1d2dc78fac4b511ffc6abe38f99ddbba12368311e8858f3ad",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3071645446921914",
    "total": "3071645446921914"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3071645446921914",
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
            "amount": "8879573069560443283675"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3071645446921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNGQ5NzgyNi0xNjRjLTVhYWItYTlkOS1kMmM2NzI4NDlkOGMifQ==",
    "nonce": 53620,
    "balances": {
      "current": "111844800923832808064168",
      "previous": "111844803998549900433003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf06789ee859698ed737d6c9eb404791a85f5e9e",
    "nonce": 1,
    "balances": {
      "current": "3071645446921914",
      "previous": "0"
    }
  },
  "blockNumber": "11010256",
  "created": "2020-10-07T18:49:20.519Z",
  "updated": "2020-10-07T18:49:20.582Z",
  "id": "5f7e0db0909a24001179228c"
}
```
* *stageAmount*: `3071645446921914`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000ae9a52fbd5eba0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000ae9a52fbd5eba000000000000000000000000000000000000000000000000000ae9a52fbd5eba0dcb253b46490821860a303ba4798c18896f24ece898b0629916aebe5dca530c3fad5b6727aa09e23ac0e469436eb0d26018fcc7fec70fc7606a1f7449ea18222e586b2b96075657a6899d237052756166a2334277596f5ce46fc67039d4af45000000000000000000000000000000000000000000000000000000000000001b0f6997dc8450125a42c6771e0a1fa9742845b3887d44a71c8d80bc283afcd36848d7b3acb3e86cc1d2dc78fac4b511ffc6abe38f99ddbba12368311e8858f3ad329605c6ad8b39f97e2142a6604f5a4af7dcba00f680b14934fc106f3a1e1671000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000a800d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000d174000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017af1e6a2512e7bb44a80000000000000000000000000000000000000000000017af1e75118343ce966b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000002cb2c55f3090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001e15cd4b4c5532ba8db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e4751354e7a67794e6930784e6a526a4c5456685957497459546c6b4f53316b4d6d4d324e7a49344e446c6b4f474d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000bf06789ee859698ed737d6c9eb404791a85f5e9e000000000000000000000000000000000000000000000000000ae9a52fbd5eba000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0dcb253b46490821860a303ba4798c18896f24ece898b0629916aebe5dca530c",
      "signature": {
        "s": "0x2e586b2b96075657a6899d237052756166a2334277596f5ce46fc67039d4af45",
        "r": "0x3fad5b6727aa09e23ac0e469436eb0d26018fcc7fec70fc7606a1f7449ea1822",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0f6997dc8450125a42c6771e0a1fa9742845b3887d44a71c8d80bc283afcd368",
      "signature": {
        "s": "0x329605c6ad8b39f97e2142a6604f5a4af7dcba00f680b14934fc106f3a1e1671",
        "r": "0x48d7b3acb3e86cc1d2dc78fac4b511ffc6abe38f99ddbba12368311e8858f3ad",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3071645446921914",
    "total": "3071645446921914"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3071645446921914",
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
            "amount": "8879573069560443283675"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3071645446921"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNGQ5NzgyNi0xNjRjLTVhYWItYTlkOS1kMmM2NzI4NDlkOGMifQ==",
    "nonce": 53620,
    "balances": {
      "current": "111844800923832808064168",
      "previous": "111844803998549900433003"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbf06789ee859698ed737d6c9eb404791a85f5e9e",
    "nonce": 1,
    "balances": {
      "current": "3071645446921914",
      "previous": "0"
    }
  },
  "blockNumber": "11010256",
  "created": "2020-10-07T18:49:20.519Z",
  "updated": "2020-10-07T18:49:20.582Z",
  "id": "5f7e0db0909a24001179228c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000ae9a52fbd5eba0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3071645446921914`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`