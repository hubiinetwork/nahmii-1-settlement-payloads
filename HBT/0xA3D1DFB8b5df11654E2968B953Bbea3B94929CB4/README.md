# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA3D1DFB8b5df11654E2968B953Bbea3B94929CB4`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000169f63a400000000000000000000000000000000000000000000000000000000169f63a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000169f63a400000000000000000000000000000000000000000000000000000000169f63a48610bc2323a052613460042e8e2b52127e628ce9c4af048c75339cc66569eb2e24edceb339ddb06064b1e4fb14c53274b5392743164e0d9de1ee0d61c1c243074804538e0aeb9de4a69efab930d106f3ee160cb88ef2c9a8008c5b79d01f966d000000000000000000000000000000000000000000000000000000000000001cf248b2809559b65afeaf05b1ee245aeab9a9969e8fbc68d25f4e24cdeed6c2ecd37e68ee395107d518cdb61815fafa0e267fb8eb45e1a032ac03d1db9be6ca87711f57b17a674926d51277ec3e97122d861621d2416afdafed419eedc7c6b5a4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0647b035e8000000000000000000000000000000000000000000000000002e0b065e55642400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005ca98000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ea4dd5e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596d4a695a6a63314d6930314e7a46694c545579593249744f546c6d595330304f474d324e444a6d5a5463354d54516966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000a3d1dfb8b5df11654e2968b953bbea3b94929cb400000000000000000000000000000000000000000000000000000000169f63a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8610bc2323a052613460042e8e2b52127e628ce9c4af048c75339cc66569eb2e",
      "signature": {
        "s": "0x4804538e0aeb9de4a69efab930d106f3ee160cb88ef2c9a8008c5b79d01f966d",
        "r": "0x24edceb339ddb06064b1e4fb14c53274b5392743164e0d9de1ee0d61c1c24307",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf248b2809559b65afeaf05b1ee245aeab9a9969e8fbc68d25f4e24cdeed6c2ec",
      "signature": {
        "s": "0x711f57b17a674926d51277ec3e97122d861621d2416afdafed419eedc7c6b5a4",
        "r": "0xd37e68ee395107d518cdb61815fafa0e267fb8eb45e1a032ac03d1db9be6ca87",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "379544484",
    "total": "379544484"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "379544484",
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
            "amount": "57690873182"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "379544"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYmJiZjc1Mi01NzFiLTUyY2ItOTlmYS00OGM2NDJmZTc5MTQifQ==",
    "nonce": 7730,
    "balances": {
      "current": "12959970529129960",
      "previous": "12959970909053988"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3d1dfb8b5df11654e2968b953bbea3b94929cb4",
    "nonce": 13,
    "balances": {
      "current": "379544484",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:05.870Z",
  "updated": "2020-05-22T08:59:05.954Z",
  "id": "5ec79459005df800101bcc58"
}
```
* *stageAmount*: `379544484`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000169f63a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000169f63a400000000000000000000000000000000000000000000000000000000169f63a48610bc2323a052613460042e8e2b52127e628ce9c4af048c75339cc66569eb2e24edceb339ddb06064b1e4fb14c53274b5392743164e0d9de1ee0d61c1c243074804538e0aeb9de4a69efab930d106f3ee160cb88ef2c9a8008c5b79d01f966d000000000000000000000000000000000000000000000000000000000000001cf248b2809559b65afeaf05b1ee245aeab9a9969e8fbc68d25f4e24cdeed6c2ecd37e68ee395107d518cdb61815fafa0e267fb8eb45e1a032ac03d1db9be6ca87711f57b17a674926d51277ec3e97122d861621d2416afdafed419eedc7c6b5a4000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e3200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0647b035e8000000000000000000000000000000000000000000000000002e0b065e55642400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000005ca98000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6ea4dd5e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596d4a695a6a63314d6930314e7a46694c545579593249744f546c6d595330304f474d324e444a6d5a5463354d54516966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000a3d1dfb8b5df11654e2968b953bbea3b94929cb400000000000000000000000000000000000000000000000000000000169f63a4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x8610bc2323a052613460042e8e2b52127e628ce9c4af048c75339cc66569eb2e",
      "signature": {
        "s": "0x4804538e0aeb9de4a69efab930d106f3ee160cb88ef2c9a8008c5b79d01f966d",
        "r": "0x24edceb339ddb06064b1e4fb14c53274b5392743164e0d9de1ee0d61c1c24307",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf248b2809559b65afeaf05b1ee245aeab9a9969e8fbc68d25f4e24cdeed6c2ec",
      "signature": {
        "s": "0x711f57b17a674926d51277ec3e97122d861621d2416afdafed419eedc7c6b5a4",
        "r": "0xd37e68ee395107d518cdb61815fafa0e267fb8eb45e1a032ac03d1db9be6ca87",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "379544484",
    "total": "379544484"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "379544484",
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
            "amount": "57690873182"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "379544"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYmJiZjc1Mi01NzFiLTUyY2ItOTlmYS00OGM2NDJmZTc5MTQifQ==",
    "nonce": 7730,
    "balances": {
      "current": "12959970529129960",
      "previous": "12959970909053988"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa3d1dfb8b5df11654e2968b953bbea3b94929cb4",
    "nonce": 13,
    "balances": {
      "current": "379544484",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:05.870Z",
  "updated": "2020-05-22T08:59:05.954Z",
  "id": "5ec79459005df800101bcc58"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000169f63a4000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `379544484`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`