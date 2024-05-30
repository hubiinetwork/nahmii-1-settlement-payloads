# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x73e5d2F260e42c42727dC059aC0dF6b59d31053B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000729e000000000000000000000000000000000000000000000000000000000000729e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000729e000000000000000000000000000000000000000000000000000000000000729e618b6ee4bb3749fc450d0918fb54c0bdca3acfc8525138e7768c2b4515cda30aaa19a8db487a118f9d101c17f342497e1cabec6735b3c188098254e227eab3de1982725f472d576767e5e306c79372f453bd3e32e5e3f441b346eaff39351a1b000000000000000000000000000000000000000000000000000000000000001b0f81d1c3d4aa010cd657936f5554ec10ec2f4be50328c205c8cd02cfa9a8c93b9b3a5f0675e67b302e9002d157ff5a2759273b1882215971f59c1a0442377812729a34249660ee4fab689e63b091905da732b1381155eef5ecf3cd4ac5478e9e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000097700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3ac617000000000000000000000000000000000000000000000000002386f2bc3b38d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c355c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d49345a5449314d793035596a51344c54557a4e6a63744f574e695a69316c593249774f4756695a5459774e57456966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000073e5d2f260e42c42727dc059ac0df6b59d31053b000000000000000000000000000000000000000000000000000000000000729e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x618b6ee4bb3749fc450d0918fb54c0bdca3acfc8525138e7768c2b4515cda30a",
      "signature": {
        "s": "0x1982725f472d576767e5e306c79372f453bd3e32e5e3f441b346eaff39351a1b",
        "r": "0xaa19a8db487a118f9d101c17f342497e1cabec6735b3c188098254e227eab3de",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0f81d1c3d4aa010cd657936f5554ec10ec2f4be50328c205c8cd02cfa9a8c93b",
      "signature": {
        "s": "0x729a34249660ee4fab689e63b091905da732b1381155eef5ecf3cd4ac5478e9e",
        "r": "0x9b3a5f0675e67b302e9002d157ff5a2759273b1882215971f59c1a0442377812",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "29342",
    "total": "29342"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "29342",
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
            "amount": "800092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "29"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZmI4ZTI1My05YjQ4LTUzNjctOWNiZi1lY2IwOGViZTYwNWEifQ==",
    "nonce": 2423,
    "balances": {
      "current": "10000001283048983",
      "previous": "10000001283078354"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73e5d2f260e42c42727dc059ac0df6b59d31053b",
    "nonce": 10,
    "balances": {
      "current": "29342",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:26.284Z",
  "updated": "2020-05-22T08:16:26.352Z",
  "id": "5ec78a5ae5756b00111b8285"
}
```
* *stageAmount*: `29342`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000729e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000729e000000000000000000000000000000000000000000000000000000000000729e618b6ee4bb3749fc450d0918fb54c0bdca3acfc8525138e7768c2b4515cda30aaa19a8db487a118f9d101c17f342497e1cabec6735b3c188098254e227eab3de1982725f472d576767e5e306c79372f453bd3e32e5e3f441b346eaff39351a1b000000000000000000000000000000000000000000000000000000000000001b0f81d1c3d4aa010cd657936f5554ec10ec2f4be50328c205c8cd02cfa9a8c93b9b3a5f0675e67b302e9002d157ff5a2759273b1882215971f59c1a0442377812729a34249660ee4fab689e63b091905da732b1381155eef5ecf3cd4ac5478e9e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000097700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3ac617000000000000000000000000000000000000000000000000002386f2bc3b38d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c355c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6d49345a5449314d793035596a51344c54557a4e6a63744f574e695a69316c593249774f4756695a5459774e57456966513d3d000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000073e5d2f260e42c42727dc059ac0df6b59d31053b000000000000000000000000000000000000000000000000000000000000729e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x618b6ee4bb3749fc450d0918fb54c0bdca3acfc8525138e7768c2b4515cda30a",
      "signature": {
        "s": "0x1982725f472d576767e5e306c79372f453bd3e32e5e3f441b346eaff39351a1b",
        "r": "0xaa19a8db487a118f9d101c17f342497e1cabec6735b3c188098254e227eab3de",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x0f81d1c3d4aa010cd657936f5554ec10ec2f4be50328c205c8cd02cfa9a8c93b",
      "signature": {
        "s": "0x729a34249660ee4fab689e63b091905da732b1381155eef5ecf3cd4ac5478e9e",
        "r": "0x9b3a5f0675e67b302e9002d157ff5a2759273b1882215971f59c1a0442377812",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "29342",
    "total": "29342"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "29342",
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
            "amount": "800092"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "29"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZmI4ZTI1My05YjQ4LTUzNjctOWNiZi1lY2IwOGViZTYwNWEifQ==",
    "nonce": 2423,
    "balances": {
      "current": "10000001283048983",
      "previous": "10000001283078354"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73e5d2f260e42c42727dc059ac0df6b59d31053b",
    "nonce": 10,
    "balances": {
      "current": "29342",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:26.284Z",
  "updated": "2020-05-22T08:16:26.352Z",
  "id": "5ec78a5ae5756b00111b8285"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000729e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `29342`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``