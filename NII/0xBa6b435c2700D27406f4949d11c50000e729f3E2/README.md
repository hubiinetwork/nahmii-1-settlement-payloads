# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xBa6b435c2700D27406f4949d11c50000e729f3E2`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000003ae129ff1cfebedd70000000000000000000000000000000000000000000000001655e2001a0555c70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001655e2001a0555c700000000000000000000000000000000000000000000000272c159e92cf6ef24fd0262f25131fc5d8ff48a6126b4cf9da8d20b0df769785968b5d5b653c48315b16bb92c292ac56e70b7495c79ddc4533fbdf665278a02bea75e9aebf94878633c9933f03e8570220d250c3902b65661a3913440347df2943143b2b0b458506f000000000000000000000000000000000000000000000000000000000000001b143c0f692a49dde412d5a57d35139cab08b8a2b1d49342cc2b8c9bc04f9ed9f7830c6833657a13a71872c002e436dd74149fe3c5d13bf60cb33f520f50622dc037b2c0fe1d303a038f4915d565bd367faa0fe284978c4229a2e9539948b2a4a6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aebc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095e26d8aaf91ef715e970000000000000000000000000000000000000000000095e283e64959347f69f400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005b7c72b08b5960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60cf9d87d7f22dbe70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a6c6c4f474a6d4d79316a4f4446694c54566a4d7a6b744f545a6d595331684e6a55774f4445304e6a41314d47516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ba6b435c2700d27406f4949d11c50000e729f3e2000000000000000000000000000000000000000000000003ae129ff1cfebedd700000000000000000000000000000000000000000000000397bcbdf1b5e6981000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfd0262f25131fc5d8ff48a6126b4cf9da8d20b0df769785968b5d5b653c48315",
      "signature": {
        "s": "0x3c9933f03e8570220d250c3902b65661a3913440347df2943143b2b0b458506f",
        "r": "0xb16bb92c292ac56e70b7495c79ddc4533fbdf665278a02bea75e9aebf9487863",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x143c0f692a49dde412d5a57d35139cab08b8a2b1d49342cc2b8c9bc04f9ed9f7",
      "signature": {
        "s": "0x37b2c0fe1d303a038f4915d565bd367faa0fe284978c4229a2e9539948b2a4a6",
        "r": "0x830c6833657a13a71872c002e436dd74149fe3c5d13bf60cb33f520f50622dc0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1609440931919254983",
    "total": "45162477396264677156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1609440931919254983",
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
            "amount": "27265222757373888879591"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1609440931919254"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YjllOGJmMy1jODFiLTVjMzktOTZmYS1hNjUwODE0NjA1MGQifQ==",
    "nonce": 110268,
    "balances": {
      "current": "707809463422573738024599",
      "previous": "707811074472946589198836"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xba6b435c2700d27406f4949d11c50000e729f3e2",
    "nonce": 46,
    "balances": {
      "current": "67883495994233187799",
      "previous": "66274055062313932816"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:24.706Z",
  "updated": "2022-05-04T08:52:24.914Z",
  "id": "62723ec83592fd001130b4a3"
}
```
* *stageAmount*: `67883495994233187799`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000006000000000000000000000000000000000000000000000000001655e2001a0555c70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000022000000000000000000000000000000000000000000000000000000000000004600000000000000000000000000000000000000000000000001655e2001a0555c700000000000000000000000000000000000000000000000272c159e92cf6ef24fd0262f25131fc5d8ff48a6126b4cf9da8d20b0df769785968b5d5b653c48315b16bb92c292ac56e70b7495c79ddc4533fbdf665278a02bea75e9aebf94878633c9933f03e8570220d250c3902b65661a3913440347df2943143b2b0b458506f000000000000000000000000000000000000000000000000000000000000001b143c0f692a49dde412d5a57d35139cab08b8a2b1d49342cc2b8c9bc04f9ed9f7830c6833657a13a71872c002e436dd74149fe3c5d13bf60cb33f520f50622dc037b2c0fe1d303a038f4915d565bd367faa0fe284978c4229a2e9539948b2a4a6000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074cd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001aebc000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000095e26d8aaf91ef715e970000000000000000000000000000000000000000000095e283e64959347f69f400000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000005b7c72b08b5960000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c60cf9d87d7f22dbe70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694935596a6c6c4f474a6d4d79316a4f4446694c54566a4d7a6b744f545a6d595331684e6a55774f4445304e6a41314d47516966513d3d000000000000000000000000000000000000000000000000000000000000002e000000000000000000000000ba6b435c2700d27406f4949d11c50000e729f3e2000000000000000000000000000000000000000000000003ae129ff1cfebedd700000000000000000000000000000000000000000000000397bcbdf1b5e6981000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0xfd0262f25131fc5d8ff48a6126b4cf9da8d20b0df769785968b5d5b653c48315",
      "signature": {
        "s": "0x3c9933f03e8570220d250c3902b65661a3913440347df2943143b2b0b458506f",
        "r": "0xb16bb92c292ac56e70b7495c79ddc4533fbdf665278a02bea75e9aebf9487863",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x143c0f692a49dde412d5a57d35139cab08b8a2b1d49342cc2b8c9bc04f9ed9f7",
      "signature": {
        "s": "0x37b2c0fe1d303a038f4915d565bd367faa0fe284978c4229a2e9539948b2a4a6",
        "r": "0x830c6833657a13a71872c002e436dd74149fe3c5d13bf60cb33f520f50622dc0",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "1609440931919254983",
    "total": "45162477396264677156"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "1609440931919254983",
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
            "amount": "27265222757373888879591"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "1609440931919254"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI5YjllOGJmMy1jODFiLTVjMzktOTZmYS1hNjUwODE0NjA1MGQifQ==",
    "nonce": 110268,
    "balances": {
      "current": "707809463422573738024599",
      "previous": "707811074472946589198836"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xba6b435c2700d27406f4949d11c50000e729f3e2",
    "nonce": 46,
    "balances": {
      "current": "67883495994233187799",
      "previous": "66274055062313932816"
    }
  },
  "blockNumber": "14709965",
  "created": "2022-05-04T08:52:24.706Z",
  "updated": "2022-05-04T08:52:24.914Z",
  "id": "62723ec83592fd001130b4a3"
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
0x0f200f9b000000000000000000000000000000000000000000000003ae129ff1cfebedd70000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `67883495994233187799`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`