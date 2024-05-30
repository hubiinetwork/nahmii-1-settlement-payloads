# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd80681ee57c2ca6a78e01ffbDdEFF5c42b6fBFad`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000007149b3e65f6225565600000000000000000000000000000000000000000000000000000015e0d68a0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000015e0d68a0b00000000000000000000000000000000000000000000003aea8ff68b9dfbc6ad3219d7aa7ee9f6591da52759b636ce868be8a0c865af41aef53a3e684e9eb4c383bb079e936d051f36d714e147852afe2118d5b9ebba1e2dbed4899d893f69d83678ddeab5872fb01d4bc095aaf2623d3d1271e07ed7b98283a88700b1604d03000000000000000000000000000000000000000000000000000000000000001c1d29b7cfcdff29617c7d682e1d316041377ea185847db86680c0a3e61e8fc5f37805700790655763b1196bf5279bf947085312891068489e13eda6ae18a847525e1803d5aff2dfd211287fc14e4b9ccdc73db9be45b56a074106c417d0d6c960000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1f3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c931dd8eeecdfc4aa40000000000000000000000000000000000000000000049c931dd8f04b46ca53400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000599d0850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d983307dfd46a66bff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e6a41334f444a685a4330774f5463314c5456684d544d74596a42694e53307a4d5467795932566a597a566a4d444d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d80681ee57c2ca6a78e01ffbddeff5c42b6fbfad00000000000000000000000000000000000000000000007149b3e65f6225565600000000000000000000000000000000000000000000007149b3e649814ecc4b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3219d7aa7ee9f6591da52759b636ce868be8a0c865af41aef53a3e684e9eb4c3",
      "signature": {
        "s": "0x3678ddeab5872fb01d4bc095aaf2623d3d1271e07ed7b98283a88700b1604d03",
        "r": "0x83bb079e936d051f36d714e147852afe2118d5b9ebba1e2dbed4899d893f69d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1d29b7cfcdff29617c7d682e1d316041377ea185847db86680c0a3e61e8fc5f3",
      "signature": {
        "s": "0x5e1803d5aff2dfd211287fc14e4b9ccdc73db9be45b56a074106c417d0d6c960",
        "r": "0x7805700790655763b1196bf5279bf947085312891068489e13eda6ae18a84752",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93966469643",
    "total": "1086813155281210164909"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93966469643",
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
            "amount": "27624229072487814949887"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "93966469"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNjA3ODJhZC0wOTc1LTVhMTMtYjBiNS0zMTgyY2VjYzVjMDMifQ==",
    "nonce": 111091,
    "balances": {
      "current": "348444141993533741222564",
      "previous": "348444141993627801658676"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd80681ee57c2ca6a78e01ffbddeff5c42b6fbfad",
    "nonce": 46,
    "balances": {
      "current": "2089792922012122175062",
      "previous": "2089792921918155705419"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:31.389Z",
  "updated": "2022-05-04T08:56:31.457Z",
  "id": "62723fbf7832e20011830c8c"
}
```
* *stageAmount*: `2089792922012122175062`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000015e0d68a0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000015e0d68a0b00000000000000000000000000000000000000000000003aea8ff68b9dfbc6ad3219d7aa7ee9f6591da52759b636ce868be8a0c865af41aef53a3e684e9eb4c383bb079e936d051f36d714e147852afe2118d5b9ebba1e2dbed4899d893f69d83678ddeab5872fb01d4bc095aaf2623d3d1271e07ed7b98283a88700b1604d03000000000000000000000000000000000000000000000000000000000000001c1d29b7cfcdff29617c7d682e1d316041377ea185847db86680c0a3e61e8fc5f37805700790655763b1196bf5279bf947085312891068489e13eda6ae18a847525e1803d5aff2dfd211287fc14e4b9ccdc73db9be45b56a074106c417d0d6c960000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1f3000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c931dd8eeecdfc4aa40000000000000000000000000000000000000000000049c931dd8f04b46ca53400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000599d0850000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d983307dfd46a66bff0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6a4e6a41334f444a685a4330774f5463314c5456684d544d74596a42694e53307a4d5467795932566a597a566a4d444d6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d80681ee57c2ca6a78e01ffbddeff5c42b6fbfad00000000000000000000000000000000000000000000007149b3e65f6225565600000000000000000000000000000000000000000000007149b3e649814ecc4b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3219d7aa7ee9f6591da52759b636ce868be8a0c865af41aef53a3e684e9eb4c3",
      "signature": {
        "s": "0x3678ddeab5872fb01d4bc095aaf2623d3d1271e07ed7b98283a88700b1604d03",
        "r": "0x83bb079e936d051f36d714e147852afe2118d5b9ebba1e2dbed4899d893f69d8",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x1d29b7cfcdff29617c7d682e1d316041377ea185847db86680c0a3e61e8fc5f3",
      "signature": {
        "s": "0x5e1803d5aff2dfd211287fc14e4b9ccdc73db9be45b56a074106c417d0d6c960",
        "r": "0x7805700790655763b1196bf5279bf947085312891068489e13eda6ae18a84752",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "93966469643",
    "total": "1086813155281210164909"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "93966469643",
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
            "amount": "27624229072487814949887"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "93966469"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJjNjA3ODJhZC0wOTc1LTVhMTMtYjBiNS0zMTgyY2VjYzVjMDMifQ==",
    "nonce": 111091,
    "balances": {
      "current": "348444141993533741222564",
      "previous": "348444141993627801658676"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd80681ee57c2ca6a78e01ffbddeff5c42b6fbfad",
    "nonce": 46,
    "balances": {
      "current": "2089792922012122175062",
      "previous": "2089792921918155705419"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:31.389Z",
  "updated": "2022-05-04T08:56:31.457Z",
  "id": "62723fbf7832e20011830c8c"
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
0x0f200f9b00000000000000000000000000000000000000000000007149b3e65f622556560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2089792922012122175062`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`