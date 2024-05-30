# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa6E45E838379ca2012480DbC87A5fbb4c04DdE10`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000004ae937acf374d376fd0000000000000000000000000000000000000000000000000000000ea843cd010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000ea843cd010000000000000000000000000000000000000000000000267be2a45b1e2e5a294f4b019f433f82ffdc8294f4e2cf21eccb6d71a26c95e1e1fdf2217e06abb4678ef2ca1914215465a30a9a1615a65b635b9cdcff18289d6880a1e9c1549ad5d9500fab347052d9d72d92b74c028e431abc5a0fa7100a08b6696870c6057217de000000000000000000000000000000000000000000000000000000000000001b3f78917a41d69568b2a49a22199acebd4165053cc0849f9726a6ddf9f61cd431a6cfe4c435eb10485f40d5900f48f911cca4a7d8c6d2f148e1550c6296eeb3ce023feda38cbf1e5a5fa89e609c8776ad7beb399ee4189041522f6ebb95f1fa82000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b523000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034f8164a35b880c5bd070000000000000000000000000000000000000000000034f8164a35c72cca1e7500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003c0946d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ded613fef93d0248480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e54426a597a566d4d79316b4f4441354c5455774e4459744f5745345a6930344e545a684e446c6d593245325a57496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a6e45e838379ca2012480dbc87a5fbb4c04dde1000000000000000000000000000000000000000000000004ae937acf374d376fd00000000000000000000000000000000000000000000004ae937ace4cc8fa9fc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f4b019f433f82ffdc8294f4e2cf21eccb6d71a26c95e1e1fdf2217e06abb467",
      "signature": {
        "s": "0x500fab347052d9d72d92b74c028e431abc5a0fa7100a08b6696870c6057217de",
        "r": "0x8ef2ca1914215465a30a9a1615a65b635b9cdcff18289d6880a1e9c1549ad5d9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f78917a41d69568b2a49a22199acebd4165053cc0849f9726a6ddf9f61cd431",
      "signature": {
        "s": "0x023feda38cbf1e5a5fa89e609c8776ad7beb399ee4189041522f6ebb95f1fa82",
        "r": "0xa6cfe4c435eb10485f40d5900f48f911cca4a7d8c6d2f148e1550c6296eeb3ce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62952557825",
    "total": "709903152923620039209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62952557825",
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
            "amount": "27722435552206844479560"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "62952557"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NTBjYzVmMy1kODA5LTUwNDYtOWE4Zi04NTZhNDlmY2E2ZWIifQ==",
    "nonce": 111907,
    "balances": {
      "current": "250139455794785181613319",
      "previous": "250139455794848197123701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa6e45e838379ca2012480dbc87a5fbb4c04dde10",
    "nonce": 46,
    "balances": {
      "current": "1381864152150700160765",
      "previous": "1381864152087747602940"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:56.082Z",
  "updated": "2022-05-04T09:00:56.163Z",
  "id": "627240c87832e20011830da0"
}
```
* *stageAmount*: `1381864152150700160765`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000ea843cd010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000ea843cd010000000000000000000000000000000000000000000000267be2a45b1e2e5a294f4b019f433f82ffdc8294f4e2cf21eccb6d71a26c95e1e1fdf2217e06abb4678ef2ca1914215465a30a9a1615a65b635b9cdcff18289d6880a1e9c1549ad5d9500fab347052d9d72d92b74c028e431abc5a0fa7100a08b6696870c6057217de000000000000000000000000000000000000000000000000000000000000001b3f78917a41d69568b2a49a22199acebd4165053cc0849f9726a6ddf9f61cd431a6cfe4c435eb10485f40d5900f48f911cca4a7d8c6d2f148e1550c6296eeb3ce023feda38cbf1e5a5fa89e609c8776ad7beb399ee4189041522f6ebb95f1fa82000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b523000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034f8164a35b880c5bd070000000000000000000000000000000000000000000034f8164a35c72cca1e7500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000003c0946d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ded613fef93d0248480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e54426a597a566d4d79316b4f4441354c5455774e4459744f5745345a6930344e545a684e446c6d593245325a57496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a6e45e838379ca2012480dbc87a5fbb4c04dde1000000000000000000000000000000000000000000000004ae937acf374d376fd00000000000000000000000000000000000000000000004ae937ace4cc8fa9fc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4f4b019f433f82ffdc8294f4e2cf21eccb6d71a26c95e1e1fdf2217e06abb467",
      "signature": {
        "s": "0x500fab347052d9d72d92b74c028e431abc5a0fa7100a08b6696870c6057217de",
        "r": "0x8ef2ca1914215465a30a9a1615a65b635b9cdcff18289d6880a1e9c1549ad5d9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x3f78917a41d69568b2a49a22199acebd4165053cc0849f9726a6ddf9f61cd431",
      "signature": {
        "s": "0x023feda38cbf1e5a5fa89e609c8776ad7beb399ee4189041522f6ebb95f1fa82",
        "r": "0xa6cfe4c435eb10485f40d5900f48f911cca4a7d8c6d2f148e1550c6296eeb3ce",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "62952557825",
    "total": "709903152923620039209"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "62952557825",
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
            "amount": "27722435552206844479560"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "62952557"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NTBjYzVmMy1kODA5LTUwNDYtOWE4Zi04NTZhNDlmY2E2ZWIifQ==",
    "nonce": 111907,
    "balances": {
      "current": "250139455794785181613319",
      "previous": "250139455794848197123701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa6e45e838379ca2012480dbc87a5fbb4c04dde10",
    "nonce": 46,
    "balances": {
      "current": "1381864152150700160765",
      "previous": "1381864152087747602940"
    }
  },
  "blockNumber": "14709984",
  "created": "2022-05-04T09:00:56.082Z",
  "updated": "2022-05-04T09:00:56.163Z",
  "id": "627240c87832e20011830da0"
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
0x0f200f9b00000000000000000000000000000000000000000000004ae937acf374d376fd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1381864152150700160765`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`