# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x38291B8A510161b890Af154e81c88a98C4505Ae6`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000001d9b09e0000000000000000000000000000000000000000000000000000000001d9b09e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001d9b09e0000000000000000000000000000000000000000000000000000000001d9b09ec9f43d804ae87f0e9d5f28622cb61543e33739a96be32b38d4efeff633359e00aa977b1552f56db2abb073209e1e9d4725cccdb7fd8b316f014864ad8092a7a273c986f64a143930bf4d83ff15e92f0ab2ce6274c7c798fdd73d9fa18ac28bd2000000000000000000000000000000000000000000000000000000000000001c003ef6f08efb1b7719bd0991f59c209337663063e28743e19b8ea69f12c85dc9527b7bedef11aa855108e567aa9c6ca7a59ad7bd696b129f573c9f9191b0125c44559a87f4ed5aac563566dcb0bb4c9f6ca4accc9bcd0d43b3c26601eae7c3e0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d378bdf6000000000000000000000000000000000000000000000000002386f2d552e7d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000794300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006461500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a575577596d4e6c4e5330314f5449354c5455355a6d5174595445354d7930334f4467334d32526d4e6a686b596a516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000038291b8a510161b890af154e81c88a98c4505ae60000000000000000000000000000000000000000000000000000000001d9b09e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc9f43d804ae87f0e9d5f28622cb61543e33739a96be32b38d4efeff633359e00",
      "signature": {
        "s": "0x73c986f64a143930bf4d83ff15e92f0ab2ce6274c7c798fdd73d9fa18ac28bd2",
        "r": "0xaa977b1552f56db2abb073209e1e9d4725cccdb7fd8b316f014864ad8092a7a2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x003ef6f08efb1b7719bd0991f59c209337663063e28743e19b8ea69f12c85dc9",
      "signature": {
        "s": "0x44559a87f4ed5aac563566dcb0bb4c9f6ca4accc9bcd0d43b3c26601eae7c3e0",
        "r": "0x527b7bedef11aa855108e567aa9c6ca7a59ad7bd696b129f573c9f9191b0125c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31043742",
    "total": "31043742"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31043742",
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
            "amount": "411157"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "31043"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWUwYmNlNS01OTI5LTU5ZmQtYTE5My03ODg3M2RmNjhkYjQifQ==",
    "nonce": 115,
    "balances": {
      "current": "10000001672986102",
      "previous": "10000001704060887"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38291b8a510161b890af154e81c88a98c4505ae6",
    "nonce": 20,
    "balances": {
      "current": "31043742",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:41.030Z",
  "updated": "2020-05-22T07:59:42.118Z",
  "id": "5ec7866db0c6090011d5a8fc"
}
```
* *stageAmount*: `31043742`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000001d9b09e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000001d9b09e0000000000000000000000000000000000000000000000000000000001d9b09ec9f43d804ae87f0e9d5f28622cb61543e33739a96be32b38d4efeff633359e00aa977b1552f56db2abb073209e1e9d4725cccdb7fd8b316f014864ad8092a7a273c986f64a143930bf4d83ff15e92f0ab2ce6274c7c798fdd73d9fa18ac28bd2000000000000000000000000000000000000000000000000000000000000001c003ef6f08efb1b7719bd0991f59c209337663063e28743e19b8ea69f12c85dc9527b7bedef11aa855108e567aa9c6ca7a59ad7bd696b129f573c9f9191b0125c44559a87f4ed5aac563566dcb0bb4c9f6ca4accc9bcd0d43b3c26601eae7c3e0000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000007300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d378bdf6000000000000000000000000000000000000000000000000002386f2d552e7d700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000794300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006461500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a575577596d4e6c4e5330314f5449354c5455355a6d5174595445354d7930334f4467334d32526d4e6a686b596a516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000038291b8a510161b890af154e81c88a98c4505ae60000000000000000000000000000000000000000000000000000000001d9b09e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc9f43d804ae87f0e9d5f28622cb61543e33739a96be32b38d4efeff633359e00",
      "signature": {
        "s": "0x73c986f64a143930bf4d83ff15e92f0ab2ce6274c7c798fdd73d9fa18ac28bd2",
        "r": "0xaa977b1552f56db2abb073209e1e9d4725cccdb7fd8b316f014864ad8092a7a2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x003ef6f08efb1b7719bd0991f59c209337663063e28743e19b8ea69f12c85dc9",
      "signature": {
        "s": "0x44559a87f4ed5aac563566dcb0bb4c9f6ca4accc9bcd0d43b3c26601eae7c3e0",
        "r": "0x527b7bedef11aa855108e567aa9c6ca7a59ad7bd696b129f573c9f9191b0125c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31043742",
    "total": "31043742"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31043742",
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
            "amount": "411157"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "31043"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZWUwYmNlNS01OTI5LTU5ZmQtYTE5My03ODg3M2RmNjhkYjQifQ==",
    "nonce": 115,
    "balances": {
      "current": "10000001672986102",
      "previous": "10000001704060887"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x38291b8a510161b890af154e81c88a98c4505ae6",
    "nonce": 20,
    "balances": {
      "current": "31043742",
      "previous": "0"
    }
  },
  "blockNumber": "10114489",
  "created": "2020-05-22T07:59:41.030Z",
  "updated": "2020-05-22T07:59:42.118Z",
  "id": "5ec7866db0c6090011d5a8fc"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000001d9b09e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `31043742`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``