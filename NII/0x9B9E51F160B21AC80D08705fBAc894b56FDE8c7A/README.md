# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x9B9E51F160B21AC80D08705fBAc894b56FDE8c7A`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000130bb868bf54b7f6bc00000000000000000000000000000000000000000000000073990a7967ceeaea0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073990a7967ceeaea00000000000000000000000000000000000000000000000cabc9804b91fc9f70cc9a71c0a52a9d790325c30074cef50cbd9b458eb84687adbeecebb490d93cf38250380d9ad78429d04230d246752387289d4cc7b24261d2a3ac15bb3186ce0d4665aab458008eba45e58adbb5d58daefac7f9ff9a7dfe9b45391542352b6da9000000000000000000000000000000000000000000000000000000000000001b9f233f751904111c3d422f4f4918ec70c70b9bc7ca9d9506b09d163abe63a9fcfe2e9d971f8a9d538410d557767e078f93d8aa70543afca1458390e4c43bdfd83c05e4c354ab569f953d1aa1b1a6ff39eb63d34b2827ce15c886d2e78436b649000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae2e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096332d0e43d445d87c4c000000000000000000000000000000000000000000009633a0c4e61f352e85a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d97d187871e710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f853398661a3a6f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930596a5a6b595455345a53316c5a44466a4c54566b5a6d59744f5449354d4330784d324e694e7a566b4d544134597a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009b9e51f160b21ac80d08705fbac894b56fde8c7a0000000000000000000000000000000000000000000000130bb868bf54b7f6bc000000000000000000000000000000000000000000000012981f5e45ece90bd200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcc9a71c0a52a9d790325c30074cef50cbd9b458eb84687adbeecebb490d93cf3",
      "signature": {
        "s": "0x4665aab458008eba45e58adbb5d58daefac7f9ff9a7dfe9b45391542352b6da9",
        "r": "0x8250380d9ad78429d04230d246752387289d4cc7b24261d2a3ac15bb3186ce0d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9f233f751904111c3d422f4f4918ec70c70b9bc7ca9d9506b09d163abe63a9fc",
      "signature": {
        "s": "0x3c05e4c354ab569f953d1aa1b1a6ff39eb63d34b2827ce15c886d2e78436b649",
        "r": "0xfe2e9d971f8a9d538410d557767e078f93d8aa70543afca1458390e4c43bdfd8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8329700502347377386",
    "total": "233739494997379293040"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8329700502347377386",
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
            "amount": "27263734705862807365365"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8329700502347377"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YjZkYTU4ZS1lZDFjLTVkZmYtOTI5MC0xM2NiNzVkMTA4YzMifQ==",
    "nonce": 110126,
    "balances": {
      "current": "709299002985166333836364",
      "previous": "709307341015369183561127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b9e51f160b21ac80d08705fbac894b56fde8c7a",
    "nonce": 46,
    "balances": {
      "current": "351332677501582833340",
      "previous": "343002976999235455954"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:40.322Z",
  "updated": "2022-05-04T08:51:40.431Z",
  "id": "62723e9c3592fd001130b477"
}
```
* *stageAmount*: `351332677501582833340`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000073990a7967ceeaea0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000073990a7967ceeaea00000000000000000000000000000000000000000000000cabc9804b91fc9f70cc9a71c0a52a9d790325c30074cef50cbd9b458eb84687adbeecebb490d93cf38250380d9ad78429d04230d246752387289d4cc7b24261d2a3ac15bb3186ce0d4665aab458008eba45e58adbb5d58daefac7f9ff9a7dfe9b45391542352b6da9000000000000000000000000000000000000000000000000000000000000001b9f233f751904111c3d422f4f4918ec70c70b9bc7ca9d9506b09d163abe63a9fcfe2e9d971f8a9d538410d557767e078f93d8aa70543afca1458390e4c43bdfd83c05e4c354ab569f953d1aa1b1a6ff39eb63d34b2827ce15c886d2e78436b649000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae2e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096332d0e43d445d87c4c000000000000000000000000000000000000000000009633a0c4e61f352e85a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001d97d187871e710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f853398661a3a6f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930596a5a6b595455345a53316c5a44466a4c54566b5a6d59744f5449354d4330784d324e694e7a566b4d544134597a4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000009b9e51f160b21ac80d08705fbac894b56fde8c7a0000000000000000000000000000000000000000000000130bb868bf54b7f6bc000000000000000000000000000000000000000000000012981f5e45ece90bd200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xcc9a71c0a52a9d790325c30074cef50cbd9b458eb84687adbeecebb490d93cf3",
      "signature": {
        "s": "0x4665aab458008eba45e58adbb5d58daefac7f9ff9a7dfe9b45391542352b6da9",
        "r": "0x8250380d9ad78429d04230d246752387289d4cc7b24261d2a3ac15bb3186ce0d",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x9f233f751904111c3d422f4f4918ec70c70b9bc7ca9d9506b09d163abe63a9fc",
      "signature": {
        "s": "0x3c05e4c354ab569f953d1aa1b1a6ff39eb63d34b2827ce15c886d2e78436b649",
        "r": "0xfe2e9d971f8a9d538410d557767e078f93d8aa70543afca1458390e4c43bdfd8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "8329700502347377386",
    "total": "233739494997379293040"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8329700502347377386",
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
            "amount": "27263734705862807365365"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8329700502347377"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YjZkYTU4ZS1lZDFjLTVkZmYtOTI5MC0xM2NiNzVkMTA4YzMifQ==",
    "nonce": 110126,
    "balances": {
      "current": "709299002985166333836364",
      "previous": "709307341015369183561127"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x9b9e51f160b21ac80d08705fbac894b56fde8c7a",
    "nonce": 46,
    "balances": {
      "current": "351332677501582833340",
      "previous": "343002976999235455954"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:40.322Z",
  "updated": "2022-05-04T08:51:40.431Z",
  "id": "62723e9c3592fd001130b477"
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
0x0f200f9b0000000000000000000000000000000000000000000000130bb868bf54b7f6bc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `351332677501582833340`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`