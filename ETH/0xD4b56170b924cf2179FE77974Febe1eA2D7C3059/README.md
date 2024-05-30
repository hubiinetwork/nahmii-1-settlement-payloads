# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD4b56170b924cf2179FE77974Febe1eA2D7C3059`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000096350000000000000000000000000000000000000000000000000000000000009635000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000096350000000000000000000000000000000000000000000000000000000000009635860912b490ade489c2b57131a076621d0049881fbcd02d0a6bfdb06d3323a83b63efb6c9343dd9f6ddffac8b75431f2fe049adcdec9aec1e4cb7aaa05500cf403f647a1693c3ec6c5627bf3475df1c7f2496a7b8c189f4cfd8c5f00bf68e54fa000000000000000000000000000000000000000000000000000000000000001c83a1788215571e86dbbfcf9dd67e9eeaff7f21bf311201307210869f0027b760667604c515b354f863f574bec278824875f4360baa01a2e80bfafa47982463300221f1a3e2bc23442b61087ba093940fc8976c57da823bd438b6a17e03b2bec5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000062700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c616f55f000000000000000000000000000000000000000000000000002386f2c6178bba00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b09600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68597a41774e54526a4d43316c4e44466b4c545532597a49744f544d354e5330334d7a5a6c5a54526b4d57526a597a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d4b56170b924cf2179fe77974febe1ea2d7c30590000000000000000000000000000000000000000000000000000000000009635000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x860912b490ade489c2b57131a076621d0049881fbcd02d0a6bfdb06d3323a83b",
      "signature": {
        "s": "0x3f647a1693c3ec6c5627bf3475df1c7f2496a7b8c189f4cfd8c5f00bf68e54fa",
        "r": "0x63efb6c9343dd9f6ddffac8b75431f2fe049adcdec9aec1e4cb7aaa05500cf40",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x83a1788215571e86dbbfcf9dd67e9eeaff7f21bf311201307210869f0027b760",
      "signature": {
        "s": "0x0221f1a3e2bc23442b61087ba093940fc8976c57da823bd438b6a17e03b2bec5",
        "r": "0x667604c515b354f863f574bec278824875f4360baa01a2e80bfafa4798246330",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38453",
    "total": "38453"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38453",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "635030"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "38"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYzAwNTRjMC1lNDFkLTU2YzItOTM5NS03MzZlZTRkMWRjYzIifQ==",
    "nonce": 1575,
    "balances": {
      "current": "10000001448473951",
      "previous": "10000001448512442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd4b56170b924cf2179fe77974febe1ea2d7c3059",
    "nonce": 20,
    "balances": {
      "current": "38453",
      "previous": "0"
    }
  },
  "blockNumber": "10114534",
  "created": "2020-05-22T08:10:38.894Z",
  "updated": "2020-05-22T08:10:38.984Z",
  "id": "5ec788fee5756b00111b8165"
}
```
* *stageAmount*: `38453`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000009635000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000096350000000000000000000000000000000000000000000000000000000000009635860912b490ade489c2b57131a076621d0049881fbcd02d0a6bfdb06d3323a83b63efb6c9343dd9f6ddffac8b75431f2fe049adcdec9aec1e4cb7aaa05500cf403f647a1693c3ec6c5627bf3475df1c7f2496a7b8c189f4cfd8c5f00bf68e54fa000000000000000000000000000000000000000000000000000000000000001c83a1788215571e86dbbfcf9dd67e9eeaff7f21bf311201307210869f0027b760667604c515b354f863f574bec278824875f4360baa01a2e80bfafa47982463300221f1a3e2bc23442b61087ba093940fc8976c57da823bd438b6a17e03b2bec5000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000062700000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2c616f55f000000000000000000000000000000000000000000000000002386f2c6178bba00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000002600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000009b09600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68597a41774e54526a4d43316c4e44466b4c545532597a49744f544d354e5330334d7a5a6c5a54526b4d57526a597a496966513d3d0000000000000000000000000000000000000000000000000000000000000014000000000000000000000000d4b56170b924cf2179fe77974febe1ea2d7c30590000000000000000000000000000000000000000000000000000000000009635000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x860912b490ade489c2b57131a076621d0049881fbcd02d0a6bfdb06d3323a83b",
      "signature": {
        "s": "0x3f647a1693c3ec6c5627bf3475df1c7f2496a7b8c189f4cfd8c5f00bf68e54fa",
        "r": "0x63efb6c9343dd9f6ddffac8b75431f2fe049adcdec9aec1e4cb7aaa05500cf40",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x83a1788215571e86dbbfcf9dd67e9eeaff7f21bf311201307210869f0027b760",
      "signature": {
        "s": "0x0221f1a3e2bc23442b61087ba093940fc8976c57da823bd438b6a17e03b2bec5",
        "r": "0x667604c515b354f863f574bec278824875f4360baa01a2e80bfafa4798246330",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "38453",
    "total": "38453"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "38453",
  "currency": {
    "ct": "0x0000000000000000000000000000000000000000",
    "id": "0"
  },
  "sender": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x0000000000000000000000000000000000000000",
              "id": "0"
            },
            "amount": "635030"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "38"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJhYzAwNTRjMC1lNDFkLTU2YzItOTM5NS03MzZlZTRkMWRjYzIifQ==",
    "nonce": 1575,
    "balances": {
      "current": "10000001448473951",
      "previous": "10000001448512442"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd4b56170b924cf2179fe77974febe1ea2d7c3059",
    "nonce": 20,
    "balances": {
      "current": "38453",
      "previous": "0"
    }
  },
  "blockNumber": "10114534",
  "created": "2020-05-22T08:10:38.894Z",
  "updated": "2020-05-22T08:10:38.984Z",
  "id": "5ec788fee5756b00111b8165"
}
```
* *standard*: ``
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000000000000000000096350000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `38453`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``