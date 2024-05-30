# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x13b406088117F4003e95Ce40d953e757874d3FFe`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000039d000000000000000000000000000000000000000000000000000000000000039d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000039d000000000000000000000000000000000000000000000000000000000000039dbd110febe505259c927cc9d7bd1cd7e4a470055d0e26e0fc3a004034c304d7ef411d12eedc6249046bb951c25c06ce738f7f3b14617a40c8f1747cf42fd48c5a5a49e41395de8b2cbd7c4c63faac537da926b13b6d4512276ff9928f8080c333000000000000000000000000000000000000000000000000000000000000001b2d4851ad867fd54df020c9400a9046801461644f9caaf6932f0433f55dcc2758360afbc2e27ea738df01f37007730199430f3e6e2663b5a3a3e7b0f91859ab68285a2b19163e5204620ae9a4ee51830bd5126703ddd0d999e52bbf76db165786000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caae3295000000000000000000000000000000000000000000000000002386f2caae363300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884a600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e32566b4d5751335969316a5954566c4c5455794e6a59744f444e6a4d79307a4d54557a597a4d355a6d51794e444d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000013b406088117f4003e95ce40d953e757874d3ffe000000000000000000000000000000000000000000000000000000000000039d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbd110febe505259c927cc9d7bd1cd7e4a470055d0e26e0fc3a004034c304d7ef",
      "signature": {
        "s": "0x5a49e41395de8b2cbd7c4c63faac537da926b13b6d4512276ff9928f8080c333",
        "r": "0x411d12eedc6249046bb951c25c06ce738f7f3b14617a40c8f1747cf42fd48c5a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d4851ad867fd54df020c9400a9046801461644f9caaf6932f0433f55dcc2758",
      "signature": {
        "s": "0x285a2b19163e5204620ae9a4ee51830bd5126703ddd0d999e52bbf76db165786",
        "r": "0x360afbc2e27ea738df01f37007730199430f3e6e2663b5a3a3e7b0f91859ab68",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "925",
    "total": "925"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "925",
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
            "amount": "558246"
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
    "data": "eyJyZWYiOiIwN2VkMWQ3Yi1jYTVlLTUyNjYtODNjMy0zMTUzYzM5ZmQyNDMifQ==",
    "nonce": 926,
    "balances": {
      "current": "10000001525494421",
      "previous": "10000001525495347"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x13b406088117f4003e95ce40d953e757874d3ffe",
    "nonce": 20,
    "balances": {
      "current": "925",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:29.369Z",
  "updated": "2020-05-22T08:05:29.437Z",
  "id": "5ec787c9005df800101bc34c"
}
```
* *stageAmount*: `925`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000039d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000039d000000000000000000000000000000000000000000000000000000000000039dbd110febe505259c927cc9d7bd1cd7e4a470055d0e26e0fc3a004034c304d7ef411d12eedc6249046bb951c25c06ce738f7f3b14617a40c8f1747cf42fd48c5a5a49e41395de8b2cbd7c4c63faac537da926b13b6d4512276ff9928f8080c333000000000000000000000000000000000000000000000000000000000000001b2d4851ad867fd54df020c9400a9046801461644f9caaf6932f0433f55dcc2758360afbc2e27ea738df01f37007730199430f3e6e2663b5a3a3e7b0f91859ab68285a2b19163e5204620ae9a4ee51830bd5126703ddd0d999e52bbf76db165786000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000039e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caae3295000000000000000000000000000000000000000000000000002386f2caae363300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000884a600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e32566b4d5751335969316a5954566c4c5455794e6a59744f444e6a4d79307a4d54557a597a4d355a6d51794e444d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000013b406088117f4003e95ce40d953e757874d3ffe000000000000000000000000000000000000000000000000000000000000039d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbd110febe505259c927cc9d7bd1cd7e4a470055d0e26e0fc3a004034c304d7ef",
      "signature": {
        "s": "0x5a49e41395de8b2cbd7c4c63faac537da926b13b6d4512276ff9928f8080c333",
        "r": "0x411d12eedc6249046bb951c25c06ce738f7f3b14617a40c8f1747cf42fd48c5a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2d4851ad867fd54df020c9400a9046801461644f9caaf6932f0433f55dcc2758",
      "signature": {
        "s": "0x285a2b19163e5204620ae9a4ee51830bd5126703ddd0d999e52bbf76db165786",
        "r": "0x360afbc2e27ea738df01f37007730199430f3e6e2663b5a3a3e7b0f91859ab68",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "925",
    "total": "925"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "925",
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
            "amount": "558246"
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
    "data": "eyJyZWYiOiIwN2VkMWQ3Yi1jYTVlLTUyNjYtODNjMy0zMTUzYzM5ZmQyNDMifQ==",
    "nonce": 926,
    "balances": {
      "current": "10000001525494421",
      "previous": "10000001525495347"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x13b406088117f4003e95ce40d953e757874d3ffe",
    "nonce": 20,
    "balances": {
      "current": "925",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:05:29.369Z",
  "updated": "2020-05-22T08:05:29.437Z",
  "id": "5ec787c9005df800101bc34c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000039d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `925`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``