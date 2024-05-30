# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x98e50b89A8dbBe2Cbb68835660C636b016459dC9`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000020acd9028a80d0a6b2000000000000000000000000000000000000000000000000000000077067363b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000077067363b00000000000000000000000000000000000000000000000e303dc4d21230de420564765b5963ace8dec4dbe86bf54c70881e390f81b703b8f263218cc35d9f0e03b80e174d76a54a4b43b2c862af63b8cb5116234eb1bd4357eef483a71757fa45c667b2c6f896119b2544fcc88d0a5ec29d9e93c4b72a6ea624c9995933832d000000000000000000000000000000000000000000000000000000000000001c6b593b2b975ce617e4b09d443f0bca3e137c474b51d7ebd896ce4b597b3e35d5f5aa94223ee3b7ee7f43fcabc174d42cbea18d244eea17164a041b5cd71f08f9186d9caf2321d5c02ffdad9b0dbc3d4845fd8ea2b013d091b4c58917d2a16067000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad88000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000967f92c3e651b35a502700000000000000000000000000000000000000000000967f92c3e65925a90d5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001e786f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e4c973ed93a7df190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596a6c6c4e32466a4d43316b5a5468694c54557a596a6b74596a637a4e79303459324e6a4d544e69597a67794e6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098e50b89a8dbbe2cbb68835660c636b016459dc9000000000000000000000000000000000000000000000020acd9028a80d0a6b2000000000000000000000000000000000000000000000020acd902831069707700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0564765b5963ace8dec4dbe86bf54c70881e390f81b703b8f263218cc35d9f0e",
      "signature": {
        "s": "0x45c667b2c6f896119b2544fcc88d0a5ec29d9e93c4b72a6ea624c9995933832d",
        "r": "0x03b80e174d76a54a4b43b2c862af63b8cb5116234eb1bd4357eef483a71757fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6b593b2b975ce617e4b09d443f0bca3e137c474b51d7ebd896ce4b597b3e35d5",
      "signature": {
        "s": "0x186d9caf2321d5c02ffdad9b0dbc3d4845fd8ea2b013d091b4c58917d2a16067",
        "r": "0xf5aa94223ee3b7ee7f43fcabc174d42cbea18d244eea17164a041b5cd71f08f9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31950583355",
    "total": "261730567925860982338"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31950583355",
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
            "amount": "27262326832244195843865"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31950583"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwYjllN2FjMC1kZThiLTUzYjktYjczNy04Y2NjMTNiYzgyNjkifQ==",
    "nonce": 109960,
    "balances": {
      "current": "710708284477396466946087",
      "previous": "710708284477428449480025"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98e50b89a8dbbe2cbb68835660c636b016459dc9",
    "nonce": 46,
    "balances": {
      "current": "602750799397065369266",
      "previous": "602750799365114785911"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:50:49.325Z",
  "updated": "2022-05-04T08:50:49.393Z",
  "id": "62723e697832e20011830b1b"
}
```
* *stageAmount*: `602750799397065369266`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000000000077067363b0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000077067363b00000000000000000000000000000000000000000000000e303dc4d21230de420564765b5963ace8dec4dbe86bf54c70881e390f81b703b8f263218cc35d9f0e03b80e174d76a54a4b43b2c862af63b8cb5116234eb1bd4357eef483a71757fa45c667b2c6f896119b2544fcc88d0a5ec29d9e93c4b72a6ea624c9995933832d000000000000000000000000000000000000000000000000000000000000001c6b593b2b975ce617e4b09d443f0bca3e137c474b51d7ebd896ce4b597b3e35d5f5aa94223ee3b7ee7f43fcabc174d42cbea18d244eea17164a041b5cd71f08f9186d9caf2321d5c02ffdad9b0dbc3d4845fd8ea2b013d091b4c58917d2a16067000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074c50000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ad88000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e8400000000000000000000000000000000000000000000967f92c3e651b35a502700000000000000000000000000000000000000000000967f92c3e65925a90d5900000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000000000001e786f70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5e4c973ed93a7df190000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694977596a6c6c4e32466a4d43316b5a5468694c54557a596a6b74596a637a4e79303459324e6a4d544e69597a67794e6a6b6966513d3d000000000000000000000000000000000000000000000000000000000000002e00000000000000000000000098e50b89a8dbbe2cbb68835660c636b016459dc9000000000000000000000000000000000000000000000020acd9028a80d0a6b2000000000000000000000000000000000000000000000020acd902831069707700000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x0564765b5963ace8dec4dbe86bf54c70881e390f81b703b8f263218cc35d9f0e",
      "signature": {
        "s": "0x45c667b2c6f896119b2544fcc88d0a5ec29d9e93c4b72a6ea624c9995933832d",
        "r": "0x03b80e174d76a54a4b43b2c862af63b8cb5116234eb1bd4357eef483a71757fa",
        "v": 28
      }
    },
    "operator": {
      "hash": "0x6b593b2b975ce617e4b09d443f0bca3e137c474b51d7ebd896ce4b597b3e35d5",
      "signature": {
        "s": "0x186d9caf2321d5c02ffdad9b0dbc3d4845fd8ea2b013d091b4c58917d2a16067",
        "r": "0xf5aa94223ee3b7ee7f43fcabc174d42cbea18d244eea17164a041b5cd71f08f9",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "31950583355",
    "total": "261730567925860982338"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "31950583355",
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
            "amount": "27262326832244195843865"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "31950583"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiIwYjllN2FjMC1kZThiLTUzYjktYjczNy04Y2NjMTNiYzgyNjkifQ==",
    "nonce": 109960,
    "balances": {
      "current": "710708284477396466946087",
      "previous": "710708284477428449480025"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x98e50b89a8dbbe2cbb68835660c636b016459dc9",
    "nonce": 46,
    "balances": {
      "current": "602750799397065369266",
      "previous": "602750799365114785911"
    }
  },
  "blockNumber": "14709957",
  "created": "2022-05-04T08:50:49.325Z",
  "updated": "2022-05-04T08:50:49.393Z",
  "id": "62723e697832e20011830b1b"
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
0x0f200f9b000000000000000000000000000000000000000000000020acd9028a80d0a6b20000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `602750799397065369266`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`