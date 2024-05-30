# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x61d07F4DFEc6b3073A387547843e9775f092442B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000035f2a4319d00000000000000000000000000000000000000000000000000000035f2a4319d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000035f2a4319d00000000000000000000000000000000000000000000000000000035f2a4319dd6f1f689e59cf372ac71c39455942e8aeeb802287546fc79e79dccae34498dd823cb18f6f0030778eae82815ea8c402c3f4a4f222c7854975c973661d55fcbdb5cb8ebb598f7babb0884052d4a0846268cf040f6126766fb3da90624e9ec77a8000000000000000000000000000000000000000000000000000000000000001ba60e9116484be5a0abe3234499be7eb5b3b6e3d420838941d7df1cbf330d4965c9440610e720c5eca52be4b085d8b4a1608cfaa22a21dc47e37abd0baa3291855d430086603d7c7e2631c45bfc0da5aff90d309f983fb1c593d06978f80443ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568c000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018c600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e195a9334c39a000000000000000000000000000000000000000000000000002e199093a87b6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000dcf8631000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c47fa8ad000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a63774e7a417a5969307a4e4467794c5455324f4745744f4449774d6930344d324d35596a6b304d6a4e6d5a57556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000061d07f4dfec6b3073a387547843e9775f092442b00000000000000000000000000000000000000000000000000000035f2a4319d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd6f1f689e59cf372ac71c39455942e8aeeb802287546fc79e79dccae34498dd8",
      "signature": {
        "s": "0x5cb8ebb598f7babb0884052d4a0846268cf040f6126766fb3da90624e9ec77a8",
        "r": "0x23cb18f6f0030778eae82815ea8c402c3f4a4f222c7854975c973661d55fcbdb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa60e9116484be5a0abe3234499be7eb5b3b6e3d420838941d7df1cbf330d4965",
      "signature": {
        "s": "0x5d430086603d7c7e2631c45bfc0da5aff90d309f983fb1c593d06978f80443ff",
        "r": "0xc9440610e720c5eca52be4b085d8b4a1608cfaa22a21dc47e37abd0baa329185",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "231704113565",
    "total": "231704113565"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "231704113565",
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
            "amount": "41951406253"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "231704113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMjcwNzAzYi0zNDgyLTU2OGEtODIwMi04M2M5Yjk0MjNmZWUifQ==",
    "nonce": 6342,
    "balances": {
      "current": "12975725736149914",
      "previous": "12975957671967592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61d07f4dfec6b3073a387547843e9775f092442b",
    "nonce": 22,
    "balances": {
      "current": "231704113565",
      "previous": "0"
    }
  },
  "blockNumber": "10114700",
  "created": "2020-05-22T08:48:20.406Z",
  "updated": "2020-05-22T08:48:20.479Z",
  "id": "5ec791d4e5756b00111b8791"
}
```
* *stageAmount*: `231704113565`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000035f2a4319d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000035f2a4319d00000000000000000000000000000000000000000000000000000035f2a4319dd6f1f689e59cf372ac71c39455942e8aeeb802287546fc79e79dccae34498dd823cb18f6f0030778eae82815ea8c402c3f4a4f222c7854975c973661d55fcbdb5cb8ebb598f7babb0884052d4a0846268cf040f6126766fb3da90624e9ec77a8000000000000000000000000000000000000000000000000000000000000001ba60e9116484be5a0abe3234499be7eb5b3b6e3d420838941d7df1cbf330d4965c9440610e720c5eca52be4b085d8b4a1608cfaa22a21dc47e37abd0baa3291855d430086603d7c7e2631c45bfc0da5aff90d309f983fb1c593d06978f80443ff000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568c000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018c600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e195a9334c39a000000000000000000000000000000000000000000000000002e199093a87b6800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000dcf8631000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c47fa8ad000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d6a63774e7a417a5969307a4e4467794c5455324f4745744f4449774d6930344d324d35596a6b304d6a4e6d5a57556966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000061d07f4dfec6b3073a387547843e9775f092442b00000000000000000000000000000000000000000000000000000035f2a4319d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd6f1f689e59cf372ac71c39455942e8aeeb802287546fc79e79dccae34498dd8",
      "signature": {
        "s": "0x5cb8ebb598f7babb0884052d4a0846268cf040f6126766fb3da90624e9ec77a8",
        "r": "0x23cb18f6f0030778eae82815ea8c402c3f4a4f222c7854975c973661d55fcbdb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa60e9116484be5a0abe3234499be7eb5b3b6e3d420838941d7df1cbf330d4965",
      "signature": {
        "s": "0x5d430086603d7c7e2631c45bfc0da5aff90d309f983fb1c593d06978f80443ff",
        "r": "0xc9440610e720c5eca52be4b085d8b4a1608cfaa22a21dc47e37abd0baa329185",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "231704113565",
    "total": "231704113565"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "231704113565",
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
            "amount": "41951406253"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "231704113"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMjcwNzAzYi0zNDgyLTU2OGEtODIwMi04M2M5Yjk0MjNmZWUifQ==",
    "nonce": 6342,
    "balances": {
      "current": "12975725736149914",
      "previous": "12975957671967592"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61d07f4dfec6b3073a387547843e9775f092442b",
    "nonce": 22,
    "balances": {
      "current": "231704113565",
      "previous": "0"
    }
  },
  "blockNumber": "10114700",
  "created": "2020-05-22T08:48:20.406Z",
  "updated": "2020-05-22T08:48:20.479Z",
  "id": "5ec791d4e5756b00111b8791"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000035f2a4319d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `231704113565`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`