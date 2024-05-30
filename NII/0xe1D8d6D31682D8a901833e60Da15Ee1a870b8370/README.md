# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe1D8d6D31682D8a901833e60Da15Ee1a870b8370`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000244716119f1f588fee000000000000000000000000000000000000000000000000dc2fb26d57f353b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f353b400000000000000000000000000000000000000000000001822a46216080dc4a40e4461a996f0836264d2490faf42cec3b5567032f95cbf014ace462ba02a0620f0ac52b99e34825846bd9518f769cfcb68704da9b4c8d0a677c5e2706d4d3fc64beebea3e27dcdd9ee1dfab66e00cf90747311a364adb3d1f864131c9722164e000000000000000000000000000000000000000000000000000000000000001c2ee594dda57b5c4015da5409e1ae89e6a7545d15a8829b69d7e20f44371d76917aeba9ec6abd307a761197519cc81131598bb55dd40aae29dc21c6a212541d78774d44719d5a69f781c9be94a3ef7ebbeebde279bc874e38d6255a901b88542f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6a4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030307040ae9f8ae57cb70000000000000000000000000000000000000000000030314ca8bf2e4684d55d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04f20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e00f04eaa6257866cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a6c6a4d475977596930334f54417a4c5455784f475574596d56684e5330304e7a6c6a4e7a55324e6d45335a6a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e1d8d6d31682d8a901833e60da15ee1a870b83700000000000000000000000000000000000000000000000244716119f1f588fee0000000000000000000000000000000000000000000000236ae65f31c7653c3a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0e4461a996f0836264d2490faf42cec3b5567032f95cbf014ace462ba02a0620",
      "signature": {
        "s": "0x4beebea3e27dcdd9ee1dfab66e00cf90747311a364adb3d1f864131c9722164e",
        "r": "0xf0ac52b99e34825846bd9518f769cfcb68704da9b4c8d0a677c5e2706d4d3fc6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2ee594dda57b5c4015da5409e1ae89e6a7545d15a8829b69d7e20f44371d7691",
      "signature": {
        "s": "0x774d44719d5a69f781c9be94a3ef7ebbeebde279bc874e38d6255a901b88542f",
        "r": "0x7aeba9ec6abd307a761197519cc81131598bb55dd40aae29dc21c6a212541d78",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946290612",
    "total": "445218085709263258788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946290612",
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
            "amount": "27744985334668955510477"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946290"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YzljMGYwYi03OTAzLTUxOGUtYmVhNS00NzljNzU2NmE3ZjYifQ==",
    "nonce": 112292,
    "balances": {
      "current": "227567123550212039474359",
      "previous": "227583005512503180711261"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1d8d6d31682d8a901833e60da15ee1a870b8370",
    "nonce": 46,
    "balances": {
      "current": "669205087654847746030",
      "previous": "653338991459901455418"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:59.724Z",
  "updated": "2022-05-04T09:02:59.814Z",
  "id": "627241437832e20011830e1e"
}
```
* *stageAmount*: `669205087654847746030`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f353b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f353b400000000000000000000000000000000000000000000001822a46216080dc4a40e4461a996f0836264d2490faf42cec3b5567032f95cbf014ace462ba02a0620f0ac52b99e34825846bd9518f769cfcb68704da9b4c8d0a677c5e2706d4d3fc64beebea3e27dcdd9ee1dfab66e00cf90747311a364adb3d1f864131c9722164e000000000000000000000000000000000000000000000000000000000000001c2ee594dda57b5c4015da5409e1ae89e6a7545d15a8829b69d7e20f44371d76917aeba9ec6abd307a761197519cc81131598bb55dd40aae29dc21c6a212541d78774d44719d5a69f781c9be94a3ef7ebbeebde279bc874e38d6255a901b88542f000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6a4000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030307040ae9f8ae57cb70000000000000000000000000000000000000000000030314ca8bf2e4684d55d00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac04f20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e00f04eaa6257866cd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694930597a6c6a4d475977596930334f54417a4c5455784f475574596d56684e5330304e7a6c6a4e7a55324e6d45335a6a596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e1d8d6d31682d8a901833e60da15ee1a870b83700000000000000000000000000000000000000000000000244716119f1f588fee0000000000000000000000000000000000000000000000236ae65f31c7653c3a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0e4461a996f0836264d2490faf42cec3b5567032f95cbf014ace462ba02a0620",
      "signature": {
        "s": "0x4beebea3e27dcdd9ee1dfab66e00cf90747311a364adb3d1f864131c9722164e",
        "r": "0xf0ac52b99e34825846bd9518f769cfcb68704da9b4c8d0a677c5e2706d4d3fc6",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2ee594dda57b5c4015da5409e1ae89e6a7545d15a8829b69d7e20f44371d7691",
      "signature": {
        "s": "0x774d44719d5a69f781c9be94a3ef7ebbeebde279bc874e38d6255a901b88542f",
        "r": "0x7aeba9ec6abd307a761197519cc81131598bb55dd40aae29dc21c6a212541d78",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946290612",
    "total": "445218085709263258788"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946290612",
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
            "amount": "27744985334668955510477"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946290"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0YzljMGYwYi03OTAzLTUxOGUtYmVhNS00NzljNzU2NmE3ZjYifQ==",
    "nonce": 112292,
    "balances": {
      "current": "227567123550212039474359",
      "previous": "227583005512503180711261"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe1d8d6d31682d8a901833e60da15ee1a870b8370",
    "nonce": 46,
    "balances": {
      "current": "669205087654847746030",
      "previous": "653338991459901455418"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:02:59.724Z",
  "updated": "2022-05-04T09:02:59.814Z",
  "id": "627241437832e20011830e1e"
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
0x0f200f9b0000000000000000000000000000000000000000000000244716119f1f588fee0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205087654847746030`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`