# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf20d0dB66538F8D865bA056cC726267d855505FA`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000385e500000000000000000000000000000000000000000000000000000000000385e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000385e500000000000000000000000000000000000000000000000000000000000385e56cd168ea23c84fbe4cbe087dd86ec86d2efb5881c9e7027ae0a4b38cdbaa30205e458872ae0ad78794a03595ad5ca87675d608b4e685ec7021f43ea6bce2fa7f10d56768032358ed33d4a13d19f4525e9d065ee981a64ac3f04c96fa7ae5d03c000000000000000000000000000000000000000000000000000000000000001bbaa47d2a1d7f4f9ed44ef99a1013e8a84372cf347d572ef635d552bfa157b63d86235b88f410241fa16b73b85ce657cd4d6dfc8faffb2777bcd647935e568a7911b77e9a4274eb4baf0df5d72107ae6ffe74747d0d6c155dc036507dc3b423d9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001cc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbca1259000000000000000000000000000000000000000000000000002386f2cbcd992400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000083cc600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e44526c4e3255324f43316d4f54686c4c5456694d6d5174596a4d334e793079597a41784e6d49344d6a5a6d4e474d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000f20d0db66538f8d865ba056cc726267d855505fa00000000000000000000000000000000000000000000000000000000000385e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6cd168ea23c84fbe4cbe087dd86ec86d2efb5881c9e7027ae0a4b38cdbaa3020",
      "signature": {
        "s": "0x10d56768032358ed33d4a13d19f4525e9d065ee981a64ac3f04c96fa7ae5d03c",
        "r": "0x5e458872ae0ad78794a03595ad5ca87675d608b4e685ec7021f43ea6bce2fa7f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbaa47d2a1d7f4f9ed44ef99a1013e8a84372cf347d572ef635d552bfa157b63d",
      "signature": {
        "s": "0x11b77e9a4274eb4baf0df5d72107ae6ffe74747d0d6c155dc036507dc3b423d9",
        "r": "0x86235b88f410241fa16b73b85ce657cd4d6dfc8faffb2777bcd647935e568a79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "230885",
    "total": "230885"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "230885",
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
            "amount": "539846"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "230"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNDRlN2U2OC1mOThlLTViMmQtYjM3Ny0yYzAxNmI4MjZmNGMifQ==",
    "nonce": 460,
    "balances": {
      "current": "10000001544098393",
      "previous": "10000001544329508"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf20d0db66538f8d865ba056cc726267d855505fa",
    "nonce": 20,
    "balances": {
      "current": "230885",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:11.105Z",
  "updated": "2020-05-22T08:02:11.181Z",
  "id": "5ec78703005df800101bc2aa"
}
```
* *stageAmount*: `230885`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000385e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000385e500000000000000000000000000000000000000000000000000000000000385e56cd168ea23c84fbe4cbe087dd86ec86d2efb5881c9e7027ae0a4b38cdbaa30205e458872ae0ad78794a03595ad5ca87675d608b4e685ec7021f43ea6bce2fa7f10d56768032358ed33d4a13d19f4525e9d065ee981a64ac3f04c96fa7ae5d03c000000000000000000000000000000000000000000000000000000000000001bbaa47d2a1d7f4f9ed44ef99a1013e8a84372cf347d572ef635d552bfa157b63d86235b88f410241fa16b73b85ce657cd4d6dfc8faffb2777bcd647935e568a7911b77e9a4274eb4baf0df5d72107ae6ffe74747d0d6c155dc036507dc3b423d9000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c5000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000001cc00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cbca1259000000000000000000000000000000000000000000000000002386f2cbcd992400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000e6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000083cc600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e44526c4e3255324f43316d4f54686c4c5456694d6d5174596a4d334e793079597a41784e6d49344d6a5a6d4e474d6966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000f20d0db66538f8d865ba056cc726267d855505fa00000000000000000000000000000000000000000000000000000000000385e5000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6cd168ea23c84fbe4cbe087dd86ec86d2efb5881c9e7027ae0a4b38cdbaa3020",
      "signature": {
        "s": "0x10d56768032358ed33d4a13d19f4525e9d065ee981a64ac3f04c96fa7ae5d03c",
        "r": "0x5e458872ae0ad78794a03595ad5ca87675d608b4e685ec7021f43ea6bce2fa7f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbaa47d2a1d7f4f9ed44ef99a1013e8a84372cf347d572ef635d552bfa157b63d",
      "signature": {
        "s": "0x11b77e9a4274eb4baf0df5d72107ae6ffe74747d0d6c155dc036507dc3b423d9",
        "r": "0x86235b88f410241fa16b73b85ce657cd4d6dfc8faffb2777bcd647935e568a79",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "230885",
    "total": "230885"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "230885",
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
            "amount": "539846"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "230"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIwNDRlN2U2OC1mOThlLTViMmQtYjM3Ny0yYzAxNmI4MjZmNGMifQ==",
    "nonce": 460,
    "balances": {
      "current": "10000001544098393",
      "previous": "10000001544329508"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf20d0db66538f8d865ba056cc726267d855505fa",
    "nonce": 20,
    "balances": {
      "current": "230885",
      "previous": "0"
    }
  },
  "blockNumber": "10114501",
  "created": "2020-05-22T08:02:11.105Z",
  "updated": "2020-05-22T08:02:11.181Z",
  "id": "5ec78703005df800101bc2aa"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000385e50000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `230885`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``