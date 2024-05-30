# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAb67C1870068C86a2A36296F7ABc49a8565cecEB`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000030fc00000000000000000000000000000000000000000000000000000000000030fc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000030fc00000000000000000000000000000000000000000000000000000000000030fc5188c49b9c7b325b69eb07c2df5cffd034a1c4fe5a416a71dc849136794a4f2a0459a94e84721302e1750b773e1cffeb59c1eabe54ac79998fa76ebcea61b9fe2391479863958e295b6f554964a68d1bd146907d171909904fd41a907f949305000000000000000000000000000000000000000000000000000000000000001b1c93ff3d02a9534e44de7949d20c9eabd6267a8b111fcea8a8accac6169bb75f509e652fcf4675010b7e04f58898c8e486f07a67df158afbf43bf2f11268e46569eecf0bd45370610b76e393dbda178f31d5e9bc8ee6c9a537d5b1a163cb53eb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007cd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b8ed11000000000000000000000000000000000000000000000000002386f2c3b91e1900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4afd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d51304e3249784d7930774e325a6c4c5455775a57497459574e6b4e7930304e6a6b314e5752685a6a426c5a57516966513d3d0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000ab67c1870068c86a2a36296f7abc49a8565ceceb00000000000000000000000000000000000000000000000000000000000030fc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5188c49b9c7b325b69eb07c2df5cffd034a1c4fe5a416a71dc849136794a4f2a",
      "signature": {
        "s": "0x2391479863958e295b6f554964a68d1bd146907d171909904fd41a907f949305",
        "r": "0x0459a94e84721302e1750b773e1cffeb59c1eabe54ac79998fa76ebcea61b9fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1c93ff3d02a9534e44de7949d20c9eabd6267a8b111fcea8a8accac6169bb75f",
      "signature": {
        "s": "0x69eecf0bd45370610b76e393dbda178f31d5e9bc8ee6c9a537d5b1a163cb53eb",
        "r": "0x509e652fcf4675010b7e04f58898c8e486f07a67df158afbf43bf2f11268e465",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12540",
    "total": "12540"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12540",
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
            "amount": "674557"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZmQ0N2IxMy0wN2ZlLTUwZWItYWNkNy00Njk1NWRhZjBlZWQifQ==",
    "nonce": 1997,
    "balances": {
      "current": "10000001408757009",
      "previous": "10000001408769561"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xab67c1870068c86a2a36296f7abc49a8565ceceb",
    "nonce": 9,
    "balances": {
      "current": "12540",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:36.577Z",
  "updated": "2020-05-22T08:13:37.642Z",
  "id": "5ec789b0b0c6090011d5ab69"
}
```
* *stageAmount*: `12540`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000030fc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000030fc00000000000000000000000000000000000000000000000000000000000030fc5188c49b9c7b325b69eb07c2df5cffd034a1c4fe5a416a71dc849136794a4f2a0459a94e84721302e1750b773e1cffeb59c1eabe54ac79998fa76ebcea61b9fe2391479863958e295b6f554964a68d1bd146907d171909904fd41a907f949305000000000000000000000000000000000000000000000000000000000000001b1c93ff3d02a9534e44de7949d20c9eabd6267a8b111fcea8a8accac6169bb75f509e652fcf4675010b7e04f58898c8e486f07a67df158afbf43bf2f11268e46569eecf0bd45370610b76e393dbda178f31d5e9bc8ee6c9a537d5b1a163cb53eb000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007cd00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3b8ed11000000000000000000000000000000000000000000000000002386f2c3b91e1900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000000c0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4afd00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a6d51304e3249784d7930774e325a6c4c5455775a57497459574e6b4e7930304e6a6b314e5752685a6a426c5a57516966513d3d0000000000000000000000000000000000000000000000000000000000000009000000000000000000000000ab67c1870068c86a2a36296f7abc49a8565ceceb00000000000000000000000000000000000000000000000000000000000030fc000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5188c49b9c7b325b69eb07c2df5cffd034a1c4fe5a416a71dc849136794a4f2a",
      "signature": {
        "s": "0x2391479863958e295b6f554964a68d1bd146907d171909904fd41a907f949305",
        "r": "0x0459a94e84721302e1750b773e1cffeb59c1eabe54ac79998fa76ebcea61b9fe",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1c93ff3d02a9534e44de7949d20c9eabd6267a8b111fcea8a8accac6169bb75f",
      "signature": {
        "s": "0x69eecf0bd45370610b76e393dbda178f31d5e9bc8ee6c9a537d5b1a163cb53eb",
        "r": "0x509e652fcf4675010b7e04f58898c8e486f07a67df158afbf43bf2f11268e465",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12540",
    "total": "12540"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12540",
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
            "amount": "674557"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "12"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJkZmQ0N2IxMy0wN2ZlLTUwZWItYWNkNy00Njk1NWRhZjBlZWQifQ==",
    "nonce": 1997,
    "balances": {
      "current": "10000001408757009",
      "previous": "10000001408769561"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xab67c1870068c86a2a36296f7abc49a8565ceceb",
    "nonce": 9,
    "balances": {
      "current": "12540",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:36.577Z",
  "updated": "2020-05-22T08:13:37.642Z",
  "id": "5ec789b0b0c6090011d5ab69"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000030fc0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `12540`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``