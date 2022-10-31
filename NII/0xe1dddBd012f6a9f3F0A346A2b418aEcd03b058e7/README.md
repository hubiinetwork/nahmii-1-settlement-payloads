# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xe1dddBd012f6a9f3F0A346A2b418aEcd03b058e7`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de64cb2b3319fde000000000000000000000000000000000000000000000000000001033a50e2a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000001033a50e2a0000000000000000000000000000000000000000000000000000017a1f40ab20cff820f054215cdb112665750c9b762c186be45b6c3b7db31109a136a257d1ccc84ec1e011613e112d97ad348766f85ecbfc8ff1da0bc37fad971405ca569a412127517ef4b1178ac6843b3a27d0ae12c689e7ff864f185375190f4135406f668000000000000000000000000000000000000000000000000000000000000001c5533e6466042348288050f1c07ecac50fa09c768e1bb07cc5522d42b84440f553f4a7d10c812cfbbf6d9b919b7c73ed8e13a64af4ffbcb777fb9070db02dd5610b6670343471759cc0deef4b732d045323734ea2a2ad376251950827caf70fc4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b745000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002daf538c6528e3cb58f3000000000000000000000000000000000000000000002daf538c662c6078fc5000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000425cc0bd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b2faddef6862f1a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d475a684f54686b5a533033595455354c5455335a6a67744f4441324e4331694f44566b597a5268596a51314e7a496966513d3d000000000000000000000000000000000000000000000000000000000000002b000000000000000000000000e1dddbd012f6a9f3f0a346a2b418aecd03b058e70000000000000000000000000000000000000000000000000de64cb2b3319fde0000000000000000000000000000000000000000000000000de64baf78e0bd3e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002d60f9cfb750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xff820f054215cdb112665750c9b762c186be45b6c3b7db31109a136a257d1ccc",
      "signature": {
        "s": "0x127517ef4b1178ac6843b3a27d0ae12c689e7ff864f185375190f4135406f668",
        "r": "0x84ec1e011613e112d97ad348766f85ecbfc8ff1da0bc37fad971405ca569a412",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5533e6466042348288050f1c07ecac50fa09c768e1bb07cc5522d42b84440f55",
      "signature": {
        "s": "0x0b6670343471759cc0deef4b732d045323734ea2a2ad376251950827caf70fc4",
        "r": "0x3f4a7d10c812cfbbf6d9b919b7c73ed8e13a64af4ffbcb777fb9070db02dd561",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1113374909088",
    "total": "25984351515148"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1113374909088",
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
            "amount": "27756799951362412704167"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1113374909"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MGZhOThkZS03YTU5LTU3ZjgtODA2NC1iODVkYzRhYjQ1NzIifQ==",
    "nonce": 112453,
    "balances": {
      "current": "215740692240061388511475",
      "previous": "215740692241175876795472"
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
            "amount": "12773000000000000"
          }
        }
      ]
    },
    "wallet": "0xe1dddbd012f6a9f3f0a346a2b418aecd03b058e7",
    "nonce": 43,
    "balances": {
      "current": "1001572297530777566",
      "previous": "1001571184155868478"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:52.356Z",
  "updated": "2022-05-04T09:03:52.438Z",
  "id": "62724178bbd75600116d07f4"
}
```
* *stageAmount*: `1001572297530777566`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000680000000000000000000000000000000000000000000000000000001033a50e2a00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000001033a50e2a0000000000000000000000000000000000000000000000000000017a1f40ab20cff820f054215cdb112665750c9b762c186be45b6c3b7db31109a136a257d1ccc84ec1e011613e112d97ad348766f85ecbfc8ff1da0bc37fad971405ca569a412127517ef4b1178ac6843b3a27d0ae12c689e7ff864f185375190f4135406f668000000000000000000000000000000000000000000000000000000000000001c5533e6466042348288050f1c07ecac50fa09c768e1bb07cc5522d42b84440f553f4a7d10c812cfbbf6d9b919b7c73ed8e13a64af4ffbcb777fb9070db02dd5610b6670343471759cc0deef4b732d045323734ea2a2ad376251950827caf70fc4000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ea00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b745000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002daf538c6528e3cb58f3000000000000000000000000000000000000000000002daf538c662c6078fc5000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000425cc0bd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b2faddef6862f1a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d475a684f54686b5a533033595455354c5455335a6a67744f4441324e4331694f44566b597a5268596a51314e7a496966513d3d000000000000000000000000000000000000000000000000000000000000002b000000000000000000000000e1dddbd012f6a9f3f0a346a2b418aecd03b058e70000000000000000000000000000000000000000000000000de64cb2b3319fde0000000000000000000000000000000000000000000000000de64baf78e0bd3e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002d60f9cfb750000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xff820f054215cdb112665750c9b762c186be45b6c3b7db31109a136a257d1ccc",
      "signature": {
        "s": "0x127517ef4b1178ac6843b3a27d0ae12c689e7ff864f185375190f4135406f668",
        "r": "0x84ec1e011613e112d97ad348766f85ecbfc8ff1da0bc37fad971405ca569a412",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5533e6466042348288050f1c07ecac50fa09c768e1bb07cc5522d42b84440f55",
      "signature": {
        "s": "0x0b6670343471759cc0deef4b732d045323734ea2a2ad376251950827caf70fc4",
        "r": "0x3f4a7d10c812cfbbf6d9b919b7c73ed8e13a64af4ffbcb777fb9070db02dd561",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1113374909088",
    "total": "25984351515148"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1113374909088",
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
            "amount": "27756799951362412704167"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1113374909"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MGZhOThkZS03YTU5LTU3ZjgtODA2NC1iODVkYzRhYjQ1NzIifQ==",
    "nonce": 112453,
    "balances": {
      "current": "215740692240061388511475",
      "previous": "215740692241175876795472"
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
            "amount": "12773000000000000"
          }
        }
      ]
    },
    "wallet": "0xe1dddbd012f6a9f3f0a346a2b418aecd03b058e7",
    "nonce": 43,
    "balances": {
      "current": "1001572297530777566",
      "previous": "1001571184155868478"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:52.356Z",
  "updated": "2022-05-04T09:03:52.438Z",
  "id": "62724178bbd75600116d07f4"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b0000000000000000000000000000000000000000000000000de64cb2b3319fde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1001572297530777566`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`