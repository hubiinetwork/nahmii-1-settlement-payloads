# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x890c5a41102E9F70fd28F05Bb520F15EdA24AF84`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000f010000000000000000000000000000000000000000000000000000000000000f0100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000f010000000000000000000000000000000000000000000000000000000000000f010a785d9b688e0f26d80b3d30a8239d2f238a8fdb96501c6d317d0c45451894933c63de8af400641f7b7a7596bda6bbc60d54f562172f3a405ed4fd24a30706b1f7161de1d5c8c332cca848aa495a09d8bd6b7646f1bfa88639e2cb4343ffef873000000000000000000000000000000000000000000000000000000000000001cbb9e7eeba861867e17481a6e55e77640784333001c4e6e476fe907c59340ff38fd548600d044538c72dd7627fa0fab0dfc399c28b8f2834ce1b18fab7f7361cc2c16a683d543ef9dd0327d439ed3a52b9a369bc7f17a273d2639f1c6ac1f8e68000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c590a782000000000000000000000000000000000000000000000000002386f2c59197cf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d2c300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935597a45304f4467354d79316c4d4463334c54566c5a44557459544934597930324f54686a5a444d304e7a51784e44636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000890c5a41102e9f70fd28f05bb520f15eda24af84000000000000000000000000000000000000000000000000000000000000f010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa785d9b688e0f26d80b3d30a8239d2f238a8fdb96501c6d317d0c45451894933",
      "signature": {
        "s": "0x7161de1d5c8c332cca848aa495a09d8bd6b7646f1bfa88639e2cb4343ffef873",
        "r": "0xc63de8af400641f7b7a7596bda6bbc60d54f562172f3a405ed4fd24a30706b1f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbb9e7eeba861867e17481a6e55e77640784333001c4e6e476fe907c59340ff38",
      "signature": {
        "s": "0x2c16a683d543ef9dd0327d439ed3a52b9a369bc7f17a273d2639f1c6ac1f8e68",
        "r": "0xfd548600d044538c72dd7627fa0fab0dfc399c28b8f2834ce1b18fab7f7361cc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "61456",
    "total": "61456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61456",
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
            "amount": "643779"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "61"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YzE0ODg5My1lMDc3LTVlZDUtYTI4Yy02OThjZDM0NzQxNDcifQ==",
    "nonce": 1727,
    "balances": {
      "current": "10000001439672194",
      "previous": "10000001439733711"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x890c5a41102e9f70fd28f05bb520f15eda24af84",
    "nonce": 20,
    "balances": {
      "current": "61456",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:39.013Z",
  "updated": "2020-05-22T08:11:40.096Z",
  "id": "5ec7893be5756b00111b819d"
}
```
* *stageAmount*: `61456`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000f0100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000f010000000000000000000000000000000000000000000000000000000000000f010a785d9b688e0f26d80b3d30a8239d2f238a8fdb96501c6d317d0c45451894933c63de8af400641f7b7a7596bda6bbc60d54f562172f3a405ed4fd24a30706b1f7161de1d5c8c332cca848aa495a09d8bd6b7646f1bfa88639e2cb4343ffef873000000000000000000000000000000000000000000000000000000000000001cbb9e7eeba861867e17481a6e55e77640784333001c4e6e476fe907c59340ff38fd548600d044538c72dd7627fa0fab0dfc399c28b8f2834ce1b18fab7f7361cc2c16a683d543ef9dd0327d439ed3a52b9a369bc7f17a273d2639f1c6ac1f8e68000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006bf00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c590a782000000000000000000000000000000000000000000000000002386f2c59197cf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000003d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d2c300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935597a45304f4467354d79316c4d4463334c54566c5a44557459544934597930324f54686a5a444d304e7a51784e44636966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000890c5a41102e9f70fd28f05bb520f15eda24af84000000000000000000000000000000000000000000000000000000000000f010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa785d9b688e0f26d80b3d30a8239d2f238a8fdb96501c6d317d0c45451894933",
      "signature": {
        "s": "0x7161de1d5c8c332cca848aa495a09d8bd6b7646f1bfa88639e2cb4343ffef873",
        "r": "0xc63de8af400641f7b7a7596bda6bbc60d54f562172f3a405ed4fd24a30706b1f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbb9e7eeba861867e17481a6e55e77640784333001c4e6e476fe907c59340ff38",
      "signature": {
        "s": "0x2c16a683d543ef9dd0327d439ed3a52b9a369bc7f17a273d2639f1c6ac1f8e68",
        "r": "0xfd548600d044538c72dd7627fa0fab0dfc399c28b8f2834ce1b18fab7f7361cc",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "61456",
    "total": "61456"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "61456",
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
            "amount": "643779"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "61"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5YzE0ODg5My1lMDc3LTVlZDUtYTI4Yy02OThjZDM0NzQxNDcifQ==",
    "nonce": 1727,
    "balances": {
      "current": "10000001439672194",
      "previous": "10000001439733711"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x890c5a41102e9f70fd28f05bb520f15eda24af84",
    "nonce": 20,
    "balances": {
      "current": "61456",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:39.013Z",
  "updated": "2020-05-22T08:11:40.096Z",
  "id": "5ec7893be5756b00111b819d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000f0100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `61456`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``