# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x415b07c5F73B56Ff03A6CA8FB97ec8E512dF38Bf`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000023ca00000000000000000000000000000000000000000000000000000000000023ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000023ca00000000000000000000000000000000000000000000000000000000000023ca25f30eda21e8c02a0f1204a3f2a0320c8ff0ccac8a784b182394c3885dc048f9098d41f7ff895e0fa31ab0dfb4991d807b00d6061449969de9d7c7b2326fedc119fd4a77d49b86d1e3b1379e6f700efe9bb171931cf795d8cabf22b667b59554000000000000000000000000000000000000000000000000000000000000001cd81aebf40bc48afc6d55104cb60a3d2c7b462b1e25a737e680c888de66b0b416b9c3f099c5a736a17301d9e16d286b6dd46caae9dd23a528d433526de12d16a54a6fb48ea268ba14aabc7686eb205d912fdd35a58803ffc031b5b6637f5eb0a5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002c900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf365d5000000000000000000000000000000000000000000000000002386f2caf389a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008734d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a4a6a5954417a4e7930774d5455774c5455304d4759744f5455785a4330344d7a6b784f5756694e6a45334f44596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000415b07c5f73b56ff03a6ca8fb97ec8e512df38bf00000000000000000000000000000000000000000000000000000000000023ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25f30eda21e8c02a0f1204a3f2a0320c8ff0ccac8a784b182394c3885dc048f9",
      "signature": {
        "s": "0x19fd4a77d49b86d1e3b1379e6f700efe9bb171931cf795d8cabf22b667b59554",
        "r": "0x098d41f7ff895e0fa31ab0dfb4991d807b00d6061449969de9d7c7b2326fedc1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd81aebf40bc48afc6d55104cb60a3d2c7b462b1e25a737e680c888de66b0b416",
      "signature": {
        "s": "0x4a6fb48ea268ba14aabc7686eb205d912fdd35a58803ffc031b5b6637f5eb0a5",
        "r": "0xb9c3f099c5a736a17301d9e16d286b6dd46caae9dd23a528d433526de12d16a5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9162",
    "total": "9162"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9162",
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
            "amount": "553805"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzJjYTAzNy0wMTUwLTU0MGYtOTUxZC04MzkxOWViNjE3ODYifQ==",
    "nonce": 713,
    "balances": {
      "current": "10000001530029525",
      "previous": "10000001530038696"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x415b07c5f73b56ff03a6ca8fb97ec8e512df38bf",
    "nonce": 20,
    "balances": {
      "current": "9162",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:09.799Z",
  "updated": "2020-05-22T08:04:10.891Z",
  "id": "5ec78779b0c6090011d5a9bd"
}
```
* *stageAmount*: `9162`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000023ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000023ca00000000000000000000000000000000000000000000000000000000000023ca25f30eda21e8c02a0f1204a3f2a0320c8ff0ccac8a784b182394c3885dc048f9098d41f7ff895e0fa31ab0dfb4991d807b00d6061449969de9d7c7b2326fedc119fd4a77d49b86d1e3b1379e6f700efe9bb171931cf795d8cabf22b667b59554000000000000000000000000000000000000000000000000000000000000001cd81aebf40bc48afc6d55104cb60a3d2c7b462b1e25a737e680c888de66b0b416b9c3f099c5a736a17301d9e16d286b6dd46caae9dd23a528d433526de12d16a54a6fb48ea268ba14aabc7686eb205d912fdd35a58803ffc031b5b6637f5eb0a5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55cb000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000002c900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2caf365d5000000000000000000000000000000000000000000000000002386f2caf389a800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008734d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4e7a4a6a5954417a4e7930774d5455774c5455304d4759744f5455785a4330344d7a6b784f5756694e6a45334f44596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000415b07c5f73b56ff03a6ca8fb97ec8e512df38bf00000000000000000000000000000000000000000000000000000000000023ca000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25f30eda21e8c02a0f1204a3f2a0320c8ff0ccac8a784b182394c3885dc048f9",
      "signature": {
        "s": "0x19fd4a77d49b86d1e3b1379e6f700efe9bb171931cf795d8cabf22b667b59554",
        "r": "0x098d41f7ff895e0fa31ab0dfb4991d807b00d6061449969de9d7c7b2326fedc1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd81aebf40bc48afc6d55104cb60a3d2c7b462b1e25a737e680c888de66b0b416",
      "signature": {
        "s": "0x4a6fb48ea268ba14aabc7686eb205d912fdd35a58803ffc031b5b6637f5eb0a5",
        "r": "0xb9c3f099c5a736a17301d9e16d286b6dd46caae9dd23a528d433526de12d16a5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9162",
    "total": "9162"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9162",
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
            "amount": "553805"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "9"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkNzJjYTAzNy0wMTUwLTU0MGYtOTUxZC04MzkxOWViNjE3ODYifQ==",
    "nonce": 713,
    "balances": {
      "current": "10000001530029525",
      "previous": "10000001530038696"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x415b07c5f73b56ff03a6ca8fb97ec8e512df38bf",
    "nonce": 20,
    "balances": {
      "current": "9162",
      "previous": "0"
    }
  },
  "blockNumber": "10114507",
  "created": "2020-05-22T08:04:09.799Z",
  "updated": "2020-05-22T08:04:10.891Z",
  "id": "5ec78779b0c6090011d5a9bd"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000023ca0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9162`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``