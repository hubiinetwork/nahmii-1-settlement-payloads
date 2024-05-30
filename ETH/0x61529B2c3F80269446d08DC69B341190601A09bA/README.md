# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x61529B2c3F80269446d08DC69B341190601A09bA`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000015780000000000000000000000000000000000000000000000000000000000001578000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000015780000000000000000000000000000000000000000000000000000000000001578dc4a7418d68b7a77290a39c21043e264b958870d1386c10049d01aab41a62ff08d5d52bbb82e11b542b89178aeea7a729833db7565f70b10ce2bac6b53fc342373a597563f53b9614539c6973fa745f2ed0099c320b2097fa93ac3010a066fa4000000000000000000000000000000000000000000000000000000000000001b9321151ad5cbe1a77bc7a774bc77ce0872de681bb9ccf029d4ce1c637517060082e7e3ab8c601556d052096a8252fa81156259fb11548779e9f97deb080b9b6c4637e15b164f7e7394df92fc48200a407b6efbb0d1777e13d5af6537ecbbd484000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000081200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3743aef000000000000000000000000000000000000000000000000002386f2c374506c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5c6e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f545532596d4d315a43316b597a59304c54566b4d7a63744f4456684e7930774d6d55344e6d49344d6d49774f44516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061529b2c3f80269446d08dc69b341190601a09ba0000000000000000000000000000000000000000000000000000000000001578000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc4a7418d68b7a77290a39c21043e264b958870d1386c10049d01aab41a62ff0",
      "signature": {
        "s": "0x73a597563f53b9614539c6973fa745f2ed0099c320b2097fa93ac3010a066fa4",
        "r": "0x8d5d52bbb82e11b542b89178aeea7a729833db7565f70b10ce2bac6b53fc3423",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9321151ad5cbe1a77bc7a774bc77ce0872de681bb9ccf029d4ce1c6375170600",
      "signature": {
        "s": "0x4637e15b164f7e7394df92fc48200a407b6efbb0d1777e13d5af6537ecbbd484",
        "r": "0x82e7e3ab8c601556d052096a8252fa81156259fb11548779e9f97deb080b9b6c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5496",
    "total": "5496"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5496",
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
            "amount": "679022"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOTU2YmM1ZC1kYzY0LTVkMzctODVhNy0wMmU4NmI4MmIwODQifQ==",
    "nonce": 2066,
    "balances": {
      "current": "10000001404254959",
      "previous": "10000001404260460"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61529b2c3f80269446d08dc69b341190601a09ba",
    "nonce": 20,
    "balances": {
      "current": "5496",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:14:09.698Z",
  "updated": "2020-05-22T08:14:09.769Z",
  "id": "5ec789d1e5756b00111b8212"
}
```
* *stageAmount*: `5496`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000001578000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000015780000000000000000000000000000000000000000000000000000000000001578dc4a7418d68b7a77290a39c21043e264b958870d1386c10049d01aab41a62ff08d5d52bbb82e11b542b89178aeea7a729833db7565f70b10ce2bac6b53fc342373a597563f53b9614539c6973fa745f2ed0099c320b2097fa93ac3010a066fa4000000000000000000000000000000000000000000000000000000000000001b9321151ad5cbe1a77bc7a774bc77ce0872de681bb9ccf029d4ce1c637517060082e7e3ab8c601556d052096a8252fa81156259fb11548779e9f97deb080b9b6c4637e15b164f7e7394df92fc48200a407b6efbb0d1777e13d5af6537ecbbd484000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000081200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3743aef000000000000000000000000000000000000000000000000002386f2c374506c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000050000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a5c6e00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f545532596d4d315a43316b597a59304c54566b4d7a63744f4456684e7930774d6d55344e6d49344d6d49774f44516966513d3d000000000000000000000000000000000000000000000000000000000000001400000000000000000000000061529b2c3f80269446d08dc69b341190601a09ba0000000000000000000000000000000000000000000000000000000000001578000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xdc4a7418d68b7a77290a39c21043e264b958870d1386c10049d01aab41a62ff0",
      "signature": {
        "s": "0x73a597563f53b9614539c6973fa745f2ed0099c320b2097fa93ac3010a066fa4",
        "r": "0x8d5d52bbb82e11b542b89178aeea7a729833db7565f70b10ce2bac6b53fc3423",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9321151ad5cbe1a77bc7a774bc77ce0872de681bb9ccf029d4ce1c6375170600",
      "signature": {
        "s": "0x4637e15b164f7e7394df92fc48200a407b6efbb0d1777e13d5af6537ecbbd484",
        "r": "0x82e7e3ab8c601556d052096a8252fa81156259fb11548779e9f97deb080b9b6c",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5496",
    "total": "5496"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5496",
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
            "amount": "679022"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "5"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyOTU2YmM1ZC1kYzY0LTVkMzctODVhNy0wMmU4NmI4MmIwODQifQ==",
    "nonce": 2066,
    "balances": {
      "current": "10000001404254959",
      "previous": "10000001404260460"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x61529b2c3f80269446d08dc69b341190601a09ba",
    "nonce": 20,
    "balances": {
      "current": "5496",
      "previous": "0"
    }
  },
  "blockNumber": "10114544",
  "created": "2020-05-22T08:14:09.698Z",
  "updated": "2020-05-22T08:14:09.769Z",
  "id": "5ec789d1e5756b00111b8212"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000015780000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `5496`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``