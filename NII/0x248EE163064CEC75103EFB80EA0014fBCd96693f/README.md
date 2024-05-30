# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x248EE163064CEC75103EFB80EA0014fBCd96693f`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000029bd17a092b4b000000000000000000000000000000000000000000000000000000000000beb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000beb4000000000000000000000000000000000000000000000000000000000011629f653170930f5f7ec181ab352054d49a41b23e193a77b129a47629cbc056982e61bb39da30ae229d773b43bc95e55ffea7ed824431bc34e293800d3abf93f3edd91a3ba36da3322d0bfa62264c4d532013b72301eabb8d3a11f7342377161438c9000000000000000000000000000000000000000000000000000000000000001c2458dfe92c5491a660891e6c52e8e621f85964bab878f3b588beda593d88dcbf6b3ab8bc1ff5e3ba6534c1ce31bafce3c5466668b082e2e652e20999417b7d6e59baf5fad29fe2a8be768cabb9eb60d0cc81c46fedc4c665da8494beba24ad89000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b405000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039dd07617d91606bfe810000000000000000000000000000000000000000000039dd07617d91606cbd6500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd95a53c47ca77c2c50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6d4934597a6b354f43316c4d574e684c5455774f5759744f4467314e79316c4e5467315a44566b4d6a526b4d6d456966513d3d000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000248ee163064cec75103efb80ea0014fbcd96693f00000000000000000000000000000000000000000000000000029bd17a092b4b00000000000000000000000000000000000000000000000000029bd17a086c9700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x653170930f5f7ec181ab352054d49a41b23e193a77b129a47629cbc056982e61",
      "signature": {
        "s": "0x1a3ba36da3322d0bfa62264c4d532013b72301eabb8d3a11f7342377161438c9",
        "r": "0xbb39da30ae229d773b43bc95e55ffea7ed824431bc34e293800d3abf93f3edd9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2458dfe92c5491a660891e6c52e8e621f85964bab878f3b588beda593d88dcbf",
      "signature": {
        "s": "0x59baf5fad29fe2a8be768cabb9eb60d0cc81c46fedc4c665da8494beba24ad89",
        "r": "0x6b3ab8bc1ff5e3ba6534c1ce31bafce3c5466668b082e2e652e20999417b7d6e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48820",
    "total": "1139359"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48820",
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
            "amount": "27699345945799882687173"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MmI4Yzk5OC1lMWNhLTUwOWYtODg1Ny1lNTg1ZDVkMjRkMmEifQ==",
    "nonce": 111621,
    "balances": {
      "current": "273252151808153935937153",
      "previous": "273252151808153935986021"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x248ee163064cec75103efb80ea0014fbcd96693f",
    "nonce": 28,
    "balances": {
      "current": "734273951312715",
      "previous": "734273951263895"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:17.530Z",
  "updated": "2022-05-04T08:59:17.603Z",
  "id": "627240653592fd001130b673"
}
```
* *stageAmount*: `734273951312715`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000000000beb40000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000000000beb4000000000000000000000000000000000000000000000000000000000011629f653170930f5f7ec181ab352054d49a41b23e193a77b129a47629cbc056982e61bb39da30ae229d773b43bc95e55ffea7ed824431bc34e293800d3abf93f3edd91a3ba36da3322d0bfa62264c4d532013b72301eabb8d3a11f7342377161438c9000000000000000000000000000000000000000000000000000000000000001c2458dfe92c5491a660891e6c52e8e621f85964bab878f3b588beda593d88dcbf6b3ab8bc1ff5e3ba6534c1ce31bafce3c5466668b082e2e652e20999417b7d6e59baf5fad29fe2a8be768cabb9eb60d0cc81c46fedc4c665da8494beba24ad89000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b405000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039dd07617d91606bfe810000000000000000000000000000000000000000000039dd07617d91606cbd6500000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000000300000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd95a53c47ca77c2c50000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949314d6d4934597a6b354f43316c4d574e684c5455774f5759744f4467314e79316c4e5467315a44566b4d6a526b4d6d456966513d3d000000000000000000000000000000000000000000000000000000000000001c000000000000000000000000248ee163064cec75103efb80ea0014fbcd96693f00000000000000000000000000000000000000000000000000029bd17a092b4b00000000000000000000000000000000000000000000000000029bd17a086c9700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x653170930f5f7ec181ab352054d49a41b23e193a77b129a47629cbc056982e61",
      "signature": {
        "s": "0x1a3ba36da3322d0bfa62264c4d532013b72301eabb8d3a11f7342377161438c9",
        "r": "0xbb39da30ae229d773b43bc95e55ffea7ed824431bc34e293800d3abf93f3edd9",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x2458dfe92c5491a660891e6c52e8e621f85964bab878f3b588beda593d88dcbf",
      "signature": {
        "s": "0x59baf5fad29fe2a8be768cabb9eb60d0cc81c46fedc4c665da8494beba24ad89",
        "r": "0x6b3ab8bc1ff5e3ba6534c1ce31bafce3c5466668b082e2e652e20999417b7d6e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "48820",
    "total": "1139359"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "48820",
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
            "amount": "27699345945799882687173"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "48"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1MmI4Yzk5OC1lMWNhLTUwOWYtODg1Ny1lNTg1ZDVkMjRkMmEifQ==",
    "nonce": 111621,
    "balances": {
      "current": "273252151808153935937153",
      "previous": "273252151808153935986021"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x248ee163064cec75103efb80ea0014fbcd96693f",
    "nonce": 28,
    "balances": {
      "current": "734273951312715",
      "previous": "734273951263895"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:17.530Z",
  "updated": "2022-05-04T08:59:17.603Z",
  "id": "627240653592fd001130b673"
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
0x0f200f9b00000000000000000000000000000000000000000000000000029bd17a092b4b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `734273951312715`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`