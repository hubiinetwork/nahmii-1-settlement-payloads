# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0881e242A1E9f9ba80d0800834DAe4549D4A3fd8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000029fa690fe3317a3000000000000000000000000000000000000000000000000000fec9054cfef9e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000fec9054cfef9e00000000000000000000000000000000000000000000000001bed857fb030831366b282b7fe35de1c1d142983856b875b6a5037cb15702f89331d713cb2798654fae01a130423930f97b244e96600b6fb06098c482c655d5388b97dc5af292c00d51e250b75d078d5958b4cbf55178506d7505b7d81905bf3499f588a8e55166000000000000000000000000000000000000000000000000000000000000001c60b044eda4044e2510c652088f2e6c481daceef638dfdbe2ca75e96fa7c7806fdd28dfcecc7c0f52243f1815816a371a4d037963cada232598253e4aa604ff7168f0f2b8ca87d3058dcdf70427f7c04db977031e215619fd3112c45e4680a4d7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac56000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8df3f19dfd43ce1c34000000000000000000000000000000000000000000009a8df4018ea1324d5bad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000041399af4fdb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db3a30bd5351d3fc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e3251314e444d774d5330785a6a63774c54557a4d6a51744f544d314e43316d4e7a64694e5749304d7a4e6d5957556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000881e242a1e9f9ba80d0800834dae4549d4a3fd8000000000000000000000000000000000000000000000000029fa690fe3317a3000000000000000000000000000000000000000000000000028fba00a963280500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x366b282b7fe35de1c1d142983856b875b6a5037cb15702f89331d713cb279865",
      "signature": {
        "s": "0x0d51e250b75d078d5958b4cbf55178506d7505b7d81905bf3499f588a8e55166",
        "r": "0x4fae01a130423930f97b244e96600b6fb06098c482c655d5388b97dc5af292c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60b044eda4044e2510c652088f2e6c481daceef638dfdbe2ca75e96fa7c7806f",
      "signature": {
        "s": "0x68f0f2b8ca87d3058dcdf70427f7c04db977031e215619fd3112c45e4680a4d7",
        "r": "0xdd28dfcecc7c0f52243f1815816a371a4d037963cada232598253e4aa604ff71",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4482229293019038",
    "total": "125775711997986865"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4482229293019038",
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
            "amount": "27243191245027958445052"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4482229293019"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4N2Q1NDMwMS0xZjcwLTUzMjQtOTM1NC1mNzdiNWI0MzNmYWUifQ==",
    "nonce": 109654,
    "balances": {
      "current": "729863007280850103311412",
      "previous": "729863011767561625623469"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0881e242a1e9f9ba80d0800834dae4549d4a3fd8",
    "nonce": 46,
    "balances": {
      "current": "189052851043112867",
      "previous": "184570621750093829"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:13.559Z",
  "updated": "2022-05-04T08:49:13.679Z",
  "id": "62723e097832e20011830ab8"
}
```
* *stageAmount*: `189052851043112867`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000fec9054cfef9e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000fec9054cfef9e00000000000000000000000000000000000000000000000001bed857fb030831366b282b7fe35de1c1d142983856b875b6a5037cb15702f89331d713cb2798654fae01a130423930f97b244e96600b6fb06098c482c655d5388b97dc5af292c00d51e250b75d078d5958b4cbf55178506d7505b7d81905bf3499f588a8e55166000000000000000000000000000000000000000000000000000000000000001c60b044eda4044e2510c652088f2e6c481daceef638dfdbe2ca75e96fa7c7806fdd28dfcecc7c0f52243f1815816a371a4d037963cada232598253e4aa604ff7168f0f2b8ca87d3058dcdf70427f7c04db977031e215619fd3112c45e4680a4d7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac56000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a8df3f19dfd43ce1c34000000000000000000000000000000000000000000009a8df4018ea1324d5bad00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000041399af4fdb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4db3a30bd5351d3fc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e3251314e444d774d5330785a6a63774c54557a4d6a51744f544d314e43316d4e7a64694e5749304d7a4e6d5957556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000000881e242a1e9f9ba80d0800834dae4549d4a3fd8000000000000000000000000000000000000000000000000029fa690fe3317a3000000000000000000000000000000000000000000000000028fba00a963280500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x366b282b7fe35de1c1d142983856b875b6a5037cb15702f89331d713cb279865",
      "signature": {
        "s": "0x0d51e250b75d078d5958b4cbf55178506d7505b7d81905bf3499f588a8e55166",
        "r": "0x4fae01a130423930f97b244e96600b6fb06098c482c655d5388b97dc5af292c0",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x60b044eda4044e2510c652088f2e6c481daceef638dfdbe2ca75e96fa7c7806f",
      "signature": {
        "s": "0x68f0f2b8ca87d3058dcdf70427f7c04db977031e215619fd3112c45e4680a4d7",
        "r": "0xdd28dfcecc7c0f52243f1815816a371a4d037963cada232598253e4aa604ff71",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "4482229293019038",
    "total": "125775711997986865"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4482229293019038",
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
            "amount": "27243191245027958445052"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4482229293019"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4N2Q1NDMwMS0xZjcwLTUzMjQtOTM1NC1mNzdiNWI0MzNmYWUifQ==",
    "nonce": 109654,
    "balances": {
      "current": "729863007280850103311412",
      "previous": "729863011767561625623469"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x0881e242a1e9f9ba80d0800834dae4549d4a3fd8",
    "nonce": 46,
    "balances": {
      "current": "189052851043112867",
      "previous": "184570621750093829"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:13.559Z",
  "updated": "2022-05-04T08:49:13.679Z",
  "id": "62723e097832e20011830ab8"
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
0x0f200f9b000000000000000000000000000000000000000000000000029fa690fe3317a30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `189052851043112867`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`