# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC2d2A53d100a83FA768FFa85213A6fa4c8BE30f7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000001568844ec21f58ef8000000000000000000000000000000000000000000000000000000009e877b370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009e877b370000000000000000000000000000000000000000000000000000000e73be8d535f9089640dd625902c145488b72cc87410b4bbac03949b99ee2be70379cb1280df4c70c23de63157b79340157faca23fb482b728f9b36e6b42e01fbe22b5d4227e0a7e0a88f6954317a0d381f4698dccc395e5866a5c8a1599aada5d2ad1ece3000000000000000000000000000000000000000000000000000000000000001c47d10884675633a9c9c35e0eb9dbf83a835f1a3b7b180d4f7f57ba46a94e7d0f8d4b9263b229193015df0a67e9c6a610d0d24fb0b6b9947a3108a2940922a59e372e3679c6b48c78fe2f1fc64d8827159f14a89cb2a4d3a8d0f68840f345fcb2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b385000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae9d2103e4f000000000000000000000000000000000000000000003bcfa9538aea70c04ee500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000028955f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b72c68ab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a4d784d4449784f533030596a4d334c5455775a6a5974596d5a684e6930334e57497a4e47466b595441324f57456966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000c2d2a53d100a83fa768ffa85213a6fa4c8be30f7000000000000000000000000000000000000000000000001568844ec21f58ef8000000000000000000000000000000000000000000000001568844eb836e13c100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5f9089640dd625902c145488b72cc87410b4bbac03949b99ee2be70379cb1280",
      "signature": {
        "s": "0x7e0a7e0a88f6954317a0d381f4698dccc395e5866a5c8a1599aada5d2ad1ece3",
        "r": "0xdf4c70c23de63157b79340157faca23fb482b728f9b36e6b42e01fbe22b5d422",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x47d10884675633a9c9c35e0eb9dbf83a835f1a3b7b180d4f7f57ba46a94e7d0f",
      "signature": {
        "s": "0x372e3679c6b48c78fe2f1fc64d8827159f14a89cb2a4d3a8d0f68840f345fcb2",
        "r": "0x8d4b9263b229193015df0a67e9c6a610d0d24fb0b6b9947a3108a2940922a59e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2659679031",
    "total": "62071410003"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2659679031",
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
            "amount": "27690156986805911316651"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2659679"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MzMxMDIxOS00YjM3LTUwZjYtYmZhNi03NWIzNGFkYTA2OWEifQ==",
    "nonce": 111493,
    "balances": {
      "current": "282450299761119277891151",
      "previous": "282450299761121940229861"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2d2a53d100a83fa768ffa85213a6fa4c8be30f7",
    "nonce": 30,
    "balances": {
      "current": "24682053538776715000",
      "previous": "24682053536117035969"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:35.775Z",
  "updated": "2022-05-04T08:58:35.902Z",
  "id": "6272403b7832e20011830d15"
}
```
* *stageAmount*: `24682053538776715000`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000009e877b370000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000009e877b370000000000000000000000000000000000000000000000000000000e73be8d535f9089640dd625902c145488b72cc87410b4bbac03949b99ee2be70379cb1280df4c70c23de63157b79340157faca23fb482b728f9b36e6b42e01fbe22b5d4227e0a7e0a88f6954317a0d381f4698dccc395e5866a5c8a1599aada5d2ad1ece3000000000000000000000000000000000000000000000000000000000000001c47d10884675633a9c9c35e0eb9dbf83a835f1a3b7b180d4f7f57ba46a94e7d0f8d4b9263b229193015df0a67e9c6a610d0d24fb0b6b9947a3108a2940922a59e372e3679c6b48c78fe2f1fc64d8827159f14a89cb2a4d3a8d0f68840f345fcb2000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b385000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa9538ae9d2103e4f000000000000000000000000000000000000000000003bcfa9538aea70c04ee500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000028955f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd161f7ec2b72c68ab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a4d784d4449784f533030596a4d334c5455775a6a5974596d5a684e6930334e57497a4e47466b595441324f57456966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000c2d2a53d100a83fa768ffa85213a6fa4c8be30f7000000000000000000000000000000000000000000000001568844ec21f58ef8000000000000000000000000000000000000000000000001568844eb836e13c100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5f9089640dd625902c145488b72cc87410b4bbac03949b99ee2be70379cb1280",
      "signature": {
        "s": "0x7e0a7e0a88f6954317a0d381f4698dccc395e5866a5c8a1599aada5d2ad1ece3",
        "r": "0xdf4c70c23de63157b79340157faca23fb482b728f9b36e6b42e01fbe22b5d422",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x47d10884675633a9c9c35e0eb9dbf83a835f1a3b7b180d4f7f57ba46a94e7d0f",
      "signature": {
        "s": "0x372e3679c6b48c78fe2f1fc64d8827159f14a89cb2a4d3a8d0f68840f345fcb2",
        "r": "0x8d4b9263b229193015df0a67e9c6a610d0d24fb0b6b9947a3108a2940922a59e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2659679031",
    "total": "62071410003"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2659679031",
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
            "amount": "27690156986805911316651"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2659679"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2MzMxMDIxOS00YjM3LTUwZjYtYmZhNi03NWIzNGFkYTA2OWEifQ==",
    "nonce": 111493,
    "balances": {
      "current": "282450299761119277891151",
      "previous": "282450299761121940229861"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2d2a53d100a83fa768ffa85213a6fa4c8be30f7",
    "nonce": 30,
    "balances": {
      "current": "24682053538776715000",
      "previous": "24682053536117035969"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:35.775Z",
  "updated": "2022-05-04T08:58:35.902Z",
  "id": "6272403b7832e20011830d15"
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
0x0f200f9b000000000000000000000000000000000000000000000001568844ec21f58ef80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `24682053538776715000`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`