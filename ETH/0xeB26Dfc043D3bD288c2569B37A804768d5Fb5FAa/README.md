# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xeB26Dfc043D3bD288c2569B37A804768d5Fb5FAa`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000138f9e0000000000000000000000000000000000000000000000000000000000138f9e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000138f9e0000000000000000000000000000000000000000000000000000000000138f9e788d564a25e546c21203acba6e49e63d4e4cc8a9883be897cb71a73b55ba34f118fec3f76a4853de75433e2e2b5db2e60d278a200a60ed73c569144bf5075a8170787709055cec990b8001ab4f4dc015bbb48971ac9420db91bb9cabf5833c44000000000000000000000000000000000000000000000000000000000000001c00c00b4ce579563be8c72cf6fbc28f76cf30e1e6899111021717a6d9d7b903e6db9d13c226fc9ffc7607462058d4dfb6d4c3049b522cc58d04bde16c5c13ddd21e44b54be39ab5db96bcfa5144c4c790cd40d701435c4f31996c33800796a2a8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000006e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d59e770d000000000000000000000000000000000000000000000000002386f2d5b20bac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000050100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b98000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e6d566c5a6d4d334f4330324d6d46684c5455314e5745744f4759774e5330774d3255304d4455344e4755305a6a516966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000eb26dfc043d3bd288c2569b37a804768d5fb5faa0000000000000000000000000000000000000000000000000000000000138f9e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x788d564a25e546c21203acba6e49e63d4e4cc8a9883be897cb71a73b55ba34f1",
      "signature": {
        "s": "0x70787709055cec990b8001ab4f4dc015bbb48971ac9420db91bb9cabf5833c44",
        "r": "0x18fec3f76a4853de75433e2e2b5db2e60d278a200a60ed73c569144bf5075a81",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x00c00b4ce579563be8c72cf6fbc28f76cf30e1e6899111021717a6d9d7b903e6",
      "signature": {
        "s": "0x1e44b54be39ab5db96bcfa5144c4c790cd40d701435c4f31996c33800796a2a8",
        "r": "0xdb9d13c226fc9ffc7607462058d4dfb6d4c3049b522cc58d04bde16c5c13ddd2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1281950",
    "total": "1281950"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1281950",
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
            "amount": "375168"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1281"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNmVlZmM3OC02MmFhLTU1NWEtOGYwNS0wM2U0MDU4NGU0ZjQifQ==",
    "nonce": 110,
    "balances": {
      "current": "10000001709012749",
      "previous": "10000001710295980"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb26dfc043d3bd288c2569b37a804768d5fb5faa",
    "nonce": 19,
    "balances": {
      "current": "1281950",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:39.097Z",
  "updated": "2020-05-22T07:59:39.163Z",
  "id": "5ec7866be5756b00111b7f93"
}
```
* *stageAmount*: `1281950`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000138f9e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000138f9e0000000000000000000000000000000000000000000000000000000000138f9e788d564a25e546c21203acba6e49e63d4e4cc8a9883be897cb71a73b55ba34f118fec3f76a4853de75433e2e2b5db2e60d278a200a60ed73c569144bf5075a8170787709055cec990b8001ab4f4dc015bbb48971ac9420db91bb9cabf5833c44000000000000000000000000000000000000000000000000000000000000001c00c00b4ce579563be8c72cf6fbc28f76cf30e1e6899111021717a6d9d7b903e6db9d13c226fc9ffc7607462058d4dfb6d4c3049b522cc58d04bde16c5c13ddd21e44b54be39ab5db96bcfa5144c4c790cd40d701435c4f31996c33800796a2a8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000006e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d59e770d000000000000000000000000000000000000000000000000002386f2d5b20bac00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000050100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005b98000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e6d566c5a6d4d334f4330324d6d46684c5455314e5745744f4759774e5330774d3255304d4455344e4755305a6a516966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000eb26dfc043d3bd288c2569b37a804768d5fb5faa0000000000000000000000000000000000000000000000000000000000138f9e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x788d564a25e546c21203acba6e49e63d4e4cc8a9883be897cb71a73b55ba34f1",
      "signature": {
        "s": "0x70787709055cec990b8001ab4f4dc015bbb48971ac9420db91bb9cabf5833c44",
        "r": "0x18fec3f76a4853de75433e2e2b5db2e60d278a200a60ed73c569144bf5075a81",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x00c00b4ce579563be8c72cf6fbc28f76cf30e1e6899111021717a6d9d7b903e6",
      "signature": {
        "s": "0x1e44b54be39ab5db96bcfa5144c4c790cd40d701435c4f31996c33800796a2a8",
        "r": "0xdb9d13c226fc9ffc7607462058d4dfb6d4c3049b522cc58d04bde16c5c13ddd2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1281950",
    "total": "1281950"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1281950",
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
            "amount": "375168"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1281"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNmVlZmM3OC02MmFhLTU1NWEtOGYwNS0wM2U0MDU4NGU0ZjQifQ==",
    "nonce": 110,
    "balances": {
      "current": "10000001709012749",
      "previous": "10000001710295980"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xeb26dfc043d3bd288c2569b37a804768d5fb5faa",
    "nonce": 19,
    "balances": {
      "current": "1281950",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:39.097Z",
  "updated": "2020-05-22T07:59:39.163Z",
  "id": "5ec7866be5756b00111b7f93"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000138f9e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1281950`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``