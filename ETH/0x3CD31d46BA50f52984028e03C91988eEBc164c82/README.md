# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3CD31d46BA50f52984028e03C91988eEBc164c82`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000003220000000000000000000000000000000000000000000000000000000000000322000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003220000000000000000000000000000000000000000000000000000000000000322700f42f159286d75f2523fce3e0e10508c7c39a4cd4daf180a8712be0773e3112c1ada058323658bae4fb5e8b84a3cae81af58c94c991f3156db8a6e1c8ac19a13baabb44b6b59bbbadb89a12700bf5b88d0b8607389e2008444e8622443c236000000000000000000000000000000000000000000000000000000000000001c1f78ab8154beef6847ea526054ec6e501c668a3bbe9d41512d675de6d41dd5227995771d0169f8bc62351b71d624cbdfb10186509a4fed161c0efcd814089f9a2042b0553510a04f09ee3d3dcb1970ab74c156cd540d404225f267611baec845000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ee00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5d24ac000000000000000000000000000000000000000000000000002386f2bc5d27cf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c7800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6a63344d6d5a694d79316c4f4445334c545577597a41744f574d794d6930304d4745775a57466d4d324e684d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003cd31d46ba50f52984028e03c91988eebc164c820000000000000000000000000000000000000000000000000000000000000322000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x700f42f159286d75f2523fce3e0e10508c7c39a4cd4daf180a8712be0773e311",
      "signature": {
        "s": "0x13baabb44b6b59bbbadb89a12700bf5b88d0b8607389e2008444e8622443c236",
        "r": "0x2c1ada058323658bae4fb5e8b84a3cae81af58c94c991f3156db8a6e1c8ac19a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1f78ab8154beef6847ea526054ec6e501c668a3bbe9d41512d675de6d41dd522",
      "signature": {
        "s": "0x2042b0553510a04f09ee3d3dcb1970ab74c156cd540d404225f267611baec845",
        "r": "0x7995771d0169f8bc62351b71d624cbdfb10186509a4fed161c0efcd814089f9a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "802",
    "total": "802"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "802",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "797816"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Zjc4MmZiMy1lODE3LTUwYzAtOWMyMi00MGEwZWFmM2NhMDMifQ==",
    "nonce": 2286,
    "balances": {
      "current": "10000001285301420",
      "previous": "10000001285302223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3cd31d46ba50f52984028e03c91988eebc164c82",
    "nonce": 8,
    "balances": {
      "current": "802",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:32.973Z",
  "updated": "2020-05-22T08:15:33.044Z",
  "id": "5ec78a24b0c6090011d5abc6"
}
```
* *stageAmount*: `802`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000322000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000003220000000000000000000000000000000000000000000000000000000000000322700f42f159286d75f2523fce3e0e10508c7c39a4cd4daf180a8712be0773e3112c1ada058323658bae4fb5e8b84a3cae81af58c94c991f3156db8a6e1c8ac19a13baabb44b6b59bbbadb89a12700bf5b88d0b8607389e2008444e8622443c236000000000000000000000000000000000000000000000000000000000000001c1f78ab8154beef6847ea526054ec6e501c668a3bbe9d41512d675de6d41dd5227995771d0169f8bc62351b71d624cbdfb10186509a4fed161c0efcd814089f9a2042b0553510a04f09ee3d3dcb1970ab74c156cd540d404225f267611baec845000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008ee00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc5d24ac000000000000000000000000000000000000000000000000002386f2bc5d27cf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2c7800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a6a63344d6d5a694d79316c4f4445334c545577597a41744f574d794d6930304d4745775a57466d4d324e684d444d6966513d3d00000000000000000000000000000000000000000000000000000000000000080000000000000000000000003cd31d46ba50f52984028e03c91988eebc164c820000000000000000000000000000000000000000000000000000000000000322000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x700f42f159286d75f2523fce3e0e10508c7c39a4cd4daf180a8712be0773e311",
      "signature": {
        "s": "0x13baabb44b6b59bbbadb89a12700bf5b88d0b8607389e2008444e8622443c236",
        "r": "0x2c1ada058323658bae4fb5e8b84a3cae81af58c94c991f3156db8a6e1c8ac19a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1f78ab8154beef6847ea526054ec6e501c668a3bbe9d41512d675de6d41dd522",
      "signature": {
        "s": "0x2042b0553510a04f09ee3d3dcb1970ab74c156cd540d404225f267611baec845",
        "r": "0x7995771d0169f8bc62351b71d624cbdfb10186509a4fed161c0efcd814089f9a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "802",
    "total": "802"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "802",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "797816"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4Zjc4MmZiMy1lODE3LTUwYzAtOWMyMi00MGEwZWFmM2NhMDMifQ==",
    "nonce": 2286,
    "balances": {
      "current": "10000001285301420",
      "previous": "10000001285302223"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3cd31d46ba50f52984028e03c91988eebc164c82",
    "nonce": 8,
    "balances": {
      "current": "802",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:32.973Z",
  "updated": "2020-05-22T08:15:33.044Z",
  "id": "5ec78a24b0c6090011d5abc6"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000003220000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `802`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``