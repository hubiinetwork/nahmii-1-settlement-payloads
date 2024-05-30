# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x597Cf942BE49A2B86c556aEa19A83396C734d2Bd`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000048650000000000000000000000000000000000000000000000000000000000004865000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000048650000000000000000000000000000000000000000000000000000000000004865ee8cbd002631e995733000fa538af1c8b8fc035f1682c6f067c5a4858bdf548f9d2c085f674f05a0f2dfa1758d6c757ac311810cdaf466d1ad460455c39966ca693b606f0a241db8645362a339a117e3affbf4dd2aff45724b324eb34695b844000000000000000000000000000000000000000000000000000000000000001bf34e94309f0e2f932ed8b799e1eab6a51fcbd122b509f72b3afab960ab76b25f6d3f0989b2f7c0641b19e28c6fc304545e79c5b92c0ba769b3c7c81d3bda3d604929cb7a928459d02f67fcbd2bbe584576fae9ed634cb6ca9b3a8b98b0cb0fd2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7bd5d86000000000000000000000000000000000000000000000000002386f2c7bda5fd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000944f200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e54426d596a41775a53316c4e4449794c54566d4e446374596d597a4e7930344d7a59314f546b784d444a6c4e7a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000597cf942be49a2b86c556aea19a83396c734d2bd0000000000000000000000000000000000000000000000000000000000004865000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xee8cbd002631e995733000fa538af1c8b8fc035f1682c6f067c5a4858bdf548f",
      "signature": {
        "s": "0x693b606f0a241db8645362a339a117e3affbf4dd2aff45724b324eb34695b844",
        "r": "0x9d2c085f674f05a0f2dfa1758d6c757ac311810cdaf466d1ad460455c39966ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf34e94309f0e2f932ed8b799e1eab6a51fcbd122b509f72b3afab960ab76b25f",
      "signature": {
        "s": "0x4929cb7a928459d02f67fcbd2bbe584576fae9ed634cb6ca9b3a8b98b0cb0fd2",
        "r": "0x6d3f0989b2f7c0641b19e28c6fc304545e79c5b92c0ba769b3c7c81d3bda3d60",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18533",
    "total": "18533"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18533",
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
            "amount": "607474"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNTBmYjAwZS1lNDIyLTVmNDctYmYzNy04MzY1OTkxMDJlNzUifQ==",
    "nonce": 1266,
    "balances": {
      "current": "10000001476156806",
      "previous": "10000001476175357"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x597cf942be49a2b86c556aea19a83396c734d2bd",
    "nonce": 20,
    "balances": {
      "current": "18533",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:05.030Z",
  "updated": "2020-05-22T08:08:05.119Z",
  "id": "5ec78865e5756b00111b810b"
}
```
* *stageAmount*: `18533`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004865000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000048650000000000000000000000000000000000000000000000000000000000004865ee8cbd002631e995733000fa538af1c8b8fc035f1682c6f067c5a4858bdf548f9d2c085f674f05a0f2dfa1758d6c757ac311810cdaf466d1ad460455c39966ca693b606f0a241db8645362a339a117e3affbf4dd2aff45724b324eb34695b844000000000000000000000000000000000000000000000000000000000000001bf34e94309f0e2f932ed8b799e1eab6a51fcbd122b509f72b3afab960ab76b25f6d3f0989b2f7c0641b19e28c6fc304545e79c5b92c0ba769b3c7c81d3bda3d604929cb7a928459d02f67fcbd2bbe584576fae9ed634cb6ca9b3a8b98b0cb0fd2000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55db000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000004f200000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c7bd5d86000000000000000000000000000000000000000000000000002386f2c7bda5fd00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000944f200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e54426d596a41775a53316c4e4449794c54566d4e446374596d597a4e7930344d7a59314f546b784d444a6c4e7a556966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000597cf942be49a2b86c556aea19a83396c734d2bd0000000000000000000000000000000000000000000000000000000000004865000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xee8cbd002631e995733000fa538af1c8b8fc035f1682c6f067c5a4858bdf548f",
      "signature": {
        "s": "0x693b606f0a241db8645362a339a117e3affbf4dd2aff45724b324eb34695b844",
        "r": "0x9d2c085f674f05a0f2dfa1758d6c757ac311810cdaf466d1ad460455c39966ca",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf34e94309f0e2f932ed8b799e1eab6a51fcbd122b509f72b3afab960ab76b25f",
      "signature": {
        "s": "0x4929cb7a928459d02f67fcbd2bbe584576fae9ed634cb6ca9b3a8b98b0cb0fd2",
        "r": "0x6d3f0989b2f7c0641b19e28c6fc304545e79c5b92c0ba769b3c7c81d3bda3d60",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18533",
    "total": "18533"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18533",
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
            "amount": "607474"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "18"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjNTBmYjAwZS1lNDIyLTVmNDctYmYzNy04MzY1OTkxMDJlNzUifQ==",
    "nonce": 1266,
    "balances": {
      "current": "10000001476156806",
      "previous": "10000001476175357"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x597cf942be49a2b86c556aea19a83396c734d2bd",
    "nonce": 20,
    "balances": {
      "current": "18533",
      "previous": "0"
    }
  },
  "blockNumber": "10114523",
  "created": "2020-05-22T08:08:05.030Z",
  "updated": "2020-05-22T08:08:05.119Z",
  "id": "5ec78865e5756b00111b810b"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000048650000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18533`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``