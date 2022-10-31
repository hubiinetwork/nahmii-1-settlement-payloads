# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xD87a99c457c3B1da16c4a20B1EC212b16fbE00d8`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000003337b9b5b0796f719eb000000000000000000000000000000000000000000000015f424eeba4f6cd16c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000015f424eeba4f6cd16c00000000000000000000000000000000000000000000056d8646211c6779f41084f158e46c155c128f412f1f022dbaf7587f2c6e77383cfb1bcc32164ac62bd3cd616019ea018de97822c497cef6e1521dcb4b538dae8c212c713c12bedcba2c01e60885c67c0e38117236cb723c925eefb493e392098abe1c2867aa6f2dae0a000000000000000000000000000000000000000000000000000000000000001c0cea2b29f9cd8e9b8aaab9bee4cd2d10fdd64215dca08d28c7cfceae0aa8f1b6388e2dba14be082f5cb96c62926e8dae31267cfb3264f87f3168d7eedde422436915b18e3b6f332603b2f485bbf70f06d33371e215ac1cc014c2784634ca2c21000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7d0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c1c299bd6f77466256e000000000000000000000000000000000000000000001c32235f877818622d5500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000059ec1c6548f367b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e5319d813df87b56fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a546b795a5449304d6930344e4441334c5455314f5445744f474e6c4f4330774d544269596a59355a6a4a694d54416966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000d87a99c457c3b1da16c4a20b1ec212b16fbe00d80000000000000000000000000000000000000000000003337b9b5b0796f719eb00000000000000000000000000000000000000000000031d87766c4d478a487f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x84f158e46c155c128f412f1f022dbaf7587f2c6e77383cfb1bcc32164ac62bd3",
      "signature": {
        "s": "0x01e60885c67c0e38117236cb723c925eefb493e392098abe1c2867aa6f2dae0a",
        "r": "0xcd616019ea018de97822c497cef6e1521dcb4b538dae8c212c713c12bedcba2c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0cea2b29f9cd8e9b8aaab9bee4cd2d10fdd64215dca08d28c7cfceae0aa8f1b6",
      "signature": {
        "s": "0x6915b18e3b6f332603b2f485bbf70f06d33371e215ac1cc014c2784634ca2c21",
        "r": "0x388e2dba14be082f5cb96c62926e8dae31267cfb3264f87f3168d7eedde42243",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "404974074076280443244",
    "total": "25632202975637898130448"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "404974074076280443244",
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
            "amount": "27839711963010077251322"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "404974074076280443"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZTkyZTI0Mi04NDA3LTU1OTEtOGNlOC0wMTBiYjY5ZjJiMTAifQ==",
    "nonce": 112592,
    "balances": {
      "current": "132745768580749176743278",
      "previous": "133151147628899533466965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd87a99c457c3b1da16c4a20b1ec212b16fbe00d8",
    "nonce": 19,
    "balances": {
      "current": "15116790209144333736427",
      "previous": "14711816135068053293183"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:41.007Z",
  "updated": "2022-05-04T09:04:41.090Z",
  "id": "627241a8bbd75600116d081e"
}
```
* *stageAmount*: `15116790209144333736427`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000015f424eeba4f6cd16c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000015f424eeba4f6cd16c00000000000000000000000000000000000000000000056d8646211c6779f41084f158e46c155c128f412f1f022dbaf7587f2c6e77383cfb1bcc32164ac62bd3cd616019ea018de97822c497cef6e1521dcb4b538dae8c212c713c12bedcba2c01e60885c67c0e38117236cb723c925eefb493e392098abe1c2867aa6f2dae0a000000000000000000000000000000000000000000000000000000000000001c0cea2b29f9cd8e9b8aaab9bee4cd2d10fdd64215dca08d28c7cfceae0aa8f1b6388e2dba14be082f5cb96c62926e8dae31267cfb3264f87f3168d7eedde422436915b18e3b6f332603b2f485bbf70f06d33371e215ac1cc014c2784634ca2c21000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7d0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c1c299bd6f77466256e000000000000000000000000000000000000000000001c32235f877818622d5500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000059ec1c6548f367b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e5319d813df87b56fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949345a546b795a5449304d6930344e4441334c5455314f5445744f474e6c4f4330774d544269596a59355a6a4a694d54416966513d3d0000000000000000000000000000000000000000000000000000000000000013000000000000000000000000d87a99c457c3b1da16c4a20b1ec212b16fbe00d80000000000000000000000000000000000000000000003337b9b5b0796f719eb00000000000000000000000000000000000000000000031d87766c4d478a487f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0x84f158e46c155c128f412f1f022dbaf7587f2c6e77383cfb1bcc32164ac62bd3",
      "signature": {
        "s": "0x01e60885c67c0e38117236cb723c925eefb493e392098abe1c2867aa6f2dae0a",
        "r": "0xcd616019ea018de97822c497cef6e1521dcb4b538dae8c212c713c12bedcba2c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0cea2b29f9cd8e9b8aaab9bee4cd2d10fdd64215dca08d28c7cfceae0aa8f1b6",
      "signature": {
        "s": "0x6915b18e3b6f332603b2f485bbf70f06d33371e215ac1cc014c2784634ca2c21",
        "r": "0x388e2dba14be082f5cb96c62926e8dae31267cfb3264f87f3168d7eedde42243",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "404974074076280443244",
    "total": "25632202975637898130448"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "404974074076280443244",
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
            "amount": "27839711963010077251322"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "404974074076280443"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4ZTkyZTI0Mi04NDA3LTU1OTEtOGNlOC0wMTBiYjY5ZjJiMTAifQ==",
    "nonce": 112592,
    "balances": {
      "current": "132745768580749176743278",
      "previous": "133151147628899533466965"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd87a99c457c3b1da16c4a20b1ec212b16fbe00d8",
    "nonce": 19,
    "balances": {
      "current": "15116790209144333736427",
      "previous": "14711816135068053293183"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:41.007Z",
  "updated": "2022-05-04T09:04:41.090Z",
  "id": "627241a8bbd75600116d081e"
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
0x0f200f9b0000000000000000000000000000000000000000000003337b9b5b0796f719eb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `15116790209144333736427`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`