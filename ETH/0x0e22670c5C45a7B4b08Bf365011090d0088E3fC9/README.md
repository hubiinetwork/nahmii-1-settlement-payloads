# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0e22670c5C45a7B4b08Bf365011090d0088E3fC9`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792326f93ec0a63db43c8331f0abdd50eb5446163de0163fe747d0250013bbffb402929b9595dc1f0fc7a4e48deeab42c4a512d2c9d0a434700c5b2428d38a6a3a415d7cce93266fc61f62c0b32e509a7319a396808d29c0ac47b1488c06937f9a4000000000000000000000000000000000000000000000000000000000000001c6270d1730a9605778d8c5a78f839a358431d49749c590c5b866eed350abd02dd0fb7fed903a357c14873ed8a0f9d1ac37e62ca82d1b310e392cc5b83594bd4e55b2ac6cbe56373ad55a73539c38462fe53569ce92486c7b221ef99ef459af4f1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bed4d0000000000000000000000000000000000000000000000000002386f2c3bf1c7400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a498100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d4446694d446b345a433030596a59344c5456694e7a457459574e6c5969316a59544979595749784e4445324d44456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000e22670c5c45a7b4b08bf365011090d0088e3fc90000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x326f93ec0a63db43c8331f0abdd50eb5446163de0163fe747d0250013bbffb40",
      "signature": {
        "s": "0x15d7cce93266fc61f62c0b32e509a7319a396808d29c0ac47b1488c06937f9a4",
        "r": "0x2929b9595dc1f0fc7a4e48deeab42c4a512d2c9d0a434700c5b2428d38a6a3a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6270d1730a9605778d8c5a78f839a358431d49749c590c5b866eed350abd02dd",
      "signature": {
        "s": "0x5b2ac6cbe56373ad55a73539c38462fe53569ce92486c7b221ef99ef459af4f1",
        "r": "0x0fb7fed903a357c14873ed8a0f9d1ac37e62ca82d1b310e392cc5b83594bd4e5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674177"
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
    "data": "eyJyZWYiOiI4MDFiMDk4ZC00YjY4LTViNzEtYWNlYi1jYTIyYWIxNDE2MDEifQ==",
    "nonce": 1978,
    "balances": {
      "current": "10000001409144016",
      "previous": "10000001409162356"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e22670c5c45a7b4b08bf365011090d0088e3fc9",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:31.790Z",
  "updated": "2020-05-22T08:13:31.865Z",
  "id": "5ec789abb0c6090011d5ab62"
}
```
* *stageAmount*: `18322`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000004792326f93ec0a63db43c8331f0abdd50eb5446163de0163fe747d0250013bbffb402929b9595dc1f0fc7a4e48deeab42c4a512d2c9d0a434700c5b2428d38a6a3a415d7cce93266fc61f62c0b32e509a7319a396808d29c0ac47b1488c06937f9a4000000000000000000000000000000000000000000000000000000000000001c6270d1730a9605778d8c5a78f839a358431d49749c590c5b866eed350abd02dd0fb7fed903a357c14873ed8a0f9d1ac37e62ca82d1b310e392cc5b83594bd4e55b2ac6cbe56373ad55a73539c38462fe53569ce92486c7b221ef99ef459af4f1000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55ef000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000007ba00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c3bed4d0000000000000000000000000000000000000000000000000002386f2c3bf1c7400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a498100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d4446694d446b345a433030596a59344c5456694e7a457459574e6c5969316a59544979595749784e4445324d44456966513d3d00000000000000000000000000000000000000000000000000000000000000140000000000000000000000000e22670c5c45a7b4b08bf365011090d0088e3fc90000000000000000000000000000000000000000000000000000000000004792000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x326f93ec0a63db43c8331f0abdd50eb5446163de0163fe747d0250013bbffb40",
      "signature": {
        "s": "0x15d7cce93266fc61f62c0b32e509a7319a396808d29c0ac47b1488c06937f9a4",
        "r": "0x2929b9595dc1f0fc7a4e48deeab42c4a512d2c9d0a434700c5b2428d38a6a3a4",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6270d1730a9605778d8c5a78f839a358431d49749c590c5b866eed350abd02dd",
      "signature": {
        "s": "0x5b2ac6cbe56373ad55a73539c38462fe53569ce92486c7b221ef99ef459af4f1",
        "r": "0x0fb7fed903a357c14873ed8a0f9d1ac37e62ca82d1b310e392cc5b83594bd4e5",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "18322",
    "total": "18322"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18322",
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
            "amount": "674177"
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
    "data": "eyJyZWYiOiI4MDFiMDk4ZC00YjY4LTViNzEtYWNlYi1jYTIyYWIxNDE2MDEifQ==",
    "nonce": 1978,
    "balances": {
      "current": "10000001409144016",
      "previous": "10000001409162356"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0e22670c5c45a7b4b08bf365011090d0088e3fc9",
    "nonce": 20,
    "balances": {
      "current": "18322",
      "previous": "0"
    }
  },
  "blockNumber": "10114543",
  "created": "2020-05-22T08:13:31.790Z",
  "updated": "2020-05-22T08:13:31.865Z",
  "id": "5ec789abb0c6090011d5ab62"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000047920000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `18322`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``