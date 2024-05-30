# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5B78E950c6Fbd1384ea127ACAa41bb62A600F6d8`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000076cabac00000000000000000000000000000000000000000000000000000000076cabac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000076cabac00000000000000000000000000000000000000000000000000000000076cabac799e0cc3ad3beaa54273468a3123dd35386894c8d51fe8dac309d3a1cd3f8e3db8a2bdda49ba0d693348a507106e085a0bbf07d76b82ec5b7132d41a06c9aaeb445f1a5629a2410c3d0a130e372d15c9d15eaca585469efa74fc8c854c073624000000000000000000000000000000000000000000000000000000000000001be94a7c109582e13356b5ea34e18ff7d7ac386ae1ee8c1717458cd742852a1ff7641b71ac33107ba3dff4a42e540cd28cc5d01cdb2d8c9d4595c6a9e2d58b0f847f4133b116b348d76745337ccfda9feb0765120627c1f14ff128b02b93b36c05000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000186700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad461960c6c000000000000000000000000000000000000000000000000002e1ad469049eaa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001e692000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963e07d3e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a544930597a63774f433169597a41314c5456684f5467744f444133597930325a54686a596a426b5a4746684f44636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005b78e950c6fbd1384ea127acaa41bb62a600f6d800000000000000000000000000000000000000000000000000000000076cabac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x799e0cc3ad3beaa54273468a3123dd35386894c8d51fe8dac309d3a1cd3f8e3d",
      "signature": {
        "s": "0x445f1a5629a2410c3d0a130e372d15c9d15eaca585469efa74fc8c854c073624",
        "r": "0xb8a2bdda49ba0d693348a507106e085a0bbf07d76b82ec5b7132d41a06c9aaeb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe94a7c109582e13356b5ea34e18ff7d7ac386ae1ee8c1717458cd742852a1ff7",
      "signature": {
        "s": "0x7f4133b116b348d76745337ccfda9feb0765120627c1f14ff128b02b93b36c05",
        "r": "0x641b71ac33107ba3dff4a42e540cd28cc5d01cdb2d8c9d4595c6a9e2d58b0f84",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "124562348",
    "total": "124562348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "124562348",
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
            "amount": "40330362174"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "124562"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTI0YzcwOC1iYzA1LTVhOTgtODA3Yy02ZThjYjBkZGFhODcifQ==",
    "nonce": 6247,
    "balances": {
      "current": "12977348401302636",
      "previous": "12977348525989546"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5b78e950c6fbd1384ea127acaa41bb62a600f6d8",
    "nonce": 22,
    "balances": {
      "current": "124562348",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:37.857Z",
  "updated": "2020-05-22T08:47:37.936Z",
  "id": "5ec791a9005df800101bca5e"
}
```
* *stageAmount*: `124562348`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000076cabac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000076cabac00000000000000000000000000000000000000000000000000000000076cabac799e0cc3ad3beaa54273468a3123dd35386894c8d51fe8dac309d3a1cd3f8e3db8a2bdda49ba0d693348a507106e085a0bbf07d76b82ec5b7132d41a06c9aaeb445f1a5629a2410c3d0a130e372d15c9d15eaca585469efa74fc8c854c073624000000000000000000000000000000000000000000000000000000000000001be94a7c109582e13356b5ea34e18ff7d7ac386ae1ee8c1717458cd742852a1ff7641b71ac33107ba3dff4a42e540cd28cc5d01cdb2d8c9d4595c6a9e2d58b0f847f4133b116b348d76745337ccfda9feb0765120627c1f14ff128b02b93b36c05000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56880000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000186700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1ad461960c6c000000000000000000000000000000000000000000000000002e1ad469049eaa00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000001e692000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000963e07d3e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a544930597a63774f433169597a41314c5456684f5467744f444133597930325a54686a596a426b5a4746684f44636966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000005b78e950c6fbd1384ea127acaa41bb62a600f6d800000000000000000000000000000000000000000000000000000000076cabac000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x799e0cc3ad3beaa54273468a3123dd35386894c8d51fe8dac309d3a1cd3f8e3d",
      "signature": {
        "s": "0x445f1a5629a2410c3d0a130e372d15c9d15eaca585469efa74fc8c854c073624",
        "r": "0xb8a2bdda49ba0d693348a507106e085a0bbf07d76b82ec5b7132d41a06c9aaeb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe94a7c109582e13356b5ea34e18ff7d7ac386ae1ee8c1717458cd742852a1ff7",
      "signature": {
        "s": "0x7f4133b116b348d76745337ccfda9feb0765120627c1f14ff128b02b93b36c05",
        "r": "0x641b71ac33107ba3dff4a42e540cd28cc5d01cdb2d8c9d4595c6a9e2d58b0f84",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "124562348",
    "total": "124562348"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "124562348",
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
            "amount": "40330362174"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "124562"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTI0YzcwOC1iYzA1LTVhOTgtODA3Yy02ZThjYjBkZGFhODcifQ==",
    "nonce": 6247,
    "balances": {
      "current": "12977348401302636",
      "previous": "12977348525989546"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5b78e950c6fbd1384ea127acaa41bb62a600f6d8",
    "nonce": 22,
    "balances": {
      "current": "124562348",
      "previous": "0"
    }
  },
  "blockNumber": "10114696",
  "created": "2020-05-22T08:47:37.857Z",
  "updated": "2020-05-22T08:47:37.936Z",
  "id": "5ec791a9005df800101bca5e"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000076cabac000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `124562348`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`