# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x081c2ea510C247037DEbd3180cF0b81b6e64827B`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000ca2ecd8c943882c800000000000000000000000000000000000000000000000010e08b03e256b2300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000010e08b03e256b230000000000000000000000000000000000000000000000000ca2ecd8c943882c83b8181fbc32a3bb1b10a9fd8f894e04296baf5251752d7be47bdab072b00c8fd0284f852409f112c8cbad028026a4e2b81dd0b080f67cce37a7ae87a7c49da1031632f997422a19b6e711dc306f40fc67c9f8f0cadf8f9a3436892103d377200000000000000000000000000000000000000000000000000000000000000001c84db78fcae75f1fa487510888286f58bda8ea57d51f2ca59eeb2acbc6d4968f8ae69f4b3bb0ae822aaabb474102e4bc6cb0e75c9b71698c1e373359435c922236895e7057f39fefde684f3cd44b064a3ef1f925fe725eb8624bda425836c2787000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b56c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000341590ade11a7b7ee5b0000000000000000000000000000000000000000000003415a192be2d7973e35100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000004520f1b9e4b710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df1002817cd9461ff20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b59324a684d6d566d4d4330314f4442684c5455785a6a6b74596a45305953316d5a6d566a4e324532596d59304f54496966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000081c2ea510c247037debd3180cf0b81b6e64827b000000000000000000000000000000000000000000000000ca2ecd8c943882c8000000000000000000000000000000000000000000000000b94e4288b1e1d09800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b8181fbc32a3bb1b10a9fd8f894e04296baf5251752d7be47bdab072b00c8fd",
      "signature": {
        "s": "0x31632f997422a19b6e711dc306f40fc67c9f8f0cadf8f9a3436892103d377200",
        "r": "0x0284f852409f112c8cbad028026a4e2b81dd0b080f67cce37a7ae87a7c49da10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x84db78fcae75f1fa487510888286f58bda8ea57d51f2ca59eeb2acbc6d4968f8",
      "signature": {
        "s": "0x6895e7057f39fefde684f3cd44b064a3ef1f925fe725eb8624bda425836c2787",
        "r": "0xae69f4b3bb0ae822aaabb474102e4bc6cb0e75c9b71698c1e373359435c92223",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1216124748188529200",
    "total": "14568807848255980232"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1216124748188529200",
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
            "amount": "27726609969613237526514"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1216124748188529"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkY2JhMmVmMC01ODBhLTUxZjktYjE0YS1mZmVjN2E2YmY0OTIifQ==",
    "nonce": 111980,
    "balances": {
      "current": "245960863970985741575600",
      "previous": "245962081311858678293329"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x081c2ea510c247037debd3180cf0b81b6e64827b",
    "nonce": 12,
    "balances": {
      "current": "14568807848255980232",
      "previous": "13352683100067451032"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:22.243Z",
  "updated": "2022-05-04T09:01:22.358Z",
  "id": "627240e23592fd001130b6ee"
}
```
* *stageAmount*: `14568807848255980232`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000010e08b03e256b2300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000010e08b03e256b230000000000000000000000000000000000000000000000000ca2ecd8c943882c83b8181fbc32a3bb1b10a9fd8f894e04296baf5251752d7be47bdab072b00c8fd0284f852409f112c8cbad028026a4e2b81dd0b080f67cce37a7ae87a7c49da1031632f997422a19b6e711dc306f40fc67c9f8f0cadf8f9a3436892103d377200000000000000000000000000000000000000000000000000000000000000001c84db78fcae75f1fa487510888286f58bda8ea57d51f2ca59eeb2acbc6d4968f8ae69f4b3bb0ae822aaabb474102e4bc6cb0e75c9b71698c1e373359435c922236895e7057f39fefde684f3cd44b064a3ef1f925fe725eb8624bda425836c2787000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e20000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b56c000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000341590ade11a7b7ee5b0000000000000000000000000000000000000000000003415a192be2d7973e35100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000004520f1b9e4b710000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df1002817cd9461ff20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b59324a684d6d566d4d4330314f4442684c5455785a6a6b74596a45305953316d5a6d566a4e324532596d59304f54496966513d3d000000000000000000000000000000000000000000000000000000000000000c000000000000000000000000081c2ea510c247037debd3180cf0b81b6e64827b000000000000000000000000000000000000000000000000ca2ecd8c943882c8000000000000000000000000000000000000000000000000b94e4288b1e1d09800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3b8181fbc32a3bb1b10a9fd8f894e04296baf5251752d7be47bdab072b00c8fd",
      "signature": {
        "s": "0x31632f997422a19b6e711dc306f40fc67c9f8f0cadf8f9a3436892103d377200",
        "r": "0x0284f852409f112c8cbad028026a4e2b81dd0b080f67cce37a7ae87a7c49da10",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x84db78fcae75f1fa487510888286f58bda8ea57d51f2ca59eeb2acbc6d4968f8",
      "signature": {
        "s": "0x6895e7057f39fefde684f3cd44b064a3ef1f925fe725eb8624bda425836c2787",
        "r": "0xae69f4b3bb0ae822aaabb474102e4bc6cb0e75c9b71698c1e373359435c92223",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1216124748188529200",
    "total": "14568807848255980232"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1216124748188529200",
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
            "amount": "27726609969613237526514"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1216124748188529"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkY2JhMmVmMC01ODBhLTUxZjktYjE0YS1mZmVjN2E2YmY0OTIifQ==",
    "nonce": 111980,
    "balances": {
      "current": "245960863970985741575600",
      "previous": "245962081311858678293329"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x081c2ea510c247037debd3180cf0b81b6e64827b",
    "nonce": 12,
    "balances": {
      "current": "14568807848255980232",
      "previous": "13352683100067451032"
    }
  },
  "blockNumber": "14709986",
  "created": "2022-05-04T09:01:22.243Z",
  "updated": "2022-05-04T09:01:22.358Z",
  "id": "627240e23592fd001130b6ee"
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
0x0f200f9b000000000000000000000000000000000000000000000000ca2ecd8c943882c80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `14568807848255980232`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`