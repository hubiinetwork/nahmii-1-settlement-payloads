# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF04766312e75Be211063fAe0070695Da8B41C4bb`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000005fd7b4d4f6fc5fc5a2000000000000000000000000000000000000000000000002a667cc241d389c5d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002a667cc241d389c5d00000000000000000000000000000000000000000000004a5cb77eff808e8d775d0e6f5c9c011a6f6e9f87ca15b33e682d972005c12726b5e95c55bbbff2d7b4aba9f6a55e8326abe22cda16cc47307410563d52f6b94bf951b98d1c9e989939527dbc2c717bd6ac524c1d645c1e01f50783ff146fc39ee02e0e45c4078f8db6000000000000000000000000000000000000000000000000000000000000001b9efbb32d1d393f29ced6018206bf0c29f8cb4e0fc43a9ae3b2bbac506d4268a6bb88afde0e749999be0070fd65f5a961654a07b8e0d4f4bd557261249d23c5f37b4e19db50b2a386cc65f00c9858698c61b19f8c7ee44816fca9c0579a02f249000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b087000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004cf05eb62fcf6d824cbb000000000000000000000000000000000000000000004cf305cba7ee75415dfc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000adabfaea8674e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8b4c24e429d3023150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e3251785a5451784e6930345a5467334c5455784e4459744f4451325953316d5a445a69595452695a5464684e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f04766312e75be211063fae0070695da8b41c4bb00000000000000000000000000000000000000000000005fd7b4d4f6fc5fc5a200000000000000000000000000000000000000000000005d314d08d2df27294500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d0e6f5c9c011a6f6e9f87ca15b33e682d972005c12726b5e95c55bbbff2d7b4",
      "signature": {
        "s": "0x527dbc2c717bd6ac524c1d645c1e01f50783ff146fc39ee02e0e45c4078f8db6",
        "r": "0xaba9f6a55e8326abe22cda16cc47307410563d52f6b94bf951b98d1c9e989939",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9efbb32d1d393f29ced6018206bf0c29f8cb4e0fc43a9ae3b2bbac506d4268a6",
      "signature": {
        "s": "0x7b4e19db50b2a386cc65f00c9858698c61b19f8c7ee44816fca9c0579a02f249",
        "r": "0xbb88afde0e749999be0070fd65f5a961654a07b8e0d4f4bd557261249d23c5f3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "48884265135797476445",
    "total": "1371740009662572825975"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48884265135797476445",
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
            "amount": "27609354193389810098965"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48884265135797476"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiN2QxZTQxNi04ZTg3LTUxNDYtODQ2YS1mZDZiYTRiZTdhNDcifQ==",
    "nonce": 110727,
    "balances": {
      "current": "363333895970636597185723",
      "previous": "363382829120037530459644"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf04766312e75be211063fae0070695da8b41c4bb",
    "nonce": 46,
    "balances": {
      "current": "1767983969373631006114",
      "previous": "1719099704237833529669"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:43.407Z",
  "updated": "2022-05-04T08:54:43.479Z",
  "id": "62723f537832e20011830c13"
}
```
* *stageAmount*: `1767983969373631006114`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000002a667cc241d389c5d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000002a667cc241d389c5d00000000000000000000000000000000000000000000004a5cb77eff808e8d775d0e6f5c9c011a6f6e9f87ca15b33e682d972005c12726b5e95c55bbbff2d7b4aba9f6a55e8326abe22cda16cc47307410563d52f6b94bf951b98d1c9e989939527dbc2c717bd6ac524c1d645c1e01f50783ff146fc39ee02e0e45c4078f8db6000000000000000000000000000000000000000000000000000000000000001b9efbb32d1d393f29ced6018206bf0c29f8cb4e0fc43a9ae3b2bbac506d4268a6bb88afde0e749999be0070fd65f5a961654a07b8e0d4f4bd557261249d23c5f37b4e19db50b2a386cc65f00c9858698c61b19f8c7ee44816fca9c0579a02f249000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b087000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004cf05eb62fcf6d824cbb000000000000000000000000000000000000000000004cf305cba7ee75415dfc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000adabfaea8674e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d8b4c24e429d3023150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e3251785a5451784e6930345a5467334c5455784e4459744f4451325953316d5a445a69595452695a5464684e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f04766312e75be211063fae0070695da8b41c4bb00000000000000000000000000000000000000000000005fd7b4d4f6fc5fc5a200000000000000000000000000000000000000000000005d314d08d2df27294500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5d0e6f5c9c011a6f6e9f87ca15b33e682d972005c12726b5e95c55bbbff2d7b4",
      "signature": {
        "s": "0x527dbc2c717bd6ac524c1d645c1e01f50783ff146fc39ee02e0e45c4078f8db6",
        "r": "0xaba9f6a55e8326abe22cda16cc47307410563d52f6b94bf951b98d1c9e989939",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9efbb32d1d393f29ced6018206bf0c29f8cb4e0fc43a9ae3b2bbac506d4268a6",
      "signature": {
        "s": "0x7b4e19db50b2a386cc65f00c9858698c61b19f8c7ee44816fca9c0579a02f249",
        "r": "0xbb88afde0e749999be0070fd65f5a961654a07b8e0d4f4bd557261249d23c5f3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "48884265135797476445",
    "total": "1371740009662572825975"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48884265135797476445",
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
            "amount": "27609354193389810098965"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48884265135797476"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiN2QxZTQxNi04ZTg3LTUxNDYtODQ2YS1mZDZiYTRiZTdhNDcifQ==",
    "nonce": 110727,
    "balances": {
      "current": "363333895970636597185723",
      "previous": "363382829120037530459644"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf04766312e75be211063fae0070695da8b41c4bb",
    "nonce": 46,
    "balances": {
      "current": "1767983969373631006114",
      "previous": "1719099704237833529669"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:43.407Z",
  "updated": "2022-05-04T08:54:43.479Z",
  "id": "62723f537832e20011830c13"
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
0x0f200f9b00000000000000000000000000000000000000000000005fd7b4d4f6fc5fc5a20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1767983969373631006114`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`