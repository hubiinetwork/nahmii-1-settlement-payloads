# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb5E52371fF2D5e211327CFa48309C78F6A9012f4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000001336700000000000000000000000000000000000000000000000000000000000133670000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001336700000000000000000000000000000000000000000000000000000000000133670fe727a4c0da852767d0f32d6fea5dc98017ab0e78f858d2e4a89128989c2492cb33cd52a44f0e30ac35d45ed2249e79d94057396c191651352194d11b7879306e4f98bdc222d619249f38c0262622528daa52b22332af8a315999b6d8fe0c0c000000000000000000000000000000000000000000000000000000000000001b5343991a19bc9fe590cb77d72dadb35942ee99e414188785fb022f2f6d16e8036451bbdb054d87d9a194ad28608dc65383e927310b681f67271125b1b3ecb28e31455146233f42ee32d1b6ee3e2ec0397a2dd558dc626608b6f9976c8740b480000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000052a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c76826ef000000000000000000000000000000000000000000000000002386f2c7695aa400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095aa800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a44597a4d574d794e4330344d546b794c54566b4e544d744f4759774e69316c4e57517a4e325668597a55344d7a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b5e52371ff2d5e211327cfa48309c78f6a9012f40000000000000000000000000000000000000000000000000000000000013367000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0fe727a4c0da852767d0f32d6fea5dc98017ab0e78f858d2e4a89128989c2492",
      "signature": {
        "s": "0x6e4f98bdc222d619249f38c0262622528daa52b22332af8a315999b6d8fe0c0c",
        "r": "0xcb33cd52a44f0e30ac35d45ed2249e79d94057396c191651352194d11b787930",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5343991a19bc9fe590cb77d72dadb35942ee99e414188785fb022f2f6d16e803",
      "signature": {
        "s": "0x31455146233f42ee32d1b6ee3e2ec0397a2dd558dc626608b6f9976c8740b480",
        "r": "0x6451bbdb054d87d9a194ad28608dc65383e927310b681f67271125b1b3ecb28e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "78695",
    "total": "78695"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78695",
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
            "amount": "613032"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "78"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZDYzMWMyNC04MTkyLTVkNTMtOGYwNi1lNWQzN2VhYzU4MzEifQ==",
    "nonce": 1322,
    "balances": {
      "current": "10000001470572271",
      "previous": "10000001470651044"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb5e52371ff2d5e211327cfa48309c78f6a9012f4",
    "nonce": 20,
    "balances": {
      "current": "78695",
      "previous": "0"
    }
  },
  "blockNumber": "10114524",
  "created": "2020-05-22T08:08:30.879Z",
  "updated": "2020-05-22T08:08:30.950Z",
  "id": "5ec7887ee5756b00111b8117"
}
```
* *stageAmount*: `78695`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000133670000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000001336700000000000000000000000000000000000000000000000000000000000133670fe727a4c0da852767d0f32d6fea5dc98017ab0e78f858d2e4a89128989c2492cb33cd52a44f0e30ac35d45ed2249e79d94057396c191651352194d11b7879306e4f98bdc222d619249f38c0262622528daa52b22332af8a315999b6d8fe0c0c000000000000000000000000000000000000000000000000000000000000001b5343991a19bc9fe590cb77d72dadb35942ee99e414188785fb022f2f6d16e8036451bbdb054d87d9a194ad28608dc65383e927310b681f67271125b1b3ecb28e31455146233f42ee32d1b6ee3e2ec0397a2dd558dc626608b6f9976c8740b480000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55dc0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000052a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c76826ef000000000000000000000000000000000000000000000000002386f2c7695aa400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000004e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000095aa800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775a44597a4d574d794e4330344d546b794c54566b4e544d744f4759774e69316c4e57517a4e325668597a55344d7a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b5e52371ff2d5e211327cfa48309c78f6a9012f40000000000000000000000000000000000000000000000000000000000013367000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0fe727a4c0da852767d0f32d6fea5dc98017ab0e78f858d2e4a89128989c2492",
      "signature": {
        "s": "0x6e4f98bdc222d619249f38c0262622528daa52b22332af8a315999b6d8fe0c0c",
        "r": "0xcb33cd52a44f0e30ac35d45ed2249e79d94057396c191651352194d11b787930",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5343991a19bc9fe590cb77d72dadb35942ee99e414188785fb022f2f6d16e803",
      "signature": {
        "s": "0x31455146233f42ee32d1b6ee3e2ec0397a2dd558dc626608b6f9976c8740b480",
        "r": "0x6451bbdb054d87d9a194ad28608dc65383e927310b681f67271125b1b3ecb28e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "78695",
    "total": "78695"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "78695",
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
            "amount": "613032"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "78"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwZDYzMWMyNC04MTkyLTVkNTMtOGYwNi1lNWQzN2VhYzU4MzEifQ==",
    "nonce": 1322,
    "balances": {
      "current": "10000001470572271",
      "previous": "10000001470651044"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb5e52371ff2d5e211327cfa48309c78f6a9012f4",
    "nonce": 20,
    "balances": {
      "current": "78695",
      "previous": "0"
    }
  },
  "blockNumber": "10114524",
  "created": "2020-05-22T08:08:30.879Z",
  "updated": "2020-05-22T08:08:30.950Z",
  "id": "5ec7887ee5756b00111b8117"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000133670000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `78695`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``