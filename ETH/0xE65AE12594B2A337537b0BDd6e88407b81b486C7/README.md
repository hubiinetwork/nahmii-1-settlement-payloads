# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xE65AE12594B2A337537b0BDd6e88407b81b486C7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000060f400000000000000000000000000000000000000000000000000000000000060f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000060f400000000000000000000000000000000000000000000000000000000000060f4a49ff035ef73108ebeaac28e6f8e08905f739687a685088bb91d17e7cd84338bf58dc7b0415eb77dbb846dc3de508447665d0961fdc94803b848bd56f4b249726d9b261c8d1da2cbe9eef503f6069f89d82068b2aefce97b74ceaa07f06cda1b000000000000000000000000000000000000000000000000000000000000001bd2e2d9df1682e4a821a263897dde495edd64c2b5fa099ada2ab9878465d9cb6eb65837b4526b585fdd66a81155fae99e013730782cd7a169b93d81842a67798471564d79203de9600dfcccfebea087d1798ac37284c982067e5a5e0f2249ceff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb0eb9d8000000000000000000000000000000000000000000000000002386f2cb0f1ae400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000018000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086c6a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795954426859575a6d5a5330325a6a4a6b4c5455314d475574596a526a5a53316a5a5459794f544d7a4d4759324d44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e65ae12594b2a337537b0bdd6e88407b81b486c700000000000000000000000000000000000000000000000000000000000060f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa49ff035ef73108ebeaac28e6f8e08905f739687a685088bb91d17e7cd84338b",
      "signature": {
        "s": "0x6d9b261c8d1da2cbe9eef503f6069f89d82068b2aefce97b74ceaa07f06cda1b",
        "r": "0xf58dc7b0415eb77dbb846dc3de508447665d0961fdc94803b848bd56f4b24972",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2e2d9df1682e4a821a263897dde495edd64c2b5fa099ada2ab9878465d9cb6e",
      "signature": {
        "s": "0x71564d79203de9600dfcccfebea087d1798ac37284c982067e5a5e0f2249ceff",
        "r": "0xb65837b4526b585fdd66a81155fae99e013730782cd7a169b93d81842a677984",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24820",
    "total": "24820"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24820",
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
            "amount": "552042"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "24"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTBhYWZmZS02ZjJkLTU1MGUtYjRjZS1jZTYyOTMzMGY2MDAifQ==",
    "nonce": 617,
    "balances": {
      "current": "10000001531820504",
      "previous": "10000001531845348"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe65ae12594b2a337537b0bdd6e88407b81b486c7",
    "nonce": 20,
    "balances": {
      "current": "24820",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:23.782Z",
  "updated": "2020-05-22T08:03:24.870Z",
  "id": "5ec7874be5756b00111b803d"
}
```
* *stageAmount*: `24820`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000060f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000060f400000000000000000000000000000000000000000000000000000000000060f4a49ff035ef73108ebeaac28e6f8e08905f739687a685088bb91d17e7cd84338bf58dc7b0415eb77dbb846dc3de508447665d0961fdc94803b848bd56f4b249726d9b261c8d1da2cbe9eef503f6069f89d82068b2aefce97b74ceaa07f06cda1b000000000000000000000000000000000000000000000000000000000000001bd2e2d9df1682e4a821a263897dde495edd64c2b5fa099ada2ab9878465d9cb6eb65837b4526b585fdd66a81155fae99e013730782cd7a169b93d81842a67798471564d79203de9600dfcccfebea087d1798ac37284c982067e5a5e0f2249ceff000000000000000000000000000000000000000000000000000000000000001c00000000000000000000000000000000000000000000000000000000009a55c80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000026900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2cb0eb9d8000000000000000000000000000000000000000000000000002386f2cb0f1ae400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000000018000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000086c6a00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949795954426859575a6d5a5330325a6a4a6b4c5455314d475574596a526a5a53316a5a5459794f544d7a4d4759324d44416966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000e65ae12594b2a337537b0bdd6e88407b81b486c700000000000000000000000000000000000000000000000000000000000060f4000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa49ff035ef73108ebeaac28e6f8e08905f739687a685088bb91d17e7cd84338b",
      "signature": {
        "s": "0x6d9b261c8d1da2cbe9eef503f6069f89d82068b2aefce97b74ceaa07f06cda1b",
        "r": "0xf58dc7b0415eb77dbb846dc3de508447665d0961fdc94803b848bd56f4b24972",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd2e2d9df1682e4a821a263897dde495edd64c2b5fa099ada2ab9878465d9cb6e",
      "signature": {
        "s": "0x71564d79203de9600dfcccfebea087d1798ac37284c982067e5a5e0f2249ceff",
        "r": "0xb65837b4526b585fdd66a81155fae99e013730782cd7a169b93d81842a677984",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "24820",
    "total": "24820"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "24820",
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
            "amount": "552042"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "24"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyYTBhYWZmZS02ZjJkLTU1MGUtYjRjZS1jZTYyOTMzMGY2MDAifQ==",
    "nonce": 617,
    "balances": {
      "current": "10000001531820504",
      "previous": "10000001531845348"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe65ae12594b2a337537b0bdd6e88407b81b486c7",
    "nonce": 20,
    "balances": {
      "current": "24820",
      "previous": "0"
    }
  },
  "blockNumber": "10114504",
  "created": "2020-05-22T08:03:23.782Z",
  "updated": "2020-05-22T08:03:24.870Z",
  "id": "5ec7874be5756b00111b803d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000060f40000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `24820`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``
