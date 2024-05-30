# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBD0FA78c201D457Da4AC86332cD2E0ED047B1341`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000006fe4a334e958f5aae0000000000000000000000000000000000000000000000008fead0839dcc95d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000008fead0839dcc95d5000000000000000000000000000000000000000000000006fe4a334e958f5aaea3ea77a2f5a33fba4c4cd322ebc0318c1198ebdff1310a7a05c4691ac6c5318eaca7c345efc1f19ab6c3520e44c8e67e3bb17f9c911fca926c542b1b5b2b8ed716061bdfd42f93d64a7f4cfa7342890d9adc9170bf157ca8540bd531cad42770000000000000000000000000000000000000000000000000000000000000001bf324f45504549aee8092db59a41653d5176ca0e21149a4d16ad9f7ed4315df4458e60db00e2daa1c17be222660facf3516285e795780034cc110011fbebacfbf2cf1962ecea6164dda53888e544657d809ac1ce7bb0c21ba410ceb2d9fb934e9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf940000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001394f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000294cb79ac0038e0e2c2d00000000000000000000000000000000000000000000294d47aa6849dce887ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000024d7c2b10dc5c80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c442d78a36fb3247590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e6d5177596a466a4d4330794e544d334c545532595449744f575a6a4e69316b595759794d4446684e44426d596a416966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000bd0fa78c201d457da4ac86332cd2e0ed047b1341000000000000000000000000000000000000000000000006fe4a334e958f5aae0000000000000000000000000000000000000000000000066e5f62caf7c2c4d900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa3ea77a2f5a33fba4c4cd322ebc0318c1198ebdff1310a7a05c4691ac6c5318e",
      "signature": {
        "s": "0x16061bdfd42f93d64a7f4cfa7342890d9adc9170bf157ca8540bd531cad42770",
        "r": "0xaca7c345efc1f19ab6c3520e44c8e67e3bb17f9c911fca926c542b1b5b2b8ed7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf324f45504549aee8092db59a41653d5176ca0e21149a4d16ad9f7ed4315df44",
      "signature": {
        "s": "0x2cf1962ecea6164dda53888e544657d809ac1ce7bb0c21ba410ceb2d9fb934e9",
        "r": "0x58e60db00e2daa1c17be222660facf3516285e795780034cc110011fbebacfbf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10370330355680712149",
    "total": "129003978888777259694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10370330355680712149",
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
            "amount": "17787477757351251035993"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10370330355680712"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2NmQwYjFjMC0yNTM3LTU2YTItOWZjNi1kYWYyMDFhNDBmYjAifQ==",
    "nonce": 80207,
    "balances": {
      "current": "195032208445234234666029",
      "previous": "195042589145920271058890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd0fa78c201d457da4ac86332cd2e0ed047b1341",
    "nonce": 11,
    "balances": {
      "current": "129003978888777259694",
      "previous": "118633648533096547545"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:20.182Z",
  "updated": "2021-07-05T11:14:20.249Z",
  "id": "60e2e98ccc369000105e3009"
}
```
* *stageAmount*: `129003978888777259694`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000008fead0839dcc95d50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000008fead0839dcc95d5000000000000000000000000000000000000000000000006fe4a334e958f5aaea3ea77a2f5a33fba4c4cd322ebc0318c1198ebdff1310a7a05c4691ac6c5318eaca7c345efc1f19ab6c3520e44c8e67e3bb17f9c911fca926c542b1b5b2b8ed716061bdfd42f93d64a7f4cfa7342890d9adc9170bf157ca8540bd531cad42770000000000000000000000000000000000000000000000000000000000000001bf324f45504549aee8092db59a41653d5176ca0e21149a4d16ad9f7ed4315df4458e60db00e2daa1c17be222660facf3516285e795780034cc110011fbebacfbf2cf1962ecea6164dda53888e544657d809ac1ce7bb0c21ba410ceb2d9fb934e9000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf940000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001394f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000294cb79ac0038e0e2c2d00000000000000000000000000000000000000000000294d47aa6849dce887ca00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000024d7c2b10dc5c80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c442d78a36fb3247590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e6d5177596a466a4d4330794e544d334c545532595449744f575a6a4e69316b595759794d4446684e44426d596a416966513d3d000000000000000000000000000000000000000000000000000000000000000b000000000000000000000000bd0fa78c201d457da4ac86332cd2e0ed047b1341000000000000000000000000000000000000000000000006fe4a334e958f5aae0000000000000000000000000000000000000000000000066e5f62caf7c2c4d900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xa3ea77a2f5a33fba4c4cd322ebc0318c1198ebdff1310a7a05c4691ac6c5318e",
      "signature": {
        "s": "0x16061bdfd42f93d64a7f4cfa7342890d9adc9170bf157ca8540bd531cad42770",
        "r": "0xaca7c345efc1f19ab6c3520e44c8e67e3bb17f9c911fca926c542b1b5b2b8ed7",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf324f45504549aee8092db59a41653d5176ca0e21149a4d16ad9f7ed4315df44",
      "signature": {
        "s": "0x2cf1962ecea6164dda53888e544657d809ac1ce7bb0c21ba410ceb2d9fb934e9",
        "r": "0x58e60db00e2daa1c17be222660facf3516285e795780034cc110011fbebacfbf",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10370330355680712149",
    "total": "129003978888777259694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10370330355680712149",
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
            "amount": "17787477757351251035993"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10370330355680712"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2NmQwYjFjMC0yNTM3LTU2YTItOWZjNi1kYWYyMDFhNDBmYjAifQ==",
    "nonce": 80207,
    "balances": {
      "current": "195032208445234234666029",
      "previous": "195042589145920271058890"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd0fa78c201d457da4ac86332cd2e0ed047b1341",
    "nonce": 11,
    "balances": {
      "current": "129003978888777259694",
      "previous": "118633648533096547545"
    }
  },
  "blockNumber": "12767124",
  "created": "2021-07-05T11:14:20.182Z",
  "updated": "2021-07-05T11:14:20.249Z",
  "id": "60e2e98ccc369000105e3009"
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
0x0f200f9b000000000000000000000000000000000000000000000006fe4a334e958f5aae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `129003978888777259694`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`