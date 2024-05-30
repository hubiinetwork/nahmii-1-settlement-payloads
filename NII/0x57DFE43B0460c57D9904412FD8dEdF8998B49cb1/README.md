# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x57DFE43B0460c57D9904412FD8dEdF8998B49cb1`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000094929c262866df200000000000000000000000000000000000000000000000000385c1f22b4efd30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000385c1f22b4efd3000000000000000000000000000000000000000000000000062d831f0050f4e92aaa38b55a3a2a735b542c7f4f25024ec61a97fb34e5dc567dd7b4b766037302bd738f0bd971605b107e70931fabfc5a0306247569ce3868fb0510a166faf09c298878f69196862629d5dd58a26a0d12f0c5c09ddc35cbbfa5331090ba99a875000000000000000000000000000000000000000000000000000000000000001c019f47948c9e893436366fcd0acf4b10bc756584a9300d524b9114a3108872542b162b4a4961f537d6e2e46e47cd68420db1b9f1157a8974cdfbaf0c565c3e0236521c156402e37665e3cc71cd7d666b197598fd41c315212416be3e326eb38e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0d7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004baba0d42691f2f34d22000000000000000000000000000000000000000000004baba10c911eaf092fe200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000e6d9960f2ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907cf5198181155910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a596a41314e475a6b5a6930775a474a6a4c545668596a6b745954566d4e53316a596a55774e5455335a4452684d7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000057dfe43b0460c57d9904412fd8dedf8998b49cb1000000000000000000000000000000000000000000000000094929c262866df20000000000000000000000000000000000000000000000000910cda33fd17e1f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2aaa38b55a3a2a735b542c7f4f25024ec61a97fb34e5dc567dd7b4b766037302",
      "signature": {
        "s": "0x298878f69196862629d5dd58a26a0d12f0c5c09ddc35cbbfa5331090ba99a875",
        "r": "0xbd738f0bd971605b107e70931fabfc5a0306247569ce3868fb0510a166faf09c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x019f47948c9e893436366fcd0acf4b10bc756584a9300d524b9114a310887254",
      "signature": {
        "s": "0x36521c156402e37665e3cc71cd7d666b197598fd41c315212416be3e326eb38e",
        "r": "0x2b162b4a4961f537d6e2e46e47cd68420db1b9f1157a8974cdfbaf0c565c3e02",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15863887491821523",
    "total": "445156107352077545"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15863887491821523",
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
            "amount": "27615338636535324038545"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15863887491821"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYjA1NGZkZi0wZGJjLTVhYjktYTVmNS1jYjUwNTU3ZDRhMzYifQ==",
    "nonce": 110807,
    "balances": {
      "current": "357343468381977143627042",
      "previous": "357343484261728522940386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57dfe43b0460c57d9904412fd8dedf8998b49cb1",
    "nonce": 46,
    "balances": {
      "current": "669111934494600690",
      "previous": "653248047002779167"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:08.262Z",
  "updated": "2022-05-04T08:55:08.333Z",
  "id": "62723f6cbbd75600116d05e8"
}
```
* *stageAmount*: `669111934494600690`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000385c1f22b4efd30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000385c1f22b4efd3000000000000000000000000000000000000000000000000062d831f0050f4e92aaa38b55a3a2a735b542c7f4f25024ec61a97fb34e5dc567dd7b4b766037302bd738f0bd971605b107e70931fabfc5a0306247569ce3868fb0510a166faf09c298878f69196862629d5dd58a26a0d12f0c5c09ddc35cbbfa5331090ba99a875000000000000000000000000000000000000000000000000000000000000001c019f47948c9e893436366fcd0acf4b10bc756584a9300d524b9114a3108872542b162b4a4961f537d6e2e46e47cd68420db1b9f1157a8974cdfbaf0c565c3e0236521c156402e37665e3cc71cd7d666b197598fd41c315212416be3e326eb38e000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0d7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004baba0d42691f2f34d22000000000000000000000000000000000000000000004baba10c911eaf092fe200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000e6d9960f2ed0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d907cf5198181155910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a596a41314e475a6b5a6930775a474a6a4c545668596a6b745954566d4e53316a596a55774e5455335a4452684d7a596966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000057dfe43b0460c57d9904412fd8dedf8998b49cb1000000000000000000000000000000000000000000000000094929c262866df20000000000000000000000000000000000000000000000000910cda33fd17e1f00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x2aaa38b55a3a2a735b542c7f4f25024ec61a97fb34e5dc567dd7b4b766037302",
      "signature": {
        "s": "0x298878f69196862629d5dd58a26a0d12f0c5c09ddc35cbbfa5331090ba99a875",
        "r": "0xbd738f0bd971605b107e70931fabfc5a0306247569ce3868fb0510a166faf09c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x019f47948c9e893436366fcd0acf4b10bc756584a9300d524b9114a310887254",
      "signature": {
        "s": "0x36521c156402e37665e3cc71cd7d666b197598fd41c315212416be3e326eb38e",
        "r": "0x2b162b4a4961f537d6e2e46e47cd68420db1b9f1157a8974cdfbaf0c565c3e02",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "15863887491821523",
    "total": "445156107352077545"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15863887491821523",
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
            "amount": "27615338636535324038545"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15863887491821"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzYjA1NGZkZi0wZGJjLTVhYjktYTVmNS1jYjUwNTU3ZDRhMzYifQ==",
    "nonce": 110807,
    "balances": {
      "current": "357343468381977143627042",
      "previous": "357343484261728522940386"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x57dfe43b0460c57d9904412fd8dedf8998b49cb1",
    "nonce": 46,
    "balances": {
      "current": "669111934494600690",
      "previous": "653248047002779167"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:08.262Z",
  "updated": "2022-05-04T08:55:08.333Z",
  "id": "62723f6cbbd75600116d05e8"
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
0x0f200f9b000000000000000000000000000000000000000000000000094929c262866df20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669111934494600690`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`