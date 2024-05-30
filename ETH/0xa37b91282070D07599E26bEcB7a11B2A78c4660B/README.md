# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa37b91282070D07599E26bEcB7a11B2A78c4660B`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7cc02c1eb73b7edb573d959d097a2a0831492b87b64fff335387731abc54b0c962d8a900ba96c73179df8e132553e8fb4a48c369ecbbded7027f1adb7b53a852d44ae73df65645ee40d7e3585159bbfedd3696d853f62c08dc01f43a8adf601ca000000000000000000000000000000000000000000000000000000000000001c33ceedcf2ef94e40e5691011521abd2605d5afc7d88c8eed63cc4df5a5048cabdce8dbc60f1c93320fcc3158e3cfdc11dd17c060fd8f0cbcb0f8017ff00e87a062f51e42f0ca91c5c8a6aa7257a4da1b4aee6af1028a435e86dd4f5ac3d5ed65000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000040600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca71a235000000000000000000000000000000000000000000000000002386f2ca71a2ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008941c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6a5578597a59354d6930344d6a677a4c54566d596a55744f4449774d53316d596a4d33595749304e44426d4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a37b91282070d07599e26becb7a11b2a78c4660b00000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcc02c1eb73b7edb573d959d097a2a0831492b87b64fff335387731abc54b0c96",
      "signature": {
        "s": "0x44ae73df65645ee40d7e3585159bbfedd3696d853f62c08dc01f43a8adf601ca",
        "r": "0x2d8a900ba96c73179df8e132553e8fb4a48c369ecbbded7027f1adb7b53a852d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x33ceedcf2ef94e40e5691011521abd2605d5afc7d88c8eed63cc4df5a5048cab",
      "signature": {
        "s": "0x62f51e42f0ca91c5c8a6aa7257a4da1b4aee6af1028a435e86dd4f5ac3d5ed65",
        "r": "0xdce8dbc60f1c93320fcc3158e3cfdc11dd17c060fd8f0cbcb0f8017ff00e87a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "562204"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNjUxYzY5Mi04MjgzLTVmYjUtODIwMS1mYjM3YWI0NDBmM2IifQ==",
    "nonce": 1030,
    "balances": {
      "current": "10000001521525301",
      "previous": "10000001521525485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa37b91282070d07599e26becb7a11b2a78c4660b",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:23.026Z",
  "updated": "2020-05-22T08:06:23.090Z",
  "id": "5ec787ffe5756b00111b80c4"
}
```
* *stageAmount*: `183`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000000b700000000000000000000000000000000000000000000000000000000000000b7cc02c1eb73b7edb573d959d097a2a0831492b87b64fff335387731abc54b0c962d8a900ba96c73179df8e132553e8fb4a48c369ecbbded7027f1adb7b53a852d44ae73df65645ee40d7e3585159bbfedd3696d853f62c08dc01f43a8adf601ca000000000000000000000000000000000000000000000000000000000000001c33ceedcf2ef94e40e5691011521abd2605d5afc7d88c8eed63cc4df5a5048cabdce8dbc60f1c93320fcc3158e3cfdc11dd17c060fd8f0cbcb0f8017ff00e87a062f51e42f0ca91c5c8a6aa7257a4da1b4aee6af1028a435e86dd4f5ac3d5ed65000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000040600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2ca71a235000000000000000000000000000000000000000000000000002386f2ca71a2ed00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008941c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e6a5578597a59354d6930344d6a677a4c54566d596a55744f4449774d53316d596a4d33595749304e44426d4d32496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000a37b91282070d07599e26becb7a11b2a78c4660b00000000000000000000000000000000000000000000000000000000000000b7000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcc02c1eb73b7edb573d959d097a2a0831492b87b64fff335387731abc54b0c96",
      "signature": {
        "s": "0x44ae73df65645ee40d7e3585159bbfedd3696d853f62c08dc01f43a8adf601ca",
        "r": "0x2d8a900ba96c73179df8e132553e8fb4a48c369ecbbded7027f1adb7b53a852d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x33ceedcf2ef94e40e5691011521abd2605d5afc7d88c8eed63cc4df5a5048cab",
      "signature": {
        "s": "0x62f51e42f0ca91c5c8a6aa7257a4da1b4aee6af1028a435e86dd4f5ac3d5ed65",
        "r": "0xdce8dbc60f1c93320fcc3158e3cfdc11dd17c060fd8f0cbcb0f8017ff00e87a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "183",
    "total": "183"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "183",
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
            "amount": "562204"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyNjUxYzY5Mi04MjgzLTVmYjUtODIwMS1mYjM3YWI0NDBmM2IifQ==",
    "nonce": 1030,
    "balances": {
      "current": "10000001521525301",
      "previous": "10000001521525485"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa37b91282070d07599e26becb7a11b2a78c4660b",
    "nonce": 20,
    "balances": {
      "current": "183",
      "previous": "0"
    }
  },
  "blockNumber": "10114516",
  "created": "2020-05-22T08:06:23.026Z",
  "updated": "2020-05-22T08:06:23.090Z",
  "id": "5ec787ffe5756b00111b80c4"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000b70000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `183`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``