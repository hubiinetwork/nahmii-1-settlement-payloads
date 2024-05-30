# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x14931bf7B62B8cec8Bb2E993f1E4F7985875Ad1b`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000012adb7b8da080ca400000000000000000000000000000000000000000000000005fac4d159a67ee80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000005fac4d159a67ee800000000000000000000000000000000000000000000000012adb7b8da080ca44d038d50966bb8f02e41958e9e3fc4c610d0cf374e7b27ed8d1e4ea52ff97218338295fda4f966cd5f1ad45a3c96bd002aac55c1756cd1c1c5cd418af56f94315a69e6152385f3516abbb73ac0fed2efd95680cdd8aaf64f30cf02e4f18dc0d1000000000000000000000000000000000000000000000000000000000000001c3d13eca8d1f8f7f92fffb34cf45129679e50992152d4dfa50ce5eac9b1964929d6f579c516602b121b0cba9873e211a2abb29cac83f046ea932f29aefca3c83104760674a7f2bf857f37dbaeea920f44ef06cc5e8429cdb2eebf72832b735a42000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023d768a574bcd122c8580000000000000000000000000000000000000000000023d76ea1c16ea1ea780400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000187e0772130c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f80458c630eeaac470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6d5533595759314f53316a5a474a6a4c5455304e474d744f44566c4e43316c4e546732596a67314e3249304e574d6966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000014931bf7b62b8cec8bb2e993f1e4f7985875ad1b00000000000000000000000000000000000000000000000012adb7b8da080ca40000000000000000000000000000000000000000000000000cb2f2e780618dbc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d038d50966bb8f02e41958e9e3fc4c610d0cf374e7b27ed8d1e4ea52ff97218",
      "signature": {
        "s": "0x5a69e6152385f3516abbb73ac0fed2efd95680cdd8aaf64f30cf02e4f18dc0d1",
        "r": "0x338295fda4f966cd5f1ad45a3c96bd002aac55c1756cd1c1c5cd418af56f9431",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d13eca8d1f8f7f92fffb34cf45129679e50992152d4dfa50ce5eac9b1964929",
      "signature": {
        "s": "0x04760674a7f2bf857f37dbaeea920f44ef06cc5e8429cdb2eebf72832b735a42",
        "r": "0xd6f579c516602b121b0cba9873e211a2abb29cac83f046ea932f29aefca3c831",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "430873117798596328",
    "total": "1345933868213472420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "430873117798596328",
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
            "amount": "16814226799316729244743"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "430873117798596"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MmU3YWY1OS1jZGJjLTU0NGMtODVlNC1lNTg2Yjg1N2I0NWMifQ==",
    "nonce": 77197,
    "balances": {
      "current": "169256417437790549231704",
      "previous": "169256848741781465626628"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x14931bf7b62b8cec8bb2e993f1e4f7985875ad1b",
    "nonce": 2,
    "balances": {
      "current": "1345933868213472420",
      "previous": "915060750414876092"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:46:03.197Z",
  "updated": "2021-06-04T12:46:03.274Z",
  "id": "60ba208b3a79970010e7b071"
}
```
* *stageAmount*: `1345933868213472420`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000005fac4d159a67ee80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000005fac4d159a67ee800000000000000000000000000000000000000000000000012adb7b8da080ca44d038d50966bb8f02e41958e9e3fc4c610d0cf374e7b27ed8d1e4ea52ff97218338295fda4f966cd5f1ad45a3c96bd002aac55c1756cd1c1c5cd418af56f94315a69e6152385f3516abbb73ac0fed2efd95680cdd8aaf64f30cf02e4f18dc0d1000000000000000000000000000000000000000000000000000000000000001c3d13eca8d1f8f7f92fffb34cf45129679e50992152d4dfa50ce5eac9b1964929d6f579c516602b121b0cba9873e211a2abb29cac83f046ea932f29aefca3c83104760674a7f2bf857f37dbaeea920f44ef06cc5e8429cdb2eebf72832b735a42000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d8d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023d768a574bcd122c8580000000000000000000000000000000000000000000023d76ea1c16ea1ea780400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000187e0772130c40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f80458c630eeaac470000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354d6d5533595759314f53316a5a474a6a4c5455304e474d744f44566c4e43316c4e546732596a67314e3249304e574d6966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000014931bf7b62b8cec8bb2e993f1e4f7985875ad1b00000000000000000000000000000000000000000000000012adb7b8da080ca40000000000000000000000000000000000000000000000000cb2f2e780618dbc00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x4d038d50966bb8f02e41958e9e3fc4c610d0cf374e7b27ed8d1e4ea52ff97218",
      "signature": {
        "s": "0x5a69e6152385f3516abbb73ac0fed2efd95680cdd8aaf64f30cf02e4f18dc0d1",
        "r": "0x338295fda4f966cd5f1ad45a3c96bd002aac55c1756cd1c1c5cd418af56f9431",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3d13eca8d1f8f7f92fffb34cf45129679e50992152d4dfa50ce5eac9b1964929",
      "signature": {
        "s": "0x04760674a7f2bf857f37dbaeea920f44ef06cc5e8429cdb2eebf72832b735a42",
        "r": "0xd6f579c516602b121b0cba9873e211a2abb29cac83f046ea932f29aefca3c831",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "430873117798596328",
    "total": "1345933868213472420"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "430873117798596328",
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
            "amount": "16814226799316729244743"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "430873117798596"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5MmU3YWY1OS1jZGJjLTU0NGMtODVlNC1lNTg2Yjg1N2I0NWMifQ==",
    "nonce": 77197,
    "balances": {
      "current": "169256417437790549231704",
      "previous": "169256848741781465626628"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x14931bf7b62b8cec8bb2e993f1e4f7985875ad1b",
    "nonce": 2,
    "balances": {
      "current": "1345933868213472420",
      "previous": "915060750414876092"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:46:03.197Z",
  "updated": "2021-06-04T12:46:03.274Z",
  "id": "60ba208b3a79970010e7b071"
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
0x0f200f9b00000000000000000000000000000000000000000000000012adb7b8da080ca40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1345933868213472420`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`