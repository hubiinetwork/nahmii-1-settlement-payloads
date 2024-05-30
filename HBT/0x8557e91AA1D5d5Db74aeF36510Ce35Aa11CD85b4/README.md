# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x8557e91AA1D5d5Db74aeF36510Ce35Aa11CD85b4`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000000000000000000000000000000000004123e81f8f500ec60a74c23cc2f73b5a2cafe55c82b04206d57224b869803df7243173ec8a9f57a214522e19f26d57e5be1f873e778122c7a30aeaf0cece5ece11c0a880267a92c72049e3c11bb9208a245638d72c6be254e07204c3fb4251a54b02db02000000000000000000000000000000000000000000000000000000000000001bd94d06104b29011b2edf89cc157a6e98b5ee43f04d6ca33f6e152b5fa7094847077e37487781498dfc5c4e7a2ebd1e84005ebe6ff1eb5bd815aa91ee980a3c357c3970d11f62d802a1e3b5027062ce3d5c4134f83ddf0e82c63f56996618e77d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000161800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfa98be0149000000000000000000000000000000000000000000000000002e1cfad9f2967000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010ad08000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d72998b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a575a684d7a51314f53307a4f4759774c54566b4d4459744f575a694e6930774d54517a5954526c5a6a426a4d7a456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008557e91aa1d5d5db74aef36510ce35aa11cd85b4000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f500ec60a74c23cc2f73b5a2cafe55c82b04206d57224b869803df7243173ec",
      "signature": {
        "s": "0x267a92c72049e3c11bb9208a245638d72c6be254e07204c3fb4251a54b02db02",
        "r": "0x8a9f57a214522e19f26d57e5be1f873e778122c7a30aeaf0cece5ece11c0a880",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd94d06104b29011b2edf89cc157a6e98b5ee43f04d6ca33f6e152b5fa7094847",
      "signature": {
        "s": "0x7c3970d11f62d802a1e3b5027062ce3d5c4134f83ddf0e82c63f56996618e77d",
        "r": "0x077e37487781498dfc5c4e7a2ebd1e84005ebe6ff1eb5bd815aa91ee980a3c35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1092872223",
    "total": "1092872223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1092872223",
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
            "amount": "37969565877"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1092872"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZWZhMzQ1OS0zOGYwLTVkMDYtOWZiNi0wMTQzYTRlZjBjMzEifQ==",
    "nonce": 5656,
    "balances": {
      "current": "12979711558680905",
      "previous": "12979712652646000"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8557e91aa1d5d5db74aef36510ce35aa11cd85b4",
    "nonce": 22,
    "balances": {
      "current": "1092872223",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:52.760Z",
  "updated": "2020-05-22T08:42:52.829Z",
  "id": "5ec7908c005df800101bc99b"
}
```
* *stageAmount*: `1092872223`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000000000000000000000000000000000004123e81f8f500ec60a74c23cc2f73b5a2cafe55c82b04206d57224b869803df7243173ec8a9f57a214522e19f26d57e5be1f873e778122c7a30aeaf0cece5ece11c0a880267a92c72049e3c11bb9208a245638d72c6be254e07204c3fb4251a54b02db02000000000000000000000000000000000000000000000000000000000000001bd94d06104b29011b2edf89cc157a6e98b5ee43f04d6ca33f6e152b5fa7094847077e37487781498dfc5c4e7a2ebd1e84005ebe6ff1eb5bd815aa91ee980a3c357c3970d11f62d802a1e3b5027062ce3d5c4134f83ddf0e82c63f56996618e77d000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56710000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000161800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1cfa98be0149000000000000000000000000000000000000000000000000002e1cfad9f2967000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000010ad08000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008d72998b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a575a684d7a51314f53307a4f4759774c54566b4d4459744f575a694e6930774d54517a5954526c5a6a426a4d7a456966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000008557e91aa1d5d5db74aef36510ce35aa11cd85b4000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8f500ec60a74c23cc2f73b5a2cafe55c82b04206d57224b869803df7243173ec",
      "signature": {
        "s": "0x267a92c72049e3c11bb9208a245638d72c6be254e07204c3fb4251a54b02db02",
        "r": "0x8a9f57a214522e19f26d57e5be1f873e778122c7a30aeaf0cece5ece11c0a880",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd94d06104b29011b2edf89cc157a6e98b5ee43f04d6ca33f6e152b5fa7094847",
      "signature": {
        "s": "0x7c3970d11f62d802a1e3b5027062ce3d5c4134f83ddf0e82c63f56996618e77d",
        "r": "0x077e37487781498dfc5c4e7a2ebd1e84005ebe6ff1eb5bd815aa91ee980a3c35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1092872223",
    "total": "1092872223"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1092872223",
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
            "amount": "37969565877"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1092872"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZWZhMzQ1OS0zOGYwLTVkMDYtOWZiNi0wMTQzYTRlZjBjMzEifQ==",
    "nonce": 5656,
    "balances": {
      "current": "12979711558680905",
      "previous": "12979712652646000"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x8557e91aa1d5d5db74aef36510ce35aa11cd85b4",
    "nonce": 22,
    "balances": {
      "current": "1092872223",
      "previous": "0"
    }
  },
  "blockNumber": "10114673",
  "created": "2020-05-22T08:42:52.760Z",
  "updated": "2020-05-22T08:42:52.829Z",
  "id": "5ec7908c005df800101bc99b"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004123e81f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1092872223`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`