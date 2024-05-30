# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe60933583d5B0544ACb11270939790d286d7877a`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000000000000000000000000000000000001cf8f2c3f94dd36b90b1c6fd40c53cf48f6c1908ee2f0e26f064525a789dacdaf86fbf50f901e6c653bac1f8d7d0b675be436cd2bc3d68dc111f26f32cb269e48ac45ee0630b188d821d0f1204e36b986b82e1a7ffbea5a15c9a648038919d1d6abdee5d000000000000000000000000000000000000000000000000000000000000001cf016e22ab03b9d799ab535f67a5e70f72242bf9a1a6ab7fa98def9c02b8b718102fa777d528332002783ce9cd622ff72fb7ef336bea701c4336b0d20d2f339b92ff4d56d042d47ee907946072a50a48c9f2c02e9cc55e1259ae653dfc4b05bea000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1247ab06e8000000000000000000000000000000000000000000000000002e1b1264ab646800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000076abd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009540bf232000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e6d4e6b5a54686a59533169597a646c4c5455775a4463744f574e694d6930334f4749354d324a6c596a59304e6d556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e60933583d5b0544acb11270939790d286d7877a000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf94dd36b90b1c6fd40c53cf48f6c1908ee2f0e26f064525a789dacdaf86fbf50",
      "signature": {
        "s": "0x630b188d821d0f1204e36b986b82e1a7ffbea5a15c9a648038919d1d6abdee5d",
        "r": "0xf901e6c653bac1f8d7d0b675be436cd2bc3d68dc111f26f32cb269e48ac45ee0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf016e22ab03b9d799ab535f67a5e70f72242bf9a1a6ab7fa98def9c02b8b7181",
      "signature": {
        "s": "0x2ff4d56d042d47ee907946072a50a48c9f2c02e9cc55e1259ae653dfc4b05bea",
        "r": "0x02fa777d528332002783ce9cd622ff72fb7ef336bea701c4336b0d20d2f339b9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "486077123",
    "total": "486077123"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "486077123",
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
            "amount": "40064774706"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "486077"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NmNkZThjYS1iYzdlLTUwZDctOWNiMi03OGI5M2JlYjY0NmUifQ==",
    "nonce": 6078,
    "balances": {
      "current": "12977614254442216",
      "previous": "12977614741005416"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe60933583d5b0544acb11270939790d286d7877a",
    "nonce": 22,
    "balances": {
      "current": "486077123",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:14.509Z",
  "updated": "2020-05-22T08:46:15.597Z",
  "id": "5ec79156e5756b00111b8739"
}
```
* *stageAmount*: `486077123`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000000000000000000000000000000000001cf8f2c3f94dd36b90b1c6fd40c53cf48f6c1908ee2f0e26f064525a789dacdaf86fbf50f901e6c653bac1f8d7d0b675be436cd2bc3d68dc111f26f32cb269e48ac45ee0630b188d821d0f1204e36b986b82e1a7ffbea5a15c9a648038919d1d6abdee5d000000000000000000000000000000000000000000000000000000000000001cf016e22ab03b9d799ab535f67a5e70f72242bf9a1a6ab7fa98def9c02b8b718102fa777d528332002783ce9cd622ff72fb7ef336bea701c4336b0d20d2f339b92ff4d56d042d47ee907946072a50a48c9f2c02e9cc55e1259ae653dfc4b05bea000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a567f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017be00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b1247ab06e8000000000000000000000000000000000000000000000000002e1b1264ab646800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000076abd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009540bf232000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e6d4e6b5a54686a59533169597a646c4c5455775a4463744f574e694d6930334f4749354d324a6c596a59304e6d556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e60933583d5b0544acb11270939790d286d7877a000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf94dd36b90b1c6fd40c53cf48f6c1908ee2f0e26f064525a789dacdaf86fbf50",
      "signature": {
        "s": "0x630b188d821d0f1204e36b986b82e1a7ffbea5a15c9a648038919d1d6abdee5d",
        "r": "0xf901e6c653bac1f8d7d0b675be436cd2bc3d68dc111f26f32cb269e48ac45ee0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf016e22ab03b9d799ab535f67a5e70f72242bf9a1a6ab7fa98def9c02b8b7181",
      "signature": {
        "s": "0x2ff4d56d042d47ee907946072a50a48c9f2c02e9cc55e1259ae653dfc4b05bea",
        "r": "0x02fa777d528332002783ce9cd622ff72fb7ef336bea701c4336b0d20d2f339b9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "486077123",
    "total": "486077123"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "486077123",
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
            "amount": "40064774706"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "486077"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NmNkZThjYS1iYzdlLTUwZDctOWNiMi03OGI5M2JlYjY0NmUifQ==",
    "nonce": 6078,
    "balances": {
      "current": "12977614254442216",
      "previous": "12977614741005416"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe60933583d5b0544acb11270939790d286d7877a",
    "nonce": 22,
    "balances": {
      "current": "486077123",
      "previous": "0"
    }
  },
  "blockNumber": "10114687",
  "created": "2020-05-22T08:46:14.509Z",
  "updated": "2020-05-22T08:46:15.597Z",
  "id": "5ec79156e5756b00111b8739"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001cf8f2c3000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `486077123`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`