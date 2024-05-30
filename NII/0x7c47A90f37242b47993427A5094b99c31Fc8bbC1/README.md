# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7c47A90f37242b47993427A5094b99c31Fc8bbC1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000000000000000000000000000005118a361ae8f12c340a3637befee0f3b9aa4a7e22558f2540b60bc37137d57f9c64841e3e9a58b58758762dd74d2a633644b5f43c66153c57a6efdca0addfdcbae841d804f2863181751f35478da9c174505e0e058d6ec616215856119b1a757af3af64ec46ccf38000000000000000000000000000000000000000000000000000000000000001b66eb4509efde3e22876cdeebb6f62cee01756e700131b19414548a923024a6d00d2264848f854ce564a6b08cb5b9a7412818f59c85d1f5975019c5186d9e0b327eaa46ee1ea32853e8f914a62fa3ab1077c3aa93f7ca7bd4c8775220c65b35d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012de3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236d98c23f9da08519e400000000000000000000000000000000000000000000236de9efa5b87e9d058000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000014c2b92f88d8d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9b551eb9c9671f1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a42694f5449344e7931694d5759354c5455345a6d51744f57526c4d5330785a6d566c5a544a6b596a41324d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000007c47a90f37242b47993427a5094b99c31fc8bbc10000000000000000000000000000000000000000000000005118a361ae8f12c3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40a3637befee0f3b9aa4a7e22558f2540b60bc37137d57f9c64841e3e9a58b58",
      "signature": {
        "s": "0x1751f35478da9c174505e0e058d6ec616215856119b1a757af3af64ec46ccf38",
        "r": "0x758762dd74d2a633644b5f43c66153c57a6efdca0addfdcbae841d804f286318",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x66eb4509efde3e22876cdeebb6f62cee01756e700131b19414548a923024a6d0",
      "signature": {
        "s": "0x7eaa46ee1ea32853e8f914a62fa3ab1077c3aa93f7ca7bd4c8775220c65b35d3",
        "r": "0x0d2264848f854ce564a6b08cb5b9a7412818f59c85d1f5975019c5186d9e0b32",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5843600156448985795",
    "total": "5843600156448985795"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5843600156448985795",
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
            "amount": "16816176737381597519644"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5843600156448985"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YjBiOTI4Ny1iMWY5LTU4ZmQtOWRlMS0xZmVlZTJkYjA2MDMifQ==",
    "nonce": 77283,
    "balances": {
      "current": "167304529434857406011876",
      "previous": "167310378878614011446656"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7c47a90f37242b47993427a5094b99c31fc8bbc1",
    "nonce": 1,
    "balances": {
      "current": "5843600156448985795",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:26.365Z",
  "updated": "2021-06-04T12:46:26.446Z",
  "id": "60ba20a2010ba300120bfdcb"
}
```
* *stageAmount*: `5843600156448985795`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000000000000000000000000000005118a361ae8f12c340a3637befee0f3b9aa4a7e22558f2540b60bc37137d57f9c64841e3e9a58b58758762dd74d2a633644b5f43c66153c57a6efdca0addfdcbae841d804f2863181751f35478da9c174505e0e058d6ec616215856119b1a757af3af64ec46ccf38000000000000000000000000000000000000000000000000000000000000001b66eb4509efde3e22876cdeebb6f62cee01756e700131b19414548a923024a6d00d2264848f854ce564a6b08cb5b9a7412818f59c85d1f5975019c5186d9e0b327eaa46ee1ea32853e8f914a62fa3ab1077c3aa93f7ca7bd4c8775220c65b35d3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012de3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236d98c23f9da08519e400000000000000000000000000000000000000000000236de9efa5b87e9d058000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000014c2b92f88d8d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9b551eb9c9671f1c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694934596a42694f5449344e7931694d5759354c5455345a6d51744f57526c4d5330785a6d566c5a544a6b596a41324d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000010000000000000000000000007c47a90f37242b47993427a5094b99c31fc8bbc10000000000000000000000000000000000000000000000005118a361ae8f12c3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x40a3637befee0f3b9aa4a7e22558f2540b60bc37137d57f9c64841e3e9a58b58",
      "signature": {
        "s": "0x1751f35478da9c174505e0e058d6ec616215856119b1a757af3af64ec46ccf38",
        "r": "0x758762dd74d2a633644b5f43c66153c57a6efdca0addfdcbae841d804f286318",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x66eb4509efde3e22876cdeebb6f62cee01756e700131b19414548a923024a6d0",
      "signature": {
        "s": "0x7eaa46ee1ea32853e8f914a62fa3ab1077c3aa93f7ca7bd4c8775220c65b35d3",
        "r": "0x0d2264848f854ce564a6b08cb5b9a7412818f59c85d1f5975019c5186d9e0b32",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "5843600156448985795",
    "total": "5843600156448985795"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5843600156448985795",
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
            "amount": "16816176737381597519644"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5843600156448985"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4YjBiOTI4Ny1iMWY5LTU4ZmQtOWRlMS0xZmVlZTJkYjA2MDMifQ==",
    "nonce": 77283,
    "balances": {
      "current": "167304529434857406011876",
      "previous": "167310378878614011446656"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7c47a90f37242b47993427a5094b99c31fc8bbc1",
    "nonce": 1,
    "balances": {
      "current": "5843600156448985795",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:26.365Z",
  "updated": "2021-06-04T12:46:26.446Z",
  "id": "60ba20a2010ba300120bfdcb"
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
0x0f200f9b0000000000000000000000000000000000000000000000005118a361ae8f12c30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5843600156448985795`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`