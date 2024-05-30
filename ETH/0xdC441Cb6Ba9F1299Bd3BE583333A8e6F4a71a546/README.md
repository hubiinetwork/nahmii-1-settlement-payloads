# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdC441Cb6Ba9F1299Bd3BE583333A8e6F4a71a546`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000a467100000000000000000000000000000000000000000000000000000000000a4671000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000a467100000000000000000000000000000000000000000000000000000000000a46711894b46c199f1181b49251b1e0cfe2dcb919a0a198ecf842e35932b30ea99ae366d3abaf787a9365cc41103901c243d847608d88cf49a050891a8212c95f1ef61bd44255b323d501169f523f3b6eb56fe20d65005a92285c61191f657c50d99e000000000000000000000000000000000000000000000000000000000000001cba45a2157fefcf4ce83d7d3273d2cc5224bbec6354e3396561f2e60084e4183afd22094b3fa5731bae63df593693e75cc2eabc70602f041f395ac8dec7e4cc8c46b75fa8ce6bf17d60fb80ef74c9bc39192a48b09c6375b485b85e96f3abf0e3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000050300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ab152b000000000000000000000000000000000000000000000000002386f2c7b55e3d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002a100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009499800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a646d4d6a63344e69316a4e4751334c54566c4d6a55744f57466c4d793078596d45325a4441354f574d7a5a44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dc441cb6ba9f1299bd3be583333a8e6f4a71a54600000000000000000000000000000000000000000000000000000000000a4671000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1894b46c199f1181b49251b1e0cfe2dcb919a0a198ecf842e35932b30ea99ae3",
      "signature": {
        "s": "0x1bd44255b323d501169f523f3b6eb56fe20d65005a92285c61191f657c50d99e",
        "r": "0x66d3abaf787a9365cc41103901c243d847608d88cf49a050891a8212c95f1ef6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba45a2157fefcf4ce83d7d3273d2cc5224bbec6354e3396561f2e60084e4183a",
      "signature": {
        "s": "0x46b75fa8ce6bf17d60fb80ef74c9bc39192a48b09c6375b485b85e96f3abf0e3",
        "r": "0xfd22094b3fa5731bae63df593693e75cc2eabc70602f041f395ac8dec7e4cc8c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "673393",
    "total": "673393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "673393",
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
            "amount": "608664"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "673"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMjdmMjc4Ni1jNGQ3LTVlMjUtOWFlMy0xYmE2ZDA5OWMzZDAifQ==",
    "nonce": 1283,
    "balances": {
      "current": "10000001474958635",
      "previous": "10000001475632701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdc441cb6ba9f1299bd3be583333a8e6f4a71a546",
    "nonce": 20,
    "balances": {
      "current": "673393",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:11.230Z",
  "updated": "2020-05-22T08:08:11.300Z",
  "id": "5ec7886bb0c6090011d5aa76"
}
```
* *stageAmount*: `673393`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000a4671000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000a467100000000000000000000000000000000000000000000000000000000000a46711894b46c199f1181b49251b1e0cfe2dcb919a0a198ecf842e35932b30ea99ae366d3abaf787a9365cc41103901c243d847608d88cf49a050891a8212c95f1ef61bd44255b323d501169f523f3b6eb56fe20d65005a92285c61191f657c50d99e000000000000000000000000000000000000000000000000000000000000001cba45a2157fefcf4ce83d7d3273d2cc5224bbec6354e3396561f2e60084e4183afd22094b3fa5731bae63df593693e75cc2eabc70602f041f395ac8dec7e4cc8c46b75fa8ce6bf17d60fb80ef74c9bc39192a48b09c6375b485b85e96f3abf0e3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000050300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7ab152b000000000000000000000000000000000000000000000000002386f2c7b55e3d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000002a100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009499800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a646d4d6a63344e69316a4e4751334c54566c4d6a55744f57466c4d793078596d45325a4441354f574d7a5a44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000dc441cb6ba9f1299bd3be583333a8e6f4a71a54600000000000000000000000000000000000000000000000000000000000a4671000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1894b46c199f1181b49251b1e0cfe2dcb919a0a198ecf842e35932b30ea99ae3",
      "signature": {
        "s": "0x1bd44255b323d501169f523f3b6eb56fe20d65005a92285c61191f657c50d99e",
        "r": "0x66d3abaf787a9365cc41103901c243d847608d88cf49a050891a8212c95f1ef6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xba45a2157fefcf4ce83d7d3273d2cc5224bbec6354e3396561f2e60084e4183a",
      "signature": {
        "s": "0x46b75fa8ce6bf17d60fb80ef74c9bc39192a48b09c6375b485b85e96f3abf0e3",
        "r": "0xfd22094b3fa5731bae63df593693e75cc2eabc70602f041f395ac8dec7e4cc8c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "673393",
    "total": "673393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "673393",
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
            "amount": "608664"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "673"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMjdmMjc4Ni1jNGQ3LTVlMjUtOWFlMy0xYmE2ZDA5OWMzZDAifQ==",
    "nonce": 1283,
    "balances": {
      "current": "10000001474958635",
      "previous": "10000001475632701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdc441cb6ba9f1299bd3be583333a8e6f4a71a546",
    "nonce": 20,
    "balances": {
      "current": "673393",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:11.230Z",
  "updated": "2020-05-22T08:08:11.300Z",
  "id": "5ec7886bb0c6090011d5aa76"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000a46710000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `673393`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``