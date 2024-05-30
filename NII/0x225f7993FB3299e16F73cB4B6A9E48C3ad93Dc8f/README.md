# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x225f7993FB3299e16F73cB4B6A9E48C3ad93Dc8f`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000000000000000000000000000003fcef5b87ed3933e3ff17c7d04ba3cb03300bdf24e6f2046ca100c4208ebfa909565f94a13050204078a604419d851bafe5a1a9cf93e01a45de4661e72833745d960c472bc27d24e1544d15848dbf4ef808ab86897f18faffa1b83034c35d9a65a82ccd58b27bb82000000000000000000000000000000000000000000000000000000000000001cb1079c71881fad3d8037d1b13a73c9aeb7cde04976cc07635d79caaee8dcd0257c2dd320e79faf9415cc7d78d69c0b6b18aefff580781e0c3c9807896512238d1df23f43a27373cc57bd06dbe04a17e5072a044b99c6431c815e67a7cea17ecf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e36000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022d71d7d38d7ccf6bc940000000000000000000000000000000000000000000022d75d5c8450397c2ff700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001055bfedb1e0250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038fc1d13995eca6b00f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d5455334d575a684d79307a4e7a52684c54566d4e475974595441334d53316b4f4451304e545a6d5a6d55334d324d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000225f7993fb3299e16f73cb4b6a9e48c3ad93dc8f0000000000000000000000000000000000000000000000003fcef5b87ed3933e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3ff17c7d04ba3cb03300bdf24e6f2046ca100c4208ebfa909565f94a13050204",
      "signature": {
        "s": "0x1544d15848dbf4ef808ab86897f18faffa1b83034c35d9a65a82ccd58b27bb82",
        "r": "0x078a604419d851bafe5a1a9cf93e01a45de4661e72833745d960c472bc27d24e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb1079c71881fad3d8037d1b13a73c9aeb7cde04976cc07635d79caaee8dcd025",
      "signature": {
        "s": "0x1df23f43a27373cc57bd06dbe04a17e5072a044b99c6431c815e67a7cea17ecf",
        "r": "0x7c2dd320e79faf9415cc7d78d69c0b6b18aefff580781e0c3c9807896512238d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4597882442342437694",
    "total": "4597882442342437694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4597882442342437694",
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
            "amount": "16818949858384937398287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4597882442342437"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMTU3MWZhMy0zNzRhLTVmNGYtYTA3MS1kODQ0NTZmZmU3M2MifQ==",
    "nonce": 77366,
    "balances": {
      "current": "164528635310514187451540",
      "previous": "164533237790838972231671"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x225f7993fb3299e16f73cb4b6a9e48c3ad93dc8f",
    "nonce": 1,
    "balances": {
      "current": "4597882442342437694",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:48.384Z",
  "updated": "2021-06-04T12:46:48.499Z",
  "id": "60ba20b83a79970010e7b0ae"
}
```
* *stageAmount*: `4597882442342437694`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000000000000000000000000000003fcef5b87ed3933e3ff17c7d04ba3cb03300bdf24e6f2046ca100c4208ebfa909565f94a13050204078a604419d851bafe5a1a9cf93e01a45de4661e72833745d960c472bc27d24e1544d15848dbf4ef808ab86897f18faffa1b83034c35d9a65a82ccd58b27bb82000000000000000000000000000000000000000000000000000000000000001cb1079c71881fad3d8037d1b13a73c9aeb7cde04976cc07635d79caaee8dcd0257c2dd320e79faf9415cc7d78d69c0b6b18aefff580781e0c3c9807896512238d1df23f43a27373cc57bd06dbe04a17e5072a044b99c6431c815e67a7cea17ecf000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e200000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012e36000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000022d71d7d38d7ccf6bc940000000000000000000000000000000000000000000022d75d5c8450397c2ff700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001055bfedb1e0250000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038fc1d13995eca6b00f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d4d5455334d575a684d79307a4e7a52684c54566d4e475974595441334d53316b4f4451304e545a6d5a6d55334d324d6966513d3d0000000000000000000000000000000000000000000000000000000000000001000000000000000000000000225f7993fb3299e16f73cb4b6a9e48c3ad93dc8f0000000000000000000000000000000000000000000000003fcef5b87ed3933e000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x3ff17c7d04ba3cb03300bdf24e6f2046ca100c4208ebfa909565f94a13050204",
      "signature": {
        "s": "0x1544d15848dbf4ef808ab86897f18faffa1b83034c35d9a65a82ccd58b27bb82",
        "r": "0x078a604419d851bafe5a1a9cf93e01a45de4661e72833745d960c472bc27d24e",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xb1079c71881fad3d8037d1b13a73c9aeb7cde04976cc07635d79caaee8dcd025",
      "signature": {
        "s": "0x1df23f43a27373cc57bd06dbe04a17e5072a044b99c6431c815e67a7cea17ecf",
        "r": "0x7c2dd320e79faf9415cc7d78d69c0b6b18aefff580781e0c3c9807896512238d",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4597882442342437694",
    "total": "4597882442342437694"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4597882442342437694",
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
            "amount": "16818949858384937398287"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4597882442342437"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmMTU3MWZhMy0zNzRhLTVmNGYtYTA3MS1kODQ0NTZmZmU3M2MifQ==",
    "nonce": 77366,
    "balances": {
      "current": "164528635310514187451540",
      "previous": "164533237790838972231671"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x225f7993fb3299e16f73cb4b6a9e48c3ad93dc8f",
    "nonce": 1,
    "balances": {
      "current": "4597882442342437694",
      "previous": "0"
    }
  },
  "blockNumber": "12568034",
  "created": "2021-06-04T12:46:48.384Z",
  "updated": "2021-06-04T12:46:48.499Z",
  "id": "60ba20b83a79970010e7b0ae"
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
0x0f200f9b0000000000000000000000000000000000000000000000003fcef5b87ed3933e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `4597882442342437694`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`