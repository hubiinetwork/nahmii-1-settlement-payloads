# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x19f23f2cF92035f39488b4A12D3d848B2eeC3aA5`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f2600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f26d37336dc6bb3230fddd8aef191b4f1f25f76ffb23fbd8bb7c0189a3f9fbd4e261dfedbb83a31d5a290d9bed26f5ff34426de36efeed8e869ad04e11e01d3afd92daa225054e8861b316982882ea5b7e74f91550caef99a44da7a2e2420f48585000000000000000000000000000000000000000000000000000000000000001b9410208c5c744cd8dea6dd8143236336e4653bf0d56afcea8bb38b3b61b397bcd1eebdd765799b25fffd4d5884426c0f1b185570441e75af561ea613bc3c9b4956884df682508c6f547199c355ca210921e2d2388d9eb0e9cb71663615cb8561000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000068400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5d7f1b0000000000000000000000000000000000000000000000000002386f2c5d880fa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c09f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5455354e7a63344d6930304d6a59334c54566a59324d744f474e6d4d533030595449335a5751354e6a63344d47596966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000019f23f2cf92035f39488b4a12d3d848b2eec3aa50000000000000000000000000000000000000000000000000000000000008f26000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd37336dc6bb3230fddd8aef191b4f1f25f76ffb23fbd8bb7c0189a3f9fbd4e26",
      "signature": {
        "s": "0x2daa225054e8861b316982882ea5b7e74f91550caef99a44da7a2e2420f48585",
        "r": "0x1dfedbb83a31d5a290d9bed26f5ff34426de36efeed8e869ad04e11e01d3afd9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9410208c5c744cd8dea6dd8143236336e4653bf0d56afcea8bb38b3b61b397bc",
      "signature": {
        "s": "0x56884df682508c6f547199c355ca210921e2d2388d9eb0e9cb71663615cb8561",
        "r": "0xd1eebdd765799b25fffd4d5884426c0f1b185570441e75af561ea613bc3c9b49",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36646",
    "total": "36646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36646",
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
            "amount": "639135"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OTU5Nzc4Mi00MjY3LTVjY2MtOGNmMS00YTI3ZWQ5Njc4MGYifQ==",
    "nonce": 1668,
    "balances": {
      "current": "10000001444344240",
      "previous": "10000001444380922"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x19f23f2cf92035f39488b4a12d3d848b2eec3aa5",
    "nonce": 20,
    "balances": {
      "current": "36646",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:16.720Z",
  "updated": "2020-05-22T08:11:16.791Z",
  "id": "5ec78924005df800101bc454"
}
```
* *stageAmount*: `36646`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000008f2600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000008f26d37336dc6bb3230fddd8aef191b4f1f25f76ffb23fbd8bb7c0189a3f9fbd4e261dfedbb83a31d5a290d9bed26f5ff34426de36efeed8e869ad04e11e01d3afd92daa225054e8861b316982882ea5b7e74f91550caef99a44da7a2e2420f48585000000000000000000000000000000000000000000000000000000000000001b9410208c5c744cd8dea6dd8143236336e4653bf0d56afcea8bb38b3b61b397bcd1eebdd765799b25fffd4d5884426c0f1b185570441e75af561ea613bc3c9b4956884df682508c6f547199c355ca210921e2d2388d9eb0e9cb71663615cb8561000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000068400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5d7f1b0000000000000000000000000000000000000000000000000002386f2c5d880fa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009c09f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5455354e7a63344d6930304d6a59334c54566a59324d744f474e6d4d533030595449335a5751354e6a63344d47596966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000019f23f2cf92035f39488b4a12d3d848b2eec3aa50000000000000000000000000000000000000000000000000000000000008f26000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd37336dc6bb3230fddd8aef191b4f1f25f76ffb23fbd8bb7c0189a3f9fbd4e26",
      "signature": {
        "s": "0x2daa225054e8861b316982882ea5b7e74f91550caef99a44da7a2e2420f48585",
        "r": "0x1dfedbb83a31d5a290d9bed26f5ff34426de36efeed8e869ad04e11e01d3afd9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9410208c5c744cd8dea6dd8143236336e4653bf0d56afcea8bb38b3b61b397bc",
      "signature": {
        "s": "0x56884df682508c6f547199c355ca210921e2d2388d9eb0e9cb71663615cb8561",
        "r": "0xd1eebdd765799b25fffd4d5884426c0f1b185570441e75af561ea613bc3c9b49",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36646",
    "total": "36646"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36646",
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
            "amount": "639135"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "36"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OTU5Nzc4Mi00MjY3LTVjY2MtOGNmMS00YTI3ZWQ5Njc4MGYifQ==",
    "nonce": 1668,
    "balances": {
      "current": "10000001444344240",
      "previous": "10000001444380922"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x19f23f2cf92035f39488b4a12d3d848b2eec3aa5",
    "nonce": 20,
    "balances": {
      "current": "36646",
      "previous": "0"
    }
  },
  "blockNumber": "10114537",
  "created": "2020-05-22T08:11:16.720Z",
  "updated": "2020-05-22T08:11:16.791Z",
  "id": "5ec78924005df800101bc454"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000008f260000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36646`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``