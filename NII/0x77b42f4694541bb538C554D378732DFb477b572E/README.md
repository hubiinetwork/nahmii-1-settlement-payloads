# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x77b42f4694541bb538C554D378732DFb477b572E`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000009e8556d64fe6e91af0000000000000000000000000000000000000000000000009bf570ffd0b053790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000009bf570ffd0b05379000000000000000000000000000000000000000000000009e8556d64fe6e91af708dc6a881cdd85cba35e26253a2b22a729f836acbbc4eb6d3ed0424e2656487d3e7ec36c49023b6483972e6b0339f9a650f8e018bdf0b5e33cdc5d3049a16134341bdfc74cd5dcb72cc11b1a726229908a7721d4cbd99251096800364c24281000000000000000000000000000000000000000000000000000000000000001b5f833e3bc3b617d1270104193533a82c7c0baf5c9c1cff3e1c84195ebc6c9c9e62e7a0904c7928db6c7639cf227fdbe1fc6fd28c823df07e04747ab21a82e21b00e9140964945b457c129ea969c280dc959fdb396782be87fc153de831bbeb00000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b55a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003440401c80d8c9b8a079000000000000000000000000000000000000000000003440dc39dec254bb0c9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000027ece9ba5218a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df0517e0b880b550e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f5459794e47466a5a4330304d4441794c54566b5957497459574d305969316a4f5467794f4749324d6a466c4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000077b42f4694541bb538c554d378732dfb477b572e000000000000000000000000000000000000000000000009e8556d64fe6e91af0000000000000000000000000000000000000000000000094c5ffc652dbe3e3600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x708dc6a881cdd85cba35e26253a2b22a729f836acbbc4eb6d3ed0424e2656487",
      "signature": {
        "s": "0x4341bdfc74cd5dcb72cc11b1a726229908a7721d4cbd99251096800364c24281",
        "r": "0xd3e7ec36c49023b6483972e6b0339f9a650f8e018bdf0b5e33cdc5d3049a1613",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5f833e3bc3b617d1270104193533a82c7c0baf5c9c1cff3e1c84195ebc6c9c9e",
      "signature": {
        "s": "0x00e9140964945b457c129ea969c280dc959fdb396782be87fc153de831bbeb00",
        "r": "0x62e7a0904c7928db6c7639cf227fdbe1fc6fd28c823df07e04747ab21a82e21b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11238012689193128825",
    "total": "182762104133738467759"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11238012689193128825",
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
            "amount": "27725823351763148034278"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11238012689193128"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5OTYyNGFjZC00MDAyLTVkYWItYWM0Yi1jOTgyOGI2MjFlMjgifQ==",
    "nonce": 111962,
    "balances": {
      "current": "246748268438925323313273",
      "previous": "246759517689627205635226"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77b42f4694541bb538c554d378732dfb477b572e",
    "nonce": 13,
    "balances": {
      "current": "182762104133738467759",
      "previous": "171524091444545338934"
    }
  },
  "blockNumber": "14709985",
  "created": "2022-05-04T09:01:16.196Z",
  "updated": "2022-05-04T09:01:16.295Z",
  "id": "627240dcbbd75600116d074e"
}
```
* *stageAmount*: `182762104133738467759`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000009bf570ffd0b053790000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000009bf570ffd0b05379000000000000000000000000000000000000000000000009e8556d64fe6e91af708dc6a881cdd85cba35e26253a2b22a729f836acbbc4eb6d3ed0424e2656487d3e7ec36c49023b6483972e6b0339f9a650f8e018bdf0b5e33cdc5d3049a16134341bdfc74cd5dcb72cc11b1a726229908a7721d4cbd99251096800364c24281000000000000000000000000000000000000000000000000000000000000001b5f833e3bc3b617d1270104193533a82c7c0baf5c9c1cff3e1c84195ebc6c9c9e62e7a0904c7928db6c7639cf227fdbe1fc6fd28c823df07e04747ab21a82e21b00e9140964945b457c129ea969c280dc959fdb396782be87fc153de831bbeb00000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074e10000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b55a000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003440401c80d8c9b8a079000000000000000000000000000000000000000000003440dc39dec254bb0c9a00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000027ece9ba5218a80000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005df0517e0b880b550e60000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f6949354f5459794e47466a5a4330304d4441794c54566b5957497459574d305969316a4f5467794f4749324d6a466c4d6a676966513d3d000000000000000000000000000000000000000000000000000000000000000d00000000000000000000000077b42f4694541bb538c554d378732dfb477b572e000000000000000000000000000000000000000000000009e8556d64fe6e91af0000000000000000000000000000000000000000000000094c5ffc652dbe3e3600000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x708dc6a881cdd85cba35e26253a2b22a729f836acbbc4eb6d3ed0424e2656487",
      "signature": {
        "s": "0x4341bdfc74cd5dcb72cc11b1a726229908a7721d4cbd99251096800364c24281",
        "r": "0xd3e7ec36c49023b6483972e6b0339f9a650f8e018bdf0b5e33cdc5d3049a1613",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x5f833e3bc3b617d1270104193533a82c7c0baf5c9c1cff3e1c84195ebc6c9c9e",
      "signature": {
        "s": "0x00e9140964945b457c129ea969c280dc959fdb396782be87fc153de831bbeb00",
        "r": "0x62e7a0904c7928db6c7639cf227fdbe1fc6fd28c823df07e04747ab21a82e21b",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "11238012689193128825",
    "total": "182762104133738467759"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "11238012689193128825",
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
            "amount": "27725823351763148034278"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "11238012689193128"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5OTYyNGFjZC00MDAyLTVkYWItYWM0Yi1jOTgyOGI2MjFlMjgifQ==",
    "nonce": 111962,
    "balances": {
      "current": "246748268438925323313273",
      "previous": "246759517689627205635226"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x77b42f4694541bb538c554d378732dfb477b572e",
    "nonce": 13,
    "balances": {
      "current": "182762104133738467759",
      "previous": "171524091444545338934"
    }
  },
  "blockNumber": "14709985",
  "created": "2022-05-04T09:01:16.196Z",
  "updated": "2022-05-04T09:01:16.295Z",
  "id": "627240dcbbd75600116d074e"
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
0x0f200f9b000000000000000000000000000000000000000000000009e8556d64fe6e91af0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `182762104133738467759`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`