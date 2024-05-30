# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA21230939e997678c679899c3D43f3990733CBF3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000014af00000000000000000000000000000000000000000000000000000000000014af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000014af00000000000000000000000000000000000000000000000000000000000014afa421b4f713a09f8e1af0051b7f2f424b54f4d44d931ee8cb2558beb5daa8eb5387c060b428fd07ba82aab2e52dbd42623ed424c14af4e727f56fc4ef686be51a5314a344378b9b62a1e29bbbb4f6538de6d5b2a87729efda305af7f17b569f67000000000000000000000000000000000000000000000000000000000000001cd856f0ba97c96d8397c9134f5bcdb4f5ead395a77508636491490edae27768751fcbec65f0f35e812e11c6bd83db2ca9b2094301e1ecf11c3fc064aa22ff0f861190d7cc52b0dd95722a14c394a791cd8d7e1e311dff79607025b55777d85b14000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000034a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae087a8000000000000000000000000000000000000000000000000002386f2cae09c5c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000877e600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a595459795a54466b5a43316a5932557a4c54557a4f446374596a5a6b595331684d6d59784e6a457a4e44466c4d47596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a21230939e997678c679899c3d43f3990733cbf300000000000000000000000000000000000000000000000000000000000014af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa421b4f713a09f8e1af0051b7f2f424b54f4d44d931ee8cb2558beb5daa8eb53",
      "signature": {
        "s": "0x5314a344378b9b62a1e29bbbb4f6538de6d5b2a87729efda305af7f17b569f67",
        "r": "0x87c060b428fd07ba82aab2e52dbd42623ed424c14af4e727f56fc4ef686be51a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd856f0ba97c96d8397c9134f5bcdb4f5ead395a77508636491490edae2776875",
      "signature": {
        "s": "0x1190d7cc52b0dd95722a14c394a791cd8d7e1e311dff79607025b55777d85b14",
        "r": "0x1fcbec65f0f35e812e11c6bd83db2ca9b2094301e1ecf11c3fc064aa22ff0f86",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5295",
    "total": "5295"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5295",
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
            "amount": "554982"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYTYyZTFkZC1jY2UzLTUzODctYjZkYS1hMmYxNjEzNDFlMGYifQ==",
    "nonce": 842,
    "balances": {
      "current": "10000001528793000",
      "previous": "10000001528798300"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa21230939e997678c679899c3d43f3990733cbf3",
    "nonce": 20,
    "balances": {
      "current": "5295",
      "previous": "0"
    }
  },
  "blockNumber": "10114513",
  "created": "2020-05-22T08:04:59.914Z",
  "updated": "2020-05-22T08:04:59.988Z",
  "id": "5ec787ab005df800101bc32f"
}
```
* *stageAmount*: `5295`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000014af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000014af00000000000000000000000000000000000000000000000000000000000014afa421b4f713a09f8e1af0051b7f2f424b54f4d44d931ee8cb2558beb5daa8eb5387c060b428fd07ba82aab2e52dbd42623ed424c14af4e727f56fc4ef686be51a5314a344378b9b62a1e29bbbb4f6538de6d5b2a87729efda305af7f17b569f67000000000000000000000000000000000000000000000000000000000000001cd856f0ba97c96d8397c9134f5bcdb4f5ead395a77508636491490edae27768751fcbec65f0f35e812e11c6bd83db2ca9b2094301e1ecf11c3fc064aa22ff0f861190d7cc52b0dd95722a14c394a791cd8d7e1e311dff79607025b55777d85b14000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000034a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cae087a8000000000000000000000000000000000000000000000000002386f2cae09c5c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000877e600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a595459795a54466b5a43316a5932557a4c54557a4f446374596a5a6b595331684d6d59784e6a457a4e44466c4d47596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a21230939e997678c679899c3d43f3990733cbf300000000000000000000000000000000000000000000000000000000000014af000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa421b4f713a09f8e1af0051b7f2f424b54f4d44d931ee8cb2558beb5daa8eb53",
      "signature": {
        "s": "0x5314a344378b9b62a1e29bbbb4f6538de6d5b2a87729efda305af7f17b569f67",
        "r": "0x87c060b428fd07ba82aab2e52dbd42623ed424c14af4e727f56fc4ef686be51a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd856f0ba97c96d8397c9134f5bcdb4f5ead395a77508636491490edae2776875",
      "signature": {
        "s": "0x1190d7cc52b0dd95722a14c394a791cd8d7e1e311dff79607025b55777d85b14",
        "r": "0x1fcbec65f0f35e812e11c6bd83db2ca9b2094301e1ecf11c3fc064aa22ff0f86",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5295",
    "total": "5295"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5295",
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
            "amount": "554982"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjYTYyZTFkZC1jY2UzLTUzODctYjZkYS1hMmYxNjEzNDFlMGYifQ==",
    "nonce": 842,
    "balances": {
      "current": "10000001528793000",
      "previous": "10000001528798300"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa21230939e997678c679899c3d43f3990733cbf3",
    "nonce": 20,
    "balances": {
      "current": "5295",
      "previous": "0"
    }
  },
  "blockNumber": "10114513",
  "created": "2020-05-22T08:04:59.914Z",
  "updated": "2020-05-22T08:04:59.988Z",
  "id": "5ec787ab005df800101bc32f"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000014af0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5295`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``