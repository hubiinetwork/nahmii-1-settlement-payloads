# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x86d621be15b493d340fCFE022cf994A8B03406B5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000260000000000000000000000000000000000000000000000000000000000000026000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000260000000000000000000000000000000000000000000000000000000000000026876c1accf1007a07d42e1280418c6750f668b877068331c367698a48168c5a386a46ccf013e00f2e9eb0fb7fc198de4f08a5f20e07bda2fbd77a12aa7cdfe4062c2329b6bbd97c338a899fe12a9ff3ab61b6ac6a83cfe682695c71bbd85d9159000000000000000000000000000000000000000000000000000000000000001c6c48affe4a02ec47e1e3c8d539af679c0bcc89d2016571627d9ee9d49cab0822c71db149216dfb46dcbd61a5bf61ab303a9949b9cf95a866567e607d2124ebce73aab34ddc3ff501952b5b091c71c953fe9885ae397b7258fb3320fa0d5d42ce000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aa9b1600065000000000000000000000000000000000000000000000000002e1aa9b160008c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ecb50f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a4d304e6d55324e5331684e4441344c5456694d3255744f4451344e4330304d7a59775a6a6468595751794e54516966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000086d621be15b493d340fcfe022cf994a8b03406b50000000000000000000000000000000000000000000000000000000000000026000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x876c1accf1007a07d42e1280418c6750f668b877068331c367698a48168c5a38",
      "signature": {
        "s": "0x2c2329b6bbd97c338a899fe12a9ff3ab61b6ac6a83cfe682695c71bbd85d9159",
        "r": "0x6a46ccf013e00f2e9eb0fb7fc198de4f08a5f20e07bda2fbd77a12aa7cdfe406",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c48affe4a02ec47e1e3c8d539af679c0bcc89d2016571627d9ee9d49cab0822",
      "signature": {
        "s": "0x73aab34ddc3ff501952b5b091c71c953fe9885ae397b7258fb3320fa0d5d42ce",
        "r": "0xc71db149216dfb46dcbd61a5bf61ab303a9949b9cf95a866567e607d2124ebce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38",
    "total": "38"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38",
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
            "amount": "40513523956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzM0NmU2NS1hNDA4LTViM2UtODQ4NC00MzYwZjdhYWQyNTQifQ==",
    "nonce": 6295,
    "balances": {
      "current": "12977165056344165",
      "previous": "12977165056344204"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x86d621be15b493d340fcfe022cf994a8b03406b5",
    "nonce": 21,
    "balances": {
      "current": "38",
      "previous": "0"
    }
  },
  "blockNumber": "10114698",
  "created": "2020-05-22T08:47:57.167Z",
  "updated": "2020-05-22T08:47:57.267Z",
  "id": "5ec791bd005df800101bca6b"
}
```
* *stageAmount*: `38`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000026000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000260000000000000000000000000000000000000000000000000000000000000026876c1accf1007a07d42e1280418c6750f668b877068331c367698a48168c5a386a46ccf013e00f2e9eb0fb7fc198de4f08a5f20e07bda2fbd77a12aa7cdfe4062c2329b6bbd97c338a899fe12a9ff3ab61b6ac6a83cfe682695c71bbd85d9159000000000000000000000000000000000000000000000000000000000000001c6c48affe4a02ec47e1e3c8d539af679c0bcc89d2016571627d9ee9d49cab0822c71db149216dfb46dcbd61a5bf61ab303a9949b9cf95a866567e607d2124ebce73aab34ddc3ff501952b5b091c71c953fe9885ae397b7258fb3320fa0d5d42ce000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a568a0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000189700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1aa9b1600065000000000000000000000000000000000000000000000000002e1aa9b160008c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000096ecb50f4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a4d304e6d55324e5331684e4441344c5456694d3255744f4451344e4330304d7a59775a6a6468595751794e54516966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000086d621be15b493d340fcfe022cf994a8b03406b50000000000000000000000000000000000000000000000000000000000000026000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x876c1accf1007a07d42e1280418c6750f668b877068331c367698a48168c5a38",
      "signature": {
        "s": "0x2c2329b6bbd97c338a899fe12a9ff3ab61b6ac6a83cfe682695c71bbd85d9159",
        "r": "0x6a46ccf013e00f2e9eb0fb7fc198de4f08a5f20e07bda2fbd77a12aa7cdfe406",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c48affe4a02ec47e1e3c8d539af679c0bcc89d2016571627d9ee9d49cab0822",
      "signature": {
        "s": "0x73aab34ddc3ff501952b5b091c71c953fe9885ae397b7258fb3320fa0d5d42ce",
        "r": "0xc71db149216dfb46dcbd61a5bf61ab303a9949b9cf95a866567e607d2124ebce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38",
    "total": "38"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38",
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
            "amount": "40513523956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0YzM0NmU2NS1hNDA4LTViM2UtODQ4NC00MzYwZjdhYWQyNTQifQ==",
    "nonce": 6295,
    "balances": {
      "current": "12977165056344165",
      "previous": "12977165056344204"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x86d621be15b493d340fcfe022cf994a8b03406b5",
    "nonce": 21,
    "balances": {
      "current": "38",
      "previous": "0"
    }
  },
  "blockNumber": "10114698",
  "created": "2020-05-22T08:47:57.167Z",
  "updated": "2020-05-22T08:47:57.267Z",
  "id": "5ec791bd005df800101bca6b"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000026000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `38`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`