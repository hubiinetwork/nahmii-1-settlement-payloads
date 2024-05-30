# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xc9FfCd9Fa0924B86d7f174901e32e2718C8f9a16`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000a294651b27ddd00000000000000000000000000000000000000000000000000000000000453b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000453b7000000000000000000000000000000000000000000000000000000000064fbc371f682ed0b14f1d64ba58223ee2d82f8173538d55327d82d21e656ccb3fe4b21b76636548f4c34eff2f0b59cb298784ed42848563f5a4c4f4f166b7aa7a9e9705033e92ca888bcc5ec4334738995bb0ce8b2718c4c3b430ff83ec0c7b6188bc0000000000000000000000000000000000000000000000000000000000000001c8cfe18d59267bdf8955009a85d3be57d29a142c354ed32041a0df9903570e03a65ca75e5cf900e4f1c878c7b16e97519e36644c0ecbf55b237d838a4b9aa3fe4168faaa0dae52e9e07da3866fd41299c30370f8e26405261954dcbe50c5b00ff000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b396000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa082944227af723f000000000000000000000000000000000000000000003bcfa082944227b3c71100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000011b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd1621bff74f82f26f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a67774e4464685a693033595749774c5455794f574d7459546b324d533034596a4e6b596a63775a6d466c4e44556966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000c9ffcd9fa0924b86d7f174901e32e2718c8f9a16000000000000000000000000000000000000000000000000000a294651b27ddd000000000000000000000000000000000000000000000000000a294651ae2a2600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x71f682ed0b14f1d64ba58223ee2d82f8173538d55327d82d21e656ccb3fe4b21",
      "signature": {
        "s": "0x5033e92ca888bcc5ec4334738995bb0ce8b2718c4c3b430ff83ec0c7b6188bc0",
        "r": "0xb76636548f4c34eff2f0b59cb298784ed42848563f5a4c4f4f166b7aa7a9e970",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8cfe18d59267bdf8955009a85d3be57d29a142c354ed32041a0df9903570e03a",
      "signature": {
        "s": "0x168faaa0dae52e9e07da3866fd41299c30370f8e26405261954dcbe50c5b00ff",
        "r": "0x65ca75e5cf900e4f1c878c7b16e97519e36644c0ecbf55b237d838a4b9aa3fe4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "283575",
    "total": "6618051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "283575",
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
            "amount": "27690157621450014650991"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "283"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZjgwNDdhZi03YWIwLTUyOWMtYTk2MS04YjNkYjcwZmFlNDUifQ==",
    "nonce": 111510,
    "balances": {
      "current": "282449664482371840209471",
      "previous": "282449664482371840493329"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc9ffcd9fa0924b86d7f174901e32e2718c8f9a16",
    "nonce": 31,
    "balances": {
      "current": "2860131762208221",
      "previous": "2860131761924646"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:41.044Z",
  "updated": "2022-05-04T08:58:41.124Z",
  "id": "627240417832e20011830d19"
}
```
* *stageAmount*: `2860131762208221`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000000453b70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000000453b7000000000000000000000000000000000000000000000000000000000064fbc371f682ed0b14f1d64ba58223ee2d82f8173538d55327d82d21e656ccb3fe4b21b76636548f4c34eff2f0b59cb298784ed42848563f5a4c4f4f166b7aa7a9e9705033e92ca888bcc5ec4334738995bb0ce8b2718c4c3b430ff83ec0c7b6188bc0000000000000000000000000000000000000000000000000000000000000001c8cfe18d59267bdf8955009a85d3be57d29a142c354ed32041a0df9903570e03a65ca75e5cf900e4f1c878c7b16e97519e36644c0ecbf55b237d838a4b9aa3fe4168faaa0dae52e9e07da3866fd41299c30370f8e26405261954dcbe50c5b00ff000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074db0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b396000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003bcfa082944227af723f000000000000000000000000000000000000000000003bcfa082944227b3c71100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000000011b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd1621bff74f82f26f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a5a6a67774e4464685a693033595749774c5455794f574d7459546b324d533034596a4e6b596a63775a6d466c4e44556966513d3d000000000000000000000000000000000000000000000000000000000000001f000000000000000000000000c9ffcd9fa0924b86d7f174901e32e2718c8f9a16000000000000000000000000000000000000000000000000000a294651b27ddd000000000000000000000000000000000000000000000000000a294651ae2a2600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x71f682ed0b14f1d64ba58223ee2d82f8173538d55327d82d21e656ccb3fe4b21",
      "signature": {
        "s": "0x5033e92ca888bcc5ec4334738995bb0ce8b2718c4c3b430ff83ec0c7b6188bc0",
        "r": "0xb76636548f4c34eff2f0b59cb298784ed42848563f5a4c4f4f166b7aa7a9e970",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8cfe18d59267bdf8955009a85d3be57d29a142c354ed32041a0df9903570e03a",
      "signature": {
        "s": "0x168faaa0dae52e9e07da3866fd41299c30370f8e26405261954dcbe50c5b00ff",
        "r": "0x65ca75e5cf900e4f1c878c7b16e97519e36644c0ecbf55b237d838a4b9aa3fe4",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "283575",
    "total": "6618051"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "283575",
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
            "amount": "27690157621450014650991"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "283"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjZjgwNDdhZi03YWIwLTUyOWMtYTk2MS04YjNkYjcwZmFlNDUifQ==",
    "nonce": 111510,
    "balances": {
      "current": "282449664482371840209471",
      "previous": "282449664482371840493329"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc9ffcd9fa0924b86d7f174901e32e2718c8f9a16",
    "nonce": 31,
    "balances": {
      "current": "2860131762208221",
      "previous": "2860131761924646"
    }
  },
  "blockNumber": "14709979",
  "created": "2022-05-04T08:58:41.044Z",
  "updated": "2022-05-04T08:58:41.124Z",
  "id": "627240417832e20011830d19"
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
0x0f200f9b000000000000000000000000000000000000000000000000000a294651b27ddd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2860131762208221`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`