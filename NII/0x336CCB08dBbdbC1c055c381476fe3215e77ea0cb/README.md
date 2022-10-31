# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0x336CCB08dBbdbC1c055c381476fe3215e77ea0cb`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000163a2185c3bbf000000000000000000000000000000000000000000000000000000097e691b960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000097e691b9600000000000000000000000000000000000000000000001106ec97b7e42912b9bb572b1ebb82d3633b4ed8dea663de86b85c0e201abb59c8cb2fa1f82ef0876f6f4b06d9e2c400bc9c00ba4b7c1d0fac195345fcf34cb90aa8c77c300a5204a11227f952af2b48554a0553d9e12892f75bd5e20489f8c430b089e7de4dcfea7a000000000000000000000000000000000000000000000000000000000000001c293ee285641594b8905482d8042ce29d525c45b6e6fc2fa062799a5951dc26e73b3f937f509fd4e30a79092bd1ff9988d84fcd72952bb7251add3d5a902cf10838849ad433a3268773d4f656a68ab056e4ae13c5e126c4bbf87c85a88e777efe000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac34000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a91dcd23b8e0b060345000000000000000000000000000000000000000000009a91dcd23b978bdd4e3e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000026e2f630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4da3a38c415ff6c3e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596d45334e47566c4e4330324f544d7a4c5455314d6a6b744f5751324f43316c4e54566c4e6a677a59575a684e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000336ccb08dbbdbc1c055c381476fe3215e77ea0cb000000000000000000000000000000000000000000000000000163a2185c3bbf0000000000000000000000000000000000000000000000000001639899f3202900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xbb572b1ebb82d3633b4ed8dea663de86b85c0e201abb59c8cb2fa1f82ef0876f",
      "signature": {
        "s": "0x1227f952af2b48554a0553d9e12892f75bd5e20489f8c430b089e7de4dcfea7a",
        "r": "0x6f4b06d9e2c400bc9c00ba4b7c1d0fac195345fcf34cb90aa8c77c300a5204a1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x293ee285641594b8905482d8042ce29d525c45b6e6fc2fa062799a5951dc26e7",
      "signature": {
        "s": "0x38849ad433a3268773d4f656a68ab056e4ae13c5e126c4bbf87c85a88e777efe",
        "r": "0x3b3f937f509fd4e30a79092bd1ff9988d84fcd72952bb7251add3d5a902cf108",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "40775523222",
    "total": "314093589727856366265"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "40775523222",
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
            "amount": "27243119196259049499710"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "40775523"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YmE3NGVlNC02OTMzLTU1MjktOWQ2OC1lNTVlNjgzYWZhNzkifQ==",
    "nonce": 109620,
    "balances": {
      "current": "729935128098527957615429",
      "previous": "729935128098568773914174"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x336ccb08dbbdbc1c055c381476fe3215e77ea0cb",
    "nonce": 46,
    "balances": {
      "current": "391022821260223",
      "previous": "390982045737001"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:01.664Z",
  "updated": "2022-05-04T08:49:01.815Z",
  "id": "62723dfd3592fd001130b3cd"
}
```
* *stageAmount*: `391022821260223`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000097e691b960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000097e691b9600000000000000000000000000000000000000000000001106ec97b7e42912b9bb572b1ebb82d3633b4ed8dea663de86b85c0e201abb59c8cb2fa1f82ef0876f6f4b06d9e2c400bc9c00ba4b7c1d0fac195345fcf34cb90aa8c77c300a5204a11227f952af2b48554a0553d9e12892f75bd5e20489f8c430b089e7de4dcfea7a000000000000000000000000000000000000000000000000000000000000001c293ee285641594b8905482d8042ce29d525c45b6e6fc2fa062799a5951dc26e73b3f937f509fd4e30a79092bd1ff9988d84fcd72952bb7251add3d5a902cf10838849ad433a3268773d4f656a68ab056e4ae13c5e126c4bbf87c85a88e777efe000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074b80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ac34000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009a91dcd23b8e0b060345000000000000000000000000000000000000000000009a91dcd23b978bdd4e3e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000026e2f630000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c4da3a38c415ff6c3e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596d45334e47566c4e4330324f544d7a4c5455314d6a6b744f5751324f43316c4e54566c4e6a677a59575a684e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000336ccb08dbbdbc1c055c381476fe3215e77ea0cb000000000000000000000000000000000000000000000000000163a2185c3bbf0000000000000000000000000000000000000000000000000001639899f3202900000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xbb572b1ebb82d3633b4ed8dea663de86b85c0e201abb59c8cb2fa1f82ef0876f",
      "signature": {
        "s": "0x1227f952af2b48554a0553d9e12892f75bd5e20489f8c430b089e7de4dcfea7a",
        "r": "0x6f4b06d9e2c400bc9c00ba4b7c1d0fac195345fcf34cb90aa8c77c300a5204a1",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x293ee285641594b8905482d8042ce29d525c45b6e6fc2fa062799a5951dc26e7",
      "signature": {
        "s": "0x38849ad433a3268773d4f656a68ab056e4ae13c5e126c4bbf87c85a88e777efe",
        "r": "0x3b3f937f509fd4e30a79092bd1ff9988d84fcd72952bb7251add3d5a902cf108",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "40775523222",
    "total": "314093589727856366265"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "40775523222",
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
            "amount": "27243119196259049499710"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "40775523"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YmE3NGVlNC02OTMzLTU1MjktOWQ2OC1lNTVlNjgzYWZhNzkifQ==",
    "nonce": 109620,
    "balances": {
      "current": "729935128098527957615429",
      "previous": "729935128098568773914174"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x336ccb08dbbdbc1c055c381476fe3215e77ea0cb",
    "nonce": 46,
    "balances": {
      "current": "391022821260223",
      "previous": "390982045737001"
    }
  },
  "blockNumber": "14709944",
  "created": "2022-05-04T08:49:01.664Z",
  "updated": "2022-05-04T08:49:01.815Z",
  "id": "62723dfd3592fd001130b3cd"
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
0x0f200f9b000000000000000000000000000000000000000000000000000163a2185c3bbf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `391022821260223`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`