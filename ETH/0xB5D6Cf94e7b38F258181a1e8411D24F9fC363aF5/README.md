# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB5D6Cf94e7b38F258181a1e8411D24F9fC363aF5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000327d000000000000000000000000000000000000000000000000000000000000327d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000327d000000000000000000000000000000000000000000000000000000000000327d060fee37ac05225896da4bab7f1533ade0dc46944922b933628a69fbf4f36814e37e5d54f28a9e87736fa99ed358d49e9d9ec0442b07ff46b90027725de733bf36b1df1b1bac87b9b1483ec49eff285721bf02c5800cb2a3442187d9ca5b8a4be000000000000000000000000000000000000000000000000000000000000001b8f5075da9c7e69540e20bae9393d4415a4d6f652a207d57c2469cf61ed56446d4374260be04c87ffc60e26e6e96fbd67433d5283c65237217d1395e4fb38114d0f6b6a3ab705b811b26c4fc7cff5bc5cd2ce34097dd93bc714f6ffc8ce324b27000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000a500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d1c36ead000000000000000000000000000000000000000000000000002386f2d1c6974b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000ce00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006b5d900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a41314d7a68694e6931684e574a6c4c54566a4e325174596d4e694e5330774f44517a5a6d59324f4746694d6d556966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000b5d6cf94e7b38f258181a1e8411d24f9fc363af500000000000000000000000000000000000000000000000000000000000327d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60fee37ac05225896da4bab7f1533ade0dc46944922b933628a69fbf4f36814e",
      "signature": {
        "s": "0x6b1df1b1bac87b9b1483ec49eff285721bf02c5800cb2a3442187d9ca5b8a4be",
        "r": "0x37e5d54f28a9e87736fa99ed358d49e9d9ec0442b07ff46b90027725de733bf3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f5075da9c7e69540e20bae9393d4415a4d6f652a207d57c2469cf61ed56446d",
      "signature": {
        "s": "0x0f6b6a3ab705b811b26c4fc7cff5bc5cd2ce34097dd93bc714f6ffc8ce324b27",
        "r": "0x4374260be04c87ffc60e26e6e96fbd67433d5283c65237217d1395e4fb38114d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "206800",
    "total": "206800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "206800",
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
            "amount": "439769"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "206"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzA1MzhiNi1hNWJlLTVjN2QtYmNiNS0wODQzZmY2OGFiMmUifQ==",
    "nonce": 165,
    "balances": {
      "current": "10000001644326573",
      "previous": "10000001644533579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb5d6cf94e7b38f258181a1e8411d24f9fc363af5",
    "nonce": 10,
    "balances": {
      "current": "206800",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:08.870Z",
  "updated": "2020-05-22T08:00:09.962Z",
  "id": "5ec78688005df800101bc248"
}
```
* *stageAmount*: `206800`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000327d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000327d000000000000000000000000000000000000000000000000000000000000327d060fee37ac05225896da4bab7f1533ade0dc46944922b933628a69fbf4f36814e37e5d54f28a9e87736fa99ed358d49e9d9ec0442b07ff46b90027725de733bf36b1df1b1bac87b9b1483ec49eff285721bf02c5800cb2a3442187d9ca5b8a4be000000000000000000000000000000000000000000000000000000000000001b8f5075da9c7e69540e20bae9393d4415a4d6f652a207d57c2469cf61ed56446d4374260be04c87ffc60e26e6e96fbd67433d5283c65237217d1395e4fb38114d0f6b6a3ab705b811b26c4fc7cff5bc5cd2ce34097dd93bc714f6ffc8ce324b27000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000a500000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d1c36ead000000000000000000000000000000000000000000000000002386f2d1c6974b00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000ce00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006b5d900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a41314d7a68694e6931684e574a6c4c54566a4e325174596d4e694e5330774f44517a5a6d59324f4746694d6d556966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000b5d6cf94e7b38f258181a1e8411d24f9fc363af500000000000000000000000000000000000000000000000000000000000327d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x60fee37ac05225896da4bab7f1533ade0dc46944922b933628a69fbf4f36814e",
      "signature": {
        "s": "0x6b1df1b1bac87b9b1483ec49eff285721bf02c5800cb2a3442187d9ca5b8a4be",
        "r": "0x37e5d54f28a9e87736fa99ed358d49e9d9ec0442b07ff46b90027725de733bf3",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x8f5075da9c7e69540e20bae9393d4415a4d6f652a207d57c2469cf61ed56446d",
      "signature": {
        "s": "0x0f6b6a3ab705b811b26c4fc7cff5bc5cd2ce34097dd93bc714f6ffc8ce324b27",
        "r": "0x4374260be04c87ffc60e26e6e96fbd67433d5283c65237217d1395e4fb38114d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "206800",
    "total": "206800"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "206800",
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
            "amount": "439769"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "206"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmMzA1MzhiNi1hNWJlLTVjN2QtYmNiNS0wODQzZmY2OGFiMmUifQ==",
    "nonce": 165,
    "balances": {
      "current": "10000001644326573",
      "previous": "10000001644533579"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb5d6cf94e7b38f258181a1e8411d24f9fc363af5",
    "nonce": 10,
    "balances": {
      "current": "206800",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:08.870Z",
  "updated": "2020-05-22T08:00:09.962Z",
  "id": "5ec78688005df800101bc248"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000327d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `206800`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``