# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3e83A1E4Afcc89e6B915D706A6B6FBb3e9774c12`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000988bc61d4d58affb7207f27723b852e0c5b7998d0f14840860164dc49a87a6d01737fd2f6bcc5fd275a9a41d504cce424ddd329ce3c99f7bcadc5c50584ed2fb10d10144405376009d9ba0644b374e63fa8fefae504dd51fd431f85a329394630000000000000000000000000000000000000000000000000000000000000001ce2dde677af4130999208a3f8b2bf4e564f14fc2c78a1a172f838ca9229f5b93c62d7d5153461fbd7d787f92c8a151868889babb148ef7cf4676fc79b199428e91c4aabe31f79a1db4ad0fba96854c8aa4ee0cf8c2856c29d354cd31432a00ecf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005ae00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c68373c7000000000000000000000000000000000000000000000000002386f2c68373d100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000994f900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c595756694e4464694e4330334d7a4d344c54557a4e6d5974595459344d5330784f5467354e4449794d546c6d596d556966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003e83a1e4afcc89e6b915d706a6b6fbb3e9774c120000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x88bc61d4d58affb7207f27723b852e0c5b7998d0f14840860164dc49a87a6d01",
      "signature": {
        "s": "0x0d10144405376009d9ba0644b374e63fa8fefae504dd51fd431f85a329394630",
        "r": "0x737fd2f6bcc5fd275a9a41d504cce424ddd329ce3c99f7bcadc5c50584ed2fb1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe2dde677af4130999208a3f8b2bf4e564f14fc2c78a1a172f838ca9229f5b93c",
      "signature": {
        "s": "0x1c4aabe31f79a1db4ad0fba96854c8aa4ee0cf8c2856c29d354cd31432a00ecf",
        "r": "0x62d7d5153461fbd7d787f92c8a151868889babb148ef7cf4676fc79b199428e9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9",
    "total": "9"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "627961"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYWViNDdiNC03MzM4LTUzNmYtYTY4MS0xOTg5NDIyMTlmYmUifQ==",
    "nonce": 1454,
    "balances": {
      "current": "10000001455584199",
      "previous": "10000001455584209"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3e83a1e4afcc89e6b915d706a6b6fbb3e9774c12",
    "nonce": 8,
    "balances": {
      "current": "9",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:39.437Z",
  "updated": "2020-05-22T08:09:39.507Z",
  "id": "5ec788c3005df800101bc40f"
}
```
* *stageAmount*: `9`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000988bc61d4d58affb7207f27723b852e0c5b7998d0f14840860164dc49a87a6d01737fd2f6bcc5fd275a9a41d504cce424ddd329ce3c99f7bcadc5c50584ed2fb10d10144405376009d9ba0644b374e63fa8fefae504dd51fd431f85a329394630000000000000000000000000000000000000000000000000000000000000001ce2dde677af4130999208a3f8b2bf4e564f14fc2c78a1a172f838ca9229f5b93c62d7d5153461fbd7d787f92c8a151868889babb148ef7cf4676fc79b199428e91c4aabe31f79a1db4ad0fba96854c8aa4ee0cf8c2856c29d354cd31432a00ecf000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55e1000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000005ae00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c68373c7000000000000000000000000000000000000000000000000002386f2c68373d100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000994f900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c595756694e4464694e4330334d7a4d344c54557a4e6d5974595459344d5330784f5467354e4449794d546c6d596d556966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003e83a1e4afcc89e6b915d706a6b6fbb3e9774c120000000000000000000000000000000000000000000000000000000000000009000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x88bc61d4d58affb7207f27723b852e0c5b7998d0f14840860164dc49a87a6d01",
      "signature": {
        "s": "0x0d10144405376009d9ba0644b374e63fa8fefae504dd51fd431f85a329394630",
        "r": "0x737fd2f6bcc5fd275a9a41d504cce424ddd329ce3c99f7bcadc5c50584ed2fb1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe2dde677af4130999208a3f8b2bf4e564f14fc2c78a1a172f838ca9229f5b93c",
      "signature": {
        "s": "0x1c4aabe31f79a1db4ad0fba96854c8aa4ee0cf8c2856c29d354cd31432a00ecf",
        "r": "0x62d7d5153461fbd7d787f92c8a151868889babb148ef7cf4676fc79b199428e9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "9",
    "total": "9"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "627961"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlYWViNDdiNC03MzM4LTUzNmYtYTY4MS0xOTg5NDIyMTlmYmUifQ==",
    "nonce": 1454,
    "balances": {
      "current": "10000001455584199",
      "previous": "10000001455584209"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3e83a1e4afcc89e6b915d706a6b6fbb3e9774c12",
    "nonce": 8,
    "balances": {
      "current": "9",
      "previous": "0"
    }
  },
  "blockNumber": "10114529",
  "created": "2020-05-22T08:09:39.437Z",
  "updated": "2020-05-22T08:09:39.507Z",
  "id": "5ec788c3005df800101bc40f"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `9`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``