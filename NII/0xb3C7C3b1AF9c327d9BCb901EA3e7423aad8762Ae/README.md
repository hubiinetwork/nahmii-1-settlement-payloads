# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xb3C7C3b1AF9c327d9BCb901EA3e7423aad8762Ae`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000002447160fc8a7286d52000000000000000000000000000000000000000000000000dc2fb26d57f097cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f097cc00000000000000000000000000000000000000000000001822a4621607c5e337c147b95dcb74b1c9d4717dea81e02a601bc00817f5bb7b2f85fc991fd77bbc69f2a97447e0617c6a128673edacd2625ab4630b3998a483782a2c8cecaa8f3525073a5130f87cd2ff3f8cffe0559f4d997dbf71e183371b9aaf55ac3d2e509bde000000000000000000000000000000000000000000000000000000000000001c8632db7a125865ea708bff457088b7000545df901835091db5d2fd22cbdc617c0aabaf65e782e4dc3b31c3f55debfa6155753c2ec3dbdc8a5c396bb0f034f3444807fc7de169c7478ad642afa2ad5321d2b67d2f8e3d85d412cc2f6fb7dd9e23000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b739000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002db1f1958eae98381793000000000000000000000000000000000000000000002db2cdfd9f3d53d4b39e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac043f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b24f825656d0ce300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d32526b5954677959693079595459334c5456684e6a5574596d4d354f5331684d444d334e5468685a4455354d44456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b3c7c3b1af9c327d9bcb901ea3e7423aad8762ae00000000000000000000000000000000000000000000002447160fc8a7286d520000000000000000000000000000000000000000000000236ae65d5b4f37d58600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc147b95dcb74b1c9d4717dea81e02a601bc00817f5bb7b2f85fc991fd77bbc69",
      "signature": {
        "s": "0x073a5130f87cd2ff3f8cffe0559f4d997dbf71e183371b9aaf55ac3d2e509bde",
        "r": "0xf2a97447e0617c6a128673edacd2625ab4630b3998a483782a2c8cecaa8f3525",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8632db7a125865ea708bff457088b7000545df901835091db5d2fd22cbdc617c",
      "signature": {
        "s": "0x4807fc7de169c7478ad642afa2ad5321d2b67d2f8e3d85d412cc2f6fb7dd9e23",
        "r": "0x0aabaf65e782e4dc3b31c3f55debfa6155753c2ec3dbdc8a5c396bb0f034f344",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946111436",
    "total": "445218085709258548023"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946111436",
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
            "amount": "27756751718428412268080"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946111"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2M2RkYTgyYi0yYTY3LTVhNjUtYmM5OS1hMDM3NThhZDU5MDEifQ==",
    "nonce": 112441,
    "balances": {
      "current": "215788973406995825039251",
      "previous": "215804855369286966096798"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3c7c3b1af9c327d9bcb901ea3e7423aad8762ae",
    "nonce": 46,
    "balances": {
      "current": "669205085634196696402",
      "previous": "653338989439250584966"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:48.919Z",
  "updated": "2022-05-04T09:03:48.992Z",
  "id": "62724174bbd75600116d07f0"
}
```
* *stageAmount*: `669205085634196696402`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000dc2fb26d57f097cc0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000dc2fb26d57f097cc00000000000000000000000000000000000000000000001822a4621607c5e337c147b95dcb74b1c9d4717dea81e02a601bc00817f5bb7b2f85fc991fd77bbc69f2a97447e0617c6a128673edacd2625ab4630b3998a483782a2c8cecaa8f3525073a5130f87cd2ff3f8cffe0559f4d997dbf71e183371b9aaf55ac3d2e509bde000000000000000000000000000000000000000000000000000000000000001c8632db7a125865ea708bff457088b7000545df901835091db5d2fd22cbdc617c0aabaf65e782e4dc3b31c3f55debfa6155753c2ec3dbdc8a5c396bb0f034f3444807fc7de169c7478ad642afa2ad5321d2b67d2f8e3d85d412cc2f6fb7dd9e23000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ea0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b739000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000002db1f1958eae98381793000000000000000000000000000000000000000000002db2cdfd9f3d53d4b39e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000385e2163ac043f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e0b24f825656d0ce300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324d32526b5954677959693079595459334c5456684e6a5574596d4d354f5331684d444d334e5468685a4455354d44456966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b3c7c3b1af9c327d9bcb901ea3e7423aad8762ae00000000000000000000000000000000000000000000002447160fc8a7286d520000000000000000000000000000000000000000000000236ae65d5b4f37d58600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc147b95dcb74b1c9d4717dea81e02a601bc00817f5bb7b2f85fc991fd77bbc69",
      "signature": {
        "s": "0x073a5130f87cd2ff3f8cffe0559f4d997dbf71e183371b9aaf55ac3d2e509bde",
        "r": "0xf2a97447e0617c6a128673edacd2625ab4630b3998a483782a2c8cecaa8f3525",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x8632db7a125865ea708bff457088b7000545df901835091db5d2fd22cbdc617c",
      "signature": {
        "s": "0x4807fc7de169c7478ad642afa2ad5321d2b67d2f8e3d85d412cc2f6fb7dd9e23",
        "r": "0x0aabaf65e782e4dc3b31c3f55debfa6155753c2ec3dbdc8a5c396bb0f034f344",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "15866096194946111436",
    "total": "445218085709258548023"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "15866096194946111436",
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
            "amount": "27756751718428412268080"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "15866096194946111"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2M2RkYTgyYi0yYTY3LTVhNjUtYmM5OS1hMDM3NThhZDU5MDEifQ==",
    "nonce": 112441,
    "balances": {
      "current": "215788973406995825039251",
      "previous": "215804855369286966096798"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3c7c3b1af9c327d9bcb901ea3e7423aad8762ae",
    "nonce": 46,
    "balances": {
      "current": "669205085634196696402",
      "previous": "653338989439250584966"
    }
  },
  "blockNumber": "14709994",
  "created": "2022-05-04T09:03:48.919Z",
  "updated": "2022-05-04T09:03:48.992Z",
  "id": "62724174bbd75600116d07f0"
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
0x0f200f9b00000000000000000000000000000000000000000000002447160fc8a7286d520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `669205085634196696402`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`