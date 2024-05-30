# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8cf91E007CAd5A1DE59EE79c3928B7C883a5FbF8`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000004011ad90000000000000000000000000000000000000000000000000000000004011ad9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000004011ad90000000000000000000000000000000000000000000000000000000004011ad9db32d1ce6ee82e6c4c084a5af0100a305696544f38bad5dcd1d36049125c26a03afbfb9e7c5f0ddb1d9c6364badda3d84dc829a5f693719206936402054dd30a1684fb3ddbdc4d2f9142fa0dd4942723b2555e4d0ea504e60ac38e986ca0f354000000000000000000000000000000000000000000000000000000000000001cae3fea12bdeef338de0f902651d27371b209b6d5f17e97a5ac190e5e41fe12cd1128f321ad29add6be4cb5b9ab0e4c7168b2023e33adbb6189793ba65c4ff3c73358879122ef4c831e3391c895f3344c928f8c177836f727594453e2f7fcddb5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014d400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e22a726b59c19000000000000000000000000000000000000000000000000002e22a72ab7bd5f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001066d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000763ae14e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a6d45344e3251794e5331694e7a5a6b4c5455324f446b74596a4a6d595331694d574d3359544d7a4f446c6d596a636966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000008cf91e007cad5a1de59ee79c3928b7c883a5fbf80000000000000000000000000000000000000000000000000000000004011ad9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb32d1ce6ee82e6c4c084a5af0100a305696544f38bad5dcd1d36049125c26a0",
      "signature": {
        "s": "0x1684fb3ddbdc4d2f9142fa0dd4942723b2555e4d0ea504e60ac38e986ca0f354",
        "r": "0x3afbfb9e7c5f0ddb1d9c6364badda3d84dc829a5f693719206936402054dd30a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xae3fea12bdeef338de0f902651d27371b209b6d5f17e97a5ac190e5e41fe12cd",
      "signature": {
        "s": "0x3358879122ef4c831e3391c895f3344c928f8c177836f727594453e2f7fcddb5",
        "r": "0x1128f321ad29add6be4cb5b9ab0e4c7168b2023e33adbb6189793ba65c4ff3c7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "67181273",
    "total": "67181273"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "67181273",
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
            "amount": "31737124073"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "67181"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZmE4N2QyNS1iNzZkLTU2ODktYjJmYS1iMWM3YTMzODlmYjcifQ==",
    "nonce": 5332,
    "balances": {
      "current": "12985950233009177",
      "previous": "12985950300257631"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8cf91e007cad5a1de59ee79c3928b7c883a5fbf8",
    "nonce": 10,
    "balances": {
      "current": "67181273",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:16.850Z",
  "updated": "2020-05-22T08:40:16.923Z",
  "id": "5ec78ff0005df800101bc92f"
}
```
* *stageAmount*: `67181273`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000004011ad9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000004011ad90000000000000000000000000000000000000000000000000000000004011ad9db32d1ce6ee82e6c4c084a5af0100a305696544f38bad5dcd1d36049125c26a03afbfb9e7c5f0ddb1d9c6364badda3d84dc829a5f693719206936402054dd30a1684fb3ddbdc4d2f9142fa0dd4942723b2555e4d0ea504e60ac38e986ca0f354000000000000000000000000000000000000000000000000000000000000001cae3fea12bdeef338de0f902651d27371b209b6d5f17e97a5ac190e5e41fe12cd1128f321ad29add6be4cb5b9ab0e4c7168b2023e33adbb6189793ba65c4ff3c73358879122ef4c831e3391c895f3344c928f8c177836f727594453e2f7fcddb5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5662000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000014d400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e22a726b59c19000000000000000000000000000000000000000000000000002e22a72ab7bd5f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001066d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000763ae14e9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795a6d45344e3251794e5331694e7a5a6b4c5455324f446b74596a4a6d595331694d574d3359544d7a4f446c6d596a636966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000008cf91e007cad5a1de59ee79c3928b7c883a5fbf80000000000000000000000000000000000000000000000000000000004011ad9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb32d1ce6ee82e6c4c084a5af0100a305696544f38bad5dcd1d36049125c26a0",
      "signature": {
        "s": "0x1684fb3ddbdc4d2f9142fa0dd4942723b2555e4d0ea504e60ac38e986ca0f354",
        "r": "0x3afbfb9e7c5f0ddb1d9c6364badda3d84dc829a5f693719206936402054dd30a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xae3fea12bdeef338de0f902651d27371b209b6d5f17e97a5ac190e5e41fe12cd",
      "signature": {
        "s": "0x3358879122ef4c831e3391c895f3344c928f8c177836f727594453e2f7fcddb5",
        "r": "0x1128f321ad29add6be4cb5b9ab0e4c7168b2023e33adbb6189793ba65c4ff3c7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "67181273",
    "total": "67181273"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "67181273",
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
            "amount": "31737124073"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "67181"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyZmE4N2QyNS1iNzZkLTU2ODktYjJmYS1iMWM3YTMzODlmYjcifQ==",
    "nonce": 5332,
    "balances": {
      "current": "12985950233009177",
      "previous": "12985950300257631"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8cf91e007cad5a1de59ee79c3928b7c883a5fbf8",
    "nonce": 10,
    "balances": {
      "current": "67181273",
      "previous": "0"
    }
  },
  "blockNumber": "10114658",
  "created": "2020-05-22T08:40:16.850Z",
  "updated": "2020-05-22T08:40:16.923Z",
  "id": "5ec78ff0005df800101bc92f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000004011ad9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `67181273`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`