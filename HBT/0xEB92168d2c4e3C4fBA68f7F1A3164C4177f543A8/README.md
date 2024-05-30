# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEB92168d2c4e3C4fBA68f7F1A3164C4177f543A8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000600611e900000000000000000000000000000000000000000000000000000000600611e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000600611e900000000000000000000000000000000000000000000000000000000600611e9101902c70281bb3f0b4f9784267faa0e59f8f0fa4b8801f2873e4187c932eb1e96b8f82a3ed38171a4bec2c9bdcf53dc8358945f9846d9df702329b476756d780c29ed984e953adb32ec90a4dfdb66c332c64d641e4be2d33a7347d854c4b090000000000000000000000000000000000000000000000000000000000000001b75a0688c99cb1ff91da8e4afc7b1a0a54247e19f480db7603c62ffa0a5bd1456ce011fe0db3eb1a073705504d048f8f4373548d8d3419d5353cc6efade79616f3e10a8dc89732a63bbc78b155d81dd5e584ac0ee19a9b029c8e012dc78d582ed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000171600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b386ca2fe34000000000000000000000000000000000000000000000000002e1b38ccc1a51f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000189502000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094a4a9cdb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463325a474d7a597930324d5468684c5456694f47457459574e6b4f4331695a57457a5954646b4e6d457a4d7a416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000eb92168d2c4e3c4fba68f7f1a3164c4177f543a800000000000000000000000000000000000000000000000000000000600611e9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x101902c70281bb3f0b4f9784267faa0e59f8f0fa4b8801f2873e4187c932eb1e",
      "signature": {
        "s": "0x0c29ed984e953adb32ec90a4dfdb66c332c64d641e4be2d33a7347d854c4b090",
        "r": "0x96b8f82a3ed38171a4bec2c9bdcf53dc8358945f9846d9df702329b476756d78",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x75a0688c99cb1ff91da8e4afc7b1a0a54247e19f480db7603c62ffa0a5bd1456",
      "signature": {
        "s": "0x3e10a8dc89732a63bbc78b155d81dd5e584ac0ee19a9b029c8e012dc78d582ed",
        "r": "0xce011fe0db3eb1a073705504d048f8f4373548d8d3419d5353cc6efade79616f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1611010537",
    "total": "1611010537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1611010537",
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
            "amount": "39901109467"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1611010"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOTc2ZGMzYy02MThhLTViOGEtYWNkOC1iZWEzYTdkNmEzMzAifQ==",
    "nonce": 5910,
    "balances": {
      "current": "12977778083429940",
      "previous": "12977779696051487"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb92168d2c4e3c4fba68f7f1a3164c4177f543a8",
    "nonce": 22,
    "balances": {
      "current": "1611010537",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:44:59.882Z",
  "updated": "2020-05-22T08:44:59.958Z",
  "id": "5ec7910bb0c6090011d5b06e"
}
```
* *stageAmount*: `1611010537`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000600611e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000600611e900000000000000000000000000000000000000000000000000000000600611e9101902c70281bb3f0b4f9784267faa0e59f8f0fa4b8801f2873e4187c932eb1e96b8f82a3ed38171a4bec2c9bdcf53dc8358945f9846d9df702329b476756d780c29ed984e953adb32ec90a4dfdb66c332c64d641e4be2d33a7347d854c4b090000000000000000000000000000000000000000000000000000000000000001b75a0688c99cb1ff91da8e4afc7b1a0a54247e19f480db7603c62ffa0a5bd1456ce011fe0db3eb1a073705504d048f8f4373548d8d3419d5353cc6efade79616f3e10a8dc89732a63bbc78b155d81dd5e584ac0ee19a9b029c8e012dc78d582ed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56770000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000171600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b386ca2fe34000000000000000000000000000000000000000000000000002e1b38ccc1a51f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000189502000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094a4a9cdb000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463325a474d7a597930324d5468684c5456694f47457459574e6b4f4331695a57457a5954646b4e6d457a4d7a416966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000eb92168d2c4e3c4fba68f7f1a3164c4177f543a800000000000000000000000000000000000000000000000000000000600611e9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x101902c70281bb3f0b4f9784267faa0e59f8f0fa4b8801f2873e4187c932eb1e",
      "signature": {
        "s": "0x0c29ed984e953adb32ec90a4dfdb66c332c64d641e4be2d33a7347d854c4b090",
        "r": "0x96b8f82a3ed38171a4bec2c9bdcf53dc8358945f9846d9df702329b476756d78",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x75a0688c99cb1ff91da8e4afc7b1a0a54247e19f480db7603c62ffa0a5bd1456",
      "signature": {
        "s": "0x3e10a8dc89732a63bbc78b155d81dd5e584ac0ee19a9b029c8e012dc78d582ed",
        "r": "0xce011fe0db3eb1a073705504d048f8f4373548d8d3419d5353cc6efade79616f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1611010537",
    "total": "1611010537"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1611010537",
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
            "amount": "39901109467"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1611010"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOTc2ZGMzYy02MThhLTViOGEtYWNkOC1iZWEzYTdkNmEzMzAifQ==",
    "nonce": 5910,
    "balances": {
      "current": "12977778083429940",
      "previous": "12977779696051487"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb92168d2c4e3c4fba68f7f1a3164c4177f543a8",
    "nonce": 22,
    "balances": {
      "current": "1611010537",
      "previous": "0"
    }
  },
  "blockNumber": "10114679",
  "created": "2020-05-22T08:44:59.882Z",
  "updated": "2020-05-22T08:44:59.958Z",
  "id": "5ec7910bb0c6090011d5b06e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000600611e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1611010537`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`