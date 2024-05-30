# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9C7240d632C663a57D6eEb7fa5d2126a2f0b5993`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000001250ea16d00b2e00000000000000000000000000000000000000000000000000000000000b8e880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000b8e8800000000000000000000000000000000000000000000000000000000010db60cc229390035330d527571effb13dbb010ee6073fe9c3ed8348af68baba62b42b0160fd7d0c3b523bf7a8fa3dd2f8f87ed2a022f24774e8ad6069b2cdd02ec0b6e654f3032ef64e9566cae0c8d4537b08d01357dd6969dc51486bed5d2461023f7000000000000000000000000000000000000000000000000000000000000001b61c3f184f87bdec58d67a5b6f62eb000c52bc3bca40e7a6568f7af013e36c9813559214fb4d6b7cb7f5a3120ced8a5e28c56e5f1125570fab3a3e3fab10e8f923c6e145fe70d90da02a134dfbcbdc4e80806f495c2f9c3096caa6de9563acf47000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b317000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fc7dacfe145ee5e32a9000000000000000000000000000000000000000000003fc7dacfe145ee69c42600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc123cc812abe477bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a57453159546b314e7930324f4745784c5455315a4451744f4456684e6930304d4463794f546b345a6a49784d57456966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000009c7240d632c663a57d6eeb7fa5d2126a2f0b5993000000000000000000000000000000000000000000000000001250ea16d00b2e000000000000000000000000000000000000000000000000001250ea16c47ca600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc229390035330d527571effb13dbb010ee6073fe9c3ed8348af68baba62b42b0",
      "signature": {
        "s": "0x654f3032ef64e9566cae0c8d4537b08d01357dd6969dc51486bed5d2461023f7",
        "r": "0x160fd7d0c3b523bf7a8fa3dd2f8f87ed2a022f24774e8ad6069b2cdd02ec0b6e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x61c3f184f87bdec58d67a5b6f62eb000c52bc3bca40e7a6568f7af013e36c981",
      "signature": {
        "s": "0x3c6e145fe70d90da02a134dfbcbdc4e80806f495c2f9c3096caa6de9563acf47",
        "r": "0x3559214fb4d6b7cb7f5a3120ced8a5e28c56e5f1125570fab3a3e3fab10e8f92",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "757384",
    "total": "17675788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "757384",
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
            "amount": "27671430255738131609531"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyZWE1YTk1Ny02OGExLTU1ZDQtODVhNi00MDcyOTk4ZjIxMWEifQ==",
    "nonce": 111383,
    "balances": {
      "current": "301195757559966764774057",
      "previous": "301195757559966765532198"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c7240d632c663a57d6eeb7fa5d2126a2f0b5993",
    "nonce": 29,
    "balances": {
      "current": "5155515916094254",
      "previous": "5155515915336870"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:01.384Z",
  "updated": "2022-05-04T08:58:01.477Z",
  "id": "627240197832e20011830cf2"
}
```
* *stageAmount*: `5155515916094254`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000b8e880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000b8e8800000000000000000000000000000000000000000000000000000000010db60cc229390035330d527571effb13dbb010ee6073fe9c3ed8348af68baba62b42b0160fd7d0c3b523bf7a8fa3dd2f8f87ed2a022f24774e8ad6069b2cdd02ec0b6e654f3032ef64e9566cae0c8d4537b08d01357dd6969dc51486bed5d2461023f7000000000000000000000000000000000000000000000000000000000000001b61c3f184f87bdec58d67a5b6f62eb000c52bc3bca40e7a6568f7af013e36c9813559214fb4d6b7cb7f5a3120ced8a5e28c56e5f1125570fab3a3e3fab10e8f923c6e145fe70d90da02a134dfbcbdc4e80806f495c2f9c3096caa6de9563acf47000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b317000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003fc7dacfe145ee5e32a9000000000000000000000000000000000000000000003fc7dacfe145ee69c42600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc123cc812abe477bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a57453159546b314e7930324f4745784c5455315a4451744f4456684e6930304d4463794f546b345a6a49784d57456966513d3d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000009c7240d632c663a57d6eeb7fa5d2126a2f0b5993000000000000000000000000000000000000000000000000001250ea16d00b2e000000000000000000000000000000000000000000000000001250ea16c47ca600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc229390035330d527571effb13dbb010ee6073fe9c3ed8348af68baba62b42b0",
      "signature": {
        "s": "0x654f3032ef64e9566cae0c8d4537b08d01357dd6969dc51486bed5d2461023f7",
        "r": "0x160fd7d0c3b523bf7a8fa3dd2f8f87ed2a022f24774e8ad6069b2cdd02ec0b6e",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x61c3f184f87bdec58d67a5b6f62eb000c52bc3bca40e7a6568f7af013e36c981",
      "signature": {
        "s": "0x3c6e145fe70d90da02a134dfbcbdc4e80806f495c2f9c3096caa6de9563acf47",
        "r": "0x3559214fb4d6b7cb7f5a3120ced8a5e28c56e5f1125570fab3a3e3fab10e8f92",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "757384",
    "total": "17675788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "757384",
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
            "amount": "27671430255738131609531"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "757"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyZWE1YTk1Ny02OGExLTU1ZDQtODVhNi00MDcyOTk4ZjIxMWEifQ==",
    "nonce": 111383,
    "balances": {
      "current": "301195757559966764774057",
      "previous": "301195757559966765532198"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9c7240d632c663a57d6eeb7fa5d2126a2f0b5993",
    "nonce": 29,
    "balances": {
      "current": "5155515916094254",
      "previous": "5155515915336870"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:01.384Z",
  "updated": "2022-05-04T08:58:01.477Z",
  "id": "627240197832e20011830cf2"
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
0x0f200f9b000000000000000000000000000000000000000000000000001250ea16d00b2e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5155515916094254`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`