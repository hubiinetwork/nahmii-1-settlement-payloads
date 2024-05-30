# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x09a4DDe1c5D2fBF3cF9Dd6410fE6a17fC5b64ca7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000001b1b3c92d00000000000000000000000000000000000000000000000000000001b1b3c92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001b1b3c92d00000000000000000000000000000000000000000000000000000001b1b3c92d167420208e2ba9c22ab956a37f7fbd2dfd018af9f446c2140cb9d3910e886936ea9c33c2c6e2d8e6b1ff37f2b9e27892eca57d0bddbd5532eeac2cde57b0f83613c564527bbe1e34b7bd1dc6d6ee5096df7ec3f977e2e077501794f8a8803859000000000000000000000000000000000000000000000000000000000000001bb53ec43a11683da14d9b6d4e74842ac00dda565058eabfced79807f8419de46e8b6dbff40d8cfb7b2a208bcb2cd8660fae01d1629010f9e074c38fb17fbc7478064d511d74ddcb6e18afce3a83b2876b0bf878dcab16120d2307809170db1929000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18055b8cbace000000000000000000000000000000000000000000000000002e18070daf8b1700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006f071c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1bc357b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5749314e6d5a6b5979316a4f446b784c545578595749744f4451334d79316b5a6a673459324a6c4f446b304d57596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000009a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca700000000000000000000000000000000000000000000000000000001b1b3c92d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x167420208e2ba9c22ab956a37f7fbd2dfd018af9f446c2140cb9d3910e886936",
      "signature": {
        "s": "0x13c564527bbe1e34b7bd1dc6d6ee5096df7ec3f977e2e077501794f8a8803859",
        "r": "0xea9c33c2c6e2d8e6b1ff37f2b9e27892eca57d0bddbd5532eeac2cde57b0f836",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb53ec43a11683da14d9b6d4e74842ac00dda565058eabfced79807f8419de46e",
      "signature": {
        "s": "0x064d511d74ddcb6e18afce3a83b2876b0bf878dcab16120d2307809170db1929",
        "r": "0x8b6dbff40d8cfb7b2a208bcb2cd8660fae01d1629010f9e074c38fb17fbc7478",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7276316973",
    "total": "7276316973"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7276316973",
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
            "amount": "43415459765"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7276316"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0OWI1NmZkYy1jODkxLTUxYWItODQ3My1kZjg4Y2JlODk0MWYifQ==",
    "nonce": 6462,
    "balances": {
      "current": "12974260218542798",
      "previous": "12974267502136087"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca7",
    "nonce": 22,
    "balances": {
      "current": "7276316973",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:18.184Z",
  "updated": "2020-05-22T08:49:18.250Z",
  "id": "5ec7920ee5756b00111b87b5"
}
```
* *stageAmount*: `7276316973`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000001b1b3c92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000001b1b3c92d00000000000000000000000000000000000000000000000000000001b1b3c92d167420208e2ba9c22ab956a37f7fbd2dfd018af9f446c2140cb9d3910e886936ea9c33c2c6e2d8e6b1ff37f2b9e27892eca57d0bddbd5532eeac2cde57b0f83613c564527bbe1e34b7bd1dc6d6ee5096df7ec3f977e2e077501794f8a8803859000000000000000000000000000000000000000000000000000000000000001bb53ec43a11683da14d9b6d4e74842ac00dda565058eabfced79807f8419de46e8b6dbff40d8cfb7b2a208bcb2cd8660fae01d1629010f9e074c38fb17fbc7478064d511d74ddcb6e18afce3a83b2876b0bf878dcab16120d2307809170db1929000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56910000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000193e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e18055b8cbace000000000000000000000000000000000000000000000000002e18070daf8b1700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000006f071c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a1bc357b5000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f5749314e6d5a6b5979316a4f446b784c545578595749744f4451334d79316b5a6a673459324a6c4f446b304d57596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000009a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca700000000000000000000000000000000000000000000000000000001b1b3c92d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x167420208e2ba9c22ab956a37f7fbd2dfd018af9f446c2140cb9d3910e886936",
      "signature": {
        "s": "0x13c564527bbe1e34b7bd1dc6d6ee5096df7ec3f977e2e077501794f8a8803859",
        "r": "0xea9c33c2c6e2d8e6b1ff37f2b9e27892eca57d0bddbd5532eeac2cde57b0f836",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb53ec43a11683da14d9b6d4e74842ac00dda565058eabfced79807f8419de46e",
      "signature": {
        "s": "0x064d511d74ddcb6e18afce3a83b2876b0bf878dcab16120d2307809170db1929",
        "r": "0x8b6dbff40d8cfb7b2a208bcb2cd8660fae01d1629010f9e074c38fb17fbc7478",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7276316973",
    "total": "7276316973"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7276316973",
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
            "amount": "43415459765"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "7276316"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0OWI1NmZkYy1jODkxLTUxYWItODQ3My1kZjg4Y2JlODk0MWYifQ==",
    "nonce": 6462,
    "balances": {
      "current": "12974260218542798",
      "previous": "12974267502136087"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x09a4dde1c5d2fbf3cf9dd6410fe6a17fc5b64ca7",
    "nonce": 22,
    "balances": {
      "current": "7276316973",
      "previous": "0"
    }
  },
  "blockNumber": "10114705",
  "created": "2020-05-22T08:49:18.184Z",
  "updated": "2020-05-22T08:49:18.250Z",
  "id": "5ec7920ee5756b00111b87b5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000001b1b3c92d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7276316973`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`