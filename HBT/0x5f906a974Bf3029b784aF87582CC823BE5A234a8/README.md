# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5f906a974Bf3029b784aF87582CC823BE5A234a8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000000000000000000000000000000000018a29c08f0aae21f46bdd6d71593193cdf877300d3fc54f2a43dc7c17b420ffb51cb0b9b4854e89ffd610db704df2c8225c0712a17728ae506cfc6347195ad14506e4ab1a4f4ccc30a7ca2e7fb8a44941b6aaba6badc06327980f3ad844c2b24374c8a31b000000000000000000000000000000000000000000000000000000000000001b07461f48b2a3007d87de7ccc3f3f3e76539854c4c1ace50d0c741c561fcdf3557a39d0f9261062605a55d3bff300a9ba737c0c66f76102974a2cc98e0bbcec897a0d4b531ea7af92b0e256d62d7479eddc51d7285f1736df50b29f6bf529f081000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139a0c98687a000000000000000000000000000000000000000000000000002e139b972710e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3d16b2cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a6d45774d3245334e4330354e7a597a4c5455784e5449744f54646c597930785954457a59324535597a4a6b596d596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005f906a974bf3029b784af87582cc823be5a234a8000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0aae21f46bdd6d71593193cdf877300d3fc54f2a43dc7c17b420ffb51cb0b9b4",
      "signature": {
        "s": "0x4f4ccc30a7ca2e7fb8a44941b6aaba6badc06327980f3ad844c2b24374c8a31b",
        "r": "0x854e89ffd610db704df2c8225c0712a17728ae506cfc6347195ad14506e4ab1a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x07461f48b2a3007d87de7ccc3f3f3e76539854c4c1ace50d0c741c561fcdf355",
      "signature": {
        "s": "0x7a0d4b531ea7af92b0e256d62d7479eddc51d7285f1736df50b29f6bf529f081",
        "r": "0x7a39d0f9261062605a55d3bff300a9ba737c0c66f76102974a2cc98e0bbcec89",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6612959375",
    "total": "6612959375"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612959375",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "48269537999"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612959"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZmEwM2E3NC05NzYzLTUxNTItOTdlYy0xYTEzY2E5YzJkYmYifQ==",
    "nonce": 7214,
    "balances": {
      "current": "12969401285896314",
      "previous": "12969407905468648"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f906a974bf3029b784af87582cc823be5a234a8",
    "nonce": 22,
    "balances": {
      "current": "6612959375",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:05.440Z",
  "updated": "2020-05-22T08:55:05.507Z",
  "id": "5ec79369005df800101bcba9"
}
```
* *stageAmount*: `6612959375`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000000000000000000000000000000000018a29c08f0aae21f46bdd6d71593193cdf877300d3fc54f2a43dc7c17b420ffb51cb0b9b4854e89ffd610db704df2c8225c0712a17728ae506cfc6347195ad14506e4ab1a4f4ccc30a7ca2e7fb8a44941b6aaba6badc06327980f3ad844c2b24374c8a31b000000000000000000000000000000000000000000000000000000000000001b07461f48b2a3007d87de7ccc3f3f3e76539854c4c1ace50d0c741c561fcdf3557a39d0f9261062605a55d3bff300a9ba737c0c66f76102974a2cc98e0bbcec897a0d4b531ea7af92b0e256d62d7479eddc51d7285f1736df50b29f6bf529f081000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c2e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e139a0c98687a000000000000000000000000000000000000000000000000002e139b972710e800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000064e7df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b3d16b2cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a6d45774d3245334e4330354e7a597a4c5455784e5449744f54646c597930785954457a59324535597a4a6b596d596966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005f906a974bf3029b784af87582cc823be5a234a8000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0aae21f46bdd6d71593193cdf877300d3fc54f2a43dc7c17b420ffb51cb0b9b4",
      "signature": {
        "s": "0x4f4ccc30a7ca2e7fb8a44941b6aaba6badc06327980f3ad844c2b24374c8a31b",
        "r": "0x854e89ffd610db704df2c8225c0712a17728ae506cfc6347195ad14506e4ab1a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x07461f48b2a3007d87de7ccc3f3f3e76539854c4c1ace50d0c741c561fcdf355",
      "signature": {
        "s": "0x7a0d4b531ea7af92b0e256d62d7479eddc51d7285f1736df50b29f6bf529f081",
        "r": "0x7a39d0f9261062605a55d3bff300a9ba737c0c66f76102974a2cc98e0bbcec89",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6612959375",
    "total": "6612959375"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6612959375",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "48269537999"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "6612959"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZmEwM2E3NC05NzYzLTUxNTItOTdlYy0xYTEzY2E5YzJkYmYifQ==",
    "nonce": 7214,
    "balances": {
      "current": "12969401285896314",
      "previous": "12969407905468648"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5f906a974bf3029b784af87582cc823be5a234a8",
    "nonce": 22,
    "balances": {
      "current": "6612959375",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:05.440Z",
  "updated": "2020-05-22T08:55:05.507Z",
  "id": "5ec79369005df800101bcba9"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000018a29c08f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6612959375`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`