# Settlement of ETH
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3ecccCA2B3Aaa3605B6478CA4627751762413218`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000009f600000000000000000000000000000000000000000000000000000000000009f6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000009f600000000000000000000000000000000000000000000000000000000000009f67625cce6cc121d23e58b0366cf16fdc08fc515e7d715443fa304410ee60e687751066e196202a551d8059977653f479b345f5c62851108f5a53314657027447870f99884aa5a5a705c73da8dcbe03c0bfdafb6c2c49d8806ff9e8812b4027721000000000000000000000000000000000000000000000000000000000000001c0486fb6cdf9055fd6e9da2d0d19dbdd9b488a3cfa2646d926f58bc09689e02b3791ba828d30b1a8e0112b8830b048f570fed857809a435addea425b4696ff35839ab97dc354e96e681df2684a137d46872fe1c75dfb7a0f8e8f16f03b9d0d5ab000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000089e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6c4e79000000000000000000000000000000000000000000000000002386f2bc6c587100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c289700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a5534593259354d79307a595759304c5456684d4445744f446b774f43316c5a5745784e4759355a5467345a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000003ecccca2b3aaa3605b6478ca462775176241321800000000000000000000000000000000000000000000000000000000000009f6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7625cce6cc121d23e58b0366cf16fdc08fc515e7d715443fa304410ee60e6877",
      "signature": {
        "s": "0x70f99884aa5a5a705c73da8dcbe03c0bfdafb6c2c49d8806ff9e8812b4027721",
        "r": "0x51066e196202a551d8059977653f479b345f5c62851108f5a533146570274478",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0486fb6cdf9055fd6e9da2d0d19dbdd9b488a3cfa2646d926f58bc09689e02b3",
      "signature": {
        "s": "0x39ab97dc354e96e681df2684a137d46872fe1c75dfb7a0f8e8f16f03b9d0d5ab",
        "r": "0x791ba828d30b1a8e0112b8830b048f570fed857809a435addea425b4696ff358",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2550",
    "total": "2550"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2550",
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
            "amount": "796823"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMzU4Y2Y5My0zYWY0LTVhMDEtODkwOC1lZWExNGY5ZTg4ZmUifQ==",
    "nonce": 2206,
    "balances": {
      "current": "10000001286295161",
      "previous": "10000001286297713"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ecccca2b3aaa3605b6478ca4627751762413218",
    "nonce": 16,
    "balances": {
      "current": "2550",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:02.710Z",
  "updated": "2020-05-22T08:15:02.785Z",
  "id": "5ec78a06e5756b00111b8241"
}
```
* *stageAmount*: `2550`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000009f6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000009f600000000000000000000000000000000000000000000000000000000000009f67625cce6cc121d23e58b0366cf16fdc08fc515e7d715443fa304410ee60e687751066e196202a551d8059977653f479b345f5c62851108f5a53314657027447870f99884aa5a5a705c73da8dcbe03c0bfdafb6c2c49d8806ff9e8812b4027721000000000000000000000000000000000000000000000000000000000000001c0486fb6cdf9055fd6e9da2d0d19dbdd9b488a3cfa2646d926f58bc09689e02b3791ba828d30b1a8e0112b8830b048f570fed857809a435addea425b4696ff35839ab97dc354e96e681df2684a137d46872fe1c75dfb7a0f8e8f16f03b9d0d5ab000000000000000000000000000000000000000000000000000000000000001b00000000000000000000000000000000000000000000000000000000009a55f30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000089e00000000000000000000000010ab8f3868df71e2992c643868cb765cca980e68000000000000000000000000000000000000000000000000002386f2bc6c4e79000000000000000000000000000000000000000000000000002386f2bc6c587100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000c289700000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794d7a5534593259354d79307a595759304c5456684d4445744f446b774f43316c5a5745784e4759355a5467345a6d556966513d3d00000000000000000000000000000000000000000000000000000000000000100000000000000000000000003ecccca2b3aaa3605b6478ca462775176241321800000000000000000000000000000000000000000000000000000000000009f6000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7625cce6cc121d23e58b0366cf16fdc08fc515e7d715443fa304410ee60e6877",
      "signature": {
        "s": "0x70f99884aa5a5a705c73da8dcbe03c0bfdafb6c2c49d8806ff9e8812b4027721",
        "r": "0x51066e196202a551d8059977653f479b345f5c62851108f5a533146570274478",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0486fb6cdf9055fd6e9da2d0d19dbdd9b488a3cfa2646d926f58bc09689e02b3",
      "signature": {
        "s": "0x39ab97dc354e96e681df2684a137d46872fe1c75dfb7a0f8e8f16f03b9d0d5ab",
        "r": "0x791ba828d30b1a8e0112b8830b048f570fed857809a435addea425b4696ff358",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "2550",
    "total": "2550"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2550",
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
            "amount": "796823"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x0000000000000000000000000000000000000000",
          "id": "0"
        },
        "amount": "2"
      }
    },
    "wallet": "0x10ab8f3868df71e2992c643868cb765cca980e68",
    "data": "eyJyZWYiOiIyMzU4Y2Y5My0zYWY0LTVhMDEtODkwOC1lZWExNGY5ZTg4ZmUifQ==",
    "nonce": 2206,
    "balances": {
      "current": "10000001286295161",
      "previous": "10000001286297713"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x3ecccca2b3aaa3605b6478ca4627751762413218",
    "nonce": 16,
    "balances": {
      "current": "2550",
      "previous": "0"
    }
  },
  "blockNumber": "10114547",
  "created": "2020-05-22T08:15:02.710Z",
  "updated": "2020-05-22T08:15:02.785Z",
  "id": "5ec78a06e5756b00111b8241"
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
0x0f200f9b00000000000000000000000000000000000000000000000000000000000009f60000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2550`
* *currencyCt*: `0x0000000000000000000000000000000000000000`
* *currencyId*: `0`
* *standard*: ``