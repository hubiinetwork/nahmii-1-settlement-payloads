# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x452665c694324aa8eA264d48bd49C56cC24022fe`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000021797000000000000000000000000000000000000000000000000000000000002179700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000021797000000000000000000000000000000000000000000000000000000000002179709d373ee9567124864e4bb55ba8632234ecfb11cccf57ddd72fdf669b1b5954d18f9dbe3222d5320f7f9a79dc40ecf29c1a9d6f08595e827ad3c72141ea1e1414b488bc3b25e85d20819df6f470118390c5d8d890e51e5dff3e9dcfd15604280000000000000000000000000000000000000000000000000000000000000001be8736f772a1dbf58df7122549e4e2ea794a8303180fa080f36de368f2379ef744b2b7afaf3fde53ae60e6059e0a35cd13394f92bdb24e4c7eb7ba183e17e08887c9cf2515c551fc85f690347fe44f918abd9f275b0fbced520446354b828b6f2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006bb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5927697000000000000000000000000000000000000000000000000002386f2c5948eb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d24e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f54637a4e44637a4e6930314d444d7a4c5455795a575174596d52685a693079595759335a5463774f4459354f54676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000452665c694324aa8ea264d48bd49c56cc24022fe0000000000000000000000000000000000000000000000000000000000021797000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x09d373ee9567124864e4bb55ba8632234ecfb11cccf57ddd72fdf669b1b5954d",
      "signature": {
        "s": "0x4b488bc3b25e85d20819df6f470118390c5d8d890e51e5dff3e9dcfd15604280",
        "r": "0x18f9dbe3222d5320f7f9a79dc40ecf29c1a9d6f08595e827ad3c72141ea1e141",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe8736f772a1dbf58df7122549e4e2ea794a8303180fa080f36de368f2379ef74",
      "signature": {
        "s": "0x7c9cf2515c551fc85f690347fe44f918abd9f275b0fbced520446354b828b6f2",
        "r": "0x4b2b7afaf3fde53ae60e6059e0a35cd13394f92bdb24e4c7eb7ba183e17e0888",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "137111",
    "total": "137111"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "137111",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "643662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "137"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OTczNDczNi01MDMzLTUyZWQtYmRhZi0yYWY3ZTcwODY5OTgifQ==",
    "nonce": 1723,
    "balances": {
      "current": "10000001439790743",
      "previous": "10000001439927991"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x452665c694324aa8ea264d48bd49c56cc24022fe",
    "nonce": 13,
    "balances": {
      "current": "137111",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:38.315Z",
  "updated": "2020-05-22T08:11:38.377Z",
  "id": "5ec7893a005df800101bc465"
}
```
* *stageAmount*: `137111`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002179700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000021797000000000000000000000000000000000000000000000000000000000002179709d373ee9567124864e4bb55ba8632234ecfb11cccf57ddd72fdf669b1b5954d18f9dbe3222d5320f7f9a79dc40ecf29c1a9d6f08595e827ad3c72141ea1e1414b488bc3b25e85d20819df6f470118390c5d8d890e51e5dff3e9dcfd15604280000000000000000000000000000000000000000000000000000000000000001be8736f772a1dbf58df7122549e4e2ea794a8303180fa080f36de368f2379ef744b2b7afaf3fde53ae60e6059e0a35cd13394f92bdb24e4c7eb7ba183e17e08887c9cf2515c551fc85f690347fe44f918abd9f275b0fbced520446354b828b6f2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ea000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000006bb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c5927697000000000000000000000000000000000000000000000000002386f2c5948eb700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009d24e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334f54637a4e44637a4e6930314d444d7a4c5455795a575174596d52685a693079595759335a5463774f4459354f54676966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000452665c694324aa8ea264d48bd49c56cc24022fe0000000000000000000000000000000000000000000000000000000000021797000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x09d373ee9567124864e4bb55ba8632234ecfb11cccf57ddd72fdf669b1b5954d",
      "signature": {
        "s": "0x4b488bc3b25e85d20819df6f470118390c5d8d890e51e5dff3e9dcfd15604280",
        "r": "0x18f9dbe3222d5320f7f9a79dc40ecf29c1a9d6f08595e827ad3c72141ea1e141",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe8736f772a1dbf58df7122549e4e2ea794a8303180fa080f36de368f2379ef74",
      "signature": {
        "s": "0x7c9cf2515c551fc85f690347fe44f918abd9f275b0fbced520446354b828b6f2",
        "r": "0x4b2b7afaf3fde53ae60e6059e0a35cd13394f92bdb24e4c7eb7ba183e17e0888",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "137111",
    "total": "137111"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "137111",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "643662"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "137"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI3OTczNDczNi01MDMzLTUyZWQtYmRhZi0yYWY3ZTcwODY5OTgifQ==",
    "nonce": 1723,
    "balances": {
      "current": "10000001439790743",
      "previous": "10000001439927991"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x452665c694324aa8ea264d48bd49c56cc24022fe",
    "nonce": 13,
    "balances": {
      "current": "137111",
      "previous": "0"
    }
  },
  "blockNumber": "10114538",
  "created": "2020-05-22T08:11:38.315Z",
  "updated": "2020-05-22T08:11:38.377Z",
  "id": "5ec7893a005df800101bc465"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000217970000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `137111`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``