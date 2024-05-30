# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe4b8E80023A478Ad63DB96189F81025c90DadEe1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000000000000000000000000000000000022fbb4c4937e3d660305e0dca52afc51efe886a8fc1bd1a693fdbd79737c44d12c3031894d72715349c8e3b0f78a1203f95ee7193de4d46ca279ab7416481fff57c29ac00544492ec5565deaa496b031bdf95a2a024aa796225c33a9d8cd8adf5bec7b75c000000000000000000000000000000000000000000000000000000000000001b9416f71ae0abe9e5b2c69b04e155cba40094550ed00f078447804ccac765838cae44346d3c81526b6cac045e44dd3a5e25e961b7c18b43b9de9b284eadd7ea96337a813bf115bbedcb5e3fa748fd40940cffd41b93efc19694f3d18ec953ab4e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2f31a73629f5000000000000000000000000000000000000000000000000002e2f33d780c0d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008f4a92000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000042e9cd1b3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a49325a54686b4e5330334d3259794c545533597a67744f5441784f43307a5a47526d4d5467314e7a52694f47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e4b8e80023a478ad63db96189f81025c90dadee1000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x37e3d660305e0dca52afc51efe886a8fc1bd1a693fdbd79737c44d12c3031894",
      "signature": {
        "s": "0x544492ec5565deaa496b031bdf95a2a024aa796225c33a9d8cd8adf5bec7b75c",
        "r": "0xd72715349c8e3b0f78a1203f95ee7193de4d46ca279ab7416481fff57c29ac00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9416f71ae0abe9e5b2c69b04e155cba40094550ed00f078447804ccac765838c",
      "signature": {
        "s": "0x337a813bf115bbedcb5e3fa748fd40940cffd41b93efc19694f3d18ec953ab4e",
        "r": "0xae44346d3c81526b6cac045e44dd3a5e25e961b7c18b43b9de9b284eadd7ea96",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9390738505",
    "total": "9390738505"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9390738505",
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
            "amount": "17961898419"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9390738"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzI2ZThkNS03M2YyLTU3YzgtOTAxOC0zZGRmMTg1NzRiOGYifQ==",
    "nonce": 5247,
    "balances": {
      "current": "12999739233937909",
      "previous": "12999748634067152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe4b8e80023a478ad63db96189f81025c90dadee1",
    "nonce": 22,
    "balances": {
      "current": "9390738505",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:38.079Z",
  "updated": "2020-05-22T08:39:38.152Z",
  "id": "5ec78fcab0c6090011d5af96"
}
```
* *stageAmount*: `9390738505`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000000000000000000000000000000000022fbb4c4937e3d660305e0dca52afc51efe886a8fc1bd1a693fdbd79737c44d12c3031894d72715349c8e3b0f78a1203f95ee7193de4d46ca279ab7416481fff57c29ac00544492ec5565deaa496b031bdf95a2a024aa796225c33a9d8cd8adf5bec7b75c000000000000000000000000000000000000000000000000000000000000001b9416f71ae0abe9e5b2c69b04e155cba40094550ed00f078447804ccac765838cae44346d3c81526b6cac045e44dd3a5e25e961b7c18b43b9de9b284eadd7ea96337a813bf115bbedcb5e3fa748fd40940cffd41b93efc19694f3d18ec953ab4e000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56610000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000147f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e2f31a73629f5000000000000000000000000000000000000000000000000002e2f33d780c0d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000008f4a92000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000042e9cd1b3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a49325a54686b4e5330334d3259794c545533597a67744f5441784f43307a5a47526d4d5467314e7a52694f47596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e4b8e80023a478ad63db96189f81025c90dadee1000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x37e3d660305e0dca52afc51efe886a8fc1bd1a693fdbd79737c44d12c3031894",
      "signature": {
        "s": "0x544492ec5565deaa496b031bdf95a2a024aa796225c33a9d8cd8adf5bec7b75c",
        "r": "0xd72715349c8e3b0f78a1203f95ee7193de4d46ca279ab7416481fff57c29ac00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9416f71ae0abe9e5b2c69b04e155cba40094550ed00f078447804ccac765838c",
      "signature": {
        "s": "0x337a813bf115bbedcb5e3fa748fd40940cffd41b93efc19694f3d18ec953ab4e",
        "r": "0xae44346d3c81526b6cac045e44dd3a5e25e961b7c18b43b9de9b284eadd7ea96",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9390738505",
    "total": "9390738505"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9390738505",
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
            "amount": "17961898419"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "9390738"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzI2ZThkNS03M2YyLTU3YzgtOTAxOC0zZGRmMTg1NzRiOGYifQ==",
    "nonce": 5247,
    "balances": {
      "current": "12999739233937909",
      "previous": "12999748634067152"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe4b8e80023a478ad63db96189f81025c90dadee1",
    "nonce": 22,
    "balances": {
      "current": "9390738505",
      "previous": "0"
    }
  },
  "blockNumber": "10114657",
  "created": "2020-05-22T08:39:38.079Z",
  "updated": "2020-05-22T08:39:38.152Z",
  "id": "5ec78fcab0c6090011d5af96"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000022fbb4c49000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9390738505`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`