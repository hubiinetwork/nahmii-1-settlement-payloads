# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdB24ee94Ea3Db3df4C52c4613e555aa8FE83cb83`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000090b000000000000000000000000000000000000000000000000000000000000090b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000090b000000000000000000000000000000000000000000000000000000000000090b3744c9f11d22dc482d35d247e6421e410b10e08b4717254247323af681768abfb49825f8b6e4de861636e9a6b489728c52a22ed1fea51079a89f446d71ce421829370e1c69e98c89b3a522645ea6da74e1870a88758d5edf0fe79b7262d6d874000000000000000000000000000000000000000000000000000000000000001bd744b1c45a8631fd6e65fd36cd18ea19f724e6d25a6ec1274d104085a5c1dd4a7cb2db0823d255e9da05223ae2702879f6882cbf9c53eeaee6b173718d173a9251a3e049a026eac696af6f3f12a68b567bcb8a73664bf0ac9046f40dd2c45d17000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc560572000000000000000000000000000000000000000000000000002386f2bc560e7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e4600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6d4a6d4e32597a5a4330324d6a686b4c54566a596a41744f5445345a53316b4e544e694e6d5132597a5534597a596966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000db24ee94ea3db3df4c52c4613e555aa8fe83cb83000000000000000000000000000000000000000000000000000000000000090b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3744c9f11d22dc482d35d247e6421e410b10e08b4717254247323af681768abf",
      "signature": {
        "s": "0x29370e1c69e98c89b3a522645ea6da74e1870a88758d5edf0fe79b7262d6d874",
        "r": "0xb49825f8b6e4de861636e9a6b489728c52a22ed1fea51079a89f446d71ce4218",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd744b1c45a8631fd6e65fd36cd18ea19f724e6d25a6ec1274d104085a5c1dd4a",
      "signature": {
        "s": "0x51a3e049a026eac696af6f3f12a68b567bcb8a73664bf0ac9046f40dd2c45d17",
        "r": "0x7cb2db0823d255e9da05223ae2702879f6882cbf9c53eeaee6b173718d173a92",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2315",
    "total": "2315"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2315",
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
            "amount": "798278"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZmJmN2YzZC02MjhkLTVjYjAtOTE4ZS1kNTNiNmQ2YzU4YzYifQ==",
    "nonce": 2298,
    "balances": {
      "current": "10000001284834674",
      "previous": "10000001284836991"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdb24ee94ea3db3df4c52c4613e555aa8fe83cb83",
    "nonce": 3,
    "balances": {
      "current": "2315",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:36.248Z",
  "updated": "2020-05-22T08:15:36.338Z",
  "id": "5ec78a28e5756b00111b825d"
}
```
* *stageAmount*: `2315`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000090b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000090b000000000000000000000000000000000000000000000000000000000000090b3744c9f11d22dc482d35d247e6421e410b10e08b4717254247323af681768abfb49825f8b6e4de861636e9a6b489728c52a22ed1fea51079a89f446d71ce421829370e1c69e98c89b3a522645ea6da74e1870a88758d5edf0fe79b7262d6d874000000000000000000000000000000000000000000000000000000000000001bd744b1c45a8631fd6e65fd36cd18ea19f724e6d25a6ec1274d104085a5c1dd4a7cb2db0823d255e9da05223ae2702879f6882cbf9c53eeaee6b173718d173a9251a3e049a026eac696af6f3f12a68b567bcb8a73664bf0ac9046f40dd2c45d17000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55f8000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000008fa00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc560572000000000000000000000000000000000000000000000000002386f2bc560e7f00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2e4600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a685a6d4a6d4e32597a5a4330324d6a686b4c54566a596a41744f5445345a53316b4e544e694e6d5132597a5534597a596966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000db24ee94ea3db3df4c52c4613e555aa8fe83cb83000000000000000000000000000000000000000000000000000000000000090b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3744c9f11d22dc482d35d247e6421e410b10e08b4717254247323af681768abf",
      "signature": {
        "s": "0x29370e1c69e98c89b3a522645ea6da74e1870a88758d5edf0fe79b7262d6d874",
        "r": "0xb49825f8b6e4de861636e9a6b489728c52a22ed1fea51079a89f446d71ce4218",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd744b1c45a8631fd6e65fd36cd18ea19f724e6d25a6ec1274d104085a5c1dd4a",
      "signature": {
        "s": "0x51a3e049a026eac696af6f3f12a68b567bcb8a73664bf0ac9046f40dd2c45d17",
        "r": "0x7cb2db0823d255e9da05223ae2702879f6882cbf9c53eeaee6b173718d173a92",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2315",
    "total": "2315"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2315",
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
            "amount": "798278"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhZmJmN2YzZC02MjhkLTVjYjAtOTE4ZS1kNTNiNmQ2YzU4YzYifQ==",
    "nonce": 2298,
    "balances": {
      "current": "10000001284834674",
      "previous": "10000001284836991"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdb24ee94ea3db3df4c52c4613e555aa8fe83cb83",
    "nonce": 3,
    "balances": {
      "current": "2315",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:36.248Z",
  "updated": "2020-05-22T08:15:36.338Z",
  "id": "5ec78a28e5756b00111b825d"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000090b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2315`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``