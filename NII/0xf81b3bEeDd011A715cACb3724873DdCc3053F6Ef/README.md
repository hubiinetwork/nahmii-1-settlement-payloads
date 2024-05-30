# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf81b3bEeDd011A715cACb3724873DdCc3053F6Ef`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000017dbcf1ce0e500000000000000000000000000000000000000000000000000000090cf2aabcd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000090cf2aabcd00000000000000000000000000000000000000000000000000000fdf7cfb2d08648c34487f3515a0f68637f671035b06818fb7d49aa65c1c6ad6b7ad0e53e8b70e0b1f8f6a05a16f649accc49bc2c89ea839b246154f0d153630accaa44f78f8506232dc035dda710366d5b6031e95b21f339c96ee78637939328dbff589be34000000000000000000000000000000000000000000000000000000000000001c3f271675611451d89b0b292670d1b90f84bfd72a5f8a63d35365bbd7b9eedbe5e23a37360b55b5b38f907f7b3b789ecf444f10c1f02790761da0bd18b765420600f71ce8a69cc1c7671cb5a73361afaed5915ad6ebce466c64ec1a60676b76b2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a34cc2765987c2a88b9000000000000000000000000000000000000000000009a34cc27662970676c8000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000251237fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f2073e59af9646590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a566d4e446c6c4f4330334d54686b4c54557a4d6a6b7459574932597930314d5445304e544d7a4f474a6d4e32516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f81b3beedd011a715cacb3724873ddcc3053f6ef000000000000000000000000000000000000000000000000000017dbcf1ce0e50000000000000000000000000000000000000000000000000000174afff2351800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x648c34487f3515a0f68637f671035b06818fb7d49aa65c1c6ad6b7ad0e53e8b7",
      "signature": {
        "s": "0x506232dc035dda710366d5b6031e95b21f339c96ee78637939328dbff589be34",
        "r": "0x0e0b1f8f6a05a16f649accc49bc2c89ea839b246154f0d153630accaa44f78f8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f271675611451d89b0b292670d1b90f84bfd72a5f8a63d35365bbd7b9eedbe5",
      "signature": {
        "s": "0x00f71ce8a69cc1c7671cb5a73361afaed5915ad6ebce466c64ec1a60676b76b2",
        "r": "0xe23a37360b55b5b38f907f7b3b789ecf444f10c1f02790761da0bd18b7654206",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "621950970829",
    "total": "17452548959496"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "621950970829",
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
            "amount": "27244834229432232592985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "621950970"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjVmNDllOC03MThkLTUzMjktYWI2Yy01MTE0NTMzOGJmN2QifQ==",
    "nonce": 109709,
    "balances": {
      "current": "728218379892171681204409",
      "previous": "728218379892794254126208"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf81b3beedd011a715cacb3724873ddcc3053f6ef",
    "nonce": 45,
    "balances": {
      "current": "26232840052965",
      "previous": "25610889082136"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:31.280Z",
  "updated": "2022-05-04T08:49:31.401Z",
  "id": "62723e1b3592fd001130b3ea"
}
```
* *stageAmount*: `26232840052965`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000090cf2aabcd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000090cf2aabcd00000000000000000000000000000000000000000000000000000fdf7cfb2d08648c34487f3515a0f68637f671035b06818fb7d49aa65c1c6ad6b7ad0e53e8b70e0b1f8f6a05a16f649accc49bc2c89ea839b246154f0d153630accaa44f78f8506232dc035dda710366d5b6031e95b21f339c96ee78637939328dbff589be34000000000000000000000000000000000000000000000000000000000000001c3f271675611451d89b0b292670d1b90f84bfd72a5f8a63d35365bbd7b9eedbe5e23a37360b55b5b38f907f7b3b789ecf444f10c1f02790761da0bd18b765420600f71ce8a69cc1c7671cb5a73361afaed5915ad6ebce466c64ec1a60676b76b2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074bc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a34cc2765987c2a88b9000000000000000000000000000000000000000000009a34cc27662970676c8000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000251237fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4f2073e59af9646590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a566d4e446c6c4f4330334d54686b4c54557a4d6a6b7459574932597930314d5445304e544d7a4f474a6d4e32516966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000f81b3beedd011a715cacb3724873ddcc3053f6ef000000000000000000000000000000000000000000000000000017dbcf1ce0e50000000000000000000000000000000000000000000000000000174afff2351800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x648c34487f3515a0f68637f671035b06818fb7d49aa65c1c6ad6b7ad0e53e8b7",
      "signature": {
        "s": "0x506232dc035dda710366d5b6031e95b21f339c96ee78637939328dbff589be34",
        "r": "0x0e0b1f8f6a05a16f649accc49bc2c89ea839b246154f0d153630accaa44f78f8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3f271675611451d89b0b292670d1b90f84bfd72a5f8a63d35365bbd7b9eedbe5",
      "signature": {
        "s": "0x00f71ce8a69cc1c7671cb5a73361afaed5915ad6ebce466c64ec1a60676b76b2",
        "r": "0xe23a37360b55b5b38f907f7b3b789ecf444f10c1f02790761da0bd18b7654206",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "621950970829",
    "total": "17452548959496"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "621950970829",
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
            "amount": "27244834229432232592985"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "621950970"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjVmNDllOC03MThkLTUzMjktYWI2Yy01MTE0NTMzOGJmN2QifQ==",
    "nonce": 109709,
    "balances": {
      "current": "728218379892171681204409",
      "previous": "728218379892794254126208"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf81b3beedd011a715cacb3724873ddcc3053f6ef",
    "nonce": 45,
    "balances": {
      "current": "26232840052965",
      "previous": "25610889082136"
    }
  },
  "blockNumber": "14709948",
  "created": "2022-05-04T08:49:31.280Z",
  "updated": "2022-05-04T08:49:31.401Z",
  "id": "62723e1b3592fd001130b3ea"
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
0x0f200f9b000000000000000000000000000000000000000000000000000017dbcf1ce0e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `26232840052965`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`