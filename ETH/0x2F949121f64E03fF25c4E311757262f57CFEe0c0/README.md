# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2F949121f64E03fF25c4E311757262f57CFEe0c0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000004b270000000000000000000000000000000000000000000000000000000000004b2700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b270000000000000000000000000000000000000000000000000000000000004b276688fd458880f3082f6601d2f29b7779c4c9c6553a84ddd96ff267654be2d9feb536e60fa80eff3d73fa6139dc924bbdd19eff142d240c638d81624c78201e175719cadcd51334007269eaee55cdae9802c80b43dc768d61f2d09c45c997c755000000000000000000000000000000000000000000000000000000000000001b9f84847cb353c9f7833eaa57610dc36df82e5f0f95438111dd7940da9984296c2c0c074c58604a1cf1a45aacd8001931536893186272d6a01f93dc0ae95222d21bb304547af2fd179dc5ea5ec37c3f3f44024f98821e507dd07dad4c0da9c654000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7dcf8d7000000000000000000000000000000000000000000000000002386f2c7dd441100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000013000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093ce100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e7a646b4d6a45354f43316c5a5756684c5455324d6d4d744f444a695a5330345954566a5a4745324f574a6a5a44676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002f949121f64e03ff25c4e311757262f57cfee0c00000000000000000000000000000000000000000000000000000000000004b27000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6688fd458880f3082f6601d2f29b7779c4c9c6553a84ddd96ff267654be2d9fe",
      "signature": {
        "s": "0x5719cadcd51334007269eaee55cdae9802c80b43dc768d61f2d09c45c997c755",
        "r": "0xb536e60fa80eff3d73fa6139dc924bbdd19eff142d240c638d81624c78201e17",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9f84847cb353c9f7833eaa57610dc36df82e5f0f95438111dd7940da9984296c",
      "signature": {
        "s": "0x1bb304547af2fd179dc5ea5ec37c3f3f44024f98821e507dd07dad4c0da9c654",
        "r": "0x2c0c074c58604a1cf1a45aacd8001931536893186272d6a01f93dc0ae95222d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19239",
    "total": "19239"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19239",
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
            "amount": "605409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNzdkMjE5OC1lZWVhLTU2MmMtODJiZS04YTVjZGE2OWJjZDgifQ==",
    "nonce": 1259,
    "balances": {
      "current": "10000001478228183",
      "previous": "10000001478247441"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2f949121f64e03ff25c4e311757262f57cfee0c0",
    "nonce": 20,
    "balances": {
      "current": "19239",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:02.748Z",
  "updated": "2020-05-22T08:08:02.821Z",
  "id": "5ec78862e5756b00111b8108"
}
```
* *stageAmount*: `19239`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004b2700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000004b270000000000000000000000000000000000000000000000000000000000004b276688fd458880f3082f6601d2f29b7779c4c9c6553a84ddd96ff267654be2d9feb536e60fa80eff3d73fa6139dc924bbdd19eff142d240c638d81624c78201e175719cadcd51334007269eaee55cdae9802c80b43dc768d61f2d09c45c997c755000000000000000000000000000000000000000000000000000000000000001b9f84847cb353c9f7833eaa57610dc36df82e5f0f95438111dd7940da9984296c2c0c074c58604a1cf1a45aacd8001931536893186272d6a01f93dc0ae95222d21bb304547af2fd179dc5ea5ec37c3f3f44024f98821e507dd07dad4c0da9c654000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004eb00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7dcf8d7000000000000000000000000000000000000000000000000002386f2c7dd441100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000013000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000093ce100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e7a646b4d6a45354f43316c5a5756684c5455324d6d4d744f444a695a5330345954566a5a4745324f574a6a5a44676966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000002f949121f64e03ff25c4e311757262f57cfee0c00000000000000000000000000000000000000000000000000000000000004b27000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6688fd458880f3082f6601d2f29b7779c4c9c6553a84ddd96ff267654be2d9fe",
      "signature": {
        "s": "0x5719cadcd51334007269eaee55cdae9802c80b43dc768d61f2d09c45c997c755",
        "r": "0xb536e60fa80eff3d73fa6139dc924bbdd19eff142d240c638d81624c78201e17",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9f84847cb353c9f7833eaa57610dc36df82e5f0f95438111dd7940da9984296c",
      "signature": {
        "s": "0x1bb304547af2fd179dc5ea5ec37c3f3f44024f98821e507dd07dad4c0da9c654",
        "r": "0x2c0c074c58604a1cf1a45aacd8001931536893186272d6a01f93dc0ae95222d2",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "19239",
    "total": "19239"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "19239",
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
            "amount": "605409"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "19"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNzdkMjE5OC1lZWVhLTU2MmMtODJiZS04YTVjZGE2OWJjZDgifQ==",
    "nonce": 1259,
    "balances": {
      "current": "10000001478228183",
      "previous": "10000001478247441"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2f949121f64e03ff25c4e311757262f57cfee0c0",
    "nonce": 20,
    "balances": {
      "current": "19239",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:02.748Z",
  "updated": "2020-05-22T08:08:02.821Z",
  "id": "5ec78862e5756b00111b8108"
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
0x0f200f9b0000000000000000000000000000000000000000000000000000000000004b270000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `19239`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``