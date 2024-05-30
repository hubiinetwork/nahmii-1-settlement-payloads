# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x59D875e96fec8b3Bf483f362dd53B58875D9d822`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de75a5ffaab58190000000000000000000000000000000000000000000001faf3853d1986f800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000001faf3853d1986f800000000000000000000000000000000000000000000000001faf3853d1986f80000cba7b00c2f8333ae5e31a70ff3fab11902e9a8acadc748ce8d2a1f12a81d482f48a03b904e082d81d5f6ba0ac051485d3e6dd764d0656efc1953524a7a53ae9d7d2eca522929ffaa72de49bce5b1d5409657d346ed5e6d7ed03f31b7ffeec3e2000000000000000000000000000000000000000000000000000000000000001c064e299a6c61c3bea0215187207aba43db5144ce6c9276a3d60a8e44650f31b122b29bde0cf408ede71969a3fd612e9fffe1ccf9b3208bc44d2f0859b8a6b60a32a866715067c5225310004293a48aec2dd2d7921d835d6478a5462aa0153a87000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1f9920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002100000000000000000000000059d875e96fec8b3bf483f362dd53b58875d9d8220000000000000000000000000000000000000000000000000de75a5ffaab58190000000000000000000000000000000000000000000001fb83342620b32e581900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000081c78ea7318b00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024d551bf4e5b870000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a4441354d6a426b4d533033596a59784c54526d4d6a49744f474e6d5a433031596a4e68595467344e3245325954516966513d3d000000000000000000000000000000000000000000000000000000000000004f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000034e10088877e237e56280000000000000000000000000000000000000000000032e60d034a649c86562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcba7b00c2f8333ae5e31a70ff3fab11902e9a8acadc748ce8d2a1f12a81d482f",
      "signature": {
        "s": "0x7d2eca522929ffaa72de49bce5b1d5409657d346ed5e6d7ed03f31b7ffeec3e2",
        "r": "0x48a03b904e082d81d5f6ba0ac051485d3e6dd764d0656efc1953524a7a53ae9d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x064e299a6c61c3bea0215187207aba43db5144ce6c9276a3d60a8e44650f31b1",
      "signature": {
        "s": "0x32a866715067c5225310004293a48aec2dd2d7921d835d6478a5462aa0153a87",
        "r": "0x22b29bde0cf408ede71969a3fd612e9fffe1ccf9b3208bc44d2f0859b8a6b60a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9351600000000000000000",
    "total": "9351600000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9351600000000000000000",
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
            "amount": "42465879000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9351600000000000000"
      }
    },
    "wallet": "0x59d875e96fec8b3bf483f362dd53b58875d9d822",
    "data": "eyJyZWYiOiJjZDA5MjBkMS03YjYxLTRmMjItOGNmZC01YjNhYTg4N2E2YTQifQ==",
    "nonce": 33,
    "balances": {
      "current": "1001868810387150873",
      "previous": "9361953468810387150873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 79,
    "balances": {
      "current": "249713612955378863986216",
      "previous": "240362012955378863986216"
    }
  },
  "blockNumber": "14809490",
  "created": "2022-05-20T06:18:50.644Z",
  "updated": "2022-05-20T06:18:50.737Z",
  "id": "628732ca7832e20011830f25"
}
```
* *stageAmount*: `1001868810387150873`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000001faf3853d1986f800000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000001faf3853d1986f800000000000000000000000000000000000000000000000001faf3853d1986f80000cba7b00c2f8333ae5e31a70ff3fab11902e9a8acadc748ce8d2a1f12a81d482f48a03b904e082d81d5f6ba0ac051485d3e6dd764d0656efc1953524a7a53ae9d7d2eca522929ffaa72de49bce5b1d5409657d346ed5e6d7ed03f31b7ffeec3e2000000000000000000000000000000000000000000000000000000000000001c064e299a6c61c3bea0215187207aba43db5144ce6c9276a3d60a8e44650f31b122b29bde0cf408ede71969a3fd612e9fffe1ccf9b3208bc44d2f0859b8a6b60a32a866715067c5225310004293a48aec2dd2d7921d835d6478a5462aa0153a87000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e1f9920000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002100000000000000000000000059d875e96fec8b3bf483f362dd53b58875d9d8220000000000000000000000000000000000000000000000000de75a5ffaab58190000000000000000000000000000000000000000000001fb83342620b32e581900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000081c78ea7318b00000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000024d551bf4e5b870000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a4441354d6a426b4d533033596a59784c54526d4d6a49744f474e6d5a433031596a4e68595467344e3245325954516966513d3d000000000000000000000000000000000000000000000000000000000000004f000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b10000000000000000000000000000000000000000000034e10088877e237e56280000000000000000000000000000000000000000000032e60d034a649c86562800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcba7b00c2f8333ae5e31a70ff3fab11902e9a8acadc748ce8d2a1f12a81d482f",
      "signature": {
        "s": "0x7d2eca522929ffaa72de49bce5b1d5409657d346ed5e6d7ed03f31b7ffeec3e2",
        "r": "0x48a03b904e082d81d5f6ba0ac051485d3e6dd764d0656efc1953524a7a53ae9d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x064e299a6c61c3bea0215187207aba43db5144ce6c9276a3d60a8e44650f31b1",
      "signature": {
        "s": "0x32a866715067c5225310004293a48aec2dd2d7921d835d6478a5462aa0153a87",
        "r": "0x22b29bde0cf408ede71969a3fd612e9fffe1ccf9b3208bc44d2f0859b8a6b60a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9351600000000000000000",
    "total": "9351600000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9351600000000000000000",
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
            "amount": "42465879000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9351600000000000000"
      }
    },
    "wallet": "0x59d875e96fec8b3bf483f362dd53b58875d9d822",
    "data": "eyJyZWYiOiJjZDA5MjBkMS03YjYxLTRmMjItOGNmZC01YjNhYTg4N2E2YTQifQ==",
    "nonce": 33,
    "balances": {
      "current": "1001868810387150873",
      "previous": "9361953468810387150873"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 79,
    "balances": {
      "current": "249713612955378863986216",
      "previous": "240362012955378863986216"
    }
  },
  "blockNumber": "14809490",
  "created": "2022-05-20T06:18:50.644Z",
  "updated": "2022-05-20T06:18:50.737Z",
  "id": "628732ca7832e20011830f25"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000de75a5ffaab58190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1001868810387150873`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`