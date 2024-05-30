# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9748d0ac74f500307DaD4bEbd77802F4C1339E9A`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000019700000000000000000000000000000000000000000000000000000000000001970000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000019700000000000000000000000000000000000000000000000000000000000001977f6aa221e9acd0935d5296a34791ebf60e3429a0da79ba43e1ebefec5650b617173fc80e02f1520defea4db7f2d4bad308400c4d1074122e26668d76cd25fb003945b091cf1e2cc4c268a54f958dcf999a07f69621f3e46ea8cdd7ee6037d599000000000000000000000000000000000000000000000000000000000000001bbb4822005cfc7fcc6c29efdbd0e6faf84b47514e7cd75392ac38f1ff3653d8783252883d8d943905a6a19c191eb34a003efeae7c4b5bae6d9c443bd12a7901d7793b96f4d87b0563e5aca01b9409e0145d4ac804ffebbb255d43ca32eae06043000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000091b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc51904f000000000000000000000000000000000000000000000000002386f2bc5191e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f7100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d7a68694f57557a4e69316c5957526a4c54566c596a41744f5745775a6930774e5451325a445a694e6a6b7a5a6d496966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000009748d0ac74f500307dad4bebd77802f4c1339e9a0000000000000000000000000000000000000000000000000000000000000197000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7f6aa221e9acd0935d5296a34791ebf60e3429a0da79ba43e1ebefec5650b617",
      "signature": {
        "s": "0x3945b091cf1e2cc4c268a54f958dcf999a07f69621f3e46ea8cdd7ee6037d599",
        "r": "0x173fc80e02f1520defea4db7f2d4bad308400c4d1074122e26668d76cd25fb00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb4822005cfc7fcc6c29efdbd0e6faf84b47514e7cd75392ac38f1ff3653d878",
      "signature": {
        "s": "0x793b96f4d87b0563e5aca01b9409e0145d4ac804ffebbb255d43ca32eae06043",
        "r": "0x3252883d8d943905a6a19c191eb34a003efeae7c4b5bae6d9c443bd12a7901d7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "407",
    "total": "407"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "407",
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
            "amount": "798577"
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
    "data": "eyJyZWYiOiI4MzhiOWUzNi1lYWRjLTVlYjAtOWEwZi0wNTQ2ZDZiNjkzZmIifQ==",
    "nonce": 2331,
    "balances": {
      "current": "10000001284542543",
      "previous": "10000001284542951"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9748d0ac74f500307dad4bebd77802f4c1339e9a",
    "nonce": 4,
    "balances": {
      "current": "407",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:50.688Z",
  "updated": "2020-05-22T08:15:50.753Z",
  "id": "5ec78a36b0c6090011d5abd8"
}
```
* *stageAmount*: `407`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000001970000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000019700000000000000000000000000000000000000000000000000000000000001977f6aa221e9acd0935d5296a34791ebf60e3429a0da79ba43e1ebefec5650b617173fc80e02f1520defea4db7f2d4bad308400c4d1074122e26668d76cd25fb003945b091cf1e2cc4c268a54f958dcf999a07f69621f3e46ea8cdd7ee6037d599000000000000000000000000000000000000000000000000000000000000001bbb4822005cfc7fcc6c29efdbd0e6faf84b47514e7cd75392ac38f1ff3653d8783252883d8d943905a6a19c191eb34a003efeae7c4b5bae6d9c443bd12a7901d7793b96f4d87b0563e5aca01b9409e0145d4ac804ffebbb255d43ca32eae06043000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000091b00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc51904f000000000000000000000000000000000000000000000000002386f2bc5191e700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c2f7100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344d7a68694f57557a4e69316c5957526a4c54566c596a41744f5745775a6930774e5451325a445a694e6a6b7a5a6d496966513d3d00000000000000000000000000000000000000000000000000000000000000040000000000000000000000009748d0ac74f500307dad4bebd77802f4c1339e9a0000000000000000000000000000000000000000000000000000000000000197000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7f6aa221e9acd0935d5296a34791ebf60e3429a0da79ba43e1ebefec5650b617",
      "signature": {
        "s": "0x3945b091cf1e2cc4c268a54f958dcf999a07f69621f3e46ea8cdd7ee6037d599",
        "r": "0x173fc80e02f1520defea4db7f2d4bad308400c4d1074122e26668d76cd25fb00",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbb4822005cfc7fcc6c29efdbd0e6faf84b47514e7cd75392ac38f1ff3653d878",
      "signature": {
        "s": "0x793b96f4d87b0563e5aca01b9409e0145d4ac804ffebbb255d43ca32eae06043",
        "r": "0x3252883d8d943905a6a19c191eb34a003efeae7c4b5bae6d9c443bd12a7901d7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "407",
    "total": "407"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "407",
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
            "amount": "798577"
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
    "data": "eyJyZWYiOiI4MzhiOWUzNi1lYWRjLTVlYjAtOWEwZi0wNTQ2ZDZiNjkzZmIifQ==",
    "nonce": 2331,
    "balances": {
      "current": "10000001284542543",
      "previous": "10000001284542951"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9748d0ac74f500307dad4bebd77802f4c1339e9a",
    "nonce": 4,
    "balances": {
      "current": "407",
      "previous": "0"
    }
  },
  "blockNumber": "10114552",
  "created": "2020-05-22T08:15:50.688Z",
  "updated": "2020-05-22T08:15:50.753Z",
  "id": "5ec78a36b0c6090011d5abd8"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000001970000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `407`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``