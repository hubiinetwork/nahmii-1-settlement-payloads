# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xd3b447C013ee90697DCdC2C70a5b4cC6EaD29D3E`.

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
0x4d3d826c00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000564de50f2b3bad68b40000000000000000000000000000000000000000000000020bd23e6a3a6bb75f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000020bd23e6a3a6bb75f0000000000000000000000000000000000000000000000396aef1a9a7654a9fe35dbb1b76e63cff772a7b9c2b1b62f29c97dbc6534c589712cf772aef4cde0eae6b6f2db17c6229f172ec1bac3d366433a207642e768ce3a228c4f7d211070ea2ecee4d2add1bb20dc1b8a6af268e08c6f332c9885f61cec45c2e6161ad4b4a5000000000000000000000000000000000000000000000000000000000000001c415bde9322be9f6a99c56277ae4fc01a4ce7e9b8945a81ce4fdf7c3e78b62ac4f45cdd0722c9276029485d8debe7fdfcb4c401977a599cc4ba615f716514aa3521b3cfb99699b192b17f49a16f8332b91e1177888b99903c11534b6b61e8f087000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b01d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9de514c7c7d47ccf22000000000000000000000000000000000000000000004f9ff16d1f589080b27600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000086192681982bf50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d80570a0f8333500a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6d4d344e4449314e43316a5a54566b4c5455345a6a59744f5451785a43316d4f5755354f4749344d3255344d32516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d3b447c013ee90697dcdc2c70a5b4cc6ead29d3e0000000000000000000000000000000000000000000000564de50f2b3bad68b40000000000000000000000000000000000000000000000544212d0c10141b15500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x35dbb1b76e63cff772a7b9c2b1b62f29c97dbc6534c589712cf772aef4cde0ea",
      "signature": {
        "s": "0x2ecee4d2add1bb20dc1b8a6af268e08c6f332c9885f61cec45c2e6161ad4b4a5",
        "r": "0xe6b6f2db17c6229f172ec1bac3d366433a207642e768ce3a228c4f7d211070ea",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x415bde9322be9f6a99c56277ae4fc01a4ce7e9b8945a81ce4fdf7c3e78b62ac4",
      "signature": {
        "s": "0x21b3cfb99699b192b17f49a16f8332b91e1177888b99903c11534b6b61e8f087",
        "r": "0xf45cdd0722c9276029485d8debe7fdfcb4c401977a599cc4ba615f716514aa35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37745300052913141599",
    "total": "1059169818939611195902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37745300052913141599",
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
            "amount": "27596721124424941895847"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "37745300052913141"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNmM4NDI1NC1jZTVkLTU4ZjYtOTQxZC1mOWU5OGI4M2U4M2QifQ==",
    "nonce": 110621,
    "balances": {
      "current": "375979598004469668564770",
      "previous": "376017381049822634619510"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b447c013ee90697dcdc2c70a5b4cc6ead29d3e",
    "nonce": 46,
    "balances": {
      "current": "1592032899527967860916",
      "previous": "1554287599475054719317"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:12.423Z",
  "updated": "2022-05-04T08:54:12.513Z",
  "id": "62723f34bbd75600116d05ab"
}
```
* *stageAmount*: `1592032899527967860916`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000020bd23e6a3a6bb75f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000020bd23e6a3a6bb75f0000000000000000000000000000000000000000000000396aef1a9a7654a9fe35dbb1b76e63cff772a7b9c2b1b62f29c97dbc6534c589712cf772aef4cde0eae6b6f2db17c6229f172ec1bac3d366433a207642e768ce3a228c4f7d211070ea2ecee4d2add1bb20dc1b8a6af268e08c6f332c9885f61cec45c2e6161ad4b4a5000000000000000000000000000000000000000000000000000000000000001c415bde9322be9f6a99c56277ae4fc01a4ce7e9b8945a81ce4fdf7c3e78b62ac4f45cdd0722c9276029485d8debe7fdfcb4c401977a599cc4ba615f716514aa3521b3cfb99699b192b17f49a16f8332b91e1177888b99903c11534b6b61e8f087000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074d10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b01d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000004f9de514c7c7d47ccf22000000000000000000000000000000000000000000004f9ff16d1f589080b27600000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000086192681982bf50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d80570a0f8333500a70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a694e6d4d344e4449314e43316a5a54566b4c5455345a6a59744f5451785a43316d4f5755354f4749344d3255344d32516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000d3b447c013ee90697dcdc2c70a5b4cc6ead29d3e0000000000000000000000000000000000000000000000564de50f2b3bad68b40000000000000000000000000000000000000000000000544212d0c10141b15500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x35dbb1b76e63cff772a7b9c2b1b62f29c97dbc6534c589712cf772aef4cde0ea",
      "signature": {
        "s": "0x2ecee4d2add1bb20dc1b8a6af268e08c6f332c9885f61cec45c2e6161ad4b4a5",
        "r": "0xe6b6f2db17c6229f172ec1bac3d366433a207642e768ce3a228c4f7d211070ea",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x415bde9322be9f6a99c56277ae4fc01a4ce7e9b8945a81ce4fdf7c3e78b62ac4",
      "signature": {
        "s": "0x21b3cfb99699b192b17f49a16f8332b91e1177888b99903c11534b6b61e8f087",
        "r": "0xf45cdd0722c9276029485d8debe7fdfcb4c401977a599cc4ba615f716514aa35",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "37745300052913141599",
    "total": "1059169818939611195902"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "37745300052913141599",
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
            "amount": "27596721124424941895847"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "37745300052913141"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJiNmM4NDI1NC1jZTVkLTU4ZjYtOTQxZC1mOWU5OGI4M2U4M2QifQ==",
    "nonce": 110621,
    "balances": {
      "current": "375979598004469668564770",
      "previous": "376017381049822634619510"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xd3b447c013ee90697dcdc2c70a5b4cc6ead29d3e",
    "nonce": 46,
    "balances": {
      "current": "1592032899527967860916",
      "previous": "1554287599475054719317"
    }
  },
  "blockNumber": "14709969",
  "created": "2022-05-04T08:54:12.423Z",
  "updated": "2022-05-04T08:54:12.513Z",
  "id": "62723f34bbd75600116d05ab"
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
0x0f200f9b0000000000000000000000000000000000000000000000564de50f2b3bad68b40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `1592032899527967860916`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`