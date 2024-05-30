# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc4C96ddBe6F3Af8217206A9A8b4E89AFF6554c3A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000f57e59e200000000000000000000000000000000000000000000000000000000f57e59e2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000f57e59e200000000000000000000000000000000000000000000000000000000f57e59e285434367c1fb6d60fef8c43e28337f93930d5a200ee475486cacb217774ca2f3c383e15400c67bc2359693afb52c249a2587c63952730e87593d1e5d079e655a69b210d0053373335b2ab03b8c3209a4e1f1823b3510a64f6955c1dd30483fca000000000000000000000000000000000000000000000000000000000000001cd015247ef1e7ebdf4dad4788bda68c3b3ed675401e0f3e8506855d61f712d6c73578314794378f04a32119834ce43165e2354850435397c4a8afe05c60169018292f50426df0285f4cc1a1e1e52738e40fe3a5dd9009cd8e21bf9043b133afed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000191900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18207049cea0000000000000000000000000000000000000000000000000002e18216607012c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003ed8aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a14d655b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f4441354f4449334d6930785a6a5a6a4c5455775a5451745954517a4d5330304e5459354d5467794e7a526b4e6a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c4c96ddbe6f3af8217206a9a8b4e89aff6554c3a00000000000000000000000000000000000000000000000000000000f57e59e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85434367c1fb6d60fef8c43e28337f93930d5a200ee475486cacb217774ca2f3",
      "signature": {
        "s": "0x69b210d0053373335b2ab03b8c3209a4e1f1823b3510a64f6955c1dd30483fca",
        "r": "0xc383e15400c67bc2359693afb52c249a2587c63952730e87593d1e5d079e655a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd015247ef1e7ebdf4dad4788bda68c3b3ed675401e0f3e8506855d61f712d6c7",
      "signature": {
        "s": "0x292f50426df0285f4cc1a1e1e52738e40fe3a5dd9009cd8e21bf9043b133afed",
        "r": "0x3578314794378f04a32119834ce43165e2354850435397c4a8afe05c60169018",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4118698466",
    "total": "4118698466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4118698466",
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
            "amount": "43299263922"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4118698"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ODA5ODI3Mi0xZjZjLTUwZTQtYTQzMS00NTY5MTgyNzRkNjgifQ==",
    "nonce": 6425,
    "balances": {
      "current": "12974376530595488",
      "previous": "12974380653412652"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4c96ddbe6f3af8217206a9a8b4e89aff6554c3a",
    "nonce": 22,
    "balances": {
      "current": "4118698466",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:01.626Z",
  "updated": "2020-05-22T08:49:01.696Z",
  "id": "5ec791fdb0c6090011d5b123"
}
```
* *stageAmount*: `4118698466`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000f57e59e2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000f57e59e200000000000000000000000000000000000000000000000000000000f57e59e285434367c1fb6d60fef8c43e28337f93930d5a200ee475486cacb217774ca2f3c383e15400c67bc2359693afb52c249a2587c63952730e87593d1e5d079e655a69b210d0053373335b2ab03b8c3209a4e1f1823b3510a64f6955c1dd30483fca000000000000000000000000000000000000000000000000000000000000001cd015247ef1e7ebdf4dad4788bda68c3b3ed675401e0f3e8506855d61f712d6c73578314794378f04a32119834ce43165e2354850435397c4a8afe05c60169018292f50426df0285f4cc1a1e1e52738e40fe3a5dd9009cd8e21bf9043b133afed000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000191900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18207049cea0000000000000000000000000000000000000000000000000002e18216607012c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003ed8aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a14d655b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f4441354f4449334d6930785a6a5a6a4c5455775a5451745954517a4d5330304e5459354d5467794e7a526b4e6a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c4c96ddbe6f3af8217206a9a8b4e89aff6554c3a00000000000000000000000000000000000000000000000000000000f57e59e2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x85434367c1fb6d60fef8c43e28337f93930d5a200ee475486cacb217774ca2f3",
      "signature": {
        "s": "0x69b210d0053373335b2ab03b8c3209a4e1f1823b3510a64f6955c1dd30483fca",
        "r": "0xc383e15400c67bc2359693afb52c249a2587c63952730e87593d1e5d079e655a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd015247ef1e7ebdf4dad4788bda68c3b3ed675401e0f3e8506855d61f712d6c7",
      "signature": {
        "s": "0x292f50426df0285f4cc1a1e1e52738e40fe3a5dd9009cd8e21bf9043b133afed",
        "r": "0x3578314794378f04a32119834ce43165e2354850435397c4a8afe05c60169018",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4118698466",
    "total": "4118698466"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4118698466",
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
            "amount": "43299263922"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4118698"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3ODA5ODI3Mi0xZjZjLTUwZTQtYTQzMS00NTY5MTgyNzRkNjgifQ==",
    "nonce": 6425,
    "balances": {
      "current": "12974376530595488",
      "previous": "12974380653412652"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc4c96ddbe6f3af8217206a9a8b4e89aff6554c3a",
    "nonce": 22,
    "balances": {
      "current": "4118698466",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:01.626Z",
  "updated": "2020-05-22T08:49:01.696Z",
  "id": "5ec791fdb0c6090011d5b123"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000f57e59e2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4118698466`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`