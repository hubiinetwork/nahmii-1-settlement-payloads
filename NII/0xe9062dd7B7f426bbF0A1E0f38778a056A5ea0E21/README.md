# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe9062dd7B7f426bbF0A1E0f38778a056A5ea0E21`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de151f8216e117100000000000000000000000000000000000000000000000000000a215fdb58b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000a215fdb58b50000000000000000000000000000000000000000000000a5f7fec787cee90515240091591ad25115a736c83f36cf5050a12f9da171971ef15dbecf98d512e42bab9dbbad47f282b1526c87895a883d8ea8eb5be16de7bfdbb7723445edc372cc54cdec054a30da6b261779cc0ee1d1992e2b1af47c37122fdec7b16770809317000000000000000000000000000000000000000000000000000000000000001caec77cc80325da1f13392965b849b15d3e7fad2ef5a880e1aa8ee83bdb31ace5d4069eadece22954f9d1c578880abce48d177eaf809cb5f694979e15cce97f1f071244f76b1f3115b1013fb209708b31a68c1531e153668cd32cef916591a71a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b525000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034f65d7a048050a610f40000000000000000000000000000000000000000000034f65d7a0ea44868ccd200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000297e763290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ded684bb4022b7200b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f5755314e324d7a4f53316b4d6d59784c5455354e544174596a686c4d4330354d7a677a4e6a51314f4755354f44596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e9062dd7b7f426bbf0a1e0f38778a056a5ea0e210000000000000000000000000000000000000000000000000de151f8216e11710000000000000000000000000000000000000000000000000de147d6c192b8bc00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000030ece67558d260000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x240091591ad25115a736c83f36cf5050a12f9da171971ef15dbecf98d512e42b",
      "signature": {
        "s": "0x54cdec054a30da6b261779cc0ee1d1992e2b1af47c37122fdec7b16770809317",
        "r": "0xab9dbbad47f282b1526c87895a883d8ea8eb5be16de7bfdbb7723445edc372cc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaec77cc80325da1f13392965b849b15d3e7fad2ef5a880e1aa8ee83bdb31ace5",
      "signature": {
        "s": "0x071244f76b1f3115b1013fb209708b31a68c1531e153668cd32cef916591a71a",
        "r": "0xd4069eadece22954f9d1c578880abce48d177eaf809cb5f694979e15cce97f1f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11138458409141",
    "total": "3061582711919634613525"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11138458409141",
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
            "amount": "27722467284416923639819"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11138458409"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwOWU1N2MzOS1kMmYxLTU5NTAtYjhlMC05MzgzNjQ1OGU5ODYifQ==",
    "nonce": 111909,
    "balances": {
      "current": "250107691852495942193396",
      "previous": "250107691863645539060946"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "3525446000000000000"
          }
        }
      ]
    },
    "wallet": "0xe9062dd7b7f426bbf0a1e0f38778a056a5ea0e21",
    "nonce": 22,
    "balances": {
      "current": "1000170718407561585",
      "previous": "1000159579949152444"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:56.644Z",
  "updated": "2022-05-04T09:00:56.720Z",
  "id": "627240c8bbd75600116d073c"
}
```
* *stageAmount*: `1000170718407561585`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000068000000000000000000000000000000000000000000000000000000a215fdb58b50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000a215fdb58b50000000000000000000000000000000000000000000000a5f7fec787cee90515240091591ad25115a736c83f36cf5050a12f9da171971ef15dbecf98d512e42bab9dbbad47f282b1526c87895a883d8ea8eb5be16de7bfdbb7723445edc372cc54cdec054a30da6b261779cc0ee1d1992e2b1af47c37122fdec7b16770809317000000000000000000000000000000000000000000000000000000000000001caec77cc80325da1f13392965b849b15d3e7fad2ef5a880e1aa8ee83bdb31ace5d4069eadece22954f9d1c578880abce48d177eaf809cb5f694979e15cce97f1f071244f76b1f3115b1013fb209708b31a68c1531e153668cd32cef916591a71a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e000000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b525000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034f65d7a048050a610f40000000000000000000000000000000000000000000034f65d7a0ea44868ccd200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000297e763290000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ded684bb4022b7200b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774f5755314e324d7a4f53316b4d6d59784c5455354e544174596a686c4d4330354d7a677a4e6a51314f4755354f44596966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000e9062dd7b7f426bbf0a1e0f38778a056a5ea0e210000000000000000000000000000000000000000000000000de151f8216e11710000000000000000000000000000000000000000000000000de147d6c192b8bc00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000030ece67558d260000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x240091591ad25115a736c83f36cf5050a12f9da171971ef15dbecf98d512e42b",
      "signature": {
        "s": "0x54cdec054a30da6b261779cc0ee1d1992e2b1af47c37122fdec7b16770809317",
        "r": "0xab9dbbad47f282b1526c87895a883d8ea8eb5be16de7bfdbb7723445edc372cc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xaec77cc80325da1f13392965b849b15d3e7fad2ef5a880e1aa8ee83bdb31ace5",
      "signature": {
        "s": "0x071244f76b1f3115b1013fb209708b31a68c1531e153668cd32cef916591a71a",
        "r": "0xd4069eadece22954f9d1c578880abce48d177eaf809cb5f694979e15cce97f1f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11138458409141",
    "total": "3061582711919634613525"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11138458409141",
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
            "amount": "27722467284416923639819"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11138458409"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwOWU1N2MzOS1kMmYxLTU5NTAtYjhlMC05MzgzNjQ1OGU5ODYifQ==",
    "nonce": 111909,
    "balances": {
      "current": "250107691852495942193396",
      "previous": "250107691863645539060946"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "3525446000000000000"
          }
        }
      ]
    },
    "wallet": "0xe9062dd7b7f426bbf0a1e0f38778a056a5ea0e21",
    "nonce": 22,
    "balances": {
      "current": "1000170718407561585",
      "previous": "1000159579949152444"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:56.644Z",
  "updated": "2022-05-04T09:00:56.720Z",
  "id": "627240c8bbd75600116d073c"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de151f8216e11710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000170718407561585`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`