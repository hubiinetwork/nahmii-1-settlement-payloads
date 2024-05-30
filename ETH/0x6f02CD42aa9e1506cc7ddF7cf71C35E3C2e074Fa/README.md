# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6f02CD42aa9e1506cc7ddF7cf71C35E3C2e074Fa`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000001b200000000000000000000000000000000000000000000000000000000000001b2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001b200000000000000000000000000000000000000000000000000000000000001b27e95594a9a624c3e53c567e191b34b7dba757ba9b3457df0eedd72d03d075114e638ae5981b52cfdf21869cedcd930e3936c2fe3ea1e6468cb978c47f9a7051575b8f45e74fb72233862614cb6d3d4002548b6eae03374874e6b89a33fd8b170000000000000000000000000000000000000000000000000000000000000001c6b4e7cf039deaedf17be9becef02f023afaa618edd887b97ec3e1c77583e8671e4603b7ba081fd4c564b604fdde8873fa7587c37c3375a6756af0c4638bec4511a317bed99caccc6b88a08ea08f0f8bebe52cd0cbd66230fe2cc1e6bd29d6f9b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000095000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc50344d000000000000000000000000000000000000000000000000002386f2bc50360000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2fd900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d4467794d6a6b355979316d4d6d46684c545579596a4574596a457a4d69316c4d6a566d4d444531596a41314e57596966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000006f02cd42aa9e1506cc7ddf7cf71c35e3c2e074fa00000000000000000000000000000000000000000000000000000000000001b2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7e95594a9a624c3e53c567e191b34b7dba757ba9b3457df0eedd72d03d075114",
      "signature": {
        "s": "0x75b8f45e74fb72233862614cb6d3d4002548b6eae03374874e6b89a33fd8b170",
        "r": "0xe638ae5981b52cfdf21869cedcd930e3936c2fe3ea1e6468cb978c47f9a70515",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6b4e7cf039deaedf17be9becef02f023afaa618edd887b97ec3e1c77583e8671",
      "signature": {
        "s": "0x1a317bed99caccc6b88a08ea08f0f8bebe52cd0cbd66230fe2cc1e6bd29d6f9b",
        "r": "0xe4603b7ba081fd4c564b604fdde8873fa7587c37c3375a6756af0c4638bec451",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "434",
    "total": "434"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "434",
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
            "amount": "798681"
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
    "data": "eyJyZWYiOiIzMDgyMjk5Yy1mMmFhLTUyYjEtYjEzMi1lMjVmMDE1YjA1NWYifQ==",
    "nonce": 2384,
    "balances": {
      "current": "10000001284453453",
      "previous": "10000001284453888"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f02cd42aa9e1506cc7ddf7cf71c35e3c2e074fa",
    "nonce": 10,
    "balances": {
      "current": "434",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:12.024Z",
  "updated": "2020-05-22T08:16:12.090Z",
  "id": "5ec78a4cb0c6090011d5abea"
}
```
* *stageAmount*: `434`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001b2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000001b200000000000000000000000000000000000000000000000000000000000001b27e95594a9a624c3e53c567e191b34b7dba757ba9b3457df0eedd72d03d075114e638ae5981b52cfdf21869cedcd930e3936c2fe3ea1e6468cb978c47f9a7051575b8f45e74fb72233862614cb6d3d4002548b6eae03374874e6b89a33fd8b170000000000000000000000000000000000000000000000000000000000000001c6b4e7cf039deaedf17be9becef02f023afaa618edd887b97ec3e1c77583e8671e4603b7ba081fd4c564b604fdde8873fa7587c37c3375a6756af0c4638bec4511a317bed99caccc6b88a08ea08f0f8bebe52cd0cbd66230fe2cc1e6bd29d6f9b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000095000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc50344d000000000000000000000000000000000000000000000000002386f2bc50360000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2fd900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d4467794d6a6b355979316d4d6d46684c545579596a4574596a457a4d69316c4d6a566d4d444531596a41314e57596966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000006f02cd42aa9e1506cc7ddf7cf71c35e3c2e074fa00000000000000000000000000000000000000000000000000000000000001b2000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7e95594a9a624c3e53c567e191b34b7dba757ba9b3457df0eedd72d03d075114",
      "signature": {
        "s": "0x75b8f45e74fb72233862614cb6d3d4002548b6eae03374874e6b89a33fd8b170",
        "r": "0xe638ae5981b52cfdf21869cedcd930e3936c2fe3ea1e6468cb978c47f9a70515",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6b4e7cf039deaedf17be9becef02f023afaa618edd887b97ec3e1c77583e8671",
      "signature": {
        "s": "0x1a317bed99caccc6b88a08ea08f0f8bebe52cd0cbd66230fe2cc1e6bd29d6f9b",
        "r": "0xe4603b7ba081fd4c564b604fdde8873fa7587c37c3375a6756af0c4638bec451",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "434",
    "total": "434"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "434",
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
            "amount": "798681"
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
    "data": "eyJyZWYiOiIzMDgyMjk5Yy1mMmFhLTUyYjEtYjEzMi1lMjVmMDE1YjA1NWYifQ==",
    "nonce": 2384,
    "balances": {
      "current": "10000001284453453",
      "previous": "10000001284453888"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f02cd42aa9e1506cc7ddf7cf71c35e3c2e074fa",
    "nonce": 10,
    "balances": {
      "current": "434",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:12.024Z",
  "updated": "2020-05-22T08:16:12.090Z",
  "id": "5ec78a4cb0c6090011d5abea"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001b20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `434`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``