# Settlement of NII
This document presents recommended in order to settle the Nahmii 1 balance of NII of account `0xd8950C2C719D3831762F872254C4DAccB8fFC680`.

The ordered steps of contract function invocations are included below and in the corresponding [steps.json](./steps.json). Please read [the general recipe for settling Nahmii 1 balance](../../README.md) before starting on the first step of settlement.
## Ordered steps
### Step 1
#### Contract
*DriipSettlementChallengeByPayment* ([0x906fd331f5e382f05b8ae26900140c37f0db139a](https://etherscan.io/address/0x906fd331f5e382f05b8ae26900140c37f0db139a#code))
#### Method name
*startChallengeFromPayment*
#### Method payload
```
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000003aba84149548c91d2a00000000000000000000000000000000000000000000000686cb3f94d9f1f1200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000686cb3f94d9f1f1200000000000000000000000000000000000000000000000532380dd5c411a9d2ae88e88430ffb951d38b5111ddf57d6491dd0b647888f03c618d5b5ee1465c501c875da60fd580034a33c17040639ff26da7c3ed49adb1a65c8b9fc8cb61d8270624019ae39d4efb7121d1c62931f0d7062c60f6042f67e6f281d1fbcf99d4a5b000000000000000000000000000000000000000000000000000000000000001ba17fc13f2ef655659c74bd60a61be95bb2013b01c0315b911802ed58c95968497468338f8645863d236b6504863ef46c42832c9cadabf12704bc99df411536a7420fb2881e9246c5d19cdc44e2d31ab055c2693f25707f1cd0256fc595e4b5a4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b544000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034cd3722d1bd0e78c45d0000000000000000000000000000000000000000000034d3bf99ca78b675726600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001abb926ce0abce90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dee10ad41bc25da8e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a474d7a4e444a6d4e6930345a6d45334c5455774f44497459546b7959533030597a4a6a4e5749784f4455314f54496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d8950c2c719d3831762f872254c4daccb8ffc68000000000000000000000000000000000000000000000003aba84149548c91d2a00000000000000000000000000000000000000000000003433b8d5006ed72c0a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xe88e88430ffb951d38b5111ddf57d6491dd0b647888f03c618d5b5ee1465c501",
      "signature": {
        "s": "0x624019ae39d4efb7121d1c62931f0d7062c60f6042f67e6f281d1fbcf99d4a5b",
        "r": "0xc875da60fd580034a33c17040639ff26da7c3ed49adb1a65c8b9fc8cb61d8270",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa17fc13f2ef655659c74bd60a61be95bb2013b01c0315b911802ed58c9596849",
      "signature": {
        "s": "0x420fb2881e9246c5d19cdc44e2d31ab055c2693f25707f1cd0256fc595e4b5a4",
        "r": "0x7468338f8645863d236b6504863ef46c42832c9cadabf12704bc99df411536a7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "120393391372156137760",
    "total": "1533638046094538218794"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "120393391372156137760",
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
            "amount": "27723225605335737542884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "120393391372156137"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZGMzNDJmNi04ZmE3LTUwODItYTkyYS00YzJjNWIxODU1OTIifQ==",
    "nonce": 111940,
    "balances": {
      "current": "249348612612763225211997",
      "previous": "249469126397526753505894"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd8950c2c719d3831762f872254c4daccb8ffc680",
    "nonce": 22,
    "balances": {
      "current": "1083351046094538218794",
      "previous": "962957654722382081034"
    }
  },
  "blockNumber": "14709985",
  "created": "2022-05-04T09:01:09.128Z",
  "updated": "2022-05-04T09:01:09.266Z",
  "id": "627240d53592fd001130b6e1"
}
```
* *stageAmount*: `1083351046094538218794`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2#code))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000686cb3f94d9f1f1200000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000686cb3f94d9f1f1200000000000000000000000000000000000000000000000532380dd5c411a9d2ae88e88430ffb951d38b5111ddf57d6491dd0b647888f03c618d5b5ee1465c501c875da60fd580034a33c17040639ff26da7c3ed49adb1a65c8b9fc8cb61d8270624019ae39d4efb7121d1c62931f0d7062c60f6042f67e6f281d1fbcf99d4a5b000000000000000000000000000000000000000000000000000000000000001ba17fc13f2ef655659c74bd60a61be95bb2013b01c0315b911802ed58c95968497468338f8645863d236b6504863ef46c42832c9cadabf12704bc99df411536a7420fb2881e9246c5d19cdc44e2d31ab055c2693f25707f1cd0256fc595e4b5a4000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b544000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000034cd3722d1bd0e78c45d0000000000000000000000000000000000000000000034d3bf99ca78b675726600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000001abb926ce0abce90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dee10ad41bc25da8e40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949355a474d7a4e444a6d4e6930345a6d45334c5455774f44497459546b7959533030597a4a6a4e5749784f4455314f54496966513d3d0000000000000000000000000000000000000000000000000000000000000016000000000000000000000000d8950c2c719d3831762f872254c4daccb8ffc68000000000000000000000000000000000000000000000003aba84149548c91d2a00000000000000000000000000000000000000000000003433b8d5006ed72c0a00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *payment*:
```{
  "seals": {
    "wallet": {
      "hash": "0xe88e88430ffb951d38b5111ddf57d6491dd0b647888f03c618d5b5ee1465c501",
      "signature": {
        "s": "0x624019ae39d4efb7121d1c62931f0d7062c60f6042f67e6f281d1fbcf99d4a5b",
        "r": "0xc875da60fd580034a33c17040639ff26da7c3ed49adb1a65c8b9fc8cb61d8270",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xa17fc13f2ef655659c74bd60a61be95bb2013b01c0315b911802ed58c9596849",
      "signature": {
        "s": "0x420fb2881e9246c5d19cdc44e2d31ab055c2693f25707f1cd0256fc595e4b5a4",
        "r": "0x7468338f8645863d236b6504863ef46c42832c9cadabf12704bc99df411536a7",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "120393391372156137760",
    "total": "1533638046094538218794"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "120393391372156137760",
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
            "amount": "27723225605335737542884"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "120393391372156137"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5ZGMzNDJmNi04ZmE3LTUwODItYTkyYS00YzJjNWIxODU1OTIifQ==",
    "nonce": 111940,
    "balances": {
      "current": "249348612612763225211997",
      "previous": "249469126397526753505894"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd8950c2c719d3831762f872254c4daccb8ffc680",
    "nonce": 22,
    "balances": {
      "current": "1083351046094538218794",
      "previous": "962957654722382081034"
    }
  },
  "blockNumber": "14709985",
  "created": "2022-05-04T09:01:09.128Z",
  "updated": "2022-05-04T09:01:09.266Z",
  "id": "627240d53592fd001130b6e1"
}
```
* *standard*: `ERC20`
### Step 3
#### Contract
*ClientFund* ([0xcc8d82f6ba952966e63001c7b320eef2ae729099](https://etherscan.io/address/0xcc8d82f6ba952966e63001c7b320eef2ae729099#code))
#### Method name
*withdraw*
#### Method payload
```
0x0f200f9b00000000000000000000000000000000000000000000003aba84149548c91d2a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encoded method args
* *value*: `1083351046094538218794`
* *currencyCt*: `0x7c8155909cd385f120a56ef90728dd50f9ccbe52`
* *currencyId*: `0`
* *standard*: `ERC20`