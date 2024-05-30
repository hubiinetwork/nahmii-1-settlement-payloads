# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x42D5d74dAC1f4F2EEa1DC90F4221F7D0Bc710Fe8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000e25f6b11ce5a353d800000000000000000000000000000000000000000000000055df66ddd81171320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000055df66ddd811713200000000000000000000000000000000000000000000000969aba122316bf2d3c4dda71a2e20f0fdd1efd1aa2f8fefff8385be9cb24adb3fd0a2a5016ab2de778953c0d0be710cbea69e67ebd0c32c7fa4245bf75d311107abbd7185302aa04b2c3df9da350523506f9f6be4c3f9dfcb12df7f523d9b7e7f3d5a8ab7a4450a8a000000000000000000000000000000000000000000000000000000000000001b165b30816243978b0650d752462f19851dd242ba0e5cbbcd9af694c7cdc150c009c4ff0ad4713def8c5949f6f6da83b9afa42448b535e968fa6c08a9a242ea3928f8059b097377e1e987774100d52aa97d604102b28c0be8171e1550c35df024000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b20f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000498287d28dd6fa1d9793000000000000000000000000000000000000000000004982ddc7f0750af9cdbf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000015fbc038cac4fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d99542eaae87d21ee20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f47526d4f546334596931694e7a4d334c5456694e44597459545a684d433078595459784f44453459574d344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000042d5d74dac1f4f2eea1dc90f4221f7d0bc710fe800000000000000000000000000000000000000000000000e25f6b11ce5a353d800000000000000000000000000000000000000000000000dd0174a3f0d91e2a600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4dda71a2e20f0fdd1efd1aa2f8fefff8385be9cb24adb3fd0a2a5016ab2de77",
      "signature": {
        "s": "0x2c3df9da350523506f9f6be4c3f9dfcb12df7f523d9b7e7f3d5a8ab7a4450a8a",
        "r": "0x8953c0d0be710cbea69e67ebd0c32c7fa4245bf75d311107abbd7185302aa04b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x165b30816243978b0650d752462f19851dd242ba0e5cbbcd9af694c7cdc150c0",
      "signature": {
        "s": "0x28f8059b097377e1e987774100d52aa97d604102b28c0be8171e1550c35df024",
        "r": "0x09c4ff0ad4713def8c5949f6f6da83b9afa42448b535e968fa6c08a9a242ea39",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6187777516029178162",
    "total": "173635053426616038099"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6187777516029178162",
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
            "amount": "27625531295238636838626"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6187777516029178"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOGRmOTc4Yi1iNzM3LTViNDYtYTZhMC0xYTYxODE4YWM4MjcifQ==",
    "nonce": 111119,
    "balances": {
      "current": "347140617019961030580115",
      "previous": "347146810985254575787455"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42d5d74dac1f4f2eea1dc90f4221f7d0bc710fe8",
    "nonce": 46,
    "balances": {
      "current": "260989985593277764568",
      "previous": "254802208077248586406"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:39.278Z",
  "updated": "2022-05-04T08:56:39.370Z",
  "id": "62723fc77832e20011830c96"
}
```
* *stageAmount*: `260989985593277764568`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000055df66ddd81171320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000055df66ddd811713200000000000000000000000000000000000000000000000969aba122316bf2d3c4dda71a2e20f0fdd1efd1aa2f8fefff8385be9cb24adb3fd0a2a5016ab2de778953c0d0be710cbea69e67ebd0c32c7fa4245bf75d311107abbd7185302aa04b2c3df9da350523506f9f6be4c3f9dfcb12df7f523d9b7e7f3d5a8ab7a4450a8a000000000000000000000000000000000000000000000000000000000000001b165b30816243978b0650d752462f19851dd242ba0e5cbbcd9af694c7cdc150c009c4ff0ad4713def8c5949f6f6da83b9afa42448b535e968fa6c08a9a242ea3928f8059b097377e1e987774100d52aa97d604102b28c0be8171e1550c35df024000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b20f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000498287d28dd6fa1d9793000000000000000000000000000000000000000000004982ddc7f0750af9cdbf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000015fbc038cac4fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d99542eaae87d21ee20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4f47526d4f546334596931694e7a4d334c5456694e44597459545a684d433078595459784f44453459574d344d6a636966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000042d5d74dac1f4f2eea1dc90f4221f7d0bc710fe800000000000000000000000000000000000000000000000e25f6b11ce5a353d800000000000000000000000000000000000000000000000dd0174a3f0d91e2a600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4dda71a2e20f0fdd1efd1aa2f8fefff8385be9cb24adb3fd0a2a5016ab2de77",
      "signature": {
        "s": "0x2c3df9da350523506f9f6be4c3f9dfcb12df7f523d9b7e7f3d5a8ab7a4450a8a",
        "r": "0x8953c0d0be710cbea69e67ebd0c32c7fa4245bf75d311107abbd7185302aa04b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x165b30816243978b0650d752462f19851dd242ba0e5cbbcd9af694c7cdc150c0",
      "signature": {
        "s": "0x28f8059b097377e1e987774100d52aa97d604102b28c0be8171e1550c35df024",
        "r": "0x09c4ff0ad4713def8c5949f6f6da83b9afa42448b535e968fa6c08a9a242ea39",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6187777516029178162",
    "total": "173635053426616038099"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6187777516029178162",
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
            "amount": "27625531295238636838626"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6187777516029178"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzOGRmOTc4Yi1iNzM3LTViNDYtYTZhMC0xYTYxODE4YWM4MjcifQ==",
    "nonce": 111119,
    "balances": {
      "current": "347140617019961030580115",
      "previous": "347146810985254575787455"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x42d5d74dac1f4f2eea1dc90f4221f7d0bc710fe8",
    "nonce": 46,
    "balances": {
      "current": "260989985593277764568",
      "previous": "254802208077248586406"
    }
  },
  "blockNumber": "14709974",
  "created": "2022-05-04T08:56:39.278Z",
  "updated": "2022-05-04T08:56:39.370Z",
  "id": "62723fc77832e20011830c96"
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
0x0f200f9b00000000000000000000000000000000000000000000000e25f6b11ce5a353d80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `260989985593277764568`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`