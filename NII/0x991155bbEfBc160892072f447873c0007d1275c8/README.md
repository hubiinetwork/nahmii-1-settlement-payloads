# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x991155bbEfBc160892072f447873c0007d1275c8`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000012238b08be0e150cae0000000000000000000000000000000000000000000000006e17d936abf98fc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006e17d936abf98fc200000000000000000000000000000000000000000000000c1152310b04048160813f18877930c70579b9e13ddbb7d806b28abb663079f284f01edecc0ea85e953277ce6928421ee6ebaf33739f312b0dd8ca20267de219617d42288ba5acd39b54676b757b236b23191d2e4f7d38ef0230daf714962735738d54e8af10c30c27000000000000000000000000000000000000000000000000000000000000001bbcd70132d2092e7b5563d62b49c86ae88445060fc4d7dfb5bb59aa6cd4bcd437d4f2c80d7a4297e05bc33604bc7848443f51ae41b97d40022afd2f766968cc53726376d2dc8f3977637b39a26bbc17013d5fda8080c7b762d66cc88e31964a6c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6b1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030260789bd73bad56c0100000000000000000000000000000000000000000000302675bdc5bb18a4fe3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001c2f10b1d602720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e011ae66ed080307e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a426c5a5445345a5330775a5456694c54566a5a4445744f4459774d7931684e5459325a445a6d4e7a51794e54636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000991155bbefbc160892072f447873c0007d1275c8000000000000000000000000000000000000000000000012238b08be0e150cae000000000000000000000000000000000000000000000011b5732f87621b7cec00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x813f18877930c70579b9e13ddbb7d806b28abb663079f284f01edecc0ea85e95",
      "signature": {
        "s": "0x54676b757b236b23191d2e4f7d38ef0230daf714962735738d54e8af10c30c27",
        "r": "0x3277ce6928421ee6ebaf33739f312b0dd8ca20267de219617d42288ba5acd39b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbcd70132d2092e7b5563d62b49c86ae88445060fc4d7dfb5bb59aa6cd4bcd437",
      "signature": {
        "s": "0x726376d2dc8f3977637b39a26bbc17013d5fda8080c7b762d66cc88e31964a6c",
        "r": "0xd4f2c80d7a4297e05bc33604bc7848443f51ae41b97d40022afd2f766968cc53",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7933048097473138626",
    "total": "222609042854631473504"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7933048097473138626",
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
            "amount": "27745177155771985758185"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7933048097473138"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NjBlZTE4ZS0wZTViLTVjZDEtODYwMy1hNTY2ZDZmNzQyNTcifQ==",
    "nonce": 112305,
    "balances": {
      "current": "227375110626078761511937",
      "previous": "227383051607224332123701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x991155bbefbc160892072f447873c0007d1275c8",
    "nonce": 46,
    "balances": {
      "current": "334602543752235257006",
      "previous": "326669495654762118380"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:03:04.133Z",
  "updated": "2022-05-04T09:03:04.227Z",
  "id": "627241487832e20011830e24"
}
```
* *stageAmount*: `334602543752235257006`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000006e17d936abf98fc20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000006e17d936abf98fc200000000000000000000000000000000000000000000000c1152310b04048160813f18877930c70579b9e13ddbb7d806b28abb663079f284f01edecc0ea85e953277ce6928421ee6ebaf33739f312b0dd8ca20267de219617d42288ba5acd39b54676b757b236b23191d2e4f7d38ef0230daf714962735738d54e8af10c30c27000000000000000000000000000000000000000000000000000000000000001bbcd70132d2092e7b5563d62b49c86ae88445060fc4d7dfb5bb59aa6cd4bcd437d4f2c80d7a4297e05bc33604bc7848443f51ae41b97d40022afd2f766968cc53726376d2dc8f3977637b39a26bbc17013d5fda8080c7b762d66cc88e31964a6c000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e60000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b6b1000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000030260789bd73bad56c0100000000000000000000000000000000000000000000302675bdc5bb18a4fe3500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001c2f10b1d602720000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005e011ae66ed080307e90000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949334e6a426c5a5445345a5330775a5456694c54566a5a4445744f4459774d7931684e5459325a445a6d4e7a51794e54636966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000991155bbefbc160892072f447873c0007d1275c8000000000000000000000000000000000000000000000012238b08be0e150cae000000000000000000000000000000000000000000000011b5732f87621b7cec00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x813f18877930c70579b9e13ddbb7d806b28abb663079f284f01edecc0ea85e95",
      "signature": {
        "s": "0x54676b757b236b23191d2e4f7d38ef0230daf714962735738d54e8af10c30c27",
        "r": "0x3277ce6928421ee6ebaf33739f312b0dd8ca20267de219617d42288ba5acd39b",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xbcd70132d2092e7b5563d62b49c86ae88445060fc4d7dfb5bb59aa6cd4bcd437",
      "signature": {
        "s": "0x726376d2dc8f3977637b39a26bbc17013d5fda8080c7b762d66cc88e31964a6c",
        "r": "0xd4f2c80d7a4297e05bc33604bc7848443f51ae41b97d40022afd2f766968cc53",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "7933048097473138626",
    "total": "222609042854631473504"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7933048097473138626",
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
            "amount": "27745177155771985758185"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7933048097473138"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI3NjBlZTE4ZS0wZTViLTVjZDEtODYwMy1hNTY2ZDZmNzQyNTcifQ==",
    "nonce": 112305,
    "balances": {
      "current": "227375110626078761511937",
      "previous": "227383051607224332123701"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x991155bbefbc160892072f447873c0007d1275c8",
    "nonce": 46,
    "balances": {
      "current": "334602543752235257006",
      "previous": "326669495654762118380"
    }
  },
  "blockNumber": "14709990",
  "created": "2022-05-04T09:03:04.133Z",
  "updated": "2022-05-04T09:03:04.227Z",
  "id": "627241487832e20011830e24"
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
0x0f200f9b000000000000000000000000000000000000000000000012238b08be0e150cae0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `334602543752235257006`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`