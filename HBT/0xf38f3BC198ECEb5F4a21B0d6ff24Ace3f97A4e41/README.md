# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf38f3BC198ECEb5F4a21B0d6ff24Ace3f97A4e41`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000009cae5460c00000000000000000000000000000000000000000000000000000009cae5460c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae5460c00000000000000000000000000000000000000000000000000000009cae5460c787680eeec3236b9467fad033bc260864579c7aab0373e59d1f906f204e32594fac85f3e2c4efb26166360d8cf5f2a24399c8e820f27d05809b69637775010d16b9a7900c9761144904146f327141d387d3f801eb69252a498653b92596f36a4000000000000000000000000000000000000000000000000000000000000001c35211327e7f3d148f8b134f4571f964bef17803982005c70d89bf885a7a4e65e16f2b1a6185ab045f2f9415a9f111d22235ed8aee5326143b9b0edf6df9a8365079a5e7a0288c10ef79b571c4b77546c4c1842894eba65d9f3f5de66a452df26000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e144a051a6d79000000000000000000000000000000000000000000000000002e1453d281776d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b1015cd4c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6a4268597a41324d433079597a41314c5455345a54637459544a6a4d69316b4e574d314d6a4532597a426c4d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f38f3bc198eceb5f4a21b0d6ff24ace3f97a4e4100000000000000000000000000000000000000000000000000000009cae5460c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x787680eeec3236b9467fad033bc260864579c7aab0373e59d1f906f204e32594",
      "signature": {
        "s": "0x6b9a7900c9761144904146f327141d387d3f801eb69252a498653b92596f36a4",
        "r": "0xfac85f3e2c4efb26166360d8cf5f2a24399c8e820f27d05809b69637775010d1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x35211327e7f3d148f8b134f4571f964bef17803982005c70d89bf885a7a4e65e",
      "signature": {
        "s": "0x079a5e7a0288c10ef79b571c4b77546c4c1842894eba65d9f3f5de66a452df26",
        "r": "0x16f2b1a6185ab045f2f9415a9f111d22235ed8aee5326143b9b0edf6df9a8365",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "42058728972",
    "total": "42058728972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058728972",
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
            "amount": "47514504524"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058728"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NjBhYzA2MC0yYzA1LTU4ZTctYTJjMi1kNWM1MjE2YzBlMmMifQ==",
    "nonce": 7123,
    "balances": {
      "current": "12970157074443641",
      "previous": "12970199175231341"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf38f3bc198eceb5f4a21b0d6ff24ace3f97a4e41",
    "nonce": 22,
    "balances": {
      "current": "42058728972",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:23.197Z",
  "updated": "2020-05-22T08:54:23.277Z",
  "id": "5ec7933fe5756b00111b8880"
}
```
* *stageAmount*: `42058728972`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000009cae5460c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae5460c00000000000000000000000000000000000000000000000000000009cae5460c787680eeec3236b9467fad033bc260864579c7aab0373e59d1f906f204e32594fac85f3e2c4efb26166360d8cf5f2a24399c8e820f27d05809b69637775010d16b9a7900c9761144904146f327141d387d3f801eb69252a498653b92596f36a4000000000000000000000000000000000000000000000000000000000000001c35211327e7f3d148f8b134f4571f964bef17803982005c70d89bf885a7a4e65e16f2b1a6185ab045f2f9415a9f111d22235ed8aee5326143b9b0edf6df9a8365079a5e7a0288c10ef79b571c4b77546c4c1842894eba65d9f3f5de66a452df26000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd300000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e144a051a6d79000000000000000000000000000000000000000000000000002e1453d281776d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3e8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b1015cd4c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e6a4268597a41324d433079597a41314c5455345a54637459544a6a4d69316b4e574d314d6a4532597a426c4d6d4d6966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000f38f3bc198eceb5f4a21b0d6ff24ace3f97a4e4100000000000000000000000000000000000000000000000000000009cae5460c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x787680eeec3236b9467fad033bc260864579c7aab0373e59d1f906f204e32594",
      "signature": {
        "s": "0x6b9a7900c9761144904146f327141d387d3f801eb69252a498653b92596f36a4",
        "r": "0xfac85f3e2c4efb26166360d8cf5f2a24399c8e820f27d05809b69637775010d1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x35211327e7f3d148f8b134f4571f964bef17803982005c70d89bf885a7a4e65e",
      "signature": {
        "s": "0x079a5e7a0288c10ef79b571c4b77546c4c1842894eba65d9f3f5de66a452df26",
        "r": "0x16f2b1a6185ab045f2f9415a9f111d22235ed8aee5326143b9b0edf6df9a8365",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "42058728972",
    "total": "42058728972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058728972",
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
            "amount": "47514504524"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058728"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NjBhYzA2MC0yYzA1LTU4ZTctYTJjMi1kNWM1MjE2YzBlMmMifQ==",
    "nonce": 7123,
    "balances": {
      "current": "12970157074443641",
      "previous": "12970199175231341"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf38f3bc198eceb5f4a21b0d6ff24ace3f97a4e41",
    "nonce": 22,
    "balances": {
      "current": "42058728972",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:23.197Z",
  "updated": "2020-05-22T08:54:23.277Z",
  "id": "5ec7933fe5756b00111b8880"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000009cae5460c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `42058728972`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`