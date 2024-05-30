# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xA2a4571835Fca8e11068D3665fef851173896f59`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000794090290ebbb20000000000000000000000000000000000000000000000000002dfefc86949210000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000002dfefc86949210000000000000000000000000000000000000000000000000050ab1916290d4dced013b4b65ec11c6dd1af09f7e12454c874a0329809fad1f164445c4ea46f261ec7386a49f0ab44d903e1a60a097d2ce62c8d92acb60bb280a84f119b978f9c639984cc9380acd1d3926abd6aa74a5c8d757f1e3c12c4ab8d95a75899481d61000000000000000000000000000000000000000000000000000000000000001b7ea8d55a811c855f92b8a3885c80d894b237722cfa51f961dcc01cb5497ecdcee2801fb80b764c6cfec1c2d44e5ac001dbea73665debcb4f641d699f40e07d4d09a0891caac454a96ff01af3e2c8cc4e89314e009711eadcd4cfecdd1a56145f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae3e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000962f7c7d5ad39ac8a27500000000000000000000000000000000000000000000962f7c803b7fc98a16ec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000bc66582b560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f944cac3c2bcbb150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e7a6c6b5a4455315a6930795a546b784c5455795932457459575a6d597930345a54597a4e6a45325a6a67795a6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000a2a4571835fca8e11068d3665fef851173896f5900000000000000000000000000000000000000000000000000794090290ebbb2000000000000000000000000000000000000000000000000007660a060a5729100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xced013b4b65ec11c6dd1af09f7e12454c874a0329809fad1f164445c4ea46f26",
      "signature": {
        "s": "0x639984cc9380acd1d3926abd6aa74a5c8d757f1e3c12c4ab8d95a75899481d61",
        "r": "0x1ec7386a49f0ab44d903e1a60a097d2ce62c8d92acb60bb280a84f119b978f9c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7ea8d55a811c855f92b8a3885c80d894b237722cfa51f961dcc01cb5497ecdce",
      "signature": {
        "s": "0x09a0891caac454a96ff01af3e2c8cc4e89314e009711eadcd4cfecdd1a56145f",
        "r": "0xe2801fb80b764c6cfec1c2d44e5ac001dbea73665debcb4f641d699f40e07d4d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "809170905942305",
    "total": "22706122371173709"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "809170905942305",
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
            "amount": "27263802701025002699541"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "809170905942"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNzlkZDU1Zi0yZTkxLTUyY2EtYWZmYy04ZTYzNjE2ZjgyZmMifQ==",
    "nonce": 110142,
    "balances": {
      "current": "709230939827808804315765",
      "previous": "709230940637788881164012"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa2a4571835fca8e11068d3665fef851173896f59",
    "nonce": 45,
    "balances": {
      "current": "34129460090289074",
      "previous": "33320289184346769"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:45.429Z",
  "updated": "2022-05-04T08:51:45.522Z",
  "id": "62723ea13592fd001130b47d"
}
```
* *stageAmount*: `34129460090289074`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000002dfefc86949210000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000002dfefc86949210000000000000000000000000000000000000000000000000050ab1916290d4dced013b4b65ec11c6dd1af09f7e12454c874a0329809fad1f164445c4ea46f261ec7386a49f0ab44d903e1a60a097d2ce62c8d92acb60bb280a84f119b978f9c639984cc9380acd1d3926abd6aa74a5c8d757f1e3c12c4ab8d95a75899481d61000000000000000000000000000000000000000000000000000000000000001b7ea8d55a811c855f92b8a3885c80d894b237722cfa51f961dcc01cb5497ecdcee2801fb80b764c6cfec1c2d44e5ac001dbea73665debcb4f641d699f40e07d4d09a0891caac454a96ff01af3e2c8cc4e89314e009711eadcd4cfecdd1a56145f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae3e000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000962f7c7d5ad39ac8a27500000000000000000000000000000000000000000000962f7c803b7fc98a16ec00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000bc66582b560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f944cac3c2bcbb150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e7a6c6b5a4455315a6930795a546b784c5455795932457459575a6d597930345a54597a4e6a45325a6a67795a6d4d6966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000a2a4571835fca8e11068d3665fef851173896f5900000000000000000000000000000000000000000000000000794090290ebbb2000000000000000000000000000000000000000000000000007660a060a5729100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xced013b4b65ec11c6dd1af09f7e12454c874a0329809fad1f164445c4ea46f26",
      "signature": {
        "s": "0x639984cc9380acd1d3926abd6aa74a5c8d757f1e3c12c4ab8d95a75899481d61",
        "r": "0x1ec7386a49f0ab44d903e1a60a097d2ce62c8d92acb60bb280a84f119b978f9c",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7ea8d55a811c855f92b8a3885c80d894b237722cfa51f961dcc01cb5497ecdce",
      "signature": {
        "s": "0x09a0891caac454a96ff01af3e2c8cc4e89314e009711eadcd4cfecdd1a56145f",
        "r": "0xe2801fb80b764c6cfec1c2d44e5ac001dbea73665debcb4f641d699f40e07d4d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "809170905942305",
    "total": "22706122371173709"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "809170905942305",
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
            "amount": "27263802701025002699541"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "809170905942"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNzlkZDU1Zi0yZTkxLTUyY2EtYWZmYy04ZTYzNjE2ZjgyZmMifQ==",
    "nonce": 110142,
    "balances": {
      "current": "709230939827808804315765",
      "previous": "709230940637788881164012"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa2a4571835fca8e11068d3665fef851173896f59",
    "nonce": 45,
    "balances": {
      "current": "34129460090289074",
      "previous": "33320289184346769"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:45.429Z",
  "updated": "2022-05-04T08:51:45.522Z",
  "id": "62723ea13592fd001130b47d"
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
0x0f200f9b00000000000000000000000000000000000000000000000000794090290ebbb20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `34129460090289074`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`