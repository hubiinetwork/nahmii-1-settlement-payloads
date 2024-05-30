# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0c255cAC8f1bD9E1E73EF86495b54100Bf94Bf22`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002fceb000000000000000000000000000000000000000000000000000000000002fceb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002fceb000000000000000000000000000000000000000000000000000000000002fcebcd94b6514d9fd686b58b0f1ecbbaf3a682e259f69eceb09058993ea1432a3e6b395b68bd8beb8a507d9671dead38ac22c8185dc329eebfce7a1d344d73a38c8a4c0bb9d6f6fed50a68a59af998431969a8cc4bb84c7d143814459e891573746b000000000000000000000000000000000000000000000000000000000000001b6245708125970f7526479cb7c45a4f2ec33c04cb08ed9458f941a2054e5c3c6d8eea97239aecee9dd375fd14808d882ba2c1d01bf19c2935513afb01faf11a1e2bf3ad408a2dc414f75b868a3256caf89282b6d241ad0dd6874d640656e16e15000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbddca85000000000000000000000000000000000000000000000000002386f2cbe0c83300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000837bc00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a6b304f4451785a6930784f5459344c54566b59324d74596d5a684e5331694e6a4d7a596d466b4f5745784e6a676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000c255cac8f1bd9e1e73ef86495b54100bf94bf22000000000000000000000000000000000000000000000000000000000002fceb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcd94b6514d9fd686b58b0f1ecbbaf3a682e259f69eceb09058993ea1432a3e6b",
      "signature": {
        "s": "0x4c0bb9d6f6fed50a68a59af998431969a8cc4bb84c7d143814459e891573746b",
        "r": "0x395b68bd8beb8a507d9671dead38ac22c8185dc329eebfce7a1d344d73a38c8a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6245708125970f7526479cb7c45a4f2ec33c04cb08ed9458f941a2054e5c3c6d",
      "signature": {
        "s": "0x2bf3ad408a2dc414f75b868a3256caf89282b6d241ad0dd6874d640656e16e15",
        "r": "0x8eea97239aecee9dd375fd14808d882ba2c1d01bf19c2935513afb01faf11a1e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "195819",
    "total": "195819"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "195819",
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
            "amount": "538556"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "195"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMjk0ODQxZi0xOTY4LTVkY2MtYmZhNS1iNjMzYmFkOWExNjgifQ==",
    "nonce": 455,
    "balances": {
      "current": "10000001545390725",
      "previous": "10000001545586739"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0c255cac8f1bd9e1e73ef86495b54100bf94bf22",
    "nonce": 20,
    "balances": {
      "current": "195819",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:09.196Z",
  "updated": "2020-05-22T08:02:09.258Z",
  "id": "5ec78701b0c6090011d5a964"
}
```
* *stageAmount*: `195819`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002fceb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002fceb000000000000000000000000000000000000000000000000000000000002fcebcd94b6514d9fd686b58b0f1ecbbaf3a682e259f69eceb09058993ea1432a3e6b395b68bd8beb8a507d9671dead38ac22c8185dc329eebfce7a1d344d73a38c8a4c0bb9d6f6fed50a68a59af998431969a8cc4bb84c7d143814459e891573746b000000000000000000000000000000000000000000000000000000000000001b6245708125970f7526479cb7c45a4f2ec33c04cb08ed9458f941a2054e5c3c6d8eea97239aecee9dd375fd14808d882ba2c1d01bf19c2935513afb01faf11a1e2bf3ad408a2dc414f75b868a3256caf89282b6d241ad0dd6874d640656e16e15000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbddca85000000000000000000000000000000000000000000000000002386f2cbe0c83300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c30000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000837bc00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d6a6b304f4451785a6930784f5459344c54566b59324d74596d5a684e5331694e6a4d7a596d466b4f5745784e6a676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000c255cac8f1bd9e1e73ef86495b54100bf94bf22000000000000000000000000000000000000000000000000000000000002fceb000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcd94b6514d9fd686b58b0f1ecbbaf3a682e259f69eceb09058993ea1432a3e6b",
      "signature": {
        "s": "0x4c0bb9d6f6fed50a68a59af998431969a8cc4bb84c7d143814459e891573746b",
        "r": "0x395b68bd8beb8a507d9671dead38ac22c8185dc329eebfce7a1d344d73a38c8a",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6245708125970f7526479cb7c45a4f2ec33c04cb08ed9458f941a2054e5c3c6d",
      "signature": {
        "s": "0x2bf3ad408a2dc414f75b868a3256caf89282b6d241ad0dd6874d640656e16e15",
        "r": "0x8eea97239aecee9dd375fd14808d882ba2c1d01bf19c2935513afb01faf11a1e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "195819",
    "total": "195819"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "195819",
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
            "amount": "538556"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "195"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMjk0ODQxZi0xOTY4LTVkY2MtYmZhNS1iNjMzYmFkOWExNjgifQ==",
    "nonce": 455,
    "balances": {
      "current": "10000001545390725",
      "previous": "10000001545586739"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0c255cac8f1bd9e1e73ef86495b54100bf94bf22",
    "nonce": 20,
    "balances": {
      "current": "195819",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:09.196Z",
  "updated": "2020-05-22T08:02:09.258Z",
  "id": "5ec78701b0c6090011d5a964"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002fceb0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `195819`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``