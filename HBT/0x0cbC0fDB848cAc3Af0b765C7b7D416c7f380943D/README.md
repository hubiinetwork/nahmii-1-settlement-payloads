# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0cbC0fDB848cAc3Af0b765C7b7D416c7f380943D`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000031aace580000000000000000000000000000000000000000000000000000000031aace58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000031aace580000000000000000000000000000000000000000000000000000000031aace584272be63c63a9d4f0c082eaa92054148657a4da37d09b54d516cfd69083a6ae6d9b001bfc612158e6405abcccc4a2a60b04cb8aa12baf6d443a83696a434db8802b1ef0d74abc32a4b1416c2f60d1de57ef1c959c44553d1f34d3c67aea15bfd000000000000000000000000000000000000000000000000000000000000001b7bd209f61d51928423357853014dcd52ef21dd07ded961c37d919d814379ee31529b94f002c17aa9f8e17acf9f73792506c9c8f40afad6c94aa75f073a05d71d1f9735c5c9b37636e170f81245eefd997b6c149f8f542de481ef67a0a0e8cff3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1cb1bbe5f5000000000000000000000000000000000000000000000000002e1b1ce3736b4a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000cb6fd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000951621d97000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a566859575a6c5a533033595449304c5455794d4751744f574d345a4330774e574e694d4759315a445a6b4d54636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000cbc0fdb848cac3af0b765c7b7d416c7f380943d0000000000000000000000000000000000000000000000000000000031aace58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4272be63c63a9d4f0c082eaa92054148657a4da37d09b54d516cfd69083a6ae6",
      "signature": {
        "s": "0x02b1ef0d74abc32a4b1416c2f60d1de57ef1c959c44553d1f34d3c67aea15bfd",
        "r": "0xd9b001bfc612158e6405abcccc4a2a60b04cb8aa12baf6d443a83696a434db88",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7bd209f61d51928423357853014dcd52ef21dd07ded961c37d919d814379ee31",
      "signature": {
        "s": "0x1f9735c5c9b37636e170f81245eefd997b6c149f8f542de481ef67a0a0e8cff3",
        "r": "0x529b94f002c17aa9f8e17acf9f73792506c9c8f40afad6c94aa75f073a05d71d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "833277528",
    "total": "833277528"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "833277528",
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
            "amount": "40020090263"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "833277"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzVhYWZlZS03YTI0LTUyMGQtOWM4ZC0wNWNiMGY1ZDZkMTcifQ==",
    "nonce": 6008,
    "balances": {
      "current": "12977658983605749",
      "previous": "12977659817716554"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0cbc0fdb848cac3af0b765c7b7d416c7f380943d",
    "nonce": 22,
    "balances": {
      "current": "833277528",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:40.629Z",
  "updated": "2020-05-22T08:45:40.761Z",
  "id": "5ec79134b0c6090011d5b092"
}
```
* *stageAmount*: `833277528`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000031aace58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000031aace580000000000000000000000000000000000000000000000000000000031aace584272be63c63a9d4f0c082eaa92054148657a4da37d09b54d516cfd69083a6ae6d9b001bfc612158e6405abcccc4a2a60b04cb8aa12baf6d443a83696a434db8802b1ef0d74abc32a4b1416c2f60d1de57ef1c959c44553d1f34d3c67aea15bfd000000000000000000000000000000000000000000000000000000000000001b7bd209f61d51928423357853014dcd52ef21dd07ded961c37d919d814379ee31529b94f002c17aa9f8e17acf9f73792506c9c8f40afad6c94aa75f073a05d71d1f9735c5c9b37636e170f81245eefd997b6c149f8f542de481ef67a0a0e8cff3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56790000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000177800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1cb1bbe5f5000000000000000000000000000000000000000000000000002e1b1ce3736b4a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000cb6fd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000951621d97000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694978597a566859575a6c5a533033595449304c5455794d4751744f574d345a4330774e574e694d4759315a445a6b4d54636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000000cbc0fdb848cac3af0b765c7b7d416c7f380943d0000000000000000000000000000000000000000000000000000000031aace58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4272be63c63a9d4f0c082eaa92054148657a4da37d09b54d516cfd69083a6ae6",
      "signature": {
        "s": "0x02b1ef0d74abc32a4b1416c2f60d1de57ef1c959c44553d1f34d3c67aea15bfd",
        "r": "0xd9b001bfc612158e6405abcccc4a2a60b04cb8aa12baf6d443a83696a434db88",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7bd209f61d51928423357853014dcd52ef21dd07ded961c37d919d814379ee31",
      "signature": {
        "s": "0x1f9735c5c9b37636e170f81245eefd997b6c149f8f542de481ef67a0a0e8cff3",
        "r": "0x529b94f002c17aa9f8e17acf9f73792506c9c8f40afad6c94aa75f073a05d71d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "833277528",
    "total": "833277528"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "833277528",
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
            "amount": "40020090263"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "833277"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxYzVhYWZlZS03YTI0LTUyMGQtOWM4ZC0wNWNiMGY1ZDZkMTcifQ==",
    "nonce": 6008,
    "balances": {
      "current": "12977658983605749",
      "previous": "12977659817716554"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0cbc0fdb848cac3af0b765c7b7d416c7f380943d",
    "nonce": 22,
    "balances": {
      "current": "833277528",
      "previous": "0"
    }
  },
  "blockNumber": "10114681",
  "created": "2020-05-22T08:45:40.629Z",
  "updated": "2020-05-22T08:45:40.761Z",
  "id": "5ec79134b0c6090011d5b092"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000031aace58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `833277528`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`