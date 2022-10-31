# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xc49937621b8CD2C99A6e47981CD365e1B258A890`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de2ab2f27793a9a00000000000000000000000000000000000000000000002664f17687da6900000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000002664f17687da6900000000000000000000000000000000000000000000000000d0b171d2de184480002d42a6c65499987e2f1b4544b9a234c2b075c91387885976da1e0b7d51dc573f7442b7c8612ee05d4d5ca5627f508e612c6a5777c62e425d7038b7e9f376d6560a7c0aabdf17e028a15561c76da37d422b07fc91141402925d9c6f023c539e29000000000000000000000000000000000000000000000000000000000000001b1a2e3d253e474b18f9be60bddffae2889a0a748853cc1bf6ecfb3330b1c8e19cc99af3a6ae384d0f402af2c003c5a381cb26abe775a4a0e5354cb6b526ab6b9874882cc2fa9c99c518733524828db0b7238a7535fcf2332504449944b0ebd3aa000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1bab300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000035000000000000000000000000c49937621b8cd2c99a6e47981cd365e1b258a8900000000000000000000000000000000000000000000000000de2ab2f27793a9a0000000000000000000000000000000000000000000000267ca85756600dda9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000009d4359f5e2ba0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000356ce9f0599fd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d5759344f4455314e7930305a44566b4c54526d595449745957526d596930784e7a55334d6d51325a546469596d596966513d3d0000000000000000000000000000000000000000000000000000000000000031000000000000000000000000e2e09f07b65bcae3944e7d2830eb1cda6ce03b9d0000000000000000000000000000000000000000000002bc60937ff0cf63d507000000000000000000000000000000000000000000000295fba20968f4fad50700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x2d42a6c65499987e2f1b4544b9a234c2b075c91387885976da1e0b7d51dc573f",
      "signature": {
        "s": "0x0a7c0aabdf17e028a15561c76da37d422b07fc91141402925d9c6f023c539e29",
        "r": "0x7442b7c8612ee05d4d5ca5627f508e612c6a5777c62e425d7038b7e9f376d656",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1a2e3d253e474b18f9be60bddffae2889a0a748853cc1bf6ecfb3330b1c8e19c",
      "signature": {
        "s": "0x74882cc2fa9c99c518733524828db0b7238a7535fcf2332504449944b0ebd3aa",
        "r": "0xc99af3a6ae384d0f402af2c003c5a381cb26abe775a4a0e5354cb6b526ab6b98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "708250000000000000000",
    "total": "3849709000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "708250000000000000000",
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
            "amount": "3849709000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "708250000000000000"
      }
    },
    "wallet": "0xc49937621b8cd2c99a6e47981cd365e1b258a890",
    "data": "eyJyZWYiOiI0MWY4ODU1Ny00ZDVkLTRmYTItYWRmYi0xNzU3MmQ2ZTdiYmYifQ==",
    "nonce": 53,
    "balances": {
      "current": "1000550286243740314",
      "previous": "709958800286243740314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2e09f07b65bcae3944e7d2830eb1cda6ce03b9d",
    "nonce": 49,
    "balances": {
      "current": "12919679898118151984391",
      "previous": "12211429898118151984391"
    }
  },
  "blockNumber": "14793395",
  "created": "2022-05-17T15:52:48.545Z",
  "updated": "2022-05-17T15:52:48.695Z",
  "id": "6283c4d0bbd75600116d088a"
}
```
* *stageAmount*: `1000550286243740314`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000002664f17687da6900000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000002664f17687da6900000000000000000000000000000000000000000000000000d0b171d2de184480002d42a6c65499987e2f1b4544b9a234c2b075c91387885976da1e0b7d51dc573f7442b7c8612ee05d4d5ca5627f508e612c6a5777c62e425d7038b7e9f376d6560a7c0aabdf17e028a15561c76da37d422b07fc91141402925d9c6f023c539e29000000000000000000000000000000000000000000000000000000000000001b1a2e3d253e474b18f9be60bddffae2889a0a748853cc1bf6ecfb3330b1c8e19cc99af3a6ae384d0f402af2c003c5a381cb26abe775a4a0e5354cb6b526ab6b9874882cc2fa9c99c518733524828db0b7238a7535fcf2332504449944b0ebd3aa000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1bab300000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000000035000000000000000000000000c49937621b8cd2c99a6e47981cd365e1b258a8900000000000000000000000000000000000000000000000000de2ab2f27793a9a0000000000000000000000000000000000000000000000267ca85756600dda9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000009d4359f5e2ba0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000356ce9f0599fd0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d5759344f4455314e7930305a44566b4c54526d595449745957526d596930784e7a55334d6d51325a546469596d596966513d3d0000000000000000000000000000000000000000000000000000000000000031000000000000000000000000e2e09f07b65bcae3944e7d2830eb1cda6ce03b9d0000000000000000000000000000000000000000000002bc60937ff0cf63d507000000000000000000000000000000000000000000000295fba20968f4fad50700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x2d42a6c65499987e2f1b4544b9a234c2b075c91387885976da1e0b7d51dc573f",
      "signature": {
        "s": "0x0a7c0aabdf17e028a15561c76da37d422b07fc91141402925d9c6f023c539e29",
        "r": "0x7442b7c8612ee05d4d5ca5627f508e612c6a5777c62e425d7038b7e9f376d656",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1a2e3d253e474b18f9be60bddffae2889a0a748853cc1bf6ecfb3330b1c8e19c",
      "signature": {
        "s": "0x74882cc2fa9c99c518733524828db0b7238a7535fcf2332504449944b0ebd3aa",
        "r": "0xc99af3a6ae384d0f402af2c003c5a381cb26abe775a4a0e5354cb6b526ab6b98",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "708250000000000000000",
    "total": "3849709000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "708250000000000000000",
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
            "amount": "3849709000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "708250000000000000"
      }
    },
    "wallet": "0xc49937621b8cd2c99a6e47981cd365e1b258a890",
    "data": "eyJyZWYiOiI0MWY4ODU1Ny00ZDVkLTRmYTItYWRmYi0xNzU3MmQ2ZTdiYmYifQ==",
    "nonce": 53,
    "balances": {
      "current": "1000550286243740314",
      "previous": "709958800286243740314"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2e09f07b65bcae3944e7d2830eb1cda6ce03b9d",
    "nonce": 49,
    "balances": {
      "current": "12919679898118151984391",
      "previous": "12211429898118151984391"
    }
  },
  "blockNumber": "14793395",
  "created": "2022-05-17T15:52:48.545Z",
  "updated": "2022-05-17T15:52:48.695Z",
  "id": "6283c4d0bbd75600116d088a"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000de2ab2f27793a9a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1000550286243740314`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`