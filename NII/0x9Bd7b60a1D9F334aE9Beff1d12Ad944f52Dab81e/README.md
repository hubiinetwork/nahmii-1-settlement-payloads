# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9Bd7b60a1D9F334aE9Beff1d12Ad944f52Dab81e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000000000000000000000000000004b4fff421c5ef3fe65bdc0ef271564ddba6f9afa1ab6ba8b3cd86fa76ca292c43b83580bba58729273ee22312c174a5f95f57f207e1aaf13c1f17c7759854c9e6424dbba15c260ce0ad4503da7c0e8fa3b49e4e1ab85a4f4f6b7401c5441f7ab3a29f5d3f8b7178b000000000000000000000000000000000000000000000000000000000000001b7641e33ac6558605cea5cdfa6e44eaa4bf45a9c70559148cf772142fb30e879d02aff7b9b8b55bb486ffd5cc7d93e6e20b20132eed5ad30f6f2485aa49a6e0cf168ddae9b2af1be4bf6a2a04d54ee814fbb7743a64a910c291f806b1355bf2a0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000dd40dc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000019ef1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000013dfa27e9c82122b493b0000000000000000000000000000000000000000000013dfede1e37212688ac700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001347ade3de4d8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000057afd02e836324ff8b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5459774e6d45795953316c4d544e694c54566a596d4d74596a6b774e69316a4d6d4d304e5759775a44557a5a57456966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000009bd7b60a1d9f334ae9beff1d12ad944f52dab81e0000000000000000000000000000000000000000000000004b4fff421c5ef3fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x65bdc0ef271564ddba6f9afa1ab6ba8b3cd86fa76ca292c43b83580bba587292",
      "signature": {
        "s": "0x0ad4503da7c0e8fa3b49e4e1ab85a4f4f6b7401c5441f7ab3a29f5d3f8b7178b",
        "r": "0x73ee22312c174a5f95f57f207e1aaf13c1f17c7759854c9e6424dbba15c260ce",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7641e33ac6558605cea5cdfa6e44eaa4bf45a9c70559148cf772142fb30e879d",
      "signature": {
        "s": "0x168ddae9b2af1be4bf6a2a04d54ee814fbb7743a64a910c291f806b1355bf2a0",
        "r": "0x02aff7b9b8b55bb486ffd5cc7d93e6e20b20132eed5ad30f6f2485aa49a6e0cf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5426836735413646334",
    "total": "5426836735413646334"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5426836735413646334",
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
            "amount": "25880566580901810534579"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5426836735413646"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZTYwNmEyYS1lMTNiLTVjYmMtYjkwNi1jMmM0NWYwZDUzZWEifQ==",
    "nonce": 106225,
    "balances": {
      "current": "93850296071124163447099",
      "previous": "93855728334696312507079"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9bd7b60a1d9f334ae9beff1d12ad944f52dab81e",
    "nonce": 1,
    "balances": {
      "current": "5426836735413646334",
      "previous": "0"
    }
  },
  "blockNumber": "14500060",
  "created": "2022-04-01T11:26:38.290Z",
  "updated": "2022-04-01T11:26:38.466Z",
  "id": "6246e16ebbd75600116cff3e"
}
```
* *stageAmount*: `5426836735413646334`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000000000000000000000000000004b4fff421c5ef3fe65bdc0ef271564ddba6f9afa1ab6ba8b3cd86fa76ca292c43b83580bba58729273ee22312c174a5f95f57f207e1aaf13c1f17c7759854c9e6424dbba15c260ce0ad4503da7c0e8fa3b49e4e1ab85a4f4f6b7401c5441f7ab3a29f5d3f8b7178b000000000000000000000000000000000000000000000000000000000000001b7641e33ac6558605cea5cdfa6e44eaa4bf45a9c70559148cf772142fb30e879d02aff7b9b8b55bb486ffd5cc7d93e6e20b20132eed5ad30f6f2485aa49a6e0cf168ddae9b2af1be4bf6a2a04d54ee814fbb7743a64a910c291f806b1355bf2a0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000dd40dc00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000019ef1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000013dfa27e9c82122b493b0000000000000000000000000000000000000000000013dfede1e37212688ac700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001347ade3de4d8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000057afd02e836324ff8b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a5459774e6d45795953316c4d544e694c54566a596d4d74596a6b774e69316a4d6d4d304e5759775a44557a5a57456966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000009bd7b60a1d9f334ae9beff1d12ad944f52dab81e0000000000000000000000000000000000000000000000004b4fff421c5ef3fe000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x65bdc0ef271564ddba6f9afa1ab6ba8b3cd86fa76ca292c43b83580bba587292",
      "signature": {
        "s": "0x0ad4503da7c0e8fa3b49e4e1ab85a4f4f6b7401c5441f7ab3a29f5d3f8b7178b",
        "r": "0x73ee22312c174a5f95f57f207e1aaf13c1f17c7759854c9e6424dbba15c260ce",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7641e33ac6558605cea5cdfa6e44eaa4bf45a9c70559148cf772142fb30e879d",
      "signature": {
        "s": "0x168ddae9b2af1be4bf6a2a04d54ee814fbb7743a64a910c291f806b1355bf2a0",
        "r": "0x02aff7b9b8b55bb486ffd5cc7d93e6e20b20132eed5ad30f6f2485aa49a6e0cf",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5426836735413646334",
    "total": "5426836735413646334"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5426836735413646334",
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
            "amount": "25880566580901810534579"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5426836735413646"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZTYwNmEyYS1lMTNiLTVjYmMtYjkwNi1jMmM0NWYwZDUzZWEifQ==",
    "nonce": 106225,
    "balances": {
      "current": "93850296071124163447099",
      "previous": "93855728334696312507079"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9bd7b60a1d9f334ae9beff1d12ad944f52dab81e",
    "nonce": 1,
    "balances": {
      "current": "5426836735413646334",
      "previous": "0"
    }
  },
  "blockNumber": "14500060",
  "created": "2022-04-01T11:26:38.290Z",
  "updated": "2022-04-01T11:26:38.466Z",
  "id": "6246e16ebbd75600116cff3e"
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
0x0f200f9b0000000000000000000000000000000000000000000000004b4fff421c5ef3fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5426836735413646334`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`