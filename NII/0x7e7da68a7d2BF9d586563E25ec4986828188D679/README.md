# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7e7da68a7d2BF9d586563E25ec4986828188D679`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000e78ef050b020ed27b09000000000000000000000000000000000000000000000000000003e4be800aab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000003e4be800aab0000000000000000000000000000000000000000000004cbe4665d0d37a6f2597bd21bbfc94fdc67f7fcc03826134f4bb367590f37dcca48177a00bb756d26afb3177e2b092ac4cd9669e6187951d201768768585b5cca2f6afb423ff459a2aa09ea4854548c5f8c7a7f2caed78b914b640847e94fb17ec714c3ee03d9373150000000000000000000000000000000000000000000000000000000000000001c6a875d5cd9db4f62b98fa8f1050fd38316823d8842161ce3fde6104b2e2f3c952b3a46de2771f0d6663ccb0365f7591288648223c52ebb80c43d4a330f07edc070779543804c69066b69927055829f21210f832fad991d104e1ea39ee4ce2b0a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af4a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000072a4886d1b6e049829df0000000000000000000000000000000000000000000072a4886d1f53c242d44b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000ff2a9fc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cf10461645c7bf142a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d574d794e7a566a4e5330784e5449774c54566d597a67744f5749795979316c4d4446684f444131597a4a684d6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007e7da68a7d2bf9d586563e25ec4986828188d679000000000000000000000000000000000000000000000e78ef050b020ed27b09000000000000000000000000000000000000000000000e78ef05071d5052705e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7bd21bbfc94fdc67f7fcc03826134f4bb367590f37dcca48177a00bb756d26af",
      "signature": {
        "s": "0x09ea4854548c5f8c7a7f2caed78b914b640847e94fb17ec714c3ee03d9373150",
        "r": "0xb3177e2b092ac4cd9669e6187951d201768768585b5cca2f6afb423ff459a2aa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a875d5cd9db4f62b98fa8f1050fd38316823d8842161ce3fde6104b2e2f3c95",
      "signature": {
        "s": "0x70779543804c69066b69927055829f21210f832fad991d104e1ea39ee4ce2b0a",
        "r": "0x2b3a46de2771f0d6663ccb0365f7591288648223c52ebb80c43d4a330f07edc0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4280983489195",
    "total": "22650612922641241535065"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4280983489195",
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
            "amount": "27431481086848039588906"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4280983489"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMWMyNzVjNS0xNTIwLTVmYzgtOWIyYy1lMDFhODA1YzJhMjIifQ==",
    "nonce": 110410,
    "balances": {
      "current": "541384875618948877920735",
      "previous": "541384875623234142393419"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e7da68a7d2bf9d586563e25ec4986828188d679",
    "nonce": 46,
    "balances": {
      "current": "68343963233473594030857",
      "previous": "68343963229192610541662"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:08.605Z",
  "updated": "2022-05-04T08:53:08.684Z",
  "id": "62723ef4bbd75600116d0560"
}
```
* *stageAmount*: `68343963233473594030857`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000003e4be800aab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000003e4be800aab0000000000000000000000000000000000000000000004cbe4665d0d37a6f2597bd21bbfc94fdc67f7fcc03826134f4bb367590f37dcca48177a00bb756d26afb3177e2b092ac4cd9669e6187951d201768768585b5cca2f6afb423ff459a2aa09ea4854548c5f8c7a7f2caed78b914b640847e94fb17ec714c3ee03d9373150000000000000000000000000000000000000000000000000000000000000001c6a875d5cd9db4f62b98fa8f1050fd38316823d8842161ce3fde6104b2e2f3c952b3a46de2771f0d6663ccb0365f7591288648223c52ebb80c43d4a330f07edc070779543804c69066b69927055829f21210f832fad991d104e1ea39ee4ce2b0a000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af4a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000072a4886d1b6e049829df0000000000000000000000000000000000000000000072a4886d1f53c242d44b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000ff2a9fc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005cf10461645c7bf142a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d574d794e7a566a4e5330784e5449774c54566d597a67744f5749795979316c4d4446684f444131597a4a684d6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007e7da68a7d2bf9d586563e25ec4986828188d679000000000000000000000000000000000000000000000e78ef050b020ed27b09000000000000000000000000000000000000000000000e78ef05071d5052705e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7bd21bbfc94fdc67f7fcc03826134f4bb367590f37dcca48177a00bb756d26af",
      "signature": {
        "s": "0x09ea4854548c5f8c7a7f2caed78b914b640847e94fb17ec714c3ee03d9373150",
        "r": "0xb3177e2b092ac4cd9669e6187951d201768768585b5cca2f6afb423ff459a2aa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a875d5cd9db4f62b98fa8f1050fd38316823d8842161ce3fde6104b2e2f3c95",
      "signature": {
        "s": "0x70779543804c69066b69927055829f21210f832fad991d104e1ea39ee4ce2b0a",
        "r": "0x2b3a46de2771f0d6663ccb0365f7591288648223c52ebb80c43d4a330f07edc0",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4280983489195",
    "total": "22650612922641241535065"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4280983489195",
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
            "amount": "27431481086848039588906"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4280983489"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyMWMyNzVjNS0xNTIwLTVmYzgtOWIyYy1lMDFhODA1YzJhMjIifQ==",
    "nonce": 110410,
    "balances": {
      "current": "541384875618948877920735",
      "previous": "541384875623234142393419"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e7da68a7d2bf9d586563e25ec4986828188d679",
    "nonce": 46,
    "balances": {
      "current": "68343963233473594030857",
      "previous": "68343963229192610541662"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:08.605Z",
  "updated": "2022-05-04T08:53:08.684Z",
  "id": "62723ef4bbd75600116d0560"
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
0x0f200f9b000000000000000000000000000000000000000000000e78ef050b020ed27b090000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `68343963233473594030857`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`