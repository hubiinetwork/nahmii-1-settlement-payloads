# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB2856DE7CAc918ADf4bF19a349f795Ef366AB878`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000334d99ec383770560000000000000000000000000000000000000000000000001450e0fe0568c5fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001450e0fe0568c5fe000000000000000000000000000000000000000000000000334d99ec3837705699582eb12ef2c9886918c9531ed076b5f732b0cd6d6b55b0122b4d5f37b5cf965c9ffa9467066d76aaa02fc7f9185b92d15c97cbaac2efe9c4385c911d398e5c4afbcf65c520532c761b37e70213e33eead178f43683e5bca952aace76c2da52000000000000000000000000000000000000000000000000000000000000001c3432d1530f34df57d8381ca88fa421e61201aca162824d7753fa5cdd2c4894b957a83cfd713d8d55edb09e1cda4938ce75953633738548f4a99db216b515eafc29554fc3d8a70b899433d99384133decac6e1de1f8051c6a9425c61721106105000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd38410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001210a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024cdc8eb4c680d878ea20000000000000000000000000000000000000000000024cddd4160d2df3b717e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005336ccc4b1cde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003591956a9a2130b13880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e7a426d595464685a53316c4d4759314c5455334f4441744f5756694e69316a4e6a4d3159325a695954646a4e54636966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000b2856de7cac918adf4bf19a349f795ef366ab878000000000000000000000000000000000000000000000000334d99ec383770560000000000000000000000000000000000000000000000001efcb8ee32ceaa5800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99582eb12ef2c9886918c9531ed076b5f732b0cd6d6b55b0122b4d5f37b5cf96",
      "signature": {
        "s": "0x4afbcf65c520532c761b37e70213e33eead178f43683e5bca952aace76c2da52",
        "r": "0x5c9ffa9467066d76aaa02fc7f9185b92d15c97cbaac2efe9c4385c911d398e5c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3432d1530f34df57d8381ca88fa421e61201aca162824d7753fa5cdd2c4894b9",
      "signature": {
        "s": "0x29554fc3d8a70b899433d99384133decac6e1de1f8051c6a9425c61721106105",
        "r": "0x57a83cfd713d8d55edb09e1cda4938ce75953633738548f4a99db216b515eafc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1463917260512478718",
    "total": "3696780108975534166"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1463917260512478718",
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
            "amount": "15810685504381600338824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1463917260512478"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNzBmYTdhZS1lMGY1LTU3ODAtOWViNi1jNjM1Y2ZiYTdjNTcifQ==",
    "nonce": 73994,
    "balances": {
      "current": "173801253667854585663138",
      "previous": "173802719049032358654334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb2856de7cac918adf4bf19a349f795ef366ab878",
    "nonce": 3,
    "balances": {
      "current": "3696780108975534166",
      "previous": "2232862848463055448"
    }
  },
  "blockNumber": "12400705",
  "created": "2021-05-09T14:36:28.204Z",
  "updated": "2021-05-09T14:36:28.270Z",
  "id": "6097f36c4fb7c70010768b85"
}
```
* *stageAmount*: `3696780108975534166`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001450e0fe0568c5fe0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001450e0fe0568c5fe000000000000000000000000000000000000000000000000334d99ec3837705699582eb12ef2c9886918c9531ed076b5f732b0cd6d6b55b0122b4d5f37b5cf965c9ffa9467066d76aaa02fc7f9185b92d15c97cbaac2efe9c4385c911d398e5c4afbcf65c520532c761b37e70213e33eead178f43683e5bca952aace76c2da52000000000000000000000000000000000000000000000000000000000000001c3432d1530f34df57d8381ca88fa421e61201aca162824d7753fa5cdd2c4894b957a83cfd713d8d55edb09e1cda4938ce75953633738548f4a99db216b515eafc29554fc3d8a70b899433d99384133decac6e1de1f8051c6a9425c61721106105000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000bd38410000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001210a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000024cdc8eb4c680d878ea20000000000000000000000000000000000000000000024cddd4160d2df3b717e00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005336ccc4b1cde0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000003591956a9a2130b13880000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949774e7a426d595464685a53316c4d4759314c5455334f4441744f5756694e69316a4e6a4d3159325a695954646a4e54636966513d3d0000000000000000000000000000000000000000000000000000000000000003000000000000000000000000b2856de7cac918adf4bf19a349f795ef366ab878000000000000000000000000000000000000000000000000334d99ec383770560000000000000000000000000000000000000000000000001efcb8ee32ceaa5800000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x99582eb12ef2c9886918c9531ed076b5f732b0cd6d6b55b0122b4d5f37b5cf96",
      "signature": {
        "s": "0x4afbcf65c520532c761b37e70213e33eead178f43683e5bca952aace76c2da52",
        "r": "0x5c9ffa9467066d76aaa02fc7f9185b92d15c97cbaac2efe9c4385c911d398e5c",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x3432d1530f34df57d8381ca88fa421e61201aca162824d7753fa5cdd2c4894b9",
      "signature": {
        "s": "0x29554fc3d8a70b899433d99384133decac6e1de1f8051c6a9425c61721106105",
        "r": "0x57a83cfd713d8d55edb09e1cda4938ce75953633738548f4a99db216b515eafc",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "1463917260512478718",
    "total": "3696780108975534166"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1463917260512478718",
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
            "amount": "15810685504381600338824"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1463917260512478"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwNzBmYTdhZS1lMGY1LTU3ODAtOWViNi1jNjM1Y2ZiYTdjNTcifQ==",
    "nonce": 73994,
    "balances": {
      "current": "173801253667854585663138",
      "previous": "173802719049032358654334"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb2856de7cac918adf4bf19a349f795ef366ab878",
    "nonce": 3,
    "balances": {
      "current": "3696780108975534166",
      "previous": "2232862848463055448"
    }
  },
  "blockNumber": "12400705",
  "created": "2021-05-09T14:36:28.204Z",
  "updated": "2021-05-09T14:36:28.270Z",
  "id": "6097f36c4fb7c70010768b85"
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
0x0f200f9b000000000000000000000000000000000000000000000000334d99ec383770560000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `3696780108975534166`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`