# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBD370F37Cf880615eA5906e2299A9fE26258ed26`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000168cca4b1aa3b231600000000000000000000000000000000000000000000000003d240a3114df99f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000003d240a3114df99f00000000000000000000000000000000000000000000000168cca4b1aa3b23165571bbcb23b7594ef006c8e6c4c96d6d4e1ba12baf9bbae9016c1f7a4a413369c3550f0ff30426c79c0174962608dc2fd1ea18e5072bd8004e7975fe925542450aa75f0f09ff2dac1c954d8a64a5eb57e9771019be5819d0b3046b4194b42b0f000000000000000000000000000000000000000000000000000000000000001ba7068b63b56cbc6f0ca72bfaf8b93ee665e2933cea628919fec6ee83ff9da4aa96cdd4a942d0a1d6dfd7d262b514a71abb65c0c0052dc7b3e4a23f0984947967303a3f7733816848b61eaca5dd43da7da6f79239926bd66e2d6db1971c0e994f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd382d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011b6f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049a4af752737e513f5240000000000000000000000000000000000000000000049a4b3486249b7ae0aea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000fa6ec14c1c270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000034fad709c5f1e14aa550000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d7a45325a4467775a69316b595749324c5455345a47457459544d34595330314e6a46694e574e6b4d7a63314d6d596966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000bd370f37cf880615ea5906e2299a9fe26258ed2600000000000000000000000000000000000000000000000168cca4b1aa3b231600000000000000000000000000000000000000000000000164fa640e98ed297700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5571bbcb23b7594ef006c8e6c4c96d6d4e1ba12baf9bbae9016c1f7a4a413369",
      "signature": {
        "s": "0x0aa75f0f09ff2dac1c954d8a64a5eb57e9771019be5819d0b3046b4194b42b0f",
        "r": "0xc3550f0ff30426c79c0174962608dc2fd1ea18e5072bd8004e7975fe92554245",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa7068b63b56cbc6f0ca72bfaf8b93ee665e2933cea628919fec6ee83ff9da4aa",
      "signature": {
        "s": "0x303a3f7733816848b61eaca5dd43da7da6f79239926bd66e2d6db1971c0e994f",
        "r": "0x96cdd4a942d0a1d6dfd7d262b514a71abb65c0c0052dc7b3e4a23f0984947967",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "275353596337191327",
    "total": "25998335831875199766"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "275353596337191327",
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
            "amount": "15636889891330283842133"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "275353596337191"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMzE2ZDgwZi1kYWI2LTU4ZGEtYTM4YS01NjFiNWNkMzc1MmYifQ==",
    "nonce": 72559,
    "balances": {
      "current": "347770662332222399575332",
      "previous": "347770937961172333103850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd370f37cf880615ea5906e2299a9fe26258ed26",
    "nonce": 4,
    "balances": {
      "current": "25998335831875199766",
      "previous": "25722982235538008439"
    }
  },
  "blockNumber": "12400685",
  "created": "2021-05-09T14:30:43.678Z",
  "updated": "2021-05-09T14:30:43.766Z",
  "id": "6097f21310d28200105e277b"
}
```
* *stageAmount*: `25998335831875199766`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000003d240a3114df99f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000003d240a3114df99f00000000000000000000000000000000000000000000000168cca4b1aa3b23165571bbcb23b7594ef006c8e6c4c96d6d4e1ba12baf9bbae9016c1f7a4a413369c3550f0ff30426c79c0174962608dc2fd1ea18e5072bd8004e7975fe925542450aa75f0f09ff2dac1c954d8a64a5eb57e9771019be5819d0b3046b4194b42b0f000000000000000000000000000000000000000000000000000000000000001ba7068b63b56cbc6f0ca72bfaf8b93ee665e2933cea628919fec6ee83ff9da4aa96cdd4a942d0a1d6dfd7d262b514a71abb65c0c0052dc7b3e4a23f0984947967303a3f7733816848b61eaca5dd43da7da6f79239926bd66e2d6db1971c0e994f000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd382d00000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011b6f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049a4af752737e513f5240000000000000000000000000000000000000000000049a4b3486249b7ae0aea00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000fa6ec14c1c270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000034fad709c5f1e14aa550000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c4d7a45325a4467775a69316b595749324c5455345a47457459544d34595330314e6a46694e574e6b4d7a63314d6d596966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000bd370f37cf880615ea5906e2299a9fe26258ed2600000000000000000000000000000000000000000000000168cca4b1aa3b231600000000000000000000000000000000000000000000000164fa640e98ed297700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5571bbcb23b7594ef006c8e6c4c96d6d4e1ba12baf9bbae9016c1f7a4a413369",
      "signature": {
        "s": "0x0aa75f0f09ff2dac1c954d8a64a5eb57e9771019be5819d0b3046b4194b42b0f",
        "r": "0xc3550f0ff30426c79c0174962608dc2fd1ea18e5072bd8004e7975fe92554245",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa7068b63b56cbc6f0ca72bfaf8b93ee665e2933cea628919fec6ee83ff9da4aa",
      "signature": {
        "s": "0x303a3f7733816848b61eaca5dd43da7da6f79239926bd66e2d6db1971c0e994f",
        "r": "0x96cdd4a942d0a1d6dfd7d262b514a71abb65c0c0052dc7b3e4a23f0984947967",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "275353596337191327",
    "total": "25998335831875199766"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "275353596337191327",
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
            "amount": "15636889891330283842133"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "275353596337191"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlMzE2ZDgwZi1kYWI2LTU4ZGEtYTM4YS01NjFiNWNkMzc1MmYifQ==",
    "nonce": 72559,
    "balances": {
      "current": "347770662332222399575332",
      "previous": "347770937961172333103850"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xbd370f37cf880615ea5906e2299a9fe26258ed26",
    "nonce": 4,
    "balances": {
      "current": "25998335831875199766",
      "previous": "25722982235538008439"
    }
  },
  "blockNumber": "12400685",
  "created": "2021-05-09T14:30:43.678Z",
  "updated": "2021-05-09T14:30:43.766Z",
  "id": "6097f21310d28200105e277b"
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
0x0f200f9b00000000000000000000000000000000000000000000000168cca4b1aa3b23160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `25998335831875199766`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`