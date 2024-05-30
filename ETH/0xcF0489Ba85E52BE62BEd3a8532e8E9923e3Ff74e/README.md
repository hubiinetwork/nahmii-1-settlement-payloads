# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcF0489Ba85E52BE62BEd3a8532e8E9923e3Ff74e`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000064ba80000000000000000000000000000000000000000000000000000000000064ba800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000064ba80000000000000000000000000000000000000000000000000000000000064ba85818818d704175eb64593f07cb02828ecbc6d5fb864eb18a69a20fd04c516bd60426b4a667aaaee3183d9739f4e4f193281a58ff9a78a0fd566190599a8caf8b3d1ace2e485176089ea6b0393c34e3d7a8f7ec676e218f603aab0f71f70d625d000000000000000000000000000000000000000000000000000000000000001c9594328dfc39d7619ac1de8b02968729b7fd292f4373aa064749f31d03385f2ef289ad8f8fda1fc94c270bfbc886a82ac779474f4ce3d7fffa2fb9778470e2ca0df5a8a623de46e2ecdf902538ab6e8afcd3ec284fcdd283e43ab82f014da750000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000042100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c97f2c86000000000000000000000000000000000000000000000000002386f2c98579ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000019c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d21500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6859324a6a4e3249354e4330335a4441324c5456684e446374595463355a69316a4e7a6b344e6d5a6a5a574978597a676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000cf0489ba85e52be62bed3a8532e8e9923e3ff74e0000000000000000000000000000000000000000000000000000000000064ba8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5818818d704175eb64593f07cb02828ecbc6d5fb864eb18a69a20fd04c516bd6",
      "signature": {
        "s": "0x3d1ace2e485176089ea6b0393c34e3d7a8f7ec676e218f603aab0f71f70d625d",
        "r": "0x0426b4a667aaaee3183d9739f4e4f193281a58ff9a78a0fd566190599a8caf8b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9594328dfc39d7619ac1de8b02968729b7fd292f4373aa064749f31d03385f2e",
      "signature": {
        "s": "0x0df5a8a623de46e2ecdf902538ab6e8afcd3ec284fcdd283e43ab82f014da750",
        "r": "0xf289ad8f8fda1fc94c270bfbc886a82ac779474f4ce3d7fffa2fb9778470e2ca",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "412584",
    "total": "412584"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "412584",
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
            "amount": "578069"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "412"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhY2JjN2I5NC03ZDA2LTVhNDctYTc5Zi1jNzk4NmZjZWIxYzgifQ==",
    "nonce": 1057,
    "balances": {
      "current": "10000001505635462",
      "previous": "10000001506048458"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcf0489ba85e52be62bed3a8532e8e9923e3ff74e",
    "nonce": 13,
    "balances": {
      "current": "412584",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:32.092Z",
  "updated": "2020-05-22T08:06:32.166Z",
  "id": "5ec78808b0c6090011d5aa2c"
}
```
* *stageAmount*: `412584`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000064ba800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000064ba80000000000000000000000000000000000000000000000000000000000064ba85818818d704175eb64593f07cb02828ecbc6d5fb864eb18a69a20fd04c516bd60426b4a667aaaee3183d9739f4e4f193281a58ff9a78a0fd566190599a8caf8b3d1ace2e485176089ea6b0393c34e3d7a8f7ec676e218f603aab0f71f70d625d000000000000000000000000000000000000000000000000000000000000001c9594328dfc39d7619ac1de8b02968729b7fd292f4373aa064749f31d03385f2ef289ad8f8fda1fc94c270bfbc886a82ac779474f4ce3d7fffa2fb9778470e2ca0df5a8a623de46e2ecdf902538ab6e8afcd3ec284fcdd283e43ab82f014da750000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000042100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c97f2c86000000000000000000000000000000000000000000000000002386f2c98579ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000019c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d21500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6859324a6a4e3249354e4330335a4441324c5456684e446374595463355a69316a4e7a6b344e6d5a6a5a574978597a676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000cf0489ba85e52be62bed3a8532e8e9923e3ff74e0000000000000000000000000000000000000000000000000000000000064ba8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5818818d704175eb64593f07cb02828ecbc6d5fb864eb18a69a20fd04c516bd6",
      "signature": {
        "s": "0x3d1ace2e485176089ea6b0393c34e3d7a8f7ec676e218f603aab0f71f70d625d",
        "r": "0x0426b4a667aaaee3183d9739f4e4f193281a58ff9a78a0fd566190599a8caf8b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9594328dfc39d7619ac1de8b02968729b7fd292f4373aa064749f31d03385f2e",
      "signature": {
        "s": "0x0df5a8a623de46e2ecdf902538ab6e8afcd3ec284fcdd283e43ab82f014da750",
        "r": "0xf289ad8f8fda1fc94c270bfbc886a82ac779474f4ce3d7fffa2fb9778470e2ca",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "412584",
    "total": "412584"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "412584",
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
            "amount": "578069"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "412"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhY2JjN2I5NC03ZDA2LTVhNDctYTc5Zi1jNzk4NmZjZWIxYzgifQ==",
    "nonce": 1057,
    "balances": {
      "current": "10000001505635462",
      "previous": "10000001506048458"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcf0489ba85e52be62bed3a8532e8e9923e3ff74e",
    "nonce": 13,
    "balances": {
      "current": "412584",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:32.092Z",
  "updated": "2020-05-22T08:06:32.166Z",
  "id": "5ec78808b0c6090011d5aa2c"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000064ba80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `412584`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``