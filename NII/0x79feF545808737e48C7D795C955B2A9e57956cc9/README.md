# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x79feF545808737e48C7D795C955B2A9e57956cc9`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003ecf665c07cfe50cd00000000000000000000000000000000000000000000000017d39714eb3f37330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000017d39714eb3f37330000000000000000000000000000000000000000000000029c986e38df052f98b03a129cddeb84c1504faba81007ca8e558eec29a858f1a2a3141e69c0d4f8d88bfbc7f6c77d657b8046329a755cfccbe251fe72fcac4d41baa8d707ec8f3d521f32a65919c589db46741055e48a6647d070b7650de1f54ea44fe8b27abb1990000000000000000000000000000000000000000000000000000000000000001bd54bf235f90dd1ff0b7fd080be1563b51c7a9c1b6c7c586e3096329792e6e148437d874e575d12687a7b103e55c2b1e9298b413aed2d656f5dace6f72782b3cf5edaf9b3fe84e897b65f8061d6cca5e9581eaa2bc332fa8edd5572ddf5a4b0ff000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abf2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c17bcf29e449c319ee6000000000000000000000000000000000000000000009c17d4cc4ed8451db31400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000006197ebdacdcfb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47684dde0cd7a23150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e3251334f546b314f53316d5a574e6c4c5455344d546b744f446c6d4d79316d59324a6d596d597a595452694e44556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000079fef545808737e48c7d795c955b2a9e57956cc9000000000000000000000000000000000000000000000003ecf665c07cfe50cd000000000000000000000000000000000000000000000003d522ceab91bf199a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb03a129cddeb84c1504faba81007ca8e558eec29a858f1a2a3141e69c0d4f8d8",
      "signature": {
        "s": "0x1f32a65919c589db46741055e48a6647d070b7650de1f54ea44fe8b27abb1990",
        "r": "0x8bfbc7f6c77d657b8046329a755cfccbe251fe72fcac4d41baa8d707ec8f3d52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd54bf235f90dd1ff0b7fd080be1563b51c7a9c1b6c7c586e3096329792e6e148",
      "signature": {
        "s": "0x5edaf9b3fe84e897b65f8061d6cca5e9581eaa2bc332fa8edd5572ddf5a4b0ff",
        "r": "0x437d874e575d12687a7b103e55c2b1e9298b413aed2d656f5dace6f72782b3cf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1716881999060219699",
    "total": "48177378204334763928"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1716881999060219699",
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
            "amount": "27235934447546289234709"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1716881999060219"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3N2Q3OTk1OS1mZWNlLTU4MTktODlmMy1mY2JmYmYzYTRiNDUifQ==",
    "nonce": 109554,
    "balances": {
      "current": "737127061560000982916838",
      "previous": "737128780158882042196756"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x79fef545808737e48c7d795c955b2a9e57956cc9",
    "nonce": 46,
    "balances": {
      "current": "72415179135755636941",
      "previous": "70698297136695417242"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:41.920Z",
  "updated": "2022-05-04T08:48:42.005Z",
  "id": "62723de9bbd75600116d0438"
}
```
* *stageAmount*: `72415179135755636941`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000017d39714eb3f37330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000017d39714eb3f37330000000000000000000000000000000000000000000000029c986e38df052f98b03a129cddeb84c1504faba81007ca8e558eec29a858f1a2a3141e69c0d4f8d88bfbc7f6c77d657b8046329a755cfccbe251fe72fcac4d41baa8d707ec8f3d521f32a65919c589db46741055e48a6647d070b7650de1f54ea44fe8b27abb1990000000000000000000000000000000000000000000000000000000000000001bd54bf235f90dd1ff0b7fd080be1563b51c7a9c1b6c7c586e3096329792e6e148437d874e575d12687a7b103e55c2b1e9298b413aed2d656f5dace6f72782b3cf5edaf9b3fe84e897b65f8061d6cca5e9581eaa2bc332fa8edd5572ddf5a4b0ff000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abf2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c17bcf29e449c319ee6000000000000000000000000000000000000000000009c17d4cc4ed8451db31400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000006197ebdacdcfb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c47684dde0cd7a23150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e3251334f546b314f53316d5a574e6c4c5455344d546b744f446c6d4d79316d59324a6d596d597a595452694e44556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000079fef545808737e48c7d795c955b2a9e57956cc9000000000000000000000000000000000000000000000003ecf665c07cfe50cd000000000000000000000000000000000000000000000003d522ceab91bf199a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb03a129cddeb84c1504faba81007ca8e558eec29a858f1a2a3141e69c0d4f8d8",
      "signature": {
        "s": "0x1f32a65919c589db46741055e48a6647d070b7650de1f54ea44fe8b27abb1990",
        "r": "0x8bfbc7f6c77d657b8046329a755cfccbe251fe72fcac4d41baa8d707ec8f3d52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd54bf235f90dd1ff0b7fd080be1563b51c7a9c1b6c7c586e3096329792e6e148",
      "signature": {
        "s": "0x5edaf9b3fe84e897b65f8061d6cca5e9581eaa2bc332fa8edd5572ddf5a4b0ff",
        "r": "0x437d874e575d12687a7b103e55c2b1e9298b413aed2d656f5dace6f72782b3cf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1716881999060219699",
    "total": "48177378204334763928"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1716881999060219699",
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
            "amount": "27235934447546289234709"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1716881999060219"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3N2Q3OTk1OS1mZWNlLTU4MTktODlmMy1mY2JmYmYzYTRiNDUifQ==",
    "nonce": 109554,
    "balances": {
      "current": "737127061560000982916838",
      "previous": "737128780158882042196756"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x79fef545808737e48c7d795c955b2a9e57956cc9",
    "nonce": 46,
    "balances": {
      "current": "72415179135755636941",
      "previous": "70698297136695417242"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:48:41.920Z",
  "updated": "2022-05-04T08:48:42.005Z",
  "id": "62723de9bbd75600116d0438"
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
0x0f200f9b000000000000000000000000000000000000000000000003ecf665c07cfe50cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `72415179135755636941`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`