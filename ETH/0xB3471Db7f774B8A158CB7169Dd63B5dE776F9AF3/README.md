# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB3471Db7f774B8A158CB7169Dd63B5dE776F9AF3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000002012f000000000000000000000000000000000000000000000000000000000002012f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002012f000000000000000000000000000000000000000000000000000000000002012f3b5eae15caf1cd6304ad4d9e4ade1787d8dbc1449aa0f3a1d893c34dacd7f38297248e0cae4bdcef2f14011da6bc23841afa4f974795c8c36919f05d242b8d6314bfce13df333e0ace568c789a47f56df0a72b58cc2483e9121b73fbf8575152000000000000000000000000000000000000000000000000000000000000001c59d1cf53e320ac5d11463fbae002dfa28dcb28bc01918d320d0ddb701717da53d33f8eebe64a3c5cf6e2bf543f91d00dbaf5050c1ce849c87101aff96aa90fd91e12c27b3563130562939b8dd40f1088f8f78d53cf992e96a8d280389945089e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcabb665000000000000000000000000000000000000000000000000002386f2bcadb81700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000830000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c186c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f444d355a474d35596930794d6d55344c5455324e5755744f474a6b4d6930774d57466d4e6a51344f5759314e57516966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000b3471db7f774b8a158cb7169dd63b5de776f9af3000000000000000000000000000000000000000000000000000000000002012f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b5eae15caf1cd6304ad4d9e4ade1787d8dbc1449aa0f3a1d893c34dacd7f382",
      "signature": {
        "s": "0x14bfce13df333e0ace568c789a47f56df0a72b58cc2483e9121b73fbf8575152",
        "r": "0x97248e0cae4bdcef2f14011da6bc23841afa4f974795c8c36919f05d242b8d63",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59d1cf53e320ac5d11463fbae002dfa28dcb28bc01918d320d0ddb701717da53",
      "signature": {
        "s": "0x1e12c27b3563130562939b8dd40f1088f8f78d53cf992e96a8d280389945089e",
        "r": "0xd33f8eebe64a3c5cf6e2bf543f91d00dbaf5050c1ce849c87101aff96aa90fd9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "131375",
    "total": "131375"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "131375",
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
            "amount": "792684"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmODM5ZGM5Yi0yMmU4LTU2NWUtOGJkMi0wMWFmNjQ4OWY1NWQifQ==",
    "nonce": 2159,
    "balances": {
      "current": "10000001290450533",
      "previous": "10000001290582039"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3471db7f774b8a158cb7169dd63b5de776f9af3",
    "nonce": 19,
    "balances": {
      "current": "131375",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:43.830Z",
  "updated": "2020-05-22T08:14:43.895Z",
  "id": "5ec789f3e5756b00111b8230"
}
```
* *stageAmount*: `131375`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000002012f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000002012f000000000000000000000000000000000000000000000000000000000002012f3b5eae15caf1cd6304ad4d9e4ade1787d8dbc1449aa0f3a1d893c34dacd7f38297248e0cae4bdcef2f14011da6bc23841afa4f974795c8c36919f05d242b8d6314bfce13df333e0ace568c789a47f56df0a72b58cc2483e9121b73fbf8575152000000000000000000000000000000000000000000000000000000000000001c59d1cf53e320ac5d11463fbae002dfa28dcb28bc01918d320d0ddb701717da53d33f8eebe64a3c5cf6e2bf543f91d00dbaf5050c1ce849c87101aff96aa90fd91e12c27b3563130562939b8dd40f1088f8f78d53cf992e96a8d280389945089e000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000086f00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bcabb665000000000000000000000000000000000000000000000000002386f2bcadb81700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000830000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c186c00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4f444d355a474d35596930794d6d55344c5455324e5755744f474a6b4d6930774d57466d4e6a51344f5759314e57516966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000b3471db7f774b8a158cb7169dd63b5de776f9af3000000000000000000000000000000000000000000000000000000000002012f000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b5eae15caf1cd6304ad4d9e4ade1787d8dbc1449aa0f3a1d893c34dacd7f382",
      "signature": {
        "s": "0x14bfce13df333e0ace568c789a47f56df0a72b58cc2483e9121b73fbf8575152",
        "r": "0x97248e0cae4bdcef2f14011da6bc23841afa4f974795c8c36919f05d242b8d63",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x59d1cf53e320ac5d11463fbae002dfa28dcb28bc01918d320d0ddb701717da53",
      "signature": {
        "s": "0x1e12c27b3563130562939b8dd40f1088f8f78d53cf992e96a8d280389945089e",
        "r": "0xd33f8eebe64a3c5cf6e2bf543f91d00dbaf5050c1ce849c87101aff96aa90fd9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "131375",
    "total": "131375"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "131375",
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
            "amount": "792684"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "131"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJmODM5ZGM5Yi0yMmU4LTU2NWUtOGJkMi0wMWFmNjQ4OWY1NWQifQ==",
    "nonce": 2159,
    "balances": {
      "current": "10000001290450533",
      "previous": "10000001290582039"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3471db7f774b8a158cb7169dd63b5de776f9af3",
    "nonce": 19,
    "balances": {
      "current": "131375",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:43.830Z",
  "updated": "2020-05-22T08:14:43.895Z",
  "id": "5ec789f3e5756b00111b8230"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000002012f0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `131375`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``