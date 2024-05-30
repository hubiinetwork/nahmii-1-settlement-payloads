# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0x7A5C4051838A77605b79Ec205273b0Ff81d583Cf`.

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
0x4d3d826c000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000b6d6ea510537710de000000000000000000000000000000000000000000000000455bd315a4af135e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bd315a4af135e0000000000000000000000000000000000000000000000079a45b3608ac252949683480e5dbe742405b5a2a78752e818afd3c3d3437aaaaf2301d9b5ec182949d1b4811fbffec255e5053f3b0d6bc2fee7376bdd49926afc45818dbde3a7df7467c5d3563d0083ee74d5b33634c3a34a8919707da1c52bc3117b79185fbd4039000000000000000000000000000000000000000000000000000000000000001b81d73c4dbdd9260be75e0e0b39b95e13f68896145ceb22ba2c9d87085b6b55b32a71b6c8fcbb0a1b3d930f424af17dd3589e6722360df3ab28c7373e1645d60e610480703b79402892761b57743965368f5d92e4dc0d08cc6c4ee4caacb676a1000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae57000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009629f1ff751440373ad200000000000000000000000000000000000000000000962a376d09a79c9dc6c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17db7b778980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5faaf902c4ba6a0480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a474532596d4e6a4e6930325954517a4c5455314d575574596a466d4f5330324d5446694e4468684e47566b4f44556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007a5c4051838a77605b79ec205273b0ff81d583cf00000000000000000000000000000000000000000000000b6d6ea510537710de00000000000000000000000000000000000000000000000b2812d1faaec7fd8000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9683480e5dbe742405b5a2a78752e818afd3c3d3437aaaaf2301d9b5ec182949",
      "signature": {
        "s": "0x67c5d3563d0083ee74d5b33634c3a34a8919707da1c52bc3117b79185fbd4039",
        "r": "0xd1b4811fbffec255e5053f3b0d6bc2fee7376bdd49926afc45818dbde3a7df74",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x81d73c4dbdd9260be75e0e0b39b95e13f68896145ceb22ba2c9d87085b6b55b3",
      "signature": {
        "s": "0x610480703b79402892761b57743965368f5d92e4dc0d08cc6c4ee4caacb676a1",
        "r": "0x2a71b6c8fcbb0a1b3d930f424af17dd3589e6722360df3ab28c7373e1645d60e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4997820301408408414",
    "total": "140243696998427021972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997820301408408414",
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
            "amount": "27263904812019336257608"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997820301408408"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZGE2YmNjNi02YTQzLTU1MWUtYjFmOS02MTFiNDhhNGVkODUifQ==",
    "nonce": 110167,
    "balances": {
      "current": "709128726722480912677586",
      "previous": "709133729540602622494408"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a5c4051838a77605b79ec205273b0ff81d583cf",
    "nonce": 46,
    "balances": {
      "current": "210799606297915756766",
      "previous": "205801785996507348352"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:52.924Z",
  "updated": "2022-05-04T08:51:53.019Z",
  "id": "62723ea8bbd75600116d0508"
}
```
* *stageAmount*: `210799606297915756766`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca00000000000000000000000000000000000000000000000000000000000000400000000000000000000000000000000000000000000000000000000000000600000000000000000000000000000000000000000000000000455bd315a4af135e0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000455bd315a4af135e0000000000000000000000000000000000000000000000079a45b3608ac252949683480e5dbe742405b5a2a78752e818afd3c3d3437aaaaf2301d9b5ec182949d1b4811fbffec255e5053f3b0d6bc2fee7376bdd49926afc45818dbde3a7df7467c5d3563d0083ee74d5b33634c3a34a8919707da1c52bc3117b79185fbd4039000000000000000000000000000000000000000000000000000000000000001b81d73c4dbdd9260be75e0e0b39b95e13f68896145ceb22ba2c9d87085b6b55b32a71b6c8fcbb0a1b3d930f424af17dd3589e6722360df3ab28c7373e1645d60e610480703b79402892761b57743965368f5d92e4dc0d08cc6c4ee4caacb676a1000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074ca0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001ae57000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e84000000000000000000000000000000000000000000009629f1ff751440373ad200000000000000000000000000000000000000000000962a376d09a79c9dc6c800000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e00000000000000000000000000000000000000000000000000011c17db7b778980000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005c5faaf902c4ba6a0480000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694a6d5a474532596d4e6a4e6930325954517a4c5455314d575574596a466d4f5330324d5446694e4468684e47566b4f44556966513d3d000000000000000000000000000000000000000000000000000000000000002e0000000000000000000000007a5c4051838a77605b79ec205273b0ff81d583cf00000000000000000000000000000000000000000000000b6d6ea510537710de00000000000000000000000000000000000000000000000b2812d1faaec7fd8000000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x9683480e5dbe742405b5a2a78752e818afd3c3d3437aaaaf2301d9b5ec182949",
      "signature": {
        "s": "0x67c5d3563d0083ee74d5b33634c3a34a8919707da1c52bc3117b79185fbd4039",
        "r": "0xd1b4811fbffec255e5053f3b0d6bc2fee7376bdd49926afc45818dbde3a7df74",
        "v": 27
      }
    },
    "operator": {
      "hash": "0x81d73c4dbdd9260be75e0e0b39b95e13f68896145ceb22ba2c9d87085b6b55b3",
      "signature": {
        "s": "0x610480703b79402892761b57743965368f5d92e4dc0d08cc6c4ee4caacb676a1",
        "r": "0x2a71b6c8fcbb0a1b3d930f424af17dd3589e6722360df3ab28c7373e1645d60e",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "4997820301408408414",
    "total": "140243696998427021972"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "4997820301408408414",
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
            "amount": "27263904812019336257608"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "4997820301408408"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiJmZGE2YmNjNi02YTQzLTU1MWUtYjFmOS02MTFiNDhhNGVkODUifQ==",
    "nonce": 110167,
    "balances": {
      "current": "709128726722480912677586",
      "previous": "709133729540602622494408"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0x7a5c4051838a77605b79ec205273b0ff81d583cf",
    "nonce": 46,
    "balances": {
      "current": "210799606297915756766",
      "previous": "205801785996507348352"
    }
  },
  "blockNumber": "14709962",
  "created": "2022-05-04T08:51:52.924Z",
  "updated": "2022-05-04T08:51:53.019Z",
  "id": "62723ea8bbd75600116d0508"
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
0x0f200f9b00000000000000000000000000000000000000000000000b6d6ea510537710de0000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `210799606297915756766`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`