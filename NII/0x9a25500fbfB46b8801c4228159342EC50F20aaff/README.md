# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9a25500fbfB46b8801c4228159342EC50F20aaff`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000002148f05ac274e4c000000000000000000000000000000000000000000000000000ca0596632d2d30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000ca0596632d2d300000000000000000000000000000000000000000000000001624edc9d912c39d204bc449d0da12fa75b8e441ccfc140bb6866d405eda8a34dba7a6ec68028193f73e88c6323e3d24de480edfb78819ffe915d5a37066d687634bb7c8d3afdc6288fd9fefb85fd3b4a0c4a5772db4d55e4c41b1f2c9e4676d9091cb3d16b5750000000000000000000000000000000000000000000000000000000000000001b3cf5ed4df6954b5af902c335cbaecf1532c341a6faf6e02ad2f6e742639122515a36ee72b7f13b5a4379164e75f41f670b93dce6e0decb1003fe02d4d76d320a7c4a78a11122ac008f241c784d1df8ee8a7fbcf0742d7daf7af5313723d7997a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae98000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000961323b496a2dd580c8800000000000000000000000000000000000000000000961323c13a37bec7d9ef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000033b7b3cfa940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60084ac4578c2b9880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934597a63344e44466d5979316d593249774c54566c4d546b74595467325953316c595459334f4755315a4759314d32556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009a25500fbfb46b8801c4228159342ec50f20aaff00000000000000000000000000000000000000000000000002148f05ac274e4c0000000000000000000000000000000000000000000000000207eeac45f47b7900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd204bc449d0da12fa75b8e441ccfc140bb6866d405eda8a34dba7a6ec6802819",
      "signature": {
        "s": "0x288fd9fefb85fd3b4a0c4a5772db4d55e4c41b1f2c9e4676d9091cb3d16b5750",
        "r": "0x3f73e88c6323e3d24de480edfb78819ffe915d5a37066d687634bb7c8d3afdc6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3cf5ed4df6954b5af902c335cbaecf1532c341a6faf6e02ad2f6e74263912251",
      "signature": {
        "s": "0x7c4a78a11122ac008f241c784d1df8ee8a7fbcf0742d7daf7af5313723d7997a",
        "r": "0x5a36ee72b7f13b5a4379164e75f41f670b93dce6e0decb1003fe02d4d76d320a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3554005547668179",
    "total": "99728851198880825"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3554005547668179",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264325085054021843336"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3554005547668"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Yzc4NDFmYy1mY2IwLTVlMTktYTg2YS1lYTY3OGU1ZGY1M2UifQ==",
    "nonce": 110232,
    "balances": {
      "current": "708708033414760641334408",
      "previous": "708708036972320194550255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9a25500fbfb46b8801c4228159342ec50f20aaff",
    "nonce": 46,
    "balances": {
      "current": "149901942135934540",
      "previous": "146347936588266361"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:13.864Z",
  "updated": "2022-05-04T08:52:13.957Z",
  "id": "62723ebdbbd75600116d0520"
}
```
* *stageAmount*: `149901942135934540`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000ca0596632d2d30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000ca0596632d2d300000000000000000000000000000000000000000000000001624edc9d912c39d204bc449d0da12fa75b8e441ccfc140bb6866d405eda8a34dba7a6ec68028193f73e88c6323e3d24de480edfb78819ffe915d5a37066d687634bb7c8d3afdc6288fd9fefb85fd3b4a0c4a5772db4d55e4c41b1f2c9e4676d9091cb3d16b5750000000000000000000000000000000000000000000000000000000000000001b3cf5ed4df6954b5af902c335cbaecf1532c341a6faf6e02ad2f6e742639122515a36ee72b7f13b5a4379164e75f41f670b93dce6e0decb1003fe02d4d76d320a7c4a78a11122ac008f241c784d1df8ee8a7fbcf0742d7daf7af5313723d7997a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae98000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000961323b496a2dd580c8800000000000000000000000000000000000000000000961323c13a37bec7d9ef00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000033b7b3cfa940000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60084ac4578c2b9880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934597a63344e44466d5979316d593249774c54566c4d546b74595467325953316c595459334f4755315a4759314d32556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009a25500fbfb46b8801c4228159342ec50f20aaff00000000000000000000000000000000000000000000000002148f05ac274e4c0000000000000000000000000000000000000000000000000207eeac45f47b7900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd204bc449d0da12fa75b8e441ccfc140bb6866d405eda8a34dba7a6ec6802819",
      "signature": {
        "s": "0x288fd9fefb85fd3b4a0c4a5772db4d55e4c41b1f2c9e4676d9091cb3d16b5750",
        "r": "0x3f73e88c6323e3d24de480edfb78819ffe915d5a37066d687634bb7c8d3afdc6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3cf5ed4df6954b5af902c335cbaecf1532c341a6faf6e02ad2f6e74263912251",
      "signature": {
        "s": "0x7c4a78a11122ac008f241c784d1df8ee8a7fbcf0742d7daf7af5313723d7997a",
        "r": "0x5a36ee72b7f13b5a4379164e75f41f670b93dce6e0decb1003fe02d4d76d320a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3554005547668179",
    "total": "99728851198880825"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3554005547668179",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264325085054021843336"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3554005547668"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4Yzc4NDFmYy1mY2IwLTVlMTktYTg2YS1lYTY3OGU1ZGY1M2UifQ==",
    "nonce": 110232,
    "balances": {
      "current": "708708033414760641334408",
      "previous": "708708036972320194550255"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9a25500fbfb46b8801c4228159342ec50f20aaff",
    "nonce": 46,
    "balances": {
      "current": "149901942135934540",
      "previous": "146347936588266361"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:13.864Z",
  "updated": "2022-05-04T08:52:13.957Z",
  "id": "62723ebdbbd75600116d0520"
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
0x0f200f9b00000000000000000000000000000000000000000000000002148f05ac274e4c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `149901942135934540`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`