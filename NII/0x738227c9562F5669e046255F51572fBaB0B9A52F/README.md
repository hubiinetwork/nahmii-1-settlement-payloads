# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x738227c9562F5669e046255F51572fBaB0B9A52F`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000040aaf7866df7400000000000000000000000000000000000000000000000000001887fe25a48a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000001887fe25a48a0000000000000000000000000000000000000000000000000002b05eb3f04c7cb156515097442993711f4d34a9de68d91ce726276a0af17fb406532eeabf978791dabffaaf36cd2d5b9634db4dc1f6e3e3ed738609c7b36d9a26a2e8c7dac1b172bbdbe81c99effb8a17e547a4ddea9a1d49fbfa87dcc3728bfa66831d93f62f000000000000000000000000000000000000000000000000000000000000001bb3028aa04934c52fb0df581ad6f9d528ff84f2dcc59959765d373e785ad073ad587d976fa18370f9476eb6c531d8dcfe60f3f1d54aa3673a06d1813e40a292712eb95c313045457c1994f11837761bf1853bb713c5ed7b495d2ccb5190f6bfb7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b02a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9bb213db7df3d71491000000000000000000000000000000000000000000004f9bb213f40c39aa542600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000647ad9b0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d806009d1d19db66d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a57566a4e3249795969303459574a6a4c54566a59324d744f44426b595330334e3259354e6a41334e4449795932556966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000738227c9562f5669e046255f51572fbab0b9a52f00000000000000000000000000000000000000000000000000040aaf7866df740000000000000000000000000000000000000000000000000003f2277a413aea00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb156515097442993711f4d34a9de68d91ce726276a0af17fb406532eeabf9787",
      "signature": {
        "s": "0x72bbdbe81c99effb8a17e547a4ddea9a1d49fbfa87dcc3728bfa66831d93f62f",
        "r": "0x91dabffaaf36cd2d5b9634db4dc1f6e3e3ed738609c7b36d9a26a2e8c7dac1b1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3028aa04934c52fb0df581ad6f9d528ff84f2dcc59959765d373e785ad073ad",
      "signature": {
        "s": "0x2eb95c313045457c1994f11837761bf1853bb713c5ed7b495d2ccb5190f6bfb7",
        "r": "0x587d976fa18370f9476eb6c531d8dcfe60f3f1d54aa3673a06d1813e40a29271",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "26972363531402",
    "total": "756870745705596"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26972363531402",
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
            "amount": "27596761652582030206681"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26972363531"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZWVjN2IyYi04YWJjLTVjY2MtODBkYS03N2Y5NjA3NDIyY2UifQ==",
    "nonce": 110634,
    "balances": {
      "current": "375939029319224269411473",
      "previous": "375939029346223605306406"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x738227c9562f5669e046255f51572fbab0b9a52f",
    "nonce": 45,
    "balances": {
      "current": "1137648662404980",
      "previous": "1110676298873578"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:16.142Z",
  "updated": "2022-05-04T08:54:16.389Z",
  "id": "62723f38bbd75600116d05ae"
}
```
* *stageAmount*: `1137648662404980`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000001887fe25a48a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000001887fe25a48a0000000000000000000000000000000000000000000000000002b05eb3f04c7cb156515097442993711f4d34a9de68d91ce726276a0af17fb406532eeabf978791dabffaaf36cd2d5b9634db4dc1f6e3e3ed738609c7b36d9a26a2e8c7dac1b172bbdbe81c99effb8a17e547a4ddea9a1d49fbfa87dcc3728bfa66831d93f62f000000000000000000000000000000000000000000000000000000000000001bb3028aa04934c52fb0df581ad6f9d528ff84f2dcc59959765d373e785ad073ad587d976fa18370f9476eb6c531d8dcfe60f3f1d54aa3673a06d1813e40a292712eb95c313045457c1994f11837761bf1853bb713c5ed7b495d2ccb5190f6bfb7000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b02a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9bb213db7df3d71491000000000000000000000000000000000000000000004f9bb213f40c39aa542600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000647ad9b0b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d806009d1d19db66d90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a57566a4e3249795969303459574a6a4c54566a59324d744f44426b595330334e3259354e6a41334e4449795932556966513d3d000000000000000000000000000000000000000000000000000000000000002d000000000000000000000000738227c9562f5669e046255f51572fbab0b9a52f00000000000000000000000000000000000000000000000000040aaf7866df740000000000000000000000000000000000000000000000000003f2277a413aea00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb156515097442993711f4d34a9de68d91ce726276a0af17fb406532eeabf9787",
      "signature": {
        "s": "0x72bbdbe81c99effb8a17e547a4ddea9a1d49fbfa87dcc3728bfa66831d93f62f",
        "r": "0x91dabffaaf36cd2d5b9634db4dc1f6e3e3ed738609c7b36d9a26a2e8c7dac1b1",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xb3028aa04934c52fb0df581ad6f9d528ff84f2dcc59959765d373e785ad073ad",
      "signature": {
        "s": "0x2eb95c313045457c1994f11837761bf1853bb713c5ed7b495d2ccb5190f6bfb7",
        "r": "0x587d976fa18370f9476eb6c531d8dcfe60f3f1d54aa3673a06d1813e40a29271",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "26972363531402",
    "total": "756870745705596"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "26972363531402",
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
            "amount": "27596761652582030206681"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "26972363531"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZWVjN2IyYi04YWJjLTVjY2MtODBkYS03N2Y5NjA3NDIyY2UifQ==",
    "nonce": 110634,
    "balances": {
      "current": "375939029319224269411473",
      "previous": "375939029346223605306406"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x738227c9562f5669e046255f51572fbab0b9a52f",
    "nonce": 45,
    "balances": {
      "current": "1137648662404980",
      "previous": "1110676298873578"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:16.142Z",
  "updated": "2022-05-04T08:54:16.389Z",
  "id": "62723f38bbd75600116d05ae"
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
0x0f200f9b00000000000000000000000000000000000000000000000000040aaf7866df740000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1137648662404980`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`