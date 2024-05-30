# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x5BB8bdd0057224700d4183A594E8CD0B9773f7E3`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000013478c112abdba5b9f000000000000000000000000000000000000000000000006958a1397a31684f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000006958a1397a31684f8000000000000000000000000000000000000000000000013478c112abdba5b9fa6ff96ad9a8eb443d30a6bd9265d0b91a97f3790bf05163df59fd3bd10dce519e367da3f4d1ac5f6c30a8dd4bcc14d1969092e440457fbbfcfae74618586a1b027e07a81b751901fa0a2f802127f4263b44897a38f18872eed3ea19cf9dc5fcc000000000000000000000000000000000000000000000000000000000000001bc13dba1fb3567b9e6945f5ae5ef71d26cc6169a315741ca31e5ea841e87293a3ad6f7e7aff4193dfabf4cb0adde580cad73ca18e6c3da8709ad4910a2a28901e65ea13ec11e1ba02aba471d4bdf960bc92256da81947b8e1b56258096d42ae84000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7e8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017639e92a77630ee408c00000000000000000000000000000000000000000000176a35cc3a8fc596f85600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001af7f81f19232d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e666b1764ae31111db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e54637a4e7a55315a433031597a55784c54566d4d4755744f47557a596930344e4745355a6d457a4d3255344f47556966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000005bb8bdd0057224700d4183a594e8cd0b9773f7e3000000000000000000000000000000000000000000000013478c112abdba5b9f00000000000000000000000000000000000000000000000cb201fd931aa3d6a700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa6ff96ad9a8eb443d30a6bd9265d0b91a97f3790bf05163df59fd3bd10dce519",
      "signature": {
        "s": "0x27e07a81b751901fa0a2f802127f4263b44897a38f18872eed3ea19cf9dc5fcc",
        "r": "0xe367da3f4d1ac5f6c30a8dd4bcc14d1969092e440457fbbfcfae74618586a1b0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc13dba1fb3567b9e6945f5ae5ef71d26cc6169a315741ca31e5ea841e87293a3",
      "signature": {
        "s": "0x65ea13ec11e1ba02aba471d4bdf960bc92256da81947b8e1b56258096d42ae84",
        "r": "0xad6f7e7aff4193dfabf4cb0adde580cad73ca18e6c3da8709ad4910a2a28901e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "121455911042691794168",
    "total": "355643651949183261599"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "121455911042691794168",
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
            "amount": "27861983377028178579931"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "121455911042691794"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNTczNzU1ZC01YzUxLTVmMGUtOGUzYi04NGE5ZmEzM2U4OGUifQ==",
    "nonce": 112616,
    "balances": {
      "current": "110452083148629746794636",
      "previous": "110573660515583481280598"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bb8bdd0057224700d4183a594e8cd0b9773f7e3",
    "nonce": 5,
    "balances": {
      "current": "355643651949183261599",
      "previous": "234187740906491467431"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:49.078Z",
  "updated": "2022-05-04T09:04:49.138Z",
  "id": "627241b1bbd75600116d0828"
}
```
* *stageAmount*: `355643651949183261599`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000006958a1397a31684f80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000006958a1397a31684f8000000000000000000000000000000000000000000000013478c112abdba5b9fa6ff96ad9a8eb443d30a6bd9265d0b91a97f3790bf05163df59fd3bd10dce519e367da3f4d1ac5f6c30a8dd4bcc14d1969092e440457fbbfcfae74618586a1b027e07a81b751901fa0a2f802127f4263b44897a38f18872eed3ea19cf9dc5fcc000000000000000000000000000000000000000000000000000000000000001bc13dba1fb3567b9e6945f5ae5ef71d26cc6169a315741ca31e5ea841e87293a3ad6f7e7aff4193dfabf4cb0adde580cad73ca18e6c3da8709ad4910a2a28901e65ea13ec11e1ba02aba471d4bdf960bc92256da81947b8e1b56258096d42ae84000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7e8000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017639e92a77630ee408c00000000000000000000000000000000000000000000176a35cc3a8fc596f85600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001af7f81f19232d20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e666b1764ae31111db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e54637a4e7a55315a433031597a55784c54566d4d4755744f47557a596930344e4745355a6d457a4d3255344f47556966513d3d00000000000000000000000000000000000000000000000000000000000000050000000000000000000000005bb8bdd0057224700d4183a594e8cd0b9773f7e3000000000000000000000000000000000000000000000013478c112abdba5b9f00000000000000000000000000000000000000000000000cb201fd931aa3d6a700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa6ff96ad9a8eb443d30a6bd9265d0b91a97f3790bf05163df59fd3bd10dce519",
      "signature": {
        "s": "0x27e07a81b751901fa0a2f802127f4263b44897a38f18872eed3ea19cf9dc5fcc",
        "r": "0xe367da3f4d1ac5f6c30a8dd4bcc14d1969092e440457fbbfcfae74618586a1b0",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xc13dba1fb3567b9e6945f5ae5ef71d26cc6169a315741ca31e5ea841e87293a3",
      "signature": {
        "s": "0x65ea13ec11e1ba02aba471d4bdf960bc92256da81947b8e1b56258096d42ae84",
        "r": "0xad6f7e7aff4193dfabf4cb0adde580cad73ca18e6c3da8709ad4910a2a28901e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "121455911042691794168",
    "total": "355643651949183261599"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "121455911042691794168",
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
            "amount": "27861983377028178579931"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "121455911042691794"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNTczNzU1ZC01YzUxLTVmMGUtOGUzYi04NGE5ZmEzM2U4OGUifQ==",
    "nonce": 112616,
    "balances": {
      "current": "110452083148629746794636",
      "previous": "110573660515583481280598"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x5bb8bdd0057224700d4183a594e8cd0b9773f7e3",
    "nonce": 5,
    "balances": {
      "current": "355643651949183261599",
      "previous": "234187740906491467431"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:49.078Z",
  "updated": "2022-05-04T09:04:49.138Z",
  "id": "627241b1bbd75600116d0828"
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
0x0f200f9b000000000000000000000000000000000000000000000013478c112abdba5b9f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `355643651949183261599`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`