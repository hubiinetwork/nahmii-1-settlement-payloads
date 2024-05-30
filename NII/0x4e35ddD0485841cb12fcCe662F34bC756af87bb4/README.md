# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4e35ddD0485841cb12fcCe662F34bC756af87bb4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de0b80e7c21aaa0000000000000000000000000000000000000000000000024b60888d11e6670000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000024b60888d11e667000000000000000000000000000000000000000000000000024b60888d11e66700073bd3e2ec88c6433fc036122ccae5e6c8d55c1b9a4b5c2b765dbeee503a3c25452abb5ad0193ece49995c97fe780c67966f4b7398231470289be6110f2578cb66eaecd2c8c755dfd807c52022ff232106fcdf0bf404553fcc5579a7b9aae7367000000000000000000000000000000000000000000000000000000000000001c93ea4118c2faf7aaf6109a32794c96f9bd47a77e36dd8eb0baaa1a22d3ea17deca972810afe2bc4828c7fefa8f82f3569cb4a8a9063724b9f40cd4a8d6808b33792b4128d1619e0ef6f5de123fe756fe7bd200be97c2f2404dd34ab5a6f2a5ef000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1d5cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000004e35ddd0485841cb12fcce662f34bc756af87bb40000000000000000000000000000000000000000000000000de0b80e7c21aaa0000000000000000000000000000000000000000000000024cd4f2662e27f80a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000965e58347f766000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000965e58347f766000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954426d5a4442684f53316c4d6a426b4c5451334f546b74596d4d314d533034595452685a446b314d47466a4e6a416966513d3d0000000000000000000000000000000000000000000000000000000000000032000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000269d14627ac4778626680000000000000000000000000000000000000000000026785e59f1f3591fb66800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x73bd3e2ec88c6433fc036122ccae5e6c8d55c1b9a4b5c2b765dbeee503a3c254",
      "signature": {
        "s": "0x6eaecd2c8c755dfd807c52022ff232106fcdf0bf404553fcc5579a7b9aae7367",
        "r": "0x52abb5ad0193ece49995c97fe780c67966f4b7398231470289be6110f2578cb6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x93ea4118c2faf7aaf6109a32794c96f9bd47a77e36dd8eb0baaa1a22d3ea17de",
      "signature": {
        "s": "0x792b4128d1619e0ef6f5de123fe756fe7bd200be97c2f2404dd34ab5a6f2a5ef",
        "r": "0xca972810afe2bc4828c7fefa8f82f3569cb4a8a9063724b9f40cd4a8d6808b33",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "677199671000000000000",
    "total": "677199671000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "677199671000000000000",
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
            "amount": "677199671000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "677199671000000000"
      }
    },
    "wallet": "0x4e35ddd0485841cb12fcce662f34bc756af87bb4",
    "data": "eyJyZWYiOiJiYTBmZDBhOS1lMjBkLTQ3OTktYmM1MS04YTRhZDk1MGFjNjAifQ==",
    "nonce": 14,
    "balances": {
      "current": "1000001489627884192",
      "previous": "678876872160627884192"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 50,
    "balances": {
      "current": "182347534040031631386216",
      "previous": "181670334369031631386216"
    }
  },
  "blockNumber": "14800331",
  "created": "2022-05-18T18:23:52.191Z",
  "updated": "2022-05-18T18:23:52.298Z",
  "id": "628539b8bbd75600116d08ae"
}
```
* *stageAmount*: `1000001489627884192`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000024b60888d11e6670000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000024b60888d11e667000000000000000000000000000000000000000000000000024b60888d11e66700073bd3e2ec88c6433fc036122ccae5e6c8d55c1b9a4b5c2b765dbeee503a3c25452abb5ad0193ece49995c97fe780c67966f4b7398231470289be6110f2578cb66eaecd2c8c755dfd807c52022ff232106fcdf0bf404553fcc5579a7b9aae7367000000000000000000000000000000000000000000000000000000000000001c93ea4118c2faf7aaf6109a32794c96f9bd47a77e36dd8eb0baaa1a22d3ea17deca972810afe2bc4828c7fefa8f82f3569cb4a8a9063724b9f40cd4a8d6808b33792b4128d1619e0ef6f5de123fe756fe7bd200be97c2f2404dd34ab5a6f2a5ef000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1d5cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000004e35ddd0485841cb12fcce662f34bc756af87bb40000000000000000000000000000000000000000000000000de0b80e7c21aaa0000000000000000000000000000000000000000000000024cd4f2662e27f80a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000965e58347f766000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000965e58347f766000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954426d5a4442684f53316c4d6a426b4c5451334f546b74596d4d314d533034595452685a446b314d47466a4e6a416966513d3d0000000000000000000000000000000000000000000000000000000000000032000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000269d14627ac4778626680000000000000000000000000000000000000000000026785e59f1f3591fb66800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x73bd3e2ec88c6433fc036122ccae5e6c8d55c1b9a4b5c2b765dbeee503a3c254",
      "signature": {
        "s": "0x6eaecd2c8c755dfd807c52022ff232106fcdf0bf404553fcc5579a7b9aae7367",
        "r": "0x52abb5ad0193ece49995c97fe780c67966f4b7398231470289be6110f2578cb6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x93ea4118c2faf7aaf6109a32794c96f9bd47a77e36dd8eb0baaa1a22d3ea17de",
      "signature": {
        "s": "0x792b4128d1619e0ef6f5de123fe756fe7bd200be97c2f2404dd34ab5a6f2a5ef",
        "r": "0xca972810afe2bc4828c7fefa8f82f3569cb4a8a9063724b9f40cd4a8d6808b33",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "677199671000000000000",
    "total": "677199671000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "677199671000000000000",
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
            "amount": "677199671000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "677199671000000000"
      }
    },
    "wallet": "0x4e35ddd0485841cb12fcce662f34bc756af87bb4",
    "data": "eyJyZWYiOiJiYTBmZDBhOS1lMjBkLTQ3OTktYmM1MS04YTRhZDk1MGFjNjAifQ==",
    "nonce": 14,
    "balances": {
      "current": "1000001489627884192",
      "previous": "678876872160627884192"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 50,
    "balances": {
      "current": "182347534040031631386216",
      "previous": "181670334369031631386216"
    }
  },
  "blockNumber": "14800331",
  "created": "2022-05-18T18:23:52.191Z",
  "updated": "2022-05-18T18:23:52.298Z",
  "id": "628539b8bbd75600116d08ae"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de0b80e7c21aaa00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000001489627884192`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`