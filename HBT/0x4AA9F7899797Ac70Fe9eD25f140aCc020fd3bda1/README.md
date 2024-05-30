# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4AA9F7899797Ac70Fe9eD25f140aCc020fd3bda1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000008529ff80000000000000000000000000000000000000000000000000000000008529ff8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008529ff80000000000000000000000000000000000000000000000000000000008529ff83f18d9f445cf2ab84b3c145b1619255290d826eeceef174d20eb36d9163c2bd250d97246e91df17697e4be098d88f920432e1646296684f05ad7c8bdcd19fddc4ee5465d5164e2d532a439b7a4e63c27b77c485f42a14da9854fea779d231cc5000000000000000000000000000000000000000000000000000000000000001c2fe15d780efa8c7ee7bbea09736ff33e8b5bdcda440afca61f82cef7ff843cac6dadb4ddedc713d676681b6e5e5c039354d3e163cb1d0949e4e52cfdb9d111711702f990e895d7e75dbd68d2133350e76cce398eccacb7772ec51e01b8c929e6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569a00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a5200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16b5b7a6125a000000000000000000000000000000000000000000000000002e16b5bffad3c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000022170000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a7199e282000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933597a4e6c4d445a6b4d69316a5a546b314c545535596d4d7459574a6d597930774e6a49795a44526a4f5463785954496966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000004aa9f7899797ac70fe9ed25f140acc020fd3bda10000000000000000000000000000000000000000000000000000000008529ff8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f18d9f445cf2ab84b3c145b1619255290d826eeceef174d20eb36d9163c2bd2",
      "signature": {
        "s": "0x4ee5465d5164e2d532a439b7a4e63c27b77c485f42a14da9854fea779d231cc5",
        "r": "0x50d97246e91df17697e4be098d88f920432e1646296684f05ad7c8bdcd19fddc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2fe15d780efa8c7ee7bbea09736ff33e8b5bdcda440afca61f82cef7ff843cac",
      "signature": {
        "s": "0x1702f990e895d7e75dbd68d2133350e76cce398eccacb7772ec51e01b8c929e6",
        "r": "0x6dadb4ddedc713d676681b6e5e5c039354d3e163cb1d0949e4e52cfdb9d11171",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "139632632",
    "total": "139632632"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139632632",
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
            "amount": "44855583362"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "139632"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YzNlMDZkMi1jZTk1LTU5YmMtYWJmYy0wNjIyZDRjOTcxYTIifQ==",
    "nonce": 6738,
    "balances": {
      "current": "12972818654696026",
      "previous": "12972818794468290"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4aa9f7899797ac70fe9ed25f140acc020fd3bda1",
    "nonce": 10,
    "balances": {
      "current": "139632632",
      "previous": "0"
    }
  },
  "blockNumber": "10114714",
  "created": "2020-05-22T08:51:21.288Z",
  "updated": "2020-05-22T08:51:21.357Z",
  "id": "5ec79289b0c6090011d5b18f"
}
```
* *stageAmount*: `139632632`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000008529ff8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000008529ff80000000000000000000000000000000000000000000000000000000008529ff83f18d9f445cf2ab84b3c145b1619255290d826eeceef174d20eb36d9163c2bd250d97246e91df17697e4be098d88f920432e1646296684f05ad7c8bdcd19fddc4ee5465d5164e2d532a439b7a4e63c27b77c485f42a14da9854fea779d231cc5000000000000000000000000000000000000000000000000000000000000001c2fe15d780efa8c7ee7bbea09736ff33e8b5bdcda440afca61f82cef7ff843cac6dadb4ddedc713d676681b6e5e5c039354d3e163cb1d0949e4e52cfdb9d111711702f990e895d7e75dbd68d2133350e76cce398eccacb7772ec51e01b8c929e6000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569a00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a5200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e16b5b7a6125a000000000000000000000000000000000000000000000000002e16b5bffad3c200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000022170000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a7199e282000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933597a4e6c4d445a6b4d69316a5a546b314c545535596d4d7459574a6d597930774e6a49795a44526a4f5463785954496966513d3d000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000004aa9f7899797ac70fe9ed25f140acc020fd3bda10000000000000000000000000000000000000000000000000000000008529ff8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3f18d9f445cf2ab84b3c145b1619255290d826eeceef174d20eb36d9163c2bd2",
      "signature": {
        "s": "0x4ee5465d5164e2d532a439b7a4e63c27b77c485f42a14da9854fea779d231cc5",
        "r": "0x50d97246e91df17697e4be098d88f920432e1646296684f05ad7c8bdcd19fddc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2fe15d780efa8c7ee7bbea09736ff33e8b5bdcda440afca61f82cef7ff843cac",
      "signature": {
        "s": "0x1702f990e895d7e75dbd68d2133350e76cce398eccacb7772ec51e01b8c929e6",
        "r": "0x6dadb4ddedc713d676681b6e5e5c039354d3e163cb1d0949e4e52cfdb9d11171",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "139632632",
    "total": "139632632"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139632632",
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
            "amount": "44855583362"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "139632"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3YzNlMDZkMi1jZTk1LTU5YmMtYWJmYy0wNjIyZDRjOTcxYTIifQ==",
    "nonce": 6738,
    "balances": {
      "current": "12972818654696026",
      "previous": "12972818794468290"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4aa9f7899797ac70fe9ed25f140acc020fd3bda1",
    "nonce": 10,
    "balances": {
      "current": "139632632",
      "previous": "0"
    }
  },
  "blockNumber": "10114714",
  "created": "2020-05-22T08:51:21.288Z",
  "updated": "2020-05-22T08:51:21.357Z",
  "id": "5ec79289b0c6090011d5b18f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000008529ff8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `139632632`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`