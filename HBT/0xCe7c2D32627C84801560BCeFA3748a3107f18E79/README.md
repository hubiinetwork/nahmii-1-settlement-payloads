# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCe7c2D32627C84801560BCeFA3748a3107f18E79`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000000000000000000000000000000000004379b3c031c5913099b54349ae8582270d03806af4617e7dad2395dd5966e0f1d855fd437f8102eec59207b87450a62e44a3d5ddcaf83f4cb661e197de89248c37cafa2578bd83f867a81c59e3decf336fd3f244bc06f95370935338ad9f07c28e9413a5000000000000000000000000000000000000000000000000000000000000001b5b6fa6d3088b04bf68b478813fa3a3d0219f10eaaf10e0e95818627c6b180cd94d09753c6e18e755bdd356624cd894a3e66f9158b654f3a95a9d8205190881e0583fddf9e04063dd647396f51c46dfc93a206449582b814be7c91b6be4589076000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c6900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e136773c92686000000000000000000000000000000000000000000000000002e1367b754205700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000114611000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4a074dfc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6a51344f57497a4e7930784d7a51334c54566b4e4459744f4449344f5330795a446b324d444d315a6a4d304f57516966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000ce7c2d32627c84801560bcefa3748a3107f18e79000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x31c5913099b54349ae8582270d03806af4617e7dad2395dd5966e0f1d855fd43",
      "signature": {
        "s": "0x78bd83f867a81c59e3decf336fd3f244bc06f95370935338ad9f07c28e9413a5",
        "r": "0x7f8102eec59207b87450a62e44a3d5ddcaf83f4cb661e197de89248c37cafa25",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5b6fa6d3088b04bf68b478813fa3a3d0219f10eaaf10e0e95818627c6b180cd9",
      "signature": {
        "s": "0x583fddf9e04063dd647396f51c46dfc93a206449582b814be7c91b6be4589076",
        "r": "0x4d09753c6e18e755bdd356624cd894a3e66f9158b654f3a95a9d8205190881e0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1132049344",
    "total": "1132049344"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1132049344",
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
            "amount": "48486632956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1132049"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZjQ4OWIzNy0xMzQ3LTVkNDYtODI4OS0yZDk2MDM1ZjM0OWQifQ==",
    "nonce": 7273,
    "balances": {
      "current": "12969183973811846",
      "previous": "12969185106993239"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce7c2d32627c84801560bcefa3748a3107f18e79",
    "nonce": 14,
    "balances": {
      "current": "1132049344",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:34.275Z",
  "updated": "2020-05-22T08:55:34.366Z",
  "id": "5ec79386005df800101bcbc5"
}
```
* *stageAmount*: `1132049344`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000000000000000000000000000000000004379b3c031c5913099b54349ae8582270d03806af4617e7dad2395dd5966e0f1d855fd437f8102eec59207b87450a62e44a3d5ddcaf83f4cb661e197de89248c37cafa2578bd83f867a81c59e3decf336fd3f244bc06f95370935338ad9f07c28e9413a5000000000000000000000000000000000000000000000000000000000000001b5b6fa6d3088b04bf68b478813fa3a3d0219f10eaaf10e0e95818627c6b180cd94d09753c6e18e755bdd356624cd894a3e66f9158b654f3a95a9d8205190881e0583fddf9e04063dd647396f51c46dfc93a206449582b814be7c91b6be4589076000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c6900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e136773c92686000000000000000000000000000000000000000000000000002e1367b754205700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000114611000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4a074dfc000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6a51344f57497a4e7930784d7a51334c54566b4e4459744f4449344f5330795a446b324d444d315a6a4d304f57516966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000ce7c2d32627c84801560bcefa3748a3107f18e79000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x31c5913099b54349ae8582270d03806af4617e7dad2395dd5966e0f1d855fd43",
      "signature": {
        "s": "0x78bd83f867a81c59e3decf336fd3f244bc06f95370935338ad9f07c28e9413a5",
        "r": "0x7f8102eec59207b87450a62e44a3d5ddcaf83f4cb661e197de89248c37cafa25",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5b6fa6d3088b04bf68b478813fa3a3d0219f10eaaf10e0e95818627c6b180cd9",
      "signature": {
        "s": "0x583fddf9e04063dd647396f51c46dfc93a206449582b814be7c91b6be4589076",
        "r": "0x4d09753c6e18e755bdd356624cd894a3e66f9158b654f3a95a9d8205190881e0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1132049344",
    "total": "1132049344"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1132049344",
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
            "amount": "48486632956"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1132049"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZjQ4OWIzNy0xMzQ3LTVkNDYtODI4OS0yZDk2MDM1ZjM0OWQifQ==",
    "nonce": 7273,
    "balances": {
      "current": "12969183973811846",
      "previous": "12969185106993239"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xce7c2d32627c84801560bcefa3748a3107f18e79",
    "nonce": 14,
    "balances": {
      "current": "1132049344",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:34.275Z",
  "updated": "2020-05-22T08:55:34.366Z",
  "id": "5ec79386005df800101bcbc5"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004379b3c0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1132049344`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`