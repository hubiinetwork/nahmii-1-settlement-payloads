# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x27Ea0660b4E92807c49DE4fFC3317F3453588b00`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000519d015263943a3440000000000000000000000000000000000000000000000007d203373f73c0c490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000007d203373f73c0c4900000000000000000000000000000000000000000000000519d015263943a34447dcba283a21c7904d93cf5f999b7bbfe337095c3bbb2726b73bdef57d8e71f9080a3b1c665fffd4dc8553d14da07a7ddff38b97f90faacf9a62670e435831c51bb328ab007e9747e99ae74200ac5d8a063f50cabc266b2334d775a0d353331d000000000000000000000000000000000000000000000000000000000000001c05a65abdf2488f6b653e73abd4aafbf59334d9090346ba803db58ea1b57bfb22c0d558db462a37d27b377e5236f7edc269de2af7a79acfc937f900efa98068374a408f40f92d3c76e51ed48984cbe8094952b4d7515328202cffe3cf4459f3a0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d93000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023d16a0b86021c4b85100000000000000000000000000000000000000000000023d1e74bc1b46676fce100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000020083e52ef6b880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f81ce038be87adf3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f4751325a6a5a6d4f53316a4e7a426c4c54557a4f546374596d5932597930344e474e6a5a6d466d4f445269596d516966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000027ea0660b4e92807c49de4ffc3317f3453588b0000000000000000000000000000000000000000000000000519d015263943a3440000000000000000000000000000000000000000000000049cafe1b2420796fb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47dcba283a21c7904d93cf5f999b7bbfe337095c3bbb2726b73bdef57d8e71f9",
      "signature": {
        "s": "0x1bb328ab007e9747e99ae74200ac5d8a063f50cabc266b2334d775a0d353331d",
        "r": "0x080a3b1c665fffd4dc8553d14da07a7ddff38b97f90faacf9a62670e435831c5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x05a65abdf2488f6b653e73abd4aafbf59334d9090346ba803db58ea1b57bfb22",
      "signature": {
        "s": "0x4a408f40f92d3c76e51ed48984cbe8094952b4d7515328202cffe3cf4459f3a0",
        "r": "0xc0d558db462a37d27b377e5236f7edc269de2af7a79acfc937f900efa9806837",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9016263027157896265",
    "total": "94093730268565447492"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9016263027157896265",
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
            "amount": "16814337268524932325178"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9016263027157896"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5OGQ2ZjZmOS1jNzBlLTUzOTctYmY2Yy04NGNjZmFmODRiYmQifQ==",
    "nonce": 77203,
    "balances": {
      "current": "169145837760379265713424",
      "previous": "169154863039669450767585"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x27ea0660b4e92807c49de4ffc3317f3453588b00",
    "nonce": 2,
    "balances": {
      "current": "94093730268565447492",
      "previous": "85077467241407551227"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:46:05.033Z",
  "updated": "2021-06-04T12:46:05.136Z",
  "id": "60ba208d0779920010014b8f"
}
```
* *stageAmount*: `94093730268565447492`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000007d203373f73c0c490000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000007d203373f73c0c4900000000000000000000000000000000000000000000000519d015263943a34447dcba283a21c7904d93cf5f999b7bbfe337095c3bbb2726b73bdef57d8e71f9080a3b1c665fffd4dc8553d14da07a7ddff38b97f90faacf9a62670e435831c51bb328ab007e9747e99ae74200ac5d8a063f50cabc266b2334d775a0d353331d000000000000000000000000000000000000000000000000000000000000001c05a65abdf2488f6b653e73abd4aafbf59334d9090346ba803db58ea1b57bfb22c0d558db462a37d27b377e5236f7edc269de2af7a79acfc937f900efa98068374a408f40f92d3c76e51ed48984cbe8094952b4d7515328202cffe3cf4459f3a0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000bfc5e000000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000012d93000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023d16a0b86021c4b85100000000000000000000000000000000000000000000023d1e74bc1b46676fce100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000020083e52ef6b880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000800000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000038f81ce038be87adf3a0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f4751325a6a5a6d4f53316a4e7a426c4c54557a4f546374596d5932597930344e474e6a5a6d466d4f445269596d516966513d3d000000000000000000000000000000000000000000000000000000000000000200000000000000000000000027ea0660b4e92807c49de4ffc3317f3453588b0000000000000000000000000000000000000000000000000519d015263943a3440000000000000000000000000000000000000000000000049cafe1b2420796fb00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x47dcba283a21c7904d93cf5f999b7bbfe337095c3bbb2726b73bdef57d8e71f9",
      "signature": {
        "s": "0x1bb328ab007e9747e99ae74200ac5d8a063f50cabc266b2334d775a0d353331d",
        "r": "0x080a3b1c665fffd4dc8553d14da07a7ddff38b97f90faacf9a62670e435831c5",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x05a65abdf2488f6b653e73abd4aafbf59334d9090346ba803db58ea1b57bfb22",
      "signature": {
        "s": "0x4a408f40f92d3c76e51ed48984cbe8094952b4d7515328202cffe3cf4459f3a0",
        "r": "0xc0d558db462a37d27b377e5236f7edc269de2af7a79acfc937f900efa9806837",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "9016263027157896265",
    "total": "94093730268565447492"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "9016263027157896265",
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
            "amount": "16814337268524932325178"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "9016263027157896"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5OGQ2ZjZmOS1jNzBlLTUzOTctYmY2Yy04NGNjZmFmODRiYmQifQ==",
    "nonce": 77203,
    "balances": {
      "current": "169145837760379265713424",
      "previous": "169154863039669450767585"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x27ea0660b4e92807c49de4ffc3317f3453588b00",
    "nonce": 2,
    "balances": {
      "current": "94093730268565447492",
      "previous": "85077467241407551227"
    }
  },
  "blockNumber": "12568032",
  "created": "2021-06-04T12:46:05.033Z",
  "updated": "2021-06-04T12:46:05.136Z",
  "id": "60ba208d0779920010014b8f"
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
0x0f200f9b00000000000000000000000000000000000000000000000519d015263943a3440000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `94093730268565447492`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`