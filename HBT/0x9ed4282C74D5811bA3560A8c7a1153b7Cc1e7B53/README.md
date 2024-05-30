# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9ed4282C74D5811bA3560A8c7a1153b7Cc1e7B53`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000004d49f500000000000000000000000000000000000000000000000000000000004d49f5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004d49f500000000000000000000000000000000000000000000000000000000004d49f56e68172f320a7de77534a72492af83c62087d6c321bfd288508892c1f22567bab6109c6ac0c94c26b7e758435ba7fd496633c08a9468bb56a39410870d652603571cec2242aa0a6081a0d5ea3baf7c14b55daf2de4db88a95f392fbbfc5fd629000000000000000000000000000000000000000000000000000000000000001b768276428c59be87860eae4d401908d74d99173c9e633292da53e5b92c12275394cdde883d885216c2ce5edeb2171fea6afc1f3de455cc6686ec0cc6bd89a99c4c99a3809b56ad776f6ae6accc3539819fa484c827ce47f9cd0ee4dfd6569c14000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d7b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b43b631281e000000000000000000000000000000000000000000000000002e0b43b67e85dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000013c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d5eeee72f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595455354e324a684d7930345a4755794c54566b59546b744f546b774d5330344d3245784f54557a4e6d4e6c4d44416966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009ed4282c74d5811ba3560a8c7a1153b7cc1e7b5300000000000000000000000000000000000000000000000000000000004d49f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e68172f320a7de77534a72492af83c62087d6c321bfd288508892c1f22567ba",
      "signature": {
        "s": "0x571cec2242aa0a6081a0d5ea3baf7c14b55daf2de4db88a95f392fbbfc5fd629",
        "r": "0xb6109c6ac0c94c26b7e758435ba7fd496633c08a9468bb56a39410870d652603",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x768276428c59be87860eae4d401908d74d99173c9e633292da53e5b92c122753",
      "signature": {
        "s": "0x4c99a3809b56ad776f6ae6accc3539819fa484c827ce47f9cd0ee4dfd6569c14",
        "r": "0x94cdde883d885216c2ce5edeb2171fea6afc1f3de455cc6686ec0cc6bd89a99c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5065205",
    "total": "5065205"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5065205",
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
            "amount": "57427289903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5065"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYTU5N2JhMy04ZGUyLTVkYTktOTkwMS04M2ExOTUzNmNlMDAifQ==",
    "nonce": 7547,
    "balances": {
      "current": "12960234376079390",
      "previous": "12960234381149660"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ed4282c74d5811ba3560a8c7a1153b7cc1e7b53",
    "nonce": 6,
    "balances": {
      "current": "5065205",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:32.784Z",
  "updated": "2020-05-22T08:57:32.976Z",
  "id": "5ec793fcb0c6090011d5b2ab"
}
```
* *stageAmount*: `5065205`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000004d49f5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000004d49f500000000000000000000000000000000000000000000000000000000004d49f56e68172f320a7de77534a72492af83c62087d6c321bfd288508892c1f22567bab6109c6ac0c94c26b7e758435ba7fd496633c08a9468bb56a39410870d652603571cec2242aa0a6081a0d5ea3baf7c14b55daf2de4db88a95f392fbbfc5fd629000000000000000000000000000000000000000000000000000000000000001b768276428c59be87860eae4d401908d74d99173c9e633292da53e5b92c12275394cdde883d885216c2ce5edeb2171fea6afc1f3de455cc6686ec0cc6bd89a99c4c99a3809b56ad776f6ae6accc3539819fa484c827ce47f9cd0ee4dfd6569c14000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d7b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b43b631281e000000000000000000000000000000000000000000000000002e0b43b67e85dc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000013c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d5eeee72f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b595455354e324a684d7930345a4755794c54566b59546b744f546b774d5330344d3245784f54557a4e6d4e6c4d44416966513d3d00000000000000000000000000000000000000000000000000000000000000060000000000000000000000009ed4282c74d5811ba3560a8c7a1153b7cc1e7b5300000000000000000000000000000000000000000000000000000000004d49f5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6e68172f320a7de77534a72492af83c62087d6c321bfd288508892c1f22567ba",
      "signature": {
        "s": "0x571cec2242aa0a6081a0d5ea3baf7c14b55daf2de4db88a95f392fbbfc5fd629",
        "r": "0xb6109c6ac0c94c26b7e758435ba7fd496633c08a9468bb56a39410870d652603",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x768276428c59be87860eae4d401908d74d99173c9e633292da53e5b92c122753",
      "signature": {
        "s": "0x4c99a3809b56ad776f6ae6accc3539819fa484c827ce47f9cd0ee4dfd6569c14",
        "r": "0x94cdde883d885216c2ce5edeb2171fea6afc1f3de455cc6686ec0cc6bd89a99c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5065205",
    "total": "5065205"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5065205",
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
            "amount": "57427289903"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "5065"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkYTU5N2JhMy04ZGUyLTVkYTktOTkwMS04M2ExOTUzNmNlMDAifQ==",
    "nonce": 7547,
    "balances": {
      "current": "12960234376079390",
      "previous": "12960234381149660"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9ed4282c74d5811ba3560a8c7a1153b7cc1e7b53",
    "nonce": 6,
    "balances": {
      "current": "5065205",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:32.784Z",
  "updated": "2020-05-22T08:57:32.976Z",
  "id": "5ec793fcb0c6090011d5b2ab"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000004d49f5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5065205`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`