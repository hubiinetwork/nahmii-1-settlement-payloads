# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb2d8F51C87DAFD781AC18456547DC17a81640D03`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000000000000000000000000000000000000000001d03f18aa167a242ed415814a1c3494f8d899d60ee56fe3cc694d926f23d4bd3af35ade158bd7a6b2bcc7fddf084adb6aa521b8fdc7813b8d424ac8869655b6a2c20d603331fbfdc27e9768dae665455240b6b20d48f183bd0523842848365974fb000000000000000000000000000000000000000000000000000000000000001b90cafac0796b39f226697aa7842b1def403515f1cf876d930298199da1a4d0b2f5e428835107c2767524cdd35ffe997a752ec7401dfb1636ef9663c652199396320f4663d88e9b3164e915b082cad53e4cd9edf823c2f4f13ab702518e2fec4c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000095c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4ee310000000000000000000000000000000000000000000000000002386f2bc4ee4e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c303300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a497a597a526c4e4330774e7a4e684c5455344e7a4574596a51315a6930314d32457a5a6d4a685a6a646d596a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000b2d8f51c87dafd781ac18456547dc17a81640d0300000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f18aa167a242ed415814a1c3494f8d899d60ee56fe3cc694d926f23d4bd3af3",
      "signature": {
        "s": "0x0d603331fbfdc27e9768dae665455240b6b20d48f183bd0523842848365974fb",
        "r": "0x5ade158bd7a6b2bcc7fddf084adb6aa521b8fdc7813b8d424ac8869655b6a2c2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x90cafac0796b39f226697aa7842b1def403515f1cf876d930298199da1a4d0b2",
      "signature": {
        "s": "0x320f4663d88e9b3164e915b082cad53e4cd9edf823c2f4f13ab702518e2fec4c",
        "r": "0xf5e428835107c2767524cdd35ffe997a752ec7401dfb1636ef9663c652199396",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "464",
    "total": "464"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "464",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798771"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzIzYzRlNC0wNzNhLTU4NzEtYjQ1Zi01M2EzZmJhZjdmYjkifQ==",
    "nonce": 2396,
    "balances": {
      "current": "10000001284367120",
      "previous": "10000001284367585"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb2d8f51c87dafd781ac18456547dc17a81640d03",
    "nonce": 10,
    "balances": {
      "current": "464",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:16.285Z",
  "updated": "2020-05-22T08:16:16.356Z",
  "id": "5ec78a50e5756b00111b8278"
}
```
* *stageAmount*: `464`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000000000000000000000000000000000000000001d03f18aa167a242ed415814a1c3494f8d899d60ee56fe3cc694d926f23d4bd3af35ade158bd7a6b2bcc7fddf084adb6aa521b8fdc7813b8d424ac8869655b6a2c20d603331fbfdc27e9768dae665455240b6b20d48f183bd0523842848365974fb000000000000000000000000000000000000000000000000000000000000001b90cafac0796b39f226697aa7842b1def403515f1cf876d930298199da1a4d0b2f5e428835107c2767524cdd35ffe997a752ec7401dfb1636ef9663c652199396320f4663d88e9b3164e915b082cad53e4cd9edf823c2f4f13ab702518e2fec4c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000095c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4ee310000000000000000000000000000000000000000000000000002386f2bc4ee4e100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c303300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a497a597a526c4e4330774e7a4e684c5455344e7a4574596a51315a6930314d32457a5a6d4a685a6a646d596a6b6966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000b2d8f51c87dafd781ac18456547dc17a81640d0300000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f18aa167a242ed415814a1c3494f8d899d60ee56fe3cc694d926f23d4bd3af3",
      "signature": {
        "s": "0x0d603331fbfdc27e9768dae665455240b6b20d48f183bd0523842848365974fb",
        "r": "0x5ade158bd7a6b2bcc7fddf084adb6aa521b8fdc7813b8d424ac8869655b6a2c2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x90cafac0796b39f226697aa7842b1def403515f1cf876d930298199da1a4d0b2",
      "signature": {
        "s": "0x320f4663d88e9b3164e915b082cad53e4cd9edf823c2f4f13ab702518e2fec4c",
        "r": "0xf5e428835107c2767524cdd35ffe997a752ec7401dfb1636ef9663c652199396",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "464",
    "total": "464"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "464",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "798771"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzIzYzRlNC0wNzNhLTU4NzEtYjQ1Zi01M2EzZmJhZjdmYjkifQ==",
    "nonce": 2396,
    "balances": {
      "current": "10000001284367120",
      "previous": "10000001284367585"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb2d8f51c87dafd781ac18456547dc17a81640d03",
    "nonce": 10,
    "balances": {
      "current": "464",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:16.285Z",
  "updated": "2020-05-22T08:16:16.356Z",
  "id": "5ec78a50e5756b00111b8278"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `464`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``