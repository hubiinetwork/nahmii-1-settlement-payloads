# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x19e225eE5eDF2a61eE79C5937CF607f600073862`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000d0ab0926335a74a74000000000000000000000000000000000000000000000000000000027168ca600000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000027168ca60000000000000000000000000000000000000000000000006f877b62367ae03ff457007631398d1a53a795a52b6b6fffa1022c77c5711d46e9d15a2e863d1a46b3b5d10bbafab908ee848701424ca4ad21ed24e6d112468ef43296872e37f894a70ce7baad9f142354503cac87cb55ae8589c9a7b973647a551d6e13e794b6f12000000000000000000000000000000000000000000000000000000000000001ce62d5e7c5442387e150875852aa5bcf0e202e4d56fdff3d0711b7b84f8af8c24d9e9753b12dadde5c27e761f2741b2926cabfce78e0262591a3a7a0b161587d7547c6d0f02e1e6f12f716762aa38d85157ca8fb756ed09612474bbf88a9d9a15000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af2b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ab2a8840110fa45be30000000000000000000000000000000000000000000095ab2a88401381ad411600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a01ad30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61b1bdcb18a9ccc100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a47566d596a63304d7930314e4455334c545669596d4d744f4445345969307a5a6d5a694e7a4d304e3259774f54416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000019e225ee5edf2a61ee79c5937cf607f60007386200000000000000000000000000000000000000000000000d0ab0926335a74a7400000000000000000000000000000000000000000000000d0ab09260c43e801400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x457007631398d1a53a795a52b6b6fffa1022c77c5711d46e9d15a2e863d1a46b",
      "signature": {
        "s": "0x70ce7baad9f142354503cac87cb55ae8589c9a7b973647a551d6e13e794b6f12",
        "r": "0x3b5d10bbafab908ee848701424ca4ad21ed24e6d112468ef43296872e37f894a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe62d5e7c5442387e150875852aa5bcf0e202e4d56fdff3d0711b7b84f8af8c24",
      "signature": {
        "s": "0x547c6d0f02e1e6f12f716762aa38d85157ca8fb756ed09612474bbf88a9d9a15",
        "r": "0xd9e9753b12dadde5c27e761f2741b2926cabfce78e0262591a3a7a0b161587d7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10492627552",
    "total": "128584443549071574015"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10492627552",
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
            "amount": "27266241138461205384208"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10492627"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZGVmYjc0My01NDU3LTViYmMtODE4Yi0zZmZiNzM0N2YwOTAifQ==",
    "nonce": 110379,
    "balances": {
      "current": "706790063954169916840931",
      "previous": "706790063954180419961110"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x19e225ee5edf2a61ee79c5937cf607f600073862",
    "nonce": 46,
    "balances": {
      "current": "240577949449304099444",
      "previous": "240577949438811471892"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:58.750Z",
  "updated": "2022-05-04T08:52:58.832Z",
  "id": "62723eeabbd75600116d0552"
}
```
* *stageAmount*: `240577949449304099444`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000027168ca600000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000027168ca60000000000000000000000000000000000000000000000006f877b62367ae03ff457007631398d1a53a795a52b6b6fffa1022c77c5711d46e9d15a2e863d1a46b3b5d10bbafab908ee848701424ca4ad21ed24e6d112468ef43296872e37f894a70ce7baad9f142354503cac87cb55ae8589c9a7b973647a551d6e13e794b6f12000000000000000000000000000000000000000000000000000000000000001ce62d5e7c5442387e150875852aa5bcf0e202e4d56fdff3d0711b7b84f8af8c24d9e9753b12dadde5c27e761f2741b2926cabfce78e0262591a3a7a0b161587d7547c6d0f02e1e6f12f716762aa38d85157ca8fb756ed09612474bbf88a9d9a15000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af2b000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095ab2a8840110fa45be30000000000000000000000000000000000000000000095ab2a88401381ad411600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a01ad30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c61b1bdcb18a9ccc100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a47566d596a63304d7930314e4455334c545669596d4d744f4445345969307a5a6d5a694e7a4d304e3259774f54416966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000019e225ee5edf2a61ee79c5937cf607f60007386200000000000000000000000000000000000000000000000d0ab0926335a74a7400000000000000000000000000000000000000000000000d0ab09260c43e801400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x457007631398d1a53a795a52b6b6fffa1022c77c5711d46e9d15a2e863d1a46b",
      "signature": {
        "s": "0x70ce7baad9f142354503cac87cb55ae8589c9a7b973647a551d6e13e794b6f12",
        "r": "0x3b5d10bbafab908ee848701424ca4ad21ed24e6d112468ef43296872e37f894a",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe62d5e7c5442387e150875852aa5bcf0e202e4d56fdff3d0711b7b84f8af8c24",
      "signature": {
        "s": "0x547c6d0f02e1e6f12f716762aa38d85157ca8fb756ed09612474bbf88a9d9a15",
        "r": "0xd9e9753b12dadde5c27e761f2741b2926cabfce78e0262591a3a7a0b161587d7",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "10492627552",
    "total": "128584443549071574015"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10492627552",
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
            "amount": "27266241138461205384208"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10492627"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZGVmYjc0My01NDU3LTViYmMtODE4Yi0zZmZiNzM0N2YwOTAifQ==",
    "nonce": 110379,
    "balances": {
      "current": "706790063954169916840931",
      "previous": "706790063954180419961110"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x19e225ee5edf2a61ee79c5937cf607f600073862",
    "nonce": 46,
    "balances": {
      "current": "240577949449304099444",
      "previous": "240577949438811471892"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:52:58.750Z",
  "updated": "2022-05-04T08:52:58.832Z",
  "id": "62723eeabbd75600116d0552"
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
0x0f200f9b00000000000000000000000000000000000000000000000d0ab0926335a74a740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `240577949449304099444`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`