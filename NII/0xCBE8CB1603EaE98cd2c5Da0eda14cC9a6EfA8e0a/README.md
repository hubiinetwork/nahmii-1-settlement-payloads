# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCBE8CB1603EaE98cd2c5Da0eda14cC9a6EfA8e0a`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000261770d28ff787482d000000000000000000000000000000000000000000000000e73214f2cf9f6c570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9f6c5700000000000000000000000000000000000000000000001957930097242a2cd83bb4cfe93b62439aba24af8bdd341591e078376ed3bfe64a3c9db6ff73c8fdfb7bfe7428e81610d69b783beb5c48a2c8abef714d9c6d92551d21507fecb3f06d26bc1cabd159daaa7b65ee8a0e1919ff8e1b58a7998f10b258e3a7c81301868c000000000000000000000000000000000000000000000000000000000000001bee1396349b56a6f8ac419e5991b03141091536844f0706bfd582357b3b89b1f580e886130538f6c29df576becaf9bf22a47b95d0f3c0c9471ab65e04da6a9a697ae89020d2f4de2507bfdba18bff323d405e4dd1e23e48f8812ee2bc1c4edc9f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ada9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000966a6976ff57b516bde600000000000000000000000000000000000000000000966b50e443ed93c4678700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d4a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ea32e574179e386e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5745784d44637a4f5330304d4441324c5455334e6d5974596a637a59533031597a51794e5745304e7a63324e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cbe8cb1603eae98cd2c5da0eda14cc9a6efa8e0a0000000000000000000000000000000000000000000000261770d28ff787482d000000000000000000000000000000000000000000000025303ebd9d27e7dbd600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3bb4cfe93b62439aba24af8bdd341591e078376ed3bfe64a3c9db6ff73c8fdfb",
      "signature": {
        "s": "0x26bc1cabd159daaa7b65ee8a0e1919ff8e1b58a7998f10b258e3a7c81301868c",
        "r": "0x7bfe7428e81610d69b783beb5c48a2c8abef714d9c6d92551d21507fecb3f06d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xee1396349b56a6f8ac419e5991b03141091536844f0706bfd582357b3b89b1f5",
      "signature": {
        "s": "0x7ae89020d2f4de2507bfdba18bff323d405e4dd1e23e48f8812ee2bc1c4edc9f",
        "r": "0x80e886130538f6c29df576becaf9bf22a47b95d0f3c0c9471ab65e04da6a9a69",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694858839",
    "total": "467478989994761792728"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694858839",
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
            "amount": "27262716799909493618798"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694858"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNWExMDczOS00MDA2LTU3NmYtYjczYS01YzQyNWE0Nzc2NzMifQ==",
    "nonce": 109993,
    "balances": {
      "current": "710317926844433394220518",
      "previous": "710334602904839093774215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcbe8cb1603eae98cd2c5da0eda14cc9a6efa8e0a",
    "nonce": 46,
    "balances": {
      "current": "702665356177001891885",
      "previous": "686005955172307033046"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:50:59.231Z",
  "updated": "2022-05-04T08:50:59.312Z",
  "id": "62723e733592fd001130b445"
}
```
* *stageAmount*: `702665356177001891885`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000e73214f2cf9f6c570000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9f6c5700000000000000000000000000000000000000000000001957930097242a2cd83bb4cfe93b62439aba24af8bdd341591e078376ed3bfe64a3c9db6ff73c8fdfb7bfe7428e81610d69b783beb5c48a2c8abef714d9c6d92551d21507fecb3f06d26bc1cabd159daaa7b65ee8a0e1919ff8e1b58a7998f10b258e3a7c81301868c000000000000000000000000000000000000000000000000000000000000001bee1396349b56a6f8ac419e5991b03141091536844f0706bfd582357b3b89b1f580e886130538f6c29df576becaf9bf22a47b95d0f3c0c9471ab65e04da6a9a697ae89020d2f4de2507bfdba18bff323d405e4dd1e23e48f8812ee2bc1c4edc9f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ada9000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000966a6976ff57b516bde600000000000000000000000000000000000000000000966b50e443ed93c4678700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d4a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ea32e574179e386e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e5745784d44637a4f5330304d4441324c5455334e6d5974596a637a59533031597a51794e5745304e7a63324e7a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cbe8cb1603eae98cd2c5da0eda14cc9a6efa8e0a0000000000000000000000000000000000000000000000261770d28ff787482d000000000000000000000000000000000000000000000025303ebd9d27e7dbd600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3bb4cfe93b62439aba24af8bdd341591e078376ed3bfe64a3c9db6ff73c8fdfb",
      "signature": {
        "s": "0x26bc1cabd159daaa7b65ee8a0e1919ff8e1b58a7998f10b258e3a7c81301868c",
        "r": "0x7bfe7428e81610d69b783beb5c48a2c8abef714d9c6d92551d21507fecb3f06d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xee1396349b56a6f8ac419e5991b03141091536844f0706bfd582357b3b89b1f5",
      "signature": {
        "s": "0x7ae89020d2f4de2507bfdba18bff323d405e4dd1e23e48f8812ee2bc1c4edc9f",
        "r": "0x80e886130538f6c29df576becaf9bf22a47b95d0f3c0c9471ab65e04da6a9a69",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694858839",
    "total": "467478989994761792728"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694858839",
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
            "amount": "27262716799909493618798"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694858"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNWExMDczOS00MDA2LTU3NmYtYjczYS01YzQyNWE0Nzc2NzMifQ==",
    "nonce": 109993,
    "balances": {
      "current": "710317926844433394220518",
      "previous": "710334602904839093774215"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcbe8cb1603eae98cd2c5da0eda14cc9a6efa8e0a",
    "nonce": 46,
    "balances": {
      "current": "702665356177001891885",
      "previous": "686005955172307033046"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:50:59.231Z",
  "updated": "2022-05-04T08:50:59.312Z",
  "id": "62723e733592fd001130b445"
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
0x0f200f9b0000000000000000000000000000000000000000000000261770d28ff787482d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `702665356177001891885`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`