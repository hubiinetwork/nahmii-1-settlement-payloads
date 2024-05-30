# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xdd23a2deBf80AEfA2A5029F76CCF4D93e70DdcaC`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000200b84fceb2dfdac5000000000000000000000000000000000000000000000000af92cd32cbe519e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000af92cd32cbe519e500000000000000000000000000000000000000000000000200b84fceb2dfdac59fac16ea37d899e5f3e209f88cb1f1155894ebd2774fc707dc0184e53de37e5bdec152ea15d82b1cd843299932ef3771aa9b4780b01e1f3edb3643405e0426372b0d62ac2c52b7237384d7f447aa3fa6391aa28b04ee7fcfff8a7448fa14c3f7000000000000000000000000000000000000000000000000000000000000001c9df3562ecca8dd308154e515d0df2aca73773f4fd0ccb462d0986a5f0203078dabbd031c1d0717d145dfc4a3fb4a49dfbb0df2f0595bb44147b0c4581d9117ad17589bcb0dbd8cb928efdb515df5b26455c6497bc052904231133c02927b8688000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b800000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000b6e9ef058090245f86b000000000000000000000000000000000000000000000b6f4eb0179d64635d5800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002cf26196384b080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e97586a8c0e4e74bab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6a4a6a4f5441774e4330344f5445334c5455334d54497459546b304e5330305a57566d4f4755344e4749345a6d456966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000dd23a2debf80aefa2a5029f76ccf4d93e70ddcac00000000000000000000000000000000000000000000000200b84fceb2dfdac50000000000000000000000000000000000000000000000015125829be6fac0e000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fac16ea37d899e5f3e209f88cb1f1155894ebd2774fc707dc0184e53de37e5b",
      "signature": {
        "s": "0x2b0d62ac2c52b7237384d7f447aa3fa6391aa28b04ee7fcfff8a7448fa14c3f7",
        "r": "0xdec152ea15d82b1cd843299932ef3771aa9b4780b01e1f3edb3643405e042637",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9df3562ecca8dd308154e515d0df2aca73773f4fd0ccb462d0986a5f0203078d",
      "signature": {
        "s": "0x17589bcb0dbd8cb928efdb515df5b26455c6497bc052904231133c02927b8688",
        "r": "0xabbd031c1d0717d145dfc4a3fb4a49dfbb0df2f0595bb44147b0c4581d9117ad",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12651399921289992677",
    "total": "36945367292316736197"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12651399921289992677",
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
            "amount": "27918392425218295942059"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12651399921289992"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZjJjOTAwNC04OTE3LTU3MTItYTk0NS00ZWVmOGU4NGI4ZmEifQ==",
    "nonce": 112640,
    "balances": {
      "current": "53986625910322267289707",
      "previous": "53999289961643478572376"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd23a2debf80aefa2a5029f76ccf4d93e70ddcac",
    "nonce": 5,
    "balances": {
      "current": "36945367292316736197",
      "previous": "24293967371026743520"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:56.526Z",
  "updated": "2022-05-04T09:04:56.614Z",
  "id": "627241b87832e20011830e96"
}
```
* *stageAmount*: `36945367292316736197`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000af92cd32cbe519e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000af92cd32cbe519e500000000000000000000000000000000000000000000000200b84fceb2dfdac59fac16ea37d899e5f3e209f88cb1f1155894ebd2774fc707dc0184e53de37e5bdec152ea15d82b1cd843299932ef3771aa9b4780b01e1f3edb3643405e0426372b0d62ac2c52b7237384d7f447aa3fa6391aa28b04ee7fcfff8a7448fa14c3f7000000000000000000000000000000000000000000000000000000000000001c9df3562ecca8dd308154e515d0df2aca73773f4fd0ccb462d0986a5f0203078dabbd031c1d0717d145dfc4a3fb4a49dfbb0df2f0595bb44147b0c4581d9117ad17589bcb0dbd8cb928efdb515df5b26455c6497bc052904231133c02927b8688000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ee0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b800000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000000b6e9ef058090245f86b000000000000000000000000000000000000000000000b6f4eb0179d64635d5800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000002cf26196384b080000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e97586a8c0e4e74bab0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6c5a6a4a6a4f5441774e4330344f5445334c5455334d54497459546b304e5330305a57566d4f4755344e4749345a6d456966513d3d0000000000000000000000000000000000000000000000000000000000000005000000000000000000000000dd23a2debf80aefa2a5029f76ccf4d93e70ddcac00000000000000000000000000000000000000000000000200b84fceb2dfdac50000000000000000000000000000000000000000000000015125829be6fac0e000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9fac16ea37d899e5f3e209f88cb1f1155894ebd2774fc707dc0184e53de37e5b",
      "signature": {
        "s": "0x2b0d62ac2c52b7237384d7f447aa3fa6391aa28b04ee7fcfff8a7448fa14c3f7",
        "r": "0xdec152ea15d82b1cd843299932ef3771aa9b4780b01e1f3edb3643405e042637",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x9df3562ecca8dd308154e515d0df2aca73773f4fd0ccb462d0986a5f0203078d",
      "signature": {
        "s": "0x17589bcb0dbd8cb928efdb515df5b26455c6497bc052904231133c02927b8688",
        "r": "0xabbd031c1d0717d145dfc4a3fb4a49dfbb0df2f0595bb44147b0c4581d9117ad",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "12651399921289992677",
    "total": "36945367292316736197"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "12651399921289992677",
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
            "amount": "27918392425218295942059"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "12651399921289992"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJlZjJjOTAwNC04OTE3LTU3MTItYTk0NS00ZWVmOGU4NGI4ZmEifQ==",
    "nonce": 112640,
    "balances": {
      "current": "53986625910322267289707",
      "previous": "53999289961643478572376"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xdd23a2debf80aefa2a5029f76ccf4d93e70ddcac",
    "nonce": 5,
    "balances": {
      "current": "36945367292316736197",
      "previous": "24293967371026743520"
    }
  },
  "blockNumber": "14709998",
  "created": "2022-05-04T09:04:56.526Z",
  "updated": "2022-05-04T09:04:56.614Z",
  "id": "627241b87832e20011830e96"
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
0x0f200f9b00000000000000000000000000000000000000000000000200b84fceb2dfdac50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `36945367292316736197`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`