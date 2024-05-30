# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x23bB4e19767c51AFd9beBdd5Cb23cEd735b97618`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000032220000000000000000000000000000000000000000000000000000000000003222000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000322200000000000000000000000000000000000000000000000000000000000032228641810060138be79a5522431f8899f760acb847103c48a5988356ecd16d52f47a3c72f90466b810e709206c53e88def88518582f3a200f07b1a26c5360f20e715bc290a9d5f7f5fff674db7fbaaf5afeba6c3ff80289bb613e3bace9bf253c9000000000000000000000000000000000000000000000000000000000000001b42960da52a9bfa79e435d289cb74aff05690db4d2a75b5eabdc505e14dfb43df4b3abc6dcf8fa10e4758fabe48588a23dcef68b76e6f01847b2500f42267988d5b50c59f2d46adb8f94c601bd19686ae706451199c77d33c9ee228dedb97d3a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d4b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b7496a657fd000000000000000000000000000000000000000000000000002e0b7496a68a2b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d526eea09000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6a63354e32597a5979316c4d6d51314c54566a4e6d5574595455344d4331685a546b794f574d794f444d345a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000023bb4e19767c51afd9bebdd5cb23ced735b976180000000000000000000000000000000000000000000000000000000000003222000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8641810060138be79a5522431f8899f760acb847103c48a5988356ecd16d52f4",
      "signature": {
        "s": "0x15bc290a9d5f7f5fff674db7fbaaf5afeba6c3ff80289bb613e3bace9bf253c9",
        "r": "0x7a3c72f90466b810e709206c53e88def88518582f3a200f07b1a26c5360f20e7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42960da52a9bfa79e435d289cb74aff05690db4d2a75b5eabdc505e14dfb43df",
      "signature": {
        "s": "0x5b50c59f2d46adb8f94c601bd19686ae706451199c77d33c9ee228dedb97d3a2",
        "r": "0x4b3abc6dcf8fa10e4758fabe48588a23dcef68b76e6f01847b2500f42267988d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12834",
    "total": "12834"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12834",
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
            "amount": "57217575433"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMjc5N2YzYy1lMmQ1LTVjNmUtYTU4MC1hZTkyOWMyODM4ZjMifQ==",
    "nonce": 7499,
    "balances": {
      "current": "12960444300285949",
      "previous": "12960444300298795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x23bb4e19767c51afd9bebdd5cb23ced735b97618",
    "nonce": 5,
    "balances": {
      "current": "12834",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:14.765Z",
  "updated": "2020-05-22T08:57:14.831Z",
  "id": "5ec793eab0c6090011d5b29a"
}
```
* *stageAmount*: `12834`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000003222000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000322200000000000000000000000000000000000000000000000000000000000032228641810060138be79a5522431f8899f760acb847103c48a5988356ecd16d52f47a3c72f90466b810e709206c53e88def88518582f3a200f07b1a26c5360f20e715bc290a9d5f7f5fff674db7fbaaf5afeba6c3ff80289bb613e3bace9bf253c9000000000000000000000000000000000000000000000000000000000000001b42960da52a9bfa79e435d289cb74aff05690db4d2a75b5eabdc505e14dfb43df4b3abc6dcf8fa10e4758fabe48588a23dcef68b76e6f01847b2500f42267988d5b50c59f2d46adb8f94c601bd19686ae706451199c77d33c9ee228dedb97d3a2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d4b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b7496a657fd000000000000000000000000000000000000000000000000002e0b7496a68a2b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d526eea09000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d6a63354e32597a5979316c4d6d51314c54566a4e6d5574595455344d4331685a546b794f574d794f444d345a6a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000500000000000000000000000023bb4e19767c51afd9bebdd5cb23ced735b976180000000000000000000000000000000000000000000000000000000000003222000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8641810060138be79a5522431f8899f760acb847103c48a5988356ecd16d52f4",
      "signature": {
        "s": "0x15bc290a9d5f7f5fff674db7fbaaf5afeba6c3ff80289bb613e3bace9bf253c9",
        "r": "0x7a3c72f90466b810e709206c53e88def88518582f3a200f07b1a26c5360f20e7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x42960da52a9bfa79e435d289cb74aff05690db4d2a75b5eabdc505e14dfb43df",
      "signature": {
        "s": "0x5b50c59f2d46adb8f94c601bd19686ae706451199c77d33c9ee228dedb97d3a2",
        "r": "0x4b3abc6dcf8fa10e4758fabe48588a23dcef68b76e6f01847b2500f42267988d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12834",
    "total": "12834"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12834",
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
            "amount": "57217575433"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMjc5N2YzYy1lMmQ1LTVjNmUtYTU4MC1hZTkyOWMyODM4ZjMifQ==",
    "nonce": 7499,
    "balances": {
      "current": "12960444300285949",
      "previous": "12960444300298795"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x23bb4e19767c51afd9bebdd5cb23ced735b97618",
    "nonce": 5,
    "balances": {
      "current": "12834",
      "previous": "0"
    }
  },
  "blockNumber": "10114741",
  "created": "2020-05-22T08:57:14.765Z",
  "updated": "2020-05-22T08:57:14.831Z",
  "id": "5ec793eab0c6090011d5b29a"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000003222000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12834`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`