# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x910c4BA923B2243dc13e00A066eEfb8ffd905EB0`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000001d1957a45f29830000000000000000000000000000000000000000000000000000000000125c450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000125c450000000000000000000000000000000000000000000000000000000001ac808a6002d3383a11f34b31f210543638b857c88c8bfc852e73ab3aa9d57e7cb895a9a2e9cf671a632e8809f9fd3e7b0d51902d6dd9e653e7f89631fd7cd30ec1159c0622d4f99b50b5e7d2a94a580fa792471940364f0d183a4e14961f0ad95fb130000000000000000000000000000000000000000000000000000000000000001c7a2f0ab2b5060ad7634d18b8eb7e832e3f3c8b8ea0b9a7affd995d521d893c1a418fc706746d388fcace44b983b92754a4f1b65d8103f3f47f0fc3329ab58ed50fffc736997aa3ab014dd7a9815e47b482922a2507c877f58e4aa901d5f914a5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2da000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000045f4ba5f5e54f48eef540000000000000000000000000000000000000000000045f4ba5f5e54f4a1504c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da7df02bb031e571450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f5467354e7a6b774f4330774d44466c4c5456695957597459575a694e4330354e546868595463794e6a51355a47596966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000910c4ba923b2243dc13e00a066eefb8ffd905eb0000000000000000000000000000000000000000000000000001d1957a45f2983000000000000000000000000000000000000000000000000001d1957a44ccd3e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6002d3383a11f34b31f210543638b857c88c8bfc852e73ab3aa9d57e7cb895a9",
      "signature": {
        "s": "0x0622d4f99b50b5e7d2a94a580fa792471940364f0d183a4e14961f0ad95fb130",
        "r": "0xa2e9cf671a632e8809f9fd3e7b0d51902d6dd9e653e7f89631fd7cd30ec1159c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7a2f0ab2b5060ad7634d18b8eb7e832e3f3c8b8ea0b9a7affd995d521d893c1a",
      "signature": {
        "s": "0x0fffc736997aa3ab014dd7a9815e47b482922a2507c877f58e4aa901d5f914a5",
        "r": "0x418fc706746d388fcace44b983b92754a4f1b65d8103f3f47f0fc3329ab58ed5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1203269",
    "total": "28082314"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1203269",
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
            "amount": "27642297423701811228997"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1203"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4OTg5NzkwOC0wMDFlLTViYWYtYWZiNC05NThhYTcyNjQ5ZGYifQ==",
    "nonce": 111322,
    "balances": {
      "current": "330357722428323465719636",
      "previous": "330357722428323466924108"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x910c4ba923b2243dc13e00a066eefb8ffd905eb0",
    "nonce": 30,
    "balances": {
      "current": "8190638535158147",
      "previous": "8190638533954878"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:42.627Z",
  "updated": "2022-05-04T08:57:42.697Z",
  "id": "627240063592fd001130b609"
}
```
* *stageAmount*: `8190638535158147`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000000125c450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000000125c450000000000000000000000000000000000000000000000000000000001ac808a6002d3383a11f34b31f210543638b857c88c8bfc852e73ab3aa9d57e7cb895a9a2e9cf671a632e8809f9fd3e7b0d51902d6dd9e653e7f89631fd7cd30ec1159c0622d4f99b50b5e7d2a94a580fa792471940364f0d183a4e14961f0ad95fb130000000000000000000000000000000000000000000000000000000000000001c7a2f0ab2b5060ad7634d18b8eb7e832e3f3c8b8ea0b9a7affd995d521d893c1a418fc706746d388fcace44b983b92754a4f1b65d8103f3f47f0fc3329ab58ed50fffc736997aa3ab014dd7a9815e47b482922a2507c877f58e4aa901d5f914a5000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d80000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b2da000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000045f4ba5f5e54f48eef540000000000000000000000000000000000000000000045f4ba5f5e54f4a1504c00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000004b30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005da7df02bb031e571450000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344f5467354e7a6b774f4330774d44466c4c5456695957597459575a694e4330354e546868595463794e6a51355a47596966513d3d000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000910c4ba923b2243dc13e00a066eefb8ffd905eb0000000000000000000000000000000000000000000000000001d1957a45f2983000000000000000000000000000000000000000000000000001d1957a44ccd3e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x6002d3383a11f34b31f210543638b857c88c8bfc852e73ab3aa9d57e7cb895a9",
      "signature": {
        "s": "0x0622d4f99b50b5e7d2a94a580fa792471940364f0d183a4e14961f0ad95fb130",
        "r": "0xa2e9cf671a632e8809f9fd3e7b0d51902d6dd9e653e7f89631fd7cd30ec1159c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x7a2f0ab2b5060ad7634d18b8eb7e832e3f3c8b8ea0b9a7affd995d521d893c1a",
      "signature": {
        "s": "0x0fffc736997aa3ab014dd7a9815e47b482922a2507c877f58e4aa901d5f914a5",
        "r": "0x418fc706746d388fcace44b983b92754a4f1b65d8103f3f47f0fc3329ab58ed5",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1203269",
    "total": "28082314"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1203269",
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
            "amount": "27642297423701811228997"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1203"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4OTg5NzkwOC0wMDFlLTViYWYtYWZiNC05NThhYTcyNjQ5ZGYifQ==",
    "nonce": 111322,
    "balances": {
      "current": "330357722428323465719636",
      "previous": "330357722428323466924108"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x910c4ba923b2243dc13e00a066eefb8ffd905eb0",
    "nonce": 30,
    "balances": {
      "current": "8190638535158147",
      "previous": "8190638533954878"
    }
  },
  "blockNumber": "14709976",
  "created": "2022-05-04T08:57:42.627Z",
  "updated": "2022-05-04T08:57:42.697Z",
  "id": "627240063592fd001130b609"
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
0x0f200f9b000000000000000000000000000000000000000000000000001d1957a45f29830000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `8190638535158147`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`