# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3595f971342Ba703132BEeaDDFB7D6631a78023a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000e764ed53f32147ce3c6d2ae6006b6d55c8cc93279bb4fac50509046deb733b4d23789b00ce06704c3311e7042f7f89c60385de74f8737f2a677fe540fd27be5a97c8bdfa05b94e592ad1b4c87cad1d3efd1ba843209d9050546fa116a03b89f02000000000000000000000000000000000000000000000000000000000000001b037a2eb7a579375453d781e9130e25878027ee99f0904ebaded73ee2105a09371a12a338e2b7a5aabd14f382fc9924e99b5b18fee536b2e0586ca215406d026448de4c84582004ca1c734db09e6bdfaf39787909246c3c378a20d6b28f2aad91000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000099000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc395a45000000000000000000000000000000000000000000000000002386f2bc395a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c35c400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f474d32593255305a69307a4f5442694c5456684f474974596a4a69597930785a6d4d785a6a6468593249314d446b6966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000003595f971342ba703132beeaddfb7d6631a78023a000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x764ed53f32147ce3c6d2ae6006b6d55c8cc93279bb4fac50509046deb733b4d2",
      "signature": {
        "s": "0x7c8bdfa05b94e592ad1b4c87cad1d3efd1ba843209d9050546fa116a03b89f02",
        "r": "0x3789b00ce06704c3311e7042f7f89c60385de74f8737f2a677fe540fd27be5a9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x037a2eb7a579375453d781e9130e25878027ee99f0904ebaded73ee2105a0937",
      "signature": {
        "s": "0x48de4c84582004ca1c734db09e6bdfaf39787909246c3c378a20d6b28f2aad91",
        "r": "0x1a12a338e2b7a5aabd14f382fc9924e99b5b18fee536b2e0586ca215406d0264",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14",
    "total": "14"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14",
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
            "amount": "800196"
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
    "data": "eyJyZWYiOiJkOGM2Y2U0Zi0zOTBiLTVhOGItYjJiYy0xZmMxZjdhY2I1MDkifQ==",
    "nonce": 2448,
    "balances": {
      "current": "10000001282955845",
      "previous": "10000001282955860"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3595f971342ba703132beeaddfb7d6631a78023a",
    "nonce": 3,
    "balances": {
      "current": "14",
      "previous": "0"
    }
  },
  "blockNumber": "10114555",
  "created": "2020-05-22T08:16:40.243Z",
  "updated": "2020-05-22T08:16:40.311Z",
  "id": "5ec78a68005df800101bc556"
}
```
* *stageAmount*: `14`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000e764ed53f32147ce3c6d2ae6006b6d55c8cc93279bb4fac50509046deb733b4d23789b00ce06704c3311e7042f7f89c60385de74f8737f2a677fe540fd27be5a97c8bdfa05b94e592ad1b4c87cad1d3efd1ba843209d9050546fa116a03b89f02000000000000000000000000000000000000000000000000000000000000001b037a2eb7a579375453d781e9130e25878027ee99f0904ebaded73ee2105a09371a12a338e2b7a5aabd14f382fc9924e99b5b18fee536b2e0586ca215406d026448de4c84582004ca1c734db09e6bdfaf39787909246c3c378a20d6b28f2aad91000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000099000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc395a45000000000000000000000000000000000000000000000000002386f2bc395a5400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c35c400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4f474d32593255305a69307a4f5442694c5456684f474974596a4a69597930785a6d4d785a6a6468593249314d446b6966513d3d00000000000000000000000000000000000000000000000000000000000000030000000000000000000000003595f971342ba703132beeaddfb7d6631a78023a000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x764ed53f32147ce3c6d2ae6006b6d55c8cc93279bb4fac50509046deb733b4d2",
      "signature": {
        "s": "0x7c8bdfa05b94e592ad1b4c87cad1d3efd1ba843209d9050546fa116a03b89f02",
        "r": "0x3789b00ce06704c3311e7042f7f89c60385de74f8737f2a677fe540fd27be5a9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x037a2eb7a579375453d781e9130e25878027ee99f0904ebaded73ee2105a0937",
      "signature": {
        "s": "0x48de4c84582004ca1c734db09e6bdfaf39787909246c3c378a20d6b28f2aad91",
        "r": "0x1a12a338e2b7a5aabd14f382fc9924e99b5b18fee536b2e0586ca215406d0264",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "14",
    "total": "14"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "14",
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
            "amount": "800196"
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
    "data": "eyJyZWYiOiJkOGM2Y2U0Zi0zOTBiLTVhOGItYjJiYy0xZmMxZjdhY2I1MDkifQ==",
    "nonce": 2448,
    "balances": {
      "current": "10000001282955845",
      "previous": "10000001282955860"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3595f971342ba703132beeaddfb7d6631a78023a",
    "nonce": 3,
    "balances": {
      "current": "14",
      "previous": "0"
    }
  },
  "blockNumber": "10114555",
  "created": "2020-05-22T08:16:40.243Z",
  "updated": "2020-05-22T08:16:40.311Z",
  "id": "5ec78a68005df800101bc556"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000000e0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``