# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB1331ed1017eDf82f59AeB4B09d7167eD60E94b5`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000760daa3941a1048e50000000000000000000000000000000000000000000000002cc85813b1123ca00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002cc85813b1123ca0000000000000000000000000000000000000000000000004e8a4a407f9fd3a3e5adf3961d180023d94358a677ac8acbe376938ef78a87890d537aaf01a4abda5fa9be558ece795c94dfd858647ac419109952b7a23852e8b8fd284eeae47cfb92a12e075856c5cf1dc84822c9d13698e0d7c2c37f162a8a772c00ff2ecc078f0000000000000000000000000000000000000000000000000000000000000001b38e9ede91da0a19e5cae0e6ddef0696c562972b338e9496927ea0504cbf1e38941727b77754829fca72f3711f84a423ebe8954e6638866c01c94a90c99b33f205ae76f1d093a30be874a9250a37abc413224388cb8a648d2b749786ad49323de000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aec7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095db2bab25e6d7f4ffc30000000000000000000000000000000000000000000095db587ef4d9c9761a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000b76df406eddc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60ed4fc6e942172de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a4d795a6a49784d6930314e5449314c5456694d575974595451334d43307a4e5467354f575131597a6b345a6d496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b1331ed1017edf82f59aeb4b09d7167ed60e94b500000000000000000000000000000000000000000000000760daa3941a1048e500000000000000000000000000000000000000000000000734124b8068fe0c4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5adf3961d180023d94358a677ac8acbe376938ef78a87890d537aaf01a4abda5",
      "signature": {
        "s": "0x2a12e075856c5cf1dc84822c9d13698e0d7c2c37f162a8a772c00ff2ecc078f0",
        "r": "0xfa9be558ece795c94dfd858647ac419109952b7a23852e8b8fd284eeae47cfb9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x38e9ede91da0a19e5cae0e6ddef0696c562972b338e9496927ea0504cbf1e389",
      "signature": {
        "s": "0x5ae76f1d093a30be874a9250a37abc413224388cb8a648d2b749786ad49323de",
        "r": "0x41727b77754829fca72f3711f84a423ebe8954e6638866c01c94a90c99b33f20",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3226925974609345696",
    "total": "90550680361983883838"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3226925974609345696",
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
            "amount": "27265356497506172760798"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3226925974609345"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjMyZjIxMi01NTI1LTViMWYtYTQ3MC0zNTg5OWQ1Yzk4ZmIifQ==",
    "nonce": 110279,
    "balances": {
      "current": "707675589550157572931523",
      "previous": "707678819703058156886564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb1331ed1017edf82f59aeb4b09d7167ed60e94b5",
    "nonce": 46,
    "balances": {
      "current": "136106278945018628325",
      "previous": "132879352970409282629"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:28.293Z",
  "updated": "2022-05-04T08:52:28.373Z",
  "id": "62723eccbbd75600116d052f"
}
```
* *stageAmount*: `136106278945018628325`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000002cc85813b1123ca00000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000002cc85813b1123ca0000000000000000000000000000000000000000000000004e8a4a407f9fd3a3e5adf3961d180023d94358a677ac8acbe376938ef78a87890d537aaf01a4abda5fa9be558ece795c94dfd858647ac419109952b7a23852e8b8fd284eeae47cfb92a12e075856c5cf1dc84822c9d13698e0d7c2c37f162a8a772c00ff2ecc078f0000000000000000000000000000000000000000000000000000000000000001b38e9ede91da0a19e5cae0e6ddef0696c562972b338e9496927ea0504cbf1e38941727b77754829fca72f3711f84a423ebe8954e6638866c01c94a90c99b33f205ae76f1d093a30be874a9250a37abc413224388cb8a648d2b749786ad49323de000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aec7000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095db2bab25e6d7f4ffc30000000000000000000000000000000000000000000095db587ef4d9c9761a2400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000b76df406eddc10000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60ed4fc6e942172de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6a4d795a6a49784d6930314e5449314c5456694d575974595451334d43307a4e5467354f575131597a6b345a6d496966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000b1331ed1017edf82f59aeb4b09d7167ed60e94b500000000000000000000000000000000000000000000000760daa3941a1048e500000000000000000000000000000000000000000000000734124b8068fe0c4500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x5adf3961d180023d94358a677ac8acbe376938ef78a87890d537aaf01a4abda5",
      "signature": {
        "s": "0x2a12e075856c5cf1dc84822c9d13698e0d7c2c37f162a8a772c00ff2ecc078f0",
        "r": "0xfa9be558ece795c94dfd858647ac419109952b7a23852e8b8fd284eeae47cfb9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x38e9ede91da0a19e5cae0e6ddef0696c562972b338e9496927ea0504cbf1e389",
      "signature": {
        "s": "0x5ae76f1d093a30be874a9250a37abc413224388cb8a648d2b749786ad49323de",
        "r": "0x41727b77754829fca72f3711f84a423ebe8954e6638866c01c94a90c99b33f20",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "3226925974609345696",
    "total": "90550680361983883838"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "3226925974609345696",
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
            "amount": "27265356497506172760798"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "3226925974609345"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNjMyZjIxMi01NTI1LTViMWYtYTQ3MC0zNTg5OWQ1Yzk4ZmIifQ==",
    "nonce": 110279,
    "balances": {
      "current": "707675589550157572931523",
      "previous": "707678819703058156886564"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb1331ed1017edf82f59aeb4b09d7167ed60e94b5",
    "nonce": 46,
    "balances": {
      "current": "136106278945018628325",
      "previous": "132879352970409282629"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:28.293Z",
  "updated": "2022-05-04T08:52:28.373Z",
  "id": "62723eccbbd75600116d052f"
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
0x0f200f9b00000000000000000000000000000000000000000000000760daa3941a1048e50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `136106278945018628325`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`