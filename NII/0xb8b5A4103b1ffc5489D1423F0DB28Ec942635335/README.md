# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb8b5A4103b1ffc5489D1423F0DB28Ec942635335`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000ecb2a9cc60c230f000000000000000000000000000000000000000000000000000000015cc55aad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000015cc55aad0000000000000000000000000000000000000000000000000000001fcbbd67ca69aae5bf3fdd8e8f61b898c740bdca48188f16a6d390ab309726ef02abc5e276a2d61be67b025eedfd523d7b1b9ff6debd45b346ea9173f40cf0282801025cac1ed42aafb4851138b1ca10fa27217bf6c795872dcd5c9c61ac1c9343d8034772000000000000000000000000000000000000000000000000000000000000001c22b0bd0b82b5ea726f823badb3ffa17c9b5c9b6f811e448b6a3c657adebe765bb42fddf635571e186fcc63cacbd54735aa7acf58bc268125578374f3283e2cfa673054a3eee671ad98ce4d214bbb475604fae4eeef5d88542b9290ccdd0a01ef000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d400000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b1ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a915947272b11f5249b000000000000000000000000000000000000000000004a915947272c6f13c85400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000059490c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d950004e864b70faa10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463784e444a69595331685a545a684c5456695a6a6374596a67775979316d4d574a694e6a46684e4468694e47516966513d3d0000000000000000000000000000000000000000000000000000000000000025000000000000000000000000b8b5a4103b1ffc5489d1423f0db28ec9426353350000000000000000000000000000000000000000000000000ecb2a9cc60c230f0000000000000000000000000000000000000000000000000ecb2a9b6946c86200000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4ef819464c8000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x69aae5bf3fdd8e8f61b898c740bdca48188f16a6d390ab309726ef02abc5e276",
      "signature": {
        "s": "0x1ed42aafb4851138b1ca10fa27217bf6c795872dcd5c9c61ac1c9343d8034772",
        "r": "0xa2d61be67b025eedfd523d7b1b9ff6debd45b346ea9173f40cf0282801025cac",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x22b0bd0b82b5ea726f823badb3ffa17c9b5c9b6f811e448b6a3c657adebe765b",
      "signature": {
        "s": "0x673054a3eee671ad98ce4d214bbb475604fae4eeef5d88542b9290ccdd0a01ef",
        "r": "0xb42fddf635571e186fcc63cacbd54735aa7acf58bc268125578374f3283e2cfa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5851404973",
    "total": "136562173898"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5851404973",
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
            "amount": "27620540572204931283617"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5851404"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTcxNDJiYS1hZTZhLTViZjctYjgwYy1mMWJiNjFhNDhiNGQifQ==",
    "nonce": 111021,
    "balances": {
      "current": "352136330776700291196059",
      "previous": "352136330776706148452436"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "46425236000000000"
          }
        }
      ]
    },
    "wallet": "0xb8b5a4103b1ffc5489d1423f0db28ec942635335",
    "nonce": 37,
    "balances": {
      "current": "1065992589629203215",
      "previous": "1065992583777798242"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:11.347Z",
  "updated": "2022-05-04T08:56:11.452Z",
  "id": "62723fabbbd75600116d062d"
}
```
* *stageAmount*: `1065992589629203215`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000680000000000000000000000000000000000000000000000000000000015cc55aad0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000015cc55aad0000000000000000000000000000000000000000000000000000001fcbbd67ca69aae5bf3fdd8e8f61b898c740bdca48188f16a6d390ab309726ef02abc5e276a2d61be67b025eedfd523d7b1b9ff6debd45b346ea9173f40cf0282801025cac1ed42aafb4851138b1ca10fa27217bf6c795872dcd5c9c61ac1c9343d8034772000000000000000000000000000000000000000000000000000000000000001c22b0bd0b82b5ea726f823badb3ffa17c9b5c9b6f811e448b6a3c657adebe765bb42fddf635571e186fcc63cacbd54735aa7acf58bc268125578374f3283e2cfa673054a3eee671ad98ce4d214bbb475604fae4eeef5d88542b9290ccdd0a01ef000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d400000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b1ad000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004a915947272b11f5249b000000000000000000000000000000000000000000004a915947272c6f13c85400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000059490c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d950004e864b70faa10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794f5463784e444a69595331685a545a684c5456695a6a6374596a67775979316d4d574a694e6a46684e4468694e47516966513d3d0000000000000000000000000000000000000000000000000000000000000025000000000000000000000000b8b5a4103b1ffc5489d1423f0db28ec9426353350000000000000000000000000000000000000000000000000ecb2a9cc60c230f0000000000000000000000000000000000000000000000000ecb2a9b6946c86200000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a4ef819464c8000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x69aae5bf3fdd8e8f61b898c740bdca48188f16a6d390ab309726ef02abc5e276",
      "signature": {
        "s": "0x1ed42aafb4851138b1ca10fa27217bf6c795872dcd5c9c61ac1c9343d8034772",
        "r": "0xa2d61be67b025eedfd523d7b1b9ff6debd45b346ea9173f40cf0282801025cac",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x22b0bd0b82b5ea726f823badb3ffa17c9b5c9b6f811e448b6a3c657adebe765b",
      "signature": {
        "s": "0x673054a3eee671ad98ce4d214bbb475604fae4eeef5d88542b9290ccdd0a01ef",
        "r": "0xb42fddf635571e186fcc63cacbd54735aa7acf58bc268125578374f3283e2cfa",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "5851404973",
    "total": "136562173898"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "5851404973",
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
            "amount": "27620540572204931283617"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "5851404"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyOTcxNDJiYS1hZTZhLTViZjctYjgwYy1mMWJiNjFhNDhiNGQifQ==",
    "nonce": 111021,
    "balances": {
      "current": "352136330776700291196059",
      "previous": "352136330776706148452436"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "46425236000000000"
          }
        }
      ]
    },
    "wallet": "0xb8b5a4103b1ffc5489d1423f0db28ec942635335",
    "nonce": 37,
    "balances": {
      "current": "1065992589629203215",
      "previous": "1065992583777798242"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:11.347Z",
  "updated": "2022-05-04T08:56:11.452Z",
  "id": "62723fabbbd75600116d062d"
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
0x0f200f9b0000000000000000000000000000000000000000000000000ecb2a9cc60c230f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1065992589629203215`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`