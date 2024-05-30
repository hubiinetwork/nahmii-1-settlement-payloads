# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8c72f8cE2F3A56Ad5E44df24a16c16CC7a85C2a1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000001372078599256691da00000000000000000000000000000000000000000000000000000003cf9fb23e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003cf9fb23e000000000000000000000000000000000000000000000009f97163bf8f82fe470db572c094985d37ae308c972b89d09de425bcb018fa7fc194ae0ff9c18891d90dc542eefdcccf48514faeefeb83b7360ea09fc0c0e983aa9cd7adda298d8ef2026594def956b73fc298a34095a2704ea1c310c6ed93ef3f37189cefb18acdc9000000000000000000000000000000000000000000000000000000000000001b8adc86bae003e9a332e560ce5395f45b4b62c8104af65645d310f945cec849a1b6ccd1269e795d22f390ed13d214f92f03d2c4c6eb2a55d14941e16534cf412e3c2558d5fa554db9cc1d053e271dced0a9dcb4eaead0c5dccb3d1ef7b047dbca000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0d4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bb47fe5b48b89d4af74000000000000000000000000000000000000000000004bb47fe5b48f5a6e242d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f9c27b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9058a81883e88cc240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e4749314d325979596930345a44566b4c5455304f4445744f445a695a6930784f5759335a57466c4d32517a4f47496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a100000000000000000000000000000000000000000000001372078599256691da0000000000000000000000000000000000000000000000137207859555c6df9c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0db572c094985d37ae308c972b89d09de425bcb018fa7fc194ae0ff9c18891d9",
      "signature": {
        "s": "0x026594def956b73fc298a34095a2704ea1c310c6ed93ef3f37189cefb18acdc9",
        "r": "0x0dc542eefdcccf48514faeefeb83b7360ea09fc0c0e983aa9cd7adda298d8ef2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8adc86bae003e9a332e560ce5395f45b4b62c8104af65645d310f945cec849a1",
      "signature": {
        "s": "0x3c2558d5fa554db9cc1d053e271dced0a9dcb4eaead0c5dccb3d1ef7b047dbca",
        "r": "0xb6ccd1269e795d22f390ed13d214f92f03d2c4c6eb2a55d14941e16534cf412e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16368251454",
    "total": "183994953925595954759"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16368251454",
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
            "amount": "27615175152282339167268"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16368251"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNGI1M2YyYi04ZDVkLTU0ODEtODZiZi0xOWY3ZWFlM2QzOGIifQ==",
    "nonce": 110804,
    "balances": {
      "current": "357507116119214999777140",
      "previous": "357507116119231384396845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a1",
    "nonce": 46,
    "balances": {
      "current": "358704820338446209498",
      "previous": "358704820322077958044"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:07.356Z",
  "updated": "2022-05-04T08:55:07.466Z",
  "id": "62723f6b3592fd001130b54f"
}
```
* *stageAmount*: `358704820338446209498`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000003cf9fb23e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000003cf9fb23e000000000000000000000000000000000000000000000009f97163bf8f82fe470db572c094985d37ae308c972b89d09de425bcb018fa7fc194ae0ff9c18891d90dc542eefdcccf48514faeefeb83b7360ea09fc0c0e983aa9cd7adda298d8ef2026594def956b73fc298a34095a2704ea1c310c6ed93ef3f37189cefb18acdc9000000000000000000000000000000000000000000000000000000000000001b8adc86bae003e9a332e560ce5395f45b4b62c8104af65645d310f945cec849a1b6ccd1269e795d22f390ed13d214f92f03d2c4c6eb2a55d14941e16534cf412e3c2558d5fa554db9cc1d053e271dced0a9dcb4eaead0c5dccb3d1ef7b047dbca000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0d4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004bb47fe5b48b89d4af74000000000000000000000000000000000000000000004bb47fe5b48f5a6e242d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000f9c27b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9058a81883e88cc240000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684e4749314d325979596930345a44566b4c5455304f4445744f445a695a6930784f5759335a57466c4d32517a4f47496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000008c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a100000000000000000000000000000000000000000000001372078599256691da0000000000000000000000000000000000000000000000137207859555c6df9c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0db572c094985d37ae308c972b89d09de425bcb018fa7fc194ae0ff9c18891d9",
      "signature": {
        "s": "0x026594def956b73fc298a34095a2704ea1c310c6ed93ef3f37189cefb18acdc9",
        "r": "0x0dc542eefdcccf48514faeefeb83b7360ea09fc0c0e983aa9cd7adda298d8ef2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8adc86bae003e9a332e560ce5395f45b4b62c8104af65645d310f945cec849a1",
      "signature": {
        "s": "0x3c2558d5fa554db9cc1d053e271dced0a9dcb4eaead0c5dccb3d1ef7b047dbca",
        "r": "0xb6ccd1269e795d22f390ed13d214f92f03d2c4c6eb2a55d14941e16534cf412e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "16368251454",
    "total": "183994953925595954759"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16368251454",
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
            "amount": "27615175152282339167268"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16368251"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhNGI1M2YyYi04ZDVkLTU0ODEtODZiZi0xOWY3ZWFlM2QzOGIifQ==",
    "nonce": 110804,
    "balances": {
      "current": "357507116119214999777140",
      "previous": "357507116119231384396845"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8c72f8ce2f3a56ad5e44df24a16c16cc7a85c2a1",
    "nonce": 46,
    "balances": {
      "current": "358704820338446209498",
      "previous": "358704820322077958044"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:07.356Z",
  "updated": "2022-05-04T08:55:07.466Z",
  "id": "62723f6b3592fd001130b54f"
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
0x0f200f9b00000000000000000000000000000000000000000000001372078599256691da0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `358704820338446209498`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`