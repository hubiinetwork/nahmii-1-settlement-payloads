# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1303F1a8960096CF22f125C4074AD43618F1276a`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000004c2ee1a6607389def4000000000000000000000000000000000000000000000001ce6429e59f40b5960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001ce6429e59f40b596000000000000000000000000000000000000000000000032af26012e487fd3f1e91ac919914f99e5a0742d45531e574f9286dc56c30faf067e6fd8b534d8eeaca755c1221551536e254ab2e55a1b3cd4aefa7721e89028ed7985e1265f1e05e325c4bad0a814353adb99f8e38fa49a2549d5e297001777d29d198a93a8c4790c000000000000000000000000000000000000000000000000000000000000001b42eaa6c2cd1084f45fe48be98b413cc827025e305c263e2981d9c2132070d884ef0db4971e8cdb043811f511e670674b1892028614f1ed88146e32b8eb818586476f6187adfac2949f9c32fccfc9dbcfbbe8d50acf1a08e7535776e5fac2bada000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad65000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096a079e9c784c6ece55b0000000000000000000000000000000000000000000096a248c450b0844a160000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000765f461e1c7b0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5dc5f47f885d375200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a6b7a4e4752694e5330334d4745324c5456694d7a6b74596d55314e6930795a6d4e6d4d54426c4f4759324e7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001303f1a8960096cf22f125c4074ad43618f1276a00000000000000000000000000000000000000000000004c2ee1a6607389def400000000000000000000000000000000000000000000004a607d7c7ad449295e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe91ac919914f99e5a0742d45531e574f9286dc56c30faf067e6fd8b534d8eeac",
      "signature": {
        "s": "0x25c4bad0a814353adb99f8e38fa49a2549d5e297001777d29d198a93a8c4790c",
        "r": "0xa755c1221551536e254ab2e55a1b3cd4aefa7721e89028ed7985e1265f1e05e3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42eaa6c2cd1084f45fe48be98b413cc827025e305c263e2981d9c2132070d884",
      "signature": {
        "s": "0x476f6187adfac2949f9c32fccfc9dbcfbbe8d50acf1a08e7535776e5fac2bada",
        "r": "0xef0db4971e8cdb043811f511e670674b1892028614f1ed88146e32b8eb818586",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "33318802009389839766",
    "total": "934957979989526434801"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33318802009389839766",
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
            "amount": "27261720486812862084384"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "33318802009389839"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzkzNGRiNS03MGE2LTViMzktYmU1Ni0yZmNmMTBlOGY2NzYifQ==",
    "nonce": 109925,
    "balances": {
      "current": "711315236254161560200539",
      "previous": "711348588374972959430144"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1303f1a8960096cf22f125c4074ad43618f1276a",
    "nonce": 46,
    "balances": {
      "current": "1405330713730615992052",
      "previous": "1372011911721226152286"
    }
  },
  "blockNumber": "14709954",
  "created": "2022-05-04T08:50:38.523Z",
  "updated": "2022-05-04T08:50:38.582Z",
  "id": "62723e5e3592fd001130b42f"
}
```
* *stageAmount*: `1405330713730615992052`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001ce6429e59f40b5960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001ce6429e59f40b596000000000000000000000000000000000000000000000032af26012e487fd3f1e91ac919914f99e5a0742d45531e574f9286dc56c30faf067e6fd8b534d8eeaca755c1221551536e254ab2e55a1b3cd4aefa7721e89028ed7985e1265f1e05e325c4bad0a814353adb99f8e38fa49a2549d5e297001777d29d198a93a8c4790c000000000000000000000000000000000000000000000000000000000000001b42eaa6c2cd1084f45fe48be98b413cc827025e305c263e2981d9c2132070d884ef0db4971e8cdb043811f511e670674b1892028614f1ed88146e32b8eb818586476f6187adfac2949f9c32fccfc9dbcfbbe8d50acf1a08e7535776e5fac2bada000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad65000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096a079e9c784c6ece55b0000000000000000000000000000000000000000000096a248c450b0844a160000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000765f461e1c7b0f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5dc5f47f885d375200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a6b7a4e4752694e5330334d4745324c5456694d7a6b74596d55314e6930795a6d4e6d4d54426c4f4759324e7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001303f1a8960096cf22f125c4074ad43618f1276a00000000000000000000000000000000000000000000004c2ee1a6607389def400000000000000000000000000000000000000000000004a607d7c7ad449295e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe91ac919914f99e5a0742d45531e574f9286dc56c30faf067e6fd8b534d8eeac",
      "signature": {
        "s": "0x25c4bad0a814353adb99f8e38fa49a2549d5e297001777d29d198a93a8c4790c",
        "r": "0xa755c1221551536e254ab2e55a1b3cd4aefa7721e89028ed7985e1265f1e05e3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42eaa6c2cd1084f45fe48be98b413cc827025e305c263e2981d9c2132070d884",
      "signature": {
        "s": "0x476f6187adfac2949f9c32fccfc9dbcfbbe8d50acf1a08e7535776e5fac2bada",
        "r": "0xef0db4971e8cdb043811f511e670674b1892028614f1ed88146e32b8eb818586",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "33318802009389839766",
    "total": "934957979989526434801"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "33318802009389839766",
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
            "amount": "27261720486812862084384"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "33318802009389839"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMzkzNGRiNS03MGE2LTViMzktYmU1Ni0yZmNmMTBlOGY2NzYifQ==",
    "nonce": 109925,
    "balances": {
      "current": "711315236254161560200539",
      "previous": "711348588374972959430144"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1303f1a8960096cf22f125c4074ad43618f1276a",
    "nonce": 46,
    "balances": {
      "current": "1405330713730615992052",
      "previous": "1372011911721226152286"
    }
  },
  "blockNumber": "14709954",
  "created": "2022-05-04T08:50:38.523Z",
  "updated": "2022-05-04T08:50:38.582Z",
  "id": "62723e5e3592fd001130b42f"
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
0x0f200f9b00000000000000000000000000000000000000000000004c2ee1a6607389def40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1405330713730615992052`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`