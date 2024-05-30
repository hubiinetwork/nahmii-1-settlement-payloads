# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6F10475F694D59B31146b37a03dF271Ed6030C3F`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000335c000000000000000000000000000000000000000000000000000000000000335c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000335c000000000000000000000000000000000000000000000000000000000000335c95e02fb8c433a2aef26c29e17ee7f8b84c1346b223ebe1641f98be66cc25102acae660bb93f57a62c82c84a64af4f47bc27fd284fff2ce9cf81dcdba2de00bbe364c58bc5af4e6a247ea3ab7cac6bbdfe7ed66e71061de8a8a1225876d91325a000000000000000000000000000000000000000000000000000000000000001b2934e4bef2ed2619fab92eaab9bda03849dbeb2125b33ffd2695818754013ba0d84ce1d4f4acfd6ee42c3c5a177eaca71b1ac998638ae7f143c6179204072be15856205d155da7a5604911befa0b291c133e48fe37e1630e0a27eaa174daa815000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000025d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb14b4e2000000000000000000000000000000000000000000000000002386f2cb14e84b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ae900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d575a6d5a54466a4e5330354d4459344c5455304e7a41744f54566b4f4330774d6a55305a4467784e5442694e44596966513d3d00000000000000000000000000000000000000000000000000000000000000120000000000000000000000006f10475f694d59b31146b37a03df271ed6030c3f000000000000000000000000000000000000000000000000000000000000335c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95e02fb8c433a2aef26c29e17ee7f8b84c1346b223ebe1641f98be66cc25102a",
      "signature": {
        "s": "0x364c58bc5af4e6a247ea3ab7cac6bbdfe7ed66e71061de8a8a1225876d91325a",
        "r": "0xcae660bb93f57a62c82c84a64af4f47bc27fd284fff2ce9cf81dcdba2de00bbe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2934e4bef2ed2619fab92eaab9bda03849dbeb2125b33ffd2695818754013ba0",
      "signature": {
        "s": "0x5856205d155da7a5604911befa0b291c133e48fe37e1630e0a27eaa174daa815",
        "r": "0xd84ce1d4f4acfd6ee42c3c5a177eaca71b1ac998638ae7f143c6179204072be1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13148",
    "total": "13148"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13148",
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
            "amount": "551657"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMWZmZTFjNS05MDY4LTU0NzAtOTVkOC0wMjU0ZDgxNTBiNDYifQ==",
    "nonce": 605,
    "balances": {
      "current": "10000001532212450",
      "previous": "10000001532225611"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f10475f694d59b31146b37a03df271ed6030c3f",
    "nonce": 18,
    "balances": {
      "current": "13148",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:16.287Z",
  "updated": "2020-05-22T08:03:16.354Z",
  "id": "5ec78744e5756b00111b8037"
}
```
* *stageAmount*: `13148`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000335c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000335c000000000000000000000000000000000000000000000000000000000000335c95e02fb8c433a2aef26c29e17ee7f8b84c1346b223ebe1641f98be66cc25102acae660bb93f57a62c82c84a64af4f47bc27fd284fff2ce9cf81dcdba2de00bbe364c58bc5af4e6a247ea3ab7cac6bbdfe7ed66e71061de8a8a1225876d91325a000000000000000000000000000000000000000000000000000000000000001b2934e4bef2ed2619fab92eaab9bda03849dbeb2125b33ffd2695818754013ba0d84ce1d4f4acfd6ee42c3c5a177eaca71b1ac998638ae7f143c6179204072be15856205d155da7a5604911befa0b291c133e48fe37e1630e0a27eaa174daa815000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000025d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb14b4e2000000000000000000000000000000000000000000000000002386f2cb14e84b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086ae900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d575a6d5a54466a4e5330354d4459344c5455304e7a41744f54566b4f4330774d6a55305a4467784e5442694e44596966513d3d00000000000000000000000000000000000000000000000000000000000000120000000000000000000000006f10475f694d59b31146b37a03df271ed6030c3f000000000000000000000000000000000000000000000000000000000000335c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x95e02fb8c433a2aef26c29e17ee7f8b84c1346b223ebe1641f98be66cc25102a",
      "signature": {
        "s": "0x364c58bc5af4e6a247ea3ab7cac6bbdfe7ed66e71061de8a8a1225876d91325a",
        "r": "0xcae660bb93f57a62c82c84a64af4f47bc27fd284fff2ce9cf81dcdba2de00bbe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x2934e4bef2ed2619fab92eaab9bda03849dbeb2125b33ffd2695818754013ba0",
      "signature": {
        "s": "0x5856205d155da7a5604911befa0b291c133e48fe37e1630e0a27eaa174daa815",
        "r": "0xd84ce1d4f4acfd6ee42c3c5a177eaca71b1ac998638ae7f143c6179204072be1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13148",
    "total": "13148"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13148",
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
            "amount": "551657"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "13"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMWZmZTFjNS05MDY4LTU0NzAtOTVkOC0wMjU0ZDgxNTBiNDYifQ==",
    "nonce": 605,
    "balances": {
      "current": "10000001532212450",
      "previous": "10000001532225611"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6f10475f694d59b31146b37a03df271ed6030c3f",
    "nonce": 18,
    "balances": {
      "current": "13148",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:16.287Z",
  "updated": "2020-05-22T08:03:16.354Z",
  "id": "5ec78744e5756b00111b8037"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000335c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13148`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``