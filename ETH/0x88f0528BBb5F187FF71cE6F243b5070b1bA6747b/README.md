# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x88f0528BBb5F187FF71cE6F243b5070b1bA6747b`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000129200000000000000000000000000000000000000000000000000000000000012920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000129200000000000000000000000000000000000000000000000000000000000012925bc7ba5561c08126818887a3c61ad6bad42ae24f7f0ff60ae32170b5847fca98f4729c8b1f02783bab0b927e1726f80ee7dbddcf0bb6b85370367ae6b0aa1cde3738d015bc8c10326c841d9438b99c869492317e9f04799c67ec59735d9b5b0d000000000000000000000000000000000000000000000000000000000000001b92bc039cf3a18798f34cf9bcb9321e3f17db2d0ddfbb1c1e50033806f7bb7993c880f0c8da43b25e84154f58e5decbfaf586f9a6a5b6ae12155016315a83a5fd26a21e21b49b9486eb7461e114be87517cad46553d8c49ac3e8112d57b5a8554000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b7fc8000000000000000000000000000000000000000000000000002386f2bc3b925e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595445304e5745315953307a4f4745324c5455334e6a4d7459575a6d4e43316b4f575269596d51774d7a466c4e6d456966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000088f0528bbb5f187ff71ce6f243b5070b1ba6747b0000000000000000000000000000000000000000000000000000000000001292000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5bc7ba5561c08126818887a3c61ad6bad42ae24f7f0ff60ae32170b5847fca98",
      "signature": {
        "s": "0x3738d015bc8c10326c841d9438b99c869492317e9f04799c67ec59735d9b5b0d",
        "r": "0xf4729c8b1f02783bab0b927e1726f80ee7dbddcf0bb6b85370367ae6b0aa1cde",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92bc039cf3a18798f34cf9bcb9321e3f17db2d0ddfbb1c1e50033806f7bb7993",
      "signature": {
        "s": "0x26a21e21b49b9486eb7461e114be87517cad46553d8c49ac3e8112d57b5a8554",
        "r": "0xc880f0c8da43b25e84154f58e5decbfaf586f9a6a5b6ae12155016315a83a5fd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4754",
    "total": "4754"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4754",
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
            "amount": "800042"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTE0NWE1YS0zOGE2LTU3NjMtYWZmNC1kOWRiYmQwMzFlNmEifQ==",
    "nonce": 2407,
    "balances": {
      "current": "10000001283096520",
      "previous": "10000001283101278"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x88f0528bbb5f187ff71ce6f243b5070b1ba6747b",
    "nonce": 7,
    "balances": {
      "current": "4754",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:18.338Z",
  "updated": "2020-05-22T08:16:18.492Z",
  "id": "5ec78a52b0c6090011d5abf0"
}
```
* *stageAmount*: `4754`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000012920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000129200000000000000000000000000000000000000000000000000000000000012925bc7ba5561c08126818887a3c61ad6bad42ae24f7f0ff60ae32170b5847fca98f4729c8b1f02783bab0b927e1726f80ee7dbddcf0bb6b85370367ae6b0aa1cde3738d015bc8c10326c841d9438b99c869492317e9f04799c67ec59735d9b5b0d000000000000000000000000000000000000000000000000000000000000001b92bc039cf3a18798f34cf9bcb9321e3f17db2d0ddfbb1c1e50033806f7bb7993c880f0c8da43b25e84154f58e5decbfaf586f9a6a5b6ae12155016315a83a5fd26a21e21b49b9486eb7461e114be87517cad46553d8c49ac3e8112d57b5a8554000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b7fc8000000000000000000000000000000000000000000000000002386f2bc3b925e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935595445304e5745315953307a4f4745324c5455334e6a4d7459575a6d4e43316b4f575269596d51774d7a466c4e6d456966513d3d000000000000000000000000000000000000000000000000000000000000000700000000000000000000000088f0528bbb5f187ff71ce6f243b5070b1ba6747b0000000000000000000000000000000000000000000000000000000000001292000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5bc7ba5561c08126818887a3c61ad6bad42ae24f7f0ff60ae32170b5847fca98",
      "signature": {
        "s": "0x3738d015bc8c10326c841d9438b99c869492317e9f04799c67ec59735d9b5b0d",
        "r": "0xf4729c8b1f02783bab0b927e1726f80ee7dbddcf0bb6b85370367ae6b0aa1cde",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x92bc039cf3a18798f34cf9bcb9321e3f17db2d0ddfbb1c1e50033806f7bb7993",
      "signature": {
        "s": "0x26a21e21b49b9486eb7461e114be87517cad46553d8c49ac3e8112d57b5a8554",
        "r": "0xc880f0c8da43b25e84154f58e5decbfaf586f9a6a5b6ae12155016315a83a5fd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4754",
    "total": "4754"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4754",
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
            "amount": "800042"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "4"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YTE0NWE1YS0zOGE2LTU3NjMtYWZmNC1kOWRiYmQwMzFlNmEifQ==",
    "nonce": 2407,
    "balances": {
      "current": "10000001283096520",
      "previous": "10000001283101278"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x88f0528bbb5f187ff71ce6f243b5070b1ba6747b",
    "nonce": 7,
    "balances": {
      "current": "4754",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:18.338Z",
  "updated": "2020-05-22T08:16:18.492Z",
  "id": "5ec78a52b0c6090011d5abf0"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000012920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4754`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``