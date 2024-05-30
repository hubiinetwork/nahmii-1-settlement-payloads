# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4b24Dfd4d637769aAb90ddcdcF50A9D8112C4307`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000002386f26fc10b620000000000000000000000000000000000000000000000000000000000000b6200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000b620000000000000000000000000000000000000000000000000000000000000b626c5aa406da39494701f0317e48e6297a5f5e58b6e23cd7d363bc86ffffbb1fcb4861c8080672bbf6adc348aa48762aff9685a5789cdc60f33c28df5c9ef071fe67d182b3364dcd412e415d6925d0a3ab612ee5f4acaf6cbf98d949c0db81c6b5000000000000000000000000000000000000000000000000000000000000001b0820c411189abd57395d531e898388362758e4e2819cfd889d6a960c7a3bd3b6a0af3b74e7ce3ce552d6e22b913f44f796cd825cabe428277c605fc722febf156444592da0ed2112cfc26fd6202167e4deeba624f00011a83c12b772e97ec143000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2eb3822c9000000000000000000000000000000000000000000000000002386f2eb382e2d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000337400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e44526a4d3259334d533034593259794c5455315a6d55744f4441314e43316d59574a6c5a6d46684e445a6b4d546b6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004b24dfd4d637769aab90ddcdcf50a9d8112c4307000000000000000000000000000000000000000000000000002386f26fc10b62000000000000000000000000000000000000000000000000002386f26fc1000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c5aa406da39494701f0317e48e6297a5f5e58b6e23cd7d363bc86ffffbb1fcb",
      "signature": {
        "s": "0x67d182b3364dcd412e415d6925d0a3ab612ee5f4acaf6cbf98d949c0db81c6b5",
        "r": "0x4861c8080672bbf6adc348aa48762aff9685a5789cdc60f33c28df5c9ef071fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0820c411189abd57395d531e898388362758e4e2819cfd889d6a960c7a3bd3b6",
      "signature": {
        "s": "0x6444592da0ed2112cfc26fd6202167e4deeba624f00011a83c12b772e97ec143",
        "r": "0xa0af3b74e7ce3ce552d6e22b913f44f796cd825cabe428277c605fc722febf15",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2914",
    "total": "2914"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2914",
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
            "amount": "13172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNDRjM2Y3MS04Y2YyLTU1ZmUtODA1NC1mYWJlZmFhNDZkMTkifQ==",
    "nonce": 27,
    "balances": {
      "current": "10000002071405257",
      "previous": "10000002071408173"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4b24dfd4d637769aab90ddcdcf50a9d8112c4307",
    "nonce": 20,
    "balances": {
      "current": "10000000000002914",
      "previous": "10000000000000000"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:15.097Z",
  "updated": "2020-05-22T07:59:15.177Z",
  "id": "5ec78653b0c6090011d5a8dc"
}
```
* *stageAmount*: `10000000000002914`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000b6200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000b620000000000000000000000000000000000000000000000000000000000000b626c5aa406da39494701f0317e48e6297a5f5e58b6e23cd7d363bc86ffffbb1fcb4861c8080672bbf6adc348aa48762aff9685a5789cdc60f33c28df5c9ef071fe67d182b3364dcd412e415d6925d0a3ab612ee5f4acaf6cbf98d949c0db81c6b5000000000000000000000000000000000000000000000000000000000000001b0820c411189abd57395d531e898388362758e4e2819cfd889d6a960c7a3bd3b6a0af3b74e7ce3ce552d6e22b913f44f796cd825cabe428277c605fc722febf156444592da0ed2112cfc26fd6202167e4deeba624f00011a83c12b772e97ec143000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2eb3822c9000000000000000000000000000000000000000000000000002386f2eb382e2d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000337400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e44526a4d3259334d533034593259794c5455315a6d55744f4441314e43316d59574a6c5a6d46684e445a6b4d546b6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000004b24dfd4d637769aab90ddcdcf50a9d8112c4307000000000000000000000000000000000000000000000000002386f26fc10b62000000000000000000000000000000000000000000000000002386f26fc1000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6c5aa406da39494701f0317e48e6297a5f5e58b6e23cd7d363bc86ffffbb1fcb",
      "signature": {
        "s": "0x67d182b3364dcd412e415d6925d0a3ab612ee5f4acaf6cbf98d949c0db81c6b5",
        "r": "0x4861c8080672bbf6adc348aa48762aff9685a5789cdc60f33c28df5c9ef071fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0820c411189abd57395d531e898388362758e4e2819cfd889d6a960c7a3bd3b6",
      "signature": {
        "s": "0x6444592da0ed2112cfc26fd6202167e4deeba624f00011a83c12b772e97ec143",
        "r": "0xa0af3b74e7ce3ce552d6e22b913f44f796cd825cabe428277c605fc722febf15",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2914",
    "total": "2914"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2914",
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
            "amount": "13172"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNDRjM2Y3MS04Y2YyLTU1ZmUtODA1NC1mYWJlZmFhNDZkMTkifQ==",
    "nonce": 27,
    "balances": {
      "current": "10000002071405257",
      "previous": "10000002071408173"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4b24dfd4d637769aab90ddcdcf50a9d8112c4307",
    "nonce": 20,
    "balances": {
      "current": "10000000000002914",
      "previous": "10000000000000000"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:15.097Z",
  "updated": "2020-05-22T07:59:15.177Z",
  "id": "5ec78653b0c6090011d5a8dc"
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
0x0f200f9b000000000000000000000000000000000000000000000000002386f26fc10b620000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10000000000002914`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``