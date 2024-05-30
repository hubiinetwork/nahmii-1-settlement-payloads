# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe2c1b339D65C989701E7f7BE2e65803600eEe691`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000001923000000000000000000000000000000000000000000000000000000000000192300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001923000000000000000000000000000000000000000000000000000000000000192397e4e7b6b8acc404bae255c4d445180605c27e1c8a33ccb124f0e20d9c512af15dabba4622604d8b097627fdc91eb3b4cc1b5da126c4c28f20f3b86788628a9a02ad241d19447358ebb846a20f5d8b4055c74f7ae7a79e9c329ca29498b86450000000000000000000000000000000000000000000000000000000000000001c041032a6571671f65365e282b2de19f6c9b6f8845ed6e7e2a4104728bd5f4b23a92bed286bd0858008db0fb92199886601d50c7b0bf299d93a82c81db0473e9955bf4ad9d88de11b0e895076885584a22058cf92dd0ebae3a2fee51dd513bdf6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000053e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74f2df4000000000000000000000000000000000000000000000000002386f2c74f471d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009610100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596d45774d3259304d4330344e4463354c545578596d4974596d55354d5330355a6a49784d5455344d6a45774e44676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e2c1b339d65c989701e7f7be2e65803600eee6910000000000000000000000000000000000000000000000000000000000001923000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97e4e7b6b8acc404bae255c4d445180605c27e1c8a33ccb124f0e20d9c512af1",
      "signature": {
        "s": "0x02ad241d19447358ebb846a20f5d8b4055c74f7ae7a79e9c329ca29498b86450",
        "r": "0x5dabba4622604d8b097627fdc91eb3b4cc1b5da126c4c28f20f3b86788628a9a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x041032a6571671f65365e282b2de19f6c9b6f8845ed6e7e2a4104728bd5f4b23",
      "signature": {
        "s": "0x55bf4ad9d88de11b0e895076885584a22058cf92dd0ebae3a2fee51dd513bdf6",
        "r": "0xa92bed286bd0858008db0fb92199886601d50c7b0bf299d93a82c81db0473e99",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6435",
    "total": "6435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6435",
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
            "amount": "614657"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYmEwM2Y0MC04NDc5LTUxYmItYmU5MS05ZjIxMTU4MjEwNDgifQ==",
    "nonce": 1342,
    "balances": {
      "current": "10000001468935668",
      "previous": "10000001468942109"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2c1b339d65c989701e7f7be2e65803600eee691",
    "nonce": 20,
    "balances": {
      "current": "6435",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:40.656Z",
  "updated": "2020-05-22T08:08:41.735Z",
  "id": "5ec78888005df800101bc3e5"
}
```
* *stageAmount*: `6435`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000192300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000001923000000000000000000000000000000000000000000000000000000000000192397e4e7b6b8acc404bae255c4d445180605c27e1c8a33ccb124f0e20d9c512af15dabba4622604d8b097627fdc91eb3b4cc1b5da126c4c28f20f3b86788628a9a02ad241d19447358ebb846a20f5d8b4055c74f7ae7a79e9c329ca29498b86450000000000000000000000000000000000000000000000000000000000000001c041032a6571671f65365e282b2de19f6c9b6f8845ed6e7e2a4104728bd5f4b23a92bed286bd0858008db0fb92199886601d50c7b0bf299d93a82c81db0473e9955bf4ad9d88de11b0e895076885584a22058cf92dd0ebae3a2fee51dd513bdf6000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000053e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74f2df4000000000000000000000000000000000000000000000000002386f2c74f471d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009610100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a69596d45774d3259304d4330344e4463354c545578596d4974596d55354d5330355a6a49784d5455344d6a45774e44676966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e2c1b339d65c989701e7f7be2e65803600eee6910000000000000000000000000000000000000000000000000000000000001923000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x97e4e7b6b8acc404bae255c4d445180605c27e1c8a33ccb124f0e20d9c512af1",
      "signature": {
        "s": "0x02ad241d19447358ebb846a20f5d8b4055c74f7ae7a79e9c329ca29498b86450",
        "r": "0x5dabba4622604d8b097627fdc91eb3b4cc1b5da126c4c28f20f3b86788628a9a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x041032a6571671f65365e282b2de19f6c9b6f8845ed6e7e2a4104728bd5f4b23",
      "signature": {
        "s": "0x55bf4ad9d88de11b0e895076885584a22058cf92dd0ebae3a2fee51dd513bdf6",
        "r": "0xa92bed286bd0858008db0fb92199886601d50c7b0bf299d93a82c81db0473e99",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6435",
    "total": "6435"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6435",
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
            "amount": "614657"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "6"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJiYmEwM2Y0MC04NDc5LTUxYmItYmU5MS05ZjIxMTU4MjEwNDgifQ==",
    "nonce": 1342,
    "balances": {
      "current": "10000001468935668",
      "previous": "10000001468942109"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2c1b339d65c989701e7f7be2e65803600eee691",
    "nonce": 20,
    "balances": {
      "current": "6435",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:40.656Z",
  "updated": "2020-05-22T08:08:41.735Z",
  "id": "5ec78888005df800101bc3e5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000019230000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `6435`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``