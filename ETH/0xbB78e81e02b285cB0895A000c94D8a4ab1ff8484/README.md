# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xbB78e81e02b285cB0895A000c94D8a4ab1ff8484`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000761a000000000000000000000000000000000000000000000000000000000000761a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000761a000000000000000000000000000000000000000000000000000000000000761a74314f8a8d3d05e36ebf637e465f7e64bfaaf55293a6e83d27ce69de1816ef9a1abe2b39225aad75fa743a2faee3aee41d07a4eb99309df842c20dec614bbaab097418d244af426a55a3a115543a55d6a08c59569efa6f6b653ca005db7e68b9000000000000000000000000000000000000000000000000000000000000001bb229ef5e0de51947509c5946f9691c10d5b1620ed4aae793fb951656c194597634c08bc133b648a4392c25a4d7d893ad7dfdf3fa019ee574edc9c964ba260d8101673268187c9581aff7d98b9ce254d431bff173ea0eae48d5e562c851f63c2a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb5a96e8000000000000000000000000000000000000000000000000002386f2cb5b0d2000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008593400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a4d314f5467314e7930334d57457a4c5455304d7a41744f575268595330794f546730596a646c4d6a49355932596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bb78e81e02b285cb0895a000c94d8a4ab1ff8484000000000000000000000000000000000000000000000000000000000000761a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x74314f8a8d3d05e36ebf637e465f7e64bfaaf55293a6e83d27ce69de1816ef9a",
      "signature": {
        "s": "0x097418d244af426a55a3a115543a55d6a08c59569efa6f6b653ca005db7e68b9",
        "r": "0x1abe2b39225aad75fa743a2faee3aee41d07a4eb99309df842c20dec614bbaab",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb229ef5e0de51947509c5946f9691c10d5b1620ed4aae793fb951656c1945976",
      "signature": {
        "s": "0x01673268187c9581aff7d98b9ce254d431bff173ea0eae48d5e562c851f63c2a",
        "r": "0x34c08bc133b648a4392c25a4d7d893ad7dfdf3fa019ee574edc9c964ba260d81",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "30234",
    "total": "30234"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30234",
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
            "amount": "547124"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "30"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzM1OTg1Ny03MWEzLTU0MzAtOWRhYS0yOTg0YjdlMjI5Y2YifQ==",
    "nonce": 509,
    "balances": {
      "current": "10000001536792296",
      "previous": "10000001536822560"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb78e81e02b285cb0895a000c94d8a4ab1ff8484",
    "nonce": 20,
    "balances": {
      "current": "30234",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:29.761Z",
  "updated": "2020-05-22T08:02:29.837Z",
  "id": "5ec78715e5756b00111b801b"
}
```
* *stageAmount*: `30234`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000761a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000761a000000000000000000000000000000000000000000000000000000000000761a74314f8a8d3d05e36ebf637e465f7e64bfaaf55293a6e83d27ce69de1816ef9a1abe2b39225aad75fa743a2faee3aee41d07a4eb99309df842c20dec614bbaab097418d244af426a55a3a115543a55d6a08c59569efa6f6b653ca005db7e68b9000000000000000000000000000000000000000000000000000000000000001bb229ef5e0de51947509c5946f9691c10d5b1620ed4aae793fb951656c194597634c08bc133b648a4392c25a4d7d893ad7dfdf3fa019ee574edc9c964ba260d8101673268187c9581aff7d98b9ce254d431bff173ea0eae48d5e562c851f63c2a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c6000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb5a96e8000000000000000000000000000000000000000000000000002386f2cb5b0d2000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008593400000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e7a4d314f5467314e7930334d57457a4c5455304d7a41744f575268595330794f546730596a646c4d6a49355932596966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000bb78e81e02b285cb0895a000c94d8a4ab1ff8484000000000000000000000000000000000000000000000000000000000000761a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x74314f8a8d3d05e36ebf637e465f7e64bfaaf55293a6e83d27ce69de1816ef9a",
      "signature": {
        "s": "0x097418d244af426a55a3a115543a55d6a08c59569efa6f6b653ca005db7e68b9",
        "r": "0x1abe2b39225aad75fa743a2faee3aee41d07a4eb99309df842c20dec614bbaab",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb229ef5e0de51947509c5946f9691c10d5b1620ed4aae793fb951656c1945976",
      "signature": {
        "s": "0x01673268187c9581aff7d98b9ce254d431bff173ea0eae48d5e562c851f63c2a",
        "r": "0x34c08bc133b648a4392c25a4d7d893ad7dfdf3fa019ee574edc9c964ba260d81",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "30234",
    "total": "30234"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "30234",
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
            "amount": "547124"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "30"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzNzM1OTg1Ny03MWEzLTU0MzAtOWRhYS0yOTg0YjdlMjI5Y2YifQ==",
    "nonce": 509,
    "balances": {
      "current": "10000001536792296",
      "previous": "10000001536822560"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbb78e81e02b285cb0895a000c94d8a4ab1ff8484",
    "nonce": 20,
    "balances": {
      "current": "30234",
      "previous": "0"
    }
  },
  "blockNumber": "10114502",
  "created": "2020-05-22T08:02:29.761Z",
  "updated": "2020-05-22T08:02:29.837Z",
  "id": "5ec78715e5756b00111b801b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000761a0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `30234`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``