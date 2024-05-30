# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x1F3A6Ae3d1A44b3a7092F510E9C65caEb41f8495`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000013a1288e14e32bbbe600000000000000000000000000000000000000000000000077240d18e96cd40f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000077240d18e96cd40f00000000000000000000000000000000000000000000000d0f35172df82bf65a52765a16456068f0450b43fc57129c4ffad09c873b2e3a6d8a70191c9c9354dd3565c5eaf9e2296379f58929765ac06052852744367fe939e7d115e15d52af296e01a1e06fc5dd75f6e84b020c060ac6c62e13a2794479804eaacea1a1520ba7000000000000000000000000000000000000000000000000000000000000001c25638b4ba2129e9f829676467ff2b78f739ed7560215f0644a5c598d08ba200edd52f42de0fff727f142084666b410269c6905579143d50f4c2feb675a1e134739f3f8a5e8028658ccb3af57373262862ad71093e6df2d490d01b0487dcf908b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0f6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b9e7609574d748eb234000000000000000000000000000000000000000000004b9eed4be469b853f40a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001e80035a586dc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90b2d612555511d650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e3251304e6a67334f53316a4d445a684c5455325a446774596d466c5a5330345a5455774f5441794d445a6c4e47556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001f3a6ae3d1a44b3a7092f510e9c65caeb41f8495000000000000000000000000000000000000000000000013a1288e14e32bbbe60000000000000000000000000000000000000000000000132a0480fbf9bee7d700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52765a16456068f0450b43fc57129c4ffad09c873b2e3a6d8a70191c9c9354dd",
      "signature": {
        "s": "0x6e01a1e06fc5dd75f6e84b020c060ac6c62e13a2794479804eaacea1a1520ba7",
        "r": "0x3565c5eaf9e2296379f58929765ac06052852744367fe939e7d115e15d52af29",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x25638b4ba2129e9f829676467ff2b78f739ed7560215f0644a5c598d08ba200e",
      "signature": {
        "s": "0x39f3f8a5e8028658ccb3af57373262862ad71093e6df2d490d01b0487dcf908b",
        "r": "0xdd52f42de0fff727f142084666b410269c6905579143d50f4c2feb675a1e1347",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8585001190321607695",
    "total": "240903480528763352666"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8585001190321607695",
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
            "amount": "27615581285064541019493"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8585001190321607"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2N2Q0Njg3OS1jMDZhLTU2ZDgtYmFlZS04ZTUwOTAyMDZlNGUifQ==",
    "nonce": 110838,
    "balances": {
      "current": "357100577204230945681972",
      "previous": "357109170790422457611274"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f3a6ae3d1a44b3a7092f510e9c65caeb41f8495",
    "nonce": 46,
    "balances": {
      "current": "362100825260018088934",
      "previous": "353515824069696481239"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:17.530Z",
  "updated": "2022-05-04T08:55:17.622Z",
  "id": "62723f753592fd001130b55b"
}
```
* *stageAmount*: `362100825260018088934`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000077240d18e96cd40f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000077240d18e96cd40f00000000000000000000000000000000000000000000000d0f35172df82bf65a52765a16456068f0450b43fc57129c4ffad09c873b2e3a6d8a70191c9c9354dd3565c5eaf9e2296379f58929765ac06052852744367fe939e7d115e15d52af296e01a1e06fc5dd75f6e84b020c060ac6c62e13a2794479804eaacea1a1520ba7000000000000000000000000000000000000000000000000000000000000001c25638b4ba2129e9f829676467ff2b78f739ed7560215f0644a5c598d08ba200edd52f42de0fff727f142084666b410269c6905579143d50f4c2feb675a1e134739f3f8a5e8028658ccb3af57373262862ad71093e6df2d490d01b0487dcf908b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d30000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b0f6000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004b9e7609574d748eb234000000000000000000000000000000000000000000004b9eed4be469b853f40a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000001e80035a586dc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d90b2d612555511d650000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949324e3251304e6a67334f53316a4d445a684c5455325a446774596d466c5a5330345a5455774f5441794d445a6c4e47556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000001f3a6ae3d1a44b3a7092f510e9c65caeb41f8495000000000000000000000000000000000000000000000013a1288e14e32bbbe60000000000000000000000000000000000000000000000132a0480fbf9bee7d700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x52765a16456068f0450b43fc57129c4ffad09c873b2e3a6d8a70191c9c9354dd",
      "signature": {
        "s": "0x6e01a1e06fc5dd75f6e84b020c060ac6c62e13a2794479804eaacea1a1520ba7",
        "r": "0x3565c5eaf9e2296379f58929765ac06052852744367fe939e7d115e15d52af29",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x25638b4ba2129e9f829676467ff2b78f739ed7560215f0644a5c598d08ba200e",
      "signature": {
        "s": "0x39f3f8a5e8028658ccb3af57373262862ad71093e6df2d490d01b0487dcf908b",
        "r": "0xdd52f42de0fff727f142084666b410269c6905579143d50f4c2feb675a1e1347",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "8585001190321607695",
    "total": "240903480528763352666"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "8585001190321607695",
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
            "amount": "27615581285064541019493"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "8585001190321607"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI2N2Q0Njg3OS1jMDZhLTU2ZDgtYmFlZS04ZTUwOTAyMDZlNGUifQ==",
    "nonce": 110838,
    "balances": {
      "current": "357100577204230945681972",
      "previous": "357109170790422457611274"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x1f3a6ae3d1a44b3a7092f510e9c65caeb41f8495",
    "nonce": 46,
    "balances": {
      "current": "362100825260018088934",
      "previous": "353515824069696481239"
    }
  },
  "blockNumber": "14709971",
  "created": "2022-05-04T08:55:17.530Z",
  "updated": "2022-05-04T08:55:17.622Z",
  "id": "62723f753592fd001130b55b"
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
0x0f200f9b000000000000000000000000000000000000000000000013a1288e14e32bbbe60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `362100825260018088934`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`