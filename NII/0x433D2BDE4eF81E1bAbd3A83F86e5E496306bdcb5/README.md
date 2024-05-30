# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x433D2BDE4eF81E1bAbd3A83F86e5E496306bdcb5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000001679fcfa3ef433300000000000000000000000000000000000000000000000001679fcfa3ef43330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000001679fcfa3ef433300000000000000000000000000000000000000000000000001679fcfa3ef4333295d9630ea2403aab5cb5d290e23ddf7bfdce1a8bfcb5f22a9ca847d56eb2530115c5fca5079710b69403e08341a66cf559aa0efc66549e74bb4866abe900d8e68d8fb351060060584c220498b51ada65e15fd81c5031c863506db805e030415000000000000000000000000000000000000000000000000000000000000001c0f08ebb446de45d636e4fdd2e785d6eeab4cedb9b55b1fd7240f5321953664ce3de1261fb6001b6f12efe0af92d099ff5379640d376107ceb6fc9747d06fc5d074690e2e6ac74fb2e25dbd71367ad535a7fd3f5bcf050b5bd0ae771074632678000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012de5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236d8801410850ac31ce00000000000000000000000000000000000000000000236d89693ce84a87fbfb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000005c1055ec86fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9b59679c867a43660000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d5463344e7a55334e7930794d6d4d334c54557a4e3255744f4749355979316c4e47566d4d4464694d6a637a4f44596966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000433d2bde4ef81e1babd3a83f86e5e496306bdcb500000000000000000000000000000000000000000000000001679fcfa3ef4333000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x295d9630ea2403aab5cb5d290e23ddf7bfdce1a8bfcb5f22a9ca847d56eb2530",
      "signature": {
        "s": "0x68d8fb351060060584c220498b51ada65e15fd81c5031c863506db805e030415",
        "r": "0x115c5fca5079710b69403e08341a66cf559aa0efc66549e74bb4866abe900d8e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0f08ebb446de45d636e4fdd2e785d6eeab4cedb9b55b1fd7240f5321953664ce",
      "signature": {
        "s": "0x74690e2e6ac74fb2e25dbd71367ad535a7fd3f5bcf050b5bd0ae771074632678",
        "r": "0x3de1261fb6001b6f12efe0af92d099ff5379640d376107ceb6fc9747d06fc5d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "101225230796538675",
    "total": "101225230796538675"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "101225230796538675",
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
            "amount": "16816177943420176319334"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "101225230796538"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMTc4NzU3Ny0yMmM3LTUzN2UtOGI5Yy1lNGVmMDdiMjczODYifQ==",
    "nonce": 77285,
    "balances": {
      "current": "167303322190240027521486",
      "previous": "167303423516696054856699"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x433d2bde4ef81e1babd3a83f86e5e496306bdcb5",
    "nonce": 1,
    "balances": {
      "current": "101225230796538675",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:26.845Z",
  "updated": "2021-06-04T12:46:26.913Z",
  "id": "60ba20a2010ba300120bfdcc"
}
```
* *stageAmount*: `101225230796538675`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000001679fcfa3ef43330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000001679fcfa3ef433300000000000000000000000000000000000000000000000001679fcfa3ef4333295d9630ea2403aab5cb5d290e23ddf7bfdce1a8bfcb5f22a9ca847d56eb2530115c5fca5079710b69403e08341a66cf559aa0efc66549e74bb4866abe900d8e68d8fb351060060584c220498b51ada65e15fd81c5031c863506db805e030415000000000000000000000000000000000000000000000000000000000000001c0f08ebb446de45d636e4fdd2e785d6eeab4cedb9b55b1fd7240f5321953664ce3de1261fb6001b6f12efe0af92d099ff5379640d376107ceb6fc9747d06fc5d074690e2e6ac74fb2e25dbd71367ad535a7fd3f5bcf050b5bd0ae771074632678000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012de5000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000236d8801410850ac31ce00000000000000000000000000000000000000000000236d89693ce84a87fbfb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000005c1055ec86fa0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f9b59679c867a43660000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949784d5463344e7a55334e7930794d6d4d334c54557a4e3255744f4749355979316c4e47566d4d4464694d6a637a4f44596966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000433d2bde4ef81e1babd3a83f86e5e496306bdcb500000000000000000000000000000000000000000000000001679fcfa3ef4333000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x295d9630ea2403aab5cb5d290e23ddf7bfdce1a8bfcb5f22a9ca847d56eb2530",
      "signature": {
        "s": "0x68d8fb351060060584c220498b51ada65e15fd81c5031c863506db805e030415",
        "r": "0x115c5fca5079710b69403e08341a66cf559aa0efc66549e74bb4866abe900d8e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x0f08ebb446de45d636e4fdd2e785d6eeab4cedb9b55b1fd7240f5321953664ce",
      "signature": {
        "s": "0x74690e2e6ac74fb2e25dbd71367ad535a7fd3f5bcf050b5bd0ae771074632678",
        "r": "0x3de1261fb6001b6f12efe0af92d099ff5379640d376107ceb6fc9747d06fc5d0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "101225230796538675",
    "total": "101225230796538675"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "101225230796538675",
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
            "amount": "16816177943420176319334"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "101225230796538"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIxMTc4NzU3Ny0yMmM3LTUzN2UtOGI5Yy1lNGVmMDdiMjczODYifQ==",
    "nonce": 77285,
    "balances": {
      "current": "167303322190240027521486",
      "previous": "167303423516696054856699"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x433d2bde4ef81e1babd3a83f86e5e496306bdcb5",
    "nonce": 1,
    "balances": {
      "current": "101225230796538675",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:26.845Z",
  "updated": "2021-06-04T12:46:26.913Z",
  "id": "60ba20a2010ba300120bfdcc"
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
0x0f200f9b00000000000000000000000000000000000000000000000001679fcfa3ef43330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `101225230796538675`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`