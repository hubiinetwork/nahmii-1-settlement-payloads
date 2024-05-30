# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdBaf20bbdde49b2afC57673d9a67082F85E8A096`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000000000000000000000000000000000000e722304f8885e65ed76115e03228a114a94ca5c8fc1c63b697343d954c3d89226327d5efe596fdde0af5920f071cc3f74a39d984bac8a9e4991ae232197b1bc612aa3f67c3a311e5c75a5def8ab242735f04ad0f684dd634a1c9b6a6b8d1e846ea10eff000000000000000000000000000000000000000000000000000000000000001baab4ff5d58c1617bde393b2da8072ecadbd992af91781c6d0515e1c7bddd1a1189ea3ab8dffc6068fe4483778bddfbdb3bda8f5cd499158f3ab6916e513de9973eb5dbd340f6c4f83422578d78b35b3d1308388512db11fc2fdbad07fadac4a5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02b0b28b9a000000000000000000000000000000000000000000000000002e0b02bf28615700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003b2b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f8fe3fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f574e68597a51314e43307759544d794c5455304e474574596a4a6a4d69316b4f4451314e444d334d3251335957496966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000dbaf20bbdde49b2afc57673d9a67082f85e8a096000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8885e65ed76115e03228a114a94ca5c8fc1c63b697343d954c3d89226327d5e",
      "signature": {
        "s": "0x7c3a311e5c75a5def8ab242735f04ad0f684dd634a1c9b6a6b8d1e846ea10eff",
        "r": "0xfe596fdde0af5920f071cc3f74a39d984bac8a9e4991ae232197b1bc612aa3f6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaab4ff5d58c1617bde393b2da8072ecadbd992af91781c6d0515e1c7bddd1a11",
      "signature": {
        "s": "0x3eb5dbd340f6c4f83422578d78b35b3d1308388512db11fc2fdbad07fadac4a5",
        "r": "0x89ea3ab8dffc6068fe4483778bddfbdb3bda8f5cd499158f3ab6916e513de997",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "242361092",
    "total": "242361092"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "242361092",
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
            "amount": "57706275838"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "242361"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOWNhYzQ1NC0wYTMyLTU0NGEtYjJjMi1kODQ1NDM3M2Q3YWIifQ==",
    "nonce": 7834,
    "balances": {
      "current": "12959955111021466",
      "previous": "12959955353624919"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbaf20bbdde49b2afc57673d9a67082f85e8a096",
    "nonce": 12,
    "balances": {
      "current": "242361092",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:55.076Z",
  "updated": "2020-05-22T08:59:55.138Z",
  "id": "5ec7948bb0c6090011d5b30b"
}
```
* *stageAmount*: `242361092`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000000000000000000000000000000000000e722304f8885e65ed76115e03228a114a94ca5c8fc1c63b697343d954c3d89226327d5efe596fdde0af5920f071cc3f74a39d984bac8a9e4991ae232197b1bc612aa3f67c3a311e5c75a5def8ab242735f04ad0f684dd634a1c9b6a6b8d1e846ea10eff000000000000000000000000000000000000000000000000000000000000001baab4ff5d58c1617bde393b2da8072ecadbd992af91781c6d0515e1c7bddd1a1189ea3ab8dffc6068fe4483778bddfbdb3bda8f5cd499158f3ab6916e513de9973eb5dbd340f6c4f83422578d78b35b3d1308388512db11fc2fdbad07fadac4a5000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e9a00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b02b0b28b9a000000000000000000000000000000000000000000000000002e0b02bf28615700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003b2b9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6f8fe3fe000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684f574e68597a51314e43307759544d794c5455304e474574596a4a6a4d69316b4f4451314e444d334d3251335957496966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000dbaf20bbdde49b2afc57673d9a67082f85e8a096000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf8885e65ed76115e03228a114a94ca5c8fc1c63b697343d954c3d89226327d5e",
      "signature": {
        "s": "0x7c3a311e5c75a5def8ab242735f04ad0f684dd634a1c9b6a6b8d1e846ea10eff",
        "r": "0xfe596fdde0af5920f071cc3f74a39d984bac8a9e4991ae232197b1bc612aa3f6",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xaab4ff5d58c1617bde393b2da8072ecadbd992af91781c6d0515e1c7bddd1a11",
      "signature": {
        "s": "0x3eb5dbd340f6c4f83422578d78b35b3d1308388512db11fc2fdbad07fadac4a5",
        "r": "0x89ea3ab8dffc6068fe4483778bddfbdb3bda8f5cd499158f3ab6916e513de997",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "242361092",
    "total": "242361092"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "242361092",
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
            "amount": "57706275838"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "242361"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhOWNhYzQ1NC0wYTMyLTU0NGEtYjJjMi1kODQ1NDM3M2Q3YWIifQ==",
    "nonce": 7834,
    "balances": {
      "current": "12959955111021466",
      "previous": "12959955353624919"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdbaf20bbdde49b2afc57673d9a67082f85e8a096",
    "nonce": 12,
    "balances": {
      "current": "242361092",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:55.076Z",
  "updated": "2020-05-22T08:59:55.138Z",
  "id": "5ec7948bb0c6090011d5b30b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000e722304000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `242361092`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`