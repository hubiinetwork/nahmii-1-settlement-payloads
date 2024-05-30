# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdB24ee94Ea3Db3df4C52c4613e555aa8FE83cb83`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000009f6324b0000000000000000000000000000000000000000000000000000000009f6324b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000009f6324b0000000000000000000000000000000000000000000000000000000009f6324b6f58482fbc31374b8381d85b813eb4d41aa4e6cdda7e3967684e22e421b7887ad36d9a433b74281778caba84e80835257a4088c720f066b3e557dd6de0c7ea975c368c37a1e7383b2a26d984338b3cb05a20ff791ba6fc3e921a3ade68f04af2000000000000000000000000000000000000000000000000000000000000001b95c58a22bcbac167cc49f61b514e4f9e2c632c93e1e3a9476228f715b9fb07203142cf059c92d99e42a824dae5f8ce3f5047422a9ff924cc09464ba75d14d8162a18e3727ff8fdd12998d0345d49b508e49ab70891a122527be1a1c905b6b4e2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e1100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0a5d5a8aac000000000000000000000000000000000000000000000000002e0b0a675349d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000028cd9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6d997127000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954597a596a67355953316b5a6d4e684c5456694e5451745954686d4e53316a595749304e7a45794f4749344e44556966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000db24ee94ea3db3df4c52c4613e555aa8fe83cb830000000000000000000000000000000000000000000000000000000009f6324b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f58482fbc31374b8381d85b813eb4d41aa4e6cdda7e3967684e22e421b7887a",
      "signature": {
        "s": "0x5c368c37a1e7383b2a26d984338b3cb05a20ff791ba6fc3e921a3ade68f04af2",
        "r": "0xd36d9a433b74281778caba84e80835257a4088c720f066b3e557dd6de0c7ea97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x95c58a22bcbac167cc49f61b514e4f9e2c632c93e1e3a9476228f715b9fb0720",
      "signature": {
        "s": "0x2a18e3727ff8fdd12998d0345d49b508e49ab70891a122527be1a1c905b6b4e2",
        "r": "0x3142cf059c92d99e42a824dae5f8ce3f5047422a9ff924cc09464ba75d14d816",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "167129675",
    "total": "167129675"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "167129675",
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
            "amount": "57673347367"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "167129"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYTYzYjg5YS1kZmNhLTViNTQtYThmNS1jYWI0NzEyOGI4NDUifQ==",
    "nonce": 7697,
    "balances": {
      "current": "12959988072483500",
      "previous": "12959988239780304"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdb24ee94ea3db3df4c52c4613e555aa8fe83cb83",
    "nonce": 5,
    "balances": {
      "current": "167129675",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:58:47.834Z",
  "updated": "2020-05-22T08:58:47.899Z",
  "id": "5ec79447b0c6090011d5b2e1"
}
```
* *stageAmount*: `167129675`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000009f6324b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000009f6324b0000000000000000000000000000000000000000000000000000000009f6324b6f58482fbc31374b8381d85b813eb4d41aa4e6cdda7e3967684e22e421b7887ad36d9a433b74281778caba84e80835257a4088c720f066b3e557dd6de0c7ea975c368c37a1e7383b2a26d984338b3cb05a20ff791ba6fc3e921a3ade68f04af2000000000000000000000000000000000000000000000000000000000000001b95c58a22bcbac167cc49f61b514e4f9e2c632c93e1e3a9476228f715b9fb07203142cf059c92d99e42a824dae5f8ce3f5047422a9ff924cc09464ba75d14d8162a18e3727ff8fdd12998d0345d49b508e49ab70891a122527be1a1c905b6b4e2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e1100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b0a5d5a8aac000000000000000000000000000000000000000000000000002e0b0a675349d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000028cd9000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6d997127000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695954597a596a67355953316b5a6d4e684c5456694e5451745954686d4e53316a595749304e7a45794f4749344e44556966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000db24ee94ea3db3df4c52c4613e555aa8fe83cb830000000000000000000000000000000000000000000000000000000009f6324b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6f58482fbc31374b8381d85b813eb4d41aa4e6cdda7e3967684e22e421b7887a",
      "signature": {
        "s": "0x5c368c37a1e7383b2a26d984338b3cb05a20ff791ba6fc3e921a3ade68f04af2",
        "r": "0xd36d9a433b74281778caba84e80835257a4088c720f066b3e557dd6de0c7ea97",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x95c58a22bcbac167cc49f61b514e4f9e2c632c93e1e3a9476228f715b9fb0720",
      "signature": {
        "s": "0x2a18e3727ff8fdd12998d0345d49b508e49ab70891a122527be1a1c905b6b4e2",
        "r": "0x3142cf059c92d99e42a824dae5f8ce3f5047422a9ff924cc09464ba75d14d816",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "167129675",
    "total": "167129675"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "167129675",
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
            "amount": "57673347367"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "167129"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYTYzYjg5YS1kZmNhLTViNTQtYThmNS1jYWI0NzEyOGI4NDUifQ==",
    "nonce": 7697,
    "balances": {
      "current": "12959988072483500",
      "previous": "12959988239780304"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdb24ee94ea3db3df4c52c4613e555aa8fe83cb83",
    "nonce": 5,
    "balances": {
      "current": "167129675",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:58:47.834Z",
  "updated": "2020-05-22T08:58:47.899Z",
  "id": "5ec79447b0c6090011d5b2e1"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000009f6324b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `167129675`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`