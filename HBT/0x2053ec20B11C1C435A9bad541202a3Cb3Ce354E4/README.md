# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2053ec20B11C1C435A9bad541202a3Cb3Ce354E4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000000000000000000000000000000000002963a7a4f8cca008be7c042027af40808781c861c9fd39add5d065de7add6a8418be616ff86c1a2113794d9b8a5e9460c2430de8efa7537a55a67bd47f4192652740c8cc7aa93d6a4e6e4aae97a6f064b793cc151aee6acd0eb8041f0f7afdb4d3cf98a6000000000000000000000000000000000000000000000000000000000000001b4b1725cd9e450f1ca63a6433f1eadc1c7b078d453b7e7759d7a51176c52a4d608e6c45adcdf21ceaf11c671d1c4f57c50bd17adbe7333ccfe334e8b2af378a0b7b060be6b86e39de56def4b05aad48d51fa9a2a682d77b93f587d9105e4f16fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000179a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b17adf0bb97000000000000000000000000000000000000000000000000002e1b17d75efbb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a987c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000952aa702a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a5464685954646b597930774d325a684c5455304f5751745957566d4e4330334d6d45324d325a6d4f5451315957556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002053ec20b11c1c435a9bad541202a3cb3ce354e4000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8cca008be7c042027af40808781c861c9fd39add5d065de7add6a8418be616f",
      "signature": {
        "s": "0x7aa93d6a4e6e4aae97a6f064b793cc151aee6acd0eb8041f0f7afdb4d3cf98a6",
        "r": "0xf86c1a2113794d9b8a5e9460c2430de8efa7537a55a67bd47f4192652740c8cc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4b1725cd9e450f1ca63a6433f1eadc1c7b078d453b7e7759d7a51176c52a4d60",
      "signature": {
        "s": "0x7b060be6b86e39de56def4b05aad48d51fa9a2a682d77b93f587d9105e4f16fe",
        "r": "0x8e6c45adcdf21ceaf11c671d1c4f57c50bd17adbe7333ccfe334e8b2af378a0b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "694396836",
    "total": "694396836"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "694396836",
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
            "amount": "40041607210"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "694396"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTdhYTdkYy0wM2ZhLTU0OWQtYWVmNC03MmE2M2ZmOTQ1YWUifQ==",
    "nonce": 6042,
    "balances": {
      "current": "12977637445122967",
      "previous": "12977638140214199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2053ec20b11c1c435a9bad541202a3cb3ce354e4",
    "nonce": 22,
    "balances": {
      "current": "694396836",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:45:56.498Z",
  "updated": "2020-05-22T08:45:57.580Z",
  "id": "5ec79144e5756b00111b872b"
}
```
* *stageAmount*: `694396836`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000000000000000000000000000000000002963a7a4f8cca008be7c042027af40808781c861c9fd39add5d065de7add6a8418be616ff86c1a2113794d9b8a5e9460c2430de8efa7537a55a67bd47f4192652740c8cc7aa93d6a4e6e4aae97a6f064b793cc151aee6acd0eb8041f0f7afdb4d3cf98a6000000000000000000000000000000000000000000000000000000000000001b4b1725cd9e450f1ca63a6433f1eadc1c7b078d453b7e7759d7a51176c52a4d608e6c45adcdf21ceaf11c671d1c4f57c50bd17adbe7333ccfe334e8b2af378a0b7b060be6b86e39de56def4b05aad48d51fa9a2a682d77b93f587d9105e4f16fe000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a567e0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000179a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b17adf0bb97000000000000000000000000000000000000000000000000002e1b17d75efbb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a987c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000952aa702a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a5464685954646b597930774d325a684c5455304f5751745957566d4e4330334d6d45324d325a6d4f5451315957556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000002053ec20b11c1c435a9bad541202a3cb3ce354e4000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8cca008be7c042027af40808781c861c9fd39add5d065de7add6a8418be616f",
      "signature": {
        "s": "0x7aa93d6a4e6e4aae97a6f064b793cc151aee6acd0eb8041f0f7afdb4d3cf98a6",
        "r": "0xf86c1a2113794d9b8a5e9460c2430de8efa7537a55a67bd47f4192652740c8cc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4b1725cd9e450f1ca63a6433f1eadc1c7b078d453b7e7759d7a51176c52a4d60",
      "signature": {
        "s": "0x7b060be6b86e39de56def4b05aad48d51fa9a2a682d77b93f587d9105e4f16fe",
        "r": "0x8e6c45adcdf21ceaf11c671d1c4f57c50bd17adbe7333ccfe334e8b2af378a0b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "694396836",
    "total": "694396836"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "694396836",
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
            "amount": "40041607210"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "694396"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTdhYTdkYy0wM2ZhLTU0OWQtYWVmNC03MmE2M2ZmOTQ1YWUifQ==",
    "nonce": 6042,
    "balances": {
      "current": "12977637445122967",
      "previous": "12977638140214199"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2053ec20b11c1c435a9bad541202a3cb3ce354e4",
    "nonce": 22,
    "balances": {
      "current": "694396836",
      "previous": "0"
    }
  },
  "blockNumber": "10114686",
  "created": "2020-05-22T08:45:56.498Z",
  "updated": "2020-05-22T08:45:57.580Z",
  "id": "5ec79144e5756b00111b872b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000002963a7a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `694396836`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`