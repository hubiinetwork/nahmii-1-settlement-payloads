# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x17fCFaC1306aa1752Fd8Dfe6e5cbF484C220FCFE`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000062b6dfa263ac94db00000000000000000000000000000000000000000000000000000000214ce36d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000214ce36d0000000000000000000000000000000000000000000000000000000309292f439bb5c5366e7c3ce4fa9ea1fa9c0c64c14d535008e4d877c518aa3e286f3f9471e186c3d020f46cb47d925e1e09a2636fcdab30c03fd96f731a609cc4091dc79411d4d415e297accc91199ea778c5bfac8fa8c6b3ed177634f8795715f8a3a630000000000000000000000000000000000000000000000000000000000000001b07215f603ba1b012470c8123b06db650b28f9173171f694e9ae2217281cfe1cfa078aa9c6ecc486c5752ab2b76698bd3b95fc939295fd78e193bacf0e13d128f0ade77f14a20a55c7ff1181bf5f4fd32e73b6ec2246b80dd6f90e45b092eda3b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3c2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003b95c8a7150dcb265fe2000000000000000000000000000000000000000000003b95c8a7150dec7bc9ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008865f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd24ecc63b2297cc870000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a466d4e7a497a4e4330774d7a55344c54566b597a67744f4459334f5330324e7a426a4d5745775a444e694e546b6966513d3d000000000000000000000000000000000000000000000000000000000000001f00000000000000000000000017fcfac1306aa1752fd8dfe6e5cbf484c220fcfe00000000000000000000000000000000000000000000000062b6dfa263ac94db00000000000000000000000000000000000000000000000062b6dfa2425fb16e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9bb5c5366e7c3ce4fa9ea1fa9c0c64c14d535008e4d877c518aa3e286f3f9471",
      "signature": {
        "s": "0x11d4d415e297accc91199ea778c5bfac8fa8c6b3ed177634f8795715f8a3a630",
        "r": "0xe186c3d020f46cb47d925e1e09a2636fcdab30c03fd96f731a609cc4091dc794",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x07215f603ba1b012470c8123b06db650b28f9173171f694e9ae2217281cfe1cf",
      "signature": {
        "s": "0x0ade77f14a20a55c7ff1181bf5f4fd32e73b6ec2246b80dd6f90e45b092eda3b",
        "r": "0xa078aa9c6ecc486c5752ab2b76698bd3b95fc939295fd78e193bacf0e13d128f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "558687085",
    "total": "13038595907"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "558687085",
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
            "amount": "27691223574075191839879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "558687"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjFmNzIzNC0wMzU4LTVkYzgtODY3OS02NzBjMWEwZDNiNTkifQ==",
    "nonce": 111554,
    "balances": {
      "current": "281382645904569474113506",
      "previous": "281382645904570033359278"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x17fcfac1306aa1752fd8dfe6e5cbf484c220fcfe",
    "nonce": 31,
    "balances": {
      "current": "7113118550028227803",
      "previous": "7113118549469540718"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:58:55.941Z",
  "updated": "2022-05-04T08:58:56.023Z",
  "id": "6272404fbbd75600116d06c8"
}
```
* *stageAmount*: `7113118550028227803`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000214ce36d0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000220000000000000000000000000000000000000000000000000000000000000046000000000000000000000000000000000000000000000000000000000214ce36d0000000000000000000000000000000000000000000000000000000309292f439bb5c5366e7c3ce4fa9ea1fa9c0c64c14d535008e4d877c518aa3e286f3f9471e186c3d020f46cb47d925e1e09a2636fcdab30c03fd96f731a609cc4091dc79411d4d415e297accc91199ea778c5bfac8fa8c6b3ed177634f8795715f8a3a630000000000000000000000000000000000000000000000000000000000000001b07215f603ba1b012470c8123b06db650b28f9173171f694e9ae2217281cfe1cfa078aa9c6ecc486c5752ab2b76698bd3b95fc939295fd78e193bacf0e13d128f0ade77f14a20a55c7ff1181bf5f4fd32e73b6ec2246b80dd6f90e45b092eda3b000000000000000000000000000000000000000000000000000000000000001c0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b3c2000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000003b95c8a7150dcb265fe2000000000000000000000000000000000000000000003b95c8a7150dec7bc9ae00000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e0000000000000000000000000000000000000000000000000000000000008865f0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd24ecc63b2297cc870000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931596a466d4e7a497a4e4330774d7a55344c54566b597a67744f4459334f5330324e7a426a4d5745775a444e694e546b6966513d3d000000000000000000000000000000000000000000000000000000000000001f00000000000000000000000017fcfac1306aa1752fd8dfe6e5cbf484c220fcfe00000000000000000000000000000000000000000000000062b6dfa263ac94db00000000000000000000000000000000000000000000000062b6dfa2425fb16e00000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9bb5c5366e7c3ce4fa9ea1fa9c0c64c14d535008e4d877c518aa3e286f3f9471",
      "signature": {
        "s": "0x11d4d415e297accc91199ea778c5bfac8fa8c6b3ed177634f8795715f8a3a630",
        "r": "0xe186c3d020f46cb47d925e1e09a2636fcdab30c03fd96f731a609cc4091dc794",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x07215f603ba1b012470c8123b06db650b28f9173171f694e9ae2217281cfe1cf",
      "signature": {
        "s": "0x0ade77f14a20a55c7ff1181bf5f4fd32e73b6ec2246b80dd6f90e45b092eda3b",
        "r": "0xa078aa9c6ecc486c5752ab2b76698bd3b95fc939295fd78e193bacf0e13d128f",
        "v": 28
      }
    }
  },
  "transfers": {
    "single": "558687085",
    "total": "13038595907"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "558687085",
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
            "amount": "27691223574075191839879"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "558687"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YjFmNzIzNC0wMzU4LTVkYzgtODY3OS02NzBjMWEwZDNiNTkifQ==",
    "nonce": 111554,
    "balances": {
      "current": "281382645904569474113506",
      "previous": "281382645904570033359278"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x17fcfac1306aa1752fd8dfe6e5cbf484c220fcfe",
    "nonce": 31,
    "balances": {
      "current": "7113118550028227803",
      "previous": "7113118549469540718"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:58:55.941Z",
  "updated": "2022-05-04T08:58:56.023Z",
  "id": "6272404fbbd75600116d06c8"
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
0x0f200f9b00000000000000000000000000000000000000000000000062b6dfa263ac94db0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `7113118550028227803`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`