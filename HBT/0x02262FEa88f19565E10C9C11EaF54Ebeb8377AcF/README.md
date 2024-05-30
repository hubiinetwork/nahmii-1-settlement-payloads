# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x02262FEa88f19565E10C9C11EaF54Ebeb8377AcF`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000000000000000000000000000000000000584b87e0d1b9476f29b54d12ddea2cab22a1d6d8ec6951154b35aae165002772ed8f08ad5a65d8b36a8c96d9d1d5e12504403460ce48c85523192fb50ec9938dccde6eb3b8e0ee882e93b3f2ecf3575919dfc4bb9b0b7aeff3b716f3d9fffc1effe839e000000000000000000000000000000000000000000000000000000000000001ba6ec2c71d2d9f09ca307e8dae1c7ddc5b28cd219660d898a974f1494829363d8b8e7e5d06169a3e1f1edb6f97777e443a033dacc78bffdb08f153830796e74c15b869963daf86000df1f72e43dec8257f521d5ba52348ddc2e677be669cc6284000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e172aa44de0ef000000000000000000000000000000000000000000000000002e172aa9d4031500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000169a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a53b2c7e0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4759784d7a466c5a69316d5a6a49354c5455324f446b744f574a684e53316c4e6a46694d32566c4f5463344e54636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002262fea88f19565e10c9c11eaf54ebeb8377acf000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d1b9476f29b54d12ddea2cab22a1d6d8ec6951154b35aae165002772ed8f08a",
      "signature": {
        "s": "0x3b8e0ee882e93b3f2ecf3575919dfc4bb9b0b7aeff3b716f3d9fffc1effe839e",
        "r": "0xd5a65d8b36a8c96d9d1d5e12504403460ce48c85523192fb50ec9938dccde6eb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa6ec2c71d2d9f09ca307e8dae1c7ddc5b28cd219660d898a974f1494829363d8",
      "signature": {
        "s": "0x5b869963daf86000df1f72e43dec8257f521d5ba52348ddc2e677be669cc6284",
        "r": "0xb8e7e5d06169a3e1f1edb6f97777e443a033dacc78bffdb08f153830796e74c1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92584062",
    "total": "92584062"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92584062",
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
            "amount": "44353898464"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "92584"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjOGYxMzFlZi1mZjI5LTU2ODktOWJhNS1lNjFiM2VlOTc4NTcifQ==",
    "nonce": 6644,
    "balances": {
      "current": "12973320841322735",
      "previous": "12973320933999381"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02262fea88f19565e10c9c11eaf54ebeb8377acf",
    "nonce": 22,
    "balances": {
      "current": "92584062",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:46.845Z",
  "updated": "2020-05-22T08:50:46.913Z",
  "id": "5ec79266b0c6090011d5b170"
}
```
* *stageAmount*: `92584062`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000000000000000000000000000000000000584b87e0d1b9476f29b54d12ddea2cab22a1d6d8ec6951154b35aae165002772ed8f08ad5a65d8b36a8c96d9d1d5e12504403460ce48c85523192fb50ec9938dccde6eb3b8e0ee882e93b3f2ecf3575919dfc4bb9b0b7aeff3b716f3d9fffc1effe839e000000000000000000000000000000000000000000000000000000000000001ba6ec2c71d2d9f09ca307e8dae1c7ddc5b28cd219660d898a974f1494829363d8b8e7e5d06169a3e1f1edb6f97777e443a033dacc78bffdb08f153830796e74c15b869963daf86000df1f72e43dec8257f521d5ba52348ddc2e677be669cc6284000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019f400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e172aa44de0ef000000000000000000000000000000000000000000000000002e172aa9d4031500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000169a8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a53b2c7e0000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4f4759784d7a466c5a69316d5a6a49354c5455324f446b744f574a684e53316c4e6a46694d32566c4f5463344e54636966513d3d000000000000000000000000000000000000000000000000000000000000001600000000000000000000000002262fea88f19565e10c9c11eaf54ebeb8377acf000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d1b9476f29b54d12ddea2cab22a1d6d8ec6951154b35aae165002772ed8f08a",
      "signature": {
        "s": "0x3b8e0ee882e93b3f2ecf3575919dfc4bb9b0b7aeff3b716f3d9fffc1effe839e",
        "r": "0xd5a65d8b36a8c96d9d1d5e12504403460ce48c85523192fb50ec9938dccde6eb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa6ec2c71d2d9f09ca307e8dae1c7ddc5b28cd219660d898a974f1494829363d8",
      "signature": {
        "s": "0x5b869963daf86000df1f72e43dec8257f521d5ba52348ddc2e677be669cc6284",
        "r": "0xb8e7e5d06169a3e1f1edb6f97777e443a033dacc78bffdb08f153830796e74c1",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "92584062",
    "total": "92584062"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "92584062",
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
            "amount": "44353898464"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "92584"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjOGYxMzFlZi1mZjI5LTU2ODktOWJhNS1lNjFiM2VlOTc4NTcifQ==",
    "nonce": 6644,
    "balances": {
      "current": "12973320841322735",
      "previous": "12973320933999381"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x02262fea88f19565e10c9c11eaf54ebeb8377acf",
    "nonce": 22,
    "balances": {
      "current": "92584062",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:46.845Z",
  "updated": "2020-05-22T08:50:46.913Z",
  "id": "5ec79266b0c6090011d5b170"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000584b87e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `92584062`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`