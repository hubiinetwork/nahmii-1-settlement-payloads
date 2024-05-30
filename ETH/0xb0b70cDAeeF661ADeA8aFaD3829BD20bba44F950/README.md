# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb0b70cDAeeF661ADeA8aFaD3829BD20bba44F950`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000015eb90000000000000000000000000000000000000000000000000000000000015eb900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000015eb90000000000000000000000000000000000000000000000000000000000015eb95a0582e008e3d640c2f829d0cdf65683e862912ae0ae031806be5345b5f6081615a7fc1bb967c366e6837fde5b70c0c7bf81da18a60190b42acb4f6d34c6ac904f27469ef8dc013d8fd5f04160d0fa91b5951a3f0387f4abcf6c48c51e2aac6b000000000000000000000000000000000000000000000000000000000000001ca3d68e8573c5b1a266b57da0ac5bbb5ea554bf69bde05a276d27878aaf2c297f03b6800324888ad2256f489fdb004a5290a71d9c013c6e6a03fd560715f8e066438679cad1183cfaab29163e3d724e3599202fc52407e95d9d34e83b224be68e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74b0070000000000000000000000000000000000000000000000000002386f2c74c5f8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009620f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e44426a4d574d354e43316a4f5445334c545668595441744f4459344e6931685a544a69596a59354d7a56684d6a416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b0b70cdaeef661adea8afad3829bd20bba44f9500000000000000000000000000000000000000000000000000000000000015eb9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5a0582e008e3d640c2f829d0cdf65683e862912ae0ae031806be5345b5f60816",
      "signature": {
        "s": "0x4f27469ef8dc013d8fd5f04160d0fa91b5951a3f0387f4abcf6c48c51e2aac6b",
        "r": "0x15a7fc1bb967c366e6837fde5b70c0c7bf81da18a60190b42acb4f6d34c6ac90",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa3d68e8573c5b1a266b57da0ac5bbb5ea554bf69bde05a276d27878aaf2c297f",
      "signature": {
        "s": "0x438679cad1183cfaab29163e3d724e3599202fc52407e95d9d34e83b224be68e",
        "r": "0x03b6800324888ad2256f489fdb004a5290a71d9c013c6e6a03fd560715f8e066",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "89785",
    "total": "89785"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "89785",
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
            "amount": "614927"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "89"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NDBjMWM5NC1jOTE3LTVhYTAtODY4Ni1hZTJiYjY5MzVhMjAifQ==",
    "nonce": 1350,
    "balances": {
      "current": "10000001468661872",
      "previous": "10000001468751746"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb0b70cdaeef661adea8afad3829bd20bba44f950",
    "nonce": 20,
    "balances": {
      "current": "89785",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:43.107Z",
  "updated": "2020-05-22T08:08:43.189Z",
  "id": "5ec7888be5756b00111b811f"
}
```
* *stageAmount*: `89785`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000015eb900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000015eb90000000000000000000000000000000000000000000000000000000000015eb95a0582e008e3d640c2f829d0cdf65683e862912ae0ae031806be5345b5f6081615a7fc1bb967c366e6837fde5b70c0c7bf81da18a60190b42acb4f6d34c6ac904f27469ef8dc013d8fd5f04160d0fa91b5951a3f0387f4abcf6c48c51e2aac6b000000000000000000000000000000000000000000000000000000000000001ca3d68e8573c5b1a266b57da0ac5bbb5ea554bf69bde05a276d27878aaf2c297f03b6800324888ad2256f489fdb004a5290a71d9c013c6e6a03fd560715f8e066438679cad1183cfaab29163e3d724e3599202fc52407e95d9d34e83b224be68e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000054600000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c74b0070000000000000000000000000000000000000000000000000002386f2c74c5f8200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000005900000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009620f00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354e44426a4d574d354e43316a4f5445334c545668595441744f4459344e6931685a544a69596a59354d7a56684d6a416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b0b70cdaeef661adea8afad3829bd20bba44f9500000000000000000000000000000000000000000000000000000000000015eb9000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5a0582e008e3d640c2f829d0cdf65683e862912ae0ae031806be5345b5f60816",
      "signature": {
        "s": "0x4f27469ef8dc013d8fd5f04160d0fa91b5951a3f0387f4abcf6c48c51e2aac6b",
        "r": "0x15a7fc1bb967c366e6837fde5b70c0c7bf81da18a60190b42acb4f6d34c6ac90",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xa3d68e8573c5b1a266b57da0ac5bbb5ea554bf69bde05a276d27878aaf2c297f",
      "signature": {
        "s": "0x438679cad1183cfaab29163e3d724e3599202fc52407e95d9d34e83b224be68e",
        "r": "0x03b6800324888ad2256f489fdb004a5290a71d9c013c6e6a03fd560715f8e066",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "89785",
    "total": "89785"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "89785",
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
            "amount": "614927"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "89"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5NDBjMWM5NC1jOTE3LTVhYTAtODY4Ni1hZTJiYjY5MzVhMjAifQ==",
    "nonce": 1350,
    "balances": {
      "current": "10000001468661872",
      "previous": "10000001468751746"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb0b70cdaeef661adea8afad3829bd20bba44f950",
    "nonce": 20,
    "balances": {
      "current": "89785",
      "previous": "0"
    }
  },
  "blockNumber": "10114525",
  "created": "2020-05-22T08:08:43.107Z",
  "updated": "2020-05-22T08:08:43.189Z",
  "id": "5ec7888be5756b00111b811f"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000015eb90000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `89785`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``