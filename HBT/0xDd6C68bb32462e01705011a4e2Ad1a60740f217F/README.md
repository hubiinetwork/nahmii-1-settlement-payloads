# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000001068cb41000000000000000000000000000000000000000000000000000000001068cb410000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001068cb41000000000000000000000000000000000000000000000000000000001068cb410f7bbd3ed1e6f2e74d133c2efd831afe90e530403059f020aa3352e9d8fb61585f91e4fab4a631d1d23b4c8df48c828d9ac4d35365b66a51eb2b703aa07dd67e340cfa0cbd92ac9790e46c1d08663349d25895e6023857a16ec20de0151385de2000000000000000000000000000000000000000000000000000000000000001b7253d287d364e5765e07f1519ec85a537888ebc3fe3a14ed7c2fc6ac965abb614c422091b74de747a66e53b445ce4703a2d174695bb135da9739df922abb6159685ab595ce9c1a57fff8ea2f3e3ec41556db67e3e5ffd8b1faed910bb8b127eb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000155200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d644934d0f9000000000000000000000000000000000000000000000000002e1d655004bb7c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000433673000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bc220fd5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f544a6d4e4445354f53316b4e5759304c54566a4d474574596d4a6a4e69316d4d7a63334f474d774e7a6b344d7a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000001068cb410000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7bbd3ed1e6f2e74d133c2efd831afe90e530403059f020aa3352e9d8fb61585",
      "signature": {
        "s": "0x40cfa0cbd92ac9790e46c1d08663349d25895e6023857a16ec20de0151385de2",
        "r": "0xf91e4fab4a631d1d23b4c8df48c828d9ac4d35365b66a51eb2b703aa07dd67e3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7253d287d364e5765e07f1519ec85a537888ebc3fe3a14ed7c2fc6ac965abb61",
      "signature": {
        "s": "0x685ab595ce9c1a57fff8ea2f3e3ec41556db67e3e5ffd8b1faed910bb8b127eb",
        "r": "0x4c422091b74de747a66e53b445ce4703a2d174695bb135da9739df922abb6159",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4404851728",
    "total": "4404851728"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4404851728",
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
            "amount": "37516087253"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4404851"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOTJmNDE5OS1kNWY0LTVjMGEtYmJjNi1mMzc3OGMwNzk4MzgifQ==",
    "nonce": 5458,
    "balances": {
      "current": "12980165490823417",
      "previous": "12980169900079996"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "nonce": 22,
    "balances": {
      "current": "4404851728",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:15.092Z",
  "updated": "2020-05-22T08:41:15.244Z",
  "id": "5ec7902bb0c6090011d5afd8"
}
```
* *stageAmount*: `4404851728`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000001068cb410000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001068cb41000000000000000000000000000000000000000000000000000000001068cb410f7bbd3ed1e6f2e74d133c2efd831afe90e530403059f020aa3352e9d8fb61585f91e4fab4a631d1d23b4c8df48c828d9ac4d35365b66a51eb2b703aa07dd67e340cfa0cbd92ac9790e46c1d08663349d25895e6023857a16ec20de0151385de2000000000000000000000000000000000000000000000000000000000000001b7253d287d364e5765e07f1519ec85a537888ebc3fe3a14ed7c2fc6ac965abb614c422091b74de747a66e53b445ce4703a2d174695bb135da9739df922abb6159685ab595ce9c1a57fff8ea2f3e3ec41556db67e3e5ffd8b1faed910bb8b127eb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56670000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000155200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1d644934d0f9000000000000000000000000000000000000000000000000002e1d655004bb7c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000433673000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008bc220fd5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784f544a6d4e4445354f53316b4e5759304c54566a4d474574596d4a6a4e69316d4d7a63334f474d774e7a6b344d7a676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000001068cb410000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf7bbd3ed1e6f2e74d133c2efd831afe90e530403059f020aa3352e9d8fb61585",
      "signature": {
        "s": "0x40cfa0cbd92ac9790e46c1d08663349d25895e6023857a16ec20de0151385de2",
        "r": "0xf91e4fab4a631d1d23b4c8df48c828d9ac4d35365b66a51eb2b703aa07dd67e3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7253d287d364e5765e07f1519ec85a537888ebc3fe3a14ed7c2fc6ac965abb61",
      "signature": {
        "s": "0x685ab595ce9c1a57fff8ea2f3e3ec41556db67e3e5ffd8b1faed910bb8b127eb",
        "r": "0x4c422091b74de747a66e53b445ce4703a2d174695bb135da9739df922abb6159",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4404851728",
    "total": "4404851728"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4404851728",
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
            "amount": "37516087253"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "4404851"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxOTJmNDE5OS1kNWY0LTVjMGEtYmJjNi1mMzc3OGMwNzk4MzgifQ==",
    "nonce": 5458,
    "balances": {
      "current": "12980165490823417",
      "previous": "12980169900079996"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
    "nonce": 22,
    "balances": {
      "current": "4404851728",
      "previous": "0"
    }
  },
  "blockNumber": "10114663",
  "created": "2020-05-22T08:41:15.092Z",
  "updated": "2020-05-22T08:41:15.244Z",
  "id": "5ec7902bb0c6090011d5afd8"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000001068cb410000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4404851728`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`