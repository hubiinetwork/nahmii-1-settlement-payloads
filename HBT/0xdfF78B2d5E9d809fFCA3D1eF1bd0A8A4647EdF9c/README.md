# Settlement of HBT
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdfF78B2d5E9d809fFCA3D1eF1bd0A8A4647EdF9c`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000000000000000000000000000000000001842552c2c69bf5412e76be7dabfa293d874879c788d89e8352d002be16f60f624b4fbb30fad569847de97a78544e9e5ddf7c55f18fefb3319985c2e703ea9f9bdf1aaf25df30ac6bf5e458ef158cd245d3681e51b12b177f3a537d2fae6971d52a90919000000000000000000000000000000000000000000000000000000000000001b81b897c17f27245a29f694f75543b5b79b65ec471049d923404074c127d599d01e0244795d7ca0362addd79a86d41b167b5c5fd936851b6e65e1ede24a0f3e0308f7e252db17c41a2fe00b399b2d85f96810195c3832828e7b0c6ee5af7260f3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56af00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c8800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13515205edce000000000000000000000000000000000000000000000000002e13516a4e78d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000635d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4fb04a67000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f4745775a5456694d6930314e5755324c5456684f4459744f544d334f533030596a6b7a4e546b784e4759774e54516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2c69bf5412e76be7dabfa293d874879c788d89e8352d002be16f60f624b4fbb3",
      "signature": {
        "s": "0x5df30ac6bf5e458ef158cd245d3681e51b12b177f3a537d2fae6971d52a90919",
        "r": "0x0fad569847de97a78544e9e5ddf7c55f18fefb3319985c2e703ea9f9bdf1aaf2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x81b897c17f27245a29f694f75543b5b79b65ec471049d923404074c127d599d0",
      "signature": {
        "s": "0x08f7e252db17c41a2fe00b399b2d85f96810195c3832828e7b0c6ee5af7260f3",
        "r": "0x1e0244795d7ca0362addd79a86d41b167b5c5fd936851b6e65e1ede24a0f3e03",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "407000364",
    "total": "407000364"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "407000364",
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
            "amount": "48581593703"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "407000"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOGEwZTViMi01NWU2LTVhODYtOTM3OS00YjkzNTkxNGYwNTQifQ==",
    "nonce": 7304,
    "balances": {
      "current": "12969088918089166",
      "previous": "12969089325496530"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c",
    "nonce": 22,
    "balances": {
      "current": "407000364",
      "previous": "0"
    }
  },
  "blockNumber": "10114735",
  "created": "2020-05-22T08:55:47.479Z",
  "updated": "2020-05-22T08:55:47.546Z",
  "id": "5ec79393e5756b00111b88b6"
}
```
* *stageAmount*: `407000364`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000000000000000000000000000000000001842552c2c69bf5412e76be7dabfa293d874879c788d89e8352d002be16f60f624b4fbb30fad569847de97a78544e9e5ddf7c55f18fefb3319985c2e703ea9f9bdf1aaf25df30ac6bf5e458ef158cd245d3681e51b12b177f3a537d2fae6971d52a90919000000000000000000000000000000000000000000000000000000000000001b81b897c17f27245a29f694f75543b5b79b65ec471049d923404074c127d599d01e0244795d7ca0362addd79a86d41b167b5c5fd936851b6e65e1ede24a0f3e0308f7e252db17c41a2fe00b399b2d85f96810195c3832828e7b0c6ee5af7260f3000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a56af00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000001c8800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002e13515205edce000000000000000000000000000000000000000000000000002e13516a4e78d200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000635d8000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000b4fb04a67000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f4745775a5456694d6930314e5755324c5456684f4459744f544d334f533030596a6b7a4e546b784e4759774e54516966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000dff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2c69bf5412e76be7dabfa293d874879c788d89e8352d002be16f60f624b4fbb3",
      "signature": {
        "s": "0x5df30ac6bf5e458ef158cd245d3681e51b12b177f3a537d2fae6971d52a90919",
        "r": "0x0fad569847de97a78544e9e5ddf7c55f18fefb3319985c2e703ea9f9bdf1aaf2",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x81b897c17f27245a29f694f75543b5b79b65ec471049d923404074c127d599d0",
      "signature": {
        "s": "0x08f7e252db17c41a2fe00b399b2d85f96810195c3832828e7b0c6ee5af7260f3",
        "r": "0x1e0244795d7ca0362addd79a86d41b167b5c5fd936851b6e65e1ede24a0f3e03",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "407000364",
    "total": "407000364"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "407000364",
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
            "amount": "48581593703"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0xdd6c68bb32462e01705011a4e2ad1a60740f217f",
          "id": "0"
        },
        "amount": "407000"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwOGEwZTViMi01NWU2LTVhODYtOTM3OS00YjkzNTkxNGYwNTQifQ==",
    "nonce": 7304,
    "balances": {
      "current": "12969088918089166",
      "previous": "12969089325496530"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdff78b2d5e9d809ffca3d1ef1bd0a8a4647edf9c",
    "nonce": 22,
    "balances": {
      "current": "407000364",
      "previous": "0"
    }
  },
  "blockNumber": "10114735",
  "created": "2020-05-22T08:55:47.479Z",
  "updated": "2020-05-22T08:55:47.546Z",
  "id": "5ec79393e5756b00111b88b6"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000001842552c000000000000000000000000dd6c68bb32462e01705011a4e2ad1a60740f217f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `407000364`
* *currencyCt*: `0xDd6C68bb32462e01705011a4e2Ad1a60740f217F`
* *currencyId*: `0`
* *standard*: `ERC20`