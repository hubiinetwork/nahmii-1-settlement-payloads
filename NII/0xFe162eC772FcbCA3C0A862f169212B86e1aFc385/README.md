# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFe162eC772FcbCA3C0A862f169212B86e1aFc385`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000002fea801c73844020900000000000000000000000000000000000000000000000057f09ee6c9a772250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000057f09ee6c9a77225000000000000000000000000000000000000000000000002fea801c7384402091279c59ab0de2b348933478072756e47571c44adcad69687377d0a19c1efe52bd8bb65293949839388f1b77859ff7f4dacded948bfdb883ec60a52e773622d27661e8f55327e1e6d12e56f2070640460b21487bd64f0b3a564145326c57fda8c000000000000000000000000000000000000000000000000000000000000001c26b37234b18cec60752c9ec3d4974cae2576580cf3e3abce9bdac4fefc6d913a6941be7a0cce39c5da7356a8ceeb93fb41caee54d551b19c78421001e065eacf79efcbccb6720f34e8a2a8c7924a77d95bf7803f8e87a4e2cfe312591c4dfe38000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000238ba168d677a94660fc00000000000000000000000000000000000000000000238bf96ff8998f4a687d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000016833b1c5c955c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f93a6cab0dfa4d1aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978596a5a684e6d4e6c4f5330795957466c4c5455344e5455745957466a597930775a546b34595441794e6a67314d57496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000fe162ec772fcbca3c0a862f169212b86e1afc385000000000000000000000000000000000000000000000002fea801c738440209000000000000000000000000000000000000000000000002a6b762e06e9c8fe400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1279c59ab0de2b348933478072756e47571c44adcad69687377d0a19c1efe52b",
      "signature": {
        "s": "0x661e8f55327e1e6d12e56f2070640460b21487bd64f0b3a564145326c57fda8c",
        "r": "0xd8bb65293949839388f1b77859ff7f4dacded948bfdb883ec60a52e773622d27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26b37234b18cec60752c9ec3d4974cae2576580cf3e3abce9bdac4fefc6d913a",
      "signature": {
        "s": "0x79efcbccb6720f34e8a2a8c7924a77d95bf7803f8e87a4e2cfe312591c4dfe38",
        "r": "0x6941be7a0cce39c5da7356a8ceeb93fb41caee54d551b19c78421001e065eacf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6336739389773148709",
    "total": "55243406784294289929"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6336739389773148709",
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
            "amount": "16815623265180126073258"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6336739389773148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxYjZhNmNlOS0yYWFlLTU4NTUtYWFjYy0wZTk4YTAyNjg1MWIifQ==",
    "nonce": 77229,
    "balances": {
      "current": "167858555108530323874044",
      "previous": "167864898184659486795901"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe162ec772fcbca3c0a862f169212b86e1afc385",
    "nonce": 2,
    "balances": {
      "current": "55243406784294289929",
      "previous": "48906667394521141220"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:12.053Z",
  "updated": "2021-06-04T12:46:12.135Z",
  "id": "60ba20940779920010014b95"
}
```
* *stageAmount*: `55243406784294289929`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000057f09ee6c9a772250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000057f09ee6c9a77225000000000000000000000000000000000000000000000002fea801c7384402091279c59ab0de2b348933478072756e47571c44adcad69687377d0a19c1efe52bd8bb65293949839388f1b77859ff7f4dacded948bfdb883ec60a52e773622d27661e8f55327e1e6d12e56f2070640460b21487bd64f0b3a564145326c57fda8c000000000000000000000000000000000000000000000000000000000000001c26b37234b18cec60752c9ec3d4974cae2576580cf3e3abce9bdac4fefc6d913a6941be7a0cce39c5da7356a8ceeb93fb41caee54d551b19c78421001e065eacf79efcbccb6720f34e8a2a8c7924a77d95bf7803f8e87a4e2cfe312591c4dfe38000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012dad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000238ba168d677a94660fc00000000000000000000000000000000000000000000238bf96ff8998f4a687d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000016833b1c5c955c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f93a6cab0dfa4d1aa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978596a5a684e6d4e6c4f5330795957466c4c5455344e5455745957466a597930775a546b34595441794e6a67314d57496966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000fe162ec772fcbca3c0a862f169212b86e1afc385000000000000000000000000000000000000000000000002fea801c738440209000000000000000000000000000000000000000000000002a6b762e06e9c8fe400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1279c59ab0de2b348933478072756e47571c44adcad69687377d0a19c1efe52b",
      "signature": {
        "s": "0x661e8f55327e1e6d12e56f2070640460b21487bd64f0b3a564145326c57fda8c",
        "r": "0xd8bb65293949839388f1b77859ff7f4dacded948bfdb883ec60a52e773622d27",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x26b37234b18cec60752c9ec3d4974cae2576580cf3e3abce9bdac4fefc6d913a",
      "signature": {
        "s": "0x79efcbccb6720f34e8a2a8c7924a77d95bf7803f8e87a4e2cfe312591c4dfe38",
        "r": "0x6941be7a0cce39c5da7356a8ceeb93fb41caee54d551b19c78421001e065eacf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6336739389773148709",
    "total": "55243406784294289929"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6336739389773148709",
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
            "amount": "16815623265180126073258"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6336739389773148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxYjZhNmNlOS0yYWFlLTU4NTUtYWFjYy0wZTk4YTAyNjg1MWIifQ==",
    "nonce": 77229,
    "balances": {
      "current": "167858555108530323874044",
      "previous": "167864898184659486795901"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfe162ec772fcbca3c0a862f169212b86e1afc385",
    "nonce": 2,
    "balances": {
      "current": "55243406784294289929",
      "previous": "48906667394521141220"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:12.053Z",
  "updated": "2021-06-04T12:46:12.135Z",
  "id": "60ba20940779920010014b95"
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
0x0f200f9b000000000000000000000000000000000000000000000002fea801c7384402090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `55243406784294289929`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`