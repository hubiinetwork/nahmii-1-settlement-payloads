# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5C868bfa7DDa94E95a06780B163579EB712Bf37c`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000fcc5100000000000000000000000000000000000000000000000000000000000fcc51000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000fcc5100000000000000000000000000000000000000000000000000000000000fcc51a21370c50de4042995ca17bc31df3d202a5cde89071868376239013b46ea916d76ed9bba146217fff0099ee50ff24c2bafb7d69f3bada3571671c59ae07879257f9cd2af017b20ff2fcec33d59b7760008bbcb36a0d30a8d9107d16324248202000000000000000000000000000000000000000000000000000000000000001c61803b43bf62481b94ea2084101c46514ae7af14c1d33a2046b61010d004de5e7390d5b9f2ae3380166960324b8066d64543aa0153beb7ef8867f187b5f10b352df1fa45a9b3b965653174b9a1463091460bbfab91ee6cbb2cbe4a475719bb97000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000153900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6ee9e18170000000000000000000000000000000000000000000000000002e1d6ee9f151cc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000040b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b96a43db000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6d45324e544d325953316b59544d784c54557a4e5751744f44466b4e69307a4e4442684e5449315a544d314d47556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005c868bfa7dda94e95a06780b163579eb712bf37c00000000000000000000000000000000000000000000000000000000000fcc51000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa21370c50de4042995ca17bc31df3d202a5cde89071868376239013b46ea916d",
      "signature": {
        "s": "0x7f9cd2af017b20ff2fcec33d59b7760008bbcb36a0d30a8d9107d16324248202",
        "r": "0x76ed9bba146217fff0099ee50ff24c2bafb7d69f3bada3571671c59ae0787925",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x61803b43bf62481b94ea2084101c46514ae7af14c1d33a2046b61010d004de5e",
      "signature": {
        "s": "0x2df1fa45a9b3b965653174b9a1463091460bbfab91ee6cbb2cbe4a475719bb97",
        "r": "0x7390d5b9f2ae3380166960324b8066d64543aa0153beb7ef8867f187b5f10b35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1035345",
    "total": "1035345"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1035345",
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
            "amount": "37470487515"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1035"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNmE2NTM2YS1kYTMxLTUzNWQtODFkNi0zNDBhNTI1ZTM1MGUifQ==",
    "nonce": 5433,
    "balances": {
      "current": "12980211136168304",
      "previous": "12980211137204684"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c868bfa7dda94e95a06780b163579eb712bf37c",
    "nonce": 22,
    "balances": {
      "current": "1035345",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:05.363Z",
  "updated": "2020-05-22T08:41:05.449Z",
  "id": "5ec79021005df800101bc954"
}
```
* *stageAmount*: `1035345`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000fcc51000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000fcc5100000000000000000000000000000000000000000000000000000000000fcc51a21370c50de4042995ca17bc31df3d202a5cde89071868376239013b46ea916d76ed9bba146217fff0099ee50ff24c2bafb7d69f3bada3571671c59ae07879257f9cd2af017b20ff2fcec33d59b7760008bbcb36a0d30a8d9107d16324248202000000000000000000000000000000000000000000000000000000000000001c61803b43bf62481b94ea2084101c46514ae7af14c1d33a2046b61010d004de5e7390d5b9f2ae3380166960324b8066d64543aa0153beb7ef8867f187b5f10b352df1fa45a9b3b965653174b9a1463091460bbfab91ee6cbb2cbe4a475719bb97000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000153900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d6ee9e18170000000000000000000000000000000000000000000000000002e1d6ee9f151cc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000040b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008b96a43db000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6d45324e544d325953316b59544d784c54557a4e5751744f44466b4e69307a4e4442684e5449315a544d314d47556966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005c868bfa7dda94e95a06780b163579eb712bf37c00000000000000000000000000000000000000000000000000000000000fcc51000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa21370c50de4042995ca17bc31df3d202a5cde89071868376239013b46ea916d",
      "signature": {
        "s": "0x7f9cd2af017b20ff2fcec33d59b7760008bbcb36a0d30a8d9107d16324248202",
        "r": "0x76ed9bba146217fff0099ee50ff24c2bafb7d69f3bada3571671c59ae0787925",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x61803b43bf62481b94ea2084101c46514ae7af14c1d33a2046b61010d004de5e",
      "signature": {
        "s": "0x2df1fa45a9b3b965653174b9a1463091460bbfab91ee6cbb2cbe4a475719bb97",
        "r": "0x7390d5b9f2ae3380166960324b8066d64543aa0153beb7ef8867f187b5f10b35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1035345",
    "total": "1035345"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1035345",
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
            "amount": "37470487515"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1035"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNmE2NTM2YS1kYTMxLTUzNWQtODFkNi0zNDBhNTI1ZTM1MGUifQ==",
    "nonce": 5433,
    "balances": {
      "current": "12980211136168304",
      "previous": "12980211137204684"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5c868bfa7dda94e95a06780b163579eb712bf37c",
    "nonce": 22,
    "balances": {
      "current": "1035345",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:05.363Z",
  "updated": "2020-05-22T08:41:05.449Z",
  "id": "5ec79021005df800101bc954"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000fcc51000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1035345`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`