# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdF21692C890e26F2Ec0531e17540CB4DC472FdFe`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000c9d15d0000000000000000000000000000000000000000000000000000000000c9d15d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c9d15d0000000000000000000000000000000000000000000000000000000000c9d15d56b6eeb2f56b9318fd6e11e66baed0426ba9dc00be5026eb8b804dfbf89c645ae59b62114ef732cb993b82e7850822402c6035d818fa9b486456cfc9f1e9587837af218ce68ef908a1777c91920619bb9831a1c6d3e4376773ebec76744a7d04000000000000000000000000000000000000000000000000000000000000001b8686c0f34fcefd478d775819f3880303d943595efeaf615bef90e9f32421419c6f72c7f6fd24fb702b6c858d8300b97aa5c4124f57cf4b8db4f9aa829fbfbfef20c12bcd7f05f0bf23d62661dab7fa6f070c7945a2a92b08e45fd6d2dd8c5c16000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56970000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000199e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17c818f226ac000000000000000000000000000000000000000000000000002e17c819bc2bb300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2b6e13ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d474979595459354f4330775a544d7a4c5455354e445974595463354d7931685a6d51775a5455324d54426d4f44676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000df21692c890e26f2ec0531e17540cb4dc472fdfe0000000000000000000000000000000000000000000000000000000000c9d15d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x56b6eeb2f56b9318fd6e11e66baed0426ba9dc00be5026eb8b804dfbf89c645a",
      "signature": {
        "s": "0x37af218ce68ef908a1777c91920619bb9831a1c6d3e4376773ebec76744a7d04",
        "r": "0xe59b62114ef732cb993b82e7850822402c6035d818fa9b486456cfc9f1e95878",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8686c0f34fcefd478d775819f3880303d943595efeaf615bef90e9f32421419c",
      "signature": {
        "s": "0x20c12bcd7f05f0bf23d62661dab7fa6f070c7945a2a92b08e45fd6d2dd8c5c16",
        "r": "0x6f72c7f6fd24fb702b6c858d8300b97aa5c4124f57cf4b8db4f9aa829fbfbfef",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13226333",
    "total": "13226333"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226333",
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
            "amount": "43678307311"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13226"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMGIyYTY5OC0wZTMzLTU5NDYtYTc5My1hZmQwZTU2MTBmODgifQ==",
    "nonce": 6558,
    "balances": {
      "current": "12973997108111020",
      "previous": "12973997121350579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdf21692c890e26f2ec0531e17540cb4dc472fdfe",
    "nonce": 22,
    "balances": {
      "current": "13226333",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:08.986Z",
  "updated": "2020-05-22T08:50:10.070Z",
  "id": "5ec79240e5756b00111b87d0"
}
```
* *stageAmount*: `13226333`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000c9d15d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000c9d15d0000000000000000000000000000000000000000000000000000000000c9d15d56b6eeb2f56b9318fd6e11e66baed0426ba9dc00be5026eb8b804dfbf89c645ae59b62114ef732cb993b82e7850822402c6035d818fa9b486456cfc9f1e9587837af218ce68ef908a1777c91920619bb9831a1c6d3e4376773ebec76744a7d04000000000000000000000000000000000000000000000000000000000000001b8686c0f34fcefd478d775819f3880303d943595efeaf615bef90e9f32421419c6f72c7f6fd24fb702b6c858d8300b97aa5c4124f57cf4b8db4f9aa829fbfbfef20c12bcd7f05f0bf23d62661dab7fa6f070c7945a2a92b08e45fd6d2dd8c5c16000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56970000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000199e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e17c818f226ac000000000000000000000000000000000000000000000000002e17c819bc2bb300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000033aa000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a2b6e13ef000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d474979595459354f4330775a544d7a4c5455354e445974595463354d7931685a6d51775a5455324d54426d4f44676966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000df21692c890e26f2ec0531e17540cb4dc472fdfe0000000000000000000000000000000000000000000000000000000000c9d15d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x56b6eeb2f56b9318fd6e11e66baed0426ba9dc00be5026eb8b804dfbf89c645a",
      "signature": {
        "s": "0x37af218ce68ef908a1777c91920619bb9831a1c6d3e4376773ebec76744a7d04",
        "r": "0xe59b62114ef732cb993b82e7850822402c6035d818fa9b486456cfc9f1e95878",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8686c0f34fcefd478d775819f3880303d943595efeaf615bef90e9f32421419c",
      "signature": {
        "s": "0x20c12bcd7f05f0bf23d62661dab7fa6f070c7945a2a92b08e45fd6d2dd8c5c16",
        "r": "0x6f72c7f6fd24fb702b6c858d8300b97aa5c4124f57cf4b8db4f9aa829fbfbfef",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "13226333",
    "total": "13226333"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "13226333",
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
            "amount": "43678307311"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "13226"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMGIyYTY5OC0wZTMzLTU5NDYtYTc5My1hZmQwZTU2MTBmODgifQ==",
    "nonce": 6558,
    "balances": {
      "current": "12973997108111020",
      "previous": "12973997121350579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdf21692c890e26f2ec0531e17540cb4dc472fdfe",
    "nonce": 22,
    "balances": {
      "current": "13226333",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:08.986Z",
  "updated": "2020-05-22T08:50:10.070Z",
  "id": "5ec79240e5756b00111b87d0"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000c9d15d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `13226333`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`