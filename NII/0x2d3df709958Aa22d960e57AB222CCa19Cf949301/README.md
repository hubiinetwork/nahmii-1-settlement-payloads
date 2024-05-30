# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x2d3df709958Aa22d960e57AB222CCa19Cf949301`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000071ae226dbb604da80000000000000000000000000000000000000000000000000a675fa96a66a3f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a675fa96a66a3f700000000000000000000000000000000000000000000000071ae226dbb604da8c734ffc96f19096b8a52ce1c10132787111104db0fcff4e9d019a6452912d9e37ecad2ad6fa6155271233fe1d00178747a0ab9c0d49b85941ef27086dbb6a00c66411ebf75e71bed825b5e7861dba8814573f9379b98b1cab3780f59f4111656000000000000000000000000000000000000000000000000000000000000001cc2552b1385c9b0a2092a5dd9e79e2142aa6a75465ae6e852be6c09672401950a22b20d68ea3a347979d719bab732f6b4f001691ad00514f5f92800eed050a0de06e4d960f502e6333b36f0b8f0bd297a1dcbd188e85e638aae753a02fa2cad4d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5de000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032af830a3e5cc689aefc0000000000000000000000000000000000000000000032af8d7447d90c6fea2700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002a9d2db7f97340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df6b947189d3511c350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493359545532593251774e6930304d6d49794c5455314d5749744f5467354d5330304d6a45355a6a45774d5746685a44496966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000002d3df709958aa22d960e57ab222cca19cf94930100000000000000000000000000000000000000000000000071ae226dbb604da80000000000000000000000000000000000000000000000006746c2c450f9a9b100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc734ffc96f19096b8a52ce1c10132787111104db0fcff4e9d019a6452912d9e3",
      "signature": {
        "s": "0x66411ebf75e71bed825b5e7861dba8814573f9379b98b1cab3780f59f4111656",
        "r": "0x7ecad2ad6fa6155271233fe1d00178747a0ab9c0d49b85941ef27086dbb6a00c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc2552b1385c9b0a2092a5dd9e79e2142aa6a75465ae6e852be6c09672401950a",
      "signature": {
        "s": "0x06e4d960f502e6333b36f0b8f0bd297a1dcbd188e85e638aae753a02fa2cad4d",
        "r": "0x22b20d68ea3a347979d719bab732f6b4f001691ad00514f5f92800eed050a0de",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "749673044219700215",
    "total": "8191522626923941288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "749673044219700215",
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
            "amount": "27733208288480837311541"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "749673044219700"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3YTU2Y2QwNi00MmIyLTU1MWItOTg5MS00MjE5ZjEwMWFhZDIifQ==",
    "nonce": 112094,
    "balances": {
      "current": "239355946784518356709116",
      "previous": "239356697207235620629031"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d3df709958aa22d960e57ab222cca19cf949301",
    "nonce": 11,
    "balances": {
      "current": "8191522626923941288",
      "previous": "7441849582704241073"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:58.906Z",
  "updated": "2022-05-04T09:01:58.967Z",
  "id": "62724106bbd75600116d077c"
}
```
* *stageAmount*: `8191522626923941288`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000a675fa96a66a3f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000a675fa96a66a3f700000000000000000000000000000000000000000000000071ae226dbb604da8c734ffc96f19096b8a52ce1c10132787111104db0fcff4e9d019a6452912d9e37ecad2ad6fa6155271233fe1d00178747a0ab9c0d49b85941ef27086dbb6a00c66411ebf75e71bed825b5e7861dba8814573f9379b98b1cab3780f59f4111656000000000000000000000000000000000000000000000000000000000000001cc2552b1385c9b0a2092a5dd9e79e2142aa6a75465ae6e852be6c09672401950a22b20d68ea3a347979d719bab732f6b4f001691ad00514f5f92800eed050a0de06e4d960f502e6333b36f0b8f0bd297a1dcbd188e85e638aae753a02fa2cad4d000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b5de000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000032af830a3e5cc689aefc0000000000000000000000000000000000000000000032af8d7447d90c6fea2700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000002a9d2db7f97340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df6b947189d3511c350000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69493359545532593251774e6930304d6d49794c5455314d5749744f5467354d5330304d6a45355a6a45774d5746685a44496966513d3d000000000000000000000000000000000000000000000000000000000000000b0000000000000000000000002d3df709958aa22d960e57ab222cca19cf94930100000000000000000000000000000000000000000000000071ae226dbb604da80000000000000000000000000000000000000000000000006746c2c450f9a9b100000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc734ffc96f19096b8a52ce1c10132787111104db0fcff4e9d019a6452912d9e3",
      "signature": {
        "s": "0x66411ebf75e71bed825b5e7861dba8814573f9379b98b1cab3780f59f4111656",
        "r": "0x7ecad2ad6fa6155271233fe1d00178747a0ab9c0d49b85941ef27086dbb6a00c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xc2552b1385c9b0a2092a5dd9e79e2142aa6a75465ae6e852be6c09672401950a",
      "signature": {
        "s": "0x06e4d960f502e6333b36f0b8f0bd297a1dcbd188e85e638aae753a02fa2cad4d",
        "r": "0x22b20d68ea3a347979d719bab732f6b4f001691ad00514f5f92800eed050a0de",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "749673044219700215",
    "total": "8191522626923941288"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "749673044219700215",
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
            "amount": "27733208288480837311541"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "749673044219700"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3YTU2Y2QwNi00MmIyLTU1MWItOTg5MS00MjE5ZjEwMWFhZDIifQ==",
    "nonce": 112094,
    "balances": {
      "current": "239355946784518356709116",
      "previous": "239356697207235620629031"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x2d3df709958aa22d960e57ab222cca19cf949301",
    "nonce": 11,
    "balances": {
      "current": "8191522626923941288",
      "previous": "7441849582704241073"
    }
  },
  "blockNumber": "14709988",
  "created": "2022-05-04T09:01:58.906Z",
  "updated": "2022-05-04T09:01:58.967Z",
  "id": "62724106bbd75600116d077c"
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
0x0f200f9b00000000000000000000000000000000000000000000000071ae226dbb604da80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8191522626923941288`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`