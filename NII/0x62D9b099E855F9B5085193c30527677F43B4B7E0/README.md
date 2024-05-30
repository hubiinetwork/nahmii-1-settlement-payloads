# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x62D9b099E855F9B5085193c30527677F43B4B7E0`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000261770d25b668b92ca000000000000000000000000000000000000000000000000e73214f2cf9f1e2f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9f1e2f0000000000000000000000000000000000000000000000195793009724215ac2799462ad7eddfcf67d0a3f95a0ee5ae685191fbbe9980e3d1e61de5918404609d49f93283c4c58008411c587e6304e21be7226961c665c2757557eaf42f7c8841bd4c60f952a173b0c878391dd8072da1f14f61f19c9f371602fecdce08ee308000000000000000000000000000000000000000000000000000000000000001cfe0ea7db5a896a2fa751f179157690d1fa9ebcc5b2efa710e835770570d1a720b9326e04295c1fb1942ca39b37bafd647a3c02930d1c7232e99f841d2c60141e58559f05b9f596aa2b782d3e65d80bdbb299a1742c4eaf9efcd88176d7e3145b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096615f2d9400263c7e42000000000000000000000000000000000000000000009662469ad89604e9d9a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec82c30905dbd1220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e5442684f4467325979316b4e474d784c5455785a444574595756685a53307a4e7a41354e44686b4e6d49325a6d516966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000062d9b099e855f9b5085193c30527677f43b4b7e00000000000000000000000000000000000000000000000261770d25b668b92ca000000000000000000000000000000000000000000000025303ebd6896ec749b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x799462ad7eddfcf67d0a3f95a0ee5ae685191fbbe9980e3d1e61de5918404609",
      "signature": {
        "s": "0x1bd4c60f952a173b0c878391dd8072da1f14f61f19c9f371602fecdce08ee308",
        "r": "0xd49f93283c4c58008411c587e6304e21be7226961c665c2757557eaf42f7c884",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfe0ea7db5a896a2fa751f179157690d1fa9ebcc5b2efa710e835770570d1a720",
      "signature": {
        "s": "0x58559f05b9f596aa2b782d3e65d80bdbb299a1742c4eaf9efcd88176d7e3145b",
        "r": "0xb9326e04295c1fb1942ca39b37bafd647a3c02930d1c7232e99f841d2c60141e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694838831",
    "total": "467478989994761214658"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694838831",
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
            "amount": "27262883395252451528994"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694838"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNTBhODg2Yy1kNGMxLTUxZDEtYWVhZS0zNzA5NDhkNmI2ZmQifQ==",
    "nonce": 110012,
    "balances": {
      "current": "710151164906132526104130",
      "previous": "710167840966538225637799"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62d9b099e855f9b5085193c30527677f43b4b7e0",
    "nonce": 46,
    "balances": {
      "current": "702665355951231177418",
      "previous": "686005954946536338587"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:05.729Z",
  "updated": "2022-05-04T08:51:05.888Z",
  "id": "62723e793592fd001130b44b"
}
```
* *stageAmount*: `702665355951231177418`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000e73214f2cf9f1e2f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000e73214f2cf9f1e2f0000000000000000000000000000000000000000000000195793009724215ac2799462ad7eddfcf67d0a3f95a0ee5ae685191fbbe9980e3d1e61de5918404609d49f93283c4c58008411c587e6304e21be7226961c665c2757557eaf42f7c8841bd4c60f952a173b0c878391dd8072da1f14f61f19c9f371602fecdce08ee308000000000000000000000000000000000000000000000000000000000000001cfe0ea7db5a896a2fa751f179157690d1fa9ebcc5b2efa710e835770570d1a720b9326e04295c1fb1942ca39b37bafd647a3c02930d1c7232e99f841d2c60141e58559f05b9f596aa2b782d3e65d80bdbb299a1742c4eaf9efcd88176d7e3145b000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001adbc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000096615f2d9400263c7e42000000000000000000000000000000000000000000009662469ad89604e9d9a700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000003b2fa30f0e3d360000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5ec82c30905dbd1220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f69497a4e5442684f4467325979316b4e474d784c5455785a444574595756685a53307a4e7a41354e44686b4e6d49325a6d516966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000062d9b099e855f9b5085193c30527677f43b4b7e00000000000000000000000000000000000000000000000261770d25b668b92ca000000000000000000000000000000000000000000000025303ebd6896ec749b00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x799462ad7eddfcf67d0a3f95a0ee5ae685191fbbe9980e3d1e61de5918404609",
      "signature": {
        "s": "0x1bd4c60f952a173b0c878391dd8072da1f14f61f19c9f371602fecdce08ee308",
        "r": "0xd49f93283c4c58008411c587e6304e21be7226961c665c2757557eaf42f7c884",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfe0ea7db5a896a2fa751f179157690d1fa9ebcc5b2efa710e835770570d1a720",
      "signature": {
        "s": "0x58559f05b9f596aa2b782d3e65d80bdbb299a1742c4eaf9efcd88176d7e3145b",
        "r": "0xb9326e04295c1fb1942ca39b37bafd647a3c02930d1c7232e99f841d2c60141e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "16659401004694838831",
    "total": "467478989994761214658"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "16659401004694838831",
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
            "amount": "27262883395252451528994"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "16659401004694838"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIzNTBhODg2Yy1kNGMxLTUxZDEtYWVhZS0zNzA5NDhkNmI2ZmQifQ==",
    "nonce": 110012,
    "balances": {
      "current": "710151164906132526104130",
      "previous": "710167840966538225637799"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x62d9b099e855f9b5085193c30527677f43b4b7e0",
    "nonce": 46,
    "balances": {
      "current": "702665355951231177418",
      "previous": "686005954946536338587"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:51:05.729Z",
  "updated": "2022-05-04T08:51:05.888Z",
  "id": "62723e793592fd001130b44b"
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
0x0f200f9b0000000000000000000000000000000000000000000000261770d25b668b92ca0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `702665355951231177418`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`