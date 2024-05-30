# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7f84Ab3BF4C5273651B1cbD33269b7B9f68C122f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000133aef4de431d5a67400000000000000000000000000000000000000000000000074b79b86955478520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000074b79b869554785200000000000000000000000000000000000000000000000ccb32d6ba5c9b60a305562a9f8ac482cbf02302df1ee46542616c5af1267cc3b03130f55773166b83306d53dc22146146756d9d61916a3ceb470151398ab1a340c80da65da3ec29536b88ac6fb9122de502e72d1dcfeef927581e77df28e3fb3db5e9d66d725289e6000000000000000000000000000000000000000000000000000000000000001b94104dc45faf7893450af8863ace40f8bd2ec49fc3f466f5bb0a63ee7a085366cf2f3908ee87ebc46fed59771061ebebb745c7895f699b2b8fc22736be826e4a70b6bb073c0904e8c118f127179e11a96ff24148fb096438dca3c8afad0f3a9b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963e7a9abf58f82d923500000000000000000000000000000000000000000000963eef703c0d82e7c1f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001de12df565b76a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f56f375b072ef2bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d7a497a597a55334e53316d5a6d4e6b4c5455334f4451744f44566c4e433034596a41334f545a684e44566a4e7a676966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007f84ab3bf4c5273651b1cbd33269b7b9f68c122f0000000000000000000000000000000000000000000000133aef4de431d5a674000000000000000000000000000000000000000000000012c637b25d9c812e2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x05562a9f8ac482cbf02302df1ee46542616c5af1267cc3b03130f55773166b83",
      "signature": {
        "s": "0x6b88ac6fb9122de502e72d1dcfeef927581e77df28e3fb3db5e9d66d725289e6",
        "r": "0x306d53dc22146146756d9d61916a3ceb470151398ab1a340c80da65da3ec2953",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x94104dc45faf7893450af8863ace40f8bd2ec49fc3f466f5bb0a63ee7a085366",
      "signature": {
        "s": "0x70b6bb073c0904e8c118f127179e11a96ff24148fb096438dca3c8afad0f3a9b",
        "r": "0xcf2f3908ee87ebc46fed59771061ebebb745c7895f699b2b8fc22736be826e4a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8410361831470954578",
    "total": "236002930318955471011"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8410361831470954578",
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
            "amount": "27263526411994817032891"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8410361831470954"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MzIzYzU3NS1mZmNkLTU3ODQtODVlNC04YjA3OTZhNDVjNzgifQ==",
    "nonce": 110082,
    "balances": {
      "current": "709507505147024656667189",
      "previous": "709515923919217959092721"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7f84ab3bf4c5273651b1cbd33269b7b9f68c122f",
    "nonce": 46,
    "balances": {
      "current": "354734836016599115380",
      "previous": "346324474185128160802"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:27.641Z",
  "updated": "2022-05-04T08:51:27.737Z",
  "id": "62723e8f3592fd001130b466"
}
```
* *stageAmount*: `354734836016599115380`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000074b79b86955478520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000074b79b869554785200000000000000000000000000000000000000000000000ccb32d6ba5c9b60a305562a9f8ac482cbf02302df1ee46542616c5af1267cc3b03130f55773166b83306d53dc22146146756d9d61916a3ceb470151398ab1a340c80da65da3ec29536b88ac6fb9122de502e72d1dcfeef927581e77df28e3fb3db5e9d66d725289e6000000000000000000000000000000000000000000000000000000000000001b94104dc45faf7893450af8863ace40f8bd2ec49fc3f466f5bb0a63ee7a085366cf2f3908ee87ebc46fed59771061ebebb745c7895f699b2b8fc22736be826e4a70b6bb073c0904e8c118f127179e11a96ff24148fb096438dca3c8afad0f3a9b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074c90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae02000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000963e7a9abf58f82d923500000000000000000000000000000000000000000000963eef703c0d82e7c1f100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001de12df565b76a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5f56f375b072ef2bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d7a497a597a55334e53316d5a6d4e6b4c5455334f4451744f44566c4e433034596a41334f545a684e44566a4e7a676966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007f84ab3bf4c5273651b1cbd33269b7b9f68c122f0000000000000000000000000000000000000000000000133aef4de431d5a674000000000000000000000000000000000000000000000012c637b25d9c812e2200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x05562a9f8ac482cbf02302df1ee46542616c5af1267cc3b03130f55773166b83",
      "signature": {
        "s": "0x6b88ac6fb9122de502e72d1dcfeef927581e77df28e3fb3db5e9d66d725289e6",
        "r": "0x306d53dc22146146756d9d61916a3ceb470151398ab1a340c80da65da3ec2953",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x94104dc45faf7893450af8863ace40f8bd2ec49fc3f466f5bb0a63ee7a085366",
      "signature": {
        "s": "0x70b6bb073c0904e8c118f127179e11a96ff24148fb096438dca3c8afad0f3a9b",
        "r": "0xcf2f3908ee87ebc46fed59771061ebebb745c7895f699b2b8fc22736be826e4a",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8410361831470954578",
    "total": "236002930318955471011"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8410361831470954578",
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
            "amount": "27263526411994817032891"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8410361831470954"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MzIzYzU3NS1mZmNkLTU3ODQtODVlNC04YjA3OTZhNDVjNzgifQ==",
    "nonce": 110082,
    "balances": {
      "current": "709507505147024656667189",
      "previous": "709515923919217959092721"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7f84ab3bf4c5273651b1cbd33269b7b9f68c122f",
    "nonce": 46,
    "balances": {
      "current": "354734836016599115380",
      "previous": "346324474185128160802"
    }
  },
  "blockNumber": "14709961",
  "created": "2022-05-04T08:51:27.641Z",
  "updated": "2022-05-04T08:51:27.737Z",
  "id": "62723e8f3592fd001130b466"
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
0x0f200f9b0000000000000000000000000000000000000000000000133aef4de431d5a6740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `354734836016599115380`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`