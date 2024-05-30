# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x916469917db7c00f6d9Fc9701d5E56878ab729f3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002204c000000000000000000000000000000000000000000000000000000000002204c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002204c000000000000000000000000000000000000000000000000000000000002204cff9a84b6bb3ade21d4dfbd81853caedc42a3c874113c9c80d6884de748b9b890f69c5e8e679492c5a9ad3d30909480f40363d5fed125123da62f1d97663a0d7c4ae349c9832f4e4148028e196e741f3d784b8c3b783a04990a854118f0806d85000000000000000000000000000000000000000000000000000000000000001cdff11bb14ef2dd30fddd01db35992c732b3d085ebf61d15bdd8f477d6a34d50c203b7699c2991e850bea29f13c486e750d746579dd0f915ef6a577c8b17414ef6fd802a43919c1fb7271f115b59b8e1ee3fd4db61b508b43be160dc9c760b8f4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004b600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7f9009e000000000000000000000000000000000000000000000000002386f2c7fb217500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000935c100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5441774d5467324e6930305a6a64694c5455324e6d59744f574932595330794f4745774e7a4d345a57593559544d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000916469917db7c00f6d9fc9701d5e56878ab729f3000000000000000000000000000000000000000000000000000000000002204c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff9a84b6bb3ade21d4dfbd81853caedc42a3c874113c9c80d6884de748b9b890",
      "signature": {
        "s": "0x4ae349c9832f4e4148028e196e741f3d784b8c3b783a04990a854118f0806d85",
        "r": "0xf69c5e8e679492c5a9ad3d30909480f40363d5fed125123da62f1d97663a0d7c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdff11bb14ef2dd30fddd01db35992c732b3d085ebf61d15bdd8f477d6a34d50c",
      "signature": {
        "s": "0x6fd802a43919c1fb7271f115b59b8e1ee3fd4db61b508b43be160dc9c760b8f4",
        "r": "0x203b7699c2991e850bea29f13c486e750d746579dd0f915ef6a577c8b17414ef",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "139340",
    "total": "139340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139340",
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
            "amount": "603585"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "139"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTAwMTg2Ni00ZjdiLTU2NmYtOWI2YS0yOGEwNzM4ZWY5YTMifQ==",
    "nonce": 1206,
    "balances": {
      "current": "10000001480065182",
      "previous": "10000001480204661"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x916469917db7c00f6d9fc9701d5e56878ab729f3",
    "nonce": 20,
    "balances": {
      "current": "139340",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:36.252Z",
  "updated": "2020-05-22T08:07:36.326Z",
  "id": "5ec78848e5756b00111b80fa"
}
```
* *stageAmount*: `139340`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002204c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002204c000000000000000000000000000000000000000000000000000000000002204cff9a84b6bb3ade21d4dfbd81853caedc42a3c874113c9c80d6884de748b9b890f69c5e8e679492c5a9ad3d30909480f40363d5fed125123da62f1d97663a0d7c4ae349c9832f4e4148028e196e741f3d784b8c3b783a04990a854118f0806d85000000000000000000000000000000000000000000000000000000000000001cdff11bb14ef2dd30fddd01db35992c732b3d085ebf61d15bdd8f477d6a34d50c203b7699c2991e850bea29f13c486e750d746579dd0f915ef6a577c8b17414ef6fd802a43919c1fb7271f115b59b8e1ee3fd4db61b508b43be160dc9c760b8f4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d9000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004b600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7f9009e000000000000000000000000000000000000000000000000002386f2c7fb217500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000935c100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5441774d5467324e6930305a6a64694c5455324e6d59744f574932595330794f4745774e7a4d345a57593559544d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000916469917db7c00f6d9fc9701d5e56878ab729f3000000000000000000000000000000000000000000000000000000000002204c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xff9a84b6bb3ade21d4dfbd81853caedc42a3c874113c9c80d6884de748b9b890",
      "signature": {
        "s": "0x4ae349c9832f4e4148028e196e741f3d784b8c3b783a04990a854118f0806d85",
        "r": "0xf69c5e8e679492c5a9ad3d30909480f40363d5fed125123da62f1d97663a0d7c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xdff11bb14ef2dd30fddd01db35992c732b3d085ebf61d15bdd8f477d6a34d50c",
      "signature": {
        "s": "0x6fd802a43919c1fb7271f115b59b8e1ee3fd4db61b508b43be160dc9c760b8f4",
        "r": "0x203b7699c2991e850bea29f13c486e750d746579dd0f915ef6a577c8b17414ef",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "139340",
    "total": "139340"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "139340",
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
            "amount": "603585"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "139"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTAwMTg2Ni00ZjdiLTU2NmYtOWI2YS0yOGEwNzM4ZWY5YTMifQ==",
    "nonce": 1206,
    "balances": {
      "current": "10000001480065182",
      "previous": "10000001480204661"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x916469917db7c00f6d9fc9701d5e56878ab729f3",
    "nonce": 20,
    "balances": {
      "current": "139340",
      "previous": "0"
    }
  },
  "blockNumber": "10114521",
  "created": "2020-05-22T08:07:36.252Z",
  "updated": "2020-05-22T08:07:36.326Z",
  "id": "5ec78848e5756b00111b80fa"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002204c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `139340`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``