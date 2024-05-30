# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa35a6A96E9b400C4DeD39514D0E65773ca0A3607`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000009184e9ea7a800000000000000000000000000000000000000000000000000000000002c07a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002c07a800000000000000000000000000000000000000000000000000000000002c07a8ffaa8b0f34c490823ad9183fe1cb98dfb38004fae1f7e9f2ccccd4abce9bfc421ea55fa296ee406fc7b1339b1f66539a2b0af98878120d3db393e2f12e3f39cf4e20d0b9b748b3e515bb750e26d087e4ff1ffdd16e38c5f6898dca375ed4a8b8000000000000000000000000000000000000000000000000000000000000001b1bcd77f7acb5250bbcdb46e5697b50f0b5672957e68e6a08b7c2218ecc8c159134c198a276ec07d8bbf18f637967f8393a024d92951376d078f79c447615169f074461e0a6b6e278a6f3cee4ffbe773c9280047da04381ed67e02cd7ef8bfe7b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df689a4a000000000000000000000000000000000000000000000000002386f2df94ad3700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000b450000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000338a600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a54686c4f57557a4d7931684e5451774c5455354d6a4574595445304e4330784e54526d5a6a67335a574d775932496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a35a6a96e9b400c4ded39514d0e65773ca0a3607000000000000000000000000000000000000000000000000000009184e9ea7a8000000000000000000000000000000000000000000000000000009184e72a00000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffaa8b0f34c490823ad9183fe1cb98dfb38004fae1f7e9f2ccccd4abce9bfc42",
      "signature": {
        "s": "0x4e20d0b9b748b3e515bb750e26d087e4ff1ffdd16e38c5f6898dca375ed4a8b8",
        "r": "0x1ea55fa296ee406fc7b1339b1f66539a2b0af98878120d3db393e2f12e3f39cf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1bcd77f7acb5250bbcdb46e5697b50f0b5672957e68e6a08b7c2218ecc8c1591",
      "signature": {
        "s": "0x074461e0a6b6e278a6f3cee4ffbe773c9280047da04381ed67e02cd7ef8bfe7b",
        "r": "0x34c198a276ec07d8bbf18f637967f8393a024d92951376d078f79c447615169f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2885544",
    "total": "2885544"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2885544",
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
            "amount": "211110"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2885"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZThlOWUzMy1hNTQwLTU5MjEtYTE0NC0xNTRmZjg3ZWMwY2IifQ==",
    "nonce": 60,
    "balances": {
      "current": "10000001873254986",
      "previous": "10000001876143415"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa35a6a96e9b400c4ded39514d0e65773ca0a3607",
    "nonce": 22,
    "balances": {
      "current": "10000002885544",
      "previous": "10000000000000"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:25.810Z",
  "updated": "2020-05-22T07:59:25.884Z",
  "id": "5ec7865db0c6090011d5a8e7"
}
```
* *stageAmount*: `10000002885544`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000002c07a8000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000002c07a800000000000000000000000000000000000000000000000000000000002c07a8ffaa8b0f34c490823ad9183fe1cb98dfb38004fae1f7e9f2ccccd4abce9bfc421ea55fa296ee406fc7b1339b1f66539a2b0af98878120d3db393e2f12e3f39cf4e20d0b9b748b3e515bb750e26d087e4ff1ffdd16e38c5f6898dca375ed4a8b8000000000000000000000000000000000000000000000000000000000000001b1bcd77f7acb5250bbcdb46e5697b50f0b5672957e68e6a08b7c2218ecc8c159134c198a276ec07d8bbf18f637967f8393a024d92951376d078f79c447615169f074461e0a6b6e278a6f3cee4ffbe773c9280047da04381ed67e02cd7ef8bfe7b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55b70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000003c00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2df689a4a000000000000000000000000000000000000000000000000002386f2df94ad3700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000b450000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000338a600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a54686c4f57557a4d7931684e5451774c5455354d6a4574595445304e4330784e54526d5a6a67335a574d775932496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000a35a6a96e9b400c4ded39514d0e65773ca0a3607000000000000000000000000000000000000000000000000000009184e9ea7a8000000000000000000000000000000000000000000000000000009184e72a00000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xffaa8b0f34c490823ad9183fe1cb98dfb38004fae1f7e9f2ccccd4abce9bfc42",
      "signature": {
        "s": "0x4e20d0b9b748b3e515bb750e26d087e4ff1ffdd16e38c5f6898dca375ed4a8b8",
        "r": "0x1ea55fa296ee406fc7b1339b1f66539a2b0af98878120d3db393e2f12e3f39cf",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x1bcd77f7acb5250bbcdb46e5697b50f0b5672957e68e6a08b7c2218ecc8c1591",
      "signature": {
        "s": "0x074461e0a6b6e278a6f3cee4ffbe773c9280047da04381ed67e02cd7ef8bfe7b",
        "r": "0x34c198a276ec07d8bbf18f637967f8393a024d92951376d078f79c447615169f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2885544",
    "total": "2885544"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2885544",
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
            "amount": "211110"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2885"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiI0ZThlOWUzMy1hNTQwLTU5MjEtYTE0NC0xNTRmZjg3ZWMwY2IifQ==",
    "nonce": 60,
    "balances": {
      "current": "10000001873254986",
      "previous": "10000001876143415"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa35a6a96e9b400c4ded39514d0e65773ca0a3607",
    "nonce": 22,
    "balances": {
      "current": "10000002885544",
      "previous": "10000000000000"
    }
  },
  "blockNumber": "10114487",
  "created": "2020-05-22T07:59:25.810Z",
  "updated": "2020-05-22T07:59:25.884Z",
  "id": "5ec7865db0c6090011d5a8e7"
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
0x0f200f9b000000000000000000000000000000000000000000000000000009184e9ea7a80000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `10000002885544`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``