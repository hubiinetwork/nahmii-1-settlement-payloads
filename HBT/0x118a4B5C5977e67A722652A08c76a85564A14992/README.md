# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x118a4B5C5977e67A722652A08c76a85564A14992`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000000000000000000000000000000000004ed51ac7826767c7fcbc64f9700bceb982f2a5a49727c7823811f48b6903472f41086e0dc129efa08aa31f5f2917209ed9b982e3497ab0c6a277475d13ddf791ae79e03101a5813c15bef09ec6cede4d80eb65dd66831f76a334620ada57c5d557d3308a000000000000000000000000000000000000000000000000000000000000001b8f6cbb622ef6e2ea32d193162cd06e262867802a63dc44177a18825164db4b32c75d70a16620fd54e0735b0472226a369b416e22009a877f0076b14f3e51f8df75b86cd493280ee1467c450e074fdc4a5613e4aebf4a4ab5d7a25f4a9784ad05000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c6d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e136588f504ec000000000000000000000000000000000000000000000000002e1365d7de4e0f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4a84d4c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a5441324d5751795a6930325a546b354c545533596a63744f44426b4d6930334e445668597a55774e3255775a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000118a4b5c5977e67a722652a08c76a85564a14992000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x826767c7fcbc64f9700bceb982f2a5a49727c7823811f48b6903472f41086e0d",
      "signature": {
        "s": "0x01a5813c15bef09ec6cede4d80eb65dd66831f76a334620ada57c5d557d3308a",
        "r": "0xc129efa08aa31f5f2917209ed9b982e3497ab0c6a277475d13ddf791ae79e031",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f6cbb622ef6e2ea32d193162cd06e262867802a63dc44177a18825164db4b32",
      "signature": {
        "s": "0x75b86cd493280ee1467c450e074fdc4a5613e4aebf4a4ab5d7a25f4a9784ad05",
        "r": "0xc75d70a16620fd54e0735b0472226a369b416e22009a877f0076b14f3e51f8df",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322588871",
    "total": "1322588871"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322588871",
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
            "amount": "48494859465"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322588"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTA2MWQyZi02ZTk5LTU3YjctODBkMi03NDVhYzUwN2UwZmIifQ==",
    "nonce": 7277,
    "balances": {
      "current": "12969175739073772",
      "previous": "12969177062985231"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x118a4b5c5977e67a722652a08c76a85564a14992",
    "nonce": 22,
    "balances": {
      "current": "1322588871",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:36.034Z",
  "updated": "2020-05-22T08:55:36.114Z",
  "id": "5ec79388e5756b00111b88b1"
}
```
* *stageAmount*: `1322588871`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000000000000000000000000000000000004ed51ac7826767c7fcbc64f9700bceb982f2a5a49727c7823811f48b6903472f41086e0dc129efa08aa31f5f2917209ed9b982e3497ab0c6a277475d13ddf791ae79e03101a5813c15bef09ec6cede4d80eb65dd66831f76a334620ada57c5d557d3308a000000000000000000000000000000000000000000000000000000000000001b8f6cbb622ef6e2ea32d193162cd06e262867802a63dc44177a18825164db4b32c75d70a16620fd54e0735b0472226a369b416e22009a877f0076b14f3e51f8df75b86cd493280ee1467c450e074fdc4a5613e4aebf4a4ab5d7a25f4a9784ad05000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ad00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c6d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e136588f504ec000000000000000000000000000000000000000000000000002e1365d7de4e0f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000142e5c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4a84d4c9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a5441324d5751795a6930325a546b354c545533596a63744f44426b4d6930334e445668597a55774e3255775a6d496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000118a4b5c5977e67a722652a08c76a85564a14992000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x826767c7fcbc64f9700bceb982f2a5a49727c7823811f48b6903472f41086e0d",
      "signature": {
        "s": "0x01a5813c15bef09ec6cede4d80eb65dd66831f76a334620ada57c5d557d3308a",
        "r": "0xc129efa08aa31f5f2917209ed9b982e3497ab0c6a277475d13ddf791ae79e031",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f6cbb622ef6e2ea32d193162cd06e262867802a63dc44177a18825164db4b32",
      "signature": {
        "s": "0x75b86cd493280ee1467c450e074fdc4a5613e4aebf4a4ab5d7a25f4a9784ad05",
        "r": "0xc75d70a16620fd54e0735b0472226a369b416e22009a877f0076b14f3e51f8df",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1322588871",
    "total": "1322588871"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1322588871",
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
            "amount": "48494859465"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1322588"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmZTA2MWQyZi02ZTk5LTU3YjctODBkMi03NDVhYzUwN2UwZmIifQ==",
    "nonce": 7277,
    "balances": {
      "current": "12969175739073772",
      "previous": "12969177062985231"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x118a4b5c5977e67a722652a08c76a85564a14992",
    "nonce": 22,
    "balances": {
      "current": "1322588871",
      "previous": "0"
    }
  },
  "blockNumber": "10114733",
  "created": "2020-05-22T08:55:36.034Z",
  "updated": "2020-05-22T08:55:36.114Z",
  "id": "5ec79388e5756b00111b88b1"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000004ed51ac7000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1322588871`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`