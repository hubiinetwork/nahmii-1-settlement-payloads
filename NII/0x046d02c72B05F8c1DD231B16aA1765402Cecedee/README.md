# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x046d02c72B05F8c1DD231B16aA1765402Cecedee`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000498d299ee98127acf00000000000000000000000000000000000000000000000145d60df8361343650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000145d60df83613436500000000000000000000000000000000000000000000000498d299ee98127acff5e4f8f8d52e722c312f7e26dfffec70d81f2e71f2cc224e412ddcb7d31ac7a792db30c72da054941924c48f994dab6627b2891c4004e1a955c316fd8aba5a2841a93ef623db01c2b254dd7e28d9b26314bec43452acbc6f0269a903eecd191c000000000000000000000000000000000000000000000000000000000000001cfaea5112dfe6557f5bbad992d82930105daded11b0bbb8e8cedca94ecfb8cae134144bfbf176bbeeb3d409c3ec268712889a469a54fa98511dbefe4c416dea280a9b829223c9aa3812ed821612b59dad097f365a60ecfc16c02a3ea11e85010e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7d6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c03436d8291471c4781000000000000000000000000000000000000000000001c048996fa88f81eaa7400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005369ff7aef1f8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e537fbaa3ed706485a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e575269596d517a5a43316d4d57526c4c5455324e5455744f4441785a5330354d6a49344f54646d4d324d354d7a416966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000046d02c72b05f8c1dd231b16aa1765402cecedee00000000000000000000000000000000000000000000000498d299ee98127acf00000000000000000000000000000000000000000000000352fc8bf661ff376a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf5e4f8f8d52e722c312f7e26dfffec70d81f2e71f2cc224e412ddcb7d31ac7a7",
      "signature": {
        "s": "0x41a93ef623db01c2b254dd7e28d9b26314bec43452acbc6f0269a903eecd191c",
        "r": "0x92db30c72da054941924c48f994dab6627b2891c4004e1a955c316fd8aba5a28",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfaea5112dfe6557f5bbad992d82930105daded11b0bbb8e8cedca94ecfb8cae1",
      "signature": {
        "s": "0x0a9b829223c9aa3812ed821612b59dad097f365a60ecfc16c02a3ea11e85010e",
        "r": "0x34144bfbf176bbeeb3d409c3ec268712889a469a54fa98511dbefe4c416dea28",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23478969067052942181",
    "total": "84799009583745104591"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23478969067052942181",
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
            "amount": "27840170812305826007130"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23478969067052942"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNWRiYmQzZC1mMWRlLTU2NTUtODAxZS05MjI4OTdmM2M5MzAifQ==",
    "nonce": 112598,
    "balances": {
      "current": "132286460435704672176001",
      "previous": "132309962883740792171124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x046d02c72b05f8c1dd231b16aa1765402cecedee",
    "nonce": 5,
    "balances": {
      "current": "84799009583745104591",
      "previous": "61320040516692162410"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:42.925Z",
  "updated": "2022-05-04T09:04:43.086Z",
  "id": "627241aa3592fd001130b7bb"
}
```
* *stageAmount*: `84799009583745104591`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000145d60df8361343650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000145d60df83613436500000000000000000000000000000000000000000000000498d299ee98127acff5e4f8f8d52e722c312f7e26dfffec70d81f2e71f2cc224e412ddcb7d31ac7a792db30c72da054941924c48f994dab6627b2891c4004e1a955c316fd8aba5a2841a93ef623db01c2b254dd7e28d9b26314bec43452acbc6f0269a903eecd191c000000000000000000000000000000000000000000000000000000000000001cfaea5112dfe6557f5bbad992d82930105daded11b0bbb8e8cedca94ecfb8cae134144bfbf176bbeeb3d409c3ec268712889a469a54fa98511dbefe4c416dea280a9b829223c9aa3812ed821612b59dad097f365a60ecfc16c02a3ea11e85010e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b7d6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000001c03436d8291471c4781000000000000000000000000000000000000000000001c048996fa88f81eaa7400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000005369ff7aef1f8e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e537fbaa3ed706485a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949794e575269596d517a5a43316d4d57526c4c5455324e5455744f4441785a5330354d6a49344f54646d4d324d354d7a416966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000046d02c72b05f8c1dd231b16aa1765402cecedee00000000000000000000000000000000000000000000000498d299ee98127acf00000000000000000000000000000000000000000000000352fc8bf661ff376a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xf5e4f8f8d52e722c312f7e26dfffec70d81f2e71f2cc224e412ddcb7d31ac7a7",
      "signature": {
        "s": "0x41a93ef623db01c2b254dd7e28d9b26314bec43452acbc6f0269a903eecd191c",
        "r": "0x92db30c72da054941924c48f994dab6627b2891c4004e1a955c316fd8aba5a28",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfaea5112dfe6557f5bbad992d82930105daded11b0bbb8e8cedca94ecfb8cae1",
      "signature": {
        "s": "0x0a9b829223c9aa3812ed821612b59dad097f365a60ecfc16c02a3ea11e85010e",
        "r": "0x34144bfbf176bbeeb3d409c3ec268712889a469a54fa98511dbefe4c416dea28",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "23478969067052942181",
    "total": "84799009583745104591"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "23478969067052942181",
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
            "amount": "27840170812305826007130"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "23478969067052942"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIyNWRiYmQzZC1mMWRlLTU2NTUtODAxZS05MjI4OTdmM2M5MzAifQ==",
    "nonce": 112598,
    "balances": {
      "current": "132286460435704672176001",
      "previous": "132309962883740792171124"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x046d02c72b05f8c1dd231b16aa1765402cecedee",
    "nonce": 5,
    "balances": {
      "current": "84799009583745104591",
      "previous": "61320040516692162410"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:42.925Z",
  "updated": "2022-05-04T09:04:43.086Z",
  "id": "627241aa3592fd001130b7bb"
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
0x0f200f9b00000000000000000000000000000000000000000000000498d299ee98127acf0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `84799009583745104591`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`