# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x52f1dd2Ed62266b59e30F3dCB99309EbF518f7ec`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000409560000000000000000000000000000000000000000000000000000000000040956000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000409560000000000000000000000000000000000000000000000000000000000040956f3164f36d92b3031e6074c905152929ebbf7a313970b6131d900a36370b6773dea72d4d479057b403f78d7b4935c0e06a41d0feb02d1bfbd077ba6b5f9f3c8b304ef9f05a7a31802ad5ebfaa108d157a650af5409b626655a792633b5ae25ce4000000000000000000000000000000000000000000000000000000000000001c64d33a318c4ae1a8e478a4e0a25da652927a7bfc8d971caddfe989b0d0c0883f6fa4265db02ad85968d2d6e62b3b1a9a2a5249851dcc408b0d0421ccd185f0be310c3cdc76b9d3a89a80b19f329750e869d5e606e0185a22024c580799d60e85000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5674000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016b700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b6a83f9f9e8000000000000000000000000000000000000000000000000002e1b6a83fe044600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000108000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093d7b1e31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d54526b59546379595330795957597a4c5455304f444974596a67774e69316a4e444e694e324a6b4e574e6c5a44676966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000052f1dd2ed62266b59e30f3dcb99309ebf518f7ec0000000000000000000000000000000000000000000000000000000000040956000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf3164f36d92b3031e6074c905152929ebbf7a313970b6131d900a36370b6773d",
      "signature": {
        "s": "0x04ef9f05a7a31802ad5ebfaa108d157a650af5409b626655a792633b5ae25ce4",
        "r": "0xea72d4d479057b403f78d7b4935c0e06a41d0feb02d1bfbd077ba6b5f9f3c8b3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x64d33a318c4ae1a8e478a4e0a25da652927a7bfc8d971caddfe989b0d0c0883f",
      "signature": {
        "s": "0x310c3cdc76b9d3a89a80b19f329750e869d5e606e0185a22024c580799d60e85",
        "r": "0x6fa4265db02ad85968d2d6e62b3b1a9a2a5249851dcc408b0d0421ccd185f0be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "264534",
    "total": "264534"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264534",
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
            "amount": "39686184497"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTRkYTcyYS0yYWYzLTU0ODItYjgwNi1jNDNiN2JkNWNlZDgifQ==",
    "nonce": 5815,
    "balances": {
      "current": "12977993223371240",
      "previous": "12977993223636038"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x52f1dd2ed62266b59e30f3dcb99309ebf518f7ec",
    "nonce": 22,
    "balances": {
      "current": "264534",
      "previous": "0"
    }
  },
  "blockNumber": "10114676",
  "created": "2020-05-22T08:44:09.632Z",
  "updated": "2020-05-22T08:44:09.698Z",
  "id": "5ec790d9005df800101bc9d5"
}
```
* *stageAmount*: `264534`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000040956000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000409560000000000000000000000000000000000000000000000000000000000040956f3164f36d92b3031e6074c905152929ebbf7a313970b6131d900a36370b6773dea72d4d479057b403f78d7b4935c0e06a41d0feb02d1bfbd077ba6b5f9f3c8b304ef9f05a7a31802ad5ebfaa108d157a650af5409b626655a792633b5ae25ce4000000000000000000000000000000000000000000000000000000000000001c64d33a318c4ae1a8e478a4e0a25da652927a7bfc8d971caddfe989b0d0c0883f6fa4265db02ad85968d2d6e62b3b1a9a2a5249851dcc408b0d0421ccd185f0be310c3cdc76b9d3a89a80b19f329750e869d5e606e0185a22024c580799d60e85000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5674000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016b700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b6a83f9f9e8000000000000000000000000000000000000000000000000002e1b6a83fe044600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000108000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093d7b1e31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d54526b59546379595330795957597a4c5455304f444974596a67774e69316a4e444e694e324a6b4e574e6c5a44676966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000052f1dd2ed62266b59e30f3dcb99309ebf518f7ec0000000000000000000000000000000000000000000000000000000000040956000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf3164f36d92b3031e6074c905152929ebbf7a313970b6131d900a36370b6773d",
      "signature": {
        "s": "0x04ef9f05a7a31802ad5ebfaa108d157a650af5409b626655a792633b5ae25ce4",
        "r": "0xea72d4d479057b403f78d7b4935c0e06a41d0feb02d1bfbd077ba6b5f9f3c8b3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x64d33a318c4ae1a8e478a4e0a25da652927a7bfc8d971caddfe989b0d0c0883f",
      "signature": {
        "s": "0x310c3cdc76b9d3a89a80b19f329750e869d5e606e0185a22024c580799d60e85",
        "r": "0x6fa4265db02ad85968d2d6e62b3b1a9a2a5249851dcc408b0d0421ccd185f0be",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "264534",
    "total": "264534"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "264534",
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
            "amount": "39686184497"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "264"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMTRkYTcyYS0yYWYzLTU0ODItYjgwNi1jNDNiN2JkNWNlZDgifQ==",
    "nonce": 5815,
    "balances": {
      "current": "12977993223371240",
      "previous": "12977993223636038"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x52f1dd2ed62266b59e30f3dcb99309ebf518f7ec",
    "nonce": 22,
    "balances": {
      "current": "264534",
      "previous": "0"
    }
  },
  "blockNumber": "10114676",
  "created": "2020-05-22T08:44:09.632Z",
  "updated": "2020-05-22T08:44:09.698Z",
  "id": "5ec790d9005df800101bc9d5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000040956000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `264534`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`