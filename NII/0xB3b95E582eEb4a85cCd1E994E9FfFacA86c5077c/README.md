# Settlement of NII
This document presents the recommended steps in order to settle the Nahmii 1
balance of NII of account `0xB3b95E582eEb4a85cCd1E994E9FfFacA86c5077c`.

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
0x4d3d826c0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000dbdc20aadf714e5900000000000000000000000000000000000000000000000000000000346619340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003466193400000000000000000000000000000000000000000000000000000004c6e0c8d31cb306adf57b3830f459771313328a9baba270d1a9b3fb997a6775fc77a0e57000e0ecfa78687014899addc3aa5e3b2ff7491d924e646dda69ea237ecd744189246862893eb1c3ba77376cb32737efa3a5afc8e7fd106c920050bfbeda60f928000000000000000000000000000000000000000000000000000000000000001cf6713c910bf01243fb8a8e1beee3964a78abdc92db94528f3b08f1fa100268b88da2c716e03f34bc89333296a1695b4003fe717df0e772e59cec4177dfc4988861ce04ed5eac39471821645ede53b0064df428fcbe711e15809670c4c48669f0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b443000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039c4e82808351c8dd53c0000000000000000000000000000000000000000000039c4e82808355101587200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000d6a020000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd9bd0837e9cc1e4730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931595755314d6d557a4d7930344e546b344c54566a4d6d51744f54457a5969316a4e54513159574d334f575132596d596966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000b3b95e582eeb4a85ccd1e994e9fffaca86c5077c000000000000000000000000000000000000000000000000dbdc20aadf714e59000000000000000000000000000000000000000000000000dbdc20aaab0b352500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d00000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1cb306adf57b3830f459771313328a9baba270d1a9b3fb997a6775fc77a0e570",
      "signature": {
        "s": "0x246862893eb1c3ba77376cb32737efa3a5afc8e7fd106c920050bfbeda60f928",
        "r": "0x00e0ecfa78687014899addc3aa5e3b2ff7491d924e646dda69ea237ecd744189",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf6713c910bf01243fb8a8e1beee3964a78abdc92db94528f3b08f1fa100268b8",
      "signature": {
        "s": "0x61ce04ed5eac39471821645ede53b0064df428fcbe711e15809670c4c48669f0",
        "r": "0x8da2c716e03f34bc89333296a1695b4003fe717df0e772e59cec4177dfc49888",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "879106356",
    "total": "20516489427"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "879106356",
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
            "amount": "27699790473088890692723"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "879106"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YWU1MmUzMy04NTk4LTVjMmQtOTEzYi1jNTQ1YWM3OWQ2YmYifQ==",
    "nonce": 111683,
    "balances": {
      "current": "272807179991856922350908",
      "previous": "272807179991857802336370"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3b95e582eeb4a85ccd1e994e9fffaca86c5077c",
    "nonce": 29,
    "balances": {
      "current": "15842573507447836249",
      "previous": "15842573506568729893"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:36.755Z",
  "updated": "2022-05-04T08:59:36.820Z",
  "id": "627240787832e20011830d5c"
}
```
* *stageAmount*: `15842573507447836249`
### Step 2
#### Contract
*DriipSettlementByPayment* ([0xd2600fd59786b44c4869066018870aa33417f8f2](https://etherscan.io/address/0xd2600fd59786b44c4869066018870aa33417f8f2))
#### Method name
*settlePayment*
#### Method payload
```
0xdd3056ca0000000000000000000000000000000000000000000000000000000000000040000000000000000000000000000000000000000000000000000000000000060000000000000000000000000000000000000000000000000000000000346619340000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe52000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000002200000000000000000000000000000000000000000000000000000000000000460000000000000000000000000000000000000000000000000000000003466193400000000000000000000000000000000000000000000000000000004c6e0c8d31cb306adf57b3830f459771313328a9baba270d1a9b3fb997a6775fc77a0e57000e0ecfa78687014899addc3aa5e3b2ff7491d924e646dda69ea237ecd744189246862893eb1c3ba77376cb32737efa3a5afc8e7fd106c920050bfbeda60f928000000000000000000000000000000000000000000000000000000000000001cf6713c910bf01243fb8a8e1beee3964a78abdc92db94528f3b08f1fa100268b88da2c716e03f34bc89333296a1695b4003fe717df0e772e59cec4177dfc4988861ce04ed5eac39471821645ede53b0064df428fcbe711e15809670c4c48669f0000000000000000000000000000000000000000000000000000000000000001b0000000000000000000000000000000000000000000000000000000000e074dd0000000000000000000000000000000000000000000000000000000000000540000000000000000000000000000000000000000000000000000000000001b443000000000000000000000000e8575e787e28bcb0ee3046605f795bf883e82e840000000000000000000000000000000000000000000039c4e82808351c8dd53c0000000000000000000000000000000000000000000039c4e82808355101587200000000000000000000000000000000000000000000000000000000000000c000000000000000000000000000000000000000000000000000000000000001e000000000000000000000000000000000000000000000000000000000000d6a020000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe5200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000005dd9bd0837e9cc1e4730000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004065794a795a5759694f694931595755314d6d557a4d7930344e546b344c54566a4d6d51744f54457a5969316a4e54513159574d334f575132596d596966513d3d000000000000000000000000000000000000000000000000000000000000001d000000000000000000000000b3b95e582eeb4a85ccd1e994e9fffaca86c5077c000000000000000000000000000000000000000000000000dbdc20aadf714e59000000000000000000000000000000000000000000000000dbdc20aaab0b352500000000000000000000000000000000000000000000000000000000000000a0000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000000000046533303d0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *payment*: 
```
{
  "seals": {
    "wallet": {
      "hash": "0x1cb306adf57b3830f459771313328a9baba270d1a9b3fb997a6775fc77a0e570",
      "signature": {
        "s": "0x246862893eb1c3ba77376cb32737efa3a5afc8e7fd106c920050bfbeda60f928",
        "r": "0x00e0ecfa78687014899addc3aa5e3b2ff7491d924e646dda69ea237ecd744189",
        "v": 28
      }
    },
    "operator": {
      "hash": "0xf6713c910bf01243fb8a8e1beee3964a78abdc92db94528f3b08f1fa100268b8",
      "signature": {
        "s": "0x61ce04ed5eac39471821645ede53b0064df428fcbe711e15809670c4c48669f0",
        "r": "0x8da2c716e03f34bc89333296a1695b4003fe717df0e772e59cec4177dfc49888",
        "v": 27
      }
    }
  },
  "transfers": {
    "single": "879106356",
    "total": "20516489427"
  },
  "operator": {
    "id": 0,
    "data": "e30="
  },
  "amount": "879106356",
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
            "amount": "27699790473088890692723"
          }
        }
      ],
      "single": {
        "currency": {
          "ct": "0x7c8155909cd385f120a56ef90728dd50f9ccbe52",
          "id": "0"
        },
        "amount": "879106"
      }
    },
    "wallet": "0xe8575e787e28bcb0ee3046605f795bf883e82e84",
    "data": "eyJyZWYiOiI1YWU1MmUzMy04NTk4LTVjMmQtOTEzYi1jNTQ1YWM3OWQ2YmYifQ==",
    "nonce": 111683,
    "balances": {
      "current": "272807179991856922350908",
      "previous": "272807179991857802336370"
    }
  },
  "recipient": {
    "fees": {
      "total": []
    },
    "wallet": "0xb3b95e582eeb4a85ccd1e994e9fffaca86c5077c",
    "nonce": 29,
    "balances": {
      "current": "15842573507447836249",
      "previous": "15842573506568729893"
    }
  },
  "blockNumber": "14709981",
  "created": "2022-05-04T08:59:36.755Z",
  "updated": "2022-05-04T08:59:36.820Z",
  "id": "627240787832e20011830d5c"
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
0x0f200f9b000000000000000000000000000000000000000000000000dbdc20aadf714e590000000000000000000000007c8155909cd385f120a56ef90728dd50f9ccbe520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000000000000000000054552433230000000000000000000000000000000000000000000000000000000
```
#### Encode method args
* *value*: `15842573507447836249`
* *currencyCt*: `0x7c8155909cd385F120A56eF90728dD50F9CcbE52`
* *currencyId*: `0`
* *standard*: `ERC20`