# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xaaDBA39F0692135f5a566b930FD73878A5560A2b`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000e5e3002bee74867e49100000000000000000000000000000000000000000000005734a6a4258cc2e0f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000005734a6a4258cc2e0f500000000000000000000000000000000000000000000098f1369593e95686b4816235901559a374d9ef77b031c22364c07cbc137a5eeb0bfe70aac328d5383f159f6c385dcdc5575a5a6e668a15a40d3c517a9abb56cef879b6819e7d01dd0780bc2ad567c3a6feeb7347953abd044e70c1bb9d6299d35460ad4859b96b1bc63000000000000000000000000000000000000000000000000000000000000001b76546c53f42bd016db7e2328d16e0e735a2eb6f9ff416c830db52d20c018a0d9040868e4cb66357b9f0210ec2f7527915ecced55af87ab7e135d43d90562b40d60bd64bd380de79d353614f9f044ec1b5c6536530c8ef1e2f88bf7406a45a0f9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af38000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000084f1d9270521c12b28ab0000000000000000000000000000000000000000000085492420c59a4934e37300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000016531c52fb46d9d30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ca620802dbb8fb082f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a5177596d55334f4330794d574a6d4c545534596a517459545179595330304d575a695a6d45335a4451315a47496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000aadba39f0692135f5a566b930fd73878a5560a2b000000000000000000000000000000000000000000000e5e3002bee74867e491000000000000000000000000000000000000000000000e06fb5c1ac1bba5039c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x16235901559a374d9ef77b031c22364c07cbc137a5eeb0bfe70aac328d5383f1",
      "signature": {
        "s": "0x0bc2ad567c3a6feeb7347953abd044e70c1bb9d6299d35460ad4859b96b1bc63",
        "r": "0x59f6c385dcdc5575a5a6e668a15a40d3c517a9abb56cef879b6819e7d01dd078",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x76546c53f42bd016db7e2328d16e0e735a2eb6f9ff416c830db52d20c018a0d9",
      "signature": {
        "s": "0x60bd64bd380de79d353614f9f044ec1b5c6536530c8ef1e2f88bf7406a45a0f9",
        "r": "0x040868e4cb66357b9f0210ec2f7527915ecced55af87ab7e135d43d90562b40d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1608660634630019539189",
    "total": "45140581495651877546824"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1608660634630019539189",
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
            "amount": "27345138616395810670639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1608660634630019539"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NzQwYmU3OC0yMWJmLTU4YjQtYTQyYS00MWZiZmE3ZDQ1ZGIifQ==",
    "nonce": 110392,
    "balances": {
      "current": "627813688541630025115819",
      "previous": "629423957836894674674547"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaadba39f0692135f5a566b930fd73878a5560a2b",
    "nonce": 46,
    "balances": {
      "current": "67850584240468066296977",
      "previous": "66241923605838046757788"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:03.204Z",
  "updated": "2022-05-04T08:53:03.294Z",
  "id": "62723eef7832e20011830ba4"
}
```
* *stageAmount*: `67850584240468066296977`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000005734a6a4258cc2e0f50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000005734a6a4258cc2e0f500000000000000000000000000000000000000000000098f1369593e95686b4816235901559a374d9ef77b031c22364c07cbc137a5eeb0bfe70aac328d5383f159f6c385dcdc5575a5a6e668a15a40d3c517a9abb56cef879b6819e7d01dd0780bc2ad567c3a6feeb7347953abd044e70c1bb9d6299d35460ad4859b96b1bc63000000000000000000000000000000000000000000000000000000000000001b76546c53f42bd016db7e2328d16e0e735a2eb6f9ff416c830db52d20c018a0d9040868e4cb66357b9f0210ec2f7527915ecced55af87ab7e135d43d90562b40d60bd64bd380de79d353614f9f044ec1b5c6536530c8ef1e2f88bf7406a45a0f9000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074ce0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001af38000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000084f1d9270521c12b28ab0000000000000000000000000000000000000000000085492420c59a4934e37300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000016531c52fb46d9d30000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005ca620802dbb8fb082f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949344e7a5177596d55334f4330794d574a6d4c545534596a517459545179595330304d575a695a6d45335a4451315a47496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000aadba39f0692135f5a566b930fd73878a5560a2b000000000000000000000000000000000000000000000e5e3002bee74867e491000000000000000000000000000000000000000000000e06fb5c1ac1bba5039c00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x16235901559a374d9ef77b031c22364c07cbc137a5eeb0bfe70aac328d5383f1",
      "signature": {
        "s": "0x0bc2ad567c3a6feeb7347953abd044e70c1bb9d6299d35460ad4859b96b1bc63",
        "r": "0x59f6c385dcdc5575a5a6e668a15a40d3c517a9abb56cef879b6819e7d01dd078",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x76546c53f42bd016db7e2328d16e0e735a2eb6f9ff416c830db52d20c018a0d9",
      "signature": {
        "s": "0x60bd64bd380de79d353614f9f044ec1b5c6536530c8ef1e2f88bf7406a45a0f9",
        "r": "0x040868e4cb66357b9f0210ec2f7527915ecced55af87ab7e135d43d90562b40d",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1608660634630019539189",
    "total": "45140581495651877546824"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1608660634630019539189",
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
            "amount": "27345138616395810670639"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1608660634630019539"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI4NzQwYmU3OC0yMWJmLTU4YjQtYTQyYS00MWZiZmE3ZDQ1ZGIifQ==",
    "nonce": 110392,
    "balances": {
      "current": "627813688541630025115819",
      "previous": "629423957836894674674547"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xaadba39f0692135f5a566b930fd73878a5560a2b",
    "nonce": 46,
    "balances": {
      "current": "67850584240468066296977",
      "previous": "66241923605838046757788"
    }
  },
  "blockNumber": "14709966",
  "created": "2022-05-04T08:53:03.204Z",
  "updated": "2022-05-04T08:53:03.294Z",
  "id": "62723eef7832e20011830ba4"
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
0x0f200f9b000000000000000000000000000000000000000000000e5e3002bee74867e4910000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `67850584240468066296977`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`