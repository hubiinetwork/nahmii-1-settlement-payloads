# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7ebDc6eEa1ac7a0ec3Df52beb1d9a4e4f61C0085`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000eb85950000000000000000000000000000000000000000000000000000000000eb859500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000eb85950000000000000000000000000000000000000000000000000000000000eb8595ad92947f10348ea112614c11bbd09d5f2b62f371bba5e7ae947fb316fe075f8876ce0c4ab85b5ac7d47bde2a2329739ae46f491ba5f805f4d39c9f7d93e797f81e8f41a2ee52285aba58806148a2756180999b2579530801f8bafc189160ee1c000000000000000000000000000000000000000000000000000000000000001c753dd44ce2fb539fbc02de6981e5bc5a5467717da82e8fe6c4f01678ba60bedddd849a6f8dace7b582a242f9266108ed286cf73e4e7310cd0ad288e10d6dbce3412d60bc20136c3e97b86a1b2a2b4ebb4e9c2fecdacf53aac8778fb91531db5a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2e001a69c000000000000000000000000000000000000000000000000002386f2e0ed687c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000003c4b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003118a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a546b784e7a63794d5330794d474a684c5455355a574d744f5451314d7930795954426d595451334d544d304d6a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007ebdc6eea1ac7a0ec3df52beb1d9a4e4f61c00850000000000000000000000000000000000000000000000000000000000eb8595000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad92947f10348ea112614c11bbd09d5f2b62f371bba5e7ae947fb316fe075f88",
      "signature": {
        "s": "0x1e8f41a2ee52285aba58806148a2756180999b2579530801f8bafc189160ee1c",
        "r": "0x76ce0c4ab85b5ac7d47bde2a2329739ae46f491ba5f805f4d39c9f7d93e797f8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x753dd44ce2fb539fbc02de6981e5bc5a5467717da82e8fe6c4f01678ba60bedd",
      "signature": {
        "s": "0x412d60bc20136c3e97b86a1b2a2b4ebb4e9c2fecdacf53aac8778fb91531db5a",
        "r": "0xdd849a6f8dace7b582a242f9266108ed286cf73e4e7310cd0ad288e10d6dbce3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15435157",
    "total": "15435157"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15435157",
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
            "amount": "201098"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "15435"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTkxNzcyMS0yMGJhLTU5ZWMtOTQ1My0yYTBmYTQ3MTM0MjMifQ==",
    "nonce": 41,
    "balances": {
      "current": "10000001883285148",
      "previous": "10000001898735740"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7ebdc6eea1ac7a0ec3df52beb1d9a4e4f61c0085",
    "nonce": 20,
    "balances": {
      "current": "15435157",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:19.953Z",
  "updated": "2020-05-22T07:59:20.024Z",
  "id": "5ec78657b0c6090011d5a8e0"
}
```
* *stageAmount*: `15435157`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000eb859500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000eb85950000000000000000000000000000000000000000000000000000000000eb8595ad92947f10348ea112614c11bbd09d5f2b62f371bba5e7ae947fb316fe075f8876ce0c4ab85b5ac7d47bde2a2329739ae46f491ba5f805f4d39c9f7d93e797f81e8f41a2ee52285aba58806148a2756180999b2579530801f8bafc189160ee1c000000000000000000000000000000000000000000000000000000000000001c753dd44ce2fb539fbc02de6981e5bc5a5467717da82e8fe6c4f01678ba60bedddd849a6f8dace7b582a242f9266108ed286cf73e4e7310cd0ad288e10d6dbce3412d60bc20136c3e97b86a1b2a2b4ebb4e9c2fecdacf53aac8778fb91531db5a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2e001a69c000000000000000000000000000000000000000000000000002386f2e0ed687c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000003c4b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003118a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a546b784e7a63794d5330794d474a684c5455355a574d744f5451314d7930795954426d595451334d544d304d6a4d6966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000007ebdc6eea1ac7a0ec3df52beb1d9a4e4f61c00850000000000000000000000000000000000000000000000000000000000eb8595000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xad92947f10348ea112614c11bbd09d5f2b62f371bba5e7ae947fb316fe075f88",
      "signature": {
        "s": "0x1e8f41a2ee52285aba58806148a2756180999b2579530801f8bafc189160ee1c",
        "r": "0x76ce0c4ab85b5ac7d47bde2a2329739ae46f491ba5f805f4d39c9f7d93e797f8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x753dd44ce2fb539fbc02de6981e5bc5a5467717da82e8fe6c4f01678ba60bedd",
      "signature": {
        "s": "0x412d60bc20136c3e97b86a1b2a2b4ebb4e9c2fecdacf53aac8778fb91531db5a",
        "r": "0xdd849a6f8dace7b582a242f9266108ed286cf73e4e7310cd0ad288e10d6dbce3",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15435157",
    "total": "15435157"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15435157",
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
            "amount": "201098"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "15435"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTkxNzcyMS0yMGJhLTU5ZWMtOTQ1My0yYTBmYTQ3MTM0MjMifQ==",
    "nonce": 41,
    "balances": {
      "current": "10000001883285148",
      "previous": "10000001898735740"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7ebdc6eea1ac7a0ec3df52beb1d9a4e4f61c0085",
    "nonce": 20,
    "balances": {
      "current": "15435157",
      "previous": "0"
    }
  },
  "blockNumber": "10114486",
  "created": "2020-05-22T07:59:19.953Z",
  "updated": "2020-05-22T07:59:20.024Z",
  "id": "5ec78657b0c6090011d5a8e0"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000eb85950000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15435157`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``