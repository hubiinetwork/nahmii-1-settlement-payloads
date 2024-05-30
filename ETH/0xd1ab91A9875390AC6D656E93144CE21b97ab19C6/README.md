# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd1ab91A9875390AC6D656E93144CE21b97ab19C6`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000042be00000000000000000000000000000000000000000000000000000000000042be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000042be00000000000000000000000000000000000000000000000000000000000042bec847963346905390126fc5e786b3a82f485d5c4be260787f190acf5cd5245c5688bd74fb70720e0b276453becfe2420d421c70301b226363d2527a89b6cab9bf4d340ec15f8d093dabe2a2dccf02b9d2f3046c31def741655e136d8a4fd90cfd000000000000000000000000000000000000000000000000000000000000001b2e336c8b51d247340dc333b4aa7eb4e553ed7336db977e6363af302b45b538da37be6cd8f32390e4712e41648e0411fff71bddc1e4ede5cca27ed7ee2309c0d67305a9bf78448176dd5f35039e734e685e6ef3f3adfff8692416b209bf56c32d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000076600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3f937b2000000000000000000000000000000000000000000000000002386f2c3f97a8100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000110000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a3ab300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5449354e7a41334f4330304e5451774c5456685a5463744f444d304e5330794f44457a4e54426a4e546b794f54596966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000d1ab91a9875390ac6d656e93144ce21b97ab19c600000000000000000000000000000000000000000000000000000000000042be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc847963346905390126fc5e786b3a82f485d5c4be260787f190acf5cd5245c56",
      "signature": {
        "s": "0x4d340ec15f8d093dabe2a2dccf02b9d2f3046c31def741655e136d8a4fd90cfd",
        "r": "0x88bd74fb70720e0b276453becfe2420d421c70301b226363d2527a89b6cab9bf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2e336c8b51d247340dc333b4aa7eb4e553ed7336db977e6363af302b45b538da",
      "signature": {
        "s": "0x7305a9bf78448176dd5f35039e734e685e6ef3f3adfff8692416b209bf56c32d",
        "r": "0x37be6cd8f32390e4712e41648e0411fff71bddc1e4ede5cca27ed7ee2309c0d6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "17086",
    "total": "17086"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17086",
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
            "amount": "670387"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "17"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNTI5NzA3OC00NTQwLTVhZTctODM0NS0yODEzNTBjNTkyOTYifQ==",
    "nonce": 1894,
    "balances": {
      "current": "10000001412970418",
      "previous": "10000001412987521"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd1ab91a9875390ac6d656e93144ce21b97ab19c6",
    "nonce": 14,
    "balances": {
      "current": "17086",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:54.479Z",
  "updated": "2020-05-22T08:12:55.635Z",
  "id": "5ec78986e5756b00111b81d5"
}
```
* *stageAmount*: `17086`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000042be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000042be00000000000000000000000000000000000000000000000000000000000042bec847963346905390126fc5e786b3a82f485d5c4be260787f190acf5cd5245c5688bd74fb70720e0b276453becfe2420d421c70301b226363d2527a89b6cab9bf4d340ec15f8d093dabe2a2dccf02b9d2f3046c31def741655e136d8a4fd90cfd000000000000000000000000000000000000000000000000000000000000001b2e336c8b51d247340dc333b4aa7eb4e553ed7336db977e6363af302b45b538da37be6cd8f32390e4712e41648e0411fff71bddc1e4ede5cca27ed7ee2309c0d67305a9bf78448176dd5f35039e734e685e6ef3f3adfff8692416b209bf56c32d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000076600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3f937b2000000000000000000000000000000000000000000000000002386f2c3f97a8100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000110000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a3ab300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e5449354e7a41334f4330304e5451774c5456685a5463744f444d304e5330794f44457a4e54426a4e546b794f54596966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000d1ab91a9875390ac6d656e93144ce21b97ab19c600000000000000000000000000000000000000000000000000000000000042be000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc847963346905390126fc5e786b3a82f485d5c4be260787f190acf5cd5245c56",
      "signature": {
        "s": "0x4d340ec15f8d093dabe2a2dccf02b9d2f3046c31def741655e136d8a4fd90cfd",
        "r": "0x88bd74fb70720e0b276453becfe2420d421c70301b226363d2527a89b6cab9bf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2e336c8b51d247340dc333b4aa7eb4e553ed7336db977e6363af302b45b538da",
      "signature": {
        "s": "0x7305a9bf78448176dd5f35039e734e685e6ef3f3adfff8692416b209bf56c32d",
        "r": "0x37be6cd8f32390e4712e41648e0411fff71bddc1e4ede5cca27ed7ee2309c0d6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "17086",
    "total": "17086"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "17086",
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
            "amount": "670387"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "17"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNTI5NzA3OC00NTQwLTVhZTctODM0NS0yODEzNTBjNTkyOTYifQ==",
    "nonce": 1894,
    "balances": {
      "current": "10000001412970418",
      "previous": "10000001412987521"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd1ab91a9875390ac6d656e93144ce21b97ab19c6",
    "nonce": 14,
    "balances": {
      "current": "17086",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:54.479Z",
  "updated": "2020-05-22T08:12:55.635Z",
  "id": "5ec78986e5756b00111b81d5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000042be0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `17086`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``