# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xf5e4E85aEf766AAB9Cf574AeC331a81274BB977f`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000004932ce396812a66bb0000000000000000000000000000000000000000000000000000000286dc41650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000286dc41650000000000000000000000000000000000000000000000000000003af864c1a6021bb2089bb8e50252488b51d3d20e0110534e4e1eb446d61ff1f966949e554586ed94f34cf356fd9d60f451b26c1714a14b3b216c56fdd40ffe44efae360f0f391fb10f75f05e476022f4645b05fa983261fee44a4dc936a38f7f75ac4455e0000000000000000000000000000000000000000000000000000000000000001be5d4bd3b0a59a1290490a1f20d5a195e2a1a773720da144dac9e2aa48c1016dcb9ae397138ed3d04b7af24afee26dc68cb4ef8b33600d5dc7f0ff17cfd43efb87c55eb49eed47bf3b2be9bcb108b291a712c2740882cf548a12cec4636581949000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b31c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003e2a17a389899ac6f150000000000000000000000000000000000000000000003e2a17a3898c2248cb5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a598a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc7c0e064e72b0726b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314f5463784e4467304d79316b4e5455774c54566c4f475174596a4d784d79316d4f474a6a4f5455354f4441325957496966513d3d0000000000000000000000000000000000000000000000000000000000000022000000000000000000000000f5e4e85aef766aab9cf574aec331a81274bb977f000000000000000000000000000000000000000000000004932ce396812a66bb000000000000000000000000000000000000000000000004932ce393fa4e255600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x021bb2089bb8e50252488b51d3d20e0110534e4e1eb446d61ff1f966949e5545",
      "signature": {
        "s": "0x391fb10f75f05e476022f4645b05fa983261fee44a4dc936a38f7f75ac4455e0",
        "r": "0x86ed94f34cf356fd9d60f451b26c1714a14b3b216c56fdd40ffe44efae360f0f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5d4bd3b0a59a1290490a1f20d5a195e2a1a773720da144dac9e2aa48c1016dc",
      "signature": {
        "s": "0x7c55eb49eed47bf3b2be9bcb108b291a712c2740882cf548a12cec4636581949",
        "r": "0xb9ae397138ed3d04b7af24afee26dc68cb4ef8b33600d5dc7f0ff17cfd43efb8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10852516197",
    "total": "253275455910"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10852516197",
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
            "amount": "27679055199808705819243"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10852516"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1OTcxNDg0My1kNTUwLTVlOGQtYjMxMy1mOGJjOTU5ODA2YWIifQ==",
    "nonce": 111388,
    "balances": {
      "current": "293563188545321980850512",
      "previous": "293563188545332844219225"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf5e4e85aef766aab9cf574aec331a81274bb977f",
    "nonce": 34,
    "balances": {
      "current": "84392077752940521147",
      "previous": "84392077742088004950"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:03.297Z",
  "updated": "2022-05-04T08:58:03.390Z",
  "id": "6272401b7832e20011830cf3"
}
```
* *stageAmount*: `84392077752940521147`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000286dc41650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000286dc41650000000000000000000000000000000000000000000000000000003af864c1a6021bb2089bb8e50252488b51d3d20e0110534e4e1eb446d61ff1f966949e554586ed94f34cf356fd9d60f451b26c1714a14b3b216c56fdd40ffe44efae360f0f391fb10f75f05e476022f4645b05fa983261fee44a4dc936a38f7f75ac4455e0000000000000000000000000000000000000000000000000000000000000001be5d4bd3b0a59a1290490a1f20d5a195e2a1a773720da144dac9e2aa48c1016dcb9ae397138ed3d04b7af24afee26dc68cb4ef8b33600d5dc7f0ff17cfd43efb87c55eb49eed47bf3b2be9bcb108b291a712c2740882cf548a12cec4636581949000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d90000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b31c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003e2a17a389899ac6f150000000000000000000000000000000000000000000003e2a17a3898c2248cb5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000000a598a40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dc7c0e064e72b0726b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314f5463784e4467304d79316b4e5455774c54566c4f475174596a4d784d79316d4f474a6a4f5455354f4441325957496966513d3d0000000000000000000000000000000000000000000000000000000000000022000000000000000000000000f5e4e85aef766aab9cf574aec331a81274bb977f000000000000000000000000000000000000000000000004932ce396812a66bb000000000000000000000000000000000000000000000004932ce393fa4e255600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x021bb2089bb8e50252488b51d3d20e0110534e4e1eb446d61ff1f966949e5545",
      "signature": {
        "s": "0x391fb10f75f05e476022f4645b05fa983261fee44a4dc936a38f7f75ac4455e0",
        "r": "0x86ed94f34cf356fd9d60f451b26c1714a14b3b216c56fdd40ffe44efae360f0f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe5d4bd3b0a59a1290490a1f20d5a195e2a1a773720da144dac9e2aa48c1016dc",
      "signature": {
        "s": "0x7c55eb49eed47bf3b2be9bcb108b291a712c2740882cf548a12cec4636581949",
        "r": "0xb9ae397138ed3d04b7af24afee26dc68cb4ef8b33600d5dc7f0ff17cfd43efb8",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "10852516197",
    "total": "253275455910"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "10852516197",
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
            "amount": "27679055199808705819243"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "10852516"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1OTcxNDg0My1kNTUwLTVlOGQtYjMxMy1mOGJjOTU5ODA2YWIifQ==",
    "nonce": 111388,
    "balances": {
      "current": "293563188545321980850512",
      "previous": "293563188545332844219225"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xf5e4e85aef766aab9cf574aec331a81274bb977f",
    "nonce": 34,
    "balances": {
      "current": "84392077752940521147",
      "previous": "84392077742088004950"
    }
  },
  "blockNumber": "14709977",
  "created": "2022-05-04T08:58:03.297Z",
  "updated": "2022-05-04T08:58:03.390Z",
  "id": "6272401b7832e20011830cf3"
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
0x0f200f9b000000000000000000000000000000000000000000000004932ce396812a66bb0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `84392077752940521147`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`