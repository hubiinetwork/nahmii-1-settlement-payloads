# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC53cd247F373a620943A10318e7a98Ef61F5e655`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000000000000000000000000000000000004ed5f92d8ea80d6dfab7a5bdb76f414bf68f470bb78f4982b656bb285e4993a9e4879aa2ea16473eef70cd1528f38872c5346b199030ae6db3944b7847a7c5c8031cd1a940e0cfc422d01d9a4878ce7295cddc5a5617387d609146f9eb9aa7be3d1cbc73000000000000000000000000000000000000000000000000000000000000001c1110be23197c5db365689c37e7241fce3a0e8673883139ec4ff4e35a8629646c88ffbd3164f803bf9e61515dad21d415d0ce7c171f8b74b50c8f184eeffcd4880cd0c3e6c10761f9e3ea6dc93e8c77882533411249552908bd3b3a4ef0685479000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0d21d07c52000000000000000000000000000000000000000000000000002e1a0d70baa41400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000996d56ef7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775932526a4d7a4d344e6930324d44637a4c5455304d7a6b74595441354d433031597a55314e4455305a6a45795a44556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c53cd247f373a620943a10318e7a98ef61f5e655000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8ea80d6dfab7a5bdb76f414bf68f470bb78f4982b656bb285e4993a9e4879aa2",
      "signature": {
        "s": "0x40e0cfc422d01d9a4878ce7295cddc5a5617387d609146f9eb9aa7be3d1cbc73",
        "r": "0xea16473eef70cd1528f38872c5346b199030ae6db3944b7847a7c5c8031cd1a9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1110be23197c5db365689c37e7241fce3a0e8673883139ec4ff4e35a8629646c",
      "signature": {
        "s": "0x0cd0c3e6c10761f9e3ea6dc93e8c77882533411249552908bd3b3a4ef0685479",
        "r": "0x88ffbd3164f803bf9e61515dad21d415d0ce7c171f8b74b50c8f184eeffcd488",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322645805",
    "total": "1322645805"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322645805",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "41185275639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322645"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwY2RjMzM4Ni02MDczLTU0MzktYTA5MC01YzU1NDU0ZjEyZDUifQ==",
    "nonce": 6325,
    "balances": {
      "current": "12976492632898642",
      "previous": "12976493956867092"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc53cd247f373a620943a10318e7a98ef61f5e655",
    "nonce": 22,
    "balances": {
      "current": "1322645805",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.863Z",
  "updated": "2020-05-22T08:48:12.937Z",
  "id": "5ec791cc005df800101bca7a"
}
```
* *stageAmount*: `1322645805`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000000000000000000000000000000000004ed5f92d8ea80d6dfab7a5bdb76f414bf68f470bb78f4982b656bb285e4993a9e4879aa2ea16473eef70cd1528f38872c5346b199030ae6db3944b7847a7c5c8031cd1a940e0cfc422d01d9a4878ce7295cddc5a5617387d609146f9eb9aa7be3d1cbc73000000000000000000000000000000000000000000000000000000000000001c1110be23197c5db365689c37e7241fce3a0e8673883139ec4ff4e35a8629646c88ffbd3164f803bf9e61515dad21d415d0ce7c171f8b74b50c8f184eeffcd4880cd0c3e6c10761f9e3ea6dc93e8c77882533411249552908bd3b3a4ef0685479000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568b000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000018b500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1a0d21d07c52000000000000000000000000000000000000000000000000002e1a0d70baa41400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e95000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000996d56ef7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949775932526a4d7a4d344e6930324d44637a4c5455304d7a6b74595441354d433031597a55314e4455305a6a45795a44556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c53cd247f373a620943a10318e7a98ef61f5e655000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8ea80d6dfab7a5bdb76f414bf68f470bb78f4982b656bb285e4993a9e4879aa2",
      "signature": {
        "s": "0x40e0cfc422d01d9a4878ce7295cddc5a5617387d609146f9eb9aa7be3d1cbc73",
        "r": "0xea16473eef70cd1528f38872c5346b199030ae6db3944b7847a7c5c8031cd1a9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1110be23197c5db365689c37e7241fce3a0e8673883139ec4ff4e35a8629646c",
      "signature": {
        "s": "0x0cd0c3e6c10761f9e3ea6dc93e8c77882533411249552908bd3b3a4ef0685479",
        "r": "0x88ffbd3164f803bf9e61515dad21d415d0ce7c171f8b74b50c8f184eeffcd488",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322645805",
    "total": "1322645805"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322645805",
  "currency": {
    "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
              "id": "0"
            },
            "amount": "41185275639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322645"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwY2RjMzM4Ni02MDczLTU0MzktYTA5MC01YzU1NDU0ZjEyZDUifQ==",
    "nonce": 6325,
    "balances": {
      "current": "12976492632898642",
      "previous": "12976493956867092"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc53cd247f373a620943a10318e7a98ef61f5e655",
    "nonce": 22,
    "balances": {
      "current": "1322645805",
      "previous": "0"
    }
  },
  "blockNumber": "10114699",
  "created": "2020-05-22T08:48:12.863Z",
  "updated": "2020-05-22T08:48:12.937Z",
  "id": "5ec791cc005df800101bca7a"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed5f92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322645805`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`