# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xF520858Bb106906441Cb54b7D64D9a49E9C60B4b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000ae2203a93c143e548000000000000000000000000000000000000000000000000420e4f20cd98e8750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd98e8750000000000000000000000000000000000000000000000073d97b7069c57da74478c53315e89a08d3dae81d96421d4b6ea520f22f7da71afaa06d65fcaacfc90c6a13773ac383cb16a790c3a7e9ae0c4033d5aa93d72c01a9d49cb865c3d270625944d439a5cb615d7a877286e37e243f8559f55de69bb900475f94dce774627000000000000000000000000000000000000000000000000000000000000001b05ad9f09ade0d9bb4395314e77d84a9bcad1ff1f4f7518ff5cf80853c0bbdd931ae79fb06ac9d5e98910fe451cdea958b4a1cb33168d4651fdf32ee1dfe84c7e1f5a332519fd83beec3afb59d495cc1fb58a9dc235f804a27e56cba96e4bcf3b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b025000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9c52bfd285609f96ff000000000000000000000000000000000000000000004f9c94df0ab03285b4ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d357a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d805d785d993bd060f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933597a6b355a44597a4d5330784d324d314c5455344d3251745957466c4e79316a4e7a4e69597a51794d7a453059324d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f520858bb106906441cb54b7d64d9a49e9c60b4b00000000000000000000000000000000000000000000000ae2203a93c143e54800000000000000000000000000000000000000000000000aa011eb72f3aafcd300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x478c53315e89a08d3dae81d96421d4b6ea520f22f7da71afaa06d65fcaacfc90",
      "signature": {
        "s": "0x25944d439a5cb615d7a877286e37e243f8559f55de69bb900475f94dce774627",
        "r": "0xc6a13773ac383cb16a790c3a7e9ae0c4033d5aa93d72c01a9d49cb865c3d2706",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x05ad9f09ade0d9bb4395314e77d84a9bcad1ff1f4f7518ff5cf80853c0bbdd93",
      "signature": {
        "s": "0x1f5a332519fd83beec3afb59d495cc1fb58a9dc235f804a27e56cba96e4bcf3b",
        "r": "0x1ae79fb06ac9d5e98910fe451cdea958b4a1cb33168d4651fdf32ee1dfe84c7e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858484090997",
    "total": "133565425712784464500"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858484090997",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27596750086529204684303"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858484090"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3Yzk5ZDYzMS0xM2M1LTU4M2QtYWFlNy1jNzNiYzQyMzE0Y2MifQ==",
    "nonce": 110629,
    "balances": {
      "current": "375950606938102617315071",
      "previous": "375955371526789959890158"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf520858bb106906441cb54b7d64d9a49e9c60b4b",
    "nonce": 46,
    "balances": {
      "current": "200761528595199026504",
      "previous": "196001699736714935507"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:14.680Z",
  "updated": "2022-05-04T08:54:14.739Z",
  "id": "62723f367832e20011830bf5"
}
```
* *stageAmount*: `200761528595199026504`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000420e4f20cd98e8750000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000420e4f20cd98e8750000000000000000000000000000000000000000000000073d97b7069c57da74478c53315e89a08d3dae81d96421d4b6ea520f22f7da71afaa06d65fcaacfc90c6a13773ac383cb16a790c3a7e9ae0c4033d5aa93d72c01a9d49cb865c3d270625944d439a5cb615d7a877286e37e243f8559f55de69bb900475f94dce774627000000000000000000000000000000000000000000000000000000000000001b05ad9f09ade0d9bb4395314e77d84a9bcad1ff1f4f7518ff5cf80853c0bbdd931ae79fb06ac9d5e98910fe451cdea958b4a1cb33168d4651fdf32ee1dfe84c7e1f5a332519fd83beec3afb59d495cc1fb58a9dc235f804a27e56cba96e4bcf3b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b025000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9c52bfd285609f96ff000000000000000000000000000000000000000000004f9c94df0ab03285b4ee00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000010e90a044d357a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d805d785d993bd060f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694933597a6b355a44597a4d5330784d324d314c5455344d3251745957466c4e79316a4e7a4e69597a51794d7a453059324d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000f520858bb106906441cb54b7d64d9a49e9c60b4b00000000000000000000000000000000000000000000000ae2203a93c143e54800000000000000000000000000000000000000000000000aa011eb72f3aafcd300000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x478c53315e89a08d3dae81d96421d4b6ea520f22f7da71afaa06d65fcaacfc90",
      "signature": {
        "s": "0x25944d439a5cb615d7a877286e37e243f8559f55de69bb900475f94dce774627",
        "r": "0xc6a13773ac383cb16a790c3a7e9ae0c4033d5aa93d72c01a9d49cb865c3d2706",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x05ad9f09ade0d9bb4395314e77d84a9bcad1ff1f4f7518ff5cf80853c0bbdd93",
      "signature": {
        "s": "0x1f5a332519fd83beec3afb59d495cc1fb58a9dc235f804a27e56cba96e4bcf3b",
        "r": "0x1ae79fb06ac9d5e98910fe451cdea958b4a1cb33168d4651fdf32ee1dfe84c7e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4759828858484090997",
    "total": "133565425712784464500"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4759828858484090997",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27596750086529204684303"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4759828858484090"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3Yzk5ZDYzMS0xM2M1LTU4M2QtYWFlNy1jNzNiYzQyMzE0Y2MifQ==",
    "nonce": 110629,
    "balances": {
      "current": "375950606938102617315071",
      "previous": "375955371526789959890158"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf520858bb106906441cb54b7d64d9a49e9c60b4b",
    "nonce": 46,
    "balances": {
      "current": "200761528595199026504",
      "previous": "196001699736714935507"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:14.680Z",
  "updated": "2022-05-04T08:54:14.739Z",
  "id": "62723f367832e20011830bf5"
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
0x0f200f9b00000000000000000000000000000000000000000000000ae2203a93c143e5480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `200761528595199026504`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`