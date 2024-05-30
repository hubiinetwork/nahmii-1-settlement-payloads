# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xcde7cc28967DFA6ce057624DD71451e8bEAC76B3`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000b756363b1590e06870000000000000000000000000000000000000000000000000000000266be46f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000266be46f50000000000000000000000000000000000000000000000057db89f595aa58916d25d12dfd5f48f568302b9ae7f7bb0281a7579416e1c92769c389970ad20207f910377dfb7f603d0b46030e6944a9f4e767ee42ebd7c681ce549262eb2a575c53d728fa2f2eee84ce658f92ae71306c1614de14d6ce1025eefb796a356a659ec000000000000000000000000000000000000000000000000000000000000001c55bdb4cbcbf3f29af98d34ad2c6e0812c758557d977e93fb2fc000148e74faec07e50e31976f2da1496d395b7e75fe9c8f8b32b03a770571b94ce774fc795cfb1d7e4e2da529b3353c7d11964c94738b2ede46f65ed0cd4e8483a31db5a1a974000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abbd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1af20c0eece0cfbcf6000000000000000000000000000000000000000000009c1af20c0eef482b63bb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000009d5fd00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475b2e01139d817e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a646d5a5751324e533032597a417a4c5455794d5745744f5751784e5330324e4455784f4749354f4455354e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cde7cc28967dfa6ce057624dd71451e8beac76b300000000000000000000000000000000000000000000000b756363b1590e068700000000000000000000000000000000000000000000000b756363aef24fbf9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd25d12dfd5f48f568302b9ae7f7bb0281a7579416e1c92769c389970ad20207f",
      "signature": {
        "s": "0x3d728fa2f2eee84ce658f92ae71306c1614de14d6ce1025eefb796a356a659ec",
        "r": "0x910377dfb7f603d0b46030e6944a9f4e767ee42ebd7c681ce549262eb2a575c5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x55bdb4cbcbf3f29af98d34ad2c6e0812c758557d977e93fb2fc000148e74faec",
      "signature": {
        "s": "0x1d7e4e2da529b3353c7d11964c94738b2ede46f65ed0cd4e8483a31db5a1a974",
        "r": "0x07e50e31976f2da1496d395b7e75fe9c8f8b32b03a770571b94ce774fc795cfb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10313680629",
    "total": "101292886225125214486"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10313680629",
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
            "amount": "27235875340208179779561"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10313680"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzdmZWQ2NS02YzAzLTUyMWEtOWQxNS02NDUxOGI5ODU5NmMifQ==",
    "nonce": 109501,
    "balances": {
      "current": "737186228005448547548406",
      "previous": "737186228005458871542715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcde7cc28967dfa6ce057624dd71451e8beac76b3",
    "nonce": 46,
    "balances": {
      "current": "211372898949291443847",
      "previous": "211372898938977763218"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:26.427Z",
  "updated": "2022-05-04T08:48:26.524Z",
  "id": "62723dda3592fd001130b3ab"
}
```
* *stageAmount*: `211372898949291443847`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000266be46f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000266be46f50000000000000000000000000000000000000000000000057db89f595aa58916d25d12dfd5f48f568302b9ae7f7bb0281a7579416e1c92769c389970ad20207f910377dfb7f603d0b46030e6944a9f4e767ee42ebd7c681ce549262eb2a575c53d728fa2f2eee84ce658f92ae71306c1614de14d6ce1025eefb796a356a659ec000000000000000000000000000000000000000000000000000000000000001c55bdb4cbcbf3f29af98d34ad2c6e0812c758557d977e93fb2fc000148e74faec07e50e31976f2da1496d395b7e75fe9c8f8b32b03a770571b94ce774fc795cfb1d7e4e2da529b3353c7d11964c94738b2ede46f65ed0cd4e8483a31db5a1a974000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074b60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001abbd000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009c1af20c0eece0cfbcf6000000000000000000000000000000000000000000009c1af20c0eef482b63bb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000009d5fd00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c475b2e01139d817e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e7a646d5a5751324e533032597a417a4c5455794d5745744f5751784e5330324e4455784f4749354f4455354e6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cde7cc28967dfa6ce057624dd71451e8beac76b300000000000000000000000000000000000000000000000b756363b1590e068700000000000000000000000000000000000000000000000b756363aef24fbf9200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xd25d12dfd5f48f568302b9ae7f7bb0281a7579416e1c92769c389970ad20207f",
      "signature": {
        "s": "0x3d728fa2f2eee84ce658f92ae71306c1614de14d6ce1025eefb796a356a659ec",
        "r": "0x910377dfb7f603d0b46030e6944a9f4e767ee42ebd7c681ce549262eb2a575c5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x55bdb4cbcbf3f29af98d34ad2c6e0812c758557d977e93fb2fc000148e74faec",
      "signature": {
        "s": "0x1d7e4e2da529b3353c7d11964c94738b2ede46f65ed0cd4e8483a31db5a1a974",
        "r": "0x07e50e31976f2da1496d395b7e75fe9c8f8b32b03a770571b94ce774fc795cfb",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10313680629",
    "total": "101292886225125214486"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10313680629",
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
            "amount": "27235875340208179779561"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10313680"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNzdmZWQ2NS02YzAzLTUyMWEtOWQxNS02NDUxOGI5ODU5NmMifQ==",
    "nonce": 109501,
    "balances": {
      "current": "737186228005448547548406",
      "previous": "737186228005458871542715"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcde7cc28967dfa6ce057624dd71451e8beac76b3",
    "nonce": 46,
    "balances": {
      "current": "211372898949291443847",
      "previous": "211372898938977763218"
    }
  },
  "blockNumber": "14709942",
  "created": "2022-05-04T08:48:26.427Z",
  "updated": "2022-05-04T08:48:26.524Z",
  "id": "62723dda3592fd001130b3ab"
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
0x0f200f9b00000000000000000000000000000000000000000000000b756363b1590e06870000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `211372898949291443847`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`