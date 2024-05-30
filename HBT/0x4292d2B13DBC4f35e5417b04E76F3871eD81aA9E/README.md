# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x4292d2B13DBC4f35e5417b04E76F3871eD81aA9E`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000009cae520a100000000000000000000000000000000000000000000000000000009cae520a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae520a100000000000000000000000000000000000000000000000000000009cae520a16a49900603750bdf376dfbacef4823a2100a4fc69e9651231705ee653caec6092e02567da1909e12a719397416e2b7723451ead044984ba78852d3fcb12a5160160464430907b4fa27c4ffdbdb0ed048a79971985a3d7989ae64ae4923ff0342000000000000000000000000000000000000000000000000000000000000001be3b2dce97052290fb865989daedbb996a724baffbf106ee1c6014ff465ecf6dbd9c1a9eb88f12b97909648d225c99e260c4fe3bd49515f56a5c4f35e76874bd67d5e3ba302d540931103cb2f7e2f74f2b1feab944cf28637b5751ce1744f7b26000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14676d509fc1000000000000000000000000000000000000000000000000002e14713ab7844100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b0890814d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d574a6a4e5463314f5330304f5467344c54566d4f446374596a526c4e7930775a444979595755785a4451314e446b6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004292d2b13dbc4f35e5417b04e76f3871ed81aa9e00000000000000000000000000000000000000000000000000000009cae520a1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a49900603750bdf376dfbacef4823a2100a4fc69e9651231705ee653caec609",
      "signature": {
        "s": "0x160464430907b4fa27c4ffdbdb0ed048a79971985a3d7989ae64ae4923ff0342",
        "r": "0x2e02567da1909e12a719397416e2b7723451ead044984ba78852d3fcb12a5160",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe3b2dce97052290fb865989daedbb996a724baffbf106ee1c6014ff465ecf6db",
      "signature": {
        "s": "0x7d5e3ba302d540931103cb2f7e2f74f2b1feab944cf28637b5751ce1744f7b26",
        "r": "0xd9c1a9eb88f12b97909648d225c99e260c4fe3bd49515f56a5c4f35e76874bd6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42058719393",
    "total": "42058719393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058719393",
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
            "amount": "47388328269"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058719"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMWJjNTc1OS00OTg4LTVmODctYjRlNy0wZDIyYWUxZDQ1NDkifQ==",
    "nonce": 7120,
    "balances": {
      "current": "12970283376877505",
      "previous": "12970325477655617"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4292d2b13dbc4f35e5417b04e76f3871ed81aa9e",
    "nonce": 22,
    "balances": {
      "current": "42058719393",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:22.621Z",
  "updated": "2020-05-22T08:54:22.716Z",
  "id": "5ec7933e005df800101bcb89"
}
```
* *stageAmount*: `42058719393`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000009cae520a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000009cae520a100000000000000000000000000000000000000000000000000000009cae520a16a49900603750bdf376dfbacef4823a2100a4fc69e9651231705ee653caec6092e02567da1909e12a719397416e2b7723451ead044984ba78852d3fcb12a5160160464430907b4fa27c4ffdbdb0ed048a79971985a3d7989ae64ae4923ff0342000000000000000000000000000000000000000000000000000000000000001be3b2dce97052290fb865989daedbb996a724baffbf106ee1c6014ff465ecf6dbd9c1a9eb88f12b97909648d225c99e260c4fe3bd49515f56a5c4f35e76874bd67d5e3ba302d540931103cb2f7e2f74f2b1feab944cf28637b5751ce1744f7b26000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56ab00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001bd000000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e14676d509fc1000000000000000000000000000000000000000000000000002e14713ab7844100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000281c3df000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b0890814d000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a684d574a6a4e5463314f5330304f5467344c54566d4f446374596a526c4e7930775a444979595755785a4451314e446b6966513d3d00000000000000000000000000000000000000000000000000000000000000160000000000000000000000004292d2b13dbc4f35e5417b04e76f3871ed81aa9e00000000000000000000000000000000000000000000000000000009cae520a1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6a49900603750bdf376dfbacef4823a2100a4fc69e9651231705ee653caec609",
      "signature": {
        "s": "0x160464430907b4fa27c4ffdbdb0ed048a79971985a3d7989ae64ae4923ff0342",
        "r": "0x2e02567da1909e12a719397416e2b7723451ead044984ba78852d3fcb12a5160",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe3b2dce97052290fb865989daedbb996a724baffbf106ee1c6014ff465ecf6db",
      "signature": {
        "s": "0x7d5e3ba302d540931103cb2f7e2f74f2b1feab944cf28637b5751ce1744f7b26",
        "r": "0xd9c1a9eb88f12b97909648d225c99e260c4fe3bd49515f56a5c4f35e76874bd6",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "42058719393",
    "total": "42058719393"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "42058719393",
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
            "amount": "47388328269"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "42058719"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhMWJjNTc1OS00OTg4LTVmODctYjRlNy0wZDIyYWUxZDQ1NDkifQ==",
    "nonce": 7120,
    "balances": {
      "current": "12970283376877505",
      "previous": "12970325477655617"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x4292d2b13dbc4f35e5417b04e76f3871ed81aa9e",
    "nonce": 22,
    "balances": {
      "current": "42058719393",
      "previous": "0"
    }
  },
  "blockNumber": "10114731",
  "created": "2020-05-22T08:54:22.621Z",
  "updated": "2020-05-22T08:54:22.716Z",
  "id": "5ec7933e005df800101bcb89"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000009cae520a1000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `42058719393`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`