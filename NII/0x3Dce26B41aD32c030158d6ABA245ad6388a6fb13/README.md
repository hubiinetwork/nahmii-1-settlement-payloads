# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3Dce26B41aD32c030158d6ABA245ad6388a6fb13`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000020d2f0cfbe31624c0000000000000000000000000000000000000000000000000000000013eb84570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013eb845700000000000000000000000000000000000000000000000000000001d0e43bfc0b43bd218204b597a3faf040c85958b5ec0efa5510941cb808d47335e2a34fb9ed318fbc6f7c065e67684c195f0a6a92d6c24d4330cac8e8f21a76fe0f357dad38424617035fa3b27138446742f6c1be085d8a03c5bc8f3317940d43158f5786000000000000000000000000000000000000000000000000000000000000001be854cc178a7f9f20de41a4a27d4d417f02fe2866c7bc13c9b248e06f95a3c29bd114f2cc9923f651e1c9954a5c7a2e9a64799b9685cbe9e533ceccd988f1fe0a6118fbfdf3cfa82c73a92dc68ba59ad8a82b3334f3c00c91efc4158d4edfb25d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ec0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b77f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000255e49c42a874aeedc7c00000000000000000000000000000000000000000000255e49c42a875edf7a4c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000519790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e2d378203b44fda2250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a686a4e4467355a53316d596a6c6c4c5456684e6a4974595449324f5330324d7a55794d7a4a694d5751794e7a456966513d3d00000000000000000000000000000000000000000000000000000000000000220000000000000000000000003dce26b41ad32c030158d6aba245ad6388a6fb1300000000000000000000000000000000000000000000000020d2f0cfbe31624c00000000000000000000000000000000000000000000000020d2f0cfaa45ddf500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b43bd218204b597a3faf040c85958b5ec0efa5510941cb808d47335e2a34fb9",
      "signature": {
        "s": "0x38424617035fa3b27138446742f6c1be085d8a03c5bc8f3317940d43158f5786",
        "r": "0xed318fbc6f7c065e67684c195f0a6a92d6c24d4330cac8e8f21a76fe0f357dad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe854cc178a7f9f20de41a4a27d4d417f02fe2866c7bc13c9b248e06f95a3c29b",
      "signature": {
        "s": "0x6118fbfdf3cfa82c73a92dc68ba59ad8a82b3334f3c00c91efc4158d4edfb25d",
        "r": "0xd114f2cc9923f651e1c9954a5c7a2e9a64799b9685cbe9e533ceccd988f1fe0a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "334201943",
    "total": "7799585788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "334201943",
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
            "amount": "27796034539784725439013"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "334201"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MjhjNDg5ZS1mYjllLTVhNjItYTI2OS02MzUyMzJiMWQyNzEifQ==",
    "nonce": 112511,
    "balances": {
      "current": "176466869229326340906108",
      "previous": "176466869229326675442252"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3dce26b41ad32c030158d6aba245ad6388a6fb13",
    "nonce": 34,
    "balances": {
      "current": "2365217529362735692",
      "previous": "2365217529028533749"
    }
  },
  "blockNumber": "14709996",
  "created": "2022-05-04T09:04:13.485Z",
  "updated": "2022-05-04T09:04:13.546Z",
  "id": "6272418d7832e20011830e6a"
}
```
* *stageAmount*: `2365217529362735692`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000013eb84570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000013eb845700000000000000000000000000000000000000000000000000000001d0e43bfc0b43bd218204b597a3faf040c85958b5ec0efa5510941cb808d47335e2a34fb9ed318fbc6f7c065e67684c195f0a6a92d6c24d4330cac8e8f21a76fe0f357dad38424617035fa3b27138446742f6c1be085d8a03c5bc8f3317940d43158f5786000000000000000000000000000000000000000000000000000000000000001be854cc178a7f9f20de41a4a27d4d417f02fe2866c7bc13c9b248e06f95a3c29bd114f2cc9923f651e1c9954a5c7a2e9a64799b9685cbe9e533ceccd988f1fe0a6118fbfdf3cfa82c73a92dc68ba59ad8a82b3334f3c00c91efc4158d4edfb25d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ec0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b77f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000255e49c42a874aeedc7c00000000000000000000000000000000000000000000255e49c42a875edf7a4c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000519790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e2d378203b44fda2250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6a686a4e4467355a53316d596a6c6c4c5456684e6a4974595449324f5330324d7a55794d7a4a694d5751794e7a456966513d3d00000000000000000000000000000000000000000000000000000000000000220000000000000000000000003dce26b41ad32c030158d6aba245ad6388a6fb1300000000000000000000000000000000000000000000000020d2f0cfbe31624c00000000000000000000000000000000000000000000000020d2f0cfaa45ddf500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0b43bd218204b597a3faf040c85958b5ec0efa5510941cb808d47335e2a34fb9",
      "signature": {
        "s": "0x38424617035fa3b27138446742f6c1be085d8a03c5bc8f3317940d43158f5786",
        "r": "0xed318fbc6f7c065e67684c195f0a6a92d6c24d4330cac8e8f21a76fe0f357dad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe854cc178a7f9f20de41a4a27d4d417f02fe2866c7bc13c9b248e06f95a3c29b",
      "signature": {
        "s": "0x6118fbfdf3cfa82c73a92dc68ba59ad8a82b3334f3c00c91efc4158d4edfb25d",
        "r": "0xd114f2cc9923f651e1c9954a5c7a2e9a64799b9685cbe9e533ceccd988f1fe0a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "334201943",
    "total": "7799585788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "334201943",
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
            "amount": "27796034539784725439013"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "334201"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MjhjNDg5ZS1mYjllLTVhNjItYTI2OS02MzUyMzJiMWQyNzEifQ==",
    "nonce": 112511,
    "balances": {
      "current": "176466869229326340906108",
      "previous": "176466869229326675442252"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3dce26b41ad32c030158d6aba245ad6388a6fb13",
    "nonce": 34,
    "balances": {
      "current": "2365217529362735692",
      "previous": "2365217529028533749"
    }
  },
  "blockNumber": "14709996",
  "created": "2022-05-04T09:04:13.485Z",
  "updated": "2022-05-04T09:04:13.546Z",
  "id": "6272418d7832e20011830e6a"
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
0x0f200f9b00000000000000000000000000000000000000000000000020d2f0cfbe31624c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2365217529362735692`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`