# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x08c1e76142dDDB175bdf0c24b6C88F148951E637`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000d3f0bfb000a281100000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c000000000000000000000000000000000000000000000000d3f0bfb000a28110c4351ee3f132df666d28632440c517e1b238a38737fdacefb496b3f117d1da93bc42eb5e9e16f92144623a8f1714030d60ac79756424ddb83479f2dad4732097558ef88347aa8d0b698ffb940ab464a30969722c4fd61729f7c0be7012adba55000000000000000000000000000000000000000000000000000000000000001c5f0f32f0dff0ee1cec149174754d161516dbeea25e1e278b56fcffe31a6fa42f21b726b633b1cb77decd38ea411936acf6d312854d9be164eac85e09ead1b20670ca10dead00a445c163a4094023399d1f3ff8cc66a7a5cddaee11ba2893ddce000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a1f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023635cdd4ad3bb214cd9000000000000000000000000000000000000000000002363bab366ceb55226b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5c5dfa84100c719e20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5459305932466d4d4330304e6d4d334c5455795a5455744f44566b5953307a4e575a6a5a546b774d3255774e44676966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000008c1e76142dddb175bdf0c24b6c88f148951e637000000000000000000000000000000000000000000000000d3f0bfb000a281100000000000000000000000000000000000000000000000007632a3393d6c54d400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4351ee3f132df666d28632440c517e1b238a38737fdacefb496b3f117d1da93",
      "signature": {
        "s": "0x558ef88347aa8d0b698ffb940ab464a30969722c4fd61729f7c0be7012adba55",
        "r": "0xbc42eb5e9e16f92144623a8f1714030d60ac79756424ddb83479f2dad4732097",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5f0f32f0dff0ee1cec149174754d161516dbeea25e1e278b56fcffe31a6fa42f",
      "signature": {
        "s": "0x70ca10dead00a445c163a4094023399d1f3ff8cc66a7a5cddaee11ba2893ddce",
        "r": "0x21b726b633b1cb77decd38ea411936acf6d312854d9be164eac85e09ead1b206",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "15271917099059151120"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6754867787509148732",
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
            "amount": "17815366331072134978018"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6754867787509148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZTY0Y2FmMC00NmM3LTUyZTUtODVkYS0zNWZjZTkwM2UwNDgifQ==",
    "nonce": 80415,
    "balances": {
      "current": "167115746150629408591065",
      "previous": "167122507773284705248945"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08c1e76142dddb175bdf0c24b6c88f148951e637",
    "nonce": 3,
    "balances": {
      "current": "15271917099059151120",
      "previous": "8517049311550002388"
    }
  },
  "blockNumber": "12767125",
  "created": "2021-07-05T11:15:20.101Z",
  "updated": "2021-07-05T11:15:20.176Z",
  "id": "60e2e9c8cc369000105e3052"
}
```
* *stageAmount*: `15271917099059151120`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000005dbe1c76c3362c3c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000005dbe1c76c3362c3c000000000000000000000000000000000000000000000000d3f0bfb000a28110c4351ee3f132df666d28632440c517e1b238a38737fdacefb496b3f117d1da93bc42eb5e9e16f92144623a8f1714030d60ac79756424ddb83479f2dad4732097558ef88347aa8d0b698ffb940ab464a30969722c4fd61729f7c0be7012adba55000000000000000000000000000000000000000000000000000000000000001c5f0f32f0dff0ee1cec149174754d161516dbeea25e1e278b56fcffe31a6fa42f21b726b633b1cb77decd38ea411936acf6d312854d9be164eac85e09ead1b20670ca10dead00a445c163a4094023399d1f3ff8cc66a7a5cddaee11ba2893ddce000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000c2cf9500000000000000000000000000000000000000000000000000000000000005400000000000000000000000000000000000000000000000000000000000013a1f000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000023635cdd4ad3bb214cd9000000000000000000000000000000000000000000002363bab366ceb55226b100000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000017ff8436faad9c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003c5c5dfa84100c719e20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a695a5459305932466d4d4330304e6d4d334c5455795a5455744f44566b5953307a4e575a6a5a546b774d3255774e44676966513d3d000000000000000000000000000000000000000000000000000000000000000300000000000000000000000008c1e76142dddb175bdf0c24b6c88f148951e637000000000000000000000000000000000000000000000000d3f0bfb000a281100000000000000000000000000000000000000000000000007632a3393d6c54d400000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xc4351ee3f132df666d28632440c517e1b238a38737fdacefb496b3f117d1da93",
      "signature": {
        "s": "0x558ef88347aa8d0b698ffb940ab464a30969722c4fd61729f7c0be7012adba55",
        "r": "0xbc42eb5e9e16f92144623a8f1714030d60ac79756424ddb83479f2dad4732097",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x5f0f32f0dff0ee1cec149174754d161516dbeea25e1e278b56fcffe31a6fa42f",
      "signature": {
        "s": "0x70ca10dead00a445c163a4094023399d1f3ff8cc66a7a5cddaee11ba2893ddce",
        "r": "0x21b726b633b1cb77decd38ea411936acf6d312854d9be164eac85e09ead1b206",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "6754867787509148732",
    "total": "15271917099059151120"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "6754867787509148732",
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
            "amount": "17815366331072134978018"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "6754867787509148"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiZTY0Y2FmMC00NmM3LTUyZTUtODVkYS0zNWZjZTkwM2UwNDgifQ==",
    "nonce": 80415,
    "balances": {
      "current": "167115746150629408591065",
      "previous": "167122507773284705248945"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x08c1e76142dddb175bdf0c24b6c88f148951e637",
    "nonce": 3,
    "balances": {
      "current": "15271917099059151120",
      "previous": "8517049311550002388"
    }
  },
  "blockNumber": "12767125",
  "created": "2021-07-05T11:15:20.101Z",
  "updated": "2021-07-05T11:15:20.176Z",
  "id": "60e2e9c8cc369000105e3052"
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
0x0f200f9b000000000000000000000000000000000000000000000000d3f0bfb000a281100000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15271917099059151120`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`