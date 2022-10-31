# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x2B812C62b90E061393A39c48441B501300462E08`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000016021072e101fdb0050000000000000000000000000000000000000000000000000000002f74fec2780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002f74fec278000000000000000000000000000000000000000000000016020f899a6ff2b258f4db2215ee5c63effaeb3eec69a994c10bd0b30fc3fd6591b04d1c25a190972da46c486af161aff682c3d294a8ccc8a27668eb4ad1332c5ec2fc7bcfd963eef51c860e57d1b7202c89cc548d09afb287d121c458d9c78f4b6a24d1168b2339d0000000000000000000000000000000000000000000000000000000000000001ccf5b5c10d0d07c2de4bff312d0d657b7b49067d6bd790027d0920966597331ac48743873de4299004a18adf1cc5a75df780c8bb23a6f67b6c2da53c2d1166e0e6780cd3bd40c2082b858a2da122198b1efedca81ef93e655469b4353d4405cb9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aea1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000960fa0a1d4e53d09fbb100000000000000000000000000000000000000000000960fa0a1d514be2ee2b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000c26248b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c6016a9b13061774390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596a6c6a4e5449334d6930324d6a63354c54566a4f4451745957457a5a43307a4e6a526b4e445134596d55785957516966513d3d000000000000000000000000000000000000000000000000000000000000002b0000000000000000000000002b812c62b90e061393a39c48441b501300462e08000000000000000000000000000000000000000000000016021072e101fdb005000000000000000000000000000000000000000000000016021072b18cfeed8d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xf4db2215ee5c63effaeb3eec69a994c10bd0b30fc3fd6591b04d1c25a190972d",
      "signature": {
        "s": "0x1c860e57d1b7202c89cc548d09afb287d121c458d9c78f4b6a24d1168b2339d0",
        "r": "0xa46c486af161aff682c3d294a8ccc8a27668eb4ad1332c5ec2fc7bcfd963eef5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcf5b5c10d0d07c2de4bff312d0d657b7b49067d6bd790027d0920966597331ac",
      "signature": {
        "s": "0x6780cd3bd40c2082b858a2da122198b1efedca81ef93e655469b4353d4405cb9",
        "r": "0x48743873de4299004a18adf1cc5a75df780c8bb23a6f67b6c2da53c2d1166e0e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "203826315896",
    "total": "405976858230732796504"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "203826315896",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264389805390295430201"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "203826315"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYjljNTI3Mi02Mjc5LTVjODQtYWEzZC0zNjRkNDQ4YmUxYWQifQ==",
    "nonce": 110241,
    "balances": {
      "current": "708643248358150780877745",
      "previous": "708643248358354811019956"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2b812c62b90e061393a39c48441b501300462e08",
    "nonce": 43,
    "balances": {
      "current": "405977114720039972869",
      "previous": "405977114516213656973"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:16.395Z",
  "updated": "2022-05-04T08:52:16.461Z",
  "id": "62723ec0bbd75600116d0524"
}
```
* *stageAmount*: `405977114720039972869`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000002f74fec2780000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000002f74fec278000000000000000000000000000000000000000000000016020f899a6ff2b258f4db2215ee5c63effaeb3eec69a994c10bd0b30fc3fd6591b04d1c25a190972da46c486af161aff682c3d294a8ccc8a27668eb4ad1332c5ec2fc7bcfd963eef51c860e57d1b7202c89cc548d09afb287d121c458d9c78f4b6a24d1168b2339d0000000000000000000000000000000000000000000000000000000000000001ccf5b5c10d0d07c2de4bff312d0d657b7b49067d6bd790027d0920966597331ac48743873de4299004a18adf1cc5a75df780c8bb23a6f67b6c2da53c2d1166e0e6780cd3bd40c2082b858a2da122198b1efedca81ef93e655469b4353d4405cb9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cb0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aea1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000960fa0a1d4e53d09fbb100000000000000000000000000000000000000000000960fa0a1d514be2ee2b400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000c26248b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c6016a9b13061774390000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a596a6c6a4e5449334d6930324d6a63354c54566a4f4451745957457a5a43307a4e6a526b4e445134596d55785957516966513d3d000000000000000000000000000000000000000000000000000000000000002b0000000000000000000000002b812c62b90e061393a39c48441b501300462e08000000000000000000000000000000000000000000000016021072e101fdb005000000000000000000000000000000000000000000000016021072b18cfeed8d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xf4db2215ee5c63effaeb3eec69a994c10bd0b30fc3fd6591b04d1c25a190972d",
      "signature": {
        "s": "0x1c860e57d1b7202c89cc548d09afb287d121c458d9c78f4b6a24d1168b2339d0",
        "r": "0xa46c486af161aff682c3d294a8ccc8a27668eb4ad1332c5ec2fc7bcfd963eef5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xcf5b5c10d0d07c2de4bff312d0d657b7b49067d6bd790027d0920966597331ac",
      "signature": {
        "s": "0x6780cd3bd40c2082b858a2da122198b1efedca81ef93e655469b4353d4405cb9",
        "r": "0x48743873de4299004a18adf1cc5a75df780c8bb23a6f67b6c2da53c2d1166e0e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "203826315896",
    "total": "405976858230732796504"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "203826315896",
  "currency": {
    "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "27264389805390295430201"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "203826315"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjYjljNTI3Mi02Mjc5LTVjODQtYWEzZC0zNjRkNDQ4YmUxYWQifQ==",
    "nonce": 110241,
    "balances": {
      "current": "708643248358150780877745",
      "previous": "708643248358354811019956"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2b812c62b90e061393a39c48441b501300462e08",
    "nonce": 43,
    "balances": {
      "current": "405977114720039972869",
      "previous": "405977114516213656973"
    }
  },
  "blockNumber": "14709963",
  "created": "2022-05-04T08:52:16.395Z",
  "updated": "2022-05-04T08:52:16.461Z",
  "id": "62723ec0bbd75600116d0524"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b000000000000000000000000000000000000000000000016021072e101fdb0050000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `405977114720039972869`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`