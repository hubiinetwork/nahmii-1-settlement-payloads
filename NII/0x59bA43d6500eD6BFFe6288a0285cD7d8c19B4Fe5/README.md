# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x59bA43d6500eD6BFFe6288a0285cD7d8c19B4Fe5`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000016153c59fa98bf2e310000000000000000000000000000000000000000000000000000000465b4387f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000465b4387f00000000000000000000000000000000000000000000000b27a2d32daba1f35d0d40e56af76c0a83f25bd7c96e76763a18bfacee8ce20eecefd29ac24f623260e01e9772eeacdb28a98655137880d1243372296f02b74a3c75ba0c5a2d659be94ace6db7a171c257d7c3c072b6a4f4fb62e041939750503d2d4b1eeed9029484000000000000000000000000000000000000000000000000000000000000001b62cc4fd4d60c71eb6316c282968989bb5ab348bd353c70fa7889215f65e40fa975b586dc65ef61596b6ca75c518982ced47eaee05952ae805cf9cd24f97664d86702adae67903d7e1763ec30867a4219b71d02f0ba515130443353a931713e11000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b24d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000491f73b901afc4e67e0800000000000000000000000000000000000000000000491f73b901b42bbae4a900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001202e220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9ae99a3b99114ab310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e446b3259544178595330344f445a684c54566b4f4459744f54566c4d53316a4e6a6b30595759305a6a55334d7a556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000059ba43d6500ed6bffe6288a0285cd7d8c19b4fe5000000000000000000000000000000000000000000000016153c59fa98bf2e31000000000000000000000000000000000000000000000016153c59f6330af5b200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d40e56af76c0a83f25bd7c96e76763a18bfacee8ce20eecefd29ac24f623260",
      "signature": {
        "s": "0x4ace6db7a171c257d7c3c072b6a4f4fb62e041939750503d2d4b1eeed9029484",
        "r": "0xe01e9772eeacdb28a98655137880d1243372296f02b74a3c75ba0c5a2d659be9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x62cc4fd4d60c71eb6316c282968989bb5ab348bd353c70fa7889215f65e40fa9",
      "signature": {
        "s": "0x6702adae67903d7e1763ec30867a4219b71d02f0ba515130443353a931713e11",
        "r": "0x75b586dc65ef61596b6ca75c518982ced47eaee05952ae805cf9cd24f97664d8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18886178943",
    "total": "205770262117617890141"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18886178943",
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
            "amount": "27627357145394633288497"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18886178"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NDk2YTAxYS04ODZhLTVkODYtOTVlMS1jNjk0YWY0ZjU3MzUifQ==",
    "nonce": 111181,
    "balances": {
      "current": "345312941013808584228360",
      "previous": "345312941013827489293481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x59ba43d6500ed6bffe6288a0285cd7d8c19b4fe5",
    "nonce": 46,
    "balances": {
      "current": "407358566527848623665",
      "previous": "407358566508962444722"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:58.431Z",
  "updated": "2022-05-04T08:56:58.510Z",
  "id": "62723fda3592fd001130b5d3"
}
```
* *stageAmount*: `407358566527848623665`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000000000000465b4387f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000000000000465b4387f00000000000000000000000000000000000000000000000b27a2d32daba1f35d0d40e56af76c0a83f25bd7c96e76763a18bfacee8ce20eecefd29ac24f623260e01e9772eeacdb28a98655137880d1243372296f02b74a3c75ba0c5a2d659be94ace6db7a171c257d7c3c072b6a4f4fb62e041939750503d2d4b1eeed9029484000000000000000000000000000000000000000000000000000000000000001b62cc4fd4d60c71eb6316c282968989bb5ab348bd353c70fa7889215f65e40fa975b586dc65ef61596b6ca75c518982ced47eaee05952ae805cf9cd24f97664d86702adae67903d7e1763ec30867a4219b71d02f0ba515130443353a931713e11000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074d70000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b24d000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000491f73b901afc4e67e0800000000000000000000000000000000000000000000491f73b901b42bbae4a900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001202e220000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005d9ae99a3b99114ab310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949304e446b3259544178595330344f445a684c54566b4f4459744f54566c4d53316a4e6a6b30595759305a6a55334d7a556966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000059ba43d6500ed6bffe6288a0285cd7d8c19b4fe5000000000000000000000000000000000000000000000016153c59fa98bf2e31000000000000000000000000000000000000000000000016153c59f6330af5b200000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0d40e56af76c0a83f25bd7c96e76763a18bfacee8ce20eecefd29ac24f623260",
      "signature": {
        "s": "0x4ace6db7a171c257d7c3c072b6a4f4fb62e041939750503d2d4b1eeed9029484",
        "r": "0xe01e9772eeacdb28a98655137880d1243372296f02b74a3c75ba0c5a2d659be9",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x62cc4fd4d60c71eb6316c282968989bb5ab348bd353c70fa7889215f65e40fa9",
      "signature": {
        "s": "0x6702adae67903d7e1763ec30867a4219b71d02f0ba515130443353a931713e11",
        "r": "0x75b586dc65ef61596b6ca75c518982ced47eaee05952ae805cf9cd24f97664d8",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "18886178943",
    "total": "205770262117617890141"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "18886178943",
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
            "amount": "27627357145394633288497"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "18886178"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI0NDk2YTAxYS04ODZhLTVkODYtOTVlMS1jNjk0YWY0ZjU3MzUifQ==",
    "nonce": 111181,
    "balances": {
      "current": "345312941013808584228360",
      "previous": "345312941013827489293481"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x59ba43d6500ed6bffe6288a0285cd7d8c19b4fe5",
    "nonce": 46,
    "balances": {
      "current": "407358566527848623665",
      "previous": "407358566508962444722"
    }
  },
  "blockNumber": "14709975",
  "created": "2022-05-04T08:56:58.431Z",
  "updated": "2022-05-04T08:56:58.510Z",
  "id": "62723fda3592fd001130b5d3"
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
0x0f200f9b000000000000000000000000000000000000000000000016153c59fa98bf2e310000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `407358566527848623665`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`