# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x248EE163064CEC75103EFB80EA0014fBCd96693f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000c050000000000000000000000000000000000000000000000000000000000000c05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000c050000000000000000000000000000000000000000000000000000000000000c05085f2bbdcb36d2a6a4f95679900866f9d37f47549af33ea2b466a72c9de8e22da7c036997ca6c515f6735594b5a3c85ed97fac74443251fdddb6da27082f225659783592d70b84ea6b61b4a8cc45a742a757af196d41f87b2ae17f45e832ba20000000000000000000000000000000000000000000000000000000000000001b025e328bee2b8ba0af5f25b5a8b649cf1445225bd1e83869e14f6cce8d76e1c51aa670c6864abd8be82b3d3209371b7e204054c43a95b91ba60a400290e2899f37627ab8d7b8051550b7724ef60833360817d51b1b84deee6ce46933c545b2d3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e2900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b09c6a265ed000000000000000000000000000000000000000000000000002e0b09c6a271f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6dbffcca000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4749305a47517a5969316d4d6a52694c54566b4d6a4d74596d526a5a5330314e7a677a4e3259794f5749784e6d516966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000248ee163064cec75103efb80ea0014fbcd96693f0000000000000000000000000000000000000000000000000000000000000c05000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x085f2bbdcb36d2a6a4f95679900866f9d37f47549af33ea2b466a72c9de8e22d",
      "signature": {
        "s": "0x59783592d70b84ea6b61b4a8cc45a742a757af196d41f87b2ae17f45e832ba20",
        "r": "0xa7c036997ca6c515f6735594b5a3c85ed97fac74443251fdddb6da27082f2256",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x025e328bee2b8ba0af5f25b5a8b649cf1445225bd1e83869e14f6cce8d76e1c5",
      "signature": {
        "s": "0x37627ab8d7b8051550b7724ef60833360817d51b1b84deee6ce46933c545b2d3",
        "r": "0x1aa670c6864abd8be82b3d3209371b7e204054c43a95b91ba60a400290e2899f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3077",
    "total": "3077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3077",
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
            "amount": "57675873482"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMGI0ZGQzYi1mMjRiLTVkMjMtYmRjZS01NzgzN2YyOWIxNmQifQ==",
    "nonce": 7721,
    "balances": {
      "current": "12959985543833069",
      "previous": "12959985543836149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x248ee163064cec75103efb80ea0014fbcd96693f",
    "nonce": 4,
    "balances": {
      "current": "3077",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:00.208Z",
  "updated": "2020-05-22T08:59:00.272Z",
  "id": "5ec79454b0c6090011d5b2ea"
}
```
* *stageAmount*: `3077`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000000c05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000000c050000000000000000000000000000000000000000000000000000000000000c05085f2bbdcb36d2a6a4f95679900866f9d37f47549af33ea2b466a72c9de8e22da7c036997ca6c515f6735594b5a3c85ed97fac74443251fdddb6da27082f225659783592d70b84ea6b61b4a8cc45a742a757af196d41f87b2ae17f45e832ba20000000000000000000000000000000000000000000000000000000000000001b025e328bee2b8ba0af5f25b5a8b649cf1445225bd1e83869e14f6cce8d76e1c51aa670c6864abd8be82b3d3209371b7e204054c43a95b91ba60a400290e2899f37627ab8d7b8051550b7724ef60833360817d51b1b84deee6ce46933c545b2d3000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56bb00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001e2900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b09c6a265ed000000000000000000000000000000000000000000000000002e0b09c6a271f500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000003000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6dbffcca000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d4749305a47517a5969316d4d6a52694c54566b4d6a4d74596d526a5a5330314e7a677a4e3259794f5749784e6d516966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000248ee163064cec75103efb80ea0014fbcd96693f0000000000000000000000000000000000000000000000000000000000000c05000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x085f2bbdcb36d2a6a4f95679900866f9d37f47549af33ea2b466a72c9de8e22d",
      "signature": {
        "s": "0x59783592d70b84ea6b61b4a8cc45a742a757af196d41f87b2ae17f45e832ba20",
        "r": "0xa7c036997ca6c515f6735594b5a3c85ed97fac74443251fdddb6da27082f2256",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x025e328bee2b8ba0af5f25b5a8b649cf1445225bd1e83869e14f6cce8d76e1c5",
      "signature": {
        "s": "0x37627ab8d7b8051550b7724ef60833360817d51b1b84deee6ce46933c545b2d3",
        "r": "0x1aa670c6864abd8be82b3d3209371b7e204054c43a95b91ba60a400290e2899f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3077",
    "total": "3077"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3077",
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
            "amount": "57675873482"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxMGI0ZGQzYi1mMjRiLTVkMjMtYmRjZS01NzgzN2YyOWIxNmQifQ==",
    "nonce": 7721,
    "balances": {
      "current": "12959985543833069",
      "previous": "12959985543836149"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x248ee163064cec75103efb80ea0014fbcd96693f",
    "nonce": 4,
    "balances": {
      "current": "3077",
      "previous": "0"
    }
  },
  "blockNumber": "10114747",
  "created": "2020-05-22T08:59:00.208Z",
  "updated": "2020-05-22T08:59:00.272Z",
  "id": "5ec79454b0c6090011d5b2ea"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000000c05000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3077`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`