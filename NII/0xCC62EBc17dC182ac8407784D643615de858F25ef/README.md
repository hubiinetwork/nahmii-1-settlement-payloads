# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xCC62EBc17dC182ac8407784D643615de858F25ef`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000047a5fe0964c92e459b000000000000000000000000000000000000000000000001b2de2eeb7204779e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b2de2eeb7204779e00000000000000000000000000000000000000000000002faad0f1c45483a82318283dbb0f7e223eda8d24226b6eedf04d16cbdab4f04c0ccb8ee422d809895b4033ca3872c734608bd08a63854ccabc93cd604797420f13762338125263271841837d9b6e1ed8f0bf1e15036552e6acc8300e9df4354e3eb0bfa443c8ba12e3000000000000000000000000000000000000000000000000000000000000001c319d9a1a207e98cfddcd68e805f7df0f351c9da1df4fea16f9cb7cce0e0a4fa75085c183b4c19cd404260dd6421e026abd01fd1d8e73e7fd184e5884e74309ae407d095c06f2f62912709d11c15a11fa17e0526e700b204a3cacf5401a34f1b7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b247000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004938ffc4138db12bd39000000000000000000000000000000000000000000000493ab31195f9e288dfc700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000006f5380bf5894990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a8110fa18f90e4270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a4e6a4f446731596930304f44646a4c5456694f574d744f57497a4d7930304e5463324e324d305a57466a4e6a516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cc62ebc17dc182ac8407784d643615de858f25ef000000000000000000000000000000000000000000000047a5fe0964c92e459b000000000000000000000000000000000000000000000045f31fda795729cdfd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18283dbb0f7e223eda8d24226b6eedf04d16cbdab4f04c0ccb8ee422d809895b",
      "signature": {
        "s": "0x41837d9b6e1ed8f0bf1e15036552e6acc8300e9df4354e3eb0bfa443c8ba12e3",
        "r": "0x4033ca3872c734608bd08a63854ccabc93cd604797420f137623381252632718",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x319d9a1a207e98cfddcd68e805f7df0f351c9da1df4fea16f9cb7cce0e0a4fa7",
      "signature": {
        "s": "0x407d095c06f2f62912709d11c15a11fa17e0526e700b204a3cacf5401a34f1b7",
        "r": "0x5085c183b4c19cd404260dd6421e026abd01fd1d8e73e7fd184e5884e74309ae",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31335534846055577502",
    "total": "879305575071486289955"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31335534846055577502",
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
            "amount": "27626886356402747532327"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31335534846055577"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0ZjNjODg1Yi00ODdjLTViOWMtOWIzMy00NTc2N2M0ZWFjNjQifQ==",
    "nonce": 111175,
    "balances": {
      "current": "345784200794686226158480",
      "previous": "345815567665067127791559"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcc62ebc17dc182ac8407784d643615de858f25ef",
    "nonce": 46,
    "balances": {
      "current": "1321679837222197413275",
      "previous": "1290344302376141835773"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:56.829Z",
  "updated": "2022-05-04T08:56:56.909Z",
  "id": "62723fd83592fd001130b5d0"
}
```
* *stageAmount*: `1321679837222197413275`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000001b2de2eeb7204779e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000001b2de2eeb7204779e00000000000000000000000000000000000000000000002faad0f1c45483a82318283dbb0f7e223eda8d24226b6eedf04d16cbdab4f04c0ccb8ee422d809895b4033ca3872c734608bd08a63854ccabc93cd604797420f13762338125263271841837d9b6e1ed8f0bf1e15036552e6acc8300e9df4354e3eb0bfa443c8ba12e3000000000000000000000000000000000000000000000000000000000000001c319d9a1a207e98cfddcd68e805f7df0f351c9da1df4fea16f9cb7cce0e0a4fa75085c183b4c19cd404260dd6421e026abd01fd1d8e73e7fd184e5884e74309ae407d095c06f2f62912709d11c15a11fa17e0526e700b204a3cacf5401a34f1b7000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b247000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004938ffc4138db12bd39000000000000000000000000000000000000000000000493ab31195f9e288dfc700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000006f5380bf5894990000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9a8110fa18f90e4270000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949305a6a4e6a4f446731596930304f44646a4c5456694f574d744f57497a4d7930304e5463324e324d305a57466a4e6a516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000cc62ebc17dc182ac8407784d643615de858f25ef000000000000000000000000000000000000000000000047a5fe0964c92e459b000000000000000000000000000000000000000000000045f31fda795729cdfd00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x18283dbb0f7e223eda8d24226b6eedf04d16cbdab4f04c0ccb8ee422d809895b",
      "signature": {
        "s": "0x41837d9b6e1ed8f0bf1e15036552e6acc8300e9df4354e3eb0bfa443c8ba12e3",
        "r": "0x4033ca3872c734608bd08a63854ccabc93cd604797420f137623381252632718",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x319d9a1a207e98cfddcd68e805f7df0f351c9da1df4fea16f9cb7cce0e0a4fa7",
      "signature": {
        "s": "0x407d095c06f2f62912709d11c15a11fa17e0526e700b204a3cacf5401a34f1b7",
        "r": "0x5085c183b4c19cd404260dd6421e026abd01fd1d8e73e7fd184e5884e74309ae",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31335534846055577502",
    "total": "879305575071486289955"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31335534846055577502",
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
            "amount": "27626886356402747532327"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31335534846055577"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0ZjNjODg1Yi00ODdjLTViOWMtOWIzMy00NTc2N2M0ZWFjNjQifQ==",
    "nonce": 111175,
    "balances": {
      "current": "345784200794686226158480",
      "previous": "345815567665067127791559"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xcc62ebc17dc182ac8407784d643615de858f25ef",
    "nonce": 46,
    "balances": {
      "current": "1321679837222197413275",
      "previous": "1290344302376141835773"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:56.829Z",
  "updated": "2022-05-04T08:56:56.909Z",
  "id": "62723fd83592fd001130b5d0"
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
0x0f200f9b000000000000000000000000000000000000000000000047a5fe0964c92e459b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1321679837222197413275`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`