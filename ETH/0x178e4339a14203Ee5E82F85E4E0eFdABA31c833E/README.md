# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x178e4339a14203Ee5E82F85E4E0eFdABA31c833E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002910b000000000000000000000000000000000000000000000000000000000002910b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002910b000000000000000000000000000000000000000000000000000000000002910bc43214094888a056f6f9b6dd794f36a8911eafc4537e2c4d0f854384eceecc67b0d5798d2c7af987e224ec3a26af420f6c2245e2aa92a6862572d5fad2c525074bb78678c7b2e91409c6467f0d0ccd318bdc13ebabf75554133c2d37385ed7a4000000000000000000000000000000000000000000000000000000000000001c22fd875161060ce8a7510b939289d7f054e2089765d26aef5020b6cf942ebf43e70bb5efed426fb786c31960eb108854e4239019fce96a84fa340305545b036150d950294bc0c9fa230f12f03839d224fd2bff01ff7cae4dc300ce1197cdbbdb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000037c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cad05c06000000000000000000000000000000000000000000000000002386f2cad2edb900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000087bf500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e7a55334e4463354e4330334e444d314c5455304e54597459546330596930774d7a5977597a59334f54566b4d57456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000178e4339a14203ee5e82f85e4e0efdaba31c833e000000000000000000000000000000000000000000000000000000000002910b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc43214094888a056f6f9b6dd794f36a8911eafc4537e2c4d0f854384eceecc67",
      "signature": {
        "s": "0x4bb78678c7b2e91409c6467f0d0ccd318bdc13ebabf75554133c2d37385ed7a4",
        "r": "0xb0d5798d2c7af987e224ec3a26af420f6c2245e2aa92a6862572d5fad2c52507",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x22fd875161060ce8a7510b939289d7f054e2089765d26aef5020b6cf942ebf43",
      "signature": {
        "s": "0x50d950294bc0c9fa230f12f03839d224fd2bff01ff7cae4dc300ce1197cdbbdb",
        "r": "0xe70bb5efed426fb786c31960eb108854e4239019fce96a84fa340305545b0361",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "168203",
    "total": "168203"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "168203",
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
            "amount": "556021"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "168"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NzU3NDc5NC03NDM1LTU0NTYtYTc0Yi0wMzYwYzY3OTVkMWEifQ==",
    "nonce": 892,
    "balances": {
      "current": "10000001527733254",
      "previous": "10000001527901625"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x178e4339a14203ee5e82f85e4e0efdaba31c833e",
    "nonce": 20,
    "balances": {
      "current": "168203",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:18.429Z",
  "updated": "2020-05-22T08:05:18.492Z",
  "id": "5ec787bee5756b00111b8094"
}
```
* *stageAmount*: `168203`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002910b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002910b000000000000000000000000000000000000000000000000000000000002910bc43214094888a056f6f9b6dd794f36a8911eafc4537e2c4d0f854384eceecc67b0d5798d2c7af987e224ec3a26af420f6c2245e2aa92a6862572d5fad2c525074bb78678c7b2e91409c6467f0d0ccd318bdc13ebabf75554133c2d37385ed7a4000000000000000000000000000000000000000000000000000000000000001c22fd875161060ce8a7510b939289d7f054e2089765d26aef5020b6cf942ebf43e70bb5efed426fb786c31960eb108854e4239019fce96a84fa340305545b036150d950294bc0c9fa230f12f03839d224fd2bff01ff7cae4dc300ce1197cdbbdb000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55d20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000037c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cad05c06000000000000000000000000000000000000000000000000002386f2cad2edb900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000087bf500000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e7a55334e4463354e4330334e444d314c5455304e54597459546330596930774d7a5977597a59334f54566b4d57456966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000178e4339a14203ee5e82f85e4e0efdaba31c833e000000000000000000000000000000000000000000000000000000000002910b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc43214094888a056f6f9b6dd794f36a8911eafc4537e2c4d0f854384eceecc67",
      "signature": {
        "s": "0x4bb78678c7b2e91409c6467f0d0ccd318bdc13ebabf75554133c2d37385ed7a4",
        "r": "0xb0d5798d2c7af987e224ec3a26af420f6c2245e2aa92a6862572d5fad2c52507",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x22fd875161060ce8a7510b939289d7f054e2089765d26aef5020b6cf942ebf43",
      "signature": {
        "s": "0x50d950294bc0c9fa230f12f03839d224fd2bff01ff7cae4dc300ce1197cdbbdb",
        "r": "0xe70bb5efed426fb786c31960eb108854e4239019fce96a84fa340305545b0361",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "168203",
    "total": "168203"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "168203",
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
            "amount": "556021"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "168"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI1NzU3NDc5NC03NDM1LTU0NTYtYTc0Yi0wMzYwYzY3OTVkMWEifQ==",
    "nonce": 892,
    "balances": {
      "current": "10000001527733254",
      "previous": "10000001527901625"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x178e4339a14203ee5e82f85e4e0efdaba31c833e",
    "nonce": 20,
    "balances": {
      "current": "168203",
      "previous": "0"
    }
  },
  "blockNumber": "10114514",
  "created": "2020-05-22T08:05:18.429Z",
  "updated": "2020-05-22T08:05:18.492Z",
  "id": "5ec787bee5756b00111b8094"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002910b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `168203`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``