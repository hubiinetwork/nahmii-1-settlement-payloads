# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa43D2dE181edf0602D1Db046814dFB92EC786960`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000ead9402b00000000000000000000000000000000000000000000000000000000ead9402b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ead9402b00000000000000000000000000000000000000000000000000000000ead9402b51e5349046082b0513e65a0170c18f781499d95c276713c9d5ba592863131b78e20c60c3523086248c56d8fa1c11f50baf66bfebcee946f0314f2274d1705dda695376ff213ec1db58d3573348c475ec24946451adf43b01e4f114585464e6f5000000000000000000000000000000000000000000000000000000000000001ce3d47d110e018f658d0275452f604a687fc1c9a4c39363290f0c8a180ba2a819e180d2ace6b7b6ce16c260f792309dbcacb0e3fd37508bc9f9fe5c9fbab452db297cb82b65344976fd68364aff85e93557a39c8b4105e3eb7f23907899b2fe10000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001afe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c97e4b041f000000000000000000000000000000000000000000000000002e15ca6960635400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003c1f0a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aae0398df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e445179596a41794d53316c4d54517a4c5455774d5745744f44426c596930304e54466d596a6c6a59325179597a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000a43d2de181edf0602d1db046814dfb92ec78696000000000000000000000000000000000000000000000000000000000ead9402b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x51e5349046082b0513e65a0170c18f781499d95c276713c9d5ba592863131b78",
      "signature": {
        "s": "0x695376ff213ec1db58d3573348c475ec24946451adf43b01e4f114585464e6f5",
        "r": "0xe20c60c3523086248c56d8fa1c11f50baf66bfebcee946f0314f2274d1705dda",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe3d47d110e018f658d0275452f604a687fc1c9a4c39363290f0c8a180ba2a819",
      "signature": {
        "s": "0x297cb82b65344976fd68364aff85e93557a39c8b4105e3eb7f23907899b2fe10",
        "r": "0xe180d2ace6b7b6ce16c260f792309dbcacb0e3fd37508bc9f9fe5c9fbab452db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3940106283",
    "total": "3940106283"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3940106283",
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
            "amount": "45869144287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3940106"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNDQyYjAyMS1lMTQzLTUwMWEtODBlYi00NTFmYjljY2QyYzMifQ==",
    "nonce": 6910,
    "balances": {
      "current": "12971804080145439",
      "previous": "12971808024191828"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d2de181edf0602d1db046814dfb92ec786960",
    "nonce": 12,
    "balances": {
      "current": "3940106283",
      "previous": "0"
    }
  },
  "blockNumber": "10114721",
  "created": "2020-05-22T08:52:34.477Z",
  "updated": "2020-05-22T08:52:34.545Z",
  "id": "5ec792d2005df800101bcb43"
}
```
* *stageAmount*: `3940106283`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000ead9402b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000ead9402b00000000000000000000000000000000000000000000000000000000ead9402b51e5349046082b0513e65a0170c18f781499d95c276713c9d5ba592863131b78e20c60c3523086248c56d8fa1c11f50baf66bfebcee946f0314f2274d1705dda695376ff213ec1db58d3573348c475ec24946451adf43b01e4f114585464e6f5000000000000000000000000000000000000000000000000000000000000001ce3d47d110e018f658d0275452f604a687fc1c9a4c39363290f0c8a180ba2a819e180d2ace6b7b6ce16c260f792309dbcacb0e3fd37508bc9f9fe5c9fbab452db297cb82b65344976fd68364aff85e93557a39c8b4105e3eb7f23907899b2fe10000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56a100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001afe00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e15c97e4b041f000000000000000000000000000000000000000000000000002e15ca6960635400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000003c1f0a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aae0398df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4e445179596a41794d53316c4d54517a4c5455774d5745744f44426c596930304e54466d596a6c6a59325179597a4d6966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000a43d2de181edf0602d1db046814dfb92ec78696000000000000000000000000000000000000000000000000000000000ead9402b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x51e5349046082b0513e65a0170c18f781499d95c276713c9d5ba592863131b78",
      "signature": {
        "s": "0x695376ff213ec1db58d3573348c475ec24946451adf43b01e4f114585464e6f5",
        "r": "0xe20c60c3523086248c56d8fa1c11f50baf66bfebcee946f0314f2274d1705dda",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe3d47d110e018f658d0275452f604a687fc1c9a4c39363290f0c8a180ba2a819",
      "signature": {
        "s": "0x297cb82b65344976fd68364aff85e93557a39c8b4105e3eb7f23907899b2fe10",
        "r": "0xe180d2ace6b7b6ce16c260f792309dbcacb0e3fd37508bc9f9fe5c9fbab452db",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3940106283",
    "total": "3940106283"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3940106283",
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
            "amount": "45869144287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3940106"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJlNDQyYjAyMS1lMTQzLTUwMWEtODBlYi00NTFmYjljY2QyYzMifQ==",
    "nonce": 6910,
    "balances": {
      "current": "12971804080145439",
      "previous": "12971808024191828"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa43d2de181edf0602d1db046814dfb92ec786960",
    "nonce": 12,
    "balances": {
      "current": "3940106283",
      "previous": "0"
    }
  },
  "blockNumber": "10114721",
  "created": "2020-05-22T08:52:34.477Z",
  "updated": "2020-05-22T08:52:34.545Z",
  "id": "5ec792d2005df800101bcb43"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000ead9402b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3940106283`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`