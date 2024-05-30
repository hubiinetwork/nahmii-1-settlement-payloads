# Settlement of HBT
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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000000000000000000000000000000000001bb0519163adfac9f3e4bd348b38a8fd70dbfd65d7463b76a13cdbd9ae70f2ead2a90a7cdff11d049a9bd46617896087e356b444809b34b3e0eaaa4264067a86f6339b5224fd7393d5f206a63ec048e05786c62d3b50993600d1a8c2347c301f350ffb48000000000000000000000000000000000000000000000000000000000000001b7cbc8ddf2ea7976cd9d56b0c8eda5628b16990d617427f9559e02bfe2b96c83e58adfea5a51b9a596cd351ec137fc023d828bdcc7ddbeebaf67ac0c4286a2b176f621c700eaae2ac748c8126af67c0fc0b91789d3b685798328ab8d23a9a946c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019fc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1725e2a34f73000000000000000000000000000000000000000000000000002e1725fe5ab7a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007169c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a54ea311e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d5446694f4449324d79307a4e7a67774c54566c4e546774596a49334d79316b4f574a685a6d52694f54646b4d47556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e2c1b339d65c989701e7f7be2e65803600eee691000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x63adfac9f3e4bd348b38a8fd70dbfd65d7463b76a13cdbd9ae70f2ead2a90a7c",
      "signature": {
        "s": "0x24fd7393d5f206a63ec048e05786c62d3b50993600d1a8c2347c301f350ffb48",
        "r": "0xdff11d049a9bd46617896087e356b444809b34b3e0eaaa4264067a86f6339b52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7cbc8ddf2ea7976cd9d56b0c8eda5628b16990d617427f9559e02bfe2b96c83e",
      "signature": {
        "s": "0x6f621c700eaae2ac748c8126af67c0fc0b91789d3b685798328ab8d23a9a946c",
        "r": "0x58adfea5a51b9a596cd351ec137fc023d828bdcc7ddbeebaf67ac0c4286a2b17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "464540049",
    "total": "464540049"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "464540049",
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
            "amount": "44374307102"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "464540"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MTFiODI2My0zNzgwLTVlNTgtYjI3My1kOWJhZmRiOTdkMGUifQ==",
    "nonce": 6652,
    "balances": {
      "current": "12973300412272499",
      "previous": "12973300877277088"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2c1b339d65c989701e7f7be2e65803600eee691",
    "nonce": 22,
    "balances": {
      "current": "464540049",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:49.333Z",
  "updated": "2020-05-22T08:50:49.411Z",
  "id": "5ec79269e5756b00111b87ef"
}
```
* *stageAmount*: `464540049`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000000000000000000000000000000000001bb0519163adfac9f3e4bd348b38a8fd70dbfd65d7463b76a13cdbd9ae70f2ead2a90a7cdff11d049a9bd46617896087e356b444809b34b3e0eaaa4264067a86f6339b5224fd7393d5f206a63ec048e05786c62d3b50993600d1a8c2347c301f350ffb48000000000000000000000000000000000000000000000000000000000000001b7cbc8ddf2ea7976cd9d56b0c8eda5628b16990d617427f9559e02bfe2b96c83e58adfea5a51b9a596cd351ec137fc023d828bdcc7ddbeebaf67ac0c4286a2b176f621c700eaae2ac748c8126af67c0fc0b91789d3b685798328ab8d23a9a946c000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a5697000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000019fc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e1725e2a34f73000000000000000000000000000000000000000000000000002e1725fe5ab7a000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000007169c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a54ea311e000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d5446694f4449324d79307a4e7a67774c54566c4e546774596a49334d79316b4f574a685a6d52694f54646b4d47556966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e2c1b339d65c989701e7f7be2e65803600eee691000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x63adfac9f3e4bd348b38a8fd70dbfd65d7463b76a13cdbd9ae70f2ead2a90a7c",
      "signature": {
        "s": "0x24fd7393d5f206a63ec048e05786c62d3b50993600d1a8c2347c301f350ffb48",
        "r": "0xdff11d049a9bd46617896087e356b444809b34b3e0eaaa4264067a86f6339b52",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7cbc8ddf2ea7976cd9d56b0c8eda5628b16990d617427f9559e02bfe2b96c83e",
      "signature": {
        "s": "0x6f621c700eaae2ac748c8126af67c0fc0b91789d3b685798328ab8d23a9a946c",
        "r": "0x58adfea5a51b9a596cd351ec137fc023d828bdcc7ddbeebaf67ac0c4286a2b17",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "464540049",
    "total": "464540049"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "464540049",
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
            "amount": "44374307102"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "464540"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1MTFiODI2My0zNzgwLTVlNTgtYjI3My1kOWJhZmRiOTdkMGUifQ==",
    "nonce": 6652,
    "balances": {
      "current": "12973300412272499",
      "previous": "12973300877277088"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe2c1b339d65c989701e7f7be2e65803600eee691",
    "nonce": 22,
    "balances": {
      "current": "464540049",
      "previous": "0"
    }
  },
  "blockNumber": "10114711",
  "created": "2020-05-22T08:50:49.333Z",
  "updated": "2020-05-22T08:50:49.411Z",
  "id": "5ec79269e5756b00111b87ef"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001bb05191000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `464540049`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`