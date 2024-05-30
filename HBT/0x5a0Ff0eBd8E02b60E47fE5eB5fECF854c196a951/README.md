# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5a0Ff0eBd8E02b60E47fE5eB5fECF854c196a951`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000d1b4fc3a00000000000000000000000000000000000000000000000000000000d1b4fc3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000d1b4fc3a00000000000000000000000000000000000000000000000000000000d1b4fc3af3ebd21f64f6e85af7f0ed55f5c42ffbd3b74bf1a0a52cec67e7d964a6c2e7dafdfe938dd73372e938413db3f6217eb2fac1b8a1060428e3971099b8ba92d9435abc70607f165d9da46e23d9869f2eefcac436c3f768a7feb6a2204906133f17000000000000000000000000000000000000000000000000000000000000001c5804b1706d089d76c311d9db1d52ef8d64dab3eb14fce2621b5e9974dd6d78f3769f1a0d8c4e42fcf4bbe0866d2e1c7f461f433b8f60bd066dc04407b42cb962735469e4a87470162e948f5dbadb455da65296294b29a8fb2d0b1525e344e523000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b40ad8d23ef000000000000000000000000000000000000000000000000002e1b417f77cf8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000035af5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009482e3f44000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e54426b4d7a55354d7930774d5759784c545577597a67744f44426c4d6930344e5456695a6d45794e7a6c6c5a44516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005a0ff0ebd8e02b60e47fe5eb5fecf854c196a95100000000000000000000000000000000000000000000000000000000d1b4fc3a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf3ebd21f64f6e85af7f0ed55f5c42ffbd3b74bf1a0a52cec67e7d964a6c2e7da",
      "signature": {
        "s": "0x5abc70607f165d9da46e23d9869f2eefcac436c3f768a7feb6a2204906133f17",
        "r": "0xfdfe938dd73372e938413db3f6217eb2fac1b8a1060428e3971099b8ba92d943",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5804b1706d089d76c311d9db1d52ef8d64dab3eb14fce2621b5e9974dd6d78f3",
      "signature": {
        "s": "0x735469e4a87470162e948f5dbadb455da65296294b29a8fb2d0b1525e344e523",
        "r": "0x769f1a0d8c4e42fcf4bbe0866d2e1c7f461f433b8f60bd066dc04407b42cb962",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3518299194",
    "total": "3518299194"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3518299194",
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
            "amount": "39865696068"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3518299"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNTBkMzU5My0wMWYxLTUwYzgtODBlMi04NTViZmEyNzllZDQifQ==",
    "nonce": 5885,
    "balances": {
      "current": "12977813532255215",
      "previous": "12977817054072708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5a0ff0ebd8e02b60e47fe5eb5fecf854c196a951",
    "nonce": 22,
    "balances": {
      "current": "3518299194",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:45.110Z",
  "updated": "2020-05-22T08:44:45.176Z",
  "id": "5ec790fdb0c6090011d5b068"
}
```
* *stageAmount*: `3518299194`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000d1b4fc3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000d1b4fc3a00000000000000000000000000000000000000000000000000000000d1b4fc3af3ebd21f64f6e85af7f0ed55f5c42ffbd3b74bf1a0a52cec67e7d964a6c2e7dafdfe938dd73372e938413db3f6217eb2fac1b8a1060428e3971099b8ba92d9435abc70607f165d9da46e23d9869f2eefcac436c3f768a7feb6a2204906133f17000000000000000000000000000000000000000000000000000000000000001c5804b1706d089d76c311d9db1d52ef8d64dab3eb14fce2621b5e9974dd6d78f3769f1a0d8c4e42fcf4bbe0866d2e1c7f461f433b8f60bd066dc04407b42cb962735469e4a87470162e948f5dbadb455da65296294b29a8fb2d0b1525e344e523000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5676000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000016fd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b40ad8d23ef000000000000000000000000000000000000000000000000002e1b417f77cf8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000035af5b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009482e3f44000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e54426b4d7a55354d7930774d5759784c545577597a67744f44426c4d6930344e5456695a6d45794e7a6c6c5a44516966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005a0ff0ebd8e02b60e47fe5eb5fecf854c196a95100000000000000000000000000000000000000000000000000000000d1b4fc3a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf3ebd21f64f6e85af7f0ed55f5c42ffbd3b74bf1a0a52cec67e7d964a6c2e7da",
      "signature": {
        "s": "0x5abc70607f165d9da46e23d9869f2eefcac436c3f768a7feb6a2204906133f17",
        "r": "0xfdfe938dd73372e938413db3f6217eb2fac1b8a1060428e3971099b8ba92d943",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5804b1706d089d76c311d9db1d52ef8d64dab3eb14fce2621b5e9974dd6d78f3",
      "signature": {
        "s": "0x735469e4a87470162e948f5dbadb455da65296294b29a8fb2d0b1525e344e523",
        "r": "0x769f1a0d8c4e42fcf4bbe0866d2e1c7f461f433b8f60bd066dc04407b42cb962",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3518299194",
    "total": "3518299194"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3518299194",
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
            "amount": "39865696068"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3518299"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNTBkMzU5My0wMWYxLTUwYzgtODBlMi04NTViZmEyNzllZDQifQ==",
    "nonce": 5885,
    "balances": {
      "current": "12977813532255215",
      "previous": "12977817054072708"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5a0ff0ebd8e02b60e47fe5eb5fecf854c196a951",
    "nonce": 22,
    "balances": {
      "current": "3518299194",
      "previous": "0"
    }
  },
  "blockNumber": "10114678",
  "created": "2020-05-22T08:44:45.110Z",
  "updated": "2020-05-22T08:44:45.176Z",
  "id": "5ec790fdb0c6090011d5b068"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000d1b4fc3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3518299194`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`