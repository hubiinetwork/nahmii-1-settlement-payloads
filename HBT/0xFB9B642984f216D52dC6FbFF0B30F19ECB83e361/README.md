# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xFB9B642984f216D52dC6FbFF0B30F19ECB83e361`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000ac9d1a5800000000000000000000000000000000000000000000000000000000ac9d1a58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ac9d1a5800000000000000000000000000000000000000000000000000000000ac9d1a585c9dbb9c58a1020609700c63b036ff5d6004db298450db3cf2992e06d3d0a86b918db2dec0cb626fce1750c8cd7d39c67f30a121edbd256140a72e807600be3c63f37755996bc3964c3aa6ebb5c7216a2e3977fd9ffefcef1a397e0767b9ae57000000000000000000000000000000000000000000000000000000000000001bce7af2ff9225b4fa252240a48ce5035ca0fcb26ac891806b949b884bf3b7d42803e7de3f682541111a030085c465b91bfa354415cc20ca618c49d093ff6bca8f5a4bff2f1195ded9b997226ca039fac54b996ce3b600d328f8f9fd170816f5ed000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ba300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1536c3fc5bb5000000000000000000000000000000000000000000000000002e153770c5a67600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002c3069000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad389f0b3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f4463304d4449334d53316a4e4449774c5455774f444974596a67354e79307a5a5745325a546730595455304e44636966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000fb9b642984f216d52dc6fbff0b30f19ecb83e36100000000000000000000000000000000000000000000000000000000ac9d1a58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c9dbb9c58a1020609700c63b036ff5d6004db298450db3cf2992e06d3d0a86b",
      "signature": {
        "s": "0x63f37755996bc3964c3aa6ebb5c7216a2e3977fd9ffefcef1a397e0767b9ae57",
        "r": "0x918db2dec0cb626fce1750c8cd7d39c67f30a121edbd256140a72e807600be3c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xce7af2ff9225b4fa252240a48ce5035ca0fcb26ac891806b949b884bf3b7d428",
      "signature": {
        "s": "0x5a4bff2f1195ded9b997226ca039fac54b996ce3b600d328f8f9fd170816f5ed",
        "r": "0x03e7de3f682541111a030085c465b91bfa354415cc20ca618c49d093ff6bca8f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2895977048",
    "total": "2895977048"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2895977048",
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
            "amount": "46498705587"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2895977"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ODc0MDI3MS1jNDIwLTUwODItYjg5Ny0zZWE2ZTg0YTU0NDcifQ==",
    "nonce": 7075,
    "balances": {
      "current": "12971173889203125",
      "previous": "12971176788076150"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb9b642984f216d52dc6fbff0b30f19ecb83e361",
    "nonce": 14,
    "balances": {
      "current": "2895977048",
      "previous": "0"
    }
  },
  "blockNumber": "10114729",
  "created": "2020-05-22T08:53:58.908Z",
  "updated": "2020-05-22T08:53:59.991Z",
  "id": "5ec79326b0c6090011d5b20c"
}
```
* *stageAmount*: `2895977048`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000ac9d1a58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ac9d1a5800000000000000000000000000000000000000000000000000000000ac9d1a585c9dbb9c58a1020609700c63b036ff5d6004db298450db3cf2992e06d3d0a86b918db2dec0cb626fce1750c8cd7d39c67f30a121edbd256140a72e807600be3c63f37755996bc3964c3aa6ebb5c7216a2e3977fd9ffefcef1a397e0767b9ae57000000000000000000000000000000000000000000000000000000000000001bce7af2ff9225b4fa252240a48ce5035ca0fcb26ac891806b949b884bf3b7d42803e7de3f682541111a030085c465b91bfa354415cc20ca618c49d093ff6bca8f5a4bff2f1195ded9b997226ca039fac54b996ce3b600d328f8f9fd170816f5ed000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a900000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ba300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1536c3fc5bb5000000000000000000000000000000000000000000000000002e153770c5a67600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002c3069000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000ad389f0b3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f4463304d4449334d53316a4e4449774c5455774f444974596a67354e79307a5a5745325a546730595455304e44636966513d3d000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000fb9b642984f216d52dc6fbff0b30f19ecb83e36100000000000000000000000000000000000000000000000000000000ac9d1a58000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5c9dbb9c58a1020609700c63b036ff5d6004db298450db3cf2992e06d3d0a86b",
      "signature": {
        "s": "0x63f37755996bc3964c3aa6ebb5c7216a2e3977fd9ffefcef1a397e0767b9ae57",
        "r": "0x918db2dec0cb626fce1750c8cd7d39c67f30a121edbd256140a72e807600be3c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xce7af2ff9225b4fa252240a48ce5035ca0fcb26ac891806b949b884bf3b7d428",
      "signature": {
        "s": "0x5a4bff2f1195ded9b997226ca039fac54b996ce3b600d328f8f9fd170816f5ed",
        "r": "0x03e7de3f682541111a030085c465b91bfa354415cc20ca618c49d093ff6bca8f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2895977048",
    "total": "2895977048"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2895977048",
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
            "amount": "46498705587"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2895977"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ODc0MDI3MS1jNDIwLTUwODItYjg5Ny0zZWE2ZTg0YTU0NDcifQ==",
    "nonce": 7075,
    "balances": {
      "current": "12971173889203125",
      "previous": "12971176788076150"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfb9b642984f216d52dc6fbff0b30f19ecb83e361",
    "nonce": 14,
    "balances": {
      "current": "2895977048",
      "previous": "0"
    }
  },
  "blockNumber": "10114729",
  "created": "2020-05-22T08:53:58.908Z",
  "updated": "2020-05-22T08:53:59.991Z",
  "id": "5ec79326b0c6090011d5b20c"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000ac9d1a58000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2895977048`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`