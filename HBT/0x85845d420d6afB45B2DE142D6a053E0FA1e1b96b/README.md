# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x85845d420d6afB45B2DE142D6a053E0FA1e1b96b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000108e401a00000000000000000000000000000000000000000000000000000000108e401a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000108e401a00000000000000000000000000000000000000000000000000000000108e401a491e262676d49c48fda990e42b34ccdffc1cd756eac32a4beddd79881d81d20d866684757ae017cb11b3ff2b4f46082dc72f11afff6cf0f039ca95ef40bc0f52457231d0a91c46cf97df545d093160b5c5cf533bb22365df181ed4d7bd184ca3000000000000000000000000000000000000000000000000000000000000001ba3e37f6e02b76cd5bc785a63700b2dcca2a6c9a9d71192316a29dcce091665359da255e9c263729d5343ef8472e5ad4e867fc32231cea0b6745ee9cf9102d7760a0ccac9e1168a8256d73e85df65abb5c8bd92a5058ce6d278641cd082d213a1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5682000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0d7d654fb9000000000000000000000000000000000000000000000000002e1b0d8df7ccd000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000043cfd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000955458ecf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e695a6a49314d693079596a6c694c5455774d6d49744f5459304e69316b596d5a68596d46694f544e6b4e47596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000085845d420d6afb45b2de142d6a053e0fa1e1b96b00000000000000000000000000000000000000000000000000000000108e401a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x491e262676d49c48fda990e42b34ccdffc1cd756eac32a4beddd79881d81d20d",
      "signature": {
        "s": "0x457231d0a91c46cf97df545d093160b5c5cf533bb22365df181ed4d7bd184ca3",
        "r": "0x866684757ae017cb11b3ff2b4f46082dc72f11afff6cf0f039ca95ef40bc0f52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa3e37f6e02b76cd5bc785a63700b2dcca2a6c9a9d71192316a29dcce09166535",
      "signature": {
        "s": "0x0a0ccac9e1168a8256d73e85df65abb5c8bd92a5058ce6d278641cd082d213a1",
        "r": "0x9da255e9c263729d5343ef8472e5ad4e867fc32231cea0b6745ee9cf9102d776",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "277757978",
    "total": "277757978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "277757978",
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
            "amount": "40085327567"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "277757"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMWNiZjI1Mi0yYjliLTUwMmItOTY0Ni1kYmZhYmFiOTNkNGYifQ==",
    "nonce": 6128,
    "balances": {
      "current": "12977593681006521",
      "previous": "12977593959042256"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x85845d420d6afb45b2de142d6a053e0fa1e1b96b",
    "nonce": 22,
    "balances": {
      "current": "277757978",
      "previous": "0"
    }
  },
  "blockNumber": "10114690",
  "created": "2020-05-22T08:46:41.396Z",
  "updated": "2020-05-22T08:46:41.494Z",
  "id": "5ec79171e5756b00111b8749"
}
```
* *stageAmount*: `277757978`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000108e401a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000108e401a00000000000000000000000000000000000000000000000000000000108e401a491e262676d49c48fda990e42b34ccdffc1cd756eac32a4beddd79881d81d20d866684757ae017cb11b3ff2b4f46082dc72f11afff6cf0f039ca95ef40bc0f52457231d0a91c46cf97df545d093160b5c5cf533bb22365df181ed4d7bd184ca3000000000000000000000000000000000000000000000000000000000000001ba3e37f6e02b76cd5bc785a63700b2dcca2a6c9a9d71192316a29dcce091665359da255e9c263729d5343ef8472e5ad4e867fc32231cea0b6745ee9cf9102d7760a0ccac9e1168a8256d73e85df65abb5c8bd92a5058ce6d278641cd082d213a1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5682000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000017f000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1b0d7d654fb9000000000000000000000000000000000000000000000000002e1b0d8df7ccd000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000043cfd000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000955458ecf000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e695a6a49314d693079596a6c694c5455774d6d49744f5459304e69316b596d5a68596d46694f544e6b4e47596966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000085845d420d6afb45b2de142d6a053e0fa1e1b96b00000000000000000000000000000000000000000000000000000000108e401a000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x491e262676d49c48fda990e42b34ccdffc1cd756eac32a4beddd79881d81d20d",
      "signature": {
        "s": "0x457231d0a91c46cf97df545d093160b5c5cf533bb22365df181ed4d7bd184ca3",
        "r": "0x866684757ae017cb11b3ff2b4f46082dc72f11afff6cf0f039ca95ef40bc0f52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa3e37f6e02b76cd5bc785a63700b2dcca2a6c9a9d71192316a29dcce09166535",
      "signature": {
        "s": "0x0a0ccac9e1168a8256d73e85df65abb5c8bd92a5058ce6d278641cd082d213a1",
        "r": "0x9da255e9c263729d5343ef8472e5ad4e867fc32231cea0b6745ee9cf9102d776",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "277757978",
    "total": "277757978"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "277757978",
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
            "amount": "40085327567"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "277757"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkMWNiZjI1Mi0yYjliLTUwMmItOTY0Ni1kYmZhYmFiOTNkNGYifQ==",
    "nonce": 6128,
    "balances": {
      "current": "12977593681006521",
      "previous": "12977593959042256"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x85845d420d6afb45b2de142d6a053e0fa1e1b96b",
    "nonce": 22,
    "balances": {
      "current": "277757978",
      "previous": "0"
    }
  },
  "blockNumber": "10114690",
  "created": "2020-05-22T08:46:41.396Z",
  "updated": "2020-05-22T08:46:41.494Z",
  "id": "5ec79171e5756b00111b8749"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000108e401a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `277757978`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`
