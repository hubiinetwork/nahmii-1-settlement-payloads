# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x389C85a7A31C52143C110f191f98fb9e936E5EAf`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000000000000000000000000000000000003d7db526492c7074db096c09f660bae91161c1be4a8e72977fbf781aa8460c88ddb20c3bd18c2f7854ae2248be7e9fd7a9458eaea913fa546344c0722c2cc82ddede63e0248f98ab1f7f0c396ece689e37e202f49ba4e62c0b93b0784ce4040919027346000000000000000000000000000000000000000000000000000000000000001ca5d3ff60bb3ada97db8b2a86d27a66a4e417fa7ee2550ff96212eebb29067a361d1c541fdf9f7db810a5fdac814ac3bd00edc276196ffc65c8dbb52f4e9999764c27f3c0f7f885832f94cfed5ba88cefc526db95d5faf14fedd760fbf47c868f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a1100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e171c7ada1c0f000000000000000000000000000000000000000000000000002e171cb8678f1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000fbde0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5751f81a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d57466c4d7a4d304f5330774d4751314c54566b4d474d744f444a684e43316c4d5459325a5759354f4445305a6d456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000389c85a7a31c52143c110f191f98fb9e936e5eaf000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x492c7074db096c09f660bae91161c1be4a8e72977fbf781aa8460c88ddb20c3b",
      "signature": {
        "s": "0x248f98ab1f7f0c396ece689e37e202f49ba4e62c0b93b0784ce4040919027346",
        "r": "0xd18c2f7854ae2248be7e9fd7a9458eaea913fa546344c0722c2cc82ddede63e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa5d3ff60bb3ada97db8b2a86d27a66a4e417fa7ee2550ff96212eebb29067a36",
      "signature": {
        "s": "0x4c27f3c0f7f885832f94cfed5ba88cefc526db95d5faf14fedd760fbf47c868f",
        "r": "0x1d1c541fdf9f7db810a5fdac814ac3bd00edc276196ffc65c8dbb52f4e999976",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1031648550",
    "total": "1031648550"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1031648550",
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
            "amount": "44414662682"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1031648"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMWFlMzM0OS0wMGQ1LTVkMGMtODJhNC1lMTY2ZWY5ODE0ZmEifQ==",
    "nonce": 6673,
    "balances": {
      "current": "12973260016327695",
      "previous": "12973261049007893"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x389c85a7a31c52143c110f191f98fb9e936e5eaf",
    "nonce": 22,
    "balances": {
      "current": "1031648550",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.755Z",
  "updated": "2020-05-22T08:50:54.822Z",
  "id": "5ec7926e005df800101bcaf7"
}
```
* *stageAmount*: `1031648550`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000000000000000000000000000000000003d7db526492c7074db096c09f660bae91161c1be4a8e72977fbf781aa8460c88ddb20c3bd18c2f7854ae2248be7e9fd7a9458eaea913fa546344c0722c2cc82ddede63e0248f98ab1f7f0c396ece689e37e202f49ba4e62c0b93b0784ce4040919027346000000000000000000000000000000000000000000000000000000000000001ca5d3ff60bb3ada97db8b2a86d27a66a4e417fa7ee2550ff96212eebb29067a361d1c541fdf9f7db810a5fdac814ac3bd00edc276196ffc65c8dbb52f4e9999764c27f3c0f7f885832f94cfed5ba88cefc526db95d5faf14fedd760fbf47c868f000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a569800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001a1100000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e171c7ada1c0f000000000000000000000000000000000000000000000000002e171cb8678f1500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000fbde0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5751f81a000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774d57466c4d7a4d304f5330774d4751314c54566b4d474d744f444a684e43316c4d5459325a5759354f4445305a6d456966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000389c85a7a31c52143c110f191f98fb9e936e5eaf000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x492c7074db096c09f660bae91161c1be4a8e72977fbf781aa8460c88ddb20c3b",
      "signature": {
        "s": "0x248f98ab1f7f0c396ece689e37e202f49ba4e62c0b93b0784ce4040919027346",
        "r": "0xd18c2f7854ae2248be7e9fd7a9458eaea913fa546344c0722c2cc82ddede63e0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa5d3ff60bb3ada97db8b2a86d27a66a4e417fa7ee2550ff96212eebb29067a36",
      "signature": {
        "s": "0x4c27f3c0f7f885832f94cfed5ba88cefc526db95d5faf14fedd760fbf47c868f",
        "r": "0x1d1c541fdf9f7db810a5fdac814ac3bd00edc276196ffc65c8dbb52f4e999976",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1031648550",
    "total": "1031648550"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1031648550",
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
            "amount": "44414662682"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "1031648"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwMWFlMzM0OS0wMGQ1LTVkMGMtODJhNC1lMTY2ZWY5ODE0ZmEifQ==",
    "nonce": 6673,
    "balances": {
      "current": "12973260016327695",
      "previous": "12973261049007893"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x389c85a7a31c52143c110f191f98fb9e936e5eaf",
    "nonce": 22,
    "balances": {
      "current": "1031648550",
      "previous": "0"
    }
  },
  "blockNumber": "10114712",
  "created": "2020-05-22T08:50:54.755Z",
  "updated": "2020-05-22T08:50:54.822Z",
  "id": "5ec7926e005df800101bcaf7"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000003d7db526000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1031648550`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`