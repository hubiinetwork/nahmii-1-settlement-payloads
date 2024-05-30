# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5aB9d116a53EF41063E3EaE26A7eBe736720E9bA`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000fa2cf00000000000000000000000000000000000000000000000000000000000fa2cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000fa2cf00000000000000000000000000000000000000000000000000000000000fa2cfb9fdd531d30fa93fe5c436d8054e93422efab21ac0f14e0a9ccd8552faedbb373942ee26b75f3a7da8f2891d5f954f9ffb45231b875515996a3c618a9edf25e4042cf665e775695d99c463e191c5a158359d78598325f0a4dbf5595c615a444e000000000000000000000000000000000000000000000000000000000000001c3040716b99a1de8b233dc7532726923a0dba6ac09e43714e1ed7ee8be1dd49417a5ef50d569223f4fc77520e8d02e86699f5923db03d122fa8aa03299ddd7fe65b0971bf6a50d58220bf463642eef64766c4d9813cc8811f78c4d8710eed6c7c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d6000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b6ddbdce973000000000000000000000000000000000000000000000000002e0b6ddbec904200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d542781c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e574d7a4f445a6c5a6931694d4441784c54566a597a41744f5745794f433168597a59325a6d59314e4749354f54516966513d3d00000000000000000000000000000000000000000000000000000000000000070000000000000000000000005ab9d116a53ef41063e3eae26a7ebe736720e9ba00000000000000000000000000000000000000000000000000000000000fa2cf000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb9fdd531d30fa93fe5c436d8054e93422efab21ac0f14e0a9ccd8552faedbb37",
      "signature": {
        "s": "0x042cf665e775695d99c463e191c5a158359d78598325f0a4dbf5595c615a444e",
        "r": "0x3942ee26b75f3a7da8f2891d5f954f9ffb45231b875515996a3c618a9edf25e4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3040716b99a1de8b233dc7532726923a0dba6ac09e43714e1ed7ee8be1dd4941",
      "signature": {
        "s": "0x5b0971bf6a50d58220bf463642eef64766c4d9813cc8811f78c4d8710eed6c7c",
        "r": "0x7a5ef50d569223f4fc77520e8d02e86699f5923db03d122fa8aa03299ddd7fe6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1024719",
    "total": "1024719"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1024719",
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
            "amount": "57246450116"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1024"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NWMzODZlZi1iMDAxLTVjYzAtOWEyOC1hYzY2ZmY1NGI5OTQifQ==",
    "nonce": 7520,
    "balances": {
      "current": "12960415396718963",
      "previous": "12960415397744706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5ab9d116a53ef41063e3eae26a7ebe736720e9ba",
    "nonce": 7,
    "balances": {
      "current": "1024719",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:22.657Z",
  "updated": "2020-05-22T08:57:22.735Z",
  "id": "5ec793f2b0c6090011d5b2a1"
}
```
* *stageAmount*: `1024719`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000fa2cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000fa2cf00000000000000000000000000000000000000000000000000000000000fa2cfb9fdd531d30fa93fe5c436d8054e93422efab21ac0f14e0a9ccd8552faedbb373942ee26b75f3a7da8f2891d5f954f9ffb45231b875515996a3c618a9edf25e4042cf665e775695d99c463e191c5a158359d78598325f0a4dbf5595c615a444e000000000000000000000000000000000000000000000000000000000000001c3040716b99a1de8b233dc7532726923a0dba6ac09e43714e1ed7ee8be1dd49417a5ef50d569223f4fc77520e8d02e86699f5923db03d122fa8aa03299ddd7fe65b0971bf6a50d58220bf463642eef64766c4d9813cc8811f78c4d8710eed6c7c000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56b600000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d6000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b6ddbdce973000000000000000000000000000000000000000000000000002e0b6ddbec904200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d542781c4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e574d7a4f445a6c5a6931694d4441784c54566a597a41744f5745794f433168597a59325a6d59314e4749354f54516966513d3d00000000000000000000000000000000000000000000000000000000000000070000000000000000000000005ab9d116a53ef41063e3eae26a7ebe736720e9ba00000000000000000000000000000000000000000000000000000000000fa2cf000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb9fdd531d30fa93fe5c436d8054e93422efab21ac0f14e0a9ccd8552faedbb37",
      "signature": {
        "s": "0x042cf665e775695d99c463e191c5a158359d78598325f0a4dbf5595c615a444e",
        "r": "0x3942ee26b75f3a7da8f2891d5f954f9ffb45231b875515996a3c618a9edf25e4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3040716b99a1de8b233dc7532726923a0dba6ac09e43714e1ed7ee8be1dd4941",
      "signature": {
        "s": "0x5b0971bf6a50d58220bf463642eef64766c4d9813cc8811f78c4d8710eed6c7c",
        "r": "0x7a5ef50d569223f4fc77520e8d02e86699f5923db03d122fa8aa03299ddd7fe6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1024719",
    "total": "1024719"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1024719",
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
            "amount": "57246450116"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1024"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NWMzODZlZi1iMDAxLTVjYzAtOWEyOC1hYzY2ZmY1NGI5OTQifQ==",
    "nonce": 7520,
    "balances": {
      "current": "12960415396718963",
      "previous": "12960415397744706"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5ab9d116a53ef41063e3eae26a7ebe736720e9ba",
    "nonce": 7,
    "balances": {
      "current": "1024719",
      "previous": "0"
    }
  },
  "blockNumber": "10114742",
  "created": "2020-05-22T08:57:22.657Z",
  "updated": "2020-05-22T08:57:22.735Z",
  "id": "5ec793f2b0c6090011d5b2a1"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000fa2cf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1024719`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`