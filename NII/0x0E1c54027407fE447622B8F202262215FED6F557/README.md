# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0E1c54027407fE447622B8F202262215FED6F557`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000000000000000000000000000000027208000b3ecd843f80802dffca14919e427f11df8dc585c9b9d86db8d735ba78cafbbfdfd5f491b94ad5b23605ec95bbd6bcaac08d08e512507246763c245d06229dfd129239b33bcbfd8b05d7f4a42340b18f51ba00df5c35f0a03e0f2f397b9e92b088ba988000000000000000000000000000000000000000000000000000000000000001c37594e8abaf2350b6b9496e2bf9d2c281ff60f20322b9cad35303626381c77d442e74ec6d3f51b436f0b887fbe0af133ce1ceaccb4dad6f54c9c287a01909d54211231a9f473141a2f2e03c1b2fd21ffd50f3b0e96f3a0575796dce624c07e94000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000adaa0b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000e7a8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000234202ce86a688ccae5200000000000000000000000000000000000000000000234202f5b12ac2d8d99b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000a0439583e710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024ab6ef9dcf5ed6f2950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f446c6c5a4442684e7930334d4441324c5455784e7a45744f44466c4d5330314e544a6859546c6a4d7a51784f47516966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1c54027407fe447622b8f202262215fed6f5570000000000000000000000000000000000000000000000000027208000b3ecd8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x43f80802dffca14919e427f11df8dc585c9b9d86db8d735ba78cafbbfdfd5f49",
      "signature": {
        "s": "0x33bcbfd8b05d7f4a42340b18f51ba00df5c35f0a03e0f2f397b9e92b088ba988",
        "r": "0x1b94ad5b23605ec95bbd6bcaac08d08e512507246763c245d06229dfd129239b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x37594e8abaf2350b6b9496e2bf9d2c281ff60f20322b9cad35303626381c77d4",
      "signature": {
        "s": "0x211231a9f473141a2f2e03c1b2fd21ffd50f3b0e96f3a0575796dce624c07e94",
        "r": "0x42e74ec6d3f51b436f0b887fbe0af133ce1ceaccb4dad6f54c9c287a01909d54",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11013258231409880",
    "total": "11013258231409880"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11013258231409880",
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
            "amount": "10822973955342108914325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11013258231409"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkODllZDBhNy03MDA2LTUxNzEtODFlMS01NTJhYTljMzQxOGQifQ==",
    "nonce": 59304,
    "balances": {
      "current": "166500514256385508945490",
      "previous": "166500525280656998586779"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e1c54027407fe447622b8f202262215fed6f557",
    "nonce": 1,
    "balances": {
      "current": "11013258231409880",
      "previous": "0"
    }
  },
  "blockNumber": "11381259",
  "created": "2020-12-03T18:25:42.937Z",
  "updated": "2020-12-03T18:25:43.039Z",
  "id": "5fc92da65ca34d0011dac465"
}
```
* *stageAmount*: `11013258231409880`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000000000000000000000000000000027208000b3ecd843f80802dffca14919e427f11df8dc585c9b9d86db8d735ba78cafbbfdfd5f491b94ad5b23605ec95bbd6bcaac08d08e512507246763c245d06229dfd129239b33bcbfd8b05d7f4a42340b18f51ba00df5c35f0a03e0f2f397b9e92b088ba988000000000000000000000000000000000000000000000000000000000000001c37594e8abaf2350b6b9496e2bf9d2c281ff60f20322b9cad35303626381c77d442e74ec6d3f51b436f0b887fbe0af133ce1ceaccb4dad6f54c9c287a01909d54211231a9f473141a2f2e03c1b2fd21ffd50f3b0e96f3a0575796dce624c07e94000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000adaa0b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000e7a8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000234202ce86a688ccae5200000000000000000000000000000000000000000000234202f5b12ac2d8d99b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000a0439583e710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024ab6ef9dcf5ed6f2950000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f446c6c5a4442684e7930334d4441324c5455784e7a45744f44466c4d5330314e544a6859546c6a4d7a51784f47516966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1c54027407fe447622b8f202262215fed6f5570000000000000000000000000000000000000000000000000027208000b3ecd8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x43f80802dffca14919e427f11df8dc585c9b9d86db8d735ba78cafbbfdfd5f49",
      "signature": {
        "s": "0x33bcbfd8b05d7f4a42340b18f51ba00df5c35f0a03e0f2f397b9e92b088ba988",
        "r": "0x1b94ad5b23605ec95bbd6bcaac08d08e512507246763c245d06229dfd129239b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x37594e8abaf2350b6b9496e2bf9d2c281ff60f20322b9cad35303626381c77d4",
      "signature": {
        "s": "0x211231a9f473141a2f2e03c1b2fd21ffd50f3b0e96f3a0575796dce624c07e94",
        "r": "0x42e74ec6d3f51b436f0b887fbe0af133ce1ceaccb4dad6f54c9c287a01909d54",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11013258231409880",
    "total": "11013258231409880"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11013258231409880",
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
            "amount": "10822973955342108914325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11013258231409"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkODllZDBhNy03MDA2LTUxNzEtODFlMS01NTJhYTljMzQxOGQifQ==",
    "nonce": 59304,
    "balances": {
      "current": "166500514256385508945490",
      "previous": "166500525280656998586779"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e1c54027407fe447622b8f202262215fed6f557",
    "nonce": 1,
    "balances": {
      "current": "11013258231409880",
      "previous": "0"
    }
  },
  "blockNumber": "11381259",
  "created": "2020-12-03T18:25:42.937Z",
  "updated": "2020-12-03T18:25:43.039Z",
  "id": "5fc92da65ca34d0011dac465"
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
0x0f200f9b0000000000000000000000000000000000000000000000000027208000b3ecd80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `11013258231409880`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`