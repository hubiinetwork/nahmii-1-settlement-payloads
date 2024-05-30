# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc7c9380936f22f0cd3EBd0B90c7585272fFeEb70`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000002accd6f6d56657b575cb449ff6b16c8d3fda63584d1d78aaa1613310c6a21cf28b838eae75241b27eea5f700b8e6bad933ad09e227adf40af228205d16f5013fd0c4884f69466cf35004e3cc7ebb5b7f1b8be7c8ea9a39792cf823881f8106edb000000000000000000000000000000000000000000000000000000000000001cbc8f7628b5e7af54c848aa44127617817b705b031331702f4c15b9fa5eb2477276339692d5e44f5378ddf99defaa85b76c09bed805dd7fcda0b22f57b99f579e39bd12b6cfd0cd9698ee8c6b283cf3be16e3d8f13b9c66cf3d8683f76496b0c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcaee6a0000000000000000000000000000000000000000000000000002386f2bcaee6a300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c179b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d4e6b4d6d55354e79316a4e5755794c54566c5a574574595445344d6930794d5441304e7a49794f57566a4e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000c7c9380936f22f0cd3ebd0b90c7585272ffeeb700000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaccd6f6d56657b575cb449ff6b16c8d3fda63584d1d78aaa1613310c6a21cf28",
      "signature": {
        "s": "0x0c4884f69466cf35004e3cc7ebb5b7f1b8be7c8ea9a39792cf823881f8106edb",
        "r": "0xb838eae75241b27eea5f700b8e6bad933ad09e227adf40af228205d16f5013fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbc8f7628b5e7af54c848aa44127617817b705b031331702f4c15b9fa5eb24772",
      "signature": {
        "s": "0x39bd12b6cfd0cd9698ee8c6b283cf3be16e3d8f13b9c66cf3d8683f76496b0c9",
        "r": "0x76339692d5e44f5378ddf99defaa85b76c09bed805dd7fcda0b22f57b99f579e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "792475"
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
    "data": "eyJyZWYiOiJlZmNkMmU5Ny1jNWUyLTVlZWEtYTE4Mi0yMTA0NzIyOWVjNjIifQ==",
    "nonce": 2153,
    "balances": {
      "current": "10000001290659488",
      "previous": "10000001290659491"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc7c9380936f22f0cd3ebd0b90c7585272ffeeb70",
    "nonce": 4,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:40.708Z",
  "updated": "2020-05-22T08:14:40.777Z",
  "id": "5ec789f0b0c6090011d5aba1"
}
```
* *stageAmount*: `2`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000002accd6f6d56657b575cb449ff6b16c8d3fda63584d1d78aaa1613310c6a21cf28b838eae75241b27eea5f700b8e6bad933ad09e227adf40af228205d16f5013fd0c4884f69466cf35004e3cc7ebb5b7f1b8be7c8ea9a39792cf823881f8106edb000000000000000000000000000000000000000000000000000000000000001cbc8f7628b5e7af54c848aa44127617817b705b031331702f4c15b9fa5eb2477276339692d5e44f5378ddf99defaa85b76c09bed805dd7fcda0b22f57b99f579e39bd12b6cfd0cd9698ee8c6b283cf3be16e3d8f13b9c66cf3d8683f76496b0c9000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcaee6a0000000000000000000000000000000000000000000000000002386f2bcaee6a300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c179b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6d4e6b4d6d55354e79316a4e5755794c54566c5a574574595445344d6930794d5441304e7a49794f57566a4e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000c7c9380936f22f0cd3ebd0b90c7585272ffeeb700000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xaccd6f6d56657b575cb449ff6b16c8d3fda63584d1d78aaa1613310c6a21cf28",
      "signature": {
        "s": "0x0c4884f69466cf35004e3cc7ebb5b7f1b8be7c8ea9a39792cf823881f8106edb",
        "r": "0xb838eae75241b27eea5f700b8e6bad933ad09e227adf40af228205d16f5013fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbc8f7628b5e7af54c848aa44127617817b705b031331702f4c15b9fa5eb24772",
      "signature": {
        "s": "0x39bd12b6cfd0cd9698ee8c6b283cf3be16e3d8f13b9c66cf3d8683f76496b0c9",
        "r": "0x76339692d5e44f5378ddf99defaa85b76c09bed805dd7fcda0b22f57b99f579e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2",
    "total": "2"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2",
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
            "amount": "792475"
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
    "data": "eyJyZWYiOiJlZmNkMmU5Ny1jNWUyLTVlZWEtYTE4Mi0yMTA0NzIyOWVjNjIifQ==",
    "nonce": 2153,
    "balances": {
      "current": "10000001290659488",
      "previous": "10000001290659491"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc7c9380936f22f0cd3ebd0b90c7585272ffeeb70",
    "nonce": 4,
    "balances": {
      "current": "2",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:40.708Z",
  "updated": "2020-05-22T08:14:40.777Z",
  "id": "5ec789f0b0c6090011d5aba1"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``