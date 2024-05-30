# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xfa4E571a25B6FB0e066E2e9b6ADE8B46342187bc`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000024471611c72795af25000000000000000000000000000000000000000000000000dc2fb26d57f38f330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f38f3300000000000000000000000000000000000000000000001822a462160814ce9e53f6e9632dfa6bf9a94ce5f44af0edff749dfe965766dbf6b14dc1c48964b418f3d5cb5a9b99152f3c12674b7013df5e2aa87200b475f0cff048e47067c4ce8d6cbf259323ec319f853ce08302101bcf432eb693ebe02ae424725bb9d950fbfc000000000000000000000000000000000000000000000000000000000000001c2901b27006c64747e4e0baaba6ead4e85c68526081030862332bb70a3c409430cf0fe582a25440cff4fe9ae41d0ad19ba7311b15a0e02850d165baf2cdbca0a02a4e5bb6df88eb5fe2749bdce9b25a87eb980a755f651c2b824c88d13b7ada81000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b682000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a9a92bb6acf72a95440000000000000000000000000000000000000000000030aa8593c73bb2ca297800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac05010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff0046d120e99d5d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a475a684d546b344e433032596a4d344c5455314d5759744f4441304e533077597a67325a6a6b354f4446684d54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000fa4e571a25b6fb0e066e2e9b6ade8b46342187bc000000000000000000000000000000000000000000000024471611c72795af250000000000000000000000000000000000000000000000236ae65f59cfa21ff200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x53f6e9632dfa6bf9a94ce5f44af0edff749dfe965766dbf6b14dc1c48964b418",
      "signature": {
        "s": "0x6cbf259323ec319f853ce08302101bcf432eb693ebe02ae424725bb9d950fbfc",
        "r": "0xf3d5cb5a9b99152f3c12674b7013df5e2aa87200b475f0cff048e47067c4ce8d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2901b27006c64747e4e0baaba6ead4e85c68526081030862332bb70a3c409430",
      "signature": {
        "s": "0x2a4e5bb6df88eb5fe2749bdce9b25a87eb980a755f651c2b824c88d13b7ada81",
        "r": "0xcf0fe582a25440cff4fe9ae41d0ad19ba7311b15a0e02850d165baf2cdbca0a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946305843",
    "total": "445218085709263720094"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946305843",
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
            "amount": "27742751411178787427799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946305"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZGZhMTk4NC02YjM4LTU1MWYtODA0NS0wYzg2Zjk5ODFhMTgifQ==",
    "nonce": 112258,
    "balances": {
      "current": "229803280963870290253124",
      "previous": "229819162926161431505272"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa4e571a25b6fb0e066e2e9b6ade8b46342187bc",
    "nonce": 46,
    "balances": {
      "current": "669205087826784661285",
      "previous": "653338991631838355442"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:49.625Z",
  "updated": "2022-05-04T09:02:49.705Z",
  "id": "627241397832e20011830e14"
}
```
* *stageAmount*: `669205087826784661285`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f38f330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f38f3300000000000000000000000000000000000000000000001822a462160814ce9e53f6e9632dfa6bf9a94ce5f44af0edff749dfe965766dbf6b14dc1c48964b418f3d5cb5a9b99152f3c12674b7013df5e2aa87200b475f0cff048e47067c4ce8d6cbf259323ec319f853ce08302101bcf432eb693ebe02ae424725bb9d950fbfc000000000000000000000000000000000000000000000000000000000000001c2901b27006c64747e4e0baaba6ead4e85c68526081030862332bb70a3c409430cf0fe582a25440cff4fe9ae41d0ad19ba7311b15a0e02850d165baf2cdbca0a02a4e5bb6df88eb5fe2749bdce9b25a87eb980a755f651c2b824c88d13b7ada81000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b682000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030a9a92bb6acf72a95440000000000000000000000000000000000000000000030aa8593c73bb2ca297800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac05010000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dff0046d120e99d5d70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a475a684d546b344e433032596a4d344c5455314d5759744f4441304e533077597a67325a6a6b354f4446684d54676966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000fa4e571a25b6fb0e066e2e9b6ade8b46342187bc000000000000000000000000000000000000000000000024471611c72795af250000000000000000000000000000000000000000000000236ae65f59cfa21ff200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x53f6e9632dfa6bf9a94ce5f44af0edff749dfe965766dbf6b14dc1c48964b418",
      "signature": {
        "s": "0x6cbf259323ec319f853ce08302101bcf432eb693ebe02ae424725bb9d950fbfc",
        "r": "0xf3d5cb5a9b99152f3c12674b7013df5e2aa87200b475f0cff048e47067c4ce8d",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2901b27006c64747e4e0baaba6ead4e85c68526081030862332bb70a3c409430",
      "signature": {
        "s": "0x2a4e5bb6df88eb5fe2749bdce9b25a87eb980a755f651c2b824c88d13b7ada81",
        "r": "0xcf0fe582a25440cff4fe9ae41d0ad19ba7311b15a0e02850d165baf2cdbca0a0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946305843",
    "total": "445218085709263720094"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946305843",
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
            "amount": "27742751411178787427799"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946305"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZGZhMTk4NC02YjM4LTU1MWYtODA0NS0wYzg2Zjk5ODFhMTgifQ==",
    "nonce": 112258,
    "balances": {
      "current": "229803280963870290253124",
      "previous": "229819162926161431505272"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xfa4e571a25b6fb0e066e2e9b6ade8b46342187bc",
    "nonce": 46,
    "balances": {
      "current": "669205087826784661285",
      "previous": "653338991631838355442"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:49.625Z",
  "updated": "2022-05-04T09:02:49.705Z",
  "id": "627241397832e20011830e14"
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
0x0f200f9b000000000000000000000000000000000000000000000024471611c72795af250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205087826784661285`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`