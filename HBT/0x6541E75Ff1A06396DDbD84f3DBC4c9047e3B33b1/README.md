# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6541E75Ff1A06396DDbD84f3DBC4c9047e3B33b1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000f56a6ef290000000000000000000000000000000000000000000000000000000f56a6ef29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f56a6ef290000000000000000000000000000000000000000000000000000000f56a6ef2927b52176ac964c071fb326aa7c99e97c1030368595f363e9f7263377caafe6273f535e6fc0694b6332d1a0a0f903e6f7e8e3b97a663ae68fc0e07d33c471a6dc1875bd75446fbbe4378e82cafa0edb0cc4cb848095897c6400aa97048e38b3cb000000000000000000000000000000000000000000000000000000000000001c7c35f6470fb5c835c5479566adecd5bb7233e3c4abfbfa12c051463395fad610ac927faacf7f77bc433edcbf24372869da38f24675650c9fadab1bedf1373794094e952cd5e0b063dfdb8acca09d04ea6f86a95f145743b4f8a4a49220c54549000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ca2d7803cbe000000000000000000000000000000000000000000000000002e1cb2321464f900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003ed3912000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008ed9af3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a54526d5a4445774e79316d4d5467334c54566d4d6d4d74596a45314d6930334e544e6d4e6a49784e6a6b324e324d6966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000006541e75ff1a06396ddbd84f3dbc4c9047e3b33b10000000000000000000000000000000000000000000000000000000f56a6ef29000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27b52176ac964c071fb326aa7c99e97c1030368595f363e9f7263377caafe627",
      "signature": {
        "s": "0x1875bd75446fbbe4378e82cafa0edb0cc4cb848095897c6400aa97048e38b3cb",
        "r": "0x3f535e6fc0694b6332d1a0a0f903e6f7e8e3b97a663ae68fc0e07d33c471a6dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7c35f6470fb5c835c5479566adecd5bb7233e3c4abfbfa12c051463395fad610",
      "signature": {
        "s": "0x094e952cd5e0b063dfdb8acca09d04ea6f86a95f145743b4f8a4a49220c54549",
        "r": "0xac927faacf7f77bc433edcbf24372869da38f24675650c9fadab1bedf1373794",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "65878290217",
    "total": "65878290217"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "65878290217",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "38346093544"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "65878290"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZTRmZDEwNy1mMTg3LTVmMmMtYjE1Mi03NTNmNjIxNjk2N2MifQ==",
    "nonce": 5694,
    "balances": {
      "current": "12979334654475454",
      "previous": "12979400598643961"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6541e75ff1a06396ddbd84f3dbc4c9047e3b33b1",
    "nonce": 16,
    "balances": {
      "current": "65878290217",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:07.052Z",
  "updated": "2020-05-22T08:43:07.140Z",
  "id": "5ec7909bb0c6090011d5b034"
}
```
* *stageAmount*: `65878290217`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000f56a6ef29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000f56a6ef290000000000000000000000000000000000000000000000000000000f56a6ef2927b52176ac964c071fb326aa7c99e97c1030368595f363e9f7263377caafe6273f535e6fc0694b6332d1a0a0f903e6f7e8e3b97a663ae68fc0e07d33c471a6dc1875bd75446fbbe4378e82cafa0edb0cc4cb848095897c6400aa97048e38b3cb000000000000000000000000000000000000000000000000000000000000001c7c35f6470fb5c835c5479566adecd5bb7233e3c4abfbfa12c051463395fad610ac927faacf7f77bc433edcbf24372869da38f24675650c9fadab1bedf1373794094e952cd5e0b063dfdb8acca09d04ea6f86a95f145743b4f8a4a49220c54549000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000163e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ca2d7803cbe000000000000000000000000000000000000000000000000002e1cb2321464f900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003ed3912000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008ed9af3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a54526d5a4445774e79316d4d5467334c54566d4d6d4d74596a45314d6930334e544e6d4e6a49784e6a6b324e324d6966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000006541e75ff1a06396ddbd84f3dbc4c9047e3b33b10000000000000000000000000000000000000000000000000000000f56a6ef29000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x27b52176ac964c071fb326aa7c99e97c1030368595f363e9f7263377caafe627",
      "signature": {
        "s": "0x1875bd75446fbbe4378e82cafa0edb0cc4cb848095897c6400aa97048e38b3cb",
        "r": "0x3f535e6fc0694b6332d1a0a0f903e6f7e8e3b97a663ae68fc0e07d33c471a6dc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7c35f6470fb5c835c5479566adecd5bb7233e3c4abfbfa12c051463395fad610",
      "signature": {
        "s": "0x094e952cd5e0b063dfdb8acca09d04ea6f86a95f145743b4f8a4a49220c54549",
        "r": "0xac927faacf7f77bc433edcbf24372869da38f24675650c9fadab1bedf1373794",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "65878290217",
    "total": "65878290217"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "65878290217",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "38346093544"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "65878290"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZTRmZDEwNy1mMTg3LTVmMmMtYjE1Mi03NTNmNjIxNjk2N2MifQ==",
    "nonce": 5694,
    "balances": {
      "current": "12979334654475454",
      "previous": "12979400598643961"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6541e75ff1a06396ddbd84f3dbc4c9047e3b33b1",
    "nonce": 16,
    "balances": {
      "current": "65878290217",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:43:07.052Z",
  "updated": "2020-05-22T08:43:07.140Z",
  "id": "5ec7909bb0c6090011d5b034"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000f56a6ef29000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `65878290217`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`