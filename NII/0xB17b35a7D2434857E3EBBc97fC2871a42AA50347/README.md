# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB17b35a7D2434857E3EBBc97fC2871a42AA50347`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000049d92780486c3d5990000000000000000000000000000000000000000000000005c7a6ec578e5b1790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005c7a6ec578e5b1790000000000000000000000000000000000000000000000049d92780486c3d5991fe433c6d416c2a981e63e966cd988ac368f23ab5fc1f090dc729d177811fbae79e70078bd9150cd9cca73083d1a9f83d11e6aca79abed06ab511811aa507d711efe047576939a1509a900b177a3c6849157247f8293b8f511ed1cec56fab8b8000000000000000000000000000000000000000000000000000000000000001c27585e8896d3d552f38bd9661d2c72b0606ac1498ce16a6a159daeb881718e71809ee98d81642ea9783de0a38080fdee30fc26b81582737679d07528d9617c3b284d1c0a4bc32c6531eb58d0598e4705060cf1f5fced4bf59265a002d4f2e508000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b561000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000343b410b80d72054710100000000000000000000000000000000000000000000343b9d9d9c443852f0bb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017aca79f18ce410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df065efde02510b77c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a597a63784d6a51784e5330304e6d566a4c5455315a5463744f446b774e7930304e44686c5a474935596a5268597a416966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000b17b35a7d2434857e3ebbc97fc2871a42aa503470000000000000000000000000000000000000000000000049d92780486c3d5990000000000000000000000000000000000000000000000044118093f0dde242000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fe433c6d416c2a981e63e966cd988ac368f23ab5fc1f090dc729d177811fbae",
      "signature": {
        "s": "0x1efe047576939a1509a900b177a3c6849157247f8293b8f511ed1cec56fab8b8",
        "r": "0x79e70078bd9150cd9cca73083d1a9f83d11e6aca79abed06ab511811aa507d71",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27585e8896d3d552f38bd9661d2c72b0606ac1498ce16a6a159daeb881718e71",
      "signature": {
        "s": "0x284d1c0a4bc32c6531eb58d0598e4705060cf1f5fced4bf59265a002d4f2e508",
        "r": "0x809ee98d81642ea9783de0a38080fdee30fc26b81582737679d07528d9617c3b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6663760393064001913",
    "total": "85141245866228831641"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6663760393064001913",
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
            "amount": "27725915426136630802300"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6663760393064001"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYzcxMjQxNS00NmVjLTU1ZTctODkwNy00NDhlZGI5YjRhYzAifQ==",
    "nonce": 111969,
    "balances": {
      "current": "246656101991069072519425",
      "previous": "246662772415222529585339"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb17b35a7d2434857e3ebbc97fc2871a42aa50347",
    "nonce": 13,
    "balances": {
      "current": "85141245866228831641",
      "previous": "78477485473164829728"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:18.793Z",
  "updated": "2022-05-04T09:01:18.874Z",
  "id": "627240debbd75600116d0750"
}
```
* *stageAmount*: `85141245866228831641`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005c7a6ec578e5b1790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005c7a6ec578e5b1790000000000000000000000000000000000000000000000049d92780486c3d5991fe433c6d416c2a981e63e966cd988ac368f23ab5fc1f090dc729d177811fbae79e70078bd9150cd9cca73083d1a9f83d11e6aca79abed06ab511811aa507d711efe047576939a1509a900b177a3c6849157247f8293b8f511ed1cec56fab8b8000000000000000000000000000000000000000000000000000000000000001c27585e8896d3d552f38bd9661d2c72b0606ac1498ce16a6a159daeb881718e71809ee98d81642ea9783de0a38080fdee30fc26b81582737679d07528d9617c3b284d1c0a4bc32c6531eb58d0598e4705060cf1f5fced4bf59265a002d4f2e508000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b561000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000343b410b80d72054710100000000000000000000000000000000000000000000343b9d9d9c443852f0bb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017aca79f18ce410000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df065efde02510b77c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a597a63784d6a51784e5330304e6d566a4c5455315a5463744f446b774e7930304e44686c5a474935596a5268597a416966513d3d000000000000000000000000000000000000000000000000000000000000000d000000000000000000000000b17b35a7d2434857e3ebbc97fc2871a42aa503470000000000000000000000000000000000000000000000049d92780486c3d5990000000000000000000000000000000000000000000000044118093f0dde242000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1fe433c6d416c2a981e63e966cd988ac368f23ab5fc1f090dc729d177811fbae",
      "signature": {
        "s": "0x1efe047576939a1509a900b177a3c6849157247f8293b8f511ed1cec56fab8b8",
        "r": "0x79e70078bd9150cd9cca73083d1a9f83d11e6aca79abed06ab511811aa507d71",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x27585e8896d3d552f38bd9661d2c72b0606ac1498ce16a6a159daeb881718e71",
      "signature": {
        "s": "0x284d1c0a4bc32c6531eb58d0598e4705060cf1f5fced4bf59265a002d4f2e508",
        "r": "0x809ee98d81642ea9783de0a38080fdee30fc26b81582737679d07528d9617c3b",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "6663760393064001913",
    "total": "85141245866228831641"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6663760393064001913",
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
            "amount": "27725915426136630802300"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6663760393064001"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYzcxMjQxNS00NmVjLTU1ZTctODkwNy00NDhlZGI5YjRhYzAifQ==",
    "nonce": 111969,
    "balances": {
      "current": "246656101991069072519425",
      "previous": "246662772415222529585339"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb17b35a7d2434857e3ebbc97fc2871a42aa50347",
    "nonce": 13,
    "balances": {
      "current": "85141245866228831641",
      "previous": "78477485473164829728"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:18.793Z",
  "updated": "2022-05-04T09:01:18.874Z",
  "id": "627240debbd75600116d0750"
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
0x0f200f9b0000000000000000000000000000000000000000000000049d92780486c3d5990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `85141245866228831641`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`