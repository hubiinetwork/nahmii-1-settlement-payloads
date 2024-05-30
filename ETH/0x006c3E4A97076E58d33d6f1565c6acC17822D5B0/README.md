# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x006c3E4A97076E58d33d6f1565c6acC17822D5B0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000009e000000000000000000000000000000000000000000000000000000000000009e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000009e000000000000000000000000000000000000000000000000000000000000009e00c15adb64578ce4a67ba5f0e5254a8496547052642e7ce59874328983c43f2301d896b3ca21cb551d404210e57c52502a7987055bc7057db6eef6d14e8500a35de4e81c0ed4d3e8ecdd3a301da5c77045bb7c5bb6f91b42573214a5697931b4000000000000000000000000000000000000000000000000000000000000001cb788749157a4c5dd7f20076c8d3f5fe7453c8b4cf294562cb11abdcf91e5e9174453ade1a43bed2559ca0e6d8e066dbb93090267a5da8071a0006f4cd61549223cb68aef436b1349a427acb9cc96d158eee531174a8f5f7120dae1d77ac3dea3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000014b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccebe3eb000000000000000000000000000000000000000000000000002386f2ccebe48a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007f2b700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f5455314d44566b4f5330334e54526d4c5455324e575574595468684d793169596a5532593245314e446b324d6a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000006c3e4a97076e58d33d6f1565c6acc17822d5b0000000000000000000000000000000000000000000000000000000000000009e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x00c15adb64578ce4a67ba5f0e5254a8496547052642e7ce59874328983c43f23",
      "signature": {
        "s": "0x5de4e81c0ed4d3e8ecdd3a301da5c77045bb7c5bb6f91b42573214a5697931b4",
        "r": "0x01d896b3ca21cb551d404210e57c52502a7987055bc7057db6eef6d14e8500a3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb788749157a4c5dd7f20076c8d3f5fe7453c8b4cf294562cb11abdcf91e5e917",
      "signature": {
        "s": "0x3cb68aef436b1349a427acb9cc96d158eee531174a8f5f7120dae1d77ac3dea3",
        "r": "0x4453ade1a43bed2559ca0e6d8e066dbb93090267a5da8071a0006f4cd6154922",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158",
    "total": "158"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158",
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
            "amount": "520887"
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
    "data": "eyJyZWYiOiJkOTU1MDVkOS03NTRmLTU2NWUtYThhMy1iYjU2Y2E1NDk2MjEifQ==",
    "nonce": 331,
    "balances": {
      "current": "10000001563091947",
      "previous": "10000001563092106"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x006c3e4a97076e58d33d6f1565c6acc17822d5b0",
    "nonce": 20,
    "balances": {
      "current": "158",
      "previous": "0"
    }
  },
  "blockNumber": "10114497",
  "created": "2020-05-22T08:01:15.502Z",
  "updated": "2020-05-22T08:01:15.572Z",
  "id": "5ec786cb005df800101bc285"
}
```
* *stageAmount*: `158`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000009e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000009e000000000000000000000000000000000000000000000000000000000000009e00c15adb64578ce4a67ba5f0e5254a8496547052642e7ce59874328983c43f2301d896b3ca21cb551d404210e57c52502a7987055bc7057db6eef6d14e8500a35de4e81c0ed4d3e8ecdd3a301da5c77045bb7c5bb6f91b42573214a5697931b4000000000000000000000000000000000000000000000000000000000000001cb788749157a4c5dd7f20076c8d3f5fe7453c8b4cf294562cb11abdcf91e5e9174453ade1a43bed2559ca0e6d8e066dbb93090267a5da8071a0006f4cd61549223cb68aef436b1349a427acb9cc96d158eee531174a8f5f7120dae1d77ac3dea3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000014b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ccebe3eb000000000000000000000000000000000000000000000000002386f2ccebe48a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007f2b700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f5455314d44566b4f5330334e54526d4c5455324e575574595468684d793169596a5532593245314e446b324d6a456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000006c3e4a97076e58d33d6f1565c6acc17822d5b0000000000000000000000000000000000000000000000000000000000000009e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x00c15adb64578ce4a67ba5f0e5254a8496547052642e7ce59874328983c43f23",
      "signature": {
        "s": "0x5de4e81c0ed4d3e8ecdd3a301da5c77045bb7c5bb6f91b42573214a5697931b4",
        "r": "0x01d896b3ca21cb551d404210e57c52502a7987055bc7057db6eef6d14e8500a3",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb788749157a4c5dd7f20076c8d3f5fe7453c8b4cf294562cb11abdcf91e5e917",
      "signature": {
        "s": "0x3cb68aef436b1349a427acb9cc96d158eee531174a8f5f7120dae1d77ac3dea3",
        "r": "0x4453ade1a43bed2559ca0e6d8e066dbb93090267a5da8071a0006f4cd6154922",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "158",
    "total": "158"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "158",
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
            "amount": "520887"
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
    "data": "eyJyZWYiOiJkOTU1MDVkOS03NTRmLTU2NWUtYThhMy1iYjU2Y2E1NDk2MjEifQ==",
    "nonce": 331,
    "balances": {
      "current": "10000001563091947",
      "previous": "10000001563092106"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x006c3e4a97076e58d33d6f1565c6acc17822d5b0",
    "nonce": 20,
    "balances": {
      "current": "158",
      "previous": "0"
    }
  },
  "blockNumber": "10114497",
  "created": "2020-05-22T08:01:15.502Z",
  "updated": "2020-05-22T08:01:15.572Z",
  "id": "5ec786cb005df800101bc285"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000009e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `158`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``