# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x22A5B9035E254F84f0029E3DddeD8c137a60c052`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000000000000000000000000000000000000f622a317908908e38164a578de6ba40ff025191cb0d8bfb5379e4949a4b72f6c090fce6dbf3dab6e4115e5f0b5f1a8cb5a3aa2d1c0ba35830315cdde9deca40e03a465b18706f74b323ec1e195146482aa7e50dbcdb3e4033caff8d3ac7fa1f6e5c0e31000000000000000000000000000000000000000000000000000000000000001cbb68a01abaad60fcc783f9a79164a7a72988e3c1974e9ae968a575c11cc2c0065b80e11db7f9adf9b321a6c315fc2643fa0e0d21ad37c5894d52ec9b4d133f5e38d29f5284349d358074faa81aa38ddbdce7ae6a8662ada264b6331b427689f8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001df300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b12f1a42fc5000000000000000000000000000000000000000000000000002e0b13010a4a2100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003f02b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b67c11a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a446b774e4455784e5330775a6a51334c5455314f544d74596a45334d5330775a6a51355a446c6c596d517a5a47516966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000022a5b9035e254f84f0029e3ddded8c137a60c052000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7908908e38164a578de6ba40ff025191cb0d8bfb5379e4949a4b72f6c090fce6",
      "signature": {
        "s": "0x18706f74b323ec1e195146482aa7e50dbcdb3e4033caff8d3ac7fa1f6e5c0e31",
        "r": "0xdbf3dab6e4115e5f0b5f1a8cb5a3aa2d1c0ba35830315cdde9deca40e03a465b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbb68a01abaad60fcc783f9a79164a7a72988e3c1974e9ae968a575c11cc2c006",
      "signature": {
        "s": "0x38d29f5284349d358074faa81aa38ddbdce7ae6a8662ada264b6331b427689f8",
        "r": "0x5b80e11db7f9adf9b321a6c315fc2643fa0e0d21ad37c5894d52ec9b4d133f5e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "258091569",
    "total": "258091569"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "258091569",
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
            "amount": "57636536602"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "258091"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZDkwNDUxNS0wZjQ3LTU1OTMtYjE3MS0wZjQ5ZDllYmQzZGQifQ==",
    "nonce": 7667,
    "balances": {
      "current": "12960024920076229",
      "previous": "12960025178425889"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x22a5b9035e254f84f0029e3ddded8c137a60c052",
    "nonce": 11,
    "balances": {
      "current": "258091569",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:35.939Z",
  "updated": "2020-05-22T08:58:36.014Z",
  "id": "5ec7943bb0c6090011d5b2d6"
}
```
* *stageAmount*: `258091569`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000000000000000000000000000000000000f622a317908908e38164a578de6ba40ff025191cb0d8bfb5379e4949a4b72f6c090fce6dbf3dab6e4115e5f0b5f1a8cb5a3aa2d1c0ba35830315cdde9deca40e03a465b18706f74b323ec1e195146482aa7e50dbcdb3e4033caff8d3ac7fa1f6e5c0e31000000000000000000000000000000000000000000000000000000000000001cbb68a01abaad60fcc783f9a79164a7a72988e3c1974e9ae968a575c11cc2c0065b80e11db7f9adf9b321a6c315fc2643fa0e0d21ad37c5894d52ec9b4d133f5e38d29f5284349d358074faa81aa38ddbdce7ae6a8662ada264b6331b427689f8000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ba00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001df300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b12f1a42fc5000000000000000000000000000000000000000000000000002e0b13010a4a2100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000003f02b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6b67c11a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a446b774e4455784e5330775a6a51334c5455314f544d74596a45334d5330775a6a51355a446c6c596d517a5a47516966513d3d000000000000000000000000000000000000000000000000000000000000000b00000000000000000000000022a5b9035e254f84f0029e3ddded8c137a60c052000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7908908e38164a578de6ba40ff025191cb0d8bfb5379e4949a4b72f6c090fce6",
      "signature": {
        "s": "0x18706f74b323ec1e195146482aa7e50dbcdb3e4033caff8d3ac7fa1f6e5c0e31",
        "r": "0xdbf3dab6e4115e5f0b5f1a8cb5a3aa2d1c0ba35830315cdde9deca40e03a465b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xbb68a01abaad60fcc783f9a79164a7a72988e3c1974e9ae968a575c11cc2c006",
      "signature": {
        "s": "0x38d29f5284349d358074faa81aa38ddbdce7ae6a8662ada264b6331b427689f8",
        "r": "0x5b80e11db7f9adf9b321a6c315fc2643fa0e0d21ad37c5894d52ec9b4d133f5e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "258091569",
    "total": "258091569"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "258091569",
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
            "amount": "57636536602"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "258091"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZDkwNDUxNS0wZjQ3LTU1OTMtYjE3MS0wZjQ5ZDllYmQzZGQifQ==",
    "nonce": 7667,
    "balances": {
      "current": "12960024920076229",
      "previous": "12960025178425889"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x22a5b9035e254f84f0029e3ddded8c137a60c052",
    "nonce": 11,
    "balances": {
      "current": "258091569",
      "previous": "0"
    }
  },
  "blockNumber": "10114746",
  "created": "2020-05-22T08:58:35.939Z",
  "updated": "2020-05-22T08:58:36.014Z",
  "id": "5ec7943bb0c6090011d5b2d6"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000f622a31000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `258091569`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`