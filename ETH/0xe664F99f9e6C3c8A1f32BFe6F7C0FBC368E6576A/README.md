# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe664F99f9e6C3c8A1f32BFe6F7C0FBC368E6576A`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000164770000000000000000000000000000000000000000000000000000000000016477000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000164770000000000000000000000000000000000000000000000000000000000016477033c762bd15bf42fc2eb1dbfc20bea95698b1cd1966888b1bd59b3126c0479c7fe6f3290cf847ae172e60f31751701c3781ad345ba57ee3fea79fd86d40d966354f86472058b590579fbb5dcfa306aa980390344b3167eaa317880ef5da3ce06000000000000000000000000000000000000000000000000000000000000001bf7da193de2bf42b98049a67f16be05232edb88884c6aa1d8802b95f53e1b9fcbb4c921b88703769caa105af0b8dd29d9981413101b8875bbd802358127fe41e50b7b58216401a4cb5511e04d187cedb422a3df7a5dc391e43c1a336f6b821b84000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cde0a9b4000000000000000000000000000000000000000000000000002386f2cde20e8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b42900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f4755355a546c695969303459546c6b4c5455794f4441744f546b305a6930334d5455324f544d794f57566b597a516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e664f99f9e6c3c8a1f32bfe6f7c0fbc368e6576a0000000000000000000000000000000000000000000000000000000000016477000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x033c762bd15bf42fc2eb1dbfc20bea95698b1cd1966888b1bd59b3126c0479c7",
      "signature": {
        "s": "0x54f86472058b590579fbb5dcfa306aa980390344b3167eaa317880ef5da3ce06",
        "r": "0xfe6f3290cf847ae172e60f31751701c3781ad345ba57ee3fea79fd86d40d9663",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf7da193de2bf42b98049a67f16be05232edb88884c6aa1d8802b95f53e1b9fcb",
      "signature": {
        "s": "0x0b7b58216401a4cb5511e04d187cedb422a3df7a5dc391e43c1a336f6b821b84",
        "r": "0xb4c921b88703769caa105af0b8dd29d9981413101b8875bbd802358127fe41e5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "91255",
    "total": "91255"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "91255",
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
            "amount": "504873"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "91"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGU5ZTliYi04YTlkLTUyODAtOTk0Zi03MTU2OTMyOWVkYzQifQ==",
    "nonce": 230,
    "balances": {
      "current": "10000001579133364",
      "previous": "10000001579224710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe664f99f9e6c3c8a1f32bfe6f7c0fbc368e6576a",
    "nonce": 20,
    "balances": {
      "current": "91255",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:32.550Z",
  "updated": "2020-05-22T08:00:32.625Z",
  "id": "5ec786a0005df800101bc25d"
}
```
* *stageAmount*: `91255`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000016477000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000164770000000000000000000000000000000000000000000000000000000000016477033c762bd15bf42fc2eb1dbfc20bea95698b1cd1966888b1bd59b3126c0479c7fe6f3290cf847ae172e60f31751701c3781ad345ba57ee3fea79fd86d40d966354f86472058b590579fbb5dcfa306aa980390344b3167eaa317880ef5da3ce06000000000000000000000000000000000000000000000000000000000000001bf7da193de2bf42b98049a67f16be05232edb88884c6aa1d8802b95f53e1b9fcbb4c921b88703769caa105af0b8dd29d9981413101b8875bbd802358127fe41e50b7b58216401a4cb5511e04d187cedb422a3df7a5dc391e43c1a336f6b821b84000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000e600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cde0a9b4000000000000000000000000000000000000000000000000002386f2cde20e8600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000007b42900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f4755355a546c695969303459546c6b4c5455794f4441744f546b305a6930334d5455324f544d794f57566b597a516966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e664f99f9e6c3c8a1f32bfe6f7c0fbc368e6576a0000000000000000000000000000000000000000000000000000000000016477000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x033c762bd15bf42fc2eb1dbfc20bea95698b1cd1966888b1bd59b3126c0479c7",
      "signature": {
        "s": "0x54f86472058b590579fbb5dcfa306aa980390344b3167eaa317880ef5da3ce06",
        "r": "0xfe6f3290cf847ae172e60f31751701c3781ad345ba57ee3fea79fd86d40d9663",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf7da193de2bf42b98049a67f16be05232edb88884c6aa1d8802b95f53e1b9fcb",
      "signature": {
        "s": "0x0b7b58216401a4cb5511e04d187cedb422a3df7a5dc391e43c1a336f6b821b84",
        "r": "0xb4c921b88703769caa105af0b8dd29d9981413101b8875bbd802358127fe41e5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "91255",
    "total": "91255"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "91255",
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
            "amount": "504873"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "91"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OGU5ZTliYi04YTlkLTUyODAtOTk0Zi03MTU2OTMyOWVkYzQifQ==",
    "nonce": 230,
    "balances": {
      "current": "10000001579133364",
      "previous": "10000001579224710"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe664f99f9e6c3c8a1f32bfe6f7c0fbc368e6576a",
    "nonce": 20,
    "balances": {
      "current": "91255",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:32.550Z",
  "updated": "2020-05-22T08:00:32.625Z",
  "id": "5ec786a0005df800101bc25d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000164770000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `91255`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``