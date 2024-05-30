# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa4e1a08b200622acdAe050b95851322DE8556B67`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002289da199d7fa555ec00000000000000000000000000000000000000000000001681da00ce085f7fd60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001681da00ce085f7fd600000000000000000000000000000000000000000000002289da199d7fa555ec3a8d92c90faa95db18f55c6f4fc8a473aa598075e931b223c99d298613ee1d52f973533478a75b7fa858c2efc3be49f6530156d9da2976a85fabbb0f4a964381785fc9370a05d42d6261309cb194b073b84976457a8a249b732c59c988aba2f3000000000000000000000000000000000000000000000000000000000000001c2cbe10ffbc29996a57c9f743c9227baf3c7cb62aafcf2f0270a31a8c3fa032aea638fd26b4439a45ba3bab26502ea205d67709cf832f8d0940f59c2344ba8b6c06caf3d4ea138fb84d745a195972b3e0c7e49a6a28e2bd8b45974c5d3a0003bc000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000d7741f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000160ff000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000076f1803a2606136a4490000000000000000000000000000000000000000000007859fa0abe2d7acc3bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000005c308b46e169f9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046f63d1eac33caeb5640000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e474a694d7a42694f4330784d7a4d794c5455334d4749744f54686c4e53316b4e446c684e444535597a557a4e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000a4e1a08b200622acdae050b95851322de8556b6700000000000000000000000000000000000000000000002289da199d7fa555ec00000000000000000000000000000000000000000000000c080018cf7745d61600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a8d92c90faa95db18f55c6f4fc8a473aa598075e931b223c99d298613ee1d52",
      "signature": {
        "s": "0x785fc9370a05d42d6261309cb194b073b84976457a8a249b732c59c988aba2f3",
        "r": "0xf973533478a75b7fa858c2efc3be49f6530156d9da2976a85fabbb0f4a964381",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2cbe10ffbc29996a57c9f743c9227baf3c7cb62aafcf2f0270a31a8c3fa032ae",
      "signature": {
        "s": "0x06caf3d4ea138fb84d745a195972b3e0c7e49a6a28e2bd8b45974c5d3a0003bc",
        "r": "0xa638fd26b4439a45ba3bab26502ea205d67709cf832f8d0940f59c2344ba8b6c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "415185161682329501654",
    "total": "637122578598485906924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "415185161682329501654",
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
            "amount": "20944247311864486081892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "415185161682329501"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NGJiMzBiOC0xMzMyLTU3MGItOThlNS1kNDlhNDE5YzUzNzMifQ==",
    "nonce": 90367,
    "balances": {
      "current": "35105884377485948658761",
      "previous": "35521484724329960489916"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa4e1a08b200622acdae050b95851322de8556b67",
    "nonce": 2,
    "balances": {
      "current": "637122578598485906924",
      "previous": "221937416916156405270"
    }
  },
  "blockNumber": "14119967",
  "created": "2022-02-01T12:01:14.834Z",
  "updated": "2022-02-01T12:01:14.948Z",
  "id": "61f9210a1d84210011fbc53c"
}
```
* *stageAmount*: `637122578598485906924`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000001681da00ce085f7fd60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000001681da00ce085f7fd600000000000000000000000000000000000000000000002289da199d7fa555ec3a8d92c90faa95db18f55c6f4fc8a473aa598075e931b223c99d298613ee1d52f973533478a75b7fa858c2efc3be49f6530156d9da2976a85fabbb0f4a964381785fc9370a05d42d6261309cb194b073b84976457a8a249b732c59c988aba2f3000000000000000000000000000000000000000000000000000000000000001c2cbe10ffbc29996a57c9f743c9227baf3c7cb62aafcf2f0270a31a8c3fa032aea638fd26b4439a45ba3bab26502ea205d67709cf832f8d0940f59c2344ba8b6c06caf3d4ea138fb84d745a195972b3e0c7e49a6a28e2bd8b45974c5d3a0003bc000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000d7741f000000000000000000000000000000000000000000000000000000000000054000000000000000000000000000000000000000000000000000000000000160ff000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000076f1803a2606136a4490000000000000000000000000000000000000000000007859fa0abe2d7acc3bc00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000005c308b46e169f9d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000046f63d1eac33caeb5640000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e474a694d7a42694f4330784d7a4d794c5455334d4749744f54686c4e53316b4e446c684e444535597a557a4e7a4d6966513d3d0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000a4e1a08b200622acdae050b95851322de8556b6700000000000000000000000000000000000000000000002289da199d7fa555ec00000000000000000000000000000000000000000000000c080018cf7745d61600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3a8d92c90faa95db18f55c6f4fc8a473aa598075e931b223c99d298613ee1d52",
      "signature": {
        "s": "0x785fc9370a05d42d6261309cb194b073b84976457a8a249b732c59c988aba2f3",
        "r": "0xf973533478a75b7fa858c2efc3be49f6530156d9da2976a85fabbb0f4a964381",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2cbe10ffbc29996a57c9f743c9227baf3c7cb62aafcf2f0270a31a8c3fa032ae",
      "signature": {
        "s": "0x06caf3d4ea138fb84d745a195972b3e0c7e49a6a28e2bd8b45974c5d3a0003bc",
        "r": "0xa638fd26b4439a45ba3bab26502ea205d67709cf832f8d0940f59c2344ba8b6c",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "415185161682329501654",
    "total": "637122578598485906924"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "415185161682329501654",
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
            "amount": "20944247311864486081892"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "415185161682329501"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NGJiMzBiOC0xMzMyLTU3MGItOThlNS1kNDlhNDE5YzUzNzMifQ==",
    "nonce": 90367,
    "balances": {
      "current": "35105884377485948658761",
      "previous": "35521484724329960489916"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa4e1a08b200622acdae050b95851322de8556b67",
    "nonce": 2,
    "balances": {
      "current": "637122578598485906924",
      "previous": "221937416916156405270"
    }
  },
  "blockNumber": "14119967",
  "created": "2022-02-01T12:01:14.834Z",
  "updated": "2022-02-01T12:01:14.948Z",
  "id": "61f9210a1d84210011fbc53c"
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
0x0f200f9b00000000000000000000000000000000000000000000002289da199d7fa555ec0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `637122578598485906924`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`