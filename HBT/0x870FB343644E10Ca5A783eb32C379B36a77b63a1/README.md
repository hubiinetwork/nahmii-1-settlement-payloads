# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x870FB343644E10Ca5A783eb32C379B36a77b63a1`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000004e572b5a900000000000000000000000000000000000000000000000000000004e572b5a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004e572b5a900000000000000000000000000000000000000000000000000000004e572b5a977b1218cf325438d42294ee0a3e51aa45d91c03b2ac9773c44ef8c6cc11882ff80bb2719f2972ec4d32d92d711d82764c901042c690f880216f62c454e587a7f070ac22cd748d6713f95541c740bbcba298df53046ae31a542d6cf1035b13024000000000000000000000000000000000000000000000000000000000000001bcf8be6c5cae2043dc3a089028c1c2441775a9df2a3b4de036fe37e0848bc688df9d5d7594219c114801243bd06e7ea001e006311523273910d4361af1f15ee194df71d52ac88ed5de9b6ca856bcdf8e50b535b11d4d58c8e515d3a61a0f22d18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1427b6314bac000000000000000000000000000000000000000000000000002e142c9ce4e34e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000140e1f9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b18dbfb1a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a574a684e545a69595331684d7a41354c5455354f5751744f4468694f4330304d3251324e4749794d32517a4d7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000870fb343644e10ca5a783eb32c379b36a77b63a100000000000000000000000000000000000000000000000000000004e572b5a9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77b1218cf325438d42294ee0a3e51aa45d91c03b2ac9773c44ef8c6cc11882ff",
      "signature": {
        "s": "0x070ac22cd748d6713f95541c740bbcba298df53046ae31a542d6cf1035b13024",
        "r": "0x80bb2719f2972ec4d32d92d711d82764c901042c690f880216f62c454e587a7f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcf8be6c5cae2043dc3a089028c1c2441775a9df2a3b4de036fe37e0848bc688d",
      "signature": {
        "s": "0x4df71d52ac88ed5de9b6ca856bcdf8e50b535b11d4d58c8e515d3a61a0f22d18",
        "r": "0xf9d5d7594219c114801243bd06e7ea001e006311523273910d4361af1f15ee19",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21029369257",
    "total": "21029369257"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21029369257",
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
            "amount": "47661710106"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "21029369"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZWJhNTZiYS1hMzA5LTU5OWQtODhiOC00M2Q2NGIyM2QzMzIifQ==",
    "nonce": 7128,
    "balances": {
      "current": "12970009721654188",
      "previous": "12970030772052814"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x870fb343644e10ca5a783eb32c379b36a77b63a1",
    "nonce": 22,
    "balances": {
      "current": "21029369257",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:25.185Z",
  "updated": "2020-05-22T08:54:25.259Z",
  "id": "5ec79341e5756b00111b8882"
}
```
* *stageAmount*: `21029369257`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000004e572b5a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000004e572b5a900000000000000000000000000000000000000000000000000000004e572b5a977b1218cf325438d42294ee0a3e51aa45d91c03b2ac9773c44ef8c6cc11882ff80bb2719f2972ec4d32d92d711d82764c901042c690f880216f62c454e587a7f070ac22cd748d6713f95541c740bbcba298df53046ae31a542d6cf1035b13024000000000000000000000000000000000000000000000000000000000000001bcf8be6c5cae2043dc3a089028c1c2441775a9df2a3b4de036fe37e0848bc688df9d5d7594219c114801243bd06e7ea001e006311523273910d4361af1f15ee194df71d52ac88ed5de9b6ca856bcdf8e50b535b11d4d58c8e515d3a61a0f22d18000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1427b6314bac000000000000000000000000000000000000000000000000002e142c9ce4e34e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000140e1f9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b18dbfb1a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a574a684e545a69595331684d7a41354c5455354f5751744f4468694f4330304d3251324e4749794d32517a4d7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000870fb343644e10ca5a783eb32c379b36a77b63a100000000000000000000000000000000000000000000000000000004e572b5a9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x77b1218cf325438d42294ee0a3e51aa45d91c03b2ac9773c44ef8c6cc11882ff",
      "signature": {
        "s": "0x070ac22cd748d6713f95541c740bbcba298df53046ae31a542d6cf1035b13024",
        "r": "0x80bb2719f2972ec4d32d92d711d82764c901042c690f880216f62c454e587a7f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xcf8be6c5cae2043dc3a089028c1c2441775a9df2a3b4de036fe37e0848bc688d",
      "signature": {
        "s": "0x4df71d52ac88ed5de9b6ca856bcdf8e50b535b11d4d58c8e515d3a61a0f22d18",
        "r": "0xf9d5d7594219c114801243bd06e7ea001e006311523273910d4361af1f15ee19",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21029369257",
    "total": "21029369257"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21029369257",
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
            "amount": "47661710106"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "21029369"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZWJhNTZiYS1hMzA5LTU5OWQtODhiOC00M2Q2NGIyM2QzMzIifQ==",
    "nonce": 7128,
    "balances": {
      "current": "12970009721654188",
      "previous": "12970030772052814"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x870fb343644e10ca5a783eb32c379b36a77b63a1",
    "nonce": 22,
    "balances": {
      "current": "21029369257",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:25.185Z",
  "updated": "2020-05-22T08:54:25.259Z",
  "id": "5ec79341e5756b00111b8882"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000004e572b5a9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `21029369257`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`