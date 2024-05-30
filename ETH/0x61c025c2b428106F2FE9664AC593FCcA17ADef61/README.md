# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x61c025c2b428106F2FE9664AC593FCcA17ADef61`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000e179000000000000000000000000000000000000000000000000000000000000e1790000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000e179000000000000000000000000000000000000000000000000000000000000e179e2fe55c096f70f7bf13dc3e2095538f82799c0fffbf0a8c7cafe0f563601b5a7363c9a9ce060962acdb610510470fabbba99e11a0d1fc78ff7d57718300122a43ec0f345c2d74321ed111fa5c91ba234cbdaea1fb5b4bd19bf270698821ec455000000000000000000000000000000000000000000000000000000000000001cb38065d55a91fe82dd274102444aa0561fb6d5bd219b46308228c6fd49ad1d7e2728c611055baf49bce0e186fec664edf05c836435fd2bff4e48073fb38851b114aa2ac0b9638545a28fd416762b136a39aeee85df53514a83a988b6e63c4c18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000021a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb3b7acd000000000000000000000000000000000000000000000000002386f2cb3c5c7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008611b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e3251335a544a6c5969316a595463314c54566a596a5174595749784e53316c5a546b30596d4a6c4e6a4a6d4d574d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061c025c2b428106f2fe9664ac593fcca17adef61000000000000000000000000000000000000000000000000000000000000e179000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe2fe55c096f70f7bf13dc3e2095538f82799c0fffbf0a8c7cafe0f563601b5a7",
      "signature": {
        "s": "0x3ec0f345c2d74321ed111fa5c91ba234cbdaea1fb5b4bd19bf270698821ec455",
        "r": "0x363c9a9ce060962acdb610510470fabbba99e11a0d1fc78ff7d57718300122a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb38065d55a91fe82dd274102444aa0561fb6d5bd219b46308228c6fd49ad1d7e",
      "signature": {
        "s": "0x14aa2ac0b9638545a28fd416762b136a39aeee85df53514a83a988b6e63c4c18",
        "r": "0x2728c611055baf49bce0e186fec664edf05c836435fd2bff4e48073fb38851b1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "57721",
    "total": "57721"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "57721",
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
            "amount": "549147"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "57"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3N2Q3ZTJlYi1jYTc1LTVjYjQtYWIxNS1lZTk0YmJlNjJmMWMifQ==",
    "nonce": 538,
    "balances": {
      "current": "10000001534753485",
      "previous": "10000001534811263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61c025c2b428106f2fe9664ac593fcca17adef61",
    "nonce": 20,
    "balances": {
      "current": "57721",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:48.425Z",
  "updated": "2020-05-22T08:02:48.489Z",
  "id": "5ec78728005df800101bc2c6"
}
```
* *stageAmount*: `57721`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000e1790000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000e179000000000000000000000000000000000000000000000000000000000000e179e2fe55c096f70f7bf13dc3e2095538f82799c0fffbf0a8c7cafe0f563601b5a7363c9a9ce060962acdb610510470fabbba99e11a0d1fc78ff7d57718300122a43ec0f345c2d74321ed111fa5c91ba234cbdaea1fb5b4bd19bf270698821ec455000000000000000000000000000000000000000000000000000000000000001cb38065d55a91fe82dd274102444aa0561fb6d5bd219b46308228c6fd49ad1d7e2728c611055baf49bce0e186fec664edf05c836435fd2bff4e48073fb38851b114aa2ac0b9638545a28fd416762b136a39aeee85df53514a83a988b6e63c4c18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000021a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb3b7acd000000000000000000000000000000000000000000000000002386f2cb3c5c7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008611b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e3251335a544a6c5969316a595463314c54566a596a5174595749784e53316c5a546b30596d4a6c4e6a4a6d4d574d6966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061c025c2b428106f2fe9664ac593fcca17adef61000000000000000000000000000000000000000000000000000000000000e179000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe2fe55c096f70f7bf13dc3e2095538f82799c0fffbf0a8c7cafe0f563601b5a7",
      "signature": {
        "s": "0x3ec0f345c2d74321ed111fa5c91ba234cbdaea1fb5b4bd19bf270698821ec455",
        "r": "0x363c9a9ce060962acdb610510470fabbba99e11a0d1fc78ff7d57718300122a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb38065d55a91fe82dd274102444aa0561fb6d5bd219b46308228c6fd49ad1d7e",
      "signature": {
        "s": "0x14aa2ac0b9638545a28fd416762b136a39aeee85df53514a83a988b6e63c4c18",
        "r": "0x2728c611055baf49bce0e186fec664edf05c836435fd2bff4e48073fb38851b1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "57721",
    "total": "57721"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "57721",
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
            "amount": "549147"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "57"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3N2Q3ZTJlYi1jYTc1LTVjYjQtYWIxNS1lZTk0YmJlNjJmMWMifQ==",
    "nonce": 538,
    "balances": {
      "current": "10000001534753485",
      "previous": "10000001534811263"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61c025c2b428106f2fe9664ac593fcca17adef61",
    "nonce": 20,
    "balances": {
      "current": "57721",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:48.425Z",
  "updated": "2020-05-22T08:02:48.489Z",
  "id": "5ec78728005df800101bc2c6"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000e1790000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `57721`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``