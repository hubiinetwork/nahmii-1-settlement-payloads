# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdc83951cf3084AA28B7494DdBD48B44dFc9F15B0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000017ced2ec0000000000000000000000000000000000000000000000000000000017ced2ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000017ced2ec0000000000000000000000000000000000000000000000000000000017ced2ecdb1943064e0b587ba4620d6bfa56db7ecfc615341f48d53110c61424864b14f9234359a37d3f937704553c1d507f549796cc9335e44d4ea3ed5cfdbd16fa6904523f3d80f64ec486f6845b92388619cd8c359517087007274cecd6ff446d89fb000000000000000000000000000000000000000000000000000000000000001cd2206246baa20808ee1706d400340c3fc0a5a5d72a73b45ff91c2ff417d8620cff4df032dde1480a13f9f26a3341bdd461230c621bd058c1f717787ef53f5d140d89c6fb4bc2ad2a27bb8be7544b0924427e81b679c4035a99bd05fa6a271533000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569e00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ad500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e161495f978da000000000000000000000000000000000000000000000000002e1614adce640c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000061846000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9acf4055000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d6a4e6b5a6a55314d69307a4d6a566a4c5455334f5749744f474d334d69316d5a6a64684f444d304d545a684e7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dc83951cf3084aa28b7494ddbd48b44dfc9f15b00000000000000000000000000000000000000000000000000000000017ced2ec000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb1943064e0b587ba4620d6bfa56db7ecfc615341f48d53110c61424864b14f9",
      "signature": {
        "s": "0x523f3d80f64ec486f6845b92388619cd8c359517087007274cecd6ff446d89fb",
        "r": "0x234359a37d3f937704553c1d507f549796cc9335e44d4ea3ed5cfdbd16fa6904",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd2206246baa20808ee1706d400340c3fc0a5a5d72a73b45ff91c2ff417d8620c",
      "signature": {
        "s": "0x0d89c6fb4bc2ad2a27bb8be7544b0924427e81b679c4035a99bd05fa6a271533",
        "r": "0xff4df032dde1480a13f9f26a3341bdd461230c621bd058c1f717787ef53f5d14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "399430380",
    "total": "399430380"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "399430380",
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
            "amount": "45546946645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "399430"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMjNkZjU1Mi0zMjVjLTU3OWItOGM3Mi1mZjdhODM0MTZhNzIifQ==",
    "nonce": 6869,
    "balances": {
      "current": "12972126600001754",
      "previous": "12972126999831564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdc83951cf3084aa28b7494ddbd48b44dfc9f15b0",
    "nonce": 22,
    "balances": {
      "current": "399430380",
      "previous": "0"
    }
  },
  "blockNumber": "10114718",
  "created": "2020-05-22T08:52:14.495Z",
  "updated": "2020-05-22T08:52:14.553Z",
  "id": "5ec792bee5756b00111b8831"
}
```
* *stageAmount*: `399430380`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000017ced2ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000017ced2ec0000000000000000000000000000000000000000000000000000000017ced2ecdb1943064e0b587ba4620d6bfa56db7ecfc615341f48d53110c61424864b14f9234359a37d3f937704553c1d507f549796cc9335e44d4ea3ed5cfdbd16fa6904523f3d80f64ec486f6845b92388619cd8c359517087007274cecd6ff446d89fb000000000000000000000000000000000000000000000000000000000000001cd2206246baa20808ee1706d400340c3fc0a5a5d72a73b45ff91c2ff417d8620cff4df032dde1480a13f9f26a3341bdd461230c621bd058c1f717787ef53f5d140d89c6fb4bc2ad2a27bb8be7544b0924427e81b679c4035a99bd05fa6a271533000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a569e00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ad500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e161495f978da000000000000000000000000000000000000000000000000002e1614adce640c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000061846000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a9acf4055000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d6a4e6b5a6a55314d69307a4d6a566a4c5455334f5749744f474d334d69316d5a6a64684f444d304d545a684e7a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dc83951cf3084aa28b7494ddbd48b44dfc9f15b00000000000000000000000000000000000000000000000000000000017ced2ec000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdb1943064e0b587ba4620d6bfa56db7ecfc615341f48d53110c61424864b14f9",
      "signature": {
        "s": "0x523f3d80f64ec486f6845b92388619cd8c359517087007274cecd6ff446d89fb",
        "r": "0x234359a37d3f937704553c1d507f549796cc9335e44d4ea3ed5cfdbd16fa6904",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd2206246baa20808ee1706d400340c3fc0a5a5d72a73b45ff91c2ff417d8620c",
      "signature": {
        "s": "0x0d89c6fb4bc2ad2a27bb8be7544b0924427e81b679c4035a99bd05fa6a271533",
        "r": "0xff4df032dde1480a13f9f26a3341bdd461230c621bd058c1f717787ef53f5d14",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "399430380",
    "total": "399430380"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "399430380",
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
            "amount": "45546946645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "399430"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMjNkZjU1Mi0zMjVjLTU3OWItOGM3Mi1mZjdhODM0MTZhNzIifQ==",
    "nonce": 6869,
    "balances": {
      "current": "12972126600001754",
      "previous": "12972126999831564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdc83951cf3084aa28b7494ddbd48b44dfc9f15b0",
    "nonce": 22,
    "balances": {
      "current": "399430380",
      "previous": "0"
    }
  },
  "blockNumber": "10114718",
  "created": "2020-05-22T08:52:14.495Z",
  "updated": "2020-05-22T08:52:14.553Z",
  "id": "5ec792bee5756b00111b8831"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000017ced2ec000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `399430380`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`