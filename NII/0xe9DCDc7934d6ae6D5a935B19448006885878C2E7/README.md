# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe9DCDc7934d6ae6D5a935B19448006885878C2E7`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b0000000000000000000000000000000000000000000000030f6d4746c3263b330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000030f6d4746c3263b3300000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b7c875db9c0f713d8edfd97990b20ff1e49f9bee9a0e4592cf16a3d58db3c08bdadc111ae982ac73947d8ee38a455a0fa0e56ecbd8321254af285301d057ac7ef475fd19e5652643a90a0ca1c0db794759ed101f838d42b8ee760f1ab688ddb49000000000000000000000000000000000000000000000000000000000000001b06a40153afe649bc91b3fb9de4c990b555bcc7d1bafc6f4760e8506a9ed10c1b11d69e846e1d339700ed09b7fbd77b80b459b829cbf104f4092ebc8bdd34e1682d2b65edb2f11e01175f9cbd1a4159ec5442462d670a1569c305341cc6c6f28d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bac19100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011503000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024885fd2bd6de4303c1900000000000000000000000000000000000000000000248b7008935e73d226f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c88ea9cc7bafac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000323032a7e183da213720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a57557a4d446b7a595330354e6a49354c54566d4d7a41744f474578597930344d446868597a46694e7a4d794e47556966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000e9dcdc7934d6ae6d5a935b19448006885878c2e700000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b00000000000000000000000000000000000000000000000a805887e3a176143800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c875db9c0f713d8edfd97990b20ff1e49f9bee9a0e4592cf16a3d58db3c08bd",
      "signature": {
        "s": "0x475fd19e5652643a90a0ca1c0db794759ed101f838d42b8ee760f1ab688ddb49",
        "r": "0xadc111ae982ac73947d8ee38a455a0fa0e56ecbd8321254af285301d057ac7ef",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x06a40153afe649bc91b3fb9de4c990b555bcc7d1bafc6f4760e8506a9ed10c1b",
      "signature": {
        "s": "0x2d2b65edb2f11e01175f9cbd1a4159ec5442462d670a1569c305341cc6c6f28d",
        "r": "0x11d69e846e1d339700ed09b7fbd77b80b459b829cbf104f4092ebc8bdd34e168",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56451855273406380851",
    "total": "250167587257043406699"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56451855273406380851",
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
            "amount": "14812963624562483925874"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56451855273406380"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZWUzMDkzYS05NjI5LTVmMzAtOGExYy04MDhhYzFiNzMyNGUifQ==",
    "nonce": 70915,
    "balances": {
      "current": "172520855366790116555801",
      "previous": "172577363673918796343032"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe9dcdc7934d6ae6d5a935b19448006885878c2e7",
    "nonce": 4,
    "balances": {
      "current": "250167587257043406699",
      "previous": "193715731983637025848"
    }
  },
  "blockNumber": "12239249",
  "created": "2021-04-14T16:22:00.774Z",
  "updated": "2021-04-14T16:22:00.865Z",
  "id": "607716a888d56c0010d62091"
}
```
* *stageAmount*: `250167587257043406699`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000030f6d4746c3263b330000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000030f6d4746c3263b3300000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b7c875db9c0f713d8edfd97990b20ff1e49f9bee9a0e4592cf16a3d58db3c08bdadc111ae982ac73947d8ee38a455a0fa0e56ecbd8321254af285301d057ac7ef475fd19e5652643a90a0ca1c0db794759ed101f838d42b8ee760f1ab688ddb49000000000000000000000000000000000000000000000000000000000000001b06a40153afe649bc91b3fb9de4c990b555bcc7d1bafc6f4760e8506a9ed10c1b11d69e846e1d339700ed09b7fbd77b80b459b829cbf104f4092ebc8bdd34e1682d2b65edb2f11e01175f9cbd1a4159ec5442462d670a1569c305341cc6c6f28d000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bac19100000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000011503000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024885fd2bd6de4303c1900000000000000000000000000000000000000000000248b7008935e73d226f800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000c88ea9cc7bafac0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000323032a7e183da213720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a5a57557a4d446b7a595330354e6a49354c54566d4d7a41744f474578597930344d446868597a46694e7a4d794e47556966513d3d0000000000000000000000000000000000000000000000000000000000000004000000000000000000000000e9dcdc7934d6ae6d5a935b19448006885878c2e700000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b00000000000000000000000000000000000000000000000a805887e3a176143800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x7c875db9c0f713d8edfd97990b20ff1e49f9bee9a0e4592cf16a3d58db3c08bd",
      "signature": {
        "s": "0x475fd19e5652643a90a0ca1c0db794759ed101f838d42b8ee760f1ab688ddb49",
        "r": "0xadc111ae982ac73947d8ee38a455a0fa0e56ecbd8321254af285301d057ac7ef",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x06a40153afe649bc91b3fb9de4c990b555bcc7d1bafc6f4760e8506a9ed10c1b",
      "signature": {
        "s": "0x2d2b65edb2f11e01175f9cbd1a4159ec5442462d670a1569c305341cc6c6f28d",
        "r": "0x11d69e846e1d339700ed09b7fbd77b80b459b829cbf104f4092ebc8bdd34e168",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "56451855273406380851",
    "total": "250167587257043406699"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "56451855273406380851",
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
            "amount": "14812963624562483925874"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "56451855273406380"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzZWUzMDkzYS05NjI5LTVmMzAtOGExYy04MDhhYzFiNzMyNGUifQ==",
    "nonce": 70915,
    "balances": {
      "current": "172520855366790116555801",
      "previous": "172577363673918796343032"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe9dcdc7934d6ae6d5a935b19448006885878c2e7",
    "nonce": 4,
    "balances": {
      "current": "250167587257043406699",
      "previous": "193715731983637025848"
    }
  },
  "blockNumber": "12239249",
  "created": "2021-04-14T16:22:00.774Z",
  "updated": "2021-04-14T16:22:00.865Z",
  "id": "607716a888d56c0010d62091"
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
0x0f200f9b00000000000000000000000000000000000000000000000d8fc5cf2a649c4f6b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `250167587257043406699`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`