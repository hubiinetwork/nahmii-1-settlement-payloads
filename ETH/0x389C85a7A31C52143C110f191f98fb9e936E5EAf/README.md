# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x389C85a7A31C52143C110f191f98fb9e936E5EAf`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4addc43c0d4b9296b3dfb0776997640936e0f5efd068d67816f8289a9bc13c87a7972e25692a11d0b0b17cf19b6402f216d2fdea7b7cad02c9d08852c1635210f17c3da4745112dc44498ae3426b61e478dc9de6d681d60dcfb893e19e4f3cdf7000000000000000000000000000000000000000000000000000000000000001cfef5755b570c7112932d00c46898bb4401979aec0e23f7b54e20d00e54e09abcc673b76573bdd14c2ebbc0873459684d0ca227af930a68154a0d4a94ff877036788d8ee6715cb7756166a93df108d1a4f4d5d068ec053c7e1486738f17fa0a3d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a9efc000000000000000000000000000000000000000000000000002386f2c74ad6de00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009622900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f4459334d5745354d69316d595455354c5455794e7a55744f546b7a5a4330354d3246684e5455784e6a59324e324d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000389c85a7a31c52143c110f191f98fb9e936e5eaf00000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaddc43c0d4b9296b3dfb0776997640936e0f5efd068d67816f8289a9bc13c87a",
      "signature": {
        "s": "0x17c3da4745112dc44498ae3426b61e478dc9de6d681d60dcfb893e19e4f3cdf7",
        "r": "0x7972e25692a11d0b0b17cf19b6402f216d2fdea7b7cad02c9d08852c1635210f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfef5755b570c7112932d00c46898bb4401979aec0e23f7b54e20d00e54e09abc",
      "signature": {
        "s": "0x788d8ee6715cb7756166a93df108d1a4f4d5d068ec053c7e1486738f17fa0a3d",
        "r": "0xc673b76573bdd14c2ebbc0873459684d0ca227af930a68154a0d4a94ff877036",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14292",
    "total": "14292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14292",
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
            "amount": "614953"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "14"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxODY3MWE5Mi1mYTU5LTUyNzUtOTkzZC05M2FhNTUxNjY2N2MifQ==",
    "nonce": 1356,
    "balances": {
      "current": "10000001468636924",
      "previous": "10000001468651230"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x389c85a7a31c52143c110f191f98fb9e936e5eaf",
    "nonce": 20,
    "balances": {
      "current": "14292",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:44.220Z",
  "updated": "2020-05-22T08:08:44.312Z",
  "id": "5ec7888ce5756b00111b8121"
}
```
* *stageAmount*: `14292`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000037d400000000000000000000000000000000000000000000000000000000000037d4addc43c0d4b9296b3dfb0776997640936e0f5efd068d67816f8289a9bc13c87a7972e25692a11d0b0b17cf19b6402f216d2fdea7b7cad02c9d08852c1635210f17c3da4745112dc44498ae3426b61e478dc9de6d681d60dcfb893e19e4f3cdf7000000000000000000000000000000000000000000000000000000000000001cfef5755b570c7112932d00c46898bb4401979aec0e23f7b54e20d00e54e09abcc673b76573bdd14c2ebbc0873459684d0ca227af930a68154a0d4a94ff877036788d8ee6715cb7756166a93df108d1a4f4d5d068ec053c7e1486738f17fa0a3d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74a9efc000000000000000000000000000000000000000000000000002386f2c74ad6de00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009622900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f4459334d5745354d69316d595455354c5455794e7a55744f546b7a5a4330354d3246684e5455784e6a59324e324d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000389c85a7a31c52143c110f191f98fb9e936e5eaf00000000000000000000000000000000000000000000000000000000000037d4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaddc43c0d4b9296b3dfb0776997640936e0f5efd068d67816f8289a9bc13c87a",
      "signature": {
        "s": "0x17c3da4745112dc44498ae3426b61e478dc9de6d681d60dcfb893e19e4f3cdf7",
        "r": "0x7972e25692a11d0b0b17cf19b6402f216d2fdea7b7cad02c9d08852c1635210f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfef5755b570c7112932d00c46898bb4401979aec0e23f7b54e20d00e54e09abc",
      "signature": {
        "s": "0x788d8ee6715cb7756166a93df108d1a4f4d5d068ec053c7e1486738f17fa0a3d",
        "r": "0xc673b76573bdd14c2ebbc0873459684d0ca227af930a68154a0d4a94ff877036",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14292",
    "total": "14292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14292",
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
            "amount": "614953"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "14"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxODY3MWE5Mi1mYTU5LTUyNzUtOTkzZC05M2FhNTUxNjY2N2MifQ==",
    "nonce": 1356,
    "balances": {
      "current": "10000001468636924",
      "previous": "10000001468651230"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x389c85a7a31c52143c110f191f98fb9e936e5eaf",
    "nonce": 20,
    "balances": {
      "current": "14292",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:44.220Z",
  "updated": "2020-05-22T08:08:44.312Z",
  "id": "5ec7888ce5756b00111b8121"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000037d40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14292`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``