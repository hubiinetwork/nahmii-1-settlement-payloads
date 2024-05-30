# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD8BA08B64Fbb3bf653A682D306Db45361b5DE064`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000024471610c57934f12d000000000000000000000000000000000000000000000000dc2fb26d57f20fef0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f20fef00000000000000000000000000000000000000000000001822a4621607eb68518459da4ff64e75e5edcf42ed8eb2df5ecc1cd0d96e6e3591739f280719fa17440c793de35db117689a2d460b3cf148cf92fd30b46af1515fd5d2f49e5afd4a043952a5d4586abbe6e41866039df86a12941c5551fbba60303f27d0e003ab6de7000000000000000000000000000000000000000000000000000000000000001b82781bbd312a0211424ba021a0c5edaccb00a4d950d28ce24d17d3a30f3d97ba05cc5dcdd067fb3260c6d9acab7dd6bad677e8593a3600838ba5082732e8ec6314342c0c6cde008353e7b07f493ac51f1fc50cd76d993d746fa74b5a61015ff1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6ec000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fc7190fbd09eda07b8c000000000000000000000000000000000000000000002fc7f577cd98a93e901a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac049f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e029f59eef2ed58f920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d544d334e7a4d774e4330304e5745774c5455774d4755744f5441354e43307a597a45785a5441354e4759334d7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d8ba08b64fbb3bf653a682d306db45361b5de064000000000000000000000000000000000000000000000024471610c57934f12d0000000000000000000000000000000000000000000000236ae65e582142e13e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8459da4ff64e75e5edcf42ed8eb2df5ecc1cd0d96e6e3591739f280719fa1744",
      "signature": {
        "s": "0x3952a5d4586abbe6e41866039df86a12941c5551fbba60303f27d0e003ab6de7",
        "r": "0x0c793de35db117689a2d460b3cf148cf92fd30b46af1515fd5d2f49e5afd4a04",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x82781bbd312a0211424ba021a0c5edaccb00a4d950d28ce24d17d3a30f3d97ba",
      "signature": {
        "s": "0x14342c0c6cde008353e7b07f493ac51f1fc50cd76d993d746fa74b5a61015ff1",
        "r": "0x05cc5dcdd067fb3260c6d9acab7dd6bad677e8593a3600838ba5082732e8ec63",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946207727",
    "total": "445218085709261006929"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946207727",
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
            "amount": "27746926584334134906770"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946207"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMTM3NzMwNC00NWEwLTUwMGUtOTA5NC0zYzExZTA5NGY3MzYifQ==",
    "nonce": 112364,
    "balances": {
      "current": "225623932635367463746444",
      "previous": "225639814597658604900378"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd8ba08b64fbb3bf653a682d306db45361b5de064",
    "nonce": 46,
    "balances": {
      "current": "669205086720052490541",
      "previous": "653338990525106282814"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:25.073Z",
  "updated": "2022-05-04T09:03:25.201Z",
  "id": "6272415dbbd75600116d07d4"
}
```
* *stageAmount*: `669205086720052490541`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f20fef0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f20fef00000000000000000000000000000000000000000000001822a4621607eb68518459da4ff64e75e5edcf42ed8eb2df5ecc1cd0d96e6e3591739f280719fa17440c793de35db117689a2d460b3cf148cf92fd30b46af1515fd5d2f49e5afd4a043952a5d4586abbe6e41866039df86a12941c5551fbba60303f27d0e003ab6de7000000000000000000000000000000000000000000000000000000000000001b82781bbd312a0211424ba021a0c5edaccb00a4d950d28ce24d17d3a30f3d97ba05cc5dcdd067fb3260c6d9acab7dd6bad677e8593a3600838ba5082732e8ec6314342c0c6cde008353e7b07f493ac51f1fc50cd76d993d746fa74b5a61015ff1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6ec000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fc7190fbd09eda07b8c000000000000000000000000000000000000000000002fc7f577cd98a93e901a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac049f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e029f59eef2ed58f920000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d544d334e7a4d774e4330304e5745774c5455774d4755744f5441354e43307a597a45785a5441354e4759334d7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d8ba08b64fbb3bf653a682d306db45361b5de064000000000000000000000000000000000000000000000024471610c57934f12d0000000000000000000000000000000000000000000000236ae65e582142e13e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8459da4ff64e75e5edcf42ed8eb2df5ecc1cd0d96e6e3591739f280719fa1744",
      "signature": {
        "s": "0x3952a5d4586abbe6e41866039df86a12941c5551fbba60303f27d0e003ab6de7",
        "r": "0x0c793de35db117689a2d460b3cf148cf92fd30b46af1515fd5d2f49e5afd4a04",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x82781bbd312a0211424ba021a0c5edaccb00a4d950d28ce24d17d3a30f3d97ba",
      "signature": {
        "s": "0x14342c0c6cde008353e7b07f493ac51f1fc50cd76d993d746fa74b5a61015ff1",
        "r": "0x05cc5dcdd067fb3260c6d9acab7dd6bad677e8593a3600838ba5082732e8ec63",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194946207727",
    "total": "445218085709261006929"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946207727",
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
            "amount": "27746926584334134906770"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946207"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhMTM3NzMwNC00NWEwLTUwMGUtOTA5NC0zYzExZTA5NGY3MzYifQ==",
    "nonce": 112364,
    "balances": {
      "current": "225623932635367463746444",
      "previous": "225639814597658604900378"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd8ba08b64fbb3bf653a682d306db45361b5de064",
    "nonce": 46,
    "balances": {
      "current": "669205086720052490541",
      "previous": "653338990525106282814"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:25.073Z",
  "updated": "2022-05-04T09:03:25.201Z",
  "id": "6272415dbbd75600116d07d4"
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
0x0f200f9b000000000000000000000000000000000000000000000024471610c57934f12d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205086720052490541`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`