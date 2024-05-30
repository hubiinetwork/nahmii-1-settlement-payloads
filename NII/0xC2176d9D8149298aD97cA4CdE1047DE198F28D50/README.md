# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xC2176d9D8149298aD97cA4CdE1047DE198F28D50`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000005683b1e7e6eb3ed1500000000000000000000000000000000000000000000000020d18c82917c26070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000020d18c82917c260700000000000000000000000000000000000000000000000398eba1461a6d79ccb99a2936ec31348241a0940e41989fbfda180716fb23ebeef9fdfa8d4d1a9aa2d25a98caf3cc3ab052a771fc86b9d8227cf05073d18df5622e3e5227b408da6702a322f2f93092044cda80e32d722590ea49890be1e698d664101a1212be78d2000000000000000000000000000000000000000000000000000000000000001ce48e49220c6dcdb5f06aca61fd153f58c7f67282847a9e576aefb4725ba6d280d93580c971876c100e6ad27492d505fdf0e0245f1c52ad2f329cd6a66cae238e6c985af45a953c2117b4e2338c70a75a09123ebdb8ef52972074797823acb6b3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aed0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d9709aa6e336294eb20000000000000000000000000000000000000000000095d991749a31afba50eb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000866cbe814dc320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60f464c18657db8560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a475178596d52694d433168596a51314c5455324d7a41744f47526859793035596d526c4e7a42685a57466d4e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c2176d9d8149298ad97ca4cde1047de198f28d50000000000000000000000000000000000000000000000005683b1e7e6eb3ed15000000000000000000000000000000000000000000000005476991fbdd37c70e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb99a2936ec31348241a0940e41989fbfda180716fb23ebeef9fdfa8d4d1a9aa2",
      "signature": {
        "s": "0x02a322f2f93092044cda80e32d722590ea49890be1e698d664101a1212be78d2",
        "r": "0xd25a98caf3cc3ab052a771fc86b9d8227cf05073d18df5622e3e5227b408da67",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe48e49220c6dcdb5f06aca61fd153f58c7f67282847a9e576aefb4725ba6d280",
      "signature": {
        "s": "0x6c985af45a953c2117b4e2338c70a75a09123ebdb8ef52972074797823acb6b3",
        "r": "0xd93580c971876c100e6ad27492d505fdf0e0245f1c52ad2f329cd6a66cae238e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2364825771760690695",
    "total": "66359310456883870156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2364825771760690695",
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
            "amount": "27265388391769321617494"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2364825771760690"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGQxYmRiMC1hYjQ1LTU2MzAtOGRhYy05YmRlNzBhZWFmNzkifQ==",
    "nonce": 110288,
    "balances": {
      "current": "707643663392745567375026",
      "previous": "707646030583343099826411"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2176d9d8149298ad97ca4cde1047de198f28d50",
    "nonce": 46,
    "balances": {
      "current": "99744350700490190101",
      "previous": "97379524928729499406"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:30.876Z",
  "updated": "2022-05-04T08:52:30.967Z",
  "id": "62723ece3592fd001130b4ab"
}
```
* *stageAmount*: `99744350700490190101`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000020d18c82917c26070000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000020d18c82917c260700000000000000000000000000000000000000000000000398eba1461a6d79ccb99a2936ec31348241a0940e41989fbfda180716fb23ebeef9fdfa8d4d1a9aa2d25a98caf3cc3ab052a771fc86b9d8227cf05073d18df5622e3e5227b408da6702a322f2f93092044cda80e32d722590ea49890be1e698d664101a1212be78d2000000000000000000000000000000000000000000000000000000000000001ce48e49220c6dcdb5f06aca61fd153f58c7f67282847a9e576aefb4725ba6d280d93580c971876c100e6ad27492d505fdf0e0245f1c52ad2f329cd6a66cae238e6c985af45a953c2117b4e2338c70a75a09123ebdb8ef52972074797823acb6b3000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aed0000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095d9709aa6e336294eb20000000000000000000000000000000000000000000095d991749a31afba50eb00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000866cbe814dc320000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60f464c18657db8560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a475178596d52694d433168596a51314c5455324d7a41744f47526859793035596d526c4e7a42685a57466d4e7a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000c2176d9d8149298ad97ca4cde1047de198f28d50000000000000000000000000000000000000000000000005683b1e7e6eb3ed15000000000000000000000000000000000000000000000005476991fbdd37c70e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb99a2936ec31348241a0940e41989fbfda180716fb23ebeef9fdfa8d4d1a9aa2",
      "signature": {
        "s": "0x02a322f2f93092044cda80e32d722590ea49890be1e698d664101a1212be78d2",
        "r": "0xd25a98caf3cc3ab052a771fc86b9d8227cf05073d18df5622e3e5227b408da67",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xe48e49220c6dcdb5f06aca61fd153f58c7f67282847a9e576aefb4725ba6d280",
      "signature": {
        "s": "0x6c985af45a953c2117b4e2338c70a75a09123ebdb8ef52972074797823acb6b3",
        "r": "0xd93580c971876c100e6ad27492d505fdf0e0245f1c52ad2f329cd6a66cae238e",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "2364825771760690695",
    "total": "66359310456883870156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "2364825771760690695",
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
            "amount": "27265388391769321617494"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "2364825771760690"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZGQxYmRiMC1hYjQ1LTU2MzAtOGRhYy05YmRlNzBhZWFmNzkifQ==",
    "nonce": 110288,
    "balances": {
      "current": "707643663392745567375026",
      "previous": "707646030583343099826411"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xc2176d9d8149298ad97ca4cde1047de198f28d50",
    "nonce": 46,
    "balances": {
      "current": "99744350700490190101",
      "previous": "97379524928729499406"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:30.876Z",
  "updated": "2022-05-04T08:52:30.967Z",
  "id": "62723ece3592fd001130b4ab"
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
0x0f200f9b000000000000000000000000000000000000000000000005683b1e7e6eb3ed150000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `99744350700490190101`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`