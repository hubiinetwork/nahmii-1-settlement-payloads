# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9752FaFe07226A458Ca3E64dEed7EB8834710135`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000011196d3a0000000000000000000000000000000000000000000000000000000011196d3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000011196d3a0000000000000000000000000000000000000000000000000000000011196d3ac15c140555f1af0b7f7c91682a35b81b7b1b3a52df9b319d202fb53eebad671c7e3718bb05d0838a63df32ef6bdb2c3802a096db5a78c9c4b6c64efcc7d33d4f72341446c923665fb0bc0929687a7aec01c909ef04dc567faf3403d28fd7a3a9000000000000000000000000000000000000000000000000000000000000001c6c972f8e7dd40727c7f01ad065fe0ff07bc42dc68bef636e5cb2b532247da055899fa0c17a9b45dffe1e1700a61a4f30e48949fed52836753fb8468c6c7ccd477943b4f04e71fdd3944b3bc2adf86f110542fdc4c4fd0d403df5b2847dca704b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001db000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21e23b4eef000000000000000000000000000000000000000000000000002e0b21f3591cc800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004609f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6795a349000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d475933596a42684d53316d4e5751774c54566a4f5751744f4445784f43316c4f54497759325135597a597a4f57596966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000009752fafe07226a458ca3e64deed7eb88347101350000000000000000000000000000000000000000000000000000000011196d3a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc15c140555f1af0b7f7c91682a35b81b7b1b3a52df9b319d202fb53eebad671c",
      "signature": {
        "s": "0x72341446c923665fb0bc0929687a7aec01c909ef04dc567faf3403d28fd7a3a9",
        "r": "0x7e3718bb05d0838a63df32ef6bdb2c3802a096db5a78c9c4b6c64efcc7d33d4f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c972f8e7dd40727c7f01ad065fe0ff07bc42dc68bef636e5cb2b532247da055",
      "signature": {
        "s": "0x7943b4f04e71fdd3944b3bc2adf86f110542fdc4c4fd0d403df5b2847dca704b",
        "r": "0x899fa0c17a9b45dffe1e1700a61a4f30e48949fed52836753fb8468c6c7ccd47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "286879034",
    "total": "286879034"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "286879034",
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
            "amount": "57572434761"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "286879"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMGY3YjBhMS1mNWQwLTVjOWQtODExOC1lOTIwY2Q5YzYzOWYifQ==",
    "nonce": 7600,
    "balances": {
      "current": "12960089086054127",
      "previous": "12960089373220040"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9752fafe07226a458ca3e64deed7eb8834710135",
    "nonce": 9,
    "balances": {
      "current": "286879034",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:55.884Z",
  "updated": "2020-05-22T08:57:56.028Z",
  "id": "5ec79413005df800101bcc27"
}
```
* *stageAmount*: `286879034`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000011196d3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000011196d3a0000000000000000000000000000000000000000000000000000000011196d3ac15c140555f1af0b7f7c91682a35b81b7b1b3a52df9b319d202fb53eebad671c7e3718bb05d0838a63df32ef6bdb2c3802a096db5a78c9c4b6c64efcc7d33d4f72341446c923665fb0bc0929687a7aec01c909ef04dc567faf3403d28fd7a3a9000000000000000000000000000000000000000000000000000000000000001c6c972f8e7dd40727c7f01ad065fe0ff07bc42dc68bef636e5cb2b532247da055899fa0c17a9b45dffe1e1700a61a4f30e48949fed52836753fb8468c6c7ccd477943b4f04e71fdd3944b3bc2adf86f110542fdc4c4fd0d403df5b2847dca704b000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001db000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b21e23b4eef000000000000000000000000000000000000000000000000002e0b21f3591cc800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000004609f000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6795a349000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694d475933596a42684d53316d4e5751774c54566a4f5751744f4445784f43316c4f54497759325135597a597a4f57596966513d3d00000000000000000000000000000000000000000000000000000000000000090000000000000000000000009752fafe07226a458ca3e64deed7eb88347101350000000000000000000000000000000000000000000000000000000011196d3a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc15c140555f1af0b7f7c91682a35b81b7b1b3a52df9b319d202fb53eebad671c",
      "signature": {
        "s": "0x72341446c923665fb0bc0929687a7aec01c909ef04dc567faf3403d28fd7a3a9",
        "r": "0x7e3718bb05d0838a63df32ef6bdb2c3802a096db5a78c9c4b6c64efcc7d33d4f",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6c972f8e7dd40727c7f01ad065fe0ff07bc42dc68bef636e5cb2b532247da055",
      "signature": {
        "s": "0x7943b4f04e71fdd3944b3bc2adf86f110542fdc4c4fd0d403df5b2847dca704b",
        "r": "0x899fa0c17a9b45dffe1e1700a61a4f30e48949fed52836753fb8468c6c7ccd47",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "286879034",
    "total": "286879034"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "286879034",
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
            "amount": "57572434761"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "286879"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiMGY3YjBhMS1mNWQwLTVjOWQtODExOC1lOTIwY2Q5YzYzOWYifQ==",
    "nonce": 7600,
    "balances": {
      "current": "12960089086054127",
      "previous": "12960089373220040"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9752fafe07226a458ca3e64deed7eb8834710135",
    "nonce": 9,
    "balances": {
      "current": "286879034",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:55.884Z",
  "updated": "2020-05-22T08:57:56.028Z",
  "id": "5ec79413005df800101bcc27"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000011196d3a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `286879034`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`