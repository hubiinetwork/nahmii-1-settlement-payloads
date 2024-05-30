# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x3A57F30A4bd6F8dA2a73E67f33252fA7a553Fded`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de21297ba0502140000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000000000000000000000000004806c704a55f8e9800001c02ef360d23d29257cb1b0cee9dd42b181098259a86047ff6c98d315dd77da1d9901d94293d60da4ace2958d73c39b0f27479c28f99a9a4178976734cc8f4b66e796b45b69aa8140b158ad8b6441d75a114cd3fc02e1d58d300cccb3a04a31000000000000000000000000000000000000000000000000000000000000001c6562ca40063c276deaf184bfd697f943dd74f521dc01f9c00b4204b29e2222c79ea69b5bb5929467a0d35a5ac6b11388b0a387bc7bfa712f922482aab44697190a40f39f80f29fd76ff238a5bae0a5d1031bb0fc199ab2219753d5e13c353dd3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000003a57f30a4bd6f8da2a73e67f33252fa7a553fded0000000000000000000000000000000000000000000000000de21297ba050214000000000000000000000000000000000000000000000481a157986514b7721400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6a6b784e5446694f5330304d7a67324c54526c5a544d74595749794f4330774d325a684e7a55304d6a45775957496966513d3d00000000000000000000000000000000000000000000000000000000000000eb000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000e55544fc8dc938ff0a5f00000000000000000000000000000000000000000000e0d4d88c437340158a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x01c02ef360d23d29257cb1b0cee9dd42b181098259a86047ff6c98d315dd77da",
      "signature": {
        "s": "0x66e796b45b69aa8140b158ad8b6441d75a114cd3fc02e1d58d300cccb3a04a31",
        "r": "0x1d9901d94293d60da4ace2958d73c39b0f27479c28f99a9a4178976734cc8f4b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6562ca40063c276deaf184bfd697f943dd74f521dc01f9c00b4204b29e2222c7",
      "signature": {
        "s": "0x0a40f39f80f29fd76ff238a5bae0a5d1031bb0fc199ab2219753d5e13c353dd3",
        "r": "0x9ea69b5bb5929467a0d35a5ac6b11388b0a387bc7bfa712f922482aab4469719",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258463000000000000000",
    "total": "21258463000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258463000000000000000",
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
            "amount": "21258463000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258463000000000000"
      }
    },
    "wallet": "0x3a57f30a4bd6f8da2a73e67f33252fa7a553fded",
    "data": "eyJyZWYiOiJiZjkxNTFiOS00Mzg2LTRlZTMtYWIyOC0wM2ZhNzU0MjEwYWIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000382510099923476",
      "previous": "21280721845510099923476"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 235,
    "balances": {
      "current": "1082994868827398160190047",
      "previous": "1061736405827398160190047"
    }
  },
  "blockNumber": "14877915",
  "created": "2022-05-31T09:23:30.149Z",
  "updated": "2022-05-31T09:23:30.259Z",
  "id": "6295de92bbd75600116d0913"
}
```
* *stageAmount*: `1000382510099923476`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000004806c704a55f8e980000000000000000000000000000000000000000000000004806c704a55f8e9800001c02ef360d23d29257cb1b0cee9dd42b181098259a86047ff6c98d315dd77da1d9901d94293d60da4ace2958d73c39b0f27479c28f99a9a4178976734cc8f4b66e796b45b69aa8140b158ad8b6441d75a114cd3fc02e1d58d300cccb3a04a31000000000000000000000000000000000000000000000000000000000000001c6562ca40063c276deaf184bfd697f943dd74f521dc01f9c00b4204b29e2222c79ea69b5bb5929467a0d35a5ac6b11388b0a387bc7bfa712f922482aab44697190a40f39f80f29fd76ff238a5bae0a5d1031bb0fc199ab2219753d5e13c353dd3000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e304db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002f0000000000000000000000003a57f30a4bd6f8da2a73e67f33252fa7a553fded0000000000000000000000000000000000000000000000000de21297ba050214000000000000000000000000000000000000000000000481a157986514b7721400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000127053b7761c8f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a6a6b784e5446694f5330304d7a67324c54526c5a544d74595749794f4330774d325a684e7a55304d6a45775957496966513d3d00000000000000000000000000000000000000000000000000000000000000eb000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b100000000000000000000000000000000000000000000e55544fc8dc938ff0a5f00000000000000000000000000000000000000000000e0d4d88c437340158a5f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x01c02ef360d23d29257cb1b0cee9dd42b181098259a86047ff6c98d315dd77da",
      "signature": {
        "s": "0x66e796b45b69aa8140b158ad8b6441d75a114cd3fc02e1d58d300cccb3a04a31",
        "r": "0x1d9901d94293d60da4ace2958d73c39b0f27479c28f99a9a4178976734cc8f4b",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6562ca40063c276deaf184bfd697f943dd74f521dc01f9c00b4204b29e2222c7",
      "signature": {
        "s": "0x0a40f39f80f29fd76ff238a5bae0a5d1031bb0fc199ab2219753d5e13c353dd3",
        "r": "0x9ea69b5bb5929467a0d35a5ac6b11388b0a387bc7bfa712f922482aab4469719",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "21258463000000000000000",
    "total": "21258463000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "21258463000000000000000",
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
            "amount": "21258463000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "21258463000000000000"
      }
    },
    "wallet": "0x3a57f30a4bd6f8da2a73e67f33252fa7a553fded",
    "data": "eyJyZWYiOiJiZjkxNTFiOS00Mzg2LTRlZTMtYWIyOC0wM2ZhNzU0MjEwYWIifQ==",
    "nonce": 47,
    "balances": {
      "current": "1000382510099923476",
      "previous": "21280721845510099923476"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 235,
    "balances": {
      "current": "1082994868827398160190047",
      "previous": "1061736405827398160190047"
    }
  },
  "blockNumber": "14877915",
  "created": "2022-05-31T09:23:30.149Z",
  "updated": "2022-05-31T09:23:30.259Z",
  "id": "6295de92bbd75600116d0913"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de21297ba0502140000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000382510099923476`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`