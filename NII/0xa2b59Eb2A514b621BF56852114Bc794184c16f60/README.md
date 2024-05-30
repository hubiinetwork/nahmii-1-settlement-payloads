# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xa2b59Eb2A514b621BF56852114Bc794184c16f60`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000039d2903b190fa16db00000000000000000000000000000000000000000000000015ef3b92ca3770760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000015ef3b92ca3770760000000000000000000000000000000000000000000000026780e3b2ee1e1571abb186ccd9526dfd70dda4e3784c93534e1797899bc33d9ceb935ce3dfcdbb902d05e5d6d088af03a25261f27bfaaf8e86a13c5f3d1cb794fc48973759989f9f787a7f82ff9e2bac64a2731332456f421030ee36664019fca5b540a42bbb68d9000000000000000000000000000000000000000000000000000000000000001b7e80af0e28d8830cf3e905b302798cb3346c094300d7bc7b58e7b7989a798b77a184e0c3621f46a50f39df9591d1e0c329334543e9f12f6d2a30e3cf379e5ec35beabb8e5abd490d6c28c826df9c6cb3551c42b1485e6a41b5161822b5560852000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1fb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c42d0f53be7419f6ab0000000000000000000000000000000000000000000049c443042cd1225c35d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000059d7fe40aceb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9847912e442e759e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e6a4d47526a5a69316d593246684c5455785a4755744f444d344e6930344f57457a4d54466b5a474a6c4e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a2b59eb2a514b621bf56852114bc794184c16f600000000000000000000000000000000000000000000000039d2903b190fa16db0000000000000000000000000000000000000000000000038739c81ec6c2a66500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabb186ccd9526dfd70dda4e3784c93534e1797899bc33d9ceb935ce3dfcdbb90",
      "signature": {
        "s": "0x787a7f82ff9e2bac64a2731332456f421030ee36664019fca5b540a42bbb68d9",
        "r": "0x2d05e5d6d088af03a25261f27bfaaf8e86a13c5f3d1cb794fc48973759989f9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7e80af0e28d8830cf3e905b302798cb3346c094300d7bc7b58e7b7989a798b77",
      "signature": {
        "s": "0x5beabb8e5abd490d6c28c826df9c6cb3551c42b1485e6a41b5161822b5560852",
        "r": "0xa184e0c3621f46a50f39df9591d1e0c329334543e9f12f6d2a30e3cf379e5ec3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1580547495874228342",
    "total": "44351699487983277425"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1580547495874228342",
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
            "amount": "27624321559999971547625"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1580547495874228"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMWNjMGRjZi1mY2FhLTUxZGUtODM4Ni04OWEzMTFkZGJlNDcifQ==",
    "nonce": 111099,
    "balances": {
      "current": "348351561993864986883755",
      "previous": "348353144121908356986325"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa2b59eb2a514b621bf56852114bc794184c16f60",
    "nonce": 46,
    "balances": {
      "current": "66664819020304881371",
      "previous": "65084271524430653029"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:33.533Z",
  "updated": "2022-05-04T08:56:33.603Z",
  "id": "62723fc13592fd001130b5b6"
}
```
* *stageAmount*: `66664819020304881371`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000015ef3b92ca3770760000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000015ef3b92ca3770760000000000000000000000000000000000000000000000026780e3b2ee1e1571abb186ccd9526dfd70dda4e3784c93534e1797899bc33d9ceb935ce3dfcdbb902d05e5d6d088af03a25261f27bfaaf8e86a13c5f3d1cb794fc48973759989f9f787a7f82ff9e2bac64a2731332456f421030ee36664019fca5b540a42bbb68d9000000000000000000000000000000000000000000000000000000000000001b7e80af0e28d8830cf3e905b302798cb3346c094300d7bc7b58e7b7989a798b77a184e0c3621f46a50f39df9591d1e0c329334543e9f12f6d2a30e3cf379e5ec35beabb8e5abd490d6c28c826df9c6cb3551c42b1485e6a41b5161822b5560852000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b1fb000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000049c42d0f53be7419f6ab0000000000000000000000000000000000000000000049c443042cd1225c35d500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000059d7fe40aceb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9847912e442e759e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b4d574e6a4d47526a5a69316d593246684c5455785a4755744f444d344e6930344f57457a4d54466b5a474a6c4e44636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000a2b59eb2a514b621bf56852114bc794184c16f600000000000000000000000000000000000000000000000039d2903b190fa16db0000000000000000000000000000000000000000000000038739c81ec6c2a66500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xabb186ccd9526dfd70dda4e3784c93534e1797899bc33d9ceb935ce3dfcdbb90",
      "signature": {
        "s": "0x787a7f82ff9e2bac64a2731332456f421030ee36664019fca5b540a42bbb68d9",
        "r": "0x2d05e5d6d088af03a25261f27bfaaf8e86a13c5f3d1cb794fc48973759989f9f",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x7e80af0e28d8830cf3e905b302798cb3346c094300d7bc7b58e7b7989a798b77",
      "signature": {
        "s": "0x5beabb8e5abd490d6c28c826df9c6cb3551c42b1485e6a41b5161822b5560852",
        "r": "0xa184e0c3621f46a50f39df9591d1e0c329334543e9f12f6d2a30e3cf379e5ec3",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1580547495874228342",
    "total": "44351699487983277425"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1580547495874228342",
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
            "amount": "27624321559999971547625"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1580547495874228"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkMWNjMGRjZi1mY2FhLTUxZGUtODM4Ni04OWEzMTFkZGJlNDcifQ==",
    "nonce": 111099,
    "balances": {
      "current": "348351561993864986883755",
      "previous": "348353144121908356986325"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xa2b59eb2a514b621bf56852114bc794184c16f60",
    "nonce": 46,
    "balances": {
      "current": "66664819020304881371",
      "previous": "65084271524430653029"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:33.533Z",
  "updated": "2022-05-04T08:56:33.603Z",
  "id": "62723fc13592fd001130b5b6"
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
0x0f200f9b0000000000000000000000000000000000000000000000039d2903b190fa16db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `66664819020304881371`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`