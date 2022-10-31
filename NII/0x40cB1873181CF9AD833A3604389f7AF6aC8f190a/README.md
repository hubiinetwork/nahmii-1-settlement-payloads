# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x40cB1873181CF9AD833A3604389f7AF6aC8f190a`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000e94324318bbf7060000000000000000000000000000000000000000000000000000001b4774adc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001b4774adc1000000000000000000000000000000000000000000000157fbcbdb4afae3e5acf17bb7843b67c4eabf574bdd64f45ed9e8737cabb7bb99f5b849b48266f146228092ae6a8c375c3af0d74d492e999a975151ad275360e7cc620fbfd9120496af6387e897392fd28b23883f590d2ad485a4295ed9f92ebe1428b1408308dd35fa000000000000000000000000000000000000000000000000000000000000001c3d618f78d5ac719a8be65769fcce3cb0b3797e31a6eaf23294ed032f1ef4a5ddad1d2ecf807cd11a55747247e6aad53ec2d203de90b2d0ccaea62731c9b6c622304bb851f0d8ac7fdba2fce29c946b243c2a2f0c4b2e0c902204b8db91204ee2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001afc8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052beecff74a3b33cbd9b0000000000000000000000000000000000000000000052beecff74bf01ad2f1d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006fbc3c10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73894b5c493666d060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5445785a6d49314e7930325a5441774c54566c5a6a41744f4463775a5330324f544d3559544931597a41315957596966513d3d000000000000000000000000000000000000000000000000000000000000002c00000000000000000000000040cb1873181cf9ad833a3604389f7af6ac8f190a0000000000000000000000000000000000000000000000000e94324318bbf7060000000000000000000000000000000000000000000000000e943227d147494500000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000051583b31c6f3c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xf17bb7843b67c4eabf574bdd64f45ed9e8737cabb7bb99f5b849b48266f14622",
      "signature": {
        "s": "0x6387e897392fd28b23883f590d2ad485a4295ed9f92ebe1428b1408308dd35fa",
        "r": "0x8092ae6a8c375c3af0d74d492e999a975151ad275360e7cc620fbfd9120496af",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d618f78d5ac719a8be65769fcce3cb0b3797e31a6eaf23294ed032f1ef4a5dd",
      "signature": {
        "s": "0x304bb851f0d8ac7fdba2fce29c946b243c2a2f0c4b2e0c902204b8db91204ee2",
        "r": "0xad1d2ecf807cd11a55747247e6aad53ec2d203de90b2d0ccaea62731c9b6c622",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "117162945985",
    "total": "6345377053921251681708"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "117162945985",
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
            "amount": "27581959473614347988230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "117162945"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NTExZmI1Ny02ZTAwLTVlZjAtODcwZS02OTM5YTI1YzA1YWYifQ==",
    "nonce": 110536,
    "balances": {
      "current": "390756010465874170133915",
      "previous": "390756010465991450242845"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "5861500000000000000"
          }
        }
      ]
    },
    "wallet": "0x40cb1873181cf9ad833a3604389f7af6ac8f190a",
    "nonce": 44,
    "balances": {
      "current": "1050519876843337478",
      "previous": "1050519759680391493"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:47.192Z",
  "updated": "2022-05-04T08:53:47.358Z",
  "id": "62723f1bbbd75600116d058b"
}
```
* *stageAmount*: `1050519876843337478`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006800000000000000000000000000000000000000000000000000000001b4774adc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000001b4774adc1000000000000000000000000000000000000000000000157fbcbdb4afae3e5acf17bb7843b67c4eabf574bdd64f45ed9e8737cabb7bb99f5b849b48266f146228092ae6a8c375c3af0d74d492e999a975151ad275360e7cc620fbfd9120496af6387e897392fd28b23883f590d2ad485a4295ed9f92ebe1428b1408308dd35fa000000000000000000000000000000000000000000000000000000000000001c3d618f78d5ac719a8be65769fcce3cb0b3797e31a6eaf23294ed032f1ef4a5ddad1d2ecf807cd11a55747247e6aad53ec2d203de90b2d0ccaea62731c9b6c622304bb851f0d8ac7fdba2fce29c946b243c2a2f0c4b2e0c902204b8db91204ee2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001afc8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000052beecff74a3b33cbd9b0000000000000000000000000000000000000000000052beecff74bf01ad2f1d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000006fbc3c10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d73894b5c493666d060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e5445785a6d49314e7930325a5441774c54566c5a6a41744f4463775a5330324f544d3559544931597a41315957596966513d3d000000000000000000000000000000000000000000000000000000000000002c00000000000000000000000040cb1873181cf9ad833a3604389f7af6ac8f190a0000000000000000000000000000000000000000000000000e94324318bbf7060000000000000000000000000000000000000000000000000e943227d147494500000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000051583b31c6f3c0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xf17bb7843b67c4eabf574bdd64f45ed9e8737cabb7bb99f5b849b48266f14622",
      "signature": {
        "s": "0x6387e897392fd28b23883f590d2ad485a4295ed9f92ebe1428b1408308dd35fa",
        "r": "0x8092ae6a8c375c3af0d74d492e999a975151ad275360e7cc620fbfd9120496af",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d618f78d5ac719a8be65769fcce3cb0b3797e31a6eaf23294ed032f1ef4a5dd",
      "signature": {
        "s": "0x304bb851f0d8ac7fdba2fce29c946b243c2a2f0c4b2e0c902204b8db91204ee2",
        "r": "0xad1d2ecf807cd11a55747247e6aad53ec2d203de90b2d0ccaea62731c9b6c622",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "117162945985",
    "total": "6345377053921251681708"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "117162945985",
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
            "amount": "27581959473614347988230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "117162945"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NTExZmI1Ny02ZTAwLTVlZjAtODcwZS02OTM5YTI1YzA1YWYifQ==",
    "nonce": 110536,
    "balances": {
      "current": "390756010465874170133915",
      "previous": "390756010465991450242845"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "5861500000000000000"
          }
        }
      ]
    },
    "wallet": "0x40cb1873181cf9ad833a3604389f7af6ac8f190a",
    "nonce": 44,
    "balances": {
      "current": "1050519876843337478",
      "previous": "1050519759680391493"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:47.192Z",
  "updated": "2022-05-04T08:53:47.358Z",
  "id": "62723f1bbbd75600116d058b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000e94324318bbf7060000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1050519876843337478`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`