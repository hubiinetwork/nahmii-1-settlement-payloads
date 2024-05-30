# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x446B92ffb3D234b88d55DD666bB4B55b46C5BA90`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000dbaf6f7000000000000000000000000000000000000000000000000000000000dbaf6f70000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000dbaf6f7000000000000000000000000000000000000000000000000000000000dbaf6f70292525acd56f044a59082087a10622d7d24b90635530920c361d6abe644d8c93a0f067d43872133abd53af6b799b619b1406220123e0b6c15ce4ac2cc7b245dd201e4a4c72985ac1b5894dc9fc18aef8ce2398ca976462ca387b86fd43c3f75b000000000000000000000000000000000000000000000000000000000000001b161f9dfc1f46d573893cb108f960cd9ba2010e1dd1de07e07a63e9507b2ea39d6a2f8fa2ff7e30e0715861071d2e9aa78e0b3cf385c7e8c338669113b1e8645311fb9975f478555dfe44a23d2dec578903356f2abe1245504610fcd18a0a7eb9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d9800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b238b964fd8000000000000000000000000000000000000000000000000002e0b24677dfc9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000383d4b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6728db12000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a59575132596d497a4e69316a5a5449774c5455324e6d55744f5459344e7931685a54566a4d5441774e7a51315932556966513d3d0000000000000000000000000000000000000000000000000000000000000011000000000000000000000000446b92ffb3d234b88d55dd666bb4b55b46c5ba9000000000000000000000000000000000000000000000000000000000dbaf6f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x292525acd56f044a59082087a10622d7d24b90635530920c361d6abe644d8c93",
      "signature": {
        "s": "0x201e4a4c72985ac1b5894dc9fc18aef8ce2398ca976462ca387b86fd43c3f75b",
        "r": "0xa0f067d43872133abd53af6b799b619b1406220123e0b6c15ce4ac2cc7b245dd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x161f9dfc1f46d573893cb108f960cd9ba2010e1dd1de07e07a63e9507b2ea39d",
      "signature": {
        "s": "0x11fb9975f478555dfe44a23d2dec578903356f2abe1245504610fcd18a0a7eb9",
        "r": "0x6a2f8fa2ff7e30e0715861071d2e9aa78e0b3cf385c7e8c338669113b1e86453",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3685707632",
    "total": "3685707632"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3685707632",
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
            "amount": "57565305618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3685707"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzYWQ2YmIzNi1jZTIwLTU2NmUtOTY4Ny1hZTVjMTAwNzQ1Y2UifQ==",
    "nonce": 7576,
    "balances": {
      "current": "12960096222334936",
      "previous": "12960099911728275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x446b92ffb3d234b88d55dd666bb4b55b46c5ba90",
    "nonce": 17,
    "balances": {
      "current": "3685707632",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:47.442Z",
  "updated": "2020-05-22T08:57:47.513Z",
  "id": "5ec7940be5756b00111b8910"
}
```
* *stageAmount*: `3685707632`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000dbaf6f70000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000dbaf6f7000000000000000000000000000000000000000000000000000000000dbaf6f70292525acd56f044a59082087a10622d7d24b90635530920c361d6abe644d8c93a0f067d43872133abd53af6b799b619b1406220123e0b6c15ce4ac2cc7b245dd201e4a4c72985ac1b5894dc9fc18aef8ce2398ca976462ca387b86fd43c3f75b000000000000000000000000000000000000000000000000000000000000001b161f9dfc1f46d573893cb108f960cd9ba2010e1dd1de07e07a63e9507b2ea39d6a2f8fa2ff7e30e0715861071d2e9aa78e0b3cf385c7e8c338669113b1e8645311fb9975f478555dfe44a23d2dec578903356f2abe1245504610fcd18a0a7eb9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a56b800000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001d9800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e0b238b964fd8000000000000000000000000000000000000000000000000002e0b24677dfc9300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000383d4b000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000d6728db12000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a59575132596d497a4e69316a5a5449774c5455324e6d55744f5459344e7931685a54566a4d5441774e7a51315932556966513d3d0000000000000000000000000000000000000000000000000000000000000011000000000000000000000000446b92ffb3d234b88d55dd666bb4b55b46c5ba9000000000000000000000000000000000000000000000000000000000dbaf6f70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x292525acd56f044a59082087a10622d7d24b90635530920c361d6abe644d8c93",
      "signature": {
        "s": "0x201e4a4c72985ac1b5894dc9fc18aef8ce2398ca976462ca387b86fd43c3f75b",
        "r": "0xa0f067d43872133abd53af6b799b619b1406220123e0b6c15ce4ac2cc7b245dd",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x161f9dfc1f46d573893cb108f960cd9ba2010e1dd1de07e07a63e9507b2ea39d",
      "signature": {
        "s": "0x11fb9975f478555dfe44a23d2dec578903356f2abe1245504610fcd18a0a7eb9",
        "r": "0x6a2f8fa2ff7e30e0715861071d2e9aa78e0b3cf385c7e8c338669113b1e86453",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "3685707632",
    "total": "3685707632"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3685707632",
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
            "amount": "57565305618"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "3685707"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzYWQ2YmIzNi1jZTIwLTU2NmUtOTY4Ny1hZTVjMTAwNzQ1Y2UifQ==",
    "nonce": 7576,
    "balances": {
      "current": "12960096222334936",
      "previous": "12960099911728275"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x446b92ffb3d234b88d55dd666bb4b55b46c5ba90",
    "nonce": 17,
    "balances": {
      "current": "3685707632",
      "previous": "0"
    }
  },
  "blockNumber": "10114744",
  "created": "2020-05-22T08:57:47.442Z",
  "updated": "2020-05-22T08:57:47.513Z",
  "id": "5ec7940be5756b00111b8910"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000dbaf6f70000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3685707632`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`