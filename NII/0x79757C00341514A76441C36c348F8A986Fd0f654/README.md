# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x79757C00341514A76441C36c348F8A986Fd0f654`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000001bcfdf601280ac84000000000000000000000000000000000000000000000051dfaa20925ec980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000051dfaa20925ec98000000000000000000000000000000000000000000000000051dfaa20925ec9800093c2423a65be1883dfcfbfa6d78649cf318200a6150d6fc9e37b4c8c95837b480f4aea974280e8f9897b415430db4cc99208fb5d6cb0bfca9c49de43755a8bd87280b4321c73b175ead0ec9de3fc7ad7d706bc336038b42c209272164d654590000000000000000000000000000000000000000000000000000000000000001be25bf88169305f3589fddea2d4de831f4225626eeca4cf3f53c86615ff40ef846349da7aafd97e7019436f8913fd402381179db23229e77b7e5769ad1f9dbe3427fd7f9bc07ec754201c50345b16c27442f473ca0c5b3160e0ad054f0a543ee1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1c5700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002b00000000000000000000000079757c00341514a76441c36c348f8a986fd0f6540000000000000000000000000000000000000000000000001bcfdf601280ac84000000000000000000000000000000000000000000000052106fac860b7f1c8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000014f5ac939a34f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000014f5ac939a34f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f4441344e324d304d4330324e474d334c5451324f4749744f474935595330304e4463324d7a526c4e4755785954676966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001aefae427b4d4f23e247000000000000000000000000000000000000000000001a9dce985abaf05a624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x93c2423a65be1883dfcfbfa6d78649cf318200a6150d6fc9e37b4c8c95837b48",
      "signature": {
        "s": "0x7280b4321c73b175ead0ec9de3fc7ad7d706bc336038b42c209272164d654590",
        "r": "0x0f4aea974280e8f9897b415430db4cc99208fb5d6cb0bfca9c49de43755a8bd8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe25bf88169305f3589fddea2d4de831f4225626eeca4cf3f53c86615ff40ef84",
      "signature": {
        "s": "0x27fd7f9bc07ec754201c50345b16c27442f473ca0c5b3160e0ad054f0a543ee1",
        "r": "0x6349da7aafd97e7019436f8913fd402381179db23229e77b7e5769ad1f9dbe34",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1510303000000000000000",
    "total": "1510303000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1510303000000000000000",
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
            "amount": "1510303000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1510303000000000000"
      }
    },
    "wallet": "0x79757c00341514a76441c36c348f8a986fd0f654",
    "data": "eyJyZWYiOiI0ODA4N2M0MC02NGM3LTQ2OGItOGI5YS00NDc2MzRlNGUxYTgifQ==",
    "nonce": 43,
    "balances": {
      "current": "2004065962923437188",
      "previous": "1513817368962923437188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 27,
    "balances": {
      "current": "127202857122510391206471",
      "previous": "125692554122510391206471"
    }
  },
  "blockNumber": "14796144",
  "created": "2022-05-18T02:15:26.343Z",
  "updated": "2022-05-18T02:15:26.423Z",
  "id": "628456be3592fd001130b830"
}
```
* *stageAmount*: `2004065962923437188`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000051dfaa20925ec980000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000051dfaa20925ec98000000000000000000000000000000000000000000000000051dfaa20925ec9800093c2423a65be1883dfcfbfa6d78649cf318200a6150d6fc9e37b4c8c95837b480f4aea974280e8f9897b415430db4cc99208fb5d6cb0bfca9c49de43755a8bd87280b4321c73b175ead0ec9de3fc7ad7d706bc336038b42c209272164d654590000000000000000000000000000000000000000000000000000000000000001be25bf88169305f3589fddea2d4de831f4225626eeca4cf3f53c86615ff40ef846349da7aafd97e7019436f8913fd402381179db23229e77b7e5769ad1f9dbe3427fd7f9bc07ec754201c50345b16c27442f473ca0c5b3160e0ad054f0a543ee1000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e1c5700000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000002b00000000000000000000000079757c00341514a76441c36c348f8a986fd0f6540000000000000000000000000000000000000000000000001bcfdf601280ac84000000000000000000000000000000000000000000000052106fac860b7f1c8400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000014f5ac939a34f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000014f5ac939a34f0000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304f4441344e324d304d4330324e474d334c5451324f4749744f474935595330304e4463324d7a526c4e4755785954676966513d3d000000000000000000000000000000000000000000000000000000000000001b000000000000000000000000180ec572bd4c2aed018f2e07b0adc05deac7f0b1000000000000000000000000000000000000000000001aefae427b4d4f23e247000000000000000000000000000000000000000000001a9dce985abaf05a624700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x93c2423a65be1883dfcfbfa6d78649cf318200a6150d6fc9e37b4c8c95837b48",
      "signature": {
        "s": "0x7280b4321c73b175ead0ec9de3fc7ad7d706bc336038b42c209272164d654590",
        "r": "0x0f4aea974280e8f9897b415430db4cc99208fb5d6cb0bfca9c49de43755a8bd8",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xe25bf88169305f3589fddea2d4de831f4225626eeca4cf3f53c86615ff40ef84",
      "signature": {
        "s": "0x27fd7f9bc07ec754201c50345b16c27442f473ca0c5b3160e0ad054f0a543ee1",
        "r": "0x6349da7aafd97e7019436f8913fd402381179db23229e77b7e5769ad1f9dbe34",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1510303000000000000000",
    "total": "1510303000000000000000"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1510303000000000000000",
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
            "amount": "1510303000000000000"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1510303000000000000"
      }
    },
    "wallet": "0x79757c00341514a76441c36c348f8a986fd0f654",
    "data": "eyJyZWYiOiI0ODA4N2M0MC02NGM3LTQ2OGItOGI5YS00NDc2MzRlNGUxYTgifQ==",
    "nonce": 43,
    "balances": {
      "current": "2004065962923437188",
      "previous": "1513817368962923437188"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x180ec572bd4c2aed018f2e07b0adc05deac7f0b1",
    "nonce": 27,
    "balances": {
      "current": "127202857122510391206471",
      "previous": "125692554122510391206471"
    }
  },
  "blockNumber": "14796144",
  "created": "2022-05-18T02:15:26.343Z",
  "updated": "2022-05-18T02:15:26.423Z",
  "id": "628456be3592fd001130b830"
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
0x0f200f9b0000000000000000000000000000000000000000000000001bcfdf601280ac840000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `2004065962923437188`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`