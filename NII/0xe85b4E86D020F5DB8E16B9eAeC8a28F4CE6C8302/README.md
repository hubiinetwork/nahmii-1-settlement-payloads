# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xe85b4E86D020F5DB8E16B9eAeC8a28F4CE6C8302`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000911c583f90ccadc1e300000000000000000000000000000000000000000000000370bec9b55fc3033d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000370bec9b55fc3033d0000000000000000000000000000000000000000000000608a9188581f268186ba3e31a0d74fa44858ebad758b6941e14d06895fa033239c11fd9d896cab4fad00c40bedadca9ef3de15143f0c048fed4e211ac237daeb37a973b749aa5d5cad601defe0b14efe57217fcbf290856d694338f9aefc8b7dab53bd4624583257fd000000000000000000000000000000000000000000000000000000000000001bf88666fc25f98ae6a7b61611350e9f3ddda7a807a44536b8064f85d0000620018ce7f059d82e9ce7b3c49f377d0eb7d4074f6ef7cfc748f3b1c4185cf64c1bfd3df8651719dc1def39b05ded116cbd354746b81ee3c3efe28d4849c9822cb18a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b72f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002ed8107eb08a0f867a83000000000000000000000000000000000000000000002edb821ef2c4fdf98ee700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e178858eb011270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0671744ab485ff1a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d446b785a544a6a5a4330314d7a49794c5455315a544974595441324d79316c4e474a694f4759774e4755335957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e85b4e86d020f5db8e16b9eaec8a28f4ce6c83020000000000000000000000000000000000000000000000911c583f90ccadc1e300000000000000000000000000000000000000000000008dab9975db6ceabea600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba3e31a0d74fa44858ebad758b6941e14d06895fa033239c11fd9d896cab4fad",
      "signature": {
        "s": "0x601defe0b14efe57217fcbf290856d694338f9aefc8b7dab53bd4624583257fd",
        "r": "0x00c40bedadca9ef3de15143f0c048fed4e211ac237daeb37a973b749aa5d5cad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf88666fc25f98ae6a7b61611350e9f3ddda7a807a44536b8064f85d000062001",
      "signature": {
        "s": "0x3df8651719dc1def39b05ded116cbd354746b81ee3c3efe28d4849c9822cb18a",
        "r": "0x8ce7f059d82e9ce7b3c49f377d0eb7d4074f6ef7cfc748f3b1c4185cf64c1bfd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "63464384779784487741",
    "total": "1780872342837035172230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "63464384779784487741",
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
            "amount": "27751331568471980896679"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "63464384779784487"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MDkxZTJjZC01MzIyLTU1ZTItYTA2My1lNGJiOGYwNGU3YWYifQ==",
    "nonce": 112431,
    "balances": {
      "current": "221214543513383627815555",
      "previous": "221278071362548192087783"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe85b4e86d020f5db8e16b9eaec8a28f4ce6c8302",
    "nonce": 46,
    "balances": {
      "current": "2676820343010039284195",
      "previous": "2613355958230254796454"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:45.739Z",
  "updated": "2022-05-04T09:03:45.827Z",
  "id": "627241717832e20011830e4b"
}
```
* *stageAmount*: `2676820343010039284195`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000370bec9b55fc3033d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000370bec9b55fc3033d0000000000000000000000000000000000000000000000608a9188581f268186ba3e31a0d74fa44858ebad758b6941e14d06895fa033239c11fd9d896cab4fad00c40bedadca9ef3de15143f0c048fed4e211ac237daeb37a973b749aa5d5cad601defe0b14efe57217fcbf290856d694338f9aefc8b7dab53bd4624583257fd000000000000000000000000000000000000000000000000000000000000001bf88666fc25f98ae6a7b61611350e9f3ddda7a807a44536b8064f85d0000620018ce7f059d82e9ce7b3c49f377d0eb7d4074f6ef7cfc748f3b1c4185cf64c1bfd3df8651719dc1def39b05ded116cbd354746b81ee3c3efe28d4849c9822cb18a000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b72f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002ed8107eb08a0f867a83000000000000000000000000000000000000000000002edb821ef2c4fdf98ee700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000e178858eb011270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0671744ab485ff1a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d446b785a544a6a5a4330314d7a49794c5455315a544974595441324d79316c4e474a694f4759774e4755335957596966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000e85b4e86d020f5db8e16b9eaec8a28f4ce6c83020000000000000000000000000000000000000000000000911c583f90ccadc1e300000000000000000000000000000000000000000000008dab9975db6ceabea600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xba3e31a0d74fa44858ebad758b6941e14d06895fa033239c11fd9d896cab4fad",
      "signature": {
        "s": "0x601defe0b14efe57217fcbf290856d694338f9aefc8b7dab53bd4624583257fd",
        "r": "0x00c40bedadca9ef3de15143f0c048fed4e211ac237daeb37a973b749aa5d5cad",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xf88666fc25f98ae6a7b61611350e9f3ddda7a807a44536b8064f85d000062001",
      "signature": {
        "s": "0x3df8651719dc1def39b05ded116cbd354746b81ee3c3efe28d4849c9822cb18a",
        "r": "0x8ce7f059d82e9ce7b3c49f377d0eb7d4074f6ef7cfc748f3b1c4185cf64c1bfd",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "63464384779784487741",
    "total": "1780872342837035172230"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "63464384779784487741",
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
            "amount": "27751331568471980896679"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "63464384779784487"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MDkxZTJjZC01MzIyLTU1ZTItYTA2My1lNGJiOGYwNGU3YWYifQ==",
    "nonce": 112431,
    "balances": {
      "current": "221214543513383627815555",
      "previous": "221278071362548192087783"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xe85b4e86d020f5db8e16b9eaec8a28f4ce6c8302",
    "nonce": 46,
    "balances": {
      "current": "2676820343010039284195",
      "previous": "2613355958230254796454"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:45.739Z",
  "updated": "2022-05-04T09:03:45.827Z",
  "id": "627241717832e20011830e4b"
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
0x0f200f9b0000000000000000000000000000000000000000000000911c583f90ccadc1e30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2676820343010039284195`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`