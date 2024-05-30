# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x6EDCeD503398d0577586005830cB0Da247420073`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000276a907000000000000000000000000000000000000000000000000000000000276a9070000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000276a907000000000000000000000000000000000000000000000000000000000276a9070bbb5ffdb2a987125ebe6bceb16380099fcf5062d5a05e079e32b0d91a23f90ebbe0517343f618129afd39d6a3d452e06683f6852b9432fb2e3598f967e6d3e89211e32355f65c763ff85078f7e60b05dd82e57bb116bd2f5090dcbc216772cde000000000000000000000000000000000000000000000000000000000000001b4e2e67ff3d332b123735291cb5edf7c495d341899f30c0d32f3c64cfa52c6c49c724e3625c30c8cde6c928324b4dbb3fd8176815f2c96c6482f33cdf435acb7d65a293e9a389d710639c94c8c75d968af9f1320c896dd85867085bdea5bc9413000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c5200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1372d7aed10c000000000000000000000000000000000000000000000000002e1372ff2378ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a172f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b471d94b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5455354d546c6d4d433168595759314c54566b5a4759744f474979596930775a57566d4f5751355954566d5a54676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006edced503398d0577586005830cb0da24742007300000000000000000000000000000000000000000000000000000000276a9070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbbb5ffdb2a987125ebe6bceb16380099fcf5062d5a05e079e32b0d91a23f90eb",
      "signature": {
        "s": "0x211e32355f65c763ff85078f7e60b05dd82e57bb116bd2f5090dcbc216772cde",
        "r": "0xbe0517343f618129afd39d6a3d452e06683f6852b9432fb2e3598f967e6d3e89",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4e2e67ff3d332b123735291cb5edf7c495d341899f30c0d32f3c64cfa52c6c49",
      "signature": {
        "s": "0x65a293e9a389d710639c94c8c75d968af9f1320c896dd85867085bdea5bc9413",
        "r": "0xc724e3625c30c8cde6c928324b4dbb3fd8176815f2c96c6482f33cdf435acb7d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "661295216",
    "total": "661295216"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "661295216",
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
            "amount": "48437761204"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "661295"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OTU5MTlmMC1hYWY1LTVkZGYtOGIyYi0wZWVmOWQ5YTVmZTgifQ==",
    "nonce": 7250,
    "balances": {
      "current": "12969232894447884",
      "previous": "12969233556404395"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6edced503398d0577586005830cb0da247420073",
    "nonce": 22,
    "balances": {
      "current": "661295216",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:21.296Z",
  "updated": "2020-05-22T08:55:21.362Z",
  "id": "5ec79379005df800101bcbbb"
}
```
* *stageAmount*: `661295216`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000276a9070000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000276a907000000000000000000000000000000000000000000000000000000000276a9070bbb5ffdb2a987125ebe6bceb16380099fcf5062d5a05e079e32b0d91a23f90ebbe0517343f618129afd39d6a3d452e06683f6852b9432fb2e3598f967e6d3e89211e32355f65c763ff85078f7e60b05dd82e57bb116bd2f5090dcbc216772cde000000000000000000000000000000000000000000000000000000000000001b4e2e67ff3d332b123735291cb5edf7c495d341899f30c0d32f3c64cfa52c6c49c724e3625c30c8cde6c928324b4dbb3fd8176815f2c96c6482f33cdf435acb7d65a293e9a389d710639c94c8c75d968af9f1320c896dd85867085bdea5bc9413000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c5200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1372d7aed10c000000000000000000000000000000000000000000000000002e1372ff2378ab00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000a172f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b471d94b4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f5455354d546c6d4d433168595759314c54566b5a4759744f474979596930775a57566d4f5751355954566d5a54676966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000006edced503398d0577586005830cb0da24742007300000000000000000000000000000000000000000000000000000000276a9070000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xbbb5ffdb2a987125ebe6bceb16380099fcf5062d5a05e079e32b0d91a23f90eb",
      "signature": {
        "s": "0x211e32355f65c763ff85078f7e60b05dd82e57bb116bd2f5090dcbc216772cde",
        "r": "0xbe0517343f618129afd39d6a3d452e06683f6852b9432fb2e3598f967e6d3e89",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4e2e67ff3d332b123735291cb5edf7c495d341899f30c0d32f3c64cfa52c6c49",
      "signature": {
        "s": "0x65a293e9a389d710639c94c8c75d968af9f1320c896dd85867085bdea5bc9413",
        "r": "0xc724e3625c30c8cde6c928324b4dbb3fd8176815f2c96c6482f33cdf435acb7d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "661295216",
    "total": "661295216"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "661295216",
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
            "amount": "48437761204"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "661295"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2OTU5MTlmMC1hYWY1LTVkZGYtOGIyYi0wZWVmOWQ5YTVmZTgifQ==",
    "nonce": 7250,
    "balances": {
      "current": "12969232894447884",
      "previous": "12969233556404395"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x6edced503398d0577586005830cb0da247420073",
    "nonce": 22,
    "balances": {
      "current": "661295216",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:21.296Z",
  "updated": "2020-05-22T08:55:21.362Z",
  "id": "5ec79379005df800101bcbbb"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000276a9070000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `661295216`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`