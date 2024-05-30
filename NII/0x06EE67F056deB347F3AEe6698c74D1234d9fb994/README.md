# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x06EE67F056deB347F3AEe6698c74D1234d9fb994`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000000000000000000000000000000990104fdde59f98177db5ecbda454d5cac2d12a2a6bc70c972cc17765c4fe10e77af197818c382656220a15f13a5842d1fb28a924034b3f35599e55cede2f04d8aa01760f436926739a19a11d857a680d35958c8491cfa39fe609dcf805fddd6eac845540386aad000000000000000000000000000000000000000000000000000000000000001b31b3330698e936fb6b5ba7c2e356ee15fc22c83c1f6b1ff57ea03fa330360d2c47c9af5fb398d736171cbd2e1c57842ba79031d62cbf61181c9ccda6c57423063e0c7a085417a08b1202a0ea275b9d985b6ce533cbf64dc25860de41393fcda0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012182000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023a642e7cb3035793a360000000000000000000000000000000000000000000023a64c7a4e346129107e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000272b44dca36b00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035964eabdf74b02e7e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e4441784e7a4269597931694d7a4d784c54566d5a544174596a646c4d5330344d5459784f4441794e474e694f47456966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000006ee67f056deb347f3aee6698c74d1234d9fb9940000000000000000000000000000000000000000000000000990104fdde59f98000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x177db5ecbda454d5cac2d12a2a6bc70c972cc17765c4fe10e77af197818c3826",
      "signature": {
        "s": "0x739a19a11d857a680d35958c8491cfa39fe609dcf805fddd6eac845540386aad",
        "r": "0x56220a15f13a5842d1fb28a924034b3f35599e55cede2f04d8aa01760f436926",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x31b3330698e936fb6b5ba7c2e356ee15fc22c83c1f6b1ff57ea03fa330360d2c",
      "signature": {
        "s": "0x3e0c7a085417a08b1202a0ea275b9d985b6ce533cbf64dc25860de41393fcda0",
        "r": "0x47c9af5fb398d736171cbd2e1c57842ba79031d62cbf61181c9ccda6c5742306",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "689068678198960024",
    "total": "689068678198960024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "689068678198960024",
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
            "amount": "15816131504587241875428"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "689068678198960"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDAxNzBiYy1iMzMxLTVmZTAtYjdlMS04MTYxODAyNGNiOGEifQ==",
    "nonce": 74114,
    "balances": {
      "current": "168349807462007407458870",
      "previous": "168350497219754284617854"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x06ee67f056deb347f3aee6698c74d1234d9fb994",
    "nonce": 1,
    "balances": {
      "current": "689068678198960024",
      "previous": "0"
    }
  },
  "blockNumber": "12400709",
  "created": "2021-05-09T14:36:57.308Z",
  "updated": "2021-05-09T14:36:57.393Z",
  "id": "6097f38910d28200105e2972"
}
```
* *stageAmount*: `689068678198960024`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000000000000000000000000000000990104fdde59f98177db5ecbda454d5cac2d12a2a6bc70c972cc17765c4fe10e77af197818c382656220a15f13a5842d1fb28a924034b3f35599e55cede2f04d8aa01760f436926739a19a11d857a680d35958c8491cfa39fe609dcf805fddd6eac845540386aad000000000000000000000000000000000000000000000000000000000000001b31b3330698e936fb6b5ba7c2e356ee15fc22c83c1f6b1ff57ea03fa330360d2c47c9af5fb398d736171cbd2e1c57842ba79031d62cbf61181c9ccda6c57423063e0c7a085417a08b1202a0ea275b9d985b6ce533cbf64dc25860de41393fcda0000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd384500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012182000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023a642e7cb3035793a360000000000000000000000000000000000000000000023a64c7a4e346129107e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000272b44dca36b00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000035964eabdf74b02e7e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314e4441784e7a4269597931694d7a4d784c54566d5a544174596a646c4d5330344d5459784f4441794e474e694f47456966513d3d000000000000000000000000000000000000000000000000000000000000000100000000000000000000000006ee67f056deb347f3aee6698c74d1234d9fb9940000000000000000000000000000000000000000000000000990104fdde59f98000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x177db5ecbda454d5cac2d12a2a6bc70c972cc17765c4fe10e77af197818c3826",
      "signature": {
        "s": "0x739a19a11d857a680d35958c8491cfa39fe609dcf805fddd6eac845540386aad",
        "r": "0x56220a15f13a5842d1fb28a924034b3f35599e55cede2f04d8aa01760f436926",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x31b3330698e936fb6b5ba7c2e356ee15fc22c83c1f6b1ff57ea03fa330360d2c",
      "signature": {
        "s": "0x3e0c7a085417a08b1202a0ea275b9d985b6ce533cbf64dc25860de41393fcda0",
        "r": "0x47c9af5fb398d736171cbd2e1c57842ba79031d62cbf61181c9ccda6c5742306",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "689068678198960024",
    "total": "689068678198960024"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "689068678198960024",
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
            "amount": "15816131504587241875428"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "689068678198960"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1NDAxNzBiYy1iMzMxLTVmZTAtYjdlMS04MTYxODAyNGNiOGEifQ==",
    "nonce": 74114,
    "balances": {
      "current": "168349807462007407458870",
      "previous": "168350497219754284617854"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x06ee67f056deb347f3aee6698c74d1234d9fb994",
    "nonce": 1,
    "balances": {
      "current": "689068678198960024",
      "previous": "0"
    }
  },
  "blockNumber": "12400709",
  "created": "2021-05-09T14:36:57.308Z",
  "updated": "2021-05-09T14:36:57.393Z",
  "id": "6097f38910d28200105e2972"
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
0x0f200f9b0000000000000000000000000000000000000000000000000990104fdde59f980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `689068678198960024`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`