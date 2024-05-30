# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbE266dFC8b6F886E6AF5c994ac6EE9f60F97cBaf`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001d800000000000000000000000000000000000000000000000000000000000001d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001d800000000000000000000000000000000000000000000000000000000000001d80cc7ff52384b46681a6bf22f5d7e3c179e83779ca8f6d5f30bbceed61447e2f854857beff4ef770241d7d1cebef123d7e31d4adc2502951abb92e0bef32ce3c638c9c7e802b8fdd2e97183309024dcd2262f57f1eb0cee1ccdfa7b6395e24921000000000000000000000000000000000000000000000000000000000000001c366a3971e76c41a2332fe839c955ad0a2703b36167de4b33c11cfeb0b11560dad4291eeef8a0c0942511dc5465fc6c9e9ad14e9cef202fbd309436d94170a2e512623ddf5843c7608ab59255538fa2b7886c8e5648e2666fc94a9e70cf76e153000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b6e68000000000000000000000000000000000000000000000000002386f2bc3b704100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a4533597a45315953316b4e6d45334c54566d4d6a49744f54526c4f5330314e7a49354e574a6a4e6a5531597a676966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000be266dfc8b6f886e6af5c994ac6ee9f60f97cbaf00000000000000000000000000000000000000000000000000000000000001d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0cc7ff52384b46681a6bf22f5d7e3c179e83779ca8f6d5f30bbceed61447e2f8",
      "signature": {
        "s": "0x38c9c7e802b8fdd2e97183309024dcd2262f57f1eb0cee1ccdfa7b6395e24921",
        "r": "0x54857beff4ef770241d7d1cebef123d7e31d4adc2502951abb92e0bef32ce3c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x366a3971e76c41a2332fe839c955ad0a2703b36167de4b33c11cfeb0b11560da",
      "signature": {
        "s": "0x12623ddf5843c7608ab59255538fa2b7886c8e5648e2666fc94a9e70cf76e153",
        "r": "0xd4291eeef8a0c0942511dc5465fc6c9e9ad14e9cef202fbd309436d94170a2e5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "472",
    "total": "472"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "472",
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
            "amount": "800046"
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
    "data": "eyJyZWYiOiIwNjE3YzE1YS1kNmE3LTVmMjItOTRlOS01NzI5NWJjNjU1YzgifQ==",
    "nonce": 2411,
    "balances": {
      "current": "10000001283092072",
      "previous": "10000001283092545"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbe266dfc8b6f886e6af5c994ac6ee9f60f97cbaf",
    "nonce": 4,
    "balances": {
      "current": "472",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:21.175Z",
  "updated": "2020-05-22T08:16:21.247Z",
  "id": "5ec78a55b0c6090011d5abf2"
}
```
* *stageAmount*: `472`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001d800000000000000000000000000000000000000000000000000000000000001d80cc7ff52384b46681a6bf22f5d7e3c179e83779ca8f6d5f30bbceed61447e2f854857beff4ef770241d7d1cebef123d7e31d4adc2502951abb92e0bef32ce3c638c9c7e802b8fdd2e97183309024dcd2262f57f1eb0cee1ccdfa7b6395e24921000000000000000000000000000000000000000000000000000000000000001c366a3971e76c41a2332fe839c955ad0a2703b36167de4b33c11cfeb0b11560dad4291eeef8a0c0942511dc5465fc6c9e9ad14e9cef202fbd309436d94170a2e512623ddf5843c7608ab59255538fa2b7886c8e5648e2666fc94a9e70cf76e153000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b6e68000000000000000000000000000000000000000000000000002386f2bc3b704100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e6a4533597a45315953316b4e6d45334c54566d4d6a49744f54526c4f5330314e7a49354e574a6a4e6a5531597a676966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000be266dfc8b6f886e6af5c994ac6ee9f60f97cbaf00000000000000000000000000000000000000000000000000000000000001d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0cc7ff52384b46681a6bf22f5d7e3c179e83779ca8f6d5f30bbceed61447e2f8",
      "signature": {
        "s": "0x38c9c7e802b8fdd2e97183309024dcd2262f57f1eb0cee1ccdfa7b6395e24921",
        "r": "0x54857beff4ef770241d7d1cebef123d7e31d4adc2502951abb92e0bef32ce3c6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x366a3971e76c41a2332fe839c955ad0a2703b36167de4b33c11cfeb0b11560da",
      "signature": {
        "s": "0x12623ddf5843c7608ab59255538fa2b7886c8e5648e2666fc94a9e70cf76e153",
        "r": "0xd4291eeef8a0c0942511dc5465fc6c9e9ad14e9cef202fbd309436d94170a2e5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "472",
    "total": "472"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "472",
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
            "amount": "800046"
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
    "data": "eyJyZWYiOiIwNjE3YzE1YS1kNmE3LTVmMjItOTRlOS01NzI5NWJjNjU1YzgifQ==",
    "nonce": 2411,
    "balances": {
      "current": "10000001283092072",
      "previous": "10000001283092545"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbe266dfc8b6f886e6af5c994ac6ee9f60f97cbaf",
    "nonce": 4,
    "balances": {
      "current": "472",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:21.175Z",
  "updated": "2020-05-22T08:16:21.247Z",
  "id": "5ec78a55b0c6090011d5abf2"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001d80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `472`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``