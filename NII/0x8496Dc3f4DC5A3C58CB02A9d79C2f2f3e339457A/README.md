# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8496Dc3f4DC5A3C58CB02A9d79C2f2f3e339457A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000264f054457915c2110000000000000000000000000000000000000000000000000000000171400f850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000171400f8500000000000000000000000000000000000000000000000000000021a999b7ea4ef8aa2e10f0c1464108ad63a640f812238746a129a43c1ca30ad5a18c8a4762550cc6f61d0d0eedd27a955cac84e1fb1e62d912f501682f2cd363eb31c1334d2a19258f0565a39f820d03052f661fcb8319e4967d591e728b102dec1f21f6bd000000000000000000000000000000000000000000000000000000000000001b3841e1f146a80fa206bfb3d855a5e499b16f8528985387832a8c29ca1a796513c3308f9238c6be7e3375a5880bc3d49a7c850ec3ba1507aee12549f1eaab9cf5398e52d9aa1ce76e8755ac1e3dab33dfd34681b0587b4bec7a7821f4d37186bc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b02b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9bb213db7c82387dde000000000000000000000000000000000000000000004f9bb213db7df3d7149100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005e872e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d806009d1d1a39ee070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593259784d7a526d4d5330794e47597a4c54566c596d4d74596a646c4e6930794d4455314d6d56684e5467324d54516966513d3d00000000000000000000000000000000000000000000000000000000000000220000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a00000000000000000000000000000000000000000000000264f054457915c21100000000000000000000000000000000000000000000000264f0544407d5b28c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4ef8aa2e10f0c1464108ad63a640f812238746a129a43c1ca30ad5a18c8a4762",
      "signature": {
        "s": "0x2a19258f0565a39f820d03052f661fcb8319e4967d591e728b102dec1f21f6bd",
        "r": "0x550cc6f61d0d0eedd27a955cac84e1fb1e62d912f501682f2cd363eb31c1334d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3841e1f146a80fa206bfb3d855a5e499b16f8528985387832a8c29ca1a796513",
      "signature": {
        "s": "0x398e52d9aa1ce76e8755ac1e3dab33dfd34681b0587b4bec7a7821f4d37186bc",
        "r": "0xc3308f9238c6be7e3375a5880bc3d49a7c850ec3ba1507aee12549f1eaab9cf5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6194990981",
    "total": "144579344362"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6194990981",
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
            "amount": "27596761652582036401671"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6194990"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Y2YxMzRmMS0yNGYzLTVlYmMtYjdlNi0yMDU1MmVhNTg2MTQifQ==",
    "nonce": 110635,
    "balances": {
      "current": "375939029319218068225502",
      "previous": "375939029319224269411473"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 34,
    "balances": {
      "current": "44166894202983399953",
      "previous": "44166894196788408972"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:16.596Z",
  "updated": "2022-05-04T08:54:16.682Z",
  "id": "62723f383592fd001130b518"
}
```
* *stageAmount*: `44166894202983399953`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000171400f850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000171400f8500000000000000000000000000000000000000000000000000000021a999b7ea4ef8aa2e10f0c1464108ad63a640f812238746a129a43c1ca30ad5a18c8a4762550cc6f61d0d0eedd27a955cac84e1fb1e62d912f501682f2cd363eb31c1334d2a19258f0565a39f820d03052f661fcb8319e4967d591e728b102dec1f21f6bd000000000000000000000000000000000000000000000000000000000000001b3841e1f146a80fa206bfb3d855a5e499b16f8528985387832a8c29ca1a796513c3308f9238c6be7e3375a5880bc3d49a7c850ec3ba1507aee12549f1eaab9cf5398e52d9aa1ce76e8755ac1e3dab33dfd34681b0587b4bec7a7821f4d37186bc000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b02b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9bb213db7c82387dde000000000000000000000000000000000000000000004f9bb213db7df3d7149100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000005e872e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d806009d1d1a39ee070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934593259784d7a526d4d5330794e47597a4c54566c596d4d74596a646c4e6930794d4455314d6d56684e5467324d54516966513d3d00000000000000000000000000000000000000000000000000000000000000220000000000000000000000008496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a00000000000000000000000000000000000000000000000264f054457915c21100000000000000000000000000000000000000000000000264f0544407d5b28c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4ef8aa2e10f0c1464108ad63a640f812238746a129a43c1ca30ad5a18c8a4762",
      "signature": {
        "s": "0x2a19258f0565a39f820d03052f661fcb8319e4967d591e728b102dec1f21f6bd",
        "r": "0x550cc6f61d0d0eedd27a955cac84e1fb1e62d912f501682f2cd363eb31c1334d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3841e1f146a80fa206bfb3d855a5e499b16f8528985387832a8c29ca1a796513",
      "signature": {
        "s": "0x398e52d9aa1ce76e8755ac1e3dab33dfd34681b0587b4bec7a7821f4d37186bc",
        "r": "0xc3308f9238c6be7e3375a5880bc3d49a7c850ec3ba1507aee12549f1eaab9cf5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6194990981",
    "total": "144579344362"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6194990981",
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
            "amount": "27596761652582036401671"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6194990"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Y2YxMzRmMS0yNGYzLTVlYmMtYjdlNi0yMDU1MmVhNTg2MTQifQ==",
    "nonce": 110635,
    "balances": {
      "current": "375939029319218068225502",
      "previous": "375939029319224269411473"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8496dc3f4dc5a3c58cb02a9d79c2f2f3e339457a",
    "nonce": 34,
    "balances": {
      "current": "44166894202983399953",
      "previous": "44166894196788408972"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:16.596Z",
  "updated": "2022-05-04T08:54:16.682Z",
  "id": "62723f383592fd001130b518"
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
0x0f200f9b00000000000000000000000000000000000000000000000264f054457915c2110000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `44166894202983399953`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`