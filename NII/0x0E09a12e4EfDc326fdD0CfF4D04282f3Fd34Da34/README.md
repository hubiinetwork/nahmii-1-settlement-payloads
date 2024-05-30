# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x0E09a12e4EfDc326fdD0CfF4D04282f3Fd34Da34`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000de26b5676eb7bd900000000000000000000000000000000000000000000000000000042e45f51520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000042e45f5152000000000000000000000000000000000000000000000000000006191fe1235d25491f1718bb8c7a4ed5e0ca6bcefe10452963f682e46a520d85cda9ae1502016e9ac1a39f0948a974d2bfa9d446d11be1fecfda90b7929b3dd415198047f2567e1d1ad1778d21f989604049a903a901dcc079f3ed910cb8f6e88a7dd11c4896000000000000000000000000000000000000000000000000000000000000001cfb4bd70d3c981ad82785377de2d3e188a2fb4099a54b06325513f3c7e848557840488fbc1e655bd8b744a8abc8d6a331d15ea4f8c03f8c52ad19c7ba7a33d38e250f91c94c60b98b77bba605cd8c88a0de688c05fef6a53889006d5fba8de37e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ed00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b792000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08420a6b0473a7540000000000000000000000000000000000000000000021af08420aadf9f2cf8300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000111fd6dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396ac56322f130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6d45774d324534596930354d5746694c54557a4d545174596a646a4e5331694d54426b596a59314d444a695a57556966513d3d00000000000000000000000000000000000000000000000000000000000000260000000000000000000000000e09a12e4efdc326fdd0cff4d04282f3fd34da340000000000000000000000000000000000000000000000000de26b5676eb7bd90000000000000000000000000000000000000000000000000de26b13928c2a8700000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002088449205d370000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25491f1718bb8c7a4ed5e0ca6bcefe10452963f682e46a520d85cda9ae150201",
      "signature": {
        "s": "0x7e1d1ad1778d21f989604049a903a901dcc079f3ed910cb8f6e88a7dd11c4896",
        "r": "0x6e9ac1a39f0948a974d2bfa9d446d11be1fecfda90b7929b3dd415198047f256",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfb4bd70d3c981ad82785377de2d3e188a2fb4099a54b06325513f3c7e8485578",
      "signature": {
        "s": "0x250f91c94c60b98b77bba605cd8c88a0de688c05fef6a53889006d5fba8de37e",
        "r": "0x40488fbc1e655bd8b744a8abc8d6a331d15ea4f8c03f8c52ad19c7ba7a33d38e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "287299293522",
    "total": "6704978797405"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "287299293522",
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
            "amount": "27813417157199484038931"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "287299293"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZmEwM2E4Yi05MWFiLTUzMTQtYjdjNS1iMTBkYjY1MDJiZWUifQ==",
    "nonce": 112530,
    "balances": {
      "current": "159066869197152982378324",
      "previous": "159066869197440568971139"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "2344199000000000000"
          }
        }
      ]
    },
    "wallet": "0x0e09a12e4efdc326fdd0cff4d04282f3fd34da34",
    "nonce": 38,
    "balances": {
      "current": "1000480086336175065",
      "previous": "1000479799036881543"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:20.556Z",
  "updated": "2022-05-04T09:04:20.673Z",
  "id": "627241947832e20011830e71"
}
```
* *stageAmount*: `1000480086336175065`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000068000000000000000000000000000000000000000000000000000000042e45f51520000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000042e45f5152000000000000000000000000000000000000000000000000000006191fe1235d25491f1718bb8c7a4ed5e0ca6bcefe10452963f682e46a520d85cda9ae1502016e9ac1a39f0948a974d2bfa9d446d11be1fecfda90b7929b3dd415198047f2567e1d1ad1778d21f989604049a903a901dcc079f3ed910cb8f6e88a7dd11c4896000000000000000000000000000000000000000000000000000000000000001cfb4bd70d3c981ad82785377de2d3e188a2fb4099a54b06325513f3c7e848557840488fbc1e655bd8b744a8abc8d6a331d15ea4f8c03f8c52ad19c7ba7a33d38e250f91c94c60b98b77bba605cd8c88a0de688c05fef6a53889006d5fba8de37e000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ed00000000000000000000000000000000000000000000000000000000000005c0000000000000000000000000000000000000000000000000000000000001b792000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000021af08420a6b0473a7540000000000000000000000000000000000000000000021af08420aadf9f2cf8300000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000111fd6dd0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e3c4b396ac56322f130000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949335a6d45774d324534596930354d5746694c54557a4d545174596a646a4e5331694d54426b596a59314d444a695a57556966513d3d00000000000000000000000000000000000000000000000000000000000000260000000000000000000000000e09a12e4efdc326fdd0cff4d04282f3fd34da340000000000000000000000000000000000000000000000000de26b5676eb7bd90000000000000000000000000000000000000000000000000de26b13928c2a8700000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000020000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002088449205d370000000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x25491f1718bb8c7a4ed5e0ca6bcefe10452963f682e46a520d85cda9ae150201",
      "signature": {
        "s": "0x7e1d1ad1778d21f989604049a903a901dcc079f3ed910cb8f6e88a7dd11c4896",
        "r": "0x6e9ac1a39f0948a974d2bfa9d446d11be1fecfda90b7929b3dd415198047f256",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xfb4bd70d3c981ad82785377de2d3e188a2fb4099a54b06325513f3c7e8485578",
      "signature": {
        "s": "0x250f91c94c60b98b77bba605cd8c88a0de688c05fef6a53889006d5fba8de37e",
        "r": "0x40488fbc1e655bd8b744a8abc8d6a331d15ea4f8c03f8c52ad19c7ba7a33d38e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "287299293522",
    "total": "6704978797405"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "287299293522",
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
            "amount": "27813417157199484038931"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "287299293"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3ZmEwM2E4Yi05MWFiLTUzMTQtYjdjNS1iMTBkYjY1MDJiZWUifQ==",
    "nonce": 112530,
    "balances": {
      "current": "159066869197152982378324",
      "previous": "159066869197440568971139"
    }
  },
  "recipient": {
    "fees": {
      "total": [
        {
          "originId": "0",
          "figure": {
            "currency": {
              "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
              "id": "0"
            },
            "amount": "2344199000000000000"
          }
        }
      ]
    },
    "wallet": "0x0e09a12e4efdc326fdd0cff4d04282f3fd34da34",
    "nonce": 38,
    "balances": {
      "current": "1000480086336175065",
      "previous": "1000479799036881543"
    }
  },
  "blockNumber": "14709997",
  "created": "2022-05-04T09:04:20.556Z",
  "updated": "2022-05-04T09:04:20.673Z",
  "id": "627241947832e20011830e71"
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
0x0f200f9b0000000000000000000000000000000000000000000000000de26b5676eb7bd90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1000480086336175065`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`