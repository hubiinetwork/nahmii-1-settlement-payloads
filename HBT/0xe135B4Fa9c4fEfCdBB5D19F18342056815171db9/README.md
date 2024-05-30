# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe135B4Fa9c4fEfCdBB5D19F18342056815171db9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000a174700000000000000000000000000000000000000000000000000000000000a1747000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000a174700000000000000000000000000000000000000000000000000000000000a174793fd026a543c2cd29c9941b100be0576af85f5ca3cc4ea343f2a935fe9719a966961b0f250d835d1162157a6fc166bbb6df73242e850f0a9fe43517caecdc35c55eac837dae0f204aef77e518afc7597760c7df8e65e20573aa98aa138750e55000000000000000000000000000000000000000000000000000000000000001c9c4b604a5b1555c28bf592781ed4b93f4871d97d2dc00c4d0208bd04bb8416a149e876bcdc4cc2cab624cced1fd8b09cb5aa3c6984441c4a71294f0562f3e2c81373e4a89dd2cc86b5eb5f8a99506369b01cb6d26f2715711bf6e050ad303b9a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18084010fc8f000000000000000000000000000000000000000000000000002e1808401b166b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000295000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b05f5b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a5a695a4455314e5331695a444d304c54566a4e7a6b7459545932596930334d6a41334d32517a4e6d4a694e32456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e135b4fa9c4fefcdbb5d19f18342056815171db900000000000000000000000000000000000000000000000000000000000a1747000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x93fd026a543c2cd29c9941b100be0576af85f5ca3cc4ea343f2a935fe9719a96",
      "signature": {
        "s": "0x55eac837dae0f204aef77e518afc7597760c7df8e65e20573aa98aa138750e55",
        "r": "0x6961b0f250d835d1162157a6fc166bbb6df73242e850f0a9fe43517caecdc35c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9c4b604a5b1555c28bf592781ed4b93f4871d97d2dc00c4d0208bd04bb8416a1",
      "signature": {
        "s": "0x1373e4a89dd2cc86b5eb5f8a99506369b01cb6d26f2715711bf6e050ad303b9a",
        "r": "0x49e876bcdc4cc2cab624cced1fd8b09cb5aa3c6984441c4a71294f0562f3e2c8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "661319",
    "total": "661319"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "661319",
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
            "amount": "43403048370"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "661"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNjZiZDU1NS1iZDM0LTVjNzktYTY2Yi03MjA3M2QzNmJiN2EifQ==",
    "nonce": 6458,
    "balances": {
      "current": "12974272642350223",
      "previous": "12974272643012203"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe135b4fa9c4fefcdbb5d19f18342056815171db9",
    "nonce": 22,
    "balances": {
      "current": "661319",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:17.433Z",
  "updated": "2020-05-22T08:49:17.510Z",
  "id": "5ec7920de5756b00111b87b4"
}
```
* *stageAmount*: `661319`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000a1747000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000a174700000000000000000000000000000000000000000000000000000000000a174793fd026a543c2cd29c9941b100be0576af85f5ca3cc4ea343f2a935fe9719a966961b0f250d835d1162157a6fc166bbb6df73242e850f0a9fe43517caecdc35c55eac837dae0f204aef77e518afc7597760c7df8e65e20573aa98aa138750e55000000000000000000000000000000000000000000000000000000000000001c9c4b604a5b1555c28bf592781ed4b93f4871d97d2dc00c4d0208bd04bb8416a149e876bcdc4cc2cab624cced1fd8b09cb5aa3c6984441c4a71294f0562f3e2c81373e4a89dd2cc86b5eb5f8a99506369b01cb6d26f2715711bf6e050ad303b9a000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18084010fc8f000000000000000000000000000000000000000000000000002e1808401b166b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000295000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1b05f5b2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a5a695a4455314e5331695a444d304c54566a4e7a6b7459545932596930334d6a41334d32517a4e6d4a694e32456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e135b4fa9c4fefcdbb5d19f18342056815171db900000000000000000000000000000000000000000000000000000000000a1747000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x93fd026a543c2cd29c9941b100be0576af85f5ca3cc4ea343f2a935fe9719a96",
      "signature": {
        "s": "0x55eac837dae0f204aef77e518afc7597760c7df8e65e20573aa98aa138750e55",
        "r": "0x6961b0f250d835d1162157a6fc166bbb6df73242e850f0a9fe43517caecdc35c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9c4b604a5b1555c28bf592781ed4b93f4871d97d2dc00c4d0208bd04bb8416a1",
      "signature": {
        "s": "0x1373e4a89dd2cc86b5eb5f8a99506369b01cb6d26f2715711bf6e050ad303b9a",
        "r": "0x49e876bcdc4cc2cab624cced1fd8b09cb5aa3c6984441c4a71294f0562f3e2c8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "661319",
    "total": "661319"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "661319",
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
            "amount": "43403048370"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "661"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNjZiZDU1NS1iZDM0LTVjNzktYTY2Yi03MjA3M2QzNmJiN2EifQ==",
    "nonce": 6458,
    "balances": {
      "current": "12974272642350223",
      "previous": "12974272643012203"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe135b4fa9c4fefcdbb5d19f18342056815171db9",
    "nonce": 22,
    "balances": {
      "current": "661319",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:17.433Z",
  "updated": "2020-05-22T08:49:17.510Z",
  "id": "5ec7920de5756b00111b87b4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000a1747000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `661319`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`