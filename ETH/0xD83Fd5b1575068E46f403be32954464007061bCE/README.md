# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD83Fd5b1575068E46f403be32954464007061bCE`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000011e4c0000000000000000000000000000000000000000000000000000000000011e4c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000011e4c0000000000000000000000000000000000000000000000000000000000011e4c9a3cd32711d2ee75011436d94f838f74c40ba382a6182aecbf4eae769da11f26ae93fb594a9f6c1adadf955749fae391eaecfc15ce2e46de596850cecf9fd7207a86efb1f46f0126d5939d0bc23b0741d016f36787466287253abecf6a3df8e5000000000000000000000000000000000000000000000000000000000000001c11380942417d5b58e873d717374a055c948e65f10e8dec93df96e776d180cabefd1282c65b5ce9aef90b8ec1f1a319f30f5a7196cb504e6641e8aae6154345417514649efeb2ad95de62cd280852b5c1d19e1bf776b945e47a1d0d2adcd7c92d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000073800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c420be78000000000000000000000000000000000000000000000000002386f2c421dd0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a30a800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a474a694d3251304d7930344f474d304c5455344d7a41744f4463314d4330334f444d79595759324e4449785957456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d83fd5b1575068e46f403be32954464007061bce0000000000000000000000000000000000000000000000000000000000011e4c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a3cd32711d2ee75011436d94f838f74c40ba382a6182aecbf4eae769da11f26",
      "signature": {
        "s": "0x7a86efb1f46f0126d5939d0bc23b0741d016f36787466287253abecf6a3df8e5",
        "r": "0xae93fb594a9f6c1adadf955749fae391eaecfc15ce2e46de596850cecf9fd720",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x11380942417d5b58e873d717374a055c948e65f10e8dec93df96e776d180cabe",
      "signature": {
        "s": "0x7514649efeb2ad95de62cd280852b5c1d19e1bf776b945e47a1d0d2adcd7c92d",
        "r": "0xfd1282c65b5ce9aef90b8ec1f1a319f30f5a7196cb504e6641e8aae615434541",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "73292",
    "total": "73292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "73292",
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
            "amount": "667816"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "73"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZGJiM2Q0My04OGM0LTU4MzAtODc1MC03ODMyYWY2NDIxYWEifQ==",
    "nonce": 1848,
    "balances": {
      "current": "10000001415560824",
      "previous": "10000001415634189"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd83fd5b1575068e46f403be32954464007061bce",
    "nonce": 20,
    "balances": {
      "current": "73292",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:30.847Z",
  "updated": "2020-05-22T08:12:31.940Z",
  "id": "5ec7896e005df800101bc48e"
}
```
* *stageAmount*: `73292`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000011e4c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000011e4c0000000000000000000000000000000000000000000000000000000000011e4c9a3cd32711d2ee75011436d94f838f74c40ba382a6182aecbf4eae769da11f26ae93fb594a9f6c1adadf955749fae391eaecfc15ce2e46de596850cecf9fd7207a86efb1f46f0126d5939d0bc23b0741d016f36787466287253abecf6a3df8e5000000000000000000000000000000000000000000000000000000000000001c11380942417d5b58e873d717374a055c948e65f10e8dec93df96e776d180cabefd1282c65b5ce9aef90b8ec1f1a319f30f5a7196cb504e6641e8aae6154345417514649efeb2ad95de62cd280852b5c1d19e1bf776b945e47a1d0d2adcd7c92d000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55ed0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000073800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c420be78000000000000000000000000000000000000000000000000002386f2c421dd0d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000490000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a30a800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a474a694d3251304d7930344f474d304c5455344d7a41744f4463314d4330334f444d79595759324e4449785957456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d83fd5b1575068e46f403be32954464007061bce0000000000000000000000000000000000000000000000000000000000011e4c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9a3cd32711d2ee75011436d94f838f74c40ba382a6182aecbf4eae769da11f26",
      "signature": {
        "s": "0x7a86efb1f46f0126d5939d0bc23b0741d016f36787466287253abecf6a3df8e5",
        "r": "0xae93fb594a9f6c1adadf955749fae391eaecfc15ce2e46de596850cecf9fd720",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x11380942417d5b58e873d717374a055c948e65f10e8dec93df96e776d180cabe",
      "signature": {
        "s": "0x7514649efeb2ad95de62cd280852b5c1d19e1bf776b945e47a1d0d2adcd7c92d",
        "r": "0xfd1282c65b5ce9aef90b8ec1f1a319f30f5a7196cb504e6641e8aae615434541",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "73292",
    "total": "73292"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "73292",
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
            "amount": "667816"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "73"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI5ZGJiM2Q0My04OGM0LTU4MzAtODc1MC03ODMyYWY2NDIxYWEifQ==",
    "nonce": 1848,
    "balances": {
      "current": "10000001415560824",
      "previous": "10000001415634189"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd83fd5b1575068e46f403be32954464007061bce",
    "nonce": 20,
    "balances": {
      "current": "73292",
      "previous": "0"
    }
  },
  "blockNumber": "10114541",
  "created": "2020-05-22T08:12:30.847Z",
  "updated": "2020-05-22T08:12:31.940Z",
  "id": "5ec7896e005df800101bc48e"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000011e4c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `73292`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``