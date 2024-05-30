# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf868280f9956844D23b5e8C52CfE6A1E661E73D7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000009497e7e2f66fc5b00000000000000000000000000000000000000000000000000385e2163ac09300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000385e2163ac0930000000000000000000000000000000000000000000000000062dbb7d764827fce7def3fecaf3b21d172ac2a5ff09eda6dfaa2db1dd1a529cc998ef78f1296588f9eca1ee7a22389d9b04cd27754f76b1fe180d3608077b2dfd9f93fe82ba3ca323be7f42718ff1db95b6dcad5a5036210847d37e73310fea66e59e2715ff04bf000000000000000000000000000000000000000000000000000000000000001c6cefaf0db02590a052f061a7b91796daadaa15501b7af326e963bace1094e024244ec844ae4d623c3a72f7369418c0aa14d9e54994fa2f3e6606bf27cac02135599729307f59c902feafadb7f61db2fc487a47eb706e8f90c9c140d430291c74000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae14000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009638dec1d9211518805a000000000000000000000000000000000000000000009638defa45b095cb9f0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000e6e1d0715830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f6de6d093ee820bf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d5445774e54426d4e6930305a4755794c54557a4e6a4574596a67344e7930304e44677a4d7a677859574d354e7a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f868280f9956844d23b5e8c52cfe6a1e661e73d700000000000000000000000000000000000000000000000009497e7e2f66fc5b0000000000000000000000000000000000000000000000000911205ccbbaf32b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7def3fecaf3b21d172ac2a5ff09eda6dfaa2db1dd1a529cc998ef78f1296588",
      "signature": {
        "s": "0x23be7f42718ff1db95b6dcad5a5036210847d37e73310fea66e59e2715ff04bf",
        "r": "0xf9eca1ee7a22389d9b04cd27754f76b1fe180d3608077b2dfd9f93fe82ba3ca3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6cefaf0db02590a052f061a7b91796daadaa15501b7af326e963bace1094e024",
      "signature": {
        "s": "0x599729307f59c902feafadb7f61db2fc487a47eb706e8f90c9c140d430291c74",
        "r": "0x244ec844ae4d623c3a72f7369418c0aa14d9e54994fa2f3e6606bf27cac02135",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194947376",
    "total": "445218085709293564"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194947376",
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
            "amount": "27263629772333645308095"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194947"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMTEwNTBmNi00ZGUyLTUzNjEtYjg4Ny00NDgzMzgxYWM5NzcifQ==",
    "nonce": 110100,
    "balances": {
      "current": "709404041447857553178714",
      "previous": "709404057329819844321037"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf868280f9956844d23b5e8c52cfe6a1e661e73d7",
    "nonce": 46,
    "balances": {
      "current": "669205100067486811",
      "previous": "653339003872539435"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:32.688Z",
  "updated": "2022-05-04T08:51:32.749Z",
  "id": "62723e947832e20011830b42"
}
```
* *stageAmount*: `669205100067486811`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000385e2163ac09300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000385e2163ac0930000000000000000000000000000000000000000000000000062dbb7d764827fce7def3fecaf3b21d172ac2a5ff09eda6dfaa2db1dd1a529cc998ef78f1296588f9eca1ee7a22389d9b04cd27754f76b1fe180d3608077b2dfd9f93fe82ba3ca323be7f42718ff1db95b6dcad5a5036210847d37e73310fea66e59e2715ff04bf000000000000000000000000000000000000000000000000000000000000001c6cefaf0db02590a052f061a7b91796daadaa15501b7af326e963bace1094e024244ec844ae4d623c3a72f7369418c0aa14d9e54994fa2f3e6606bf27cac02135599729307f59c902feafadb7f61db2fc487a47eb706e8f90c9c140d430291c74000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae14000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009638dec1d9211518805a000000000000000000000000000000000000000000009638defa45b095cb9f0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000e6e1d0715830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f6de6d093ee820bf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d5445774e54426d4e6930305a4755794c54557a4e6a4574596a67344e7930304e44677a4d7a677859574d354e7a636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f868280f9956844d23b5e8c52cfe6a1e661e73d700000000000000000000000000000000000000000000000009497e7e2f66fc5b0000000000000000000000000000000000000000000000000911205ccbbaf32b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe7def3fecaf3b21d172ac2a5ff09eda6dfaa2db1dd1a529cc998ef78f1296588",
      "signature": {
        "s": "0x23be7f42718ff1db95b6dcad5a5036210847d37e73310fea66e59e2715ff04bf",
        "r": "0xf9eca1ee7a22389d9b04cd27754f76b1fe180d3608077b2dfd9f93fe82ba3ca3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6cefaf0db02590a052f061a7b91796daadaa15501b7af326e963bace1094e024",
      "signature": {
        "s": "0x599729307f59c902feafadb7f61db2fc487a47eb706e8f90c9c140d430291c74",
        "r": "0x244ec844ae4d623c3a72f7369418c0aa14d9e54994fa2f3e6606bf27cac02135",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15866096194947376",
    "total": "445218085709293564"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194947376",
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
            "amount": "27263629772333645308095"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194947"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMTEwNTBmNi00ZGUyLTUzNjEtYjg4Ny00NDgzMzgxYWM5NzcifQ==",
    "nonce": 110100,
    "balances": {
      "current": "709404041447857553178714",
      "previous": "709404057329819844321037"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf868280f9956844d23b5e8c52cfe6a1e661e73d7",
    "nonce": 46,
    "balances": {
      "current": "669205100067486811",
      "previous": "653339003872539435"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:32.688Z",
  "updated": "2022-05-04T08:51:32.749Z",
  "id": "62723e947832e20011830b42"
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
0x0f200f9b00000000000000000000000000000000000000000000000009497e7e2f66fc5b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205100067486811`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`