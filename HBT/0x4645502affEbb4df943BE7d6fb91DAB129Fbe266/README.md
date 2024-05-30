# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4645502affEbb4df943BE7d6fb91DAB129Fbe266`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000052c764f70000000000000000000000000000000000000000000000000000000052c764f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c764f70000000000000000000000000000000000000000000000000000000052c764f70461a5ba4e1b24001bc0c5f021bcb3490d16d8ad1d779db4de717652647a7a805aac015855c477ae113c1fef1968332c431ed185960c55d1bb93f6ef9fe4128c4eac688559f39a63c1f239e1f935436b3bb9001e5f452714ef5c1833a8743337000000000000000000000000000000000000000000000000000000000000001b49cbbb7208c961e1b5f58365b22a8c1b2073fa7e8f93591b17dd0cb35701efbdefd1c3584308523290eb38c931ec0c97e3419174af8d7122fdd5f4bf747f56db0d31e6eee74782f947b413375af737f767c8939668072bb1c525c056942a9d08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2cf5e7ab01000000000000000000000000000000000000000000000000002e1b2d48c440f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d392739000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a6b774d6d55355953316c4e6d557a4c5455304d5751745957566c5a533032596d4a695a4456694d6d4e6a4d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004645502affebb4df943be7d6fb91dab129fbe2660000000000000000000000000000000000000000000000000000000052c764f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0461a5ba4e1b24001bc0c5f021bcb3490d16d8ad1d779db4de717652647a7a80",
      "signature": {
        "s": "0x4eac688559f39a63c1f239e1f935436b3bb9001e5f452714ef5c1833a8743337",
        "r": "0x5aac015855c477ae113c1fef1968332c431ed185960c55d1bb93f6ef9fe4128c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x49cbbb7208c961e1b5f58365b22a8c1b2073fa7e8f93591b17dd0cb35701efbd",
      "signature": {
        "s": "0x0d31e6eee74782f947b413375af737f767c8939668072bb1c525c056942a9d08",
        "r": "0xefd1c3584308523290eb38c931ec0c97e3419174af8d7122fdd5f4bf747f56db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799223",
    "total": "1388799223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799223",
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
            "amount": "39950296889"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNzkwMmU5YS1lNmUzLTU0MWQtYWVlZS02YmJiZDViMmNjMDMifQ==",
    "nonce": 5947,
    "balances": {
      "current": "12977728846801665",
      "previous": "12977730236989687"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4645502affebb4df943be7d6fb91dab129fbe266",
    "nonce": 22,
    "balances": {
      "current": "1388799223",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:13.118Z",
  "updated": "2020-05-22T08:45:13.188Z",
  "id": "5ec79119005df800101bc9fd"
}
```
* *stageAmount*: `1388799223`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000052c764f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000052c764f70000000000000000000000000000000000000000000000000000000052c764f70461a5ba4e1b24001bc0c5f021bcb3490d16d8ad1d779db4de717652647a7a805aac015855c477ae113c1fef1968332c431ed185960c55d1bb93f6ef9fe4128c4eac688559f39a63c1f239e1f935436b3bb9001e5f452714ef5c1833a8743337000000000000000000000000000000000000000000000000000000000000001b49cbbb7208c961e1b5f58365b22a8c1b2073fa7e8f93591b17dd0cb35701efbdefd1c3584308523290eb38c931ec0c97e3419174af8d7122fdd5f4bf747f56db0d31e6eee74782f947b413375af737f767c8939668072bb1c525c056942a9d08000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56780000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000173b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b2cf5e7ab01000000000000000000000000000000000000000000000000002e1b2d48c440f700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000001530ff000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000094d392739000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a6b774d6d55355953316c4e6d557a4c5455304d5751745957566c5a533032596d4a695a4456694d6d4e6a4d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004645502affebb4df943be7d6fb91dab129fbe2660000000000000000000000000000000000000000000000000000000052c764f7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0461a5ba4e1b24001bc0c5f021bcb3490d16d8ad1d779db4de717652647a7a80",
      "signature": {
        "s": "0x4eac688559f39a63c1f239e1f935436b3bb9001e5f452714ef5c1833a8743337",
        "r": "0x5aac015855c477ae113c1fef1968332c431ed185960c55d1bb93f6ef9fe4128c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x49cbbb7208c961e1b5f58365b22a8c1b2073fa7e8f93591b17dd0cb35701efbd",
      "signature": {
        "s": "0x0d31e6eee74782f947b413375af737f767c8939668072bb1c525c056942a9d08",
        "r": "0xefd1c3584308523290eb38c931ec0c97e3419174af8d7122fdd5f4bf747f56db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1388799223",
    "total": "1388799223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1388799223",
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
            "amount": "39950296889"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1388799"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiNzkwMmU5YS1lNmUzLTU0MWQtYWVlZS02YmJiZDViMmNjMDMifQ==",
    "nonce": 5947,
    "balances": {
      "current": "12977728846801665",
      "previous": "12977730236989687"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4645502affebb4df943be7d6fb91dab129fbe266",
    "nonce": 22,
    "balances": {
      "current": "1388799223",
      "previous": "0"
    }
  },
  "blockNumber": "10114680",
  "created": "2020-05-22T08:45:13.118Z",
  "updated": "2020-05-22T08:45:13.188Z",
  "id": "5ec79119005df800101bc9fd"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000052c764f7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1388799223`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`