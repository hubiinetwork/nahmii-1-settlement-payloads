# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc674B7f9ab1FC1590D1c0c01acDCD7cBD450780f`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000181bf02200000000000000000000000000000000000000000000000000000000181bf022000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000181bf02200000000000000000000000000000000000000000000000000000000181bf02260dd87447559ba33981c99008d3b1da882f2f7ab6cf30287129e4490183d49e7eb18c5eac6e606e373040044c1119e7e5548701a39b8fa51d8c23d4e77747c621864ec1c20be0b94bd0bfd058bbd8e4049c95ba955e3041d99f9f78906e2e3d0000000000000000000000000000000000000000000000000000000000000001b4f3fdee7039ed598cd1312aef92cce84a4bc29e7ad396440976877d82a99f43217b4f13206a88c23e40a0a3f62716f9bc7e1ec0135bf386730000fe17fa8446b5843aa846fe3a03aee2102f340a48943d09b2ce67111aff74d5a022b6ff4250e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bc200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14dd0ea61298000000000000000000000000000000000000000000000000002e14dd26c82ebe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000062c04000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aea7b316b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6d49304e6a41794d4330345a475a6c4c5455324d324974596d566d4d5330325a5451344d5749774f54597a4e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c674b7f9ab1fc1590d1c0c01acdcd7cbd450780f00000000000000000000000000000000000000000000000000000000181bf022000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60dd87447559ba33981c99008d3b1da882f2f7ab6cf30287129e4490183d49e7",
      "signature": {
        "s": "0x1864ec1c20be0b94bd0bfd058bbd8e4049c95ba955e3041d99f9f78906e2e3d0",
        "r": "0xeb18c5eac6e606e373040044c1119e7e5548701a39b8fa51d8c23d4e77747c62",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4f3fdee7039ed598cd1312aef92cce84a4bc29e7ad396440976877d82a99f432",
      "signature": {
        "s": "0x5843aa846fe3a03aee2102f340a48943d09b2ce67111aff74d5a022b6ff4250e",
        "r": "0x17b4f13206a88c23e40a0a3f62716f9bc7e1ec0135bf386730000fe17fa8446b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "404484130",
    "total": "404484130"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "404484130",
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
            "amount": "46883615083"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "404484"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZmI0NjAyMC04ZGZlLTU2M2ItYmVmMS02ZTQ4MWIwOTYzNjIifQ==",
    "nonce": 7106,
    "balances": {
      "current": "12970788594782872",
      "previous": "12970788999671486"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc674b7f9ab1fc1590d1c0c01acdcd7cbd450780f",
    "nonce": 22,
    "balances": {
      "current": "404484130",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:18.983Z",
  "updated": "2020-05-22T08:54:19.054Z",
  "id": "5ec7933ab0c6090011d5b216"
}
```
* *stageAmount*: `404484130`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000181bf022000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000181bf02200000000000000000000000000000000000000000000000000000000181bf02260dd87447559ba33981c99008d3b1da882f2f7ab6cf30287129e4490183d49e7eb18c5eac6e606e373040044c1119e7e5548701a39b8fa51d8c23d4e77747c621864ec1c20be0b94bd0bfd058bbd8e4049c95ba955e3041d99f9f78906e2e3d0000000000000000000000000000000000000000000000000000000000000001b4f3fdee7039ed598cd1312aef92cce84a4bc29e7ad396440976877d82a99f43217b4f13206a88c23e40a0a3f62716f9bc7e1ec0135bf386730000fe17fa8446b5843aa846fe3a03aee2102f340a48943d09b2ce67111aff74d5a022b6ff4250e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bc200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14dd0ea61298000000000000000000000000000000000000000000000000002e14dd26c82ebe00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000062c04000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000aea7b316b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6d49304e6a41794d4330345a475a6c4c5455324d324974596d566d4d5330325a5451344d5749774f54597a4e6a496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000c674b7f9ab1fc1590d1c0c01acdcd7cbd450780f00000000000000000000000000000000000000000000000000000000181bf022000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60dd87447559ba33981c99008d3b1da882f2f7ab6cf30287129e4490183d49e7",
      "signature": {
        "s": "0x1864ec1c20be0b94bd0bfd058bbd8e4049c95ba955e3041d99f9f78906e2e3d0",
        "r": "0xeb18c5eac6e606e373040044c1119e7e5548701a39b8fa51d8c23d4e77747c62",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x4f3fdee7039ed598cd1312aef92cce84a4bc29e7ad396440976877d82a99f432",
      "signature": {
        "s": "0x5843aa846fe3a03aee2102f340a48943d09b2ce67111aff74d5a022b6ff4250e",
        "r": "0x17b4f13206a88c23e40a0a3f62716f9bc7e1ec0135bf386730000fe17fa8446b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "404484130",
    "total": "404484130"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "404484130",
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
            "amount": "46883615083"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "404484"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiZmI0NjAyMC04ZGZlLTU2M2ItYmVmMS02ZTQ4MWIwOTYzNjIifQ==",
    "nonce": 7106,
    "balances": {
      "current": "12970788594782872",
      "previous": "12970788999671486"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc674b7f9ab1fc1590d1c0c01acdcd7cbd450780f",
    "nonce": 22,
    "balances": {
      "current": "404484130",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:18.983Z",
  "updated": "2020-05-22T08:54:19.054Z",
  "id": "5ec7933ab0c6090011d5b216"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000181bf022000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `404484130`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`