# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xEC63913528365fc4B845df57171b63D71eC68442`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000000000000000000000000000000010d92f57ecee423e5b7a8f72594eb6ba82d829cd9bcbcf8d13b4da1680833534493517d0272d317dfb04b9003ceb0173814e0e11e0ab6223eecb56e14a98435c8f7ebce15675fd1b9020ac43d490a9f8e5a5e0d9441aca9873bf511ad3c8fe555b524b6105e11a000000000000000000000000000000000000000000000000000000000000001c81b705c94f88cbaade1190a02c60181abf14c90f38035f5e7943128096bbb3e5135e1ef7c190e1ca107315b54005d85a6d84ee41acb49fc5e42eaf6feb7da55a7ee7c8e3d4102ae2ff39d3cf968235d8c2056de0db3f729406ea9f7a18600bbf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000a18e2b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000bb55000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017d67aeace3ed73f7d870000000000000000000000000000000000000000000017d67afbabbe5c0fbadf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000004502ce34f160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000017502eaab7f3e67ed340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f54517a4d5449795a69316c4d5467324c54557a4f574d74596a4532597930794f57493359324532597a49315957456966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ec63913528365fc4b845df57171b63d71ec684420000000000000000000000000000000000000000000000000010d92f57ecee42000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e5b7a8f72594eb6ba82d829cd9bcbcf8d13b4da1680833534493517d0272d31",
      "signature": {
        "s": "0x1b9020ac43d490a9f8e5a5e0d9441aca9873bf511ad3c8fe555b524b6105e11a",
        "r": "0x7dfb04b9003ceb0173814e0e11e0ab6223eecb56e14a98435c8f7ebce15675fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x81b705c94f88cbaade1190a02c60181abf14c90f38035f5e7943128096bbb3e5",
      "signature": {
        "s": "0x7ee7c8e3d4102ae2ff39d3cf968235d8c2056de0db3f729406ea9f7a18600bbf",
        "r": "0x135e1ef7c190e1ca107315b54005d85a6d84ee41acb49fc5e42eaf6feb7da55a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4742396989206082",
    "total": "4742396989206082"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4742396989206082",
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
            "amount": "6880845708389285096756"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4742396989206"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2OTQzMTIyZi1lMTg2LTUzOWMtYjE2Yy0yOWI3Y2E2YzI1YWEifQ==",
    "nonce": 47957,
    "balances": {
      "current": "112570889456162156019079",
      "previous": "112570894203301542214367"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xec63913528365fc4b845df57171b63d71ec68442",
    "nonce": 1,
    "balances": {
      "current": "4742396989206082",
      "previous": "0"
    }
  },
  "blockNumber": "10587691",
  "created": "2020-08-03T15:46:55.466Z",
  "updated": "2020-08-03T15:46:55.539Z",
  "id": "5f28316f6b6add00111700f3"
}
```
* *stageAmount*: `4742396989206082`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000000000000000000000000000000010d92f57ecee423e5b7a8f72594eb6ba82d829cd9bcbcf8d13b4da1680833534493517d0272d317dfb04b9003ceb0173814e0e11e0ab6223eecb56e14a98435c8f7ebce15675fd1b9020ac43d490a9f8e5a5e0d9441aca9873bf511ad3c8fe555b524b6105e11a000000000000000000000000000000000000000000000000000000000000001c81b705c94f88cbaade1190a02c60181abf14c90f38035f5e7943128096bbb3e5135e1ef7c190e1ca107315b54005d85a6d84ee41acb49fc5e42eaf6feb7da55a7ee7c8e3d4102ae2ff39d3cf968235d8c2056de0db3f729406ea9f7a18600bbf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000a18e2b0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000000bb55000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000017d67aeace3ed73f7d870000000000000000000000000000000000000000000017d67afbabbe5c0fbadf00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000004502ce34f160000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000017502eaab7f3e67ed340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324f54517a4d5449795a69316c4d5467324c54557a4f574d74596a4532597930794f57493359324532597a49315957456966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000ec63913528365fc4b845df57171b63d71ec684420000000000000000000000000000000000000000000000000010d92f57ecee42000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3e5b7a8f72594eb6ba82d829cd9bcbcf8d13b4da1680833534493517d0272d31",
      "signature": {
        "s": "0x1b9020ac43d490a9f8e5a5e0d9441aca9873bf511ad3c8fe555b524b6105e11a",
        "r": "0x7dfb04b9003ceb0173814e0e11e0ab6223eecb56e14a98435c8f7ebce15675fd",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x81b705c94f88cbaade1190a02c60181abf14c90f38035f5e7943128096bbb3e5",
      "signature": {
        "s": "0x7ee7c8e3d4102ae2ff39d3cf968235d8c2056de0db3f729406ea9f7a18600bbf",
        "r": "0x135e1ef7c190e1ca107315b54005d85a6d84ee41acb49fc5e42eaf6feb7da55a",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4742396989206082",
    "total": "4742396989206082"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4742396989206082",
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
            "amount": "6880845708389285096756"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4742396989206"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2OTQzMTIyZi1lMTg2LTUzOWMtYjE2Yy0yOWI3Y2E2YzI1YWEifQ==",
    "nonce": 47957,
    "balances": {
      "current": "112570889456162156019079",
      "previous": "112570894203301542214367"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xec63913528365fc4b845df57171b63d71ec68442",
    "nonce": 1,
    "balances": {
      "current": "4742396989206082",
      "previous": "0"
    }
  },
  "blockNumber": "10587691",
  "created": "2020-08-03T15:46:55.466Z",
  "updated": "2020-08-03T15:46:55.539Z",
  "id": "5f28316f6b6add00111700f3"
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
0x0f200f9b0000000000000000000000000000000000000000000000000010d92f57ecee420000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4742396989206082`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`