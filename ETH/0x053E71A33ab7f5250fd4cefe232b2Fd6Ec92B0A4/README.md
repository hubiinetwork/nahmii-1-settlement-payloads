# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x053E71A33ab7f5250fd4cefe232b2Fd6Ec92B0A4`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000014d250000000000000000000000000000000000000000000000000000000000014d2500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000014d250000000000000000000000000000000000000000000000000000000000014d2559cc92606168ba34910c886736fe64bd934037b82cba99d14bb0ff595154aa65f8415252b79b65919aedd5833a7940bae51db304816e2afd5db027f036d17582059f7f1b7bb3b39a53d3d5a7dca366ca0ff574eddb5893c8ccb93e1bf137b3ff000000000000000000000000000000000000000000000000000000000000001cd956762d36df8a5fbd41b87f86c392ce4efcfc7383c91e17e5a4b54c01372317ce6082e5a84a86de63cda335e01a1811326baf61a9f09a2393d22fbe855e7e72012578752d5f7b725c4f161716833c5226d3bc945ef54bcb555f45d6fbb26361000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000036d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cadce4d1000000000000000000000000000000000000000000000000002386f2cade324b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000550000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000878c500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e5467784e6a526d4f5330344f5751334c54566a5a546374596a59334d7931694f445a6b4d324d304e574d785954456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000053e71a33ab7f5250fd4cefe232b2fd6ec92b0a40000000000000000000000000000000000000000000000000000000000014d25000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59cc92606168ba34910c886736fe64bd934037b82cba99d14bb0ff595154aa65",
      "signature": {
        "s": "0x059f7f1b7bb3b39a53d3d5a7dca366ca0ff574eddb5893c8ccb93e1bf137b3ff",
        "r": "0xf8415252b79b65919aedd5833a7940bae51db304816e2afd5db027f036d17582",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd956762d36df8a5fbd41b87f86c392ce4efcfc7383c91e17e5a4b54c01372317",
      "signature": {
        "s": "0x012578752d5f7b725c4f161716833c5226d3bc945ef54bcb555f45d6fbb26361",
        "r": "0xce6082e5a84a86de63cda335e01a1811326baf61a9f09a2393d22fbe855e7e72",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "85285",
    "total": "85285"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "85285",
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
            "amount": "555205"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "85"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNTgxNjRmOS04OWQ3LTVjZTctYjY3My1iODZkM2M0NWMxYTEifQ==",
    "nonce": 877,
    "balances": {
      "current": "10000001528554705",
      "previous": "10000001528640075"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x053e71a33ab7f5250fd4cefe232b2fd6ec92b0a4",
    "nonce": 20,
    "balances": {
      "current": "85285",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:12.733Z",
  "updated": "2020-05-22T08:05:12.821Z",
  "id": "5ec787b8b0c6090011d5a9f5"
}
```
* *stageAmount*: `85285`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000014d2500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000014d250000000000000000000000000000000000000000000000000000000000014d2559cc92606168ba34910c886736fe64bd934037b82cba99d14bb0ff595154aa65f8415252b79b65919aedd5833a7940bae51db304816e2afd5db027f036d17582059f7f1b7bb3b39a53d3d5a7dca366ca0ff574eddb5893c8ccb93e1bf137b3ff000000000000000000000000000000000000000000000000000000000000001cd956762d36df8a5fbd41b87f86c392ce4efcfc7383c91e17e5a4b54c01372317ce6082e5a84a86de63cda335e01a1811326baf61a9f09a2393d22fbe855e7e72012578752d5f7b725c4f161716833c5226d3bc945ef54bcb555f45d6fbb26361000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000036d00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cadce4d1000000000000000000000000000000000000000000000000002386f2cade324b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000550000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000878c500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e5467784e6a526d4f5330344f5751334c54566a5a546374596a59334d7931694f445a6b4d324d304e574d785954456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000053e71a33ab7f5250fd4cefe232b2fd6ec92b0a40000000000000000000000000000000000000000000000000000000000014d25000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x59cc92606168ba34910c886736fe64bd934037b82cba99d14bb0ff595154aa65",
      "signature": {
        "s": "0x059f7f1b7bb3b39a53d3d5a7dca366ca0ff574eddb5893c8ccb93e1bf137b3ff",
        "r": "0xf8415252b79b65919aedd5833a7940bae51db304816e2afd5db027f036d17582",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd956762d36df8a5fbd41b87f86c392ce4efcfc7383c91e17e5a4b54c01372317",
      "signature": {
        "s": "0x012578752d5f7b725c4f161716833c5226d3bc945ef54bcb555f45d6fbb26361",
        "r": "0xce6082e5a84a86de63cda335e01a1811326baf61a9f09a2393d22fbe855e7e72",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "85285",
    "total": "85285"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "85285",
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
            "amount": "555205"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "85"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNTgxNjRmOS04OWQ3LTVjZTctYjY3My1iODZkM2M0NWMxYTEifQ==",
    "nonce": 877,
    "balances": {
      "current": "10000001528554705",
      "previous": "10000001528640075"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x053e71a33ab7f5250fd4cefe232b2fd6ec92b0a4",
    "nonce": 20,
    "balances": {
      "current": "85285",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:12.733Z",
  "updated": "2020-05-22T08:05:12.821Z",
  "id": "5ec787b8b0c6090011d5a9f5"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000014d250000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `85285`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``