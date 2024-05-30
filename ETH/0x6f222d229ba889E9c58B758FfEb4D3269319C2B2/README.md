# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6f222d229ba889E9c58B758FfEb4D3269319C2B2`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728f18c8f2c9ad0ccf62e55517cebe71dcc8efe5e00560c23fa363fd108d17b2c4e405abe703991b01fc6940c3fffbc27b16ec3dff5fc3bfe8d8ab5250b1f942f866ea6cb478c3885789ed71689c21f53376c63c240aacc878a0a5848df459f6884000000000000000000000000000000000000000000000000000000000000001c4d88a968a08ff27d1bc708f19d73d85967d0b4d6d91f441a4d1d3821c210f3b6aa0b6af98ad60416556e4d7e6468dbe7e6e7930e71b116b4dad03f678bd0cf0d0ed16c34bb12f36a3884c68fa029369c1b9650ae3d0a521f7b26406a06326b38000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3d000b6000000000000000000000000000000000000000000000000002386f2c3d007df00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a452400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325954566b596a68695a69316b4e6d45794c54566a5a6d5174596a42685979303459574e684d54637a4e6d517a5a47596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000006f222d229ba889e9c58b758ffeb4d3269319c2b20000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf18c8f2c9ad0ccf62e55517cebe71dcc8efe5e00560c23fa363fd108d17b2c4e",
      "signature": {
        "s": "0x6ea6cb478c3885789ed71689c21f53376c63c240aacc878a0a5848df459f6884",
        "r": "0x405abe703991b01fc6940c3fffbc27b16ec3dff5fc3bfe8d8ab5250b1f942f86",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4d88a968a08ff27d1bc708f19d73d85967d0b4d6d91f441a4d1d3821c210f3b6",
      "signature": {
        "s": "0x0ed16c34bb12f36a3884c68fa029369c1b9650ae3d0a521f7b26406a06326b38",
        "r": "0xaa0b6af98ad60416556e4d7e6468dbe7e6e7930e71b116b4dad03f678bd0cf0d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1832",
    "total": "1832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1832",
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
            "amount": "673060"
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
    "data": "eyJyZWYiOiI2YTVkYjhiZi1kNmEyLTVjZmQtYjBhYy04YWNhMTczNmQzZGYifQ==",
    "nonce": 1962,
    "balances": {
      "current": "10000001410269366",
      "previous": "10000001410271199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f222d229ba889e9c58b758ffeb4d3269319c2b2",
    "nonce": 20,
    "balances": {
      "current": "1832",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:24.839Z",
  "updated": "2020-05-22T08:13:24.915Z",
  "id": "5ec789a4005df800101bc4b7"
}
```
* *stageAmount*: `1832`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000728f18c8f2c9ad0ccf62e55517cebe71dcc8efe5e00560c23fa363fd108d17b2c4e405abe703991b01fc6940c3fffbc27b16ec3dff5fc3bfe8d8ab5250b1f942f866ea6cb478c3885789ed71689c21f53376c63c240aacc878a0a5848df459f6884000000000000000000000000000000000000000000000000000000000000001c4d88a968a08ff27d1bc708f19d73d85967d0b4d6d91f441a4d1d3821c210f3b6aa0b6af98ad60416556e4d7e6468dbe7e6e7930e71b116b4dad03f678bd0cf0d0ed16c34bb12f36a3884c68fa029369c1b9650ae3d0a521f7b26406a06326b38000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007aa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3d000b6000000000000000000000000000000000000000000000000002386f2c3d007df00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a452400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949325954566b596a68695a69316b4e6d45794c54566a5a6d5174596a42685979303459574e684d54637a4e6d517a5a47596966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000006f222d229ba889e9c58b758ffeb4d3269319c2b20000000000000000000000000000000000000000000000000000000000000728000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf18c8f2c9ad0ccf62e55517cebe71dcc8efe5e00560c23fa363fd108d17b2c4e",
      "signature": {
        "s": "0x6ea6cb478c3885789ed71689c21f53376c63c240aacc878a0a5848df459f6884",
        "r": "0x405abe703991b01fc6940c3fffbc27b16ec3dff5fc3bfe8d8ab5250b1f942f86",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4d88a968a08ff27d1bc708f19d73d85967d0b4d6d91f441a4d1d3821c210f3b6",
      "signature": {
        "s": "0x0ed16c34bb12f36a3884c68fa029369c1b9650ae3d0a521f7b26406a06326b38",
        "r": "0xaa0b6af98ad60416556e4d7e6468dbe7e6e7930e71b116b4dad03f678bd0cf0d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1832",
    "total": "1832"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1832",
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
            "amount": "673060"
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
    "data": "eyJyZWYiOiI2YTVkYjhiZi1kNmEyLTVjZmQtYjBhYy04YWNhMTczNmQzZGYifQ==",
    "nonce": 1962,
    "balances": {
      "current": "10000001410269366",
      "previous": "10000001410271199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f222d229ba889e9c58b758ffeb4d3269319c2b2",
    "nonce": 20,
    "balances": {
      "current": "1832",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:24.839Z",
  "updated": "2020-05-22T08:13:24.915Z",
  "id": "5ec789a4005df800101bc4b7"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000007280000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1832`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``