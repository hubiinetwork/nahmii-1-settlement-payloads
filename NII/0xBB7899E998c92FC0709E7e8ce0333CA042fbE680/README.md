# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xBB7899E998c92FC0709E7e8ce0333CA042fbE680`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000312888aee77b1ae21b00000000000000000000000000000000000000000000000382d7226196f8d89a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000382d7226196f8d89a0000000000000000000000000000000000000000000000628655ad0b02fb8b1a518fcc25be6023314ae7037063be2adca6eac36058262464de74358d13d563b242701eacbbe30da7cb3422ab230bbc4da6bc138adf8ba0031fdc407befb0712d34822d76f1a45e2c26bad207dfdd580d0e893c23ca1360d4de3590e10cfcfd4a000000000000000000000000000000000000000000000000000000000000001b67b5b1698b223021fb7c98c6b5b55c278640374aec78b524bbc0272e7b07de430ee82109405542b209d0c18452d65c487705c8f012d0d15cfb5a4848bf9edae34fa157cb024b291d45639ed0749ba644941b43e63321093c41ff3559ef5dca00000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0ddb877caf4f1000000000000000000000000000000000000000000004ef2496e1a811138469700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e61a670274790c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd427ca88c10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6a4d794e4446694e5331685a6a6c694c5455315a444d74595445774d793035596d4a695a6a426c4e7a6b335a54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000bb7899e998c92fc0709e7e8ce0333ca042fbe6800000000000000000000000000000000000000000000000312888aee77b1ae21b00000000000000000000000000000000000000000000002da5b18c85e422098100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x518fcc25be6023314ae7037063be2adca6eac36058262464de74358d13d563b2",
      "signature": {
        "s": "0x34822d76f1a45e2c26bad207dfdd580d0e893c23ca1360d4de3590e10cfcfd4a",
        "r": "0x42701eacbbe30da7cb3422ab230bbc4da6bc138adf8ba0031fdc407befb0712d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x67b5b1698b223021fb7c98c6b5b55c278640374aec78b524bbc0272e7b07de43",
      "signature": {
        "s": "0x4fa157cb024b291d45639ed0749ba644941b43e63321093c41ff3559ef5dca00",
        "r": "0x0ee82109405542b209d0c18452d65c487705c8f012d0d15cfb5a4848bf9edae3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "64768274368592140442",
    "total": "1817460752460445092634"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "64768274368592140442",
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
            "amount": "27599948339331723856065"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "64768274368592140"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MjMyNDFiNS1hZjliLTU1ZDMtYTEwMy05YmJiZjBlNzk3ZTgifQ==",
    "nonce": 110698,
    "balances": {
      "current": "372749155882780926342385",
      "previous": "372813988925423887074967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb7899e998c92fc0709e7e8ce0333ca042fbe680",
    "nonce": 46,
    "balances": {
      "current": "906811236279343833627",
      "previous": "842042961910751693185"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:34.743Z",
  "updated": "2022-05-04T08:54:34.822Z",
  "id": "62723f4abbd75600116d05c1"
}
```
* *stageAmount*: `906811236279343833627`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000382d7226196f8d89a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000382d7226196f8d89a0000000000000000000000000000000000000000000000628655ad0b02fb8b1a518fcc25be6023314ae7037063be2adca6eac36058262464de74358d13d563b242701eacbbe30da7cb3422ab230bbc4da6bc138adf8ba0031fdc407befb0712d34822d76f1a45e2c26bad207dfdd580d0e893c23ca1360d4de3590e10cfcfd4a000000000000000000000000000000000000000000000000000000000000001b67b5b1698b223021fb7c98c6b5b55c278640374aec78b524bbc0272e7b07de430ee82109405542b209d0c18452d65c487705c8f012d0d15cfb5a4848bf9edae34fa157cb024b291d45639ed0749ba644941b43e63321093c41ff3559ef5dca00000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b06a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004eeec5b0ddb877caf4f1000000000000000000000000000000000000000000004ef2496e1a811138469700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e61a670274790c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d83239ffd427ca88c10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304d6a4d794e4446694e5331685a6a6c694c5455315a444d74595445774d793035596d4a695a6a426c4e7a6b335a54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000bb7899e998c92fc0709e7e8ce0333ca042fbe6800000000000000000000000000000000000000000000000312888aee77b1ae21b00000000000000000000000000000000000000000000002da5b18c85e422098100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x518fcc25be6023314ae7037063be2adca6eac36058262464de74358d13d563b2",
      "signature": {
        "s": "0x34822d76f1a45e2c26bad207dfdd580d0e893c23ca1360d4de3590e10cfcfd4a",
        "r": "0x42701eacbbe30da7cb3422ab230bbc4da6bc138adf8ba0031fdc407befb0712d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x67b5b1698b223021fb7c98c6b5b55c278640374aec78b524bbc0272e7b07de43",
      "signature": {
        "s": "0x4fa157cb024b291d45639ed0749ba644941b43e63321093c41ff3559ef5dca00",
        "r": "0x0ee82109405542b209d0c18452d65c487705c8f012d0d15cfb5a4848bf9edae3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "64768274368592140442",
    "total": "1817460752460445092634"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "64768274368592140442",
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
            "amount": "27599948339331723856065"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "64768274368592140"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0MjMyNDFiNS1hZjliLTU1ZDMtYTEwMy05YmJiZjBlNzk3ZTgifQ==",
    "nonce": 110698,
    "balances": {
      "current": "372749155882780926342385",
      "previous": "372813988925423887074967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb7899e998c92fc0709e7e8ce0333ca042fbe680",
    "nonce": 46,
    "balances": {
      "current": "906811236279343833627",
      "previous": "842042961910751693185"
    }
  },
  "blockNumber": "14709970",
  "created": "2022-05-04T08:54:34.743Z",
  "updated": "2022-05-04T08:54:34.822Z",
  "id": "62723f4abbd75600116d05c1"
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
0x0f200f9b0000000000000000000000000000000000000000000000312888aee77b1ae21b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `906811236279343833627`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`