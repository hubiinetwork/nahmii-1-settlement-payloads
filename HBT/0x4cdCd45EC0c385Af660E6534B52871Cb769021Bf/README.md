# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4cdCd45EC0c385Af660E6534B52871Cb769021Bf`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000052cc84e4ea00000000000000000000000000000000000000000000000000000052cc84e4ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000052cc84e4ea00000000000000000000000000000000000000000000000000000052cc84e4eaa1c4a0b941c2c9aff50e60e2019c201e7f90899466199b587cc905f112c78d9d6b9f7815aea9923cea08d76644424a241828065f32aa19c10b290665b40151b27f390117688e99a9b872a938bbaf58a9f56970129f16bfc6a939c2299bd5000a000000000000000000000000000000000000000000000000000000000000001c3aa7de8e677d79e820f26bcbc3cd8c1663bb32935bc0de8bc9be5dd0516ec7c6817f53cafd6fb872181097a24dd70cccdd6511302f936eb6fe570bec29248d316c1142cd03060758726380760cd7912861b59903fd65947d04b982bf6c8a5975000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d2600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0cfb6d3ea17b000000000000000000000000000000000000000000000000002e0d4e4ef5d57800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000015324f13000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cee7a86d0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d544e6d4d4752694e4331684e6d52694c5456694e3251744f44526d4d6930305a445a694e6a5130596d4a6c4e44676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004cdcd45ec0c385af660e6534b52871cb769021bf00000000000000000000000000000000000000000000000000000052cc84e4ea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1c4a0b941c2c9aff50e60e2019c201e7f90899466199b587cc905f112c78d9d",
      "signature": {
        "s": "0x7f390117688e99a9b872a938bbaf58a9f56970129f16bfc6a939c2299bd5000a",
        "r": "0x6b9f7815aea9923cea08d76644424a241828065f32aa19c10b290665b40151b2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3aa7de8e677d79e820f26bcbc3cd8c1663bb32935bc0de8bc9be5dd0516ec7c6",
      "signature": {
        "s": "0x6c1142cd03060758726380760cd7912861b59903fd65947d04b982bf6c8a5975",
        "r": "0x817f53cafd6fb872181097a24dd70cccdd6511302f936eb6fe570bec29248d31",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "355618579690",
    "total": "355618579690"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "355618579690",
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
            "amount": "55540614864"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "355618579"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTNmMGRiNC1hNmRiLTViN2QtODRmMi00ZDZiNjQ0YmJlNDgifQ==",
    "nonce": 7462,
    "balances": {
      "current": "12962122937835899",
      "previous": "12962478912034168"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4cdcd45ec0c385af660e6534b52871cb769021bf",
    "nonce": 22,
    "balances": {
      "current": "355618579690",
      "previous": "0"
    }
  },
  "blockNumber": "10114740",
  "created": "2020-05-22T08:57:03.669Z",
  "updated": "2020-05-22T08:57:03.755Z",
  "id": "5ec793dfb0c6090011d5b28b"
}
```
* *stageAmount*: `355618579690`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000052cc84e4ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000052cc84e4ea00000000000000000000000000000000000000000000000000000052cc84e4eaa1c4a0b941c2c9aff50e60e2019c201e7f90899466199b587cc905f112c78d9d6b9f7815aea9923cea08d76644424a241828065f32aa19c10b290665b40151b27f390117688e99a9b872a938bbaf58a9f56970129f16bfc6a939c2299bd5000a000000000000000000000000000000000000000000000000000000000000001c3aa7de8e677d79e820f26bcbc3cd8c1663bb32935bc0de8bc9be5dd0516ec7c6817f53cafd6fb872181097a24dd70cccdd6511302f936eb6fe570bec29248d316c1142cd03060758726380760cd7912861b59903fd65947d04b982bf6c8a5975000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b400000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d2600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0cfb6d3ea17b000000000000000000000000000000000000000000000000002e0d4e4ef5d57800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000015324f13000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000cee7a86d0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d544e6d4d4752694e4331684e6d52694c5456694e3251744f44526d4d6930305a445a694e6a5130596d4a6c4e44676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004cdcd45ec0c385af660e6534b52871cb769021bf00000000000000000000000000000000000000000000000000000052cc84e4ea000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa1c4a0b941c2c9aff50e60e2019c201e7f90899466199b587cc905f112c78d9d",
      "signature": {
        "s": "0x7f390117688e99a9b872a938bbaf58a9f56970129f16bfc6a939c2299bd5000a",
        "r": "0x6b9f7815aea9923cea08d76644424a241828065f32aa19c10b290665b40151b2",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3aa7de8e677d79e820f26bcbc3cd8c1663bb32935bc0de8bc9be5dd0516ec7c6",
      "signature": {
        "s": "0x6c1142cd03060758726380760cd7912861b59903fd65947d04b982bf6c8a5975",
        "r": "0x817f53cafd6fb872181097a24dd70cccdd6511302f936eb6fe570bec29248d31",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "355618579690",
    "total": "355618579690"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "355618579690",
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
            "amount": "55540614864"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "355618579"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMTNmMGRiNC1hNmRiLTViN2QtODRmMi00ZDZiNjQ0YmJlNDgifQ==",
    "nonce": 7462,
    "balances": {
      "current": "12962122937835899",
      "previous": "12962478912034168"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4cdcd45ec0c385af660e6534b52871cb769021bf",
    "nonce": 22,
    "balances": {
      "current": "355618579690",
      "previous": "0"
    }
  },
  "blockNumber": "10114740",
  "created": "2020-05-22T08:57:03.669Z",
  "updated": "2020-05-22T08:57:03.755Z",
  "id": "5ec793dfb0c6090011d5b28b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000052cc84e4ea000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `355618579690`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`