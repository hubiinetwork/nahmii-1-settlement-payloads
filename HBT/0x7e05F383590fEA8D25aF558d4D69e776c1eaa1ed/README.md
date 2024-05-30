# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7e05F383590fEA8D25aF558d4D69e776c1eaa1ed`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000001296d800000000000000000000000000000000000000000000000000000000001296d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000001296d800000000000000000000000000000000000000000000000000000000001296d87621fb272f8ad7447859cc44e7e6e9e48201911fa1cdcb07431847192c259778cbf5b03a30724b48d1ed8ce02f6c72869df60338e3d149cd733558df044a61316e6126de79454bc22149af9afb1cdf0844b74c2df0d8941c491b1efaa69275ca000000000000000000000000000000000000000000000000000000000000001c6a96e968c7305f7e1c8042a8f7aa4121d47a19d7e45f297fadf52fce1cdd9e348fecca83461424db9bb296c11851edede52750f52dd8b931a5dd4aaedd21e580125ff6f44e9b2728e2eb13af2aa10feaad6b416790a4ed725eb8b3f7c9f8b933000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e8200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0453ace674000000000000000000000000000000000000000000000000002e0b0453bf820e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f24bd55000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a6c6b4e7a677a5a693034595467784c5455344e7a5174596a41784e4330344e6a5131596d51304e545a6c4d7a6b6966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000007e05f383590fea8d25af558d4d69e776c1eaa1ed00000000000000000000000000000000000000000000000000000000001296d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7621fb272f8ad7447859cc44e7e6e9e48201911fa1cdcb07431847192c259778",
      "signature": {
        "s": "0x6e6126de79454bc22149af9afb1cdf0844b74c2df0d8941c491b1efaa69275ca",
        "r": "0xcbf5b03a30724b48d1ed8ce02f6c72869df60338e3d149cd733558df044a6131",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a96e968c7305f7e1c8042a8f7aa4121d47a19d7e45f297fadf52fce1cdd9e34",
      "signature": {
        "s": "0x125ff6f44e9b2728e2eb13af2aa10feaad6b416790a4ed725eb8b3f7c9f8b933",
        "r": "0x8fecca83461424db9bb296c11851edede52750f52dd8b931a5dd4aaedd21e580",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1218264",
    "total": "1218264"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1218264",
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
            "amount": "57699253589"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1218"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYjlkNzgzZi04YTgxLTU4NzQtYjAxNC04NjQ1YmQ0NTZlMzkifQ==",
    "nonce": 7810,
    "balances": {
      "current": "12959962140305012",
      "previous": "12959962141524494"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e05f383590fea8d25af558d4d69e776c1eaa1ed",
    "nonce": 6,
    "balances": {
      "current": "1218264",
      "previous": "0"
    }
  },
  "blockNumber": "10114753",
  "created": "2020-05-22T08:59:45.444Z",
  "updated": "2020-05-22T08:59:45.507Z",
  "id": "5ec79481e5756b00111b895d"
}
```
* *stageAmount*: `1218264`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000001296d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000001296d800000000000000000000000000000000000000000000000000000000001296d87621fb272f8ad7447859cc44e7e6e9e48201911fa1cdcb07431847192c259778cbf5b03a30724b48d1ed8ce02f6c72869df60338e3d149cd733558df044a61316e6126de79454bc22149af9afb1cdf0844b74c2df0d8941c491b1efaa69275ca000000000000000000000000000000000000000000000000000000000000001c6a96e968c7305f7e1c8042a8f7aa4121d47a19d7e45f297fadf52fce1cdd9e348fecca83461424db9bb296c11851edede52750f52dd8b931a5dd4aaedd21e580125ff6f44e9b2728e2eb13af2aa10feaad6b416790a4ed725eb8b3f7c9f8b933000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e8200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0453ace674000000000000000000000000000000000000000000000000002e0b0453bf820e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004c2000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f24bd55000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d596a6c6b4e7a677a5a693034595467784c5455344e7a5174596a41784e4330344e6a5131596d51304e545a6c4d7a6b6966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000007e05f383590fea8d25af558d4d69e776c1eaa1ed00000000000000000000000000000000000000000000000000000000001296d8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7621fb272f8ad7447859cc44e7e6e9e48201911fa1cdcb07431847192c259778",
      "signature": {
        "s": "0x6e6126de79454bc22149af9afb1cdf0844b74c2df0d8941c491b1efaa69275ca",
        "r": "0xcbf5b03a30724b48d1ed8ce02f6c72869df60338e3d149cd733558df044a6131",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6a96e968c7305f7e1c8042a8f7aa4121d47a19d7e45f297fadf52fce1cdd9e34",
      "signature": {
        "s": "0x125ff6f44e9b2728e2eb13af2aa10feaad6b416790a4ed725eb8b3f7c9f8b933",
        "r": "0x8fecca83461424db9bb296c11851edede52750f52dd8b931a5dd4aaedd21e580",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1218264",
    "total": "1218264"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1218264",
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
            "amount": "57699253589"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1218"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmYjlkNzgzZi04YTgxLTU4NzQtYjAxNC04NjQ1YmQ0NTZlMzkifQ==",
    "nonce": 7810,
    "balances": {
      "current": "12959962140305012",
      "previous": "12959962141524494"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7e05f383590fea8d25af558d4d69e776c1eaa1ed",
    "nonce": 6,
    "balances": {
      "current": "1218264",
      "previous": "0"
    }
  },
  "blockNumber": "10114753",
  "created": "2020-05-22T08:59:45.444Z",
  "updated": "2020-05-22T08:59:45.507Z",
  "id": "5ec79481e5756b00111b895d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000001296d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1218264`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`