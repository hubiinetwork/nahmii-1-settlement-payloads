# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x73e5d2F260e42c42727dC059aC0dF6b59d31053B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000000000000000000000000000000000007e3dc29a5efd9db70b3e6eb844b56174512bc7ba2ac8e9c43456f3a3dd0c20eda6ea1afe285ecad72c3155756227cbad360908b75fcbe0a37f2de75bb5149bb680b67bcc569c12c0a1ff4ed614f3372417b14071ed1becaf888963a3ca293dade04359aa000000000000000000000000000000000000000000000000000000000000001bfa41e4fb322c34e1de384b77e722ac5f2bf66636036204db86eb7dafbdbef101be0975128945049226044010e1371d50c1e287f1d2c13342cce7060ac3cfdd5b5fa594ce3e5961668fafcfce10634f6d6c138f31f9e0a4ffa30d8c4e6bfa9718000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ea700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aec28a2cd69000000000000000000000000000000000000000000000000002e0aeca700e15b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000205158000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75530a03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d44566c595459304f433035596a55304c54566d4e544174595455304d793033596a6b794f444669596a4d344f574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000073e5d2f260e42c42727dc059ac0df6b59d31053b000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5efd9db70b3e6eb844b56174512bc7ba2ac8e9c43456f3a3dd0c20eda6ea1afe",
      "signature": {
        "s": "0x569c12c0a1ff4ed614f3372417b14071ed1becaf888963a3ca293dade04359aa",
        "r": "0x285ecad72c3155756227cbad360908b75fcbe0a37f2de75bb5149bb680b67bcc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa41e4fb322c34e1de384b77e722ac5f2bf66636036204db86eb7dafbdbef101",
      "signature": {
        "s": "0x5fa594ce3e5961668fafcfce10634f6d6c138f31f9e0a4ffa30d8c4e6bfa9718",
        "r": "0xbe0975128945049226044010e1371d50c1e287f1d2c13342cce7060ac3cfdd5b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2117976730",
    "total": "2117976730"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2117976730",
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
            "amount": "57802951171"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2117976"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMDVlYTY0OC05YjU0LTVmNTAtYTU0My03YjkyODFiYjM4OWMifQ==",
    "nonce": 7847,
    "balances": {
      "current": "12959858339007849",
      "previous": "12959860459102555"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73e5d2f260e42c42727dc059ac0df6b59d31053b",
    "nonce": 12,
    "balances": {
      "current": "2117976730",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:57.566Z",
  "updated": "2020-05-22T08:59:57.631Z",
  "id": "5ec7948de5756b00111b8966"
}
```
* *stageAmount*: `2117976730`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000000000000000000000000000000000007e3dc29a5efd9db70b3e6eb844b56174512bc7ba2ac8e9c43456f3a3dd0c20eda6ea1afe285ecad72c3155756227cbad360908b75fcbe0a37f2de75bb5149bb680b67bcc569c12c0a1ff4ed614f3372417b14071ed1becaf888963a3ca293dade04359aa000000000000000000000000000000000000000000000000000000000000001bfa41e4fb322c34e1de384b77e722ac5f2bf66636036204db86eb7dafbdbef101be0975128945049226044010e1371d50c1e287f1d2c13342cce7060ac3cfdd5b5fa594ce3e5961668fafcfce10634f6d6c138f31f9e0a4ffa30d8c4e6bfa9718000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56c200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001ea700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0aec28a2cd69000000000000000000000000000000000000000000000000002e0aeca700e15b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000205158000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d75530a03000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d44566c595459304f433035596a55304c54566d4e544174595455304d793033596a6b794f444669596a4d344f574d6966513d3d000000000000000000000000000000000000000000000000000000000000000c00000000000000000000000073e5d2f260e42c42727dc059ac0df6b59d31053b000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5efd9db70b3e6eb844b56174512bc7ba2ac8e9c43456f3a3dd0c20eda6ea1afe",
      "signature": {
        "s": "0x569c12c0a1ff4ed614f3372417b14071ed1becaf888963a3ca293dade04359aa",
        "r": "0x285ecad72c3155756227cbad360908b75fcbe0a37f2de75bb5149bb680b67bcc",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xfa41e4fb322c34e1de384b77e722ac5f2bf66636036204db86eb7dafbdbef101",
      "signature": {
        "s": "0x5fa594ce3e5961668fafcfce10634f6d6c138f31f9e0a4ffa30d8c4e6bfa9718",
        "r": "0xbe0975128945049226044010e1371d50c1e287f1d2c13342cce7060ac3cfdd5b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2117976730",
    "total": "2117976730"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2117976730",
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
            "amount": "57802951171"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2117976"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMDVlYTY0OC05YjU0LTVmNTAtYTU0My03YjkyODFiYjM4OWMifQ==",
    "nonce": 7847,
    "balances": {
      "current": "12959858339007849",
      "previous": "12959860459102555"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x73e5d2f260e42c42727dc059ac0df6b59d31053b",
    "nonce": 12,
    "balances": {
      "current": "2117976730",
      "previous": "0"
    }
  },
  "blockNumber": "10114754",
  "created": "2020-05-22T08:59:57.566Z",
  "updated": "2020-05-22T08:59:57.631Z",
  "id": "5ec7948de5756b00111b8966"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000007e3dc29a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2117976730`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`