# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xD841afA9d7dCB237530eca7CCb5a668DBc9274B1`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000476c9f08f308d51000000000000000000000000000000000000000000000000001b181f8846d51c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001b181f8846d51c00000000000000000000000000000000000000000000000002f84a5c3485e4c3b0fd0fd96e3d91b2697e460f561d46e4595044d76cdd998ab8266bdb72c6e0038ddbdcd7c13d3af84bd193f8ee72cd1474b4c789fe84a53837fb409fd5ad6b40296819bd6facd08c6023ca19323bcd7c5b169daa0c9ca0142956207288ae1772000000000000000000000000000000000000000000000000000000000000001bd20888181ca2991ce24c41ed767ec878730a56ff7b5b5370af18bff76445e5081904bd2b8d0058b3695066c36d7008b429349a970a410b2b4380137b304b980636d23996bed0e724aa6511bc0305ef5b185ac910f408a4d9f60ef6e39b367bb2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b199000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004acbc90288048dac53a4000000000000000000000000000000000000000000004acbc91da713bbb7d68700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000006efa5c4adc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9410e70f40c261e6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a545134597a493359793034596a56694c54566b5a6d49744f54466d4e4331684e7a4a6c5a4451794f5755774d446b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d841afa9d7dcb237530eca7ccb5a668dbc9274b10000000000000000000000000000000000000000000000000476c9f08f308d51000000000000000000000000000000000000000000000000045bb1d106e9b83500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb0fd0fd96e3d91b2697e460f561d46e4595044d76cdd998ab8266bdb72c6e003",
      "signature": {
        "s": "0x296819bd6facd08c6023ca19323bcd7c5b169daa0c9ca0142956207288ae1772",
        "r": "0x8ddbdcd7c13d3af84bd193f8ee72cd1474b4c789fe84a53837fb409fd5ad6b40",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd20888181ca2991ce24c41ed767ec878730a56ff7b5b5370af18bff76445e508",
      "signature": {
        "s": "0x36d23996bed0e724aa6511bc0305ef5b185ac910f408a4d9f60ef6e39b367bb2",
        "r": "0x1904bd2b8d0058b3695066c36d7008b429349a970a410b2b4380137b304b9806",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7626348080583964",
    "total": "214002742178735299"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7626348080583964",
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
            "amount": "27619463686798816190061"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7626348080583"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkZTQ4YzI3Yy04YjViLTVkZmItOTFmNC1hNzJlZDQyOWUwMDkifQ==",
    "nonce": 111001,
    "balances": {
      "current": "353214293068221499855780",
      "previous": "353214300702195928520327"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd841afa9d7dcb237530eca7ccb5a668dbc9274b1",
    "nonce": 46,
    "balances": {
      "current": "321666458435226961",
      "previous": "314040110354642997"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:05.483Z",
  "updated": "2022-05-04T08:56:05.539Z",
  "id": "62723fa53592fd001130b598"
}
```
* *stageAmount*: `321666458435226961`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000001b181f8846d51c0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000001b181f8846d51c00000000000000000000000000000000000000000000000002f84a5c3485e4c3b0fd0fd96e3d91b2697e460f561d46e4595044d76cdd998ab8266bdb72c6e0038ddbdcd7c13d3af84bd193f8ee72cd1474b4c789fe84a53837fb409fd5ad6b40296819bd6facd08c6023ca19323bcd7c5b169daa0c9ca0142956207288ae1772000000000000000000000000000000000000000000000000000000000000001bd20888181ca2991ce24c41ed767ec878730a56ff7b5b5370af18bff76445e5081904bd2b8d0058b3695066c36d7008b429349a970a410b2b4380137b304b980636d23996bed0e724aa6511bc0305ef5b185ac910f408a4d9f60ef6e39b367bb2000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d40000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b199000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004acbc90288048dac53a4000000000000000000000000000000000000000000004acbc91da713bbb7d68700000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000006efa5c4adc70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9410e70f40c261e6d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6b5a545134597a493359793034596a56694c54566b5a6d49744f54466d4e4331684e7a4a6c5a4451794f5755774d446b6966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d841afa9d7dcb237530eca7ccb5a668dbc9274b10000000000000000000000000000000000000000000000000476c9f08f308d51000000000000000000000000000000000000000000000000045bb1d106e9b83500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xb0fd0fd96e3d91b2697e460f561d46e4595044d76cdd998ab8266bdb72c6e003",
      "signature": {
        "s": "0x296819bd6facd08c6023ca19323bcd7c5b169daa0c9ca0142956207288ae1772",
        "r": "0x8ddbdcd7c13d3af84bd193f8ee72cd1474b4c789fe84a53837fb409fd5ad6b40",
        "v": 27
      }
    },
    "operator": {
      "hash": "0xd20888181ca2991ce24c41ed767ec878730a56ff7b5b5370af18bff76445e508",
      "signature": {
        "s": "0x36d23996bed0e724aa6511bc0305ef5b185ac910f408a4d9f60ef6e39b367bb2",
        "r": "0x1904bd2b8d0058b3695066c36d7008b429349a970a410b2b4380137b304b9806",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "7626348080583964",
    "total": "214002742178735299"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "7626348080583964",
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
            "amount": "27619463686798816190061"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "7626348080583"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJkZTQ4YzI3Yy04YjViLTVkZmItOTFmNC1hNzJlZDQyOWUwMDkifQ==",
    "nonce": 111001,
    "balances": {
      "current": "353214293068221499855780",
      "previous": "353214300702195928520327"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd841afa9d7dcb237530eca7ccb5a668dbc9274b1",
    "nonce": 46,
    "balances": {
      "current": "321666458435226961",
      "previous": "314040110354642997"
    }
  },
  "blockNumber": "14709972",
  "created": "2022-05-04T08:56:05.483Z",
  "updated": "2022-05-04T08:56:05.539Z",
  "id": "62723fa53592fd001130b598"
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
0x0f200f9b0000000000000000000000000000000000000000000000000476c9f08f308d510000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `321666458435226961`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`