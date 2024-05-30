# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa1b0305DD5FEa0B116D8601133A9d161b276C1F6`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000260a1e52df29800000000000000000000000000000000000000000000000000000e6e13921c180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000e6e13921c18000000000000000000000000000000000000000000000000000194eb6079c18a678fbe234e05e3e4813d6f6d0c3af4423fd5dfb30b8aede7dd3529d621a45f79e4d72a4099488e63d22fb17028bac3efc4b401b0217d297107f302ec227ca8fb520b1caaab34d6d21dc11649714db84366d4b528251309ff62a6dc10cf6ddf07000000000000000000000000000000000000000000000000000000000000001b197e2cd1921f74bc0b40951b43cdb0ad33c651d192f8232d13710261bd22aa7d7678914cf6279726f0a7418ab82f8d38a6f5fe47144c9923a3cc727df1ee31a90e6170a2fd33ea9638d3d2c9ef78ac2457bd181a393d030f04b371c9f4fed63e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af91000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000538478356d4ba93e293f00000000000000000000000000000000000000000000538478357bbd6e7f43d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000003b1aefe7d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d1b4e99f260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596a517a4e444d334d53316c4d5449354c5455334d444574596a68694d43316b5a5451304e574d354d4463334e54456966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000a1b0305dd5fea0b116d8601133a9d161b276c1f6000000000000000000000000000000000000000000000000000260a1e52df29800000000000000000000000000000000000000000000000000025233d19bd68000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x678fbe234e05e3e4813d6f6d0c3af4423fd5dfb30b8aede7dd3529d621a45f79",
      "signature": {
        "s": "0x520b1caaab34d6d21dc11649714db84366d4b528251309ff62a6dc10cf6ddf07",
        "r": "0xe4d72a4099488e63d22fb17028bac3efc4b401b0217d297107f302ec227ca8fb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x197e2cd1921f74bc0b40951b43cdb0ad33c651d192f8232d13710261bd22aa7d",
      "signature": {
        "s": "0x0e6170a2fd33ea9638d3d2c9ef78ac2457bd181a393d030f04b371c9f4fed63e",
        "r": "0x7678914cf6279726f0a7418ab82f8d38a6f5fe47144c9923a3cc727df1ee31a9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15865937533976",
    "total": "445213633528202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15865937533976",
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
            "amount": "27578319074234062184230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15865937533"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYjQzNDM3MS1lMTI5LTU3MDEtYjhiMC1kZTQ0NWM5MDc3NTEifQ==",
    "nonce": 110481,
    "balances": {
      "current": "394400050245540259965247",
      "previous": "394400050261422063436756"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa1b0305dd5fea0b116d8601133a9d161b276c1f6",
    "nonce": 45,
    "balances": {
      "current": "669198404416152",
      "previous": "653332466882176"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:30.489Z",
  "updated": "2022-05-04T08:53:30.572Z",
  "id": "62723f0abbd75600116d0577"
}
```
* *stageAmount*: `669198404416152`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000e6e13921c180000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000e6e13921c18000000000000000000000000000000000000000000000000000194eb6079c18a678fbe234e05e3e4813d6f6d0c3af4423fd5dfb30b8aede7dd3529d621a45f79e4d72a4099488e63d22fb17028bac3efc4b401b0217d297107f302ec227ca8fb520b1caaab34d6d21dc11649714db84366d4b528251309ff62a6dc10cf6ddf07000000000000000000000000000000000000000000000000000000000000001b197e2cd1921f74bc0b40951b43cdb0ad33c651d192f8232d13710261bd22aa7d7678914cf6279726f0a7418ab82f8d38a6f5fe47144c9923a3cc727df1ee31a90e6170a2fd33ea9638d3d2c9ef78ac2457bd181a393d030f04b371c9f4fed63e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d00000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af91000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000538478356d4ba93e293f00000000000000000000000000000000000000000000538478357bbd6e7f43d400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000003b1aefe7d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d7060f69d1b4e99f260000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a68596a517a4e444d334d53316c4d5449354c5455334d444574596a68694d43316b5a5451304e574d354d4463334e54456966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000a1b0305dd5fea0b116d8601133a9d161b276c1f6000000000000000000000000000000000000000000000000000260a1e52df29800000000000000000000000000000000000000000000000000025233d19bd68000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x678fbe234e05e3e4813d6f6d0c3af4423fd5dfb30b8aede7dd3529d621a45f79",
      "signature": {
        "s": "0x520b1caaab34d6d21dc11649714db84366d4b528251309ff62a6dc10cf6ddf07",
        "r": "0xe4d72a4099488e63d22fb17028bac3efc4b401b0217d297107f302ec227ca8fb",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x197e2cd1921f74bc0b40951b43cdb0ad33c651d192f8232d13710261bd22aa7d",
      "signature": {
        "s": "0x0e6170a2fd33ea9638d3d2c9ef78ac2457bd181a393d030f04b371c9f4fed63e",
        "r": "0x7678914cf6279726f0a7418ab82f8d38a6f5fe47144c9923a3cc727df1ee31a9",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15865937533976",
    "total": "445213633528202"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15865937533976",
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
            "amount": "27578319074234062184230"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15865937533"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJhYjQzNDM3MS1lMTI5LTU3MDEtYjhiMC1kZTQ0NWM5MDc3NTEifQ==",
    "nonce": 110481,
    "balances": {
      "current": "394400050245540259965247",
      "previous": "394400050261422063436756"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa1b0305dd5fea0b116d8601133a9d161b276c1f6",
    "nonce": 45,
    "balances": {
      "current": "669198404416152",
      "previous": "653332466882176"
    }
  },
  "blockNumber": "14709968",
  "created": "2022-05-04T08:53:30.489Z",
  "updated": "2022-05-04T08:53:30.572Z",
  "id": "62723f0abbd75600116d0577"
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
0x0f200f9b000000000000000000000000000000000000000000000000000260a1e52df2980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669198404416152`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`