# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x57746012680D44b2EE75C7A539596aEf0Ab1c9a9`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000020e100000000000000000000000000000000000000000000000000000000000020e1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000020e100000000000000000000000000000000000000000000000000000000000020e10a781b68920ac6661ad035d207e8a38ac6af561a118f6cd3a15852fd56bcde16fbb218ec16e618fae5e8b0a6bc4ff69c62f3a8a0bcffaadeb74a109bc57710d886d94e4213da4e4b3486e7021bf0d6ddf1319eabbc74ec369fa7d73f05cfdfefc000000000000000000000000000000000000000000000000000000000000001bb8b6438f862be37dfe8aec3174e13fa572f05d036ff6b3e189bf89229a87bc09ca2c3c5b5f4177f271c78bd733113911d1173beb89750a5d69ad155fa8e762e95223ec177ef8aaf27790ee91b0e89639d8b8c8d5c2862d63c943489bb43766c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d15be50e000000000000000000000000000000000000000000000000002386f2d15df3a400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006d05300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a54686c4e7a63354f5330344e5749344c5455304d474d744f544e684d4330314f574e684e57526a4f44686d4f444d6966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000057746012680d44b2ee75c7a539596aef0ab1c9a90000000000000000000000000000000000000000000000000000000000020e10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa781b68920ac6661ad035d207e8a38ac6af561a118f6cd3a15852fd56bcde16f",
      "signature": {
        "s": "0x6d94e4213da4e4b3486e7021bf0d6ddf1319eabbc74ec369fa7d73f05cfdfefc",
        "r": "0xbb218ec16e618fae5e8b0a6bc4ff69c62f3a8a0bcffaadeb74a109bc57710d88",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb8b6438f862be37dfe8aec3174e13fa572f05d036ff6b3e189bf89229a87bc09",
      "signature": {
        "s": "0x5223ec177ef8aaf27790ee91b0e89639d8b8c8d5c2862d63c943489bb43766c4",
        "r": "0xca2c3c5b5f4177f271c78bd733113911d1173beb89750a5d69ad155fa8e762e9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "134672",
    "total": "134672"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "134672",
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
            "amount": "446547"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "134"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZThlNzc5OS04NWI4LTU0MGMtOTNhMC01OWNhNWRjODhmODMifQ==",
    "nonce": 169,
    "balances": {
      "current": "10000001637541134",
      "previous": "10000001637675940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57746012680d44b2ee75c7a539596aef0ab1c9a9",
    "nonce": 21,
    "balances": {
      "current": "134672",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:10.734Z",
  "updated": "2020-05-22T08:00:10.820Z",
  "id": "5ec7868ae5756b00111b7fa6"
}
```
* *stageAmount*: `134672`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000020e1000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000020e100000000000000000000000000000000000000000000000000000000000020e10a781b68920ac6661ad035d207e8a38ac6af561a118f6cd3a15852fd56bcde16fbb218ec16e618fae5e8b0a6bc4ff69c62f3a8a0bcffaadeb74a109bc57710d886d94e4213da4e4b3486e7021bf0d6ddf1319eabbc74ec369fa7d73f05cfdfefc000000000000000000000000000000000000000000000000000000000000001bb8b6438f862be37dfe8aec3174e13fa572f05d036ff6b3e189bf89229a87bc09ca2c3c5b5f4177f271c78bd733113911d1173beb89750a5d69ad155fa8e762e95223ec177ef8aaf27790ee91b0e89639d8b8c8d5c2862d63c943489bb43766c4000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55bc000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000000a900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2d15be50e000000000000000000000000000000000000000000000000002386f2d15df3a400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000008600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000006d05300000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a54686c4e7a63354f5330344e5749344c5455304d474d744f544e684d4330314f574e684e57526a4f44686d4f444d6966513d3d000000000000000000000000000000000000000000000000000000000000001500000000000000000000000057746012680d44b2ee75c7a539596aef0ab1c9a90000000000000000000000000000000000000000000000000000000000020e10000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa781b68920ac6661ad035d207e8a38ac6af561a118f6cd3a15852fd56bcde16f",
      "signature": {
        "s": "0x6d94e4213da4e4b3486e7021bf0d6ddf1319eabbc74ec369fa7d73f05cfdfefc",
        "r": "0xbb218ec16e618fae5e8b0a6bc4ff69c62f3a8a0bcffaadeb74a109bc57710d88",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb8b6438f862be37dfe8aec3174e13fa572f05d036ff6b3e189bf89229a87bc09",
      "signature": {
        "s": "0x5223ec177ef8aaf27790ee91b0e89639d8b8c8d5c2862d63c943489bb43766c4",
        "r": "0xca2c3c5b5f4177f271c78bd733113911d1173beb89750a5d69ad155fa8e762e9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "134672",
    "total": "134672"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "134672",
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
            "amount": "446547"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "134"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI4ZThlNzc5OS04NWI4LTU0MGMtOTNhMC01OWNhNWRjODhmODMifQ==",
    "nonce": 169,
    "balances": {
      "current": "10000001637541134",
      "previous": "10000001637675940"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57746012680d44b2ee75c7a539596aef0ab1c9a9",
    "nonce": 21,
    "balances": {
      "current": "134672",
      "previous": "0"
    }
  },
  "blockNumber": "10114492",
  "created": "2020-05-22T08:00:10.734Z",
  "updated": "2020-05-22T08:00:10.820Z",
  "id": "5ec7868ae5756b00111b7fa6"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000020e100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `134672`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``