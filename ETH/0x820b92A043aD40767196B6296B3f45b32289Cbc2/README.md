# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x820b92A043aD40767196B6296B3f45b32289Cbc2`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000249e3af916a96140b98ba2639e1a7876ce3abd83365aa1a5a75f44a5aa5e9d6710f5ca22b6205b375560df99021fb16fdbe3cd79fb4577a143aa48008e069bd955603bb9292c896ab4d621ddc1b7cb26917a86f840d330d365591eee1f7ecc23f1000000000000000000000000000000000000000000000000000000000000001c4477c43bff7d64909a98173034953b12110f4730bded1e69efd5a3e8e10d3fb66a84f09e0f691a03c1029e0b869ca509f2659a24742aff43fdb33efd68774b6f1042f51b1a6ba730ac9d5bc0e143b7755da07a0563500943de0629672d67a7cc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b0917000000000000000000000000000000000000000000000000002386f2bc8b093c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20c800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d546c6c5a6a49334e69307a4f44426b4c5455354d6d45744f544a6b4f43316d5a5451794e57566c597a6b774e7a416966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000820b92a043ad40767196b6296b3f45b32289cbc20000000000000000000000000000000000000000000000000000000000000024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9e3af916a96140b98ba2639e1a7876ce3abd83365aa1a5a75f44a5aa5e9d6710",
      "signature": {
        "s": "0x603bb9292c896ab4d621ddc1b7cb26917a86f840d330d365591eee1f7ecc23f1",
        "r": "0xf5ca22b6205b375560df99021fb16fdbe3cd79fb4577a143aa48008e069bd955",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4477c43bff7d64909a98173034953b12110f4730bded1e69efd5a3e8e10d3fb6",
      "signature": {
        "s": "0x1042f51b1a6ba730ac9d5bc0e143b7755da07a0563500943de0629672d67a7cc",
        "r": "0x6a84f09e0f691a03c1029e0b869ca509f2659a24742aff43fdb33efd68774b6f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36",
    "total": "36"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36",
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
            "amount": "794824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMTllZjI3Ni0zODBkLTU5MmEtOTJkOC1mZTQyNWVlYzkwNzAifQ==",
    "nonce": 2169,
    "balances": {
      "current": "10000001288309015",
      "previous": "10000001288309052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x820b92a043ad40767196b6296b3f45b32289cbc2",
    "nonce": 19,
    "balances": {
      "current": "36",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:47.682Z",
  "updated": "2020-05-22T08:14:47.781Z",
  "id": "5ec789f7b0c6090011d5aba5"
}
```
* *stageAmount*: `36`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000002400000000000000000000000000000000000000000000000000000000000000249e3af916a96140b98ba2639e1a7876ce3abd83365aa1a5a75f44a5aa5e9d6710f5ca22b6205b375560df99021fb16fdbe3cd79fb4577a143aa48008e069bd955603bb9292c896ab4d621ddc1b7cb26917a86f840d330d365591eee1f7ecc23f1000000000000000000000000000000000000000000000000000000000000001c4477c43bff7d64909a98173034953b12110f4730bded1e69efd5a3e8e10d3fb66a84f09e0f691a03c1029e0b869ca509f2659a24742aff43fdb33efd68774b6f1042f51b1a6ba730ac9d5bc0e143b7755da07a0563500943de0629672d67a7cc000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000087900000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc8b0917000000000000000000000000000000000000000000000000002386f2bc8b093c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c20c800000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4d546c6c5a6a49334e69307a4f44426b4c5455354d6d45744f544a6b4f43316d5a5451794e57566c597a6b774e7a416966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000820b92a043ad40767196b6296b3f45b32289cbc20000000000000000000000000000000000000000000000000000000000000024000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9e3af916a96140b98ba2639e1a7876ce3abd83365aa1a5a75f44a5aa5e9d6710",
      "signature": {
        "s": "0x603bb9292c896ab4d621ddc1b7cb26917a86f840d330d365591eee1f7ecc23f1",
        "r": "0xf5ca22b6205b375560df99021fb16fdbe3cd79fb4577a143aa48008e069bd955",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x4477c43bff7d64909a98173034953b12110f4730bded1e69efd5a3e8e10d3fb6",
      "signature": {
        "s": "0x1042f51b1a6ba730ac9d5bc0e143b7755da07a0563500943de0629672d67a7cc",
        "r": "0x6a84f09e0f691a03c1029e0b869ca509f2659a24742aff43fdb33efd68774b6f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "36",
    "total": "36"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "36",
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
            "amount": "794824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "1"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiJjMTllZjI3Ni0zODBkLTU5MmEtOTJkOC1mZTQyNWVlYzkwNzAifQ==",
    "nonce": 2169,
    "balances": {
      "current": "10000001288309015",
      "previous": "10000001288309052"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x820b92a043ad40767196b6296b3f45b32289cbc2",
    "nonce": 19,
    "balances": {
      "current": "36",
      "previous": "0"
    }
  },
  "blockNumber": "10114546",
  "created": "2020-05-22T08:14:47.682Z",
  "updated": "2020-05-22T08:14:47.781Z",
  "id": "5ec789f7b0c6090011d5aba5"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000000240000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``