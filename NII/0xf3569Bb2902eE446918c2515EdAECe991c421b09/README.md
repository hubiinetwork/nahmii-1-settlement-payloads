# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf3569Bb2902eE446918c2515EdAECe991c421b09`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000130bb868d1b9bb537600000000000000000000000000000000000000000000000073990a7967cf063f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073990a7967cf063f00000000000000000000000000000000000000000000000cabc9804b91ff1d54e1e90687c6e5f32f03cec0bc3a307b3af8d141c0222bb99686f1a682ac66bf90c26e4e65db88af01a79a408c2730fcb08d3051a16824ce1d1c9f46014ee892db645ce577f5ffe3199af09c02ec56939a0a58a6e1d1c6129e39262545142ee2db000000000000000000000000000000000000000000000000000000000000001cc767d3a645ce26e36772db27eefc0c3e46204a00d89077db74001c91be9d38953ee5f99b9cb9812a67051ea609e7a83a7407fccba897e73e862929b2fdc0b9ca55aaba0ab26db534d92a14b1d022f91f280377bb985a1cdb012201eba54d86ed000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae05000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963cb9dbfc8dbd37e45600000000000000000000000000000000000000000000963d2d929ed8ac8e090d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d97d187871e780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f5e1faf0547a206c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6d51314f5467354d5331694e5445354c5455314f4445744f5445774e5330345a5445314e6d4d344d544d335a6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f3569bb2902ee446918c2515edaece991c421b090000000000000000000000000000000000000000000000130bb868d1b9bb5376000000000000000000000000000000000000000000000012981f5e5851ec4d3700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1e90687c6e5f32f03cec0bc3a307b3af8d141c0222bb99686f1a682ac66bf90",
      "signature": {
        "s": "0x645ce577f5ffe3199af09c02ec56939a0a58a6e1d1c6129e39262545142ee2db",
        "r": "0xc26e4e65db88af01a79a408c2730fcb08d3051a16824ce1d1c9f46014ee892db",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc767d3a645ce26e36772db27eefc0c3e46204a00d89077db74001c91be9d3895",
      "signature": {
        "s": "0x55aaba0ab26db534d92a14b1d022f91f280377bb985a1cdb012201eba54d86ed",
        "r": "0x3ee5f99b9cb9812a67051ea609e7a83a7407fccba897e73e862929b2fdc0b9ca",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8329700502347384383",
    "total": "233739494997379456340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8329700502347384383",
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
            "amount": "27263558715188176363628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8329700502347384"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMmQ1OTg5MS1iNTE5LTU1ODEtOTEwNS04ZTE1NmM4MTM3ZmYifQ==",
    "nonce": 110085,
    "balances": {
      "current": "709475169650471966598230",
      "previous": "709483507680674816329997"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf3569bb2902ee446918c2515edaece991c421b09",
    "nonce": 46,
    "balances": {
      "current": "351332677580586963830",
      "previous": "343002977078239579447"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:28.442Z",
  "updated": "2022-05-04T08:51:28.533Z",
  "id": "62723e90bbd75600116d04f1"
}
```
* *stageAmount*: `351332677580586963830`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000073990a7967cf063f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073990a7967cf063f00000000000000000000000000000000000000000000000cabc9804b91ff1d54e1e90687c6e5f32f03cec0bc3a307b3af8d141c0222bb99686f1a682ac66bf90c26e4e65db88af01a79a408c2730fcb08d3051a16824ce1d1c9f46014ee892db645ce577f5ffe3199af09c02ec56939a0a58a6e1d1c6129e39262545142ee2db000000000000000000000000000000000000000000000000000000000000001cc767d3a645ce26e36772db27eefc0c3e46204a00d89077db74001c91be9d38953ee5f99b9cb9812a67051ea609e7a83a7407fccba897e73e862929b2fdc0b9ca55aaba0ab26db534d92a14b1d022f91f280377bb985a1cdb012201eba54d86ed000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae05000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963cb9dbfc8dbd37e45600000000000000000000000000000000000000000000963d2d929ed8ac8e090d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d97d187871e780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f5e1faf0547a206c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6d51314f5467354d5331694e5445354c5455314f4445744f5445774e5330345a5445314e6d4d344d544d335a6d596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f3569bb2902ee446918c2515edaece991c421b090000000000000000000000000000000000000000000000130bb868d1b9bb5376000000000000000000000000000000000000000000000012981f5e5851ec4d3700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe1e90687c6e5f32f03cec0bc3a307b3af8d141c0222bb99686f1a682ac66bf90",
      "signature": {
        "s": "0x645ce577f5ffe3199af09c02ec56939a0a58a6e1d1c6129e39262545142ee2db",
        "r": "0xc26e4e65db88af01a79a408c2730fcb08d3051a16824ce1d1c9f46014ee892db",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc767d3a645ce26e36772db27eefc0c3e46204a00d89077db74001c91be9d3895",
      "signature": {
        "s": "0x55aaba0ab26db534d92a14b1d022f91f280377bb985a1cdb012201eba54d86ed",
        "r": "0x3ee5f99b9cb9812a67051ea609e7a83a7407fccba897e73e862929b2fdc0b9ca",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8329700502347384383",
    "total": "233739494997379456340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8329700502347384383",
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
            "amount": "27263558715188176363628"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8329700502347384"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMmQ1OTg5MS1iNTE5LTU1ODEtOTEwNS04ZTE1NmM4MTM3ZmYifQ==",
    "nonce": 110085,
    "balances": {
      "current": "709475169650471966598230",
      "previous": "709483507680674816329997"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf3569bb2902ee446918c2515edaece991c421b09",
    "nonce": 46,
    "balances": {
      "current": "351332677580586963830",
      "previous": "343002977078239579447"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:28.442Z",
  "updated": "2022-05-04T08:51:28.533Z",
  "id": "62723e90bbd75600116d04f1"
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
0x0f200f9b0000000000000000000000000000000000000000000000130bb868d1b9bb53760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `351332677580586963830`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`