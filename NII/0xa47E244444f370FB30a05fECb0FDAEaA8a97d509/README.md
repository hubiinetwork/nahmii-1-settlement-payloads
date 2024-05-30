# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa47E244444f370FB30a05fECb0FDAEaA8a97d509`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000006e772d9899380615000000000000000000000000000000000000000000000000029e77a3268d5271e30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000029e77a3268d5271e30000000000000000000000000000000000000000000000497df71b4fe94aa415e9c6594c683af7c83ed961abb993123a46d0b98a0fa8db5b7b276301ded642c62dcc57551e317b1df40289e77c920a7b0b12c5b6ab10c7c6f9b25760b26259253aec9ec46b9ac11982a96157d2fc2e76eb089763e63e9ad8f9773af30174c167000000000000000000000000000000000000000000000000000000000000001b6ac64ed0399427055b556ae2cdd3213f363322c15b4161bca847a026e522e93653717ddae5f4302d2a8a7fb43de5a40ad0d431d465236978593f9fcc9d99643f2f5aaaa61728de8d11f90554d8b36361fdf02d67fdaffa6535cc8d97cf0c5c74000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad2a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096df0efdb897f585ec260000000000000000000000000000000000000000000096e1ae20ff7dc81b440900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000aba3bf4542e6000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cc5dfb84a6c53d3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a457959544e6b5a43316a596a5a6c4c5455344d6a4d7459546b304d5330324e6a4e6d5a47453559544a6d4e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a47e244444f370fb30a05fecb0fdaeaa8a97d50900000000000000000000000000000000000000000000006e772d98993806150000000000000000000000000000000000000000000000006bd8b5f572aab3a31d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe9c6594c683af7c83ed961abb993123a46d0b98a0fa8db5b7b276301ded642c6",
      "signature": {
        "s": "0x3aec9ec46b9ac11982a96157d2fc2e76eb089763e63e9ad8f9773af30174c167",
        "r": "0x2dcc57551e317b1df40289e77c920a7b0b12c5b6ab10c7c6f9b25760b2625925",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6ac64ed0399427055b556ae2cdd3213f363322c15b4161bca847a026e522e936",
      "signature": {
        "s": "0x2f5aaaa61728de8d11f90554d8b36361fdf02d67fdaffa6535cc8d97cf0c5c74",
        "r": "0x53717ddae5f4302d2a8a7fb43de5a40ad0d431d465236978593f9fcc9d99643f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48312262913615360483",
    "total": "1355689070984816141333"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48312262913615360483",
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
            "amount": "27260567199772731325754"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48312262913615360"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMzEyYTNkZC1jYjZlLTU4MjMtYTk0MS02NjNmZGE5YTJmNDcifQ==",
    "nonce": 109866,
    "balances": {
      "current": "712469676581332449618982",
      "previous": "712518037156508978594825"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa47e244444f370fb30a05fecb0fdaeaa8a97d509",
    "nonce": 46,
    "balances": {
      "current": "2037729535956353422592",
      "previous": "1989417273042738062109"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:21.114Z",
  "updated": "2022-05-04T08:50:21.198Z",
  "id": "62723e4d7832e20011830afe"
}
```
* *stageAmount*: `2037729535956353422592`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000029e77a3268d5271e30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000029e77a3268d5271e30000000000000000000000000000000000000000000000497df71b4fe94aa415e9c6594c683af7c83ed961abb993123a46d0b98a0fa8db5b7b276301ded642c62dcc57551e317b1df40289e77c920a7b0b12c5b6ab10c7c6f9b25760b26259253aec9ec46b9ac11982a96157d2fc2e76eb089763e63e9ad8f9773af30174c167000000000000000000000000000000000000000000000000000000000000001b6ac64ed0399427055b556ae2cdd3213f363322c15b4161bca847a026e522e93653717ddae5f4302d2a8a7fb43de5a40ad0d431d465236978593f9fcc9d99643f2f5aaaa61728de8d11f90554d8b36361fdf02d67fdaffa6535cc8d97cf0c5c74000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad2a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096df0efdb897f585ec260000000000000000000000000000000000000000000096e1ae20ff7dc81b440900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000aba3bf4542e6000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5cc5dfb84a6c53d3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d7a457959544e6b5a43316a596a5a6c4c5455344d6a4d7459546b304d5330324e6a4e6d5a47453559544a6d4e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a47e244444f370fb30a05fecb0fdaeaa8a97d50900000000000000000000000000000000000000000000006e772d98993806150000000000000000000000000000000000000000000000006bd8b5f572aab3a31d00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xe9c6594c683af7c83ed961abb993123a46d0b98a0fa8db5b7b276301ded642c6",
      "signature": {
        "s": "0x3aec9ec46b9ac11982a96157d2fc2e76eb089763e63e9ad8f9773af30174c167",
        "r": "0x2dcc57551e317b1df40289e77c920a7b0b12c5b6ab10c7c6f9b25760b2625925",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x6ac64ed0399427055b556ae2cdd3213f363322c15b4161bca847a026e522e936",
      "signature": {
        "s": "0x2f5aaaa61728de8d11f90554d8b36361fdf02d67fdaffa6535cc8d97cf0c5c74",
        "r": "0x53717ddae5f4302d2a8a7fb43de5a40ad0d431d465236978593f9fcc9d99643f",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48312262913615360483",
    "total": "1355689070984816141333"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48312262913615360483",
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
            "amount": "27260567199772731325754"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48312262913615360"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMzEyYTNkZC1jYjZlLTU4MjMtYTk0MS02NjNmZGE5YTJmNDcifQ==",
    "nonce": 109866,
    "balances": {
      "current": "712469676581332449618982",
      "previous": "712518037156508978594825"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa47e244444f370fb30a05fecb0fdaeaa8a97d509",
    "nonce": 46,
    "balances": {
      "current": "2037729535956353422592",
      "previous": "1989417273042738062109"
    }
  },
  "blockNumber": "14709953",
  "created": "2022-05-04T08:50:21.114Z",
  "updated": "2022-05-04T08:50:21.198Z",
  "id": "62723e4d7832e20011830afe"
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
0x0f200f9b00000000000000000000000000000000000000000000006e772d9899380615000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2037729535956353422592`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`