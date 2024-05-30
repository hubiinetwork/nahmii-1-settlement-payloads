# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1c7429f62595097315289ceBaC1fDbdA587Ad512`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000049ad50000000000000000000000000000000000000000000000000000000000049ad500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000049ad50000000000000000000000000000000000000000000000000000000000049ad5bb93843efa10880d6f685cb15601d0ec1ca7a2612b45f7ffca5b12cea6f08ac01b18b6d1ec0480208fad6ec2cc27b8398129552a1ffc35e5f4d28f9a6243d2d71f9933eab75b25976730e9a2324246a52b3dd41e0f626e2ccd6260e5cb5de6f2000000000000000000000000000000000000000000000000000000000000001cb8879a1f62e65a403bb17830abf9f592142c954dd0e0ea00c1fe1c16c94cac61a5b6318c5f053fcb4821ba537de7256033d62f58fec7dc9270357f6af66190205dea855f8d7d24d3a5231e8ba15d3aea279fab8a996dca5d5f5d3673f8f448cc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2decbb476000000000000000000000000000000000000000000000000002386f2ded0507800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000012d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000360c200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a5459785a4451314e43316a4d474d794c5455324e4745744f4759774e7930784d4745324f5459344e5759355957516966513d3d00000000000000000000000000000000000000000000000000000000000000110000000000000000000000001c7429f62595097315289cebac1fdbda587ad5120000000000000000000000000000000000000000000000000000000000049ad5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb93843efa10880d6f685cb15601d0ec1ca7a2612b45f7ffca5b12cea6f08ac0",
      "signature": {
        "s": "0x1f9933eab75b25976730e9a2324246a52b3dd41e0f626e2ccd6260e5cb5de6f2",
        "r": "0x1b18b6d1ec0480208fad6ec2cc27b8398129552a1ffc35e5f4d28f9a6243d2d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb8879a1f62e65a403bb17830abf9f592142c954dd0e0ea00c1fe1c16c94cac61",
      "signature": {
        "s": "0x5dea855f8d7d24d3a5231e8ba15d3aea279fab8a996dca5d5f5d3673f8f448cc",
        "r": "0xa5b6318c5f053fcb4821ba537de7256033d62f58fec7dc9270357f6af6619020",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "301781",
    "total": "301781"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "301781",
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
            "amount": "221378"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "301"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZTYxZDQ1NC1jMGMyLTU2NGEtOGYwNy0xMGE2OTY4NWY5YWQifQ==",
    "nonce": 72,
    "balances": {
      "current": "10000001862972534",
      "previous": "10000001863274616"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1c7429f62595097315289cebac1fdbda587ad512",
    "nonce": 17,
    "balances": {
      "current": "301781",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:29.060Z",
  "updated": "2020-05-22T07:59:29.133Z",
  "id": "5ec78661e5756b00111b7f88"
}
```
* *stageAmount*: `301781`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000049ad500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000049ad50000000000000000000000000000000000000000000000000000000000049ad5bb93843efa10880d6f685cb15601d0ec1ca7a2612b45f7ffca5b12cea6f08ac01b18b6d1ec0480208fad6ec2cc27b8398129552a1ffc35e5f4d28f9a6243d2d71f9933eab75b25976730e9a2324246a52b3dd41e0f626e2ccd6260e5cb5de6f2000000000000000000000000000000000000000000000000000000000000001cb8879a1f62e65a403bb17830abf9f592142c954dd0e0ea00c1fe1c16c94cac61a5b6318c5f053fcb4821ba537de7256033d62f58fec7dc9270357f6af66190205dea855f8d7d24d3a5231e8ba15d3aea279fab8a996dca5d5f5d3673f8f448cc000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000004800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2decbb476000000000000000000000000000000000000000000000000002386f2ded0507800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000012d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000360c200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a5459785a4451314e43316a4d474d794c5455324e4745744f4759774e7930784d4745324f5459344e5759355957516966513d3d00000000000000000000000000000000000000000000000000000000000000110000000000000000000000001c7429f62595097315289cebac1fdbda587ad5120000000000000000000000000000000000000000000000000000000000049ad5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbb93843efa10880d6f685cb15601d0ec1ca7a2612b45f7ffca5b12cea6f08ac0",
      "signature": {
        "s": "0x1f9933eab75b25976730e9a2324246a52b3dd41e0f626e2ccd6260e5cb5de6f2",
        "r": "0x1b18b6d1ec0480208fad6ec2cc27b8398129552a1ffc35e5f4d28f9a6243d2d7",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb8879a1f62e65a403bb17830abf9f592142c954dd0e0ea00c1fe1c16c94cac61",
      "signature": {
        "s": "0x5dea855f8d7d24d3a5231e8ba15d3aea279fab8a996dca5d5f5d3673f8f448cc",
        "r": "0xa5b6318c5f053fcb4821ba537de7256033d62f58fec7dc9270357f6af6619020",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "301781",
    "total": "301781"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "301781",
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
            "amount": "221378"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "301"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZTYxZDQ1NC1jMGMyLTU2NGEtOGYwNy0xMGE2OTY4NWY5YWQifQ==",
    "nonce": 72,
    "balances": {
      "current": "10000001862972534",
      "previous": "10000001863274616"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1c7429f62595097315289cebac1fdbda587ad512",
    "nonce": 17,
    "balances": {
      "current": "301781",
      "previous": "0"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:29.060Z",
  "updated": "2020-05-22T07:59:29.133Z",
  "id": "5ec78661e5756b00111b7f88"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000049ad50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `301781`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``