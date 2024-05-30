# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xAFe9e1431c0286A5B4DDD31f4eBAf9Cfd71049E7`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000053b000000000000000000000000000000000000000000000000000000000000053b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000053b000000000000000000000000000000000000000000000000000000000000053b832243596b3ea780860ac9d3daf0d5c2300a06dfcca4ea7d7a112c5e953952d73208082471ea887a286788bd8796880f918881bca76ba21ccaa0dd6338f75dec067b680a96d9e7ee931b21b99d5a207f21638f4d7ee3993360008f536365160c000000000000000000000000000000000000000000000000000000000000001c537ed1191cb19c4ffcf3b3b160b9904145abb68c88f11b684b28cf9a0d23d900318fd84032b3248c64ec93e177f79490f911f9039c3d9403df7397372674511f71531b8e7170dede25b9867a1441eeb70c89429cb2286b385b6ab59832bef55b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b7a8c000000000000000000000000000000000000000000000000002386f2bc3b7fc800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5459354d4467354f53316d4f5451324c5455344e7a41744f47566b59533030596a6b795a4459784e474e6b4e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000afe9e1431c0286a5b4ddd31f4ebaf9cfd71049e7000000000000000000000000000000000000000000000000000000000000053b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x832243596b3ea780860ac9d3daf0d5c2300a06dfcca4ea7d7a112c5e953952d7",
      "signature": {
        "s": "0x067b680a96d9e7ee931b21b99d5a207f21638f4d7ee3993360008f536365160c",
        "r": "0x3208082471ea887a286788bd8796880f918881bca76ba21ccaa0dd6338f75dec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x537ed1191cb19c4ffcf3b3b160b9904145abb68c88f11b684b28cf9a0d23d900",
      "signature": {
        "s": "0x71531b8e7170dede25b9867a1441eeb70c89429cb2286b385b6ab59832bef55b",
        "r": "0x318fd84032b3248c64ec93e177f79490f911f9039c3d9403df7397372674511f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1339",
    "total": "1339"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1339",
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
            "amount": "800043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTY5MDg5OS1mOTQ2LTU4NzAtOGVkYS00YjkyZDYxNGNkNmMifQ==",
    "nonce": 2408,
    "balances": {
      "current": "10000001283095180",
      "previous": "10000001283096520"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xafe9e1431c0286a5b4ddd31f4ebaf9cfd71049e7",
    "nonce": 10,
    "balances": {
      "current": "1339",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:18.604Z",
  "updated": "2020-05-22T08:16:18.675Z",
  "id": "5ec78a52005df800101bc54c"
}
```
* *stageAmount*: `1339`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000053b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000053b000000000000000000000000000000000000000000000000000000000000053b832243596b3ea780860ac9d3daf0d5c2300a06dfcca4ea7d7a112c5e953952d73208082471ea887a286788bd8796880f918881bca76ba21ccaa0dd6338f75dec067b680a96d9e7ee931b21b99d5a207f21638f4d7ee3993360008f536365160c000000000000000000000000000000000000000000000000000000000000001c537ed1191cb19c4ffcf3b3b160b9904145abb68c88f11b684b28cf9a0d23d900318fd84032b3248c64ec93e177f79490f911f9039c3d9403df7397372674511f71531b8e7170dede25b9867a1441eeb70c89429cb2286b385b6ab59832bef55b000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55fa0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000096800000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc3b7a8c000000000000000000000000000000000000000000000000002386f2bc3b7fc800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c352b00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949785a5459354d4467354f53316d4f5451324c5455344e7a41744f47566b59533030596a6b795a4459784e474e6b4e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000000a000000000000000000000000afe9e1431c0286a5b4ddd31f4ebaf9cfd71049e7000000000000000000000000000000000000000000000000000000000000053b000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x832243596b3ea780860ac9d3daf0d5c2300a06dfcca4ea7d7a112c5e953952d7",
      "signature": {
        "s": "0x067b680a96d9e7ee931b21b99d5a207f21638f4d7ee3993360008f536365160c",
        "r": "0x3208082471ea887a286788bd8796880f918881bca76ba21ccaa0dd6338f75dec",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x537ed1191cb19c4ffcf3b3b160b9904145abb68c88f11b684b28cf9a0d23d900",
      "signature": {
        "s": "0x71531b8e7170dede25b9867a1441eeb70c89429cb2286b385b6ab59832bef55b",
        "r": "0x318fd84032b3248c64ec93e177f79490f911f9039c3d9403df7397372674511f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1339",
    "total": "1339"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1339",
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
            "amount": "800043"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIxZTY5MDg5OS1mOTQ2LTU4NzAtOGVkYS00YjkyZDYxNGNkNmMifQ==",
    "nonce": 2408,
    "balances": {
      "current": "10000001283095180",
      "previous": "10000001283096520"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xafe9e1431c0286a5b4ddd31f4ebaf9cfd71049e7",
    "nonce": 10,
    "balances": {
      "current": "1339",
      "previous": "0"
    }
  },
  "blockNumber": "10114554",
  "created": "2020-05-22T08:16:18.604Z",
  "updated": "2020-05-22T08:16:18.675Z",
  "id": "5ec78a52005df800101bc54c"
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
0x0f200f9b000000000000000000000000000000000000000000000000000000000000053b0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1339`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``