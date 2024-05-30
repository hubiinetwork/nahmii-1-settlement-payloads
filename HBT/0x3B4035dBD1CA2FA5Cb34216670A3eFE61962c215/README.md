# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3B4035dBD1CA2FA5Cb34216670A3eFE61962c215`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000a58c821b00000000000000000000000000000000000000000000000000000000a58c821b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a58c821b00000000000000000000000000000000000000000000000000000000a58c821b91d71d5a85aae33ca107c7e9e06417c4dac027bf89866d42152b377e6c3656d11d4555b836fb1b2dc977739073b92e92e93c15b566c31e10ef90cfe914cce68a349eaf4efee598799a9022d4c9985822c474dc26995761099a09550f4b00a6ab000000000000000000000000000000000000000000000000000000000000001ce757fc54624612abe9c924602fddc68f9cc5ab0d3389cb20c00cf06f682a2f861fc1b3eae6a957e0779892c480b9ac2bc1f20e546fef8d769487ec4e6b4d477f471acfd85a0f931a6b0f98944916c6200aa74d84ea6b24a3bb11ee28eac877fa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c0c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13af0a2b422c000000000000000000000000000000000000000000000000002e13afafe225af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002a6168000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b37b87027000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a646b4e7a5a6c5a69316b596a55794c5455314e4459744f44426a5a4330304e7a5a6a4d6d526c4f54673059544d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003b4035dbd1ca2fa5cb34216670a3efe61962c21500000000000000000000000000000000000000000000000000000000a58c821b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91d71d5a85aae33ca107c7e9e06417c4dac027bf89866d42152b377e6c3656d1",
      "signature": {
        "s": "0x349eaf4efee598799a9022d4c9985822c474dc26995761099a09550f4b00a6ab",
        "r": "0x1d4555b836fb1b2dc977739073b92e92e93c15b566c31e10ef90cfe914cce68a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe757fc54624612abe9c924602fddc68f9cc5ab0d3389cb20c00cf06f682a2f86",
      "signature": {
        "s": "0x471acfd85a0f931a6b0f98944916c6200aa74d84ea6b24a3bb11ee28eac877fa",
        "r": "0x1fc1b3eae6a957e0779892c480b9ac2bc1f20e546fef8d769487ec4e6b4d477f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2777448987",
    "total": "2777448987"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2777448987",
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
            "amount": "48179474471"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2777448"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzdkNzZlZi1kYjUyLTU1NDYtODBjZC00NzZjMmRlOTg0YTMifQ==",
    "nonce": 7180,
    "balances": {
      "current": "12969491439501868",
      "previous": "12969494219728303"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3b4035dbd1ca2fa5cb34216670a3efe61962c215",
    "nonce": 22,
    "balances": {
      "current": "2777448987",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:46.796Z",
  "updated": "2020-05-22T08:54:46.866Z",
  "id": "5ec79356e5756b00111b8895"
}
```
* *stageAmount*: `2777448987`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000a58c821b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000a58c821b00000000000000000000000000000000000000000000000000000000a58c821b91d71d5a85aae33ca107c7e9e06417c4dac027bf89866d42152b377e6c3656d11d4555b836fb1b2dc977739073b92e92e93c15b566c31e10ef90cfe914cce68a349eaf4efee598799a9022d4c9985822c474dc26995761099a09550f4b00a6ab000000000000000000000000000000000000000000000000000000000000001ce757fc54624612abe9c924602fddc68f9cc5ab0d3389cb20c00cf06f682a2f861fc1b3eae6a957e0779892c480b9ac2bc1f20e546fef8d769487ec4e6b4d477f471acfd85a0f931a6b0f98944916c6200aa74d84ea6b24a3bb11ee28eac877fa000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ac00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c0c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13af0a2b422c000000000000000000000000000000000000000000000000002e13afafe225af00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000002a6168000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b37b87027000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d7a646b4e7a5a6c5a69316b596a55794c5455314e4459744f44426a5a4330304e7a5a6a4d6d526c4f54673059544d6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000003b4035dbd1ca2fa5cb34216670a3efe61962c21500000000000000000000000000000000000000000000000000000000a58c821b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x91d71d5a85aae33ca107c7e9e06417c4dac027bf89866d42152b377e6c3656d1",
      "signature": {
        "s": "0x349eaf4efee598799a9022d4c9985822c474dc26995761099a09550f4b00a6ab",
        "r": "0x1d4555b836fb1b2dc977739073b92e92e93c15b566c31e10ef90cfe914cce68a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe757fc54624612abe9c924602fddc68f9cc5ab0d3389cb20c00cf06f682a2f86",
      "signature": {
        "s": "0x471acfd85a0f931a6b0f98944916c6200aa74d84ea6b24a3bb11ee28eac877fa",
        "r": "0x1fc1b3eae6a957e0779892c480b9ac2bc1f20e546fef8d769487ec4e6b4d477f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2777448987",
    "total": "2777448987"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2777448987",
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
            "amount": "48179474471"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "2777448"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI2MzdkNzZlZi1kYjUyLTU1NDYtODBjZC00NzZjMmRlOTg0YTMifQ==",
    "nonce": 7180,
    "balances": {
      "current": "12969491439501868",
      "previous": "12969494219728303"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3b4035dbd1ca2fa5cb34216670a3efe61962c215",
    "nonce": 22,
    "balances": {
      "current": "2777448987",
      "previous": "0"
    }
  },
  "blockNumber": "10114732",
  "created": "2020-05-22T08:54:46.796Z",
  "updated": "2020-05-22T08:54:46.866Z",
  "id": "5ec79356e5756b00111b8895"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000a58c821b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2777448987`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`