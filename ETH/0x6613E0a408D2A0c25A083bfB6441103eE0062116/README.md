# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6613E0a408D2A0c25A083bfB6441103eE0062116`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000703b000000000000000000000000000000000000000000000000000000000000703b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000703b000000000000000000000000000000000000000000000000000000000000703bc227050c061bbaf448fabf752f7a0d3320b0038b1469177394a66043c6ee5330e6226e578ecc9ba232f6ee7593dbeef377ab13478c56fc3515629e5f4c35745058acbdff7c15c764e57da3dee10299b34cf30d18e43a62a23f04a2ce1a8a3952000000000000000000000000000000000000000000000000000000000000001b24bd571d829f3e9d4789d0badbacec8de939c7d0109fedb6f0d4723ee78c883799d359d589578a7f51c30c1990b38f07a6ea32cd2793e51e28bf8e1426782eb1062c5c4d93ebf2441ba9d35069b6f7e06118f6f7e8eda00a637b099da9e85e94000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4e6a50000000000000000000000000000000000000000000000000002386f2bc4edaa700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c305600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d474e694d6a55354f5330315a6d49784c5455345a574974596d4e6c5969316d4e32566d5a5451314f546b305a6d456966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000006613e0a408d2a0c25a083bfb6441103ee0062116000000000000000000000000000000000000000000000000000000000000703b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc227050c061bbaf448fabf752f7a0d3320b0038b1469177394a66043c6ee5330",
      "signature": {
        "s": "0x58acbdff7c15c764e57da3dee10299b34cf30d18e43a62a23f04a2ce1a8a3952",
        "r": "0xe6226e578ecc9ba232f6ee7593dbeef377ab13478c56fc3515629e5f4c357450",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x24bd571d829f3e9d4789d0badbacec8de939c7d0109fedb6f0d4723ee78c8837",
      "signature": {
        "s": "0x062c5c4d93ebf2441ba9d35069b6f7e06118f6f7e8eda00a637b099da9e85e94",
        "r": "0x99d359d589578a7f51c30c1990b38f07a6ea32cd2793e51e28bf8e1426782eb1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "28731",
    "total": "28731"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28731",
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
            "amount": "798806"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "28"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MGNiMjU5OS01ZmIxLTU4ZWItYmNlYi1mN2VmZTQ1OTk0ZmEifQ==",
    "nonce": 2404,
    "balances": {
      "current": "10000001284336208",
      "previous": "10000001284364967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6613e0a408d2a0c25a083bfb6441103ee0062116",
    "nonce": 10,
    "balances": {
      "current": "28731",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:17.771Z",
  "updated": "2020-05-22T08:16:17.853Z",
  "id": "5ec78a51e5756b00111b827b"
}
```
* *stageAmount*: `28731`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000703b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000703b000000000000000000000000000000000000000000000000000000000000703bc227050c061bbaf448fabf752f7a0d3320b0038b1469177394a66043c6ee5330e6226e578ecc9ba232f6ee7593dbeef377ab13478c56fc3515629e5f4c35745058acbdff7c15c764e57da3dee10299b34cf30d18e43a62a23f04a2ce1a8a3952000000000000000000000000000000000000000000000000000000000000001b24bd571d829f3e9d4789d0badbacec8de939c7d0109fedb6f0d4723ee78c883799d359d589578a7f51c30c1990b38f07a6ea32cd2793e51e28bf8e1426782eb1062c5c4d93ebf2441ba9d35069b6f7e06118f6f7e8eda00a637b099da9e85e94000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc4e6a50000000000000000000000000000000000000000000000000002386f2bc4edaa700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c305600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d474e694d6a55354f5330315a6d49784c5455345a574974596d4e6c5969316d4e32566d5a5451314f546b305a6d456966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000006613e0a408d2a0c25a083bfb6441103ee0062116000000000000000000000000000000000000000000000000000000000000703b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc227050c061bbaf448fabf752f7a0d3320b0038b1469177394a66043c6ee5330",
      "signature": {
        "s": "0x58acbdff7c15c764e57da3dee10299b34cf30d18e43a62a23f04a2ce1a8a3952",
        "r": "0xe6226e578ecc9ba232f6ee7593dbeef377ab13478c56fc3515629e5f4c357450",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x24bd571d829f3e9d4789d0badbacec8de939c7d0109fedb6f0d4723ee78c8837",
      "signature": {
        "s": "0x062c5c4d93ebf2441ba9d35069b6f7e06118f6f7e8eda00a637b099da9e85e94",
        "r": "0x99d359d589578a7f51c30c1990b38f07a6ea32cd2793e51e28bf8e1426782eb1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "28731",
    "total": "28731"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "28731",
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
            "amount": "798806"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "28"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MGNiMjU5OS01ZmIxLTU4ZWItYmNlYi1mN2VmZTQ1OTk0ZmEifQ==",
    "nonce": 2404,
    "balances": {
      "current": "10000001284336208",
      "previous": "10000001284364967"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6613e0a408d2a0c25a083bfb6441103ee0062116",
    "nonce": 10,
    "balances": {
      "current": "28731",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:17.771Z",
  "updated": "2020-05-22T08:16:17.853Z",
  "id": "5ec78a51e5756b00111b827b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000703b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `28731`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``