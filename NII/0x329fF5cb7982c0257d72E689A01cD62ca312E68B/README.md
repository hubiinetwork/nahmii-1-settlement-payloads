# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x329fF5cb7982c0257d72E689A01cD62ca312E68B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000005802c8000000000000000000000000000000000000000000000000000000000002162e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002162e00000000000000000000000000000000000000000000000000000000003a8d9aeb56a28acbd8bb05227a5eaa299c422ed5a59219d7ad21122c67f8a94932b8abb7dc89fb4a44d04af4c18ed7bc3d7831bc089e53a33bfa190365269b125ddd2c63904ca930dc307d33c0886e7f11589c84550da28f513e92aa6cccf62d437b01000000000000000000000000000000000000000000000000000000000000001b89ea840c80db69aa8a01f5c5052dbe02be887820f7f5fcd936750f2ac0db423d73f43b3aee1e9bde0467b04312b17f9a23e198b2252065451610e707896d4f0e5438407853261a529c9aa081ef0e65130a8955b77080a60fb2ea0fdcaec4167b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2af000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000472d0c30167bfa8a9dd400000000000000000000000000000000000000000000472d0c30167bfa8cb48a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2e107111153f369d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d3259774d6a6b324e6930314f5745324c5455784f574974596d45314d5330344f5455785a6a6c6d4d446c684e7a456966513d3d000000000000000000000000000000000000000000000000000000000000002c000000000000000000000000329ff5cb7982c0257d72e689a01cd62ca312e68b00000000000000000000000000000000000000000000000000000000005802c8000000000000000000000000000000000000000000000000000000000055ec9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeb56a28acbd8bb05227a5eaa299c422ed5a59219d7ad21122c67f8a94932b8ab",
      "signature": {
        "s": "0x63904ca930dc307d33c0886e7f11589c84550da28f513e92aa6cccf62d437b01",
        "r": "0xb7dc89fb4a44d04af4c18ed7bc3d7831bc089e53a33bfa190365269b125ddd2c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x89ea840c80db69aa8a01f5c5052dbe02be887820f7f5fcd936750f2ac0db423d",
      "signature": {
        "s": "0x5438407853261a529c9aa081ef0e65130a8955b77080a60fb2ea0fdcaec4167b",
        "r": "0x73f43b3aee1e9bde0467b04312b17f9a23e198b2252065451610e707896d4f0e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "136750",
    "total": "3837338"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "136750",
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
            "amount": "27636541899660465223325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "136"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhM2YwMjk2Ni01OWE2LTUxOWItYmE1MS04OTUxZjlmMDlhNzEifQ==",
    "nonce": 111279,
    "balances": {
      "current": "336119001993710817418708",
      "previous": "336119001993710817555594"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x329ff5cb7982c0257d72e689a01cd62ca312e68b",
    "nonce": 44,
    "balances": {
      "current": "5767880",
      "previous": "5631130"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:28.584Z",
  "updated": "2022-05-04T08:57:28.662Z",
  "id": "62723ff8bbd75600116d0678"
}
```
* *stageAmount*: `5767880`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002162e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002162e00000000000000000000000000000000000000000000000000000000003a8d9aeb56a28acbd8bb05227a5eaa299c422ed5a59219d7ad21122c67f8a94932b8abb7dc89fb4a44d04af4c18ed7bc3d7831bc089e53a33bfa190365269b125ddd2c63904ca930dc307d33c0886e7f11589c84550da28f513e92aa6cccf62d437b01000000000000000000000000000000000000000000000000000000000000001b89ea840c80db69aa8a01f5c5052dbe02be887820f7f5fcd936750f2ac0db423d73f43b3aee1e9bde0467b04312b17f9a23e198b2252065451610e707896d4f0e5438407853261a529c9aa081ef0e65130a8955b77080a60fb2ea0fdcaec4167b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2af000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000472d0c30167bfa8a9dd400000000000000000000000000000000000000000000472d0c30167bfa8cb48a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da2e107111153f369d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d3259774d6a6b324e6930314f5745324c5455784f574974596d45314d5330344f5455785a6a6c6d4d446c684e7a456966513d3d000000000000000000000000000000000000000000000000000000000000002c000000000000000000000000329ff5cb7982c0257d72e689a01cd62ca312e68b00000000000000000000000000000000000000000000000000000000005802c8000000000000000000000000000000000000000000000000000000000055ec9a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xeb56a28acbd8bb05227a5eaa299c422ed5a59219d7ad21122c67f8a94932b8ab",
      "signature": {
        "s": "0x63904ca930dc307d33c0886e7f11589c84550da28f513e92aa6cccf62d437b01",
        "r": "0xb7dc89fb4a44d04af4c18ed7bc3d7831bc089e53a33bfa190365269b125ddd2c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x89ea840c80db69aa8a01f5c5052dbe02be887820f7f5fcd936750f2ac0db423d",
      "signature": {
        "s": "0x5438407853261a529c9aa081ef0e65130a8955b77080a60fb2ea0fdcaec4167b",
        "r": "0x73f43b3aee1e9bde0467b04312b17f9a23e198b2252065451610e707896d4f0e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "136750",
    "total": "3837338"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "136750",
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
            "amount": "27636541899660465223325"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "136"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhM2YwMjk2Ni01OWE2LTUxOWItYmE1MS04OTUxZjlmMDlhNzEifQ==",
    "nonce": 111279,
    "balances": {
      "current": "336119001993710817418708",
      "previous": "336119001993710817555594"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x329ff5cb7982c0257d72e689a01cd62ca312e68b",
    "nonce": 44,
    "balances": {
      "current": "5767880",
      "previous": "5631130"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:57:28.584Z",
  "updated": "2022-05-04T08:57:28.662Z",
  "id": "62723ff8bbd75600116d0678"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000005802c80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5767880`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`