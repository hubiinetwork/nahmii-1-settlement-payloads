# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb9c6fcE32Ea917c26C67a6d1932A0Ed8ef159fE1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef94054acb176e50de054f299bda174148d8ab87088168f11b126d0464798cf84b511e43c1c0ea44c1b965da2a255ecff02f9c1901802cdfb9580405608f564bcc6638019e9cc4faf1478572e1d57b5d365681f373cc3663e0d9a9d4f5399bcd8842000000000000000000000000000000000000000000000000000000000000001be4c9ea8e97110255dd2028a0fa12fd7dba158a8fbee71c6b3913e316eb5a6a8989248f71682d75b7e5d1b2987d48aca1e9156c5f49fb766506e7edce29c30cc815b3a6360235eff77a2643e0b197fa99911a5cc0b763e19820246751b4c9e926000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbebbd52000000000000000000000000000000000000000000000000002386f2cbeeada600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008342d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a46684e6a6c6c5a69316a4f5756694c5455345a574d74596d59324e4330334d6d526b4f57566c5a474d324f57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b9c6fce32ea917c26c67a6d1932a0ed8ef159fe1000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x054acb176e50de054f299bda174148d8ab87088168f11b126d0464798cf84b51",
      "signature": {
        "s": "0x38019e9cc4faf1478572e1d57b5d365681f373cc3663e0d9a9d4f5399bcd8842",
        "r": "0x1e43c1c0ea44c1b965da2a255ecff02f9c1901802cdfb9580405608f564bcc66",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe4c9ea8e97110255dd2028a0fa12fd7dba158a8fbee71c6b3913e316eb5a6a89",
      "signature": {
        "s": "0x15b3a6360235eff77a2643e0b197fa99911a5cc0b763e19820246751b4c9e926",
        "r": "0x89248f71682d75b7e5d1b2987d48aca1e9156c5f49fb766506e7edce29c30cc8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192404",
    "total": "192404"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192404",
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
            "amount": "537645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzFhNjllZi1jOWViLTU4ZWMtYmY2NC03MmRkOWVlZGM2OWUifQ==",
    "nonce": 452,
    "balances": {
      "current": "10000001546304850",
      "previous": "10000001546497446"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9c6fce32ea917c26c67a6d1932a0ed8ef159fe1",
    "nonce": 20,
    "balances": {
      "current": "192404",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.608Z",
  "updated": "2020-05-22T08:02:07.677Z",
  "id": "5ec786ffe5756b00111b800a"
}
```
* *stageAmount*: `192404`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000002ef94054acb176e50de054f299bda174148d8ab87088168f11b126d0464798cf84b511e43c1c0ea44c1b965da2a255ecff02f9c1901802cdfb9580405608f564bcc6638019e9cc4faf1478572e1d57b5d365681f373cc3663e0d9a9d4f5399bcd8842000000000000000000000000000000000000000000000000000000000000001be4c9ea8e97110255dd2028a0fa12fd7dba158a8fbee71c6b3913e316eb5a6a8989248f71682d75b7e5d1b2987d48aca1e9156c5f49fb766506e7edce29c30cc815b3a6360235eff77a2643e0b197fa99911a5cc0b763e19820246751b4c9e926000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001c400000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbebbd52000000000000000000000000000000000000000000000000002386f2cbeeada600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008342d00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4d7a46684e6a6c6c5a69316a4f5756694c5455345a574d74596d59324e4330334d6d526b4f57566c5a474d324f57556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000b9c6fce32ea917c26c67a6d1932a0ed8ef159fe1000000000000000000000000000000000000000000000000000000000002ef94000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x054acb176e50de054f299bda174148d8ab87088168f11b126d0464798cf84b51",
      "signature": {
        "s": "0x38019e9cc4faf1478572e1d57b5d365681f373cc3663e0d9a9d4f5399bcd8842",
        "r": "0x1e43c1c0ea44c1b965da2a255ecff02f9c1901802cdfb9580405608f564bcc66",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe4c9ea8e97110255dd2028a0fa12fd7dba158a8fbee71c6b3913e316eb5a6a89",
      "signature": {
        "s": "0x15b3a6360235eff77a2643e0b197fa99911a5cc0b763e19820246751b4c9e926",
        "r": "0x89248f71682d75b7e5d1b2987d48aca1e9156c5f49fb766506e7edce29c30cc8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "192404",
    "total": "192404"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "192404",
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
            "amount": "537645"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "192"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIzMzFhNjllZi1jOWViLTU4ZWMtYmY2NC03MmRkOWVlZGM2OWUifQ==",
    "nonce": 452,
    "balances": {
      "current": "10000001546304850",
      "previous": "10000001546497446"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb9c6fce32ea917c26c67a6d1932a0ed8ef159fe1",
    "nonce": 20,
    "balances": {
      "current": "192404",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:07.608Z",
  "updated": "2020-05-22T08:02:07.677Z",
  "id": "5ec786ffe5756b00111b800a"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002ef940000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `192404`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``