# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC729fC3F4Fa351349DB74f27232F2029A13aD7A7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000021d9bf400000000000000000000000000000000000000000000000000000000021d9bf4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000021d9bf400000000000000000000000000000000000000000000000000000000021d9bf4a36c5c2b4b6b2956f1bfea554b9db2d39e06e57cd26ce76887582ab332525b8d60832babfec75d5b8619552d5ff9249d0dd4ed886fbb6f2d199c313414404bbb52106769cc4de17bfe0f376debab220ade44e901bc4290c9a626f81e958af8b1000000000000000000000000000000000000000000000000000000000000001b26fbb7305b8ca8409d4c5ddd1ea678e0ae6feca288a063e4663a7f9598fc395dee921bfb11ffa118136b1f5bef05e31ffee0b1b06bebc9af70be04c850b66a6c37b76ddac918d68d799cc708a48592c571c7f9d1ea46bedaf3988219d494cd0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001de700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b13b0d48ed8000000000000000000000000000000000000000000000000002e0b13b2f2b57200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000008aa6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b36dbe3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d6a4532595745335a533033595751304c5455354f5451745957597a4d7930304e32557a4e6d51344e7a67345a57516966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000c729fc3f4fa351349db74f27232f2029a13ad7a700000000000000000000000000000000000000000000000000000000021d9bf4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa36c5c2b4b6b2956f1bfea554b9db2d39e06e57cd26ce76887582ab332525b8d",
      "signature": {
        "s": "0x52106769cc4de17bfe0f376debab220ade44e901bc4290c9a626f81e958af8b1",
        "r": "0x60832babfec75d5b8619552d5ff9249d0dd4ed886fbb6f2d199c313414404bbb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x26fbb7305b8ca8409d4c5ddd1ea678e0ae6feca288a063e4663a7f9598fc395d",
      "signature": {
        "s": "0x37b76ddac918d68d799cc708a48592c571c7f9d1ea46bedaf3988219d494cd0b",
        "r": "0xee921bfb11ffa118136b1f5bef05e31ffee0b1b06bebc9af70be04c850b66a6c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "35494900",
    "total": "35494900"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35494900",
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
            "amount": "57633332195"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35494"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMjE2YWE3ZS03YWQ0LTU5OTQtYWYzMy00N2UzNmQ4Nzg4ZWQifQ==",
    "nonce": 7655,
    "balances": {
      "current": "12960028127694552",
      "previous": "12960028163224946"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc729fc3f4fa351349db74f27232f2029a13ad7a7",
    "nonce": 15,
    "balances": {
      "current": "35494900",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:26.683Z",
  "updated": "2020-05-22T08:58:26.747Z",
  "id": "5ec79432005df800101bcc3d"
}
```
* *stageAmount*: `35494900`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000021d9bf4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000021d9bf400000000000000000000000000000000000000000000000000000000021d9bf4a36c5c2b4b6b2956f1bfea554b9db2d39e06e57cd26ce76887582ab332525b8d60832babfec75d5b8619552d5ff9249d0dd4ed886fbb6f2d199c313414404bbb52106769cc4de17bfe0f376debab220ade44e901bc4290c9a626f81e958af8b1000000000000000000000000000000000000000000000000000000000000001b26fbb7305b8ca8409d4c5ddd1ea678e0ae6feca288a063e4663a7f9598fc395dee921bfb11ffa118136b1f5bef05e31ffee0b1b06bebc9af70be04c850b66a6c37b76ddac918d68d799cc708a48592c571c7f9d1ea46bedaf3988219d494cd0b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001de700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b13b0d48ed8000000000000000000000000000000000000000000000000002e0b13b2f2b57200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000008aa6000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b36dbe3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d6a4532595745335a533033595751304c5455354f5451745957597a4d7930304e32557a4e6d51344e7a67345a57516966513d3d000000000000000000000000000000000000000000000000000000000000000f000000000000000000000000c729fc3f4fa351349db74f27232f2029a13ad7a700000000000000000000000000000000000000000000000000000000021d9bf4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa36c5c2b4b6b2956f1bfea554b9db2d39e06e57cd26ce76887582ab332525b8d",
      "signature": {
        "s": "0x52106769cc4de17bfe0f376debab220ade44e901bc4290c9a626f81e958af8b1",
        "r": "0x60832babfec75d5b8619552d5ff9249d0dd4ed886fbb6f2d199c313414404bbb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x26fbb7305b8ca8409d4c5ddd1ea678e0ae6feca288a063e4663a7f9598fc395d",
      "signature": {
        "s": "0x37b76ddac918d68d799cc708a48592c571c7f9d1ea46bedaf3988219d494cd0b",
        "r": "0xee921bfb11ffa118136b1f5bef05e31ffee0b1b06bebc9af70be04c850b66a6c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "35494900",
    "total": "35494900"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "35494900",
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
            "amount": "57633332195"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "35494"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMjE2YWE3ZS03YWQ0LTU5OTQtYWYzMy00N2UzNmQ4Nzg4ZWQifQ==",
    "nonce": 7655,
    "balances": {
      "current": "12960028127694552",
      "previous": "12960028163224946"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc729fc3f4fa351349db74f27232f2029a13ad7a7",
    "nonce": 15,
    "balances": {
      "current": "35494900",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:26.683Z",
  "updated": "2020-05-22T08:58:26.747Z",
  "id": "5ec79432005df800101bcc3d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000021d9bf4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `35494900`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`