# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x11e742D8cc0B73455Ca882a6e6a742a6f954dc2a`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000488e2c20778f2ec027000000000000000000000000000000000000000000000001b85f64daafe286330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64daafe286330000000000000000000000000000000000000000000000304548c42c0fab02335160c7e9737119c1cd6b1ab8b0044fc5527ae60ddafa3fb2a84555f96fb530464c599b4cc0de8da85d36edb7bf472e0a97776cf5b2f0beb865a851b3bf0fcefc1b77f96602e6d32352d8e2e255e571aa94212c991ce76fc86ca2bc1e194dfe13000000000000000000000000000000000000000000000000000000000000001cd75faf3c4e7bf850c5ee3a78aafa12bbeb4527d6fe528f3aefea66a8d81aae0ca42367fdb0b9b3839ad5c288cfb4581d24ab95d09ebb5070f4de9c444a70077d2779edd9094bae79104076f4b947f13fc8ae2cfb5a65aa1a1a273bb6497173d5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6ee000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fc483d78b5dbac8961b000000000000000000000000000000000000000000002fc63ca7ac7b3203252400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c75808d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02a9eb95359d99cd70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d324d31595441324e79316b4e47557a4c5455334d44637459544e694e5330324f44646b5a5445344f444d345a6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000011e742d8cc0b73455ca882a6e6a742a6f954dc2a0000000000000000000000000000000000000000000000488e2c20778f2ec027000000000000000000000000000000000000000000000046d5ccbb9cdf4c39f400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5160c7e9737119c1cd6b1ab8b0044fc5527ae60ddafa3fb2a84555f96fb53046",
      "signature": {
        "s": "0x1b77f96602e6d32352d8e2e255e571aa94212c991ce76fc86ca2bc1e194dfe13",
        "r": "0x4c599b4cc0de8da85d36edb7bf472e0a97776cf5b2f0beb865a851b3bf0fcefc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd75faf3c4e7bf850c5ee3a78aafa12bbeb4527d6fe528f3aefea66a8d81aae0c",
      "signature": {
        "s": "0x2779edd9094bae79104076f4b947f13fc8ae2cfb5a65aa1a1a273bb6497173d5",
        "r": "0xa42367fdb0b9b3839ad5c288cfb4581d24ab95d09ebb5070f4de9c444a70077d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31732192389892310579",
    "total": "890436171418519142963"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389892310579",
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
            "amount": "27746974182622719745239"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389892310"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxM2M1YTA2Ny1kNGUzLTU3MDctYTNiNS02ODdkZTE4ODM4ZjIifQ==",
    "nonce": 112366,
    "balances": {
      "current": "225576286748494040438299",
      "previous": "225608050673076322641188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x11e742d8cc0b73455ca882a6e6a742a6f954dc2a",
    "nonce": 46,
    "balances": {
      "current": "1338410172257324154919",
      "previous": "1306677979867431844340"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:25.841Z",
  "updated": "2022-05-04T09:03:25.951Z",
  "id": "6272415d3592fd001130b772"
}
```
* *stageAmount*: `1338410172257324154919`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001b85f64daafe286330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b85f64daafe286330000000000000000000000000000000000000000000000304548c42c0fab02335160c7e9737119c1cd6b1ab8b0044fc5527ae60ddafa3fb2a84555f96fb530464c599b4cc0de8da85d36edb7bf472e0a97776cf5b2f0beb865a851b3bf0fcefc1b77f96602e6d32352d8e2e255e571aa94212c991ce76fc86ca2bc1e194dfe13000000000000000000000000000000000000000000000000000000000000001cd75faf3c4e7bf850c5ee3a78aafa12bbeb4527d6fe528f3aefea66a8d81aae0ca42367fdb0b9b3839ad5c288cfb4581d24ab95d09ebb5070f4de9c444a70077d2779edd9094bae79104076f4b947f13fc8ae2cfb5a65aa1a1a273bb6497173d5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6ee000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002fc483d78b5dbac8961b000000000000000000000000000000000000000000002fc63ca7ac7b3203252400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000070bc42c75808d60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e02a9eb95359d99cd70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d324d31595441324e79316b4e47557a4c5455334d44637459544e694e5330324f44646b5a5445344f444d345a6a496966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000011e742d8cc0b73455ca882a6e6a742a6f954dc2a0000000000000000000000000000000000000000000000488e2c20778f2ec027000000000000000000000000000000000000000000000046d5ccbb9cdf4c39f400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5160c7e9737119c1cd6b1ab8b0044fc5527ae60ddafa3fb2a84555f96fb53046",
      "signature": {
        "s": "0x1b77f96602e6d32352d8e2e255e571aa94212c991ce76fc86ca2bc1e194dfe13",
        "r": "0x4c599b4cc0de8da85d36edb7bf472e0a97776cf5b2f0beb865a851b3bf0fcefc",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xd75faf3c4e7bf850c5ee3a78aafa12bbeb4527d6fe528f3aefea66a8d81aae0c",
      "signature": {
        "s": "0x2779edd9094bae79104076f4b947f13fc8ae2cfb5a65aa1a1a273bb6497173d5",
        "r": "0xa42367fdb0b9b3839ad5c288cfb4581d24ab95d09ebb5070f4de9c444a70077d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "31732192389892310579",
    "total": "890436171418519142963"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31732192389892310579",
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
            "amount": "27746974182622719745239"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31732192389892310"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxM2M1YTA2Ny1kNGUzLTU3MDctYTNiNS02ODdkZTE4ODM4ZjIifQ==",
    "nonce": 112366,
    "balances": {
      "current": "225576286748494040438299",
      "previous": "225608050673076322641188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x11e742d8cc0b73455ca882a6e6a742a6f954dc2a",
    "nonce": 46,
    "balances": {
      "current": "1338410172257324154919",
      "previous": "1306677979867431844340"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:25.841Z",
  "updated": "2022-05-04T09:03:25.951Z",
  "id": "6272415d3592fd001130b772"
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
0x0f200f9b0000000000000000000000000000000000000000000000488e2c20778f2ec0270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1338410172257324154919`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`